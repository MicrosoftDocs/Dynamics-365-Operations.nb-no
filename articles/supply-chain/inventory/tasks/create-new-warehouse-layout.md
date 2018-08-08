---
title: Opprette et nytt lageroppsett
description: "Denne fremgangsmåten viser hvordan du definerer informasjon om lokasjonene i lageret."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 11ad27e68e8eb499b2cf8e477d3dbf51d930b736
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="7ca1d-103">Opprette et nytt lageroppsett</span><span class="sxs-lookup"><span data-stu-id="7ca1d-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ca1d-104">Denne fremgangsmåten viser hvordan du definerer informasjon om lokasjonene i lageret.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="7ca1d-105">Dette gjelder bare for lagrene som er opprettet ved hjelp av "grunnleggende lageraktiviteter" i lagermodulen, ikke for lagre som er opprettet i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="7ca1d-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="7ca1d-107">Angi standard lokasjonskapasitet</span><span class="sxs-lookup"><span data-stu-id="7ca1d-107">Set the default location capacity</span></span>
1. <span data-ttu-id="7ca1d-108">Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="7ca1d-109">Klikk kategorien Lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="7ca1d-110">Angi et nummer i Standardbredde-feltet.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="7ca1d-111">Angi et nummer i Standarddybde-feltet.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="7ca1d-112">Angi et tall i Standardhøyde-feltet.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="7ca1d-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-113">Click Save.</span></span>
7. <span data-ttu-id="7ca1d-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="7ca1d-115">Definer formatet for plasseringsnavn</span><span class="sxs-lookup"><span data-stu-id="7ca1d-115">Define the location name format</span></span>
1. <span data-ttu-id="7ca1d-116">Gå til Lagerstyring > Oppsett > Lageroppdeling > Lagre.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="7ca1d-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-117">Click New.</span></span>
3. <span data-ttu-id="7ca1d-118">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="7ca1d-119">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7ca1d-120">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7ca1d-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="7ca1d-122">Aktiver/deaktiver utvidelsen av delen Lokasjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="7ca1d-123">Alternativene i denne delen definerer standardformatet for lokasjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="7ca1d-124">I vårt eksempel skal vi ta med gangnummer, reolnummer og hyllenummer.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="7ca1d-125">Sett alternativet Inkluder gang til Ja.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="7ca1d-126">Sett alternativet Ta med reol til Ja.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="7ca1d-127">I Format-feltet velger du en verdi for reolen.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="7ca1d-128">For eksempel: -##</span><span class="sxs-lookup"><span data-stu-id="7ca1d-128">For example: -##</span></span>  
11. <span data-ttu-id="7ca1d-129">Sett alternativet Ta med hylle til Ja.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="7ca1d-130">I Format-feltet velger du en verdi for hyllen.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="7ca1d-131">For eksempel: -##</span><span class="sxs-lookup"><span data-stu-id="7ca1d-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="7ca1d-132">Definer lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="7ca1d-132">Define warehouse locations</span></span>
1. <span data-ttu-id="7ca1d-133">Klikk Lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="7ca1d-134">Klikk Lokasjonsveiviser.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="7ca1d-135">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-135">Click Next.</span></span>
4. <span data-ttu-id="7ca1d-136">Fjern merkingen av alternativet Utleveringsporter</span><span class="sxs-lookup"><span data-stu-id="7ca1d-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="7ca1d-137">Fjern merkingen av alternativet Bulklokasjoner</span><span class="sxs-lookup"><span data-stu-id="7ca1d-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="7ca1d-138">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-138">Click Next.</span></span>
7. <span data-ttu-id="7ca1d-139">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-139">Click Next.</span></span>
8. <span data-ttu-id="7ca1d-140">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-140">Click Next.</span></span>
9. <span data-ttu-id="7ca1d-141">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-141">Click Next.</span></span>
10. <span data-ttu-id="7ca1d-142">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-142">Click Next.</span></span>
11. <span data-ttu-id="7ca1d-143">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-143">Click Next.</span></span>
12. <span data-ttu-id="7ca1d-144">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-144">Click Next.</span></span>
    * <span data-ttu-id="7ca1d-145">Legg merke til at de fysiske dimensjonene som vises på denne siden er de du angir i begynnelsen av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="7ca1d-146">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-146">Click Next.</span></span>
14. <span data-ttu-id="7ca1d-147">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-147">Click Finish.</span></span>
15. <span data-ttu-id="7ca1d-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-148">Close the page.</span></span>
16. <span data-ttu-id="7ca1d-149">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="7ca1d-149">Refresh the page.</span></span>

