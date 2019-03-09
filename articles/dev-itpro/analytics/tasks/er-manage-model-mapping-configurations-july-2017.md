---
title: Administrere ER-modelltilordning i separate ER-konfigurasjoner
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner.
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
ms.openlocfilehash: 24ca4124d190df94e7ca9ac31c2ea757fe9ff242
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "349153"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="7f645-103">Administrere ER-modelltilordning i separate ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="7f645-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f645-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="7f645-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="7f645-105">I denne oppgaveveiledningen skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre denne oppgaveveiledningen, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv."</span><span class="sxs-lookup"><span data-stu-id="7f645-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="7f645-106">Fordi ER konfigurasjoner deles mellom firmaer, kan du fullføre oppgaveveiledningen ved hjelp av datasettet firmaet velger.</span><span class="sxs-lookup"><span data-stu-id="7f645-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="7f645-107">Funksjonaliteten for denne oppgaveveiledningen er tilgjengelig hvis du har installert én av følgende hurtigreparasjoner: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for Dynamics AX 7.0-versjonen eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for Dynamics 365 for Operations-versjonen.</span><span class="sxs-lookup"><span data-stu-id="7f645-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="7f645-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="7f645-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="7f645-109">Kontroller at konfigurasjonsleverandøren for eksempelfirmaET "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="7f645-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="7f645-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i oppgaveveilednignen "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="7f645-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="7f645-111">Legg til en ny ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f645-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="7f645-112">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="7f645-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="7f645-113">Legg til en ny modellkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="7f645-113">Add a new model configuration.</span></span> <span data-ttu-id="7f645-114">Navnet må være unikt i konfigurasjonstreet.</span><span class="sxs-lookup"><span data-stu-id="7f645-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="7f645-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="7f645-116">Skriv inn Eksempeldatamodell i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="7f645-117">Eksempel på datamodell</span><span class="sxs-lookup"><span data-stu-id="7f645-117">Sample data model</span></span>  
4. <span data-ttu-id="7f645-118">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="7f645-118">Click Create configuration.</span></span>
5. <span data-ttu-id="7f645-119">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="7f645-119">Click Designer.</span></span>
6. <span data-ttu-id="7f645-120">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="7f645-121">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="7f645-122">Rot</span><span class="sxs-lookup"><span data-stu-id="7f645-122">Root</span></span>  
8. <span data-ttu-id="7f645-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="7f645-123">Click Add.</span></span>
9. <span data-ttu-id="7f645-124">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="7f645-125">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="7f645-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="7f645-126">Firma</span><span class="sxs-lookup"><span data-stu-id="7f645-126">Company</span></span>  
11. <span data-ttu-id="7f645-127">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="7f645-127">Click Add.</span></span>
12. <span data-ttu-id="7f645-128">I Beskrivelse-feltet angir du teksten, beskrivelsen av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="7f645-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="7f645-129">Beskrivelse av den juridiske enheten eller firmaet der brukeren logget under kjøring.</span><span class="sxs-lookup"><span data-stu-id="7f645-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="7f645-130">Klikk Rotreferanse.</span><span class="sxs-lookup"><span data-stu-id="7f645-130">Click Root reference.</span></span>
14. <span data-ttu-id="7f645-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-131">Click OK.</span></span>
15. <span data-ttu-id="7f645-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f645-132">Click Save.</span></span>
16. <span data-ttu-id="7f645-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-133">Close the page.</span></span>
17. <span data-ttu-id="7f645-134">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="7f645-134">Click Change status.</span></span>
18. <span data-ttu-id="7f645-135">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="7f645-135">Click Complete.</span></span>
19. <span data-ttu-id="7f645-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="7f645-137">Legg til en ny ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f645-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="7f645-138">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="7f645-139">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="7f645-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="7f645-140">Skriv inn Eksempeltilordning i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="7f645-141">Eksempeltilordning</span><span class="sxs-lookup"><span data-stu-id="7f645-141">Sample mapping</span></span>  
4. <span data-ttu-id="7f645-142">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="7f645-142">Click Create configuration.</span></span>
5. <span data-ttu-id="7f645-143">Utvid seksjonen Forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="7f645-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="7f645-144">Legg merke til at gruppen Forutsetninger for implementasjoner er lagt til automatisk.</span><span class="sxs-lookup"><span data-stu-id="7f645-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="7f645-145">Gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og merkes som implementering.</span><span class="sxs-lookup"><span data-stu-id="7f645-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="7f645-146">Dette betyr at implementeringen av datamodellen, datamodellen for eksempel er lagt til konfigurasjon for tilordning av dette eksemplet tilordning.</span><span class="sxs-lookup"><span data-stu-id="7f645-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="7f645-147">Derfor tvinger denne komponenten ER å laste ned konfigurasjonen for tilordning, eksempel på tilordning fra en database ER når konfigurasjonen av modellen, prøve datamodellen, lastes ned.</span><span class="sxs-lookup"><span data-stu-id="7f645-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="7f645-148">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="7f645-148">Click Designer.</span></span>
    * <span data-ttu-id="7f645-149">Merk at konfigurasjonen for opprettede tilordningen inneholder en ny, tom tilordning med samme navn som opprettet konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="7f645-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="7f645-150">Vær oppmerksom på at når en konfigurasjon for valgte overordnede inneholder tilordninger av verdimodellen, vil de bli kopiert til en ny konfigurasjon for tilordning.</span><span class="sxs-lookup"><span data-stu-id="7f645-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="7f645-151">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="7f645-151">Click Designer.</span></span>
