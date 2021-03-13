---
title: Opprette en Kanban-regel for uttak
description: Denne fremgangsmåten viser oppsettet som kreves for å opprette en kanban-regel for uttak for overføring av materialer i en lean-miljø.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1694472e20c28a0b0f94c1ced8544b7258c22b40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007097"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="ec0a0-103">Opprette en Kanban-regel for uttak</span><span class="sxs-lookup"><span data-stu-id="ec0a0-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec0a0-104">Denne fremgangsmåten viser oppsettet som kreves for å opprette en kanban-regel for uttak for overføring av materialer i en lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="ec0a0-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ec0a0-106">Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen, når de klargjør etterfylling av et nytt eller endret materiale.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="ec0a0-107">Opprette ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="ec0a0-107">Create new kanban rule</span></span>
1. <span data-ttu-id="ec0a0-108">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ec0a0-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-109">Click New.</span></span>
3. <span data-ttu-id="ec0a0-110">Velg Uttak i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="ec0a0-111">Typen Uttak brukes for kanban-regler for å overføre materialer eller varer.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="ec0a0-112">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ec0a0-113">Velg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="ec0a0-114">Denne aktiviteten er konfigurert til å flytte komponenter fra lager 11, lokasjon 11 til lager 12 og lokasjon 12.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="ec0a0-115">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ec0a0-116">Velg M0007.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-116">Select M0007.</span></span>  
6. <span data-ttu-id="ec0a0-117">Angi et tall i feltet Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="ec0a0-118">For eksempel 60.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-118">For example, 60.</span></span>  
7. <span data-ttu-id="ec0a0-119">I Måleenhet-feltet angir eller velger du en verdi.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="ec0a0-120">For eksempel Minutter.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="ec0a0-121">Angi antall for Kanban</span><span class="sxs-lookup"><span data-stu-id="ec0a0-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="ec0a0-122">Angi Standardantall som 5.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="ec0a0-123">Dette er antallet som skal overføres til hver kanban.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="ec0a0-124">Angi 2 i feltet Fast Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="ec0a0-125">Dette er antall Kanbaner som skal være aktive.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="ec0a0-126">I dette tilfellet overfører 2 Kanbaner 5 hver.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="ec0a0-127">Angi 1 i feltet Nedre varslingsgrense.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="ec0a0-128">Brukes til å holde oversikt over minimumsbeløpet for alle Kanbaner som skal være på målet.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="ec0a0-129">Dette brukes for eksempel brukes i oversikten over kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="ec0a0-130">Angi 2 i feltet Øvre varslingsgrense.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="ec0a0-131">Brukes til å holde oversikt over maksimumsbeløpet for alle Kanbaner som skal være på målet.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="ec0a0-132">Dette brukes for eksempel brukes i oversikten over kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="ec0a0-133">Opprett Kanbaner</span><span class="sxs-lookup"><span data-stu-id="ec0a0-133">Create kanbans</span></span>
1. <span data-ttu-id="ec0a0-134">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-134">Click Save.</span></span>
    * <span data-ttu-id="ec0a0-135">Kanban-regelen må lagres før du kan opprette Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="ec0a0-136">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-136">Click Add.</span></span>
    * <span data-ttu-id="ec0a0-137">Legg merke til at det ikke finnes noen aktive Kanbaner fordi foreslått antall nye Kanban er 2, og dette er lik Fast Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="ec0a0-138">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-138">Click Create.</span></span>
    * <span data-ttu-id="ec0a0-139">Dette vil opprette to Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="ec0a0-140">Legg merke til at 2 Kanbaner, for 5 hver, ble opprettet for denne kanban-regelen for uttak.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="ec0a0-141">Dette er det siste trinnet i prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ec0a0-141">This is the last step in this procedure.</span></span>  

