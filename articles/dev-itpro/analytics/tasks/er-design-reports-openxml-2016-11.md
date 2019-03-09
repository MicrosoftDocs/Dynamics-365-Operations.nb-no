---
title: ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)
description: De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "326659"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="41dea-103">ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)</span><span class="sxs-lookup"><span data-stu-id="41dea-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41dea-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="41dea-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="41dea-105">Denne konfigurasjonen vil bli brukt til å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="41dea-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="41dea-106">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i GBSI-firmaet.</span><span class="sxs-lookup"><span data-stu-id="41dea-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="41dea-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="41dea-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="41dea-108">Du må også ha en Excel-fil som importeres når du oppretter malen.</span><span class="sxs-lookup"><span data-stu-id="41dea-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="41dea-109">Denne filen kan åpnes fra [Mal for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="41dea-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="41dea-110">Laste opp modellkonfigurasjon for betalingsdata</span><span class="sxs-lookup"><span data-stu-id="41dea-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="41dea-111">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="41dea-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="41dea-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="41dea-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="41dea-113">Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="41dea-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="41dea-114">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="41dea-114">Click Set active.</span></span>
4. <span data-ttu-id="41dea-115">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="41dea-115">Click Repositories.</span></span>
    * <span data-ttu-id="41dea-116">Velg et repositorium for operasjonsressurstypen, hvis tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="41dea-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="41dea-117">Hvis den er tilgjengelige, hopper du over følgende trinn for hvordan du oppretter et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="41dea-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="41dea-118">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="41dea-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="41dea-119">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="41dea-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="41dea-120">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="41dea-120">Click Create repository.</span></span>
8. <span data-ttu-id="41dea-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="41dea-121">Click OK.</span></span>
9. <span data-ttu-id="41dea-122">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="41dea-122">Click Open.</span></span>
10. <span data-ttu-id="41dea-123">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="41dea-124">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="41dea-124">Click Import.</span></span>
    * <span data-ttu-id="41dea-125">Importer denne datamodellen.</span><span class="sxs-lookup"><span data-stu-id="41dea-125">Import this data model.</span></span> <span data-ttu-id="41dea-126">Den vil bli brukt som datakilde i en ny formatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="41dea-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="41dea-127">Hopp over dette trinnet hvis denne konfigurasjonen allerede er importert.</span><span class="sxs-lookup"><span data-stu-id="41dea-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="41dea-128">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="41dea-128">Click Yes.</span></span>
13. <span data-ttu-id="41dea-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-129">Close the page.</span></span>
14. <span data-ttu-id="41dea-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="41dea-131">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="41dea-131">Create a new format configuration</span></span>
1. <span data-ttu-id="41dea-132">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="41dea-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="41dea-133">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="41dea-134">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="41dea-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="41dea-135">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="41dea-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="41dea-136">Opprett et format som er basert på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="41dea-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="41dea-137">Skriv inn Regnearkeksempelrapport i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="41dea-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="41dea-138">Regnearkeksempelrapport</span><span class="sxs-lookup"><span data-stu-id="41dea-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="41dea-139">Skriv inn Regnearkeksempelrapport for leverandørenes betalinger i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="41dea-140">Regnearkeksempelrapport for leverandørenes betalinger.</span><span class="sxs-lookup"><span data-stu-id="41dea-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="41dea-141">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="41dea-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="41dea-142">Velg definisjonen CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="41dea-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="41dea-143">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="41dea-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="41dea-144">Utforme et nytt dokument i OPENXML-regnearkformat</span><span class="sxs-lookup"><span data-stu-id="41dea-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="41dea-145">Velg Betalingsmodell\Regnearkeksempelrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="41dea-146">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="41dea-146">Click Designer.</span></span>
3. <span data-ttu-id="41dea-147">Klikk Import i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="41dea-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="41dea-148">Klikk Importer fra Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="41dea-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="41dea-149">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="41dea-149">Click Attachments.</span></span>
    * <span data-ttu-id="41dea-150">Knytte det eksisterende Excel-dokumentet til som en mal.</span><span class="sxs-lookup"><span data-stu-id="41dea-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="41dea-151">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="41dea-151">Click New.</span></span>
7. <span data-ttu-id="41dea-152">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="41dea-152">Click File.</span></span>
    * <span data-ttu-id="41dea-153">Velg den eksisterende Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="41dea-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="41dea-154">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-154">Close the page.</span></span>
9. <span data-ttu-id="41dea-155">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="41dea-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="41dea-156">Velg at den vedlagte Excel-filen skal brukes som en mal.</span><span class="sxs-lookup"><span data-stu-id="41dea-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="41dea-157">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="41dea-157">Click OK.</span></span>
    * <span data-ttu-id="41dea-158">Legg merke til at ER-formatkomponenter er opprettet i utformingsformatet basert på strukturen til det refererende MS Excel-dokumentet (navngitte områder).</span><span class="sxs-lookup"><span data-stu-id="41dea-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="41dea-159">Opprette en ny datakilde for å beregne totaler etter valutakoder</span><span class="sxs-lookup"><span data-stu-id="41dea-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="41dea-160">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="41dea-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="41dea-161">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="41dea-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="41dea-162">Velg Funksjoner\Grupper etter i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="41dea-163">Skriv inn PaymentByCurrency i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="41dea-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="41dea-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="41dea-165">Klikk Rediger gruppe etter.</span><span class="sxs-lookup"><span data-stu-id="41dea-165">Click Edit group by.</span></span>
