--- 
title: Opprette en Kanban-regel for hendelse for stykklistelinje
description: "Denne oppgaven fokuserer på oppsettet som kreves for å opprette en kanban-regel for hendelse for å sikre forsyning for stykklistelinjer for produksjon i et blandet lean-produksjonsmiljø og klassisk produksjonsmiljø."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="dd4e3-103">Opprette en Kanban-regel for hendelse for stykklistelinje</span><span class="sxs-lookup"><span data-stu-id="dd4e3-103">Create a BOM line event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd4e3-104">Denne oppgaven fokuserer på oppsettet som kreves for å opprette en kanban-regel for hendelse for å sikre forsyning for stykklistelinjer for produksjon i et blandet lean-produksjonsmiljø og klassisk produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="dd4e3-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="dd4e3-106">Denne oppgaven er ment for prosessingeniøren eller verdistrømsbehandling, når de klargjør produksjon av et nytt eller endret produkt.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="dd4e3-107">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="dd4e3-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="dd4e3-108">Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="dd4e3-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-109">Click New.</span></span>
3. <span data-ttu-id="dd4e3-110">Velg Uttak i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="dd4e3-111">Typen Uttak brukes til å opprette Kanbaner for overføring.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="dd4e3-112">Velg Hendelse i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="dd4e3-113">Hendelsesstrategien velges for å opprette overføringen av Kanbaner basert på en hendelse.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="dd4e3-114">Senere i denne aktivitetsveiledningen vil vi utløse den ved å beregne en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="dd4e3-115">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="dd4e3-116">Angi eller velg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="dd4e3-117">Denne overføringsaktiviteten har mottakslager (utdata), og lokasjon 12, noe som innebærer at materiale vil bli flyttet til lokasjon 12 i lager 12.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="dd4e3-118">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-118">Expand the Details section.</span></span>
7. <span data-ttu-id="dd4e3-119">Angi eller velg M0001 i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="dd4e3-120">Utvid delen Hendelser.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-120">Expand the Events section.</span></span>
9. <span data-ttu-id="dd4e3-121">Velg Automatisk i hendelsesfeltet Stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="dd4e3-122">Med hendelsesfeltet for stykklistelinje satt til Automatisk, vil en kanban opprettes for å oppfylle materialbehov for stykklistelinjer for produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="dd4e3-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="dd4e3-124">Opprette og endre en ny produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="dd4e3-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="dd4e3-125">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="dd4e3-126">Klikk Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-126">Click New production order.</span></span>
3. <span data-ttu-id="dd4e3-127">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="dd4e3-128">Angi eller velg L0001.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="dd4e3-129">Vi bruker vare L0001 fordi vare M0001 inngår i stykklisten for vare L0001.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="dd4e3-130">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-130">Click Create.</span></span>
5. <span data-ttu-id="dd4e3-131">Klikk koblingen i raden for L0001 i listen.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="dd4e3-132">Klikk Stykkliste.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-132">Click BOM.</span></span>
7. <span data-ttu-id="dd4e3-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="dd4e3-134">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-134">Click Edit.</span></span>
9. <span data-ttu-id="dd4e3-135">Velg Tilknyttet forsyning i Linjetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="dd4e3-136">Tilknyttet forsyning velges for å utløse forsyningsopprettelsen av en kanban.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="dd4e3-137">Velg Nei i Ressursforbruk-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="dd4e3-138">Hvis du fjerner merket for Ressursforbruk, kan vi endre lageret.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="dd4e3-139">Vis delen Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="dd4e3-140">Skriv inn 12 i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="dd4e3-141">Lageret er satt til 12, fordi dette er utleveringslager for uttaksaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="dd4e3-142">Skriv inn 12 i Lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="dd4e3-143">Lokasjonen er satt til 12, fordi dette er utleveringslokasjonen for uttaksaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="dd4e3-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-144">Close the page.</span></span>
15. <span data-ttu-id="dd4e3-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="dd4e3-146">Beregne produksjonsordren og vise opprettet kanban</span><span class="sxs-lookup"><span data-stu-id="dd4e3-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="dd4e3-147">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-147">Click Estimate.</span></span>
    * <span data-ttu-id="dd4e3-148">Estimering av produksjonsordren utløser oppretting av tilknyttet kanban for å levere M0001.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="dd4e3-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-149">Click OK.</span></span>
3. <span data-ttu-id="dd4e3-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-150">Close the page.</span></span>
4. <span data-ttu-id="dd4e3-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-151">Close the page.</span></span>
5. <span data-ttu-id="dd4e3-152">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="dd4e3-153">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd4e3-154">Velg Kanban-regel for hendelse som ble opprettet for vare M0001.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="dd4e3-155">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="dd4e3-156">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dd4e3-157">Legg merke til kanbanen som er opprettet for å levere M0001 for den estimerte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="dd4e3-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="dd4e3-158">Dette er det siste trinnet!</span><span class="sxs-lookup"><span data-stu-id="dd4e3-158">This is the last step!</span></span>  


