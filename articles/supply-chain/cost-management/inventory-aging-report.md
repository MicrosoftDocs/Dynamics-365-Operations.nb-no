---
title: Eksempler og logikk for rapport for aldersfordeling for lager
description: Dette emnet presenterer noen eksempler som viser hvordan du kan tolke resultatene av en rapport for aldersfordeling for lager.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983931"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="ea7a1-103">Eksempler og logikk for rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea7a1-104">Dette emnet presenterer noen eksempler som viser hvordan du kan tolke resultatene av en **Aldersfordeling for lager**-rapport.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="ea7a1-105">Denne rapporten kategoriserer antall på lager og lagerverdier for en valgt vare eller varegruppe i flere perioder.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="ea7a1-106">Dette emnet viser også den interne logikken i rapporten.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="ea7a1-107">Eksemplene i dette emnet viser resultater som vises på en standardrapport for **aldersfordeling for lager**.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="ea7a1-108">Generelt sett anbefales det imidlertid at du bruker versjonen [Lagring av rapport for aldersfordeling for lager](inventory-aging-report-storage.md) av denne rapporten, særlig når du har mange varer og lagre som må behandles.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="ea7a1-109">Lagring av rapport for aldersfordeling for lager lagrer hver rapport du genererer, viser resultatene som en interaktiv side og et diagram, og lar deg eksportere alle lagrede rapporter.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="ea7a1-110">Eksempeldata som brukes i disse eksemplene</span><span class="sxs-lookup"><span data-stu-id="ea7a1-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="ea7a1-111">Eksemplene i dette emnet er basert på eksempeldata for lagertransaksjon som er beskrevet i denne delen.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="ea7a1-112">Lagringsdimensjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="ea7a1-112">Storage dimension setup</span></span>

<span data-ttu-id="ea7a1-113">Eksempelsystemet inneholder følgende oppsett av lagringsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="ea7a1-114">Navn</span><span class="sxs-lookup"><span data-stu-id="ea7a1-114">Name</span></span>      | <span data-ttu-id="ea7a1-115">Aktivt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-115">Active</span></span> | <span data-ttu-id="ea7a1-116">Aktuell beholdning</span><span class="sxs-lookup"><span data-stu-id="ea7a1-116">Physical inventory</span></span> | <span data-ttu-id="ea7a1-117">Økonomisk lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="ea7a1-118">Nettsted</span><span class="sxs-lookup"><span data-stu-id="ea7a1-118">Site</span></span>      | <span data-ttu-id="ea7a1-119">Ja</span><span class="sxs-lookup"><span data-stu-id="ea7a1-119">Yes</span></span>    | <span data-ttu-id="ea7a1-120">Ja</span><span class="sxs-lookup"><span data-stu-id="ea7a1-120">Yes</span></span>                | <span data-ttu-id="ea7a1-121">Ja</span><span class="sxs-lookup"><span data-stu-id="ea7a1-121">Yes</span></span>                 |
| <span data-ttu-id="ea7a1-122">Lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-122">Warehouse</span></span> | <span data-ttu-id="ea7a1-123">Ja</span><span class="sxs-lookup"><span data-stu-id="ea7a1-123">Yes</span></span>    | <span data-ttu-id="ea7a1-124">Ja</span><span class="sxs-lookup"><span data-stu-id="ea7a1-124">Yes</span></span>                | <span data-ttu-id="ea7a1-125">Nei</span><span class="sxs-lookup"><span data-stu-id="ea7a1-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="ea7a1-126">Lagermodell</span><span class="sxs-lookup"><span data-stu-id="ea7a1-126">Inventory model</span></span>

<span data-ttu-id="ea7a1-127">For eksempelsystemet er lagermodellen for de frigitte produktene *FIFO*, og **Kostpris**-innstillingen for lagermodellen er *Ta med fysisk verdi*.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="ea7a1-128">Lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="ea7a1-128">Inventory transactions</span></span>

