---
title: Bruke én betaling til å utligne fakturaer som strekker seg over flere rabattperioder
description: Dette emnet viser hvordan flere fakturaer betales når hver faktura kvalifiserer for kontantrabatt. Scenarioene i denne artikkelen fremhever hvordan kontantrabattene som tas, varierer avhengig av når betalingen skjer.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c86423c9e3453d8be11e6bdbc3484647e26e9eeec59c9a2e888cc5a2b2b5592
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769065"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Bruke én betaling til å utligne fakturaer som strekker seg over flere rabattperioder

[!include [banner](../includes/banner.md)]

Dette emnet viser hvordan flere fakturaer betales når hver faktura kvalifiserer for kontantrabatt. Scenarioene i denne artikkelen fremhever hvordan kontantrabattene som tas, varierer avhengig av når betalingen skjer.

Fabrikam selger varer til kunden 4032. Fabrikam tilbyr en kontantrabatt på 1 prosent hvis fakturaen er betalt innen 14 dager. Fabrikam tilbyr også kontantrabatter på delvise betalinger. Du finner parameterne for utligning på siden **Kundeparametere**.

## <a name="invoices"></a>Fakturaer
Kunde 4032 har tre fakturaer på til sammen 3 000,00:

-   Faktura FTI-10040 på 1 000,00 ble registrert 15. mai. Denne fakturaen er kvalifisert for en kontantrabatt på 1 prosent hvis den betales innen 14 dager.
-   Faktura FTI-10041 på 1 000,00 ble registrert 25. juni. Denne fakturaen er kvalifisert for en kontantrabatt på 1 prosent hvis den betales innen 14 dager.
-   Faktura FTI-10042 på 1 000,00 ble registrert 25. juni. Denne fakturaen er kvalifisert for en kontantrabatt på 2 prosent hvis den betales innen fem dager, og 1 prosent rabatt hvis den betales innen 14 dager.

## <a name="settle-all-invoices-on-june-29"></a>Utligne alle fakturaer 29. juni
Hvis Magnus oppretter en betalingsjournal for å utligne disse fakturaene fullt ut 29. juni, er betalingen 2 970,00. Summen av alle rabattbeløp er 30,00. Magnus oppretter en betaling for kunde 4032, og åpner deretter siden **Utlign transaksjoner**. På siden **Utlign transaksjoner** merker Magnus alle tre fakturalinjene for utligning:

-   Betalingen for faktura FTI-10040 er 1 000.00. Ingen kontantrabatt er brukt.
-   Betalingen for faktura FTI-10041 er 990,00. En kontantrabatt på 1 prosent eller 10,00 brukes.
-   Betalingen for faktura FTI-10042 er 980,00. En kontantrabatt på 2 prosent eller 20,00 brukes.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valgt                 | Normal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Valgt                 | Normal            | FTI-10041 | 4032    | 25/6/2015 | 25/7/2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Valgt og uthevet | Normal            | FTI-10042 | 4032    | 25/6/2015 | 25/7/2015 | 10042   | 1 000,00                             |                                       | USD      | 980,00           |

Når betalingen er postert, er kundesaldoen 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Utligne alle fakturaer i 1. juli
Hvis Magnus oppretter en betalingsjournal for å utligne disse fakturaene fullt ut 1. juli, er betalingen 2 980,00. Magnus oppretter en betaling for kunde 4032, og åpner deretter siden **Utlign transaksjoner**. På siden **Utlign transaksjoner** merker Magnus alle tre fakturalinjene for utligning:

