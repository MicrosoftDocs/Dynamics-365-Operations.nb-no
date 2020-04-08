---
title: Flytte planlagte Kanban-jobber
description: Denne prosedyren fokuserer på å flytte planlagte kanban-prosessjobber til en annen periode.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cad61ad292f80d6092ecea679645f729469b8a8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149004"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="d1463-103">Flytte planlagte Kanban-jobber</span><span class="sxs-lookup"><span data-stu-id="d1463-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1463-104">Denne prosedyren fokuserer på å flytte planlagte kanban-prosessjobber til en annen periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="d1463-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d1463-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d1463-106">Denne prosedyren er ment for arbeidsledere eller produksjonsplanleggere som arbeider med Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="d1463-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="d1463-107">Velge planlagte Kanban-jobber.</span><span class="sxs-lookup"><span data-stu-id="d1463-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="d1463-108">Gå til **Produksjonskontroll > Kanban > Kanban-jobbplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="d1463-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="d1463-109">Klikk rullegardinknappen i **Arbeidscelle**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d1463-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="d1463-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d1463-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="d1463-111">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="d1463-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="d1463-112">Klikk **Velg**.</span><span class="sxs-lookup"><span data-stu-id="d1463-112">Click **Select**.</span></span> 

5. <span data-ttu-id="d1463-113">I feltet **Vis jobbstatus** velger du **Planlagt**.</span><span class="sxs-lookup"><span data-stu-id="d1463-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="d1463-114">Dette filtrerer jobblisten for å vise bare de planlagte kanban-jobbene.</span><span class="sxs-lookup"><span data-stu-id="d1463-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="d1463-115">Flytte Kanban-jobber til en annen periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="d1463-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d1463-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="d1463-117">Velg en jobb som har statusen **Planlagt jobb**, for eksempel en jobb som er planlagt den 20. desember 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="d1463-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="d1463-118">Flytt deretter jobben til forrige periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="d1463-119">Klikk **Forrige periode**.</span><span class="sxs-lookup"><span data-stu-id="d1463-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="d1463-120">Klikk på **Avslutt** for å flytte jobben til slutten av jobblisten som den siste jobben i forrige periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="d1463-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d1463-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="d1463-122">Velg en jobb som har statusen **Planlagt jobb**, for eksempel en jobb som er planlagt den 18. desember 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="d1463-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="d1463-123">Flytt deretter jobben til neste periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="d1463-124">Klikk **Neste periode**.</span><span class="sxs-lookup"><span data-stu-id="d1463-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="d1463-125">Klikk på **Start** for å flytte jobben til starten av jobblisten som den første jobben i forrige periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="d1463-126">Flytte en jobb i en periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="d1463-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d1463-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="d1463-128">Velg en jobb som har statusen Planlagt jobb, for eksempel den andre jobben som er planlagt den 19. desember 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="d1463-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="d1463-129">Flytt deretter jobben innenfor planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="d1463-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="d1463-130">Klikk **Forover**.</span><span class="sxs-lookup"><span data-stu-id="d1463-130">Click **Forward**.</span></span> <span data-ttu-id="d1463-131">Legg merke til at jobben er flyttet én linje ned i listen.</span><span class="sxs-lookup"><span data-stu-id="d1463-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="d1463-132">Klikk **Bakover**.</span><span class="sxs-lookup"><span data-stu-id="d1463-132">Click **Backward**.</span></span> <span data-ttu-id="d1463-133">Legg merke til at jobben er flyttet én linje opp i listen.</span><span class="sxs-lookup"><span data-stu-id="d1463-133">Notice that the job is moved one line up on the list.</span></span>
