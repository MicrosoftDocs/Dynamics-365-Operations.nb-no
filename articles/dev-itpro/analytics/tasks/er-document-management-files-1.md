--- 
title: "Klargjøre datamodell for bruk av dokumentbehandlingsfiler i formatutdata"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a768f9705e190b04c4a1e1b1533c0ec03b19e616
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="6e02a-103">Klargjøre datamodell for bruk av dokumentbehandlingsfiler i formatutdata</span><span class="sxs-lookup"><span data-stu-id="6e02a-103">Prepare data model to use Document Management files in format outputs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e02a-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="6e02a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="6e02a-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="6e02a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6e02a-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="6e02a-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="6e02a-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="6e02a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="6e02a-108">Få tilgang til listen over konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="6e02a-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6e02a-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="6e02a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6e02a-110">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="6e02a-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="6e02a-111">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="6e02a-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="6e02a-112">Velg Litware, Inc. som</span><span class="sxs-lookup"><span data-stu-id="6e02a-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="6e02a-113">leverandør.</span><span class="sxs-lookup"><span data-stu-id="6e02a-113">provider.</span></span>
3. <span data-ttu-id="6e02a-114">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="6e02a-114">Click Repositories.</span></span>
    * <span data-ttu-id="6e02a-115">Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.</span><span class="sxs-lookup"><span data-stu-id="6e02a-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="6e02a-116">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6e02a-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="6e02a-117">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="6e02a-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="6e02a-118">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="6e02a-118">Click Create repository.</span></span>
7. <span data-ttu-id="6e02a-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6e02a-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="6e02a-120">Få konfigurasjonene for kundefakturamodell fra Microsoft</span><span class="sxs-lookup"><span data-stu-id="6e02a-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6e02a-121">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="6e02a-121">Click Show filters.</span></span>
2. <span data-ttu-id="6e02a-122">Bruk følgende filtre: Skriv inn en filterverdi for "Operasjonsressurser" i Navn-feltet ved hjelp av filteroperatoren "begynner med". Skriv inn en filterverdi for "" i Beskrivelse-feltet ved hjelp av operatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="6e02a-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="6e02a-123">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="6e02a-123">Click Show filters.</span></span>
4. <span data-ttu-id="6e02a-124">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="6e02a-124">Click Open.</span></span>
5. <span data-ttu-id="6e02a-125">Velg Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="6e02a-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="6e02a-126">Velg modellkonfigurasjonen Kundefakturamodell for å importere den.</span><span class="sxs-lookup"><span data-stu-id="6e02a-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="6e02a-127">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="6e02a-127">Click Import.</span></span>
    * <span data-ttu-id="6e02a-128">Klikk Importer for versjon 1 av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6e02a-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="6e02a-129">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="6e02a-129">Click Yes.</span></span>
8. <span data-ttu-id="6e02a-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6e02a-130">Close the page.</span></span>
9. <span data-ttu-id="6e02a-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6e02a-131">Close the page.</span></span>
10. <span data-ttu-id="6e02a-132">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="6e02a-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="6e02a-133">Velg Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="6e02a-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="6e02a-134">Opprett den avledede modellen for å støtte tilgang til dokumentbehandlingsfilene</span><span class="sxs-lookup"><span data-stu-id="6e02a-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="6e02a-135">Du vil opprette vår egen konfigurasjon for kundefakturamodellen og avlede den fra konfigurasjonen som leveres av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e02a-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="6e02a-136">Du vil bruke denne konfigurasjonen til å implementere tilgang til dokumentbehandlingsfilene, og gjøre dem tilgjengelige for elektroniske dokumenter som du vil opprette basert på denne modellen.</span><span class="sxs-lookup"><span data-stu-id="6e02a-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="6e02a-137">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6e02a-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6e02a-138">I Ny-feltet angir du Avled fra navnet: Kundefakturamodell, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e02a-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="6e02a-139">I Navn-feltet skriver du inn Kundefakturamodell (egendefinert).</span><span class="sxs-lookup"><span data-stu-id="6e02a-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="6e02a-140">Kundefakturamodell (egendefinert)</span><span class="sxs-lookup"><span data-stu-id="6e02a-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="6e02a-141">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="6e02a-141">Click Create configuration.</span></span>


