---
title: Livssyklustilstander for aktiva
description: Dette emnet forklarer livssyklustilstander for aktiva og livssyklusmodeller i Aktivastyring.
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
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64be80777991a9fa674ef494cea103a602c7559f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230134"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="591a5-103">Livssyklustilstander for aktiva</span><span class="sxs-lookup"><span data-stu-id="591a5-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="591a5-104">Dette emnet forklarer livssyklustilstander for aktiva og livssyklusmodeller i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="591a5-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="591a5-105">Livssyklustilstander for aktiva brukes til å definere om aktivumet er aktivt eller inaktivt.</span><span class="sxs-lookup"><span data-stu-id="591a5-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="591a5-106">Du kan for eksempel definere livssyklustilstander for aktiva, blant annet **Opprettet**, **Aktiv** og **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="591a5-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="591a5-107">Livssyklustilstander for forespørsel er knyttet til livssyklustilstander for aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="591a5-108">Når en forespørsel endres til en ny livssyklustilstand for forespørsel, endres derfor aktivumet som er knyttet til forespørselen, til en ny livssyklustilstand for aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="591a5-109">Hvis for eksempel livssyklustilstanden for en forespørsel endres til **Inngående**, endres livssyklustilstanden til det tilknyttede anleggsmidlet til livssyklustilstanden som er valgt i feltet **Innkommende livssyklustilstand** på hurtigfanen **Livssyklustilstand for aktiva** på siden **Livssyklustilstand for aktivamodeller**.</span><span class="sxs-lookup"><span data-stu-id="591a5-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="591a5-110">Livssyklustilstander for aktiva kan defineres i livssyklusmodeller for aktiva, der du kan definere de nødvendige livssyklustilstandene for ulike typer aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="591a5-111">Du setter først opp livssyklustilstander.</span><span class="sxs-lookup"><span data-stu-id="591a5-111">You first set up lifecycle states.</span></span> <span data-ttu-id="591a5-112">Deretter oppretter du en livssyklusmodell og velger livssyklustilstander for den.</span><span class="sxs-lookup"><span data-stu-id="591a5-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="591a5-113">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="591a5-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="591a5-114">Velg **Ny** for å opprette en ny livssyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="591a5-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="591a5-115">I feltet **Livssyklustilstand** angir du ID-en for livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="591a5-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="591a5-116">Angi en beskrivelse i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="591a5-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="591a5-117">Feltet **Livssyklusmodeller** viser antall livssyklusmodeller for aktiva som bruker livssyklustilstanden for aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="591a5-118">Angi **Aktiv** til **Ja** hvis denne livssyklustilstanden skal være en aktiv livssyklustilstand (med andre ord om arbeidsordrer kan opprettes for aktiva som er i denne livssyklustilstanden).</span><span class="sxs-lookup"><span data-stu-id="591a5-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="591a5-119">Sett alternativet **Slett åpne kalenderlinjer** til **Ja** hvis åpne aktivakalenderlinjer som har livssyklustilstanden **Opprettet**, skal slettes når de er i denne livssyklustilstanden.</span><span class="sxs-lookup"><span data-stu-id="591a5-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="591a5-120">Denne innstillingen er nyttig hvis du vil rydde opp i eventuelle åpne vedlikeholdsplaner som ikke lenger er relevante for aktivumet (for eksempel hvis aktivumet ikke lenger er aktiv).</span><span class="sxs-lookup"><span data-stu-id="591a5-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="591a5-121">Livssyklustilstander for aktiva, livssyklusmodeller for aktiva og aktivatyper er relatert.</span><span class="sxs-lookup"><span data-stu-id="591a5-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="591a5-122">De brukes på samme måte som livssyklustilstander for arbeidsordrer, livssyklusmodeller for arbeidsordrer og arbeidsordretyper.</span><span class="sxs-lookup"><span data-stu-id="591a5-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="591a5-123">Når du har opprettet de nødvendige livssyklustilstandene for aktiva, kan du definere livssyklustilstander i livssyklusmodeller for aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="591a5-124">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livssyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="591a5-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="591a5-125">Velg **Ny** for å opprette en ny livssyklusmodell.</span><span class="sxs-lookup"><span data-stu-id="591a5-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="591a5-126">I feltet **Livssyklusmodell** angir du ID-en for livssyklusmodellen.</span><span class="sxs-lookup"><span data-stu-id="591a5-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="591a5-127">Angi en beskrivelse i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="591a5-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="591a5-128">Feltet **Livssyklustilstander** viser antall livssyklustilstander for aktiva som er valgt i livssyklusmodellen for aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="591a5-129">Feltet **Aktivatyper** viser antall aktivatyper som bruker livssyklusmodellen.</span><span class="sxs-lookup"><span data-stu-id="591a5-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="591a5-130">I hurtigfanen **Livssyklustilstander** velger du livssyklustilstandene for aktiva som skal inkluderes i livssyklusmodellen for aktiva:</span><span class="sxs-lookup"><span data-stu-id="591a5-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="591a5-131">Hvis du vil bruke en livssyklustilstand for modellen, velger du den i delen **Gjenværende livssyklustilstander**, og deretter velger du pil høyre ![Pil høyre](media/15-setup-for-objects.png) for å flytte den til delen **Valgte livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="591a5-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="591a5-132">Hvis du vil bruke alle tilgjengelige livssyklustilstander for modellen, velger du **Alle tilgjengelige livssyklustilstander**-knappen ![Alle tilgjengelige livssyklustilstander](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="591a5-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="591a5-133">Alle livssyklustilstander overføres til delen **Valgte livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="591a5-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="591a5-134">Hvis du vil fjerne en livssyklustilstand fra modellen, velger du den i delen **Valgte livssyklustilstander**, og deretter velger du pil venstre ![Pil venstre](media/16-setup-for-objects.png) for å flytte den til delen **Gjenværende livssyklustilstander**.</span><span class="sxs-lookup"><span data-stu-id="591a5-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="591a5-135">Velg **Oppdateringer av livssyklustilstander** for å definere livssyklustilstander for aktiva som kan følge en valgt livssyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="591a5-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="591a5-136">Du bruker hurtigfanen **Aktiva** hvis du håndterer aktiva du mottar for reparasjon.</span><span class="sxs-lookup"><span data-stu-id="591a5-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="591a5-137">I delen **Innkommende/utgående** kan du velge livssyklustilstander for aktiva for å angi arbeidsflyten for et aktivum du mottar for reparasjon.</span><span class="sxs-lookup"><span data-stu-id="591a5-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="591a5-138">Hvis du tilbyr lån av aktiva til kunder eller avdelinger i **Lån**-delen, kan du velge livssyklustilstander for lånte aktiva.</span><span class="sxs-lookup"><span data-stu-id="591a5-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]