---
title: Tilordne trinnikoner og -titler for mobilappen Warehouse Management
description: Dette emnet beskriver hvordan du tilordner trinnikoner og -titler for nye eller tilpassede oppgaveflyter for Warehouse Management-mobilappen.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049370"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ef8f9-103">Tilordne trinnikoner og -titler for mobilappen Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="ef8f9-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef8f9-104">Dette emnet beskriver hvordan du tilordner trinnikoner og -titler for nye eller tilpassede oppgaveflyter for mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ef8f9-105">Følgende illustrasjoner viser hvordan trinnikoner og titler vises i mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ef8f9-106">![Eksempel på et trinnikon og en trinntittel i Warehouse Management-mobilappen](media/step-icon-example.png "Eksempel på et trinnikon og en trinntittel i Warehouse Management-mobilappen")</span><span class="sxs-lookup"><span data-stu-id="ef8f9-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="ef8f9-107">Aktivere denne funksjonen i systemet</span><span class="sxs-lookup"><span data-stu-id="ef8f9-107">Turn on this feature in your system</span></span>

<span data-ttu-id="ef8f9-108">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ef8f9-109">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ef8f9-110">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="ef8f9-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ef8f9-111">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="ef8f9-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ef8f9-112">**Funksjonsnavn:** *Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen*</span><span class="sxs-lookup"><span data-stu-id="ef8f9-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="ef8f9-113">Standard trinn-IDer, klasser og ikoner</span><span class="sxs-lookup"><span data-stu-id="ef8f9-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="ef8f9-114">Hvert trinn i en oppgaveflyt identifiseres av en trinn-ID, og hver trinn-ID har en tilsvarende trinnklasse.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="ef8f9-115">Trinnikonet og tittelen angis i hver trinnklasse.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="ef8f9-116">Trinn-IDer og trinnklasser</span><span class="sxs-lookup"><span data-stu-id="ef8f9-116">Step IDs and step classes</span></span>

