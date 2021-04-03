---
title: ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 1 - Utforme format)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som OPENXML-regnearkfiler (Excel). (Del 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5119255b119a99f3809d2d75bbfdc7b3bad9932
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569563"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="2e583-104">ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 1 - Utforme format)</span><span class="sxs-lookup"><span data-stu-id="2e583-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e583-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.</span><span class="sxs-lookup"><span data-stu-id="2e583-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="2e583-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="2e583-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="2e583-107">For å fullføre disse trinnene, må du først fullføre disse tre oppgaveveiledningene:</span><span class="sxs-lookup"><span data-stu-id="2e583-107">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="2e583-108">"ER Opprette en konfigurasjonsleverandør og merke den som aktiv"</span><span class="sxs-lookup"><span data-stu-id="2e583-108">"ER Create a configuration provider and mark it as active"</span></span>

<span data-ttu-id="2e583-109">"ER Bruke finansdimensjoner som en datakilde (del 1: Utforme datamodell)"</span><span class="sxs-lookup"><span data-stu-id="2e583-109">"ER Use financial dimensions as a data source (Part 1: Design data model)"</span></span>

<span data-ttu-id="2e583-110">"ER Bruke finansdimensjoner som en datakilde (del 2: Modelltilordning)"</span><span class="sxs-lookup"><span data-stu-id="2e583-110">"ER Use financial dimensions as a data source (Part 2: Model mapping)"</span></span>

<span data-ttu-id="2e583-111">Du må også laste ned og lagre en lokal kopi av malen med en eksempelrapport som finnes her: [Eksempel på webtjenesterapport i Finansdimensjoner](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="2e583-111">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="2e583-112">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="2e583-112">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="2e583-113">Opprette en ny rapportkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="2e583-113">Create a new report configuration</span></span>
1. <span data-ttu-id="2e583-114">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="2e583-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2e583-115">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-115">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2e583-116">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="2e583-116">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="2e583-117">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="2e583-117">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="2e583-118">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="2e583-118">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="2e583-119">Skriv inn Eksempelrapport med vannrett utvidbare områder i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e583-119">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="2e583-120">Eksempelrapport med vannrett utvidbare områder</span><span class="sxs-lookup"><span data-stu-id="2e583-120">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="2e583-121">I Beskrivelse-feltet skriver du inn Lage Excel-utdata ved å legge til kolonner dynamisk.</span><span class="sxs-lookup"><span data-stu-id="2e583-121">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="2e583-122">Lage Excel-utdata ved å legge til kolonner dynamisk</span><span class="sxs-lookup"><span data-stu-id="2e583-122">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="2e583-123">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e583-123">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="2e583-124">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="2e583-124">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="2e583-125">Utforme rapportformatet</span><span class="sxs-lookup"><span data-stu-id="2e583-125">Design the report format</span></span>
1. <span data-ttu-id="2e583-126">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="2e583-126">Click Designer.</span></span>
2. <span data-ttu-id="2e583-127">Slå på veksleknappen Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="2e583-127">Turn on the 'Show details' toggle button.</span></span>
3. <span data-ttu-id="2e583-128">Klikk på Import i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2e583-128">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="2e583-129">Klikk på Importer fra Excel.</span><span class="sxs-lookup"><span data-stu-id="2e583-129">Click Import from Excel.</span></span>
5. <span data-ttu-id="2e583-130">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="2e583-130">Click Attachments.</span></span>
    * <span data-ttu-id="2e583-131">Importer malen for rapporten.</span><span class="sxs-lookup"><span data-stu-id="2e583-131">Import the report's template.</span></span> <span data-ttu-id="2e583-132">Bruk Excel-filen som du lastet ned for dette.</span><span class="sxs-lookup"><span data-stu-id="2e583-132">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="2e583-133">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="2e583-133">Click New.</span></span>
7. <span data-ttu-id="2e583-134">Klikk på Fil.</span><span class="sxs-lookup"><span data-stu-id="2e583-134">Click File.</span></span>
8. <span data-ttu-id="2e583-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2e583-135">Close the page.</span></span>
9. <span data-ttu-id="2e583-136">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="2e583-136">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="2e583-137">Velg malen du lastet ned.</span><span class="sxs-lookup"><span data-stu-id="2e583-137">Select the downloaded template.</span></span>  
10. <span data-ttu-id="2e583-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2e583-138">Click OK.</span></span>
    * <span data-ttu-id="2e583-139">Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="2e583-139">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="2e583-140">Hver celle for hver enkelt kolonne vil representere navnet på én finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="2e583-140">Each cell for every column will represent a single financial dimension's name.</span></span>  
11. <span data-ttu-id="2e583-141">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="2e583-141">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="2e583-142">Velg Excel\Område i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-142">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="2e583-143">Skriv inn DimNames i feltet Excel-område.</span><span class="sxs-lookup"><span data-stu-id="2e583-143">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="2e583-144">DimNames</span><span class="sxs-lookup"><span data-stu-id="2e583-144">DimNames</span></span>  
14. <span data-ttu-id="2e583-145">Velg Vannrett i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="2e583-145">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="2e583-146">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2e583-146">Click OK.</span></span>
16. <span data-ttu-id="2e583-147">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-147">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="2e583-148">Klikk på Flytt opp.</span><span class="sxs-lookup"><span data-stu-id="2e583-148">Click Move up.</span></span>
18. <span data-ttu-id="2e583-149">Velg 'Excel = "SampleFinDimWsReport"\Celle<DimNames>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-149">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="2e583-150">Klikk på Klipp ut.</span><span class="sxs-lookup"><span data-stu-id="2e583-150">Click Cut.</span></span>
20. <span data-ttu-id="2e583-151">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-151">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="2e583-152">Klikk på Lim inn.</span><span class="sxs-lookup"><span data-stu-id="2e583-152">Click Paste.</span></span>
22. <span data-ttu-id="2e583-153">Utvid 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="2e583-154">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="2e583-155">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-155">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="2e583-156">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-156">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="2e583-157">Legg til et nytt område for å opprette Excel-utdata dynamisk med like mange kolonner som du valgte (i brukerdialogskjemaet) for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="2e583-157">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="2e583-158">Hver celle for hver enkelt kolonne vil representere verdien for én finansdimensjon for hver rapporteringstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2e583-158">Each cell for every column will represent a single financial dimension's value for each reporting transaction.</span></span>  
26. <span data-ttu-id="2e583-159">Klikk på Legg til område.</span><span class="sxs-lookup"><span data-stu-id="2e583-159">Click Add Range.</span></span>
27. <span data-ttu-id="2e583-160">Skriv inn DimValues i feltet Excel-område.</span><span class="sxs-lookup"><span data-stu-id="2e583-160">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="2e583-161">DimValues</span><span class="sxs-lookup"><span data-stu-id="2e583-161">DimValues</span></span>  
28. <span data-ttu-id="2e583-162">Velg Vannrett i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="2e583-162">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="2e583-163">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2e583-163">Click OK.</span></span>
30. <span data-ttu-id="2e583-164">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<DimValues>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-164">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="2e583-165">Klikk på Klipp ut.</span><span class="sxs-lookup"><span data-stu-id="2e583-165">Click Cut.</span></span>
32. <span data-ttu-id="2e583-166">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-166">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="2e583-167">Klikk på Lim inn.</span><span class="sxs-lookup"><span data-stu-id="2e583-167">Click Paste.</span></span>
34. <span data-ttu-id="2e583-168">Utvid 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-168">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="2e583-169">Tilordne formatelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="2e583-169">Map format elements to data sources</span></span>
1. <span data-ttu-id="2e583-170">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="2e583-170">Click the Mapping tab.</span></span>
2. <span data-ttu-id="2e583-171">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-171">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2e583-172">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="2e583-173">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="2e583-174">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="2e583-175">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett\celle<DimValues>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-175">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="2e583-176">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-176">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="2e583-177">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-177">Click Bind.</span></span>
9. <span data-ttu-id="2e583-178">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/område<DimValues>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-178">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="2e583-179">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="2e583-180">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-180">Click Bind.</span></span>
12. <span data-ttu-id="2e583-181">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Credit>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-181">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="2e583-182">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="2e583-183">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-183">Click Bind.</span></span>
15. <span data-ttu-id="2e583-184">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Debit>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-184">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="2e583-185">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="2e583-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-186">Click Bind.</span></span>
18. <span data-ttu-id="2e583-187">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<Currency>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-187">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="2e583-188">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-188">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="2e583-189">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-189">Click Bind.</span></span>
21. <span data-ttu-id="2e583-190">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransDate>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-190">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="2e583-191">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="2e583-192">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-192">Click Bind.</span></span>
24. <span data-ttu-id="2e583-193">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransVoucher>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-193">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="2e583-194">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="2e583-195">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-195">Click Bind.</span></span>
27. <span data-ttu-id="2e583-196">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett/celle<TransBatch>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-196">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="2e583-197">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="2e583-198">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-198">Click Bind.</span></span>
30. <span data-ttu-id="2e583-199">Velg 'Excel = "SampleFinDimWsReport"\Område<JournalLine>Loddrett/område<TransactionLine>: Loddrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-199">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="2e583-200">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="2e583-201">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-201">Click Bind.</span></span>
33. <span data-ttu-id="2e583-202">Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett/celle<Batch> i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-202">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="2e583-203">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="2e583-204">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-204">Click Bind.</span></span>
36. <span data-ttu-id="2e583-205">Velg Excel = "SampleFinDimWsReport"\Område<JournalLine>:Loddrett i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-205">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="2e583-206">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="2e583-207">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-207">Click Bind.</span></span>
39. <span data-ttu-id="2e583-208">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-208">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="2e583-209">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-209">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="2e583-210">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett\celle<DimNames>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-210">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="2e583-211">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-211">Click Bind.</span></span>
43. <span data-ttu-id="2e583-212">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Dimensjonsinnstilling: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-212">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="2e583-213">Velg 'Excel = "SampleFinDimWsReport"\Område<DimNames>:Vannrett' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-213">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="2e583-214">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-214">Click Bind.</span></span>
46. <span data-ttu-id="2e583-215">Velg 'Excel = "SampleFinDimWsReport"\Celle<CompanyName>' i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-215">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="2e583-216">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="2e583-216">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="2e583-217">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="2e583-217">Click Bind.</span></span>
49. <span data-ttu-id="2e583-218">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="2e583-218">Click Save.</span></span>
50. <span data-ttu-id="2e583-219">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2e583-219">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]