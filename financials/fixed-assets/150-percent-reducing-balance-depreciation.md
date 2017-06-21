---
title: 150 prosent saldoavskrivning
description: Denne artikkelen gir en oversikt over avskrivningsmetoden 150 prosent saldoavskrivning.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 99535abef547b928eaf7d6d79a29e5e2ed245f03
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="150-percent-reducing-balance-depreciation"></a>150 prosent saldoavskrivning

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over avskrivningsmetoden 150 prosent saldoavskrivning.

Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **150 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode. Denne prosenten beregnes på grunnlag av anleggsmidlets levetid. Hvis anleggsmidlet for eksempel har en levetid på fem år, beregnes prosenten som 30 prosent (150 % ÷ 5). 

Hvis du vil definere 150 % saldoavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**. Alternativene som er tilgjengelige i **Periodefrekvens**-feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.

## <a name="selection-of-depreciation-year"></a>Velge avskrivningsår
Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden. 

Standardverdien er **Kalender**. Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet. Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.

### <a name="calendar"></a>Kalender

Du kan beholde standardverdien i **Avskrivningsår**-feltet, **Kalender**. 

**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år. Avskrivningsgrunnlaget er vanligvis netto bokført verdi minus svinnverdien. I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen. 

Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:

-   **Årlig** posterer et beløp 31. desember.
-   **Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.
-   **Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).
-   **Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderhalvår (30. juni og 31. desember).
-   **Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.

### <a name="fiscal"></a>Skattemessig

Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 150 % saldoavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden. Regnskapskalendere defineres på **Regnskapskalendere**-siden. 

For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli. Regnskapsåret kan være lengre eller kortere enn 12 måneder. Avskrivningen justeres for hver periode. Lengden på det neste regnskapsåret fastsettes av definisjonen av periodene på siden **Regnskapskalendere**. 

Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:

-   **Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret på den siste dagen i regnskapsåret.
-   **Regnskapsperiode** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret. Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.

## <a name="example-of-150-reducing-balance-depreciation"></a>Eksempel på 150 % redusert saldoavskrivning
|                                |        |
|--------------------------------|--------|
| Anskaffelseskostnad               | 11 000 |
| Restverdi                  | 1 000  |
| Avskrivningsgrunnlag              | 10 000 |
| Levetid i år             | 5      |
| Årlig avskrivningsprosent | 30 %    |

Metoden 150 % saldoavskrivning dividerer 150 prosent med antall levetidsår. Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.

| Periode | Beregning av årlig avskrivningsbeløp | Bokført verdi             | Netto bokverdi på slutten av året |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| År 1 | (11 000 – 1 000) × 30 % = 3 000                | 11 000 – 3 000 = 8 000 | 11 000 – 1 000 – 3 000 = 7 000        |
| År 2 | 7 000 × 30 % = 2 100                           | 8 000 – 2 100 = 5 900  | 7 000 – 2 100 = 4 900                 |
| År 3 | 4 900 × 30 % = 1 470                           | 5 900 – 1 470 = 4 430  | 4 900 – 1 470 = 3 430                 |

> [!NOTE]
> Vanligvis når beløpet som beregnes ved å bruke 150% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.




