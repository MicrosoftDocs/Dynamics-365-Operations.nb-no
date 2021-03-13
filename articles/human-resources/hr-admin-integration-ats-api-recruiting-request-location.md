---
title: Rekrutteringsforespørselssted
description: Dette emnet beskriver Rekrutteringsforespørselslokasjon-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa153b1cfcbb70294ed6da3618c83396df04f8db
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125239"
---
# <a name="recruiting-request-location"></a>Rekrutteringsforespørselssted

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
