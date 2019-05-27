---
title: ER Tilordningen datamodell til valgte datakilder
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne en elektronisk rapportering (ER)-datamodell til valgte Dynamics 365 for Finance and Operations, Enterprise Edition-datakilder.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551236"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="ffd9f-103">ER Tilordningen datamodell til valgte datakilder</span><span class="sxs-lookup"><span data-stu-id="ffd9f-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffd9f-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne en elektronisk rapportering (ER)-datamodell til valgte Dynamics 365 for Finance and Operations, Enterprise Edition-datakilder.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="ffd9f-105">Denne modelltilordningen brukes senere som datakilde i en formatkonfigurasjon som skal brukes til å administrere elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="ffd9f-106">I dette eksemplet tilordner du en datamodell for eksempelfirmaet Litware, Inc. til datakilder.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="ffd9f-107">Når du skal fullføre disse trinnene, må du først fullføre trinnene i fremgangsmåten Velg datakildene for tilordning av modell.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="ffd9f-108">Åpne ER-konfigurasjonstreet</span><span class="sxs-lookup"><span data-stu-id="ffd9f-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="ffd9f-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ffd9f-110">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="ffd9f-111">Velg opprettet modelltilordning</span><span class="sxs-lookup"><span data-stu-id="ffd9f-111">Select created model mapping</span></span>
1. <span data-ttu-id="ffd9f-112">Velg Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="ffd9f-113">Kontroller at modellkonfigurasjonen Betalinger (forenklet modell) er opprettet på forhånd.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="ffd9f-114">Ellers stopper du nå og går tilbake etter at du har fullført oppgaveveiledningen Opprette en ny konfigurasjon med datamodellen for det valgte domenet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="ffd9f-115">Velg Modellutforming.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-115">Click Model designer.</span></span>
3. <span data-ttu-id="ffd9f-116">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="ffd9f-117">Velg posten Tilordning for kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="ffd9f-118">Tilordning for kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="ffd9f-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="ffd9f-119">Bind opprettede datakilder til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="ffd9f-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="ffd9f-120">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-120">Click Designer.</span></span>
2. <span data-ttu-id="ffd9f-121">I konsolltreet velger du Dato og klokkeslett for behandling(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="ffd9f-122">I konsolltreet velger du Behandlingsdato(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="ffd9f-123">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-123">Click Bind.</span></span>
5. <span data-ttu-id="ffd9f-124">Velg Betalingsmeldingsidentifikasjon(MessageIdentification) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="ffd9f-125">Utvid Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="ffd9f-126">Velg Transaksjoner\Journalpartinummer(JournalNum) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="ffd9f-127">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-127">Click Bind.</span></span>
9. <span data-ttu-id="ffd9f-128">Velg Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="ffd9f-129">Velg Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="ffd9f-130">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-130">Click Bind.</span></span>
12. <span data-ttu-id="ffd9f-131">Utvid Betalinger= Transaksjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="ffd9f-132">Utvid Betalinger= Transaksjoner\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="ffd9f-133">Utvid Betalinger= Transaksjoner\Kreditor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="ffd9f-134">I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\Valutakode(Valuta).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="ffd9f-135">I treet utvider du Transaksjoner\vendBankAccountInTransactionCompany().</span><span class="sxs-lookup"><span data-stu-id="ffd9f-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="ffd9f-136">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Valuta(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="ffd9f-137">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-137">Click Bind.</span></span>
19. <span data-ttu-id="ffd9f-138">I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\IBAN-kode(IBAN).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="ffd9f-139">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="ffd9f-140">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-140">Click Bind.</span></span>
22. <span data-ttu-id="ffd9f-141">I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\Nummer.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="ffd9f-142">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Bankkontonummer(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="ffd9f-143">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-143">Click Bind.</span></span>
25. <span data-ttu-id="ffd9f-144">Utvid Betalinger= Transaksjoner\Kreditor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="ffd9f-145">I treet velger du Betalinger = Transaksjoner\Kreditor\Agent\Navn.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="ffd9f-146">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Navn.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="ffd9f-147">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-147">Click Bind.</span></span>
29. <span data-ttu-id="ffd9f-148">I treet velger du Betalinger= Transaksjoner\Kreditor\Agent\Rutingsnummer(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="ffd9f-149">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Rutingsnummer(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="ffd9f-150">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-150">Click Bind.</span></span>
32. <span data-ttu-id="ffd9f-151">I treet velger du Betalinger = Transaksjoner\Kreditor\Agent\SWIFT-kode(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="ffd9f-152">I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\SWIFT-kode(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="ffd9f-153">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-153">Click Bind.</span></span>
35. <span data-ttu-id="ffd9f-154">I treet velger du Betalinger = Transaksjoner\Kreditor\Navn.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="ffd9f-155">Utvid Transaksjoner\findVendTable() i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="ffd9f-156">I treet velger du Transaksjoner\findVendTable()\name().</span><span class="sxs-lookup"><span data-stu-id="ffd9f-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="ffd9f-157">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-157">Click Bind.</span></span>
39. <span data-ttu-id="ffd9f-158">I treet velger du Betalinger = Transaksjoner\Valutakode(Valuta).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="ffd9f-159">Utvid Transaksjoner\>Relasjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="ffd9f-160">I treet utvider du Transaksjoner\>Relasjoner\Valutatabell(Valuta).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="ffd9f-161">I treet velger du Transaksjoner\>Relasjoner\Valutatabell(Valuta)\Valutakode(CurrencyCodeISO).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="ffd9f-162">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-162">Click Bind.</span></span>
44. <span data-ttu-id="ffd9f-163">Utvid Betalinger= Transaksjoner\Debitor i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="ffd9f-164">Utvid Betalinger= Transaksjoner\Debitor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="ffd9f-165">I treet velger du Betalinger = Transaksjoner\Debitor\Konto\Valutakode(Valuta).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="ffd9f-166">Velg Bankkonto(BankAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="ffd9f-167">Utvid Bankkonto(BankAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="ffd9f-168">I treet velger du Bankkonto(BankAccount)\Valuta(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="ffd9f-169">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-169">Click Bind.</span></span>
51. <span data-ttu-id="ffd9f-170">I treet velger du Bankkonto(BankAccount)\IBAN.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="ffd9f-171">I treet velger du Betalinger = Transaksjoner\Debitor\Konto\IBAN-kode(IBAN).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="ffd9f-172">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-172">Click Bind.</span></span>
54. <span data-ttu-id="ffd9f-173">I treet velger du Betalinger = Transaksjoner\Debitor\Konto\Nummer.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="ffd9f-174">I treet velger du Bankkonto(BankAccount)\Bankkontonummer(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="ffd9f-175">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-175">Click Bind.</span></span>
57. <span data-ttu-id="ffd9f-176">Utvid Betalinger= Transaksjoner\Debitor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="ffd9f-177">I treet velger du Betalinger = Transaksjoner\Debitor\Agent\Navn.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="ffd9f-178">Velg Bankkonto(BankAccount)\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="ffd9f-179">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-179">Click Bind.</span></span>
61. <span data-ttu-id="ffd9f-180">I treet velger du Betalinger= Transaksjoner\Debitor\Agent\Rutingsnummer(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="ffd9f-181">I treet velger du Bankkonto(BankAccount)\Rutingsnummer(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="ffd9f-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-182">Click Bind.</span></span>
64. <span data-ttu-id="ffd9f-183">I treet velger du Betalinger = Transaksjoner\Debitor\Agent\SWIFT-kode(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="ffd9f-184">I treet velger du Bankkonto(BankAccount)\SWIFT-kode(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="ffd9f-185">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-185">Click Bind.</span></span>
67. <span data-ttu-id="ffd9f-186">I treet velger du Betalinger = Transaksjoner\Debitor\Navn.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="ffd9f-187">Velg Firmainformasjon (Firma) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="ffd9f-188">Utvid Firmainformasjon (Firma) i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="ffd9f-189">Velg Firmainformasjon (Firma)\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="ffd9f-190">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-190">Click Bind.</span></span>
72. <span data-ttu-id="ffd9f-191">I treet velger du Betalinger = Transaksjoner\Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="ffd9f-192">I treet velger du Transaksjoner\Beskrivelse(Txt).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="ffd9f-193">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-193">Click Bind.</span></span>
75. <span data-ttu-id="ffd9f-194">I treet velger du Betalinger = Transaksjoner\Ende-til-ende-identifikasjonskode(End2EndID).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="ffd9f-195">I treet velger du Transaksjoner\$EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="ffd9f-196">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-196">Click Bind.</span></span>
78. <span data-ttu-id="ffd9f-197">I treet velger du Betalinger = Transaksjoner\Instruert beløp(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="ffd9f-198">I treet velger du Transaksjoner\$Amount.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="ffd9f-199">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-199">Click Bind.</span></span>
81. <span data-ttu-id="ffd9f-200">I treet velger du Betalinger = Transaksjoner\Transaksjonsdato(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="ffd9f-201">I treet velger du Transaksjoner\Dato(TransDate).</span><span class="sxs-lookup"><span data-stu-id="ffd9f-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="ffd9f-202">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="ffd9f-203">Valider opprettet tilordning</span><span class="sxs-lookup"><span data-stu-id="ffd9f-203">Validate created mapping</span></span>
1. <span data-ttu-id="ffd9f-204">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-204">Click Validate.</span></span>
    * <span data-ttu-id="ffd9f-205">Valider den nye tilordningen for å sikre at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="ffd9f-206">Klikk pilen for å vise eller skjule delen Feilliste.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="ffd9f-207">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-207">Click Save.</span></span>
4. <span data-ttu-id="ffd9f-208">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-208">Close the page.</span></span>
5. <span data-ttu-id="ffd9f-209">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-209">Close the page.</span></span>
6. <span data-ttu-id="ffd9f-210">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="ffd9f-211">Endre statusen til gjeldende versjon av modellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="ffd9f-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="ffd9f-212">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-212">Click Change status.</span></span>
    * <span data-ttu-id="ffd9f-213">Endre statusen for utformet modellkonfigurasjon – fra Utkast til Fullført for å gjøre den tilgjengelig for utforming av betalingsformat.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="ffd9f-214">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-214">Click Complete.</span></span>
    * <span data-ttu-id="ffd9f-215">Velg Fullført.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-215">Select Complete.</span></span>  
3. <span data-ttu-id="ffd9f-216">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ffd9f-217">For eksempel versjon 1.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="ffd9f-218">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-218">Click OK.</span></span>
5. <span data-ttu-id="ffd9f-219">Velg den fullførte versjonen av den gjeldende konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="ffd9f-220">Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.</span><span class="sxs-lookup"><span data-stu-id="ffd9f-220">Note that the created configuration is saved as completed version 1.</span></span>  

