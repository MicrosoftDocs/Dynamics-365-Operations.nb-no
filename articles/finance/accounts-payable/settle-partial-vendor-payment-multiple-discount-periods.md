---
title: Utligne en delvis leverandørbetaling som har flere rabattperioder
description: Denne artikkelen leder deg gjennom et scenario der flere delvise betalinger foretas til en leverandør som har flere kontantrabatter.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da69d61c657ddc168a27a97fe16909d5f60eb4fd
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778044"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Utligne en delvis leverandørbetaling som har flere rabattperioder

[!include [banner](../includes/banner.md)]

Denne artikkelen leder deg gjennom et scenario der flere delvise betalinger foretas til en leverandør som har flere kontantrabatter. 

Leverandør 3054 tilbyr Fabrikam en kontantrabatt på 2 prosent hvis en faktura er betalt innen fem dager og en kontantrabatt på 1 prosent hvis fakturaen er betalt innen 14 dager.

## <a name="invoice"></a>Faktura
28. juni opprettes en faktura på 1 000,00 for leverandøren 3054. April kan se transaksjonene på siden **Leverandørtransaksjoner**.

| Bilag   | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo   | Valuta. |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 28/6/2020 | 10060   |                                      | 1,000.00                              | -1 000,00 | USD      |

De følgende kontantrabattdatoene og -beløpene er tilgjengelige for denne fakturaen.

| Kontantrabattdato | Kontantrabattbeløp | Beløp i transaksjonsvaluta |
|--------------------|----------------------|--------------------------------|
| 3/7/2020           | 20.00                | 980.00                         |
| 12/7/2020          | 10,00                | 990.00                         |
| 25/7/2020          | 0,00                 | 1,000.00                       |

## <a name="payment-on-july-2"></a>Betaling 2. juli
2. juli vil April betale 300,00 for denne fakturaen. Hun oppretter en engangsbetaling ved hjelp av siden **Betalingsjournal** for Leverandører. Hun legger til en linje for leverandør 3054 og angir et betalingsbeløp på **300,00**. April åpner deretter **Utlign transaksjoner**-siden, slik at hun kan merke av for fakturaen som skal utlignes. Hun oppdaterer verdien i feltet **Beløp som skal utlignes** til **300,00** og ser at verdien i feltet **Kontantrabattbeløp som skal brukes** endres til **6,12**. Fordi denne betalingen foretas i den første rabattperioden, brukes en rabatt på 2 prosent.

| Merk | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta. | Beløp som skal utlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 28/6/2020 | 28/7/2020 | 10060   | 1,000.00                       | USD      | 300,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 02/07/2020 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -6,12     |

Fordi det finnes en kontantrabatt, ønsker April å endre betalingsbeløpet slik at totalt utlignet beløp er 300,00 for både betalingen og kontantrabatten. Hun endrer verdien i feltet **Beløp som skal utlignes** til **294,00** og ser at verdien i feltet **Kontantrabattbeløp som skal brukes** endres til **6,00**.

| Merk | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta. | Beløp som skal utlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 28/6/2020 | 28/7/2020 | 10060   | 1,000.00                       | USD      | 294,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 02/07/2020 |
| Kontantrabattbeløp         | -20,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -6.00     |

April posterer betalingen. Hun kan se transaksjonene på siden **Leverandørtransaksjoner**. Hun ser at 300,00 er brukt på fakturaen. Dette beløpet inkluderer en rabatt på 6,00. Derfor er den gjenstående saldoen 700,00.

| Bilag    | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta. |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28/6/2020 | 10060   |                                      | 1,000.00                              | -700,00 | USD      |
| APP-10060  | 2/7/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 2/7/2020  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Betaling 8. juli
8. juli legger April inn en ekstra betaling mot fakturaen. For å skrive inn et beløp åpner hun **Utlign transaksjoner**-siden og klikker deretter **Kontantrabatt**-fanen. Hun åpner dataene og beløpene for de to kontantrabattene som er tilgjengelige. Fordi denne betalingen foretas i den andre rabattperioden, er en rabatt på 1 prosent eller 5,00 tilgjengelig. Dette beløpet beregnes som halve 1-prosentrabatten på 1000,00 eller halvparten av 10,00.

| Kontantrabattdato | Kontantrabattbeløp | Beløp i transaksjonsvaluta |
|--------------------|----------------------|--------------------------------|
| 3/7/2020           | 20.00                | 680,00                         |
| 12/7/2020          | 10,00                | 690,00                         |
| 25/7/2020          | 0,00                 | 700.00                         |

April bestemmer seg å betale 495,00 og bruke kontantrabatten på 5,00. Det totale beløpet som er utlignet er derfor 500,00.

| Merk | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta. | Beløp som skal utlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 28/6/2020 | 28/7/2020 | 10060   | 1,000.00                       | USD      | 495.00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2020 |
| Kontantrabattbeløp         | -10,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | -6,00     |
| Kontantrabattbeløp som skal brukes | -5,00     |

På siden **Leverandørtransaksjoner** ser April at den nye saldoen er 200,00.

| Bilag    | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta. |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28/6/2020 | 10060   |                                      | 1,000.00                              | -200,00 | USD      |
| APP-10060  | 2/7/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 2/7/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12/7/2020 |         | 495.00                               |                                       | 0,00    | USD      |
| DISC-10061 | 12/7/2020 |         | 5.00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Betaling 20. juli
20. juli oppretter April en siste betaling på 200,00. Ingen rabatt brukes fordi betalingen skjer etter begge rabattperiodene. Saldoen på fakturaen er nå 0,00.

| Bilag    | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta. |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28/6/2020 | 10060   |                                      | 1,000.00                              | -200,00 | USD      |
| APP-10060  | 2/7/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 2/7/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12/7/2020 |         | 495.00                               |                                       | 0,00    | USD      |
| DISC-10061 | 12/7/2020 |         | 5.00                                 |                                       | 0,00    | USD      |
| APP-10062  | 20/7/2020 |         | 200.00                               |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
