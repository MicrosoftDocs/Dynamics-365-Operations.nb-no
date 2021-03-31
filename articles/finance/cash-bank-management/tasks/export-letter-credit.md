---
title: Eksporter remburser
description: Denne prosedyren hjelper deg med å eksportere en remburs.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127f38e7db0a8c0703fd95274f45ff4ca49c131e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225447"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="83f34-103">Eksporter remburser</span><span class="sxs-lookup"><span data-stu-id="83f34-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83f34-104">Denne prosedyren hjelper deg med å eksportere en remburs.</span><span class="sxs-lookup"><span data-stu-id="83f34-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="83f34-105">En remburs er en avtale som utstedes av en bank, der banken godtar å sikre betaling på vegne av kjøperen hvis vilkårene i avtalen mellom kjøper og selger er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="83f34-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="83f34-106">Kjør prosedyren Definere Bankfasilitetene og posteringsprofilene og Opprette en fasilitetsavtale for remburs før denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="83f34-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="83f34-107">Demonstrasjonsfirmaet USMF må velges for at denne prosedyren skal kunne kjøres.</span><span class="sxs-lookup"><span data-stu-id="83f34-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="83f34-108">Opprette salgsordre for remburseksport</span><span class="sxs-lookup"><span data-stu-id="83f34-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="83f34-109">Gå til Kunder > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="83f34-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="83f34-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="83f34-110">Click New.</span></span>
3. <span data-ttu-id="83f34-111">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="83f34-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="83f34-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="83f34-114">Vis eller skjul delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="83f34-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="83f34-115">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="83f34-116">Velg stedet der varen som skal utstedes, er på lager.</span><span class="sxs-lookup"><span data-stu-id="83f34-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="83f34-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="83f34-118">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="83f34-119">Velg lageret der varen som skal utstedes, befinner seg.</span><span class="sxs-lookup"><span data-stu-id="83f34-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="83f34-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="83f34-121">Obs!  Feltet Bankdokumenttype må velges med verdien Remburs.</span><span class="sxs-lookup"><span data-stu-id="83f34-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="83f34-122">Velg Remburs i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="83f34-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="83f34-123">Vis eller skjul Levering-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="83f34-124">Velg Leveringsdatokontroll = Ingen.</span><span class="sxs-lookup"><span data-stu-id="83f34-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="83f34-125">Angi en dato i feltet Ønsket leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="83f34-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="83f34-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="83f34-126">Click OK.</span></span>
15. <span data-ttu-id="83f34-127">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="83f34-128">Velg varen som skal utstedes/selges.</span><span class="sxs-lookup"><span data-stu-id="83f34-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="83f34-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="83f34-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="83f34-131">Angi et tall i Enhetspris-feltet.</span><span class="sxs-lookup"><span data-stu-id="83f34-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="83f34-132">Vis eller skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="83f34-133">Velg kategorien Levering.</span><span class="sxs-lookup"><span data-stu-id="83f34-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="83f34-134">Angi en dato i feltet Ønsket forsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="83f34-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="83f34-135">Angi en dato i Bekreftet forsendelsesdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="83f34-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="83f34-136">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="83f34-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="83f34-137">Klikk Remburs.</span><span class="sxs-lookup"><span data-stu-id="83f34-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="83f34-138">Angi en verdi i feltet Bankdokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="83f34-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="83f34-139">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="83f34-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="83f34-140">Vis eller skjul Bankdetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="83f34-141">Klikk rullegardinknappen i Rembursbank-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="83f34-142">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="83f34-143">Klikk rullegardinknappen i Advisbank-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="83f34-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="83f34-145">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="83f34-146">Klikk Hent salgsordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="83f34-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="83f34-147">Klikk Utsted bankdokument.</span><span class="sxs-lookup"><span data-stu-id="83f34-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="83f34-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="83f34-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="83f34-149">Postere følgeseddel</span><span class="sxs-lookup"><span data-stu-id="83f34-149">Post Packing slip</span></span>
1. <span data-ttu-id="83f34-150">Klikk Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="83f34-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="83f34-151">Klikk Poster følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="83f34-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="83f34-152">Vis eller skjul delen Parametere.</span><span class="sxs-lookup"><span data-stu-id="83f34-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="83f34-153">Velg Alle i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="83f34-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="83f34-154">Vis eller skjul Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="83f34-155">Angi en dato i Følgeseddeldato-feltet.</span><span class="sxs-lookup"><span data-stu-id="83f34-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="83f34-156">Velg forsendelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="83f34-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="83f34-157">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="83f34-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="83f34-158">Click OK.</span></span>
10. <span data-ttu-id="83f34-159">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="83f34-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="83f34-160">Postere salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="83f34-160">Post sales invoice</span></span>
1. <span data-ttu-id="83f34-161">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="83f34-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="83f34-162">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="83f34-162">Click Invoice.</span></span>
3. <span data-ttu-id="83f34-163">Vis eller skjul Oversikt-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="83f34-164">Velg forsendelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="83f34-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="83f34-165">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="83f34-166">Vis eller skjul Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="83f34-167">Angi en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="83f34-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="83f34-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="83f34-168">Click OK.</span></span>
9. <span data-ttu-id="83f34-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="83f34-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="83f34-170">Status for sendt forsendelsesdokument</span><span class="sxs-lookup"><span data-stu-id="83f34-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="83f34-171">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="83f34-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="83f34-172">Klikk Remburs.</span><span class="sxs-lookup"><span data-stu-id="83f34-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="83f34-173">Vis eller skjul Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="83f34-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="83f34-174">Obs!  Feltet Dokumentet er sendt må settes til Ja.</span><span class="sxs-lookup"><span data-stu-id="83f34-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="83f34-175">Kontrollere remburseksport</span><span class="sxs-lookup"><span data-stu-id="83f34-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="83f34-176">Gå til Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="83f34-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="83f34-177">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="83f34-178">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="83f34-179">Kontroller at Eksporter remburs har forsendelsesstatusen Fakturert.</span><span class="sxs-lookup"><span data-stu-id="83f34-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="83f34-180">Kundebetaling</span><span class="sxs-lookup"><span data-stu-id="83f34-180">Customer payment</span></span>
1. <span data-ttu-id="83f34-181">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="83f34-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="83f34-182">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="83f34-182">Click New.</span></span>
3. <span data-ttu-id="83f34-183">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="83f34-184">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="83f34-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="83f34-185">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="83f34-186">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="83f34-186">Click Lines.</span></span>
7. <span data-ttu-id="83f34-187">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="83f34-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="83f34-188">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="83f34-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="83f34-189">Klikk Utligning.</span><span class="sxs-lookup"><span data-stu-id="83f34-189">Click Settlement.</span></span>
10. <span data-ttu-id="83f34-190">Merk av i boksen i hodet i Totaler.</span><span class="sxs-lookup"><span data-stu-id="83f34-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="83f34-191">Obs!  Sett Vis felt til Remburs.</span><span class="sxs-lookup"><span data-stu-id="83f34-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="83f34-192">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="83f34-193">Merk av eller fjern merket i avmerkingsboksen Merk.</span><span class="sxs-lookup"><span data-stu-id="83f34-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="83f34-194">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="83f34-194">Click OK.</span></span>
14. <span data-ttu-id="83f34-195">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="83f34-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="83f34-196">Kontrollere detaljene om bankdokumentnummer og forsendelsesnummer</span><span class="sxs-lookup"><span data-stu-id="83f34-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="83f34-197">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="83f34-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="83f34-198">Kontrollere remburseksport etter betaling</span><span class="sxs-lookup"><span data-stu-id="83f34-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="83f34-199">Gå til Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="83f34-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="83f34-200">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="83f34-201">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="83f34-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="83f34-202">Kontroller at forsendelsesstatus = betaling mottatt og saldobeløp = 0,00.</span><span class="sxs-lookup"><span data-stu-id="83f34-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]