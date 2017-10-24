--- 
title: Planlegge en produksjonsordre med operasjoner og finplanlegging
description: "Denne fremgangsmåten fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="7b39a-103">Planlegge en produksjonsordre med operasjoner og finplanlegging</span><span class="sxs-lookup"><span data-stu-id="7b39a-103">Schedule a production order with operations and job scheduling</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b39a-104">Denne fremgangsmåten fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7b39a-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="7b39a-105">Ingen jobber opprettes med grovplanlegging, mens jobber opprettes med finplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7b39a-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="7b39a-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="7b39a-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7b39a-107">Denne fremgangsmåten er ment for produksjonssjef, produksjonsplanlegger eller arbeidsleder som arbeider i et atskilt produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="7b39a-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="7b39a-108">Opprette en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="7b39a-108">Create a production order</span></span>
1. <span data-ttu-id="7b39a-109">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="7b39a-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="7b39a-110">Klikk Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="7b39a-110">Click New production order.</span></span>
3. <span data-ttu-id="7b39a-111">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b39a-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7b39a-112">Velg varenummer D0001.</span><span class="sxs-lookup"><span data-stu-id="7b39a-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="7b39a-113">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="7b39a-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="7b39a-114">Planlegge operasjoner for produksjonsordren</span><span class="sxs-lookup"><span data-stu-id="7b39a-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="7b39a-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7b39a-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7b39a-116">Velg produksjonsordren du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="7b39a-116">Select the production order that you have just created.</span></span> <span data-ttu-id="7b39a-117">Den bør være på toppen av listen.</span><span class="sxs-lookup"><span data-stu-id="7b39a-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="7b39a-118">Klikk Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7b39a-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="7b39a-119">Klikk Planlegg operasjoner.</span><span class="sxs-lookup"><span data-stu-id="7b39a-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="7b39a-120">Velg Fremover fra planleggingsdato i Planleggingsretning-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b39a-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="7b39a-121">Angi en dato i Planleggingsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b39a-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="7b39a-122">Velg en fremtidig dato, for eksempel i dag pluss én uke.</span><span class="sxs-lookup"><span data-stu-id="7b39a-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="7b39a-123">Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.</span><span class="sxs-lookup"><span data-stu-id="7b39a-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="7b39a-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7b39a-124">Click OK.</span></span>
7. <span data-ttu-id="7b39a-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7b39a-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7b39a-126">Vær oppmerksom på at statusen endres til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="7b39a-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="7b39a-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7b39a-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7b39a-128">Klikk Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="7b39a-128">Click All jobs.</span></span>
    * <span data-ttu-id="7b39a-129">Vær oppmerksom på at ingen jobber opprettes med grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7b39a-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="7b39a-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7b39a-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="7b39a-131">Planlegge jobber for produksjonsordren</span><span class="sxs-lookup"><span data-stu-id="7b39a-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="7b39a-132">Klikk Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7b39a-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="7b39a-133">Klikk Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="7b39a-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="7b39a-134">Velg Fremover fra planleggingsdato i Planleggingsretning-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b39a-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="7b39a-135">Angi en dato i Planleggingsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="7b39a-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="7b39a-136">Velg en fremtidig dato, for eksempel i dag pluss én uke.</span><span class="sxs-lookup"><span data-stu-id="7b39a-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="7b39a-137">Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.</span><span class="sxs-lookup"><span data-stu-id="7b39a-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="7b39a-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7b39a-138">Click OK.</span></span>
6. <span data-ttu-id="7b39a-139">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7b39a-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="7b39a-140">Klikk Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="7b39a-140">Click All jobs.</span></span>
    * <span data-ttu-id="7b39a-141">Vær oppmerksom på at basert på den aktive ruten, opprettes fem jobber med finplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7b39a-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


