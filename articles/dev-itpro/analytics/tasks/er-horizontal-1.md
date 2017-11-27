--- 
title: "Utforme et format for å bruke områder som kan utvides vannrett for å legge til kolonner i Excel-rapporter dynamisk for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: 1ccf3b2d81066fce80fe14428fab24020ab85496
ms.openlocfilehash: b921b5ff51f951112031fe8b1bc2faa90cf29a28
ms.contentlocale: nb-no
ms.lasthandoff: 11/07/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="eb6c7-103">Utforme et format for å bruke områder som kan utvides vannrett for å legge til kolonner i Excel-rapporter dynamisk for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="eb6c7-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb6c7-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="eb6c7-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="eb6c7-106">For å fullføre disse trinnene, må du først fullføre disse tre oppgaveveiledningene:</span><span class="sxs-lookup"><span data-stu-id="eb6c7-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="eb6c7-107">"ER Opprette en konfigurasjonsleverandør og merke den som aktiv"</span><span class="sxs-lookup"><span data-stu-id="eb6c7-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="eb6c7-108">"ER Bruke finansdimensjoner som en datakilde (del 1: Utforme datamodell)"</span><span class="sxs-lookup"><span data-stu-id="eb6c7-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="eb6c7-109">"ER Bruke finansdimensjoner som en datakilde (del 2: Modelltilordning)"</span><span class="sxs-lookup"><span data-stu-id="eb6c7-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="eb6c7-110">Du må også laste ned og lagre en lokal kopi av malen med en eksempelrapport som finnes her: [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="eb6c7-110">You must also download and save a local copy of the template with a sample report found here, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 


<span data-ttu-id="eb6c7-111">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="eb6c7-112">Opprette en ny rapportkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="eb6c7-112">Create a new report configuration</span></span>
1. <span data-ttu-id="eb6c7-113">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="eb6c7-114">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="eb6c7-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="eb6c7-116">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="eb6c7-117">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="eb6c7-118">Skriv inn Eksempelrapport med vannrett utvidbare områder i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="eb6c7-119">Eksempelrapport med vannrett utvidbare områder</span><span class="sxs-lookup"><span data-stu-id="eb6c7-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="eb6c7-120">I Beskrivelse-feltet skriver du inn Lage Excel-utdata ved å legge til kolonner dynamisk.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="eb6c7-121">Lage Excel-utdata ved å legge til kolonner dynamisk</span><span class="sxs-lookup"><span data-stu-id="eb6c7-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="eb6c7-122">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="eb6c7-123">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="eb6c7-124">Utforme rapportformatet</span><span class="sxs-lookup"><span data-stu-id="eb6c7-124">Design the report format</span></span>
1. <span data-ttu-id="eb6c7-125">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-125">Click Designer.</span></span>
2. <span data-ttu-id="eb6c7-126">Slå på veksleknappen Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="eb6c7-127">Klikk Import i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="eb6c7-128">Klikk Importer fra Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="eb6c7-129">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-129">Click Attachments.</span></span>
    * <span data-ttu-id="eb6c7-130">Importer malen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-130">Import the report’s template.</span></span> <span data-ttu-id="eb6c7-131">Bruk Excel-filen som du lastet ned for dette.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="eb6c7-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-132">Click New.</span></span>
7. <span data-ttu-id="eb6c7-133">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-133">Click File.</span></span>
8. <span data-ttu-id="eb6c7-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-134">Close the page.</span></span>
9. <span data-ttu-id="eb6c7-135">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="eb6c7-136">Velg malen du lastet ned.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="eb6c7-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-137">Click OK.</span></span>
    * <span data-ttu-id="eb6c7-138">Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="eb6c7-139">Hver celle for hver enkelt kolonne vil representere navnet på én finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="eb6c7-140">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="eb6c7-141">Velg Excel\Område i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="eb6c7-142">Skriv inn DimNames i feltet Excel-område.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="eb6c7-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="eb6c7-143">DimNames</span></span>  
14. <span data-ttu-id="eb6c7-144">Velg Vannrett i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="eb6c7-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-145">Click OK.</span></span>
16. <span data-ttu-id="eb6c7-146">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="eb6c7-147">Klikk Flytt opp.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-147">Click Move up.</span></span>
18. <span data-ttu-id="eb6c7-148">Velg 'Excel = "SampleFinDimWsReport"\Celle<DimNames>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="eb6c7-149">Klikk Klipp ut.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-149">Click Cut.</span></span>
20. <span data-ttu-id="eb6c7-150">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="eb6c7-151">Klikk Lim inn.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-151">Click Paste.</span></span>
22. <span data-ttu-id="eb6c7-152">Utvid 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="eb6c7-153">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="eb6c7-154">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="eb6c7-155">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="eb6c7-156">Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="eb6c7-157">Hver celle for hver enkelt kolonne vil representere verdien for én finansdimensjon for hver rapporteringstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="eb6c7-158">Klikk Legg til område.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-158">Click Add Range.</span></span>
27. <span data-ttu-id="eb6c7-159">Skriv inn DimValues i feltet Excel-område.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="eb6c7-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="eb6c7-160">DimValues</span></span>  
28. <span data-ttu-id="eb6c7-161">Velg Vannrett i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="eb6c7-162">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-162">Click OK.</span></span>
30. <span data-ttu-id="eb6c7-163">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<DimValues>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="eb6c7-164">Klikk Klipp ut.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-164">Click Cut.</span></span>
32. <span data-ttu-id="eb6c7-165">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="eb6c7-166">Klikk Lim inn.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-166">Click Paste.</span></span>
34. <span data-ttu-id="eb6c7-167">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="eb6c7-168">Tilordne formatelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="eb6c7-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="eb6c7-169">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="eb6c7-170">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="eb6c7-171">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="eb6c7-172">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="eb6c7-173">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="eb6c7-174">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett\celle<DimValues>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="eb6c7-175">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="eb6c7-176">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-176">Click Bind.</span></span>
9. <span data-ttu-id="eb6c7-177">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="eb6c7-178">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="eb6c7-179">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-179">Click Bind.</span></span>
12. <span data-ttu-id="eb6c7-180">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Credit>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="eb6c7-181">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="eb6c7-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-182">Click Bind.</span></span>
15. <span data-ttu-id="eb6c7-183">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Debit>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="eb6c7-184">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="eb6c7-185">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-185">Click Bind.</span></span>
18. <span data-ttu-id="eb6c7-186">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Currency>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="eb6c7-187">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="eb6c7-188">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-188">Click Bind.</span></span>
21. <span data-ttu-id="eb6c7-189">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransDate>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="eb6c7-190">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="eb6c7-191">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-191">Click Bind.</span></span>
24. <span data-ttu-id="eb6c7-192">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransVoucher>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="eb6c7-193">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="eb6c7-194">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-194">Click Bind.</span></span>
27. <span data-ttu-id="eb6c7-195">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransBatch>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="eb6c7-196">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="eb6c7-197">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-197">Click Bind.</span></span>
30. <span data-ttu-id="eb6c7-198">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="eb6c7-199">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="eb6c7-200">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-200">Click Bind.</span></span>
33. <span data-ttu-id="eb6c7-201">Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett/celle<Batch> i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="eb6c7-202">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="eb6c7-203">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-203">Click Bind.</span></span>
36. <span data-ttu-id="eb6c7-204">Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="eb6c7-205">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="eb6c7-206">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-206">Click Bind.</span></span>
39. <span data-ttu-id="eb6c7-207">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="eb6c7-208">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="eb6c7-209">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett\celle<DimNames>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="eb6c7-210">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-210">Click Bind.</span></span>
43. <span data-ttu-id="eb6c7-211">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="eb6c7-212">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="eb6c7-213">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-213">Click Bind.</span></span>
46. <span data-ttu-id="eb6c7-214">Velg 'Excel = "SampleFinDimWsReport"\Celle<CompanyName>' i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="eb6c7-215">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="eb6c7-216">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-216">Click Bind.</span></span>
49. <span data-ttu-id="eb6c7-217">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-217">Click Save.</span></span>
50. <span data-ttu-id="eb6c7-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eb6c7-218">Close the page.</span></span>


