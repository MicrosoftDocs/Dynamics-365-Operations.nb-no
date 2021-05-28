---
title: Generer og gå gjennom lønnsenheter
description: Dette emnet beskriver hvordan du genererer og gjennomgår lønnsenheter.
author: andreabichsel
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4adab0225190b4dea5213dccf297eaab33efc863
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021326"
---
# <a name="generate-payroll-entities"></a><span data-ttu-id="3f35b-103">Generer lønnsenheter</span><span class="sxs-lookup"><span data-stu-id="3f35b-103">Generate payroll entities</span></span>

<span data-ttu-id="3f35b-104">Bruk denne OData-funksjonen til å generere enhetene som trengs for lønnsintegrering.</span><span class="sxs-lookup"><span data-stu-id="3f35b-104">Use this OData function to generate the entities needed for payroll integration.</span></span> <span data-ttu-id="3f35b-105">Hvis det gjøres endringer i disse enhetene i Human Resources, for eksempel legge til egendefinerte felt, kan denne funksjonen kalles på nytt for å oppdatere metadataene for hver enhet.</span><span class="sxs-lookup"><span data-stu-id="3f35b-105">If any changes are made to these entities in Human Resources, such as adding custom fields, this function can be called again to refresh the metadata of each entity.</span></span> <span data-ttu-id="3f35b-106">Svaret inneholder en operasjons-ID som du kan overvåke, slik at du vet når genereringsprosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="3f35b-106">The response contains an operation ID that you can monitor so you know when the generation process has completed.</span></span>

<span data-ttu-id="3f35b-107">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="3f35b-107">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/RefreshHumanResourcesVirtualEntities
```

<span data-ttu-id="3f35b-108">**meldingstekst**</span><span class="sxs-lookup"><span data-stu-id="3f35b-108">**body**</span></span>

```json
{
    "PhysicalNames" : ["PayrollEmployeeEntity", "HcmWorkerBaseEntity", "PayrollPositionEntity", "PayrollPositionJobEntity", "PayrollWorkerAddressEntity", "HcmJobDetailEntity", "HcmCompFixedPlanTableEntity", "PayrollFixedCompensationPlanEntity", "HcmEmploymentDetailEntity"]
}
```

<span data-ttu-id="3f35b-109">**Svar**</span><span class="sxs-lookup"><span data-stu-id="3f35b-109">**Response**</span></span>

```json
{
    "AsyncOperationId": "8b98d338-f939-4c86-9a91-80b76b6ab2ea"
}
```

## <a name="review-payroll-entities"></a><span data-ttu-id="3f35b-110">Gå gjennom lønnsenheter</span><span class="sxs-lookup"><span data-stu-id="3f35b-110">Review payroll entities</span></span>

<span data-ttu-id="3f35b-111">Bruk denne API-en til å hente en liste over enhetene som har blitt generert og er klare til bruk.</span><span class="sxs-lookup"><span data-stu-id="3f35b-111">Use this API to retrieve a list of the entities that have been successfully generated and are ready for use.</span></span>

<span data-ttu-id="3f35b-112">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="3f35b-112">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hrvirtualentitycatalogs?$filter=mshr_hasbeengenerated eq true
```

<span data-ttu-id="3f35b-113">**Svar**</span><span class="sxs-lookup"><span data-stu-id="3f35b-113">**Response**</span></span>

```json
{
      "value": [
        {
            "mshr_physicalname": "PayrollWorkerAddressEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-1c00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmJobDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6400-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmCompFixedPlanTableEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6b00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollEmployeeEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6d00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmEmploymentDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-7e00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollFixedCompensationPlanEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-9300-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmWorkerBaseEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-c000-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollPositionJobEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-e700-005001000000",
            "mshr_refresh": null
        }
    ]
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]