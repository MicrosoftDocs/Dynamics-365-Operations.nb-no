--- 
title: Administrere konfigurasjoner av modelltilordning for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 473cad588253b0eb42eb927834e186ccfa4c4f1e
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a><span data-ttu-id="f3cb6-103">Administrere konfigurasjoner av modelltilordning for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="f3cb6-103">Manage model mapping configurations for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3cb6-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="f3cb6-105">I denne oppgaveveiledningen skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre denne oppgaveveiledningen, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv."</span><span class="sxs-lookup"><span data-stu-id="f3cb6-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="f3cb6-106">Fordi ER konfigurasjoner deles mellom firmaer, kan du fullføre oppgaveveiledningen ved hjelp av datasettet firmaet velger.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="f3cb6-107">Funksjonaliteten for denne oppgaven håndboken er tilgjengelig hvis du har installert ett av følgende hurtigreparasjoner: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for Dynamics AX-7.0-versjonen eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for Dynamics 365 for Operations-versjonen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="f3cb6-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f3cb6-109">Kontroller at konfigurasjonsleverandøren for eksempelfirmaET "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="f3cb6-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i oppgaveveilednignen "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="f3cb6-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="f3cb6-111">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f3cb6-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="f3cb6-112">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="f3cb6-113">Legg til en ny modellkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-113">Add a new model configuration.</span></span> <span data-ttu-id="f3cb6-114">Navnet må være unikt i konfigurasjonstreet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="f3cb6-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f3cb6-116">Skriv inn Eksempeldatamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="f3cb6-117">Eksempel på datamodell</span><span class="sxs-lookup"><span data-stu-id="f3cb6-117">Sample data model</span></span>  
4. <span data-ttu-id="f3cb6-118">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-118">Click Create configuration.</span></span>
5. <span data-ttu-id="f3cb6-119">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-119">Click Designer.</span></span>
6. <span data-ttu-id="f3cb6-120">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="f3cb6-121">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="f3cb6-122">Rot</span><span class="sxs-lookup"><span data-stu-id="f3cb6-122">Root</span></span>  
8. <span data-ttu-id="f3cb6-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-123">Click Add.</span></span>
9. <span data-ttu-id="f3cb6-124">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="f3cb6-125">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="f3cb6-126">Firma</span><span class="sxs-lookup"><span data-stu-id="f3cb6-126">Company</span></span>  
11. <span data-ttu-id="f3cb6-127">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-127">Click Add.</span></span>
12. <span data-ttu-id="f3cb6-128">I Beskrivelse-feltet angir du teksten, beskrivelsen av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="f3cb6-129">Beskrivelse av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="f3cb6-130">Klikk Rotreferanse.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-130">Click Root reference.</span></span>
14. <span data-ttu-id="f3cb6-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-131">Click OK.</span></span>
15. <span data-ttu-id="f3cb6-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-132">Click Save.</span></span>
16. <span data-ttu-id="f3cb6-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-133">Close the page.</span></span>
17. <span data-ttu-id="f3cb6-134">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-134">Click Change status.</span></span>
18. <span data-ttu-id="f3cb6-135">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-135">Click Complete.</span></span>
19. <span data-ttu-id="f3cb6-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="f3cb6-137">Legg til en ny ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f3cb6-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="f3cb6-138">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f3cb6-139">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="f3cb6-140">Skriv inn Eksempeltilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="f3cb6-141">Eksempeltilordning</span><span class="sxs-lookup"><span data-stu-id="f3cb6-141">Sample mapping</span></span>  
4. <span data-ttu-id="f3cb6-142">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-142">Click Create configuration.</span></span>
5. <span data-ttu-id="f3cb6-143">Utvid seksjonen Forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="f3cb6-144">Legg merke til at gruppen Forutsetninger for implementasjoner er lagt til automatisk.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="f3cb6-145">Gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og merkes som implementering.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="f3cb6-146">Dette betyr at implementeringen av datamodellen, datamodellen for eksempel er lagt til konfigurasjon for tilordning av dette eksemplet tilordning.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="f3cb6-147">Derfor tvinger denne komponenten ER å laste ned konfigurasjonen for tilordning, eksempel på tilordning fra en database ER når konfigurasjonen av modellen, prøve datamodellen, lastes ned.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="f3cb6-148">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-148">Click Designer.</span></span>
    * <span data-ttu-id="f3cb6-149">Merk at konfigurasjonen for opprettede tilordningen inneholder en ny, tom tilordning med samme navn som opprettet konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="f3cb6-150">Vær oppmerksom på at når en konfigurasjon for valgte overordnede inneholder tilordninger av verdimodellen, vil de bli kopiert til en ny konfigurasjon for tilordning.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="f3cb6-151">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-151">Click Designer.</span></span>
