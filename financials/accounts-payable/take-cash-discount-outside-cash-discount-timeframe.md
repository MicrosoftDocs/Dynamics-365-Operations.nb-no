---
title: Ta en kontantrabatt utenfor perioden kontantrabatt
description: Denne artikkelen inneholder to scenarier som viser hvordan en kontantrabatt kan tas, selv om betalingen skjer utenfor kontantrabattperioden.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: bea9565f488c01e5e6aede8cabe73ac13b75dacb
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Ta en kontantrabatt utenfor perioden kontantrabatt

Denne artikkelen inneholder to scenarier som viser hvordan en kontantrabatt kan tas, selv om betalingen skjer utenfor kontantrabattperioden.

I juni 28 oppretter April en faktura for 2,000.00 for 3052 for leverandør. Fakturaen har en kontantrabatt på 1 prosent hvis fakturaen er betalt i 14 dager.

## <a name="use-cash-discount-option--always"></a>Alternativet Bruk kontantrabatt = Alltid
April oppretter en betaling 1. juli som er etter rabattdatoen. April åpner siden **Utlign transaksjoner** for å vise transaksjonene som kan utlignes. 

April markerer fakturaen for betaling. Ingen kontantrabatt brukes fordi betalingen er etter rabattdatoen. Leverandøren har imidlertid gitt April godkjenning for å få kontantrabatt likevel. Derfor April endrer verdien i den **Bruk kontantrabatt** feltet til **alltid**.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Kontantrabattdato | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Alltid            | Inv-10030 | 3052    | 28/6/2015          | 12/7/2015 | 10030   | -2 000,00                      | USD      | -1 980,00        |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2015 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Alltid    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Dato som skal brukes til å beregne rabatter = Valgt dato
Hvis både fakturaen og betalingen er postert, kan fremdeles kontantrabatten brukes når transaksjonene utlignes på siden **Utlign transaksjoner**. April endrer verdien i feltet **Dato som skal brukes til å beregne rabatter** til **Valgt dato**. Hun angir deretter datoen 28. juni, som er i kontantrabattperioden for fakturaen. Denne datoen brukes til å beregne kontantrabatt for transaksjonen. På siden **Utlign åpne transaksjoner** ser April at hele rabatten på 20,00 vises som standard. Fakturalinjen viser at beløpet som skal utlignes er 1 980,00.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Kontantrabattdato | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valgt og uthevet | Normal            | Inv-10030 | 3052    | 28/6/2015          | 12/7/2015 | 10030   | -2 000,00                      | USD      | -1 980,00        |
| Valgt                 | Normal            | APP-10030 | 3052    | 15/7/2015          | 15/7/2015 |         | 500,00                         | USD      | 500,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**. Rabattbeløpet som brukes er 20,00, fordi beløpet som skal utlignes for fakturaen er standardbeløpet 1,980.00.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2015 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -20,00    |

April oppdaterer verdien i feltet **Beløp som skal utlignes** til **500,00**. Verdien i feltet **Kontantrabattbeløp som skal brukes** beregnes som **5,05**.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt og uthevet | Normal            | Inv-10030 | 3052    | 28/6/2015 | 12/7/2015 | 10030   | 2 000,00                       | USD      | -500,00          |
| Valgt                 | Normal            | APP-10030 | 3052    | 15/7/2015 | 15/7/2015 |         | 500,00                         | USD      | 500,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**. Verdien i feltet **Kontantrabattbeløp som skal brukes** er **5,05**, fordi beløpet som skal utlignes for fakturaen ble endret til betalingsbeløpet, 500,00.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2015 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -5,05     |




