---
title: Beholdningsobjektverdier
description: Denne artikkelen inneholder informasjon om hvordan verdiene for et beholdningsobjekt beregnes.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52f39c18888b94b533743f546554d5cd1b2d56df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832256"
---
# <a name="inventory-object-values"></a><span data-ttu-id="4909a-103">Beholdningsobjektverdier</span><span class="sxs-lookup"><span data-stu-id="4909a-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4909a-104">Denne artikkelen inneholder informasjon om hvordan verdiene for et beholdningsobjekt beregnes.</span><span class="sxs-lookup"><span data-stu-id="4909a-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="4909a-105">En ny funksjon kalt **fysisk antall** gjør at du kan se verdiene til et bestemt beholdningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4909a-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="4909a-106">Et kostnadsobjekt representerer enhetsnivået der lagerregnskapet gjøres.</span><span class="sxs-lookup"><span data-stu-id="4909a-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="4909a-107">Hvis du vil ha mer informasjon om kostnadsobjekter, kan du se [Kostnadsobjekter](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="4909a-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="4909a-108">Hvis du vil se verdiene for et bestemt beholdningsobjekt, klikker du **Fysisk antall** på **Kostobjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="4909a-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="4909a-109">Slik beregnes verdien til et beholdningsobjekt:</span><span class="sxs-lookup"><span data-stu-id="4909a-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="4909a-110">Beholdningsobjekt.Verdi = Kostnadsobjekt.Gjennomsnittlig enhetskostnad × Beholdningsobjektet.Antall</span><span class="sxs-lookup"><span data-stu-id="4909a-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="4909a-111">Eksemplet nedenfor viser hvordan en verdiene til et beholdningsobjekt og et kostnadsobjekt beregnes.</span><span class="sxs-lookup"><span data-stu-id="4909a-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="4909a-112">To produktkvitteringshendelser er registrert for vare A:</span><span class="sxs-lookup"><span data-stu-id="4909a-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="4909a-113">Produktkvittering 1: Antall = 100 stk., Beløp = USD 1 000,00, Område = 1, Lager = 11, Partinr.</span><span class="sxs-lookup"><span data-stu-id="4909a-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="4909a-114">= B1</span><span class="sxs-lookup"><span data-stu-id="4909a-114">= B1</span></span>
-   <span data-ttu-id="4909a-115">Produktkvittering 2: Antall = 50 stk., Beløp = USD 800,00, Område = 1, Lager = 11, Partinr.</span><span class="sxs-lookup"><span data-stu-id="4909a-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="4909a-116">= B2</span><span class="sxs-lookup"><span data-stu-id="4909a-116">= B2</span></span>

