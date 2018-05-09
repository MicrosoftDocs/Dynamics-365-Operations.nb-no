--- 
title: "Utforme et format for å bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 81edbccd8d94ea322e80056879a6d4b6caca4555
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="4a4bc-103">Utforme et format for å bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk</span><span class="sxs-lookup"><span data-stu-id="4a4bc-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a4bc-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="4a4bc-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4a4bc-106">For å fullføre disse trinnene, må du først fullføre disse tre oppgaveveiledningene:</span><span class="sxs-lookup"><span data-stu-id="4a4bc-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="4a4bc-107">"ER Opprette en konfigurasjonsleverandør og merke den som aktiv"</span><span class="sxs-lookup"><span data-stu-id="4a4bc-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="4a4bc-108">"ER Bruke finansdimensjoner som en datakilde (del 1: Utforme datamodell)"</span><span class="sxs-lookup"><span data-stu-id="4a4bc-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="4a4bc-109">"ER Bruke finansdimensjoner som en datakilde (del 2: Modelltilordning)"</span><span class="sxs-lookup"><span data-stu-id="4a4bc-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="4a4bc-110">Du må også laste ned og lagre en lokal kopi av malen med en eksempelrapport du finner her [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="4a4bc-110">You must also download and save a local copy of the template with a sample report found here, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 


<span data-ttu-id="4a4bc-111">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="4a4bc-112">Opprette en ny rapportkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="4a4bc-112">Create a new report configuration</span></span>
1. <span data-ttu-id="4a4bc-113">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4a4bc-114">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4a4bc-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="4a4bc-116">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="4a4bc-117">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="4a4bc-118">Skriv inn Eksempelrapport med vannrett utvidbare områder i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="4a4bc-119">Eksempelrapport med vannrett utvidbare områder</span><span class="sxs-lookup"><span data-stu-id="4a4bc-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="4a4bc-120">I Beskrivelse-feltet skriver du inn Lage Excel-utdata ved å legge til kolonner dynamisk.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="4a4bc-121">Lage Excel-utdata ved å legge til kolonner dynamisk</span><span class="sxs-lookup"><span data-stu-id="4a4bc-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="4a4bc-122">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="4a4bc-123">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="4a4bc-124">Utforme rapportformatet</span><span class="sxs-lookup"><span data-stu-id="4a4bc-124">Design the report format</span></span>
1. <span data-ttu-id="4a4bc-125">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-125">Click Designer.</span></span>
2. <span data-ttu-id="4a4bc-126">Slå på veksleknappen Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="4a4bc-127">Klikk Import i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="4a4bc-128">Klikk Importer fra Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="4a4bc-129">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-129">Click Attachments.</span></span>
    * <span data-ttu-id="4a4bc-130">Importer malen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-130">Import the report’s template.</span></span> <span data-ttu-id="4a4bc-131">Bruk Excel-filen som du lastet ned for dette.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="4a4bc-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-132">Click New.</span></span>
7. <span data-ttu-id="4a4bc-133">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-133">Click File.</span></span>
8. <span data-ttu-id="4a4bc-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-134">Close the page.</span></span>
9. <span data-ttu-id="4a4bc-135">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="4a4bc-136">Velg malen du lastet ned.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="4a4bc-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-137">Click OK.</span></span>
    * <span data-ttu-id="4a4bc-138">Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="4a4bc-139">Hver celle for hver enkelt kolonne vil representere navnet på én finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="4a4bc-140">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="4a4bc-141">Velg Excel\Område i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="4a4bc-142">Skriv inn DimNames i feltet Excel-område.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="4a4bc-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="4a4bc-143">DimNames</span></span>  