8. <span data-ttu-id="f3cb6-152">I treet velger du Dynamics 365 for Operations\Tabell.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="f3cb6-153">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-153">Click Add root.</span></span>
10. <span data-ttu-id="f3cb6-154">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="f3cb6-155">Firma</span><span class="sxs-lookup"><span data-stu-id="f3cb6-155">Company</span></span>  
11. <span data-ttu-id="f3cb6-156">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="f3cb6-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="f3cb6-157">CompanyInfo</span></span>  
12. <span data-ttu-id="f3cb6-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-158">Click OK.</span></span>
13. <span data-ttu-id="f3cb6-159">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="f3cb6-160">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="f3cb6-161">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="f3cb6-162">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-162">Click Bind.</span></span>
17. <span data-ttu-id="f3cb6-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-163">Click Save.</span></span>
18. <span data-ttu-id="f3cb6-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-164">Close the page.</span></span>
19. <span data-ttu-id="f3cb6-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-165">Close the page.</span></span>
20. <span data-ttu-id="f3cb6-166">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="f3cb6-167">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-167">Click User parameters.</span></span>
22. <span data-ttu-id="f3cb6-168">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="f3cb6-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-169">Click OK.</span></span>
24. <span data-ttu-id="f3cb6-170">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-170">Click Edit.</span></span>
25. <span data-ttu-id="f3cb6-171">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="f3cb6-172">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f3cb6-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="f3cb6-173">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="f3cb6-174">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f3cb6-175">I feltet Ny angir du Format basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="f3cb6-176">Skriv inn Eksempelformat i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="f3cb6-177">Eksempelformat</span><span class="sxs-lookup"><span data-stu-id="f3cb6-177">Sample format</span></span>  
5. <span data-ttu-id="f3cb6-178">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-178">Click Create configuration.</span></span>
6. <span data-ttu-id="f3cb6-179">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-179">Click Designer.</span></span>
7. <span data-ttu-id="f3cb6-180">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="f3cb6-181">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="f3cb6-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-182">Click OK.</span></span>
10. <span data-ttu-id="f3cb6-183">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="f3cb6-184">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="f3cb6-185">Velg 'model\Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="f3cb6-186">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-186">Click Bind.</span></span>
14. <span data-ttu-id="f3cb6-187">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-187">Click Save.</span></span>
15. <span data-ttu-id="f3cb6-188">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-188">Close the page.</span></span>
    * <span data-ttu-id="f3cb6-189">Kjør utkastversjonen av formatet som er opprettet for testformål.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="f3cb6-190">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-190">Click Run.</span></span>
    * <span data-ttu-id="f3cb6-191">Klikk Kjør på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="f3cb6-192">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-192">Click OK.</span></span>
    * <span data-ttu-id="f3cb6-193">Gå gjennom utdataene som inneholder navnet på firmaet der brukeren som kjører denne formatkonfigurasjonen er logget på.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="f3cb6-194">Legg merke til at den opprettede tilordningen konfigurasjonen brukes av denne formatkonfigurasjonen fordi bare én tilgjengelig konfigurasjon som inneholder tilordninger av nødvendige modellen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="f3cb6-195">Legg til en alternativ ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f3cb6-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="f3cb6-196">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="f3cb6-197">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f3cb6-198">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="f3cb6-199">Skriv inn Eksempel på tilordning (alternativ) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="f3cb6-200">Eksempel på tilordning (alternativ)</span><span class="sxs-lookup"><span data-stu-id="f3cb6-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="f3cb6-201">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-201">Click Create configuration.</span></span>
6. <span data-ttu-id="f3cb6-202">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-202">Click Designer.</span></span>
7. <span data-ttu-id="f3cb6-203">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-203">Click Designer.</span></span>
8. <span data-ttu-id="f3cb6-204">I treet velger du Dynamics 365 for Operations\Tabell.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="f3cb6-205">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-205">Click Add root.</span></span>
10. <span data-ttu-id="f3cb6-206">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="f3cb6-207">Firma</span><span class="sxs-lookup"><span data-stu-id="f3cb6-207">Company</span></span>  
11. <span data-ttu-id="f3cb6-208">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="f3cb6-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="f3cb6-209">CompanyInfo</span></span>  
12. <span data-ttu-id="f3cb6-210">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-210">Click OK.</span></span>
13. <span data-ttu-id="f3cb6-211">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-211">Click Edit.</span></span>
14. <span data-ttu-id="f3cb6-212">I treet velger du Streng\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="f3cb6-213">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-213">Click Add function.</span></span>
16. <span data-ttu-id="f3cb6-214">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="f3cb6-215">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="f3cb6-216">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="f3cb6-217">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-217">Click Add data source.</span></span>
20. <span data-ttu-id="f3cb6-218">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="f3cb6-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="f3cb6-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="f3cb6-220">Velg 'Company\find()\Company(DataArea)' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="f3cb6-221">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-221">Click Add data source.</span></span>
23. <span data-ttu-id="f3cb6-222">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="f3cb6-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="f3cb6-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="f3cb6-224">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-224">Click Save.</span></span>
25. <span data-ttu-id="f3cb6-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-225">Close the page.</span></span>
26. <span data-ttu-id="f3cb6-226">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-226">Click Save.</span></span>
27. <span data-ttu-id="f3cb6-227">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-227">Close the page.</span></span>
28. <span data-ttu-id="f3cb6-228">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-228">Close the page.</span></span>
29. <span data-ttu-id="f3cb6-229">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="f3cb6-230">Bruk en eksisterende ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f3cb6-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="f3cb6-231">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="f3cb6-232">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-232">Click Run.</span></span>
    * <span data-ttu-id="f3cb6-233">Vær oppmerksom på at valgte utkastversjonen av formatkonfigurasjonen ER ikke kan utføres fordi det er mer enn én konfigurasjon for tilordning til udefinert datamodellen som er valgt som datakilden for glidende ER formatet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="f3cb6-234">Nå vil du definere tilordning av alternativ konfigurasjon som fra hvilken modell tilordningene brukes som datakilder ER formateringen.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="f3cb6-235">Velg 'Sample data model\Sample mapping (alternative)' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="f3cb6-236">Velg Ja i feltet Standard for modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="f3cb6-237">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="f3cb6-238">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-238">Click Run.</span></span>
7. <span data-ttu-id="f3cb6-239">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3cb6-239">Click OK.</span></span>
    * <span data-ttu-id="f3cb6-240">Legg merke til at den standard tilordning konfigurasjonen brukes av denne formatkonfigurasjonen for generering av det elektroniske dokumentet (opprettet utdataene inneholder firmakoden).</span><span class="sxs-lookup"><span data-stu-id="f3cb6-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  


