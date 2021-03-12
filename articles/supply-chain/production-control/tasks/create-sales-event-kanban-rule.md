---
title: Opprette en Kanban-regel for salgshendelse
description: Denne prosedyren fokuserer på oppsettet for å opprette en kanban-regel utløses under salgsordreopprettelse.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd8d55619f52fcd1beff7a27ff814b3dc00dd25a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998634"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="8fbb4-103">Opprette en Kanban-regel for salgshendelse</span><span class="sxs-lookup"><span data-stu-id="8fbb4-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fbb4-104">Denne prosedyren fokuserer på oppsettet for å opprette en kanban-regel utløses under salgsordreopprettelse.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="8fbb4-105">Kanban-regelen for hendelse etterfyller behov som stammer fra salgsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="8fbb4-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8fbb4-107">Den er ment for prosessingeniøren eller verdistrømlederen når de klargjør produksjon av et nytt eller endret produkt.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="8fbb4-108">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="8fbb4-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="8fbb4-109">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="8fbb4-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-110">Click New.</span></span>
3. <span data-ttu-id="8fbb4-111">Velg Hendelse i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="8fbb4-112">Hvis du velger Hendelse betyr det at kanban-regelen blir utløst av en hendelse, for eksempel oppretting av en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="8fbb4-113">Dette brukes for områder der hver kanban skal dekke et bestemt behov.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="8fbb4-114">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="8fbb4-115">Velg Endelig sammenstilling.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="8fbb4-116">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-116">Expand the Details section.</span></span>
6. <span data-ttu-id="8fbb4-117">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="8fbb4-118">Velg L0050.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="8fbb4-119">Definere en hendelse</span><span class="sxs-lookup"><span data-stu-id="8fbb4-119">Define an event</span></span>
1. <span data-ttu-id="8fbb4-120">Utvid delen Hendelser.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-120">Expand the Events section.</span></span>
2. <span data-ttu-id="8fbb4-121">Velg Automatisk i feltet Salgshendelse.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="8fbb4-122">Når du velger salgshendelsen Automatisk, utløses denne kanban-regelen automatisk når en salgslinje samsvarer med produkt- og mottakslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="8fbb4-123">I denne fremgangsmåten er det produkt L0050 på lager 13.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="8fbb4-124">Sett Minimumsantall for hendelse til 50.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="8fbb4-125">Med et minimumsantall for hendelse på 50 utløses kanban-regelen bare av hendelser med et antall på 50 eller flere.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="8fbb4-126">Utvid delen Produksjonsflyt.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="8fbb4-127">Legg merke til at mottaksplasseringen er lager 13.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="8fbb4-128">Dette betyr at denne kanban-regelen utløses for denne lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="8fbb4-129">I dette eksemplet vil en salgslinje for produktet L0050, med et antall på 50 eller mer, på lager 13, utløse denne kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="8fbb4-130">Opprette salgslinje for å utløse Kanban-regel for hendelse</span><span class="sxs-lookup"><span data-stu-id="8fbb4-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="8fbb4-131">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="8fbb4-132">En advarsel vises når kanban-regelen lagres, noe som betyr at Kanbaner opprettes i sanntid under oppretting av salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="8fbb4-133">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-133">Click New.</span></span>
3. <span data-ttu-id="8fbb4-134">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="8fbb4-135">Velg for eksempel US-003.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="8fbb4-136">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-136">Click OK.</span></span>
5. <span data-ttu-id="8fbb4-137">Skriv inn L0050 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="8fbb4-138">Skriv inn 1 i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="8fbb4-139">Velg område 1 fordi lager 13 er i område 1.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="8fbb4-140">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8fbb4-141">Sett Lager til 13.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="8fbb4-142">Sett verdien for Antall til 75.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="8fbb4-143">Angi et antall på 50 eller høyere, for å utløse den opprettede kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="8fbb4-144">Kontroller at kanban er opprettet</span><span class="sxs-lookup"><span data-stu-id="8fbb4-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="8fbb4-145">Klikk på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-145">Click Product and supply.</span></span>
2. <span data-ttu-id="8fbb4-146">Klikk på Vis utligningstre.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="8fbb4-147">Legg merke til at en kanban med samme antall som salgslinjen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="8fbb4-148">Du kan også se materialutstedelsene som trengs for å produsere L0050.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="8fbb4-149">Dette er det siste trinnet i prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8fbb4-149">This is the last step in this procedure.</span></span>  

