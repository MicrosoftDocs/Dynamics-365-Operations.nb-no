---
title: Livsløpstilstander for vedlikeholdsanmodning
description: Dette emnet beskriver hvordan du definerer livsløpstilstander for vedlikeholdsanmodninger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 151db9ca8a121759e39b690ec296b36a18dc1729
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571168"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="3ec08-103">Livsløpstilstander for vedlikeholdsanmodning</span><span class="sxs-lookup"><span data-stu-id="3ec08-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="3ec08-104">Livsløpstilstander for vedlikeholdsanmodninger definerer stadiene som en forespørsel kan gå gjennom.</span><span class="sxs-lookup"><span data-stu-id="3ec08-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="3ec08-105">Eksempler er **Opprettet**, **Aktiv** og **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="3ec08-106">Når en vedlikeholdsanmondning konverteres til en arbeidsordre, bør livsløpstilstanden for vedlikeholdsanmodningen oppdateres til **Avsluttet** eller **Lukket** for å indikere at vedlikeholdsanmodningen ikke lenger er aktiv.</span><span class="sxs-lookup"><span data-stu-id="3ec08-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="3ec08-107">På listesiden **Alle vedlikeholdsanmodninger** kan du vise alle vedlikeholdsanmodninger, uavhengig av livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="3ec08-108">Definer livsløpstilstander for vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="3ec08-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="3ec08-109">Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="3ec08-110">Velg **Ny** for å opprette en livsløpstilstand for vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="3ec08-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="3ec08-111">I feltet **Livsløpstilstand** angir du en ID for livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="3ec08-112">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ec08-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="3ec08-113">På hurtigfanen **Detaljer** viser feltet **Livsløpsmodeller** viser antall livsløpsmodeller for vedlikeholdsanmodninger som bruker denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="3ec08-114">På hurtigfanen **Generelt** setter du alternativet **Aktiv** til **Ja** hvis en vedlikeholdsanmodning skal være aktiv mens den er i denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="3ec08-115">Angi alternativet **Angi faktisk slutt** til **Ja** hvis en faktisk sluttdato og et klokkeslett automatisk skal angis på en vedlikeholdsanmodning som er i denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="3ec08-116">Angi alternativet **Opprett arbeidsordre** til **Ja** hvis en arbeidsordre kan opprettes fra en vedlikeholdsanmodning som er i denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="3ec08-117">Sett alternativet **Slett** til **Ja** hvis en vedlikeholdsanmodning kan slettes mens den er i denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="3ec08-118">På hurtigfanen **Oppdater** er alternativene **Innkommende** og **Utgående** i **Aktiva**-delen relevante hvis du bruker depotreparasjon. Angi det aktuelle alternativet til **Ja** hvis livsløpstilstnaden for aktivaene som er valgt i en vedlikeholdsanmodning, skal oppdateres automatisk til **Innkommende** eller **Utgående** når livsløpstilstanden for denne vedlikeholdsanmodningen er angitt til **Innkommende** eller **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="3ec08-119">Illustrasjonen nedenfor viser et eksempel på siden **Livsløpstilstander for vedlikeholdsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Siden Livsløpstilstander for vedlikeholdsanmodning](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="3ec08-121">Livsløpstilstander for vedlikeholdsanmodninger, livsløpstilstandsgrupper og -typer er knyttet til, og brukes på samme måte som, livsløpstilstander for arbeidsordre, livsløpstilstandsgrupper og -typer.</span><span class="sxs-lookup"><span data-stu-id="3ec08-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="3ec08-122">Definer livsløpsmodeller for vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="3ec08-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="3ec08-123">Når du har opprettet livsløpstilstandene som kreves for vedlikeholdsanmodningene dine, kan de deles inn i livsløpstilstandsgrupper eller livsløpsmodeller.</span><span class="sxs-lookup"><span data-stu-id="3ec08-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="3ec08-124">Livsløpsmodeller for vedlikeholdsanmodninger brukes til å opprette flyten som kan brukes for ulike typer vedlikeholdsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="3ec08-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="3ec08-125">Som et minimum bør en standard livsløpsmodell for vedlikeholdsanmodninger opprettes.</span><span class="sxs-lookup"><span data-stu-id="3ec08-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="3ec08-126">Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Livsløpsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="3ec08-127">Velg **Ny** for å opprette en livsløpsmodell for vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="3ec08-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="3ec08-128">I feltet **Livsløpsmodell** angir du en ID for livsløpsmodellen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="3ec08-129">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ec08-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="3ec08-130">På hurtigfanen **Detaljer** viser feltet **Livsløpstilstander** viser antall livsløpstilstander som er valgt i denne livsløpsmodellen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="3ec08-131">Feltet **Typer vedlikeholdsanmodninger** viser antall typer vedlikeholdsanmodninger som bruker denne livsløpsmodellen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="3ec08-132">I hurtigfanen **Livsløpstilstander** velger du livsløpstilstandene som skal inkluderes i livsløpsmodellen:</span><span class="sxs-lookup"><span data-stu-id="3ec08-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="3ec08-133">Hvis du vil inkludere en livsløpstilstand i livsløpsmodellen, velger du den i delen **Gjenværende livsløpstilstander**, og deretter velger du pil høyre ![Pil høyre](media/03-setup-for-requests.png) for å flytte den til delen **Valgte livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="3ec08-134">Hvis du vil inkludere alle tilgjengelige livsløpstilstander i livsløpsmodellen, velger du **Velg alle tilgjengelige tilstander**-knappen ![Velg alle tilgjengelige tilstander](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="3ec08-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="3ec08-135">Alle livsløpstilstander flyttes til delen **Valgte livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="3ec08-136">Hvis du vil fjerne en livsløpstilstand fra livsløpsmodellen, velger du den i delen **Valgte livsløpstilstander**, og deretter velger du pil venstre ![Pil venstre](media/05-setup-for-requests.png) for å flytte den til delen **Gjenværende livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="3ec08-137">I hurtigfanen **Generelt** er feltene i delen **Oppdateringer** relevante hvis du bruker depotreparasjon.</span><span class="sxs-lookup"><span data-stu-id="3ec08-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="3ec08-138">I feltet **Livsløpstilstand for mottatt aktiva** velger du livsløpstilstanden som aktiva som er valgt i en vedlikeholdsanmodning skal oppdateres automatisk til når de mottas for depotreparasjon.</span><span class="sxs-lookup"><span data-stu-id="3ec08-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="3ec08-139">I feltet **Livsløpstilstand for levert aktiva** velger du livsløpstilstanden som aktiva som er valgt i en vedlikeholdsanmodning skal oppdateres automatisk til når de returneres etter reparasjon.</span><span class="sxs-lookup"><span data-stu-id="3ec08-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="3ec08-140">Illustrasjonen nedenfor viser et eksempel på siden **Livsløpsmodeller for vedlikeholdsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Siden Livsløpsmodeller for vedlikeholdsanmodning](media/06-setup-for-requests.png)
