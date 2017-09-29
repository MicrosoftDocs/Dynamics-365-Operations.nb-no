---
title: "Lineær levetidsavskrivning"
description: "Denne artikkelen gir en oversikt over avskrivningsmetoden lineær levetid."
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2b8c078841ca2e4bd994bbfbbe2abb130a4cf6fa
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="efa41-103">Lineær levetidsavskrivning</span><span class="sxs-lookup"><span data-stu-id="efa41-103">Straight line service life depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="efa41-104">Denne artikkelen gir en oversikt over avskrivningsmetoden lineær levetid.</span><span class="sxs-lookup"><span data-stu-id="efa41-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="efa41-105">Når du definerer en avskrivningsprofil for anleggsmidler og velger Lineær levetid i feltet Metode på siden Avskrivningsprofiler, avskrives anleggsmidlene som har denne avskrivningsprofilen basert på den samlede levetiden til anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="efa41-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="efa41-106">Dette er vanligvis det samme avskrivningsbeløpet i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="efa41-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="efa41-107">Forskjellen i avskrivningsbeløpet som beregnes mellom gjenværende lineær levetid og lineær levetid, er hvis det er en justering postert til anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="efa41-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="efa41-108">Hvis du vil definere lineær levetidsavskrivning, må du også velge alternativer i feltet Avskrivningsår og feltet Periodefrekvens på siden Avskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="efa41-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="efa41-109">Velge et avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="efa41-109">Select a depreciation year</span></span>
<span data-ttu-id="efa41-110">Du kan velge enten Kalender eller Regnskapsår i Avskrivningsår-feltet på siden Avskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="efa41-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="efa41-111">Valget definerer alternativene som er tilgjengelige i Periodefrekvens-feltet.</span><span class="sxs-lookup"><span data-stu-id="efa41-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="efa41-112">Standardvalget er Kalender.</span><span class="sxs-lookup"><span data-stu-id="efa41-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="efa41-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="efa41-113">Calendar</span></span>

<span data-ttu-id="efa41-114">Hvis du velger Kalender, antas det at året er 1. januar til 31.desember, selv om du har definert den økonomiske kalenderen på en annen måte.</span><span class="sxs-lookup"><span data-stu-id="efa41-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="efa41-115">Alternativet Kalender oppdaterer avskrivningsgrunnlaget, som vanligvis er netto bokført verdi minus restverdi, 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="efa41-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="efa41-116">I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="efa41-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="efa41-117">Hvis du velger Kalender, er følgende alternativer tilgjengelige i Periodefrekvens-feltet, som definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom hele kalenderåret:</span><span class="sxs-lookup"><span data-stu-id="efa41-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="efa41-118">Årlig posterer et beløp 31. desember.</span><span class="sxs-lookup"><span data-stu-id="efa41-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="efa41-119">Månedlige posteringer av et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="efa41-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="efa41-120">Kvartalsvise posteringer av et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="efa41-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="efa41-121">Halvårlig posterer et halvårlig beløp på slutten av hvert kalenderår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="efa41-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="efa41-122">Daglige posteringer av avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="efa41-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="efa41-123">Hvis du velger for eksempel Årlig, posteres den årlige avskrivningen bare én gang, den 31. desember i hvert år.</span><span class="sxs-lookup"><span data-stu-id="efa41-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="efa41-124">Hvis du velger Månedlig, posteres den månedlige avskrivningen hver måned som en tolvdel av det årlige avskrivningsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="efa41-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="efa41-125">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="efa41-125">Fiscal</span></span>

