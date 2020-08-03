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
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb7b7a055c26b53ee3acc3b872acf04fcf089eca
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597246"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="894b8-103">Eksempler og logikk for rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="894b8-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="894b8-104">Dette emnet presenterer noen eksempler som viser hvordan du kan tolke resultatene av en **Aldersfordeling for lager**-rapport.</span><span class="sxs-lookup"><span data-stu-id="894b8-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="894b8-105">Denne rapporten kategoriserer antall på lager og lagerverdier for en valgt vare eller varegruppe i flere perioder.</span><span class="sxs-lookup"><span data-stu-id="894b8-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="894b8-106">Dette emnet viser også den interne logikken i rapporten.</span><span class="sxs-lookup"><span data-stu-id="894b8-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="894b8-107">Eksemplene i dette emnet viser resultater som vises på en standardrapport for **aldersfordeling for lager**.</span><span class="sxs-lookup"><span data-stu-id="894b8-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="894b8-108">Generelt sett anbefales det imidlertid at du bruker versjonen [Lagring av rapport for aldersfordeling for lager](inventory-aging-report-storage.md) av denne rapporten, særlig når du har mange varer og lagre som må behandles.</span><span class="sxs-lookup"><span data-stu-id="894b8-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="894b8-109">Lagring av rapport for aldersfordeling for lager lagrer hver rapport du genererer, viser resultatene som en interaktiv side og et diagram, og lar deg eksportere alle lagrede rapporter.</span><span class="sxs-lookup"><span data-stu-id="894b8-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="894b8-110">Eksempeldata som brukes i disse eksemplene</span><span class="sxs-lookup"><span data-stu-id="894b8-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="894b8-111">Eksemplene i dette emnet er basert på eksempeldata for lagertransaksjon som er beskrevet i denne delen.</span><span class="sxs-lookup"><span data-stu-id="894b8-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="894b8-112">Lagringsdimensjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="894b8-112">Storage dimension setup</span></span>

<span data-ttu-id="894b8-113">Eksempelsystemet inneholder følgende oppsett av lagringsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="894b8-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="894b8-114">Navn</span><span class="sxs-lookup"><span data-stu-id="894b8-114">Name</span></span>      | <span data-ttu-id="894b8-115">Aktivt</span><span class="sxs-lookup"><span data-stu-id="894b8-115">Active</span></span> | <span data-ttu-id="894b8-116">Aktuell beholdning</span><span class="sxs-lookup"><span data-stu-id="894b8-116">Physical inventory</span></span> | <span data-ttu-id="894b8-117">Økonomisk lager</span><span class="sxs-lookup"><span data-stu-id="894b8-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="894b8-118">Nettsted</span><span class="sxs-lookup"><span data-stu-id="894b8-118">Site</span></span>      | <span data-ttu-id="894b8-119">Ja</span><span class="sxs-lookup"><span data-stu-id="894b8-119">Yes</span></span>    | <span data-ttu-id="894b8-120">Ja</span><span class="sxs-lookup"><span data-stu-id="894b8-120">Yes</span></span>                | <span data-ttu-id="894b8-121">Ja</span><span class="sxs-lookup"><span data-stu-id="894b8-121">Yes</span></span>                 |
| <span data-ttu-id="894b8-122">Lager</span><span class="sxs-lookup"><span data-stu-id="894b8-122">Warehouse</span></span> | <span data-ttu-id="894b8-123">Ja</span><span class="sxs-lookup"><span data-stu-id="894b8-123">Yes</span></span>    | <span data-ttu-id="894b8-124">Ja</span><span class="sxs-lookup"><span data-stu-id="894b8-124">Yes</span></span>                | <span data-ttu-id="894b8-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="894b8-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="894b8-126">Lagermodell</span><span class="sxs-lookup"><span data-stu-id="894b8-126">Inventory model</span></span>

<span data-ttu-id="894b8-127">For eksempelsystemet er lagermodellen for de frigitte produktene *FIFO*, og **Kostpris**-innstillingen for lagermodellen er *Ta med fysisk verdi*.</span><span class="sxs-lookup"><span data-stu-id="894b8-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="894b8-128">Lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="894b8-128">Inventory transactions</span></span>

