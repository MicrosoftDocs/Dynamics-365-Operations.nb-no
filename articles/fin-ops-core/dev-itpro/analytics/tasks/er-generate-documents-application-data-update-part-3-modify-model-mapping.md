---
title: Endre modeller og tilordninger for å generere dokumenter med programdata
description: 'For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 2: generere dokumenter)".'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4546de2c5c1773aadce0ec084ee7058ff2ae153
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141885"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="ff609-103">Endre modeller og tilordninger for å generere dokumenter med programdata</span><span class="sxs-lookup"><span data-stu-id="ff609-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff609-104">For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 2: generere dokumenter)".</span><span class="sxs-lookup"><span data-stu-id="ff609-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="ff609-105">Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="ff609-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="ff609-106">I denne fremgangsmåten skal du endre ER-konfigurasjonene for å begynne med å bruke dem til å generere elektroniske dokumenter og oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="ff609-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="ff609-107">Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler.</span><span class="sxs-lookup"><span data-stu-id="ff609-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="ff609-108">Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="ff609-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="ff609-109">Endre datamodell</span><span class="sxs-lookup"><span data-stu-id="ff609-109">Modify data model</span></span>
1. <span data-ttu-id="ff609-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="ff609-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ff609-111">Velg 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="ff609-112">Du vil utvide hvordan du bruker datamodellen.</span><span class="sxs-lookup"><span data-stu-id="ff609-112">You will extend how you use the data model.</span></span> <span data-ttu-id="ff609-113">I tillegg til å bruke den som datakilde for å generere Intrastat-rapporten, brukes datamodellen til å samle inn informasjon om Intrastat-rapportering av prosessen.</span><span class="sxs-lookup"><span data-stu-id="ff609-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="ff609-114">Detaljene vil deretter brukes til å oppdatere applikasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="ff609-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="ff609-115">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="ff609-115">Click Designer.</span></span>
4. <span data-ttu-id="ff609-116">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="ff609-117">I feltet Ny node som en for angir du Modellrot.</span><span class="sxs-lookup"><span data-stu-id="ff609-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="ff609-118">Skriv inn "For oppdatering av programdata" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="ff609-119">For oppdatering av programdata</span><span class="sxs-lookup"><span data-stu-id="ff609-119">For application data update</span></span>  
7. <span data-ttu-id="ff609-120">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-120">Click Add.</span></span>
8. <span data-ttu-id="ff609-121">Velg "For oppdatering av programdata" i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="ff609-122">Denne nye rotelementet legges til å angi dataflyten for å flytte data fra rapporten Intrastat (brukes som en datakilde) til applikasjonen tabellene (oppdatering målet).</span><span class="sxs-lookup"><span data-stu-id="ff609-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="ff609-123">Roten for ulike varer må tilordnes automatisk for å hente data som er postert til det utgående dokumentet og henter data fra dokumentet som brukes til å oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="ff609-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="ff609-124">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="ff609-125">Skriv inn "Arkivhode" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="ff609-126">Arkivhode</span><span class="sxs-lookup"><span data-stu-id="ff609-126">Archive header</span></span>  
11. <span data-ttu-id="ff609-127">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="ff609-128">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-128">Click Add.</span></span>
    * <span data-ttu-id="ff609-129">Siden du vil opprette en post for hver Intrastat-rapport som genereres, må du opprette en ny vare for den.</span><span class="sxs-lookup"><span data-stu-id="ff609-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="ff609-130">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="ff609-131">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="ff609-132">Filnavn</span><span class="sxs-lookup"><span data-stu-id="ff609-132">File name</span></span>  
