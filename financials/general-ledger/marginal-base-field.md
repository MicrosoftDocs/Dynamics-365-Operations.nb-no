---
title: "Mva-satser basert på feltene grensegrunnlag og beregningsmetoder"
description: "Denne artikkelen beskriver hvordan verdiene i feltene Grensegrunnlag og Beregningsmetode fastslår avgiftssats(er) i salgs- og kjøpstransaksjoner."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 49cbaba7360fb3a16a70c6889d23608c7fbfa412
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Mva-satser basert på feltene grensegrunnlag og beregningsmetoder

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan verdiene i feltene Grensegrunnlag og Beregningsmetode fastslår avgiftssats(er) i salgs- og kjøpstransaksjoner.

Grensegrunnlag på hurtigfanen Beregning på siden Mva-koder bestemmer hvilket beløp som skal brukes til å velge riktig(e) avgiftssats(er) fra satsene på siden Verdier for merverdiavgiftskode. Beløpstypen i Grensegrunnlag-feltet sammen med metoden i feltet Beregningsmåte fastsetter logikken for å finne riktig(e) avgiftssats(er) for en transaksjon. 

Forskjellige kombinasjoner av verdier i disse feltene gir meget forskjellige mva-beregninger, slik eksemplene nedenfor viser. I eksemplene brukes de samme verdiene for avgiftsintervall, som defineres for hver kode på siden Verdier for merverdiavgiftskode. Åpne denne siden ved å klikke Mva-kode &gt; siden Verdier for merverdiavgiftskode.

> [!Important]                                                                                                                  
> Hvis grensegrunnlaget for én eller flere av merverdiavgiftskodene er basert på linjebeløp eller enheter, må verdien i feltet Beregningsmåte på siden Parameter for økonomimodul settes til Linje. |

## <a name="net-amount-per-line"></a>Nettobeløp per linje
Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av fakturalinjenes nettobeløp, ekskludert andre avgifter.

### <a name="example"></a>Eksempel

Mva-kodene er angitt i følgende intervaller.

| Beløpsintervall    | Avgiftssats |
|--------------------|----------|
| 0 -  50             | 30 %      |
| 50 -100           | 20 %      |
| 100–0 (&gt; 100) | 10 %      |

> [!NOTE]                                                                                                             
> Den øvre grensen på null (0) i det siste intervallet betyr at alle beløp som er større enn 100, inkluderes i intervallet.

Grensegrunnlag: **Nettobeløp per linje** 

Beregningsmetode: **Intervall** 

Du kjøper åtte lamper som koster 25,00 per stykk. 

Nettobeløpet for fakturalinjen er 200,00. 

Avgiften blir beregnet slik: 

Total merverdiavgift = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00 

Totalt fakturabeløp = 200,00 + 35,00 = 235,00 

**Variasjon** 

Hvis fakturaen har to linjer med fire varer på hver linje, blir nettobeløpet på hver linje 100,00, og merverdiavgiften beregnes slik: 

Mva-linje 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Mva-linje 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Total merverdiavgift = 25,00 +25,00 = 50,00 

Totalt fakturabeløp = 200,00 +50,00 = 250,00

## <a name="net-amount-per-unit"></a> Nettobeløp per enhet
Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av verdien av hver enhet, ekskludert andre avgifter. Når et enhetsbasert Grensegrunnlag er valgt, må en Enhet også angis for Mva-koden.

### <a name="example"></a>Eksempel

Mva-kodene er angitt i følgende intervaller.

| Beløp             | Avgiftssats |
|--------------------|----------|
| 0 -  50             | 30 %      |
| 50 -100           | 20 %      |
| 100–0 (&gt; 100) | 10 %      |

Grensegrunnlag: **Nettobeløp per enhet** 

Beregningsmetode: **Hele beløp** 

Du kjøper åtte lamper som koster 25,00 per stykk. 

Nettobeløpet for fakturalinjen er 200,00. 

Mva beregnes på følgende måte: Merverdiavgift per enhet = 25,00 x 30 % = 7,50 Total merverdiavgift = 7,50 x 8 enheter = 60,00 Totalt fakturabeløp = 200,00 + 60,00 = 260.00

## <a name="net-amount-of-invoice-balance"></a> Nettobeløp på fakturasaldo

Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av fakturaens totalverdi, ekskludert andre avgifter.

### <a name="example"></a>Eksempel

Mva-kodene er angitt i følgende intervaller.

