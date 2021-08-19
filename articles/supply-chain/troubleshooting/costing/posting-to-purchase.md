---
title: Innkjøps, avsetning som har et nullbeløp, posteres for et produktmottak med null verdi
description: Når et produktmottak som har nullverdi, posteres, oppretter systemet en postering til innkjøpsutsetning der beløpet er 0 (null).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722181"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Innkjøps, avsetning som har et nullbeløp, posteres for et produktmottak med null verdi

KB-nummer: 4612588

## <a name="symptoms"></a>Symptomer

Når et produktmottak som har nullverdi, posteres, oppretter systemet en postering til innkjøpsutsetning der beløpet er 0 (null).

## <a name="resolution"></a>Oppløsning

Som standard for finansposteringer av typen *Innkjøp, avsetning* er `IsTransferredIndetail`-feltet alltid satt til *Sammendrag* i underregnskapstransaksjoner. Derfor oppretter systemet en tilknyttet bilagsoppføring selv om beløpet er 0 (null).

Hvis du vil hoppe over denne posteringstypen når beløpet er 0 (null), utvider du `subledgerJournalizer.markDoNotTransferEntries`-metoden, slik at den inkluderer `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, som vist i eksemplet nedenfor.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
