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
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017


---

# <a name="factor-depreciation"></a><span data-ttu-id="28f4c-103">Faktoravskrivning</span><span class="sxs-lookup"><span data-stu-id="28f4c-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="28f4c-104">Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="28f4c-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="28f4c-105">Faktorer er prosentandeler som brukes til å avskrive midler.</span><span class="sxs-lookup"><span data-stu-id="28f4c-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="28f4c-106">Når du definerer en avskrivningsprofil for anleggsmidler og velger **Faktor** i **Metode**-feltet på **Avskrivningsprofiler**, kan du definere progressiv, degressiv eller lineær avskrivning:</span><span class="sxs-lookup"><span data-stu-id="28f4c-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="28f4c-107">Ved progressiv avskrivning øker avskrivningsbeløpet for hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="28f4c-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="28f4c-108">Ved degressiv avskrivning reduseres avskrivningsbeløpet over tid.</span><span class="sxs-lookup"><span data-stu-id="28f4c-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="28f4c-109">Ved lineær avskrivning er avskrivningen den samme i hver periode.</span><span class="sxs-lookup"><span data-stu-id="28f4c-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="28f4c-110">Reglene og eksemplene nedenfor indikerer hvordan du kan definere faktorer for hver avskrivningstype.</span><span class="sxs-lookup"><span data-stu-id="28f4c-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="28f4c-111">Når du velger **Faktor** i **Metode**-feltet, vises **Faktor**-feltet og **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="28f4c-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="28f4c-112">Progressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="28f4c-112">Progressive depreciation</span></span>
<span data-ttu-id="28f4c-113">Verdien i **Faktor**-feltet er større enn **50**.</span><span class="sxs-lookup"><span data-stu-id="28f4c-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="28f4c-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="28f4c-114">Example</span></span>

<span data-ttu-id="28f4c-115">Anskaffelsesprisen er 100 000, faktoren er 70, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="28f4c-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="28f4c-116">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="28f4c-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="28f4c-117">År</span><span class="sxs-lookup"><span data-stu-id="28f4c-117">Year</span></span> | <span data-ttu-id="28f4c-118">Periode</span><span class="sxs-lookup"><span data-stu-id="28f4c-118">Period</span></span>      | <span data-ttu-id="28f4c-119">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="28f4c-119">Depreciation amount</span></span> | <span data-ttu-id="28f4c-120">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="28f4c-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="28f4c-121">1</span><span class="sxs-lookup"><span data-stu-id="28f4c-121">1</span></span>    | <span data-ttu-id="28f4c-122">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-122">December 31</span></span> | <span data-ttu-id="28f4c-123">307,69</span><span class="sxs-lookup"><span data-stu-id="28f4c-123">307.69</span></span>              | <span data-ttu-id="28f4c-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="28f4c-124">99,692.31</span></span>             |
| <span data-ttu-id="28f4c-125">2</span><span class="sxs-lookup"><span data-stu-id="28f4c-125">2</span></span>    | <span data-ttu-id="28f4c-126">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-126">December 31</span></span> | <span data-ttu-id="28f4c-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="28f4c-127">1,447.21</span></span>            | <span data-ttu-id="28f4c-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="28f4c-128">98,245.10</span></span>             |
| <span data-ttu-id="28f4c-129">3</span><span class="sxs-lookup"><span data-stu-id="28f4c-129">3</span></span>    | <span data-ttu-id="28f4c-130">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-130">December 31</span></span> | <span data-ttu-id="28f4c-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="28f4c-131">3,104.50</span></span>            | <span data-ttu-id="28f4c-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="28f4c-132">95,140.60</span></span>             |
| <span data-ttu-id="28f4c-133">4</span><span class="sxs-lookup"><span data-stu-id="28f4c-133">4</span></span>    | <span data-ttu-id="28f4c-134">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-134">December 31</span></span> | <span data-ttu-id="28f4c-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="28f4c-135">5,150.21</span></span>            | <span data-ttu-id="28f4c-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="28f4c-136">89,990.39</span></span>             |
| <span data-ttu-id="28f4c-137">5</span><span class="sxs-lookup"><span data-stu-id="28f4c-137">5</span></span>    | <span data-ttu-id="28f4c-138">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-138">December 31</span></span> | <span data-ttu-id="28f4c-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="28f4c-139">7,522.95</span></span>            | <span data-ttu-id="28f4c-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="28f4c-140">82,467.44</span></span>             |
| <span data-ttu-id="28f4c-141">6</span><span class="sxs-lookup"><span data-stu-id="28f4c-141">6</span></span>    | <span data-ttu-id="28f4c-142">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-142">December 31</span></span> | <span data-ttu-id="28f4c-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="28f4c-143">10,184.06</span></span>           | <span data-ttu-id="28f4c-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="28f4c-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="28f4c-145">Degressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="28f4c-145">Digressive depreciation</span></span>
<span data-ttu-id="28f4c-146">Verdien i **Faktor**-feltet er mindre enn **50**.</span><span class="sxs-lookup"><span data-stu-id="28f4c-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="28f4c-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="28f4c-147">Example</span></span>