| Beløp            | Avgiftssats |
|-------------------|----------|
| 0 -  50            | 30 %      |
| 50 -100          | 20 %      |
| 100–0 (&gt; 100) | 10 %      |

Grensegrunnlag: **Nettobeløp på fakturasaldo** 

Beregningsmetode: **Intervall** En salgsfaktura har to linjer med fire lamper på hver linje for 25,00 per stykk. Nettobeløpet på fakturasaldo er 4 x 25,00 + 4 x 25,00 = 200,00. Mva beregnes på følgende måte: Total merverdiavgift = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Totalt fakturabeløp = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Bruttobeløp per linje

Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av verdien på linjen inkludert alle andre avgifter for linjen.

> [!NOTE]
> I en mva-gruppe kan du bare ha én mva-kode med dette valget i Grensegrunnlag-feltet.

### <a name="example"></a>Eksempel

Mva-kodene er angitt i følgende intervaller.

| Beløp             | Avgiftssats |
|--------------------|----------|
| 0 -  50             | 30 %      |
| 50 -100           | 20 %      |
| 100–0 (&gt; 100) | 10 %      |

Grensegrunnlag: **Bruttobeløp per linje** Beregningsmetode: **Intervall** I tillegg er en annen kode beregnet for en spesialavgift på 5,00 for hver lampe. Avgiften blir lagt til nettobeløpet før beregningen av merverdiavgiften. Du kjøper åtte lamper som koster 25,00 per stykk. Nettobeløpet for fakturalinjen er 200,00. Bruttobeløpet på fakturalinjen er 8 x 25,00 + 8 x 5,00 = 240,00. Mva beregnes på følgende måte: Total merverdiavgift = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 39,00 + 40,00 = 279,00

**Variasjon** 

Hvis fakturaen er opprettet med to fakturalinjer med fire varer på hver linje, blir nettobeløpet per fakturalinje 100,00. Bruttobeløpet (inkludert avgiften på 4 x 5,00) per fakturalinje blir 120,00, og merverdiavgiften er opprettet på følgende måte: Mva-fakturalinje 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Mva-fakturalinje 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Total merverdiavgift = 27,00 + 27,00 = 54,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a> Bruttobeløp per enhet

Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av verdien av enheten inkludert andre avgifter.

> [!NOTE]
> I en mva-gruppe kan du bare ha én mva-kode med dette valget i Grensegrunnlag-feltet.

### <a name="example"></a>Eksempel

Mva-kodene er angitt i følgende intervaller.

| Beløp             | Avgiftssats |
|--------------------|----------|
| 0 -  50             | 30 %      |
| 50 -100           | 20 %      |
| 100–0 (&gt; 100) | 10 %      |

Grensegrunnlag: **Bruttobeløpet per enhet** Det er en spesialavgift på 5,00 for hver lampe. Avgiften blir lagt til nettobeløpet før beregningen av merverdiavgiften. Du kjøper åtte lamper som koster 25,00 per stykk. Bruttobeløpet per enhet er 30,00. Mva beregnes på følgende måte: Merverdiavgift per enhet = 30 x 30 % = 9,00 Total salgsavgift = 9,00 x 8 = 72,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Fakturatotal inkl. andre mva-beløp

Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av fakturaens totalverdi, inkludert andre avgifter.
> [!NOTE]
> I en mva-gruppe kan du bare ha én mva-kode med dette valget i Grensegrunnlag-feltet.

### <a name="example"></a>Eksempel

Mva-kodene er angitt i følgende intervaller.

| Beløp             | Avgiftssats |
|--------------------|----------|
| 0 -  50             | 30 %      |
| 50 -100           | 20 %      |
| 100–0 (&gt; 100) | 10 %      |

Grensegrunnlag: **Fakturatotal inkl. andre mva-beløp** Beregningsmetode: **Intervall**   
Det er en spesialavgift på 5,00 for hver lampe. Avgiften blir lagt til nettobeløpet før beregningen av merverdiavgiften. Du kjøper åtte lamper som koster 25,00 per stykk. Nettobeløpet for fakturaen er 200,00. Bruttobeløpet på fakturaen er 200,00 + (8 x 5,00) = 240,00. Mva beregnes på følgende måte: Total merverdiavgift = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 39,00 + 40,00 = 279,00

For mer informasjon, se [Alternativer for beregning av hele beløp og intervall for mva-koder](whole-amount-interval-options-sales-tax-codes.md) og [Beregningsmetoder for merverdiavgift i Opprinnelse-feltet](sales-tax-calculation-methods-origin-field.md).




