---
title: Screeningtyper
description: Denne artikkelen beskriver Screeningtyper-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 95f4a3dce6851c7080ac665f5922e3b5877fa9f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880545"
---
# <a name="screening-types"></a>Screeningtyper


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Screeningtyper-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmscreeningtypeentity

## <a name="description"></a>beskrivelse

Denne enheten beskriver screeningtypene som er definert av firmaet for screeningprosesser før ansettelse og nåværende ansatte.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **ID for Screeningtype-enhet**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | Unik primær-ID for posten for screeningtype. |
| **ID for screeningtype**<br>mshr_screeningtypeid<br>*Streng* | Lese/skrive<br>Obligatorisk | Brukerdefinert unik identifikator for screeningtype. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Lese/skrive<br>Obligatorisk | Beskrivelse av screeningtypen. |
| **Frekvensenhet**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit-alternativsett* | Lese/skrive<br>Obligatorisk | Beskriver hvor ofte screeningen må fullføres for den tilordnede personen. |
| **Generer fra**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom-alternativsett* | Lese/skrive<br>Obligatorisk | Hvis frekvensverdien er en annen verdi enn "Bare én gang", bestemmer GenerateFrom-verdien datoen som neste screeninghendelse skal beregnes fra. |
| **Frekvensintervall**<br>mshr_frequencyinterval<br>*Heltall* | Lese/skrive<br>Obligatorisk | Hvis frekvensverdien er en annen verdi enn "Bare én gang", må du definere et intervall for tidsenhetene mellom hver screeninghendelse. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
