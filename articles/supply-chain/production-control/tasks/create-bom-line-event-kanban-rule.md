---
title: Opprette en Kanban-regel for hendelse for stykklistelinje
description: Denne oppgaven fokuserer på oppsettet som kreves for å opprette en kanban-regel for hendelse for å sikre forsyning for stykklistelinjer for produksjon i et blandet lean-produksjonsmiljø og klassisk produksjonsmiljø.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a4252548fd030f2a044436ff607da5125d2854
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "337101"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="6a89a-103">Opprette en Kanban-regel for hendelse for stykklistelinje</span><span class="sxs-lookup"><span data-stu-id="6a89a-103">Create a BOM line event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a89a-104">Denne oppgaven fokuserer på oppsettet som kreves for å opprette en kanban-regel for hendelse for å sikre forsyning for stykklistelinjer for produksjon i et blandet lean-produksjonsmiljø og klassisk produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="6a89a-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="6a89a-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="6a89a-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6a89a-106">Denne oppgaven er ment for prosessingeniøren eller verdistrømsbehandling, når de klargjør produksjon av et nytt eller endret produkt.</span><span class="sxs-lookup"><span data-stu-id="6a89a-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="6a89a-107">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="6a89a-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="6a89a-108">Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="6a89a-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="6a89a-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6a89a-109">Click New.</span></span>
3. <span data-ttu-id="6a89a-110">Velg Uttak i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="6a89a-111">Typen Uttak brukes til å opprette Kanbaner for overføring.</span><span class="sxs-lookup"><span data-stu-id="6a89a-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="6a89a-112">Velg Hendelse i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="6a89a-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="6a89a-113">Hendelsesstrategien velges for å opprette overføringen av Kanbaner basert på en hendelse.</span><span class="sxs-lookup"><span data-stu-id="6a89a-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="6a89a-114">Senere i denne aktivitetsveiledningen vil vi utløse den ved å beregne en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="6a89a-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="6a89a-115">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="6a89a-116">Angi eller velg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="6a89a-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="6a89a-117">Denne overføringsaktiviteten har mottakslager (utdata), og lokasjon 12, noe som innebærer at materiale vil bli flyttet til lokasjon 12 i lager 12.</span><span class="sxs-lookup"><span data-stu-id="6a89a-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="6a89a-118">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="6a89a-118">Expand the Details section.</span></span>
7. <span data-ttu-id="6a89a-119">Angi eller velg M0001 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="6a89a-120">Utvid delen Hendelser.</span><span class="sxs-lookup"><span data-stu-id="6a89a-120">Expand the Events section.</span></span>
9. <span data-ttu-id="6a89a-121">Velg Automatisk i hendelsesfeltet Stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="6a89a-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="6a89a-122">Med hendelsesfeltet for stykklistelinje satt til Automatisk, vil en kanban opprettes for å oppfylle materialbehov for stykklistelinjer for produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="6a89a-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="6a89a-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a89a-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="6a89a-124">Opprette og endre en ny produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="6a89a-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="6a89a-125">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="6a89a-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="6a89a-126">Klikk Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="6a89a-126">Click New production order.</span></span>
3. <span data-ttu-id="6a89a-127">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6a89a-128">Angi eller velg L0001.</span><span class="sxs-lookup"><span data-stu-id="6a89a-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="6a89a-129">Vi bruker vare L0001 fordi vare M0001 inngår i stykklisten for vare L0001.</span><span class="sxs-lookup"><span data-stu-id="6a89a-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="6a89a-130">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="6a89a-130">Click Create.</span></span>
5. <span data-ttu-id="6a89a-131">Klikk koblingen i raden for L0001 i listen.</span><span class="sxs-lookup"><span data-stu-id="6a89a-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="6a89a-132">Klikk Stykkliste.</span><span class="sxs-lookup"><span data-stu-id="6a89a-132">Click BOM.</span></span>
7. <span data-ttu-id="6a89a-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6a89a-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6a89a-134">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="6a89a-134">Click Edit.</span></span>
9. <span data-ttu-id="6a89a-135">Velg Tilknyttet forsyning i Linjetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="6a89a-136">Tilknyttet forsyning velges for å utløse forsyningsopprettelsen av en kanban.</span><span class="sxs-lookup"><span data-stu-id="6a89a-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="6a89a-137">Velg Nei i Ressursforbruk-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="6a89a-138">Hvis du fjerner merket for Ressursforbruk, kan vi endre lageret.</span><span class="sxs-lookup"><span data-stu-id="6a89a-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="6a89a-139">Vis delen Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="6a89a-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="6a89a-140">Skriv inn 12 i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="6a89a-141">Lageret er satt til 12, fordi dette er utleveringslager for uttaksaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="6a89a-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="6a89a-142">Skriv inn 12 i Lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="6a89a-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="6a89a-143">Lokasjonen er satt til 12, fordi dette er utleveringslokasjonen for uttaksaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="6a89a-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="6a89a-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a89a-144">Close the page.</span></span>
15. <span data-ttu-id="6a89a-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a89a-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="6a89a-146">Beregne produksjonsordren og vise opprettet kanban</span><span class="sxs-lookup"><span data-stu-id="6a89a-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="6a89a-147">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="6a89a-147">Click Estimate.</span></span>
    * <span data-ttu-id="6a89a-148">Estimering av produksjonsordren utløser oppretting av tilknyttet kanban for å levere M0001.</span><span class="sxs-lookup"><span data-stu-id="6a89a-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="6a89a-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6a89a-149">Click OK.</span></span>
3. <span data-ttu-id="6a89a-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a89a-150">Close the page.</span></span>
4. <span data-ttu-id="6a89a-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a89a-151">Close the page.</span></span>
5. <span data-ttu-id="6a89a-152">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="6a89a-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="6a89a-153">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6a89a-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a89a-154">Velg Kanban-regel for hendelse som ble opprettet for vare M0001.</span><span class="sxs-lookup"><span data-stu-id="6a89a-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="6a89a-155">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="6a89a-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="6a89a-156">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6a89a-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6a89a-157">Legg merke til kanbanen som er opprettet for å levere M0001 for den estimerte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="6a89a-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="6a89a-158">Dette er det siste trinnet!</span><span class="sxs-lookup"><span data-stu-id="6a89a-158">This is the last step!</span></span>  