15. <span data-ttu-id="ff609-133">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="ff609-134">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-134">Click Add.</span></span>
17. <span data-ttu-id="ff609-135">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="ff609-136">Skriv inn "Antall linjer" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="ff609-137">Antall linjer</span><span class="sxs-lookup"><span data-stu-id="ff609-137">Number of lines</span></span>  
19. <span data-ttu-id="ff609-138">Velg "Heltall" i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="ff609-139">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-139">Click Add.</span></span>
    * <span data-ttu-id="ff609-140">Legg til denne varen for å angi antallet Intrastat-transaksjoner som er rapportert under gjeldende rapporteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ff609-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="ff609-141">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="ff609-142">Skriv inn "Arkivlinjer" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="ff609-143">Arkivlinjer</span><span class="sxs-lookup"><span data-stu-id="ff609-143">Archive lines</span></span>  
23. <span data-ttu-id="ff609-144">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="ff609-145">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-145">Click Add.</span></span>
    * <span data-ttu-id="ff609-146">Legg til denne varen for å representere listen over Intrastat-transaksjoner som er rapportert under gjeldende rapporteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ff609-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="ff609-147">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="ff609-148">I Navn-feltet skriver du inn Beløp.</span><span class="sxs-lookup"><span data-stu-id="ff609-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="ff609-149">Beløp</span><span class="sxs-lookup"><span data-stu-id="ff609-149">Amount</span></span>  
27. <span data-ttu-id="ff609-150">Velg Faktisk i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="ff609-151">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-151">Click Add.</span></span>
29. <span data-ttu-id="ff609-152">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="ff609-153">Skriv inn "Artikkelpost-ID" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="ff609-154">Artikkelpost-ID</span><span class="sxs-lookup"><span data-stu-id="ff609-154">Commodity rec id</span></span>  
31. <span data-ttu-id="ff609-155">Velg Int64 i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="ff609-156">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-156">Click Add.</span></span>
33. <span data-ttu-id="ff609-157">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="ff609-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="ff609-158">I Navn-feltet skriver du inn Varenummer.</span><span class="sxs-lookup"><span data-stu-id="ff609-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="ff609-159">Varenummer</span><span class="sxs-lookup"><span data-stu-id="ff609-159">Item number</span></span>  
35. <span data-ttu-id="ff609-160">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="ff609-161">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-161">Click Add.</span></span>
37. <span data-ttu-id="ff609-162">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff609-162">Click Save.</span></span>
38. <span data-ttu-id="ff609-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff609-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="ff609-164">Endre modelltilordning</span><span class="sxs-lookup"><span data-stu-id="ff609-164">Modify model mapping</span></span>
1. <span data-ttu-id="ff609-165">Utvid 'Intrastat (modell)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="ff609-166">Velg 'Intrastat (modell)\Intrastat (tilordning)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="ff609-167">Endre den eksisterende modell tilordningen til å bruke den for oppdateringen av programdata og for å arkivere Intrastat-rapportering detaljer.</span><span class="sxs-lookup"><span data-stu-id="ff609-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="ff609-168">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="ff609-168">Click Designer.</span></span>
4. <span data-ttu-id="ff609-169">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ff609-169">Click New.</span></span>
5. <span data-ttu-id="ff609-170">Skriv inn "Oppdater arkiv" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="ff609-171">Oppdater arkiv</span><span class="sxs-lookup"><span data-stu-id="ff609-171">Update archive</span></span>  
6. <span data-ttu-id="ff609-172">Velg "Til mål" i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="ff609-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="ff609-173">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff609-173">Click Save.</span></span>
    * <span data-ttu-id="ff609-174">Denne nye tilordningen angir dataflyt for flytting av data (rapportere Intrastat-detaljer) fra datamodellen til programmet tabellene (oppdatering målet).</span><span class="sxs-lookup"><span data-stu-id="ff609-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="ff609-175">Legg merke til at ulike modeller roten varer må brukes til å hente data fra programmet for rapporteringsprosessen og deretter bruke dataene fra datamodellen for oppdateringen av programdata.</span><span class="sxs-lookup"><span data-stu-id="ff609-175">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="ff609-176">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="ff609-176">Click Designer.</span></span>
