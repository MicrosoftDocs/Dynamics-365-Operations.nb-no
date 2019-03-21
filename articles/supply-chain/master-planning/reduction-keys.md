---
title: Reduksjonsnøkler
description: Denne artikkelen inneholder eksempler som viser hvordan du definerer en reduksjonsnøkkel. Den inneholder informasjon om de ulike innstillingene for reduksjonsnøkler for og resultatene av hver. Du kan bruke en reduksjonsnøkkel til å definere hvordan du kan redusere prognosebehov.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2019
ms.locfileid: "770922"
---
# <a name="reduction-keys"></a><span data-ttu-id="e67c7-105">Reduksjonsnøkler</span><span class="sxs-lookup"><span data-stu-id="e67c7-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e67c7-106">Denne artikkelen inneholder eksempler som viser hvordan du definerer en reduksjonsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="e67c7-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="e67c7-107">Den inneholder informasjon om de ulike innstillingene for reduksjonsnøkler for og resultatene av hver.</span><span class="sxs-lookup"><span data-stu-id="e67c7-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="e67c7-108">Du kan bruke en reduksjonsnøkkel til å definere hvordan du kan redusere prognosebehov.</span><span class="sxs-lookup"><span data-stu-id="e67c7-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="e67c7-109">Eksempel 1: Prosent - reduksjonsprinsipp for reduksjonsnøkkelprognose</span><span class="sxs-lookup"><span data-stu-id="e67c7-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="e67c7-110">Dette eksemplet viser hvordan en reduksjonsnøkkel reduserer behovene i behovsprognosen i henhold til prosentene og tidsperiodene som er definert av reduksjonsnøkkelen.</span><span class="sxs-lookup"><span data-stu-id="e67c7-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="e67c7-111">På siden **Reduksjonsnøkler** definerer du følgende linjer.</span><span class="sxs-lookup"><span data-stu-id="e67c7-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="e67c7-112">Vekslepenger</span><span class="sxs-lookup"><span data-stu-id="e67c7-112">Change</span></span> | <span data-ttu-id="e67c7-113">Enhet</span><span class="sxs-lookup"><span data-stu-id="e67c7-113">Unit</span></span>  | <span data-ttu-id="e67c7-114">Prosent</span><span class="sxs-lookup"><span data-stu-id="e67c7-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="e67c7-115">1</span><span class="sxs-lookup"><span data-stu-id="e67c7-115">1</span></span>    | <span data-ttu-id="e67c7-116">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-116">Month</span></span> |   <span data-ttu-id="e67c7-117">100</span><span class="sxs-lookup"><span data-stu-id="e67c7-117">100</span></span>   |
   |   <span data-ttu-id="e67c7-118">2</span><span class="sxs-lookup"><span data-stu-id="e67c7-118">2</span></span>    | <span data-ttu-id="e67c7-119">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-119">Month</span></span> |   <span data-ttu-id="e67c7-120">75</span><span class="sxs-lookup"><span data-stu-id="e67c7-120">75</span></span>    |
   |   <span data-ttu-id="e67c7-121">3</span><span class="sxs-lookup"><span data-stu-id="e67c7-121">3</span></span>    | <span data-ttu-id="e67c7-122">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-122">Month</span></span> |   <span data-ttu-id="e67c7-123">50</span><span class="sxs-lookup"><span data-stu-id="e67c7-123">50</span></span>    |
   |   <span data-ttu-id="e67c7-124">4</span><span class="sxs-lookup"><span data-stu-id="e67c7-124">4</span></span>    | <span data-ttu-id="e67c7-125">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-125">Month</span></span> |   <span data-ttu-id="e67c7-126">25</span><span class="sxs-lookup"><span data-stu-id="e67c7-126">25</span></span>    |


