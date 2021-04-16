---
title: 125 prosent redusert saldoavskrivning
description: Denne artikkelen gir en oversikt over avskrivningsmetoden 125 prosent saldoavskrivning.
author: saraschi2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d05ec02d47a563c0d7ae7cb0fafdbad45bd140
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827200"
---
# <a name="125-percent-reducing-balance-depreciation"></a>125 prosent redusert saldoavskrivning

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over avskrivningsmetoden 125 prosent saldoavskrivning.

Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **125 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt til avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode. Denne prosenten beregnes på grunnlag av anleggsmidlets levetid. Hvis anleggsmidlet for eksempel har en levetid på fem år, beregnes prosenten som 25 prosent (125 % ÷ 5).

Hvis du vil definere 125 % saldoverdiavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**. Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.

## <a name="select-a-depreciation-year"></a>Velge et avskrivningsår
Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden. Standardverdien er **Kalender**. 

Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet. Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.

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

Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 125 % saldoverdiavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden. Regnskapskalendere defineres på **Regnskapskalendere**-siden. 

For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli. Regnskapsåret kan være lengre eller kortere enn 12 måneder. Avskrivningen justeres automatisk for hver periode, og lengden på det neste regnskapsåret fastslås ved oppsettet av perioder på den siden **Regnskapskalendere**. 

Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:

-   **Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.
-   **Regnskapsperiode** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret. Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.

## <a name="example-of-125-reducing-balance-depreciation"></a>Eksempel på 125 % saldoverdiavskrivning

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Anskaffelseskostnad               | 11 000 |
| Restverdi                  | 1 000  |
| Avskrivningsgrunnlag              | 10 000 |
| Levetid i år             | 5      |
| Årlig avskrivningsprosent | 25 %    |

Metoden 125 % saldoavskrivning dividerer 125 prosent med antall levetidsår. Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.

| Periode | Beregning av årlig avskrivningsbeløp | Bokført verdi                    | Netto bokverdi på slutten av året |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| År 1 | (11 000 – 1 000) × 25 % = 2 500                | (11 000 – 2 500) = 8 500      | (11 000 – 1 000 – 2 500) = 7 500      |
| År 2 | 7 500 × 25 % = 1 875                           | (8 500 – 1 875) = 6 625       | (7 500 – 1 875) = 5 625               |
| År 3 | 5 625 × 25 % = 1 406,25                        | (6 625 – 1 406,25) = 5 218.75 | (5 625 – 1 406,25) = 4 218,75         |

> [!NOTE] 
> Vanligvis når beløpet som beregnes ved å bruke 125% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]