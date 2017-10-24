---
title: Faktoravskrivning
description: Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.
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
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="factor-depreciation"></a><span data-ttu-id="33d98-103">Faktoravskrivning</span><span class="sxs-lookup"><span data-stu-id="33d98-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="33d98-104">Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="33d98-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="33d98-105">Faktorer er prosentandeler som brukes til å avskrive midler.</span><span class="sxs-lookup"><span data-stu-id="33d98-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="33d98-106">Når du definerer en avskrivningsprofil for anleggsmidler og velger **Faktor** i **Metode**-feltet på **Avskrivningsprofiler**, kan du definere progressiv, degressiv eller lineær avskrivning:</span><span class="sxs-lookup"><span data-stu-id="33d98-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="33d98-107">Ved progressiv avskrivning øker avskrivningsbeløpet for hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="33d98-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="33d98-108">Ved degressiv avskrivning reduseres avskrivningsbeløpet over tid.</span><span class="sxs-lookup"><span data-stu-id="33d98-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="33d98-109">Ved lineær avskrivning er avskrivningen den samme i hver periode.</span><span class="sxs-lookup"><span data-stu-id="33d98-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="33d98-110">Reglene og eksemplene nedenfor indikerer hvordan du kan definere faktorer for hver avskrivningstype.</span><span class="sxs-lookup"><span data-stu-id="33d98-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="33d98-111">Når du velger **Faktor** i **Metode**-feltet, vises **Faktor**-feltet og **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="33d98-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="33d98-112">Progressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="33d98-112">Progressive depreciation</span></span>
<span data-ttu-id="33d98-113">Verdien i **Faktor**-feltet er større enn **50**.</span><span class="sxs-lookup"><span data-stu-id="33d98-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="33d98-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="33d98-114">Example</span></span>

<span data-ttu-id="33d98-115">Anskaffelsesprisen er 100 000, faktoren er 70, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="33d98-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="33d98-116">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="33d98-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="33d98-117">År</span><span class="sxs-lookup"><span data-stu-id="33d98-117">Year</span></span> | <span data-ttu-id="33d98-118">Periode</span><span class="sxs-lookup"><span data-stu-id="33d98-118">Period</span></span>      | <span data-ttu-id="33d98-119">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="33d98-119">Depreciation amount</span></span> | <span data-ttu-id="33d98-120">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="33d98-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="33d98-121">1</span><span class="sxs-lookup"><span data-stu-id="33d98-121">1</span></span>    | <span data-ttu-id="33d98-122">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-122">December 31</span></span> | <span data-ttu-id="33d98-123">307,69</span><span class="sxs-lookup"><span data-stu-id="33d98-123">307.69</span></span>              | <span data-ttu-id="33d98-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="33d98-124">99,692.31</span></span>             |
| <span data-ttu-id="33d98-125">2</span><span class="sxs-lookup"><span data-stu-id="33d98-125">2</span></span>    | <span data-ttu-id="33d98-126">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-126">December 31</span></span> | <span data-ttu-id="33d98-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="33d98-127">1,447.21</span></span>            | <span data-ttu-id="33d98-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="33d98-128">98,245.10</span></span>             |
| <span data-ttu-id="33d98-129">3</span><span class="sxs-lookup"><span data-stu-id="33d98-129">3</span></span>    | <span data-ttu-id="33d98-130">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-130">December 31</span></span> | <span data-ttu-id="33d98-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="33d98-131">3,104.50</span></span>            | <span data-ttu-id="33d98-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="33d98-132">95,140.60</span></span>             |
| <span data-ttu-id="33d98-133">4</span><span class="sxs-lookup"><span data-stu-id="33d98-133">4</span></span>    | <span data-ttu-id="33d98-134">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-134">December 31</span></span> | <span data-ttu-id="33d98-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="33d98-135">5,150.21</span></span>            | <span data-ttu-id="33d98-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="33d98-136">89,990.39</span></span>             |
| <span data-ttu-id="33d98-137">5</span><span class="sxs-lookup"><span data-stu-id="33d98-137">5</span></span>    | <span data-ttu-id="33d98-138">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-138">December 31</span></span> | <span data-ttu-id="33d98-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="33d98-139">7,522.95</span></span>            | <span data-ttu-id="33d98-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="33d98-140">82,467.44</span></span>             |
| <span data-ttu-id="33d98-141">6</span><span class="sxs-lookup"><span data-stu-id="33d98-141">6</span></span>    | <span data-ttu-id="33d98-142">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-142">December 31</span></span> | <span data-ttu-id="33d98-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="33d98-143">10,184.06</span></span>           | <span data-ttu-id="33d98-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="33d98-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="33d98-145">Degressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="33d98-145">Digressive depreciation</span></span>
<span data-ttu-id="33d98-146">Verdien i **Faktor**-feltet er mindre enn **50**.</span><span class="sxs-lookup"><span data-stu-id="33d98-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="33d98-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="33d98-147">Example</span></span>