<span data-ttu-id="4909a-117">Følgende tabell viser resultatet av beregningen for et kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4909a-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="4909a-118">Du kan vise resultatet på **Kostnadsobjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="4909a-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4909a-119">Objekttype</span><span class="sxs-lookup"><span data-stu-id="4909a-119">Object type</span></span></th>
<th><span data-ttu-id="4909a-120">Varenummer</span><span class="sxs-lookup"><span data-stu-id="4909a-120">Item number</span></span></th>
<th><span data-ttu-id="4909a-121">Område</span><span class="sxs-lookup"><span data-stu-id="4909a-121">Site</span></span></th>
<th><span data-ttu-id="4909a-122">Antall</span><span class="sxs-lookup"><span data-stu-id="4909a-122">Quantity</span></span></th>
<th><span data-ttu-id="4909a-123">Lagerenhet</span><span class="sxs-lookup"><span data-stu-id="4909a-123">Inventory unit</span></span></th>
<th><span data-ttu-id="4909a-124">Verdi</span><span class="sxs-lookup"><span data-stu-id="4909a-124">Value</span></span></th>
<th><span data-ttu-id="4909a-125">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="4909a-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4909a-126">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4909a-126">Cost object</span></span></td>
<td><span data-ttu-id="4909a-127">A</span><span class="sxs-lookup"><span data-stu-id="4909a-127">A</span></span></td>
<td><span data-ttu-id="4909a-128">1</span><span class="sxs-lookup"><span data-stu-id="4909a-128">1</span></span></td>
<td><span data-ttu-id="4909a-129">150</span><span class="sxs-lookup"><span data-stu-id="4909a-129">150</span></span></td>
<td><span data-ttu-id="4909a-130">Stk.</span><span class="sxs-lookup"><span data-stu-id="4909a-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="4909a-131">USD 1 800,00</span><span class="sxs-lookup"><span data-stu-id="4909a-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="4909a-132">USD 12,00</span><span class="sxs-lookup"><span data-stu-id="4909a-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4909a-133">Følgende tabell viser resultatet av beregningen for et beholdningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4909a-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="4909a-134">Du kan vise resultatet ved å klikke **Fysisk antall** på **Kostnadsobjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="4909a-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4909a-135">Objekttype</span><span class="sxs-lookup"><span data-stu-id="4909a-135">Object type</span></span></th>
<th><span data-ttu-id="4909a-136">Varenummer</span><span class="sxs-lookup"><span data-stu-id="4909a-136">Item number</span></span></th>
<th><span data-ttu-id="4909a-137">Område</span><span class="sxs-lookup"><span data-stu-id="4909a-137">Site</span></span></th>
<th><span data-ttu-id="4909a-138">Lager</span><span class="sxs-lookup"><span data-stu-id="4909a-138">Warehouse</span></span></th>
<th><span data-ttu-id="4909a-139">Partinr.</span><span class="sxs-lookup"><span data-stu-id="4909a-139">Batch No.</span></span></th>
<th><span data-ttu-id="4909a-140">Antall</span><span class="sxs-lookup"><span data-stu-id="4909a-140">Quantity</span></span></th>
<th><span data-ttu-id="4909a-141">Lagerenhet</span><span class="sxs-lookup"><span data-stu-id="4909a-141">Inventory unit</span></span></th>
<th><span data-ttu-id="4909a-142">Verdi</span><span class="sxs-lookup"><span data-stu-id="4909a-142">Value</span></span></th>
<th><span data-ttu-id="4909a-143">Gjennomsnittlig enhetskostnad</span><span class="sxs-lookup"><span data-stu-id="4909a-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4909a-144">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="4909a-144">Inventory object</span></span></td>
<td><span data-ttu-id="4909a-145">A</span><span class="sxs-lookup"><span data-stu-id="4909a-145">A</span></span></td>
<td><span data-ttu-id="4909a-146">1</span><span class="sxs-lookup"><span data-stu-id="4909a-146">1</span></span></td>
<td><span data-ttu-id="4909a-147">11</span><span class="sxs-lookup"><span data-stu-id="4909a-147">11</span></span></td>
<td><span data-ttu-id="4909a-148">B1</span><span class="sxs-lookup"><span data-stu-id="4909a-148">B1</span></span></td>
<td><span data-ttu-id="4909a-149">100</span><span class="sxs-lookup"><span data-stu-id="4909a-149">100</span></span></td>
<td><span data-ttu-id="4909a-150">Stk.</span><span class="sxs-lookup"><span data-stu-id="4909a-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="4909a-151">USD 1 200,00</span><span class="sxs-lookup"><span data-stu-id="4909a-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="4909a-152">USD 12,00</span><span class="sxs-lookup"><span data-stu-id="4909a-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4909a-153">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="4909a-153">Inventory object</span></span></td>
<td><span data-ttu-id="4909a-154">A</span><span class="sxs-lookup"><span data-stu-id="4909a-154">A</span></span></td>
<td><span data-ttu-id="4909a-155">1</span><span class="sxs-lookup"><span data-stu-id="4909a-155">1</span></span></td>
<td><span data-ttu-id="4909a-156">11</span><span class="sxs-lookup"><span data-stu-id="4909a-156">11</span></span></td>
<td><span data-ttu-id="4909a-157">B2</span><span class="sxs-lookup"><span data-stu-id="4909a-157">B2</span></span></td>
<td><span data-ttu-id="4909a-158">50</span><span class="sxs-lookup"><span data-stu-id="4909a-158">50</span></span></td>
<td><span data-ttu-id="4909a-159">Stk.</span><span class="sxs-lookup"><span data-stu-id="4909a-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="4909a-160">USD 600,00</span><span class="sxs-lookup"><span data-stu-id="4909a-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="4909a-161">USD 12,00</span><span class="sxs-lookup"><span data-stu-id="4909a-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="4909a-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4909a-162">Additional resources</span></span>
--------

[<span data-ttu-id="4909a-163">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="4909a-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="4909a-164">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="4909a-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="4909a-165">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="4909a-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]