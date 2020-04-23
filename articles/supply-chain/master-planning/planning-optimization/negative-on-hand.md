---
title: Planlegging med negative lagerbeholdningsantall
description: Dette emnet forklarer hvordan negativ beholdning håndteres når du bruker planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8803b0b90f22711b844442d16f717ab87dabf041
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209864"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="cfb4c-103">Planlegging med negative lagerbeholdningsantall</span><span class="sxs-lookup"><span data-stu-id="cfb4c-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfb4c-104">Hvis systemet viser et negativt antall av lagerbeholdningen, behandler planleggingsmotoren antallet som 0 (null) for å unngå overforsyning.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="cfb4c-105">Slik fungerer denne funksjonaliteten:</span><span class="sxs-lookup"><span data-stu-id="cfb4c-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="cfb4c-106">Funksjonen for planleggingsoptimalisering samler opp beholdningsantall på det laveste nivået av dekningsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="cfb4c-107">(Hvis *sted* for eksempel ikke er en dekningsdimensjon, samler planleggingsoptimalisering lagerbeholdningsantall på nivået *lager*.)</span><span class="sxs-lookup"><span data-stu-id="cfb4c-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="cfb4c-108">Hvis det samlede lagerbeholdningsantallet på det laveste nivået av dekningsdimensjoner er negativt, forutsetter systemet at beholdningsantallet virkelig er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cfb4c-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfb4c-109">Planleggingssystemet kan bare være like nøyaktig som inndataene.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="cfb4c-110">Hvis inndataene er unøyaktige, vil negative lagerposter vise at beholdningsinformasjonen i Microsoft Dynamics 365 Supply Chain Management ikke er synkronisert med den virkelige verden.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="cfb4c-111">Derfor vil planleggingsresultatet bli feil.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="cfb4c-112">Hvis du vil ha et nøyaktig planleggingsresultat, må du minimere antallet poster som viser et negativt beholdningsantall.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="cfb4c-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="cfb4c-113">Example 1</span></span>

<span data-ttu-id="cfb4c-114">Lager 13 konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="cfb4c-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="cfb4c-115">**Dekningskode:** Min/maks</span><span class="sxs-lookup"><span data-stu-id="cfb4c-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="cfb4c-116">**Minimum:** 15 stykker (stk.)</span><span class="sxs-lookup"><span data-stu-id="cfb4c-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="cfb4c-117">**Maksimum:** 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="cfb4c-118">Det laveste nivået av dekningsdimensjoner er *lager*, og følgende lagerbeholdninger registreres på nivået *sted*:</span><span class="sxs-lookup"><span data-stu-id="cfb4c-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="cfb4c-119">**Område 1, lager 13, sted 1:** 20 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="cfb4c-120">**Område 1, lager 13, sted 2:** &minus;8 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="cfb4c-121">Derfor er det totale beholdningsantallet 12 stk. for lager 13.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="cfb4c-122">(= 20 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-122">(= 20 pcs.</span></span> <span data-ttu-id="cfb4c-123">&minus; 8 stk.).</span><span class="sxs-lookup"><span data-stu-id="cfb4c-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="cfb4c-124">I dette tilfellet bruker planleggingsmotoren et samlet lagerbeholdningsantall på 12 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="cfb4c-125">for lager 13.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-125">for warehouse 13.</span></span>

<span data-ttu-id="cfb4c-126">Resultatet er en planlagt bestilling på 13 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="cfb4c-127">(= 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-127">(= 25 pcs.</span></span> <span data-ttu-id="cfb4c-128">&minus; 12 stk.) for å fylle på lager 13 fra 12 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="cfb4c-129">til 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="cfb4c-130">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="cfb4c-130">Example 2</span></span>

<span data-ttu-id="cfb4c-131">Lager 13 konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="cfb4c-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="cfb4c-132">**Dekningskode:** Min/maks</span><span class="sxs-lookup"><span data-stu-id="cfb4c-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="cfb4c-133">**Minimum:** 15 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="cfb4c-134">**Maksimum:** 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="cfb4c-135">Det laveste nivået av dekningsdimensjoner er *lager*, og følgende lagerbeholdninger registreres på nivået *sted*:</span><span class="sxs-lookup"><span data-stu-id="cfb4c-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="cfb4c-136">**Område 1, lager 13, sted 1:** 4 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="cfb4c-137">**Område 1, lager 13, sted 2:** &minus;8 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="cfb4c-138">Derfor er det totale beholdningsantallet &minus;4 stk. for lager 13.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="cfb4c-139">(= 4 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-139">(= 4 pcs.</span></span> <span data-ttu-id="cfb4c-140">&minus; 8 stk.).</span><span class="sxs-lookup"><span data-stu-id="cfb4c-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="cfb4c-141">Det er med andre ord mindre enn 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cfb4c-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="cfb4c-142">I dette tilfellet forutsetter planleggingsmotoren at beholdningen for lager 13 er 0 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="cfb4c-143">i stedet for &minus;4 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="cfb4c-144">Resultatet er en planlagt bestilling på 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="cfb4c-145">(= 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-145">(= 25 pcs.</span></span> <span data-ttu-id="cfb4c-146">&minus; 0 stk.) for å fylle på lager 13 fra 0 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="cfb4c-147">til 25 stk.</span><span class="sxs-lookup"><span data-stu-id="cfb4c-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="cfb4c-148">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="cfb4c-148">Related resources</span></span>

[<span data-ttu-id="cfb4c-149">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="cfb4c-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="cfb4c-150">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="cfb4c-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="cfb4c-151">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="cfb4c-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="cfb4c-152">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="cfb4c-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="cfb4c-153">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="cfb4c-153">Cancel a planning job</span></span>](cancel-planning-job.md)
