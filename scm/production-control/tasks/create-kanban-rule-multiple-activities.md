--- 
title: Opprette en Kanban-regel for flere aktiviteter
description: "Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.openlocfilehash: d6d0c50da3124553124b65f6ba0e1c5ed35e8613
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="22d77-103">Opprette en Kanban-regel for flere aktiviteter</span><span class="sxs-lookup"><span data-stu-id="22d77-103">Create a kanban rule for multiple activities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22d77-104">Denne fremgangsmåten viser hvordan du oppretter en Kanban-regel som inkluderer flere aktiviteter fra en produksjonsflyt.</span><span class="sxs-lookup"><span data-stu-id="22d77-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="22d77-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="22d77-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="22d77-106">Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="22d77-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="22d77-107">Opprett en ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="22d77-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="22d77-108">Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="22d77-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="22d77-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="22d77-109">Click New.</span></span>
3. <span data-ttu-id="22d77-110">Velg Planlagt i feltet Etterfyllingsstrategi.</span><span class="sxs-lookup"><span data-stu-id="22d77-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="22d77-111">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="22d77-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="22d77-112">Velg SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="22d77-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="22d77-113">Merk av for Flere aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="22d77-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="22d77-114">Formålet er å inkludere flere enn én aktivitet i Kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="22d77-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="22d77-115">Du kan velge en bane i produksjonsflyten når du velger den siste planaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="22d77-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="22d77-116">Angi eller velg en verdi i feltet Siste planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="22d77-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="22d77-117">Velg SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="22d77-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="22d77-118">Når du har valgt verdien, åpnes en side automatisk.</span><span class="sxs-lookup"><span data-stu-id="22d77-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="22d77-119">Velg Kanban-flyten SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="22d77-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="22d77-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="22d77-120">Click OK.</span></span>  
7. <span data-ttu-id="22d77-121">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="22d77-121">Expand the Details section.</span></span>
8. <span data-ttu-id="22d77-122">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="22d77-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="22d77-123">Velg vare L0006.</span><span class="sxs-lookup"><span data-stu-id="22d77-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="22d77-124">Opprette Kanban og vise jobber</span><span class="sxs-lookup"><span data-stu-id="22d77-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="22d77-125">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="22d77-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="22d77-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="22d77-126">Click Add.</span></span>
3. <span data-ttu-id="22d77-127">Skriv inn 1 i feltet Antall nye Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="22d77-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="22d77-128">Dette oppretter én Kanban.</span><span class="sxs-lookup"><span data-stu-id="22d77-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="22d77-129">Sett Produktantall til 3.</span><span class="sxs-lookup"><span data-stu-id="22d77-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="22d77-130">Kanbanen behandler tre produkter.</span><span class="sxs-lookup"><span data-stu-id="22d77-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="22d77-131">Angi dato og klokkeslett i feltet Forfallsdato/-klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="22d77-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="22d77-132">Du kan angi I dag.</span><span class="sxs-lookup"><span data-stu-id="22d77-132">You can enter Today.</span></span>  
6. <span data-ttu-id="22d77-133">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="22d77-133">Click Create.</span></span>
7. <span data-ttu-id="22d77-134">Klikk Detaljer.</span><span class="sxs-lookup"><span data-stu-id="22d77-134">Click Details.</span></span>
    * <span data-ttu-id="22d77-135">Legg merke til at Kanbanen har to prosessjobber fra produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="22d77-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="22d77-136">Den første er SpeakerAssemblyAndPolish, og den andre er SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="22d77-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="22d77-137">Dette er det siste trinnet!</span><span class="sxs-lookup"><span data-stu-id="22d77-137">This is the last step!</span></span>  