<span data-ttu-id="ea7a1-129">Eksempelsystemet inneholder følgende lagertransaksjoner for et frigitt produkt som har varenummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="ea7a1-130">Referanse</span><span class="sxs-lookup"><span data-stu-id="ea7a1-130">Reference</span></span>      | <span data-ttu-id="ea7a1-131">Nettsted</span><span class="sxs-lookup"><span data-stu-id="ea7a1-131">Site</span></span> | <span data-ttu-id="ea7a1-132">Lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-132">Warehouse</span></span> | <span data-ttu-id="ea7a1-133">Tilgang</span><span class="sxs-lookup"><span data-stu-id="ea7a1-133">Receipt</span></span>   | <span data-ttu-id="ea7a1-134">Avgang</span><span class="sxs-lookup"><span data-stu-id="ea7a1-134">Issue</span></span> | <span data-ttu-id="ea7a1-135">Fysisk dato</span><span class="sxs-lookup"><span data-stu-id="ea7a1-135">Physical date</span></span> | <span data-ttu-id="ea7a1-136">Økonomisk dato</span><span class="sxs-lookup"><span data-stu-id="ea7a1-136">Financial date</span></span> | <span data-ttu-id="ea7a1-137">Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-137">Quantity</span></span> | <span data-ttu-id="ea7a1-138">Kostnadsbeløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-138">Cost amount</span></span> | <span data-ttu-id="ea7a1-139">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="ea7a1-140">Bestilling</span><span class="sxs-lookup"><span data-stu-id="ea7a1-140">Purchase order</span></span> | <span data-ttu-id="ea7a1-141">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-141">1</span></span>    | <span data-ttu-id="ea7a1-142">11</span><span class="sxs-lookup"><span data-stu-id="ea7a1-142">11</span></span>        | <span data-ttu-id="ea7a1-143">Kjøpt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-143">Purchased</span></span> |       | <span data-ttu-id="ea7a1-144">15. mars</span><span class="sxs-lookup"><span data-stu-id="ea7a1-144">March 15</span></span>      | <span data-ttu-id="ea7a1-145">15. mars</span><span class="sxs-lookup"><span data-stu-id="ea7a1-145">March 15</span></span>       | <span data-ttu-id="ea7a1-146">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-146">10</span></span>       | <span data-ttu-id="ea7a1-147">1 000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-147">1,000</span></span>       | <span data-ttu-id="ea7a1-148">1 000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-148">1,000</span></span>                |
| <span data-ttu-id="ea7a1-149">Bestilling</span><span class="sxs-lookup"><span data-stu-id="ea7a1-149">Purchase order</span></span> | <span data-ttu-id="ea7a1-150">2</span><span class="sxs-lookup"><span data-stu-id="ea7a1-150">2</span></span>    | <span data-ttu-id="ea7a1-151">21</span><span class="sxs-lookup"><span data-stu-id="ea7a1-151">21</span></span>        | <span data-ttu-id="ea7a1-152">Kjøpt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-152">Purchased</span></span> |       | <span data-ttu-id="ea7a1-153">15. mars</span><span class="sxs-lookup"><span data-stu-id="ea7a1-153">March 15</span></span>      | <span data-ttu-id="ea7a1-154">15. mars</span><span class="sxs-lookup"><span data-stu-id="ea7a1-154">March 15</span></span>       | <span data-ttu-id="ea7a1-155">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-155">10</span></span>       | <span data-ttu-id="ea7a1-156">2,000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-156">2,000</span></span>       | <span data-ttu-id="ea7a1-157">2,000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-157">2,000</span></span>                |
| <span data-ttu-id="ea7a1-158">Bestilling</span><span class="sxs-lookup"><span data-stu-id="ea7a1-158">Purchase order</span></span> | <span data-ttu-id="ea7a1-159">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-159">1</span></span>    | <span data-ttu-id="ea7a1-160">11</span><span class="sxs-lookup"><span data-stu-id="ea7a1-160">11</span></span>        | <span data-ttu-id="ea7a1-161">Mottatt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-161">Received</span></span>  |       | <span data-ttu-id="ea7a1-162">15. april</span><span class="sxs-lookup"><span data-stu-id="ea7a1-162">April 15</span></span>      |                | <span data-ttu-id="ea7a1-163">5</span><span class="sxs-lookup"><span data-stu-id="ea7a1-163">5</span></span>        |             | <span data-ttu-id="ea7a1-164">375</span><span class="sxs-lookup"><span data-stu-id="ea7a1-164">375</span></span>                  |
| <span data-ttu-id="ea7a1-165">Overføringsordre</span><span class="sxs-lookup"><span data-stu-id="ea7a1-165">Transfer order</span></span> | <span data-ttu-id="ea7a1-166">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-166">1</span></span>    | <span data-ttu-id="ea7a1-167">11</span><span class="sxs-lookup"><span data-stu-id="ea7a1-167">11</span></span>        |           | <span data-ttu-id="ea7a1-168">Solgt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-168">Sold</span></span>  | <span data-ttu-id="ea7a1-169">2. mai</span><span class="sxs-lookup"><span data-stu-id="ea7a1-169">May 2</span></span>         | <span data-ttu-id="ea7a1-170">2. mai</span><span class="sxs-lookup"><span data-stu-id="ea7a1-170">May 2</span></span>          | <span data-ttu-id="ea7a1-171">-5</span><span class="sxs-lookup"><span data-stu-id="ea7a1-171">-5</span></span>       | <span data-ttu-id="ea7a1-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-172">-458.33</span></span>     | <span data-ttu-id="ea7a1-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-173">-458.33</span></span>              |
| <span data-ttu-id="ea7a1-174">Overføringsordre</span><span class="sxs-lookup"><span data-stu-id="ea7a1-174">Transfer order</span></span> | <span data-ttu-id="ea7a1-175">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-175">1</span></span>    | <span data-ttu-id="ea7a1-176">12</span><span class="sxs-lookup"><span data-stu-id="ea7a1-176">12</span></span>        | <span data-ttu-id="ea7a1-177">Kjøpt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-177">Purchased</span></span> |       | <span data-ttu-id="ea7a1-178">2. mai</span><span class="sxs-lookup"><span data-stu-id="ea7a1-178">May 2</span></span>         | <span data-ttu-id="ea7a1-179">2. mai</span><span class="sxs-lookup"><span data-stu-id="ea7a1-179">May 2</span></span>          | <span data-ttu-id="ea7a1-180">5</span><span class="sxs-lookup"><span data-stu-id="ea7a1-180">5</span></span>        | <span data-ttu-id="ea7a1-181">458.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-181">458.33</span></span>      | <span data-ttu-id="ea7a1-182">458.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-182">458.33</span></span>               |
| <span data-ttu-id="ea7a1-183">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="ea7a1-183">Sales order</span></span>    | <span data-ttu-id="ea7a1-184">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-184">1</span></span>    | <span data-ttu-id="ea7a1-185">12</span><span class="sxs-lookup"><span data-stu-id="ea7a1-185">12</span></span>        |           | <span data-ttu-id="ea7a1-186">Solgt</span><span class="sxs-lookup"><span data-stu-id="ea7a1-186">Sold</span></span>  | <span data-ttu-id="ea7a1-187">3. mai</span><span class="sxs-lookup"><span data-stu-id="ea7a1-187">May 3</span></span>         | <span data-ttu-id="ea7a1-188">3. mai</span><span class="sxs-lookup"><span data-stu-id="ea7a1-188">May 3</span></span>          | <span data-ttu-id="ea7a1-189">-1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-189">-1</span></span>       | <span data-ttu-id="ea7a1-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-190">-91.67</span></span>      | <span data-ttu-id="ea7a1-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="ea7a1-192">Slik beregnes antall og beløp i hver periode</span><span class="sxs-lookup"><span data-stu-id="ea7a1-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="ea7a1-193">Ved å bruke eksempeldataene som er beskrevet i de forrige delene, kan du kjøre en rapport for **aldersfordeling for lager** med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="ea7a1-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="ea7a1-194">**Per dato:** *9. mai 2020*</span><span class="sxs-lookup"><span data-stu-id="ea7a1-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="ea7a1-195">**Område:** *Visning*</span><span class="sxs-lookup"><span data-stu-id="ea7a1-195">**Site:** *View*</span></span>
- <span data-ttu-id="ea7a1-196">**Lager:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="ea7a1-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="ea7a1-197">**Varenummer:** *Total*</span><span class="sxs-lookup"><span data-stu-id="ea7a1-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="ea7a1-198">**Aldersfordelingsperiode:** Sett dette feltet til å generere månedlige perioder.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="ea7a1-199">I dette tilfellet vil innholdet i rapporten som genereres, ligne følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="ea7a1-200">Varenummer</span><span class="sxs-lookup"><span data-stu-id="ea7a1-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-201">Nettsted</span><span class="sxs-lookup"><span data-stu-id="ea7a1-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-202">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-203">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="ea7a1-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-204">Lagerverdiantall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-205">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="ea7a1-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-206">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="ea7a1-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-207">5/8/2020–5/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-208">4/30/2020–4/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-209">3/31/2020–3/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="ea7a1-210">P1:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-211">P1:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="ea7a1-212">P2:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-213">P2:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="ea7a1-214">P3:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-215">P3:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="ea7a1-216">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-216">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-217">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-217">1</span></span></td>
    <td><span data-ttu-id="ea7a1-218">14</span><span class="sxs-lookup"><span data-stu-id="ea7a1-218">14</span></span></td>
    <td><span data-ttu-id="ea7a1-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-219">1,283.33</span></span></td>
    <td><span data-ttu-id="ea7a1-220">14</span><span class="sxs-lookup"><span data-stu-id="ea7a1-220">14</span></span></td>
    <td><span data-ttu-id="ea7a1-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-221">1,283.33</span></span></td>
    <td><span data-ttu-id="ea7a1-222">91.67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-223">5.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-223">5.00</span></span></td>
    <td><span data-ttu-id="ea7a1-224">458.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-224">458.33</span></span></td>
    <td><span data-ttu-id="ea7a1-225">9.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-225">9.00</span></span></td>
    <td><span data-ttu-id="ea7a1-226">825.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="ea7a1-227">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-227">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-228">2</span><span class="sxs-lookup"><span data-stu-id="ea7a1-228">2</span></span></td>
    <td><span data-ttu-id="ea7a1-229">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-229">10</span></span></td>
    <td><span data-ttu-id="ea7a1-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-230">2,000.00</span></span></td>
    <td><span data-ttu-id="ea7a1-231">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-231">10</span></span></td>
    <td><span data-ttu-id="ea7a1-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-232">2,000.00</span></span></td>
    <td><span data-ttu-id="ea7a1-233">200.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-234">10,00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-234">10.00</span></span></td>
    <td><span data-ttu-id="ea7a1-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="ea7a1-236"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="ea7a1-243">Merk deg følgende detaljer i denne eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="ea7a1-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="ea7a1-244">Verdiene **Lagerverdiantall**, **Lagerverdi** og **Gjennomsnittlig enhetskostnad** som vises i rapporten, er verdier for den økonomiske lagerdimensjonen (**Område** i dette tilfellet).</span><span class="sxs-lookup"><span data-stu-id="ea7a1-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="ea7a1-245">Rapporten viser for eksempel følgende informasjon for område 1:</span><span class="sxs-lookup"><span data-stu-id="ea7a1-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="ea7a1-246">Verdien **Lagerverdiantall** er *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="ea7a1-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="ea7a1-247">Verdien **Lagerverdi** er *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="ea7a1-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="ea7a1-248">Verdien **Gjennomsnittlig enhetskostnad** er *91,67*.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="ea7a1-249">Verdien **Beholdningsverdi** og **Beløp** i hver periode beregnes ved hjelp av verdien **Gjennomsnittlig enhetskostnad**.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="ea7a1-250">Rapporten bestemmer lagerbeholdningen for hver periode ved å summere det totale mottatte beholdningsantallet for hver periode.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="ea7a1-251">Deretter brukes prinsippet først-inn-først-ut (FIFO) til å trekke fra det totale utstedte antallet, uansett lagermodellen som varene bruker.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="ea7a1-252">Hvis du kjører samme rapport på nytt, men denne gangen angir både verdiene **Område** og **Lager** til *Visning*, vil den nye rapporten ligne på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="ea7a1-253">Varenummer</span><span class="sxs-lookup"><span data-stu-id="ea7a1-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-254">Nettsted</span><span class="sxs-lookup"><span data-stu-id="ea7a1-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-255">Lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-256">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-257">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="ea7a1-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-258">Lagerverdiantall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-259">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="ea7a1-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-260">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="ea7a1-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-261">5/8/2020–5/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-262">4/30/2020–4/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-263">3/31/2020–3/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="ea7a1-264">P1:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-265">P1:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="ea7a1-266">P2:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-267">P2:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="ea7a1-268">P3:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-269">P3:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="ea7a1-270">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-270">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-271">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-271">1</span></span></td>
    <td><span data-ttu-id="ea7a1-272">11</span><span class="sxs-lookup"><span data-stu-id="ea7a1-272">11</span></span></td>
    <td><span data-ttu-id="ea7a1-273">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-273">10</span></span></td>
    <td><span data-ttu-id="ea7a1-274">916.67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-274">916.67</span></span></td>
    <td><span data-ttu-id="ea7a1-275">14</span><span class="sxs-lookup"><span data-stu-id="ea7a1-275">14</span></span></td>
    <td><span data-ttu-id="ea7a1-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-276">1,283.33</span></span></td>
    <td><span data-ttu-id="ea7a1-277">91.67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-278">5.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-278">5.00</span></span></td>
    <td><span data-ttu-id="ea7a1-279">458.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-279">458.33</span></span></td>
    <td><span data-ttu-id="ea7a1-280">5.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-280">5.00</span></span></td>
    <td><span data-ttu-id="ea7a1-281">458.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="ea7a1-282">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-282">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-283">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-283">1</span></span></td>
    <td><span data-ttu-id="ea7a1-284">12</span><span class="sxs-lookup"><span data-stu-id="ea7a1-284">12</span></span></td>
    <td><span data-ttu-id="ea7a1-285">4</span><span class="sxs-lookup"><span data-stu-id="ea7a1-285">4</span></span></td>
    <td><span data-ttu-id="ea7a1-286">366.67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-286">366.67</span></span></td>
    <td><span data-ttu-id="ea7a1-287">14</span><span class="sxs-lookup"><span data-stu-id="ea7a1-287">14</span></span></td>
    <td><span data-ttu-id="ea7a1-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ea7a1-288">1,283.33</span></span></td>
    <td><span data-ttu-id="ea7a1-289">91.67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-289">91.67</span></span></td>
    <td><span data-ttu-id="ea7a1-290">4.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-290">4.00</span></span></td>
    <td><span data-ttu-id="ea7a1-291">366.67</span><span class="sxs-lookup"><span data-stu-id="ea7a1-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="ea7a1-292">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-292">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-293">2</span><span class="sxs-lookup"><span data-stu-id="ea7a1-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-294">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-294">10</span></span></td>
    <td><span data-ttu-id="ea7a1-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-295">2,000.00</span></span></td>
    <td><span data-ttu-id="ea7a1-296">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-296">10</span></span></td>
    <td><span data-ttu-id="ea7a1-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-297">2,000.00</span></span></td>
    <td><span data-ttu-id="ea7a1-298">200.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-299">10,00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-299">10.00</span></span></td>
    <td><span data-ttu-id="ea7a1-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="ea7a1-301"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="ea7a1-310">Denne gangen er område 1 delt inn i to rader, én for lager 11 og én for lager 12.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="ea7a1-311">Verdiene **Lagerverdiantall**, **Lagerverdi** og **Gjennomsnittlig enhetskostnad** er imidlertid de samme fordi **Lager** ikke er en økonomisk lagerdimensjon.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="ea7a1-312">Legg også merke til at antallsdistribusjonen for område 1 er forskjellig.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="ea7a1-313">I den første rapporten du kjørte, ignorerte systemet overføringsordren som ble funnet på det samme området, og trakk fra antallet av salgsfakturaen fra **3/31/2020–3/1/2020**-perioden i område 1.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="ea7a1-314">I den nye rapporten trekker imidlertid systemet fra antallet for salgsfakturaen fra **5/8/2020–5/1/2020**-perioden i lager 12.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="ea7a1-315">Virkninger av lagerlukking</span><span class="sxs-lookup"><span data-stu-id="ea7a1-315">Effects of inventory closing</span></span>

