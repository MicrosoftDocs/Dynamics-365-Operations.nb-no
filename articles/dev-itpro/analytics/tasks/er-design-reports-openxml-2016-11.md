--- 
title: "Utforme en konfigurasjon for å generere rapporter i OpenXML-format for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: nb-no
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="98084-103">Utforme en konfigurasjon for å generere rapporter i OpenXML-format for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="98084-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98084-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="98084-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="98084-105">Denne konfigurasjonen vil bli brukt til å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="98084-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="98084-106">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i GBSI-firmaet.</span><span class="sxs-lookup"><span data-stu-id="98084-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="98084-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="98084-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="98084-108">Du må også laste ned og lagre Microsoft Excel-filen [Mal for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="98084-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="98084-109">Laste opp modellkonfigurasjon for betalingsdata</span><span class="sxs-lookup"><span data-stu-id="98084-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="98084-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="98084-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="98084-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="98084-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="98084-112">Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="98084-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="98084-113">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="98084-113">Click Set active.</span></span>
4. <span data-ttu-id="98084-114">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="98084-114">Click Repositories.</span></span>
    * <span data-ttu-id="98084-115">Velg et repositorium for operasjonsressurstypen, hvis tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="98084-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="98084-116">Hvis den er tilgjengelige, hopper du over følgende trinn for hvordan du oppretter et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="98084-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="98084-117">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="98084-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="98084-118">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="98084-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="98084-119">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="98084-119">Click Create repository.</span></span>
8. <span data-ttu-id="98084-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98084-120">Click OK.</span></span>
9. <span data-ttu-id="98084-121">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="98084-121">Click Open.</span></span>
10. <span data-ttu-id="98084-122">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="98084-123">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="98084-123">Click Import.</span></span>
    * <span data-ttu-id="98084-124">Importer denne datamodellen.</span><span class="sxs-lookup"><span data-stu-id="98084-124">Import this data model.</span></span> <span data-ttu-id="98084-125">Den vil bli brukt som datakilde i en ny formatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="98084-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="98084-126">Hopp over dette trinnet hvis denne konfigurasjonen allerede er importert.</span><span class="sxs-lookup"><span data-stu-id="98084-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="98084-127">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="98084-127">Click Yes.</span></span>
13. <span data-ttu-id="98084-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-128">Close the page.</span></span>
14. <span data-ttu-id="98084-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="98084-130">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="98084-130">Create a new format configuration</span></span>
1. <span data-ttu-id="98084-131">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="98084-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="98084-132">Velg Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="98084-133">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="98084-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="98084-134">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="98084-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="98084-135">Opprett et format som er basert på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="98084-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="98084-136">Skriv inn Regnearkeksempelrapport i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="98084-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="98084-137">Regnearkeksempelrapport</span><span class="sxs-lookup"><span data-stu-id="98084-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="98084-138">Skriv inn Regnearkeksempelrapport for leverandørenes betalinger i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="98084-139">Regnearkeksempelrapport for leverandørenes betalinger.</span><span class="sxs-lookup"><span data-stu-id="98084-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="98084-140">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="98084-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="98084-141">Velg definisjonen CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="98084-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="98084-142">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="98084-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="98084-143">Utforme et nytt dokument i OPENXML-regnearkformat</span><span class="sxs-lookup"><span data-stu-id="98084-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="98084-144">Velg Betalingsmodell\Regnearkeksempelrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="98084-145">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="98084-145">Click Designer.</span></span>
3. <span data-ttu-id="98084-146">Klikk Import i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="98084-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="98084-147">Klikk Importer fra Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="98084-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="98084-148">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="98084-148">Click Attachments.</span></span>
    * <span data-ttu-id="98084-149">Knytte det eksisterende Excel-dokumentet til som en mal.</span><span class="sxs-lookup"><span data-stu-id="98084-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="98084-150">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="98084-150">Click New.</span></span>
7. <span data-ttu-id="98084-151">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="98084-151">Click File.</span></span>
    * <span data-ttu-id="98084-152">Velg den eksisterende Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="98084-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="98084-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-153">Close the page.</span></span>
9. <span data-ttu-id="98084-154">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="98084-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="98084-155">Velg at den vedlagte Excel-filen skal brukes som en mal.</span><span class="sxs-lookup"><span data-stu-id="98084-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="98084-156">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98084-156">Click OK.</span></span>
    * <span data-ttu-id="98084-157">Legg merke til at ER-formatkomponenter er opprettet i utformingsformatet basert på strukturen til det refererende MS Excel-dokumentet (navngitte områder).</span><span class="sxs-lookup"><span data-stu-id="98084-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="98084-158">Opprette en ny datakilde for å beregne totaler etter valutakoder</span><span class="sxs-lookup"><span data-stu-id="98084-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="98084-159">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="98084-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="98084-160">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="98084-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="98084-161">Velg Funksjoner\Grupper etter i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="98084-162">Skriv inn PaymentByCurrency i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="98084-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="98084-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="98084-164">Klikk Rediger gruppe etter.</span><span class="sxs-lookup"><span data-stu-id="98084-164">Click Edit group by.</span></span>
6. <span data-ttu-id="98084-165">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="98084-166">Velg modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="98084-167">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="98084-167">Click Add field to.</span></span>
9. <span data-ttu-id="98084-168">Klikk Hva skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="98084-168">Click What to group.</span></span>
10. <span data-ttu-id="98084-169">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="98084-170">Velg model\Payments\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="98084-171">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="98084-171">Click Add field to.</span></span>
13. <span data-ttu-id="98084-172">Klikk Grupperte felt.</span><span class="sxs-lookup"><span data-stu-id="98084-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="98084-173">Velg model\Payments\Instructed Amount(InstructedAmount) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="98084-174">Klikk Legg til felt i.</span><span class="sxs-lookup"><span data-stu-id="98084-174">Click Add field to.</span></span>
16. <span data-ttu-id="98084-175">Klikk Aggregeringsfelt.</span><span class="sxs-lookup"><span data-stu-id="98084-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="98084-176">Velg et alternativ i Metode-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="98084-177">Velg mengdefunksjonen SUM.</span><span class="sxs-lookup"><span data-stu-id="98084-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="98084-178">Skriv inn TotalInstructuredAmount i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="98084-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="98084-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="98084-180">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="98084-180">Click Save.</span></span>
20. <span data-ttu-id="98084-181">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-181">Close the page.</span></span>
21. <span data-ttu-id="98084-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98084-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="98084-183">Tilordne formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="98084-183">Map format components to data sources</span></span>
1. <span data-ttu-id="98084-184">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="98084-185">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="98084-186">Vis modell\Betalinger\Initialiseringspart(InitiatingParty) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="98084-187">Velg model\Payments\Initiating Party(InitiatingParty)\Name i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="98084-188">Vis Excel\ReportHeader i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="98084-189">Velg Excel\ReportHeader\CompanyName i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="98084-190">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-190">Click Bind.</span></span>
8. <span data-ttu-id="98084-191">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="98084-192">Vis modell\Betalinger\Kreditor\Identifikasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="98084-193">Velg model\Payments\Creditor\Identification\Source ID(SourceID) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="98084-194">Vis Excel\PaymLines i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="98084-195">Velg Excel\PaymLines\VendAccountName i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="98084-196">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-196">Click Bind.</span></span>
14. <span data-ttu-id="98084-197">I treet velger du modell\Betalinger\Kreditor\Navn.</span><span class="sxs-lookup"><span data-stu-id="98084-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="98084-198">Velg Excel\PaymLines\VendName i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="98084-199">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-199">Click Bind.</span></span>
17. <span data-ttu-id="98084-200">Vis modell\Betalinger\Kreditoragent(CreditorAgent) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="98084-201">Velg model\Payments\Creditor Agent(CreditorAgent)\Name i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="98084-202">Velg Excel\PaymLines\Bank i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="98084-203">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-203">Click Bind.</span></span>
21. <span data-ttu-id="98084-204">Velg model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="98084-205">Velg Excel\PaymLines\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="98084-206">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-206">Click Bind.</span></span>
24. <span data-ttu-id="98084-207">Utvid model\Payments\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="98084-208">Utvid model\Payments\Creditor Account(CreditorAccount)\Identification i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="98084-209">Velg model\Payments\Creditor Account(CreditorAccount)\Identification\Number i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="98084-210">Velg Excel\PaymLines\AccountNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="98084-211">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-211">Click Bind.</span></span>
29. <span data-ttu-id="98084-212">Velg model\Payments\Instructed Amount(InstructedAmount) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="98084-213">Velg Excel\PaymLines\Debit i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="98084-214">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-214">Click Bind.</span></span>
32. <span data-ttu-id="98084-215">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="98084-216">Utvid model\Payments\Creditor Account(CreditorAccount) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="98084-217">Vis modell\Betalinger\Kreditoragent(CreditorAgent) i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="98084-218">Velg model\Payments\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="98084-219">Velg Excel\PaymLines\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="98084-220">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-220">Click Bind.</span></span>
38. <span data-ttu-id="98084-221">Vis PaymentByCurrency i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="98084-222">Vis PaymentByCurrency\grouped i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="98084-223">Velg PaymentByCurrency\grouped\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="98084-224">Vis Excel\SummaryLines i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="98084-225">Velg Excel\SummaryLines\SummaryCurrency i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="98084-226">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-226">Click Bind.</span></span>
44. <span data-ttu-id="98084-227">Vis PaymentByCurrency\aggregated i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="98084-228">Velg PaymentByCurrency\aggregated\TotalInstructuredAmount i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="98084-229">Velg Excel\SummaryLines\SummaryAmount i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="98084-230">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-230">Click Bind.</span></span>
48. <span data-ttu-id="98084-231">Velg PaymentByCurrency i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="98084-232">Velg Excel\SummaryLines i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="98084-233">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-233">Click Bind.</span></span>
51. <span data-ttu-id="98084-234">Velg modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="98084-235">Velg Excel\PaymLines i treet.</span><span class="sxs-lookup"><span data-stu-id="98084-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="98084-236">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="98084-236">Click Bind.</span></span>
54. <span data-ttu-id="98084-237">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="98084-237">Click Save.</span></span>
55. <span data-ttu-id="98084-238">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="98084-239">Bruke den opprettede konfigurasjonen for behandling av betalinger</span><span class="sxs-lookup"><span data-stu-id="98084-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="98084-240">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="98084-240">Click Change status.</span></span>
2. <span data-ttu-id="98084-241">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="98084-241">Click Complete.</span></span>
3. <span data-ttu-id="98084-242">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98084-242">Click OK.</span></span>
4. <span data-ttu-id="98084-243">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-243">Close the page.</span></span>
5. <span data-ttu-id="98084-244">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-244">Close the page.</span></span>
6. <span data-ttu-id="98084-245">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="98084-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="98084-246">Bruk hurtigfilteret til å filtrere på Betalingsmåte-feltet med verdien Elektronisk.</span><span class="sxs-lookup"><span data-stu-id="98084-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="98084-247">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="98084-247">Electronic</span></span>  
8. <span data-ttu-id="98084-248">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="98084-248">Click Edit.</span></span>
9. <span data-ttu-id="98084-249">Vis delen Filformater.</span><span class="sxs-lookup"><span data-stu-id="98084-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="98084-250">Velg Ja i feltet Generell elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="98084-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="98084-251">Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="98084-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="98084-252">Velg konfigurasjonen Regnearkeksempelrapport.</span><span class="sxs-lookup"><span data-stu-id="98084-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="98084-253">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="98084-253">Click Save.</span></span>
13. <span data-ttu-id="98084-254">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98084-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="98084-255">Bruke den opprettede konfigurasjonen for testing av behandling av betalingsjournaler</span><span class="sxs-lookup"><span data-stu-id="98084-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="98084-256">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="98084-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="98084-257">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="98084-257">Click New.</span></span>
    * <span data-ttu-id="98084-258">Opprett ny betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="98084-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="98084-259">Skriv inn VendPay i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="98084-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="98084-260">VendPay</span></span>  
4. <span data-ttu-id="98084-261">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="98084-261">Click Lines.</span></span>
5. <span data-ttu-id="98084-262">Angi verdiene GB_SI_000001 i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="98084-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="98084-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="98084-264">Sett Debet til 1000.</span><span class="sxs-lookup"><span data-stu-id="98084-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="98084-265">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="98084-265">Click New.</span></span>
8. <span data-ttu-id="98084-266">Angi verdiene GB_SI_000005 i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="98084-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="98084-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="98084-268">Sett Debet til 2000.</span><span class="sxs-lookup"><span data-stu-id="98084-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="98084-269">Skriv inn EUR i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="98084-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="98084-270">EUR</span><span class="sxs-lookup"><span data-stu-id="98084-270">EUR</span></span>  
11. <span data-ttu-id="98084-271">Angi verdiene GBSI OPER i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="98084-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="98084-272">GBSI OPER</span></span>  
12. <span data-ttu-id="98084-273">Skriv inn Elektronisk i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="98084-274">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="98084-274">Electronic</span></span>  
13. <span data-ttu-id="98084-275">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="98084-275">Click Save.</span></span>
14. <span data-ttu-id="98084-276">Klikk Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="98084-276">Click Generate payments.</span></span>
15. <span data-ttu-id="98084-277">Skriv inn Elektronisk i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="98084-278">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="98084-278">Electronic</span></span>  
16. <span data-ttu-id="98084-279">Skriv inn Betalinger i Filnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="98084-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="98084-280">Skriv for eksempel inn Betalinger.</span><span class="sxs-lookup"><span data-stu-id="98084-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="98084-281">Skriv inn GBSI OPER i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="98084-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="98084-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="98084-282">GBSI OPER</span></span>  
18. <span data-ttu-id="98084-283">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98084-283">Click OK.</span></span>
19. <span data-ttu-id="98084-284">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98084-284">Click OK.</span></span>
    * <span data-ttu-id="98084-285">Se gjennom det opprettede regnearket, inkludert detaljer om betalingslinjer samt totalene for hver valutakode som brukes i denne betalingsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="98084-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


