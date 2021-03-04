---
title: Manuell avskrivning
description: Denne artikkelen gir en oversikt over den manuelle avskrivningsmetoden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446256"
---
# <a name="manual-depreciation"></a>Manuell avskrivning

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over den manuelle avskrivningsmetoden.

Når du definerer en avskrivningsprofil for anleggsmiddel og velger **Manuelt** i feltet **Metode** på siden **Avskrivningsprofiler**, bestemmes avskrivningen for anleggsmidler som er tilordnet avskrivningsprofilen, av prosenten du angir for hvert intervall i kalenderåret. Intervallene du angir prosenter for, posteres i henhold til verdien du velger i **Periodefrekvens** i **Generelt**-hurtigkategorien av på siden **Avskrivningsprofiler**. Her er verdiene du kan velge:

-   Årlig
-   Månedlig
-   Kvartalsvis
-   Halvårlig
-   Daglig

Når du velger posteringsfrekvens, klikker du **Manuelle planer** og angir prosenter for hvert posteringsintervall. De manuelle planene og posteringsintervallene definerer sammen avskrivningsbeløpet, som vist i eksemplene senere i denne artikkelen. Manuell avskrivning beregnes alltid som en prosent av anskaffelsesprisen. For manuell avskrivning inneholder ikke prosentene du angir i intervallene, totalt 100 prosent. Manuell avskrivning er en fleksibel avskrivningsmetode som ofte brukes til å definere en ekstraordinær avskrivningsprofil på siden **Tablåer**, for eksempel en avskrivning som ikke er periodisk, for bestemte formål (for eksempel avgift).

## <a name="examples"></a>Eksempler
Anskaffelsespris: 11 000,00 Forventet skrapverdi: 1000,00 Følgende tabell viser intervallene og prosentene du definerer på siden **Planer for anleggsmidlets avskrivningsprofil**.

| Intervallnummer | Prosent |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Følgende tabell viser hvordan avskrivning for hvert intervall beregnes.

|  Intervallnummer | Beregning av årlig avskrivningsbeløp | Netto bokført verdi på slutten av intervallet |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11 000 – 1 000) × 10 % = 1 000                | 10 000 (11 000 – 1 000)                   |
| 2                | (11 000 – 1 000) × 50 % = 5 000                | 5 000 (10 000 – 5 000)                    |
| 3                | (11 000 – 1 000) × 8 % = 800                   | 4 200 (5 000 – 800)                       |

Hvis du velger **Månedlig** i feltet **Periodefrekvens**, må du definere 12 manuelle planleggingsintervaller. Følgende tabell viser avskrivningsbeløpene for de to første intervallene.

| Intervall | Avskrivningsbeløp            |
|----------|--------------------------------|
| Januar  | (11 000 – 1 000) × 10 % = 1 000 |
| Februar | (11 000 – 1 000) × 50 % = 5 000 |

Hvis du velger <strong>Halvårlig</strong> i *<strong><em>Periodefrekvens</em>*-feltet</strong>, må du definere to manuelle planleggingsintervaller. Følgende tabell viser avskrivningsbeløpene for disse intervallene.

| Intervall    | Avskrivningsbeløp            |
|-------------|--------------------------------|
| 30. juni     | (11 000 – 1 000) × 10 % = 1 000 |
| 31. desember | (11 000 – 1 000) × 50 % = 5 000 |

Den totale prosenten for alle intervallene behøver ikke å være 100. Imidlertid du mottar en melding hvis verdien i feltet **Kumulert prosent** på siden **Planer for anleggsmidlets avskrivningsprofil** ikke er **100**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]