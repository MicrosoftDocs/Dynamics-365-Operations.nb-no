---
title: 150 prosent saldoavskrivning
description: Denne artikkelen gir en oversikt over avskrivningsmetoden 150 prosent saldoavskrivning.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 931c12278853d87e6fddbb166b56c6079d40b142
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="69ad1-103">150 prosent saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="69ad1-103">150 percent reducing balance depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="69ad1-104">Denne artikkelen gir en oversikt over avskrivningsmetoden 150 prosent saldoavskrivning.</span><span class="sxs-lookup"><span data-stu-id="69ad1-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="69ad1-105">Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **150 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="69ad1-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="69ad1-106">Denne prosenten beregnes på grunnlag av anleggsmidlets levetid.</span><span class="sxs-lookup"><span data-stu-id="69ad1-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="69ad1-107">Hvis anleggsmidlet for eksempel har en levetid på fem år, beregnes prosenten som 30 prosent (150 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="69ad1-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="69ad1-108">Hvis du vil definere 150 % saldoavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="69ad1-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="69ad1-109">Alternativene som er tilgjengelige i **Periodefrekvens**-feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69ad1-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="69ad1-110">Velge avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="69ad1-110">Selection of depreciation year</span></span>
<span data-ttu-id="69ad1-111">Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="69ad1-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="69ad1-112">Standardverdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="69ad1-112">The default value is **Calendar**.</span></span> <span data-ttu-id="69ad1-113">Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69ad1-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="69ad1-114">Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="69ad1-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="69ad1-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="69ad1-115">Calendar</span></span>

<span data-ttu-id="69ad1-116">Du kan beholde standardverdien i **Avskrivningsår**-feltet, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="69ad1-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="69ad1-117">**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="69ad1-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="69ad1-118">Avskrivningsgrunnlaget er vanligvis netto bokført verdi minus svinnverdien.</span><span class="sxs-lookup"><span data-stu-id="69ad1-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="69ad1-119">I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="69ad1-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="69ad1-120">Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="69ad1-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="69ad1-121">**Årlig** posterer et beløp 31. desember.</span><span class="sxs-lookup"><span data-stu-id="69ad1-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="69ad1-122">**Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="69ad1-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="69ad1-123">**Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="69ad1-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="69ad1-124">**Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderhalvår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="69ad1-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="69ad1-125">**Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="69ad1-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="69ad1-126">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="69ad1-126">Fiscal</span></span>

<span data-ttu-id="69ad1-127">Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 150 % saldoavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden.</span><span class="sxs-lookup"><span data-stu-id="69ad1-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="69ad1-128">Regnskapskalendere defineres på **Regnskapskalendere**-siden.</span><span class="sxs-lookup"><span data-stu-id="69ad1-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="69ad1-129">For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli.</span><span class="sxs-lookup"><span data-stu-id="69ad1-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="69ad1-130">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="69ad1-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="69ad1-131">Avskrivningen justeres for hver periode.</span><span class="sxs-lookup"><span data-stu-id="69ad1-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="69ad1-132">Lengden på det neste regnskapsåret fastsettes av definisjonen av periodene på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="69ad1-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="69ad1-133">Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="69ad1-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="69ad1-134">**Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="69ad1-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="69ad1-135">**Regnskapsperiode** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="69ad1-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="69ad1-136">Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="69ad1-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="69ad1-137">Eksempel på 150 % redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="69ad1-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="69ad1-138">Anskaffelseskostnad</span><span class="sxs-lookup"><span data-stu-id="69ad1-138">Acquisition cost</span></span>               | <span data-ttu-id="69ad1-139">11 000</span><span class="sxs-lookup"><span data-stu-id="69ad1-139">11,000</span></span> |
| <span data-ttu-id="69ad1-140">Restverdi</span><span class="sxs-lookup"><span data-stu-id="69ad1-140">Salvage value</span></span>                  | <span data-ttu-id="69ad1-141">1 000</span><span class="sxs-lookup"><span data-stu-id="69ad1-141">1,000</span></span>  |
| <span data-ttu-id="69ad1-142">Avskrivningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="69ad1-142">Depreciation base</span></span>              | <span data-ttu-id="69ad1-143">10 000</span><span class="sxs-lookup"><span data-stu-id="69ad1-143">10,000</span></span> |
| <span data-ttu-id="69ad1-144">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="69ad1-144">Service life years</span></span>             | <span data-ttu-id="69ad1-145">5</span><span class="sxs-lookup"><span data-stu-id="69ad1-145">5</span></span>      |
| <span data-ttu-id="69ad1-146">Årlig avskrivningsprosent</span><span class="sxs-lookup"><span data-stu-id="69ad1-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="69ad1-147">30 %</span><span class="sxs-lookup"><span data-stu-id="69ad1-147">30%</span></span>    |

<span data-ttu-id="69ad1-148">Metoden 150 % saldoavskrivning dividerer 150 prosent med antall levetidsår.</span><span class="sxs-lookup"><span data-stu-id="69ad1-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="69ad1-149">Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.</span><span class="sxs-lookup"><span data-stu-id="69ad1-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="69ad1-150">Periode</span><span class="sxs-lookup"><span data-stu-id="69ad1-150">Period</span></span> | <span data-ttu-id="69ad1-151">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="69ad1-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="69ad1-152">Bokført verdi</span><span class="sxs-lookup"><span data-stu-id="69ad1-152">Book value</span></span>             | <span data-ttu-id="69ad1-153">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="69ad1-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="69ad1-154">År 1</span><span class="sxs-lookup"><span data-stu-id="69ad1-154">Year 1</span></span> | <span data-ttu-id="69ad1-155">(11 000 – 1 000) × 30 % = 3 000</span><span class="sxs-lookup"><span data-stu-id="69ad1-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="69ad1-156">11 000 – 3 000 = 8 000</span><span class="sxs-lookup"><span data-stu-id="69ad1-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="69ad1-157">11 000 – 1 000 – 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="69ad1-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="69ad1-158">År 2</span><span class="sxs-lookup"><span data-stu-id="69ad1-158">Year 2</span></span> | <span data-ttu-id="69ad1-159">7 000 × 30 % = 2 100</span><span class="sxs-lookup"><span data-stu-id="69ad1-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="69ad1-160">8 000 – 2 100 = 5 900</span><span class="sxs-lookup"><span data-stu-id="69ad1-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="69ad1-161">7 000 – 2 100 = 4 900</span><span class="sxs-lookup"><span data-stu-id="69ad1-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="69ad1-162">År 3</span><span class="sxs-lookup"><span data-stu-id="69ad1-162">Year 3</span></span> | <span data-ttu-id="69ad1-163">4 900 × 30 % = 1 470</span><span class="sxs-lookup"><span data-stu-id="69ad1-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="69ad1-164">5 900 – 1 470 = 4 430</span><span class="sxs-lookup"><span data-stu-id="69ad1-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="69ad1-165">4 900 – 1 470 = 3 430</span><span class="sxs-lookup"><span data-stu-id="69ad1-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="69ad1-166">Vanligvis når beløpet som beregnes ved å bruke 150% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.</span><span class="sxs-lookup"><span data-stu-id="69ad1-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