<span data-ttu-id="28f4c-148">Anskaffelsesprisen er 100 000, faktoren er 20, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="28f4c-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="28f4c-149">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="28f4c-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="28f4c-150">År</span><span class="sxs-lookup"><span data-stu-id="28f4c-150">Year</span></span> | <span data-ttu-id="28f4c-151">Periode</span><span class="sxs-lookup"><span data-stu-id="28f4c-151">Period</span></span>      | <span data-ttu-id="28f4c-152">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="28f4c-152">Depreciation amount</span></span> | <span data-ttu-id="28f4c-153">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="28f4c-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="28f4c-154">1</span><span class="sxs-lookup"><span data-stu-id="28f4c-154">1</span></span>    | <span data-ttu-id="28f4c-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-155">December 31</span></span> | <span data-ttu-id="28f4c-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="28f4c-156">56,080.43</span></span>           | <span data-ttu-id="28f4c-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="28f4c-157">43,919.57</span></span>             |
| <span data-ttu-id="28f4c-158">2</span><span class="sxs-lookup"><span data-stu-id="28f4c-158">2</span></span>    | <span data-ttu-id="28f4c-159">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-159">December 31</span></span> | <span data-ttu-id="28f4c-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="28f4c-160">10,665.70</span></span>           | <span data-ttu-id="28f4c-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="28f4c-161">33,253.87</span></span>             |
| <span data-ttu-id="28f4c-162">3</span><span class="sxs-lookup"><span data-stu-id="28f4c-162">3</span></span>    | <span data-ttu-id="28f4c-163">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-163">December 31</span></span> | <span data-ttu-id="28f4c-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="28f4c-164">7,156.22</span></span>            | <span data-ttu-id="28f4c-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="28f4c-165">26,097.65</span></span>             |
| <span data-ttu-id="28f4c-166">4</span><span class="sxs-lookup"><span data-stu-id="28f4c-166">4</span></span>    | <span data-ttu-id="28f4c-167">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-167">December 31</span></span> | <span data-ttu-id="28f4c-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="28f4c-168">5,538.06</span></span>            | <span data-ttu-id="28f4c-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="28f4c-169">20,559.59</span></span>             |
| <span data-ttu-id="28f4c-170">5</span><span class="sxs-lookup"><span data-stu-id="28f4c-170">5</span></span>    | <span data-ttu-id="28f4c-171">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-171">December 31</span></span> | <span data-ttu-id="28f4c-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="28f4c-172">4,579.89</span></span>            | <span data-ttu-id="28f4c-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="28f4c-173">15,979.70</span></span>             |
| <span data-ttu-id="28f4c-174">6</span><span class="sxs-lookup"><span data-stu-id="28f4c-174">6</span></span>    | <span data-ttu-id="28f4c-175">31. desember</span><span class="sxs-lookup"><span data-stu-id="28f4c-175">December 31</span></span> | <span data-ttu-id="28f4c-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="28f4c-176">3,937.36</span></span>            | <span data-ttu-id="28f4c-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="28f4c-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="28f4c-178">Lineær avskrivning</span><span class="sxs-lookup"><span data-stu-id="28f4c-178">Straight line depreciation</span></span>
<span data-ttu-id="28f4c-179">Verdien i **Faktor**-feltet er lik **50**.</span><span class="sxs-lookup"><span data-stu-id="28f4c-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="28f4c-180">I dette tilfellet er avskrivningen den samme i hver periode, og du bør vurdere hvilke implikasjoner dette valget kan ha for andre felt. Les mer i [Lineær levetidsavskrivning](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="28f4c-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




