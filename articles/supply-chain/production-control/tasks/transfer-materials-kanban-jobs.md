---
title: Overføre materialer med Kanban-jobber
description: Denne prosedyren fokuserer på å utføre en kanban-jobb for uttak for å overføre materialer.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df65ea59be29dbe4eaad30558fcff4394737158f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224936"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="8e62e-103">Overføre materialer med Kanban-jobber</span><span class="sxs-lookup"><span data-stu-id="8e62e-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e62e-104">Denne prosedyren fokuserer på å utføre en kanban-jobb for uttak for å overføre materialer.</span><span class="sxs-lookup"><span data-stu-id="8e62e-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="8e62e-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8e62e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8e62e-106">Denne fremgangsmåten er ment for Lagermedarbeideren.</span><span class="sxs-lookup"><span data-stu-id="8e62e-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="8e62e-107">Vis overføringsjobber</span><span class="sxs-lookup"><span data-stu-id="8e62e-107">Display transfer jobs</span></span>
1. <span data-ttu-id="8e62e-108">Gå til Produksjonskontroll > Kanban > Kanban-tavle for overføringsjobber.</span><span class="sxs-lookup"><span data-stu-id="8e62e-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="8e62e-109">Vis eller skjul delen Filtre.</span><span class="sxs-lookup"><span data-stu-id="8e62e-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="8e62e-110">I delen Filtre, kan du angi hvilke jobber som du vil se ved å filtrere etter produksjonsflyten, Aktivitetsnavn, fra lageret og lokasjonen, og til lager og lokasjon.</span><span class="sxs-lookup"><span data-stu-id="8e62e-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="8e62e-111">Skriv inn 11 i Fra lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e62e-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="8e62e-112">Skriv inn 12 i Til lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="8e62e-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="8e62e-113">Start en overføringsjobb</span><span class="sxs-lookup"><span data-stu-id="8e62e-113">Start a transfer job</span></span>
1. <span data-ttu-id="8e62e-114">I listen, fjerner du merket for den merkede raden - hvis det finnes.</span><span class="sxs-lookup"><span data-stu-id="8e62e-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="8e62e-115">Velg rad 4 i listen.</span><span class="sxs-lookup"><span data-stu-id="8e62e-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="8e62e-116">Velg den første jobben med statusen Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="8e62e-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="8e62e-117">Kontroller at dette er den eneste jobben som er valgt.</span><span class="sxs-lookup"><span data-stu-id="8e62e-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="8e62e-118">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="8e62e-118">Click Start.</span></span>
    * <span data-ttu-id="8e62e-119">Legg merke til at et ikon angir at jobben er startet.</span><span class="sxs-lookup"><span data-stu-id="8e62e-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="8e62e-120">Velg en annen overføringsjobb og endre antallet</span><span class="sxs-lookup"><span data-stu-id="8e62e-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="8e62e-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8e62e-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8e62e-122">Du kan har flere jobber som er valgt, men denne gangen velger du rad 5.</span><span class="sxs-lookup"><span data-stu-id="8e62e-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="8e62e-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8e62e-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8e62e-124">Kontroller at jobben i det forrige trinnet, er den eneste som er valgt.</span><span class="sxs-lookup"><span data-stu-id="8e62e-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="8e62e-125">Fjern merket for alle andre jobber.</span><span class="sxs-lookup"><span data-stu-id="8e62e-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="8e62e-126">Merk deg verdien i Jobbantall-feltet for senere bruk</span><span class="sxs-lookup"><span data-stu-id="8e62e-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="8e62e-127">Sett Jobbantall til 30.</span><span class="sxs-lookup"><span data-stu-id="8e62e-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="8e62e-128">Legg merke til advarselen.</span><span class="sxs-lookup"><span data-stu-id="8e62e-128">Notice the warning!</span></span> <span data-ttu-id="8e62e-129">Du kan ikke overføre 30.</span><span class="sxs-lookup"><span data-stu-id="8e62e-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="8e62e-130">Du kan bare overføre det opprinnelige antallet i henhold til oppsettet for kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="8e62e-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="8e62e-131">Bruk verdien du merket deg tidligere i Jobbantall-feltet</span><span class="sxs-lookup"><span data-stu-id="8e62e-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="8e62e-132">Sett jobbantallet til den forrige verdien.</span><span class="sxs-lookup"><span data-stu-id="8e62e-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="8e62e-133">Start den andre overføringsjobben</span><span class="sxs-lookup"><span data-stu-id="8e62e-133">Start the second transfer job</span></span>
1. <span data-ttu-id="8e62e-134">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="8e62e-134">Click Start.</span></span>
    * <span data-ttu-id="8e62e-135">Dette vil starte overføringen av jobben i rad 5.</span><span class="sxs-lookup"><span data-stu-id="8e62e-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="8e62e-136">Fullfør begge overføringsjobbene</span><span class="sxs-lookup"><span data-stu-id="8e62e-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="8e62e-137">Velg rad 4 i listen.</span><span class="sxs-lookup"><span data-stu-id="8e62e-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="8e62e-138">Nå er to overføringsjobber valgt i rad 4 og rad 5.</span><span class="sxs-lookup"><span data-stu-id="8e62e-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="8e62e-139">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="8e62e-139">Click Complete.</span></span>
    * <span data-ttu-id="8e62e-140">Dette vil fullføre overføringen av begge jobber.</span><span class="sxs-lookup"><span data-stu-id="8e62e-140">This will complete the transfer of both jobs.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]