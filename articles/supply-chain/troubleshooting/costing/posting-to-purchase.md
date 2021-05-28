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
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026795"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="fa16a-103">Innkjøps, avsetning som har et nullbeløp, posteres for et produktmottak med null verdi</span><span class="sxs-lookup"><span data-stu-id="fa16a-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="fa16a-104">KB-nummer: 4612588</span><span class="sxs-lookup"><span data-stu-id="fa16a-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="fa16a-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="fa16a-105">Symptoms</span></span>

<span data-ttu-id="fa16a-106">Når et produktmottak som har nullverdi, posteres, oppretter systemet en postering til innkjøpsutsetning der beløpet er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fa16a-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="fa16a-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="fa16a-107">Resolution</span></span>

<span data-ttu-id="fa16a-108">Som standard for finansposteringer av typen *Innkjøp, avsetning* er `IsTransferredIndetail`-feltet alltid satt til *Sammendrag* i underregnskapstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="fa16a-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="fa16a-109">Derfor oppretter systemet en tilknyttet bilagsoppføring selv om beløpet er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fa16a-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="fa16a-110">Hvis du vil hoppe over denne posteringstypen når beløpet er 0 (null), utvider du `subledgerJournalizer.markDoNotTransferEntries`-metoden, slik at den inkluderer `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, som vist i eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fa16a-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
