---
title: "Gjenstående lineær levetidsavskrivning"
description: "Denne artikkelen gir en oversikt over lineær levetid gjenværende metode for avskrivning."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 765825ba43cad44b076ea6628d2787011e97fc57
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Gjenstående lineær levetidsavskrivning

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over lineær levetid gjenværende metode for avskrivning.

Når du definerer en avskrivningsprofil for anleggsmidler og velger **Lineær levetid som gjenstår** i feltet **Metode** på siden **Avskrivningsprofiler**, blir avskrivningen av anleggsmidler som er knyttet til avskrivningsprofilen, da basert på anleggsmiddelets gjenværende levetid. Avskrivningsbeløpet er vanligvis det samme i hver avskrivningsperiode. Hvis du vil definere avskrivning for gjenværende lineær levetid, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**. Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.

## <a name="select-a-depreciation-year"></a>Velge et avskrivningsår
Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden. Standardverdien er **Kalender**. Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet. Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.

### <a name="calendar"></a>Kalender

Hvis du velger **Kalender** i feltet ***Avskrivningsår***, antas et år fra 1. januar til og med 31. desember, selv om du har definert regnskapskalenderen annerledes. **Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år. Avskrivningsgrunnlaget er vanligvis netto bokført verdi minus restverdien. I eksemplet senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen. Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:

-   **Årlig** posterer et beløp 31. desember.
-   **Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.
-   **Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).
-   **Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderår (30. juni og 31. desember).
-   **Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.

Hvis du velger for eksempel **Årlig**, posteres den årlige avskrivningen bare én gang, den 31. desember i hvert år. Hvis du velger **Månedlig**, posteres den månedlige avskrivningen hver måned, som en tolvdel av Årlig avskrivningsbeløp.

### <a name="fiscal"></a>Skattemessig

Hvis du velger **Skattemessig** i feltet **Avskrivningsår** , brukes avskrivning for gjenværende lineær levetid. Avskrivning beregnes basert på de gjenværende regnskapsårene. For regnskapsåret 1. juli 2015 til 30. juni 2016 starter for eksempel avskrivningsberegningen 1. juli. Regnskapsåret kan være lengre eller kortere enn 12 måneder. Avskrivningen justeres for hver regnskapsperiode. Lengden på det neste regnskapsåret bestemmes av regnskapsperiodene som er definert på siden **Regnskapskalendere**. Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:

-   **Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.
-   **Regnskapsperiode**beregner totalbeløpet for avskrivningen for regnskapsåret. Dette beløpet avsettes deretter i regnskapsperiodene som defineres på siden **Regnskapskalendere** for regnskapskalenderen som er angitt for tablået.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Eksempel på lineær avskrivning for et uendret anleggsmiddel
Et anleggsmiddel har følgende kjennetegn.

|                     |        |
|---------------------|--------|
| Anskaffelseskostnad    | 11 000 |
| Restverdi       | 1 000  |
| Avskrivningsgrunnlag   | 10 000 |
| Levetid i år  | 5      |
| Årlig avskrivning | 2 000  |

Avskrivningsbeløpet er det samme hvert år: (anskaffelseskostnad-restverdi) ÷ levetidsår

| Periode | Beregning av årlig avskrivningsbeløp | Netto bokverdi på slutten av året |
|--------|-----------------------------------------------|---------------------------------------|
| År 1 | (11 000 – 1 000) ÷ 5 = 2 000                  | 9 000                                 |
| År 2 | (9 000 – 1 000) ÷ 4 = 2 000                   | 7 000                                 |
| År 3 | (7 000 – 1 000) ÷ 3 = 2 000                   | 5 000                                 |
| År 4 | (5 000 – 1 000) ÷ 2 = 2 000                   | 3 000                                 |
| År 5 | (3 000 – 1 000) ÷ 1 = 2 000                   | 1 000                                 |






