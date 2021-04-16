---
title: Endre modeller og tilordninger for å generere dokumenter med programdata
description: Dette emnet beskriver hvordan du utformer konfigurasjoner for rapportering for å generere et elektronisk dokument og oppdatere programdata. (Del 2 – generere dokumenter).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751612"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="d28ba-104">Endre modeller og tilordninger for å generere dokumenter med programdata</span><span class="sxs-lookup"><span data-stu-id="d28ba-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d28ba-105">For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 2: generere dokumenter)".</span><span class="sxs-lookup"><span data-stu-id="d28ba-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="d28ba-106">Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="d28ba-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="d28ba-107">I denne fremgangsmåten skal du endre ER-konfigurasjonene for å begynne med å bruke dem til å generere elektroniske dokumenter og oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="d28ba-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="d28ba-108">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="d28ba-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="d28ba-109">Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="d28ba-110">Endre datamodell</span><span class="sxs-lookup"><span data-stu-id="d28ba-110">Modify data model</span></span>
1. <span data-ttu-id="d28ba-111">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="d28ba-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d28ba-112">Velg 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="d28ba-113">Du vil utvide hvordan du bruker datamodellen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-113">You will extend how you use the data model.</span></span> <span data-ttu-id="d28ba-114">I tillegg til å bruke den som datakilde for å generere Intrastat-rapporten, brukes datamodellen til å samle inn informasjon om Intrastat-rapportering av prosessen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="d28ba-115">Detaljene vil deretter brukes til å oppdatere applikasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="d28ba-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="d28ba-116">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d28ba-116">Click Designer.</span></span>
4. <span data-ttu-id="d28ba-117">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="d28ba-118">I feltet Ny node som en for angir du Modellrot.</span><span class="sxs-lookup"><span data-stu-id="d28ba-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="d28ba-119">Skriv inn "For oppdatering av programdata" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="d28ba-120">For oppdatering av programdata</span><span class="sxs-lookup"><span data-stu-id="d28ba-120">For application data update</span></span>  
7. <span data-ttu-id="d28ba-121">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-121">Click Add.</span></span>
8. <span data-ttu-id="d28ba-122">Velg "For oppdatering av programdata" i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="d28ba-123">Denne nye rotelementet legges til å angi dataflyten for å flytte data fra rapporten Intrastat (brukes som en datakilde) til applikasjonen tabellene (oppdatering målet).</span><span class="sxs-lookup"><span data-stu-id="d28ba-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="d28ba-124">Roten for ulike varer må tilordnes automatisk for å hente data som er postert til det utgående dokumentet og henter data fra dokumentet som brukes til å oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="d28ba-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="d28ba-125">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="d28ba-126">Skriv inn "Arkivhode" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="d28ba-127">Arkivhode</span><span class="sxs-lookup"><span data-stu-id="d28ba-127">Archive header</span></span>  
11. <span data-ttu-id="d28ba-128">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="d28ba-129">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-129">Click Add.</span></span>
    * <span data-ttu-id="d28ba-130">Siden du vil opprette en post for hver Intrastat-rapport som genereres, må du opprette en ny vare for den.</span><span class="sxs-lookup"><span data-stu-id="d28ba-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="d28ba-131">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="d28ba-132">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="d28ba-133">Filnavn</span><span class="sxs-lookup"><span data-stu-id="d28ba-133">File name</span></span>  
15. <span data-ttu-id="d28ba-134">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="d28ba-135">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-135">Click Add.</span></span>
17. <span data-ttu-id="d28ba-136">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="d28ba-137">Skriv inn "Antall linjer" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="d28ba-138">Antall linjer</span><span class="sxs-lookup"><span data-stu-id="d28ba-138">Number of lines</span></span>  
19. <span data-ttu-id="d28ba-139">Velg "Heltall" i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="d28ba-140">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-140">Click Add.</span></span>
    * <span data-ttu-id="d28ba-141">Legg til denne varen for å angi antallet Intrastat-transaksjoner som er rapportert under gjeldende rapporteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="d28ba-142">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="d28ba-143">Skriv inn "Arkivlinjer" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="d28ba-144">Arkivlinjer</span><span class="sxs-lookup"><span data-stu-id="d28ba-144">Archive lines</span></span>  
