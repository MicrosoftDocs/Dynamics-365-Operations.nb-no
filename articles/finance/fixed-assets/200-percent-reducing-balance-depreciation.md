---
title: 200 prosent redusert saldoavskrivning
description: Denne artikkelen gir en oversikt over avskrivningsmetoden 200 prosent saldoavskrivning.
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
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b761a14f44be292e9dd21eb580473bd0981d9044
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230328"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="91de5-103">200 prosent redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="91de5-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91de5-104">Denne artikkelen gir en oversikt over avskrivningsmetoden 200 prosent saldoavskrivning.</span><span class="sxs-lookup"><span data-stu-id="91de5-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="91de5-105">Når du definerer en avskrivningsprofil for anleggsmiddel og velger verdien **200 % saldoverdi** i **Metode**-feltet på **Avskrivningsprofiler**-siden, avskrives anleggsmidler som er tildelt avskrivningsprofilen, med den samme prosenten i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="91de5-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="91de5-106">Prosenten beregnes på grunnlag av anleggsmidlets levetid.</span><span class="sxs-lookup"><span data-stu-id="91de5-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="91de5-107">Hvis anleggsmidlet for eksempel har en levetid på fem år, beregnes prosenten som 40 prosent (200 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="91de5-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="91de5-108">Denne metoden kalles også dobbel degressiv avskrivning.</span><span class="sxs-lookup"><span data-stu-id="91de5-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="91de5-109">Hvis du vil definere 200 % saldoverdiavskrivning, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="91de5-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="91de5-110">Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som du velger i **Avskrivningsår**-feltet.</span><span class="sxs-lookup"><span data-stu-id="91de5-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="91de5-111">Velge et avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="91de5-111">Select a depreciation year</span></span>
<span data-ttu-id="91de5-112">Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="91de5-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="91de5-113">Standardverdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="91de5-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="91de5-114">Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet.</span><span class="sxs-lookup"><span data-stu-id="91de5-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="91de5-115">Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="91de5-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="91de5-116">Kalender</span><span class="sxs-lookup"><span data-stu-id="91de5-116">Calendar</span></span>

<span data-ttu-id="91de5-117">Du kan beholde standardverdien i **Avskrivningsår**-feltet, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="91de5-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="91de5-118">**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="91de5-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="91de5-119">Avskrivningen er vanligvis netto bokført verdi minus svinnverdien.</span><span class="sxs-lookup"><span data-stu-id="91de5-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="91de5-120">I eksemplene senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="91de5-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="91de5-121">Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="91de5-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="91de5-122">**Årlig** posterer et beløp 31. desember.</span><span class="sxs-lookup"><span data-stu-id="91de5-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="91de5-123">**Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="91de5-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="91de5-124">**Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="91de5-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="91de5-125">**Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderhalvår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="91de5-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="91de5-126">**Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="91de5-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="91de5-127">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="91de5-127">Fiscal</span></span>

<span data-ttu-id="91de5-128">Hvis du velger **Skattemessig** i feltet **Avskrivningsår**, beregnes 200 % saldoavskrivning basert på regnskapsåret for den økonomiske kalenderen som er angitt for tablået, eller for den økonomiske kalenderen som er valgt på **Finans**-siden.</span><span class="sxs-lookup"><span data-stu-id="91de5-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="91de5-129">Regnskapskalendere defineres på **Regnskapskalendere**-siden.</span><span class="sxs-lookup"><span data-stu-id="91de5-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="91de5-130">For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen den 1. juli.</span><span class="sxs-lookup"><span data-stu-id="91de5-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="91de5-131">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="91de5-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="91de5-132">Avskrivningen justeres for hver periode.</span><span class="sxs-lookup"><span data-stu-id="91de5-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="91de5-133">Lengden på det neste regnskapsåret fastsettes av definisjonen av periodene på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="91de5-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="91de5-134">Når **Skattemessig** er valgt som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**- feltet:</span><span class="sxs-lookup"><span data-stu-id="91de5-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="91de5-135">**Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="91de5-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="91de5-136">**Regnskapsperiode** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="91de5-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="91de5-137">Dette beløpet avsettes i regnskapsperiodene som defineres på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="91de5-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="91de5-138">Eksempel på 200 % saldoverdiavskrivning</span><span class="sxs-lookup"><span data-stu-id="91de5-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="91de5-139">Anskaffelseskostnad</span><span class="sxs-lookup"><span data-stu-id="91de5-139">Acquisition cost</span></span>               | <span data-ttu-id="91de5-140">11 000</span><span class="sxs-lookup"><span data-stu-id="91de5-140">11,000</span></span> |
| <span data-ttu-id="91de5-141">Restverdi</span><span class="sxs-lookup"><span data-stu-id="91de5-141">Salvage value</span></span>                  | <span data-ttu-id="91de5-142">1 000</span><span class="sxs-lookup"><span data-stu-id="91de5-142">1, 000</span></span> |
| <span data-ttu-id="91de5-143">Avskrivningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="91de5-143">Depreciation base</span></span>              | <span data-ttu-id="91de5-144">10 000</span><span class="sxs-lookup"><span data-stu-id="91de5-144">10,000</span></span> |
| <span data-ttu-id="91de5-145">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="91de5-145">Service life years</span></span>             | <span data-ttu-id="91de5-146">5</span><span class="sxs-lookup"><span data-stu-id="91de5-146">5</span></span>      |
| <span data-ttu-id="91de5-147">Årlig avskrivningsprosent</span><span class="sxs-lookup"><span data-stu-id="91de5-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="91de5-148">40 %</span><span class="sxs-lookup"><span data-stu-id="91de5-148">40%</span></span>    |

<span data-ttu-id="91de5-149">Metoden 200 % redusert saldo dividerer 200 prosent med antall levetidsår.</span><span class="sxs-lookup"><span data-stu-id="91de5-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="91de5-150">Avskrivningsbeløpet for året beregnes ved å multiplisere denne prosentandelen med anleggsmiddelets netto bokført verdi.</span><span class="sxs-lookup"><span data-stu-id="91de5-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="91de5-151">Periode</span><span class="sxs-lookup"><span data-stu-id="91de5-151">Period</span></span> | <span data-ttu-id="91de5-152">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="91de5-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="91de5-153">Bokført verdi</span><span class="sxs-lookup"><span data-stu-id="91de5-153">Book value</span></span>             | <span data-ttu-id="91de5-154">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="91de5-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="91de5-155">År 1</span><span class="sxs-lookup"><span data-stu-id="91de5-155">Year 1</span></span> | <span data-ttu-id="91de5-156">(11 000 – 1 000) × 40 % = 4 000</span><span class="sxs-lookup"><span data-stu-id="91de5-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="91de5-157">11 000 – 4 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="91de5-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="91de5-158">11 000 – 1 000 – 4 000 = 6 000</span><span class="sxs-lookup"><span data-stu-id="91de5-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="91de5-159">År 2</span><span class="sxs-lookup"><span data-stu-id="91de5-159">Year 2</span></span> | <span data-ttu-id="91de5-160">6 000 × 40 % = 2 400</span><span class="sxs-lookup"><span data-stu-id="91de5-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="91de5-161">7 000 – 2 400 = 4 600</span><span class="sxs-lookup"><span data-stu-id="91de5-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="91de5-162">6 000 – 2 400 = 3 600</span><span class="sxs-lookup"><span data-stu-id="91de5-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="91de5-163">År 3</span><span class="sxs-lookup"><span data-stu-id="91de5-163">Year 3</span></span> | <span data-ttu-id="91de5-164">3 600 × 40 % = 1 440</span><span class="sxs-lookup"><span data-stu-id="91de5-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="91de5-165">4 600 – 1 440 = 3 160</span><span class="sxs-lookup"><span data-stu-id="91de5-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="91de5-166">3 600 – 1 440 = 2 160</span><span class="sxs-lookup"><span data-stu-id="91de5-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="91de5-167">Vanligvis når beløpet som beregnes ved å bruke 200% saldoavskrivningsmetode, blir mindre enn beløpet som ville blitt beregnet ved hjelp av den lineære metoden, går man over til lineær avskrivning resten av levetiden.</span><span class="sxs-lookup"><span data-stu-id="91de5-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]