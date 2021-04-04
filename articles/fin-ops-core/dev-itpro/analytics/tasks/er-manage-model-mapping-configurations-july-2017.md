---
title: Administrere ER-modelltilordning i separate ER-konfigurasjoner
description: Dette emnet beskriver hvordan du administrerer ER-modelltilordninger (Elektronisk rapportering) i separate ER-konfigurasjoner.
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: fdd6804c33cc153974229c60b64c3bd76426241a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569419"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="d90a8-103">Administrere ER-modelltilordning i separate ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="d90a8-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d90a8-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="d90a8-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="d90a8-105">I denne oppgaveveiledningen skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre denne oppgaveveiledningen, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv."</span><span class="sxs-lookup"><span data-stu-id="d90a8-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="d90a8-106">Fordi ER konfigurasjoner deles mellom firmaer, kan du fullføre oppgaveveiledningen ved hjelp av datasettet firmaet velger.</span><span class="sxs-lookup"><span data-stu-id="d90a8-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="d90a8-107">Funksjonaliteten for denne oppgaveveiledningen er tilgjengelig hvis du har installert én av følgende hurtigreparasjoner: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for Dynamics AX 7.0-versjonen eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for Dynamics 365 for Operations-versjonen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="d90a8-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d90a8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d90a8-109">Kontroller at konfigurasjonsleverandøren for eksempelfirmaET "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d90a8-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="d90a8-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i oppgaveveilednignen "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="d90a8-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="d90a8-111">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="d90a8-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="d90a8-112">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="d90a8-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d90a8-113">Legg til en ny modellkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-113">Add a new model configuration.</span></span> <span data-ttu-id="d90a8-114">Navnet må være unikt i konfigurasjonstreet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="d90a8-115">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d90a8-116">Skriv inn Eksempeldatamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="d90a8-117">Eksempel på datamodell</span><span class="sxs-lookup"><span data-stu-id="d90a8-117">Sample data model</span></span>  
4. <span data-ttu-id="d90a8-118">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-118">Click Create configuration.</span></span>
5. <span data-ttu-id="d90a8-119">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d90a8-119">Click Designer.</span></span>
6. <span data-ttu-id="d90a8-120">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d90a8-121">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="d90a8-122">Rot</span><span class="sxs-lookup"><span data-stu-id="d90a8-122">Root</span></span>  
8. <span data-ttu-id="d90a8-123">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d90a8-123">Click Add.</span></span>
9. <span data-ttu-id="d90a8-124">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="d90a8-125">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="d90a8-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d90a8-126">Firma</span><span class="sxs-lookup"><span data-stu-id="d90a8-126">Company</span></span>  
11. <span data-ttu-id="d90a8-127">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d90a8-127">Click Add.</span></span>
12. <span data-ttu-id="d90a8-128">I Beskrivelse-feltet angir du teksten, beskrivelsen av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="d90a8-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="d90a8-129">Beskrivelse av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="d90a8-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="d90a8-130">Klikk på Rotreferanse.</span><span class="sxs-lookup"><span data-stu-id="d90a8-130">Click Root reference.</span></span>
14. <span data-ttu-id="d90a8-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-131">Click OK.</span></span>
15. <span data-ttu-id="d90a8-132">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d90a8-132">Click Save.</span></span>
16. <span data-ttu-id="d90a8-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-133">Close the page.</span></span>
17. <span data-ttu-id="d90a8-134">Klikk på Endre status.</span><span class="sxs-lookup"><span data-stu-id="d90a8-134">Click Change status.</span></span>
18. <span data-ttu-id="d90a8-135">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="d90a8-135">Click Complete.</span></span>
19. <span data-ttu-id="d90a8-136">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="d90a8-137">Legg til en ny ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="d90a8-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="d90a8-138">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="d90a8-139">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="d90a8-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="d90a8-140">Skriv inn Eksempeltilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="d90a8-141">Eksempeltilordning</span><span class="sxs-lookup"><span data-stu-id="d90a8-141">Sample mapping</span></span>  
4. <span data-ttu-id="d90a8-142">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-142">Click Create configuration.</span></span>
5. <span data-ttu-id="d90a8-143">Utvid seksjonen Forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="d90a8-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="d90a8-144">Gruppen Forutsetninger for implementasjoner er lagt til automatisk.</span><span class="sxs-lookup"><span data-stu-id="d90a8-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="d90a8-145">Gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og merkes som implementering.</span><span class="sxs-lookup"><span data-stu-id="d90a8-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="d90a8-146">Dette betyr at denne modelltilordningskonfigurasjonen for eksempeltilordning betraktes som implementering av datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="d90a8-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="d90a8-147">Derfor tvinger denne komponenten ER å laste ned modelltilordningskonfigurasjon for eksempeltilordning fra et ER-repositorium når modellkonfigurasjonen for eksempeldatamodellen lastes ned.</span><span class="sxs-lookup"><span data-stu-id="d90a8-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="d90a8-148">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d90a8-148">Click Designer.</span></span>
    * <span data-ttu-id="d90a8-149">Den opprettede modelltilordningskonfigurasjonen inneholder en ny, tom tilordning med samme navn som den opprettet konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="d90a8-150">Når en valgt overordnet modellkonfigurasjon inneholder modelltilordninger, vil de bli kopiert til en ny modelltilordningskonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="d90a8-151">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d90a8-151">Click Designer.</span></span>
