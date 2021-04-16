---
title: Administrere ER-modelltilordning i separate ER-konfigurasjoner
description: Dette emnet beskriver hvordan du administrerer ER-modelltilordninger (Elektronisk rapportering) i separate ER-konfigurasjoner.
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
ms.openlocfilehash: 0370074766e92802164d96daee4204836b7f17c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751516"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="cfccc-103">Administrere ER-modelltilordning i separate ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="cfccc-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfccc-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="cfccc-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="cfccc-105">I denne oppgaveveiledningen skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre denne oppgaveveiledningen, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv."</span><span class="sxs-lookup"><span data-stu-id="cfccc-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="cfccc-106">Fordi ER konfigurasjoner deles mellom firmaer, kan du fullføre oppgaveveiledningen ved hjelp av datasettet firmaet velger.</span><span class="sxs-lookup"><span data-stu-id="cfccc-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="cfccc-107">Funksjonaliteten for denne oppgaveveiledningen er tilgjengelig hvis du har installert én av følgende hurtigreparasjoner: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for Dynamics AX 7.0-versjonen eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for Dynamics 365 for Operations-versjonen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="cfccc-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="cfccc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="cfccc-109">Kontroller at konfigurasjonsleverandøren for eksempelfirmaET "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="cfccc-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="cfccc-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i oppgaveveilednignen "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="cfccc-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="cfccc-111">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cfccc-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="cfccc-112">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="cfccc-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="cfccc-113">Legg til en ny modellkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-113">Add a new model configuration.</span></span> <span data-ttu-id="cfccc-114">Navnet må være unikt i konfigurasjonstreet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="cfccc-115">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="cfccc-116">Skriv inn Eksempeldatamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="cfccc-117">Eksempel på datamodell</span><span class="sxs-lookup"><span data-stu-id="cfccc-117">Sample data model</span></span>  
4. <span data-ttu-id="cfccc-118">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-118">Click Create configuration.</span></span>
5. <span data-ttu-id="cfccc-119">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="cfccc-119">Click Designer.</span></span>
6. <span data-ttu-id="cfccc-120">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="cfccc-121">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="cfccc-122">Rot</span><span class="sxs-lookup"><span data-stu-id="cfccc-122">Root</span></span>  
8. <span data-ttu-id="cfccc-123">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="cfccc-123">Click Add.</span></span>
9. <span data-ttu-id="cfccc-124">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="cfccc-125">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="cfccc-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="cfccc-126">Firma</span><span class="sxs-lookup"><span data-stu-id="cfccc-126">Company</span></span>  
11. <span data-ttu-id="cfccc-127">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="cfccc-127">Click Add.</span></span>
12. <span data-ttu-id="cfccc-128">I Beskrivelse-feltet angir du teksten, beskrivelsen av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="cfccc-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="cfccc-129">Beskrivelse av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="cfccc-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="cfccc-130">Klikk på Rotreferanse.</span><span class="sxs-lookup"><span data-stu-id="cfccc-130">Click Root reference.</span></span>
14. <span data-ttu-id="cfccc-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-131">Click OK.</span></span>
15. <span data-ttu-id="cfccc-132">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cfccc-132">Click Save.</span></span>
16. <span data-ttu-id="cfccc-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-133">Close the page.</span></span>
17. <span data-ttu-id="cfccc-134">Klikk på Endre status.</span><span class="sxs-lookup"><span data-stu-id="cfccc-134">Click Change status.</span></span>
18. <span data-ttu-id="cfccc-135">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="cfccc-135">Click Complete.</span></span>
19. <span data-ttu-id="cfccc-136">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="cfccc-137">Legg til en ny ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cfccc-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="cfccc-138">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="cfccc-139">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="cfccc-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="cfccc-140">Skriv inn Eksempeltilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="cfccc-141">Eksempeltilordning</span><span class="sxs-lookup"><span data-stu-id="cfccc-141">Sample mapping</span></span>  
4. <span data-ttu-id="cfccc-142">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-142">Click Create configuration.</span></span>
5. <span data-ttu-id="cfccc-143">Utvid seksjonen Forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="cfccc-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="cfccc-144">Gruppen Forutsetninger for implementasjoner er lagt til automatisk.</span><span class="sxs-lookup"><span data-stu-id="cfccc-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="cfccc-145">Gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og merkes som implementering.</span><span class="sxs-lookup"><span data-stu-id="cfccc-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="cfccc-146">Dette betyr at denne modelltilordningskonfigurasjonen for eksempeltilordning betraktes som implementering av datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="cfccc-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="cfccc-147">Derfor tvinger denne komponenten ER å laste ned modelltilordningskonfigurasjon for eksempeltilordning fra et ER-repositorium når modellkonfigurasjonen for eksempeldatamodellen lastes ned.</span><span class="sxs-lookup"><span data-stu-id="cfccc-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="cfccc-148">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="cfccc-148">Click Designer.</span></span>
    * <span data-ttu-id="cfccc-149">Den opprettede modelltilordningskonfigurasjonen inneholder en ny, tom tilordning med samme navn som den opprettet konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="cfccc-150">Når en valgt overordnet modellkonfigurasjon inneholder modelltilordninger, vil de bli kopiert til en ny modelltilordningskonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="cfccc-151">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="cfccc-151">Click Designer.</span></span>
