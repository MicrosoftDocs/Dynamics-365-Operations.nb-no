---
title: Utligne delvise og endelige betalinger i sin helhet før rabattdatoen
description: Denne artikkelen gir scenarier som viser hvordan du registrerer delvise betalinger for en kunde og tar kontantrabatter i kontantrabattperioden.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
ms.openlocfilehash: ee11647f6f700042e11133181de919e13f16c018
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715971"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Utligne delvise og endelige betalinger i sin helhet før rabattdatoen

[!include [banner](../includes/banner.md)]

Denne artikkelen gir scenarier som viser hvordan du registrerer delvise betalinger for en kunde og tar kontantrabatter i kontantrabattperioden.

Fabrikam selger varer til kunden 4028. Fabrikam tilbyr en kontantrabatt på 1 prosent hvis fakturaen er betalt innen 14 dager. Fakturaer må betales innen 30 dager. Fabrikam tilbyr også kontantrabatter på delvise betalinger. Du finner parameterne for utligning på siden **Kundeparametere**.

## <a name="customer-invoice"></a>Kundefaktura
25. juni legger Magnus inn og posterer en faktura for 1 000,00 for kunde 4028. Magnus kan vise denne transaksjonen på siden **Kundetransaksjoner**.

| Bilag   | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Faktura          | 25/6/2015 | 10010   | 1 000,00                             |                                       | 1 000,00 | USD      |

Fra siden **Kunde** eller **Kundetransaksjoner** kan Magnus åpne siden **Utlign transaksjoner** for å vise datoene og beløpene for kontantrabatter som er tilgjengelige for fakturaen. Forfallsdatoen er 25. juli, og en kontantrabatt på 10,00 er tilgjengelig hvis fakturaen er betalt innen 9. juli.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner** for den merkede fakturaen.

|    &nbsp;                    |  &nbsp;   |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 10,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 10,00     |

Magnus klikker kategorien **Kontantrabatt** for å vise rabattbeløpet.

| Kontantrabattdato | Kontantrabattbeløp | Beløp i transaksjonsvaluta |
|--------------------|----------------------|--------------------------------|
| 9/7/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Delbetaling ved hjelp av siden Angi kundebetalinger
Kunde 4028 sender en betaling på 500,00 1. juli. For å registrere denne betalingen klikker ikke Magnus på **Linjer**. I stedet registrerer Magnus betalingen ved å opprette en ny betalingsjournal og deretter åpne siden **Angi kundebetalinger**. Magnus legger inn betalingsinformasjonen og markerer fakturaen som de angav. Når Magnus registrerer **500,00** som beløp, skriver de også inn **500,00** i feltet **Beløp som skal betales** i rutenettet. Ettersom Fabrikam gir en kontantrabatt på delvise betalinger, ser Magnus at en delvis kontantrabatt på 5,05 også skal tas. Beregningen for denne rabatten er 500,00 ÷ 0,99 x 0,01 = 5,05. (I denne beregningen deles 500,00 på 0,99, fordi det finnes en rabatt på 1 prosent. Kunden betaler derfor 99 prosent av fakturaen. Resultatet multipliseres deretter med rabattprosenten, som er 1 prosent, eller 0,01. Hvis kunden tar hele rabatten på 10,00, er beløpet som skal utlignes, 990,00.) Rabattinformasjonen vises i rutenettet nederst på siden **Angi kundebetalinger**.

| Kontantrabattbeløp som skal brukes | Kontantrabatt brukt | Beløp som skal betales |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Delbetaling ved hjelp av journallinjene
I stedet for å åpne siden **Angi kundebetalinger** i betalingsjournalen kan Magnus klikk **Linjer** for å angi en betaling. Betalingsjournalen vises, der Magnus kan angi en linje for kunde 4028. Magnus åpner deretter **Utlign transaksjoner**-siden, slik at han kan merke av fakturaen for utligning. Magnus markerer fakturaen og endrer verdien i feltet **Beløp som skal utlignes** til **500,00**. Magnus ser igjen at verdien i feltet **Kontantrabattbeløp** er **10,00** for hele fakturaen, og at verdien i feltet **Kontantrabattbeløp som skal brukes** er **5,05**. Magnus utligner derfor 505,05 av denne fakturaen.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | 500,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 10,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 5,05      |

Hvis kunden ønsker å utligne nøyaktig halvparten fakturaen, sender kunden en betaling på 495,00. I dette tilfeller registrerer Magnus **495,00** i feltet **Beløp som skal utlignes**. Kontantrabatten for 5,00 skal også brukes, slik at totalt utlignet beløp er 500,00.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 10,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 5,00      |

Magnus lukker siden **Utlign transaksjoner**. Det opprettes en betalingslinje for 495,00 i journalen, og deretter posterer Magnus journalen. Magnus kan se gjennom kundetransaksjonene på siden **Kundetransaksjoner**. På denne siden ser Magnus at fakturaen har en saldo på 500,00. Magnus ser også en betaling på 495,00 og en rabatt på 5,00.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Faktura          | 25/6/2015 | 10010   | 1 000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Betaling         | 1/7/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Kontantrabatt   | 1/7/2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Betaling for det gjenstående beløpet
Kunde 4028 betaler det gjenstående beløpet på 495,00 8. juli som er i kontantrabattperioden. Magnus lager betalingsjournalen 8. juli og merker transaksjonen for utligning. Magnus ser at beløpet som skal utlignes, er 495,00. Verdien i feltet **Beregnet kontantrabatt** er **5,00**, fordi rabatten på 5,00 tidligere ble brukt.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| Merket total            | 495,00 |
| Beregnet kontantrabatt | 5,00   |

Informasjon om den merkede transaksjonen vises i rutenettet på siden **Utlign åpne transaksjoner**.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 10,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 5,00      |
| Kontantrabattbeløp som skal brukes | 5,00      |

Magnus posterer denne journalen og ser gjennom kundetransaksjonene på siden **Kundetransaksjoner**. Saldoen for fakturaen er 0,00 og Magnus ser de to betalingene og de to kontantrabattene.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Faktura          | 25/6/2015 | 10010   | 1 000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Betaling          | 1/7/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Kontantrabatt    | 1/7/2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Betaling          | 8/7/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Kontantrabatt    | 8/7/2015  |         |                                      | 5,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
