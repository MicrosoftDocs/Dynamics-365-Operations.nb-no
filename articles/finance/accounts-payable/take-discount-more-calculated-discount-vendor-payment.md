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
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810252"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="4da67-104">Bruke mer enn beregnet rabatt for en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="4da67-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4da67-105">Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="4da67-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="4da67-106">Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="4da67-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="4da67-107">Leverandør 3051 gir Fabrikam en kontantrabatt på 4 prosent hvis en faktura betales innen sju dager.</span><span class="sxs-lookup"><span data-stu-id="4da67-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="4da67-108">29. juni registrerer April en faktura for 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="4da67-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="4da67-109">Leverandøren lar April bruke en rabatt på 60,00 i stedet for standardrabatten på 40,00 som er tilgjengelig for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="4da67-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="4da67-110">April registrerer en engangs betaling ved hjelp av betalingsjournalen for Leverandører.</span><span class="sxs-lookup"><span data-stu-id="4da67-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="4da67-111">Hun angir leverandøren for betalingen og åpner deretter siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="4da67-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="4da67-112">Hun markerer fakturaen og endrer verdien i feltet **Kontantrabattbeløp** til **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="4da67-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="4da67-113">Merk</span><span class="sxs-lookup"><span data-stu-id="4da67-113">Mark</span></span>     | <span data-ttu-id="4da67-114">Bruk kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="4da67-114">Use cash discount</span></span> | <span data-ttu-id="4da67-115">Bilag</span><span class="sxs-lookup"><span data-stu-id="4da67-115">Voucher</span></span>   | <span data-ttu-id="4da67-116">Konto</span><span class="sxs-lookup"><span data-stu-id="4da67-116">Account</span></span> | <span data-ttu-id="4da67-117">Dato</span><span class="sxs-lookup"><span data-stu-id="4da67-117">Date</span></span>      | <span data-ttu-id="4da67-118">Forfallsdato</span><span class="sxs-lookup"><span data-stu-id="4da67-118">Due date</span></span>  | <span data-ttu-id="4da67-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="4da67-119">Invoice</span></span> | <span data-ttu-id="4da67-120">Beløp i transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="4da67-120">Amount in transaction currency</span></span> | <span data-ttu-id="4da67-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="4da67-121">Currency</span></span> | <span data-ttu-id="4da67-122">Beløp som skal utlignes</span><span class="sxs-lookup"><span data-stu-id="4da67-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="4da67-123">Valgt</span><span class="sxs-lookup"><span data-stu-id="4da67-123">Selected</span></span> | <span data-ttu-id="4da67-124">Normal</span><span class="sxs-lookup"><span data-stu-id="4da67-124">Normal</span></span>            | <span data-ttu-id="4da67-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="4da67-125">Inv-10040</span></span> | <span data-ttu-id="4da67-126">3051</span><span class="sxs-lookup"><span data-stu-id="4da67-126">3051</span></span>    | <span data-ttu-id="4da67-127">29/6/2015</span><span class="sxs-lookup"><span data-stu-id="4da67-127">6/29/2015</span></span> | <span data-ttu-id="4da67-128">29/7/2015</span><span class="sxs-lookup"><span data-stu-id="4da67-128">7/29/2015</span></span> | <span data-ttu-id="4da67-129">10040</span><span class="sxs-lookup"><span data-stu-id="4da67-129">10040</span></span>   | <span data-ttu-id="4da67-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4da67-130">1,000.00</span></span>                       | <span data-ttu-id="4da67-131">USD</span><span class="sxs-lookup"><span data-stu-id="4da67-131">USD</span></span>      | <span data-ttu-id="4da67-132">940.00</span><span class="sxs-lookup"><span data-stu-id="4da67-132">940.00</span></span>           |

<span data-ttu-id="4da67-133">Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="4da67-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="4da67-134">Felt</span><span class="sxs-lookup"><span data-stu-id="4da67-134">Field</span></span>                        | <span data-ttu-id="4da67-135">Verdi</span><span class="sxs-lookup"><span data-stu-id="4da67-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="4da67-136">Kontantrabattdato</span><span class="sxs-lookup"><span data-stu-id="4da67-136">Cash discount date</span></span>           | <span data-ttu-id="4da67-137">12/7/2015</span><span class="sxs-lookup"><span data-stu-id="4da67-137">7/12/2015</span></span> |
| <span data-ttu-id="4da67-138">Kontantrabattbeløp</span><span class="sxs-lookup"><span data-stu-id="4da67-138">Cash discount amount</span></span>         | <span data-ttu-id="4da67-139">60.00</span><span class="sxs-lookup"><span data-stu-id="4da67-139">60.00</span></span>     |
| <span data-ttu-id="4da67-140">Bruk kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="4da67-140">Use cash discount</span></span>            | <span data-ttu-id="4da67-141">Normal</span><span class="sxs-lookup"><span data-stu-id="4da67-141">Normal</span></span>    |
| <span data-ttu-id="4da67-142">Kontantrabatt brukt</span><span class="sxs-lookup"><span data-stu-id="4da67-142">Cash discount taken</span></span>          | <span data-ttu-id="4da67-143">0,00</span><span class="sxs-lookup"><span data-stu-id="4da67-143">0.00</span></span>      |
| <span data-ttu-id="4da67-144">Kontantrabattbeløp som skal brukes</span><span class="sxs-lookup"><span data-stu-id="4da67-144">Cash discount amount to take</span></span> | <span data-ttu-id="4da67-145">60.00</span><span class="sxs-lookup"><span data-stu-id="4da67-145">60.00</span></span>     |

<span data-ttu-id="4da67-146">April posterer betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="4da67-146">April posts the payment journal.</span></span> <span data-ttu-id="4da67-147">Fakturaen utlignes fullstendig ved hjelp av en betaling på 940,00 og en rabatt på 60,00.</span><span class="sxs-lookup"><span data-stu-id="4da67-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]