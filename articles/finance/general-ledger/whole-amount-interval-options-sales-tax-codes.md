---
title: Hele beløp og alternativer for intervallberegning for mva-koder
description: Denne artikkelen beskriver alternativene for feltet Beregningsmåte når det gjelder mva-koder og hvordan mva beregnes for intervaller og hele beløp.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec724030e12e504625b2b102cba25b7eddbf7e96
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978442"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Hele beløp og alternativer for intervallberegning for mva-koder

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver alternativene for feltet Beregningsmåte når det gjelder mva-koder og hvordan mva beregnes for intervaller og hele beløp.

Du kan definere en mva-kode som skal beregnes basert på et helt beløp eller et fakturabeløp. Bruk Beregningsmåte-feltet på hurtigfanen Beregning på Mva-kode-siden for å velge hvordan du vil beregne en mva-kode.
- Hele beløp – mva-satsen brukes for hele det avgiftspliktige beløpet.
- Intervall – Det avgiftspliktige beløpet er inndelt i deler, og hver del er innenfor et intervall som har en bestemt mva-sats. Den delen av beløpet som ligger innen et gitt intervall blir avgiftsbelagt i henhold til mva-satsen for det intervallet. Mva er summen av mva-beløpene som beregnes for hvert beløpsintervall.
  > [!NOTE]                                                                                                                              
  > Intervallalternativet er bare tilgjengelig når du velger Linje i Beregningsmåte-feltet i mva-området på siden Økonomiparametere. 

Intervaller defineres på siden Verdier for merverdiavgiftskode ved å angi minimum og maksimum grensebeløp per mva-sats. For at mva skal kunne beregnes av alle avgiftspliktige beløp, uavhengig av hvilken metode som er valgt, må intervallene oppfylle følgende regler:
-   Det første intervallet må ha en nedre grense på 0.
-   Det siste intervallet må ha en maksimal grense på null, som angir uendelig.
-   Den maksimale grensen til et intervall må være minimumsgrensen til det neste intervallet.

Hvis et beløp er den øvre grensen til det forrige intervallet, og den nedre grensen til det neste intervallet, er det mva-satsen til det første intervallet som brukes på beløpet. Hvis et beløp faller utenfor intervallene som er definert av øvre og nedre grenser, brukes en mva-sats på 0.

## <a name="example-whole-amount-method-of-calculation"></a>Eksempel: beregningsmåte Hele beløp
På Siden Verdier for merverdiavgiftskode defineres mva-satser i følgende intervaller:

|                   |                   |              |
|-------------------|-------------------|--------------|
| **Minimumsgrense** | **Maksimumsgrense** | **Avgiftssats** |
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Mva-satsen beregnes på hele det avgiftspliktige beløpet.

| Avgiftsbelagt beløp (pris) | Beregning    | Merverdiavgift |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Eksempel: Beregningsmåte intervall
På Verdier-siden er mva-satsene angitt i følgende intervaller:

|                   |                   |              |
|-------------------|-------------------|--------------|
| **Minimumsgrense** | **Maksimumsgrense** | **Avgiftssats** |
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Mva er summen av mva-beløpene som beregnes for hvert beløpsintervall.

| Avgiftsbelagt beløp (pris) | Beregning                                                               | Merverdiavgift |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Hvis du vil ha mer informasjon, kan du se [Mva-satser basert på feltene grensegrunnlag og beregningsmetoder](marginal-base-field.md).





