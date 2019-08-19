---
title: Faktoravskrivning
description: Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840535"
---
# <a name="factor-depreciation"></a><span data-ttu-id="fd44b-103">Faktoravskrivning</span><span class="sxs-lookup"><span data-stu-id="fd44b-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd44b-104">Denne artikkelen gir en oversikt over faktoravskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="fd44b-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="fd44b-105">Faktorer er prosentandeler som brukes til å avskrive midler.</span><span class="sxs-lookup"><span data-stu-id="fd44b-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="fd44b-106">Når du definerer en avskrivningsprofil for anleggsmidler og velger **Faktor** i **Metode**-feltet på **Avskrivningsprofiler**, kan du definere progressiv, degressiv eller lineær avskrivning:</span><span class="sxs-lookup"><span data-stu-id="fd44b-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="fd44b-107">Ved progressiv avskrivning øker avskrivningsbeløpet for hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="fd44b-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="fd44b-108">Ved degressiv avskrivning reduseres avskrivningsbeløpet over tid.</span><span class="sxs-lookup"><span data-stu-id="fd44b-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="fd44b-109">Ved lineær avskrivning er avskrivningen den samme i hver periode.</span><span class="sxs-lookup"><span data-stu-id="fd44b-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="fd44b-110">Reglene og eksemplene nedenfor indikerer hvordan du kan definere faktorer for hver avskrivningstype.</span><span class="sxs-lookup"><span data-stu-id="fd44b-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="fd44b-111">Når du velger **Faktor** i **Metode**-feltet, vises **Faktor**-feltet og **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fd44b-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="fd44b-112">Progressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="fd44b-112">Progressive depreciation</span></span>
<span data-ttu-id="fd44b-113">Verdien i **Faktor**-feltet er større enn **50**.</span><span class="sxs-lookup"><span data-stu-id="fd44b-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="fd44b-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fd44b-114">Example</span></span>

<span data-ttu-id="fd44b-115">Anskaffelsesprisen er 100 000, faktoren er 70, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="fd44b-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="fd44b-116">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="fd44b-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="fd44b-117">År</span><span class="sxs-lookup"><span data-stu-id="fd44b-117">Year</span></span> | <span data-ttu-id="fd44b-118">Periode</span><span class="sxs-lookup"><span data-stu-id="fd44b-118">Period</span></span>      | <span data-ttu-id="fd44b-119">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="fd44b-119">Depreciation amount</span></span> | <span data-ttu-id="fd44b-120">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="fd44b-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="fd44b-121">1</span><span class="sxs-lookup"><span data-stu-id="fd44b-121">1</span></span>    | <span data-ttu-id="fd44b-122">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-122">December 31</span></span> | <span data-ttu-id="fd44b-123">307,69</span><span class="sxs-lookup"><span data-stu-id="fd44b-123">307.69</span></span>              | <span data-ttu-id="fd44b-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="fd44b-124">99,692.31</span></span>             |
| <span data-ttu-id="fd44b-125">2</span><span class="sxs-lookup"><span data-stu-id="fd44b-125">2</span></span>    | <span data-ttu-id="fd44b-126">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-126">December 31</span></span> | <span data-ttu-id="fd44b-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="fd44b-127">1,447.21</span></span>            | <span data-ttu-id="fd44b-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="fd44b-128">98,245.10</span></span>             |
| <span data-ttu-id="fd44b-129">3</span><span class="sxs-lookup"><span data-stu-id="fd44b-129">3</span></span>    | <span data-ttu-id="fd44b-130">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-130">December 31</span></span> | <span data-ttu-id="fd44b-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="fd44b-131">3,104.50</span></span>            | <span data-ttu-id="fd44b-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="fd44b-132">95,140.60</span></span>             |
| <span data-ttu-id="fd44b-133">4</span><span class="sxs-lookup"><span data-stu-id="fd44b-133">4</span></span>    | <span data-ttu-id="fd44b-134">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-134">December 31</span></span> | <span data-ttu-id="fd44b-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="fd44b-135">5,150.21</span></span>            | <span data-ttu-id="fd44b-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="fd44b-136">89,990.39</span></span>             |
| <span data-ttu-id="fd44b-137">5</span><span class="sxs-lookup"><span data-stu-id="fd44b-137">5</span></span>    | <span data-ttu-id="fd44b-138">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-138">December 31</span></span> | <span data-ttu-id="fd44b-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="fd44b-139">7,522.95</span></span>            | <span data-ttu-id="fd44b-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="fd44b-140">82,467.44</span></span>             |
| <span data-ttu-id="fd44b-141">6</span><span class="sxs-lookup"><span data-stu-id="fd44b-141">6</span></span>    | <span data-ttu-id="fd44b-142">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-142">December 31</span></span> | <span data-ttu-id="fd44b-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="fd44b-143">10,184.06</span></span>           | <span data-ttu-id="fd44b-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="fd44b-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="fd44b-145">Degressiv avskrivning</span><span class="sxs-lookup"><span data-stu-id="fd44b-145">Digressive depreciation</span></span>
<span data-ttu-id="fd44b-146">Verdien i **Faktor**-feltet er mindre enn **50**.</span><span class="sxs-lookup"><span data-stu-id="fd44b-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="fd44b-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fd44b-147">Example</span></span>

