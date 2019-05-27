---
title: ER Importere en konfigurasjon fra Lifecycle Services
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan importere en ny versjon av etnformatkonfigurasjon for elektronisk rapportering (ER) fra Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551328"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="08f3a-103">ER Importere en konfigurasjon fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="08f3a-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08f3a-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan importere en ny versjon av etnformatkonfigurasjon for elektronisk rapportering (ER) fra Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="08f3a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="08f3a-105">I dette eksemplet skal du velge ønsket versjon av ER-konfigurasjonen og importere den for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="08f3a-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="08f3a-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Laste opp en ER-konfigurasjon til Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="08f3a-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="08f3a-107">Tilgang til LCS kreves også for fullføring av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="08f3a-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="08f3a-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="08f3a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="08f3a-109">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="08f3a-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="08f3a-110">Slette en delt versjon av datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="08f3a-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="08f3a-111">Velg Eksempelmodellkonfigurasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="08f3a-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="08f3a-112">Den første versjonen av en konfigurasjon for eksempeldatamodell er opprettet og publisert på LCS under prosedyren "Laste opp en ER-konfigurasjon til Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="08f3a-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="08f3a-113">I denne fremgangsmåten sletter du denne versjonen av ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="08f3a-114">Denne versjonen av en konfigurasjon for eksempel data vil senere bli importert fra LCS.</span><span class="sxs-lookup"><span data-stu-id="08f3a-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="08f3a-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="08f3a-116">Velg versjonen av denne konfigurasjonen som har statusen Delt.</span><span class="sxs-lookup"><span data-stu-id="08f3a-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="08f3a-117">Denne statusen angir at konfigurasjonen er publisert til LCS.</span><span class="sxs-lookup"><span data-stu-id="08f3a-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="08f3a-118">Klikk Endre status.</span><span class="sxs-lookup"><span data-stu-id="08f3a-118">Click Change status.</span></span>
4. <span data-ttu-id="08f3a-119">Klikk Avslutt.</span><span class="sxs-lookup"><span data-stu-id="08f3a-119">Click Discontinue.</span></span>
    * <span data-ttu-id="08f3a-120">Endre statusen for den valgte versjonen fra Delt til Utgått for å gjøre den tilgjengelig for sletting.</span><span class="sxs-lookup"><span data-stu-id="08f3a-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="08f3a-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="08f3a-121">Click OK.</span></span>
6. <span data-ttu-id="08f3a-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="08f3a-123">Velg versjonen av denne konfigurasjonen som har statusen Utgått.</span><span class="sxs-lookup"><span data-stu-id="08f3a-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="08f3a-124">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="08f3a-124">Click Delete.</span></span>
8. <span data-ttu-id="08f3a-125">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="08f3a-125">Click Yes.</span></span>
    * <span data-ttu-id="08f3a-126">Legg merke til at bare utkastversjon 2 av den valgte datamodellkonfigurasjonen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="08f3a-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="08f3a-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="08f3a-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="08f3a-128">Importere en delt versjon av datamodellkonfigurasjon fra LCS</span><span class="sxs-lookup"><span data-stu-id="08f3a-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="08f3a-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="08f3a-130">Åpne listen over repositorier for Litware, Inc.-</span><span class="sxs-lookup"><span data-stu-id="08f3a-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="08f3a-131">-konfigurasjonsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="08f3a-131">configuration provider.</span></span>  
2. <span data-ttu-id="08f3a-132">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="08f3a-132">Click Repositories.</span></span>
3. <span data-ttu-id="08f3a-133">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="08f3a-133">Click Open.</span></span>
    * <span data-ttu-id="08f3a-134">Velg LCS-repositorium, og åpne det.</span><span class="sxs-lookup"><span data-stu-id="08f3a-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="08f3a-135">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="08f3a-136">Velg den første versjonen av eksempelmodellkonfigurasjonen i versjonslisten.</span><span class="sxs-lookup"><span data-stu-id="08f3a-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="08f3a-137">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="08f3a-137">Click Import.</span></span>
6. <span data-ttu-id="08f3a-138">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="08f3a-138">Click Yes.</span></span>
    * <span data-ttu-id="08f3a-139">Bekreft importen av den valgte versjonen fra LCS.</span><span class="sxs-lookup"><span data-stu-id="08f3a-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="08f3a-140">Legg merke til at Informasjonsmeldingen (over skjemaet) bekrefter fullføring av importen av den valgte versjonen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="08f3a-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="08f3a-141">Close the page.</span></span>
8. <span data-ttu-id="08f3a-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="08f3a-142">Close the page.</span></span>
9. <span data-ttu-id="08f3a-143">Klikk Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="08f3a-143">Click Configurations.</span></span>
10. <span data-ttu-id="08f3a-144">Velg Eksempelmodellkonfigurasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="08f3a-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="08f3a-145">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="08f3a-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="08f3a-146">Velg versjonen av denne konfigurasjonen som har statusen Delt.</span><span class="sxs-lookup"><span data-stu-id="08f3a-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="08f3a-147">Legg merke til at den delte versjon 1 av den valgte datamodellkonfigurasjonen nå også er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="08f3a-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

