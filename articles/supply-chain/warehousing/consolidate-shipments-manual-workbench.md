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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1eec1a8e3a9a2a0f95302e1d6ea68eb90b9a3b93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016822"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="fa470-103">Konsolidere forsendelser ved hjelp av arbeidsområdet for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="fa470-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa470-104">Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert til forsendelser senere ved hjelp av arbeidsområdet for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="fa470-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="fa470-105">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="fa470-105">Make demo data available</span></span>

<span data-ttu-id="fa470-106"> i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fa470-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fa470-107">Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="fa470-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="fa470-108">Definer policyer for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="fa470-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="fa470-109"> som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="fa470-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="fa470-110">Husk å utføre øvelsene før du fortsetter med dette .</span><span class="sxs-lookup"><span data-stu-id="fa470-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="fa470-111">Aktivere funksjonen Manuell forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="fa470-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="fa470-112">Før du kan bruke funksjonen *Manuell forsendelseskonsolidering* , må du aktivere den i systemet.</span><span class="sxs-lookup"><span data-stu-id="fa470-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="fa470-113">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="fa470-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="fa470-114">I **Funksjonsadministrering** -arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="fa470-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fa470-115">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="fa470-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="fa470-116">**Funksjonsnavn:** *Manuell forsendelseskonsolidering*</span><span class="sxs-lookup"><span data-stu-id="fa470-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="fa470-117">Som nevnt i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md), må du også aktivere funksjonen *Konsolider forsendelse* før du kan opprette policyer.</span><span class="sxs-lookup"><span data-stu-id="fa470-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="fa470-118">Du bør imidlertid allerede ha fullført det trinnet.</span><span class="sxs-lookup"><span data-stu-id="fa470-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="fa470-119">Opprett salgsordrene for dette </span><span class="sxs-lookup"><span data-stu-id="fa470-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="fa470-120">Begynn med å opprette en samling salgsordrer du kan arbeide med.</span><span class="sxs-lookup"><span data-stu-id="fa470-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="fa470-121">Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS).</span><span class="sxs-lookup"><span data-stu-id="fa470-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="fa470-122">Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.</span><span class="sxs-lookup"><span data-stu-id="fa470-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="fa470-123">Gå til **Kunde \> Ordrer \> Alle salgsordrer** , og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.</span><span class="sxs-lookup"><span data-stu-id="fa470-123">Go to **Accounts receivable \> Orders \> All sales orders** , and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="fa470-124">Opprett ordresett 1</span><span class="sxs-lookup"><span data-stu-id="fa470-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="fa470-125">Salgsordrer 1-1 og 1-2</span><span class="sxs-lookup"><span data-stu-id="fa470-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="fa470-126">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-127">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="fa470-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="fa470-128">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="fa470-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="fa470-129">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-130">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-131">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-132">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-132">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="fa470-133">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="fa470-133">Sales order 1-3</span></span>

