---
title: "Bruke en rabatt som er større enn beregnet rabatt for en leverandørbetaling"
description: "Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen. Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0c9e4bccb6e38e2e6d50256bc609b1552d9b21c5
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="a1614-104">Bruke en rabatt som er større enn beregnet rabatt for en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="a1614-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a1614-105">Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a1614-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="a1614-106">Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a1614-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="a1614-107">Leverandør 3051 gir Fabrikam en kontantrabatt på 4 prosent hvis en faktura betales innen sju dager.</span><span class="sxs-lookup"><span data-stu-id="a1614-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="a1614-108">29. juni registrerer April en faktura for 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="a1614-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="a1614-109">Leverandøren lar April bruke en rabatt på 60,00 i stedet for standardrabatten på 40,00 som er tilgjengelig for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a1614-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="a1614-110">April registrerer en engangs betaling ved hjelp av betalingsjournalen for Leverandører.</span><span class="sxs-lookup"><span data-stu-id="a1614-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="a1614-111">Hun angir leverandøren for betalingen og åpner deretter siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="a1614-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="a1614-112">Hun markerer fakturaen og endrer verdien i feltet **Kontantrabattbeløp** til **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="a1614-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>
| <span data-ttu-id="a1614-113">Merk</span><span class="sxs-lookup"><span data-stu-id="a1614-113">Mark</span></span>     | <span data-ttu-id="a1614-114">Bruk kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="a1614-114">Use cash discount</span></span> | <span data-ttu-id="a1614-115">Bilag</span><span class="sxs-lookup"><span data-stu-id="a1614-115">Voucher</span></span>   | <span data-ttu-id="a1614-116">Konto</span><span class="sxs-lookup"><span data-stu-id="a1614-116">Account</span></span> | <span data-ttu-id="a1614-117">Dato</span><span class="sxs-lookup"><span data-stu-id="a1614-117">Date</span></span>      | <span data-ttu-id="a1614-118">Forfallsdato</span><span class="sxs-lookup"><span data-stu-id="a1614-118">Due date</span></span>  | <span data-ttu-id="a1614-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="a1614-119">Invoice</span></span> | <span data-ttu-id="a1614-120">Beløp i transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a1614-120">Amount in transaction currency</span></span> | <span data-ttu-id="a1614-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="a1614-121">Currency</span></span> | <span data-ttu-id="a1614-122">Beløp som skal utlignes</span><span class="sxs-lookup"><span data-stu-id="a1614-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="a1614-123">Valgt</span><span class="sxs-lookup"><span data-stu-id="a1614-123">Selected</span></span> | <span data-ttu-id="a1614-124">Normal</span><span class="sxs-lookup"><span data-stu-id="a1614-124">Normal</span></span>            | <span data-ttu-id="a1614-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="a1614-125">Inv-10040</span></span> | <span data-ttu-id="a1614-126">3051</span><span class="sxs-lookup"><span data-stu-id="a1614-126">3051</span></span>    | <span data-ttu-id="a1614-127">29/6/2015</span><span class="sxs-lookup"><span data-stu-id="a1614-127">6/29/2015</span></span> | <span data-ttu-id="a1614-128">29/7/2015</span><span class="sxs-lookup"><span data-stu-id="a1614-128">7/29/2015</span></span> | <span data-ttu-id="a1614-129">10040</span><span class="sxs-lookup"><span data-stu-id="a1614-129">10040</span></span>   | <span data-ttu-id="a1614-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="a1614-130">1,000.00</span></span>                       | <span data-ttu-id="a1614-131">USD</span><span class="sxs-lookup"><span data-stu-id="a1614-131">USD</span></span>      | <span data-ttu-id="a1614-132">940.00</span><span class="sxs-lookup"><span data-stu-id="a1614-132">940.00</span></span>           |

<span data-ttu-id="a1614-133">Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="a1614-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>
|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="a1614-134">Kontantrabattdato</span><span class="sxs-lookup"><span data-stu-id="a1614-134">Cash discount date</span></span>           | <span data-ttu-id="a1614-135">12/7/2015</span><span class="sxs-lookup"><span data-stu-id="a1614-135">7/12/2015</span></span> |
| <span data-ttu-id="a1614-136">Kontantrabattbeløp</span><span class="sxs-lookup"><span data-stu-id="a1614-136">Cash discount amount</span></span>         | <span data-ttu-id="a1614-137">60.00</span><span class="sxs-lookup"><span data-stu-id="a1614-137">60.00</span></span>     |
| <span data-ttu-id="a1614-138">Bruk kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="a1614-138">Use cash discount</span></span>            | <span data-ttu-id="a1614-139">Normal</span><span class="sxs-lookup"><span data-stu-id="a1614-139">Normal</span></span>    |
| <span data-ttu-id="a1614-140">Kontantrabatt brukt</span><span class="sxs-lookup"><span data-stu-id="a1614-140">Cash discount taken</span></span>          | <span data-ttu-id="a1614-141">0,00</span><span class="sxs-lookup"><span data-stu-id="a1614-141">0.00</span></span>      |
| <span data-ttu-id="a1614-142">Kontantrabattbeløp som skal brukes</span><span class="sxs-lookup"><span data-stu-id="a1614-142">Cash discount amount to take</span></span> | <span data-ttu-id="a1614-143">60.00</span><span class="sxs-lookup"><span data-stu-id="a1614-143">60.00</span></span>     |

<span data-ttu-id="a1614-144">April posterer betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="a1614-144">April posts the payment journal.</span></span> <span data-ttu-id="a1614-145">Fakturaen utlignes fullstendig ved hjelp av en betaling på 940,00 og en rabatt på 60,00.</span><span class="sxs-lookup"><span data-stu-id="a1614-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




