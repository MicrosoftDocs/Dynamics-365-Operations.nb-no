---
title: Fjerne en Kanban-jobb fra tidsplanen
description: Denne prosedyren fokuserer på å fjerne en planlagt kanban-prosessjobb fra tidsplanen ved å tilbakestille jobbstatusen til Ikke planlagt.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcd9247e24323ba606377d7e51bd4447ab51c905
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961621"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="b6b11-103">Fjerne en Kanban-jobb fra tidsplanen</span><span class="sxs-lookup"><span data-stu-id="b6b11-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6b11-104">Denne prosedyren fokuserer på å fjerne en planlagt kanban-prosessjobb fra tidsplanen ved å tilbakestille jobbstatusen til Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="b6b11-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="b6b11-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="b6b11-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b6b11-106">Denne prosedyren er ment for arbeidsledere eller produksjonsplanleggere.</span><span class="sxs-lookup"><span data-stu-id="b6b11-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="b6b11-107">Finne en planlagt Kanban-jobb</span><span class="sxs-lookup"><span data-stu-id="b6b11-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="b6b11-108">Gå til Produksjonskontroll > Kanban > Kanban-jobbplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b6b11-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="b6b11-109">Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b6b11-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b6b11-110">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b6b11-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6b11-111">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="b6b11-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="b6b11-112">Klikk på Velg.</span><span class="sxs-lookup"><span data-stu-id="b6b11-112">Click Select.</span></span>
5. <span data-ttu-id="b6b11-113">I feltet Vis jobbstatus velger du "Planlagt".</span><span class="sxs-lookup"><span data-stu-id="b6b11-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="b6b11-114">Fjerne den planlagte kanban-jobb fra tidsplanen</span><span class="sxs-lookup"><span data-stu-id="b6b11-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="b6b11-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b6b11-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b6b11-116">Velg en jobb med statusen planlagt, for eksempel en jobb fra 19. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="b6b11-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="b6b11-117">Klikk på Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b6b11-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="b6b11-118">Klikk på Tilbakestill jobbstatus.</span><span class="sxs-lookup"><span data-stu-id="b6b11-118">Click Revert job status.</span></span>
4. <span data-ttu-id="b6b11-119">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="b6b11-119">Click OK.</span></span>
    * <span data-ttu-id="b6b11-120">Dette vil tilbakestille den gjeldende jobbstatusen fra "Planlagt" til "Ikke planlagt" og fjerne den fra prosesstavlen.</span><span class="sxs-lookup"><span data-stu-id="b6b11-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

