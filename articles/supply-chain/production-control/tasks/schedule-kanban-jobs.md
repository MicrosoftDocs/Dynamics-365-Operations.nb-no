---
title: Planlegge Kanban-jobber
description: Denne prosedyren fokuserer på planlegging av kanban-prosessjobber for en bestemt arbeidscelle.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5170fecf0190591d74f45d35fecc4472e7f5e900
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562167"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="f4bcd-103">Planlegge Kanban-jobber</span><span class="sxs-lookup"><span data-stu-id="f4bcd-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4bcd-104">Denne prosedyren fokuserer på planlegging av kanban-prosessjobber for en bestemt arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="f4bcd-105">Fremgangsmåten "Klargjøre en kanban-prosessjobb når materialer ikke er tilgjengelige" er en forutsetning for oppretting av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="f4bcd-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f4bcd-107">Denne oppgaven er ment for arbeidsledere og produksjonsplanleggere som arbeider med Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="f4bcd-108">Velge kanban-jobber for en arbeidscelle</span><span class="sxs-lookup"><span data-stu-id="f4bcd-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="f4bcd-109">Gå til Produksjonskontroll > Kanban > Kanban-jobbplanlegging.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="f4bcd-110">Vis faktaboksen Periodekapasitet.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="f4bcd-111">Vis faktaboksen Kanban.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="f4bcd-112">Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f4bcd-113">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f4bcd-114">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-114">Select work cell 1250.</span></span> <span data-ttu-id="f4bcd-115">Dette filtrerer visningen slik at bare jobbene for arbeidscellen 1250 vises.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="f4bcd-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4bcd-117">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="f4bcd-118">Planlegge en kanban-jobb i den første tilgjengelige perioden</span><span class="sxs-lookup"><span data-stu-id="f4bcd-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="f4bcd-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f4bcd-120">Velg den første raden i listen som har Ikke planlagt-status.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="f4bcd-121">Det prikkede ikonet i Jobbstatus-feltet angir ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="f4bcd-122">Klikk Tidsplan.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-122">Click Schedule.</span></span>
    * <span data-ttu-id="f4bcd-123">Dette vil planlegg kanban-jobben i den første tilgjengelige perioden.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="f4bcd-124">Legg merke til at kanban-jobben er flyttet til slutten av listen fordi den er lagt til i perioden fra dagens dato.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="f4bcd-125">Hvis perioden fra dagens dato er opptatt, flyttes jobben til den første tilgjengelige perioden.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="f4bcd-126">Planlegge to kanban-jobber for en bestemt dag</span><span class="sxs-lookup"><span data-stu-id="f4bcd-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="f4bcd-127">Velg rad 1 i listen.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="f4bcd-128">Du skal se at den første raden har Ikke planlagt-statusen i jobbstatus-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="f4bcd-129">Velg rad 2 i listen.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="f4bcd-130">Du skal se at den andre raden har Ikke planlagt-statusen i jobbstatus-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="f4bcd-131">Nå har du valgt de to første jobbene.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="f4bcd-132">Klikk Planlegg fra dato for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="f4bcd-133">Merk av eller fjern merket for Overstyr reaksjon på kapasitetsmangel.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="f4bcd-134">Med dette alternativet kan du overstyre standardreaksjonen på kapasitetsmangel.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="f4bcd-135">Velg Legg til i den ønskede perioden i feltet Reaksjon på kapasitetsmangel.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="f4bcd-136">Dette alternativet sikrer at jobben er lagt til den ønskede perioden, uansett om arbeidscellen kan være overbelastet.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="f4bcd-137">Klikk Tidsplan.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-137">Click Schedule.</span></span>
    * <span data-ttu-id="f4bcd-138">Legg merke til at begge jobber er lagt til den ønskede perioden.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="f4bcd-139">I delen Periodisk kapasitet kan du se belastningen for hver periode.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="f4bcd-140">Forbruk-feltet viser det planlagte forbruket i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="f4bcd-141">Hvis det planlagte forbruket er høyere enn den tilgjengelige kapasiteten i denne perioden, vil det overbelastede forbruket velges.</span><span class="sxs-lookup"><span data-stu-id="f4bcd-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