2. <span data-ttu-id="e67c7-127">Koble reduksjonsnøkkelen til varens dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e67c7-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="e67c7-128">På **Hovedplaner**-siden, i **Reduksjonsprinsipp**-feltet, velger du **Prosent - reduksjonsnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="e67c7-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="e67c7-129">Opprett en behovsprognose på 1 000 stykker per måned.</span><span class="sxs-lookup"><span data-stu-id="e67c7-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="e67c7-130">Hvis du kjører prognoseplanlegging 1. januar, forbrukes behovene i behovsprognosen i henhold til prosentene du definerer på **Reduksjonsnøkler**-siden.</span><span class="sxs-lookup"><span data-stu-id="e67c7-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="e67c7-131">Følgende behovsantall overføres til hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="e67c7-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="e67c7-132">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-132">Month</span></span>                | <span data-ttu-id="e67c7-133">Antall stykker som kreves</span><span class="sxs-lookup"><span data-stu-id="e67c7-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="e67c7-134">Januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-134">January</span></span>              | <span data-ttu-id="e67c7-135">0</span><span class="sxs-lookup"><span data-stu-id="e67c7-135">0</span></span>                         |
| <span data-ttu-id="e67c7-136">Februar</span><span class="sxs-lookup"><span data-stu-id="e67c7-136">February</span></span>             | <span data-ttu-id="e67c7-137">250</span><span class="sxs-lookup"><span data-stu-id="e67c7-137">250</span></span>                       |
| <span data-ttu-id="e67c7-138">Mars</span><span class="sxs-lookup"><span data-stu-id="e67c7-138">March</span></span>                | <span data-ttu-id="e67c7-139">500</span><span class="sxs-lookup"><span data-stu-id="e67c7-139">500</span></span>                       |
| <span data-ttu-id="e67c7-140">April</span><span class="sxs-lookup"><span data-stu-id="e67c7-140">April</span></span>                | <span data-ttu-id="e67c7-141">750</span><span class="sxs-lookup"><span data-stu-id="e67c7-141">750</span></span>                       |
| <span data-ttu-id="e67c7-142">Mai til desember</span><span class="sxs-lookup"><span data-stu-id="e67c7-142">May through December</span></span> | <span data-ttu-id="e67c7-143">1 000</span><span class="sxs-lookup"><span data-stu-id="e67c7-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="e67c7-144">Eksempel 2: Transaksjoner - reduksjonsprinsipp for reduksjonsnøkkelprognose</span><span class="sxs-lookup"><span data-stu-id="e67c7-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="e67c7-145">Dette eksemplet viser hvordan faktiske ordrer som skjer i periodene som er definert av reduksjonsnøkkelen, reduserer behovene i behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="e67c7-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="e67c7-146">På **Hovedplaner**-siden, i **Reduksjonsprinsipp**-feltet, velger du **Transaksjoner - reduksjonsnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="e67c7-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="e67c7-147">Følgende salgsordrer finnes den 1. januar.</span><span class="sxs-lookup"><span data-stu-id="e67c7-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="e67c7-148">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-148">Month</span></span>    | <span data-ttu-id="e67c7-149">Antall stykker som er bestilt</span><span class="sxs-lookup"><span data-stu-id="e67c7-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="e67c7-150">Januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-150">January</span></span>  | <span data-ttu-id="e67c7-151">956</span><span class="sxs-lookup"><span data-stu-id="e67c7-151">956</span></span>                      |
| <span data-ttu-id="e67c7-152">Februar</span><span class="sxs-lookup"><span data-stu-id="e67c7-152">February</span></span> | <span data-ttu-id="e67c7-153">1,176</span><span class="sxs-lookup"><span data-stu-id="e67c7-153">1,176</span></span>                    |
| <span data-ttu-id="e67c7-154">Mars</span><span class="sxs-lookup"><span data-stu-id="e67c7-154">March</span></span>    | <span data-ttu-id="e67c7-155">451</span><span class="sxs-lookup"><span data-stu-id="e67c7-155">451</span></span>                      |
| <span data-ttu-id="e67c7-156">April</span><span class="sxs-lookup"><span data-stu-id="e67c7-156">April</span></span>    | <span data-ttu-id="e67c7-157">119</span><span class="sxs-lookup"><span data-stu-id="e67c7-157">119</span></span>                      |