6. <span data-ttu-id="41dea-166">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="41dea-167">Velg modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="41dea-168">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="41dea-168">Click Add field to.</span></span>
9. <span data-ttu-id="41dea-169">Klikk Hva skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="41dea-169">Click What to group.</span></span>
10. <span data-ttu-id="41dea-170">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="41dea-171">Velg model\Payments\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="41dea-172">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="41dea-172">Click Add field to.</span></span>
13. <span data-ttu-id="41dea-173">Klikk Grupperte felt.</span><span class="sxs-lookup"><span data-stu-id="41dea-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="41dea-174">Velg model\Payments\Instructed Amount(InstructedAmount) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="41dea-175">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="41dea-175">Click Add field to.</span></span>
16. <span data-ttu-id="41dea-176">Klikk Aggregeringsfelt.</span><span class="sxs-lookup"><span data-stu-id="41dea-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="41dea-177">Velg et alternativ i Metode-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="41dea-178">Velg mengdefunksjonen SUM.</span><span class="sxs-lookup"><span data-stu-id="41dea-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="41dea-179">Skriv inn TotalInstructuredAmount i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="41dea-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="41dea-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="41dea-181">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="41dea-181">Click Save.</span></span>
20. <span data-ttu-id="41dea-182">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-182">Close the page.</span></span>
21. <span data-ttu-id="41dea-183">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="41dea-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="41dea-184">Tilordne formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="41dea-184">Map format components to data sources</span></span>
1. <span data-ttu-id="41dea-185">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="41dea-186">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="41dea-187">Vis modell\Betalinger\Initialiseringspart(InitiatingParty) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="41dea-188">Velg model\Payments\Initiating Party(InitiatingParty)\Name i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="41dea-189">Vis Excel\ReportHeader i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="41dea-190">Velg Excel\ReportHeader\CompanyName i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="41dea-191">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-191">Click Bind.</span></span>
8. <span data-ttu-id="41dea-192">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="41dea-193">Vis modell\Betalinger\Kreditor\Identifikasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="41dea-194">Velg model\Payments\Creditor\Identification\Source ID(SourceID) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="41dea-195">Vis Excel\PaymLines i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="41dea-196">Velg Excel\PaymLines\VendAccountName i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="41dea-197">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-197">Click Bind.</span></span>
14. <span data-ttu-id="41dea-198">I treet velger du modell\Betalinger\Kreditor\Navn.</span><span class="sxs-lookup"><span data-stu-id="41dea-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="41dea-199">Velg Excel\PaymLines\VendName i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="41dea-200">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-200">Click Bind.</span></span>
17. <span data-ttu-id="41dea-201">Vis modell\Betalinger\Kreditoragent(CreditorAgent) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="41dea-202">Velg model\Payments\Creditor Agent(CreditorAgent)\Name i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="41dea-203">Velg Excel\PaymLines\Bank i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="41dea-204">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-204">Click Bind.</span></span>
21. <span data-ttu-id="41dea-205">Velg model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="41dea-206">Velg Excel\PaymLines\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="41dea-207">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-207">Click Bind.</span></span>
24. <span data-ttu-id="41dea-208">Utvid model\Payments\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="41dea-209">Utvid model\Payments\Creditor Account(CreditorAccount)\Identification i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="41dea-210">Velg model\Payments\Creditor Account(CreditorAccount)\Identification\Number i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="41dea-211">Velg Excel\PaymLines\AccountNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="41dea-212">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-212">Click Bind.</span></span>
29. <span data-ttu-id="41dea-213">Velg model\Payments\Instructed Amount(InstructedAmount) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="41dea-214">Velg Excel\PaymLines\Debit i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="41dea-215">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-215">Click Bind.</span></span>
32. <span data-ttu-id="41dea-216">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="41dea-217">Utvid model\Payments\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="41dea-218">Vis modell\Betalinger\Kreditoragent(CreditorAgent) i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="41dea-219">Velg model\Payments\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="41dea-220">Velg Excel\PaymLines\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="41dea-221">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-221">Click Bind.</span></span>
38. <span data-ttu-id="41dea-222">Vis PaymentByCurrency i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="41dea-223">Vis PaymentByCurrency\grouped i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="41dea-224">Velg PaymentByCurrency\grouped\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="41dea-225">Vis Excel\SummaryLines i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="41dea-226">Velg Excel\SummaryLines\SummaryCurrency i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="41dea-227">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-227">Click Bind.</span></span>
44. <span data-ttu-id="41dea-228">Vis PaymentByCurrency\aggregated i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="41dea-229">Velg PaymentByCurrency\aggregated\TotalInstructuredAmount i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="41dea-230">Velg Excel\SummaryLines\SummaryAmount i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="41dea-231">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-231">Click Bind.</span></span>
48. <span data-ttu-id="41dea-232">Velg PaymentByCurrency i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="41dea-233">Velg Excel\SummaryLines i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="41dea-234">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-234">Click Bind.</span></span>
51. <span data-ttu-id="41dea-235">Velg modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="41dea-236">Velg Excel\PaymLines i treet.</span><span class="sxs-lookup"><span data-stu-id="41dea-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="41dea-237">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="41dea-237">Click Bind.</span></span>
54. <span data-ttu-id="41dea-238">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="41dea-238">Click Save.</span></span>
55. <span data-ttu-id="41dea-239">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="41dea-240">Bruke den opprettede konfigurasjonen for behandling av betalinger</span><span class="sxs-lookup"><span data-stu-id="41dea-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="41dea-241">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="41dea-241">Click Change status.</span></span>
2. <span data-ttu-id="41dea-242">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="41dea-242">Click Complete.</span></span>
3. <span data-ttu-id="41dea-243">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="41dea-243">Click OK.</span></span>
4. <span data-ttu-id="41dea-244">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-244">Close the page.</span></span>
5. <span data-ttu-id="41dea-245">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-245">Close the page.</span></span>
6. <span data-ttu-id="41dea-246">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="41dea-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="41dea-247">Bruk hurtigfilteret til å filtrere på Betalingsmåte-feltet med verdien Elektronisk.</span><span class="sxs-lookup"><span data-stu-id="41dea-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="41dea-248">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="41dea-248">Electronic</span></span>  
8. <span data-ttu-id="41dea-249">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="41dea-249">Click Edit.</span></span>
9. <span data-ttu-id="41dea-250">Vis delen Filformater.</span><span class="sxs-lookup"><span data-stu-id="41dea-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="41dea-251">Velg Ja i feltet Generell elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="41dea-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="41dea-252">Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="41dea-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="41dea-253">Velg konfigurasjonen Regnearkeksempelrapport.</span><span class="sxs-lookup"><span data-stu-id="41dea-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="41dea-254">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="41dea-254">Click Save.</span></span>
13. <span data-ttu-id="41dea-255">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="41dea-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="41dea-256">Bruke den opprettede konfigurasjonen for testing av behandling av betalingsjournaler</span><span class="sxs-lookup"><span data-stu-id="41dea-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="41dea-257">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="41dea-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="41dea-258">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="41dea-258">Click New.</span></span>
    * <span data-ttu-id="41dea-259">Opprett ny betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="41dea-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="41dea-260">Skriv inn VendPay i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="41dea-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="41dea-261">VendPay</span></span>  
