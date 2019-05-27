---
title: Kostnadsobjekter
description: Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres. Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for. En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275855f2fb4d32df91449d7ebb9ad9ba2bd3f36b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558555"
---
# <a name="cost-objects"></a><span data-ttu-id="0886f-105">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="0886f-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0886f-106">Denne artikkelen inneholder informasjon om kostnadsobjekter, og forklarer hvordan kostnader og antall akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="0886f-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="0886f-107">Et kostnadsobjekt er en enhet som kostnader og antall akkumuleres for.</span><span class="sxs-lookup"><span data-stu-id="0886f-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="0886f-108">En kostnadsobjektenhet kan være et produkt eller produktvarianter, for eksempel varianter for stil og farge.</span><span class="sxs-lookup"><span data-stu-id="0886f-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="0886f-109">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="0886f-109">Cost objects</span></span>

<span data-ttu-id="0886f-110">**Kostnadsobjekter**-siden viser alle kostnadsobjekter som er registrert for et produkt.</span><span class="sxs-lookup"><span data-stu-id="0886f-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="0886f-111">Kostnadsobjektene er definert av data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="0886f-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="0886f-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="0886f-112">Product</span></span>
-   <span data-ttu-id="0886f-113">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="0886f-113">Product dimension group</span></span>
-   <span data-ttu-id="0886f-114">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="0886f-114">Storage dimension group</span></span>
-   <span data-ttu-id="0886f-115">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="0886f-115">Tracking dimension group</span></span>

<span data-ttu-id="0886f-116">**Obs!** Et kostnadsobjekt representerer bare et kostnadselement av typen **Direkte materialer**.</span><span class="sxs-lookup"><span data-stu-id="0886f-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="0886f-117">Et kostnadsobjekt og et beholdningsobjekt er ulike ved at et kostnadsobjekt defineres av lagerdimensjonene som er valgt for økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="0886f-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="0886f-118">En vare har for eksempel følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="0886f-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="0886f-119">**Område:** Aktuell beholdning = Ja, Økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="0886f-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="0886f-120">**Lager:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="0886f-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="0886f-121">**Partinr.:** Aktuell beholdning = Ja, Økonomisk lager = Nei</span><span class="sxs-lookup"><span data-stu-id="0886f-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="0886f-122">Tabellen nedenfor viser hva et kostnadsobjekt er, og hva et beholdningsobjekt er.</span><span class="sxs-lookup"><span data-stu-id="0886f-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="0886f-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="0886f-123">Object type</span></span>      | <span data-ttu-id="0886f-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="0886f-124">Item number</span></span> | <span data-ttu-id="0886f-125">Område</span><span class="sxs-lookup"><span data-stu-id="0886f-125">Site</span></span> | <span data-ttu-id="0886f-126">Lager</span><span class="sxs-lookup"><span data-stu-id="0886f-126">Warehouse</span></span> | <span data-ttu-id="0886f-127">Partinr.</span><span class="sxs-lookup"><span data-stu-id="0886f-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="0886f-128">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="0886f-128">Cost object</span></span>      | <span data-ttu-id="0886f-129">x</span><span class="sxs-lookup"><span data-stu-id="0886f-129">x</span></span>           | <span data-ttu-id="0886f-130">x</span><span class="sxs-lookup"><span data-stu-id="0886f-130">x</span></span>    |           |           |
| <span data-ttu-id="0886f-131">Beholdningsobjekt</span><span class="sxs-lookup"><span data-stu-id="0886f-131">Inventory object</span></span> | <span data-ttu-id="0886f-132">x</span><span class="sxs-lookup"><span data-stu-id="0886f-132">x</span></span>           | <span data-ttu-id="0886f-133">x</span><span class="sxs-lookup"><span data-stu-id="0886f-133">x</span></span>    |  <span data-ttu-id="0886f-134">x</span><span class="sxs-lookup"><span data-stu-id="0886f-134">x</span></span>        | <span data-ttu-id="0886f-135">x</span><span class="sxs-lookup"><span data-stu-id="0886f-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="0886f-136">Akkumulering av kostnader og antall</span><span class="sxs-lookup"><span data-stu-id="0886f-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="0886f-137">Verdien i **Verdi**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="0886f-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="0886f-138">Fysisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="0886f-138">Physical cost amount</span></span>
    -   <span data-ttu-id="0886f-139">Økonomisk kostbeløp</span><span class="sxs-lookup"><span data-stu-id="0886f-139">Financial cost amount</span></span>
    -   <span data-ttu-id="0886f-140">Justeringer</span><span class="sxs-lookup"><span data-stu-id="0886f-140">Adjustments</span></span>
-   <span data-ttu-id="0886f-141">Verdien i **Antall**-feltet er en sum av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="0886f-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="0886f-142">Mottatt</span><span class="sxs-lookup"><span data-stu-id="0886f-142">Received</span></span>
    -   <span data-ttu-id="0886f-143">Fratrukket</span><span class="sxs-lookup"><span data-stu-id="0886f-143">Deducted</span></span>
    -   <span data-ttu-id="0886f-144">Postert antall</span><span class="sxs-lookup"><span data-stu-id="0886f-144">Posted quantity</span></span>
-   <span data-ttu-id="0886f-145">Feltet **Gjennomsnittlig enhetskostnad** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="0886f-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="0886f-146">Verdien beregnes ved å dele **Verdi**-verdien på **Antall**-verdien.</span><span class="sxs-lookup"><span data-stu-id="0886f-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="0886f-147">**Obs!**   Parameteren **Ta med fysisk verdi** har ingen innvirkning på de foregående beregningene.</span><span class="sxs-lookup"><span data-stu-id="0886f-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0886f-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0886f-148">Additional resources</span></span>
--------

[<span data-ttu-id="0886f-149">Produktdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="0886f-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="0886f-150">Lagringsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="0886f-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="0886f-151">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="0886f-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="0886f-152">Hva er nytt eller endret?</span><span class="sxs-lookup"><span data-stu-id="0886f-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="0886f-153">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="0886f-153">Cost entries</span></span>](cost-entries.md)