<span data-ttu-id="e67c7-158">Hvis du bruker den samme behovsprognosen på 1 000 stykker per måned, overføres følgende behovsantall til hovedplanen:</span><span class="sxs-lookup"><span data-stu-id="e67c7-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="e67c7-159">Måned</span><span class="sxs-lookup"><span data-stu-id="e67c7-159">Month</span></span>                | <span data-ttu-id="e67c7-160">Antall stykker som kreves</span><span class="sxs-lookup"><span data-stu-id="e67c7-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="e67c7-161">Januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-161">January</span></span>              | <span data-ttu-id="e67c7-162">44</span><span class="sxs-lookup"><span data-stu-id="e67c7-162">44</span></span>                        |
| <span data-ttu-id="e67c7-163">Februar</span><span class="sxs-lookup"><span data-stu-id="e67c7-163">February</span></span>             | <span data-ttu-id="e67c7-164">0</span><span class="sxs-lookup"><span data-stu-id="e67c7-164">0</span></span>                         |
| <span data-ttu-id="e67c7-165">Mars</span><span class="sxs-lookup"><span data-stu-id="e67c7-165">March</span></span>                | <span data-ttu-id="e67c7-166">549</span><span class="sxs-lookup"><span data-stu-id="e67c7-166">549</span></span>                       |
| <span data-ttu-id="e67c7-167">April</span><span class="sxs-lookup"><span data-stu-id="e67c7-167">April</span></span>                | <span data-ttu-id="e67c7-168">881</span><span class="sxs-lookup"><span data-stu-id="e67c7-168">881</span></span>                       |
| <span data-ttu-id="e67c7-169">Mai til desember</span><span class="sxs-lookup"><span data-stu-id="e67c7-169">May through December</span></span> | <span data-ttu-id="e67c7-170">1 000</span><span class="sxs-lookup"><span data-stu-id="e67c7-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="e67c7-171">Eksempel 3: Transaksjoner - reduksjonsprinsipp for dynamisk periodeprognose</span><span class="sxs-lookup"><span data-stu-id="e67c7-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="e67c7-172">I de fleste tilfeller er systemer er satt opp slik at transaksjoner reduserer behovsprognose i bestemte perioder for prognose: uker, måneder og så videre.</span><span class="sxs-lookup"><span data-stu-id="e67c7-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="e67c7-173">Disse er definert i reduksjonsnøkkelen.</span><span class="sxs-lookup"><span data-stu-id="e67c7-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="e67c7-174">Tiden mellom to behovsprognoselinjer kan imidlertid også *angi* en periode.</span><span class="sxs-lookup"><span data-stu-id="e67c7-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="e67c7-175">Opprett en behovsprognose for følgende datoer og antall.</span><span class="sxs-lookup"><span data-stu-id="e67c7-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="e67c7-176">Dato</span><span class="sxs-lookup"><span data-stu-id="e67c7-176">Date</span></span>       | <span data-ttu-id="e67c7-177">Behovsprognose</span><span class="sxs-lookup"><span data-stu-id="e67c7-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="e67c7-178">1. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-178">January 1</span></span>  | <span data-ttu-id="e67c7-179">1 000</span><span class="sxs-lookup"><span data-stu-id="e67c7-179">1,000</span></span>           |
   | <span data-ttu-id="e67c7-180">5. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-180">January 5</span></span>  | <span data-ttu-id="e67c7-181">500</span><span class="sxs-lookup"><span data-stu-id="e67c7-181">500</span></span>             |
   | <span data-ttu-id="e67c7-182">12. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-182">January 12</span></span> | <span data-ttu-id="e67c7-183">1 000</span><span class="sxs-lookup"><span data-stu-id="e67c7-183">1,000</span></span>           |

   <span data-ttu-id="e67c7-184">I denne prognosen er det ikke en ledig periode mellom prognosedatoene: det finnes en periode på fire dager mellom første og andre dato, og det er et tidsintervall på sju dager mellom andre og tredje dato.</span><span class="sxs-lookup"><span data-stu-id="e67c7-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="e67c7-185">Disse ulike intervallene er dynamiske perioder.</span><span class="sxs-lookup"><span data-stu-id="e67c7-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="e67c7-186">Opprett salgsordrelinjer på følgende måte.</span><span class="sxs-lookup"><span data-stu-id="e67c7-186">Create sales order lines as follows.</span></span>

   | <span data-ttu-id="e67c7-187">Dato</span><span class="sxs-lookup"><span data-stu-id="e67c7-187">Date</span></span>                             | <span data-ttu-id="e67c7-188">Salgsordreantall</span><span class="sxs-lookup"><span data-stu-id="e67c7-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="e67c7-189">15. desember i fjor</span><span class="sxs-lookup"><span data-stu-id="e67c7-189">December 15 in the previous year</span></span> | <span data-ttu-id="e67c7-190">500</span><span class="sxs-lookup"><span data-stu-id="e67c7-190">500</span></span>                  |
   | <span data-ttu-id="e67c7-191">3. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-191">January 3</span></span>                        | <span data-ttu-id="e67c7-192">100</span><span class="sxs-lookup"><span data-stu-id="e67c7-192">100</span></span>                  |
   | <span data-ttu-id="e67c7-193">10. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-193">January 10</span></span>                       | <span data-ttu-id="e67c7-194">200</span><span class="sxs-lookup"><span data-stu-id="e67c7-194">200</span></span>                  |

