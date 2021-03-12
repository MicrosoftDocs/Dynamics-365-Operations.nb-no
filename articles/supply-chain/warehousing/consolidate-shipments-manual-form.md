---
title: Konsolidere forsendelser manuelt ved hjelp av siden Konsolider forsendelser
description: Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert senere ved hjelp av siden Konsolider forsendelser.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983021"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="cc06e-103">Konsolidere forsendelser manuelt ved hjelp av siden Konsolider forsendelser</span><span class="sxs-lookup"><span data-stu-id="cc06e-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc06e-104">Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert senere ved hjelp av siden **Konsolider forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="cc06e-105">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="cc06e-105">Make demo data available</span></span>

<span data-ttu-id="cc06e-106"> i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cc06e-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cc06e-107">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="cc06e-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="cc06e-108">Definer policyer for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="cc06e-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="cc06e-109"> som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="cc06e-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="cc06e-110">Husk å utføre øvelsene før du fortsetter med dette .</span><span class="sxs-lookup"><span data-stu-id="cc06e-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="cc06e-111">Opprett salgsordrene for dette </span><span class="sxs-lookup"><span data-stu-id="cc06e-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="cc06e-112">Begynn med å opprette en samling salgsordrer du kan arbeide med.</span><span class="sxs-lookup"><span data-stu-id="cc06e-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="cc06e-113">Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS).</span><span class="sxs-lookup"><span data-stu-id="cc06e-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="cc06e-114">Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.</span><span class="sxs-lookup"><span data-stu-id="cc06e-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="cc06e-115">Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.</span><span class="sxs-lookup"><span data-stu-id="cc06e-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="cc06e-116">Opprette salgsordre 1 og 2</span><span class="sxs-lookup"><span data-stu-id="cc06e-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="cc06e-117">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="cc06e-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="cc06e-118">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="cc06e-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="cc06e-119">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="cc06e-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="cc06e-120">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="cc06e-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="cc06e-121">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="cc06e-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="cc06e-122">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="cc06e-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="cc06e-123">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="cc06e-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="cc06e-124">Opprette salgsordre 3 og 4</span><span class="sxs-lookup"><span data-stu-id="cc06e-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="cc06e-125">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="cc06e-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="cc06e-126">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="cc06e-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="cc06e-127">**Pulje:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc06e-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="cc06e-128">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="cc06e-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="cc06e-129">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="cc06e-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="cc06e-130">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="cc06e-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="cc06e-131">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="cc06e-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="cc06e-132">Frigi ordrene til lageret</span><span class="sxs-lookup"><span data-stu-id="cc06e-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="cc06e-133">Følg disse trinnene for å frigi hver salgsordre du har opprettet for dette , til lageret.</span><span class="sxs-lookup"><span data-stu-id="cc06e-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="cc06e-134">Gå til **Kunde \> Ordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="cc06e-135">Finn og velg salgosordren som skal frigis.</span><span class="sxs-lookup"><span data-stu-id="cc06e-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="cc06e-136">I handlingsruten velger du **Handlinger \> Frigi til lager** i fanen **Lager** for å frigi den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="cc06e-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="cc06e-137">Gjenta denne prosedyren for hver salgsordre du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="cc06e-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="cc06e-138">Konsolider forsendelser</span><span class="sxs-lookup"><span data-stu-id="cc06e-138">Consolidate shipments</span></span>

1. <span data-ttu-id="cc06e-139">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="cc06e-140">Finn og velg en forsendelse som ble opprettet da salgsordre 1 ble frigitt til lageret.</span><span class="sxs-lookup"><span data-stu-id="cc06e-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="cc06e-141">(Feltet **Policy for forsendelseskonsolidering** for forsendelsen må settes til *Ordrepulje*.)</span><span class="sxs-lookup"><span data-stu-id="cc06e-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="cc06e-142">I handlingsruten velger du **Forsendelser \> Konsolider forsendelser** i fanen **Forsendeler**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="cc06e-143">Kontroller forsendelsene som er foreslått for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="cc06e-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="cc06e-144">Bare én forsendelse som har samme policy, bør foreslås for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="cc06e-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="cc06e-145">Lukk siden **Forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="cc06e-146">Finn og velg en forsendelse som ble opprettet da salgsordre 3 ble frigitt til lageret.</span><span class="sxs-lookup"><span data-stu-id="cc06e-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="cc06e-147">(Feltet **Policy for forsendelseskonsolidering** for forsendelsen må settes til *Standard*.)</span><span class="sxs-lookup"><span data-stu-id="cc06e-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="cc06e-148">I handlingsruten velger du **Forsendelser \> Konsolider forsendelser** i fanen **Forsendeler**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="cc06e-149">Kontroller at ingen forsendelser er foreslått for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="cc06e-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="cc06e-150">Velg **Vis filtre**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="cc06e-151">I ruten **Filtre** fjerner du filteret **Ordrenummer**, og deretter velger du **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="cc06e-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="cc06e-152">Kontroller forsendelsene som er foreslått for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="cc06e-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="cc06e-153">Bare én forsendelse som har samme policy, bør foreslås for konsolidering.</span><span class="sxs-lookup"><span data-stu-id="cc06e-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc06e-154">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cc06e-154">Additional resources</span></span>

- [<span data-ttu-id="cc06e-155">Policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="cc06e-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="cc06e-156">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="cc06e-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)