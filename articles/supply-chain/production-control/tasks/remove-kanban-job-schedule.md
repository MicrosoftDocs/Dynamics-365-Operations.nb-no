---
title: Fjerne en Kanban-jobb fra tidsplanen
description: Denne prosedyren fokuserer på å fjerne en planlagt kanban-prosessjobb fra tidsplanen ved å tilbakestille jobbstatusen til Ikke planlagt.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "352074"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="9a04f-103">Fjerne en Kanban-jobb fra tidsplanen</span><span class="sxs-lookup"><span data-stu-id="9a04f-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a04f-104">Denne prosedyren fokuserer på å fjerne en planlagt kanban-prosessjobb fra tidsplanen ved å tilbakestille jobbstatusen til Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="9a04f-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="9a04f-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9a04f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9a04f-106">Denne prosedyren er ment for arbeidsledere eller produksjonsplanleggere.</span><span class="sxs-lookup"><span data-stu-id="9a04f-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="9a04f-107">Finne en planlagt Kanban-jobb</span><span class="sxs-lookup"><span data-stu-id="9a04f-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="9a04f-108">Gå til Produksjonskontroll > Kanban > Kanban-jobbplanlegging.</span><span class="sxs-lookup"><span data-stu-id="9a04f-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="9a04f-109">Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9a04f-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9a04f-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9a04f-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9a04f-111">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="9a04f-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="9a04f-112">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="9a04f-112">Click Select.</span></span>
5. <span data-ttu-id="9a04f-113">I feltet Vis jobbstatus velger du "Planlagt".</span><span class="sxs-lookup"><span data-stu-id="9a04f-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="9a04f-114">Fjerne den planlagte kanban-jobb fra tidsplanen</span><span class="sxs-lookup"><span data-stu-id="9a04f-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="9a04f-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9a04f-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9a04f-116">Velg en jobb med statusen planlagt, for eksempel en jobb fra 19. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="9a04f-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="9a04f-117">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9a04f-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="9a04f-118">Klikk Tilbakestill jobbstatus.</span><span class="sxs-lookup"><span data-stu-id="9a04f-118">Click Revert job status.</span></span>
4. <span data-ttu-id="9a04f-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9a04f-119">Click OK.</span></span>
    * <span data-ttu-id="9a04f-120">Dette vil tilbakestille den gjeldende jobbstatusen fra "Planlagt" til "Ikke planlagt" og fjerne den fra prosesstavlen.</span><span class="sxs-lookup"><span data-stu-id="9a04f-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

