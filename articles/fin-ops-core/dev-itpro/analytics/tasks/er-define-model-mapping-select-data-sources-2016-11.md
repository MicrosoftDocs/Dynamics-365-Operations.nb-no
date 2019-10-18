---
title: Definere ER-modelltilordninger og velge datakilder for dem
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan velge datakilder for en elektronisk rapporteringsdatamodell.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46dc13416aa094f33879c017c1a1815fc791409d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185112"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="8e075-103">Definere ER-modelltilordninger og velge datakilder for dem</span><span class="sxs-lookup"><span data-stu-id="8e075-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e075-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan velge datakilder for en elektronisk rapportering (ER)-datamodell.</span><span class="sxs-lookup"><span data-stu-id="8e075-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="8e075-105">Datakildene bindes til individuelle komponenter for den valgte datamodellen under utformingen og fyller ut forretningsdata til denne datamodellen under kjøring.</span><span class="sxs-lookup"><span data-stu-id="8e075-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="8e075-106">I dette eksemplet velger du datakilder for en eksisterende datamodell som er opprettet for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Opprett en ny datamodell.</span><span class="sxs-lookup"><span data-stu-id="8e075-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="8e075-107">Åpne konfigurasjonstreet for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="8e075-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="8e075-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="8e075-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8e075-109">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="8e075-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="8e075-110">Sette inn en ny modell-tilordning</span><span class="sxs-lookup"><span data-stu-id="8e075-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="8e075-111">Velg Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="8e075-112">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="8e075-112">Click Designer.</span></span>
3. <span data-ttu-id="8e075-113">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="8e075-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="8e075-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8e075-114">Click New.</span></span>
    * <span data-ttu-id="8e075-115">Dette vil opprette en ny post som tilordner datamodellen til datakilder.</span><span class="sxs-lookup"><span data-stu-id="8e075-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="8e075-116">I dette eksemplet tilordner du datamodellen til datakilder for ønsket betalingstype: kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="8e075-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="8e075-117">Det er mulig å utforme flere tilordningen for en bestemt datamodell.</span><span class="sxs-lookup"><span data-stu-id="8e075-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="8e075-118">Du kan for eksempel opprette en tilordning for ulike typer betalinger, som for direkte debitering eller kredittoverføringer.</span><span class="sxs-lookup"><span data-stu-id="8e075-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="8e075-119">I dette eksemplet skal du opprette en tilordning for kredittoverføringer.</span><span class="sxs-lookup"><span data-stu-id="8e075-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="8e075-120">Skriv inn Beskrivelse i feltet Tilordning for kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="8e075-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="8e075-121">Tilordning for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="8e075-121">CT mapping</span></span>  
6. <span data-ttu-id="8e075-122">Skriv inn Betalingsmodell for tilordning for kredittoverføring i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="8e075-123">Betalingsmodell for tilordning for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="8e075-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="8e075-124">I Definisjon-feltet skriver du inn CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="8e075-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="8e075-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="8e075-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="8e075-126">ResolveChanges definisjonen.</span><span class="sxs-lookup"><span data-stu-id="8e075-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="8e075-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8e075-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="8e075-128">Definer nødvendige datakilder for den gjeldende modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="8e075-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="8e075-129">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="8e075-129">Click Designer.</span></span>
2. <span data-ttu-id="8e075-130">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="8e075-131">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="8e075-131">Click Add root.</span></span>
    * <span data-ttu-id="8e075-132">Angi denne datakilden hvis du vil åpne betalingstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="8e075-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="8e075-133">Skriv inn Transaksjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="8e075-134">Transaksjoner</span><span class="sxs-lookup"><span data-stu-id="8e075-134">Transactions</span></span>  
5. <span data-ttu-id="8e075-135">Angi Transaksjoner i Etikett-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="8e075-136">Transaksjoner</span><span class="sxs-lookup"><span data-stu-id="8e075-136">Transactions</span></span>  
6. <span data-ttu-id="8e075-137">Angi Finansjournallinjer i Hjelp-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="8e075-138">Finansjournallinjer</span><span class="sxs-lookup"><span data-stu-id="8e075-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="8e075-139">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="8e075-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="8e075-140">Velg Ja.</span><span class="sxs-lookup"><span data-stu-id="8e075-140">Select Yes.</span></span>  
8. <span data-ttu-id="8e075-141">Skriv inn 'LedgerJournalTrans' i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="8e075-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="8e075-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="8e075-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e075-143">Click OK.</span></span>
    * <span data-ttu-id="8e075-144">Velg tabellen LedgerJournalTrans som datakilde for gjeldende datamodell.</span><span class="sxs-lookup"><span data-stu-id="8e075-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="8e075-145">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="8e075-146">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8e075-146">Click Add.</span></span>
    * <span data-ttu-id="8e075-147">Klikk Legg til for å legge til et nytt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="8e075-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="8e075-148">I Navn-feltet skriver du inn $EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="8e075-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="8e075-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="8e075-149">$EndToEndID</span></span>  
