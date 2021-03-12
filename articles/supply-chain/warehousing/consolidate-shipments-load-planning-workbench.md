---
title: Konsolidere forsendelser ved hjelp av siden Frigi til lager fra arbeidsområdet for lastplanlegging
description: Dette emnet viser et scenario der flere ordrer frigis til lageret i samme last, og deretter blir de konsolidert automatisk til forsendelser.
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
ms.openlocfilehash: c0af6764742532cbe181c8a20e7bf783b0e6d7cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983098"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="9b08b-103">Konsolidere forsendelser ved hjelp av siden Frigi til lager fra arbeidsområdet for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="9b08b-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b08b-104">Dette emnet viser et scenario der flere ordrer frigis til lageret i samme last, og deretter blir de konsolidert automatisk til forsendelser.</span><span class="sxs-lookup"><span data-stu-id="9b08b-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="9b08b-105">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="9b08b-105">Make demo data available</span></span>

<span data-ttu-id="9b08b-106"> i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9b08b-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9b08b-107">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="9b08b-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="9b08b-108">Definer policyer for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="9b08b-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="9b08b-109"> som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="9b08b-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="9b08b-110">Husk å utføre øvelsene før du fortsetter med dette .</span><span class="sxs-lookup"><span data-stu-id="9b08b-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="9b08b-111">Opprett salgsordrene for dette </span><span class="sxs-lookup"><span data-stu-id="9b08b-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="9b08b-112">Begynn med å opprette en samling salgsordrer du kan arbeide med.</span><span class="sxs-lookup"><span data-stu-id="9b08b-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="9b08b-113">Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS).</span><span class="sxs-lookup"><span data-stu-id="9b08b-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="9b08b-114">Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.</span><span class="sxs-lookup"><span data-stu-id="9b08b-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="9b08b-115">Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.</span><span class="sxs-lookup"><span data-stu-id="9b08b-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="9b08b-116">Opprett ordresett 1</span><span class="sxs-lookup"><span data-stu-id="9b08b-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="9b08b-117">Salgsordre 1-1</span><span class="sxs-lookup"><span data-stu-id="9b08b-117">Sales order 1-1</span></span>

1. <span data-ttu-id="9b08b-118">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-119">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9b08b-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9b08b-120">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9b08b-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9b08b-121">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-122">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-123">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-124">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="9b08b-125">Salgsordre 1-2</span><span class="sxs-lookup"><span data-stu-id="9b08b-125">Sales order 1-2</span></span>

1. <span data-ttu-id="9b08b-126">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-127">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9b08b-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9b08b-128">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9b08b-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9b08b-129">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-130">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-131">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-132">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="9b08b-133">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="9b08b-133">Sales order 1-3</span></span>