8. <span data-ttu-id="d90a8-152">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d90a8-153">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="d90a8-153">Click Add root.</span></span>
10. <span data-ttu-id="d90a8-154">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="d90a8-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d90a8-155">Firma</span><span class="sxs-lookup"><span data-stu-id="d90a8-155">Company</span></span>  
11. <span data-ttu-id="d90a8-156">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d90a8-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d90a8-157">CompanyInfo</span></span>  
12. <span data-ttu-id="d90a8-158">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-158">Click OK.</span></span>
13. <span data-ttu-id="d90a8-159">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="d90a8-160">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="d90a8-161">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="d90a8-162">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d90a8-162">Click Bind.</span></span>
17. <span data-ttu-id="d90a8-163">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d90a8-163">Click Save.</span></span>
18. <span data-ttu-id="d90a8-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-164">Close the page.</span></span>
19. <span data-ttu-id="d90a8-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-165">Close the page.</span></span>
20. <span data-ttu-id="d90a8-166">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d90a8-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="d90a8-167">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="d90a8-167">Click User parameters.</span></span>
22. <span data-ttu-id="d90a8-168">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="d90a8-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="d90a8-169">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-169">Click OK.</span></span>
24. <span data-ttu-id="d90a8-170">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d90a8-170">Click Edit.</span></span>
25. <span data-ttu-id="d90a8-171">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="d90a8-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="d90a8-172">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="d90a8-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="d90a8-173">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d90a8-174">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d90a8-175">I feltet Ny angir du Format basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="d90a8-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d90a8-176">Skriv inn Eksempelformat i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="d90a8-177">Eksempelformat</span><span class="sxs-lookup"><span data-stu-id="d90a8-177">Sample format</span></span>  
5. <span data-ttu-id="d90a8-178">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-178">Click Create configuration.</span></span>
6. <span data-ttu-id="d90a8-179">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d90a8-179">Click Designer.</span></span>
7. <span data-ttu-id="d90a8-180">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="d90a8-181">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="d90a8-182">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-182">Click OK.</span></span>
10. <span data-ttu-id="d90a8-183">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="d90a8-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="d90a8-184">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="d90a8-185">Velg 'model\Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="d90a8-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="d90a8-186">Click Bind.</span></span>
14. <span data-ttu-id="d90a8-187">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d90a8-187">Click Save.</span></span>
15. <span data-ttu-id="d90a8-188">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-188">Close the page.</span></span>
    * <span data-ttu-id="d90a8-189">Kjør utkastversjonen av formatet som er opprettet for testformål.</span><span class="sxs-lookup"><span data-stu-id="d90a8-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="d90a8-190">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="d90a8-190">Click Run.</span></span>
    * <span data-ttu-id="d90a8-191">Klikk Kjør på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="d90a8-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="d90a8-192">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-192">Click OK.</span></span>
    * <span data-ttu-id="d90a8-193">Gå gjennom utdataene som inneholder navnet på firmaet der brukeren som kjører denne formatkonfigurasjonen er logget på.</span><span class="sxs-lookup"><span data-stu-id="d90a8-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="d90a8-194">Den opprettede modelltilordningskonfigurasjonen brukes av denne formatkonfigurasjonen fordi det bare er én tilgjengelig konfigurasjon som inneholder nødvendige modelltilordninger.</span><span class="sxs-lookup"><span data-stu-id="d90a8-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="d90a8-195">Legg til alternativ ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="d90a8-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="d90a8-196">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d90a8-197">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d90a8-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d90a8-198">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="d90a8-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d90a8-199">Skriv inn Eksempel på tilordning (alternativ) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="d90a8-200">Eksempel på tilordning (alternativ)</span><span class="sxs-lookup"><span data-stu-id="d90a8-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="d90a8-201">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-201">Click Create configuration.</span></span>
