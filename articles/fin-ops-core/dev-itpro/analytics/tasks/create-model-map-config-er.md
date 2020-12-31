---
title: Opprette konfigurasjoner av modelltilordning for elektronisk rapportering (ER)
description: Bruk denne fremgangsmåten for å utforme en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruke innebygde ER-funksjoner for effektive aggregerte beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23bc3a525be9f65b7e5100114d02f6b79a286fb5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682075"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="a9e33-103">Opprette konfigurasjoner av modelltilordning for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="a9e33-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9e33-104">Bruk denne fremgangsmåten for å utforme en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruke innebygde ER-funksjoner for effektive aggregerte beregninger.</span><span class="sxs-lookup"><span data-stu-id="a9e33-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="a9e33-105">I denne prosedyren skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a9e33-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="a9e33-106">Denne fremgangsmåten er opprettet for bruk med rollen som Systemansvarlig eller Utvikler av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="a9e33-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="a9e33-107">Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett.</span><span class="sxs-lookup"><span data-stu-id="a9e33-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="a9e33-108">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="a9e33-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="a9e33-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="a9e33-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a9e33-110">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="a9e33-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="a9e33-111">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="a9e33-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="a9e33-112">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a9e33-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a9e33-113">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="a9e33-113">Click Show filters.</span></span>
4. <span data-ttu-id="a9e33-114">Angi filterverdien "Intrastat" i Navn-feltet og bruk filteroperatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="a9e33-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="a9e33-115">Bruk dette filteret hvis du vil finne konfigurasjon av Intrastat-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="a9e33-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="a9e33-116">Denne modellen finnes kanskje allerede i konfigurasjonstreet.</span><span class="sxs-lookup"><span data-stu-id="a9e33-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="a9e33-117">Hvis den finnes, kan du hoppe over neste underoppgave.</span><span class="sxs-lookup"><span data-stu-id="a9e33-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="a9e33-118">Få Intrastat-modellkonfigurasjonen som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="a9e33-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="a9e33-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9e33-119">Close the page.</span></span>
2. <span data-ttu-id="a9e33-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9e33-120">Close the page.</span></span>
3. <span data-ttu-id="a9e33-121">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="a9e33-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="a9e33-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a9e33-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a9e33-123">Velg flisen Microsoft-leverandør.</span><span class="sxs-lookup"><span data-stu-id="a9e33-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="a9e33-124">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="a9e33-124">Click Repositories.</span></span>
    * <span data-ttu-id="a9e33-125">Klikk på Repositorier i Microsoft-leverandørflisen.</span><span class="sxs-lookup"><span data-stu-id="a9e33-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="a9e33-126">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="a9e33-126">Click Show filters.</span></span>
7. <span data-ttu-id="a9e33-127">Angi filterverdien "ressurser" i Typenavn-feltet og bruk filteroperatoren "inneholder".</span><span class="sxs-lookup"><span data-stu-id="a9e33-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="a9e33-128">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="a9e33-128">Click Open.</span></span>
9. <span data-ttu-id="a9e33-129">Velg 'Intrastat-modell' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9e33-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="a9e33-130">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="a9e33-130">Click Import.</span></span>
11. <span data-ttu-id="a9e33-131">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="a9e33-131">Click Yes.</span></span>
    * <span data-ttu-id="a9e33-132">Du har importert ER-modellkonfigurasjonen som inneholder datamodellen som du vil bruke til å undersøke hvordan den nye ER-funksjonen kan brukes.</span><span class="sxs-lookup"><span data-stu-id="a9e33-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="a9e33-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9e33-133">Close the page.</span></span>
13. <span data-ttu-id="a9e33-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9e33-134">Close the page.</span></span>
14. <span data-ttu-id="a9e33-135">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a9e33-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="a9e33-136">Legg til en ny modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a9e33-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="a9e33-137">Velg 'Intrastat-modell' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9e33-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="a9e33-138">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a9e33-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="a9e33-139">I feltet Ny angir du Modelltilordning basert på datamodell Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a9e33-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="a9e33-140">Skriv inn Eksempeltilordning for Intrastat i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9e33-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="a9e33-141">Eksempeltilordning for Intrastat</span><span class="sxs-lookup"><span data-stu-id="a9e33-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="a9e33-142">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a9e33-142">Click Create configuration.</span></span>

