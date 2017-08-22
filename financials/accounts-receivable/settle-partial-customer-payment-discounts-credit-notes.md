---
title: "Utligne en delvis kundebetaling som har rabatter på kreditnotaer"
description: "Denne artikkelen leder deg gjennom et scenario der en kontantrabatt blir utført på en kreditnota når den opprinnelige fakturaen har kontantrabatt."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4fbbd4d4b4ff9ecfcb30cd0ded2bc366d07dc1c4
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Utligne en delvis kundebetaling som har rabatter på kreditnotaer

[!include[banner](../includes/banner.md)]


Denne artikkelen leder deg gjennom et scenario der en kontantrabatt blir utført på en kreditnota når den opprinnelige fakturaen har kontantrabatt. 

Fabrikam tillater kunder å ta kontantrabatter for delvise betalinger og også kreditnotaer. En kontantrabatt kan tas på en kreditnota når kreditnotaen er utstedt for en faktura som kunden tok en kontantrabatt på. I stedet for å gi kredit for hele beløpet, kan du kreditere kundens saldo for et beløp som ekskluderer kontantrabattprosenten som kunden tok. Du finner parameterne for utligning på siden **Kundeparametere**.

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




