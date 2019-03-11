---
title: 200 prosent redusert saldoavskrivning
description: Denne artikkelen gir en oversikt over avskrivningsmetoden 200 prosent saldoavskrivning.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec51f9e12e31e81c56fab9e82d0fc18d45beb5e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "322726"
---
# <a name="200-percent-reducing-balance-depreciation"></a>200 prosent redusert saldoavskrivning

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over avskrivningsmetoden 200 prosent saldoavskrivning.

Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **200 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode. Prosenten beregnes på grunnlag av anleggsmidlets levetid. Hvis anleggsmidlet for eksempel har en levetid på fem år, beregnes prosenten som 40 prosent (200 % ÷ 5). 

Denne metoden kalles også dobbel degressiv avskrivning.

Hvis du vil definere 200 % saldoverdiavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**. Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som du velger i **Avskrivningsår**-feltet.

## <a name="select-a-depreciation-year"></a>Velge et avskrivningsår
Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden. Standardverdien er **Kalender**. 

Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet. Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.

### <a name="calendar"></a>Kalender

Du kan beholde standardverdien i **Avskrivningsår**-feltet, **Kalender**. 

**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år. Avskrivningen er vanligvis netto bokført verdi minus svinnverdien. I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen. 

Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:

-   **Årlig** posterer et beløp 31. desember.
-   **Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.
-   **Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).
-   **Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderhalvår (30. juni og 31. desember).
-   **Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.

### <a name="fiscal"></a>Skattemessig

Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 200 % saldoavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden. Regnskapskalendere defineres på **Regnskapskalendere**-siden. 

For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli. Regnskapsåret kan være lengre eller kortere enn 12 måneder. Avskrivningen justeres for hver periode. Lengden på det neste regnskapsåret fastsettes av definisjonen av periodene på siden **Regnskapskalendere**. 

Når **Skattemessig** er valgt som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**- feltet:

-   **Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.
-   **Regnskapsperiode** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret. Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.

## <a name="example-of-200-reducing-balance-depreciation"></a>Eksempel på 200 % saldoverdiavskrivning

|                                |        |
|--------------------------------|--------|
| Anskaffelseskostnad               | 11 000 |
| Restverdi                  | 1 000 |
| Avskrivningsgrunnlag              | 10 000 |
| Levetid i år             | 5      |
| Årlig avskrivningsprosent | 40 %    |

Metoden 200 % saldoavskrivning dividerer 200 prosent med antall levetidsår. Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.

| Periode | Beregning av årlig avskrivningsbeløp | Bokført verdi             | Netto bokverdi på slutten av året |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| År 1 | (11 000 – 1 000) × 40 % = 4 000                | 11 000 – 4 000 = 7 000 | 11 000 – 1 000 – 4 000 = 6 000        |
| År 2 | 6 000 × 40 % = 2 400                           | 7 000 – 2 400 = 4 600  | 6 000 – 2 400 = 3 600                 |
| År 3 | 3 600 × 40 % = 1 440                           | 4 600 – 1 440 = 3 160  | 3 600 – 1 440 = 2 160                 |

> [!NOTE] 
> Vanligvis når beløpet som beregnes ved å bruke 200% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.



