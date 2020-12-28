---
title: Konsolidere forsendelser når de frigis til lageret ved hjelp av automatisk frigivelse av salgsordrer
description: Dette emnet viser et scenario der flere ordrer frigis til lageret i samme automatiserte fremgangsmåte for automatisk frigivelse-til-lager.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac3ab25dc1355ee15e1209950ff0f3b3933b7095
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434751"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="343d9-103">Konsolidere forsendelser når de frigis til lageret ved hjelp av automatisk frigivelse av salgsordrer</span><span class="sxs-lookup"><span data-stu-id="343d9-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="343d9-104">Dette emnet viser et scenario der flere ordrer frigis til lageret i samme automatiserte fremgangsmåte for automatisk frigivelse-til-lager.</span><span class="sxs-lookup"><span data-stu-id="343d9-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="343d9-105">Ordrene blir automatisk konsolidert i forsendelser, basert på regler som er definert som policyer for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="343d9-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="343d9-106">I løpet av  kan du opprette sett med salgsordrer og frigi hvert sett til lageret.</span><span class="sxs-lookup"><span data-stu-id="343d9-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="343d9-107">Du vil deretter se over forsendelsene som ble opprettet eller oppdatert under forsendelseskonsolideringen, basert på de konfigurerte policyene.</span><span class="sxs-lookup"><span data-stu-id="343d9-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="343d9-108">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="343d9-108">Make demo data available</span></span>

<span data-ttu-id="343d9-109"> i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="343d9-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="343d9-110">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="343d9-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="343d9-111">Definer policyer for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="343d9-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="343d9-112"> som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="343d9-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="343d9-113">Husk å utføre øvelsene før du fortsetter med dette .</span><span class="sxs-lookup"><span data-stu-id="343d9-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="343d9-114">Opprett salgsordrene for dette </span><span class="sxs-lookup"><span data-stu-id="343d9-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="343d9-115">Begynn med å opprette en samling salgsordrer du kan arbeide med.</span><span class="sxs-lookup"><span data-stu-id="343d9-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="343d9-116">Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS).</span><span class="sxs-lookup"><span data-stu-id="343d9-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="343d9-117">Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.</span><span class="sxs-lookup"><span data-stu-id="343d9-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="343d9-118">Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.</span><span class="sxs-lookup"><span data-stu-id="343d9-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="343d9-119">Opprett ordresett 1</span><span class="sxs-lookup"><span data-stu-id="343d9-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="343d9-120">Salgsordre 1-1</span><span class="sxs-lookup"><span data-stu-id="343d9-120">Sales order 1-1</span></span>

1. <span data-ttu-id="343d9-121">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="343d9-122">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="343d9-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="343d9-123">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="343d9-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="343d9-124">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-125">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-126">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="343d9-127">Salgsordre 1-2</span><span class="sxs-lookup"><span data-stu-id="343d9-127">Sales order 1-2</span></span>

1. <span data-ttu-id="343d9-128">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="343d9-129">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="343d9-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="343d9-130">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="343d9-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="343d9-131">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-132">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-133">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="343d9-134">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="343d9-134">Sales order 1-3</span></span>

1. <span data-ttu-id="343d9-135">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="343d9-136">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="343d9-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="343d9-137">**Leveringsmåte:** *10*</span><span class="sxs-lookup"><span data-stu-id="343d9-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="343d9-138">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-139">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-140">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="343d9-141">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-142">**Varenummer:** *A0002* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-143">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="343d9-144">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="343d9-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="343d9-145">Opprett ordresett 2</span><span class="sxs-lookup"><span data-stu-id="343d9-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="343d9-146">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="343d9-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="343d9-147">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="343d9-148">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="343d9-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="343d9-149">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-150">**Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)</span><span class="sxs-lookup"><span data-stu-id="343d9-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="343d9-151">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="343d9-152">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-153">**Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)</span><span class="sxs-lookup"><span data-stu-id="343d9-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="343d9-154">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="343d9-155">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="343d9-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="343d9-156">Opprett ordresett 3</span><span class="sxs-lookup"><span data-stu-id="343d9-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="343d9-157">Salgsordre 3-1</span><span class="sxs-lookup"><span data-stu-id="343d9-157">Sales order 3-1</span></span>