1. <span data-ttu-id="fa470-134">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="fa470-135">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="fa470-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="fa470-136">**Leveringsmåte:** *10*</span><span class="sxs-lookup"><span data-stu-id="fa470-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="fa470-137">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-138">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-139">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-140">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-140">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="fa470-141">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-142">**Varenummer:** *A0002* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-143">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="fa470-144">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="fa470-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="fa470-145">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-145">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="fa470-146">Opprett ordresett 2</span><span class="sxs-lookup"><span data-stu-id="fa470-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="fa470-147">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="fa470-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="fa470-148">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-149">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="fa470-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="fa470-150">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="fa470-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="fa470-151">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-152">**Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig* )</span><span class="sxs-lookup"><span data-stu-id="fa470-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable* )</span></span>
    - <span data-ttu-id="fa470-153">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-154">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-154">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="fa470-155">Legg til en ny ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-156">**Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt* )</span><span class="sxs-lookup"><span data-stu-id="fa470-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive* )</span></span>
    - <span data-ttu-id="fa470-157">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="fa470-158">**Leveringsmåte:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="fa470-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="fa470-159">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-159">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="fa470-160">Opprett ordresett 3</span><span class="sxs-lookup"><span data-stu-id="fa470-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="fa470-161">Salgsordrer 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="fa470-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="fa470-162">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-163">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="fa470-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="fa470-164">**Kunderekvisisjon:** *1*</span><span class="sxs-lookup"><span data-stu-id="fa470-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="fa470-165">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-166">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-167">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-168">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-168">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="fa470-169">Salgsordrer 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="fa470-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="fa470-170">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-171">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="fa470-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="fa470-172">**Kunderekvisisjon:** *2*</span><span class="sxs-lookup"><span data-stu-id="fa470-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="fa470-173">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-174">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-175">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-176">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-176">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="fa470-177">Opprett ordresett 4</span><span class="sxs-lookup"><span data-stu-id="fa470-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="fa470-178">Salgsordrer 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="fa470-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="fa470-179">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-180">**Kundekonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="fa470-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="fa470-181">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-182">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-183">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-184">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-184">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="fa470-185">Salgsordrer 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="fa470-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="fa470-186">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-187">**Kundekonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="fa470-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="fa470-188">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-189">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-190">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-191">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-191">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="fa470-192">Salgsordrer 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="fa470-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="fa470-193">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-194">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="fa470-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="fa470-195">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="fa470-195">**Site:** *6*</span></span>
    - <span data-ttu-id="fa470-196">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="fa470-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="fa470-197">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="fa470-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="fa470-198">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-199">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-200">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-201">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-201">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="fa470-202">Salgsordrer 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="fa470-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="fa470-203">Opprett to identiske salgsordrer som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="fa470-204">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="fa470-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="fa470-205">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="fa470-205">**Site:** *6*</span></span>
    - <span data-ttu-id="fa470-206">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="fa470-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="fa470-207">**Pulje:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fa470-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="fa470-208">Legg til en ordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="fa470-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="fa470-209">**Varenummer:** *A0001* (en vare uten **Kode 4** -filter tilordnet)</span><span class="sxs-lookup"><span data-stu-id="fa470-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="fa470-210">**Antall:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="fa470-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="fa470-211">Velg **Lager \> Reservasjon** , og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fa470-211">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="fa470-212">Frigi ordrene til lageret</span><span class="sxs-lookup"><span data-stu-id="fa470-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="fa470-213">Følg disse trinnene for å frigi hver salgsordre du har opprettet for dette , til lageret.</span><span class="sxs-lookup"><span data-stu-id="fa470-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="fa470-214">Gå til **Kunde \> Ordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="fa470-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="fa470-215">Finn og velg salgosordren som skal frigis.</span><span class="sxs-lookup"><span data-stu-id="fa470-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="fa470-216">I handlingsruten velger du **Handlinger \> Frigi til lager** i kategorien **Lager** for å frigi den valgte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="fa470-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="fa470-217">Gjenta denne prosedyren for hver salgsordre du opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="fa470-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="fa470-218">Konsolidere forsendelsene ved hjelp av arbeidsområdet for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="fa470-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="fa470-219">Gå til **Lagerstyring \> Frigi til lager \> Arbeidsområde for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="fa470-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="fa470-220">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="fa470-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="fa470-221">Velg **Legg til** i kategorien **Område** i dialogboksen for redigeringsprogrammet for spørring for å legge til en rad som har følgende innstillinger i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="fa470-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="fa470-222">**Tabell:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="fa470-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="fa470-223">**Felt:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="fa470-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="fa470-224">**Vilkår:** Angi en kommadelt liste over salgsordrenumrene for hvert ordresett du har opprettet for dette .</span><span class="sxs-lookup"><span data-stu-id="fa470-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="fa470-225">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fa470-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="fa470-226">Velg **Konsolider forsendelser** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fa470-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="fa470-227">Merk alle forsendelsene, og velg deretter **Konsolider** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fa470-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="fa470-228">Bekrefte forsendelsene</span><span class="sxs-lookup"><span data-stu-id="fa470-228">Verify the shipments</span></span>

<span data-ttu-id="fa470-229">I den følgende prosedyren kan du kontrollere forsendelsene som er opprettet eller oppdatert som et resultat av forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="fa470-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="fa470-230">Bruk det til å gå gjennom hvert ordresett du har opprettet for dette , og se gjennom underinndelinge nedenfor for å kontrollere at du har fått de forventede resultatene.</span><span class="sxs-lookup"><span data-stu-id="fa470-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="fa470-231">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="fa470-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="fa470-232">Finn og velg den påkrevde forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="fa470-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="fa470-233">Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="fa470-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="fa470-234">Relaterte forsendelser for ordresett 1</span><span class="sxs-lookup"><span data-stu-id="fa470-234">Related shipments for order set 1</span></span>

<span data-ttu-id="fa470-235">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="fa470-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="fa470-236">Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="fa470-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="fa470-237">Den andre forsendelen, som ikke bruker transportmåten *Airways* , ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="fa470-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="fa470-238">Relaterte forsendelser for ordresett 2</span><span class="sxs-lookup"><span data-stu-id="fa470-238">Related shipments for order set 2</span></span>

<span data-ttu-id="fa470-239">Tre forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="fa470-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="fa470-240">Den første forsendelsen inneholder varer med statusen *Brannfarlig*.</span><span class="sxs-lookup"><span data-stu-id="fa470-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="fa470-241">Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.</span><span class="sxs-lookup"><span data-stu-id="fa470-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="fa470-242">Relaterte forsendelser for ordresett 3</span><span class="sxs-lookup"><span data-stu-id="fa470-242">Related shipments for order set 3</span></span>

<span data-ttu-id="fa470-243">To forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="fa470-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="fa470-244">Den første forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *1*.</span><span class="sxs-lookup"><span data-stu-id="fa470-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="fa470-245">Den andre forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *2*.</span><span class="sxs-lookup"><span data-stu-id="fa470-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="fa470-246">Relaterte forsendelser for ordresett 4</span><span class="sxs-lookup"><span data-stu-id="fa470-246">Related shipments for order set 4</span></span>

<span data-ttu-id="fa470-247">Fire forsendelser skal ha blitt opprettet:</span><span class="sxs-lookup"><span data-stu-id="fa470-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="fa470-248">Linjer fra to ordrer for kunde *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="fa470-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="fa470-249">Linjer fra to ordrer for kunde *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="fa470-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="fa470-250">Linjer fra salgsordre 4-5 og 4-6 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.</span><span class="sxs-lookup"><span data-stu-id="fa470-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="fa470-251">Linjer fra salgsordre 4-7 og 4-8 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.</span><span class="sxs-lookup"><span data-stu-id="fa470-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa470-252">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fa470-252">Additional resources</span></span>

- [<span data-ttu-id="fa470-253">Policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="fa470-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="fa470-254">Konfigurere policyer for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="fa470-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
