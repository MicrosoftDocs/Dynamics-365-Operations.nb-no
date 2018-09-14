--- 
title: Opprette en Kanban-regel for salgshendelse
description: "Denne prosedyren fokuserer på oppsettet for å opprette en kanban-regel utløses under salgsordreopprettelse."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="ffa3e-103">Opprette en Kanban-regel for salgshendelse</span><span class="sxs-lookup"><span data-stu-id="ffa3e-103">Create a sales event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffa3e-104">Denne prosedyren fokuserer på oppsettet for å opprette en kanban-regel utløses under salgsordreopprettelse.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="ffa3e-105">Kanban-regelen for hendelse etterfyller behov som stammer fra salgsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="ffa3e-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ffa3e-107">Den er ment for prosessingeniøren eller verdistrømlederen når de klargjør produksjon av et nytt eller endret produkt.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ffa3e-108">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ffa3e-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="ffa3e-109">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ffa3e-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-110">Click New.</span></span>
3. <span data-ttu-id="ffa3e-111">Velg Hendelse i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="ffa3e-112">Hvis du velger Hendelse betyr det at kanban-regelen blir utløst av en hendelse, for eksempel oppretting av en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="ffa3e-113">Dette brukes for områder der hver kanban skal dekke et bestemt behov.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="ffa3e-114">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ffa3e-115">Velg Endelig sammenstilling.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="ffa3e-116">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-116">Expand the Details section.</span></span>
6. <span data-ttu-id="ffa3e-117">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ffa3e-118">Velg L0050.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="ffa3e-119">Definere en hendelse</span><span class="sxs-lookup"><span data-stu-id="ffa3e-119">Define an event</span></span>
1. <span data-ttu-id="ffa3e-120">Utvid delen Hendelser.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-120">Expand the Events section.</span></span>
2. <span data-ttu-id="ffa3e-121">Velg Automatisk i feltet Salgshendelse.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="ffa3e-122">Når du velger salgshendelsen Automatisk, utløses denne kanban-regelen automatisk når en salgslinje samsvarer med produkt- og mottakslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="ffa3e-123">I denne fremgangsmåten er det produkt L0050 på lager 13.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="ffa3e-124">Sett Minimumsantall for hendelse til 50.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="ffa3e-125">Med et minimumsantall for hendelse på 50 utløses kanban-regelen bare av hendelser med et antall på 50 eller flere.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="ffa3e-126">Utvid delen Produksjonsflyt.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="ffa3e-127">Legg merke til at mottaksplasseringen er lager 13.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="ffa3e-128">Dette betyr at denne kanban-regelen utløses for denne lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="ffa3e-129">I dette eksemplet vil en salgslinje for produktet L0050, med et antall på 50 eller mer, på lager 13, utløse denne kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="ffa3e-130">Opprette salgslinje for å utløse Kanban-regel for hendelse</span><span class="sxs-lookup"><span data-stu-id="ffa3e-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="ffa3e-131">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="ffa3e-132">En advarsel vises når kanban-regelen lagres, noe som betyr at Kanbaner opprettes i sanntid under oppretting av salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="ffa3e-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-133">Click New.</span></span>
3. <span data-ttu-id="ffa3e-134">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="ffa3e-135">Velg for eksempel US-003.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="ffa3e-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-136">Click OK.</span></span>
5. <span data-ttu-id="ffa3e-137">Skriv inn L0050 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="ffa3e-138">Skriv inn 1 i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="ffa3e-139">Velg område 1 fordi lager 13 er i område 1.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="ffa3e-140">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ffa3e-141">Sett Lager til 13.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="ffa3e-142">Sett verdien for Antall til 75.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="ffa3e-143">Angi et antall på 50 eller høyere, for å utløse den opprettede kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="ffa3e-144">Kontroller at kanban er opprettet</span><span class="sxs-lookup"><span data-stu-id="ffa3e-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="ffa3e-145">Klikk Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-145">Click Product and supply.</span></span>
2. <span data-ttu-id="ffa3e-146">Klikk Vis utligningstre.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="ffa3e-147">Legg merke til at en kanban med samme antall som salgslinjen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="ffa3e-148">Du kan også se materialutstedelsene som trengs for å produsere L0050.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="ffa3e-149">Dette er det siste trinnet i prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ffa3e-149">This is the last step in this procedure.</span></span>  