9. <span data-ttu-id="ff609-177">Velg 'Datamodell\Datamodell' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="ff609-178">Legg til den obligatoriske datakilden.</span><span class="sxs-lookup"><span data-stu-id="ff609-178">Add the required data source.</span></span> <span data-ttu-id="ff609-179">Dette er datamodellen som inneholder detaljer om de rapporterte Intrastat-transaksjonene som må være arkivert.</span><span class="sxs-lookup"><span data-stu-id="ff609-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="ff609-180">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="ff609-180">Click Add root.</span></span>
11. <span data-ttu-id="ff609-181">I Navn-feltet skriver du inn "modell".</span><span class="sxs-lookup"><span data-stu-id="ff609-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="ff609-182">modell</span><span class="sxs-lookup"><span data-stu-id="ff609-182">model</span></span>  
12. <span data-ttu-id="ff609-183">I feltet Definisjon, angir eller velger du verdien "For oppdatering av programdata".</span><span class="sxs-lookup"><span data-stu-id="ff609-183">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="ff609-184">For oppdatering av programdata</span><span class="sxs-lookup"><span data-stu-id="ff609-184">For application data update</span></span>  
13. <span data-ttu-id="ff609-185">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ff609-185">Click OK.</span></span>
14. <span data-ttu-id="ff609-186">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="ff609-187">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="ff609-188">Velg 'modell\Arkivhode' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="ff609-189">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ff609-189">Click Add.</span></span>
    * <span data-ttu-id="ff609-190">Hvis du vil nummerere rapporterte Intrastat-transaksjoner for arkivering, må den riktige datakilden legges til.</span><span class="sxs-lookup"><span data-stu-id="ff609-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="ff609-191">Skriv inn "Opplistede linjer" i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="ff609-192">Opplistede linjer</span><span class="sxs-lookup"><span data-stu-id="ff609-192">Enumerated lines</span></span>  
19. <span data-ttu-id="ff609-193">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="ff609-193">Click Edit formula.</span></span>
20. <span data-ttu-id="ff609-194">Velg 'List\ENUMERATE' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="ff609-195">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="ff609-195">Click Add function.</span></span>
22. <span data-ttu-id="ff609-196">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="ff609-197">Utvide 'modell\Arkivhode' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="ff609-198">Velg 'modell\Arkivhode\Arkivlinjer'.</span><span class="sxs-lookup"><span data-stu-id="ff609-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="ff609-199">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="ff609-199">Click Add data source.</span></span>
26. <span data-ttu-id="ff609-200">I Formel-feltet angir du 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span><span class="sxs-lookup"><span data-stu-id="ff609-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="ff609-201">ENUMERATE(model.'Arkivhode'.'Arkivlinjer')</span><span class="sxs-lookup"><span data-stu-id="ff609-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="ff609-202">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff609-202">Click Save.</span></span>
28. <span data-ttu-id="ff609-203">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff609-203">Close the page.</span></span>
29. <span data-ttu-id="ff609-204">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ff609-204">Click OK.</span></span>
30. <span data-ttu-id="ff609-205">Klikk Legg til mål.</span><span class="sxs-lookup"><span data-stu-id="ff609-205">Click Add destination.</span></span>
    * <span data-ttu-id="ff609-206">Legg til programtabeller som nødvendige mål som krever oppdateringer for å arkivere detaljene i rapporterte Intrastat-transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ff609-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="ff609-207">I Navn-feltet skriver du inn "Arkiv".</span><span class="sxs-lookup"><span data-stu-id="ff609-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="ff609-208">Arkiver</span><span class="sxs-lookup"><span data-stu-id="ff609-208">Archive</span></span>  
