---
title: Mva-beregning og -avrunding
description: Denne artikkelen gir en oversikt over beregning og avrunding av merverdiavgift, og forklarer parameterne for mva-beregning og avrunding.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939240"
---
# <a name="sales-tax-calculation-and-rounding"></a>Mva-beregning og -avrunding

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over beregning og avrunding av merverdiavgift i Microsoft Dynamics 365 Finance. Det forklarer også parameterne som brukes i oppsettet for mva-beregning og -avrunding, og hvordan disse parameterne fungerer sammen.

## <a name="parameters"></a>Parametere

Flere parametere styrer beregning og avrunding av merverdiavgift:

- **Beregningsmetode** – Denne parameteren er angitt på siden **Parametere for økonomimodul** og definerer om avgiftsgrunnlagsbeløpet skal beregnes per dokument eller per linje. Hvis **Grensegrunnlag**-parameteren for mva-koden er satt til **Nettobeløp for fakturasaldo**, beregnes avgiftsgrunnlagsbeløpet alltid per dokument, uavhengig av innstillingen for denne parameteren.
- **Avrunding** – Denne parameteren er angitt for mva-gruppen, og definerer om mva-beløpet skal avrundes per mva-kode eller per kombinasjon av mva-kode.
- **Opprinnelse** – Denne parameteren er definert for mva-koden, og definerer hvordan mva-beløpet skal beregnes. Hvis du vil ha mer informasjon, kan du se [Beregningsmåter for merverdiavgift i grunnlagsfeltet](sales-tax-calculation-methods-origin-field.md).
- **Grensegrunnlag** – Denne parameteren er satt for mva-koden og bestemmer hvilket beløp som skal brukes til å velge riktig(e) avgiftssats(er) fra satsene på siden **Verdier for merverdiavgiftskode**. Hvis du vil ha mer informasjon, kan du se [Mva-satser basert på feltene grensegrunnlag og beregningsmetoder](marginal-base-field.md).
- **Regel for avrunding av merverdiavgift** – Denne parameteren er angitt for mva-koden, og definerer hvordan det bestemte mva-beløpet skal avrundes, inkludert avrundingspresisjonen og avrundingsmetoden.

Resten av denne artikkelen gir noen vanlige eksempler på mva-beregning og avrunding som bruker en kombinasjon av de foregående parameterne.

## <a name="scenario-for-the-examples"></a>Scenario for eksemplene

- Det er to linjer i det avgiftspliktige dokumentet, og avgiftsgrunnlagsbeløpet for hver linje er 42.42.
- To mva-koder er definert for hver linje: mva-kode 1 og mva-kode 2.
- Avgiftssatsen for både mva-kode 1 og avgiftskode 2 er 10 prosent.
- Prisen er uten mva.
- Avrundingspresisjonen er 0,01.
- Avrundingsmetoden er **Avrundes opp**.

## <a name="example-1"></a>Eksempel 1

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter    | Grunnlag                   | Grensegrunnlag       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Linje               | Mva-kode | Prosent av nettobeløp | Nettobeløp per linje |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ------------| ---------------| --------------| -----------------|
| 1           | Kode 1         | 42.42         | 4.25             |
| 1           | Kode 2         | 42.42         | 4.25             |
| 2           | Kode 1         | 42.42         | 4.25             |
| 2           | Kode 2         | 42.42         | 4.25             |

Avgiftsgrunnbeløp beregnes per linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Avgiften beregnes per mva-kode:

- **Linje 1:**

    - Mva-beløp for mva-kode 1 = 42,42 &times;10 prosent = 4,242
    - Mva-beløp for mva-kode 2 = 42,42 &times;10 prosent = 4,242

- **Linje 2:**

    - Mva-beløp for mva-kode 1 = 42,42 &times;10 prosent = 4,242
    - Mva-beløp for mva-kode 2 = 42,42 &times;10 prosent = 4,242

Avgiften avrundes per mva-kode:

- **Linje 1:**

    - Avrundet mva-beløp for mva-kode 1 = 4,25
    - Avrundet mva-beløp for mva-kode 2 = 4,25

- **Linje 2:**

    - Avrundet mva-beløp for mva-kode 1 = 4,25
    - Avrundet mva-beløp for mva-kode 2 = 4,25

## <a name="example-2"></a>Eksempel 2

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter    | Grunnlag                   | Grensegrunnlag                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Linje/total         | Mva-kode | Prosent av nettobeløp | Nettobeløp på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.25             |
| 1           | Kode 2         | 42.42         | 4.25             |
| 2           | Kode 1         | 42.42         | 4.24             |
| 2           | Kode 2         | 42.42         | 4.24             |

Avgiftsgrunnbeløp beregnes per dokument:

- Avgiftsgrunnlagsbeløp = 42,42 + 42,42 = 84,84

Avgiften beregnes per mva-kode:

- Mva-beløp for mva-kode 1 = 84,84 &times;10 prosent = 8,484
- Mva-beløp for mva-kode 2 = 84,84 &times;10 prosent = 8,484

Avgiften avrundes per mva-kode:

- Avrundet mva-beløp for mva-kode 1 = 8,49
- Avrundet mva-beløp for mva-kode 2 = 8,49

Den avrundede mva-beløpet tildeles hver linjer per mva-kode:

- Fordel det avrundede mva-beløpet for mva-kode 1 (8,49) til linje 1 (4,25) og linje 2 (4,24).
- Fordel det avrundede mva-beløpet for mva-kode 2 (8,49) til linje 1 (4,25) og linje 2 (4,24).

## <a name="example-3"></a>Eksempel 3

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter    | Grunnlag                              | Grensegrunnlag       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Linje               | Mva-kode | Beregnet prosent av nettobeløp | Nettobeløp per linje |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.72             |
| 1           | Kode 2         | 42.42         | 4.72             |
| 2           | Kode 1         | 42.42         | 4.72             |
| 2           | Kode 2         | 42.42         | 4.72             |

Avgiftsgrunnbeløp beregnes per linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Avgiften beregnes per mva-kode:

- **Linje 1:**

    - Mva-beløp for mva-kode 1 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133
    - Mva-beløp for mva-kode 2 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133

- **Linje 2:**

    - Mva-beløp for mva-kode 1 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133
    - Mva-beløp for mva-kode 2 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133

Avgiften avrundes per mva-kode:

- **Linje 1:**

    - Avrundet mva-beløp for mva-kode 1 = 4,72
    - Avrundet mva-beløp for mva-kode 2 = 4,72

- **Linje 2:**

    - Avrundet mva-beløp for mva-kode 1 = 4,72
    - Avrundet mva-beløp for mva-kode 2 = 4,72

## <a name="example-4"></a>Eksempel 4

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter    | Grunnlag                              | Grensegrunnlag                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Linje/total         | Mva-kode | Beregnet prosent av nettobeløp | Nettobeløp på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.72             |
| 1           | Kode 2         | 42.42         | 4.72             |
| 2           | Kode 1         | 42.42         | 4.71             |
| 2           | Kode 2         | 42.42         | 4.71             |

Avgiftsgrunnbeløp beregnes per dokument:

- Avgiftsgrunnlagsbeløp = 42,42 + 42,42 = 84,84

Avgiften beregnes per mva-kode:

- Mva-beløp for mva-kode 1 = 84,84 &times; 10 prosent &divide; (1 – 10 prosent) = 9,4267
- Mva-beløp for mva-kode 2 = 84,84 &times; 10 prosent &divide; (1 – 10 prosent) = 9,4267

Avgiften avrundes per mva-kode:

- Avrundet mva-beløp for mva-kode 1 = 9,43
- Avrundet mva-beløp for mva-kode 2 = 9,43

Den avrundede mva-beløpet tildeles hver linjer per mva-kode:

- Fordel mva-beløpet for mva-kode 1 (9,43) til linje 1 (4,72) og linje 2 (4,71).
- Fordel mva-beløpet for mva-kode 2 (9,43) til linje 1 (4,72) og linje 2 (4,71).

## <a name="example-5"></a>Eksempel 5

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter                | Grunnlag                   | Grensegrunnlag       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Linje               | Mva-kodekombinasjon | Prosent av nettobeløp | Nettobeløp per linje |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.25             |
| 1           | Kode 2         | 42.42         | 4.24             |
| 2           | Kode 1         | 42.42         | 4.24             |
| 2           | Kode 2         | 42.42         | 4.24             |

Avgiftsgrunnbeløp beregnes per linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Avgiften beregnes per mva-kode:

- **Linje 1:**

    - Mva-beløp for mva-kode 1 = 42,42 &times;10 prosent = 4,242
    - mva-beløp for mva-kode 2 = 42,42 &times;10 prosent = 4,242

- **Linje 2:**

    - Mva-beløp for mva-kode 1 = 42,42 &times;10 prosent = 4,242
    - Mva-beløp for mva-kode 2 = 42,42 &times;10 prosent = 4,242

Avgiften avrundes per mva-kodekombinasjon:

- Totalt mva-beløp = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, som avrundes opp til 16,97

Den avrundede mva-beløpet tildeles hver linjer per mva-kode:

- Tildel mva-beløpet (16,97) til linje 1 og linje 2:

    - **Linje 1:**

        - Mva-beløp for mva-kode 1 = 4,25
        - Mva-beløp for mva-kode 2 = 4,24

    - **Linje 2:**

        - Mva-beløp for mva-kode 1 = 4,24
        - Mva-beløp for mva-kode 2 = 4,24

