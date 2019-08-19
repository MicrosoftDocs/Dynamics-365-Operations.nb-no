---
title: 125 prosent redusert saldoavskrivning
description: Denne artikkelen gir en oversikt over avskrivningsmetoden 125 prosent saldoavskrivning.
author: saraschi2
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5af050fb6099b583be4e9c60ba56dacf38d31c08
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840871"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="b3296-103">125 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="b3296-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3296-104">Denne artikkelen gir en oversikt over avskrivningsmetoden 125 prosent saldoavskrivning.</span><span class="sxs-lookup"><span data-stu-id="b3296-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="b3296-105">Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **125 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt til avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="b3296-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="b3296-106">Denne prosenten beregnes på grunnlag av anleggsmidlets levetid.</span><span class="sxs-lookup"><span data-stu-id="b3296-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="b3296-107">Hvis anleggsmidlet for eksempel har en levetid på fem år, beregnes prosenten som 25 prosent (125 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="b3296-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="b3296-108">Hvis du vil definere 125 % saldoverdiavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="b3296-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="b3296-109">Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b3296-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b3296-110">Velge et avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="b3296-110">Select a depreciation year</span></span>
<span data-ttu-id="b3296-111">Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="b3296-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="b3296-112">Standardverdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="b3296-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="b3296-113">Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b3296-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="b3296-114">Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="b3296-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="b3296-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="b3296-115">Calendar</span></span>

<span data-ttu-id="b3296-116">Du kan beholde standardverdien i **Avskrivningsår**-feltet, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="b3296-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="b3296-117">**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="b3296-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="b3296-118">Avskrivningsgrunnlaget er vanligvis netto bokført verdi minus svinnverdien.</span><span class="sxs-lookup"><span data-stu-id="b3296-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="b3296-119">I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="b3296-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b3296-120">Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="b3296-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="b3296-121">**Årlig** posterer et beløp 31. desember.</span><span class="sxs-lookup"><span data-stu-id="b3296-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="b3296-122">**Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="b3296-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b3296-123">**Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="b3296-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b3296-124">**Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderhalvår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="b3296-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b3296-125">**Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="b3296-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b3296-126">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="b3296-126">Fiscal</span></span>

<span data-ttu-id="b3296-127">Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 125 % saldoverdiavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden.</span><span class="sxs-lookup"><span data-stu-id="b3296-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="b3296-128">Regnskapskalendere defineres på **Regnskapskalendere**-siden.</span><span class="sxs-lookup"><span data-stu-id="b3296-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="b3296-129">For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli.</span><span class="sxs-lookup"><span data-stu-id="b3296-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b3296-130">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="b3296-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b3296-131">Avskrivningen justeres automatisk for hver periode, og lengden på det neste regnskapsåret fastslås ved oppsettet av perioder på den siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="b3296-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="b3296-132">Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="b3296-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="b3296-133">**Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="b3296-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b3296-134">**Regnskapsperiode** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="b3296-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="b3296-135">Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="b3296-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="b3296-136">Eksempel på 125 % saldoverdiavskrivning</span><span class="sxs-lookup"><span data-stu-id="b3296-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="b3296-137">Anskaffelseskostnad</span><span class="sxs-lookup"><span data-stu-id="b3296-137">Acquisition cost</span></span>               | <span data-ttu-id="b3296-138">11 000</span><span class="sxs-lookup"><span data-stu-id="b3296-138">11,000</span></span> |
| <span data-ttu-id="b3296-139">Restverdi</span><span class="sxs-lookup"><span data-stu-id="b3296-139">Salvage value</span></span>                  | <span data-ttu-id="b3296-140">1 000</span><span class="sxs-lookup"><span data-stu-id="b3296-140">1,000</span></span>  |
| <span data-ttu-id="b3296-141">Avskrivningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="b3296-141">Depreciation base</span></span>              | <span data-ttu-id="b3296-142">10 000</span><span class="sxs-lookup"><span data-stu-id="b3296-142">10,000</span></span> |
| <span data-ttu-id="b3296-143">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="b3296-143">Service life years</span></span>             | <span data-ttu-id="b3296-144">5</span><span class="sxs-lookup"><span data-stu-id="b3296-144">5</span></span>      |
| <span data-ttu-id="b3296-145">Årlig avskrivningsprosent</span><span class="sxs-lookup"><span data-stu-id="b3296-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="b3296-146">25 %</span><span class="sxs-lookup"><span data-stu-id="b3296-146">25%</span></span>    |

<span data-ttu-id="b3296-147">Metoden 125 % saldoavskrivning dividerer 125 prosent med antall levetidsår.</span><span class="sxs-lookup"><span data-stu-id="b3296-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="b3296-148">Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.</span><span class="sxs-lookup"><span data-stu-id="b3296-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="b3296-149">Periode</span><span class="sxs-lookup"><span data-stu-id="b3296-149">Period</span></span> | <span data-ttu-id="b3296-150">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="b3296-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="b3296-151">Bokført verdi</span><span class="sxs-lookup"><span data-stu-id="b3296-151">Book value</span></span>                    | <span data-ttu-id="b3296-152">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="b3296-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="b3296-153">År 1</span><span class="sxs-lookup"><span data-stu-id="b3296-153">Year 1</span></span> | <span data-ttu-id="b3296-154">(11 000 – 1 000) × 25 % = 2 500</span><span class="sxs-lookup"><span data-stu-id="b3296-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="b3296-155">(11 000 – 2 500) = 8 500</span><span class="sxs-lookup"><span data-stu-id="b3296-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="b3296-156">(11 000 – 1 000 – 2 500) = 7 500</span><span class="sxs-lookup"><span data-stu-id="b3296-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="b3296-157">År 2</span><span class="sxs-lookup"><span data-stu-id="b3296-157">Year 2</span></span> | <span data-ttu-id="b3296-158">7 500 × 25 % = 1 875</span><span class="sxs-lookup"><span data-stu-id="b3296-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="b3296-159">(8 500 – 1 875) = 6 625</span><span class="sxs-lookup"><span data-stu-id="b3296-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="b3296-160">(7 500 – 1 875) = 5 625</span><span class="sxs-lookup"><span data-stu-id="b3296-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="b3296-161">År 3</span><span class="sxs-lookup"><span data-stu-id="b3296-161">Year 3</span></span> | <span data-ttu-id="b3296-162">5 625 × 25 % = 1 406,25</span><span class="sxs-lookup"><span data-stu-id="b3296-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="b3296-163">(6 625 – 1 406,25) = 5 218.75</span><span class="sxs-lookup"><span data-stu-id="b3296-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="b3296-164">(5 625 – 1 406,25) = 4 218,75</span><span class="sxs-lookup"><span data-stu-id="b3296-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="b3296-165">Vanligvis når beløpet som beregnes ved å bruke 125% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.</span><span class="sxs-lookup"><span data-stu-id="b3296-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