4. <span data-ttu-id="41dea-262">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="41dea-262">Click Lines.</span></span>
5. <span data-ttu-id="41dea-263">Angi verdiene GB_SI_000001 i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="41dea-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="41dea-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="41dea-265">Sett Debet til 1000.</span><span class="sxs-lookup"><span data-stu-id="41dea-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="41dea-266">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="41dea-266">Click New.</span></span>
8. <span data-ttu-id="41dea-267">Angi verdiene GB_SI_000005 i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="41dea-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="41dea-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="41dea-269">Sett Debet til 2000.</span><span class="sxs-lookup"><span data-stu-id="41dea-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="41dea-270">Skriv inn EUR i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="41dea-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="41dea-271">EUR</span><span class="sxs-lookup"><span data-stu-id="41dea-271">EUR</span></span>  
11. <span data-ttu-id="41dea-272">Angi verdiene GBSI OPER i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="41dea-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="41dea-273">GBSI OPER</span></span>  
12. <span data-ttu-id="41dea-274">Skriv inn Elektronisk i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="41dea-275">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="41dea-275">Electronic</span></span>  
13. <span data-ttu-id="41dea-276">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="41dea-276">Click Save.</span></span>
14. <span data-ttu-id="41dea-277">Klikk Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="41dea-277">Click Generate payments.</span></span>
15. <span data-ttu-id="41dea-278">Skriv inn Elektronisk i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="41dea-279">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="41dea-279">Electronic</span></span>  
16. <span data-ttu-id="41dea-280">Skriv inn Betalinger i Filnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="41dea-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="41dea-281">Skriv for eksempel inn Betalinger.</span><span class="sxs-lookup"><span data-stu-id="41dea-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="41dea-282">Skriv inn GBSI OPER i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="41dea-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="41dea-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="41dea-283">GBSI OPER</span></span>  
18. <span data-ttu-id="41dea-284">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="41dea-284">Click OK.</span></span>
19. <span data-ttu-id="41dea-285">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="41dea-285">Click OK.</span></span>
    * <span data-ttu-id="41dea-286">Se gjennom det opprettede regnearket, inkludert detaljer om betalingslinjer samt totalene for hver valutakode som brukes i denne betalingsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="41dea-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

