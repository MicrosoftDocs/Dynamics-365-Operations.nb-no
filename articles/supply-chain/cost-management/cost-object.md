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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee7c170d5a330c0080931a67c1548eb0d3522bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232404"
---
# <a name="cost-objects"></a><span data-ttu-id="75361-105">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="75361-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75361-106">Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="75361-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="75361-107">Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for.</span><span class="sxs-lookup"><span data-stu-id="75361-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="75361-108">En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.</span><span class="sxs-lookup"><span data-stu-id="75361-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="75361-109">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="75361-109">Cost objects</span></span>

<span data-ttu-id="75361-110">**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt.</span><span class="sxs-lookup"><span data-stu-id="75361-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="75361-111">Kostnadsobjektene er definert av data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="75361-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="75361-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="75361-112">Product</span></span>
-   <span data-ttu-id="75361-113">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="75361-113">Product dimension group</span></span>
-   <span data-ttu-id="75361-114">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="75361-114">Storage dimension group</span></span>
-   <span data-ttu-id="75361-115">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="75361-115">Tracking dimension group</span></span>

<span data-ttu-id="75361-116">**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**.</span><span class="sxs-lookup"><span data-stu-id="75361-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="75361-117">Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="75361-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="75361-118">En vare har for eksempel følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="75361-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="75361-119">**Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="75361-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="75361-120">**Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="75361-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="75361-121">**Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="75361-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="75361-122">Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.</span><span class="sxs-lookup"><span data-stu-id="75361-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="75361-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="75361-123">Object type</span></span>      | <span data-ttu-id="75361-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="75361-124">Item number</span></span> | <span data-ttu-id="75361-125">Område</span><span class="sxs-lookup"><span data-stu-id="75361-125">Site</span></span> | <span data-ttu-id="75361-126">Lager</span><span class="sxs-lookup"><span data-stu-id="75361-126">Warehouse</span></span> | <span data-ttu-id="75361-127">Partinr.</span><span class="sxs-lookup"><span data-stu-id="75361-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="75361-128">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="75361-128">Cost object</span></span>      | <span data-ttu-id="75361-129">x</span><span class="sxs-lookup"><span data-stu-id="75361-129">x</span></span>           | <span data-ttu-id="75361-130">x</span><span class="sxs-lookup"><span data-stu-id="75361-130">x</span></span>    |           |           |
| <span data-ttu-id="75361-131">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="75361-131">Inventory object</span></span> | <span data-ttu-id="75361-132">x</span><span class="sxs-lookup"><span data-stu-id="75361-132">x</span></span>           | <span data-ttu-id="75361-133">x</span><span class="sxs-lookup"><span data-stu-id="75361-133">x</span></span>    |  <span data-ttu-id="75361-134">x</span><span class="sxs-lookup"><span data-stu-id="75361-134">x</span></span>        | <span data-ttu-id="75361-135">x</span><span class="sxs-lookup"><span data-stu-id="75361-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="75361-136">Akkumulering av kostnader og antall</span><span class="sxs-lookup"><span data-stu-id="75361-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="75361-137">Verdien i **Verdi**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="75361-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="75361-138">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="75361-138">Physical cost amount</span></span>
    -   <span data-ttu-id="75361-139">Økonomisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="75361-139">Financial cost amount</span></span>
    -   <span data-ttu-id="75361-140">Justeringer</span><span class="sxs-lookup"><span data-stu-id="75361-140">Adjustments</span></span>
-   <span data-ttu-id="75361-141">Verdien i **Antall**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="75361-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="75361-142">Mottatt</span><span class="sxs-lookup"><span data-stu-id="75361-142">Received</span></span>
    -   <span data-ttu-id="75361-143">Fratrukket</span><span class="sxs-lookup"><span data-stu-id="75361-143">Deducted</span></span>
    -   <span data-ttu-id="75361-144">Postert antall</span><span class="sxs-lookup"><span data-stu-id="75361-144">Posted quantity</span></span>
-   <span data-ttu-id="75361-145">Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="75361-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="75361-146">Verdien beregnes ved å dele **Verdi**-verdien på **Antall**-verdien.</span><span class="sxs-lookup"><span data-stu-id="75361-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="75361-147">**Obs!**   Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.</span><span class="sxs-lookup"><span data-stu-id="75361-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="75361-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="75361-148">Additional resources</span></span>
--------

[<span data-ttu-id="75361-149">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="75361-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="75361-150">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="75361-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="75361-151">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="75361-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="75361-152">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="75361-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="75361-153">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="75361-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]