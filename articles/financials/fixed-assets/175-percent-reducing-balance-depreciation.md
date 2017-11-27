---
title: 175 % redusert saldoavskrivning
description: Dette emnet gir en oversikt over avskrivningsmetoden 175 prosent saldoavskrivning.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a61e743898e3e65c0012a7aeb9837e55e9143d01
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="ef2d3-103">175 % redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="ef2d3-103">175 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef2d3-104">Dette emnet gir en oversikt over avskrivningsmetoden 175 prosent saldoavskrivning.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="ef2d3-105">Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **175 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="ef2d3-106">Hvis du vil definere 175 % saldoavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ef2d3-107">Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="ef2d3-108">Velge et avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="ef2d3-108">Select a depreciation year</span></span>
<span data-ttu-id="ef2d3-109">Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ef2d3-110">Standardverdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="ef2d3-111">Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ef2d3-112">Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ef2d3-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="ef2d3-113">Calendar</span></span>

<span data-ttu-id="ef2d3-114">Du kan beholde standardverdien i **Avskrivningsår**-feltet, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="ef2d3-115">**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ef2d3-116">Avskrivningsgrunnlaget er vanligvis netto bokført verdi minus svinnverdien.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="ef2d3-117">I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="ef2d3-118">Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="ef2d3-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ef2d3-119">**Årlig** posterer et beløp 31. desember.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ef2d3-120">**Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ef2d3-121">**Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="ef2d3-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ef2d3-122">**Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderhalvår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="ef2d3-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ef2d3-123">**Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ef2d3-124">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="ef2d3-124">Fiscal</span></span>

<span data-ttu-id="ef2d3-125">Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 175 % saldoavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="ef2d3-126">Regnskapskalendere defineres på **Regnskapskalendere**-siden.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="ef2d3-127">Hvis du vil ha mer informasjon, se [Regnskapskalendere, regnskapsår og perioder](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="ef2d3-127">For more information, see [Fiscal calendars, fiscal years, and periods](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="ef2d3-128">For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ef2d3-129">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ef2d3-130">Avskrivningen justeres automatisk for hver periode, og lengden på det neste regnskapsåret fastslås ved oppsettet av perioder på den siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ef2d3-131">Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="ef2d3-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ef2d3-132">**Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ef2d3-133">**Regnskapsperiode** beregner totalbeløpet for avskrivningen for regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="ef2d3-134">Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="ef2d3-135">Eksempel på 175% redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="ef2d3-135">Example of 175% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="ef2d3-136">Anskaffelseskostnad</span><span class="sxs-lookup"><span data-stu-id="ef2d3-136">Acquisition cost</span></span>               | <span data-ttu-id="ef2d3-137">11 000</span><span class="sxs-lookup"><span data-stu-id="ef2d3-137">11,000</span></span> |
| <span data-ttu-id="ef2d3-138">Restverdi</span><span class="sxs-lookup"><span data-stu-id="ef2d3-138">Salvage value</span></span>                  | <span data-ttu-id="ef2d3-139">1 000</span><span class="sxs-lookup"><span data-stu-id="ef2d3-139">1,000</span></span>  |
| <span data-ttu-id="ef2d3-140">Avskrivningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="ef2d3-140">Depreciation base</span></span>              | <span data-ttu-id="ef2d3-141">10 000</span><span class="sxs-lookup"><span data-stu-id="ef2d3-141">10,000</span></span> |
| <span data-ttu-id="ef2d3-142">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="ef2d3-142">Service life years</span></span>             | <span data-ttu-id="ef2d3-143">5</span><span class="sxs-lookup"><span data-stu-id="ef2d3-143">5</span></span>      |
| <span data-ttu-id="ef2d3-144">Årlig avskrivningsprosent</span><span class="sxs-lookup"><span data-stu-id="ef2d3-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="ef2d3-145">35 %</span><span class="sxs-lookup"><span data-stu-id="ef2d3-145">35%</span></span>    |

<span data-ttu-id="ef2d3-146">Avskrivingsmetoden 175 % saldoavskrivning dividerer 175 prosent med antall levetidsår.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="ef2d3-147">Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="ef2d3-148">Periode</span><span class="sxs-lookup"><span data-stu-id="ef2d3-148">Period</span></span> | <span data-ttu-id="ef2d3-149">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="ef2d3-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ef2d3-150">Bokført verdi</span><span class="sxs-lookup"><span data-stu-id="ef2d3-150">Book value</span></span>                  | <span data-ttu-id="ef2d3-151">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="ef2d3-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="ef2d3-152">År 1</span><span class="sxs-lookup"><span data-stu-id="ef2d3-152">Year 1</span></span> | <span data-ttu-id="ef2d3-153">(11 000 - 1 000) × 35 % = 3 500</span><span class="sxs-lookup"><span data-stu-id="ef2d3-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="ef2d3-154">11 000 - 3 500 = 7 500</span><span class="sxs-lookup"><span data-stu-id="ef2d3-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="ef2d3-155">11 000 - 1 000 - 3 500 = 6 500</span><span class="sxs-lookup"><span data-stu-id="ef2d3-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="ef2d3-156">År 2</span><span class="sxs-lookup"><span data-stu-id="ef2d3-156">Year 2</span></span> | <span data-ttu-id="ef2d3-157">6 500 × 35 % = 2 275</span><span class="sxs-lookup"><span data-stu-id="ef2d3-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="ef2d3-158">7 500 - 2 275 = 5 225</span><span class="sxs-lookup"><span data-stu-id="ef2d3-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="ef2d3-159">6 500 - 2 275 = 4 225</span><span class="sxs-lookup"><span data-stu-id="ef2d3-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="ef2d3-160">År 3</span><span class="sxs-lookup"><span data-stu-id="ef2d3-160">Year 3</span></span> | <span data-ttu-id="ef2d3-161">4 225 × 35 % = 1 478,75</span><span class="sxs-lookup"><span data-stu-id="ef2d3-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="ef2d3-162">5 225 - 1 478,75 = 3 746,25</span><span class="sxs-lookup"><span data-stu-id="ef2d3-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="ef2d3-163">4 225 - 1 478,75 = 2 746,25</span><span class="sxs-lookup"><span data-stu-id="ef2d3-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="ef2d3-164">Vanligvis når beløpet som beregnes ved å bruke 175% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.</span><span class="sxs-lookup"><span data-stu-id="ef2d3-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