32. <span data-ttu-id="ff609-209">Skriv inn "IntrastatArchiveGeneral" i Tabellnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff609-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="ff609-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="ff609-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="ff609-211">Behold posthandlingen "Sett inn" slik at du kan legge til poster i løpet av den detaljerte arkiveringen av hver Intrastat-rapportering prosessen.</span><span class="sxs-lookup"><span data-stu-id="ff609-211">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="ff609-212">Velg Ja i feltet Postinfologg.</span><span class="sxs-lookup"><span data-stu-id="ff609-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="ff609-213">Velg Ja hvis du vil ha informasjon om problemer med oppdateringen av programdata.</span><span class="sxs-lookup"><span data-stu-id="ff609-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="ff609-214">Velg Ja i feltet Hopp over validering av posthandling.</span><span class="sxs-lookup"><span data-stu-id="ff609-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="ff609-215">Velg Ja hvis du vil skjule valideringsfeil om det tomme feltet "ID for Intrastat-arkiv".</span><span class="sxs-lookup"><span data-stu-id="ff609-215">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="ff609-216">Dette vil bli gjort når poster legges til, basert på sekvens nummerserie innstillingene som er konfigurert for denne tabellen i parameterskjemaet Utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="ff609-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="ff609-217">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ff609-217">Click OK.</span></span>
    * <span data-ttu-id="ff609-218">Bind elementene for de tillagte datakildene (filtrerte modell basert på valgte rotelementet) med elementer fra det nye målet.</span><span class="sxs-lookup"><span data-stu-id="ff609-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="ff609-219">Utvid "Arkiv" i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="ff609-220">Utvid "Arkiv\<Relasjoner" i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="ff609-221">Utvid "Arkiv\<Relasjoner\IntrastatArchiveDetail" i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="ff609-222">I treet velger du "Arkiv\<Relasjoner\Intrastat\ArchiveDetail\Amount(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="ff609-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="ff609-223">Utvid 'modell\Arkivhode\Opplistede linjer' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="ff609-224">Utvid 'modell\Arkivhode\Opplistede linjer\Verdi' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="ff609-225">Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Beløp' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="ff609-226">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-226">Click Bind.</span></span>
44. <span data-ttu-id="ff609-227">Velg 'arkiv\<Relasjoner\IntrastatArchiveDetail\Commodity(IntrastatCommodity)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="ff609-228">Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Artikkelpost-ID' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="ff609-229">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-229">Click Bind.</span></span>
47. <span data-ttu-id="ff609-230">I treet velger du "Arkiv\<Relasjoner\IntrastatArchiveDetail\Item number(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="ff609-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="ff609-231">Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Varenummer' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="ff609-232">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-232">Click Bind.</span></span>
50. <span data-ttu-id="ff609-233">I treet velger du "Arkiv\<Relasjoner\IntrastatArchiveDetail\Line number(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="ff609-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="ff609-234">Velg 'modell\Arkivhode\Opplistede linjer\Nummer' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="ff609-235">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-235">Click Bind.</span></span>
53. <span data-ttu-id="ff609-236">Velg "Arkiv\<Relasjoner\Intrastat\ArchiveDetail" i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="ff609-237">Velg 'modell\Arkivhode\Opplistede linjer' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="ff609-238">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-238">Click Bind.</span></span>
56. <span data-ttu-id="ff609-239">Velg 'Arkiv\Filnavn(FileName)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="ff609-240">Velg 'modell\Arkivhode\Filnavn' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="ff609-241">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-241">Click Bind.</span></span>
59. <span data-ttu-id="ff609-242">Velg 'Arkiv\Antall linjer(NumberOfLines)' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="ff609-243">Velg 'modell\Arkivhode\Antall linjer' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="ff609-244">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-244">Click Bind.</span></span>
62. <span data-ttu-id="ff609-245">Velg 'Arkiv' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="ff609-246">Velg 'modell\Arkivhode' i treet.</span><span class="sxs-lookup"><span data-stu-id="ff609-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="ff609-247">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="ff609-247">Click Bind.</span></span>
65. <span data-ttu-id="ff609-248">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff609-248">Click Save.</span></span>
66. <span data-ttu-id="ff609-249">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff609-249">Close the page.</span></span>
67. <span data-ttu-id="ff609-250">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff609-250">Close the page.</span></span>

