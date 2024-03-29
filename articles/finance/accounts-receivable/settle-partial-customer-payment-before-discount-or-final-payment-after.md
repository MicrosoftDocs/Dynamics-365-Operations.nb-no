---
title: Utligne en delvis leverandørbetaling før rabattdatoen med en endelige betaling etter rabattdatoen
description: Denne artikkelen beskriver virkningen av utligning av betalinger mot fakturaer for kunder. Scenariet fokuserer på virkningen i underfinan, ikke i økonomimodulen.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f6b4527a9f176857e0cc6ba4665688dc8721ac1
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780488"
---
# <a name="settle-partial-payment-before-discount-date-with-final-payment-after-discount-date"></a>Utligne en delvis leverandørbetaling før rabattdatoen med en endelige betaling etter rabattdatoen

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver virkningen av utligning av betalinger mot fakturaer for kunder. Scenariet fokuserer på virkningen i underfinan, ikke i økonomimodulen.

Fabrikam selger varer til kunden 4027. Fabrikam tilbyr en kontantrabatt på 1 prosent hvis fakturaen er betalt innen 14 dager. Fakturaer må betales innen 30 dager. Fabrikam tilbyr også kontantrabatter på delvise betalinger. Du finner parameterne for utligning på siden **Kundeparametere**.

## <a name="invoice"></a>Faktura
25. juni legger Magnus inn og posterer en faktura på 1 000,00 for kunden 4027. Magnus kan vise denne fakturaen ved hjelp av **Transaksjoner**-knappen på siden **Kunder**.

| Bilag   | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo  | Valuta. |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Faktura          | 25/6/2020 | 10020   | 1,000.00                             |                                       | 1,000.00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Delbetaling før kontantrabattdatoen
2. juli gjør kunden 4027 en delvis innbetaling på 297.00 for fakturaen. Betalingen er kvalifisert for kontantrabatt, fordi Fabrikam gir kontantrabatter for delvise betalinger, og den delvise betalingen foretas før kontantrabattdatoen. Derfor tar kunden 4027 en kontantrabatt på 3,00. Magnus registrerer betalingen for kunden 4027 ved hjelp av betalingsjournalen. Magnus åpner deretter **Utlign transaksjoner**-siden, slik at han kan merke av fakturaen for utligning.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Valuta. | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10020 | 4027    | 25/6/2020 | 25/7/2020 | 10020   | 1,000.00                             | USD      | 297.00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**. Hvis du ikke endrer verdien for **Beløp som skal utlignes** til 297,00, vil verdiene for **Kontantrabattbeløp** som vises, variere. Imidlertid vil 3,00 behandles som kontantrabatten når betalingen er postert, fordi utligning justerer automatisk verdien for **Beløp som skal utlignes** for deg.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 9/7/2020 |
| Kontantrabattbeløp         | 10,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 3,00      |

Magnus posterer denne betalingen. Fakturaen har nå en saldo på 700,00. Du kan se følgende transaksjoner for kunden.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta. |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Faktura          | 25/6/2020 | 10020   | 1,000.00                             |                                       | 700.00  | USD      |
| ARP-10020  |  Betaling         | 01.07.2020  |         |                                      | 297.00                                | 0,00    | USD      |
| RAB-10020 |  Kontantrabatt   | 01.07.2020  |         |                                      | 3.00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Gjenstående betaling etter kontantrabattdatoen
Den 11. juli, som er etter rabattperioden, betaler kunde 4027 resten av denne fakturaen. På siden **Utlign åpne transaksjoner** vises ingen rabattbeløp i feltet **Beregnet kontantrabatt**, og verdien i feltet **Kontantrabattbeløp** er **0,00**. Når kunde 4027 betaler de gjenværende 700,00, brukes ingen ekstra rabatt.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Valuta. | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10020 | 4027    | 25/6/2020 | 25/7/2020 | 10020   | 700.00                               | USD      | 700.00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 9/7/2020 |
| Kontantrabattbeløp         | 0,00      |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 3,00      |
| Kontantrabattbeløp som skal brukes | 0,00      |

Hvis Magnus endrer verdien i feltet **Bruk kontantrabatt** til **Alltid**, ovestyres innstillingen **Beregn kontantrabatter for delvise betalinger**, og kontantrabatten brukes. Betalingsbeløpet endres til 693,00, og kontantrabatten er de gjenværende 7,00.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Valuta. | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|---------------|---------------------|----------|------------------|
| Valgt | Alltid            | FTI-10020 | 4027    | 25/6/2020 | 25/7/2020 | 10020   | 700.00        |                        | USD      | 693.00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 9/7/2020 |
| Kontantrabattbeløp         | 7.00      |
| Bruk kontantrabatt            | Alltid    |
| Kontantrabatt brukt          | 3,00      |
| Kontantrabattbeløp som skal brukes | 7,00      |

Magnus endrer verdien i feltet **Bruk kontantrabatt** tilbake til **Normal**, fordi han ikke lar denne kunden bruke den gjenværende kontantrabatten på 7,00. Magnus posterer deretter betalingen. Når Magnus åpner siden **Kundetransaksjoner**, har fakturaen en saldo på 0,00. Det finnes to betalinger. Én betaling er på 297,00 og har en kontantrabatt på 3,00, og den andre betalingen er på 700,00.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta. |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Faktura          | 25/6/2020 | 10020   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 01.07.2020  |         |                                      | 297.00                                | 0,00    | USD      |
| RAB-10020 |                  | 01.07.2020  |         |                                      | 3.00                                  | 0,00    | USD      |
| ARP-10021  |                  | 11/7/2020 |         |                                      | 700.00                                | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
