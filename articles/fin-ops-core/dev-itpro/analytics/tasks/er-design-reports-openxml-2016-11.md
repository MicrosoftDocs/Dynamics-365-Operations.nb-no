---
title: ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)
description: Det emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
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
ms.openlocfilehash: d1229c89f43f9ded955dadf2f4d87825c9ab4e71
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182583"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="5e959-103">ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)</span><span class="sxs-lookup"><span data-stu-id="5e959-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e959-104">Det emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en mal for generering av elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="5e959-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="5e959-105">Denne konfigurasjonen vil bli brukt til å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="5e959-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="5e959-106">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i GBSI-firmaet.</span><span class="sxs-lookup"><span data-stu-id="5e959-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="5e959-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="5e959-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="5e959-108">Du må også ha en Excel-fil som importeres når du oppretter malen.</span><span class="sxs-lookup"><span data-stu-id="5e959-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="5e959-109">Denne filen kan åpnes fra [Mal for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="5e959-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="5e959-110">Laste opp modellkonfigurasjon for betalingsdata</span><span class="sxs-lookup"><span data-stu-id="5e959-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="5e959-111">I navigasjonsruten går du til **Moduler > Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="5e959-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="5e959-112">I listen velger du konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5e959-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="5e959-113">Velg **Angi som aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5e959-113">Select **Set active**.</span></span>
4. <span data-ttu-id="5e959-114">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="5e959-114">Select **Repositories**.</span></span> <span data-ttu-id="5e959-115">Velg et repositorium for operasjonsressurstypen, hvis tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5e959-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="5e959-116">Hvis den er tilgjengelige, hopper du over følgende trinn for hvordan du oppretter et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="5e959-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="5e959-117">Velg **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5e959-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="5e959-118">I feltet **Type konfigurasjonsrepositorium** angir du `Operations resourcesdd`.</span><span class="sxs-lookup"><span data-stu-id="5e959-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="5e959-119">Velg **Opprett repositorium**.</span><span class="sxs-lookup"><span data-stu-id="5e959-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="5e959-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e959-120">Select **OK**.</span></span>
9. <span data-ttu-id="5e959-121">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="5e959-121">Select **Open**.</span></span>
10. <span data-ttu-id="5e959-122">Velg **Betalingsmodell** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="5e959-123">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="5e959-123">Select **Import**.</span></span> <span data-ttu-id="5e959-124">Importer denne datamodellen.</span><span class="sxs-lookup"><span data-stu-id="5e959-124">Import this data model.</span></span> <span data-ttu-id="5e959-125">Den vil bli brukt som datakilde i en ny formatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="5e959-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="5e959-126">Hopp over dette trinnet hvis denne konfigurasjonen allerede er importert.</span><span class="sxs-lookup"><span data-stu-id="5e959-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="5e959-127">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5e959-127">Select **Yes**.</span></span>
13. <span data-ttu-id="5e959-128">Lukk sidene til du kommer tilbake til siden for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5e959-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="5e959-129">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="5e959-129">Create a new format configuration</span></span>
1. <span data-ttu-id="5e959-130">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="5e959-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="5e959-131">Velg **Betalingsmodell** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="5e959-132">Velg **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5e959-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="5e959-133">I **Ny**-feltet angir du `Format based on data model PaymentModel`.</span><span class="sxs-lookup"><span data-stu-id="5e959-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="5e959-134">Opprett et format som er basert på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="5e959-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="5e959-135">I **Navn**-feltet skriver du inn `Sample worksheet report`.</span><span class="sxs-lookup"><span data-stu-id="5e959-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="5e959-136">Regnearkeksempelrapport</span><span class="sxs-lookup"><span data-stu-id="5e959-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="5e959-137">I **Beskrivelse**-feltet skriver du inn `Sample worksheet report for vendors’ payments`.</span><span class="sxs-lookup"><span data-stu-id="5e959-137">In the **Description** field, type `Sample worksheet report for vendors’ payments`.</span></span> <span data-ttu-id="5e959-138">Regnearkeksempelrapport for leverandørenes betalinger.</span><span class="sxs-lookup"><span data-stu-id="5e959-138">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="5e959-139">Angi eller velg en verdi i feltet **Definisjon av datamodell**.</span><span class="sxs-lookup"><span data-stu-id="5e959-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="5e959-140">Velg definisjonen **CustomerCreditTransferInitiation**.</span><span class="sxs-lookup"><span data-stu-id="5e959-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="5e959-141">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="5e959-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="5e959-142">Utforme et nytt dokument i OPENXML-regnearkformat</span><span class="sxs-lookup"><span data-stu-id="5e959-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="5e959-143">Velg **Betalingsmodell\Regnearkeksempelrapport** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="5e959-144">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="5e959-144">Select **Designer**.</span></span>
3. <span data-ttu-id="5e959-145">Velg **Importer** på handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5e959-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="5e959-146">Velg **Importer fra Excel**.</span><span class="sxs-lookup"><span data-stu-id="5e959-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="5e959-147">Velg **Vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="5e959-147">Select **Attachments**.</span></span> <span data-ttu-id="5e959-148">Knytte det eksisterende Excel-dokumentet til som en mal.</span><span class="sxs-lookup"><span data-stu-id="5e959-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="5e959-149">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e959-149">Select **New**.</span></span>
7. <span data-ttu-id="5e959-150">Velg **Fil**.</span><span class="sxs-lookup"><span data-stu-id="5e959-150">Select **File**.</span></span> <span data-ttu-id="5e959-151">Velg den eksisterende Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="5e959-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="5e959-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e959-152">Close the page.</span></span>
9. <span data-ttu-id="5e959-153">Angi eller velg en verdi i feltet **Mal**.</span><span class="sxs-lookup"><span data-stu-id="5e959-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="5e959-154">Velg at den vedlagte Excel-filen skal brukes som en mal.</span><span class="sxs-lookup"><span data-stu-id="5e959-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="5e959-155">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e959-155">Select **OK**.</span></span> <span data-ttu-id="5e959-156">Legg merke til at ER-formatkomponenter er opprettet i utformingsformatet basert på strukturen til det refererende MS Excel-dokumentet (navngitte områder).</span><span class="sxs-lookup"><span data-stu-id="5e959-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="5e959-157">Opprette en ny datakilde for å beregne totaler etter valutakoder</span><span class="sxs-lookup"><span data-stu-id="5e959-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="5e959-158">Velg kategorien **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="5e959-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="5e959-159">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5e959-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="5e959-160">Velg **Funksjoner\Grupper etter** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="5e959-161">I **Navn**-feltet skriver du inn `PaymentByCurrency`.</span><span class="sxs-lookup"><span data-stu-id="5e959-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="5e959-162">Velg **Rediger gruppe etter**.</span><span class="sxs-lookup"><span data-stu-id="5e959-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="5e959-163">Utvid **modell** i treet, og velg deretter **modell\Betalinger.**</span><span class="sxs-lookup"><span data-stu-id="5e959-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="5e959-164">Velg **Legg til felt i**.</span><span class="sxs-lookup"><span data-stu-id="5e959-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="5e959-165">Velg **Hva skal grupperes**.</span><span class="sxs-lookup"><span data-stu-id="5e959-165">Select **What to group**.</span></span>
9. <span data-ttu-id="5e959-166">Utvid **modell\Betalinger** i treet, og velg deretter **modell\Betalinger\Valuta**.</span><span class="sxs-lookup"><span data-stu-id="5e959-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="5e959-167">Velg **Legg til felt i**.</span><span class="sxs-lookup"><span data-stu-id="5e959-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="5e959-168">Velg **Grupperte felt**.</span><span class="sxs-lookup"><span data-stu-id="5e959-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="5e959-169">Velg **model\Payments\Instructed Amount(InstructedAmount)** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="5e959-170">Velg **Legg til felt i**, og velg deretter **Aggregeringsfelt**.</span><span class="sxs-lookup"><span data-stu-id="5e959-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="5e959-171">Velg et alternativ i **Metode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5e959-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="5e959-172">Velg **mengdefunksjonen SUM**.</span><span class="sxs-lookup"><span data-stu-id="5e959-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="5e959-173">I **Navn**-feltet skriver du inn `TotalInstructuredAmount`.</span><span class="sxs-lookup"><span data-stu-id="5e959-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="5e959-174">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5e959-174">Select **Save**.</span></span>
17. <span data-ttu-id="5e959-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e959-175">Close the page.</span></span>
18. <span data-ttu-id="5e959-176">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e959-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="5e959-177">Tilordne formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="5e959-177">Map format components to data sources</span></span>
1. <span data-ttu-id="5e959-178">Velg **model\Payments\Initiating Party(InitiatingParty)\Name** og **Excel\ReportHeader\CompanyName** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="5e959-179">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-179">Select **Bind**.</span></span>
3. <span data-ttu-id="5e959-180">Velg **model\Payments\Creditor\Identification\Source ID(SourceID)** og **Excel\PaymLines\VendAccountName** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="5e959-181">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-181">Select **Bind**.</span></span>
5. <span data-ttu-id="5e959-182">Velg **model\Payments\Creditor\Name** og **Excel\PaymLines\VendName** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="5e959-183">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-183">Select **Bind**.</span></span>
7. <span data-ttu-id="5e959-184">Velg **model\Payments\Creditor Agent(CreditorAgent)\Name** og **Excel\PaymLines\Bank** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="5e959-185">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-185">Select **Bind**.</span></span>
9. <span data-ttu-id="5e959-186">Velg **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** og **Excel\PaymLines\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="5e959-187">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-187">Select **Bind**.</span></span>
11. <span data-ttu-id="5e959-188">Velg **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** og **Excel\PaymLines\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="5e959-189">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-189">Select **Bind**.</span></span>
13. <span data-ttu-id="5e959-190">Velg **model\Payments\Instructed Amount(InstructedAmount)** og **Excel\PaymLines\Debit** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="5e959-191">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-191">Select **Bind**.</span></span>
15. <span data-ttu-id="5e959-192">Velg **model\Payments\Currency** og **Excel\PaymLines\Currency** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="5e959-193">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-193">Select **Bind**.</span></span>
17. <span data-ttu-id="5e959-194">Velg **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="5e959-195">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-195">Select **Bind**.</span></span>
19. <span data-ttu-id="5e959-196">Velg **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="5e959-197">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-197">Select **Bind**.</span></span>
21. <span data-ttu-id="5e959-198">Velg **PaymentByCurrency** og **Excel\SummaryLines** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="5e959-199">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-199">Select **Bind**.</span></span>
23. <span data-ttu-id="5e959-200">Velg **model\Payments** og **Excel\PaymLines** i treet.</span><span class="sxs-lookup"><span data-stu-id="5e959-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="5e959-201">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5e959-201">Select **Bind**.</span></span>
25. <span data-ttu-id="5e959-202">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="5e959-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="5e959-203">Bruke den opprettede konfigurasjonen for behandling av betalinger</span><span class="sxs-lookup"><span data-stu-id="5e959-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="5e959-204">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="5e959-204">Select **Change status**.</span></span>
2. <span data-ttu-id="5e959-205">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="5e959-205">Select **Complete**.</span></span>
3. <span data-ttu-id="5e959-206">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e959-206">Select **OK**.</span></span>
4. <span data-ttu-id="5e959-207">I navigasjonsruten går du til **Moduler > Leverandører > Betalingsoppsett > Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="5e959-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="5e959-208">Bruk hurtigfilteret til å filtrere på **Betalingsmåte**-feltet med verdien **Elektronisk**.</span><span class="sxs-lookup"><span data-stu-id="5e959-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="5e959-209">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="5e959-209">Select **Edit**.</span></span>
7. <span data-ttu-id="5e959-210">Vis delen **Filformater**.</span><span class="sxs-lookup"><span data-stu-id="5e959-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="5e959-211">Velg **Ja** i feltet **Generell elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="5e959-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="5e959-212">Angi eller velg en verdi i feltet **Eksportformatkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="5e959-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="5e959-213">Velg konfigurasjonen **Regnearkeksempelrapport**.</span><span class="sxs-lookup"><span data-stu-id="5e959-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="5e959-214">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5e959-214">Select **Save**.</span></span>
11. <span data-ttu-id="5e959-215">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e959-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="5e959-216">Bruke den opprettede konfigurasjonen for testing av behandling av betalingsjournaler</span><span class="sxs-lookup"><span data-stu-id="5e959-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="5e959-217">Gå til **Moduler > Leverandører > Fakturaer > Betalinger > Betalingsjournal** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="5e959-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="5e959-218">Velg **Ny** for å opprette en ny betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="5e959-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="5e959-219">Skriv inn **VendPay** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5e959-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="5e959-220">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="5e959-220">Select **Lines**.</span></span>
5. <span data-ttu-id="5e959-221">I **Konto**-feltet angir du verdiene `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="5e959-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="5e959-222">Sett **Debet** til `1000`.</span><span class="sxs-lookup"><span data-stu-id="5e959-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="5e959-223">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e959-223">Select **New**.</span></span>
8. <span data-ttu-id="5e959-224">I **Konto**-feltet angir du verdiene `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="5e959-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="5e959-225">Sett **Debet** til `2000`.</span><span class="sxs-lookup"><span data-stu-id="5e959-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="5e959-226">I **Valuta**-feltet skriver du inn `EUR`.</span><span class="sxs-lookup"><span data-stu-id="5e959-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="5e959-227">I **Motkonto**-feltet angir du verdiene `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="5e959-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="5e959-228">I **Betalingsmåte**-feltet skriver du inn `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="5e959-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="5e959-229">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5e959-229">Select **Save**.</span></span>
14. <span data-ttu-id="5e959-230">Velg **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="5e959-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="5e959-231">I **Betalingsmåte**-feltet skriver du inn `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="5e959-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="5e959-232">I **Filnavn**-feltet skriver du inn `Payments`.</span><span class="sxs-lookup"><span data-stu-id="5e959-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="5e959-233">I **Bankkonto**-feltet skriver du inn `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="5e959-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="5e959-234">Velg **OK**, og velg deretter **OK** på nytt.</span><span class="sxs-lookup"><span data-stu-id="5e959-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="5e959-235">Se gjennom det opprettede regnearket, inkludert detaljer om betalingslinjer samt totalene for hver valutakode som brukes i denne betalingsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="5e959-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

