---
title: Vurderingsnivå
description: Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: a821e3cd90e85571da4a09f5dd564beb2de35989
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068640"
---
# <a name="rating-level"></a>Vurderingsnivå


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmratinglevelentity

## <a name="description"></a>beskrivelse

Denne enheten inneholder tilgjengelige vurderingsnivåer for ferdigheter. Vurderingsnivåer gjelder på tvers av alle juridiske enheter.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Vurderingsnivå-enhet**<br>mshr_hcmratinglevelentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | Den systemgenererte unike identifikatoren for nivået. |
| **Vurderingsnivå-ID**<br>mshr_ratinglevelid<br>*Streng* | Lese/skrive<br>Obligatorisk | Brukerlesbare unik identifikator for nivået. |
| **ID for vurderingsmodell**<br>mshr_ratingmodelid<br>*Streng* | Lese/skrive<br>Obligatorisk | Vurderingsmodellen som vurderingsnivået tilhører. |
| **ID for Vurderingsmodell-enhet**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Sekundærnøkkel: mshr_hcmratingmodelentityid i mshr_hcmratingmodelentity | Den systemgenererte IDen for vurderingsmodellen som vurderingsnivået tilhører. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | Beskrivelsen av vurderingsnivået. |
| **Omregningsfaktor**<br>mshr_factor<br>*Heltall* | Lese/skrive<br>Obligatorisk | Faktoren for vurderingsnivået. Når du sammenligner varer med et annet antall vurderingsnivåer, brukes faktoren til å normalisere poengsummene. Verdien må være et heltall mellom 0 og 9. |
| **Obs!**<br>mshr_note<br>*Streng* | Lese/skrive<br>Valgfri | Eventuelle merknader som er knyttet til vurderingsnivået. |
| **Primærfelt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Felt som brukes som en identifikator for enhetsposten. Kombinasjon av vurderingsnivå-ID og vurderingsmodell-ID. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
