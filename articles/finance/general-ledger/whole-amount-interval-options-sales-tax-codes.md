---
title: Hele beløp og alternativer for intervallberegning for mva-koder
description: Denne artikkelen beskriver alternativene for feltet Beregningsmåte når det gjelder mva-koder og hvordan mva beregnes for intervaller og hele beløp.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d452ccc94324a695f0d203486fc5fa8fe9db79f6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770557"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="8956d-103">Hele beløp og alternativer for intervallberegning for mva-koder</span><span class="sxs-lookup"><span data-stu-id="8956d-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8956d-104">Denne artikkelen beskriver alternativene for feltet Beregningsmåte når det gjelder mva-koder og hvordan mva beregnes for intervaller og hele beløp.</span><span class="sxs-lookup"><span data-stu-id="8956d-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="8956d-105">Du kan definere en mva-kode som skal beregnes basert på et helt beløp eller et fakturabeløp.</span><span class="sxs-lookup"><span data-stu-id="8956d-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="8956d-106">Bruk Beregningsmåte-feltet på hurtigfanen Beregning på Mva-kode-siden for å velge hvordan du vil beregne en mva-kode.</span><span class="sxs-lookup"><span data-stu-id="8956d-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="8956d-107">Hele beløp – mva-satsen brukes for hele det avgiftspliktige beløpet.</span><span class="sxs-lookup"><span data-stu-id="8956d-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="8956d-108">Intervall – Det avgiftspliktige beløpet er inndelt i deler, og hver del er innenfor et intervall som har en bestemt mva-sats.</span><span class="sxs-lookup"><span data-stu-id="8956d-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="8956d-109">Den delen av beløpet som ligger innen et gitt intervall blir avgiftsbelagt i henhold til mva-satsen for det intervallet.</span><span class="sxs-lookup"><span data-stu-id="8956d-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="8956d-110">Mva er summen av mva-beløpene som beregnes for hvert beløpsintervall.</span><span class="sxs-lookup"><span data-stu-id="8956d-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="8956d-111">Intervallalternativet er bare tilgjengelig når du velger Linje i Beregningsmåte-feltet i mva-området på siden Økonomiparametere.</span><span class="sxs-lookup"><span data-stu-id="8956d-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="8956d-112">Intervaller defineres på siden Verdier for merverdiavgiftskode ved å angi minimum og maksimum grensebeløp per mva-sats.</span><span class="sxs-lookup"><span data-stu-id="8956d-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="8956d-113">For at mva skal kunne beregnes av alle avgiftspliktige beløp, uavhengig av hvilken metode som er valgt, må intervallene oppfylle følgende regler:</span><span class="sxs-lookup"><span data-stu-id="8956d-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="8956d-114">Det første intervallet må ha en nedre grense på 0.</span><span class="sxs-lookup"><span data-stu-id="8956d-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="8956d-115">Det siste intervallet må ha en maksimal grense på null, som angir uendelig.</span><span class="sxs-lookup"><span data-stu-id="8956d-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="8956d-116">Den maksimale grensen til et intervall må være minimumsgrensen til det neste intervallet.</span><span class="sxs-lookup"><span data-stu-id="8956d-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="8956d-117">Hvis et beløp er den øvre grensen til det forrige intervallet, og den nedre grensen til det neste intervallet, er det mva-satsen til det første intervallet som brukes på beløpet.</span><span class="sxs-lookup"><span data-stu-id="8956d-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="8956d-118">Hvis et beløp faller utenfor intervallene som er definert av øvre og nedre grenser, brukes en mva-sats på 0.</span><span class="sxs-lookup"><span data-stu-id="8956d-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="8956d-119">Eksempel: beregningsmåte Hele beløp</span><span class="sxs-lookup"><span data-stu-id="8956d-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="8956d-120">På Siden Verdier for merverdiavgiftskode defineres mva-satser i følgende intervaller:</span><span class="sxs-lookup"><span data-stu-id="8956d-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="8956d-121">**Minimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8956d-121">**Minimum limit**</span></span> | <span data-ttu-id="8956d-122">**Maksimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8956d-122">**Maximum limit**</span></span> | <span data-ttu-id="8956d-123">**Avgiftssats**</span><span class="sxs-lookup"><span data-stu-id="8956d-123">**Tax rate**</span></span> |
| <span data-ttu-id="8956d-124">0,00</span><span class="sxs-lookup"><span data-stu-id="8956d-124">0.00</span></span>              | <span data-ttu-id="8956d-125">50,00</span><span class="sxs-lookup"><span data-stu-id="8956d-125">50.00</span></span>             | <span data-ttu-id="8956d-126">30 %</span><span class="sxs-lookup"><span data-stu-id="8956d-126">30%</span></span>          |
| <span data-ttu-id="8956d-127">50,00</span><span class="sxs-lookup"><span data-stu-id="8956d-127">50.00</span></span>             | <span data-ttu-id="8956d-128">100,00</span><span class="sxs-lookup"><span data-stu-id="8956d-128">100.00</span></span>            | <span data-ttu-id="8956d-129">20 %</span><span class="sxs-lookup"><span data-stu-id="8956d-129">20%</span></span>          |
| <span data-ttu-id="8956d-130">100,00</span><span class="sxs-lookup"><span data-stu-id="8956d-130">100.00</span></span>            | <span data-ttu-id="8956d-131">0,00</span><span class="sxs-lookup"><span data-stu-id="8956d-131">0.00</span></span>              | <span data-ttu-id="8956d-132">10 %</span><span class="sxs-lookup"><span data-stu-id="8956d-132">10%</span></span>          |

