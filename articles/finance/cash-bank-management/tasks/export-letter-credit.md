---
title: Eksporter remburser
description: Denne prosedyren hjelper deg med å eksportere en remburs.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 260ef2d05e1f21708817346af2db2841aa6acdd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834794"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="ef8ba-103">Eksporter remburser</span><span class="sxs-lookup"><span data-stu-id="ef8ba-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef8ba-104">Denne prosedyren hjelper deg med å eksportere en remburs.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="ef8ba-105">En remburs er en avtale som utstedes av en bank, der banken godtar å sikre betaling på vegne av kjøperen hvis vilkårene i avtalen mellom kjøper og selger er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="ef8ba-106">Kjør prosedyren Definere Bankfasilitetene og posteringsprofilene og Opprette en fasilitetsavtale for remburs før denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="ef8ba-107">Demonstrasjonsfirmaet USMF må velges for at denne prosedyren skal kunne kjøres.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="ef8ba-108">Opprette salgsordre for remburseksport</span><span class="sxs-lookup"><span data-stu-id="ef8ba-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="ef8ba-109">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ef8ba-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-110">Click New.</span></span>
3. <span data-ttu-id="ef8ba-111">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ef8ba-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ef8ba-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ef8ba-114">Vis eller skjul delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="ef8ba-115">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef8ba-116">Velg stedet der varen som skal utstedes, er på lager.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="ef8ba-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ef8ba-118">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef8ba-119">Velg lageret der varen som skal utstedes, befinner seg.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="ef8ba-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef8ba-121">Obs!  Feltet Bankdokumenttype må velges med verdien Remburs.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="ef8ba-122">Velg Remburs i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="ef8ba-123">Vis eller skjul Levering-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="ef8ba-124">Velg Leveringsdatokontroll = Ingen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="ef8ba-125">Angi en dato i feltet Ønsket leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="ef8ba-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-126">Click OK.</span></span>
15. <span data-ttu-id="ef8ba-127">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef8ba-128">Velg varen som skal utstedes/selges.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="ef8ba-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ef8ba-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ef8ba-131">Angi et tall i Enhetspris-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="ef8ba-132">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="ef8ba-133">Velg kategorien Levering.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="ef8ba-134">Angi en dato i feltet Ønsket forsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="ef8ba-135">Angi en dato i Bekreftet forsendelsesdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="ef8ba-136">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="ef8ba-137">Klikk Remburs.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="ef8ba-138">Angi en verdi i feltet Bankdokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="ef8ba-139">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="ef8ba-140">Vis eller skjul Bankdetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="ef8ba-141">Klikk rullegardinknappen i Rembursbank-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="ef8ba-142">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="ef8ba-143">Klikk rullegardinknappen i Advisbank-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="ef8ba-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="ef8ba-145">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="ef8ba-146">Klikk Hent salgsordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="ef8ba-147">Klikk Utsted bankdokument.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="ef8ba-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="ef8ba-149">Postere følgeseddel</span><span class="sxs-lookup"><span data-stu-id="ef8ba-149">Post Packing slip</span></span>
1. <span data-ttu-id="ef8ba-150">Klikk Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="ef8ba-151">Klikk Poster følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="ef8ba-152">Vis eller skjul delen Parametere.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="ef8ba-153">Velg Alle i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="ef8ba-154">Vis eller skjul Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="ef8ba-155">Angi en dato i Følgeseddeldato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="ef8ba-156">Velg forsendelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="ef8ba-157">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ef8ba-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-158">Click OK.</span></span>
10. <span data-ttu-id="ef8ba-159">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="ef8ba-160">Postere salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="ef8ba-160">Post sales invoice</span></span>
1. <span data-ttu-id="ef8ba-161">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="ef8ba-162">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-162">Click Invoice.</span></span>
3. <span data-ttu-id="ef8ba-163">Vis eller skjul Oversikt-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="ef8ba-164">Velg forsendelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="ef8ba-165">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ef8ba-166">Vis eller skjul Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="ef8ba-167">Angi en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="ef8ba-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-168">Click OK.</span></span>
9. <span data-ttu-id="ef8ba-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="ef8ba-170">Status for sendt forsendelsesdokument</span><span class="sxs-lookup"><span data-stu-id="ef8ba-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="ef8ba-171">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="ef8ba-172">Klikk Remburs.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="ef8ba-173">Vis eller skjul Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="ef8ba-174">Obs!  Feltet Dokumentet er sendt må settes til Ja.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="ef8ba-175">Kontrollere remburseksport</span><span class="sxs-lookup"><span data-stu-id="ef8ba-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="ef8ba-176">Gå til Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="ef8ba-177">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ef8ba-178">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef8ba-179">Kontroller at Eksporter remburs har forsendelsesstatusen Fakturert.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="ef8ba-180">Kundebetaling</span><span class="sxs-lookup"><span data-stu-id="ef8ba-180">Customer payment</span></span>
1. <span data-ttu-id="ef8ba-181">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ef8ba-182">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-182">Click New.</span></span>
3. <span data-ttu-id="ef8ba-183">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ef8ba-184">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ef8ba-185">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ef8ba-186">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-186">Click Lines.</span></span>
7. <span data-ttu-id="ef8ba-187">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="ef8ba-188">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="ef8ba-189">Klikk Utligning.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-189">Click Settlement.</span></span>
10. <span data-ttu-id="ef8ba-190">Merk av i boksen i hodet i Totaler.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="ef8ba-191">Obs!  Sett Vis felt til Remburs.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="ef8ba-192">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ef8ba-193">Merk av eller fjern merket i avmerkingsboksen Merk.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="ef8ba-194">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-194">Click OK.</span></span>
14. <span data-ttu-id="ef8ba-195">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="ef8ba-196">Kontrollere detaljene om bankdokumentnummer og forsendelsesnummer</span><span class="sxs-lookup"><span data-stu-id="ef8ba-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="ef8ba-197">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="ef8ba-198">Kontrollere remburseksport etter betaling</span><span class="sxs-lookup"><span data-stu-id="ef8ba-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="ef8ba-199">Gå til Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="ef8ba-200">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ef8ba-201">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef8ba-202">Kontroller at forsendelsesstatus = betaling mottatt og saldobeløp = 0,00.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]