---
title: Eksempelspørring for Kandidat for ansettelse
description: Dette emnet inneholder en eksempelspørring for Kandidat for ansettelse-enheten i Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ea6fc745ffb5892a32196394cb28cb5e646b7639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795075"
---
# <a name="example-query-for-candidate-to-hire"></a>Eksempelspørring for Kandidat for ansettelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet inneholder en eksempelspørring for Kandidat for ansettelse-enheten i Dynamics 365 Human Resources.

Dette emnet gir et eksempel på hvordan du kan bruke *dybdeinnlegg* til å opprette alle detaljene til en ny kandidatpost i én enkelt API-operasjon. Hvis du vil ha mer informasjon om dybdeinnlegg, kan du se [Opprette relaterte enhetsposter i én operasjon](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Enheten **mshr_hcmcandidatetohireentity** er unik på grunn av relasjonen til enheten **mshr_dirpersonentity**. Mange av egenskapene i **mshr_hcmcandidatetohireentity** (for eksempel **mshr_firstname**, **mshr_lastname** og **mshr_birthdate**) avledes fra posten **mshr_dirpersonentity**. Hvis du posterer en ny kandidatpost til **mshr_hcmcandidatetohireentity** uten å bruke dybdeinnlegg, kan du definere verdier for disse egenskapene direkte i posten **mshr_hcmcandidatetohireentity**. Den tilknyttede **mshr_dirpersonentity**-posten opprettes implisitt med de definerte verdiene for egenskapene. Du kan deretter opprette andre relaterte enhetsposter (for eksempel ferdigheter eller utdanning) som separate API-kall.

Hvis du imidlertid vil bruke dybdeinnlegg for å opprette alle relaterte enheter i én operasjon, må egenskapene som er spesifikke for **mshr_dirpersonentity**-enheten, defineres på det nestede nivået for operasjonen.

Dette eksemplet viser hvordan du kan opprette en kandidatpost, den tilknyttede personposten og personens ferdigheter og utdannelse på tre nestede nivåer ved hjelp av dybdeinnlegg i en enkelt API-operasjon.

> [!NOTE]
> Eksemplet inneholder ikke alle egenskapene til hver av API-enhetene. Den er forenklet for demonstrasjonsformål.

**Forespørsel**

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

**Svar**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]