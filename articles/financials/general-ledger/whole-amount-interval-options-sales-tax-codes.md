---
title: "Hele beløp og alternativer for intervallberegning for mva-koder"
description: "Denne artikkelen beskriver alternativene for feltet Beregningsmåte når det gjelder mva-koder og hvordan mva beregnes for intervaller og hele beløp."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 647252c7b47ee9c3c6b33b0c1413a1d44ede7c30
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="8257a-103">Hele beløp og alternativer for intervallberegning for mva-koder</span><span class="sxs-lookup"><span data-stu-id="8257a-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="8257a-104">Denne artikkelen beskriver alternativene for feltet Beregningsmåte når det gjelder mva-koder og hvordan mva beregnes for intervaller og hele beløp.</span><span class="sxs-lookup"><span data-stu-id="8257a-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="8257a-105">Du kan definere en mva-kode som skal beregnes basert på et helt beløp eller et fakturabeløp.</span><span class="sxs-lookup"><span data-stu-id="8257a-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="8257a-106">Bruk Beregningsmåte-feltet på hurtigfanen Beregning på Mva-kode-siden for å velge hvordan du vil beregne en mva-kode.</span><span class="sxs-lookup"><span data-stu-id="8257a-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="8257a-107">Hele beløp – mva-satsen brukes for hele det avgiftspliktige beløpet.</span><span class="sxs-lookup"><span data-stu-id="8257a-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="8257a-108">Intervall – Det avgiftspliktige beløpet er inndelt i deler, og hver del er innenfor et intervall som har en bestemt mva-sats.</span><span class="sxs-lookup"><span data-stu-id="8257a-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="8257a-109">Den delen av beløpet som ligger innen et gitt intervall blir avgiftsbelagt i henhold til mva-satsen for det intervallet.</span><span class="sxs-lookup"><span data-stu-id="8257a-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="8257a-110">Mva er summen av mva-beløpene som beregnes for hvert beløpsintervall.</span><span class="sxs-lookup"><span data-stu-id="8257a-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="8257a-111">Intervallalternativet er bare tilgjengelig når du velger Linje i Beregningsmåte-feltet i mva-området på siden Økonomiparametere.</span><span class="sxs-lookup"><span data-stu-id="8257a-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="8257a-112">Intervaller defineres på siden Verdier for merverdiavgiftskode ved å angi minimum og maksimum grensebeløp per mva-sats.</span><span class="sxs-lookup"><span data-stu-id="8257a-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="8257a-113">For at mva skal kunne beregnes av alle avgiftspliktige beløp, uavhengig av hvilken metode som er valgt, må intervallene oppfylle følgende regler:</span><span class="sxs-lookup"><span data-stu-id="8257a-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="8257a-114">Det første intervallet må ha en nedre grense på 0.</span><span class="sxs-lookup"><span data-stu-id="8257a-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="8257a-115">Det siste intervallet må ha en maksimal grense på null, som angir uendelig.</span><span class="sxs-lookup"><span data-stu-id="8257a-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="8257a-116">Den maksimale grensen til et intervall må være minimumsgrensen til det neste intervallet.</span><span class="sxs-lookup"><span data-stu-id="8257a-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="8257a-117">Hvis et beløp er den øvre grensen til det forrige intervallet, og den nedre grensen til det neste intervallet, er det mva-satsen til det første intervallet som brukes på beløpet.</span><span class="sxs-lookup"><span data-stu-id="8257a-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="8257a-118">Hvis et beløp faller utenfor intervallene som er definert av øvre og nedre grenser, brukes en mva-sats på 0.</span><span class="sxs-lookup"><span data-stu-id="8257a-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="8257a-119">Eksempel: beregningsmåte Hele beløp</span><span class="sxs-lookup"><span data-stu-id="8257a-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="8257a-120">På Siden Verdier for merverdiavgiftskode defineres mva-satser i følgende intervaller:</span><span class="sxs-lookup"><span data-stu-id="8257a-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="8257a-121">**Minimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8257a-121">**Minimum limit**</span></span> | <span data-ttu-id="8257a-122">**Maksimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8257a-122">**Maximum limit**</span></span> | <span data-ttu-id="8257a-123">**Avgiftssats**</span><span class="sxs-lookup"><span data-stu-id="8257a-123">**Tax rate**</span></span> |
| <span data-ttu-id="8257a-124">0,00</span><span class="sxs-lookup"><span data-stu-id="8257a-124">0.00</span></span>              | <span data-ttu-id="8257a-125">50,00</span><span class="sxs-lookup"><span data-stu-id="8257a-125">50.00</span></span>             | <span data-ttu-id="8257a-126">30 %</span><span class="sxs-lookup"><span data-stu-id="8257a-126">30%</span></span>          |
| <span data-ttu-id="8257a-127">50,00</span><span class="sxs-lookup"><span data-stu-id="8257a-127">50.00</span></span>             | <span data-ttu-id="8257a-128">100,00</span><span class="sxs-lookup"><span data-stu-id="8257a-128">100.00</span></span>            | <span data-ttu-id="8257a-129">20 %</span><span class="sxs-lookup"><span data-stu-id="8257a-129">20%</span></span>          |
| <span data-ttu-id="8257a-130">100,00</span><span class="sxs-lookup"><span data-stu-id="8257a-130">100.00</span></span>            | <span data-ttu-id="8257a-131">0,00</span><span class="sxs-lookup"><span data-stu-id="8257a-131">0.00</span></span>              | <span data-ttu-id="8257a-132">10 %</span><span class="sxs-lookup"><span data-stu-id="8257a-132">10%</span></span>          |

