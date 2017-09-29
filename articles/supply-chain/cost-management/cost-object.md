---
title: Kostnadsobjekter
description: "Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge."
author: YuyuScheller
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d43ea6c0d80a1602f298bbbedb88dd8f7decca4e
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="cost-objects"></a><span data-ttu-id="82224-105">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="82224-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="82224-106">Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="82224-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="82224-107">Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for.</span><span class="sxs-lookup"><span data-stu-id="82224-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="82224-108">En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.</span><span class="sxs-lookup"><span data-stu-id="82224-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

<a name="cost-objects"></a><span data-ttu-id="82224-109">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="82224-109">Cost objects</span></span>
------------

<span data-ttu-id="82224-110">**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt.</span><span class="sxs-lookup"><span data-stu-id="82224-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="82224-111">Kostnadsobjektene er definert av data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="82224-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="82224-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="82224-112">Product</span></span>
-   <span data-ttu-id="82224-113">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="82224-113">Product dimension group</span></span>
-   <span data-ttu-id="82224-114">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="82224-114">Storage dimension group</span></span>
-   <span data-ttu-id="82224-115">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="82224-115">Tracking dimension group</span></span>

<span data-ttu-id="82224-116">**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**.</span><span class="sxs-lookup"><span data-stu-id="82224-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="82224-117">Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="82224-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="82224-118">En vare har for eksempel følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="82224-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="82224-119">**Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="82224-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="82224-120">**Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="82224-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="82224-121">**Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="82224-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="82224-122">Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.</span><span class="sxs-lookup"><span data-stu-id="82224-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="82224-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="82224-123">Object type</span></span>      | <span data-ttu-id="82224-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="82224-124">Item number</span></span> | <span data-ttu-id="82224-125">Område</span><span class="sxs-lookup"><span data-stu-id="82224-125">Site</span></span> | <span data-ttu-id="82224-126">Lager</span><span class="sxs-lookup"><span data-stu-id="82224-126">Warehouse</span></span> | <span data-ttu-id="82224-127">Partinr.</span><span class="sxs-lookup"><span data-stu-id="82224-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="82224-128">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="82224-128">Cost object</span></span>      | <span data-ttu-id="82224-129">x</span><span class="sxs-lookup"><span data-stu-id="82224-129">x</span></span>           | <span data-ttu-id="82224-130">x</span><span class="sxs-lookup"><span data-stu-id="82224-130">x</span></span>    |           |           |
| <span data-ttu-id="82224-131">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="82224-131">Inventory object</span></span> | <span data-ttu-id="82224-132">x</span><span class="sxs-lookup"><span data-stu-id="82224-132">x</span></span>           | <span data-ttu-id="82224-133">x</span><span class="sxs-lookup"><span data-stu-id="82224-133">x</span></span>    |  <span data-ttu-id="82224-134">x</span><span class="sxs-lookup"><span data-stu-id="82224-134">x</span></span>        | <span data-ttu-id="82224-135">x</span><span class="sxs-lookup"><span data-stu-id="82224-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="82224-136">Akkumulering av kostnader og antall</span><span class="sxs-lookup"><span data-stu-id="82224-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="82224-137">Verdien i **Verdi**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="82224-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="82224-138">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="82224-138">Physical cost amount</span></span>
    -   <span data-ttu-id="82224-139">Økonomisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="82224-139">Financial cost amount</span></span>
    -   <span data-ttu-id="82224-140">Justeringer</span><span class="sxs-lookup"><span data-stu-id="82224-140">Adjustments</span></span>
-   <span data-ttu-id="82224-141">Verdien i **Antall**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="82224-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="82224-142">Mottatt</span><span class="sxs-lookup"><span data-stu-id="82224-142">Received</span></span>
    -   <span data-ttu-id="82224-143">Fratrukket</span><span class="sxs-lookup"><span data-stu-id="82224-143">Deducted</span></span>
    -   <span data-ttu-id="82224-144">Postert antall</span><span class="sxs-lookup"><span data-stu-id="82224-144">Posted quantity</span></span>
-   <span data-ttu-id="82224-145">Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="82224-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="82224-146">Verdien beregnes ved å dele **Verdi**-verdien på **Antall**-verdien.</span><span class="sxs-lookup"><span data-stu-id="82224-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="82224-147">**Obs!**  Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.</span><span class="sxs-lookup"><span data-stu-id="82224-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="82224-148">Se også</span><span class="sxs-lookup"><span data-stu-id="82224-148">See also</span></span>
--------

[<span data-ttu-id="82224-149">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="82224-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="82224-150">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="82224-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="82224-151">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="82224-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="82224-152">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="82224-152">What's new or changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[<span data-ttu-id="82224-153">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="82224-153">Cost entries</span></span>](cost-entries.md)




