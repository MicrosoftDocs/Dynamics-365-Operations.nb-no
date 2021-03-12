---
title: Vurderingsprofiler
description: Dette emnet beskriver hvordan du setter opp data for vurderingsprofiler.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973966"
---
# <a name="rating-profiles"></a><span data-ttu-id="a508c-103">Vurderingsprofiler</span><span class="sxs-lookup"><span data-stu-id="a508c-103">Rating profiles</span></span>

<span data-ttu-id="a508c-104">En vurderingsprofil ligner en logistikkontrakt (men ikke en gyldig kontrakt).</span><span class="sxs-lookup"><span data-stu-id="a508c-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="a508c-105">Den brukes til å fastsette transporttariffer for last.</span><span class="sxs-lookup"><span data-stu-id="a508c-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="a508c-106">Hver vurderingsprofil er unik for en transportør.</span><span class="sxs-lookup"><span data-stu-id="a508c-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="a508c-107">I profilen kan du tilknytte transportøren til en vurderingsstandard.</span><span class="sxs-lookup"><span data-stu-id="a508c-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="a508c-108">Vurderingsstandarden definerer tilordningen av satsgrunnlag og satsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="a508c-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="a508c-109">Satsgrunnlaget angir satsen til transportøren.</span><span class="sxs-lookup"><span data-stu-id="a508c-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="a508c-110">Du kan definere en vurderingsprofil ved hjelp av et generisk side som gir en oversikt over alle eksisterende vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="a508c-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="a508c-111">Du kan også definere en vurderingsprofil direkte fra transportøren.</span><span class="sxs-lookup"><span data-stu-id="a508c-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="a508c-112">I begge tilfeller er informasjonen du angir for vurderingsprofilen, den samme.</span><span class="sxs-lookup"><span data-stu-id="a508c-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="a508c-113">Opprette eller redigere en vurderingsprofil på Vurderingsprofiler-siden</span><span class="sxs-lookup"><span data-stu-id="a508c-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="a508c-114">På siden **Vurderingsprofiler** kan du se gjennom alle tilgjengelige vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="a508c-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="a508c-115">Du kan også redigere eksisterende profiler og opprette nye profiler.</span><span class="sxs-lookup"><span data-stu-id="a508c-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="a508c-116">Gå til **Transportstyring \> Oppsett \> Vurdering \> Vurderingsprofil**.</span><span class="sxs-lookup"><span data-stu-id="a508c-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="a508c-117">Velg **Ny** i handlingsruten for å legge til en ny vurderingsprofil i rutenettet, eller velg **Rediger** for å redigere en eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="a508c-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="a508c-118">I raden for den nye eller eksisterende vurderingsprofilen angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="a508c-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="a508c-119">**Vurderingsprofil** – Angi en unik identifikator (ID) for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a508c-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="a508c-120">**Navn** – Angi et beskrivende navn for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a508c-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="a508c-121">**Transportør** – Velg en transportør.</span><span class="sxs-lookup"><span data-stu-id="a508c-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="a508c-122">Vurderingsprofilen du konfigurerer, vises også på **Transportører**-siden for den valgte transportøren.</span><span class="sxs-lookup"><span data-stu-id="a508c-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="a508c-123">**Område** og **Lager** – Velg et område og lager.</span><span class="sxs-lookup"><span data-stu-id="a508c-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="a508c-124">**Ratemotor** – Velg ratemotoren for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a508c-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="a508c-125">**Vurderingsstandard** – Velg vurderingsstandarden for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a508c-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="a508c-126">Du kan bruke vurderingsstandarden til å definere en satsgrunnlagstype og et satsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="a508c-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="a508c-127">Hvis du vil ha mer informasjon, kan du se [Definere vurderingsstandarder](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="a508c-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="a508c-128">**Transittidmotor** – Velg transittidmotoren for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a508c-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="a508c-129">**Drivstoffindeks for transportør** – Velg vurderingsprofilens drivstoffindeks for transportør.</span><span class="sxs-lookup"><span data-stu-id="a508c-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="a508c-130">**Startdato og -klokkeslett for virkning** og **Sluttdato og -klokkeslett for virkning** – Definer perioden når vurderingsprofilen skal være aktiv.</span><span class="sxs-lookup"><span data-stu-id="a508c-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="a508c-131">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a508c-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="a508c-132">Opprette en vurderingsprofil direkte på Transportører-siden</span><span class="sxs-lookup"><span data-stu-id="a508c-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="a508c-133">Gå til **Transportstyring \> Oppsett \> Transpotører \> Transportører**.</span><span class="sxs-lookup"><span data-stu-id="a508c-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="a508c-134">Velg en transportør i listen.</span><span class="sxs-lookup"><span data-stu-id="a508c-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="a508c-135">Velg **Ny** i hurtigfanen **Vurderingsprofiler** for å opprette en vurderingsprofil.</span><span class="sxs-lookup"><span data-stu-id="a508c-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="a508c-136">Angi feltene for den nye vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a508c-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="a508c-137">Disse feltene tilsvarer feltene på siden **Vurderingsprofiler**, som beskrevet i forrige del av dette emnet.</span><span class="sxs-lookup"><span data-stu-id="a508c-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="a508c-138">Profiler som opprettes på **Transportører**-siden, vises også på **Vurderingsprofiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="a508c-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