1. <span data-ttu-id="9b08b-134">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-135">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9b08b-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9b08b-136">**Leveringsmåte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9b08b-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="9b08b-137">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-138">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-139">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-140">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9b08b-141">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-142">**Varenummer:** *A0002* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-143">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9b08b-144">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9b08b-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9b08b-145">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="9b08b-146">Opprett ordresett 2</span><span class="sxs-lookup"><span data-stu-id="9b08b-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="9b08b-147">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="9b08b-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="9b08b-148">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-149">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="9b08b-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="9b08b-150">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-151">**Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)</span><span class="sxs-lookup"><span data-stu-id="9b08b-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="9b08b-152">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-153">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9b08b-154">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-155">**Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)</span><span class="sxs-lookup"><span data-stu-id="9b08b-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="9b08b-156">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9b08b-157">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9b08b-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9b08b-158">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="9b08b-159">Opprett ordresett 3</span><span class="sxs-lookup"><span data-stu-id="9b08b-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="9b08b-160">Salgsordrer 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="9b08b-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="9b08b-161">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-162">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9b08b-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9b08b-163">**Kunderekvisisjon:** *1*</span><span class="sxs-lookup"><span data-stu-id="9b08b-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9b08b-164">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-165">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-166">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-167">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="9b08b-168">Salgsordrer 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="9b08b-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="9b08b-169">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-170">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9b08b-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9b08b-171">**Kunderekvisisjon:** *2*</span><span class="sxs-lookup"><span data-stu-id="9b08b-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="9b08b-172">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-173">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-174">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-175">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="9b08b-176">Opprett ordresett 4</span><span class="sxs-lookup"><span data-stu-id="9b08b-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="9b08b-177">Salgsordrer 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="9b08b-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="9b08b-178">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-179">**Kundekonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="9b08b-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="9b08b-180">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-181">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-182">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-183">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="9b08b-184">Salgsordrer 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="9b08b-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="9b08b-185">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-186">**Kundekonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="9b08b-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="9b08b-187">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-188">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-189">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-190">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="9b08b-191">Salgsordrer 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="9b08b-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="9b08b-192">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-193">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9b08b-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9b08b-194">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="9b08b-194">**Site:** *6*</span></span>
    - <span data-ttu-id="9b08b-195">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="9b08b-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9b08b-196">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="9b08b-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="9b08b-197">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-198">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-199">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-200">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="9b08b-201">Salgsordrer 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="9b08b-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="9b08b-202">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9b08b-203">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9b08b-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9b08b-204">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="9b08b-204">**Site:** *6*</span></span>
    - <span data-ttu-id="9b08b-205">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="9b08b-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9b08b-206">**Pulje:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="9b08b-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="9b08b-207">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9b08b-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9b08b-208">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9b08b-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9b08b-209">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9b08b-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9b08b-210">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="9b08b-211">Bruk arbeidsområde for lastplanlegging til å opprette laster og frigi dem til lageret</span><span class="sxs-lookup"><span data-stu-id="9b08b-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="9b08b-212">Følg disse trinnene for å opprette en belastning for hvert ordresett du har opprettet for dette , og deretter frigi det til lageret.</span><span class="sxs-lookup"><span data-stu-id="9b08b-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="9b08b-213">Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="9b08b-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="9b08b-214">I fanen **Salgslinjer** finner du og velger alle salgsordrelinjene fra ett av ordresettene du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="9b08b-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="9b08b-215">I handlingsruten velger du **Legg til \> I ny last** i fanen **Tilbud og etterspørsel** for å legge til de valgte ordrelinjene i en ny last.</span><span class="sxs-lookup"><span data-stu-id="9b08b-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="9b08b-216">I dialogboksen **Tilordning av lastmal** velger du en lastmal i feltet **Lastmal-ID**, for eksempel *Standard lastmal*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="9b08b-217">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="9b08b-218">I delen **Laster** finner og velger du lasten du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="9b08b-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="9b08b-219">Velg **Frigi \> Frigi til lager** for å frigi den valgte lasten til lageret.</span><span class="sxs-lookup"><span data-stu-id="9b08b-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="9b08b-220">Gjenta denne prosedyren for de andre tre ordresettene du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="9b08b-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="9b08b-221">Bekrefte forsendelsene</span><span class="sxs-lookup"><span data-stu-id="9b08b-221">Verify the shipments</span></span>

<span data-ttu-id="9b08b-222">I den følgende prosedyren kan du kontrollere forsendelsene som er opprettet eller oppdatert som et resultat av forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="9b08b-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="9b08b-223">Bruk det til å gå gjennom hvert ordresett du har opprettet for dette , og se gjennom underinndelinge nedenfor for å kontrollere at du har fått de forventede resultatene.</span><span class="sxs-lookup"><span data-stu-id="9b08b-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="9b08b-224">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="9b08b-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="9b08b-225">Finn og velg den påkrevde forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="9b08b-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="9b08b-226">Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="9b08b-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="9b08b-227">Frigi ordresett 1 i én last</span><span class="sxs-lookup"><span data-stu-id="9b08b-227">Release order set 1 in one load</span></span>

<span data-ttu-id="9b08b-228">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9b08b-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="9b08b-229">Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="9b08b-230">Den andre forsendelen, som ikke bruker transportmåten *Airways*, ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="9b08b-231">Frigi ordresett 2 i én last</span><span class="sxs-lookup"><span data-stu-id="9b08b-231">Release order set 2 in one load</span></span>

<span data-ttu-id="9b08b-232">Tre forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9b08b-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="9b08b-233">Den første forsendelsen inneholder varer med statusen *Brannfarlig*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="9b08b-234">Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="9b08b-235">Frigi ordresett 3 i én last</span><span class="sxs-lookup"><span data-stu-id="9b08b-235">Release order set 3 in one load</span></span>

<span data-ttu-id="9b08b-236">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9b08b-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="9b08b-237">Den første forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *1*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="9b08b-238">Den andre forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *2*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="9b08b-239">Frigi ordresett 4 i én last</span><span class="sxs-lookup"><span data-stu-id="9b08b-239">Release order set 4 in one load</span></span>

<span data-ttu-id="9b08b-240">Fire forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9b08b-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="9b08b-241">Linjer fra to ordrer for kundekonto *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9b08b-242">Linjer fra to ordrer for kundekonto *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9b08b-243">Linjer fra salgsordre 4-5 og 4-6 for kundekonto *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9b08b-244">Linjer fra salgsordre 4-7 og 4-8 for kundekonto *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.</span><span class="sxs-lookup"><span data-stu-id="9b08b-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b08b-245">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9b08b-245">Additional resources</span></span>

- [<span data-ttu-id="9b08b-246">Policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9b08b-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="9b08b-247">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9b08b-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
