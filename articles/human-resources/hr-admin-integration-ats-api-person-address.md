---
title: Personadresse
description: Denne artikkelen beskriver Personadresse-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: be5cf649771eaddcb4f2198821530e61b76b2cd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871023"
---
# <a name="person-address"></a>Personadresse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Personadresse-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonaddressentities

## <a name="description"></a>beskrivelse

Denne enheten inneholder listen over postadresser for kandidatposter.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Personadresse-enhet**<br>mshr_hcmpersonaddressentityid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik identifikator for enhetsposten. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | IDen til den tilknyttede partsposten (person). |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for partsenhetsposten (person). |
| **Plasserings-ID**<br>mshr_locationid<br>*Streng* | Lese/skrive<br>Obligatorisk | Lokasjons-IDen for adresseposten. Oppsett i enheten mshr_logisticspostaladdresslocationcdsentity. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | En beskrivelse av kandidatens adresse. |
| **Roller**<br>mshr_roles<br>*Streng* | Lese/skrive<br>Obligatorisk | Rollene som er tilordnet denne adressen. Du kan tilordne mer enn én rolle. Hver rolle må skilles med et semikolon. Gyldige verdier i enheten mshr_logisticslocationroleentity. |
| **Gate**<br>mshr_street<br>*Streng* | Lese/skrive<br>Valgfri | Gatenummeret. |
| **Poststed**<br>mshr_city<br>*Streng* | Lese/skrive<br>Valgfri | Poststedet for adressen. Defineres i enheten mshr_logisticsaddresscityentity. |
| **Status**<br>mshr_state<br>*Streng* | Lese/skrive<br>Valgfri | Staten for adressen. Defineres i enheten mshr_logisticsaddressstateentity. |
| **Kommune**<br>mshr_county<br>*Streng* | Lese/skrive<br>Valgfri | Regionen i adressen. Defineres i enheten mshr_logisticsaddresscountyentity. |
| **Postnummer**<br>mshr_zipcode<br>*Streng* | Lese/skrive<br>Valgfri | Postnummeret i adressen. Defineres i enheten mshr_logisticsaddresspostalcodeentity. |
| **ID for land/område**<br>mshr_countryregionid<br>*Streng* | Lese/skrive<br>Valgfri | Landet eller området i adressen. |
| **Verdi for ID for land/område**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_logisticaddresscountryregionentityid i mshr_logisticsaddresscountryregionentity | Systemgenererte unik identifikator for land/-område i adressen. |
| **Er primær**<br>mshr_isprimary<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Identifiserer om denne adressen er primæradressen for personen i den definerte rollen. |
| **Er privat**<br>mshr_isprivate<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Identifiserer om denne adressen er en privat adresse for personen. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en primær identifikator for enhetsposten. Kombinasjon av partnummer og lokasjons-ID. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