8. <span data-ttu-id="cfccc-152">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="cfccc-153">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="cfccc-153">Click Add root.</span></span>
10. <span data-ttu-id="cfccc-154">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="cfccc-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="cfccc-155">Firma</span><span class="sxs-lookup"><span data-stu-id="cfccc-155">Company</span></span>  
11. <span data-ttu-id="cfccc-156">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="cfccc-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="cfccc-157">CompanyInfo</span></span>  
12. <span data-ttu-id="cfccc-158">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-158">Click OK.</span></span>
13. <span data-ttu-id="cfccc-159">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="cfccc-160">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="cfccc-161">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="cfccc-162">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="cfccc-162">Click Bind.</span></span>
17. <span data-ttu-id="cfccc-163">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cfccc-163">Click Save.</span></span>
18. <span data-ttu-id="cfccc-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-164">Close the page.</span></span>
19. <span data-ttu-id="cfccc-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-165">Close the page.</span></span>
20. <span data-ttu-id="cfccc-166">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cfccc-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="cfccc-167">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="cfccc-167">Click User parameters.</span></span>
22. <span data-ttu-id="cfccc-168">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="cfccc-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="cfccc-169">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-169">Click OK.</span></span>
24. <span data-ttu-id="cfccc-170">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cfccc-170">Click Edit.</span></span>
25. <span data-ttu-id="cfccc-171">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="cfccc-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="cfccc-172">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cfccc-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="cfccc-173">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="cfccc-174">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="cfccc-175">I feltet Ny angir du Format basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="cfccc-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="cfccc-176">Skriv inn Eksempelformat i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="cfccc-177">Eksempelformat</span><span class="sxs-lookup"><span data-stu-id="cfccc-177">Sample format</span></span>  
5. <span data-ttu-id="cfccc-178">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-178">Click Create configuration.</span></span>
6. <span data-ttu-id="cfccc-179">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="cfccc-179">Click Designer.</span></span>
7. <span data-ttu-id="cfccc-180">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="cfccc-181">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="cfccc-182">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-182">Click OK.</span></span>
10. <span data-ttu-id="cfccc-183">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="cfccc-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="cfccc-184">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="cfccc-185">Velg 'model\Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="cfccc-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="cfccc-186">Click Bind.</span></span>
14. <span data-ttu-id="cfccc-187">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cfccc-187">Click Save.</span></span>
15. <span data-ttu-id="cfccc-188">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-188">Close the page.</span></span>
    * <span data-ttu-id="cfccc-189">Kjør utkastversjonen av formatet som er opprettet for testformål.</span><span class="sxs-lookup"><span data-stu-id="cfccc-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="cfccc-190">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="cfccc-190">Click Run.</span></span>
    * <span data-ttu-id="cfccc-191">Klikk Kjør på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="cfccc-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="cfccc-192">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-192">Click OK.</span></span>
    * <span data-ttu-id="cfccc-193">Gå gjennom utdataene som inneholder navnet på firmaet der brukeren som kjører denne formatkonfigurasjonen er logget på.</span><span class="sxs-lookup"><span data-stu-id="cfccc-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="cfccc-194">Den opprettede modelltilordningskonfigurasjonen brukes av denne formatkonfigurasjonen fordi det bare er én tilgjengelig konfigurasjon som inneholder nødvendige modelltilordninger.</span><span class="sxs-lookup"><span data-stu-id="cfccc-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="cfccc-195">Legg til alternativ ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cfccc-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="cfccc-196">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="cfccc-197">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="cfccc-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="cfccc-198">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="cfccc-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="cfccc-199">Skriv inn Eksempel på tilordning (alternativ) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="cfccc-200">Eksempel på tilordning (alternativ)</span><span class="sxs-lookup"><span data-stu-id="cfccc-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="cfccc-201">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-201">Click Create configuration.</span></span>