23. <span data-ttu-id="d28ba-145">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="d28ba-146">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-146">Click Add.</span></span>
    * <span data-ttu-id="d28ba-147">Legg til denne varen for å representere listen over Intrastat-transaksjoner som er rapportert under gjeldende rapporteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="d28ba-148">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="d28ba-149">I Navn-feltet skriver du inn Beløp.</span><span class="sxs-lookup"><span data-stu-id="d28ba-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="d28ba-150">Beløp</span><span class="sxs-lookup"><span data-stu-id="d28ba-150">Amount</span></span>  
27. <span data-ttu-id="d28ba-151">Velg Faktisk i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="d28ba-152">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-152">Click Add.</span></span>
29. <span data-ttu-id="d28ba-153">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="d28ba-154">Skriv inn "Artikkelpost-ID" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="d28ba-155">Artikkelpost-ID</span><span class="sxs-lookup"><span data-stu-id="d28ba-155">Commodity rec id</span></span>  
31. <span data-ttu-id="d28ba-156">Velg Int64 i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="d28ba-157">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-157">Click Add.</span></span>
33. <span data-ttu-id="d28ba-158">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="d28ba-159">I Navn-feltet skriver du inn Varenummer.</span><span class="sxs-lookup"><span data-stu-id="d28ba-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="d28ba-160">Varenummer</span><span class="sxs-lookup"><span data-stu-id="d28ba-160">Item number</span></span>  
35. <span data-ttu-id="d28ba-161">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="d28ba-162">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-162">Click Add.</span></span>
37. <span data-ttu-id="d28ba-163">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d28ba-163">Click Save.</span></span>
38. <span data-ttu-id="d28ba-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d28ba-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="d28ba-165">Endre modelltilordning</span><span class="sxs-lookup"><span data-stu-id="d28ba-165">Modify model mapping</span></span>
1. <span data-ttu-id="d28ba-166">Utvid 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="d28ba-167">Velg 'Intrastat (modell)\Intrastat (tilordning)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="d28ba-168">Endre den eksisterende modell tilordningen til å bruke den for oppdateringen av programdata og for å arkivere Intrastat-rapportering detaljer.</span><span class="sxs-lookup"><span data-stu-id="d28ba-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="d28ba-169">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d28ba-169">Click Designer.</span></span>
4. <span data-ttu-id="d28ba-170">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="d28ba-170">Click New.</span></span>
5. <span data-ttu-id="d28ba-171">Skriv inn "Oppdater arkiv" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="d28ba-172">Oppdater arkiv</span><span class="sxs-lookup"><span data-stu-id="d28ba-172">Update archive</span></span>  
6. <span data-ttu-id="d28ba-173">Velg "Til mål" i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="d28ba-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="d28ba-174">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d28ba-174">Click Save.</span></span>
    * <span data-ttu-id="d28ba-175">Denne nye tilordningen angir dataflyt for flytting av data (rapportere Intrastat-detaljer) fra datamodellen til programmet tabellene (oppdatering målet).</span><span class="sxs-lookup"><span data-stu-id="d28ba-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="d28ba-176">Legg merke til at ulike modeller roten varer må brukes til å hente data fra programmet for rapporteringsprosessen og deretter bruke dataene fra datamodellen for oppdateringen av programdata.</span><span class="sxs-lookup"><span data-stu-id="d28ba-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="d28ba-177">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d28ba-177">Click Designer.</span></span>
