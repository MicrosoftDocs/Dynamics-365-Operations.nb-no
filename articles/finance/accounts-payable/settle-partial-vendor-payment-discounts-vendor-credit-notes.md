---
title: Utligne en delvis leverandørbetaling som har rabatter på kreditnotaer
description: Denne artikkelen leder deg gjennom et scenario der en kreditnota utlignes mot en faktura.
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
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
ms.openlocfilehash: b926d94059fb12b143b9c9b4b5c04cb7f39f8e99
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715944"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>Utligne en delvis leverandørbetaling som har rabatter på kreditnotaer

[!include [banner](../includes/banner.md)]

Denne artikkelen leder deg gjennom et scenario der en kreditnota utlignes mot en faktura.

Fabrikams leverandører gi kontantrabatter på kreditnotaer. Leverandør 3050 gir Fabrikam en kontantrabatt på 1 prosent hvis en faktura betales innen 14 dager.

## <a name="invoice-and-credit-memo"></a>Faktura og kreditnota
29. juni opprettes en faktura på 1 000,00 for leverandøren 3050. 2. juli oppretter hun en kreditnota på 200,00. April åpner **Utlign transaksjoner** på **Leverandører**-siden. Hun kan bruke siden **Utligne transaksjoner** til å merke både kreditnotaen og fakturaen for utligning. Det beregnes rabatt på 2,00 på kreditnotaen. Den totale verdien til kreditnotaen reduseres dermed til 198,00.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt                 | Normal            | Fakt-10070 | 3050    | 29.06.2015 | 29.07.2015 | 10070   | -1 000,00                      | USD      | -990,00          |
| Valgt og uthevet | Normal            | K-10070  | 3050    | 02.07.2015  | 29.07.2015 |         | 200,00                         | USD      | 198,00           |

Rabattinformasjonen for kreditnotaen vises nederst på siden **Utlign åpne transaksjoner**.

| Felt                        | Verdi     |
|------------------------------|-----------|
| Kontantrabattdato           | 13.07.2015 |
| Kontantrabattbeløp         | 2.00      |
| Bruk kontantrabatt            | Normal    |
| Kontantrabatt brukt          | 0,00      |
| Kontantrabattbeløp som skal brukes | 2,00      |

April klikker **Poster**. Deretter ser hun gjennom den fullførte utligningen. April ser at 198,00 av kreditnotaen ble brukt, og at det ble brukt en rabatt på 2,00. Derfor er totalen 200,00.

| Merk                     | Bruk kontantrabatt | Bilag   | Konto | Dato      | Forfallsdato  | Faktura  | Beløp i transaksjonsvaluta | Valuta | Beløp som skal utlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valgt og uthevet | Normal            | Fakt-10070 | 3050    | 29.06.2015 | 29.07.2015 | 10070    | -1 000,00                      | USD      | -200,00          |
| Valgt                 | Normal            | K-10070  | 3050    | 02.07.2015  | 29.07.2015 | K-10070 | 200,00                         | USD      | 198,00           |

April kan gå gjennom leverandørtransaksjonene på **Leverandørtransaksjoner**-siden ved å velge en leverandør på **Alle leverandører**-siden og deretter klikke **Transaksjoner** i handlingsruten. På denne siden ser April at fakturaen har en saldo på -800,00. Hun ser også en kreditnota på 198,00 og en rabatt på 2,00.

| Bilag    | transaksjonstype | Dato      | Faktura | Beløp i transaksjonsvaluta, debet | Beløp i transaksjonsvaluta, kredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fakt-10070  | Faktura          | 29.06.2015 | 10070   |                                      | 1 000,00                              | -800.00 | USD      |
| Fakt-10071  |                  | 02.07.2015  | K10071 | 200,00                               |                                       | 0,00    | USD      |
| RAB-10071 |  Kontantrabatt   | 02.07.2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| RAB-10071 |  Kontantrabatt   | 02.07.2015  |         |                                      | 2,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