13. <span data-ttu-id="8e075-150">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="8e075-150">Click Edit formula.</span></span>
14. <span data-ttu-id="8e075-151">I treet velger du Streng\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="8e075-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="8e075-152">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="8e075-152">Click Add function.</span></span>
16. <span data-ttu-id="8e075-153">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="8e075-154">I treet velger du Transaksjoner\Bilag.</span><span class="sxs-lookup"><span data-stu-id="8e075-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="8e075-155">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="8e075-155">Click Add data source.</span></span>
19. <span data-ttu-id="8e075-156">I Formel-feltet skriver du inn 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="8e075-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="8e075-157">Skriv inn [ , “-“, ] på slutten av formelen.</span><span class="sxs-lookup"><span data-stu-id="8e075-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="8e075-158">I treet velger du Streng\TEXT.</span><span class="sxs-lookup"><span data-stu-id="8e075-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="8e075-159">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="8e075-159">Click Add function.</span></span>
22. <span data-ttu-id="8e075-160">Velg Transactions\Record-ID(RecId) i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="8e075-161">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="8e075-161">Click Add data source.</span></span>
24. <span data-ttu-id="8e075-162">I Formel-feltet skriver du inn CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId)).</span><span class="sxs-lookup"><span data-stu-id="8e075-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="8e075-163">Skriv inn [))] på slutten av formelen.</span><span class="sxs-lookup"><span data-stu-id="8e075-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="8e075-164">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8e075-164">Click Save.</span></span>
    * <span data-ttu-id="8e075-165">Kontroller at det ikke er oppdaget noen feil for formelen som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="8e075-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="8e075-166">Se kategorien FEIL under kontrollen for formelredigeringen.</span><span class="sxs-lookup"><span data-stu-id="8e075-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="8e075-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e075-167">Close the page.</span></span>
27. <span data-ttu-id="8e075-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e075-168">Click OK.</span></span>
    * <span data-ttu-id="8e075-169">Legg til det beregnede feltet i denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="8e075-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="8e075-170">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8e075-170">Click Add.</span></span>
    * <span data-ttu-id="8e075-171">Klikk Legg til for å legge til et nytt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="8e075-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="8e075-172">I Navn-feltet skriver du inn $Amount.</span><span class="sxs-lookup"><span data-stu-id="8e075-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="8e075-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="8e075-173">$Amount</span></span>  
30. <span data-ttu-id="8e075-174">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="8e075-174">Click Edit formula.</span></span>
31. <span data-ttu-id="8e075-175">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="8e075-176">I treet velger du Transaksjoner\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="8e075-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="8e075-177">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="8e075-177">Click Add data source.</span></span>
34. <span data-ttu-id="8e075-178">I Formel-feltet skriver du inn 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="8e075-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="8e075-179">Skriv inn [ - ] ved slutten av formelen.</span><span class="sxs-lookup"><span data-stu-id="8e075-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="8e075-180">I treet velger du Transaksjoner\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="8e075-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="8e075-181">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="8e075-181">Click Add data source.</span></span>
37. <span data-ttu-id="8e075-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8e075-182">Click Save.</span></span>
38. <span data-ttu-id="8e075-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e075-183">Close the page.</span></span>
39. <span data-ttu-id="8e075-184">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e075-184">Click OK.</span></span>
    * <span data-ttu-id="8e075-185">Det beregnede feltet $Amount legges til i den valgte datakilden for den gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="8e075-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="8e075-186">I treet velger du Transaksjoner\$Amount.</span><span class="sxs-lookup"><span data-stu-id="8e075-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="8e075-187">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="8e075-188">I treet viser eller skjuler du Transaksjoner\$Amount.</span><span class="sxs-lookup"><span data-stu-id="8e075-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="8e075-189">Vis eller skjul Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="8e075-190">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="8e075-191">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="8e075-191">Click Add root.</span></span>
    * <span data-ttu-id="8e075-192">Angi denne datakilden for å vise detaljer for firmaets bankkonto.</span><span class="sxs-lookup"><span data-stu-id="8e075-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="8e075-193">Skriv inn BankAccount i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="8e075-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="8e075-194">BankAccount</span></span>  
