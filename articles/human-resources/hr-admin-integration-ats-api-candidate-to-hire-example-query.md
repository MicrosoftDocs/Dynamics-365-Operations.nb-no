---
title: Eksempelspørring for Kandidat for ansettelse
description: Dette emnet inneholder en eksempelspørring for Kandidat for ansettelse-enheten i Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2fc08586914fd3815b0da062f24d83ac550302f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467631"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="008e9-103">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="008e9-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="008e9-104">Dette emnet inneholder en eksempelspørring for Kandidat for ansettelse-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="008e9-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="008e9-105">Dette emnet gir et eksempel på hvordan du kan bruke *dybdeinnlegg* til å opprette alle detaljene til en ny kandidatpost i én enkelt API-operasjon.</span><span class="sxs-lookup"><span data-stu-id="008e9-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="008e9-106">Hvis du vil ha mer informasjon om dybdeinnlegg, kan du se [Opprette relaterte enhetsposter i én operasjon](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="008e9-106">For more information about deep inserts, see [Create related entity records in one operation](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="008e9-107">Enheten **mshr_hcmcandidatetohireentity** er unik på grunn av relasjonen til enheten **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="008e9-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="008e9-108">Mange av egenskapene i **mshr_hcmcandidatetohireentity** (for eksempel **mshr_firstname**, **mshr_lastname** og **mshr_birthdate**) avledes fra posten **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="008e9-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="008e9-109">Hvis du posterer en ny kandidatpost til **mshr_hcmcandidatetohireentity** uten å bruke dybdeinnlegg, kan du definere verdier for disse egenskapene direkte i posten **mshr_hcmcandidatetohireentity**.</span><span class="sxs-lookup"><span data-stu-id="008e9-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="008e9-110">Den tilknyttede **mshr_dirpersonentity**-posten opprettes implisitt med de definerte verdiene for egenskapene.</span><span class="sxs-lookup"><span data-stu-id="008e9-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="008e9-111">Du kan deretter opprette andre relaterte enhetsposter (for eksempel ferdigheter eller utdanning) som separate API-kall.</span><span class="sxs-lookup"><span data-stu-id="008e9-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="008e9-112">Hvis du imidlertid vil bruke dybdeinnlegg for å opprette alle relaterte enheter i én operasjon, må egenskapene som er spesifikke for **mshr_dirpersonentity**-enheten, defineres på det nestede nivået for operasjonen.</span><span class="sxs-lookup"><span data-stu-id="008e9-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="008e9-113">Dette eksemplet viser hvordan du kan opprette en kandidatpost, den tilknyttede personposten og personens ferdigheter og utdannelse på tre nestede nivåer ved hjelp av dybdeinnlegg i en enkelt API-operasjon.</span><span class="sxs-lookup"><span data-stu-id="008e9-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="008e9-114">Eksemplet inneholder ikke alle egenskapene til hver av API-enhetene.</span><span class="sxs-lookup"><span data-stu-id="008e9-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="008e9-115">Den er forenklet for demonstrasjonsformål.</span><span class="sxs-lookup"><span data-stu-id="008e9-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="008e9-116">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="008e9-116">**Request**</span></span>

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

<span data-ttu-id="008e9-117">**Svar**</span><span class="sxs-lookup"><span data-stu-id="008e9-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="008e9-118">Se også</span><span class="sxs-lookup"><span data-stu-id="008e9-118">See also</span></span>

[<span data-ttu-id="008e9-119">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="008e9-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]