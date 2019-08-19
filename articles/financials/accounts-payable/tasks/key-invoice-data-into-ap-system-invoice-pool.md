---
title: Registrere fakturadata i AP-systemet ved hjelp av fakturapulje
description: Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til å opprette fakturaer.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843223"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="92fdf-103">Registrere fakturadata i AP-systemet ved hjelp av fakturapulje</span><span class="sxs-lookup"><span data-stu-id="92fdf-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92fdf-104">Denne oppgaveveiledningen viser hvordan du bruker ankomstregistreringen til å opprette fakturaer.</span><span class="sxs-lookup"><span data-stu-id="92fdf-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="92fdf-105">Bruk deretter fakturapuljen for å samsvare fakturaen med en bestilling og fullføre kostnaden på leverandørens fakturaside.</span><span class="sxs-lookup"><span data-stu-id="92fdf-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="92fdf-106">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="92fdf-106">Create a purchase order</span></span>
1. <span data-ttu-id="92fdf-107">Gå til Leverandører > Bestillinger > Bestillinger.</span><span class="sxs-lookup"><span data-stu-id="92fdf-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="92fdf-108">Klikk Ny for å opprette en ny bestilling.</span><span class="sxs-lookup"><span data-stu-id="92fdf-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="92fdf-109">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="92fdf-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="92fdf-110">Velg leverandøren fra listen.</span><span class="sxs-lookup"><span data-stu-id="92fdf-110">Select the vendor from the list.</span></span> <span data-ttu-id="92fdf-111">For eksempel leverandør 1001.</span><span class="sxs-lookup"><span data-stu-id="92fdf-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="92fdf-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="92fdf-112">Click OK.</span></span>
6. <span data-ttu-id="92fdf-113">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="92fdf-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="92fdf-114">Finn varenummeret for tjenesten i listen.</span><span class="sxs-lookup"><span data-stu-id="92fdf-114">Find the services item number in the list.</span></span> <span data-ttu-id="92fdf-115">Velg for eksempel S0001.</span><span class="sxs-lookup"><span data-stu-id="92fdf-115">For example, select S0001.</span></span>
8. <span data-ttu-id="92fdf-116">Klikk på varenummeret og velg det.</span><span class="sxs-lookup"><span data-stu-id="92fdf-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="92fdf-117">Nettbeløpet er USD 75.00.</span><span class="sxs-lookup"><span data-stu-id="92fdf-117">The net amount is 75.00.</span></span>  <span data-ttu-id="92fdf-118">Dette er beløpet vi forventer å se på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="92fdf-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="92fdf-119">Klikk Innkjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="92fdf-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="92fdf-120">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="92fdf-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="92fdf-121">Opprette og postere en faktura</span><span class="sxs-lookup"><span data-stu-id="92fdf-121">Create and post and invoice</span></span>
1. <span data-ttu-id="92fdf-122">Gå til Leverandører > Fakturaer > Ankomstregistrering.</span><span class="sxs-lookup"><span data-stu-id="92fdf-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="92fdf-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="92fdf-123">Click New.</span></span>
3. <span data-ttu-id="92fdf-124">Åpne oppslaget for å velge navnet på ankomstregistreringen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="92fdf-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="92fdf-125">Velg navnet på ankomstregistreringen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="92fdf-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="92fdf-126">Klikk Linjer for å åpne registeret og angi utgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="92fdf-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="92fdf-127">Velg en leverandør i oppslaget.</span><span class="sxs-lookup"><span data-stu-id="92fdf-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="92fdf-128">Klikk for eksempel på leverandør 1001.</span><span class="sxs-lookup"><span data-stu-id="92fdf-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="92fdf-129">I Faktura-feltet angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="92fdf-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="92fdf-130">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="92fdf-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="92fdf-131">Angi et tall i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="92fdf-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="92fdf-132">Klikk rullegardinknappen i Bestilling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="92fdf-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="92fdf-133">Velg bestillingen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="92fdf-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="92fdf-134">Klikk rullegardinknappen i Godkjent av-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="92fdf-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="92fdf-135">Merk en godkjenner, og klikk Velg for å velge denne godkjenneren.</span><span class="sxs-lookup"><span data-stu-id="92fdf-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="92fdf-136">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="92fdf-136">Click Post.</span></span>
15. <span data-ttu-id="92fdf-137">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="92fdf-137">Close the form.</span></span>
16. <span data-ttu-id="92fdf-138">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="92fdf-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="92fdf-139">Åpne en faktura fra utvalget og sammenlign den med en bestilling for å fullføre fakturaprosessen</span><span class="sxs-lookup"><span data-stu-id="92fdf-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="92fdf-140">Gå til Leverandører > Fakturaer > Fakturapulje.</span><span class="sxs-lookup"><span data-stu-id="92fdf-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="92fdf-141">Klikk Bestilling for å opprette en leverandørfaktura fra fakturaen i puljen.</span><span class="sxs-lookup"><span data-stu-id="92fdf-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="92fdf-142">Velg fakturaen du vil se gjennom.</span><span class="sxs-lookup"><span data-stu-id="92fdf-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="92fdf-143">Klikk Oppdater samsvarsstatus for å fullføre samsvaret.</span><span class="sxs-lookup"><span data-stu-id="92fdf-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="92fdf-144">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="92fdf-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="92fdf-145">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="92fdf-145">Click Change view.</span></span>
7. <span data-ttu-id="92fdf-146">Klikk Rutenettvisning.</span><span class="sxs-lookup"><span data-stu-id="92fdf-146">Click Grid view.</span></span>
8. <span data-ttu-id="92fdf-147">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="92fdf-147">Click Post.</span></span>
9. <span data-ttu-id="92fdf-148">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="92fdf-148">Close the form.</span></span>
10. <span data-ttu-id="92fdf-149">Gå til Leverandører > Leverandører > Leverandører.</span><span class="sxs-lookup"><span data-stu-id="92fdf-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="92fdf-150">Velg leverandøren som var på bestillingen.</span><span class="sxs-lookup"><span data-stu-id="92fdf-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="92fdf-151">Velg for eksempel leverandør 1001.</span><span class="sxs-lookup"><span data-stu-id="92fdf-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="92fdf-152">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="92fdf-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="92fdf-153">Klikk Leverandør i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="92fdf-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="92fdf-154">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="92fdf-154">Click Transactions.</span></span>
15. <span data-ttu-id="92fdf-155">Merk fakturaen som du opprettet.</span><span class="sxs-lookup"><span data-stu-id="92fdf-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="92fdf-156">Ankomstregistreringsavsetningen ble tilbakeført og postert til den aktuelle kontoen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="92fdf-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