1. <span data-ttu-id="343d9-158">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="343d9-159">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="343d9-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="343d9-160">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-161">**Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)</span><span class="sxs-lookup"><span data-stu-id="343d9-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="343d9-162">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="343d9-163">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-164">**Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)</span><span class="sxs-lookup"><span data-stu-id="343d9-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="343d9-165">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="343d9-166">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="343d9-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="343d9-167">Denne ordren er identisk med de to ordrene du opprettet for ordresett 2.</span><span class="sxs-lookup"><span data-stu-id="343d9-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="343d9-168">Den er imidlertid oppført som sitt eget ordresett, ettersom du kan frigi den separat senere i dette .</span><span class="sxs-lookup"><span data-stu-id="343d9-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="343d9-169">Opprett ordresett 4</span><span class="sxs-lookup"><span data-stu-id="343d9-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="343d9-170">Salgsordre 4-1</span><span class="sxs-lookup"><span data-stu-id="343d9-170">Sales order 4-1</span></span>

1. <span data-ttu-id="343d9-171">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="343d9-172">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="343d9-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="343d9-173">**Kunderekvisisjon:** *1*</span><span class="sxs-lookup"><span data-stu-id="343d9-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="343d9-174">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-175">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-176">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="343d9-177">Opprett ordresett 5</span><span class="sxs-lookup"><span data-stu-id="343d9-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="343d9-178">Salgsordrer 5-1 og 5-2</span><span class="sxs-lookup"><span data-stu-id="343d9-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="343d9-179">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="343d9-180">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="343d9-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="343d9-181">**Kunderekvisisjon:** *2*</span><span class="sxs-lookup"><span data-stu-id="343d9-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="343d9-182">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-183">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-184">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="343d9-185">Salgsordre 5-3</span><span class="sxs-lookup"><span data-stu-id="343d9-185">Sales order 5-3</span></span>

