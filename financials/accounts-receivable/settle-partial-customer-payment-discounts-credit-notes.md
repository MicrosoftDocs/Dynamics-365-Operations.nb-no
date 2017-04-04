---
title: "Utligne en delvis kundebetaling med rabatter på kreditnotaer"
description: "Denne artikkelen leder deg gjennom et scenario der en kontantrabatt blir utført på en kreditnota når den opprinnelige fakturaen har kontantrabatt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e43bcea67d9c408c93258f9b64565560b59fbb88
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Utligne en delvis kundebetaling med rabatter på kreditnotaer

Denne artikkelen leder deg gjennom et scenario der en kontantrabatt blir utført på en kreditnota når den opprinnelige fakturaen har kontantrabatt. 

Fabrikam tillater kunder å ta kontantrabatter for delvise betalinger og også kreditnotaer. En kontantrabatt kan tas på en kreditnota når kreditnotaen er utstedt for en faktura som kunden tok en kontantrabatt på. I stedet for å gi kredit for hele beløpet, kan du kreditere kundens saldo for et beløp som ekskluderer kontantrabattprosenten som kunden tok. Parametere for utligning er plassert på den **Kundeparametere** siden.

## <a name="invoice-and-credit-note"></a>Faktura/kreditnota
Kunde 4035 har en faktura for 1000,00 og en kreditnota for 100,00. Hvert dokument har 1 prosent rabatt ved betaling innen 14 dager. Magnus kan vise denne informasjonen på siden **Kundetransaksjoner**.

| Bilag    | transaksjonstype | Dato      | Faktura  | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo  | Valuta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Faktura          | 28/6/2015 | 10050    | 1 000,00                             |                                       | 1 000,00 | USD      |
| CCRN-10050 | Kreditnota      | 28/6/2015 | K-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Utligne en kreditnota med en faktura
Magnus åpner siden **Utlign transaksjoner** fra **Kundetransaksjoner**-siden. Han kan bruke siden **Utligne transaksjoner** til å utligne fakturaen og kreditnotaen. Som en del av utligningsprosessen ser han kontantrabattdatoene og -beløpene. Han merker de to dokumentene og klikker deretter **Poster** for å utligne transaksjonene. Det er en rabatt på -1,00 på kreditnotaen, fordi Fabrikam tillater rabatter på kreditnotaer.

| Merk     | Bruk kontantrabatt | Bilag    | Konto | Dato      | Forfallsdato  | Faktura  | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI-10050  | 4035    | 28/6/2015 | 28/7/2015 | 10050    | 1 000,00                       | USD      | 990.00           |
| Valgt | Normal            | CCRN-10050 | 4035    | 28/6/2015 | 28/7/2015 | K-10050 | -100,00                        | USD      | -99.00           |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2015 |
| Kontantrabattbeløp         | -1.00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | -1.00     |

Utligningen skal være 100,00, og inkluderer en betaling på 99,00 og en rabatt på 1,00.


