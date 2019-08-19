---
title: Redusere saldoavskriving
description: Denne artikkelen gir en oversikt over redusert saldoverdimetode for avskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd4a8726ca194de2e5d95128659f3b212eaace5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840223"
---
# <a name="reduce-balance-depreciation"></a>Redusere saldoavskriving

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over redusert saldoverdimetode for avskrivning.

Når du definerer en avskrivningsprofil for anleggsmiddel og velger Saldoverdi i Metode-feltet på Avskrivningsprofiler-siden, avskrives anleggsmidler som har denne avskrivningsprofilen tilordnet, med den samme prosenten i hver avskrivningsperiode.

Hvis du vil definere redusert saldoavskrivning, må du også foreta valg i feltene til hurtigfanen Generelt på siden Avskrivningsprofiler. Først velger du et år i Avskrivningsår-feltet. Avhengig av hva du har valgt, vises forskjellige alternativer i Periodefrekvens-feltet, som forklart i avsnittene nedenfor. 

Du må også skrive inn en verdi i Prosent-feltet avskrivningsprofilen. Hvis du velger Full avskrivning, utføres den gjenværende avskrivningen i den siste avskrivningsperioden, og det kan være et stort beløp. Noen land/regioner bytter ikke til lineær avskrivningsmetode. Når beløpet fra den alternative metoden er større enn eller lik beløpet i den primære avskrivningsprofilen og det brukte avskrivningsbeløpet er beløpet for den alternative metoden, utføres bytte. 

Siden et anleggsmiddel aldri helt avskrives basert på en prosentberegning, må du velge Full avskrivning for å få full avskrivning for et anleggsmiddel.

## <a name="select-a-depreciation-year"></a>Velge et avskrivningsår
Du kan velge enten Kalender eller Regnskapsår i Avskrivningsår-feltet på siden Avskrivningsprofiler. Valget definerer alternativene som er tilgjengelige i Periodefrekvens-feltet. Standardvalget er Kalender.

### <a name="calendar"></a>Kalender

Alternativet Kalender oppdaterer avskrivningsgrunnlaget, som vanligvis er netto bokført verdi minus svinnverdi, 1. januar hvert år. I eksemplet på redusert saldoavskrivning senere i dette emnet, er avskrivningsgrunnlaget telleren i det første uttrykket i beregninger i beregningskolonnen. 

Hvis du velger Kalender, er følgende alternativer tilgjengelige i Periodefrekvens-feltet, som definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom hele kalenderåret:

-   Årlige posteringer 31. desember.
-   Månedlige posteringer av et månedlig beløp på slutten av hver kalendermåned.
-   Kvartalsvise posteringer av et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).
-   Halvårlige posteringer av et halvårlig beløp på slutten av hvert kalenderår (30. juni og 31. desember).
-   Daglige posteringer av avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.

Hvis du velger for eksempel Årlig, posteres den årlige avskrivningen bare én gang, den 31. desember i hvert år. Hvis du velger Månedlig, posteres den månedlige avskrivningen hver måned som en tolvdel av det årlige avskrivningsbeløpet.

### <a name="fiscal"></a>Skattemessig

Hvis du velger Regnskapsår i Avskrivningsår-feltet, brukes den lineære avskrivningsmetoden. Det beregnes basert på regnskapsåret, som er definert på siden Regnskapskalendere for den økonomiske kalenderen som er valgt på finanssiden. For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen 1. juli. Regnskapsåret kan være lengre eller kortere enn 12 måneder. Avskrivningen justeres for hver regnskapsperiode. Lengden på det neste regnskapsåret baseres på regnskapsperiodene som du definerer når du oppretter et nytt regnskapsår på siden med regnskapskalendere.


Hvis du velger Regnskapsår, er følgende alternativer tilgjengelige i Periodefrekvens-feltet:

-   Årlige posteringer av totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.
-   Regnskapsperioden posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som avsettes i regnskapsperiodene som er definert for regnskapskalenderen som er valgt på finanssiden, eller for regnskapskalenderen som er valgt for tablået for et anleggsmiddel.

## <a name="example-of-reducing-balance-depreciation"></a>Eksempel på redusert saldoavskrivning

Anta at anskaffelsesprisen for anleggsmidler er 11 000, svinnverdien er 1000 og avskrivningsprosentfaktoren er 30. 

Ifølge Saldoverdi-metoden beregnes 30 prosent av avskrivningsgrunnlaget (netto bokført verdi minus svinnverdi) på slutten av forrige avskrivningsperiode. Avskrivningen for de første tre årene vises i tabellen nedenfor.

| Periode | Beregning av årlig avskrivningsbeløp | Netto bokverdi på slutten av året |
|--------|-------------------------------------------|---------------------------------------|
| År 1 | (11 000 - 1 000) \* 30 % = 3 000           | (11 000 - 1 000) - 3 000 = 7 000      |
| År 2 | (7 000 - 1 000) \* 30 % = 1 800            | (7 000 -1 800) = 5 200                |
| År 3 | (5 200 - 1 000) \* 30 % = 1 260            | (5 200 - 1 260) = 3 940               |


-





