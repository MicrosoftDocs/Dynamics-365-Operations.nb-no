---
title: Importere remburs
description: Denne prosedyren hjelper deg med å importere en remburs.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1768494182a79d7a33044498c1e768e61d937d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "313572"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="2f178-103">Importere remburs</span><span class="sxs-lookup"><span data-stu-id="2f178-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f178-104">Denne prosedyren hjelper deg med å importere en remburs.</span><span class="sxs-lookup"><span data-stu-id="2f178-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="2f178-105">Følgende må defineres før du fullfører denne prosedyren: bankfasiliteter, posteringsprofiler, en bankfasilitetsavtale og leverandørbankdetaljer.</span><span class="sxs-lookup"><span data-stu-id="2f178-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="2f178-106">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="2f178-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="2f178-107">Opprette en bestilling med remburs</span><span class="sxs-lookup"><span data-stu-id="2f178-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="2f178-108">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="2f178-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="2f178-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2f178-109">Click New.</span></span>
3. <span data-ttu-id="2f178-110">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="2f178-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2f178-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2f178-113">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="2f178-113">Expand the General section.</span></span>
7. <span data-ttu-id="2f178-114">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="2f178-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2f178-116">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="2f178-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="2f178-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2f178-118">Angi en dato i feltet Regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="2f178-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="2f178-119">Angi en dato i Leveringsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="2f178-120">Obs!  Feltet Bankdokumenttype må velges med verdien Remburs.</span><span class="sxs-lookup"><span data-stu-id="2f178-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="2f178-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2f178-121">Click OK.</span></span>
14. <span data-ttu-id="2f178-122">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="2f178-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="2f178-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2f178-125">Vis delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="2f178-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="2f178-126">Velg kategorien Levering.</span><span class="sxs-lookup"><span data-stu-id="2f178-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="2f178-127">Angi en dato i Leveringsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="2f178-128">Angi en dato i Bekreftet leveringsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="2f178-129">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="2f178-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2f178-130">Definer rembursdetaljene.</span><span class="sxs-lookup"><span data-stu-id="2f178-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="2f178-131">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="2f178-132">Klikk Remburs/importinkasso.</span><span class="sxs-lookup"><span data-stu-id="2f178-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="2f178-133">Angi dato og klokkeslett i Søknadsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="2f178-134">Kontroller at Bankkonto-feltet har en standard aktiv bankkonto, som er basert på programdatoen.</span><span class="sxs-lookup"><span data-stu-id="2f178-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="2f178-135">Angi en verdi i feltet Bankdokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="2f178-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="2f178-136">Angi dato og klokkeslett i Mottaksdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="2f178-137">Vis delen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="2f178-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="2f178-138">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="2f178-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="2f178-139">Vis delen Bankdetaljer.</span><span class="sxs-lookup"><span data-stu-id="2f178-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="2f178-140">Angi eller velg en verdi i Advisbank-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="2f178-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="2f178-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2f178-142">Click Save.</span></span>
33. <span data-ttu-id="2f178-143">Klikk Hent bestillingsforsendelser.</span><span class="sxs-lookup"><span data-stu-id="2f178-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="2f178-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-144">Close the page.</span></span>
35. <span data-ttu-id="2f178-145">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="2f178-146">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="2f178-146">Click Confirm.</span></span>
37. <span data-ttu-id="2f178-147">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="2f178-148">Klikk Remburs/importinkasso.</span><span class="sxs-lookup"><span data-stu-id="2f178-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="2f178-149">Velg Behandle.</span><span class="sxs-lookup"><span data-stu-id="2f178-149">Click Process.</span></span>
40. <span data-ttu-id="2f178-150">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="2f178-150">Click Confirm.</span></span>
    * <span data-ttu-id="2f178-151">Kontroller at fasilitetssaldoen reduserer bestillingsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="2f178-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="2f178-152">I dette eksemplet: innkjøpsbeløp = 500,00, fasilitetsgrense = 10000,00, derfor fasilitetssaldo = 9500,00.</span><span class="sxs-lookup"><span data-stu-id="2f178-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="2f178-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-153">Close the page.</span></span>
