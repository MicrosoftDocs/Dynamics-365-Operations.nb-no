---
title: Faktoravskrivning
description: Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: fa8bc4566def9dd770a97facb459e6b977bfaffb
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="factor-depreciation"></a><span data-ttu-id="a8694-103">Faktoravskrivning</span><span class="sxs-lookup"><span data-stu-id="a8694-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8694-104">Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="a8694-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="a8694-105">Faktorer er prosentandeler som brukes til å avskrive midler.</span><span class="sxs-lookup"><span data-stu-id="a8694-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="a8694-106">Når du definerer en avskrivningsprofil for anleggsmidler og velger **Faktor** i **Metode**-feltet på **Avskrivningsprofiler**, kan du definere progressiv, degressiv eller lineær avskrivning:</span><span class="sxs-lookup"><span data-stu-id="a8694-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="a8694-107">Ved progressiv avskrivning øker avskrivningsbeløpet for hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="a8694-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="a8694-108">Ved degressiv avskrivning reduseres avskrivningsbeløpet over tid.</span><span class="sxs-lookup"><span data-stu-id="a8694-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="a8694-109">Ved lineær avskrivning er avskrivningen den samme i hver periode.</span><span class="sxs-lookup"><span data-stu-id="a8694-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="a8694-110">Reglene og eksemplene nedenfor indikerer hvordan du kan definere faktorer for hver avskrivningstype.</span><span class="sxs-lookup"><span data-stu-id="a8694-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="a8694-111">Når du velger **Faktor** i **Metode**-feltet, vises **Faktor**-feltet og **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a8694-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="a8694-112">Progressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="a8694-112">Progressive depreciation</span></span>
<span data-ttu-id="a8694-113">Verdien i **Faktor**-feltet er større enn **50**.</span><span class="sxs-lookup"><span data-stu-id="a8694-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="a8694-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a8694-114">Example</span></span>

<span data-ttu-id="a8694-115">Anskaffelsesprisen er 100 000, faktoren er 70, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="a8694-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="a8694-116">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="a8694-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="a8694-117">År</span><span class="sxs-lookup"><span data-stu-id="a8694-117">Year</span></span> | <span data-ttu-id="a8694-118">Periode</span><span class="sxs-lookup"><span data-stu-id="a8694-118">Period</span></span>      | <span data-ttu-id="a8694-119">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="a8694-119">Depreciation amount</span></span> | <span data-ttu-id="a8694-120">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="a8694-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="a8694-121">1</span><span class="sxs-lookup"><span data-stu-id="a8694-121">1</span></span>    | <span data-ttu-id="a8694-122">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-122">December 31</span></span> | <span data-ttu-id="a8694-123">307,69</span><span class="sxs-lookup"><span data-stu-id="a8694-123">307.69</span></span>              | <span data-ttu-id="a8694-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="a8694-124">99,692.31</span></span>             |
| <span data-ttu-id="a8694-125">2</span><span class="sxs-lookup"><span data-stu-id="a8694-125">2</span></span>    | <span data-ttu-id="a8694-126">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-126">December 31</span></span> | <span data-ttu-id="a8694-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="a8694-127">1,447.21</span></span>            | <span data-ttu-id="a8694-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="a8694-128">98,245.10</span></span>             |
| <span data-ttu-id="a8694-129">3</span><span class="sxs-lookup"><span data-stu-id="a8694-129">3</span></span>    | <span data-ttu-id="a8694-130">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-130">December 31</span></span> | <span data-ttu-id="a8694-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="a8694-131">3,104.50</span></span>            | <span data-ttu-id="a8694-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="a8694-132">95,140.60</span></span>             |
| <span data-ttu-id="a8694-133">4</span><span class="sxs-lookup"><span data-stu-id="a8694-133">4</span></span>    | <span data-ttu-id="a8694-134">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-134">December 31</span></span> | <span data-ttu-id="a8694-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="a8694-135">5,150.21</span></span>            | <span data-ttu-id="a8694-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="a8694-136">89,990.39</span></span>             |
| <span data-ttu-id="a8694-137">5</span><span class="sxs-lookup"><span data-stu-id="a8694-137">5</span></span>    | <span data-ttu-id="a8694-138">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-138">December 31</span></span> | <span data-ttu-id="a8694-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="a8694-139">7,522.95</span></span>            | <span data-ttu-id="a8694-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="a8694-140">82,467.44</span></span>             |
| <span data-ttu-id="a8694-141">6</span><span class="sxs-lookup"><span data-stu-id="a8694-141">6</span></span>    | <span data-ttu-id="a8694-142">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-142">December 31</span></span> | <span data-ttu-id="a8694-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="a8694-143">10,184.06</span></span>           | <span data-ttu-id="a8694-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="a8694-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="a8694-145">Degressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="a8694-145">Digressive depreciation</span></span>
<span data-ttu-id="a8694-146">Verdien i **Faktor**-feltet er mindre enn **50**.</span><span class="sxs-lookup"><span data-stu-id="a8694-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="a8694-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a8694-147">Example</span></span>

