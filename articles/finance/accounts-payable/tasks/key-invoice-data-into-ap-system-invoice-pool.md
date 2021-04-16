---
title: Registrere fakturadata i AP-systemet ved hjelp av fakturapulje
description: Dette emnet beskriver hvordan du bruker ankomstregistrering til å opprette fakturaer.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c54f610e45d288ed58fd209d290d73bfe1ff2f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820671"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="8bf27-103">Registrere fakturadata i AP-systemet ved hjelp av fakturapulje</span><span class="sxs-lookup"><span data-stu-id="8bf27-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8bf27-104">Dette emnet beskriver hvordan du bruker ankomstregistrering til å opprette fakturaer.</span><span class="sxs-lookup"><span data-stu-id="8bf27-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="8bf27-105">Bruk deretter fakturapuljen for å samsvare fakturaen med en bestilling og fullføre kostnaden på leverandørens fakturaside.</span><span class="sxs-lookup"><span data-stu-id="8bf27-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="8bf27-106">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="8bf27-106">Create a purchase order</span></span>
1. <span data-ttu-id="8bf27-107">I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="8bf27-108">Velg **Ny** for å opprette en bestilling.</span><span class="sxs-lookup"><span data-stu-id="8bf27-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="8bf27-109">I feltet **Leverandørkonto** velger du en leverandør fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="8bf27-110">Velg for eksempel leverandør **1001**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="8bf27-111">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-111">Select **OK**.</span></span>
5. <span data-ttu-id="8bf27-112">Velg varenummeret for tjenesten i rullegardinlisten i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf27-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="8bf27-113">Velg for eksempel **S0001**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-113">For example, select **S0001**.</span></span> <span data-ttu-id="8bf27-114">Nettbeløpet er USD 75.00.</span><span class="sxs-lookup"><span data-stu-id="8bf27-114">The net amount is 75.00.</span></span>  <span data-ttu-id="8bf27-115">Dette er beløpet vi forventer å se på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="8bf27-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="8bf27-116">Velg **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="8bf27-117">Velg **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="8bf27-118">Opprette og postere en faktura</span><span class="sxs-lookup"><span data-stu-id="8bf27-118">Create and post and invoice</span></span>
1. <span data-ttu-id="8bf27-119">Gå til **Moduler > Leverandører > Fakturaer > Ankomstregistrering** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="8bf27-120">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-120">Select **New**.</span></span>
3. <span data-ttu-id="8bf27-121">Åpne oppslaget for å velge navnet på ankomstregistreringen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="8bf27-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="8bf27-122">Velg navnet på ankomstregistreringen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="8bf27-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="8bf27-123">Velg **Linjer** for å åpne registeret og angi utgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="8bf27-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="8bf27-124">Velg en leverandør i oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8bf27-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="8bf27-125">Velg for eksempel leverandør **1001**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="8bf27-126">I **Faktura**-feltet angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="8bf27-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="8bf27-127">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf27-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="8bf27-128">Angi et tall i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf27-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="8bf27-129">I **Bestilling**-feltet åpner du rullegardinlisten for å velge bestillingen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="8bf27-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="8bf27-130">Merk en godkjenner i rullegardinlisten i **Godkjent av**-feltet, og klikk på **Velg** for å velge denne godkjenneren.</span><span class="sxs-lookup"><span data-stu-id="8bf27-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="8bf27-131">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="8bf27-132">Åpne en faktura fra utvalget og sammenlign den med en bestilling for å fullføre fakturaprosessen</span><span class="sxs-lookup"><span data-stu-id="8bf27-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="8bf27-133">Gå til **Moduler > Leverandører > Fakturaer > Fakturapulje** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="8bf27-134">Velg **Bestilling** for å opprette en leverandørfaktura fra fakturaen i puljen.</span><span class="sxs-lookup"><span data-stu-id="8bf27-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="8bf27-135">Velg fakturaen du vil se gjennom.</span><span class="sxs-lookup"><span data-stu-id="8bf27-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="8bf27-136">Velg **Oppdater samsvarsstatus** for å fullføre samsvaret.</span><span class="sxs-lookup"><span data-stu-id="8bf27-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="8bf27-137">Velg **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="8bf27-138">Velg **Endre visning**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-138">Select **Change view**.</span></span>
7. <span data-ttu-id="8bf27-139">Velg **Rutenettvisning**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="8bf27-140">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-140">Select **Post**.</span></span>
9. <span data-ttu-id="8bf27-141">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8bf27-141">Close the form.</span></span>
10. <span data-ttu-id="8bf27-142">Gå til **Moduler > Leverandører > Leverandører > Leverandører** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="8bf27-143">Velg leverandøren som var på bestillingen.</span><span class="sxs-lookup"><span data-stu-id="8bf27-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="8bf27-144">Velg for eksempel leverandør **1001**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="8bf27-145">Velg **Leverandør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8bf27-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="8bf27-146">Velg **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="8bf27-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="8bf27-147">Merk fakturaen som du opprettet.</span><span class="sxs-lookup"><span data-stu-id="8bf27-147">Select the invoice that you created.</span></span> <span data-ttu-id="8bf27-148">Ankomstregistreringsavsetningen ble tilbakeført og postert til den aktuelle kontoen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="8bf27-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]