---
title: Tilbakestill Kanban-jobbstatus
description: Denne prosedyren fokuserer på å tilbakestille en ugyldig Kanban-jobbstatus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27874f89cede151b52b869fa0d58e320d548e6d3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562213"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="30199-103">Tilbakestill Kanban-jobbstatus</span><span class="sxs-lookup"><span data-stu-id="30199-103">Revert kanban job status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30199-104">Denne prosedyren fokuserer på å tilbakestille en ugyldig Kanban-jobbstatus.</span><span class="sxs-lookup"><span data-stu-id="30199-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="30199-105">Dette er nyttig hvis maskinoperatøren oppdaterer feil jobb, eller angir feil status ved en feiltakelse.</span><span class="sxs-lookup"><span data-stu-id="30199-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="30199-106">I denne prosedyren er Kanban-jobben registrert som klargjort ved et uhell, og statusen tilbakestilles.</span><span class="sxs-lookup"><span data-stu-id="30199-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="30199-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="30199-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="30199-108">Denne prosedyren er ment for verkstedsleder eller maskinoperatør som arbeider i et lean manufacturing-firma.</span><span class="sxs-lookup"><span data-stu-id="30199-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="30199-109">Åpne prosesstavlen for arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="30199-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="30199-110">Gå til Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="30199-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="30199-111">Angi eller velg en verdi i Arbeidscelle-feltet.</span><span class="sxs-lookup"><span data-stu-id="30199-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="30199-112">Velg arbeidscellen 1260.</span><span class="sxs-lookup"><span data-stu-id="30199-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="30199-113">Klargjør kanban-jobben</span><span class="sxs-lookup"><span data-stu-id="30199-113">Prepare kanban job</span></span>
1. <span data-ttu-id="30199-114">Klikk Klargjør.</span><span class="sxs-lookup"><span data-stu-id="30199-114">Click Prepare.</span></span>
    * <span data-ttu-id="30199-115">Hvis du ikke kan klikke Klargjør fordi det er nedtonet, må du kontrollere at den valgte Kanban-jobben har statusen Planlagt, som er angitt av Tøm Kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="30199-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="30199-116">Hvis Klargjør mislykkes, må du kontrollere at alle materialene i plukklisten er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="30199-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="30199-117">Velg den klargjorte jobben i listen.</span><span class="sxs-lookup"><span data-stu-id="30199-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="30199-118">Velg den første jobben som du nettopp har klargjort.</span><span class="sxs-lookup"><span data-stu-id="30199-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="30199-119">Legg merke til at jobbstatusen er klargjort, noe som angis med en trekant inni Kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="30199-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="30199-120">Tilbakestill statusen for klargjorte Kanban-jobben</span><span class="sxs-lookup"><span data-stu-id="30199-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="30199-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="30199-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="30199-122">Velg den første jobben som ble klargjort.</span><span class="sxs-lookup"><span data-stu-id="30199-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="30199-123">Klikk Produksjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="30199-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="30199-124">Klikk Tilbakestill status.</span><span class="sxs-lookup"><span data-stu-id="30199-124">Click Revert status.</span></span>
    * <span data-ttu-id="30199-125">Du kan bruke en alternativ Kanban-regel når følgende betingelser er oppfylt: – Strategien for etterfylling er den samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="30199-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="30199-126">- Versjonen for produksjonsflyten er den samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="30199-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="30199-127">- Produktet som leveres, er det samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="30199-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="30199-128">- Nedstrømsaktiviteter som konfigureres for den siste aktiviteten i Kanban-reglene, må være de samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="30199-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="30199-129">- De samme lagerdimensjonene som er angitt, må konfigureres for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="30199-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="30199-130">- Statusen for håndteringsenheten må være Ikke tilordnet.</span><span class="sxs-lookup"><span data-stu-id="30199-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="30199-131">- Konfigurasjonen for hendelses-Kanbaner må være den samme.</span><span class="sxs-lookup"><span data-stu-id="30199-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="30199-132">Kontroller at den nye statusen er Planlagt.</span><span class="sxs-lookup"><span data-stu-id="30199-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="30199-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="30199-133">Click OK.</span></span>
5. <span data-ttu-id="30199-134">Fjern merket for den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="30199-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="30199-135">Velg den samme jobben.</span><span class="sxs-lookup"><span data-stu-id="30199-135">Select the same job.</span></span>  
    * <span data-ttu-id="30199-136">Legg merke til at jobbstatusen for Kanban-jobben tilbakestilles til Planlagt, som angis av Tøm Kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="30199-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