8. <span data-ttu-id="7f645-152">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="7f645-153">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="7f645-153">Click Add root.</span></span>
10. <span data-ttu-id="7f645-154">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="7f645-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="7f645-155">Firma</span><span class="sxs-lookup"><span data-stu-id="7f645-155">Company</span></span>  
11. <span data-ttu-id="7f645-156">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="7f645-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="7f645-157">CompanyInfo</span></span>  
12. <span data-ttu-id="7f645-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-158">Click OK.</span></span>
13. <span data-ttu-id="7f645-159">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="7f645-160">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="7f645-161">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="7f645-162">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="7f645-162">Click Bind.</span></span>
17. <span data-ttu-id="7f645-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f645-163">Click Save.</span></span>
18. <span data-ttu-id="7f645-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-164">Close the page.</span></span>
19. <span data-ttu-id="7f645-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-165">Close the page.</span></span>
20. <span data-ttu-id="7f645-166">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7f645-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="7f645-167">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="7f645-167">Click User parameters.</span></span>
22. <span data-ttu-id="7f645-168">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="7f645-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="7f645-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-169">Click OK.</span></span>
24. <span data-ttu-id="7f645-170">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="7f645-170">Click Edit.</span></span>
25. <span data-ttu-id="7f645-171">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="7f645-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="7f645-172">Legg til en ny ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f645-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="7f645-173">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="7f645-174">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="7f645-175">I feltet Ny angir du Format basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="7f645-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="7f645-176">Skriv inn Eksempelformat i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="7f645-177">Eksempelformat</span><span class="sxs-lookup"><span data-stu-id="7f645-177">Sample format</span></span>  
5. <span data-ttu-id="7f645-178">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="7f645-178">Click Create configuration.</span></span>
6. <span data-ttu-id="7f645-179">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="7f645-179">Click Designer.</span></span>
7. <span data-ttu-id="7f645-180">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="7f645-181">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="7f645-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-182">Click OK.</span></span>
10. <span data-ttu-id="7f645-183">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="7f645-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="7f645-184">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="7f645-185">Velg 'model\Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="7f645-186">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="7f645-186">Click Bind.</span></span>
14. <span data-ttu-id="7f645-187">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f645-187">Click Save.</span></span>
15. <span data-ttu-id="7f645-188">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-188">Close the page.</span></span>
    * <span data-ttu-id="7f645-189">Kjør utkastversjonen av formatet som er opprettet for testformål.</span><span class="sxs-lookup"><span data-stu-id="7f645-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="7f645-190">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="7f645-190">Click Run.</span></span>
    * <span data-ttu-id="7f645-191">Klikk Kjør på hurtigfanen Versjoner.</span><span class="sxs-lookup"><span data-stu-id="7f645-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="7f645-192">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-192">Click OK.</span></span>
    * <span data-ttu-id="7f645-193">Gå gjennom utdataene som inneholder navnet på firmaet der brukeren som kjører denne formatkonfigurasjonen er logget på.</span><span class="sxs-lookup"><span data-stu-id="7f645-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="7f645-194">Legg merke til at den opprettede tilordningen konfigurasjonen brukes av denne formatkonfigurasjonen fordi bare én tilgjengelig konfigurasjon som inneholder tilordninger av nødvendige modellen.</span><span class="sxs-lookup"><span data-stu-id="7f645-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="7f645-195">Legg til en alternativ ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f645-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="7f645-196">Velg 'Sample data model' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="7f645-197">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="7f645-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="7f645-198">I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.</span><span class="sxs-lookup"><span data-stu-id="7f645-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="7f645-199">Skriv inn Eksempel på tilordning (alternativ) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="7f645-200">Eksempel på tilordning (alternativ)</span><span class="sxs-lookup"><span data-stu-id="7f645-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="7f645-201">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="7f645-201">Click Create configuration.</span></span>