1. <span data-ttu-id="343d9-186">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="343d9-187">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="343d9-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="343d9-188">**Kunderekvisisjon:** *1*</span><span class="sxs-lookup"><span data-stu-id="343d9-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="343d9-189">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-190">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-191">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="343d9-192">Opprett ordresett 6</span><span class="sxs-lookup"><span data-stu-id="343d9-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="343d9-193">Salgsordrer 6-1 og 6-2</span><span class="sxs-lookup"><span data-stu-id="343d9-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="343d9-194">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="343d9-195">**Kundekonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="343d9-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="343d9-196">**Kunderekvisisjon:** *2*</span><span class="sxs-lookup"><span data-stu-id="343d9-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="343d9-197">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-198">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-199">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="343d9-200">Salgsordrer 6-3 og 6-4</span><span class="sxs-lookup"><span data-stu-id="343d9-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="343d9-201">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="343d9-202">**Kundekonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="343d9-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="343d9-203">**Kunderekvisisjon:** *1*</span><span class="sxs-lookup"><span data-stu-id="343d9-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="343d9-204">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-205">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-206">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="343d9-207">Salgsordrer 6-5 og 6-6</span><span class="sxs-lookup"><span data-stu-id="343d9-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="343d9-208">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="343d9-209">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="343d9-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="343d9-210">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="343d9-210">**Site:** *6*</span></span>
    - <span data-ttu-id="343d9-211">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="343d9-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="343d9-212">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="343d9-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="343d9-213">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-214">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-215">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="343d9-216">Salgsordrer 6-7 og 6-8</span><span class="sxs-lookup"><span data-stu-id="343d9-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="343d9-217">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="343d9-218">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="343d9-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="343d9-219">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="343d9-219">**Site:** *6*</span></span>
    - <span data-ttu-id="343d9-220">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="343d9-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="343d9-221">**Pulje:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="343d9-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="343d9-222">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="343d9-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="343d9-223">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="343d9-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="343d9-224">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="343d9-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="343d9-225">Automatisk frigivelse av salgsordrer til lageret</span><span class="sxs-lookup"><span data-stu-id="343d9-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="343d9-226">For hvert sett med salgsordrer du har opprettet tidligere, vil du fullføre en fremgangsmåte for automatisk frigivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="343d9-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="343d9-227">I hvert tilfelle vil du arbeide med den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) som finnes her.</span><span class="sxs-lookup"><span data-stu-id="343d9-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="343d9-228">Grunnleggende fremgangsmåte for frigivelse til lager</span><span class="sxs-lookup"><span data-stu-id="343d9-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="343d9-229">For hvert sett med salgsordrer du har opprettet tidligere, fullfører du de tre fremgangsmåtene som er skissert i følgende underinndelinger.</span><span class="sxs-lookup"><span data-stu-id="343d9-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="343d9-230">Oppdatere bølgemalen som vil bli brukt under frigivelse</span><span class="sxs-lookup"><span data-stu-id="343d9-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="343d9-231">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="343d9-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="343d9-232">Angi verdien *Forsendelse* for feltet **Bølgemaltype**.</span><span class="sxs-lookup"><span data-stu-id="343d9-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="343d9-233">Finn og velg bølgemalen som er knyttet til lageret du brukte i ordresettene du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="343d9-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="343d9-234">Hvis du for eksempel brukte lager *24*, velger du bølgemalen **24 Standardforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="343d9-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="343d9-235">Hvis du brukte lager *61*, velger du bølgemalen **61 Forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="343d9-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="343d9-236">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="343d9-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="343d9-237">Sett alternativet **Behandle bølge ved frigivelse til lager** til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="343d9-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="343d9-238">Frigi til lageret</span><span class="sxs-lookup"><span data-stu-id="343d9-238">Release to the warehouse</span></span>

