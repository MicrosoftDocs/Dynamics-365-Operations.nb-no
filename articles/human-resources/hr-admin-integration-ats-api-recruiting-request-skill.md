---
title: Rekrutteringsforespørselsferdighet
description: Dette emnet beskriver Rekrutteringsforespørselsferdighet-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9347b6f2e18c7ec12c18137846507532fc9fcc3149a3638d12c070dc848a1fc7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712127"
---
# <a name="recruiting-request-skill"></a>Rekrutteringsforespørselsferdighet

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Rekrutteringsforespørselsferdighet-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>beskrivelse

Beskriver kompetansekrav for en RecruitingRequest.

### <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Rekrutteringsforespørselsferdighet-enhet**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik ID for posten **Rekrutteringsforespørselsferdighet**. |
| **ID for rekrutteringsforespørsel**<br>mshr_recruitingrequestid<br>*Streng* | Skriv én gang<br>Obligatorisk | Den brukerlesbare unike identifikatoren for den tilknyttede rekrutteringsforespørselen. |
| **ID for rekrutteringsforespørselsverdi**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br> Sekundærnøkkel: mshr_hcmrecruitingrequestentityid i mshr_hcmrecruitingrequestentity-enhet | Systemgenerert unik ID for den tilknyttede rekrutteringsforespørselen. |
| **Ferdighets-ID**<br>mshr_skillid<br>*Streng*<br> | Skriv én gang<br>Obligatorisk | Den brukerlesbare unike identifikatoren for den påkrevde ferdigheten. |
| **Verdi for ferdighets-ID**<br>_mshr_fk_skill_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmskillentityid i mshr_hcmskillentity-enhet | Systemgenerert unik identifikator for den nødvendige ferdigheten. |
| **Vurderingsnivå-ID**<br>mshr_ratinglevelid<br>*Streng* | Skriv én gang<br>Valgfri | Den nødvendige ferdighetsnivåverdien som er valgt for jobben, basert på vurderingsmodellen som er tilordnet ferdigheten. |
| **Verdien for vurderingsnivå-ID**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmratinglevelentityid i mshr_hcmratinglevelentity-enhet | Systemgenerert unik identifikator for nivået. |
| **Ferdighetsbeskrivelse**<br>mshr_skilldescription<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Ferdighetsbeskrivelsen. |
| **Beskrivelse av vurderingsnivå**<br>mshr_ratingleveldescription<br>*Streng* | Skrivebeskyttet<br>Valgfri | Beskrivelsen av det valgte ferdighetsnivået. |
| **Dataområde-ID**<br>mshr_dataareaid<br>*Streng* | Lese/skrive<br>Valgfri | Angir den juridiske enheten (firmaet). |
| **Verdi for dataområde-ID**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: cdm_companyid i cdm_company-enhet | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet). |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Sammenslåing av rekrutteringsforespørselsverdi og ferdighets-ID som en annen metode for å identifisere posten entydig. |
| **ID for vurderingsmodell**<br>mshr_ratingmodelid<br>*Streng* | Lese/skrive<br>Obligatorisk | Vurderingsmodellen som brukes til å vurdere ferdigheten. |
| **Verdien for vurderingsmodell-ID**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmratingmodelentityid i mshr_hcmratingmodelentity-enhet | Systemgenerert unik identifikator for vurderingsmodellen som brukes til å vurdere ferdigheten. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]