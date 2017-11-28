---
title: Utligne en delvis kundebetaling som har flere rabattperioder
description: "Denne artikkelen viser hvordan delvis kundebetalinger gjøres opp når det er flere rabattperioder."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ac64ece82abe75f3cba437b1ec1af499fbbce8e4
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Utligne en delvis kundebetaling som har flere rabattperioder

[!include[banner](../includes/banner.md)]


Denne artikkelen viser hvordan delvis kundebetalinger gjøres opp når det er flere rabattperioder.

Fabrikam tilbyr kunde 4031 to kontantrabattperioder. Kunden mottar en kontantrabatt på 2 prosent hvis fakturaen er betalt innen fem dager og 1% kontantrabatt hvis fakturaen er betalt innen 14 dager. Fabrikam tilbyr også kontantrabatter på delvise betalinger. Du finner parameterne for utligning på siden **Kundeparametere**.

## <a name="invoice"></a>Faktura
25. juni legger Magnus inn og posterer en faktura på 1 000,00 for kunden 4031. Når han ser gjennom kontantrabattene for denne fakturaen, ser Magnus at kunde 4031 får 20,00 i rabatt hvis fakturaen betales innen 30. juni. Hvis fakturaen betales innen 9. juli, får kunden 10,00 i rabatt.

| Kontantrabattdato | Kontantrabattbeløp | Beløp i transaksjonsvaluta |
|--------------------|----------------------|--------------------------------|
| 30/6/2015          | 20,00                | 980,00                         |
| 9/7/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1 000,00                       |

Magnus kan vise denne transaksjonen på siden **Kundetransaksjoner**.

| Bilag   | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Faktura          | 25/6/2015 | 10030   | 1 000,00                             |                                       | 1 000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Delbetaling før kontantrabattdatoen
På 28. juni gjør kunden 4031 en delvis innbetaling av 294,00. Fordi 28. juni er innenfor den første kontantrabattperioden utnytter kunden 6,00 rabatt. På siden **Utlign transaksjoner** er verdien for **kontantrabattbeløpet** 20,00 og verdien for **Kontantrabattbeløp som skal brukes** er 6,00.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10030 | 4031    | 25/6/2015 | 25/7/2015 | 10030   | 1 000,00                       | USD      | 294,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**. Hvis du ikke endrer verdien for **beløp som skal utlignes** til **294,00**, vil verdiene for **kontantrabattbeløpet** som vises, variere. Imidlertid vil 6,00 behandles som kontantrabatten når betalingen er postert, fordi utligning justerer automatisk verdien for **beløp som skal utlignes** for deg.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 30/6/2015 |
| Kontantrabattbeløp         | 20,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 6,00      |

Når Magnus posterer betalingen, er fakturasaldoen 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Delbetaling før den andre kontantrabattdatoen
8. juli betaler kunden resten av fakturabeløpet. En 7,00 rabatt (1 %) er brukt, fordi betalingen er utført innenfor den andre kontantrabattperioden.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10030 | 4031    | 25/6/2015 | 25/7/2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 30,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 6,00      |
| Kontantrabattbeløp som skal brukes | 7,00      |

Fakturasaldoen er nå 0,00. Magnus viser informasjonen på siden **Kundetransaksjoner**.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Faktura          | 25/6/2015 | 10030   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Betaling         | 28/6/2015 |         |                                      | 294,00                                | 0,00    | USD      |
| DISC-10030 |  Kontantrabatt   | 28/6/2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Betaling         | 8/7/2015  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Kontantrabatt   | 8/7/2015  |         |                                      | 7,00                                  | 0,00    | USD      |