<span data-ttu-id="894b8-129">Eksempelsystemet inneholder følgende lagertransaksjoner for et frigitt produkt som har varenummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="894b8-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="894b8-130">Referanse</span><span class="sxs-lookup"><span data-stu-id="894b8-130">Reference</span></span>      | <span data-ttu-id="894b8-131">Nettsted</span><span class="sxs-lookup"><span data-stu-id="894b8-131">Site</span></span> | <span data-ttu-id="894b8-132">Lager</span><span class="sxs-lookup"><span data-stu-id="894b8-132">Warehouse</span></span> | <span data-ttu-id="894b8-133">Tilgang</span><span class="sxs-lookup"><span data-stu-id="894b8-133">Receipt</span></span>   | <span data-ttu-id="894b8-134">Avgang</span><span class="sxs-lookup"><span data-stu-id="894b8-134">Issue</span></span> | <span data-ttu-id="894b8-135">Fysisk dato</span><span class="sxs-lookup"><span data-stu-id="894b8-135">Physical date</span></span> | <span data-ttu-id="894b8-136">Økonomisk dato</span><span class="sxs-lookup"><span data-stu-id="894b8-136">Financial date</span></span> | <span data-ttu-id="894b8-137">Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-137">Quantity</span></span> | <span data-ttu-id="894b8-138">Kostnadsbeløp</span><span class="sxs-lookup"><span data-stu-id="894b8-138">Cost amount</span></span> | <span data-ttu-id="894b8-139">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="894b8-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="894b8-140">Bestilling</span><span class="sxs-lookup"><span data-stu-id="894b8-140">Purchase order</span></span> | <span data-ttu-id="894b8-141">1</span><span class="sxs-lookup"><span data-stu-id="894b8-141">1</span></span>    | <span data-ttu-id="894b8-142">11</span><span class="sxs-lookup"><span data-stu-id="894b8-142">11</span></span>        | <span data-ttu-id="894b8-143">Kjøpt</span><span class="sxs-lookup"><span data-stu-id="894b8-143">Purchased</span></span> |       | <span data-ttu-id="894b8-144">15. mars</span><span class="sxs-lookup"><span data-stu-id="894b8-144">March 15</span></span>      | <span data-ttu-id="894b8-145">15. mars</span><span class="sxs-lookup"><span data-stu-id="894b8-145">March 15</span></span>       | <span data-ttu-id="894b8-146">10</span><span class="sxs-lookup"><span data-stu-id="894b8-146">10</span></span>       | <span data-ttu-id="894b8-147">1 000</span><span class="sxs-lookup"><span data-stu-id="894b8-147">1,000</span></span>       | <span data-ttu-id="894b8-148">1 000</span><span class="sxs-lookup"><span data-stu-id="894b8-148">1,000</span></span>                |
| <span data-ttu-id="894b8-149">Bestilling</span><span class="sxs-lookup"><span data-stu-id="894b8-149">Purchase order</span></span> | <span data-ttu-id="894b8-150">2</span><span class="sxs-lookup"><span data-stu-id="894b8-150">2</span></span>    | <span data-ttu-id="894b8-151">21</span><span class="sxs-lookup"><span data-stu-id="894b8-151">21</span></span>        | <span data-ttu-id="894b8-152">Kjøpt</span><span class="sxs-lookup"><span data-stu-id="894b8-152">Purchased</span></span> |       | <span data-ttu-id="894b8-153">15. mars</span><span class="sxs-lookup"><span data-stu-id="894b8-153">March 15</span></span>      | <span data-ttu-id="894b8-154">15. mars</span><span class="sxs-lookup"><span data-stu-id="894b8-154">March 15</span></span>       | <span data-ttu-id="894b8-155">10</span><span class="sxs-lookup"><span data-stu-id="894b8-155">10</span></span>       | <span data-ttu-id="894b8-156">2,000</span><span class="sxs-lookup"><span data-stu-id="894b8-156">2,000</span></span>       | <span data-ttu-id="894b8-157">2,000</span><span class="sxs-lookup"><span data-stu-id="894b8-157">2,000</span></span>                |
| <span data-ttu-id="894b8-158">Bestilling</span><span class="sxs-lookup"><span data-stu-id="894b8-158">Purchase order</span></span> | <span data-ttu-id="894b8-159">1</span><span class="sxs-lookup"><span data-stu-id="894b8-159">1</span></span>    | <span data-ttu-id="894b8-160">11</span><span class="sxs-lookup"><span data-stu-id="894b8-160">11</span></span>        | <span data-ttu-id="894b8-161">Mottatt</span><span class="sxs-lookup"><span data-stu-id="894b8-161">Received</span></span>  |       | <span data-ttu-id="894b8-162">15. april</span><span class="sxs-lookup"><span data-stu-id="894b8-162">April 15</span></span>      |                | <span data-ttu-id="894b8-163">5</span><span class="sxs-lookup"><span data-stu-id="894b8-163">5</span></span>        |             | <span data-ttu-id="894b8-164">375</span><span class="sxs-lookup"><span data-stu-id="894b8-164">375</span></span>                  |
| <span data-ttu-id="894b8-165">Overføringsordre</span><span class="sxs-lookup"><span data-stu-id="894b8-165">Transfer order</span></span> | <span data-ttu-id="894b8-166">1</span><span class="sxs-lookup"><span data-stu-id="894b8-166">1</span></span>    | <span data-ttu-id="894b8-167">11</span><span class="sxs-lookup"><span data-stu-id="894b8-167">11</span></span>        |           | <span data-ttu-id="894b8-168">Solgt</span><span class="sxs-lookup"><span data-stu-id="894b8-168">Sold</span></span>  | <span data-ttu-id="894b8-169">2. mai</span><span class="sxs-lookup"><span data-stu-id="894b8-169">May 2</span></span>         | <span data-ttu-id="894b8-170">2. mai</span><span class="sxs-lookup"><span data-stu-id="894b8-170">May 2</span></span>          | <span data-ttu-id="894b8-171">-5</span><span class="sxs-lookup"><span data-stu-id="894b8-171">-5</span></span>       | <span data-ttu-id="894b8-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="894b8-172">-458.33</span></span>     | <span data-ttu-id="894b8-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="894b8-173">-458.33</span></span>              |
| <span data-ttu-id="894b8-174">Overføringsordre</span><span class="sxs-lookup"><span data-stu-id="894b8-174">Transfer order</span></span> | <span data-ttu-id="894b8-175">1</span><span class="sxs-lookup"><span data-stu-id="894b8-175">1</span></span>    | <span data-ttu-id="894b8-176">12</span><span class="sxs-lookup"><span data-stu-id="894b8-176">12</span></span>        | <span data-ttu-id="894b8-177">Kjøpt</span><span class="sxs-lookup"><span data-stu-id="894b8-177">Purchased</span></span> |       | <span data-ttu-id="894b8-178">2. mai</span><span class="sxs-lookup"><span data-stu-id="894b8-178">May 2</span></span>         | <span data-ttu-id="894b8-179">2. mai</span><span class="sxs-lookup"><span data-stu-id="894b8-179">May 2</span></span>          | <span data-ttu-id="894b8-180">5</span><span class="sxs-lookup"><span data-stu-id="894b8-180">5</span></span>        | <span data-ttu-id="894b8-181">458.33</span><span class="sxs-lookup"><span data-stu-id="894b8-181">458.33</span></span>      | <span data-ttu-id="894b8-182">458.33</span><span class="sxs-lookup"><span data-stu-id="894b8-182">458.33</span></span>               |
| <span data-ttu-id="894b8-183">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="894b8-183">Sales order</span></span>    | <span data-ttu-id="894b8-184">1</span><span class="sxs-lookup"><span data-stu-id="894b8-184">1</span></span>    | <span data-ttu-id="894b8-185">12</span><span class="sxs-lookup"><span data-stu-id="894b8-185">12</span></span>        |           | <span data-ttu-id="894b8-186">Solgt</span><span class="sxs-lookup"><span data-stu-id="894b8-186">Sold</span></span>  | <span data-ttu-id="894b8-187">3. mai</span><span class="sxs-lookup"><span data-stu-id="894b8-187">May 3</span></span>         | <span data-ttu-id="894b8-188">3. mai</span><span class="sxs-lookup"><span data-stu-id="894b8-188">May 3</span></span>          | <span data-ttu-id="894b8-189">-1</span><span class="sxs-lookup"><span data-stu-id="894b8-189">-1</span></span>       | <span data-ttu-id="894b8-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="894b8-190">-91.67</span></span>      | <span data-ttu-id="894b8-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="894b8-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="894b8-192">Slik beregnes antall og beløp i hver periode</span><span class="sxs-lookup"><span data-stu-id="894b8-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="894b8-193">Ved å bruke eksempeldataene som er beskrevet i de forrige delene, kan du kjøre en rapport for **aldersfordeling for lager** med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="894b8-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="894b8-194">**Per dato:** *9. mai 2020*</span><span class="sxs-lookup"><span data-stu-id="894b8-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="894b8-195">**Område:** *Visning*</span><span class="sxs-lookup"><span data-stu-id="894b8-195">**Site:** *View*</span></span>
- <span data-ttu-id="894b8-196">**Lager:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="894b8-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="894b8-197">**Varenummer:** *Total*</span><span class="sxs-lookup"><span data-stu-id="894b8-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="894b8-198">**Aldersfordelingsperiode:** Sett dette feltet til å generere månedlige perioder.</span><span class="sxs-lookup"><span data-stu-id="894b8-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="894b8-199">I dette tilfellet vil innholdet i rapporten som genereres, ligne følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="894b8-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="894b8-200">Varenummer</span><span class="sxs-lookup"><span data-stu-id="894b8-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-201">Nettsted</span><span class="sxs-lookup"><span data-stu-id="894b8-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-202">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="894b8-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-203">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="894b8-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-204">Lagerverdiantall</span><span class="sxs-lookup"><span data-stu-id="894b8-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-205">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="894b8-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-206">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="894b8-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-207">5/8/2020–5/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-208">4/30/2020–4/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-209">3/31/2020–3/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="894b8-210">P1:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-211">P1:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="894b8-212">P2:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-213">P2:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="894b8-214">P3:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-215">P3:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="894b8-216">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-216">1000</span></span></td>
    <td><span data-ttu-id="894b8-217">1</span><span class="sxs-lookup"><span data-stu-id="894b8-217">1</span></span></td>
    <td><span data-ttu-id="894b8-218">14</span><span class="sxs-lookup"><span data-stu-id="894b8-218">14</span></span></td>
    <td><span data-ttu-id="894b8-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="894b8-219">1,283.33</span></span></td>
    <td><span data-ttu-id="894b8-220">14</span><span class="sxs-lookup"><span data-stu-id="894b8-220">14</span></span></td>
    <td><span data-ttu-id="894b8-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="894b8-221">1,283.33</span></span></td>
    <td><span data-ttu-id="894b8-222">91.67</span><span class="sxs-lookup"><span data-stu-id="894b8-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-223">5.00</span><span class="sxs-lookup"><span data-stu-id="894b8-223">5.00</span></span></td>
    <td><span data-ttu-id="894b8-224">458.33</span><span class="sxs-lookup"><span data-stu-id="894b8-224">458.33</span></span></td>
    <td><span data-ttu-id="894b8-225">9.00</span><span class="sxs-lookup"><span data-stu-id="894b8-225">9.00</span></span></td>
    <td><span data-ttu-id="894b8-226">825.00</span><span class="sxs-lookup"><span data-stu-id="894b8-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="894b8-227">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-227">1000</span></span></td>
    <td><span data-ttu-id="894b8-228">2</span><span class="sxs-lookup"><span data-stu-id="894b8-228">2</span></span></td>
    <td><span data-ttu-id="894b8-229">10</span><span class="sxs-lookup"><span data-stu-id="894b8-229">10</span></span></td>
    <td><span data-ttu-id="894b8-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-230">2,000.00</span></span></td>
    <td><span data-ttu-id="894b8-231">10</span><span class="sxs-lookup"><span data-stu-id="894b8-231">10</span></span></td>
    <td><span data-ttu-id="894b8-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-232">2,000.00</span></span></td>
    <td><span data-ttu-id="894b8-233">200.00</span><span class="sxs-lookup"><span data-stu-id="894b8-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-234">10,00</span><span class="sxs-lookup"><span data-stu-id="894b8-234">10.00</span></span></td>
    <td><span data-ttu-id="894b8-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="894b8-236"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="894b8-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="894b8-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="894b8-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="894b8-243">Merk deg følgende detaljer i denne eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="894b8-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="894b8-244">Verdiene **Lagerverdiantall**, **Lagerverdi** og **Gjennomsnittlig enhetskostnad** som vises i rapporten, er verdier for den økonomiske lagerdimensjonen (**Område** i dette tilfellet).</span><span class="sxs-lookup"><span data-stu-id="894b8-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="894b8-245">Rapporten viser for eksempel følgende informasjon for område 1:</span><span class="sxs-lookup"><span data-stu-id="894b8-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="894b8-246">Verdien **Lagerverdiantall** er *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="894b8-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="894b8-247">Verdien **Lagerverdi** er *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="894b8-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="894b8-248">Verdien **Gjennomsnittlig enhetskostnad** er *91,67*.</span><span class="sxs-lookup"><span data-stu-id="894b8-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="894b8-249">Verdien **Beholdningsverdi** og **Beløp** i hver periode beregnes ved hjelp av verdien **Gjennomsnittlig enhetskostnad**.</span><span class="sxs-lookup"><span data-stu-id="894b8-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="894b8-250">Rapporten bestemmer lagerbeholdningen for hver periode ved å summere det totale mottatte beholdningsantallet for hver periode.</span><span class="sxs-lookup"><span data-stu-id="894b8-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="894b8-251">Deretter brukes prinsippet først-inn-først-ut (FIFO) til å trekke fra det totale utstedte antallet, uansett lagermodellen som varene bruker.</span><span class="sxs-lookup"><span data-stu-id="894b8-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="894b8-252">Hvis du kjører samme rapport på nytt, men denne gangen angir både verdiene **Område** og **Lager** til *Visning*, vil den nye rapporten ligne på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="894b8-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="894b8-253">Varenummer</span><span class="sxs-lookup"><span data-stu-id="894b8-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-254">Nettsted</span><span class="sxs-lookup"><span data-stu-id="894b8-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-255">Lager</span><span class="sxs-lookup"><span data-stu-id="894b8-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-256">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="894b8-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-257">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="894b8-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-258">Lagerverdiantall</span><span class="sxs-lookup"><span data-stu-id="894b8-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-259">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="894b8-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-260">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="894b8-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-261">5/8/2020–5/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-262">4/30/2020–4/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-263">3/31/2020–3/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="894b8-264">P1:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-265">P1:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="894b8-266">P2:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-267">P2:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="894b8-268">P3:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-269">P3:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="894b8-270">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-270">1000</span></span></td>
    <td><span data-ttu-id="894b8-271">1</span><span class="sxs-lookup"><span data-stu-id="894b8-271">1</span></span></td>
    <td><span data-ttu-id="894b8-272">11</span><span class="sxs-lookup"><span data-stu-id="894b8-272">11</span></span></td>
    <td><span data-ttu-id="894b8-273">10</span><span class="sxs-lookup"><span data-stu-id="894b8-273">10</span></span></td>
    <td><span data-ttu-id="894b8-274">916.67</span><span class="sxs-lookup"><span data-stu-id="894b8-274">916.67</span></span></td>
    <td><span data-ttu-id="894b8-275">14</span><span class="sxs-lookup"><span data-stu-id="894b8-275">14</span></span></td>
    <td><span data-ttu-id="894b8-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="894b8-276">1,283.33</span></span></td>
    <td><span data-ttu-id="894b8-277">91.67</span><span class="sxs-lookup"><span data-stu-id="894b8-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-278">5.00</span><span class="sxs-lookup"><span data-stu-id="894b8-278">5.00</span></span></td>
    <td><span data-ttu-id="894b8-279">458.33</span><span class="sxs-lookup"><span data-stu-id="894b8-279">458.33</span></span></td>
    <td><span data-ttu-id="894b8-280">5.00</span><span class="sxs-lookup"><span data-stu-id="894b8-280">5.00</span></span></td>
    <td><span data-ttu-id="894b8-281">458.33</span><span class="sxs-lookup"><span data-stu-id="894b8-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="894b8-282">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-282">1000</span></span></td>
    <td><span data-ttu-id="894b8-283">1</span><span class="sxs-lookup"><span data-stu-id="894b8-283">1</span></span></td>
    <td><span data-ttu-id="894b8-284">12</span><span class="sxs-lookup"><span data-stu-id="894b8-284">12</span></span></td>
    <td><span data-ttu-id="894b8-285">4</span><span class="sxs-lookup"><span data-stu-id="894b8-285">4</span></span></td>
    <td><span data-ttu-id="894b8-286">366.67</span><span class="sxs-lookup"><span data-stu-id="894b8-286">366.67</span></span></td>
    <td><span data-ttu-id="894b8-287">14</span><span class="sxs-lookup"><span data-stu-id="894b8-287">14</span></span></td>
    <td><span data-ttu-id="894b8-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="894b8-288">1,283.33</span></span></td>
    <td><span data-ttu-id="894b8-289">91.67</span><span class="sxs-lookup"><span data-stu-id="894b8-289">91.67</span></span></td>
    <td><span data-ttu-id="894b8-290">4.00</span><span class="sxs-lookup"><span data-stu-id="894b8-290">4.00</span></span></td>
    <td><span data-ttu-id="894b8-291">366.67</span><span class="sxs-lookup"><span data-stu-id="894b8-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="894b8-292">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-292">1000</span></span></td>
    <td><span data-ttu-id="894b8-293">2</span><span class="sxs-lookup"><span data-stu-id="894b8-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="894b8-294">10</span><span class="sxs-lookup"><span data-stu-id="894b8-294">10</span></span></td>
    <td><span data-ttu-id="894b8-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-295">2,000.00</span></span></td>
    <td><span data-ttu-id="894b8-296">10</span><span class="sxs-lookup"><span data-stu-id="894b8-296">10</span></span></td>
    <td><span data-ttu-id="894b8-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-297">2,000.00</span></span></td>
    <td><span data-ttu-id="894b8-298">200.00</span><span class="sxs-lookup"><span data-stu-id="894b8-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-299">10,00</span><span class="sxs-lookup"><span data-stu-id="894b8-299">10.00</span></span></td>
    <td><span data-ttu-id="894b8-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="894b8-301"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="894b8-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="894b8-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="894b8-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="894b8-310">Denne gangen er område 1 delt inn i to rader, én for lager 11 og én for lager 12.</span><span class="sxs-lookup"><span data-stu-id="894b8-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="894b8-311">Verdiene **Lagerverdiantall**, **Lagerverdi** og **Gjennomsnittlig enhetskostnad** er imidlertid de samme fordi **Lager** ikke er en økonomisk lagerdimensjon.</span><span class="sxs-lookup"><span data-stu-id="894b8-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="894b8-312">Legg også merke til at antallsdistribusjonen for område 1 er forskjellig.</span><span class="sxs-lookup"><span data-stu-id="894b8-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="894b8-313">I den første rapporten du kjørte, ignorerte systemet overføringsordren som ble funnet på det samme området, og trakk fra antallet av salgsfakturaen fra **3/31/2020–3/1/2020**-perioden i område 1.</span><span class="sxs-lookup"><span data-stu-id="894b8-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="894b8-314">I den nye rapporten trekker imidlertid systemet fra antallet for salgsfakturaen fra **5/8/2020–5/1/2020**-perioden i lager 12.</span><span class="sxs-lookup"><span data-stu-id="894b8-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="894b8-315">Virkninger av lagerlukking</span><span class="sxs-lookup"><span data-stu-id="894b8-315">Effects of inventory closing</span></span>