<span data-ttu-id="efa41-126">Hvis du velger Skattemessig i feltet Avskrivningsår, brukes lineær levetidsavskrivning.</span><span class="sxs-lookup"><span data-stu-id="efa41-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="efa41-127">Det beregnes basert på regnskapsåret, som er definert av den økonomiske kalenderen som er angitt for tablået, eller av den økonomiske kalenderen som er valgt på Finans-siden.</span><span class="sxs-lookup"><span data-stu-id="efa41-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="efa41-128">Regnskapskalendere defineres på Regnskapskalendere-siden.</span><span class="sxs-lookup"><span data-stu-id="efa41-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="efa41-129">For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen 1. juli.</span><span class="sxs-lookup"><span data-stu-id="efa41-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="efa41-130">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="efa41-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="efa41-131">Avskrivningen justeres automatisk for hver regnskapsperiode.</span><span class="sxs-lookup"><span data-stu-id="efa41-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="efa41-132">Lengden på det neste regnskapsåret baseres på regnskapsperiodene som du definerer når du oppretter et nytt regnskapsår på skjemaet med regnskapskalendere.</span><span class="sxs-lookup"><span data-stu-id="efa41-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="efa41-133">Hvis du velger Regnskapsår, er følgende alternativer tilgjengelige i Periodefrekvens-feltet:</span><span class="sxs-lookup"><span data-stu-id="efa41-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="efa41-134">Årlig posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="efa41-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="efa41-135">Regnskapsperioder beregner totalbeløpet for avskrivningen for regnskapsåret, som avsettes i regnskapsperiodene som defineres i skjemaet for regnskapskalender for regnsapskalenderen.</span><span class="sxs-lookup"><span data-stu-id="efa41-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="efa41-136">Eksempel på lineær avskrivning for et uendret anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="efa41-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="efa41-137">Anta at anleggsmidlet har følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="efa41-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="efa41-138">Anskaffelseskostnad</span><span class="sxs-lookup"><span data-stu-id="efa41-138">Acquisition cost</span></span>    | <span data-ttu-id="efa41-139">11 000</span><span class="sxs-lookup"><span data-stu-id="efa41-139">11,000</span></span> |
| <span data-ttu-id="efa41-140">Restverdi</span><span class="sxs-lookup"><span data-stu-id="efa41-140">Salvage value</span></span>       | <span data-ttu-id="efa41-141">1 000</span><span class="sxs-lookup"><span data-stu-id="efa41-141">1,000</span></span>  |
| <span data-ttu-id="efa41-142">Avskrivningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="efa41-142">Depreciation base</span></span>   | <span data-ttu-id="efa41-143">10 000</span><span class="sxs-lookup"><span data-stu-id="efa41-143">10,000</span></span> |
| <span data-ttu-id="efa41-144">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="efa41-144">Service life years</span></span>  | <span data-ttu-id="efa41-145">5</span><span class="sxs-lookup"><span data-stu-id="efa41-145">5</span></span>      |
| <span data-ttu-id="efa41-146">Årlig avskrivning</span><span class="sxs-lookup"><span data-stu-id="efa41-146">Yearly depreciation</span></span> | <span data-ttu-id="efa41-147">2 000</span><span class="sxs-lookup"><span data-stu-id="efa41-147">2,000</span></span>  |

