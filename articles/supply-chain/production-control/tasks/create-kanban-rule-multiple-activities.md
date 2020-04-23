---
title: Opprette en Kanban-regel for flere aktiviteter
description: Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68cac0f581e786cdb3801e03fb60db7bc05ffb2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212231"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="c96ae-103">Opprette en Kanban-regel for flere aktiviteter</span><span class="sxs-lookup"><span data-stu-id="c96ae-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c96ae-104">Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt.</span><span class="sxs-lookup"><span data-stu-id="c96ae-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="c96ae-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c96ae-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c96ae-106">Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="c96ae-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="c96ae-107">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="c96ae-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="c96ae-108">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="c96ae-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="c96ae-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c96ae-109">Click New.</span></span>
3. <span data-ttu-id="c96ae-110">Velg Planlagt i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="c96ae-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="c96ae-111">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="c96ae-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c96ae-112">Velg SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="c96ae-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="c96ae-113">Merk av for Flere aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c96ae-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="c96ae-114">Formålet er å inkludere flere enn én aktivitet i Kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="c96ae-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="c96ae-115">Du kan velge en bane i produksjonsflyten når du velger den siste planaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="c96ae-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="c96ae-116">Angi eller velg en verdi i feltet Siste planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="c96ae-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c96ae-117">Velg SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="c96ae-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="c96ae-118">Når du har valgt verdien, åpnes en side automatisk.</span><span class="sxs-lookup"><span data-stu-id="c96ae-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="c96ae-119">Velg Kanban-flyten SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="c96ae-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="c96ae-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c96ae-120">Click OK.</span></span>  
7. <span data-ttu-id="c96ae-121">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="c96ae-121">Expand the Details section.</span></span>
8. <span data-ttu-id="c96ae-122">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="c96ae-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c96ae-123">Velg vare L0006.</span><span class="sxs-lookup"><span data-stu-id="c96ae-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="c96ae-124">Opprette Kanban og vise jobber</span><span class="sxs-lookup"><span data-stu-id="c96ae-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="c96ae-125">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="c96ae-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="c96ae-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c96ae-126">Click Add.</span></span>
3. <span data-ttu-id="c96ae-127">Skriv inn 1 i feltet Antall nye Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="c96ae-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="c96ae-128">Dette oppretter én Kanban.</span><span class="sxs-lookup"><span data-stu-id="c96ae-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="c96ae-129">Sett Produktantall til 3.</span><span class="sxs-lookup"><span data-stu-id="c96ae-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="c96ae-130">Kanbanen behandler tre produkter.</span><span class="sxs-lookup"><span data-stu-id="c96ae-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="c96ae-131">Angi dato og klokkeslett i feltet Forfallsdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="c96ae-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="c96ae-132">Du kan angi I dag.</span><span class="sxs-lookup"><span data-stu-id="c96ae-132">You can enter Today.</span></span>  
6. <span data-ttu-id="c96ae-133">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="c96ae-133">Click Create.</span></span>
7. <span data-ttu-id="c96ae-134">Klikk Detaljer.</span><span class="sxs-lookup"><span data-stu-id="c96ae-134">Click Details.</span></span>
    * <span data-ttu-id="c96ae-135">Legg merke til at Kanbanen har to prosessjobber fra produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="c96ae-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="c96ae-136">Den første er SpeakerAssemblyAndPolish, og den andre er SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="c96ae-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="c96ae-137">Dette er det siste trinnet!</span><span class="sxs-lookup"><span data-stu-id="c96ae-137">This is the last step!</span></span>  