<span data-ttu-id="e67c7-195">Prognosen reduseres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="e67c7-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="e67c7-196">Den første salgsordren er ikke innenfor noen perioden, så den vil ikke redusere noen prognoser.</span><span class="sxs-lookup"><span data-stu-id="e67c7-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="e67c7-197">Den andre salgsordren er mellom 1. og 5. januar, så den vil redusere prognosen for 1. januar med 100.</span><span class="sxs-lookup"><span data-stu-id="e67c7-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="e67c7-198">Den tredje salgsordren er mellom 5. og 12. januar, så den vil redusere prognosen for 5. januar med 200.</span><span class="sxs-lookup"><span data-stu-id="e67c7-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="e67c7-199">Følgende planlagte ordre opprettes for å oppfylle prognosen.</span><span class="sxs-lookup"><span data-stu-id="e67c7-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="e67c7-200">Behovsprognosedato</span><span class="sxs-lookup"><span data-stu-id="e67c7-200">Demand forecast date</span></span> | <span data-ttu-id="e67c7-201">Redusert antall</span><span class="sxs-lookup"><span data-stu-id="e67c7-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="e67c7-202">1. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-202">January 1</span></span>            | <span data-ttu-id="e67c7-203">900</span><span class="sxs-lookup"><span data-stu-id="e67c7-203">900</span></span>              |
| <span data-ttu-id="e67c7-204">5. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-204">January 5</span></span>            | <span data-ttu-id="e67c7-205">300</span><span class="sxs-lookup"><span data-stu-id="e67c7-205">300</span></span>              |
| <span data-ttu-id="e67c7-206">12. januar</span><span class="sxs-lookup"><span data-stu-id="e67c7-206">January 12</span></span>           | <span data-ttu-id="e67c7-207">1 000</span><span class="sxs-lookup"><span data-stu-id="e67c7-207">1,000</span></span>            |

<span data-ttu-id="e67c7-208">Her er et sammendrag av reduksjonen **Transaksjoner - dynamisk periode**:</span><span class="sxs-lookup"><span data-stu-id="e67c7-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="e67c7-209">Prognosebehov reduseres med de faktiske ordretransaksjonene som forekommer i løpet av en dynamiske perioden.</span><span class="sxs-lookup"><span data-stu-id="e67c7-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="e67c7-210">Den dynamiske perioden dekker gjeldende prognosedatoer og slutter ved starten av neste prognose.</span><span class="sxs-lookup"><span data-stu-id="e67c7-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="e67c7-211">Denne metoden bruker eller krever ikke en reduksjonsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="e67c7-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="e67c7-212">Når dette alternativet brukes, skjer følgende:</span><span class="sxs-lookup"><span data-stu-id="e67c7-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="e67c7-213">Hvis prognosen reduseres fullstendig, blir behovene i prognosen for nåværende prognose 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e67c7-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="e67c7-214">Hvis det ikke er noen fremtidig prognose, reduseres behovene i prognosen fra den siste prognosen som ble angitt.</span><span class="sxs-lookup"><span data-stu-id="e67c7-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="e67c7-215">Horisonter er inkludert i beregningen av prognosereduksjon.</span><span class="sxs-lookup"><span data-stu-id="e67c7-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="e67c7-216">Positive dager er inkludert i beregningen av prognosereduksjon.</span><span class="sxs-lookup"><span data-stu-id="e67c7-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="e67c7-217">Hvis faktiske ordretransaksjoner overskrider de prognoseberegnede kravene, videresendes ikke de gjenværende transaksjonene til neste prognoseperiode.</span><span class="sxs-lookup"><span data-stu-id="e67c7-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e67c7-218">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e67c7-218">Additional resources</span></span>
--------

[<span data-ttu-id="e67c7-219">Hovedplaner</span><span class="sxs-lookup"><span data-stu-id="e67c7-219">Master plans</span></span>](master-plans.md)



