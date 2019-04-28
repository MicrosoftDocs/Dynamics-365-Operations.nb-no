---
title: Bruke en rabatt som er større enn beregnet rabatt for en leverandørbetaling
description: Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen. Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 730ea9bb23368d24c5a09f98fbf6bbb41d685702
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/25/2019
ms.locfileid: "896103"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="e155c-104">Bruke en rabatt som er større enn beregnet rabatt for en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="e155c-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e155c-105">Denne artikkelen leder deg gjennom et scenario der en kontantrabatt tas for et beløp som er større enn rabatten som var opprinnelig tilgjengelig på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e155c-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="e155c-106">Denne situasjonen kan oppstå hvis en organisasjon inngår en avtale med leverandøren om å betale et mindre beløp på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e155c-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="e155c-107">Leverandør 3051 gir Fabrikam en kontantrabatt på 4 prosent hvis en faktura betales innen sju dager.</span><span class="sxs-lookup"><span data-stu-id="e155c-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="e155c-108">29. juni registrerer April en faktura for 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="e155c-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="e155c-109">Leverandøren lar April bruke en rabatt på 60,00 i stedet for standardrabatten på 40,00 som er tilgjengelig for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e155c-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="e155c-110">April registrerer en engangs betaling ved hjelp av betalingsjournalen for Leverandører.</span><span class="sxs-lookup"><span data-stu-id="e155c-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="e155c-111">Hun angir leverandøren for betalingen og åpner deretter siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="e155c-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="e155c-112">Hun markerer fakturaen og endrer verdien i feltet **Kontantrabattbeløp** til **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="e155c-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="e155c-113">Merk</span><span class="sxs-lookup"><span data-stu-id="e155c-113">Mark</span></span>     | <span data-ttu-id="e155c-114">Bruk kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="e155c-114">Use cash discount</span></span> | <span data-ttu-id="e155c-115">Bilag</span><span class="sxs-lookup"><span data-stu-id="e155c-115">Voucher</span></span>   | <span data-ttu-id="e155c-116">Konto</span><span class="sxs-lookup"><span data-stu-id="e155c-116">Account</span></span> | <span data-ttu-id="e155c-117">Dato</span><span class="sxs-lookup"><span data-stu-id="e155c-117">Date</span></span>      | <span data-ttu-id="e155c-118">Forfallsdato</span><span class="sxs-lookup"><span data-stu-id="e155c-118">Due date</span></span>  | <span data-ttu-id="e155c-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="e155c-119">Invoice</span></span> | <span data-ttu-id="e155c-120">Beløp i transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="e155c-120">Amount in transaction currency</span></span> | <span data-ttu-id="e155c-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="e155c-121">Currency</span></span> | <span data-ttu-id="e155c-122">Beløp som skal utlignes</span><span class="sxs-lookup"><span data-stu-id="e155c-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="e155c-123">Valgt</span><span class="sxs-lookup"><span data-stu-id="e155c-123">Selected</span></span> | <span data-ttu-id="e155c-124">Normal</span><span class="sxs-lookup"><span data-stu-id="e155c-124">Normal</span></span>            | <span data-ttu-id="e155c-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="e155c-125">Inv-10040</span></span> | <span data-ttu-id="e155c-126">3051</span><span class="sxs-lookup"><span data-stu-id="e155c-126">3051</span></span>    | <span data-ttu-id="e155c-127">29/6/2015</span><span class="sxs-lookup"><span data-stu-id="e155c-127">6/29/2015</span></span> | <span data-ttu-id="e155c-128">29/7/2015</span><span class="sxs-lookup"><span data-stu-id="e155c-128">7/29/2015</span></span> | <span data-ttu-id="e155c-129">10040</span><span class="sxs-lookup"><span data-stu-id="e155c-129">10040</span></span>   | <span data-ttu-id="e155c-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e155c-130">1,000.00</span></span>                       | <span data-ttu-id="e155c-131">USD</span><span class="sxs-lookup"><span data-stu-id="e155c-131">USD</span></span>      | <span data-ttu-id="e155c-132">940.00</span><span class="sxs-lookup"><span data-stu-id="e155c-132">940.00</span></span>           |

<span data-ttu-id="e155c-133">Rabattinformasjonen vises nederst på siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="e155c-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="e155c-134">Kontantrabattdato</span><span class="sxs-lookup"><span data-stu-id="e155c-134">Cash discount date</span></span>           | <span data-ttu-id="e155c-135">12/7/2015</span><span class="sxs-lookup"><span data-stu-id="e155c-135">7/12/2015</span></span> |
| <span data-ttu-id="e155c-136">Kontantrabattbeløp</span><span class="sxs-lookup"><span data-stu-id="e155c-136">Cash discount amount</span></span>         | <span data-ttu-id="e155c-137">60.00</span><span class="sxs-lookup"><span data-stu-id="e155c-137">60.00</span></span>     |
| <span data-ttu-id="e155c-138">Bruk kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="e155c-138">Use cash discount</span></span>            | <span data-ttu-id="e155c-139">Normal</span><span class="sxs-lookup"><span data-stu-id="e155c-139">Normal</span></span>    |
| <span data-ttu-id="e155c-140">Kontantrabatt brukt</span><span class="sxs-lookup"><span data-stu-id="e155c-140">Cash discount taken</span></span>          | <span data-ttu-id="e155c-141">0,00</span><span class="sxs-lookup"><span data-stu-id="e155c-141">0.00</span></span>      |
| <span data-ttu-id="e155c-142">Kontantrabattbeløp som skal brukes</span><span class="sxs-lookup"><span data-stu-id="e155c-142">Cash discount amount to take</span></span> | <span data-ttu-id="e155c-143">60.00</span><span class="sxs-lookup"><span data-stu-id="e155c-143">60.00</span></span>     |

<span data-ttu-id="e155c-144">April posterer betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="e155c-144">April posts the payment journal.</span></span> <span data-ttu-id="e155c-145">Fakturaen utlignes fullstendig ved hjelp av en betaling på 940,00 og en rabatt på 60,00.</span><span class="sxs-lookup"><span data-stu-id="e155c-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