6. <span data-ttu-id="cfccc-202">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="cfccc-202">Click Designer.</span></span>
7. <span data-ttu-id="cfccc-203">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="cfccc-203">Click Designer.</span></span>
8. <span data-ttu-id="cfccc-204">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="cfccc-205">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="cfccc-205">Click Add root.</span></span>
10. <span data-ttu-id="cfccc-206">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="cfccc-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="cfccc-207">Firma</span><span class="sxs-lookup"><span data-stu-id="cfccc-207">Company</span></span>  
11. <span data-ttu-id="cfccc-208">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="cfccc-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="cfccc-209">CompanyInfo</span></span>  
12. <span data-ttu-id="cfccc-210">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-210">Click OK.</span></span>
13. <span data-ttu-id="cfccc-211">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cfccc-211">Click Edit.</span></span>
14. <span data-ttu-id="cfccc-212">I treet velger du Streng\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="cfccc-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="cfccc-213">Klikk på Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="cfccc-213">Click Add function.</span></span>
16. <span data-ttu-id="cfccc-214">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="cfccc-215">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="cfccc-216">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="cfccc-217">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="cfccc-217">Click Add data source.</span></span>
20. <span data-ttu-id="cfccc-218">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cfccc-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="cfccc-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="cfccc-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="cfccc-220">Velg 'Company\find()\Company(DataArea)' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="cfccc-221">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="cfccc-221">Click Add data source.</span></span>
23. <span data-ttu-id="cfccc-222">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cfccc-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="cfccc-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="cfccc-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="cfccc-224">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cfccc-224">Click Save.</span></span>
25. <span data-ttu-id="cfccc-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-225">Close the page.</span></span>
26. <span data-ttu-id="cfccc-226">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="cfccc-226">Click Save.</span></span>
27. <span data-ttu-id="cfccc-227">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-227">Close the page.</span></span>
28. <span data-ttu-id="cfccc-228">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cfccc-228">Close the page.</span></span>
29. <span data-ttu-id="cfccc-229">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="cfccc-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="cfccc-230">Bruk en eksisterende ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="cfccc-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="cfccc-231">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="cfccc-232">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="cfccc-232">Click Run.</span></span>
    * <span data-ttu-id="cfccc-233">Den valgte utkastversjonen av ER-formatkonfigurasjonen ikke kan utføres, fordi det er mer enn én tilgjengelig modelltilordningskonfigurasjon for den udefinerte datamodellen som er valgt som datakilden for det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="cfccc-234">Nå skal du definere den alternative modelltilordningskonfigurasjonen som den som modelltilordningene skal brukes fra som datakilder for det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="cfccc-235">Velg 'Sample data model\Sample mapping (alternative)' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="cfccc-236">Velg Ja i feltet Standard for modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="cfccc-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="cfccc-237">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="cfccc-238">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="cfccc-238">Click Run.</span></span>
7. <span data-ttu-id="cfccc-239">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="cfccc-239">Click OK.</span></span>
    * <span data-ttu-id="cfccc-240">Standard modelltilordningskonfigurasjon brukes av denne formatkonfigurasjonen for generering av det elektroniske dokumentet (opprettede utdata inneholder firmakoden).</span><span class="sxs-lookup"><span data-stu-id="cfccc-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]