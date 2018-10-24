--- 
title: ER Laste opp en konfigurasjon til Lifecycle Services
description: "De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en ny formatkonfigurasjon for elektronisk rapportering (ER) og laste den opp til Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="02dd7-103">ER Laste opp en konfigurasjon til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="02dd7-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02dd7-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en ny formatkonfigurasjon for elektronisk rapportering (ER) og laste den opp til Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="02dd7-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="02dd7-105">I dette eksemplet skal du opprette en konfigurasjon og laste den opp til LCS for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="02dd7-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="02dd7-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="02dd7-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="02dd7-107">Tilgang til LCS kreves også for fullføring av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="02dd7-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="02dd7-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="02dd7-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="02dd7-109">Velg Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="02dd7-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="02dd7-110">og angi som aktiv.</span><span class="sxs-lookup"><span data-stu-id="02dd7-110">and set it as active.</span></span>
3. <span data-ttu-id="02dd7-111">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="02dd7-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="02dd7-112">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="02dd7-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="02dd7-113">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="02dd7-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="02dd7-114">Du vil opprette en konfigurasjon som inneholder en eksempeldatamodell for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="02dd7-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="02dd7-115">Denne datamodellkonfigurasjonen lastes inn i LCS senere.</span><span class="sxs-lookup"><span data-stu-id="02dd7-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="02dd7-116">Skriv inn Eksempelmodellkonfigurasjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="02dd7-117">Eksempelmodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="02dd7-117">Sample model configuration</span></span>  
3. <span data-ttu-id="02dd7-118">Skriv inn Eksempelmodellkonfigurasjon i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="02dd7-119">Eksempelmodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="02dd7-119">Sample model configuration</span></span>  
4. <span data-ttu-id="02dd7-120">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="02dd7-120">Click Create configuration.</span></span>
5. <span data-ttu-id="02dd7-121">Velg Modellutforming.</span><span class="sxs-lookup"><span data-stu-id="02dd7-121">Click Model designer.</span></span>
6. <span data-ttu-id="02dd7-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="02dd7-122">Click New.</span></span>
7. <span data-ttu-id="02dd7-123">Skriv inn Inngangspunkt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="02dd7-124">Inngangspunkt</span><span class="sxs-lookup"><span data-stu-id="02dd7-124">Entry point</span></span>  
8. <span data-ttu-id="02dd7-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="02dd7-125">Click Add.</span></span>
9. <span data-ttu-id="02dd7-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="02dd7-126">Click Save.</span></span>
10. <span data-ttu-id="02dd7-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="02dd7-127">Close the page.</span></span>
11. <span data-ttu-id="02dd7-128">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="02dd7-128">Click Change status.</span></span>
12. <span data-ttu-id="02dd7-129">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="02dd7-129">Click Complete.</span></span>
13. <span data-ttu-id="02dd7-130">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="02dd7-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="02dd7-131">Registrere et nytt repositorium</span><span class="sxs-lookup"><span data-stu-id="02dd7-131">Register a new  repository</span></span>
1. <span data-ttu-id="02dd7-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="02dd7-132">Close the page.</span></span>
2. <span data-ttu-id="02dd7-133">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="02dd7-133">Click Repositories.</span></span>
    * <span data-ttu-id="02dd7-134">Denne lar deg åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="02dd7-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="02dd7-135">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="02dd7-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="02dd7-136">Dette lar deg legge til et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="02dd7-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="02dd7-137">Velg LCS i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="02dd7-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="02dd7-138">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="02dd7-138">Click Create repository.</span></span>
6. <span data-ttu-id="02dd7-139">Angi eller velg en verdi i feltet Prosjekt.</span><span class="sxs-lookup"><span data-stu-id="02dd7-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="02dd7-140">Velg ønsket LCS-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="02dd7-140">Select the desired LCS project.</span></span> <span data-ttu-id="02dd7-141">Du må ha tilgang til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="02dd7-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="02dd7-142">Click OK.</span></span>
    * <span data-ttu-id="02dd7-143">Fullfør en ny oppføring i repositoriet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="02dd7-144">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="02dd7-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="02dd7-145">Velg LCS-repositoriumposten.</span><span class="sxs-lookup"><span data-stu-id="02dd7-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="02dd7-146">Legg merke til at et registrert repositorium er merket med gjeldende leverandør, som betyr at bare konfigurasjoner som eies av denne leverandøren kan settes til dette repositoriet og derfor lastes opp til det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="02dd7-147">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="02dd7-147">Click Open.</span></span>
    * <span data-ttu-id="02dd7-148">Åpne repositoriet for å vise listen over ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="02dd7-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="02dd7-149">Den er tom hvis prosjektet ennå ikke er brukt for deling av ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="02dd7-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="02dd7-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="02dd7-150">Close the page.</span></span>
11. <span data-ttu-id="02dd7-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="02dd7-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="02dd7-152">Laste opp konfigurasjon til LCS</span><span class="sxs-lookup"><span data-stu-id="02dd7-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="02dd7-153">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="02dd7-153">Click Configurations.</span></span>
2. <span data-ttu-id="02dd7-154">Velg Eksempelmodellkonfigurasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="02dd7-155">Velg en opprettet konfigurasjon som allerede er fullført.</span><span class="sxs-lookup"><span data-stu-id="02dd7-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="02dd7-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="02dd7-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="02dd7-157">Velg versjonen av den valgte konfigurasjonen med statusen Fullført.</span><span class="sxs-lookup"><span data-stu-id="02dd7-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="02dd7-158">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="02dd7-158">Click Change status.</span></span>
5. <span data-ttu-id="02dd7-159">Klikk Del.</span><span class="sxs-lookup"><span data-stu-id="02dd7-159">Click Share.</span></span>
    * <span data-ttu-id="02dd7-160">Konfigurasjonsstatusen endres fra Fullført til Delt når den er publisert i LCS.</span><span class="sxs-lookup"><span data-stu-id="02dd7-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="02dd7-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="02dd7-161">Click OK.</span></span>
7. <span data-ttu-id="02dd7-162">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="02dd7-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="02dd7-163">Velg konfigurasjonsversjonen med statusen Delt.</span><span class="sxs-lookup"><span data-stu-id="02dd7-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="02dd7-164">Legg merke til at statusen for den valgte versjonen er endret fra Fullført til Delt.</span><span class="sxs-lookup"><span data-stu-id="02dd7-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="02dd7-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="02dd7-165">Close the page.</span></span>
9. <span data-ttu-id="02dd7-166">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="02dd7-166">Click Repositories.</span></span>
    * <span data-ttu-id="02dd7-167">Denne lar deg åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="02dd7-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="02dd7-168">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="02dd7-168">Click Open.</span></span>
    * <span data-ttu-id="02dd7-169">Velg LCS-repositorium, og åpne det.</span><span class="sxs-lookup"><span data-stu-id="02dd7-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="02dd7-170">Legg merke til at den valgte konfigurasjonen vises som et anleggsmiddel for det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="02dd7-171">Åpne LCS ved hjelp av https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="02dd7-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="02dd7-172">Åpne et prosjekt som ble brukt tidligere for registrering av repositoriet, åpne Aktivabibliotek for dette prosjektet og vis innholdet i aktivatypen Ger-konfigurasjonstypen – den opplastede ER-konfigurasjonen vil være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02dd7-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="02dd7-173">Legg merke til at den opplastede LCS-konfigurasjonen kan importeres til en annen forekomst av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition hvis leverandører har tilgang til dette LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  


