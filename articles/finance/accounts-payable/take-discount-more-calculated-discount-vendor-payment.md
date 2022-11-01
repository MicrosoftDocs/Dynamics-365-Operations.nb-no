---
title: Bruke mer enn beregnet rabatt for en leverandørbetaling
description: Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen. Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27a6ec8fdba495535227d9d893d59edac5588985
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715701"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Bruke mer enn beregnet rabatt for en leverandørbetaling

[!include [banner](../includes/banner.md)]

Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen. Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen. 

Leverandør 3051 gir Fabrikam en kontantrabatt på 4 prosent hvis en faktura betales innen sju dager. 29. juni registrerer April en faktura for 1 000,00. Leverandøren lar April bruke en rabatt på 60,00 i stedet for standardrabatten på 40,00 som er tilgjengelig for fakturaen. April registrerer en engangs betaling ved hjelp av betalingsjournalen for Leverandører. Hun angir leverandøren for betalingen og åpner deretter siden **Utlign transaksjoner**. Hun markerer fakturaen og endrer verdien i feltet **Kontantrabattbeløp** til **-60,00**.

| Merk     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | Inv-10040 | 3051    | 29/6/2015 | 29/7/2015 | 10040   | 1 000,00                       | USD      | 940.00           |

Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 12/7/2015 |
| Kontantrabattbeløp         | 60.00     |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 60.00     |

April posterer betalingsjournalen. Fakturaen utlignes fullstendig ved hjelp av en betaling på 940,00 og en rabatt på 60,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
