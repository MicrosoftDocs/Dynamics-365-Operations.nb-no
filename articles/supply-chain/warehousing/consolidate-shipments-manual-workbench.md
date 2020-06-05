---
title: Konsolidere forsendelser ved hjelp av arbeidsområdet for forsendelseskonsolidering
description: Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert til forsendelser senere ved hjelp av arbeidsområdet for forsendelseskonsolidering.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b1a2c9506b4444fc98a9e4f0389cbd69db4ce052
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383833"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="9e2f6-103">Konsolidere forsendelser ved hjelp av arbeidsområdet for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9e2f6-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e2f6-104">Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert til forsendelser senere ved hjelp av arbeidsområdet for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="9e2f6-105">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="9e2f6-105">Make demo data available</span></span>

<span data-ttu-id="9e2f6-106"> i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9e2f6-107">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="9e2f6-108">Definer policyer for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="9e2f6-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="9e2f6-109"> som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="9e2f6-110">Husk å utføre øvelsene før du fortsetter med dette .</span><span class="sxs-lookup"><span data-stu-id="9e2f6-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="9e2f6-111">Aktivere funksjonen Manuell forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9e2f6-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="9e2f6-112">Før du kan bruke funksjonen *Manuell forsendelseskonsolidering*, må du aktivere den i systemet.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="9e2f6-113">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9e2f6-114">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9e2f6-115">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9e2f6-116">**Funksjonsnavn:** *Manuell forsendelseskonsolidering*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="9e2f6-117">Som nevnt i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md), må du også aktivere funksjonen *Konsolider forsendelse* før du kan opprette policyer.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="9e2f6-118">Du bør imidlertid allerede ha fullført det trinnet.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="9e2f6-119">Opprett salgsordrene for dette </span><span class="sxs-lookup"><span data-stu-id="9e2f6-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="9e2f6-120">Begynn med å opprette en samling salgsordrer du kan arbeide med.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="9e2f6-121">Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS).</span><span class="sxs-lookup"><span data-stu-id="9e2f6-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="9e2f6-122">Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="9e2f6-123">Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="9e2f6-124">Opprett ordresett 1</span><span class="sxs-lookup"><span data-stu-id="9e2f6-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="9e2f6-125">Salgsordrer 1-1 og 1-2</span><span class="sxs-lookup"><span data-stu-id="9e2f6-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="9e2f6-126">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-127">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9e2f6-128">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9e2f6-129">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-130">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-131">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-132">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="9e2f6-133">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="9e2f6-133">Sales order 1-3</span></span>