<span data-ttu-id="ef8f9-117">I tabellen nedenfor finner du en oversikt over alle trinn-IDer som er tilgjengelige, og den tilhørende trinnklassen.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="ef8f9-118">Kontrollnavnet til hovedinndatafeltet brukes som trinn-IDen.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="ef8f9-119">Hvis du vil ha et eksempel som viser hvordan disse trinn-IDene og klassene brukes, kan du se implementeringen av metoden `WHSMobileAppStepInfoBuilder.stepId()` i delen [Eksempel: Tilordne trinnikoner og titler for en egendefinert flyt](#example) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="ef8f9-120">Trinn-ID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-120">Step ID</span></span> | <span data-ttu-id="ef8f9-121">Trinnklasse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="ef8f9-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-122">BatchDisposition</span></span> | <span data-ttu-id="ef8f9-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="ef8f9-124">Transportør</span><span class="sxs-lookup"><span data-stu-id="ef8f9-124">Carrier</span></span> | <span data-ttu-id="ef8f9-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="ef8f9-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="ef8f9-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-126">CatchWeight</span></span> | <span data-ttu-id="ef8f9-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ef8f9-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="ef8f9-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ef8f9-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ef8f9-130">CatchWeightTag</span></span> | <span data-ttu-id="ef8f9-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ef8f9-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ef8f9-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="ef8f9-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="ef8f9-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="ef8f9-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="ef8f9-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="ef8f9-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="ef8f9-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="ef8f9-136">CheckDigit</span></span> | <span data-ttu-id="ef8f9-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="ef8f9-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="ef8f9-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-138">ClusterId</span></span> | <span data-ttu-id="ef8f9-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="ef8f9-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="ef8f9-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ef8f9-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-142">ClusterPosition</span></span> | <span data-ttu-id="ef8f9-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="ef8f9-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-144">ConfigId</span></span> | <span data-ttu-id="ef8f9-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="ef8f9-146">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-146">Confirmation</span></span> | <span data-ttu-id="ef8f9-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="ef8f9-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="ef8f9-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="ef8f9-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="ef8f9-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="ef8f9-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="ef8f9-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="ef8f9-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ef8f9-154">ContainerType</span></span> | <span data-ttu-id="ef8f9-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="ef8f9-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="ef8f9-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ef8f9-156">CountingReasonCode</span></span> | <span data-ttu-id="ef8f9-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ef8f9-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="ef8f9-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="ef8f9-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="ef8f9-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="ef8f9-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="ef8f9-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="ef8f9-160">CycleCountQty1</span></span> | <span data-ttu-id="ef8f9-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ef8f9-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="ef8f9-162">CycleCountQty2</span></span> | <span data-ttu-id="ef8f9-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ef8f9-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="ef8f9-164">CycleCountQty3</span></span> | <span data-ttu-id="ef8f9-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ef8f9-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="ef8f9-166">CycleCountQty4</span></span> | <span data-ttu-id="ef8f9-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ef8f9-168">Disposisjon</span><span class="sxs-lookup"><span data-stu-id="ef8f9-168">Disposition</span></span> | <span data-ttu-id="ef8f9-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="ef8f9-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="ef8f9-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="ef8f9-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-172">DriverCheckInId</span></span> | <span data-ttu-id="ef8f9-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="ef8f9-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="ef8f9-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="ef8f9-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-176">DriverCheckOutId</span></span> | <span data-ttu-id="ef8f9-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="ef8f9-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="ef8f9-178">ExpDate</span></span> | <span data-ttu-id="ef8f9-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="ef8f9-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="ef8f9-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-180">FromBatchDisposition</span></span> | <span data-ttu-id="ef8f9-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="ef8f9-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="ef8f9-182">FromInventoryStatus</span></span> | <span data-ttu-id="ef8f9-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="ef8f9-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="ef8f9-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-184">FullQty</span></span> | <span data-ttu-id="ef8f9-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="ef8f9-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-186">InboundPut</span></span> | <span data-ttu-id="ef8f9-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="ef8f9-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-188">InventBatchId</span></span> | <span data-ttu-id="ef8f9-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="ef8f9-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="ef8f9-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-190">InventColorId</span></span> | <span data-ttu-id="ef8f9-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="ef8f9-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-192">InventLocation</span></span> | <span data-ttu-id="ef8f9-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="ef8f9-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-194">InventLocationId</span></span> | <span data-ttu-id="ef8f9-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="ef8f9-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-196">InventSerialId</span></span> | <span data-ttu-id="ef8f9-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="ef8f9-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-198">InventSizeId</span></span> | <span data-ttu-id="ef8f9-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="ef8f9-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-200">InventStatusId</span></span> | <span data-ttu-id="ef8f9-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="ef8f9-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="ef8f9-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-202">InventStyleId</span></span> | <span data-ttu-id="ef8f9-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="ef8f9-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-204">InventVersionId</span></span> | <span data-ttu-id="ef8f9-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="ef8f9-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-206">ItemId</span></span> | <span data-ttu-id="ef8f9-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="ef8f9-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="ef8f9-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-208">ITMContainerID</span></span> | <span data-ttu-id="ef8f9-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="ef8f9-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-210">ITMShipmentID</span></span> | <span data-ttu-id="ef8f9-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="ef8f9-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-212">KanbanCardId</span></span> | <span data-ttu-id="ef8f9-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="ef8f9-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ef8f9-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="ef8f9-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="ef8f9-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-216">KanbanOrCardId</span></span> | <span data-ttu-id="ef8f9-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="ef8f9-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ef8f9-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-218">LicensePlateId</span></span> | <span data-ttu-id="ef8f9-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="ef8f9-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="ef8f9-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-220">LoadId</span></span> | <span data-ttu-id="ef8f9-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="ef8f9-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="ef8f9-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="ef8f9-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-224">LocOrLP</span></span> | <span data-ttu-id="ef8f9-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="ef8f9-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="ef8f9-226">LocOrLP_From</span></span> | <span data-ttu-id="ef8f9-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="ef8f9-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="ef8f9-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="ef8f9-228">LocOrLP_To</span></span> | <span data-ttu-id="ef8f9-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="ef8f9-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="ef8f9-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ef8f9-230">LocOrLPCheck</span></span> | <span data-ttu-id="ef8f9-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ef8f9-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="ef8f9-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-232">LocVerification</span></span> | <span data-ttu-id="ef8f9-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="ef8f9-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ef8f9-234">LPAdjustIn</span></span> | <span data-ttu-id="ef8f9-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ef8f9-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="ef8f9-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-236">LPBreakChildLP</span></span> | <span data-ttu-id="ef8f9-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="ef8f9-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-238">LPBreakParentLP</span></span> | <span data-ttu-id="ef8f9-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="ef8f9-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-240">LPBuildChildLP</span></span> | <span data-ttu-id="ef8f9-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="ef8f9-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-242">LPBuildParentLP</span></span> | <span data-ttu-id="ef8f9-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="ef8f9-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-244">LPVerification</span></span> | <span data-ttu-id="ef8f9-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="ef8f9-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-246">MergeContainerId</span></span> | <span data-ttu-id="ef8f9-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="ef8f9-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-248">MixedLPLineNum</span></span> | <span data-ttu-id="ef8f9-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="ef8f9-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="ef8f9-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="ef8f9-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="ef8f9-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="ef8f9-252">MovementConfirmCancel</span></span> | <span data-ttu-id="ef8f9-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="ef8f9-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="ef8f9-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-254">NewCaptureWeight</span></span> | <span data-ttu-id="ef8f9-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ef8f9-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-256">NewQty</span></span> | <span data-ttu-id="ef8f9-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="ef8f9-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ef8f9-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="ef8f9-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ef8f9-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ef8f9-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-260">OutboundPut</span></span> | <span data-ttu-id="ef8f9-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="ef8f9-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-262">OutboundWeight</span></span> | <span data-ttu-id="ef8f9-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ef8f9-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-264">OverridePutNewLocation</span></span> | <span data-ttu-id="ef8f9-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="ef8f9-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="ef8f9-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ef8f9-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-268">POLineNum</span></span> | <span data-ttu-id="ef8f9-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="ef8f9-270">Best.nr.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-270">PONum</span></span> | <span data-ttu-id="ef8f9-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="ef8f9-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="ef8f9-272">PositionFull</span></span> | <span data-ttu-id="ef8f9-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="ef8f9-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="ef8f9-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-274">PositionFullQty</span></span> | <span data-ttu-id="ef8f9-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="ef8f9-276">Styrke</span><span class="sxs-lookup"><span data-stu-id="ef8f9-276">Potency</span></span> | <span data-ttu-id="ef8f9-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="ef8f9-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="ef8f9-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="ef8f9-278">PrinterName</span></span> | <span data-ttu-id="ef8f9-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="ef8f9-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="ef8f9-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-280">ProdId</span></span> | <span data-ttu-id="ef8f9-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="ef8f9-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="ef8f9-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="ef8f9-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-284">ProductConfirmation</span></span> | <span data-ttu-id="ef8f9-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="ef8f9-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="ef8f9-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="ef8f9-288">Plasser</span><span class="sxs-lookup"><span data-stu-id="ef8f9-288">Put</span></span> | <span data-ttu-id="ef8f9-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="ef8f9-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-290">PutawayClusterId</span></span> | <span data-ttu-id="ef8f9-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="ef8f9-292">Antall</span><span class="sxs-lookup"><span data-stu-id="ef8f9-292">Qty</span></span> | <span data-ttu-id="ef8f9-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="ef8f9-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ef8f9-294">QtyAdjust</span></span> | <span data-ttu-id="ef8f9-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ef8f9-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ef8f9-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="ef8f9-296">QtyShort</span></span> | <span data-ttu-id="ef8f9-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="ef8f9-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="ef8f9-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ef8f9-298">QtyToConsume</span></span> | <span data-ttu-id="ef8f9-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ef8f9-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="ef8f9-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="ef8f9-300">QtyToPick</span></span> | <span data-ttu-id="ef8f9-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="ef8f9-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="ef8f9-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-302">QtyToPut</span></span> | <span data-ttu-id="ef8f9-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="ef8f9-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ef8f9-304">QtyToScrap</span></span> | <span data-ttu-id="ef8f9-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ef8f9-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="ef8f9-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-306">QtyVerification</span></span> | <span data-ttu-id="ef8f9-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ef8f9-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="ef8f9-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="ef8f9-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ef8f9-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ef8f9-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="ef8f9-310">ReasonString</span></span> | <span data-ttu-id="ef8f9-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="ef8f9-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="ef8f9-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-312">RecvLocationId</span></span> | <span data-ttu-id="ef8f9-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="ef8f9-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-314">RemoveContainerId</span></span> | <span data-ttu-id="ef8f9-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="ef8f9-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="ef8f9-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="ef8f9-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-318">RMANum</span></span> | <span data-ttu-id="ef8f9-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="ef8f9-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ef8f9-320">ShortPickReason</span></span> | <span data-ttu-id="ef8f9-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ef8f9-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="ef8f9-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-322">SortConOrLP</span></span> | <span data-ttu-id="ef8f9-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="ef8f9-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-324">SortLicensePlateId</span></span> | <span data-ttu-id="ef8f9-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="ef8f9-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-326">SortPositionId</span></span> | <span data-ttu-id="ef8f9-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="ef8f9-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-328">SortVerification</span></span> | <span data-ttu-id="ef8f9-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="ef8f9-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="ef8f9-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-330">StartLocationId</span></span> | <span data-ttu-id="ef8f9-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="ef8f9-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="ef8f9-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="ef8f9-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-334">TargetLicensePlateId</span></span> | <span data-ttu-id="ef8f9-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="ef8f9-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-336">TOLineNum</span></span> | <span data-ttu-id="ef8f9-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="ef8f9-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-338">ToLocation</span></span> | <span data-ttu-id="ef8f9-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="ef8f9-340">TONum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-340">TONum</span></span> | <span data-ttu-id="ef8f9-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="ef8f9-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-342">ToWarehouse</span></span> | <span data-ttu-id="ef8f9-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="ef8f9-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="ef8f9-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-344">TransportLoadId</span></span> | <span data-ttu-id="ef8f9-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="ef8f9-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-346">WaveLabelId</span></span> | <span data-ttu-id="ef8f9-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="ef8f9-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-348">WaveLblQty</span></span> | <span data-ttu-id="ef8f9-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="ef8f9-350">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-350">Weight</span></span> | <span data-ttu-id="ef8f9-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="ef8f9-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ef8f9-352">WeightToConsume</span></span> | <span data-ttu-id="ef8f9-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ef8f9-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="ef8f9-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ef8f9-354">WHSAdjustmentType</span></span> | <span data-ttu-id="ef8f9-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ef8f9-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="ef8f9-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ef8f9-356">WHSReceivingException</span></span> | <span data-ttu-id="ef8f9-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ef8f9-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="ef8f9-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="ef8f9-358">WHSWorkException</span></span> | <span data-ttu-id="ef8f9-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="ef8f9-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="ef8f9-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="ef8f9-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="ef8f9-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-362">WMSLocationId</span></span> | <span data-ttu-id="ef8f9-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="ef8f9-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-364">WorkId</span></span> | <span data-ttu-id="ef8f9-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="ef8f9-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ef8f9-366">WorkIdToCancel</span></span> | <span data-ttu-id="ef8f9-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ef8f9-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="ef8f9-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ef8f9-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="ef8f9-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ef8f9-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="ef8f9-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-370">WorkPoolId</span></span> | <span data-ttu-id="ef8f9-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="ef8f9-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-372">ZoneId</span></span> | <span data-ttu-id="ef8f9-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="ef8f9-374">Tilgjengelige trinnikoner</span><span class="sxs-lookup"><span data-stu-id="ef8f9-374">Available step icons</span></span>

<span data-ttu-id="ef8f9-375">Systemet inneholder en samling standard trinnikoner som du også kan bruke til de egendefinerte trinnene.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="ef8f9-376">Du kan ikke laste opp egendefinerte trinnikoner.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="ef8f9-377">Derfor må du alltid velge ett av de standard trinnikonene.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="ef8f9-378">Følgende tabell viser hvert standard trinnikon som er tilgjengelig, og navnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Om-trinnikon"><br><span data-ttu-id="ef8f9-380">Om</span><span class="sxs-lookup"><span data-stu-id="ef8f9-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Legge til nummerskilt- eller elementtrinnikon"><br><span data-ttu-id="ef8f9-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="ef8f9-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Trinnikon for partidisposisjon"><br><span data-ttu-id="ef8f9-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Transportørt-trinnikon"><br><span data-ttu-id="ef8f9-386">Transportør</span><span class="sxs-lookup"><span data-stu-id="ef8f9-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Trinnikon for faktisk vekt-kode"><br><span data-ttu-id="ef8f9-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ef8f9-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Trinnikon for faktisk vekt-kode"><br><span data-ttu-id="ef8f9-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Trinnikon for kontrollsiffer"><br><span data-ttu-id="ef8f9-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="ef8f9-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Trinnikon for ID for inn- eller utsjekking"><br><span data-ttu-id="ef8f9-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Trinnikon for underordnet nummerskilt"><br><span data-ttu-id="ef8f9-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Trinnikon for klynge-ID"><br><span data-ttu-id="ef8f9-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Trinnikon for klyngeposisjon"><br><span data-ttu-id="ef8f9-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Trinnikon for konfigurasjons-ID"><br><span data-ttu-id="ef8f9-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Trinnikon for konfigurert felt"><br><span data-ttu-id="ef8f9-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="ef8f9-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Trinnsikon for Con eller LP"><br><span data-ttu-id="ef8f9-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Trinnikon for konsolider fra nummerskilt-ID"><br><span data-ttu-id="ef8f9-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Trinnikon for konsolider til nummerskilt-ID"><br><span data-ttu-id="ef8f9-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Trinnikon for containertype"><br><span data-ttu-id="ef8f9-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ef8f9-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Trinnikon for opptelling"><br><span data-ttu-id="ef8f9-414">Opptelling</span><span class="sxs-lookup"><span data-stu-id="ef8f9-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Trinnikonet for årsakskode for telling"><br><span data-ttu-id="ef8f9-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ef8f9-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Trinnikon for kode for opprinnelsesland"><br><span data-ttu-id="ef8f9-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="ef8f9-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Trinnikon for disposisjon"><br><span data-ttu-id="ef8f9-420">Disposisjon</span><span class="sxs-lookup"><span data-stu-id="ef8f9-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Trinnikon for utført"><br><span data-ttu-id="ef8f9-422">Utført</span><span class="sxs-lookup"><span data-stu-id="ef8f9-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Trinikon for bekreftelse for sjåførinnsjekking"><br><span data-ttu-id="ef8f9-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Trinnikon for ID for sjåførinnsjekking"><br><span data-ttu-id="ef8f9-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Trinnikon for ID for sjåførutsjekking"><br><span data-ttu-id="ef8f9-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Trinnikon for utløpsdato"><br><span data-ttu-id="ef8f9-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="ef8f9-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Trinnikon for felt"><br><span data-ttu-id="ef8f9-432">Felt</span><span class="sxs-lookup"><span data-stu-id="ef8f9-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Trinnikon for fra partidisposisjon"><br><span data-ttu-id="ef8f9-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Trinnikon for fra lagerstatus"><br><span data-ttu-id="ef8f9-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="ef8f9-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Trinnikon for ID-attributt"><br><span data-ttu-id="ef8f9-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="ef8f9-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Trinnikon for lagerparti-ID"><br><span data-ttu-id="ef8f9-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Trinnikon for lagerfarge-ID"><br><span data-ttu-id="ef8f9-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Trinnikon for lagerlokasjon"><br><span data-ttu-id="ef8f9-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Trinnikon for lagerserie-ID"><br><span data-ttu-id="ef8f9-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Trinnikon for lagerstørrelses-ID"><br><span data-ttu-id="ef8f9-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Trinnikon for fra lagerstatus-ID"><br><span data-ttu-id="ef8f9-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Trinnikon for lagerstil-ID"><br><span data-ttu-id="ef8f9-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Trinnikon for fra lagerversjons-ID"><br><span data-ttu-id="ef8f9-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Trinnikon for element-ID"><br><span data-ttu-id="ef8f9-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Trinnikon for ITM-container-ID"><br><span data-ttu-id="ef8f9-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Trinnikon for ITM-forsendelses-ID"><br><span data-ttu-id="ef8f9-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Trinnikon for Kanban-kort-ID"><br><span data-ttu-id="ef8f9-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Trinnikon for Kanban- eller kort-ID"><br><span data-ttu-id="ef8f9-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Trinnikon for nummerskilt-ID"><br><span data-ttu-id="ef8f9-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Trinnikon for last-ID"><br><span data-ttu-id="ef8f9-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Trinnikon for nummerskiltposisjon"><br><span data-ttu-id="ef8f9-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ef8f9-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Trinnikon for lokasjon og nummerskilt"><br><span data-ttu-id="ef8f9-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Trinnikon for lokasjons- og nummerskiltkontroll"><br><span data-ttu-id="ef8f9-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ef8f9-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Trinnikon for lokasjons- og nummerskilt"><br><span data-ttu-id="ef8f9-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="ef8f9-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Trinnikon for lokasjon og nummerskilt"><br><span data-ttu-id="ef8f9-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="ef8f9-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Trinnikon for langt prosesstrinn fullført"><br><span data-ttu-id="ef8f9-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="ef8f9-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Trinnikon for nummerskilt bryt for overordnede nummerskilt"><br><span data-ttu-id="ef8f9-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Trinnikon for slå sammen container-ID"><br><span data-ttu-id="ef8f9-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Trinnikon for kombinert skiltnummer"><br><span data-ttu-id="ef8f9-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Trinnikon for utgående vekt"><br><span data-ttu-id="ef8f9-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ef8f9-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Trinnikon for eier"><br><span data-ttu-id="ef8f9-490">Eier</span><span class="sxs-lookup"><span data-stu-id="ef8f9-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Trinnikon for overordnet nummerskilt"><br><span data-ttu-id="ef8f9-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="ef8f9-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Trinnikon for vennligst bekreft"><br><span data-ttu-id="ef8f9-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="ef8f9-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Trinnikon for bestillingslinje"><br><span data-ttu-id="ef8f9-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Trinnikon for bestillingsnummer"><br><span data-ttu-id="ef8f9-498">Best.nr.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Trinnikon for posisjon full"><br><span data-ttu-id="ef8f9-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="ef8f9-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Trinnikon for styrke"><br><span data-ttu-id="ef8f9-502">Styrke</span><span class="sxs-lookup"><span data-stu-id="ef8f9-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Trinnikon for skrivernavn"><br><span data-ttu-id="ef8f9-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="ef8f9-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Trinnikon for produkt-ID"><br><span data-ttu-id="ef8f9-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Trinnikon for produktbekreftelse"><br><span data-ttu-id="ef8f9-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Trinnikon for Plasser"><br><span data-ttu-id="ef8f9-510">Plasser</span><span class="sxs-lookup"><span data-stu-id="ef8f9-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Trinnikon for gruppe-ID for plassering"><br><span data-ttu-id="ef8f9-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Trinnikon for antall"><br><span data-ttu-id="ef8f9-514">Antall</span><span class="sxs-lookup"><span data-stu-id="ef8f9-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Trinnikon for juster inn antall"><br><span data-ttu-id="ef8f9-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ef8f9-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Trinnikon for lavt antall"><br><span data-ttu-id="ef8f9-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="ef8f9-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Trinnikon for antall som skal konsumeres"><br><span data-ttu-id="ef8f9-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ef8f9-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Trinnikon for antall som skal plasseres"><br><span data-ttu-id="ef8f9-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="ef8f9-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Trinnikon for antall som skal kasseres"><br><span data-ttu-id="ef8f9-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ef8f9-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Trinnikon for antallsbekreftelse"><br><span data-ttu-id="ef8f9-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Trinnikon for ferdigmelding av avslutningsjobb"><br><span data-ttu-id="ef8f9-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="ef8f9-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Trinnikon for motta plasserings-ID"><br><span data-ttu-id="ef8f9-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Trinnikon for fjern container-ID"><br><span data-ttu-id="ef8f9-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Trinnikon for autorisasjonsreturnummer"><br><span data-ttu-id="ef8f9-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Trinnikon for velg ordre"><br><span data-ttu-id="ef8f9-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="ef8f9-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Trinnikon for plukk med mangler"><br><span data-ttu-id="ef8f9-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ef8f9-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Trinnikon for sporteringsposisjons-ID"><br><span data-ttu-id="ef8f9-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Trinnikon for målnummerskilt-ID"><br><span data-ttu-id="ef8f9-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Trinnikon for Til-linjenummer"><br><span data-ttu-id="ef8f9-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Trinnikon for Til-plassering"><br><span data-ttu-id="ef8f9-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="ef8f9-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Trinnikon for Til-nummer"><br><span data-ttu-id="ef8f9-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="ef8f9-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Trinnikon for Til-lager"><br><span data-ttu-id="ef8f9-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Trinnikon for transportlast-ID"><br><span data-ttu-id="ef8f9-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Trinnikon for leverandørparti-ID"><br><span data-ttu-id="ef8f9-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Trinnikon for bølgeetikett-ID"><br><span data-ttu-id="ef8f9-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Trinnikon for bølgeetikettantall"><br><span data-ttu-id="ef8f9-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ef8f9-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Trinnikon for vekt"><br><span data-ttu-id="ef8f9-560">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="ef8f9-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Trinnikon for vekt som skal konsumeres"><br><span data-ttu-id="ef8f9-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ef8f9-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Trinnikon for WHS-justering"><br><span data-ttu-id="ef8f9-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ef8f9-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Trinnikon for WHS-mottaksunntak"><br><span data-ttu-id="ef8f9-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ef8f9-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Trinnikon for WMS-plasserings-ID"><br><span data-ttu-id="ef8f9-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Trinnikon for arbeids-ID"><br><span data-ttu-id="ef8f9-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Trinnikon for arbeids-ID som skal avbrytes"><br><span data-ttu-id="ef8f9-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ef8f9-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Trinnikon for nummerskilt-ID for jobb"><br><span data-ttu-id="ef8f9-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ef8f9-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Trinnikon for plasseringsgruppe for nummerskilt-ID for jobb"><br><span data-ttu-id="ef8f9-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ef8f9-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Trinnikon for arbeidsutvalg-ID"><br><span data-ttu-id="ef8f9-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Trinnikon for sone-ID"><br><span data-ttu-id="ef8f9-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="ef8f9-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="ef8f9-581">Eksempel: Tilordne trinnikoner og -titler for en egendefinert flyt</span><span class="sxs-lookup"><span data-stu-id="ef8f9-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="ef8f9-582">Dette eksemplet beskriver hvordan du konfigurerer trinnikoner og -titler for en egendefinert oppgaveflyt.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="ef8f9-583">Scenariet er bygd på et eksempel på en egendefinert oppgaveflyt som presenteres og utforskes mer detaljert i følgende kommentarpost: [Tilpasse Warehouse Management-appen](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="ef8f9-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="ef8f9-584">Oppgaveflyten fungerer på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="ef8f9-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="ef8f9-585">Appen viser en side som ber arbeideren om å angi en container-ID (for eksempel ved å skanne en strekkode).</span><span class="sxs-lookup"><span data-stu-id="ef8f9-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="ef8f9-586">Hvis container-IDen er gyldig, åpner appen en ny side som ber arbeideren om vekten.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="ef8f9-587">(Hvis beholder-IDen ikke er gyldig, returneres arbeideren til første side.)</span><span class="sxs-lookup"><span data-stu-id="ef8f9-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="ef8f9-588">Når arbeideren angir en gyldig vekt, lagrer systemet vekten og returnerer arbeideren til den første siden.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="ef8f9-589">Følgende illustrasjon viser denne oppgaveflyten.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="ef8f9-590">![Oppgaveflytdiagram](media/step-icons-example-task-flow.png "Oppgaveflytdiagram")</span><span class="sxs-lookup"><span data-stu-id="ef8f9-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="ef8f9-591">Opprette en trinnklasse for containerinndatasiden</span><span class="sxs-lookup"><span data-stu-id="ef8f9-591">Create a step class for the container input page</span></span>

<span data-ttu-id="ef8f9-592">Med containerinndatasiden kan arbeideren skanne eller angi en container-ID.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="ef8f9-593">![Containerinndataside](media/step-icons-example-container-input.png "Containerinndataside")</span><span class="sxs-lookup"><span data-stu-id="ef8f9-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="ef8f9-594">På containerinndatasiden er kontrollnavnet for inndatafeltet `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="ef8f9-595">Ettersom dette kontrollnavnet ikke står på [listen over trinn-IDer](#step-ids-classes), vil du ikke finne et eksisterende trinn som er basert på det.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="ef8f9-596">Derfor må du opprette en trinnklasse som representerer trinnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="ef8f9-597">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="ef8f9-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="ef8f9-598">Trinnikonets ID lagres i `defaultStepIcon`-klassemedlemmet, og trinntittelen lagres i `defaultStepTitle`-klassemedlemmet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="ef8f9-599">Hvis du vil tilordne et trinnikon, angir du `defaultStepIcon` til ett av ikon-IDene som vises i delen [Tilgjengelige trinnikoner](#step-icons) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="ef8f9-600">Bruk et standard eller egendefinert trinnikon og en tittel for vektinndataen</span><span class="sxs-lookup"><span data-stu-id="ef8f9-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="ef8f9-601">På vektinndatasiden kan du angi en vekt for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="ef8f9-602">![Vektinndataside](media/step-icons-example-weight-input.png "Vektinndataside")</span><span class="sxs-lookup"><span data-stu-id="ef8f9-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="ef8f9-603">På vektinndatasiden er kontrollnavnet for inndatafeltet `Weight`, som finne i [listen over trinn-IDer](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="ef8f9-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="ef8f9-604">Hvis trinnikonet og -tittelen som er definert i klassen `WHSMobileAppStepWeight`, er akseptabelt for deg, behøver du derfor ikke å endre noe for dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="ef8f9-605">Hvis du imidlertid foretrekker å bruke et annet ikon eller en annen tittel for dette trinnet, kan du overstyre enten metoden `stepId()` eller metoden `stepInfo()` i byggerklassen.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="ef8f9-606">Hver oppgaveflyt har sin egen trinninformasjonskonfigurator.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="ef8f9-607">Overstyre stepId()-metoden</span><span class="sxs-lookup"><span data-stu-id="ef8f9-607">Override the stepId() method</span></span>

<span data-ttu-id="ef8f9-608">Følgende eksempel viser én måte du kan endre en byggerklasse på ved å overstyre `stepId()`-metoden.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="ef8f9-609">Deretter oppretter du en trinnklasse for `NewWeight`-trinnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="ef8f9-610">Koden bør ligne på koden for `ContainerId`-eksemplet som ble vist tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="ef8f9-611">Overstyre stepInfo()-metoden</span><span class="sxs-lookup"><span data-stu-id="ef8f9-611">Override the stepInfo() method</span></span>

<span data-ttu-id="ef8f9-612">Følgende eksempel viser én måte du kan endre en byggerklasse på ved å overstyre `stepInfo()`-metoden.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="ef8f9-613">Deretter konstruerer du et `WHSMobileAppStepInfo`-objekt og angir ikonet og/eller tittelen direkte.</span><span class="sxs-lookup"><span data-stu-id="ef8f9-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef8f9-614">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ef8f9-614">Additional resources</span></span>

- [<span data-ttu-id="ef8f9-615">Installere og koble til mobilappen Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ef8f9-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="ef8f9-616">Brukinnstillinger for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="ef8f9-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
