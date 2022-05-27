---
title: Avrundingsregler for avgiftsberegning
description: Dette emnet gir informasjon om avrundingsreglene i avgiftsberegningsparameterne for avgiftsberegningstjenesten.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 167db4d836aa754509bb28677916a30901cebbbb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694181"
---
# <a name="tax-calculation-rounding-rules"></a>Avrundingsregler for avgiftsberegning

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om hvordan avrundingsreglene fungerer i avgiftsberegningsparameterne for avgiftsberegningstjenesten.

> [!NOTE] 
> Når tjenesten for avgiftsberegning er aktivert, er ikke avrundingsreglene på sidene **Mva-kode** og **Mva-gruppe** gyldige.

Du kan vise konfigurasjonen til avrundingsregler for avgiftsberegningstjenesten i delen **Avrundingsregel for mva** på hurtigfanen **Beregning** på fanen **Generelt** på siden **Parametere for avgiftsberegning** (**Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Parametere for avgiftsberegning**).

[![Konfigurasjon av avrundingsregel på siden Parametere for avgiftsberegning](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Feltene **Avrundingspresisjon** og **Avrundingsmetode** bestemmer hvordan beregnede beløp i nyttelast fra avgiftsberegningstjenesten avrundes.

## <a name="rounding-precision"></a>Avrundingspresisjon

Feltet **Avrundingspresisjon** støtter en verdi som har opptil seks desimalplasser. Hvis du for eksempel setter feltet **Avrundingspresisjon** til **0,000000**, avrundes beregnede beløp til seks desimalplasser og sendes deretter til Microsoft Dynamics 365 Finance. Hvis for eksempel avrundingsmetoden **Normal** brukes, blir beløpet **987,1234567** rundet av til **987,123457**.

> [!NOTE]
> Finance avrunder beløp i henhold til valutaavrundingsreglene. Derfor påvirkes avgiftsbeløpene som vises og registreres i transaksjoner, av både avrundingsregler for avgiftsberegning og avrundingsregler for valuta.

## <a name="rounding-method"></a>Avrundingsmetode

Avrundingsmetoden for avgiftsberegning kan konfigureres for hver juridiske enhet. I feltet **Avrundingsmetode** kan du velge mellom tre alternativer: **Normal**, **Nedover** og **Avrundes opp**.

### <a name="rounding-example"></a>Avrundingseksempel

Følgende tabell gir et eksempel som viser hvordan beløpet **987,345** avrundes for forskjellige kombinasjoner av avrundingspresisjoner og avrundingsmetoder.

<table>
<thead>
<tr>
<th rowspan="2">Avrundingsmetode</th>
<th colspan="8">Avrundingspresisjon</th>
</tr>
<tr>
<th>0.00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10,00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normal</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Nedover</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Avrundes opp</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Beregnings- og avrundingslogikk for avgiftsbeløp kan konfigureres i henhold til avgiftsregler.

## <a name="rounding-by"></a>Avrunding etter 

I feltet **Avrunding etter** velger du avrundingsprinsippet som gjelder for avgiftene. Følgende alternativer er tilgjengelige:

- **Mva-koder** – Avrund mva-beløpet innenfor hver mva-kode.
- **Mva-kodekombinasjoner** – Avrund mva-beløpet i mva-kodekombinasjonen på linjen.

## <a name="calculation-method"></a>Beregningsmåte

I feltet **Beregningsmetode** velger du om avgifter på fakturaer skal beregnes for hver linje eller for alle linjene. Følgende alternativer er tilgjengelige:

- **Linje** – Beregner mva-beløpet linje for linje. Avgiftsbeløpet på hver linje påvirkes ikke av avgiftsbeløpet på andre linjer.
- **Totalt** – Beregn mva-beløpet på tvers av alle linjene i ett dokument.

### <a name="rounding-calculation-example"></a>Eksempel på avrundingsberegning

Dette eksemplet viser de forskjellige beregningene som kan utføres for én faktura, for ulike kombinasjoner av verdiene **Avrunding etter** og **Beregningsmetode**. For dette eksemplet er følgende oppsett på plass:

- Fakturaen har fire linjer.
- Det finnes to avgiftskoder: **MVA1** (10 prosent) og **MVA2** (10 prosent).
- Avrundingspresisjonen er satt til **0,01**.
- Avrundingsmetoden er satt til **Avrundes opp**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Avrunding etter = avgiftskoder og beregningsmetode = linje

| Linjenummer | Nettobeløp for linje | Bestemte avgiftskoder | Avgiftsbeløp før avrunding | Avrundet avgiftsbeløp |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | MVA1                 | 1.111                      | 1.12               |
| 2           | 22.22           | MVA1; MVA2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | MVA1                 | 3.333                      | 3.34               |
| 4           | 44.44           | MVA1; MVA2           | 4,444; 4,444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Avrunding etter = avgiftskodekombinasjoner og beregningsmetode = linje

| Linjenummer | Nettobeløp for linje | Bestemte avgiftskoder | Avgiftsbeløp før avrunding | Avrundet avgiftsbeløp |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | MVA1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | MVA1; MVA2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | MVA1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | MVA1; MVA2           | 4,444; 4,444               | 4,45; 4,44         |

\* Linje 2 = Rund av\[22,22 × (10 prosent + 10 prosent)\] = 2.23 + 2.22

\*\* Line 4 = Rund av\[44,44 × (10 prosent + 10 prosent)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Avrunding etter = avgiftskoder og beregningsmetode = totalt

| Linjenummer | Nettobeløp for linje | Bestemte avgiftskoder | Avgiftsbeløp før avrunding | Avrundet avgiftsbeløp |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | MVA1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | MVA1\*; MVA2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | MVA1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | MVA1\*; MVA2\*\*     | 4,444; 4,444               | 4,44; 4,44         |

\*MVA1 (linje 1, linje 2, linje 3, linje 4) = Rund av\[(11,11 + 22,22 + 33,33 + 44,44) × 10 prosent\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* MVA2 (linje 2, linje 4) = Rund av\[(22,22 + 44,44) × 10 prosent\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Avrunding etter = avgiftskodekombinasjoner og beregningsmetode = totalt

| Linjenummer | Nettobeløp for linje | Bestemte avgiftskoder | Avgiftsbeløp før avrunding | Avrundet avgiftsbeløp |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | MVA1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | MVA1; MVA2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | MVA1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | MVA1; MVA2           | 4,444; 4,444               | 4,44; 4,45         |

\* Linje 1, linje 3 = Rund av\[(11,11 + 33,33) × 10 prosent\] = 1,12 + 3,33

\*\* Linje 2, linje 4 = Rund av\[(22,22 + 44,44) × (10 prosent + 10 prosent)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