14. <span data-ttu-id="4a4bc-144">Velg Vannrett i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="4a4bc-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-145">Click OK.</span></span>
16. <span data-ttu-id="4a4bc-146">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="4a4bc-147">Klikk Flytt opp.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-147">Click Move up.</span></span>
18. <span data-ttu-id="4a4bc-148">Velg 'Excel = "SampleFinDimWsReport"\Celle<DimNames>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="4a4bc-149">Klikk Klipp ut.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-149">Click Cut.</span></span>
20. <span data-ttu-id="4a4bc-150">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="4a4bc-151">Klikk Lim inn.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-151">Click Paste.</span></span>
22. <span data-ttu-id="4a4bc-152">Utvid 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="4a4bc-153">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="4a4bc-154">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="4a4bc-155">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="4a4bc-156">Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="4a4bc-157">Hver celle for hver enkelt kolonne vil representere verdien for én finansdimensjon for hver rapporteringstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="4a4bc-158">Klikk Legg til område.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-158">Click Add Range.</span></span>
27. <span data-ttu-id="4a4bc-159">Skriv inn DimValues i feltet Excel-område.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="4a4bc-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="4a4bc-160">DimValues</span></span>  
28. <span data-ttu-id="4a4bc-161">Velg Vannrett i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="4a4bc-162">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-162">Click OK.</span></span>
30. <span data-ttu-id="4a4bc-163">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<DimValues>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="4a4bc-164">Klikk Klipp ut.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-164">Click Cut.</span></span>
32. <span data-ttu-id="4a4bc-165">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="4a4bc-166">Klikk Lim inn.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-166">Click Paste.</span></span>
34. <span data-ttu-id="4a4bc-167">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="4a4bc-168">Tilordne formatelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="4a4bc-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="4a4bc-169">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="4a4bc-170">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4a4bc-171">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="4a4bc-172">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="4a4bc-173">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="4a4bc-174">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett\celle<DimValues>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="4a4bc-175">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="4a4bc-176">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-176">Click Bind.</span></span>
9. <span data-ttu-id="4a4bc-177">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="4a4bc-178">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="4a4bc-179">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-179">Click Bind.</span></span>
12. <span data-ttu-id="4a4bc-180">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Credit>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="4a4bc-181">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="4a4bc-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-182">Click Bind.</span></span>
15. <span data-ttu-id="4a4bc-183">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Debit>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="4a4bc-184">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="4a4bc-185">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-185">Click Bind.</span></span>
18. <span data-ttu-id="4a4bc-186">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Currency>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="4a4bc-187">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="4a4bc-188">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-188">Click Bind.</span></span>
21. <span data-ttu-id="4a4bc-189">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransDate>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="4a4bc-190">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="4a4bc-191">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-191">Click Bind.</span></span>
24. <span data-ttu-id="4a4bc-192">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransVoucher>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="4a4bc-193">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="4a4bc-194">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-194">Click Bind.</span></span>
27. <span data-ttu-id="4a4bc-195">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransBatch>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="4a4bc-196">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="4a4bc-197">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-197">Click Bind.</span></span>
30. <span data-ttu-id="4a4bc-198">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="4a4bc-199">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="4a4bc-200">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-200">Click Bind.</span></span>
33. <span data-ttu-id="4a4bc-201">Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett/celle<Batch> i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="4a4bc-202">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="4a4bc-203">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-203">Click Bind.</span></span>
36. <span data-ttu-id="4a4bc-204">Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="4a4bc-205">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="4a4bc-206">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-206">Click Bind.</span></span>
39. <span data-ttu-id="4a4bc-207">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="4a4bc-208">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="4a4bc-209">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett\celle<DimNames>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="4a4bc-210">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-210">Click Bind.</span></span>
43. <span data-ttu-id="4a4bc-211">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="4a4bc-212">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="4a4bc-213">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-213">Click Bind.</span></span>
46. <span data-ttu-id="4a4bc-214">Velg 'Excel = "SampleFinDimWsReport"\Celle<CompanyName>' i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="4a4bc-215">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="4a4bc-216">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-216">Click Bind.</span></span>
49. <span data-ttu-id="4a4bc-217">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-217">Click Save.</span></span>
50. <span data-ttu-id="4a4bc-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4a4bc-218">Close the page.</span></span>


