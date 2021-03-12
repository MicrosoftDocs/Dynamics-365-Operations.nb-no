---
title: Klargjøre en Kanban-prosessjobb når materialer ikke er tilgjengelige for arbeidscellen
description: Denne prosedyren fokuserer på å klargjøre en kanban-prosessjobb når noen materialer ikke er tilgjengelige for arbeidscellen. Derfor er det nødvendig å plukker materialer fra lageret.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df0396a1d00e61ad82e52fc07779e239cd811ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994097"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="81f8c-103">Klargjøre en Kanban-prosessjobb når materialer ikke er tilgjengelige for arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="81f8c-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81f8c-104">Denne prosedyren fokuserer på å klargjøre en kanban-prosessjobb når noen materialer ikke er tilgjengelige for arbeidscellen. Derfor er det nødvendig å plukker materialer fra lageret.</span><span class="sxs-lookup"><span data-stu-id="81f8c-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="81f8c-105">Fremgangsmåten "Klargjøre en kanban-prosessjobb når materialer er tilgjengelige" er en forutsetning for oppretting av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="81f8c-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="81f8c-106">Denne prosedyren er ment for maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="81f8c-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="81f8c-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="81f8c-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="81f8c-108">Gå til Produksjonskontroll > Kanban > Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="81f8c-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="81f8c-109">Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="81f8c-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="81f8c-110">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="81f8c-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="81f8c-111">Velg arbeidscellen 1250.</span><span class="sxs-lookup"><span data-stu-id="81f8c-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="81f8c-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="81f8c-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81f8c-113">Velg Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="81f8c-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="81f8c-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="81f8c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81f8c-115">Opphev valget av rad 4 i listen.</span><span class="sxs-lookup"><span data-stu-id="81f8c-115">In the list, deselect row 4.</span></span> <span data-ttu-id="81f8c-116">Velg eventuelt rad 4 hvis du ikke har fullført oppgaven "Klargjøre en kanban-prosessjobb når materialer er tilgjengelige."</span><span class="sxs-lookup"><span data-stu-id="81f8c-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="81f8c-117">Aktiver/deaktiver utvidelsen av delen Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="81f8c-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="81f8c-118">Ingen oppføring-ikonet i forsyningsstatusen angir at 48 stk. av vare P0002 mangler for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="81f8c-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="81f8c-119">Overføre materialer til arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="81f8c-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="81f8c-120">Aktiver/deaktiver utvidelsen av delen Overføringsjobber.</span><span class="sxs-lookup"><span data-stu-id="81f8c-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="81f8c-121">Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P0002.</span><span class="sxs-lookup"><span data-stu-id="81f8c-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="81f8c-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="81f8c-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="81f8c-123">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="81f8c-123">Click Start.</span></span>
    * <span data-ttu-id="81f8c-124">Overføring pågår.</span><span class="sxs-lookup"><span data-stu-id="81f8c-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="81f8c-125">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="81f8c-125">Click Complete.</span></span>
    * <span data-ttu-id="81f8c-126">Vare P0002 er nå tilgjengelig i plukklisten for kanban-jobben.</span><span class="sxs-lookup"><span data-stu-id="81f8c-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="81f8c-127">Dette betyr at vi kan forberede kanban med alle de nødvendige materialene.</span><span class="sxs-lookup"><span data-stu-id="81f8c-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="81f8c-128">Klikk på Klargjør.</span><span class="sxs-lookup"><span data-stu-id="81f8c-128">Click Prepare.</span></span>
    * <span data-ttu-id="81f8c-129">Legg merke til at et ikon i jobbstatusen angir at jobben er klar.</span><span class="sxs-lookup"><span data-stu-id="81f8c-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

