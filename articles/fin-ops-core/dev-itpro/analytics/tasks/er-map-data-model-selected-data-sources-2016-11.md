---
title: ER Tilordningen datamodell til valgte datakilder
description: Dette emnet beskriver hvordan du tilordner en ER-datamodell (Elektronisk rapportering) til valgte Microsoft Dynamics 365 Finance-datakilder.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eb7f48a50e32637003c1488d80899a704709068
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751492"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="6eebe-103">ER Tilordningen datamodell til valgte datakilder</span><span class="sxs-lookup"><span data-stu-id="6eebe-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6eebe-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne en elektronisk rapportering (ER)-datamodell til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="6eebe-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="6eebe-105">Denne modelltilordningen brukes senere som datakilde i en formatkonfigurasjon som skal brukes til å administrere elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="6eebe-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="6eebe-106">I dette eksemplet tilordner du en datamodell for eksempelfirmaet Litware, Inc. til datakilder.</span><span class="sxs-lookup"><span data-stu-id="6eebe-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="6eebe-107">Når du skal fullføre disse trinnene, må du først fullføre trinnene i fremgangsmåten "Velg datakildene for tilordning av modell".</span><span class="sxs-lookup"><span data-stu-id="6eebe-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="6eebe-108">Åpne ER-konfigurasjonstreet</span><span class="sxs-lookup"><span data-stu-id="6eebe-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="6eebe-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="6eebe-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6eebe-110">Klikk på Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="6eebe-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="6eebe-111">Velg opprettet modelltilordning</span><span class="sxs-lookup"><span data-stu-id="6eebe-111">Select created model mapping</span></span>
1. <span data-ttu-id="6eebe-112">Velg Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="6eebe-113">Kontroller at modellkonfigurasjonen "Betalinger (forenklet modell)" er opprettet på forhånd.</span><span class="sxs-lookup"><span data-stu-id="6eebe-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="6eebe-114">Ellers stopper du nå og går tilbake etter at du har fullført oppgaveveiledningen Opprette en ny konfigurasjon med datamodellen for det valgte domenet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="6eebe-115">Velg Modellutforming.</span><span class="sxs-lookup"><span data-stu-id="6eebe-115">Click Model designer.</span></span>
3. <span data-ttu-id="6eebe-116">Klikk på Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6eebe-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="6eebe-117">Velg posten Tilordning for kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="6eebe-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="6eebe-118">Tilordning for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="6eebe-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="6eebe-119">Bind opprettede datakilder til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="6eebe-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="6eebe-120">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="6eebe-120">Click Designer.</span></span>
2. <span data-ttu-id="6eebe-121">I konsolltreet velger du Dato og klokkeslett for behandling(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="6eebe-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="6eebe-122">I konsolltreet velger du Behandlingsdato(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="6eebe-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="6eebe-123">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-123">Click Bind.</span></span>
5. <span data-ttu-id="6eebe-124">Velg Betalingsmeldingsidentifikasjon(MessageIdentification) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="6eebe-125">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="6eebe-126">Velg Transaksjoner\Journalpartinummer(JournalNum) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="6eebe-127">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-127">Click Bind.</span></span>
9. <span data-ttu-id="6eebe-128">Velg Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="6eebe-129">Velg Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="6eebe-130">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-130">Click Bind.</span></span>
12. <span data-ttu-id="6eebe-131">Utvid Betalinger= Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="6eebe-132">Utvid Betalinger= Transaksjoner\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="6eebe-133">Utvid Betalinger= Transaksjoner\Kreditor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="6eebe-134">I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\Valutakode(Valuta).</span><span class="sxs-lookup"><span data-stu-id="6eebe-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="6eebe-135">I treet utvider du Transaksjoner\vendBankAccountInTransactionCompany().</span><span class="sxs-lookup"><span data-stu-id="6eebe-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="6eebe-136">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Valuta(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="6eebe-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="6eebe-137">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-137">Click Bind.</span></span>
19. <span data-ttu-id="6eebe-138">I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\IBAN-kode(IBAN).</span><span class="sxs-lookup"><span data-stu-id="6eebe-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="6eebe-139">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).</span><span class="sxs-lookup"><span data-stu-id="6eebe-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="6eebe-140">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-140">Click Bind.</span></span>
22. <span data-ttu-id="6eebe-141">I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\Nummer.</span><span class="sxs-lookup"><span data-stu-id="6eebe-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="6eebe-142">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Bankkontonummer(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="6eebe-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="6eebe-143">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-143">Click Bind.</span></span>
25. <span data-ttu-id="6eebe-144">Utvid Betalinger= Transaksjoner\Kreditor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="6eebe-145">I treet velger du Betalinger = Transaksjoner\Kreditor\Agent\Navn.</span><span class="sxs-lookup"><span data-stu-id="6eebe-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="6eebe-146">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Navn.</span><span class="sxs-lookup"><span data-stu-id="6eebe-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="6eebe-147">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-147">Click Bind.</span></span>
29. <span data-ttu-id="6eebe-148">I treet velger du Betalinger= Transaksjoner\Kreditor\Agent\Rutingsnummer(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="6eebe-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="6eebe-149">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Rutingsnummer(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="6eebe-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="6eebe-150">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-150">Click Bind.</span></span>
32. <span data-ttu-id="6eebe-151">I treet velger du Betalinger = Transaksjoner\Kreditor\Agent\SWIFT-kode(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="6eebe-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="6eebe-152">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\SWIFT-kode(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="6eebe-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="6eebe-153">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-153">Click Bind.</span></span>
35. <span data-ttu-id="6eebe-154">I treet velger du Betalinger = Transaksjoner\Kreditor\Navn.</span><span class="sxs-lookup"><span data-stu-id="6eebe-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="6eebe-155">Utvid Transaksjoner\findVendTable() i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="6eebe-156">I treet velger du Transaksjoner\findVendTable()\name().</span><span class="sxs-lookup"><span data-stu-id="6eebe-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="6eebe-157">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-157">Click Bind.</span></span>
39. <span data-ttu-id="6eebe-158">I treet velger du Betalinger = Transaksjoner\Valutakode(Valuta).</span><span class="sxs-lookup"><span data-stu-id="6eebe-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="6eebe-159">Utvid Transaksjoner\>Relasjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="6eebe-160">I treet utvider du Transaksjoner\>Relasjoner\Valutatabell(Valuta).</span><span class="sxs-lookup"><span data-stu-id="6eebe-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="6eebe-161">I treet velger du Transaksjoner\>Relasjoner\Valutatabell(Valuta)\Valutakode(CurrencyCodeISO).</span><span class="sxs-lookup"><span data-stu-id="6eebe-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="6eebe-162">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-162">Click Bind.</span></span>
44. <span data-ttu-id="6eebe-163">Utvid Betalinger= Transaksjoner\Debitor i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="6eebe-164">Utvid Betalinger= Transaksjoner\Debitor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="6eebe-165">I treet velger du Betalinger = Transaksjoner\Debitor\Konto\Valutakode(Valuta).</span><span class="sxs-lookup"><span data-stu-id="6eebe-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="6eebe-166">Velg Bankkonto(BankAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="6eebe-167">Utvid Bankkonto(BankAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="6eebe-168">I treet velger du Bankkonto(BankAccount)\Valuta(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="6eebe-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="6eebe-169">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-169">Click Bind.</span></span>
51. <span data-ttu-id="6eebe-170">I treet velger du Bankkonto(BankAccount)\IBAN.</span><span class="sxs-lookup"><span data-stu-id="6eebe-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="6eebe-171">I treet velger du Betalinger = Transaksjoner\Debitor\Konto\IBAN-kode(IBAN).</span><span class="sxs-lookup"><span data-stu-id="6eebe-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="6eebe-172">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-172">Click Bind.</span></span>
54. <span data-ttu-id="6eebe-173">I treet velger du Betalinger = Transaksjoner\Debitor\Konto\Nummer.</span><span class="sxs-lookup"><span data-stu-id="6eebe-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="6eebe-174">I treet velger du Bankkonto(BankAccount)\Bankkontonummer(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="6eebe-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="6eebe-175">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-175">Click Bind.</span></span>
57. <span data-ttu-id="6eebe-176">Utvid Betalinger= Transaksjoner\Debitor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="6eebe-177">I treet velger du Betalinger = Transaksjoner\Debitor\Agent\Navn.</span><span class="sxs-lookup"><span data-stu-id="6eebe-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="6eebe-178">Velg Bankkonto(BankAccount)\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="6eebe-179">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-179">Click Bind.</span></span>
61. <span data-ttu-id="6eebe-180">I treet velger du Betalinger= Transaksjoner\Debitor\Agent\Rutingsnummer(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="6eebe-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="6eebe-181">I treet velger du Bankkonto(BankAccount)\Rutingsnummer(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="6eebe-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="6eebe-182">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-182">Click Bind.</span></span>
64. <span data-ttu-id="6eebe-183">I treet velger du Betalinger = Transaksjoner\Debitor\Agent\SWIFT-kode(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="6eebe-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="6eebe-184">I treet velger du Bankkonto(BankAccount)\SWIFT-kode(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="6eebe-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="6eebe-185">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-185">Click Bind.</span></span>
67. <span data-ttu-id="6eebe-186">I treet velger du Betalinger = Transaksjoner\Debitor\Navn.</span><span class="sxs-lookup"><span data-stu-id="6eebe-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="6eebe-187">Velg Firmainformasjon (Firma) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="6eebe-188">Utvid Firmainformasjon (Firma) i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="6eebe-189">Velg Firmainformasjon (Firma)\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="6eebe-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="6eebe-190">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-190">Click Bind.</span></span>
72. <span data-ttu-id="6eebe-191">I treet velger du Betalinger = Transaksjoner\Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6eebe-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="6eebe-192">I treet velger du Transaksjoner\Beskrivelse(Txt).</span><span class="sxs-lookup"><span data-stu-id="6eebe-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="6eebe-193">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-193">Click Bind.</span></span>
75. <span data-ttu-id="6eebe-194">I treet velger du Betalinger = Transaksjoner\Ende-til-ende-identifikasjonskode(End2EndID).</span><span class="sxs-lookup"><span data-stu-id="6eebe-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="6eebe-195">I treet velger du Transaksjoner\$EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="6eebe-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="6eebe-196">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-196">Click Bind.</span></span>
78. <span data-ttu-id="6eebe-197">I treet velger du Betalinger = Transaksjoner\Instruert beløp(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="6eebe-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="6eebe-198">I treet velger du Transaksjoner\$Amount.</span><span class="sxs-lookup"><span data-stu-id="6eebe-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="6eebe-199">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-199">Click Bind.</span></span>
81. <span data-ttu-id="6eebe-200">I treet velger du Betalinger = Transaksjoner\Transaksjonsdato(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="6eebe-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="6eebe-201">I treet velger du Transaksjoner\Dato(TransDate).</span><span class="sxs-lookup"><span data-stu-id="6eebe-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="6eebe-202">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="6eebe-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="6eebe-203">Valider opprettet tilordning</span><span class="sxs-lookup"><span data-stu-id="6eebe-203">Validate created mapping</span></span>
1. <span data-ttu-id="6eebe-204">Klikk på Valider.</span><span class="sxs-lookup"><span data-stu-id="6eebe-204">Click Validate.</span></span>
    * <span data-ttu-id="6eebe-205">Valider den nye tilordningen for å sikre at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="6eebe-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="6eebe-206">Klikk på pilen for å vise eller skjule delen Feilliste.</span><span class="sxs-lookup"><span data-stu-id="6eebe-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="6eebe-207">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="6eebe-207">Click Save.</span></span>
4. <span data-ttu-id="6eebe-208">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6eebe-208">Close the page.</span></span>
5. <span data-ttu-id="6eebe-209">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6eebe-209">Close the page.</span></span>
6. <span data-ttu-id="6eebe-210">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6eebe-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="6eebe-211">Endre statusen til gjeldende versjon av modellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="6eebe-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="6eebe-212">Klikk på Endre status.</span><span class="sxs-lookup"><span data-stu-id="6eebe-212">Click Change status.</span></span>
    * <span data-ttu-id="6eebe-213">Endre statusen for utformet modellkonfigurasjon – fra Utkast til Fullført for å gjøre den tilgjengelig for utforming av betalingsformat.</span><span class="sxs-lookup"><span data-stu-id="6eebe-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="6eebe-214">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="6eebe-214">Click Complete.</span></span>
    * <span data-ttu-id="6eebe-215">Velg Fullført.</span><span class="sxs-lookup"><span data-stu-id="6eebe-215">Select Complete.</span></span>  
3. <span data-ttu-id="6eebe-216">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6eebe-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6eebe-217">For eksempel versjon 1.</span><span class="sxs-lookup"><span data-stu-id="6eebe-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="6eebe-218">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6eebe-218">Click OK.</span></span>
5. <span data-ttu-id="6eebe-219">Velg den fullførte versjonen av den gjeldende konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6eebe-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="6eebe-220">Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.</span><span class="sxs-lookup"><span data-stu-id="6eebe-220">Note that the created configuration is saved as completed version 1.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]