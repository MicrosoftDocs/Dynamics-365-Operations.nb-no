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
ms.openlocfilehash: a6287fa95b7ce7341e99d1b1a6b972db68a30398
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142178"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="9dfcb-103">Definere ER-modelltilordninger og velge datakilder for dem</span><span class="sxs-lookup"><span data-stu-id="9dfcb-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dfcb-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan velge datakilder for en elektronisk rapportering (ER)-datamodell.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="9dfcb-105">Datakildene bindes til individuelle komponenter for den valgte datamodellen under utformingen og fyller ut forretningsdata til denne datamodellen under kjøring.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="9dfcb-106">I dette eksemplet velger du datakilder for en eksisterende datamodell som er opprettet for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Opprett en ny datamodell.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="9dfcb-107">Åpne konfigurasjonstreet for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="9dfcb-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="9dfcb-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9dfcb-109">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="9dfcb-110">Sette inn en ny modell-tilordning</span><span class="sxs-lookup"><span data-stu-id="9dfcb-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="9dfcb-111">Velg Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="9dfcb-112">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-112">Click Designer.</span></span>
3. <span data-ttu-id="9dfcb-113">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="9dfcb-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-114">Click New.</span></span>
    * <span data-ttu-id="9dfcb-115">Dette vil opprette en ny post som tilordner datamodellen til datakilder.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="9dfcb-116">I dette eksemplet tilordner du datamodellen til datakilder for ønsket betalingstype: kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="9dfcb-117">Det er mulig å utforme flere tilordningen for en bestemt datamodell.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="9dfcb-118">Du kan for eksempel opprette en tilordning for ulike typer betalinger, som for direkte debitering eller kredittoverføringer.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="9dfcb-119">I dette eksemplet skal du opprette en tilordning for kredittoverføringer.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="9dfcb-120">Skriv inn Beskrivelse i feltet Tilordning for kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="9dfcb-121">Tilordning for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="9dfcb-121">CT mapping</span></span>  
6. <span data-ttu-id="9dfcb-122">Skriv inn Betalingsmodell for tilordning for kredittoverføring i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="9dfcb-123">Betalingsmodell for tilordning for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="9dfcb-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="9dfcb-124">I Definisjon-feltet skriver du inn CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="9dfcb-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="9dfcb-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="9dfcb-126">ResolveChanges definisjonen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="9dfcb-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="9dfcb-128">Definer nødvendige datakilder for den gjeldende modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="9dfcb-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="9dfcb-129">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-129">Click Designer.</span></span>
2. <span data-ttu-id="9dfcb-130">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="9dfcb-131">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-131">Click Add root.</span></span>
    * <span data-ttu-id="9dfcb-132">Angi denne datakilden hvis du vil åpne betalingstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="9dfcb-133">Skriv inn Transaksjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="9dfcb-134">Transaksjoner</span><span class="sxs-lookup"><span data-stu-id="9dfcb-134">Transactions</span></span>  
5. <span data-ttu-id="9dfcb-135">Angi Transaksjoner i Etikett-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="9dfcb-136">Transaksjoner</span><span class="sxs-lookup"><span data-stu-id="9dfcb-136">Transactions</span></span>  
6. <span data-ttu-id="9dfcb-137">Angi Finansjournallinjer i Hjelp-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="9dfcb-138">Finansjournallinjer</span><span class="sxs-lookup"><span data-stu-id="9dfcb-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="9dfcb-139">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="9dfcb-140">Velg Ja.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-140">Select Yes.</span></span>  
8. <span data-ttu-id="9dfcb-141">Skriv inn 'LedgerJournalTrans' i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="9dfcb-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="9dfcb-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="9dfcb-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-143">Click OK.</span></span>
    * <span data-ttu-id="9dfcb-144">Velg tabellen LedgerJournalTrans som datakilde for gjeldende datamodell.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="9dfcb-145">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="9dfcb-146">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-146">Click Add.</span></span>
    * <span data-ttu-id="9dfcb-147">Klikk Legg til for å legge til et nytt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="9dfcb-148">I Navn-feltet skriver du inn $EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="9dfcb-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="9dfcb-149">$EndToEndID</span></span>  
13. <span data-ttu-id="9dfcb-150">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-150">Click Edit formula.</span></span>
14. <span data-ttu-id="9dfcb-151">I treet velger du Streng\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="9dfcb-152">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-152">Click Add function.</span></span>
16. <span data-ttu-id="9dfcb-153">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="9dfcb-154">I treet velger du Transaksjoner\Bilag.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="9dfcb-155">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-155">Click Add data source.</span></span>
19. <span data-ttu-id="9dfcb-156">I Formel-feltet skriver du inn 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="9dfcb-157">Skriv inn [ , "-", ] på slutten av formelen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="9dfcb-158">I treet velger du Streng\TEXT.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="9dfcb-159">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-159">Click Add function.</span></span>
22. <span data-ttu-id="9dfcb-160">Velg Transactions\Record-ID(RecId) i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="9dfcb-161">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-161">Click Add data source.</span></span>
24. <span data-ttu-id="9dfcb-162">I Formel-feltet skriver du inn CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId)).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="9dfcb-163">Skriv inn [))] på slutten av formelen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="9dfcb-164">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-164">Click Save.</span></span>
    * <span data-ttu-id="9dfcb-165">Kontroller at det ikke er oppdaget noen feil for formelen som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="9dfcb-166">Se kategorien FEIL under kontrollen for formelredigeringen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="9dfcb-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-167">Close the page.</span></span>
