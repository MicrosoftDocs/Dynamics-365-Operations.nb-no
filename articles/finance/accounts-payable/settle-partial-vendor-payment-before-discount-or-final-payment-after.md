---
title: Utligne en delvis leverandørbetaling før rabattdatoen og en endelige betaling etter rabattdatoen
description: Denne artikkelen veileder deg gjennom et scenario der flere delvise betalinger foretas, noen innenfor kontantrabattperioden og andre utenfor kontantrabattperioden.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a30bd1c032d27405c17388465eb813d6c87c270
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971984"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Utligne en delvis leverandørbetaling før rabattdatoen og en endelige betaling etter rabattdatoen

[!include [banner](../includes/banner.md)]

Denne artikkelen veileder deg gjennom et scenario der flere delvise betalinger foretas, noen innenfor kontantrabattperioden og andre utenfor kontantrabattperioden.

Fabrikam kjøper varer fra leverandøren 3057. Fabrikam får en kontantrabatt på 1 prosent hvis fakturaen er betalt innen 14 dager. Fakturaer må betales innen 30 dager. Leverandøren lar også Fabrikam få kontantrabatter på delvise betalinger. Du finner parameterne for utligning på siden **Leverandørparametere**.

## <a name="invoice-on-june-25"></a>Faktura 25. juni
25. juni registreres og posteres en faktura på 1 000,00 for leverandøren 3057. April kan se transaksjonene på siden **Leverandørtransaksjoner**.

| Bilag   | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo   | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fakt-10020 | Faktura          | 25/6/2015 | 10020   |                                      | 1 000,00                              | -1 000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Delvis betaling 2. juli
2. juli ønsker April å utligne 300,00 for denne fakturaen. Betalingen er kvalifisert for rabatt fordi Fabrikam får rabatter på delbetalinger. Derfor betaler April 297,00 og får 3,00 i rabatt. Hun oppretter en betalingsjournal og angir en linje for leverandør 3057. Hun åpner siden **Utlign transaksjoner**, slik at hun kan merke fakturaen for utligning.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | Fakt-10020 | 3057    | 25/6/2015 | 25/7/2015 | 10020   | -1 000,00                      | USD      | -297,00          |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | -10,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -3,00     |

April posterer deretter betalingen. Fakturaen har nå en saldo på 700,00. April kan se transaksjonene på siden **Leverandørtransaksjoner**.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10020  | Faktura          | 25/6/2015 | 10020   |                                      | 1 000,00                              | -700,00 | USD      |
| APP-10020  | Betaling          | 1/7/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| RAB-10020 | Kontantrabatt    | 1/7/2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Gjenstående betaling 15. juli, Bruk kontantrabatt = Normal
April betaler resten av fakturaen 15. juli, som er etter rabattperioden. På siden **Utlign åpne transaksjoner** vises ingen rabattbeløpet i feltet **Beregnet kontantrabatt**, og verdien i feltet **Kontantrabattbeløp** er **0,00**. Når April betaler de gjenværende 700,00, hentes ingen ekstra rabatt.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | Fakt-10020 | 3057    | 25/6/2015 | 25/7/2015 | 10020   | -700,00                        | USD      | -700,00          |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**. April kan se at hun allerede har fått en 3,00-rabatt.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 0,00      |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | -3,00     |
| Kontantrabattbeløp som skal brukes | 0,00      |

April posterer deretter betalingen. Når hun åpner siden **Leverandørtransaksjoner**, ser hun at fakturaen har en saldo på 0,00. Hun ser også at det finnes to betalinger. Én betaling er på 297,00 og har en rabatt på 3,00, og den andre betalingen er på 700,00.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10020  | Faktura          | 25/6/2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 1/7/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| RAB-10020 | Kontantrabatt    | 1/7/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 15/7/2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Gjenstående betaling 15. juli, Bruk kontantrabatt = Alltid
Hvis leverandøren lar April ta rabatt selv om hun betaler etter rabattdatoen, kan hun endre verdien i feltet **Bruk kontantrabatt** til **Alltid**. Innstillingen **Beregn kontantrabatter for delvise betalinger** overstyres, og rabatten utføres. Betalingsbeløpet er 693,00, og rabatten er de gjenværende 7,00.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valgt | Alltid            | Fakt-10020 | 3057    | 25/6/2015 | 25/7/2015 | 10020   | 700,00                               |                                       | USD      | -693,00          |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 7,00      |
| Bruk kontantrabatt            | Alltid    |
| Kontantrabatt brukt          | -3,00     |
| Kontantrabattbeløp som skal brukes | -7,00     |

April posterer deretter betalingen. Når hun åpner siden **Leverandørtransaksjoner**, ser hun at fakturaen har en saldo på 0,00. Hun ser også at det finnes to betalinger. Én betaling er på 297,00 og har en rabatt på 3,00, og den andre betalingen er på 693,00 og har en rabatt på 7,00.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10020  | Faktura          | 25/6/2015 | 10020   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 1/7/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| RAB-10020 | Kontantrabatt    | 1/7/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 15/7/2015 |         | 693,00                               |                                       | 0,00    | USD      |
| RAB-10021 | Kontantrabatt    | 15/7/2015 |         | 7,00                                 |                                       | 0,00    | USD      |