9. <span data-ttu-id="d28ba-178">Velg 'Datamodell\Datamodell' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="d28ba-179">Legg til den obligatoriske datakilden.</span><span class="sxs-lookup"><span data-stu-id="d28ba-179">Add the required data source.</span></span> <span data-ttu-id="d28ba-180">Dette er datamodellen som inneholder detaljer om de rapporterte Intrastat-transaksjonene som må være arkivert.</span><span class="sxs-lookup"><span data-stu-id="d28ba-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="d28ba-181">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="d28ba-181">Click Add root.</span></span>
11. <span data-ttu-id="d28ba-182">I Navn-feltet skriver du inn "modell".</span><span class="sxs-lookup"><span data-stu-id="d28ba-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="d28ba-183">modell</span><span class="sxs-lookup"><span data-stu-id="d28ba-183">model</span></span>  
12. <span data-ttu-id="d28ba-184">I feltet Definisjon, angir eller velger du verdien "For oppdatering av programdata".</span><span class="sxs-lookup"><span data-stu-id="d28ba-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="d28ba-185">For oppdatering av programdata</span><span class="sxs-lookup"><span data-stu-id="d28ba-185">For application data update</span></span>  
13. <span data-ttu-id="d28ba-186">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d28ba-186">Click OK.</span></span>
14. <span data-ttu-id="d28ba-187">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="d28ba-188">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="d28ba-189">Velg 'modell\Arkivhode' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="d28ba-190">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-190">Click Add.</span></span>
    * <span data-ttu-id="d28ba-191">Hvis du vil nummerere rapporterte Intrastat-transaksjoner for arkivering, må den riktige datakilden legges til.</span><span class="sxs-lookup"><span data-stu-id="d28ba-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="d28ba-192">Skriv inn "Opplistede linjer" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="d28ba-193">Opplistede linjer</span><span class="sxs-lookup"><span data-stu-id="d28ba-193">Enumerated lines</span></span>  
19. <span data-ttu-id="d28ba-194">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="d28ba-194">Click Edit formula.</span></span>
20. <span data-ttu-id="d28ba-195">Velg 'List\ENUMERATE' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="d28ba-196">Klikk på Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="d28ba-196">Click Add function.</span></span>
22. <span data-ttu-id="d28ba-197">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="d28ba-198">Utvide 'modell\Arkivhode' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="d28ba-199">Velg 'modell\Arkivhode\Arkivlinjer'.</span><span class="sxs-lookup"><span data-stu-id="d28ba-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="d28ba-200">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="d28ba-200">Click Add data source.</span></span>
26. <span data-ttu-id="d28ba-201">I Formel-feltet angir du 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span><span class="sxs-lookup"><span data-stu-id="d28ba-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="d28ba-202">ENUMERATE(model.'Arkivhode'.'Arkivlinjer')</span><span class="sxs-lookup"><span data-stu-id="d28ba-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="d28ba-203">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d28ba-203">Click Save.</span></span>
28. <span data-ttu-id="d28ba-204">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d28ba-204">Close the page.</span></span>
29. <span data-ttu-id="d28ba-205">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d28ba-205">Click OK.</span></span>
30. <span data-ttu-id="d28ba-206">Klikk på Legg til mål.</span><span class="sxs-lookup"><span data-stu-id="d28ba-206">Click Add destination.</span></span>
    * <span data-ttu-id="d28ba-207">Legg til programtabeller som nødvendige mål som krever oppdateringer for å arkivere detaljene i rapporterte Intrastat-transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="d28ba-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="d28ba-208">I Navn-feltet skriver du inn "Arkiv".</span><span class="sxs-lookup"><span data-stu-id="d28ba-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="d28ba-209">Arkiver</span><span class="sxs-lookup"><span data-stu-id="d28ba-209">Archive</span></span>  