-   Betalingen for faktura FTI-10040 er 1 000.00. Ingen kontantrabatt er brukt.
-   Betalingen for faktura FTI-10041 er 990,00. En kontantrabatt på 1 prosent eller 10,00 brukes.
-   Betalingen for faktura FTI-10042 er 990,00. En kontantrabatt på 1 prosent eller 10,00 brukes. Selv om 1. juli er etter perioden som kvalifiserer for rabatten på 2 %, er det fremdeles i perioden som kvalifiserer for rabatten på 1 %.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valgt                 | Normal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1 000,00                             |                                       | USD      | 1 000,00         |
| Valgt                 | Normal            | FTI-10041 | 4032    | 25/6/2015 | 25/7/2015 | 10041   | 1 000,00                             |                                       | USD      | 990,00           |
| Valgt og uthevet | Normal            | FTI-10042 | 4032    | 25/6/2015 | 25/7/2015 | 10042   | 1 000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Delvis utligning 29. juni
Kunde 4032 kan betale et delbeløp, for eksempel halvparten av hver faktura. Magnus oppretter en betaling for kunde 4032, og åpner deretter siden **Utlign transaksjoner**. På siden **Utlign transaksjoner** merker Magnus alle tre fakturalinjene for utligning. På hver linje angir han beløpet som skal utlignes, basert på instruksjonene som kunden har gitt. Når Magnus legger til en linje, ser han rabattbeløpet for denne linjen og kontantrabattbeløpet som er brukt. Ettersom kunden betaler halve fakturaen, ser Magnus at verdien i feltet **Kontantrabattbeløp** for FTI-10042 er **20,00**, men verdien i feltet **Kontantrabatt brukt** er **10,00**. Betalingsbeløpet er 1 485,00.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valgt                 | Normal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1 000,00                             |                                       | USD      | 500,00           |
| Valgt                 | Normal            | FTI-10041 | 4032    | 25/6/2015 | 25/7/2015 | 10041   | 1 000,00                             |                                       | USD      | 495.00           |
| Valgt og uthevet | Normal            | FTI-10042 | 4032    | 25/6/2015 | 25/7/2015 | 10042   | 1 000,00                             |                                       | USD      | 490.00           |

Magnus kan også angi betalingsbeløpet på 1 485,00 manuelt før han åpner siden **Utlign transaksjoner**. Hvis Magnus registrerer betalingsbeløpet manuelt og deretter merker alle tre transaksjonene, men ikke justerer verdien i feltet **Beløp som skal utlignes** for hver transaksjon, mottar han følgende melding når han lukker siden:

> Totalbeløpet av merkede transaksjoner er forskjellig fra journalbeløpet. Vil du endre journalbeløpet?

Hvis Magnus vil at betalingsbeløpet bare skal være 1 485,00, klikker han **Nei** og posterer journalen. Transaksjonene utlignes på følgende måte:

1.  Faktura FTI-10040 er helt utlignet med 1 000,00 fordi den ble angitt 15. mai og er den eldste fakturaen. Ingen kontantrabatt er brukt. Restbeløpet på betalingstransaksjonen er 485,00.
2.  Faktura FTI-10041 er ikke utlignet i det hele tatt. Fakturaene FTI-10041 og FTI-10042 ble angitt på samme dato. Det er imidlertid tilgjengelig en rabatt på 1 % for faktura FTI-10041, og en rabatt på 2 prosent for faktura FTI-10042. Ettersom det finnes en bedre rabatt for faktura FTI-10042, utlignes gjenværende 485,00 med faktura FTI-10042.
3.  Faktura FTI-10042 utlignes med gjenværende 485,00. Fabrikam tilbyr delrabatter. I dette tilfellet er rabatten 9,90 (485,00 ÷ 0,98 × 0,02 =). Beløpet (485,00) deles med 0,98 fordi det er en rabatt på 2 prosent (derfor betaler kunden 98 prosent av fakturaen). Resultatet multipliseres deretter med rabattprosenten, eller 2 prosent. Betalingen på 485,00 pluss rabatten på 9,90 er lik 494,90. Beløpet på den opprinnelige fakturaen var 1 000,00. Derfor har transaksjonen en saldo på 505,10 (= 1 000,00 – 494,90).

Magnus viser informasjonen på siden **Kundetransaksjoner**.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo  | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Faktura          | 15/5/2015 | 10040   | 1 000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Faktura          | 25/6/2015 | 10041   | 1 000,00                             |                                       | 1 000,00 | USD      |
| FTI-10042  | Faktura          | 25/6/2015 | 10042   | 1 000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Betaling          | 29/6/2015 |         |                                      | 1 485,00                              | 0,00     | USD      |
| DISC-10040 | Kontantrabatt    | 29/6/2015 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]