42. <span data-ttu-id="2f178-154">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="2f178-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="2f178-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2f178-155">Click Save.</span></span>
44. <span data-ttu-id="2f178-156">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="2f178-157">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="2f178-157">Click Confirm.</span></span>
    * <span data-ttu-id="2f178-158">Endre rembursen på grunn av endringen i enhetspris.</span><span class="sxs-lookup"><span data-stu-id="2f178-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="2f178-159">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="2f178-160">Klikk Remburs/importinkasso.</span><span class="sxs-lookup"><span data-stu-id="2f178-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="2f178-161">Endre rembursen på grunn av endringen i innkjøpsenhetspris.</span><span class="sxs-lookup"><span data-stu-id="2f178-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="2f178-162">Velg Behandle.</span><span class="sxs-lookup"><span data-stu-id="2f178-162">Click Process.</span></span>
49. <span data-ttu-id="2f178-163">Klikk Endre.</span><span class="sxs-lookup"><span data-stu-id="2f178-163">Click Amend.</span></span>
50. <span data-ttu-id="2f178-164">Klikk Fjern.</span><span class="sxs-lookup"><span data-stu-id="2f178-164">Click Remove.</span></span>
51. <span data-ttu-id="2f178-165">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="2f178-165">Click Yes.</span></span>
52. <span data-ttu-id="2f178-166">Klikk Hent bestillingsforsendelser.</span><span class="sxs-lookup"><span data-stu-id="2f178-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="2f178-167">Velg Behandle.</span><span class="sxs-lookup"><span data-stu-id="2f178-167">Click Process.</span></span>
54. <span data-ttu-id="2f178-168">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="2f178-168">Click Confirm.</span></span>
    * <span data-ttu-id="2f178-169">Kontroller at fasilitetssaldoen reduserer bestillingsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="2f178-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="2f178-170">I dette eksemplet: redigert innkjøpsbeløp = 600,00, fasilitetsgrense = 10000,00, derfor fasilitetssaldo = 9400,00.</span><span class="sxs-lookup"><span data-stu-id="2f178-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="2f178-171">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="2f178-172">Postere følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2f178-172">Post Packing slip</span></span>
1. <span data-ttu-id="2f178-173">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="2f178-174">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="2f178-174">Click Product receipt.</span></span>
3. <span data-ttu-id="2f178-175">Skriv inn en verdi i feltet PurchParmTable_Num.</span><span class="sxs-lookup"><span data-stu-id="2f178-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="2f178-176">Velg forsendelsesnummeret som ble opprettet med referanse til rembursen.</span><span class="sxs-lookup"><span data-stu-id="2f178-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="2f178-177">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2f178-178">Angi en dato i feltet Produktkvitteringsdato.</span><span class="sxs-lookup"><span data-stu-id="2f178-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="2f178-179">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2f178-179">Click OK.</span></span>
7. <span data-ttu-id="2f178-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-180">Close the page.</span></span>
8. <span data-ttu-id="2f178-181">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="2f178-182">Kontrollere statusen for rembursimporten</span><span class="sxs-lookup"><span data-stu-id="2f178-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="2f178-183">Gå til Kontant- og bankbehandling > Purringer > Importer remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="2f178-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="2f178-184">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2f178-185">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2f178-186">Kontroller statusen for rembursimporten.</span><span class="sxs-lookup"><span data-stu-id="2f178-186">Verify the Import letter of credit status.</span></span>    
    *   
