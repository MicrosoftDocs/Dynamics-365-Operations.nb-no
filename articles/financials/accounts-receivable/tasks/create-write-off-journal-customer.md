--- 
title: Opprette en avskrivningsjournal for en kunde
description: "Denne oppgaveveiledningen viser hvordan du definerer parameterne for avskrivninger og deretter skriver av transaksjoner fra Innkrevinger-siden, siden Åpne kundefakturaer og Kunde-siden."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="405f6-103">Opprette en avskrivningsjournal for en kunde</span><span class="sxs-lookup"><span data-stu-id="405f6-103">Create a write-off journal for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="405f6-104">Denne oppgaveveiledningen viser hvordan du definerer parameterne for avskrivninger og deretter skriver av transaksjoner fra Innkrevinger-siden, siden Åpne kundefakturaer og Kunde-siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="405f6-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="405f6-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="405f6-106">Konfigurere avskrivningsparameterne</span><span class="sxs-lookup"><span data-stu-id="405f6-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="405f6-107">Gå til Kreditt og innkreving > Oppsett > Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="405f6-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="405f6-108">Klikk kategorien Innkrevinger.</span><span class="sxs-lookup"><span data-stu-id="405f6-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="405f6-109">Vis eller skjul Avskrive-delen.</span><span class="sxs-lookup"><span data-stu-id="405f6-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="405f6-110">Avskrivningsjournalen er økonomijournalen som skal inneholde avskrivningstransaksjonene som du oppretter.</span><span class="sxs-lookup"><span data-stu-id="405f6-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="405f6-111">Du kan knytte en årsakskode til hver avskrivning.</span><span class="sxs-lookup"><span data-stu-id="405f6-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="405f6-112">Du kan overskrive denne standardverdien under avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="405f6-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="405f6-113">Angi dette som Ja hvis du vil skille merverdiavgiften fra den opprinnelige transaksjonen i avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="405f6-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="405f6-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-114">Close the page.</span></span>
5. <span data-ttu-id="405f6-115">Gå til Kreditt og innkreving > Oppsett > Kundeposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="405f6-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="405f6-116">Avskrivningskontoen skal brukes som utgiftskontoen eller reserverejustering i økonomijournalen.</span><span class="sxs-lookup"><span data-stu-id="405f6-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="405f6-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="405f6-118">Avskrive en kundesaldo fra siden Aldersfordelte saldoer</span><span class="sxs-lookup"><span data-stu-id="405f6-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="405f6-119">Gå til Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer.</span><span class="sxs-lookup"><span data-stu-id="405f6-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="405f6-120">Merk raden for kunden som du vil skrive av.</span><span class="sxs-lookup"><span data-stu-id="405f6-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="405f6-121">Merk for eksempel linjen med Birch firma på den.</span><span class="sxs-lookup"><span data-stu-id="405f6-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="405f6-122">Klikk Innkreving i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="405f6-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="405f6-123">Klikk Avskrive.</span><span class="sxs-lookup"><span data-stu-id="405f6-123">Click Write off.</span></span>
5. <span data-ttu-id="405f6-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="405f6-124">Click OK.</span></span>
6. <span data-ttu-id="405f6-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-125">Close the page.</span></span>
7. <span data-ttu-id="405f6-126">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="405f6-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="405f6-127">Velg journalpartinummeret for journalen som inneholder avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="405f6-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="405f6-128">Det opprettes én linje for å tilbakeføre kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="405f6-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="405f6-129">Én eller flere linjer opprettes for å postere avskrivningen til avskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="405f6-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="405f6-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-130">Close the page.</span></span>
10. <span data-ttu-id="405f6-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="405f6-132">Skriv av transaksjoner fra purreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="405f6-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="405f6-133">Gå til Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer.</span><span class="sxs-lookup"><span data-stu-id="405f6-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="405f6-134">Velg navnet på kunden som har transaksjonene du vil skrive av.</span><span class="sxs-lookup"><span data-stu-id="405f6-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="405f6-135">Velg for eksempel Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="405f6-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="405f6-136">Merk raden for den første transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="405f6-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="405f6-137">Merk raden for den andre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="405f6-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="405f6-138">Klikk Avskrive.</span><span class="sxs-lookup"><span data-stu-id="405f6-138">Click Write off.</span></span>
6. <span data-ttu-id="405f6-139">Skriv inn "Misligholdt gjeld" i Årsakskommentar-feltet.</span><span class="sxs-lookup"><span data-stu-id="405f6-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="405f6-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="405f6-140">Click OK.</span></span>
8. <span data-ttu-id="405f6-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-141">Close the page.</span></span>
9. <span data-ttu-id="405f6-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-142">Close the page.</span></span>
10. <span data-ttu-id="405f6-143">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="405f6-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="405f6-144">Velg journalpartinummeret for journalen som inneholder avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="405f6-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="405f6-145">Det opprettes én linje for å tilbakeføre kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="405f6-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="405f6-146">Én eller flere linjer opprettes for å postere avskrivningen til avskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="405f6-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="405f6-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-147">Close the page.</span></span>
13. <span data-ttu-id="405f6-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="405f6-149">Skrive av en faktura fra siden Åpne kundefakturaer</span><span class="sxs-lookup"><span data-stu-id="405f6-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="405f6-150">Gå til Kunder > Fakturaer > Åpne kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="405f6-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="405f6-151">Merk linjen for en faktura.</span><span class="sxs-lookup"><span data-stu-id="405f6-151">Mark the line for an invoice.</span></span> <span data-ttu-id="405f6-152">Merk for eksempel linjen for CIV-000667..</span><span class="sxs-lookup"><span data-stu-id="405f6-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="405f6-153">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="405f6-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="405f6-154">Klikk Avskrive.</span><span class="sxs-lookup"><span data-stu-id="405f6-154">Click Write off.</span></span>
5. <span data-ttu-id="405f6-155">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="405f6-155">Click OK.</span></span>
6. <span data-ttu-id="405f6-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="405f6-157">Skrive av en kundesaldo fra kundesiden</span><span class="sxs-lookup"><span data-stu-id="405f6-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="405f6-158">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="405f6-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="405f6-159">Velg en kundekonto.</span><span class="sxs-lookup"><span data-stu-id="405f6-159">Select a customer account.</span></span> <span data-ttu-id="405f6-160">Velg for eksempel US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="405f6-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="405f6-161">Klikk Innkreving i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="405f6-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="405f6-162">Klikk Avskrive.</span><span class="sxs-lookup"><span data-stu-id="405f6-162">Click Write off.</span></span>
5. <span data-ttu-id="405f6-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="405f6-163">Click OK.</span></span>
6. <span data-ttu-id="405f6-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="405f6-164">Close the page.</span></span>


