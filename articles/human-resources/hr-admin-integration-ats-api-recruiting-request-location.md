---
title: Rekrutteringsforespørselssted
description: Dette emnet beskriver Rekrutteringsforespørselslokasjon-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: be87c51737bb9021e2ca56e4ec3993d01714dbef
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057388"
---
# <a name="recruiting-request-location"></a>Rekrutteringsforespørselssted

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Rekrutteringsforespørselslokasjon-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>beskrivelse

Listen over lokasjoner som er definert som lokasjoner der rekrutteringsansatte vil arbeide ved ansettelse. Dette er lokasjoner som opprettes på tvers av juridiske enheter.

### <a name="json-representation"></a>JSON-representasjon

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Plasserings-ID**<br>mshr_locationid<br>*Streng* | Skriv én gang<br>Obligatorisk | Den systemgenererte brukerlesbare identifikator for rekrutteringslokasjon. |
| **Rekrutteringsforespørselslokasjon**<br>mshr_recruitingrequestlocationid<br>*Streng* | Skriv én gang<br>Obligatorisk | Brukerdefinert unik identifikator for rekrutteringslokasjonen. |
| **ID for Rekrutteringsforespørselslokasjon-enhet**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik ID for posten rekrutteringsforespørselslokasjon. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | Beskrivelse av plasseringen. |
| **ID for land/område**<br>mshr_countryregionid<br>*Streng* | Skrivebeskyttet<br>Valgfri | Angir landet eller området der kandidaten har statsborgerskap. |
| **Verdi for ID for land/område**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_logisticaddresscountryregionentityid i mshr_logisticsaddresscountryregionentity | Systemgenererte unik identifikator for land/-område i adressen. |
| **Postnummer**<br>mshr_zipcode<br>*Streng* | Skrivebeskyttet<br>Valgfri | Postnummer. |
| **Gate**<br>mshr_street<br>*Streng* | Skrivebeskyttet<br>Valgfri | Gateadresse. |
| **Poststed**<br>mshr_city<br>*Streng* | Skrivebeskyttet<br>Valgfri | Poststed. |
| **Status**<br>mshr_state<br>*Streng* | Skrivebeskyttet<br>Valgfri | Stat eller provins. |
| **Kommune**<br>mshr_county<br>*Streng* | Skrivebeskyttet<br>Valgfri | Kommune. |
| **Telefon**<br>mshr_telephone<br>*Streng* | Lese/skrive<br>Valgfri | Telefonnummer til lokasjonen. |
| **E-post**<br>mshr_email<br>*Streng* | Lese/skrive<br>Valgfri | E-postadresse. |
| **InternetAddress**<br>mshr_internetaddress<br>*Streng* | Lese/skrive<br>Valgfri | URL-adresse til webområdet for lokasjonen. |
| **Dataområde-ID**<br>mshr_dataareaid<br>*Streng* | Lese/skrive<br>Valgfri | Angir den juridiske enheten (firmaet). |
| **Verdi for dataområde-ID**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: cdm_companyid i cdm_company-enhet | Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet). |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]