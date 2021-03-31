---
title: Planlegge en produksjonsordre med operasjoner og finplanlegging
description: Dette emnet fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ace204f1ec79cc8f9ce10ebfdc3606879e40d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215847"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="b0bdb-103">Planlegge en produksjonsordre med operasjoner og finplanlegging</span><span class="sxs-lookup"><span data-stu-id="b0bdb-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0bdb-104">Dette emnet fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="b0bdb-105">Ingen jobber opprettes med grovplanlegging, mens jobber opprettes med finplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="b0bdb-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b0bdb-107">Denne fremgangsmåten er ment for produksjonssjef, produksjonsplanlegger eller arbeidsleder som arbeider i et atskilt produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="b0bdb-108">Opprette en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="b0bdb-108">Create a production order</span></span>
1. <span data-ttu-id="b0bdb-109">I navigasjonsruten går du til **Moduler > Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="b0bdb-110">Velg **Ny produksjonsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-110">Select **New production order**.</span></span>
3. <span data-ttu-id="b0bdb-111">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="b0bdb-112">Velg varenummer **D0001**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="b0bdb-113">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="b0bdb-114">Planlegge operasjoner for produksjonsordren</span><span class="sxs-lookup"><span data-stu-id="b0bdb-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="b0bdb-115">Merk den nyopprettede raden.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="b0bdb-116">Velg **Planlegg** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="b0bdb-117">Velg **Planlegg operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="b0bdb-118">Velg **Fremover fra planleggingsdato** i **Planleggingsretning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="b0bdb-119">Angi en dato i **Planleggingsdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="b0bdb-120">Velg en fremtidig dato, for eksempel i dag pluss én uke.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="b0bdb-121">Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="b0bdb-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-122">Select **OK**.</span></span>
7. <span data-ttu-id="b0bdb-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-123">In the list, mark the selected row.</span></span> <span data-ttu-id="b0bdb-124">Vær oppmerksom på at statusen endres til **Planlagt**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="b0bdb-125">Velg **Alle jobber**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-125">Select **All jobs**.</span></span> <span data-ttu-id="b0bdb-126">Vær oppmerksom på at ingen jobber opprettes med grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="b0bdb-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="b0bdb-128">Planlegge jobber for produksjonsordren</span><span class="sxs-lookup"><span data-stu-id="b0bdb-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="b0bdb-129">Velg **Planlegg** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="b0bdb-130">Velg **Planlegg jobber**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="b0bdb-131">Velg **Fremover fra planleggingsdato** i **Planleggingsretning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="b0bdb-132">Angi en dato i **Planleggingsdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="b0bdb-133">Velg en fremtidig dato, for eksempel i dag pluss én uke.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="b0bdb-134">Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="b0bdb-135">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-135">Select **OK**.</span></span>
6. <span data-ttu-id="b0bdb-136">Velg **Produksjonsordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="b0bdb-137">Velg **Alle jobber**.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-137">Select **All jobs**.</span></span> <span data-ttu-id="b0bdb-138">Vær oppmerksom på at basert på den aktive ruten, opprettes fem jobber med finplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b0bdb-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]