<span data-ttu-id="8257a-133">Mva-satsen beregnes på hele det avgiftspliktige beløpet.</span><span class="sxs-lookup"><span data-stu-id="8257a-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="8257a-134">Avgiftsbelagt beløp (pris)</span><span class="sxs-lookup"><span data-stu-id="8257a-134">Taxable amount (price)</span></span> | <span data-ttu-id="8257a-135">Beregning</span><span class="sxs-lookup"><span data-stu-id="8257a-135">Calculation</span></span>    | <span data-ttu-id="8257a-136">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="8257a-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="8257a-137">35,00</span><span class="sxs-lookup"><span data-stu-id="8257a-137">35.00</span></span>                  | <span data-ttu-id="8257a-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8257a-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="8257a-139">10,50</span><span class="sxs-lookup"><span data-stu-id="8257a-139">10.50</span></span>     |
| <span data-ttu-id="8257a-140">50,00</span><span class="sxs-lookup"><span data-stu-id="8257a-140">50.00</span></span>                  | <span data-ttu-id="8257a-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8257a-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="8257a-142">15,00</span><span class="sxs-lookup"><span data-stu-id="8257a-142">15.00</span></span>     |
| <span data-ttu-id="8257a-143">85,00</span><span class="sxs-lookup"><span data-stu-id="8257a-143">85.00</span></span>                  | <span data-ttu-id="8257a-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="8257a-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="8257a-145">17,00</span><span class="sxs-lookup"><span data-stu-id="8257a-145">17.00</span></span>     |
| <span data-ttu-id="8257a-146">305,00</span><span class="sxs-lookup"><span data-stu-id="8257a-146">305.00</span></span>                 | <span data-ttu-id="8257a-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="8257a-147">305.00 \* 0.10</span></span> | <span data-ttu-id="8257a-148">30,50</span><span class="sxs-lookup"><span data-stu-id="8257a-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="8257a-149">Eksempel: Beregningsmåte intervall</span><span class="sxs-lookup"><span data-stu-id="8257a-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="8257a-150">På Verdier-siden er mva-satsene angitt i følgende intervaller:</span><span class="sxs-lookup"><span data-stu-id="8257a-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="8257a-151">**Minimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8257a-151">**Minimum limit**</span></span> | <span data-ttu-id="8257a-152">**Maksimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8257a-152">**Maximum limit**</span></span> | <span data-ttu-id="8257a-153">**Avgiftssats**</span><span class="sxs-lookup"><span data-stu-id="8257a-153">**Tax rate**</span></span> |
| <span data-ttu-id="8257a-154">0,00</span><span class="sxs-lookup"><span data-stu-id="8257a-154">0.00</span></span>              | <span data-ttu-id="8257a-155">50,00</span><span class="sxs-lookup"><span data-stu-id="8257a-155">50.00</span></span>             | <span data-ttu-id="8257a-156">30 %</span><span class="sxs-lookup"><span data-stu-id="8257a-156">30%</span></span>          |
| <span data-ttu-id="8257a-157">50,00</span><span class="sxs-lookup"><span data-stu-id="8257a-157">50.00</span></span>             | <span data-ttu-id="8257a-158">100,00</span><span class="sxs-lookup"><span data-stu-id="8257a-158">100.00</span></span>            | <span data-ttu-id="8257a-159">20 %</span><span class="sxs-lookup"><span data-stu-id="8257a-159">20%</span></span>          |
| <span data-ttu-id="8257a-160">100,00</span><span class="sxs-lookup"><span data-stu-id="8257a-160">100.00</span></span>            | <span data-ttu-id="8257a-161">0,00</span><span class="sxs-lookup"><span data-stu-id="8257a-161">0.00</span></span>              | <span data-ttu-id="8257a-162">10 %</span><span class="sxs-lookup"><span data-stu-id="8257a-162">10%</span></span>          |

<span data-ttu-id="8257a-163">Mva er summen av mva-beløpene som beregnes for hvert beløpsintervall.</span><span class="sxs-lookup"><span data-stu-id="8257a-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="8257a-164">Avgiftsbelagt beløp (pris)</span><span class="sxs-lookup"><span data-stu-id="8257a-164">Taxable amount (price)</span></span> | <span data-ttu-id="8257a-165">Beregning</span><span class="sxs-lookup"><span data-stu-id="8257a-165">Calculation</span></span>                                                               | <span data-ttu-id="8257a-166">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="8257a-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8257a-167">35,00</span><span class="sxs-lookup"><span data-stu-id="8257a-167">35.00</span></span>                  | <span data-ttu-id="8257a-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8257a-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="8257a-169">10,50</span><span class="sxs-lookup"><span data-stu-id="8257a-169">10.50</span></span>     |
| <span data-ttu-id="8257a-170">50,00</span><span class="sxs-lookup"><span data-stu-id="8257a-170">50.00</span></span>                  | <span data-ttu-id="8257a-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8257a-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="8257a-172">15,00</span><span class="sxs-lookup"><span data-stu-id="8257a-172">15.00</span></span>     |
| <span data-ttu-id="8257a-173">85,00</span><span class="sxs-lookup"><span data-stu-id="8257a-173">85.00</span></span>                  | <span data-ttu-id="8257a-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="8257a-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="8257a-175">22,00</span><span class="sxs-lookup"><span data-stu-id="8257a-175">22.00</span></span>     |
| <span data-ttu-id="8257a-176">305,00</span><span class="sxs-lookup"><span data-stu-id="8257a-176">305.00</span></span>                 | <span data-ttu-id="8257a-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="8257a-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="8257a-178">45,50</span><span class="sxs-lookup"><span data-stu-id="8257a-178">45.50</span></span>     |



<span data-ttu-id="8257a-179">Hvis du vil ha mer informasjon , kan du se [Bestemme mva-satser basert på feltene Grensegrunnlag og Beregningsmåte](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="8257a-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






