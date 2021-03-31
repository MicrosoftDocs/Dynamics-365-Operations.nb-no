---
title: Opprette en avskrivningsjournal for en kunde
description: Denne oppgaveveiledningen viser hvordan du definerer parameterne for avskrivninger og deretter skriver av transaksjoner fra Innkrevinger-siden, siden Åpne kundefakturaer og Kunde-siden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 182afb5b105fec6dcac323b4f98db5fb7b3e0d68
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220281"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="e1342-103">Opprette en avskrivningsjournal for en kunde</span><span class="sxs-lookup"><span data-stu-id="e1342-103">Create a write-off journal for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1342-104">Denne oppgaveveiledningen viser hvordan du definerer parameterne for avskrivninger og deretter skriver av transaksjoner fra Innkrevinger-siden, siden Åpne kundefakturaer og Kunde-siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="e1342-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e1342-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="e1342-106">Konfigurere avskrivningsparameterne</span><span class="sxs-lookup"><span data-stu-id="e1342-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="e1342-107">Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="e1342-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="e1342-108">Klikk fanen **Innkrevinger**.</span><span class="sxs-lookup"><span data-stu-id="e1342-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="e1342-109">Vis eller skjul **Avskrive**-delen.</span><span class="sxs-lookup"><span data-stu-id="e1342-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="e1342-110">**Avskrivningsjournalen** er økonomijournalen som skal inneholde avskrivningstransaksjonene som du oppretter.</span><span class="sxs-lookup"><span data-stu-id="e1342-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="e1342-111">Du kan knytte en årsakskode til hver avskrivning.</span><span class="sxs-lookup"><span data-stu-id="e1342-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="e1342-112">Du kan overskrive denne standardverdien under avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="e1342-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="e1342-113">Angi **Separat merverdiavgift** til Ja hvis du vil skille merverdiavgiften fra den opprinnelige transaksjonen i avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="e1342-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="e1342-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-114">Close the page.</span></span>
5. <span data-ttu-id="e1342-115">Gå til **Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="e1342-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="e1342-116">Avskrivningskontoen skal brukes som utgiftskontoen eller reserverejustering i økonomijournalen.</span><span class="sxs-lookup"><span data-stu-id="e1342-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="e1342-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="e1342-118">Avskrive en kundesaldo fra siden Aldersfordelte saldoer</span><span class="sxs-lookup"><span data-stu-id="e1342-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="e1342-119">Gå til **Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer**.</span><span class="sxs-lookup"><span data-stu-id="e1342-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="e1342-120">Merk raden for kunden som du vil skrive av.</span><span class="sxs-lookup"><span data-stu-id="e1342-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="e1342-121">Merk for eksempel linjen med Birch firma på den.</span><span class="sxs-lookup"><span data-stu-id="e1342-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="e1342-122">Klikk **Innkreving** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="e1342-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="e1342-123">Klikk **Avskrive**.</span><span class="sxs-lookup"><span data-stu-id="e1342-123">Click **Write off**.</span></span>
5. <span data-ttu-id="e1342-124">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1342-124">Click **OK**.</span></span>
6. <span data-ttu-id="e1342-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-125">Close the page.</span></span>
7. <span data-ttu-id="e1342-126">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppføringer > Økonomijournaler**.</span><span class="sxs-lookup"><span data-stu-id="e1342-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="e1342-127">Velg journalpartinummeret for journalen som inneholder avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="e1342-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="e1342-128">Det opprettes én linje for å tilbakeføre kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="e1342-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="e1342-129">Én eller flere linjer opprettes for å postere avskrivningen til avskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="e1342-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="e1342-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-130">Close the page.</span></span>
10. <span data-ttu-id="e1342-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="e1342-132">Skriv av transaksjoner fra purreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="e1342-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="e1342-133">Gå til **Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer**.</span><span class="sxs-lookup"><span data-stu-id="e1342-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="e1342-134">Velg navnet på kunden som har transaksjonene du vil skrive av.</span><span class="sxs-lookup"><span data-stu-id="e1342-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="e1342-135">Velg for eksempel Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="e1342-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="e1342-136">Merk raden for den første transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="e1342-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="e1342-137">Merk raden for den andre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="e1342-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="e1342-138">Klikk **Avskrive**.</span><span class="sxs-lookup"><span data-stu-id="e1342-138">Click **Write off**.</span></span>
6. <span data-ttu-id="e1342-139">Skriv inn "Misligholdt gjeld" i **Årsakskommentar**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e1342-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="e1342-140">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1342-140">Click **OK**.</span></span>
8. <span data-ttu-id="e1342-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-141">Close the page.</span></span>
9. <span data-ttu-id="e1342-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-142">Close the page.</span></span>
10. <span data-ttu-id="e1342-143">Gå til **Økonomimodul > Journaloppføringer > Økonomijournaler**.</span><span class="sxs-lookup"><span data-stu-id="e1342-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="e1342-144">Velg journalpartinummeret for journalen som inneholder avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="e1342-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="e1342-145">Det opprettes én linje for å tilbakeføre kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="e1342-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="e1342-146">Én eller flere linjer opprettes for å postere avskrivningen til avskrivningskontoen.</span><span class="sxs-lookup"><span data-stu-id="e1342-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="e1342-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-147">Close the page.</span></span>
13. <span data-ttu-id="e1342-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="e1342-149">Skrive av en faktura fra siden Åpne kundefakturaer</span><span class="sxs-lookup"><span data-stu-id="e1342-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="e1342-150">Gå til **Navigasjonsrute > Moduler > Kunder > Fakturaer > Åpne fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="e1342-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="e1342-151">Merk linjen for en faktura.</span><span class="sxs-lookup"><span data-stu-id="e1342-151">Mark the line for an invoice.</span></span> <span data-ttu-id="e1342-152">Merk for eksempel linjen for CIV-000667..</span><span class="sxs-lookup"><span data-stu-id="e1342-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="e1342-153">Klikk **Faktura** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="e1342-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="e1342-154">Klikk **Avskrive**.</span><span class="sxs-lookup"><span data-stu-id="e1342-154">Click **Write off**.</span></span>
5. <span data-ttu-id="e1342-155">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1342-155">Click **OK**.</span></span>
6. <span data-ttu-id="e1342-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="e1342-157">Skrive av en kundesaldo fra kundesiden</span><span class="sxs-lookup"><span data-stu-id="e1342-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="e1342-158">Gå til **Kunder > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="e1342-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="e1342-159">Velg en kundekonto.</span><span class="sxs-lookup"><span data-stu-id="e1342-159">Select a customer account.</span></span> <span data-ttu-id="e1342-160">Velg for eksempel US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="e1342-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="e1342-161">Klikk **Innkreving** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="e1342-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="e1342-162">Klikk **Avskrive**.</span><span class="sxs-lookup"><span data-stu-id="e1342-162">Click **Write off**.</span></span>
5. <span data-ttu-id="e1342-163">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1342-163">Click **OK**.</span></span>
6. <span data-ttu-id="e1342-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e1342-164">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]