<span data-ttu-id="8956d-133">Mva-satsen beregnes på hele det avgiftspliktige beløpet.</span><span class="sxs-lookup"><span data-stu-id="8956d-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="8956d-134">Avgiftsbelagt beløp (pris)</span><span class="sxs-lookup"><span data-stu-id="8956d-134">Taxable amount (price)</span></span> | <span data-ttu-id="8956d-135">Beregning</span><span class="sxs-lookup"><span data-stu-id="8956d-135">Calculation</span></span>    | <span data-ttu-id="8956d-136">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="8956d-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="8956d-137">35,00</span><span class="sxs-lookup"><span data-stu-id="8956d-137">35.00</span></span>                  | <span data-ttu-id="8956d-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8956d-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="8956d-139">10,50</span><span class="sxs-lookup"><span data-stu-id="8956d-139">10.50</span></span>     |
| <span data-ttu-id="8956d-140">50,00</span><span class="sxs-lookup"><span data-stu-id="8956d-140">50.00</span></span>                  | <span data-ttu-id="8956d-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8956d-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="8956d-142">15,00</span><span class="sxs-lookup"><span data-stu-id="8956d-142">15.00</span></span>     |
| <span data-ttu-id="8956d-143">85,00</span><span class="sxs-lookup"><span data-stu-id="8956d-143">85.00</span></span>                  | <span data-ttu-id="8956d-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="8956d-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="8956d-145">17,00</span><span class="sxs-lookup"><span data-stu-id="8956d-145">17.00</span></span>     |
| <span data-ttu-id="8956d-146">305,00</span><span class="sxs-lookup"><span data-stu-id="8956d-146">305.00</span></span>                 | <span data-ttu-id="8956d-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="8956d-147">305.00 \* 0.10</span></span> | <span data-ttu-id="8956d-148">30,50</span><span class="sxs-lookup"><span data-stu-id="8956d-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="8956d-149">Eksempel: Beregningsmåte intervall</span><span class="sxs-lookup"><span data-stu-id="8956d-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="8956d-150">På Verdier-siden er mva-satsene angitt i følgende intervaller:</span><span class="sxs-lookup"><span data-stu-id="8956d-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="8956d-151">**Minimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8956d-151">**Minimum limit**</span></span> | <span data-ttu-id="8956d-152">**Maksimumsgrense**</span><span class="sxs-lookup"><span data-stu-id="8956d-152">**Maximum limit**</span></span> | <span data-ttu-id="8956d-153">**Avgiftssats**</span><span class="sxs-lookup"><span data-stu-id="8956d-153">**Tax rate**</span></span> |
| <span data-ttu-id="8956d-154">0,00</span><span class="sxs-lookup"><span data-stu-id="8956d-154">0.00</span></span>              | <span data-ttu-id="8956d-155">50,00</span><span class="sxs-lookup"><span data-stu-id="8956d-155">50.00</span></span>             | <span data-ttu-id="8956d-156">30 %</span><span class="sxs-lookup"><span data-stu-id="8956d-156">30%</span></span>          |
| <span data-ttu-id="8956d-157">50,00</span><span class="sxs-lookup"><span data-stu-id="8956d-157">50.00</span></span>             | <span data-ttu-id="8956d-158">100,00</span><span class="sxs-lookup"><span data-stu-id="8956d-158">100.00</span></span>            | <span data-ttu-id="8956d-159">20 %</span><span class="sxs-lookup"><span data-stu-id="8956d-159">20%</span></span>          |
| <span data-ttu-id="8956d-160">100,00</span><span class="sxs-lookup"><span data-stu-id="8956d-160">100.00</span></span>            | <span data-ttu-id="8956d-161">0,00</span><span class="sxs-lookup"><span data-stu-id="8956d-161">0.00</span></span>              | <span data-ttu-id="8956d-162">10 %</span><span class="sxs-lookup"><span data-stu-id="8956d-162">10%</span></span>          |

<span data-ttu-id="8956d-163">Mva er summen av mva-beløpene som beregnes for hvert beløpsintervall.</span><span class="sxs-lookup"><span data-stu-id="8956d-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="8956d-164">Avgiftsbelagt beløp (pris)</span><span class="sxs-lookup"><span data-stu-id="8956d-164">Taxable amount (price)</span></span> | <span data-ttu-id="8956d-165">Beregning</span><span class="sxs-lookup"><span data-stu-id="8956d-165">Calculation</span></span>                                                               | <span data-ttu-id="8956d-166">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="8956d-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8956d-167">35,00</span><span class="sxs-lookup"><span data-stu-id="8956d-167">35.00</span></span>                  | <span data-ttu-id="8956d-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8956d-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="8956d-169">10,50</span><span class="sxs-lookup"><span data-stu-id="8956d-169">10.50</span></span>     |
| <span data-ttu-id="8956d-170">50,00</span><span class="sxs-lookup"><span data-stu-id="8956d-170">50.00</span></span>                  | <span data-ttu-id="8956d-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="8956d-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="8956d-172">15,00</span><span class="sxs-lookup"><span data-stu-id="8956d-172">15.00</span></span>     |
| <span data-ttu-id="8956d-173">85,00</span><span class="sxs-lookup"><span data-stu-id="8956d-173">85.00</span></span>                  | <span data-ttu-id="8956d-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="8956d-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="8956d-175">22,00</span><span class="sxs-lookup"><span data-stu-id="8956d-175">22.00</span></span>     |
| <span data-ttu-id="8956d-176">305,00</span><span class="sxs-lookup"><span data-stu-id="8956d-176">305.00</span></span>                 | <span data-ttu-id="8956d-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="8956d-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="8956d-178">45.50</span><span class="sxs-lookup"><span data-stu-id="8956d-178">45.50</span></span>     |



<span data-ttu-id="8956d-179">Hvis du vil ha mer informasjon, kan du se [Mva-satser basert på feltene grensegrunnlag og beregningsmetoder](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="8956d-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





