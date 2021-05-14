---
title: Vise, behandle og godkjenne planlagte bestillinger
description: Dette emnet inneholder informasjon om hvordan du viser, behandler og godkjenner planlagte ordrer i planleggingsoptimalisering.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935663"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="79f5e-103">Vise, behandle og godkjenne planlagte bestillinger</span><span class="sxs-lookup"><span data-stu-id="79f5e-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79f5e-104">Dette emnet inneholder informasjon om hvordan du viser, behandler og godkjenner planlagte ordrer i planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="79f5e-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="79f5e-105">Vise og behandle planlagte bestillinger</span><span class="sxs-lookup"><span data-stu-id="79f5e-105">View and manage planned orders</span></span>

<span data-ttu-id="79f5e-106">Du kan vise og administrere planlagte bestillinger på en hvilken som helst listeside med planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="79f5e-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="79f5e-107">Gå til et av følgende steder, avhengig av hvilken type planlagte bestillinger du vil arbeide med:</span><span class="sxs-lookup"><span data-stu-id="79f5e-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="79f5e-108">Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="79f5e-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="79f5e-109">Hovedplanlegging \> Hovedplanlegging \> Planlagte bestillinger</span><span class="sxs-lookup"><span data-stu-id="79f5e-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="79f5e-110">Produksjonskontroll \> Produksjonsordrer \> Planlagte produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="79f5e-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="79f5e-111">Innkjøp og leverandører \> Bestillinger \> Planlagte bestillinger</span><span class="sxs-lookup"><span data-stu-id="79f5e-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="79f5e-112">Lagerstyring \> Innkommende ordrer \> Planlagte overføringer</span><span class="sxs-lookup"><span data-stu-id="79f5e-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="79f5e-113">Lagerstyring \> Utgående ordrer \> Planlagte overføringer</span><span class="sxs-lookup"><span data-stu-id="79f5e-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="79f5e-114">Vis og rediger statusen for planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="79f5e-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="79f5e-115">Du kan bruke **Status**-feltet for hver planlagte bestilling til å spore fremdriften eller endre hvordan en planlagt bestilling skal behandles.</span><span class="sxs-lookup"><span data-stu-id="79f5e-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="79f5e-116">Følgende verdier for **Status** er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="79f5e-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="79f5e-117">**Ubehandlet** – Når hovedplanlegging genererer planlagte ordrer, gis de denne statusen.</span><span class="sxs-lookup"><span data-stu-id="79f5e-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="79f5e-118">Planlagte ordrer med denne statusen blir slettet under neste planleggingskjøring.</span><span class="sxs-lookup"><span data-stu-id="79f5e-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="79f5e-119">**Fullført** – Denne statusen angir at den planlagte bestillingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="79f5e-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="79f5e-120">Hvis du velger ikke å bekrefte en planlagt bestilling, kan du endre statusen manuelt til *Fullført*.</span><span class="sxs-lookup"><span data-stu-id="79f5e-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="79f5e-121">Legg merke til at systemet behandler statusene *Ubehandlet* og *Fullført* på samme måte.</span><span class="sxs-lookup"><span data-stu-id="79f5e-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="79f5e-122">**Godkjent** – Denne statusen angir at den planlagte bestillingen er godkjent for autorisering.</span><span class="sxs-lookup"><span data-stu-id="79f5e-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="79f5e-123">Hvis du vil autorisere en planlagt ordre, kan du endre statusen til *Godkjent*.</span><span class="sxs-lookup"><span data-stu-id="79f5e-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="79f5e-124">Hvis du vil beholde endringene som er gjort i en planlagt bestilling, eller hvis du planlegger å autorisere en planlagt bestilling, endrer du statusen til *Godkjent*.</span><span class="sxs-lookup"><span data-stu-id="79f5e-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="79f5e-125">Planlagte bestillinger med status *Godkjent* betraktes som fast og forventet forsyning i hovedplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="79f5e-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="79f5e-126">Derfor blir de ikke endret eller slettet i løpet av senere hovedplanleggingskjøringer.</span><span class="sxs-lookup"><span data-stu-id="79f5e-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="79f5e-127">For å oppnå denne atferden kopierer planleggingslogikken planlagte ordrer med statusen *Godkjent* fra den gamle planversjonen til den nye planversjonen under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="79f5e-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="79f5e-128">Legg merke til at planlaget ordrer med statusen *Godkjent* bare regnes som forsyning i den bestemte hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="79f5e-128">Note that planned orders that have a status of *Approved*\* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="79f5e-129">Hvis du vil endre statusen for én enkelt planlagt bestilling, [åpner du en listeside for planlagte bestillinger](#view-planned-orders), åpner ordren og følger deretter ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="79f5e-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="79f5e-130">I hurtigkategorien **Generelt** endrer du verdien for **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f5e-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="79f5e-131">I handlingsruten i fanen **Planlagt ordre** **Behandle**-gruppen velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="79f5e-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="79f5e-132">Hvis du vil merke orden som godkjent, velger du **Godkjenn** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="79f5e-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="79f5e-133">Hvis du vil endre statusen for flere planlagte bestillinger samtidig, [åpner du en listeside for planlagte ordrer](#view-planned-orders), merker av for hver ordre du vil endre, og deretter følger ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="79f5e-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="79f5e-134">I handlingsruten i fanen **Planlagt ordre** **Behandle**-gruppen velger du **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="79f5e-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="79f5e-135">Hvis du vil merke ordrene som godkjent, velger du **Godkjenn** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="79f5e-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="79f5e-136">Godkjenn planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="79f5e-136">Approve planned orders</span></span>

<span data-ttu-id="79f5e-137">Godkjenning av planlagte ordrer er et valgfritt trinn i prosessen med å opprette en autorisert ordre fra en planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="79f5e-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="79f5e-138">Illustrasjonen nedenfor viser hvordan du kan bruke **Status**-verdien som er tilordnet hver planlagte ordre, til å implementere en godkjenningsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="79f5e-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="79f5e-139">Når du skal implementere en godkjenningsprosess, justerer du **Status**-verdien manuelt for hver planlagte ordre som beskrevet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="79f5e-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Planlagt ordreflyt](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="79f5e-141">Det anbefales at du godkjenner alle endrede planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="79f5e-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="79f5e-142">Ellers blir endringene ignorert og overskrevet av neste planleggingskjøring.</span><span class="sxs-lookup"><span data-stu-id="79f5e-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79f5e-143">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="79f5e-143">Additional resources</span></span>

- [<span data-ttu-id="79f5e-144">Autoriser planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="79f5e-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
