---
title: Manuell avskrivning
description: Denne artikkelen gir en oversikt over den manuelle avskrivningsmetoden.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e43b9397dd4e362eff9d78f302732e6bcc53d1db
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="36afd-103">Manuell avskrivning</span><span class="sxs-lookup"><span data-stu-id="36afd-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="36afd-104">Denne artikkelen gir en oversikt over den manuelle avskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="36afd-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="36afd-105">Når du definerer en avskrivningsprofil for anleggsmiddel og velger **Manuelt** i feltet **Metode** på siden **Avskrivningsprofiler**, bestemmes avskrivningen for anleggsmidler som er tilordnet avskrivningsprofilen, av prosenten du angir for hvert intervall i kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="36afd-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="36afd-106">Intervallene du angir prosenter for, posteres i henhold til verdien du velger i **Periodefrekvens** i **Generelt**-hurtigkategorien av på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="36afd-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="36afd-107">Her er verdiene du kan velge:</span><span class="sxs-lookup"><span data-stu-id="36afd-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="36afd-108">Årlig</span><span class="sxs-lookup"><span data-stu-id="36afd-108">Yearly</span></span>
-   <span data-ttu-id="36afd-109">Månedlig</span><span class="sxs-lookup"><span data-stu-id="36afd-109">Monthly</span></span>
-   <span data-ttu-id="36afd-110">Kvartalsvis</span><span class="sxs-lookup"><span data-stu-id="36afd-110">Quarterly</span></span>
-   <span data-ttu-id="36afd-111">Halvårlig</span><span class="sxs-lookup"><span data-stu-id="36afd-111">Half-Yearly</span></span>
-   <span data-ttu-id="36afd-112">Daglig</span><span class="sxs-lookup"><span data-stu-id="36afd-112">Daily</span></span>

<span data-ttu-id="36afd-113">Når du velger posteringsfrekvens, klikker du **Manuelle planer** og angir prosenter for hvert posteringsintervall.</span><span class="sxs-lookup"><span data-stu-id="36afd-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="36afd-114">De manuelle planene og posteringsintervallene definerer sammen avskrivningsbeløpet, som vist i eksemplene senere i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="36afd-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="36afd-115">Manuell avskrivning beregnes alltid som en prosent av anskaffelsesprisen.</span><span class="sxs-lookup"><span data-stu-id="36afd-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="36afd-116">For manuell avskrivning inneholder ikke prosentene du angir i intervallene, totalt 100 prosent.</span><span class="sxs-lookup"><span data-stu-id="36afd-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="36afd-117">Manuell avskrivning er en fleksibel avskrivningsmetode som ofte brukes til å definere en ekstraordinær avskrivningsprofil på siden **Tablåer**, for eksempel en avskrivning som ikke er periodisk, for bestemte formål (for eksempel avgift).</span><span class="sxs-lookup"><span data-stu-id="36afd-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="36afd-118">Eksempler</span><span class="sxs-lookup"><span data-stu-id="36afd-118">Examples</span></span>
<span data-ttu-id="36afd-119">Anskaffelsespris: 11 000,00 Forventet skrapverdi: 1000,00 Følgende tabell viser intervallene og prosentene du definerer på siden **Planer for anleggsmidlets avskrivningsprofil**.</span><span class="sxs-lookup"><span data-stu-id="36afd-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="36afd-120">Intervallnummer</span><span class="sxs-lookup"><span data-stu-id="36afd-120">Interval number</span></span> | <span data-ttu-id="36afd-121">Prosent</span><span class="sxs-lookup"><span data-stu-id="36afd-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="36afd-122">1</span><span class="sxs-lookup"><span data-stu-id="36afd-122">1</span></span>               | <span data-ttu-id="36afd-123">10,00</span><span class="sxs-lookup"><span data-stu-id="36afd-123">10.00</span></span>      |
| <span data-ttu-id="36afd-124">2</span><span class="sxs-lookup"><span data-stu-id="36afd-124">2</span></span>               | <span data-ttu-id="36afd-125">50,00</span><span class="sxs-lookup"><span data-stu-id="36afd-125">50.00</span></span>      |
| <span data-ttu-id="36afd-126">3</span><span class="sxs-lookup"><span data-stu-id="36afd-126">3</span></span>               | <span data-ttu-id="36afd-127">8,00</span><span class="sxs-lookup"><span data-stu-id="36afd-127">8.00</span></span>       |

