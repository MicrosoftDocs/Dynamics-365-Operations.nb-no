---
title: "Lineær levetidsavskrivning"
description: "Denne artikkelen gir en oversikt over avskrivningsmetoden lineær levetid."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b8c078841ca2e4bd994bbfbbe2abb130a4cf6fa
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-service-life-depreciation"></a>Lineær levetidsavskrivning

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over avskrivningsmetoden lineær levetid.

Når du definerer en avskrivningsprofil for anleggsmidler og velger Lineær levetid i feltet Metode på siden Avskrivningsprofiler, avskrives anleggsmidlene som har denne avskrivningsprofilen basert på den samlede levetiden til anleggsmiddelet. Dette er vanligvis det samme avskrivningsbeløpet i hver avskrivningsperiode. 

Forskjellen i avskrivningsbeløpet som beregnes mellom gjenværende lineær levetid og lineær levetid, er hvis det er en justering postert til anleggsmidlet. 

Hvis du vil definere lineær levetidsavskrivning, må du også velge alternativer i feltet Avskrivningsår og feltet Periodefrekvens på siden Avskrivningsprofiler.

## <a name="select-a-depreciation-year"></a>Velge et avskrivningsår
Du kan velge enten Kalender eller Regnskapsår i Avskrivningsår-feltet på siden Avskrivningsprofiler. Valget definerer alternativene som er tilgjengelige i Periodefrekvens-feltet. Standardvalget er Kalender.

### <a name="calendar"></a>Kalender

Hvis du velger Kalender, antas det at året er 1. januar til 31.desember, selv om du har definert den økonomiske kalenderen på en annen måte. 

Alternativet Kalender oppdaterer avskrivningsgrunnlaget, som vanligvis er netto bokført verdi minus restverdi, 1. januar hvert år. I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen. 

Hvis du velger Kalender, er følgende alternativer tilgjengelige i Periodefrekvens-feltet, som definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom hele kalenderåret:
-   Årlig posterer et beløp 31. desember.
-   Månedlige posteringer av et månedlig beløp på slutten av hver kalendermåned.
-   Kvartalsvise posteringer av et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).
-   Halvårlig posterer et halvårlig beløp på slutten av hvert kalenderår (30. juni og 31. desember).
-   Daglige posteringer av avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.

Hvis du velger for eksempel Årlig, posteres den årlige avskrivningen bare én gang, den 31. desember i hvert år. Hvis du velger Månedlig, posteres den månedlige avskrivningen hver måned som en tolvdel av det årlige avskrivningsbeløpet.

### <a name="fiscal"></a>Skattemessig

Hvis du velger Skattemessig i feltet Avskrivningsår, brukes lineær levetidsavskrivning. Det beregnes basert på regnskapsåret, som er definert av den økonomiske kalenderen som er angitt for tablået, eller av den økonomiske kalenderen som er valgt på Finans-siden. Regnskapskalendere defineres på Regnskapskalendere-siden.

For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen 1. juli. Regnskapsåret kan være lengre eller kortere enn 12 måneder. Avskrivningen justeres automatisk for hver regnskapsperiode. Lengden på det neste regnskapsåret baseres på regnskapsperiodene som du definerer når du oppretter et nytt regnskapsår på skjemaet med regnskapskalendere. 

Hvis du velger Regnskapsår, er følgende alternativer tilgjengelige i Periodefrekvens-feltet:
-   Årlig posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.
-   Regnskapsperioder beregner totalbeløpet for avskrivningen for regnskapsåret, som avsettes i regnskapsperiodene som defineres i skjemaet for regnskapskalender for regnsapskalenderen.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Eksempel på lineær avskrivning for et uendret anleggsmiddel
Anta at anleggsmidlet har følgende egenskaper:

|                     |        |
|---------------------|--------|
| Anskaffelseskostnad    | 11 000 |
| Restverdi       | 1 000  |
| Avskrivningsgrunnlag   | 10 000 |
| Levetid i år  | 5      |
| Årlig avskrivning | 2 000  |

Du får samme avskrivningsbeløp hvert år. (Anskaffelseskostnad - Restverdi) / Levetidsår

| Periode | Beregning av årlig avskrivningsbeløp | Netto bokført verdi på slutten av året |
|--------|-------------------------------------------|---------------------------------------|
| År 1 | (11,000 - 1,000) / 5 = 2,000              | 9 000                                 |
| År 2 | (11,000 - 1,000) / 5 = 2,000              | 7 000                                 |
| År 3 | (11,000 - 1,000) / 5 = 2,000              | 5 000                                 |
| År 4 | (11,000 - 1,000) / 5 = 2,000              | 3 000                                 |
| År 5 | (11,000 - 1,000) / 5 = 2,000              | 1 000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Eksempel på lineær avskrivning av et endret anleggsmiddel

Sett at du legger til en anskaffelsesjustering på 4 000 i år 2 for samme anleggsmiddel. 

Levetiden for anskaffelsesjusteringen er den samme som den til anleggsmidlet, og begynner på anskaffelsestidspunktet. En netto bokført verdi gjenstår ved utgangen av år 5, som tilsvarer netto bokført verdi for anskaffelsesjusteringen. Avskrivning etter periode blir beregnet som vist i følgende tabell.

| Periode | Beregning av årlig avskrivningsbeløp | Netto bokverdi på slutten av året |
|--------|-------------------------------------------|---------------------------------------|
| År 1 | 10,000 / 5 = 2,000                        | 11,000 - 2,000 = 9,000                |
| År 2 | 4,000 (anskaffelsesjustering)            | 9,000 + 4,000 =13,000                 |
| År 2 | 14,000 / 5 = 2,800                        | 13,000 - 2,800 = 10,200               |
| År 3 | 14,000 / 5 = 2,800                        | 10,200 - 2,800 = 7,400                |
| År 4 | 14,000 / 5 = 2,800                        | 7,400 - 2,800 = 4,600                 |
| År 5 | 14,000 / 5 = 2,800                        | 4,600 - 2,800 = 1,800                 |
| År 6 | Gjenværende 800*\*                           | 1,800 – 800 = 1,000                   |

\*Fordi gjenværende beløp er mindre en avskrivningsbeløpet, brukes bare gjenværende beløp minus enn restverdien.