## <a name="example-6"></a>Eksempel 6

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter                | Grunnlag                   | Grensegrunnlag                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Linje/total         | Mva-kodekombinasjon | Prosent av nettobeløp | Nettobeløp på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.25             |
| 1           | Kode 2         | 42.42         | 4.24             |
| 2           | Kode 1         | 42.42         | 4.24             |
| 2           | Kode 2         | 42.42         | 4.24             |

Avgiftsgrunnbeløp beregnes per dokument:

- Avgiftsgrunnlagsbeløp = 42,42 + 42,42 = 84,84

Avgiften beregnes per mva-kode:

- Mva-beløp for mva-kode 1 = 84,84 &times;10 prosent = 8,484
- Mva-beløp for mva-kode 2 = 84,84 &times;10 prosent = 8,484

Avgiften avrundes per mva-kodekombinasjon:

- Totalt mva-beløp = 8,484 + 8,484 = 16,968, som avrundes opp til 16,97

Den avrundede mva-beløpet tildeles hver linjer per mva-kode:

- Tildel mva-beløpet (16,97) til linje 1 og linje 2:

    - **Linje 1:**

        - Mva-beløp for mva-kode 1 = 4,25
        - Mva-beløp for mva-kode 2 = 4,24

    - **Linje 2:**

        - Mva-beløp for mva-kode 1 = 4,24
        - Mva-beløp for mva-kode 2 = 4,24

## <a name="example-7"></a>Eksempel 7

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter                | Grunnlag                              | Grensegrunnlag       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Linje               | Mva-kodekombinasjon | Beregnet prosent av nettobeløp | Nettobeløp per linje |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.72             |
| 1           | Kode 2         | 42.42         | 4.71             |
| 2           | Kode 1         | 42.42         | 4.71             |
| 2           | Kode 2         | 42.42         | 4.72             |

Avgiftsgrunnbeløp beregnes per linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Avgiften beregnes per mva-kode:

- **Linje 1:**

    - Mva-beløp for mva-kode 1 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133
    - Mva-beløp for mva-kode 2 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133

- **Linje 2:**

    - Mva-beløp for mva-kode 1 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133
    - Mva-beløp for mva-kode 2 = 42,42 &times; 10 prosent &divide; (1 – 10 prosent) = 4,7133

Avgiften avrundes per mva-kodekombinasjon:

- Totalt mva-beløp = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, som avrundes opp til 18,86

Den avrundede mva-beløpet tildeles hver linjer per mva-kode:

- Tildel mva-beløpet (18,86) til linje 1 og linje 2:

    - **Linje 1:**

        - Mva-beløp for mva-kode 1 = 4,72
        - Mva-beløp for mva-kode 2 = 4,71

    - **Linje 2:**

        - Mva-beløp for mva-kode 1 = 4,71
        - Mva-beløp for mva-kode 2 = 4,72

## <a name="example-8"></a>Eksempel 8

### <a name="parameter-values"></a>Parameterverdier

| Beregningsmåte | Avrunding etter                | Grunnlag                              | Grensegrunnlag                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Linje/total         | Mva-kodekombinasjon | Beregnet prosent av nettobeløp | Nettobeløp på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregning og avrundingsfunksjon

| Linjenummer | Mva-kode | Beløpsgrunnlag | Mva-beløp |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42.42         | 4.72             |
| 1           | Kode 2         | 42.42         | 4.71             |
| 2           | Kode 1         | 42.42         | 4.71             |
| 2           | Kode 2         | 42.42         | 4.72             |

Avgiftsgrunnbeløp beregnes per dokument:

- Avgiftsgrunnlagsbeløp = 42,42 + 42,42 = 84,84

Avgiften beregnes per mva-kode:

- Mva-beløp for mva-kode 1 = 84,84 &times; 10 prosent &divide; (1 – 10 prosent) = 9,4267
- Mva-beløp for mva-kode 2 = 84,84 &times; 10 prosent &divide; (1 – 10 prosent) = 9,4267

Avgiften avrundes per mva-kodekombinasjon:

- Totalt mva-beløp = 9,4267 + 9,4267 = 18,8534, som avrundes opp til 18,86

Den avrundede mva-beløpet tildeles hver linjer per mva-kode:

- Tildel mva-beløpet (18,86) til linje 1 og linje 2:

    - **Linje 1:**

        - Mva-beløp for mva-kode 1 = 4,72
        - Mva-beløp for mva-kode 2 = 4,71

    - **Linje 2:**

        - Mva-beløp for mva-kode 1 = 4,71
        - Mva-beløp for mva-kode 2 = 4,72

## <a name="additional-resources"></a>Tilleggsressurser

- [Beregningsmåter for merverdiavgift i grunnlagsfeltet](sales-tax-calculation-methods-origin-field.md)
- [Mva-satser basert på feltene grensegrunnlag og beregningsmetoder](marginal-base-field.md)
- [Hele beløp og alternativer for intervallberegning for mva-koder](whole-amount-interval-options-sales-tax-codes.md)
