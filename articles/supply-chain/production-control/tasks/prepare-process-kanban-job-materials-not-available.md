--- 
title: "Klargjøre en Kanban-prosessjobb når materialer ikke er tilgjengelige for arbeidscellen"
description: "Denne prosedyren fokuserer på å klargjøre en kanban-prosessjobb når noen materialer ikke er tilgjengelige for arbeidscellen. Derfor er det nødvendig å plukker materialer fra lageret."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="362d2-103">Klargjøre en Kanban-prosessjobb når materialer ikke er tilgjengelige for arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="362d2-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="362d2-104">Denne prosedyren fokuserer på å klargjøre en kanban-prosessjobb når noen materialer ikke er tilgjengelige for arbeidscellen. Derfor er det nødvendig å plukker materialer fra lageret.</span><span class="sxs-lookup"><span data-stu-id="362d2-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="362d2-105">Fremgangsmåten "Klargjøre en kanban-prosessjobb når materialer er tilgjengelige" er en forutsetning for oppretting av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="362d2-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="362d2-106">Denne prosedyren er ment for maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="362d2-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="362d2-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="362d2-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="362d2-108">Gå til Produksjonskontroll > Kanban > Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="362d2-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="362d2-109">Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="362d2-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="362d2-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="362d2-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="362d2-111">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="362d2-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="362d2-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="362d2-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="362d2-113">Velg Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="362d2-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="362d2-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="362d2-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="362d2-115">Opphev valget av rad 4 i listen.</span><span class="sxs-lookup"><span data-stu-id="362d2-115">In the list, deselect row 4.</span></span> <span data-ttu-id="362d2-116">Velg eventuelt rad 4 hvis du ikke har fullført oppgaven "Klargjøre en kanban-prosessjobb når materialer er tilgjengelige."</span><span class="sxs-lookup"><span data-stu-id="362d2-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="362d2-117">Aktiver/deaktiver utvidelsen av delen Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="362d2-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="362d2-118">Ingen oppføring-ikonet i forsyningsstatusen angir at 48 stk. av vare P0002 mangler for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="362d2-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="362d2-119">Overføre materialer til arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="362d2-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="362d2-120">Aktiver/deaktiver utvidelsen av delen Overføringsjobber.</span><span class="sxs-lookup"><span data-stu-id="362d2-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="362d2-121">Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P0002.</span><span class="sxs-lookup"><span data-stu-id="362d2-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="362d2-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="362d2-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="362d2-123">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="362d2-123">Click Start.</span></span>
    * <span data-ttu-id="362d2-124">Overføring pågår.</span><span class="sxs-lookup"><span data-stu-id="362d2-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="362d2-125">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="362d2-125">Click Complete.</span></span>
    * <span data-ttu-id="362d2-126">Vare P0002 er nå tilgjengelig i plukklisten for kanban-jobben.</span><span class="sxs-lookup"><span data-stu-id="362d2-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="362d2-127">Dette betyr at vi kan forberede kanban med alle de nødvendige materialene.</span><span class="sxs-lookup"><span data-stu-id="362d2-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="362d2-128">Klikk Klargjør.</span><span class="sxs-lookup"><span data-stu-id="362d2-128">Click Prepare.</span></span>
    * <span data-ttu-id="362d2-129">Legg merke til at et ikon i jobbstatusen angir at jobben er klar.</span><span class="sxs-lookup"><span data-stu-id="362d2-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