27. <span data-ttu-id="9dfcb-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-168">Click OK.</span></span>
    * <span data-ttu-id="9dfcb-169">Legg til det beregnede feltet i denne datakilden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="9dfcb-170">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-170">Click Add.</span></span>
    * <span data-ttu-id="9dfcb-171">Klikk Legg til for å legge til et nytt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="9dfcb-172">I Navn-feltet skriver du inn $Amount.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="9dfcb-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="9dfcb-173">$Amount</span></span>  
30. <span data-ttu-id="9dfcb-174">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-174">Click Edit formula.</span></span>
31. <span data-ttu-id="9dfcb-175">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="9dfcb-176">I treet velger du Transaksjoner\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="9dfcb-177">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-177">Click Add data source.</span></span>
34. <span data-ttu-id="9dfcb-178">I Formel-feltet skriver du inn 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="9dfcb-179">Skriv inn [ - ] ved slutten av formelen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="9dfcb-180">I treet velger du Transaksjoner\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="9dfcb-181">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-181">Click Add data source.</span></span>
37. <span data-ttu-id="9dfcb-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-182">Click Save.</span></span>
38. <span data-ttu-id="9dfcb-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-183">Close the page.</span></span>
39. <span data-ttu-id="9dfcb-184">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-184">Click OK.</span></span>
    * <span data-ttu-id="9dfcb-185">Det beregnede feltet $Amount legges til i den valgte datakilden for den gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="9dfcb-186">I treet velger du Transaksjoner\$Amount.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="9dfcb-187">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="9dfcb-188">I treet viser eller skjuler du Transaksjoner\$Amount.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="9dfcb-189">Vis eller skjul Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="9dfcb-190">Velg Dynamics 365 for Operations\Tabellposter i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="9dfcb-191">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-191">Click Add root.</span></span>
    * <span data-ttu-id="9dfcb-192">Angi denne datakilden for å vise detaljer for firmaets bankkonto.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="9dfcb-193">Skriv inn BankAccount i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="9dfcb-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="9dfcb-194">BankAccount</span></span>  
47. <span data-ttu-id="9dfcb-195">Angi BankAccount i Etikett-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="9dfcb-196">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="9dfcb-196">Bank Account</span></span>  
48. <span data-ttu-id="9dfcb-197">Angi Bankkonto i Hjelp-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="9dfcb-198">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="9dfcb-198">Bank Account</span></span>  
49. <span data-ttu-id="9dfcb-199">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="9dfcb-200">Velg Ja.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-200">Select Yes.</span></span>  
50. <span data-ttu-id="9dfcb-201">Skriv inn BankAccountTable i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="9dfcb-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="9dfcb-202">BankAccountTable</span></span>  
51. <span data-ttu-id="9dfcb-203">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-203">Click OK.</span></span>
    * <span data-ttu-id="9dfcb-204">Velg tabellen BankAccountTable som datakilde for gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="9dfcb-205">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-205">Click Add root.</span></span>
    * <span data-ttu-id="9dfcb-206">Angi denne datakilden for å vise detaljer for firmaets forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="9dfcb-207">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="9dfcb-208">Bedrift</span><span class="sxs-lookup"><span data-stu-id="9dfcb-208">Company</span></span>  
54. <span data-ttu-id="9dfcb-209">Skriv inn en verdi i feltet Etikett.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="9dfcb-210">Firmainformasjon</span><span class="sxs-lookup"><span data-stu-id="9dfcb-210">Company information</span></span>  
55. <span data-ttu-id="9dfcb-211">Angi Firmainformasjon i Hjelp-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="9dfcb-212">Firmainformasjon</span><span class="sxs-lookup"><span data-stu-id="9dfcb-212">Company information</span></span>  
56. <span data-ttu-id="9dfcb-213">Velg Ja i feltet Be om spørring.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="9dfcb-214">Velg Ja.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-214">Select Yes.</span></span>  
57. <span data-ttu-id="9dfcb-215">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="9dfcb-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="9dfcb-216">CompanyInfo</span></span>  
58. <span data-ttu-id="9dfcb-217">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-217">Click OK.</span></span>
    * <span data-ttu-id="9dfcb-218">Velg tabellen CompanyInfo som en datakilde for gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="9dfcb-219">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="9dfcb-220">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-220">Click Add root.</span></span>
    * <span data-ttu-id="9dfcb-221">Sett inn et beregnet felt som en ny datakilde.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="9dfcb-222">Skriv inn ProcessingDateTime i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="9dfcb-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="9dfcb-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="9dfcb-224">I Etikett-feltet skriver du inn Dato og klokkeslett for behandling.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="9dfcb-225">Dato og klokkeslett for behandling</span><span class="sxs-lookup"><span data-stu-id="9dfcb-225">Processing date & time</span></span>  
63. <span data-ttu-id="9dfcb-226">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-226">Click Edit formula.</span></span>
64. <span data-ttu-id="9dfcb-227">I treet velger du Dato/klokkeslett\SESSIONNOW.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="9dfcb-228">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-228">Click Add function.</span></span>
66. <span data-ttu-id="9dfcb-229">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-229">Click Save.</span></span>
67. <span data-ttu-id="9dfcb-230">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-230">Close the page.</span></span>
68. <span data-ttu-id="9dfcb-231">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-231">Click OK.</span></span>
    * <span data-ttu-id="9dfcb-232">Legg til det beregnede feltet ProcessingDateTime som en datakilde for gjeldende datamodellen.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="9dfcb-233">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-233">Click Save.</span></span>
70. <span data-ttu-id="9dfcb-234">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-234">Close the page.</span></span>
71. <span data-ttu-id="9dfcb-235">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-235">Close the page.</span></span>
72. <span data-ttu-id="9dfcb-236">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-236">Close the page.</span></span>

