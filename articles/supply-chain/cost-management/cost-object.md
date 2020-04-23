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
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50849a173e74ad88dd10c6a30ea66c91b936e165
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201784"
---
# <a name="cost-objects"></a><span data-ttu-id="8d380-105">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="8d380-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d380-106">Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="8d380-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="8d380-107">Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for.</span><span class="sxs-lookup"><span data-stu-id="8d380-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="8d380-108">En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.</span><span class="sxs-lookup"><span data-stu-id="8d380-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="8d380-109">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="8d380-109">Cost objects</span></span>

<span data-ttu-id="8d380-110">**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt.</span><span class="sxs-lookup"><span data-stu-id="8d380-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="8d380-111">Kostnadsobjektene er definert av data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="8d380-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="8d380-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="8d380-112">Product</span></span>
-   <span data-ttu-id="8d380-113">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d380-113">Product dimension group</span></span>
-   <span data-ttu-id="8d380-114">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d380-114">Storage dimension group</span></span>
-   <span data-ttu-id="8d380-115">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d380-115">Tracking dimension group</span></span>

<span data-ttu-id="8d380-116">**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**.</span><span class="sxs-lookup"><span data-stu-id="8d380-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="8d380-117">Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="8d380-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="8d380-118">En vare har for eksempel følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="8d380-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="8d380-119">**Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="8d380-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="8d380-120">**Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="8d380-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="8d380-121">**Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="8d380-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="8d380-122">Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.</span><span class="sxs-lookup"><span data-stu-id="8d380-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="8d380-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="8d380-123">Object type</span></span>      | <span data-ttu-id="8d380-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="8d380-124">Item number</span></span> | <span data-ttu-id="8d380-125">Område</span><span class="sxs-lookup"><span data-stu-id="8d380-125">Site</span></span> | <span data-ttu-id="8d380-126">Lager</span><span class="sxs-lookup"><span data-stu-id="8d380-126">Warehouse</span></span> | <span data-ttu-id="8d380-127">Partinr.</span><span class="sxs-lookup"><span data-stu-id="8d380-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="8d380-128">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8d380-128">Cost object</span></span>      | <span data-ttu-id="8d380-129">x</span><span class="sxs-lookup"><span data-stu-id="8d380-129">x</span></span>           | <span data-ttu-id="8d380-130">x</span><span class="sxs-lookup"><span data-stu-id="8d380-130">x</span></span>    |           |           |
| <span data-ttu-id="8d380-131">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="8d380-131">Inventory object</span></span> | <span data-ttu-id="8d380-132">x</span><span class="sxs-lookup"><span data-stu-id="8d380-132">x</span></span>           | <span data-ttu-id="8d380-133">x</span><span class="sxs-lookup"><span data-stu-id="8d380-133">x</span></span>    |  <span data-ttu-id="8d380-134">x</span><span class="sxs-lookup"><span data-stu-id="8d380-134">x</span></span>        | <span data-ttu-id="8d380-135">x</span><span class="sxs-lookup"><span data-stu-id="8d380-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="8d380-136">Akkumulering av kostnader og antall</span><span class="sxs-lookup"><span data-stu-id="8d380-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="8d380-137">Verdien i **Verdi**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="8d380-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="8d380-138">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="8d380-138">Physical cost amount</span></span>
    -   <span data-ttu-id="8d380-139">Økonomisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="8d380-139">Financial cost amount</span></span>
    -   <span data-ttu-id="8d380-140">Justeringer</span><span class="sxs-lookup"><span data-stu-id="8d380-140">Adjustments</span></span>
-   <span data-ttu-id="8d380-141">Verdien i **Antall**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="8d380-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="8d380-142">Mottatt</span><span class="sxs-lookup"><span data-stu-id="8d380-142">Received</span></span>
    -   <span data-ttu-id="8d380-143">Fratrukket</span><span class="sxs-lookup"><span data-stu-id="8d380-143">Deducted</span></span>
    -   <span data-ttu-id="8d380-144">Postert antall</span><span class="sxs-lookup"><span data-stu-id="8d380-144">Posted quantity</span></span>
-   <span data-ttu-id="8d380-145">Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="8d380-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="8d380-146">Verdien beregnes ved å dele **Verdi**-verdien på **Antall**-verdien.</span><span class="sxs-lookup"><span data-stu-id="8d380-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="8d380-147">**Obs!**   Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.</span><span class="sxs-lookup"><span data-stu-id="8d380-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8d380-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d380-148">Additional resources</span></span>
--------

[<span data-ttu-id="8d380-149">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d380-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="8d380-150">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d380-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="8d380-151">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d380-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="8d380-152">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="8d380-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="8d380-153">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="8d380-153">Cost entries</span></span>](cost-entries.md)