<span data-ttu-id="efa41-148">Du får samme avskrivningsbeløp hvert år.</span><span class="sxs-lookup"><span data-stu-id="efa41-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="efa41-149">(Anskaffelseskostnad - Restverdi) / Levetidsår</span><span class="sxs-lookup"><span data-stu-id="efa41-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="efa41-150">Periode</span><span class="sxs-lookup"><span data-stu-id="efa41-150">Period</span></span> | <span data-ttu-id="efa41-151">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="efa41-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="efa41-152">Netto bokført verdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="efa41-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="efa41-153">År 1</span><span class="sxs-lookup"><span data-stu-id="efa41-153">Year 1</span></span> | <span data-ttu-id="efa41-154">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="efa41-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="efa41-155">9 000</span><span class="sxs-lookup"><span data-stu-id="efa41-155">9,000</span></span>                                 |
| <span data-ttu-id="efa41-156">År 2</span><span class="sxs-lookup"><span data-stu-id="efa41-156">Year 2</span></span> | <span data-ttu-id="efa41-157">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="efa41-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="efa41-158">7 000</span><span class="sxs-lookup"><span data-stu-id="efa41-158">7,000</span></span>                                 |
| <span data-ttu-id="efa41-159">År 3</span><span class="sxs-lookup"><span data-stu-id="efa41-159">Year 3</span></span> | <span data-ttu-id="efa41-160">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="efa41-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="efa41-161">5 000</span><span class="sxs-lookup"><span data-stu-id="efa41-161">5,000</span></span>                                 |
| <span data-ttu-id="efa41-162">År 4</span><span class="sxs-lookup"><span data-stu-id="efa41-162">Year 4</span></span> | <span data-ttu-id="efa41-163">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="efa41-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="efa41-164">3 000</span><span class="sxs-lookup"><span data-stu-id="efa41-164">3,000</span></span>                                 |
| <span data-ttu-id="efa41-165">År 5</span><span class="sxs-lookup"><span data-stu-id="efa41-165">Year 5</span></span> | <span data-ttu-id="efa41-166">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="efa41-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="efa41-167">1 000</span><span class="sxs-lookup"><span data-stu-id="efa41-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="efa41-168">Eksempel på lineær avskrivning av et endret anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="efa41-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="efa41-169">Sett at du legger til en anskaffelsesjustering på 4 000 i år 2 for samme anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="efa41-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="efa41-170">Levetiden for anskaffelsesjusteringen er den samme som den til anleggsmidlet, og begynner på anskaffelsestidspunktet.</span><span class="sxs-lookup"><span data-stu-id="efa41-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="efa41-171">En netto bokført verdi gjenstår ved utgangen av år 5, som tilsvarer netto bokført verdi for anskaffelsesjusteringen.</span><span class="sxs-lookup"><span data-stu-id="efa41-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="efa41-172">Avskrivning etter periode blir beregnet som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="efa41-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="efa41-173">Periode</span><span class="sxs-lookup"><span data-stu-id="efa41-173">Period</span></span> | <span data-ttu-id="efa41-174">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="efa41-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="efa41-175">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="efa41-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="efa41-176">År 1</span><span class="sxs-lookup"><span data-stu-id="efa41-176">Year 1</span></span> | <span data-ttu-id="efa41-177">10,000 / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="efa41-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="efa41-178">11,000 - 2,000 = 9,000</span><span class="sxs-lookup"><span data-stu-id="efa41-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="efa41-179">År 2</span><span class="sxs-lookup"><span data-stu-id="efa41-179">Year 2</span></span> | <span data-ttu-id="efa41-180">4,000 (anskaffelsesjustering)</span><span class="sxs-lookup"><span data-stu-id="efa41-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="efa41-181">9,000 + 4,000 =13,000</span><span class="sxs-lookup"><span data-stu-id="efa41-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="efa41-182">År 2</span><span class="sxs-lookup"><span data-stu-id="efa41-182">Year 2</span></span> | <span data-ttu-id="efa41-183">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="efa41-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="efa41-184">13,000 - 2,800 = 10,200</span><span class="sxs-lookup"><span data-stu-id="efa41-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="efa41-185">År 3</span><span class="sxs-lookup"><span data-stu-id="efa41-185">Year 3</span></span> | <span data-ttu-id="efa41-186">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="efa41-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="efa41-187">10,200 - 2,800 = 7,400</span><span class="sxs-lookup"><span data-stu-id="efa41-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="efa41-188">År 4</span><span class="sxs-lookup"><span data-stu-id="efa41-188">Year 4</span></span> | <span data-ttu-id="efa41-189">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="efa41-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="efa41-190">7,400 - 2,800 = 4,600</span><span class="sxs-lookup"><span data-stu-id="efa41-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="efa41-191">År 5</span><span class="sxs-lookup"><span data-stu-id="efa41-191">Year 5</span></span> | <span data-ttu-id="efa41-192">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="efa41-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="efa41-193">4,600 - 2,800 = 1,800</span><span class="sxs-lookup"><span data-stu-id="efa41-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="efa41-194">År 6</span><span class="sxs-lookup"><span data-stu-id="efa41-194">Year 6</span></span> | <span data-ttu-id="efa41-195">Gjenværende 800*\*</span><span class="sxs-lookup"><span data-stu-id="efa41-195">Remaining 800\*</span></span>                           | <span data-ttu-id="efa41-196">1,800 – 800 = 1,000</span><span class="sxs-lookup"><span data-stu-id="efa41-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="efa41-197">\*Fordi gjenværende beløp er mindre en avskrivningsbeløpet, brukes bare gjenværende beløp minus enn restverdien.</span><span class="sxs-lookup"><span data-stu-id="efa41-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






