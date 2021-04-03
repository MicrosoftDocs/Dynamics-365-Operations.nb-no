---
title: Tilbakestill Kanban-jobbstatus
description: Denne prosedyren fokuserer på å tilbakestille en ugyldig Kanban-jobbstatus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94618494b9c338ed27b2558c91dc662c853d3cda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261100"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="60057-103">Tilbakestill Kanban-jobbstatus</span><span class="sxs-lookup"><span data-stu-id="60057-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60057-104">Denne prosedyren fokuserer på å tilbakestille en ugyldig Kanban-jobbstatus.</span><span class="sxs-lookup"><span data-stu-id="60057-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="60057-105">Dette er nyttig hvis maskinoperatøren oppdaterer feil jobb, eller angir feil status ved en feiltakelse.</span><span class="sxs-lookup"><span data-stu-id="60057-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="60057-106">I denne prosedyren er Kanban-jobben registrert som klargjort ved et uhell, og statusen tilbakestilles.</span><span class="sxs-lookup"><span data-stu-id="60057-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="60057-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="60057-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="60057-108">Denne prosedyren er ment for verkstedsleder eller maskinoperatør som arbeider i et lean manufacturing-firma.</span><span class="sxs-lookup"><span data-stu-id="60057-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="60057-109">Åpne prosesstavlen for arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="60057-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="60057-110">Gå til Kanban-tavle for prosessjobber.</span><span class="sxs-lookup"><span data-stu-id="60057-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="60057-111">Angi eller velg en verdi i Arbeidscelle-feltet.</span><span class="sxs-lookup"><span data-stu-id="60057-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="60057-112">Velg arbeidscellen 1260.</span><span class="sxs-lookup"><span data-stu-id="60057-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="60057-113">Klargjør kanban-jobben</span><span class="sxs-lookup"><span data-stu-id="60057-113">Prepare kanban job</span></span>
1. <span data-ttu-id="60057-114">Klikk på Klargjør.</span><span class="sxs-lookup"><span data-stu-id="60057-114">Click Prepare.</span></span>
    * <span data-ttu-id="60057-115">Hvis du ikke kan klikke Klargjør fordi det er nedtonet, må du kontrollere at den valgte Kanban-jobben har statusen Planlagt, som er angitt av Tøm Kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="60057-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="60057-116">Hvis Klargjør mislykkes, må du kontrollere at alle materialene i plukklisten er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="60057-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="60057-117">Velg den klargjorte jobben i listen.</span><span class="sxs-lookup"><span data-stu-id="60057-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="60057-118">Velg den første jobben som du nettopp har klargjort.</span><span class="sxs-lookup"><span data-stu-id="60057-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="60057-119">Legg merke til at jobbstatusen er klargjort, noe som angis med en trekant inni Kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="60057-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="60057-120">Tilbakestill statusen for klargjorte Kanban-jobben</span><span class="sxs-lookup"><span data-stu-id="60057-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="60057-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="60057-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="60057-122">Velg den første jobben som ble klargjort.</span><span class="sxs-lookup"><span data-stu-id="60057-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="60057-123">Klikk på Produksjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="60057-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="60057-124">Klikk på Tilbakestill status.</span><span class="sxs-lookup"><span data-stu-id="60057-124">Click Revert status.</span></span>
    * <span data-ttu-id="60057-125">Du kan bruke en alternativ Kanban-regel når følgende betingelser er oppfylt: – Strategien for etterfylling er den samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="60057-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="60057-126">- Versjonen for produksjonsflyten er den samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="60057-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="60057-127">- Produktet som leveres, er det samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="60057-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="60057-128">- Nedstrømsaktiviteter som konfigureres for den siste aktiviteten i Kanban-reglene, må være de samme for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="60057-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="60057-129">- De samme lagerdimensjonene som er angitt, må konfigureres for begge reglene.</span><span class="sxs-lookup"><span data-stu-id="60057-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="60057-130">- Statusen for håndteringsenheten må være Ikke tilordnet.</span><span class="sxs-lookup"><span data-stu-id="60057-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="60057-131">- Konfigurasjonen for hendelses-Kanbaner må være den samme.</span><span class="sxs-lookup"><span data-stu-id="60057-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="60057-132">Kontroller at den nye statusen er Planlagt.</span><span class="sxs-lookup"><span data-stu-id="60057-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="60057-133">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="60057-133">Click OK.</span></span>
5. <span data-ttu-id="60057-134">Fjern merket for den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="60057-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="60057-135">Velg den samme jobben.</span><span class="sxs-lookup"><span data-stu-id="60057-135">Select the same job.</span></span>  
    * <span data-ttu-id="60057-136">Legg merke til at jobbstatusen for Kanban-jobben tilbakestilles til Planlagt, som angis av Tøm Kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="60057-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]