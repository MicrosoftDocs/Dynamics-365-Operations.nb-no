---
title: Utligne en delvis leverandørbetaling som har rabatter på kreditnotaer
description: Denne artikkelen leder deg gjennom et scenario der en kreditnota utlignes mot en faktura.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9a23ef6bff5f135e7f4189add776aeed18fbe79
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227310"
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

|                              |           |
|------------------------------|-----------|
| Kontantrabattdato           | 13.07.2015 |
| Kontantrabattbeløp         | 2,00      |
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