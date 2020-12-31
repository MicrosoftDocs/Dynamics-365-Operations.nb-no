---
title: Garantibrevtransaksjon
description: Denne prosedyren hjelper deg gjennom garantibrevprosessen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446490"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="eec18-103">Garantibrevtransaksjon</span><span class="sxs-lookup"><span data-stu-id="eec18-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eec18-104">Denne prosedyren hjelper deg gjennom garantibrevprosessen.</span><span class="sxs-lookup"><span data-stu-id="eec18-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="eec18-105">Følgende oppgaver må være fullført før du kan gjennomføre denne prosedyren:</span><span class="sxs-lookup"><span data-stu-id="eec18-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="eec18-106">Definere bankfasiliteter og posteringsprofiler for et garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="eec18-107">Opprette en bankfasilitetsavtale for en remburs.</span><span class="sxs-lookup"><span data-stu-id="eec18-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="eec18-108">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="eec18-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="eec18-109">Opprette salgsordre med garantibrev</span><span class="sxs-lookup"><span data-stu-id="eec18-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="eec18-110">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="eec18-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="eec18-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="eec18-111">Click New.</span></span>
3. <span data-ttu-id="eec18-112">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="eec18-113">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="eec18-113">Expand the General section.</span></span>
5. <span data-ttu-id="eec18-114">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="eec18-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="eec18-116">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="eec18-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="eec18-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="eec18-118">Velg Garantibrev i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="eec18-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="eec18-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-119">Click OK.</span></span>
11. <span data-ttu-id="eec18-120">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="eec18-121">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="eec18-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="eec18-122">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="eec18-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="eec18-123">Velg kategorien Levering.</span><span class="sxs-lookup"><span data-stu-id="eec18-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="eec18-124">Obs!  Velg Leveringsdatokontroll = Ingen</span><span class="sxs-lookup"><span data-stu-id="eec18-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="eec18-125">Angi en dato i feltet Ønsket forsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="eec18-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="eec18-126">Angi en dato i Bekreftet forsendelsesdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="eec18-127">Behandle garantibrev_Forespørsel</span><span class="sxs-lookup"><span data-stu-id="eec18-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="eec18-128">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="eec18-129">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="eec18-130">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="eec18-131">Klikk Forespørsel for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="eec18-132">Angi eller velg en verdi i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="eec18-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="eec18-134">Angi et tall i Verdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="eec18-135">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="eec18-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="eec18-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-136">Click OK.</span></span>
10. <span data-ttu-id="eec18-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eec18-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="eec18-138">Behandle garantibrev_Send til bank</span><span class="sxs-lookup"><span data-stu-id="eec18-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="eec18-139">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="eec18-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eec18-141">Klikk Send til bank for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="eec18-142">Angi eller velg en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="eec18-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="eec18-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="eec18-145">Behandle garantibrev_Motta fra bank</span><span class="sxs-lookup"><span data-stu-id="eec18-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="eec18-146">Klikk Motta fra bank for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="eec18-147">Skriv inn en verdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="eec18-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="eec18-148">Kontroller verdiene som er beregnet, i feltene Margin og Utgift.</span><span class="sxs-lookup"><span data-stu-id="eec18-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="eec18-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-149">Click OK.</span></span>
4. <span data-ttu-id="eec18-150">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="eec18-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="eec18-151">Kontroller posten Motta fra bank.</span><span class="sxs-lookup"><span data-stu-id="eec18-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="eec18-152">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="eec18-153">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="eec18-153">Click Lines.</span></span>
    * <span data-ttu-id="eec18-154">Kontroller posteringen av journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="eec18-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="eec18-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eec18-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="eec18-156">Behandle garantibrev_Gi til mottaker</span><span class="sxs-lookup"><span data-stu-id="eec18-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="eec18-157">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="eec18-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="eec18-158">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="eec18-159">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="eec18-160">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="eec18-161">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="eec18-162">Klikk Gi til mottaker for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="eec18-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-163">Click OK.</span></span>
8. <span data-ttu-id="eec18-164">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="eec18-165">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="eec18-166">Klikk Gi til mottaker for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="eec18-167">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-167">Click OK.</span></span>
12. <span data-ttu-id="eec18-168">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="eec18-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="eec18-169">Valider posten Gi til mottaker.</span><span class="sxs-lookup"><span data-stu-id="eec18-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="eec18-170">Behandle garantibrev_Øk verdi</span><span class="sxs-lookup"><span data-stu-id="eec18-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="eec18-171">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="eec18-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="eec18-172">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="eec18-173">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="eec18-174">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="eec18-175">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="eec18-176">Klikk Øk verdi for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="eec18-177">Angi en verdi i feltet Verdi som skal legges til.</span><span class="sxs-lookup"><span data-stu-id="eec18-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="eec18-178">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-178">Click OK.</span></span>
9. <span data-ttu-id="eec18-179">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="eec18-180">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="eec18-181">Klikk Øk verdi for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="eec18-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-182">Click OK.</span></span>
13. <span data-ttu-id="eec18-183">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="eec18-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="eec18-184">Kontroller posten Øk verdi.</span><span class="sxs-lookup"><span data-stu-id="eec18-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="eec18-185">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="eec18-186">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="eec18-187">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="eec18-187">Click Lines.</span></span>
    * <span data-ttu-id="eec18-188">Kontroller de posterte journaloppføringene.</span><span class="sxs-lookup"><span data-stu-id="eec18-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="eec18-189">Behandle garantibrev_Avvikle</span><span class="sxs-lookup"><span data-stu-id="eec18-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="eec18-190">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="eec18-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="eec18-191">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="eec18-192">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="eec18-193">Klikk Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="eec18-194">Klikk Garantibrev i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eec18-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="eec18-195">Klikk Avvikle for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="eec18-196">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-196">Click OK.</span></span>
8. <span data-ttu-id="eec18-197">Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="eec18-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="eec18-198">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="eec18-199">Klikk Avvikle for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eec18-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="eec18-200">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eec18-200">Click OK.</span></span>
12. <span data-ttu-id="eec18-201">Utvid Handlinger-delen.</span><span class="sxs-lookup"><span data-stu-id="eec18-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="eec18-202">Kontroller posten Avvikle.</span><span class="sxs-lookup"><span data-stu-id="eec18-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="eec18-203">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eec18-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="eec18-204">Klikk for å følge koblingen i Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eec18-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="eec18-205">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="eec18-205">Click Lines.</span></span>
    * <span data-ttu-id="eec18-206">Kontroller de posterte journaloppføringene.</span><span class="sxs-lookup"><span data-stu-id="eec18-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="eec18-207">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eec18-207">Close the page.</span></span>