<span data-ttu-id="ea7a1-316">Hvis du kjører lagerlukking for mai og deretter kjører den forrige rapporten på nytt, men du angir feltet **Per dato** til *31. mai 2020*, vil du se følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="ea7a1-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="ea7a1-317">Verdiene **Beholdningsverdi** og **Gjennomsnittlig enhetskostnad** oppdateres.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="ea7a1-318">Verdien **Beholdningsverdi** og verdiene **Beløp** i hver periode oppdateres i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="ea7a1-319">Den nye rapporten vil ligne på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="ea7a1-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="ea7a1-320">Varenummer</span><span class="sxs-lookup"><span data-stu-id="ea7a1-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-321">Nettsted</span><span class="sxs-lookup"><span data-stu-id="ea7a1-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-322">Lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-323">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="ea7a1-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-324">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="ea7a1-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-325">Lagerverdiantall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-326">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="ea7a1-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ea7a1-327">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="ea7a1-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-328">5/31/2020–5/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-329">4/30/2020–4/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ea7a1-330">3/31/2020–3/1/2020</span><span class="sxs-lookup"><span data-stu-id="ea7a1-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="ea7a1-331">P1:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-332">P1:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="ea7a1-333">P2:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-334">P2:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="ea7a1-335">P3:Antall</span><span class="sxs-lookup"><span data-stu-id="ea7a1-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="ea7a1-336">P3:Beløp</span><span class="sxs-lookup"><span data-stu-id="ea7a1-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="ea7a1-337">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-337">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-338">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-338">1</span></span></td>
    <td><span data-ttu-id="ea7a1-339">11</span><span class="sxs-lookup"><span data-stu-id="ea7a1-339">11</span></span></td>
    <td><span data-ttu-id="ea7a1-340">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-340">10</span></span></td>
    <td><span data-ttu-id="ea7a1-341">910.70</span><span class="sxs-lookup"><span data-stu-id="ea7a1-341">910.70</span></span></td>
    <td><span data-ttu-id="ea7a1-342">14</span><span class="sxs-lookup"><span data-stu-id="ea7a1-342">14</span></span></td>
    <td><span data-ttu-id="ea7a1-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-343">1,275.00</span></span></td>
    <td><span data-ttu-id="ea7a1-344">91.07</span><span class="sxs-lookup"><span data-stu-id="ea7a1-344">91.07</span></span></td>
    <td><span data-ttu-id="ea7a1-345">0.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-346">5.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-346">5.00</span></span></td>
    <td><span data-ttu-id="ea7a1-347">455.36</span><span class="sxs-lookup"><span data-stu-id="ea7a1-347">455.36</span></span></td>
    <td><span data-ttu-id="ea7a1-348">5.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-348">5.00</span></span></td>
    <td><span data-ttu-id="ea7a1-349">455.36</span><span class="sxs-lookup"><span data-stu-id="ea7a1-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="ea7a1-350">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-350">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-351">1</span><span class="sxs-lookup"><span data-stu-id="ea7a1-351">1</span></span></td>
    <td><span data-ttu-id="ea7a1-352">12</span><span class="sxs-lookup"><span data-stu-id="ea7a1-352">12</span></span></td>
    <td><span data-ttu-id="ea7a1-353">4</span><span class="sxs-lookup"><span data-stu-id="ea7a1-353">4</span></span></td>
    <td><span data-ttu-id="ea7a1-354">364.29</span><span class="sxs-lookup"><span data-stu-id="ea7a1-354">364.29</span></span></td>
    <td><span data-ttu-id="ea7a1-355">14</span><span class="sxs-lookup"><span data-stu-id="ea7a1-355">14</span></span></td>
    <td><span data-ttu-id="ea7a1-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-356">1,275.00</span></span></td>
    <td><span data-ttu-id="ea7a1-357">91.07</span><span class="sxs-lookup"><span data-stu-id="ea7a1-357">91.07</span></span></td>
    <td><span data-ttu-id="ea7a1-358">4.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-358">4.00</span></span></td>
    <td><span data-ttu-id="ea7a1-359">364.29</span><span class="sxs-lookup"><span data-stu-id="ea7a1-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="ea7a1-360">1000</span><span class="sxs-lookup"><span data-stu-id="ea7a1-360">1000</span></span></td>
    <td><span data-ttu-id="ea7a1-361">2</span><span class="sxs-lookup"><span data-stu-id="ea7a1-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-362">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-362">10</span></span></td>
    <td><span data-ttu-id="ea7a1-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-363">2,000.00</span></span></td>
    <td><span data-ttu-id="ea7a1-364">10</span><span class="sxs-lookup"><span data-stu-id="ea7a1-364">10</span></span></td>
    <td><span data-ttu-id="ea7a1-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-365">2,000.00</span></span></td>
    <td><span data-ttu-id="ea7a1-366">200.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-367">10,00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-367">10.00</span></span></td>
    <td><span data-ttu-id="ea7a1-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ea7a1-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="ea7a1-369"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ea7a1-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="ea7a1-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="ea7a1-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
