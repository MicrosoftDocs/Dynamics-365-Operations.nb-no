---
title: Bruke en kontantrabatt utenfor kontantrabattperioden
description: Denne artikkelen inneholder to scenarier som viser hvordan en kontantrabatt kan tas, selv om betalingen skjer utenfor kontantrabattperioden.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b1eb5e542acf7496d1a0cf7196716a5de75e4e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780590"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Bruke en kontantrabatt utenfor kontantrabattperioden

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder to scenarier som viser hvordan en kontantrabatt kan tas, selv om betalingen skjer utenfor kontantrabattperioden.

28. juni opprettes en faktura på 2 000,00 for leverandøren 3052. Fakturaen har en kontantrabatt på 1 prosent hvis fakturaen betales innen 14 dager.

## <a name="use-cash-discount-option--always"></a>Alternativet Bruk kontantrabatt = Alltid
April oppretter en betaling 1. juli som er etter rabattdatoen. April åpner siden **Utlign transaksjoner** for å vise transaksjonene som kan utlignes. 

April markerer fakturaen for betaling. Ingen kontantrabatt brukes fordi betalingen er etter rabattdatoen. Leverandøren har imidlertid gitt godkjenning for å få kontantrabatt likevel. Derfor endres verdien i feltet **Bruk kontantrabatt** til **Alltid**.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Kontantrabattdato | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta. | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Alltid            | Inv-10030 | 3052    | 28/6/2020          | 12/7/2020 | 10030   | -2 000,00                      | USD      | -1 980,00        |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2020 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Alltid    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Dato som skal brukes til å beregne rabatter = Valgt dato
Hvis både fakturaen og betalingen er postert, kan fremdeles kontantrabatten brukes når transaksjonene utlignes på siden **Utlign transaksjoner**. April endrer verdien i feltet **Dato som skal brukes til å beregne rabatter** til **Valgt dato**. Hun angir deretter datoen 28. juni, som er i kontantrabattperioden for fakturaen. Denne datoen brukes til å beregne kontantrabatt for transaksjonen. På siden **Utlign åpne transaksjoner** ser April at hele rabatten på 20,00 vises som standard. Fakturalinjen viser at beløpet som skal utlignes er 1 980,00.

| Merk          | Bruk kontantrabatt | Bilag   | Konto | Kontantrabattdato | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|--------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valgt og uthevet | Normal    | Inv-10030 | 3052    | 28/6/2020         | 12/7/2020 | 10030   | -2 000,00                      | USD      | -1 980,00        |
| Valgt                 | Normal    | APP-10030 | 3052    | 15/7/2020          | 15/7/2020 |         | 500.00                         | USD      | 500.00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**. Rabattbeløpet som brukes er 20,00, fordi beløpet som skal utlignes for fakturaen er standardbeløpet 1,980.00.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2020 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -20,00    |

April oppdaterer verdien i feltet **Beløp som skal utlignes** til **500,00**. Verdien i feltet **Kontantrabattbeløp som skal brukes** beregnes som **5,05**.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt og uthevet | Normal            | Inv-10030 | 3052    | 28/6/2020 | 12/7/2020 | 10030   | 2,000.00                       | USD      | -500,00          |
| Valgt                 | Normal            | APP-10030 | 3052    | 15/7/2020 | 15/7/2020 |         | 500.00                         | USD      | 500.00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**. Verdien i feltet **Kontantrabattbeløp som skal brukes** er **5,05**, fordi beløpet som skal utlignes for fakturaen ble endret til betalingsbeløpet, 500,00.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2020 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
