---
title: Personferdighet
description: Dette emnet beskriver Personferdighet-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: d2721e3eace401537e85e57b5895d508317e6c4b71d481d15ff176b786a937e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756202"
---
# <a name="person-skill"></a>Personferdighet

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Personferdighet-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonskillentity

## <a name="description"></a>beskrivelse

Denne enheten beskriver kandidatens ferdigheter.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Enhets-ID for personferdighet**<br>mshr_hcmpersonskillentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk | Systemgenerert unik identifikator for enhetsposten. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Lese/skrive<br>Obligatorisk |   IDen til den tilknyttede partsposten (person). |
| **Verdi for person-ID**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity | Systemgenerert unik identifikator for partsenhetsposten (person). |
| **Godkjenner**<br>mshr_certifier<br>*Streng* | Lese/skrive<br>Valgfri | Personalnummeret til arbeideren som godkjente denne ferdigheten. |
| **Verdi for godkjenner-ID**<br>_mshr_fk_certifier_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmworkerentityid i mshr_hcmworkerentity | Systemgenerert unik ID for arbeiderposten for arbeideren som bekreftet ferdigheten. |
| **Ferdighets-ID**<br>mshr_skillid<br>*Streng* | Lese/skrive<br>Obligatorisk | IDen for ferdigheten som er definert i Human Resources. |
| **Verdi for ferdighets-ID**<br>_mshr_fk_skill_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmskillentityid i mshr_hcmskillentity | Systemgenerert identifikator for den valgte ferdigheten. |
| **År med erfaring**<br>mshr_yearsofexperience<br>*Desimal* | Lese/skrive<br>Valgfri | År med erfaring kandidaten har i denne ferdigheten. |
| **Vurderings-ID**<br>mshr_ratingid<br>*Streng* | Lese/skrive<br>Obligatorisk | Vurderingsskalatypen. For denne enheten er verdien **Ferdigheter**. |
| **Nivåtype**<br>mshr_leveltype<br>*mshr_hrmskillleveltype-alternativsett* | Lese/skrive<br>Obligatorisk | En typekategorisering for nivået som er tilordnet ferdigheten. |
| **Nivå-ID**<br>mshr_levelid<br>*Streng* | Lese/skrive<br>Obligatorisk | IDen til vurderingsnivået kandidaten har for denne ferdigheten. |
| **Verdien for vurderingsnivå-ID**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmratinglevelentityid i mshr_hcmratinglevelentity | Systemgenerert identifikator for vurderingsnivået. |
| **Nivådato**<br>mshr_leveldate<br>*Datetime* | Lese/skrive<br>Obligatorisk | Datoen da kandidaten ble vurdert til ferdigheten. |
| **Vurderingsnivåeksaminator**<br>mshr_ratinglevelexaminer<br>*Streng* | Lese/skrive<br>Valgfri | Personalnummeret til arbeideren som vurderte denne kandidaten. |
| **Verdi for vurderingsnivåeksaminator-ID**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Sekundærnøkkel: mshr_hcmworkerentityid i mshr_hcmworkerentity | Den systemgenererte identifikator til den ansatte som vurderte kandidatens ferdighetsnivå. |
| **Verifisert**<br>mshr_verified<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Obligatorisk | Angir om det vurderte ferdighetsnivået er godkjent. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en identifikator for enhetsposten. Kombinasjon av partnummer, nivåtype, ferdighets-ID og nivådato. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]