1. <span data-ttu-id="9e2f6-134">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-135">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9e2f6-136">**Leveringsmåte:** *10*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="9e2f6-137">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-138">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-139">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-140">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9e2f6-141">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-142">**Varenummer:** *A0002* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-143">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9e2f6-144">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9e2f6-145">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="9e2f6-146">Opprett ordresett 2</span><span class="sxs-lookup"><span data-stu-id="9e2f6-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="9e2f6-147">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="9e2f6-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="9e2f6-148">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-149">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="9e2f6-150">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9e2f6-151">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-152">**Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="9e2f6-153">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-154">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9e2f6-155">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-156">**Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="9e2f6-157">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9e2f6-158">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9e2f6-159">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="9e2f6-160">Opprett ordresett 3</span><span class="sxs-lookup"><span data-stu-id="9e2f6-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="9e2f6-161">Salgsordrer 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="9e2f6-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="9e2f6-162">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-163">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9e2f6-164">**Kunderekvisisjon:** *1*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9e2f6-165">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-166">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-167">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-168">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="9e2f6-169">Salgsordrer 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="9e2f6-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="9e2f6-170">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-171">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9e2f6-172">**Kunderekvisisjon:** *2*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="9e2f6-173">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-174">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-175">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-176">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="9e2f6-177">Opprett ordresett 4</span><span class="sxs-lookup"><span data-stu-id="9e2f6-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="9e2f6-178">Salgsordrer 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="9e2f6-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="9e2f6-179">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-180">**Kundekonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="9e2f6-181">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-182">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-183">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-184">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="9e2f6-185">Salgsordrer 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="9e2f6-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="9e2f6-186">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-187">**Kundekonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="9e2f6-188">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-189">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-190">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-191">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="9e2f6-192">Salgsordrer 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="9e2f6-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="9e2f6-193">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-194">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9e2f6-195">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-195">**Site:** *6*</span></span>
    - <span data-ttu-id="9e2f6-196">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9e2f6-197">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="9e2f6-198">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-199">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-200">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-201">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="9e2f6-202">Salgsordrer 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="9e2f6-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="9e2f6-203">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9e2f6-204">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9e2f6-205">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-205">**Site:** *6*</span></span>
    - <span data-ttu-id="9e2f6-206">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9e2f6-207">**Pulje:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="9e2f6-208">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9e2f6-209">**Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="9e2f6-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9e2f6-210">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9e2f6-211">Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="9e2f6-212">Frigi ordrene til lageret</span><span class="sxs-lookup"><span data-stu-id="9e2f6-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="9e2f6-213">Følg disse trinnene for å frigi hver salgsordre du har opprettet for dette , til lageret.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="9e2f6-214">Gå til **Kunde \> Ordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="9e2f6-215">Finn og velg salgosordren som skal frigis.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="9e2f6-216">I handlingsruten velger du **Handlinger \> Frigi til lager** i kategorien **Lager** for å frigi den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="9e2f6-217">Gjenta denne prosedyren for hver salgsordre du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="9e2f6-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="9e2f6-218">Konsolidere forsendelsene ved hjelp av arbeidsområdet for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9e2f6-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="9e2f6-219">Gå til **Lagerstyring \> Frigi til lager \> Arbeidsområde for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="9e2f6-220">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9e2f6-221">Velg **Legg til** i kategorien **Område** i dialogboksen for redigeringsprogrammet for spørring for å legge til en rad som har følgende innstillinger i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="9e2f6-222">**Tabell:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="9e2f6-223">**Felt:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="9e2f6-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="9e2f6-224">**Vilkår:** Angi en kommadelt liste over salgsordrenumrene for hvert ordresett du har opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="9e2f6-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="9e2f6-225">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="9e2f6-226">Velg **Konsolider forsendelser** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="9e2f6-227">Merk alle forsendelsene, og velg deretter **Konsolider** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="9e2f6-228">Bekrefte forsendelsene</span><span class="sxs-lookup"><span data-stu-id="9e2f6-228">Verify the shipments</span></span>

<span data-ttu-id="9e2f6-229">I den følgende prosedyren kan du kontrollere forsendelsene som er opprettet eller oppdatert som et resultat av forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="9e2f6-230">Bruk det til å gå gjennom hvert ordresett du har opprettet for dette , og se gjennom underinndelinge nedenfor for å kontrollere at du har fått de forventede resultatene.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="9e2f6-231">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="9e2f6-232">Finn og velg den påkrevde forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="9e2f6-233">Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="9e2f6-234">Relaterte forsendelser for ordresett 1</span><span class="sxs-lookup"><span data-stu-id="9e2f6-234">Related shipments for order set 1</span></span>

<span data-ttu-id="9e2f6-235">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="9e2f6-236">Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="9e2f6-237">Den andre forsendelen, som ikke bruker transportmåten *Airways*, ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="9e2f6-238">Relaterte forsendelser for ordresett 2</span><span class="sxs-lookup"><span data-stu-id="9e2f6-238">Related shipments for order set 2</span></span>

<span data-ttu-id="9e2f6-239">Tre forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="9e2f6-240">Den første forsendelsen inneholder varer med statusen *Brannfarlig*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="9e2f6-241">Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="9e2f6-242">Relaterte forsendelser for ordresett 3</span><span class="sxs-lookup"><span data-stu-id="9e2f6-242">Related shipments for order set 3</span></span>

<span data-ttu-id="9e2f6-243">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="9e2f6-244">Den første forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *1*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="9e2f6-245">Den andre forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *2*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="9e2f6-246">Relaterte forsendelser for ordresett 4</span><span class="sxs-lookup"><span data-stu-id="9e2f6-246">Related shipments for order set 4</span></span>

<span data-ttu-id="9e2f6-247">Fire forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="9e2f6-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="9e2f6-248">Linjer fra to ordrer for kunde *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9e2f6-249">Linjer fra to ordrer for kunde *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9e2f6-250">Linjer fra salgsordre 4-5 og 4-6 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9e2f6-251">Linjer fra salgsordre 4-7 og 4-8 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.</span><span class="sxs-lookup"><span data-stu-id="9e2f6-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e2f6-252">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9e2f6-252">Additional resources</span></span>

- [<span data-ttu-id="9e2f6-253">Policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9e2f6-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="9e2f6-254">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="9e2f6-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