<span data-ttu-id="fd44b-148">Anskaffelsesprisen er 100 000, faktoren er 20, levetiden er 10 år og avskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="fd44b-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="fd44b-149">Avskrivningsbeløpet og beløpet for netto bokført verdi vises kun i de første seks årene av levetiden.</span><span class="sxs-lookup"><span data-stu-id="fd44b-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="fd44b-150">År</span><span class="sxs-lookup"><span data-stu-id="fd44b-150">Year</span></span> | <span data-ttu-id="fd44b-151">Periode</span><span class="sxs-lookup"><span data-stu-id="fd44b-151">Period</span></span>      | <span data-ttu-id="fd44b-152">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="fd44b-152">Depreciation amount</span></span> | <span data-ttu-id="fd44b-153">Netto bokført verdibeløp</span><span class="sxs-lookup"><span data-stu-id="fd44b-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="fd44b-154">1</span><span class="sxs-lookup"><span data-stu-id="fd44b-154">1</span></span>    | <span data-ttu-id="fd44b-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-155">December 31</span></span> | <span data-ttu-id="fd44b-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="fd44b-156">56,080.43</span></span>           | <span data-ttu-id="fd44b-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="fd44b-157">43,919.57</span></span>             |
| <span data-ttu-id="fd44b-158">2</span><span class="sxs-lookup"><span data-stu-id="fd44b-158">2</span></span>    | <span data-ttu-id="fd44b-159">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-159">December 31</span></span> | <span data-ttu-id="fd44b-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="fd44b-160">10,665.70</span></span>           | <span data-ttu-id="fd44b-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="fd44b-161">33,253.87</span></span>             |
| <span data-ttu-id="fd44b-162">3</span><span class="sxs-lookup"><span data-stu-id="fd44b-162">3</span></span>    | <span data-ttu-id="fd44b-163">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-163">December 31</span></span> | <span data-ttu-id="fd44b-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="fd44b-164">7,156.22</span></span>            | <span data-ttu-id="fd44b-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="fd44b-165">26,097.65</span></span>             |
| <span data-ttu-id="fd44b-166">4</span><span class="sxs-lookup"><span data-stu-id="fd44b-166">4</span></span>    | <span data-ttu-id="fd44b-167">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-167">December 31</span></span> | <span data-ttu-id="fd44b-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="fd44b-168">5,538.06</span></span>            | <span data-ttu-id="fd44b-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="fd44b-169">20,559.59</span></span>             |
| <span data-ttu-id="fd44b-170">5</span><span class="sxs-lookup"><span data-stu-id="fd44b-170">5</span></span>    | <span data-ttu-id="fd44b-171">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-171">December 31</span></span> | <span data-ttu-id="fd44b-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="fd44b-172">4,579.89</span></span>            | <span data-ttu-id="fd44b-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="fd44b-173">15,979.70</span></span>             |
| <span data-ttu-id="fd44b-174">6</span><span class="sxs-lookup"><span data-stu-id="fd44b-174">6</span></span>    | <span data-ttu-id="fd44b-175">31. desember</span><span class="sxs-lookup"><span data-stu-id="fd44b-175">December 31</span></span> | <span data-ttu-id="fd44b-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="fd44b-176">3,937.36</span></span>            | <span data-ttu-id="fd44b-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="fd44b-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="fd44b-178">Lineær avskrivning</span><span class="sxs-lookup"><span data-stu-id="fd44b-178">Straight line depreciation</span></span>
<span data-ttu-id="fd44b-179">Verdien i **Faktor**-feltet er lik **50**.</span><span class="sxs-lookup"><span data-stu-id="fd44b-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="fd44b-180">I dette tilfellet er avskrivningen den samme i hver periode, og du bør vurdere hvilke implikasjoner dette valget kan ha for andre felt. Les mer i [Lineær levetidsavskrivning](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="fd44b-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



