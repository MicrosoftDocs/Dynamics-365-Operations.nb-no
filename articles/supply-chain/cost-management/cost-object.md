---
title: Kostnadsobjekter
description: "Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 13efb284c24c20cf4115ce2dd50be31dd3e5543e
ms.contentlocale: nb-no
ms.lasthandoff: 10/13/2017

---

# <a name="cost-objects"></a><span data-ttu-id="1e5e7-105">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="1e5e7-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1e5e7-106">Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="1e5e7-107">Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="1e5e7-108">En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="1e5e7-109">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="1e5e7-109">Cost objects</span></span>

<span data-ttu-id="1e5e7-110">**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="1e5e7-111">Kostnadsobjektene er definert av data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="1e5e7-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="1e5e7-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="1e5e7-112">Product</span></span>
-   <span data-ttu-id="1e5e7-113">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="1e5e7-113">Product dimension group</span></span>
-   <span data-ttu-id="1e5e7-114">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="1e5e7-114">Storage dimension group</span></span>
-   <span data-ttu-id="1e5e7-115">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="1e5e7-115">Tracking dimension group</span></span>

<span data-ttu-id="1e5e7-116">**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="1e5e7-117">Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="1e5e7-118">En vare har for eksempel følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="1e5e7-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="1e5e7-119">**Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="1e5e7-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="1e5e7-120">**Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="1e5e7-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="1e5e7-121">**Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="1e5e7-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="1e5e7-122">Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="1e5e7-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="1e5e7-123">Object type</span></span>      | <span data-ttu-id="1e5e7-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="1e5e7-124">Item number</span></span> | <span data-ttu-id="1e5e7-125">Område</span><span class="sxs-lookup"><span data-stu-id="1e5e7-125">Site</span></span> | <span data-ttu-id="1e5e7-126">Lager</span><span class="sxs-lookup"><span data-stu-id="1e5e7-126">Warehouse</span></span> | <span data-ttu-id="1e5e7-127">Partinr.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="1e5e7-128">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="1e5e7-128">Cost object</span></span>      | <span data-ttu-id="1e5e7-129">x</span><span class="sxs-lookup"><span data-stu-id="1e5e7-129">x</span></span>           | <span data-ttu-id="1e5e7-130">x</span><span class="sxs-lookup"><span data-stu-id="1e5e7-130">x</span></span>    |           |           |
| <span data-ttu-id="1e5e7-131">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="1e5e7-131">Inventory object</span></span> | <span data-ttu-id="1e5e7-132">x</span><span class="sxs-lookup"><span data-stu-id="1e5e7-132">x</span></span>           | <span data-ttu-id="1e5e7-133">x</span><span class="sxs-lookup"><span data-stu-id="1e5e7-133">x</span></span>    |  <span data-ttu-id="1e5e7-134">x</span><span class="sxs-lookup"><span data-stu-id="1e5e7-134">x</span></span>        | <span data-ttu-id="1e5e7-135">x</span><span class="sxs-lookup"><span data-stu-id="1e5e7-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="1e5e7-136">Akkumulering av kostnader og antall</span><span class="sxs-lookup"><span data-stu-id="1e5e7-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="1e5e7-137">Verdien i **Verdi**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="1e5e7-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="1e5e7-138">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="1e5e7-138">Physical cost amount</span></span>
    -   <span data-ttu-id="1e5e7-139">Økonomisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="1e5e7-139">Financial cost amount</span></span>
    -   <span data-ttu-id="1e5e7-140">Justeringer</span><span class="sxs-lookup"><span data-stu-id="1e5e7-140">Adjustments</span></span>
-   <span data-ttu-id="1e5e7-141">Verdien i **Antall**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="1e5e7-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="1e5e7-142">Mottatt</span><span class="sxs-lookup"><span data-stu-id="1e5e7-142">Received</span></span>
    -   <span data-ttu-id="1e5e7-143">Fratrukket</span><span class="sxs-lookup"><span data-stu-id="1e5e7-143">Deducted</span></span>
    -   <span data-ttu-id="1e5e7-144">Postert antall</span><span class="sxs-lookup"><span data-stu-id="1e5e7-144">Posted quantity</span></span>
-   <span data-ttu-id="1e5e7-145">Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="1e5e7-146">Verdien beregnes ved å dele **Verdi**-verdien på **Antall**-verdien.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="1e5e7-147">**Obs!**  Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.</span><span class="sxs-lookup"><span data-stu-id="1e5e7-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="1e5e7-148">Se også</span><span class="sxs-lookup"><span data-stu-id="1e5e7-148">See also</span></span>
--------

[<span data-ttu-id="1e5e7-149">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="1e5e7-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="1e5e7-150">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="1e5e7-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="1e5e7-151">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="1e5e7-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="1e5e7-152">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="1e5e7-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="1e5e7-153">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="1e5e7-153">Cost entries</span></span>](cost-entries.md)




