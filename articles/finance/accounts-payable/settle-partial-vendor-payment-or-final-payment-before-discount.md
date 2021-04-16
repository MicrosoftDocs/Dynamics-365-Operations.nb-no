---
title: Utligne en delvis leverandørbetaling og den endelige betalingen i sin helhet før rabattdatoen
description: Denne artikkelen leder deg gjennom et scenario der delvise betalinger foretas for en leverandørfaktura og en kontantrabatt blir utført.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89cb38656766b23761665518f9ec39f78349f79b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810324"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Utligne en delvis leverandørbetaling og den endelige betalingen i sin helhet før rabattdatoen

[!include [banner](../includes/banner.md)]

Denne artikkelen leder deg gjennom et scenario der delvise betalinger foretas for en leverandørfaktura og en kontantrabatt blir utført.

Fabrikam kjøper varer fra leverandøren 3064. Leverandøren gir Fabrikam en kontantrabatt på 1 prosent hvis fakturaen betales innen 14 dager. Fakturaer må betales innen 30 dager. Leverandøren lar også Fabrikam få kontantrabatter på delvise betalinger. Du finner parameterne for utligning på siden **Leverandørparametere**. 25 juni registrerer April en faktura for 1 000,00 for leverandøren 3064.

## <a name="vendor-invoice-on-june-25"></a>Leverandørfaktura 25. juni.
25. juni registreres og posteres en faktura på 1 000,00 for leverandøren 3064. April kan se transaksjonene på siden **Leverandørtransaksjoner**.

| Bilag   | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo   | Valuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 25/6/2015 | 10010   |                                      | 1 000,00                              | -1 000,00 | USD      |

April åpner **Utlign transaksjoner** på **Leverandører**-siden. Hun kan bruke siden **Utlign transaksjoner** til å vise dato og beløp for kontantrabatter. Forfallsdatoen er 25. juli, og en kontantrabatt på -10,00 er tilgjengelig hvis fakturaen er betalt innen 9. juli.

| Merk | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10010 | 3064    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | 990,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|       &nbsp;                 | &nbsp;    |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | -10,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -10,00    |

April klikker kategorien **Kontantrabatt** for å vise rabattbeløpet.

| Kontantrabattdato | Kontantrabattbeløp | Beløp i transaksjonsvaluta |
|--------------------|----------------------|--------------------------------|
| 9/7/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Delbetaling 1. juli ved hjelp av siden Utlign transaksjoner
April kan opprette en betalingsjournal for denne betalingen ved å åpne siden **Betalingsjournal** i leverandørmodulen. Det opprettes en ny journal, og angis en linje for leverandøren 3064. Hun åpner siden **Utlign transaksjoner**, slik at hun kan merke fakturaen for utligning. April markerer fakturaen og endrer verdien i feltet **Beløp som skal utlignes** til **-500,00**. Hun ser at verdien i feltet **Kontantrabattbeløp** er **-10,00** for hele fakturaen, og at verdien i feltet **Kontantrabattbeløp som skal brukes** er **-5,05**. April utligner derfor -505,05 av denne fakturaen.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | -500,00          |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | -10,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -5,05     |

April ønsker å utligne nøyaktig halvparten av fakturaen. Derfor endrer hun verdien i feltet **Beløp som skal utlignes** til **-495,00**. Det totale beløpet som er utlignet er nå 500,00. Dette beløpet inkluderer -5,00 kontantrabatt.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | -495,00          |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | -10,00    |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -5,00     |

April lukker siden **Utlign transaksjoner**. Det opprettes en betalingslinje for 495,00 i journalen, og deretter posterer April journalen. April kan se gjennom leverandørtransaksjonene på siden **Leverandørtransaksjoner**. Hun ser at fakturaen har en saldo på -500,00. Hun ser også en betaling på 495,00 og en kontantrabatt på 5,00.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Faktura          | 25/6/2015 | 10010   |                                      | 1 000,00                              | -500,00 | USD      |
| APP-10010  | Betaling          | 1/7/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Kontantrabatt    | 1/7/2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Gjenværende beløp betalt 8. juli
April betaler resten av fakturaen for leverandør 3064 den 8. juli, som er i kontantrabattperioden. April lager betalingsjournalen 8. juli og merker transaksjonen for utligning. Hun ser at beløpet som skal utlignes, er 495,00. Verdien i feltet **Beregnet kontantrabatt** er **-5,00**, fordi rabatten på 5,00 tidligere ble brukt.

|  &nbsp;                 |  &nbsp; |
|-------------------------|--------|
| Merket total            | 495,00 |
| Beregnet kontantrabatt | -5,00  |

Informasjon om den merkede transaksjonen vises i rutenettet på siden **Utlign åpne transaksjoner**.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1 000,00                       | USD      | 495,00           |

Rabattinformasjonen vises nederst på siden **Utlign åpne transaksjoner**.

|  &nbsp;                      | &nbsp;    |
|------------------------------|-----------|
| Kontantrabattdato           | 09/7/2015 |
| Kontantrabattbeløp         | 10,00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 5,00      |
| Kontantrabattbeløp som skal brukes | 5,00      |

April posterer betalingsjournalen og går gjennom leverandørtransaksjonene på siden **Leverandørtransaksjoner**. Saldoen for fakturaen er 0,00 og April ser de to betalingene og de to kontantrabattene.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Faktura          | 25/6/2015 | 10010   |                                      | 1 000,00                              | 0,00    | USD      |
| APP-10010  |  Betaling         | 1/7/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Kontantrabatt    | 1/7/2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Betaling          | 8/7/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Kontantrabatt    | 8/7/2015  |         | 5,00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]