32. <span data-ttu-id="d28ba-210">Skriv inn "IntrastatArchiveGeneral" i Tabellnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="d28ba-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="d28ba-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="d28ba-212">Behold posthandlingen "Sett inn" slik at du kan legge til poster i løpet av den detaljerte arkiveringen av hver Intrastat-rapportering prosessen.</span><span class="sxs-lookup"><span data-stu-id="d28ba-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="d28ba-213">Velg Ja i feltet Postinfologg.</span><span class="sxs-lookup"><span data-stu-id="d28ba-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="d28ba-214">Velg Ja hvis du vil ha informasjon om problemer med oppdateringen av programdata.</span><span class="sxs-lookup"><span data-stu-id="d28ba-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="d28ba-215">Velg Ja i feltet Hopp over validering av posthandling.</span><span class="sxs-lookup"><span data-stu-id="d28ba-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="d28ba-216">Velg Ja hvis du vil skjule valideringsfeil om det tomme feltet "ID for Intrastat-arkiv".</span><span class="sxs-lookup"><span data-stu-id="d28ba-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="d28ba-217">Dette vil bli gjort når poster legges til, basert på sekvens nummerserie innstillingene som er konfigurert for denne tabellen i parameterskjemaet Utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="d28ba-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="d28ba-218">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d28ba-218">Click OK.</span></span>
    * <span data-ttu-id="d28ba-219">Bind elementene for de tillagte datakildene (filtrerte modell basert på valgte rotelementet) med elementer fra det nye målet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="d28ba-220">Utvid "Arkiv" i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="d28ba-221">Utvid "Arkiv\<Relasjoner" i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="d28ba-222">Utvid "Arkiv\<Relasjoner\IntrastatArchiveDetail" i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="d28ba-223">I treet velger du "Arkiv\<Relasjoner\Intrastat\ArchiveDetail\Amount(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="d28ba-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="d28ba-224">Utvid 'modell\Arkivhode\Opplistede linjer' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="d28ba-225">Utvid 'modell\Arkivhode\Opplistede linjer\Verdi' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="d28ba-226">Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Beløp' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="d28ba-227">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-227">Click Bind.</span></span>
44. <span data-ttu-id="d28ba-228">Velg 'arkiv\<Relasjoner\IntrastatArchiveDetail\Commodity(IntrastatCommodity)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="d28ba-229">Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Artikkelpost-ID' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="d28ba-230">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-230">Click Bind.</span></span>
47. <span data-ttu-id="d28ba-231">I treet velger du "Arkiv\<Relasjoner\IntrastatArchiveDetail\Item number(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="d28ba-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="d28ba-232">Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Varenummer' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="d28ba-233">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-233">Click Bind.</span></span>
50. <span data-ttu-id="d28ba-234">I treet velger du "Arkiv\<Relasjoner\IntrastatArchiveDetail\Line number(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="d28ba-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="d28ba-235">Velg 'modell\Arkivhode\Opplistede linjer\Nummer' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="d28ba-236">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-236">Click Bind.</span></span>
53. <span data-ttu-id="d28ba-237">Velg "Arkiv\<Relasjoner\Intrastat\ArchiveDetail" i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="d28ba-238">Velg 'modell\Arkivhode\Opplistede linjer' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="d28ba-239">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-239">Click Bind.</span></span>
56. <span data-ttu-id="d28ba-240">Velg 'Arkiv\Filnavn(FileName)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="d28ba-241">Velg 'modell\Arkivhode\Filnavn' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="d28ba-242">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-242">Click Bind.</span></span>
59. <span data-ttu-id="d28ba-243">Velg 'Arkiv\Antall linjer(NumberOfLines)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="d28ba-244">Velg 'modell\Arkivhode\Antall linjer' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="d28ba-245">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-245">Click Bind.</span></span>
62. <span data-ttu-id="d28ba-246">Velg 'Arkiv' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="d28ba-247">Velg 'modell\Arkivhode' i treet.</span><span class="sxs-lookup"><span data-stu-id="d28ba-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="d28ba-248">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d28ba-248">Click Bind.</span></span>
65. <span data-ttu-id="d28ba-249">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d28ba-249">Click Save.</span></span>
66. <span data-ttu-id="d28ba-250">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d28ba-250">Close the page.</span></span>
67. <span data-ttu-id="d28ba-251">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d28ba-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]