6. <span data-ttu-id="d90a8-202">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d90a8-202">Click Designer.</span></span>
7. <span data-ttu-id="d90a8-203">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="d90a8-203">Click Designer.</span></span>
8. <span data-ttu-id="d90a8-204">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d90a8-205">Klikk på Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="d90a8-205">Click Add root.</span></span>
10. <span data-ttu-id="d90a8-206">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="d90a8-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d90a8-207">Firma</span><span class="sxs-lookup"><span data-stu-id="d90a8-207">Company</span></span>  
11. <span data-ttu-id="d90a8-208">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d90a8-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d90a8-209">CompanyInfo</span></span>  
12. <span data-ttu-id="d90a8-210">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-210">Click OK.</span></span>
13. <span data-ttu-id="d90a8-211">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d90a8-211">Click Edit.</span></span>
14. <span data-ttu-id="d90a8-212">I treet velger du Streng\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="d90a8-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="d90a8-213">Klikk på Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="d90a8-213">Click Add function.</span></span>
16. <span data-ttu-id="d90a8-214">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="d90a8-215">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="d90a8-216">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="d90a8-217">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="d90a8-217">Click Add data source.</span></span>
20. <span data-ttu-id="d90a8-218">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="d90a8-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d90a8-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="d90a8-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="d90a8-220">Velg 'Company\find()\Company(DataArea)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="d90a8-221">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="d90a8-221">Click Add data source.</span></span>
23. <span data-ttu-id="d90a8-222">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="d90a8-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d90a8-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="d90a8-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="d90a8-224">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d90a8-224">Click Save.</span></span>
25. <span data-ttu-id="d90a8-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-225">Close the page.</span></span>
26. <span data-ttu-id="d90a8-226">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d90a8-226">Click Save.</span></span>
27. <span data-ttu-id="d90a8-227">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-227">Close the page.</span></span>
28. <span data-ttu-id="d90a8-228">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d90a8-228">Close the page.</span></span>
29. <span data-ttu-id="d90a8-229">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="d90a8-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="d90a8-230">Bruk en eksisterende ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="d90a8-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="d90a8-231">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="d90a8-232">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="d90a8-232">Click Run.</span></span>
    * <span data-ttu-id="d90a8-233">Den valgte utkastversjonen av ER-formatkonfigurasjonen ikke kan utføres, fordi det er mer enn én tilgjengelig modelltilordningskonfigurasjon for den udefinerte datamodellen som er valgt som datakilden for det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="d90a8-234">Nå skal du definere den alternative modelltilordningskonfigurasjonen som den som modelltilordningene skal brukes fra som datakilder for det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="d90a8-235">Velg 'Sample data model\Sample mapping (alternative)' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="d90a8-236">Velg Ja i feltet Standard for modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="d90a8-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="d90a8-237">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="d90a8-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="d90a8-238">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="d90a8-238">Click Run.</span></span>
7. <span data-ttu-id="d90a8-239">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d90a8-239">Click OK.</span></span>
    * <span data-ttu-id="d90a8-240">Standard modelltilordningskonfigurasjon brukes av denne formatkonfigurasjonen for generering av det elektroniske dokumentet (opprettede utdata inneholder firmakoden).</span><span class="sxs-lookup"><span data-stu-id="d90a8-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]