<span data-ttu-id="894b8-316">Hvis du kjører lagerlukking for mai og deretter kjører den forrige rapporten på nytt, men du angir feltet **Per dato** til *31. mai 2020*, vil du se følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="894b8-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="894b8-317">Verdiene **Beholdningsverdi** og **Gjennomsnittlig enhetskostnad** oppdateres.</span><span class="sxs-lookup"><span data-stu-id="894b8-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="894b8-318">Verdien **Beholdningsverdi** og verdiene **Beløp** i hver periode oppdateres i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="894b8-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="894b8-319">Den nye rapporten vil ligne på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="894b8-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="894b8-320">Varenummer</span><span class="sxs-lookup"><span data-stu-id="894b8-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-321">Nettsted</span><span class="sxs-lookup"><span data-stu-id="894b8-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-322">Lager</span><span class="sxs-lookup"><span data-stu-id="894b8-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-323">Antall på lager</span><span class="sxs-lookup"><span data-stu-id="894b8-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-324">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="894b8-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-325">Lagerverdiantall</span><span class="sxs-lookup"><span data-stu-id="894b8-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-326">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="894b8-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="894b8-327">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="894b8-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-328">5/31/2020–5/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-329">4/30/2020–4/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="894b8-330">3/31/2020–3/1/2020</span><span class="sxs-lookup"><span data-stu-id="894b8-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="894b8-331">P1:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-332">P1:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="894b8-333">P2:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-334">P2:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="894b8-335">P3:Antall</span><span class="sxs-lookup"><span data-stu-id="894b8-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="894b8-336">P3:Beløp</span><span class="sxs-lookup"><span data-stu-id="894b8-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="894b8-337">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-337">1000</span></span></td>
    <td><span data-ttu-id="894b8-338">1</span><span class="sxs-lookup"><span data-stu-id="894b8-338">1</span></span></td>
    <td><span data-ttu-id="894b8-339">11</span><span class="sxs-lookup"><span data-stu-id="894b8-339">11</span></span></td>
    <td><span data-ttu-id="894b8-340">10</span><span class="sxs-lookup"><span data-stu-id="894b8-340">10</span></span></td>
    <td><span data-ttu-id="894b8-341">910.70</span><span class="sxs-lookup"><span data-stu-id="894b8-341">910.70</span></span></td>
    <td><span data-ttu-id="894b8-342">14</span><span class="sxs-lookup"><span data-stu-id="894b8-342">14</span></span></td>
    <td><span data-ttu-id="894b8-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="894b8-343">1,275.00</span></span></td>
    <td><span data-ttu-id="894b8-344">91.07</span><span class="sxs-lookup"><span data-stu-id="894b8-344">91.07</span></span></td>
    <td><span data-ttu-id="894b8-345">0.00</span><span class="sxs-lookup"><span data-stu-id="894b8-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="894b8-346">5.00</span><span class="sxs-lookup"><span data-stu-id="894b8-346">5.00</span></span></td>
    <td><span data-ttu-id="894b8-347">455.36</span><span class="sxs-lookup"><span data-stu-id="894b8-347">455.36</span></span></td>
    <td><span data-ttu-id="894b8-348">5.00</span><span class="sxs-lookup"><span data-stu-id="894b8-348">5.00</span></span></td>
    <td><span data-ttu-id="894b8-349">455.36</span><span class="sxs-lookup"><span data-stu-id="894b8-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="894b8-350">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-350">1000</span></span></td>
    <td><span data-ttu-id="894b8-351">1</span><span class="sxs-lookup"><span data-stu-id="894b8-351">1</span></span></td>
    <td><span data-ttu-id="894b8-352">12</span><span class="sxs-lookup"><span data-stu-id="894b8-352">12</span></span></td>
    <td><span data-ttu-id="894b8-353">4</span><span class="sxs-lookup"><span data-stu-id="894b8-353">4</span></span></td>
    <td><span data-ttu-id="894b8-354">364.29</span><span class="sxs-lookup"><span data-stu-id="894b8-354">364.29</span></span></td>
    <td><span data-ttu-id="894b8-355">14</span><span class="sxs-lookup"><span data-stu-id="894b8-355">14</span></span></td>
    <td><span data-ttu-id="894b8-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="894b8-356">1,275.00</span></span></td>
    <td><span data-ttu-id="894b8-357">91.07</span><span class="sxs-lookup"><span data-stu-id="894b8-357">91.07</span></span></td>
    <td><span data-ttu-id="894b8-358">4.00</span><span class="sxs-lookup"><span data-stu-id="894b8-358">4.00</span></span></td>
    <td><span data-ttu-id="894b8-359">364.29</span><span class="sxs-lookup"><span data-stu-id="894b8-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="894b8-360">1000</span><span class="sxs-lookup"><span data-stu-id="894b8-360">1000</span></span></td>
    <td><span data-ttu-id="894b8-361">2</span><span class="sxs-lookup"><span data-stu-id="894b8-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="894b8-362">10</span><span class="sxs-lookup"><span data-stu-id="894b8-362">10</span></span></td>
    <td><span data-ttu-id="894b8-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-363">2,000.00</span></span></td>
    <td><span data-ttu-id="894b8-364">10</span><span class="sxs-lookup"><span data-stu-id="894b8-364">10</span></span></td>
    <td><span data-ttu-id="894b8-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-365">2,000.00</span></span></td>
    <td><span data-ttu-id="894b8-366">200.00</span><span class="sxs-lookup"><span data-stu-id="894b8-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-367">10,00</span><span class="sxs-lookup"><span data-stu-id="894b8-367">10.00</span></span></td>
    <td><span data-ttu-id="894b8-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="894b8-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="894b8-369"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="894b8-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="894b8-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="894b8-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="894b8-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="894b8-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="894b8-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