47. <span data-ttu-id="8e075-195">Angi BankAccount i Etikett-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="8e075-196">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="8e075-196">Bank Account</span></span>  
48. <span data-ttu-id="8e075-197">Angi Bankkonto i Hjelp-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="8e075-198">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="8e075-198">Bank Account</span></span>  
49. <span data-ttu-id="8e075-199">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="8e075-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="8e075-200">Velg Ja.</span><span class="sxs-lookup"><span data-stu-id="8e075-200">Select Yes.</span></span>  
50. <span data-ttu-id="8e075-201">Skriv inn BankAccountTable i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="8e075-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="8e075-202">BankAccountTable</span></span>  
51. <span data-ttu-id="8e075-203">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e075-203">Click OK.</span></span>
    * <span data-ttu-id="8e075-204">Velg tabellen BankAccountTable som datakilde for gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="8e075-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="8e075-205">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="8e075-205">Click Add root.</span></span>
    * <span data-ttu-id="8e075-206">Angi denne datakilden for å vise detaljer for firmaets forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="8e075-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="8e075-207">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="8e075-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8e075-208">Firma</span><span class="sxs-lookup"><span data-stu-id="8e075-208">Company</span></span>  
54. <span data-ttu-id="8e075-209">Skriv inn en verdi i feltet Etikett.</span><span class="sxs-lookup"><span data-stu-id="8e075-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="8e075-210">Firmainformasjon</span><span class="sxs-lookup"><span data-stu-id="8e075-210">Company information</span></span>  
55. <span data-ttu-id="8e075-211">Angi Firmainformasjon i Hjelp-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="8e075-212">Firmainformasjon</span><span class="sxs-lookup"><span data-stu-id="8e075-212">Company information</span></span>  
56. <span data-ttu-id="8e075-213">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="8e075-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="8e075-214">Velg Ja.</span><span class="sxs-lookup"><span data-stu-id="8e075-214">Select Yes.</span></span>  
57. <span data-ttu-id="8e075-215">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="8e075-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="8e075-216">CompanyInfo</span></span>  
58. <span data-ttu-id="8e075-217">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e075-217">Click OK.</span></span>
    * <span data-ttu-id="8e075-218">Velg tabellen CompanyInfo som en datakilde for gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="8e075-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="8e075-219">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="8e075-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="8e075-220">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="8e075-220">Click Add root.</span></span>
    * <span data-ttu-id="8e075-221">Sett inn et beregnet felt som en ny datakilde.</span><span class="sxs-lookup"><span data-stu-id="8e075-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="8e075-222">Skriv inn ProcessingDateTime i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e075-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="8e075-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="8e075-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="8e075-224">I Etikett-feltet skriver du inn Dato og klokkeslett for behandling.</span><span class="sxs-lookup"><span data-stu-id="8e075-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="8e075-225">Dato og klokkeslett for behandling</span><span class="sxs-lookup"><span data-stu-id="8e075-225">Processing date & time</span></span>  
63. <span data-ttu-id="8e075-226">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="8e075-226">Click Edit formula.</span></span>
64. <span data-ttu-id="8e075-227">I treet velger du Dato/klokkeslett\SESSIONNOW.</span><span class="sxs-lookup"><span data-stu-id="8e075-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="8e075-228">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="8e075-228">Click Add function.</span></span>
66. <span data-ttu-id="8e075-229">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8e075-229">Click Save.</span></span>
67. <span data-ttu-id="8e075-230">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e075-230">Close the page.</span></span>
68. <span data-ttu-id="8e075-231">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8e075-231">Click OK.</span></span>
    * <span data-ttu-id="8e075-232">Legg til det beregnede feltet ProcessingDateTime som en datakilde for gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="8e075-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="8e075-233">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8e075-233">Click Save.</span></span>
70. <span data-ttu-id="8e075-234">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e075-234">Close the page.</span></span>
71. <span data-ttu-id="8e075-235">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e075-235">Close the page.</span></span>
72. <span data-ttu-id="8e075-236">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8e075-236">Close the page.</span></span>

