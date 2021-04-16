---
title: Flytte planlagte Kanban-jobber
description: Denne prosedyren fokuserer på å flytte planlagte kanban-prosessjobber til en annen periode.
author: ChristianRytt
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d58ee740824809f15da68db66616bb01d5dbfab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825020"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="4dc41-103">Flytte planlagte Kanban-jobber</span><span class="sxs-lookup"><span data-stu-id="4dc41-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4dc41-104">Denne prosedyren fokuserer på å flytte planlagte kanban-prosessjobber til en annen periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="4dc41-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="4dc41-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4dc41-106">Denne prosedyren er ment for arbeidsledere eller produksjonsplanleggere som arbeider med Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="4dc41-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="4dc41-107">Velge planlagte Kanban-jobber.</span><span class="sxs-lookup"><span data-stu-id="4dc41-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="4dc41-108">Gå til **Produksjonskontroll > Kanban > Kanban-jobbplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="4dc41-109">Klikk på rullegardinknappen i **Arbeidscelle**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4dc41-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="4dc41-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4dc41-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="4dc41-111">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="4dc41-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="4dc41-112">Klikk på **Velg**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-112">Click **Select**.</span></span> 

5. <span data-ttu-id="4dc41-113">I feltet **Vis jobbstatus** velger du **Planlagt**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="4dc41-114">Dette filtrerer jobblisten for å vise bare de planlagte kanban-jobbene.</span><span class="sxs-lookup"><span data-stu-id="4dc41-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="4dc41-115">Flytte Kanban-jobber til en annen periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="4dc41-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4dc41-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="4dc41-117">Velg en jobb som har statusen **Planlagt jobb**, for eksempel en jobb som er planlagt den 20. desember 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="4dc41-118">Flytt deretter jobben til forrige periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="4dc41-119">Klikk på **Forrige periode**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="4dc41-120">Klikk på **Avslutt** for å flytte jobben til slutten av jobblisten som den siste jobben i forrige periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="4dc41-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4dc41-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="4dc41-122">Velg en jobb som har statusen **Planlagt jobb**, for eksempel en jobb som er planlagt den 18. desember 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="4dc41-123">Flytt deretter jobben til neste periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="4dc41-124">Klikk på **Neste periode**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="4dc41-125">Klikk på **Start** for å flytte jobben til starten av jobblisten som den første jobben i forrige periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="4dc41-126">Flytte en jobb i en periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="4dc41-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4dc41-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="4dc41-128">Velg en jobb som har statusen Planlagt jobb, for eksempel den andre jobben som er planlagt den 19. desember 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="4dc41-129">Flytt deretter jobben innenfor planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="4dc41-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="4dc41-130">Klikk på **Forover**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-130">Click **Forward**.</span></span> <span data-ttu-id="4dc41-131">Legg merke til at jobben er flyttet én linje ned i listen.</span><span class="sxs-lookup"><span data-stu-id="4dc41-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="4dc41-132">Klikk på **Bakover**.</span><span class="sxs-lookup"><span data-stu-id="4dc41-132">Click **Backward**.</span></span> <span data-ttu-id="4dc41-133">Legg merke til at jobben er flyttet én linje opp i listen.</span><span class="sxs-lookup"><span data-stu-id="4dc41-133">Notice that the job is moved one line up on the list.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]