6. <span data-ttu-id="7f645-202">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="7f645-202">Click Designer.</span></span>
7. <span data-ttu-id="7f645-203">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="7f645-203">Click Designer.</span></span>
8. <span data-ttu-id="7f645-204">Velg Dynamics 365 for Operations\Tabell i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="7f645-205">Klikk Legg til rot.</span><span class="sxs-lookup"><span data-stu-id="7f645-205">Click Add root.</span></span>
10. <span data-ttu-id="7f645-206">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="7f645-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="7f645-207">Firma</span><span class="sxs-lookup"><span data-stu-id="7f645-207">Company</span></span>  
11. <span data-ttu-id="7f645-208">Skriv inn CompanyInfo i Tabell-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f645-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="7f645-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="7f645-209">CompanyInfo</span></span>  
12. <span data-ttu-id="7f645-210">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-210">Click OK.</span></span>
13. <span data-ttu-id="7f645-211">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="7f645-211">Click Edit.</span></span>
14. <span data-ttu-id="7f645-212">I treet velger du Streng\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="7f645-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="7f645-213">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="7f645-213">Click Add function.</span></span>
16. <span data-ttu-id="7f645-214">Utvid 'Company' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="7f645-215">Utvid 'Company\find()' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="7f645-216">Velg 'Company\find()\Name' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="7f645-217">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="7f645-217">Click Add data source.</span></span>
20. <span data-ttu-id="7f645-218">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="7f645-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="7f645-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="7f645-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="7f645-220">Velg 'Company\find()\Company(DataArea)' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="7f645-221">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="7f645-221">Click Add data source.</span></span>
23. <span data-ttu-id="7f645-222">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="7f645-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="7f645-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="7f645-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="7f645-224">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f645-224">Click Save.</span></span>
25. <span data-ttu-id="7f645-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-225">Close the page.</span></span>
26. <span data-ttu-id="7f645-226">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f645-226">Click Save.</span></span>
27. <span data-ttu-id="7f645-227">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-227">Close the page.</span></span>
28. <span data-ttu-id="7f645-228">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f645-228">Close the page.</span></span>
29. <span data-ttu-id="7f645-229">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="7f645-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="7f645-230">Bruk en eksisterende ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="7f645-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="7f645-231">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="7f645-232">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="7f645-232">Click Run.</span></span>
    * <span data-ttu-id="7f645-233">Vær oppmerksom på at valgte utkastversjonen av formatkonfigurasjonen ER ikke kan utføres fordi det er mer enn én konfigurasjon for tilordning til udefinert datamodellen som er valgt som datakilden for glidende ER formatet.</span><span class="sxs-lookup"><span data-stu-id="7f645-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="7f645-234">Nå vil du definere tilordning av alternativ konfigurasjon som fra hvilken modell tilordningene brukes som datakilder ER formateringen.</span><span class="sxs-lookup"><span data-stu-id="7f645-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="7f645-235">Velg 'Sample data model\Sample mapping (alternative)' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="7f645-236">Velg Ja i feltet Standard for modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="7f645-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="7f645-237">Velg 'Sample data model\Sample format' i treet.</span><span class="sxs-lookup"><span data-stu-id="7f645-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="7f645-238">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="7f645-238">Click Run.</span></span>
7. <span data-ttu-id="7f645-239">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f645-239">Click OK.</span></span>
    * <span data-ttu-id="7f645-240">Legg merke til at den standard tilordning konfigurasjonen brukes av denne formatkonfigurasjonen for generering av det elektroniske dokumentet (opprettet utdataene inneholder firmakoden).</span><span class="sxs-lookup"><span data-stu-id="7f645-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

