---
title: Bruke mer enn beregnet rabatt for en leverandørbetaling
description: Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen. Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df8f1aa7e0af3a44ec49d84b6ca095a484834c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888071"
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
