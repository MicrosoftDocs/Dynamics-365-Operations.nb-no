---
title: Opprette et nytt lageroppsett
description: Denne fremgangsmåten viser hvordan du definerer informasjon om lokasjonene i lageret.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845528"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="d1ab4-103">Opprette et nytt lageroppsett</span><span class="sxs-lookup"><span data-stu-id="d1ab4-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1ab4-104">Denne fremgangsmåten viser hvordan du definerer informasjon om lokasjonene i lageret.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="d1ab4-105">Dette gjelder bare for lagrene som er opprettet ved hjelp av "grunnleggende lageraktiviteter" i lagermodulen, ikke for lagre som er opprettet i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="d1ab4-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="d1ab4-107">Angi standard lokasjonskapasitet</span><span class="sxs-lookup"><span data-stu-id="d1ab4-107">Set the default location capacity</span></span>
1. <span data-ttu-id="d1ab4-108">Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="d1ab4-109">Klikk kategorien Lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="d1ab4-110">Angi et nummer i Standardbredde-feltet.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="d1ab4-111">Angi et nummer i Standarddybde-feltet.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="d1ab4-112">Angi et tall i Standardhøyde-feltet.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="d1ab4-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-113">Click Save.</span></span>
7. <span data-ttu-id="d1ab4-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="d1ab4-115">Definer formatet for plasseringsnavn</span><span class="sxs-lookup"><span data-stu-id="d1ab4-115">Define the location name format</span></span>
1. <span data-ttu-id="d1ab4-116">Gå til Lagerstyring > Oppsett > Lageroppdeling > Lagre.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="d1ab4-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-117">Click New.</span></span>
3. <span data-ttu-id="d1ab4-118">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="d1ab4-119">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d1ab4-120">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d1ab4-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d1ab4-122">Aktiver/deaktiver utvidelsen av delen Lokasjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="d1ab4-123">Alternativene i denne delen definerer standardformatet for lokasjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="d1ab4-124">I vårt eksempel skal vi ta med gangnummer, reolnummer og hyllenummer.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="d1ab4-125">Sett alternativet Inkluder gang til Ja.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="d1ab4-126">Sett alternativet Ta med reol til Ja.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="d1ab4-127">I Format-feltet velger du en verdi for reolen.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="d1ab4-128">For eksempel: -##</span><span class="sxs-lookup"><span data-stu-id="d1ab4-128">For example: -##</span></span>  
11. <span data-ttu-id="d1ab4-129">Sett alternativet Ta med hylle til Ja.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="d1ab4-130">I Format-feltet velger du en verdi for hyllen.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="d1ab4-131">For eksempel: -##</span><span class="sxs-lookup"><span data-stu-id="d1ab4-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="d1ab4-132">Definer lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="d1ab4-132">Define warehouse locations</span></span>
1. <span data-ttu-id="d1ab4-133">Klikk Lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="d1ab4-134">Klikk Lokasjonsveiviser.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="d1ab4-135">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-135">Click Next.</span></span>
4. <span data-ttu-id="d1ab4-136">Fjern merkingen av alternativet Utleveringsporter</span><span class="sxs-lookup"><span data-stu-id="d1ab4-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="d1ab4-137">Fjern merkingen av alternativet Bulklokasjoner</span><span class="sxs-lookup"><span data-stu-id="d1ab4-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="d1ab4-138">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-138">Click Next.</span></span>
7. <span data-ttu-id="d1ab4-139">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-139">Click Next.</span></span>
8. <span data-ttu-id="d1ab4-140">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-140">Click Next.</span></span>
9. <span data-ttu-id="d1ab4-141">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-141">Click Next.</span></span>
10. <span data-ttu-id="d1ab4-142">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-142">Click Next.</span></span>
11. <span data-ttu-id="d1ab4-143">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-143">Click Next.</span></span>
12. <span data-ttu-id="d1ab4-144">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-144">Click Next.</span></span>
    * <span data-ttu-id="d1ab4-145">Legg merke til at de fysiske dimensjonene som vises på denne siden er de du angir i begynnelsen av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="d1ab4-146">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-146">Click Next.</span></span>
14. <span data-ttu-id="d1ab4-147">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-147">Click Finish.</span></span>
15. <span data-ttu-id="d1ab4-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-148">Close the page.</span></span>
16. <span data-ttu-id="d1ab4-149">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="d1ab4-149">Refresh the page.</span></span>

