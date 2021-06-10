---
title: Rekrutteringsforespørselsutdanning
description: Dette emnet beskriver Rekrutteringsforespørselsutdannelses-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4976e51dbe0cb7f50290b40d6342bcc18044cd52
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057436"
---
# <a name="recruiting-request-education"></a>Rekrutteringsforespørselsutdanning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Rekrutteringsforespørselsutdannelses-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>beskrivelse

Beskriver utdannelsesskrav for en rekrutteringsforespørsel.

### <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Rekrutteringsforespørselsutdanning-enhet**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik ID for posten rekrutteringsforespørselsutdannelse. |
| **ID for rekrutteringsforespørsel**<br>mshr_recruitingrequestid<br>*Streng* | Skriv én gang<br>Obligatorisk | Den brukerlesbare unike identifikatoren for den relaterte rekrutteringsforespørselen. |
| **ID for rekrutteringsforespørselsverdi**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmrecruitingrequestentityid i mshr_hcmrecruitingrequestentity | Systemgenerert unik ID for den relaterte rekrutteringsforespørselen. |
| **ID for utdannelsesnivå**<br>mshr_educationlevelid<br>*Streng* | Skriv én gang<br>Obligatorisk | Nivået for den påkrevde utdannelsen. |
| **Verdien på ID for utdannelsesnivå**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmeducationlevelentityid i mshr_hcmeducationlevelentity | Systemgenerert unik identifikator for nivået for den påkrevde utdannelsen. |
| **Beskrivelse av utdanningsnivå**<br>mshr_educationleveldescription<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Beskrivelsen av nivået som kreves for ferdigheten. |
| **ID for utdannelsesdisiplin**<br>mshr_educationdisciplinedescription<br>*Streng* | Skriv én gang<br>Obligatorisk | Området for utdannelsesdisiplinen. |
| **Verdi for ID for utdannelsesdisiplin**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmeducationdisciplineentityid i mshr_hcmeducationdisciplineentity-enhet | Systemgenerert unik identifikator for området for utdannelsesdisiplinen. |
| **Beskrivelse av utdannelsesdisiplin**<br>mshr_educationdisciplinedescription<br>Streng | Skrivebeskyttet<br>Obligatorisk | Beskrivelsen av området for utdannelsesdisiplinen. |
| **Dataområde-ID**<br>mshr_dataareaid<br>*Streng* | Lese/skrive<br>Valgfri | Angir den juridiske enheten (firmaet).|
| **Verdi for dataområde-ID**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: cdm_companyid i cdm_company-enhet | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet). |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Sammenslåing av rekrutteringsforespørselsverdi, ID for utdannelsesnivå og ID for utdannelsesdisiplin som en annen metode for å identifisere posten entydig. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]