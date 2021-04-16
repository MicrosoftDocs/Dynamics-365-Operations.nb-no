---
title: Opprette en Kanban-regel for flere aktiviteter
description: Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 828b01fbb3b94b1fcb9fe8a565b1191a4f4bf630
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829120"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="298c3-103">Opprette en Kanban-regel for flere aktiviteter</span><span class="sxs-lookup"><span data-stu-id="298c3-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="298c3-104">Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt.</span><span class="sxs-lookup"><span data-stu-id="298c3-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="298c3-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="298c3-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="298c3-106">Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="298c3-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="298c3-107">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="298c3-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="298c3-108">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="298c3-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="298c3-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="298c3-109">Click New.</span></span>
3. <span data-ttu-id="298c3-110">Velg Planlagt i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="298c3-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="298c3-111">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="298c3-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="298c3-112">Velg SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="298c3-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="298c3-113">Merk av for Flere aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="298c3-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="298c3-114">Formålet er å inkludere flere enn én aktivitet i Kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="298c3-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="298c3-115">Du kan velge en bane i produksjonsflyten når du velger den siste planaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="298c3-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="298c3-116">Angi eller velg en verdi i feltet Siste planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="298c3-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="298c3-117">Velg SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="298c3-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="298c3-118">Når du har valgt verdien, åpnes en side automatisk.</span><span class="sxs-lookup"><span data-stu-id="298c3-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="298c3-119">Velg Kanban-flyten SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="298c3-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="298c3-120">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="298c3-120">Click OK.</span></span>  
7. <span data-ttu-id="298c3-121">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="298c3-121">Expand the Details section.</span></span>
8. <span data-ttu-id="298c3-122">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="298c3-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="298c3-123">Velg vare L0006.</span><span class="sxs-lookup"><span data-stu-id="298c3-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="298c3-124">Opprette Kanban og vise jobber</span><span class="sxs-lookup"><span data-stu-id="298c3-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="298c3-125">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="298c3-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="298c3-126">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="298c3-126">Click Add.</span></span>
3. <span data-ttu-id="298c3-127">Skriv inn 1 i feltet Antall nye Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="298c3-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="298c3-128">Dette oppretter én Kanban.</span><span class="sxs-lookup"><span data-stu-id="298c3-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="298c3-129">Sett Produktantall til 3.</span><span class="sxs-lookup"><span data-stu-id="298c3-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="298c3-130">Kanbanen behandler tre produkter.</span><span class="sxs-lookup"><span data-stu-id="298c3-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="298c3-131">Angi dato og klokkeslett i feltet Forfallsdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="298c3-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="298c3-132">Du kan angi I dag.</span><span class="sxs-lookup"><span data-stu-id="298c3-132">You can enter Today.</span></span>  
6. <span data-ttu-id="298c3-133">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="298c3-133">Click Create.</span></span>
7. <span data-ttu-id="298c3-134">Klikk på Detaljer.</span><span class="sxs-lookup"><span data-stu-id="298c3-134">Click Details.</span></span>
    * <span data-ttu-id="298c3-135">Legg merke til at Kanbanen har to prosessjobber fra produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="298c3-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="298c3-136">Den første er SpeakerAssemblyAndPolish, og den andre er SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="298c3-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="298c3-137">Dette er det siste trinnet!</span><span class="sxs-lookup"><span data-stu-id="298c3-137">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]