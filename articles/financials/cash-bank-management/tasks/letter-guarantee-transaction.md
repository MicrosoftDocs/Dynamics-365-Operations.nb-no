--- 
title: Garantibrevtransaksjon
description: Denne prosedyren hjelper deg gjennom garantibrevprosessen.
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 182b6eb0f9aa1ceffd2336ecb217d3e29e3046d6
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="b7595-103">Garantibrevtransaksjon</span><span class="sxs-lookup"><span data-stu-id="b7595-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7595-104">Denne prosedyren hjelper deg gjennom garantibrevprosessen.</span><span class="sxs-lookup"><span data-stu-id="b7595-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="b7595-105">Følgende oppgaver må være fullført før du kan gjennomføre denne prosedyren:</span><span class="sxs-lookup"><span data-stu-id="b7595-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="b7595-106">Definere bankfasiliteter og posteringsprofiler for et garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="b7595-107">Opprette en bankfasilitetsavtale for en remburs.</span><span class="sxs-lookup"><span data-stu-id="b7595-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="b7595-108">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b7595-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="b7595-109">Opprette salgsordre med garantibrev</span><span class="sxs-lookup"><span data-stu-id="b7595-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="b7595-110">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b7595-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b7595-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b7595-111">Click New.</span></span>
3. <span data-ttu-id="b7595-112">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="b7595-113">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b7595-113">Expand the General section.</span></span>
5. <span data-ttu-id="b7595-114">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="b7595-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b7595-116">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="b7595-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="b7595-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b7595-118">Velg Garantibrev i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="b7595-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="b7595-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-119">Click OK.</span></span>
11. <span data-ttu-id="b7595-120">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="b7595-121">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="b7595-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="b7595-122">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="b7595-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="b7595-123">Velg kategorien Levering.</span><span class="sxs-lookup"><span data-stu-id="b7595-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="b7595-124">Obs!  Velg Leveringsdatokontroll = Ingen</span><span class="sxs-lookup"><span data-stu-id="b7595-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="b7595-125">Angi en dato i feltet Ønsket forsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="b7595-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="b7595-126">Angi en dato i Bekreftet forsendelsesdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="b7595-127">Behandle garantibrev_Forespørsel</span><span class="sxs-lookup"><span data-stu-id="b7595-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="b7595-128">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="b7595-129">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="b7595-130">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="b7595-131">Klikk Forespørsel for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="b7595-132">Angi eller velg en verdi i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="b7595-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b7595-134">Angi et tall i Verdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="b7595-135">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="b7595-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="b7595-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-136">Click OK.</span></span>
10. <span data-ttu-id="b7595-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b7595-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="b7595-138">Behandle garantibrev_Send til bank</span><span class="sxs-lookup"><span data-stu-id="b7595-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="b7595-139">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="b7595-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b7595-141">Klikk Send til bank for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="b7595-142">Angi eller velg en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="b7595-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b7595-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="b7595-145">Behandle garantibrev_Motta fra bank</span><span class="sxs-lookup"><span data-stu-id="b7595-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="b7595-146">Klikk Motta fra bank for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="b7595-147">Skriv inn en verdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="b7595-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="b7595-148">Kontroller verdiene som er beregnet, i feltene Margin og Utgift.</span><span class="sxs-lookup"><span data-stu-id="b7595-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="b7595-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-149">Click OK.</span></span>
4. <span data-ttu-id="b7595-150">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="b7595-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="b7595-151">Kontroller posten Motta fra bank.</span><span class="sxs-lookup"><span data-stu-id="b7595-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="b7595-152">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="b7595-153">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="b7595-153">Click Lines.</span></span>
    * <span data-ttu-id="b7595-154">Kontroller posteringen av journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="b7595-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="b7595-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b7595-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="b7595-156">Behandle garantibrev_Gi til mottaker</span><span class="sxs-lookup"><span data-stu-id="b7595-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="b7595-157">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b7595-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b7595-158">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b7595-159">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="b7595-160">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="b7595-161">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="b7595-162">Klikk Gi til mottaker for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="b7595-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-163">Click OK.</span></span>
8. <span data-ttu-id="b7595-164">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="b7595-165">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b7595-166">Klikk Gi til mottaker for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="b7595-167">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-167">Click OK.</span></span>
12. <span data-ttu-id="b7595-168">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="b7595-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="b7595-169">Valider posten Gi til mottaker.</span><span class="sxs-lookup"><span data-stu-id="b7595-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="b7595-170">Behandle garantibrev_Øk verdi</span><span class="sxs-lookup"><span data-stu-id="b7595-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="b7595-171">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b7595-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b7595-172">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b7595-173">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="b7595-174">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="b7595-175">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="b7595-176">Klikk Øk verdi for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="b7595-177">Angi en verdi i feltet Verdi som skal legges til.</span><span class="sxs-lookup"><span data-stu-id="b7595-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="b7595-178">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-178">Click OK.</span></span>
9. <span data-ttu-id="b7595-179">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="b7595-180">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="b7595-181">Klikk Øk verdi for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="b7595-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-182">Click OK.</span></span>
13. <span data-ttu-id="b7595-183">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="b7595-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="b7595-184">Kontroller posten Øk verdi.</span><span class="sxs-lookup"><span data-stu-id="b7595-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="b7595-185">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b7595-186">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="b7595-187">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="b7595-187">Click Lines.</span></span>
    * <span data-ttu-id="b7595-188">Kontroller de posterte journaloppføringene.</span><span class="sxs-lookup"><span data-stu-id="b7595-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="b7595-189">Behandle garantibrev_Avvikle</span><span class="sxs-lookup"><span data-stu-id="b7595-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="b7595-190">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b7595-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b7595-191">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b7595-192">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="b7595-193">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="b7595-194">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7595-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="b7595-195">Klikk Avvikle for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="b7595-196">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-196">Click OK.</span></span>
8. <span data-ttu-id="b7595-197">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="b7595-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="b7595-198">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b7595-199">Klikk Avvikle for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b7595-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="b7595-200">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b7595-200">Click OK.</span></span>
12. <span data-ttu-id="b7595-201">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="b7595-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="b7595-202">Kontroller posten Avvikle.</span><span class="sxs-lookup"><span data-stu-id="b7595-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="b7595-203">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b7595-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b7595-204">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b7595-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="b7595-205">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="b7595-205">Click Lines.</span></span>
    * <span data-ttu-id="b7595-206">Kontroller de posterte journaloppføringene.</span><span class="sxs-lookup"><span data-stu-id="b7595-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="b7595-207">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b7595-207">Close the page.</span></span>