4. <span data-ttu-id="2f178-187">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-187">Close the page.</span></span>
5. <span data-ttu-id="2f178-188">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="2f178-189">Postere innkjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="2f178-189">Post purchase invoice</span></span>
1. <span data-ttu-id="2f178-190">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="2f178-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="2f178-191">Velg bestillingen som ble opprettet med rembursen.</span><span class="sxs-lookup"><span data-stu-id="2f178-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="2f178-192">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2f178-193">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2f178-194">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2f178-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="2f178-195">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="2f178-195">Click Invoice.</span></span>
6. <span data-ttu-id="2f178-196">Skriv inn en verdi i Nummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="2f178-197">Angi eller velg en verdi i feltet Forsendelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="2f178-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="2f178-198">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2f178-199">Angi en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="2f178-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="2f178-200">Klikk Oppdater samsvarsstatus.</span><span class="sxs-lookup"><span data-stu-id="2f178-200">Click Update match status.</span></span>
11. <span data-ttu-id="2f178-201">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="2f178-201">Click Post.</span></span>
12. <span data-ttu-id="2f178-202">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-202">Close the page.</span></span>
13. <span data-ttu-id="2f178-203">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="2f178-204">Kontrollere statusen for rembursimporten</span><span class="sxs-lookup"><span data-stu-id="2f178-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="2f178-205">Gå til Kontant- og bankbehandling > Purringer > Importer remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="2f178-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="2f178-206">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2f178-207">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2f178-208">Kontroller rembursimporten.</span><span class="sxs-lookup"><span data-stu-id="2f178-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="2f178-209">Valider: Forsendelsesstatus = fakturerte bankfasilitetsdetaljer</span><span class="sxs-lookup"><span data-stu-id="2f178-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="2f178-210">Klikk Vis.</span><span class="sxs-lookup"><span data-stu-id="2f178-210">Click View.</span></span>
5. <span data-ttu-id="2f178-211">Klikk Skriv ut søknad.</span><span class="sxs-lookup"><span data-stu-id="2f178-211">Click Print application.</span></span>
6. <span data-ttu-id="2f178-212">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2f178-212">Click OK.</span></span>
    * <span data-ttu-id="2f178-213">Kontroller at remburssøknaden blir skrevet ut.</span><span class="sxs-lookup"><span data-stu-id="2f178-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="2f178-214">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-214">Close the page.</span></span>
8. <span data-ttu-id="2f178-215">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-215">Close the page.</span></span>
9. <span data-ttu-id="2f178-216">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="2f178-217">Postere leverandørbetalingsjournalen for den opprettede innkjøpsfakturaen med remburs</span><span class="sxs-lookup"><span data-stu-id="2f178-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="2f178-218">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="2f178-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2f178-219">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2f178-219">Click New.</span></span>
3. <span data-ttu-id="2f178-220">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2f178-221">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2f178-222">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="2f178-222">Click Lines.</span></span>
6. <span data-ttu-id="2f178-223">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="2f178-224">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="2f178-225">Klikk Utlign transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="2f178-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="2f178-226">Vis delen Totaler.</span><span class="sxs-lookup"><span data-stu-id="2f178-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="2f178-227">Velg et alternativ i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="2f178-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="2f178-228">Kontroller at feltet Bankdokumentnummer og Forsendelsesnummer er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="2f178-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="2f178-229">Merk av for Merk.</span><span class="sxs-lookup"><span data-stu-id="2f178-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="2f178-230">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2f178-230">Click OK.</span></span>
13. <span data-ttu-id="2f178-231">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="2f178-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="2f178-232">Kontroller at feltet Bankdokumentnummer og Forsendelsesnummer er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="2f178-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="2f178-233">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="2f178-233">Click Post.</span></span>
15. <span data-ttu-id="2f178-234">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-234">Close the page.</span></span>
16. <span data-ttu-id="2f178-235">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="2f178-236">Kontrollere statusen for rembursimporten etter fakturaen er betalt</span><span class="sxs-lookup"><span data-stu-id="2f178-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="2f178-237">Gå til Kontant- og bankbehandling > Purringer > Importer remburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="2f178-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="2f178-238">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2f178-239">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2f178-240">Kontroller statusen for rembursimporten.</span><span class="sxs-lookup"><span data-stu-id="2f178-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="2f178-241">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="2f178-242">Kontrollere bankfasilitetsgrensen og utnyttelsesrapporten</span><span class="sxs-lookup"><span data-stu-id="2f178-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="2f178-243">Gå til Kontant- og bankbehandling > Forespørsler og rapporter > Purringer eller garanti > Rapport om bankfasiliteter og bruk.</span><span class="sxs-lookup"><span data-stu-id="2f178-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="2f178-244">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="2f178-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="2f178-245">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="2f178-245">Click Filter.</span></span>
    * <span data-ttu-id="2f178-246">Definer Kriterier-feltet med den påkrevde bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="2f178-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="2f178-247">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="2f178-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="2f178-248">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2f178-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2f178-249">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2f178-249">Click OK.</span></span>
7. <span data-ttu-id="2f178-250">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2f178-250">Click OK.</span></span>
    * <span data-ttu-id="2f178-251">Kontroller rapporten som viser transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="2f178-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="2f178-252">Kontroller at rapporten angir transaksjonene med bankdokumentnummer, fasilitetsgrense, brukt beløp og fasilitetssaldobeløp.</span><span class="sxs-lookup"><span data-stu-id="2f178-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="2f178-253">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2f178-253">Close the page.</span></span>