1. <span data-ttu-id="343d9-239">Gå til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse av salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="343d9-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="343d9-240">Angi verdien *Alle* for feltet **Antall som skal frigis**.</span><span class="sxs-lookup"><span data-stu-id="343d9-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="343d9-241">I hurtigkategorien **Poster som skal inkluderes** velger du **Filter** for å åpne dialogboksen for spørring.</span><span class="sxs-lookup"><span data-stu-id="343d9-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="343d9-242">Velg **Legg til** i kategorien **Område** for å legge til en rad som har følgende innstillinger i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="343d9-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="343d9-243">**Tabell:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="343d9-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="343d9-244">**Avledet tabell:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="343d9-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="343d9-245">**Felt:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="343d9-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="343d9-246">**Vilkår:** Angi en kommadelt liste over salgsordrenumrene fra ønsket ordresett.</span><span class="sxs-lookup"><span data-stu-id="343d9-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="343d9-247">Velg **OK** for å lagre spørringen.</span><span class="sxs-lookup"><span data-stu-id="343d9-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="343d9-248">Velg **OK** for å starte prosedyren *Automatisk frigivelse til lager*.</span><span class="sxs-lookup"><span data-stu-id="343d9-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="343d9-249">Gå gjennom forsendelsen som er opprettet eller oppdatert</span><span class="sxs-lookup"><span data-stu-id="343d9-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="343d9-250">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="343d9-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="343d9-251">Finn og velg den påkrevde forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="343d9-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="343d9-252">Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="343d9-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="343d9-253">Frigi salgsordrer fra ordresett 1</span><span class="sxs-lookup"><span data-stu-id="343d9-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="343d9-254">Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 1.</span><span class="sxs-lookup"><span data-stu-id="343d9-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="343d9-255">Når du er ferdig, skal du kunne se at to forsendelser ble opprettet:</span><span class="sxs-lookup"><span data-stu-id="343d9-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="343d9-256">Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="343d9-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="343d9-257">Den andre forsendelen, som ikke bruker transportmåten *Airways*, ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="343d9-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="343d9-258">Frigi salgsordrer fra ordresett 2</span><span class="sxs-lookup"><span data-stu-id="343d9-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="343d9-259">Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 2.</span><span class="sxs-lookup"><span data-stu-id="343d9-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="343d9-260">Når du er ferdig, skal du kunne se at tre forsendelser ble opprettet:</span><span class="sxs-lookup"><span data-stu-id="343d9-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="343d9-261">Den første forsendelsen inneholder varer med statusen *Brannfarlig*.</span><span class="sxs-lookup"><span data-stu-id="343d9-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="343d9-262">Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.</span><span class="sxs-lookup"><span data-stu-id="343d9-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="343d9-263">Frigi salgsordrer fra ordresett 3</span><span class="sxs-lookup"><span data-stu-id="343d9-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="343d9-264">Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 3.</span><span class="sxs-lookup"><span data-stu-id="343d9-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="343d9-265">Når du er ferdig, skal du kunne se at følgende handlinger oppstod:</span><span class="sxs-lookup"><span data-stu-id="343d9-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="343d9-266">En eksisterende forsendelse (forsendelsen som ble opprettet da ordresett 2 ble frigitt til lageret) ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="343d9-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="343d9-267">En linje som har elementet *Brannfarlig*, ble lagt til.</span><span class="sxs-lookup"><span data-stu-id="343d9-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="343d9-268">Én ny forsendelse ble opprettet, og den inneholder elementet *Eksplosivt*.</span><span class="sxs-lookup"><span data-stu-id="343d9-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="343d9-269">Frigi salgsordrer fra ordresett 4</span><span class="sxs-lookup"><span data-stu-id="343d9-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="343d9-270">Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 4.</span><span class="sxs-lookup"><span data-stu-id="343d9-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="343d9-271">Når du er ferdig, skal du kunne se at den eksisterende forsendelsen (der feltet **Kunderekvisisjon** er satt til *1*) ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="343d9-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="343d9-272">En ny linje ble lagt til for forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="343d9-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="343d9-273">Frigi salgsordrer fra ordresett 5</span><span class="sxs-lookup"><span data-stu-id="343d9-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="343d9-274">Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 5.</span><span class="sxs-lookup"><span data-stu-id="343d9-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="343d9-275">Når du er ferdig, skal du kunne se at følgende handlinger oppstod:</span><span class="sxs-lookup"><span data-stu-id="343d9-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="343d9-276">En eksisterende forsendelse (der feltet **Kunderekvisisjon** er satt til *1*) ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="343d9-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="343d9-277">En linje fra salgsordre 5-3 (der feltet **Kunderekvisisjon** er satt til *1*) ble lagt til for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="343d9-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="343d9-278">Én ny forsendelse ble opprettet, der linjer fra salgsordre 5-1 og 5-2 grupperes i én forsendelse.</span><span class="sxs-lookup"><span data-stu-id="343d9-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="343d9-279">Frigi salgsordrer fra ordresett 6</span><span class="sxs-lookup"><span data-stu-id="343d9-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="343d9-280">Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 6.</span><span class="sxs-lookup"><span data-stu-id="343d9-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="343d9-281">Når du er ferdig, skal du kunne se at fire forsendelser ble opprettet:</span><span class="sxs-lookup"><span data-stu-id="343d9-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="343d9-282">Linjer fra to ordrer for kunde *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="343d9-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="343d9-283">Linjer fra to ordrer for kunde *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="343d9-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="343d9-284">Linjer fra salgsordre 6-5 og 6-6 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="343d9-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="343d9-285">Linjer fra salgsordre 6-7 og 6-8 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.</span><span class="sxs-lookup"><span data-stu-id="343d9-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="343d9-286">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="343d9-286">Additional resources</span></span>

- [<span data-ttu-id="343d9-287">Policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="343d9-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="343d9-288">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="343d9-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
