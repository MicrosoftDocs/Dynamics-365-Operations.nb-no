---
title: ER Laste opp en konfigurasjon til Lifecycle Services
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en ny formatkonfigurasjon for elektronisk rapportering (ER) og laste den opp til Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551119"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="3f88c-103">ER Laste opp en konfigurasjon til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3f88c-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f88c-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en ny formatkonfigurasjon for elektronisk rapportering (ER) og laste den opp til Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3f88c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3f88c-105">I dette eksemplet skal du opprette en konfigurasjon og laste den opp til LCS for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="3f88c-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="3f88c-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="3f88c-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="3f88c-107">Tilgang til LCS kreves også for fullføring av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3f88c-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="3f88c-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="3f88c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3f88c-109">Velg Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3f88c-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="3f88c-110">og angi som aktiv.</span><span class="sxs-lookup"><span data-stu-id="3f88c-110">and set it as active.</span></span>
3. <span data-ttu-id="3f88c-111">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3f88c-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="3f88c-112">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3f88c-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="3f88c-113">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3f88c-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="3f88c-114">Du vil opprette en konfigurasjon som inneholder en eksempeldatamodell for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3f88c-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="3f88c-115">Denne datamodellkonfigurasjonen lastes inn i LCS senere.</span><span class="sxs-lookup"><span data-stu-id="3f88c-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="3f88c-116">Skriv inn Eksempelmodellkonfigurasjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="3f88c-117">Eksempelmodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3f88c-117">Sample model configuration</span></span>  
3. <span data-ttu-id="3f88c-118">Skriv inn Eksempelmodellkonfigurasjon i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="3f88c-119">Eksempelmodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3f88c-119">Sample model configuration</span></span>  
4. <span data-ttu-id="3f88c-120">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3f88c-120">Click Create configuration.</span></span>
5. <span data-ttu-id="3f88c-121">Velg Modellutforming.</span><span class="sxs-lookup"><span data-stu-id="3f88c-121">Click Model designer.</span></span>
6. <span data-ttu-id="3f88c-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3f88c-122">Click New.</span></span>
7. <span data-ttu-id="3f88c-123">Skriv inn Inngangspunkt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="3f88c-124">Inngangspunkt</span><span class="sxs-lookup"><span data-stu-id="3f88c-124">Entry point</span></span>  
8. <span data-ttu-id="3f88c-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="3f88c-125">Click Add.</span></span>
9. <span data-ttu-id="3f88c-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3f88c-126">Click Save.</span></span>
10. <span data-ttu-id="3f88c-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f88c-127">Close the page.</span></span>
11. <span data-ttu-id="3f88c-128">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="3f88c-128">Click Change status.</span></span>
12. <span data-ttu-id="3f88c-129">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="3f88c-129">Click Complete.</span></span>
13. <span data-ttu-id="3f88c-130">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3f88c-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="3f88c-131">Registrere et nytt repositorium</span><span class="sxs-lookup"><span data-stu-id="3f88c-131">Register a new  repository</span></span>
1. <span data-ttu-id="3f88c-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f88c-132">Close the page.</span></span>
2. <span data-ttu-id="3f88c-133">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="3f88c-133">Click Repositories.</span></span>
    * <span data-ttu-id="3f88c-134">Denne lar deg åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3f88c-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="3f88c-135">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="3f88c-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="3f88c-136">Dette lar deg legge til et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="3f88c-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="3f88c-137">Velg LCS i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="3f88c-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="3f88c-138">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="3f88c-138">Click Create repository.</span></span>
6. <span data-ttu-id="3f88c-139">Angi eller velg en verdi i feltet Prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3f88c-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="3f88c-140">Velg ønsket LCS-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3f88c-140">Select the desired LCS project.</span></span> <span data-ttu-id="3f88c-141">Du må ha tilgang til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="3f88c-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3f88c-142">Click OK.</span></span>
    * <span data-ttu-id="3f88c-143">Fullfør en ny oppføring i repositoriet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="3f88c-144">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3f88c-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3f88c-145">Velg LCS-repositoriumposten.</span><span class="sxs-lookup"><span data-stu-id="3f88c-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="3f88c-146">Legg merke til at et registrert repositorium er merket med gjeldende leverandør, som betyr at bare konfigurasjoner som eies av denne leverandøren kan settes til dette repositoriet og derfor lastes opp til det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="3f88c-147">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="3f88c-147">Click Open.</span></span>
    * <span data-ttu-id="3f88c-148">Åpne repositoriet for å vise listen over ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3f88c-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="3f88c-149">Den er tom hvis prosjektet ennå ikke er brukt for deling av ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3f88c-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="3f88c-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f88c-150">Close the page.</span></span>
11. <span data-ttu-id="3f88c-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f88c-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="3f88c-152">Laste opp konfigurasjon til LCS</span><span class="sxs-lookup"><span data-stu-id="3f88c-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="3f88c-153">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3f88c-153">Click Configurations.</span></span>
2. <span data-ttu-id="3f88c-154">Velg Eksempelmodellkonfigurasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="3f88c-155">Velg en opprettet konfigurasjon som allerede er fullført.</span><span class="sxs-lookup"><span data-stu-id="3f88c-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="3f88c-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3f88c-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f88c-157">Velg versjonen av den valgte konfigurasjonen med statusen Fullført.</span><span class="sxs-lookup"><span data-stu-id="3f88c-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="3f88c-158">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="3f88c-158">Click Change status.</span></span>
5. <span data-ttu-id="3f88c-159">Klikk Del.</span><span class="sxs-lookup"><span data-stu-id="3f88c-159">Click Share.</span></span>
    * <span data-ttu-id="3f88c-160">Konfigurasjonsstatusen endres fra Fullført til Delt når den er publisert i LCS.</span><span class="sxs-lookup"><span data-stu-id="3f88c-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="3f88c-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3f88c-161">Click OK.</span></span>
7. <span data-ttu-id="3f88c-162">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3f88c-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f88c-163">Velg konfigurasjonsversjonen med statusen Delt.</span><span class="sxs-lookup"><span data-stu-id="3f88c-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="3f88c-164">Legg merke til at statusen for den valgte versjonen er endret fra Fullført til Delt.</span><span class="sxs-lookup"><span data-stu-id="3f88c-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="3f88c-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f88c-165">Close the page.</span></span>
9. <span data-ttu-id="3f88c-166">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="3f88c-166">Click Repositories.</span></span>
    * <span data-ttu-id="3f88c-167">Denne lar deg åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3f88c-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="3f88c-168">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="3f88c-168">Click Open.</span></span>
    * <span data-ttu-id="3f88c-169">Velg LCS-repositorium, og åpne det.</span><span class="sxs-lookup"><span data-stu-id="3f88c-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="3f88c-170">Legg merke til at den valgte konfigurasjonen vises som et anleggsmiddel for det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="3f88c-171">Åpne LCS ved hjelp av https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="3f88c-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="3f88c-172">Åpne et prosjekt som ble brukt tidligere for registrering av repositoriet, åpne Aktivabibliotek for dette prosjektet og vis innholdet i aktivatypen Ger-konfigurasjonstypen – den opplastede ER-konfigurasjonen vil være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3f88c-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="3f88c-173">Legg merke til at den opplastede LCS-konfigurasjonen kan importeres til en annen forekomst av Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition hvis leverandører har tilgang til dette LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f88c-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  

