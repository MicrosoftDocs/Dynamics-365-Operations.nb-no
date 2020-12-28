---
title: Opprette en Kanban-regel ved hjelp av en hendelse for minste beholdning
description: Denne fremgangsmåten fokuserer på oppsettet for å opprette en Kanban-regel som bruker en minste beholdning-hendelse for å sikre at et bestemt produkt alltid er tilgjengelig på em bestemt lokasjon.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434129"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="97bfd-103">Opprette en Kanban-regel ved hjelp av en hendelse for minste beholdning</span><span class="sxs-lookup"><span data-stu-id="97bfd-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97bfd-104">Denne fremgangsmåten fokuserer på oppsettet for å opprette en Kanban-regel som bruker en minste beholdning-hendelse for å sikre at et bestemt produkt alltid er tilgjengelig på em bestemt lokasjon.</span><span class="sxs-lookup"><span data-stu-id="97bfd-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="97bfd-105">Det opprettes en Kanban-regel for å overføre materiale til lokasjonen når lagernivået faller under 200 enheter.</span><span class="sxs-lookup"><span data-stu-id="97bfd-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="97bfd-106">Ved å kjøre Behandling av utligningshendelse, opprettes de nødvendige Kanbanene.</span><span class="sxs-lookup"><span data-stu-id="97bfd-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="97bfd-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="97bfd-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="97bfd-108">Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="97bfd-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="97bfd-109">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="97bfd-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="97bfd-110">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="97bfd-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="97bfd-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="97bfd-111">Click New.</span></span>
3. <span data-ttu-id="97bfd-112">Velg Uttak i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="97bfd-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="97bfd-113">Denne typen brukes til å opprette Kanbaner for overføring.</span><span class="sxs-lookup"><span data-stu-id="97bfd-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="97bfd-114">Velg Hendelse i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="97bfd-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="97bfd-115">Hendelsesstrategien brukes for å opprette overføringen av Kanbaner basert på en hendelse.</span><span class="sxs-lookup"><span data-stu-id="97bfd-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="97bfd-116">Senere i fremgangsmåten utløser du Kanbaner for overføring ved hjelp av lageretterfylling.</span><span class="sxs-lookup"><span data-stu-id="97bfd-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="97bfd-117">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="97bfd-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="97bfd-118">Angi eller velg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="97bfd-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="97bfd-119">Denne overføringsaktiviteten har mottakslager (utdata), og lokasjon 12, noe som innebærer at materialer vil bli flyttet til lokasjon 12 i lager 12.</span><span class="sxs-lookup"><span data-stu-id="97bfd-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="97bfd-120">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="97bfd-120">Expand the Details section.</span></span>
7. <span data-ttu-id="97bfd-121">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="97bfd-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="97bfd-122">Velg M0007.</span><span class="sxs-lookup"><span data-stu-id="97bfd-122">Select M0007.</span></span>  
8. <span data-ttu-id="97bfd-123">Utvid delen Hendelser.</span><span class="sxs-lookup"><span data-stu-id="97bfd-123">Expand the Events section.</span></span>
9. <span data-ttu-id="97bfd-124">Velg Parti i feltet Hendelse for lageretterfylling.</span><span class="sxs-lookup"><span data-stu-id="97bfd-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="97bfd-125">Dette oppretter Kanbaner for å oppfylle materialbehov på den tilknyttede plasseringen under behandling av utligningshendelse.</span><span class="sxs-lookup"><span data-stu-id="97bfd-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="97bfd-126">Sette minimumsantallet for varen</span><span class="sxs-lookup"><span data-stu-id="97bfd-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="97bfd-127">Klikk for å følge koblingen i Produkt-feltet.</span><span class="sxs-lookup"><span data-stu-id="97bfd-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="97bfd-128">Klikk for å følge koblingen i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="97bfd-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="97bfd-129">Vis Produktbilde-faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="97bfd-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="97bfd-130">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="97bfd-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="97bfd-131">Klikk Varedekning.</span><span class="sxs-lookup"><span data-stu-id="97bfd-131">Click Item coverage.</span></span>
6. <span data-ttu-id="97bfd-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="97bfd-132">Click New.</span></span>
7. <span data-ttu-id="97bfd-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="97bfd-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="97bfd-134">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="97bfd-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="97bfd-135">Sett Lager til 12.</span><span class="sxs-lookup"><span data-stu-id="97bfd-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="97bfd-136">Sett Minimum til 200.</span><span class="sxs-lookup"><span data-stu-id="97bfd-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="97bfd-137">Kjøre den satsvise jobben for oppretting av hendelse</span><span class="sxs-lookup"><span data-stu-id="97bfd-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="97bfd-138">Gå til Produksjonskontroll > Periodiske oppgaver > Satsvis behandling av Kanban-jobb > Behandling av utligningshendelse.</span><span class="sxs-lookup"><span data-stu-id="97bfd-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="97bfd-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="97bfd-139">Click OK.</span></span>
3. <span data-ttu-id="97bfd-140">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="97bfd-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="97bfd-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="97bfd-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="97bfd-142">Velg Kanban-regelen som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="97bfd-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="97bfd-143">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="97bfd-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="97bfd-144">Legg merke til at en Kanban ble opprettet for å overføre det nødvendige materialet til lager 12.</span><span class="sxs-lookup"><span data-stu-id="97bfd-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

