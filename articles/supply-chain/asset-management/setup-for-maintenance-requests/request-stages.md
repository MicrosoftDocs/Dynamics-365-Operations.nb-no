---
title: Livssyklustilstander for melding
description: Dette emnet beskriver hvordan du definerer livssyklustilstander for meldinger i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9022d866bf0da08a72ba9169587f87c1b77527a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217227"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="af74d-103">Livssyklustilstander for melding</span><span class="sxs-lookup"><span data-stu-id="af74d-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="af74d-104">Livssyklustilstander for meldinger definerer stadiene som en forespørsel kan gå gjennom.</span><span class="sxs-lookup"><span data-stu-id="af74d-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="af74d-105">Eksempler er **Opprettet**, **Aktiv** og **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="af74d-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="af74d-106">Når en vedlikeholdsanmondning konverteres til en arbeidsordre, bør livssyklustilstanden for meldingen oppdateres til **Avsluttet** eller **Lukket** for å indikere at meldingen ikke lenger er aktiv.</span><span class="sxs-lookup"><span data-stu-id="af74d-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="af74d-107">På listesiden **Alle meldinger** kan du vise alle meldinger, uavhengig av livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="af74d-108">Definer livssyklustilstander for meldinger</span><span class="sxs-lookup"><span data-stu-id="af74d-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="af74d-109">Velg **Aktivastyring** \> **Oppsett** \> **Meldinger** \> **Livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="af74d-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="af74d-110">Velg **Ny** for å opprette en livssyklustilstand for melding.</span><span class="sxs-lookup"><span data-stu-id="af74d-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="af74d-111">I feltet **Livssyklustilstand** angir du en ID for livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="af74d-112">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="af74d-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="af74d-113">På hurtigfanen **Detaljer** viser feltet **Livssyklusmodeller** viser antall livssyklusmodeller for meldinger som bruker denne livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="af74d-114">På hurtigfanen **Generelt** setter du alternativet **Aktiv** til **Ja** hvis en melding skal være aktiv mens den er i denne livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="af74d-115">Angi alternativet **Angi faktisk slutt** til **Ja** hvis en faktisk sluttdato og et klokkeslett automatisk skal angis på en melding som er i denne livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="af74d-116">Angi alternativet **Opprett arbeidsordre** til **Ja** hvis en arbeidsordre kan opprettes fra en melding som er i denne livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="af74d-117">Sett alternativet **Slett** til **Ja** hvis en melding kan slettes mens den er i denne livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="af74d-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="af74d-118">I hurtigfanen **Oppdater** er de **inngående** og **utgående** alternativene i **Aktiva**-delen relevante hvis du bruker depotreparasjon.</span><span class="sxs-lookup"><span data-stu-id="af74d-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="af74d-119">Sett det riktige alternativet til **Ja** hvis livssyklustilstanden for aktivaene som er valgt i en vedlikeholdsforespørsel, automatisk skal oppdateres til **Inngående** eller **Utgående** når livssyklustilstanden for melding for vedlikeholdsforespørselen er satt til **Inngående** eller **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="af74d-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="af74d-120">Illustrasjonen nedenfor viser et eksempel på siden **Livssyklustilstander for melding**.</span><span class="sxs-lookup"><span data-stu-id="af74d-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Siden Livssyklustilstander for melding](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="af74d-122">Livssyklustilstander for meldinger, livssyklustilstandsgrupper og -typer er knyttet til, og brukes på samme måte som, livssyklustilstander for arbeidsordre, livssyklustilstandsgrupper og -typer.</span><span class="sxs-lookup"><span data-stu-id="af74d-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="af74d-123">Definer livssyklusmodeller for meldinger</span><span class="sxs-lookup"><span data-stu-id="af74d-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="af74d-124">Når du har opprettet livssyklustilstandene som kreves for meldingene dine, kan de deles inn i livssyklustilstandsgrupper eller livssyklusmodeller.</span><span class="sxs-lookup"><span data-stu-id="af74d-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="af74d-125">Livssyklusmodeller for meldinger brukes til å opprette flyten som kan brukes for ulike typer meldinger.</span><span class="sxs-lookup"><span data-stu-id="af74d-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="af74d-126">Som et minimum bør en standard livssyklusmodell for meldinger opprettes.</span><span class="sxs-lookup"><span data-stu-id="af74d-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="af74d-127">Velg **Aktivastyring** \> **Oppsett** \> **Meldinger** \> **Livssyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="af74d-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="af74d-128">Velg **Ny** for å opprette en livssyklusmodell for melding.</span><span class="sxs-lookup"><span data-stu-id="af74d-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="af74d-129">I feltet **Livssyklusmodell** angir du en ID for livssyklusmodellen.</span><span class="sxs-lookup"><span data-stu-id="af74d-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="af74d-130">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="af74d-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="af74d-131">På hurtigfanen **Detaljer** viser feltet **Livssyklustilstander** viser antall livssyklustilstander som er valgt i denne livssyklusmodellen.</span><span class="sxs-lookup"><span data-stu-id="af74d-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="af74d-132">Feltet **Typer meldinger** viser antall typer meldinger som bruker denne livssyklusmodellen.</span><span class="sxs-lookup"><span data-stu-id="af74d-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="af74d-133">I hurtigfanen **Livssyklustilstander** velger du livssyklustilstandene som skal inkluderes i livssyklusmodellen:</span><span class="sxs-lookup"><span data-stu-id="af74d-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="af74d-134">Hvis du vil inkludere en livssyklustilstand i livssyklusmodellen, velger du den i delen **Gjenværende livssyklustilstander**, og deretter velger du pil høyre ![Pil høyre](media/03-setup-for-requests.png) for å flytte den til delen **Valgte livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="af74d-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="af74d-135">Hvis du vil inkludere alle tilgjengelige livssyklustilstander i livssyklusmodellen, velger du **Velg alle tilgjengelige tilstander**-knappen ![Velg alle tilgjengelige tilstander](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="af74d-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="af74d-136">Alle livssyklustilstander flyttes til delen **Valgte livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="af74d-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="af74d-137">Hvis du vil fjerne en livssyklustilstand fra livssyklusmodellen, velger du den i delen **Valgte livssyklustilstander**, og deretter velger du pil venstre ![Pil venstre](media/05-setup-for-requests.png) for å flytte den til delen **Gjenværende livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="af74d-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="af74d-138">I hurtigfanen **Generelt** er feltene i delen **Oppdateringer** relevante hvis du bruker depotreparasjon.</span><span class="sxs-lookup"><span data-stu-id="af74d-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="af74d-139">I feltet **Livssyklustilstand for mottatt aktiva** velger du livssyklustilstanden som aktiva som er valgt i en melding skal oppdateres automatisk til når de mottas for depotreparasjon.</span><span class="sxs-lookup"><span data-stu-id="af74d-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="af74d-140">I feltet **Livssyklustilstand for levert aktiva** velger du livssyklustilstanden som aktiva som er valgt i en melding skal oppdateres automatisk til når de returneres etter reparasjon.</span><span class="sxs-lookup"><span data-stu-id="af74d-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="af74d-141">Illustrasjonen nedenfor viser et eksempel på siden **Livssyklusmodeller for melding**.</span><span class="sxs-lookup"><span data-stu-id="af74d-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Siden Livssyklusmodeller for melding](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]