---
title: Kostnadsobjekter
description: Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e590322c75cfb2ad21236af56656061037a4b7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983531"
---
# <a name="cost-objects"></a><span data-ttu-id="3a552-105">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="3a552-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a552-106">Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="3a552-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="3a552-107">Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for.</span><span class="sxs-lookup"><span data-stu-id="3a552-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="3a552-108">En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.</span><span class="sxs-lookup"><span data-stu-id="3a552-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="3a552-109">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="3a552-109">Cost objects</span></span>

<span data-ttu-id="3a552-110">**Kostnadsobjekter** -siden viser alle kostnadsobjekter som er registrert for et produkt.</span><span class="sxs-lookup"><span data-stu-id="3a552-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="3a552-111">Kostnadsobjektene er definert av data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="3a552-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="3a552-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="3a552-112">Product</span></span>
-   <span data-ttu-id="3a552-113">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a552-113">Product dimension group</span></span>
-   <span data-ttu-id="3a552-114">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a552-114">Storage dimension group</span></span>
-   <span data-ttu-id="3a552-115">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a552-115">Tracking dimension group</span></span>

<span data-ttu-id="3a552-116">**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer** .</span><span class="sxs-lookup"><span data-stu-id="3a552-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="3a552-117">Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="3a552-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="3a552-118">En vare har for eksempel følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="3a552-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="3a552-119">**Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="3a552-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="3a552-120">**Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="3a552-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="3a552-121">**Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="3a552-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="3a552-122">Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.</span><span class="sxs-lookup"><span data-stu-id="3a552-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="3a552-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="3a552-123">Object type</span></span>      | <span data-ttu-id="3a552-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="3a552-124">Item number</span></span> | <span data-ttu-id="3a552-125">Område</span><span class="sxs-lookup"><span data-stu-id="3a552-125">Site</span></span> | <span data-ttu-id="3a552-126">Lager</span><span class="sxs-lookup"><span data-stu-id="3a552-126">Warehouse</span></span> | <span data-ttu-id="3a552-127">Partinr.</span><span class="sxs-lookup"><span data-stu-id="3a552-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="3a552-128">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="3a552-128">Cost object</span></span>      | <span data-ttu-id="3a552-129">x</span><span class="sxs-lookup"><span data-stu-id="3a552-129">x</span></span>           | <span data-ttu-id="3a552-130">x</span><span class="sxs-lookup"><span data-stu-id="3a552-130">x</span></span>    |           |           |
| <span data-ttu-id="3a552-131">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="3a552-131">Inventory object</span></span> | <span data-ttu-id="3a552-132">x</span><span class="sxs-lookup"><span data-stu-id="3a552-132">x</span></span>           | <span data-ttu-id="3a552-133">x</span><span class="sxs-lookup"><span data-stu-id="3a552-133">x</span></span>    |  <span data-ttu-id="3a552-134">x</span><span class="sxs-lookup"><span data-stu-id="3a552-134">x</span></span>        | <span data-ttu-id="3a552-135">x</span><span class="sxs-lookup"><span data-stu-id="3a552-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="3a552-136">Akkumulering av kostnader og antall</span><span class="sxs-lookup"><span data-stu-id="3a552-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="3a552-137">Verdien i **Verdi** -feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3a552-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="3a552-138">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="3a552-138">Physical cost amount</span></span>
    -   <span data-ttu-id="3a552-139">Økonomisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="3a552-139">Financial cost amount</span></span>
    -   <span data-ttu-id="3a552-140">Justeringer</span><span class="sxs-lookup"><span data-stu-id="3a552-140">Adjustments</span></span>
-   <span data-ttu-id="3a552-141">Verdien i **Antall** -feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3a552-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="3a552-142">Mottatt</span><span class="sxs-lookup"><span data-stu-id="3a552-142">Received</span></span>
    -   <span data-ttu-id="3a552-143">Fratrukket</span><span class="sxs-lookup"><span data-stu-id="3a552-143">Deducted</span></span>
    -   <span data-ttu-id="3a552-144">Postert antall</span><span class="sxs-lookup"><span data-stu-id="3a552-144">Posted quantity</span></span>
-   <span data-ttu-id="3a552-145">Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="3a552-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="3a552-146">Verdien beregnes ved å dele **Verdi** -verdien på **Antall** -verdien.</span><span class="sxs-lookup"><span data-stu-id="3a552-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="3a552-147">**Obs!**   Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.</span><span class="sxs-lookup"><span data-stu-id="3a552-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="3a552-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3a552-148">Additional resources</span></span>
--------

[<span data-ttu-id="3a552-149">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a552-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="3a552-150">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a552-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="3a552-151">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a552-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="3a552-152">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="3a552-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="3a552-153">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="3a552-153">Cost entries</span></span>](cost-entries.md)



