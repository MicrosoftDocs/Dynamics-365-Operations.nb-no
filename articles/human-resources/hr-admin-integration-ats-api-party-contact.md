---
title: Partskontakt
description: Dette emnet beskriver Partskontakt-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: fe25e37025a9f7945121a2a999c164a273e803fed750cc258e1ad30e33fc709b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727191"
---
# <a name="party-contact"></a>Partskontakt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Partskontakt-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_dirpartycontactentities

## <a name="description"></a>beskrivelse

Denne enheten beskriver kandidatens kontaktinformasjon, inkludert telefon-, e-post- og sosiale medier-kontoer.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Partskontakt-enhet**<br>mshr_dirpartycontactentityid<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik identifikator for enhetsposten. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk | IDen til den tilknyttede partsposten (person). |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for partsenhetsposten (person). |
| **Plasserings-ID**<br>mshr_locationid<br>*Streng* | Lese/skrive<br>Obligatorisk | Lokasjons-IDen for adresseposten. Oppsett i enheten mshr_logisticspostaladdresslocationcdsentity. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | Beskrivelse av kontaktdetaljene. |
| **Type**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype-alternativsett* | Lese/skrive<br>Obligatorisk | Kontaktdetaljtypen. |
| **Land-/områdekode**<br>mshr_countryregioncode<br>*Streng* | Lese/skrive<br>Valgfri | Landet eller området i adressen. |
| **Lokator**<br>mshr_locator<br>*Streng* | Lese/skrive<br>Valgfri | Kontaktdetaljene. Hvis for eksempel typen er **E-postadresse**, inneholder dette feltet kandidatens e-postadresse. |
| **Lokatorutvidelse**<br>mshr_locatorextension<br>*Streng* | Lese/skrive<br>Valgfri | Lokatorutvidelsen. Hvis for eksempel typen er **Telefon**, vil denne egenskapen inneholde direktenummeret. |
| **Er mobil**<br>mshr_ismobile<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Angir om telefonen er et mobilnummer. |
| **Er direktemelding**<br>mshr_isinstantmessage<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Angir om telefonen er aktivert for direktemeldinger. |
| **Er primær**<br>mshr_isprimary<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Bestemmer primærkontakten for kontakttypen. Det må bare være én primærpost per kontakttype. |
| **Er privat**<br>mshr_isprivate<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Identifiserer om denne adressen er en privat adresse for personen. |
| **Formål**<br>mshr_purpose<br>*Streng* | Lese/skrive<br>Valgfri | Formål/rolle for kontaktdetaljene. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en primær identifikator for enhetsposten. Kombinasjon av partnummer, type, beskrivelse og lokator. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]