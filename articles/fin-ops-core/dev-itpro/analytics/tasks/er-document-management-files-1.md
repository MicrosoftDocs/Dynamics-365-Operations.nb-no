---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 1 - Klargjøre datamodell)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det bruker dokumentbehandlingsfiler (vedlegg) i ER-utdata. (Del 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35bffd6d3688a9887fcdaf4edbd89c344cb9b18d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559803"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="5c63d-104">ER Bruke dokumentbehandlingsfiler i formatutdata (del 1 - Klargjøre datamodell)</span><span class="sxs-lookup"><span data-stu-id="5c63d-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c63d-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="5c63d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5c63d-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="5c63d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="5c63d-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="5c63d-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="5c63d-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="5c63d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="5c63d-109">Få tilgang til listen over konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="5c63d-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="5c63d-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5c63d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="5c63d-111">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="5c63d-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="5c63d-112">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="5c63d-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="5c63d-113">Velg Litware, Inc. som</span><span class="sxs-lookup"><span data-stu-id="5c63d-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="5c63d-114">leverandør.</span><span class="sxs-lookup"><span data-stu-id="5c63d-114">provider.</span></span>
3. <span data-ttu-id="5c63d-115">Klikk på Repositorier.</span><span class="sxs-lookup"><span data-stu-id="5c63d-115">Click Repositories.</span></span>

    <span data-ttu-id="5c63d-116">Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.</span><span class="sxs-lookup"><span data-stu-id="5c63d-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="5c63d-117">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5c63d-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="5c63d-118">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="5c63d-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="5c63d-119">Klikk på Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="5c63d-119">Click Create repository.</span></span>
7. <span data-ttu-id="5c63d-120">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5c63d-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="5c63d-121">Få konfigurasjonene for kundefakturamodell fra Microsoft</span><span class="sxs-lookup"><span data-stu-id="5c63d-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="5c63d-122">Klikk på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="5c63d-122">Click Show filters.</span></span>
2. <span data-ttu-id="5c63d-123">Bruk følgende filtre: Skriv inn en filterverdi for "Operasjonsressurser" i Navn-feltet ved hjelp av filteroperatoren "begynner med". Skriv inn en filterverdi for "" i Beskrivelse-feltet ved hjelp av operatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="5c63d-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="5c63d-124">Klikk på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="5c63d-124">Click Show filters.</span></span>
4. <span data-ttu-id="5c63d-125">Klikk på Åpne.</span><span class="sxs-lookup"><span data-stu-id="5c63d-125">Click Open.</span></span>
5. <span data-ttu-id="5c63d-126">Velg Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="5c63d-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="5c63d-127">Velg modellkonfigurasjonen Kundefakturamodell for å importere den.</span><span class="sxs-lookup"><span data-stu-id="5c63d-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="5c63d-128">Klikk på Importer.</span><span class="sxs-lookup"><span data-stu-id="5c63d-128">Click Import.</span></span>

    <span data-ttu-id="5c63d-129">Klikk på Importer for versjon 1 av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="5c63d-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="5c63d-130">Klikk på Ja.</span><span class="sxs-lookup"><span data-stu-id="5c63d-130">Click Yes.</span></span>
8. <span data-ttu-id="5c63d-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c63d-131">Close the page.</span></span>
9. <span data-ttu-id="5c63d-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c63d-132">Close the page.</span></span>
10. <span data-ttu-id="5c63d-133">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="5c63d-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="5c63d-134">Velg Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="5c63d-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="5c63d-135">Opprett den avledede modellen for å støtte tilgang til dokumentbehandlingsfilene</span><span class="sxs-lookup"><span data-stu-id="5c63d-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="5c63d-136">Du vil opprette vår egen konfigurasjon for kundefakturamodellen og avlede den fra konfigurasjonen som leveres av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5c63d-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="5c63d-137">Du vil bruke denne konfigurasjonen til å implementere tilgang til dokumentbehandlingsfilene, og gjøre dem tilgjengelige for elektroniske dokumenter som du vil opprette basert på denne modellen.</span><span class="sxs-lookup"><span data-stu-id="5c63d-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="5c63d-138">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5c63d-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="5c63d-139">I Ny-feltet angir du Avled fra navnet: Kundefakturamodell, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5c63d-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="5c63d-140">I Navn-feltet skriver du inn Kundefakturamodell (egendefinert).</span><span class="sxs-lookup"><span data-stu-id="5c63d-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="5c63d-141">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="5c63d-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]