--- 
title: Flytte planlagte Kanban-jobber
description: "Denne prosedyren fokuserer på å flytte planlagte kanban-prosessjobber til en annen periode."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a20765f29a3d8b3bff75229ebbb1996a4d601154
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="6638d-103">Flytte planlagte Kanban-jobber</span><span class="sxs-lookup"><span data-stu-id="6638d-103">Move scheduled kanban jobs</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6638d-104">Denne prosedyren fokuserer på å flytte planlagte kanban-prosessjobber til en annen periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="6638d-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6638d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6638d-106">Denne prosedyren er ment for arbeidsledere eller produksjonsplanleggere som arbeider med Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="6638d-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="6638d-107">Velge planlagte Kanban-jobber</span><span class="sxs-lookup"><span data-stu-id="6638d-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="6638d-108">Gå til Produksjonsstyring > Kanban > Tidsplanlegging av kanban-jobb.</span><span class="sxs-lookup"><span data-stu-id="6638d-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="6638d-109">!MtCMR!Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6638d-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="6638d-110">áçêìõý!</span><span class="sxs-lookup"><span data-stu-id="6638d-110">áçêìõý !</span></span>
3. <span data-ttu-id="6638d-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6638d-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="6638d-112">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="6638d-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="6638d-113">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="6638d-113">Klik på Select.</span></span>
5. <span data-ttu-id="6638d-114">Velg "Planlagt" i feltet Vis jobbstatus.</span><span class="sxs-lookup"><span data-stu-id="6638d-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="6638d-115">Dette filtrerer jobblisten for å vise bare de planlagte kanban-jobbene.</span><span class="sxs-lookup"><span data-stu-id="6638d-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="6638d-116">Flytte Kanban-jobber til en annen periode</span><span class="sxs-lookup"><span data-stu-id="6638d-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="6638d-117">Finn og velg den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="6638d-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6638d-118">Velg en jobb som har jobbstatusen planlagt, for eksempel en jobb som er planlagt den 20. desember 2012, i feltet Planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="6638d-119">Flytt deretter jobben til forrige periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="6638d-120">Klikk Forrige periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="6638d-121">Klikk Slutt.</span><span class="sxs-lookup"><span data-stu-id="6638d-121">Klik på End.</span></span>
    * <span data-ttu-id="6638d-122">Dette flytter jobben til slutten av jobblisten som den siste jobben i forrige periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="6638d-123">Finn og velg den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="6638d-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6638d-124">Velg en jobb som har jobbstatusen planlagt, for eksempel en jobb som er planlagt den 18. desember 2012, i feltet Planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="6638d-125">Flytt deretter jobben til neste periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="6638d-126">Klikk Neste periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-126">Klik på Next period.</span></span>
6. <span data-ttu-id="6638d-127">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="6638d-127">Klik på Start.</span></span>
    * <span data-ttu-id="6638d-128">Dette flytter jobben til starten av jobblisten som den første jobben i forrige periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="6638d-129">Oppgave: Flytte en jobb i en periode</span><span class="sxs-lookup"><span data-stu-id="6638d-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="6638d-130">Finn og velg den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="6638d-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6638d-131">Velg en jobb som har jobbstatusen planlagt, for eksempel den andre jobben som er planlagt den 19. desember 2012, i feltet Planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="6638d-132">Flytt deretter jobben innenfor planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="6638d-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="6638d-133">Klikk Fremover.</span><span class="sxs-lookup"><span data-stu-id="6638d-133">Klik på Forward.</span></span>
    * <span data-ttu-id="6638d-134">Legg merke til at jobben er flyttet én linje ned i listen.</span><span class="sxs-lookup"><span data-stu-id="6638d-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="6638d-135">Klikk Bakover.</span><span class="sxs-lookup"><span data-stu-id="6638d-135">Klik på Backward.</span></span>
    * <span data-ttu-id="6638d-136">Legg merke til at jobben er flyttet én linje opp i listen.</span><span class="sxs-lookup"><span data-stu-id="6638d-136">Notice that the job is moved one line up on the list.</span></span>  


