---
title: Livsløpstilstander for aktiva
description: Dette emnet forklarer livsløpstilstander for aktiva og livsløpsmodeller i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889919"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="c2f20-103">Livsløpstilstander for aktiva</span><span class="sxs-lookup"><span data-stu-id="c2f20-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c2f20-104">Dette emnet forklarer livsløpstilstander for aktiva og livsløpsmodeller i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="c2f20-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="c2f20-105">Livsløpstilstander for aktiva brukes til å definere om aktivaet er aktivt eller inaktivt.</span><span class="sxs-lookup"><span data-stu-id="c2f20-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="c2f20-106">Du kan for eksempel definere livsløpstilstander for aktiva, blant annet **Opprettet**, **Aktiv** og **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="c2f20-107">Livsløpstilstander for forespørsel er knyttet til livsløpstilstander for aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="c2f20-108">Når en forespørsel endres til en ny livsløpstilstand for forespørsel, endres derfor aktivumet som er knyttet til forespørselen, til en ny livsløpstilstand for aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="c2f20-109">Hvis for eksempel livsløpstilstanden for en forespørsel endres til **Inngående**, endres livsløpstilstanden til det tilknyttede anleggsmidlet til livsløpstilstanden som er valgt i feltet **Innkommende livsløpstilstand** på hurtigfanen **Livsløpstilstand for aktiva** på siden **Livsløpstilstand for aktivamodeller**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="c2f20-110">Livsløpstilstander for aktiva kan defineres i livsløpsmodeller for aktiva, der du kan definere de nødvendige livsløpstilstandene for ulike typer aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="c2f20-111">Du setter først opp livsløpstilstander.</span><span class="sxs-lookup"><span data-stu-id="c2f20-111">You first set up lifecycle states.</span></span> <span data-ttu-id="c2f20-112">Deretter oppretter du en livsløpsmodell og velger livsløpstilstander for den.</span><span class="sxs-lookup"><span data-stu-id="c2f20-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="c2f20-113">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="c2f20-114">Velg **Ny** for å opprette en ny livsløpstilstand.</span><span class="sxs-lookup"><span data-stu-id="c2f20-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="c2f20-115">I feltet **Livsløpstilstand** angir du ID-en for livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="c2f20-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="c2f20-116">Angi en beskrivelse i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f20-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="c2f20-117">Feltet **Livsløpsmodeller** viser antall livsløpsmodeller for aktiva som bruker livsløpstilstanden for aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="c2f20-118">Angi **Aktiv** til **Ja** hvis denne livsløpstilstanden skal være en aktiv livsløpstilstand (med andre ord om arbeidsordrer kan opprettes for aktiva som er i denne livsløpstilstanden).</span><span class="sxs-lookup"><span data-stu-id="c2f20-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="c2f20-119">Sett alternativet **Slett åpne kalenderlinjer** til **Ja** hvis åpne aktivakalenderlinjer som har livsløpstilstanden **Opprettet**, skal slettes når de er i denne livsløpstilstanden.</span><span class="sxs-lookup"><span data-stu-id="c2f20-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="c2f20-120">Denne innstillingen er nyttig hvis du vil rydde opp i eventuelle åpne vedlikeholdsplaner som ikke lenger er relevante for aktivaet (for eksempel hvis aktivaet ikke lenger er aktiv).</span><span class="sxs-lookup"><span data-stu-id="c2f20-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="c2f20-121">Livsløpstilstander for aktiva, livsløpsmodeller for aktiva og aktivatyper er relatert.</span><span class="sxs-lookup"><span data-stu-id="c2f20-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="c2f20-122">De brukes på samme måte som livsløpstilstander for arbeidsordrer, livsløpsmodeller for arbeidsordrer og arbeidsordretyper.</span><span class="sxs-lookup"><span data-stu-id="c2f20-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="c2f20-123">Når du har opprettet de nødvendige livsløpstilstandene for aktiva, kan du definere livsløpstilstander i livsløpsmodeller for aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="c2f20-124">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livsløpsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="c2f20-125">Velg **Ny** for å opprette en ny livsløpsmodell.</span><span class="sxs-lookup"><span data-stu-id="c2f20-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="c2f20-126">I feltet **Livsløpsmodell** angir du ID-en for livsløpsmodellen.</span><span class="sxs-lookup"><span data-stu-id="c2f20-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="c2f20-127">Angi en beskrivelse i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2f20-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="c2f20-128">Feltet **Livsløpstilstander** viser antall livsløpstilstander for aktiva som er valgt i livsløpsmodellen for aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="c2f20-129">Feltet **Aktivatyper** viser antall aktivatyper som bruker livsløpsmodellen.</span><span class="sxs-lookup"><span data-stu-id="c2f20-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="c2f20-130">I hurtigfanen **Livsløpstilstander** velger du livsløpstilstandene for aktiva som skal inkluderes i livsløpsmodellen for aktiva:</span><span class="sxs-lookup"><span data-stu-id="c2f20-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="c2f20-131">Hvis du vil bruke en livsløpstilstand for modellen, velger du den i delen **Gjenværende livsløpstilstander**, og deretter velger du pil høyre ![Pil høyre](media/15-setup-for-objects.png) for å flytte den til delen **Valgte livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c2f20-132">Hvis du vil bruke alle tilgjengelige livsløpstilstander for modellen, velger du **Alle tilgjengelige livsløpstilstander**-knappen ![Alle tilgjengelige livsløpstilstander](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="c2f20-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="c2f20-133">Alle livsløpstilstander overføres til delen **Valgte livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c2f20-134">Hvis du vil fjerne en livsløpstilstand fra modellen, velger du den i delen **Valgte livsløpstilstander**, og deretter velger du pil venstre ![Pil venstre](media/16-setup-for-objects.png) for å flytte den til delen **Gjenværende livsløpstilstander**.</span><span class="sxs-lookup"><span data-stu-id="c2f20-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="c2f20-135">Velg **Oppdateringer av livsløpstilstander** for å definere livsløpstilstander for aktiva som kan følge en valgt livsløpstilstand.</span><span class="sxs-lookup"><span data-stu-id="c2f20-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="c2f20-136">Du bruker hurtigfanen **Aktiva** hvis du håndterer aktiva du mottar for reparasjon.</span><span class="sxs-lookup"><span data-stu-id="c2f20-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="c2f20-137">I delen **Innkommende/utgående** kan du velge livsløpstilstander for aktiva for å angi arbeidsflyten for et aktivum du mottar for reparasjon.</span><span class="sxs-lookup"><span data-stu-id="c2f20-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="c2f20-138">Hvis du tilbyr lån av aktiva til kunder eller avdelinger i **Lån**-delen, kan du velge livsløpstilstander for lånte aktiva.</span><span class="sxs-lookup"><span data-stu-id="c2f20-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