<span data-ttu-id="33d98-148">Anskaffelsesprisen er 100 000, faktoren er 20, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="33d98-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="33d98-149">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="33d98-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="33d98-150">År</span><span class="sxs-lookup"><span data-stu-id="33d98-150">Year</span></span> | <span data-ttu-id="33d98-151">Periode</span><span class="sxs-lookup"><span data-stu-id="33d98-151">Period</span></span>      | <span data-ttu-id="33d98-152">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="33d98-152">Depreciation amount</span></span> | <span data-ttu-id="33d98-153">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="33d98-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="33d98-154">1</span><span class="sxs-lookup"><span data-stu-id="33d98-154">1</span></span>    | <span data-ttu-id="33d98-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-155">December 31</span></span> | <span data-ttu-id="33d98-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="33d98-156">56,080.43</span></span>           | <span data-ttu-id="33d98-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="33d98-157">43,919.57</span></span>             |
| <span data-ttu-id="33d98-158">2</span><span class="sxs-lookup"><span data-stu-id="33d98-158">2</span></span>    | <span data-ttu-id="33d98-159">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-159">December 31</span></span> | <span data-ttu-id="33d98-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="33d98-160">10,665.70</span></span>           | <span data-ttu-id="33d98-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="33d98-161">33,253.87</span></span>             |
| <span data-ttu-id="33d98-162">3</span><span class="sxs-lookup"><span data-stu-id="33d98-162">3</span></span>    | <span data-ttu-id="33d98-163">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-163">December 31</span></span> | <span data-ttu-id="33d98-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="33d98-164">7,156.22</span></span>            | <span data-ttu-id="33d98-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="33d98-165">26,097.65</span></span>             |
| <span data-ttu-id="33d98-166">4</span><span class="sxs-lookup"><span data-stu-id="33d98-166">4</span></span>    | <span data-ttu-id="33d98-167">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-167">December 31</span></span> | <span data-ttu-id="33d98-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="33d98-168">5,538.06</span></span>            | <span data-ttu-id="33d98-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="33d98-169">20,559.59</span></span>             |
| <span data-ttu-id="33d98-170">5</span><span class="sxs-lookup"><span data-stu-id="33d98-170">5</span></span>    | <span data-ttu-id="33d98-171">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-171">December 31</span></span> | <span data-ttu-id="33d98-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="33d98-172">4,579.89</span></span>            | <span data-ttu-id="33d98-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="33d98-173">15,979.70</span></span>             |
| <span data-ttu-id="33d98-174">6</span><span class="sxs-lookup"><span data-stu-id="33d98-174">6</span></span>    | <span data-ttu-id="33d98-175">31. desember</span><span class="sxs-lookup"><span data-stu-id="33d98-175">December 31</span></span> | <span data-ttu-id="33d98-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="33d98-176">3,937.36</span></span>            | <span data-ttu-id="33d98-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="33d98-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="33d98-178">Lineær avskrivning</span><span class="sxs-lookup"><span data-stu-id="33d98-178">Straight line depreciation</span></span>
<span data-ttu-id="33d98-179">Verdien i **Faktor**-feltet er lik **50**.</span><span class="sxs-lookup"><span data-stu-id="33d98-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="33d98-180">I dette tilfellet er avskrivningen den samme i hver periode, og du bør vurdere hvilke implikasjoner dette valget kan ha for andre felt. Les mer i [Lineær levetidsavskrivning](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="33d98-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