<span data-ttu-id="36afd-128">Følgende tabell viser hvordan avskrivning for hvert intervall beregnes.</span><span class="sxs-lookup"><span data-stu-id="36afd-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="36afd-129">Intervallnummer</span><span class="sxs-lookup"><span data-stu-id="36afd-129">Interval number</span></span> | <span data-ttu-id="36afd-130">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="36afd-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="36afd-131">Netto bokført verdi på slutten av intervallet</span><span class="sxs-lookup"><span data-stu-id="36afd-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="36afd-132">1</span><span class="sxs-lookup"><span data-stu-id="36afd-132">1</span></span>                | <span data-ttu-id="36afd-133">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="36afd-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="36afd-134">10 000 (11 000 – 1 000)</span><span class="sxs-lookup"><span data-stu-id="36afd-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="36afd-135">2</span><span class="sxs-lookup"><span data-stu-id="36afd-135">2</span></span>                | <span data-ttu-id="36afd-136">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="36afd-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="36afd-137">5 000 (10 000 – 5 000)</span><span class="sxs-lookup"><span data-stu-id="36afd-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="36afd-138">3</span><span class="sxs-lookup"><span data-stu-id="36afd-138">3</span></span>                | <span data-ttu-id="36afd-139">(11 000 – 1 000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="36afd-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="36afd-140">4 200 (5 000 – 800)</span><span class="sxs-lookup"><span data-stu-id="36afd-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="36afd-141">Hvis du velger **Månedlig** i feltet**Periodefrekvens**, må du definere 12 manuelle planleggingsintervaller.</span><span class="sxs-lookup"><span data-stu-id="36afd-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="36afd-142">Følgende tabell viser avskrivningsbeløpene for de to første intervallene.</span><span class="sxs-lookup"><span data-stu-id="36afd-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="36afd-143">Intervall</span><span class="sxs-lookup"><span data-stu-id="36afd-143">Interval</span></span> | <span data-ttu-id="36afd-144">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="36afd-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="36afd-145">Januar</span><span class="sxs-lookup"><span data-stu-id="36afd-145">January</span></span>  | <span data-ttu-id="36afd-146">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="36afd-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="36afd-147">Februar</span><span class="sxs-lookup"><span data-stu-id="36afd-147">February</span></span> | <span data-ttu-id="36afd-148">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="36afd-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="36afd-149">Hvis du velger **Halvårlig** i ****Periodefrekvens**-feltet**, må du definere to manuelle planleggingsintervaller.</span><span class="sxs-lookup"><span data-stu-id="36afd-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="36afd-150">Følgende tabell viser avskrivningsbeløpene for disse intervallene.</span><span class="sxs-lookup"><span data-stu-id="36afd-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="36afd-151">Intervall</span><span class="sxs-lookup"><span data-stu-id="36afd-151">Interval</span></span>    | <span data-ttu-id="36afd-152">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="36afd-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="36afd-153">30. juni</span><span class="sxs-lookup"><span data-stu-id="36afd-153">June 30</span></span>     | <span data-ttu-id="36afd-154">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="36afd-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="36afd-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="36afd-155">December 31</span></span> | <span data-ttu-id="36afd-156">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="36afd-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="36afd-157">Den totale prosenten for alle intervallene behøver ikke å være 100.</span><span class="sxs-lookup"><span data-stu-id="36afd-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="36afd-158">Imidlertid du mottar en melding hvis verdien i feltet **Kumulert prosent** på siden **Planer for anleggsmidlets avskrivningsprofil** ikke er **100**.</span><span class="sxs-lookup"><span data-stu-id="36afd-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