<span data-ttu-id="a8694-148">Anskaffelsesprisen er 100 000, faktoren er 20, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="a8694-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="a8694-149">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="a8694-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="a8694-150">År</span><span class="sxs-lookup"><span data-stu-id="a8694-150">Year</span></span> | <span data-ttu-id="a8694-151">Periode</span><span class="sxs-lookup"><span data-stu-id="a8694-151">Period</span></span>      | <span data-ttu-id="a8694-152">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="a8694-152">Depreciation amount</span></span> | <span data-ttu-id="a8694-153">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="a8694-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="a8694-154">1</span><span class="sxs-lookup"><span data-stu-id="a8694-154">1</span></span>    | <span data-ttu-id="a8694-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-155">December 31</span></span> | <span data-ttu-id="a8694-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="a8694-156">56,080.43</span></span>           | <span data-ttu-id="a8694-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="a8694-157">43,919.57</span></span>             |
| <span data-ttu-id="a8694-158">2</span><span class="sxs-lookup"><span data-stu-id="a8694-158">2</span></span>    | <span data-ttu-id="a8694-159">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-159">December 31</span></span> | <span data-ttu-id="a8694-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="a8694-160">10,665.70</span></span>           | <span data-ttu-id="a8694-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="a8694-161">33,253.87</span></span>             |
| <span data-ttu-id="a8694-162">3</span><span class="sxs-lookup"><span data-stu-id="a8694-162">3</span></span>    | <span data-ttu-id="a8694-163">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-163">December 31</span></span> | <span data-ttu-id="a8694-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="a8694-164">7,156.22</span></span>            | <span data-ttu-id="a8694-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="a8694-165">26,097.65</span></span>             |
| <span data-ttu-id="a8694-166">4</span><span class="sxs-lookup"><span data-stu-id="a8694-166">4</span></span>    | <span data-ttu-id="a8694-167">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-167">December 31</span></span> | <span data-ttu-id="a8694-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="a8694-168">5,538.06</span></span>            | <span data-ttu-id="a8694-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="a8694-169">20,559.59</span></span>             |
| <span data-ttu-id="a8694-170">5</span><span class="sxs-lookup"><span data-stu-id="a8694-170">5</span></span>    | <span data-ttu-id="a8694-171">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-171">December 31</span></span> | <span data-ttu-id="a8694-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="a8694-172">4,579.89</span></span>            | <span data-ttu-id="a8694-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="a8694-173">15,979.70</span></span>             |
| <span data-ttu-id="a8694-174">6</span><span class="sxs-lookup"><span data-stu-id="a8694-174">6</span></span>    | <span data-ttu-id="a8694-175">31. desember</span><span class="sxs-lookup"><span data-stu-id="a8694-175">December 31</span></span> | <span data-ttu-id="a8694-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="a8694-176">3,937.36</span></span>            | <span data-ttu-id="a8694-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="a8694-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="a8694-178">Lineær avskrivning</span><span class="sxs-lookup"><span data-stu-id="a8694-178">Straight line depreciation</span></span>
<span data-ttu-id="a8694-179">Verdien i **Faktor**-feltet er lik **50**.</span><span class="sxs-lookup"><span data-stu-id="a8694-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="a8694-180">I dette tilfellet er avskrivningen den samme i hver periode, og du bør vurdere hvilke implikasjoner dette valget kan ha for andre felt. Les mer i [Lineær levetidsavskrivning](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="a8694-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




