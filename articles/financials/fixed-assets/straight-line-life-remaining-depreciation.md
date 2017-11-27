---
title: "Gjenstående lineær levetidsavskrivning"
description: "Denne artikkelen gir en oversikt over lineær levetid gjenværende metode for avskrivning."
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
ms.search.scope: Core, Operations
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ebca31727ecdaa2b94d4930174b2461845ab5578
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="474ff-103">Gjenstående lineær levetidsavskrivning</span><span class="sxs-lookup"><span data-stu-id="474ff-103">Straight line life remaining depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="474ff-104">Denne artikkelen gir en oversikt over lineær levetid gjenværende metode for avskrivning.</span><span class="sxs-lookup"><span data-stu-id="474ff-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="474ff-105">Når du definerer en avskrivningsprofil for anleggsmidler og velger **Lineær levetid som gjenstår** i feltet **Metode** på siden **Avskrivningsprofiler**, blir avskrivningen av anleggsmidler som er knyttet til avskrivningsprofilen, da basert på anleggsmiddelets gjenværende levetid.</span><span class="sxs-lookup"><span data-stu-id="474ff-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="474ff-106">Avskrivningsbeløpet er vanligvis det samme i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="474ff-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="474ff-107">Hvis du vil definere avskrivning for gjenværende lineær levetid, må du også velge alternativer i feltet **Avskrivningsår** og feltet **Periodefrekvens** på siden **Avskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="474ff-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="474ff-108">Alternativene som er tilgjengelige i feltet **Periodefrekvens** feltet varierer, avhengig av verdien som er valgt i **Avskrivningsår**-feltet.</span><span class="sxs-lookup"><span data-stu-id="474ff-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="474ff-109">Velge et avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="474ff-109">Select a depreciation year</span></span>
<span data-ttu-id="474ff-110">Du kan velge enten **Kalender** eller **Skattemessig** i **Avskrivningsår**-feltet på **Avskrivningsprofiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="474ff-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="474ff-111">Standardverdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="474ff-111">The default value is **Calendar**.</span></span> <span data-ttu-id="474ff-112">Valget ditt fastsetter alternativene som er tilgjengelige i **Periodefrekvens**-feltet.</span><span class="sxs-lookup"><span data-stu-id="474ff-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="474ff-113">Dette feltet definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="474ff-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="474ff-114">Kalender</span><span class="sxs-lookup"><span data-stu-id="474ff-114">Calendar</span></span>

<span data-ttu-id="474ff-115">Hvis du velger **Kalender** i feltet ***Avskrivningsår***, antas et år fra 1. januar til og med 31. desember, selv om du har definert regnskapskalenderen annerledes.</span><span class="sxs-lookup"><span data-stu-id="474ff-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="474ff-116">**Kalender**-alternativet oppdaterer avskrivningsgrunnlag 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="474ff-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="474ff-117">Avskrivningsgrunnlaget er vanligvis netto bokført verdi minus restverdien.</span><span class="sxs-lookup"><span data-stu-id="474ff-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="474ff-118">I eksemplet senere i dette emnet er avskrivningsgrunnlaget telleren i det første uttrykket i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="474ff-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="474ff-119">Hvis du velger **Kalender** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="474ff-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="474ff-120">**Årlig** posterer et beløp 31. desember.</span><span class="sxs-lookup"><span data-stu-id="474ff-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="474ff-121">**Månedlig** posterer et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="474ff-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="474ff-122">**Kvartalsvis** posterer et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="474ff-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="474ff-123">**Halvårlig** posterer et halvårlig beløp på slutten av hvert kalenderår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="474ff-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="474ff-124">**Daglig** posterer avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="474ff-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="474ff-125">Hvis du velger for eksempel **Årlig**, posteres den årlige avskrivningen bare én gang, den 31. desember i hvert år.</span><span class="sxs-lookup"><span data-stu-id="474ff-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="474ff-126">Hvis du velger **Månedlig**, posteres den månedlige avskrivningen hver måned, som en tolvdel av Årlig avskrivningsbeløp.</span><span class="sxs-lookup"><span data-stu-id="474ff-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="474ff-127">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="474ff-127">Fiscal</span></span>

<span data-ttu-id="474ff-128">Hvis du velger **Skattemessig** i feltet **Avskrivningsår** , brukes avskrivning for gjenværende lineær levetid.</span><span class="sxs-lookup"><span data-stu-id="474ff-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="474ff-129">Avskrivning beregnes basert på de gjenværende regnskapsårene.</span><span class="sxs-lookup"><span data-stu-id="474ff-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="474ff-130">For regnskapsåret 1. juli 2015 til 30. juni 2016 starter for eksempel avskrivningsberegningen 1. juli.</span><span class="sxs-lookup"><span data-stu-id="474ff-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="474ff-131">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="474ff-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="474ff-132">Avskrivningen justeres for hver regnskapsperiode.</span><span class="sxs-lookup"><span data-stu-id="474ff-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="474ff-133">Lengden på det neste regnskapsåret bestemmes av regnskapsperiodene som er definert på siden **Regnskapskalendere**.</span><span class="sxs-lookup"><span data-stu-id="474ff-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="474ff-134">Hvis du velger **Skattemessig** som avskrivningsår, er følgende alternativer tilgjengelige i **Periodefrekvens**-feltet:</span><span class="sxs-lookup"><span data-stu-id="474ff-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="474ff-135">**Årlig** posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="474ff-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="474ff-136">**Regnskapsperiode**beregner totalbeløpet for avskrivningen for regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="474ff-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="474ff-137">Dette beløpet avsettes deretter i regnskapsperiodene som defineres på siden **Regnskapskalendere** for regnskapskalenderen som er angitt for tablået.</span><span class="sxs-lookup"><span data-stu-id="474ff-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="474ff-138">Eksempel på lineær avskrivning for et uendret anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="474ff-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="474ff-139">Et anleggsmiddel har følgende kjennetegn.</span><span class="sxs-lookup"><span data-stu-id="474ff-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="474ff-140">Anskaffelseskostnad</span><span class="sxs-lookup"><span data-stu-id="474ff-140">Acquisition cost</span></span>    | <span data-ttu-id="474ff-141">11 000</span><span class="sxs-lookup"><span data-stu-id="474ff-141">11,000</span></span> |
| <span data-ttu-id="474ff-142">Restverdi</span><span class="sxs-lookup"><span data-stu-id="474ff-142">Salvage value</span></span>       | <span data-ttu-id="474ff-143">1 000</span><span class="sxs-lookup"><span data-stu-id="474ff-143">1,000</span></span>  |
| <span data-ttu-id="474ff-144">Avskrivningsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="474ff-144">Depreciation base</span></span>   | <span data-ttu-id="474ff-145">10 000</span><span class="sxs-lookup"><span data-stu-id="474ff-145">10,000</span></span> |
| <span data-ttu-id="474ff-146">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="474ff-146">Service life years</span></span>  | <span data-ttu-id="474ff-147">5</span><span class="sxs-lookup"><span data-stu-id="474ff-147">5</span></span>      |
| <span data-ttu-id="474ff-148">Årlig avskrivning</span><span class="sxs-lookup"><span data-stu-id="474ff-148">Yearly depreciation</span></span> | <span data-ttu-id="474ff-149">2 000</span><span class="sxs-lookup"><span data-stu-id="474ff-149">2,000</span></span>  |

<span data-ttu-id="474ff-150">Avskrivningsbeløpet er det samme hvert år: (anskaffelseskostnad-restverdi) ÷ levetidsår</span><span class="sxs-lookup"><span data-stu-id="474ff-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="474ff-151">Periode</span><span class="sxs-lookup"><span data-stu-id="474ff-151">Period</span></span> | <span data-ttu-id="474ff-152">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="474ff-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="474ff-153">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="474ff-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="474ff-154">År 1</span><span class="sxs-lookup"><span data-stu-id="474ff-154">Year 1</span></span> | <span data-ttu-id="474ff-155">(11 000 – 1 000) ÷ 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="474ff-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="474ff-156">9 000</span><span class="sxs-lookup"><span data-stu-id="474ff-156">9,000</span></span>                                 |
| <span data-ttu-id="474ff-157">År 2</span><span class="sxs-lookup"><span data-stu-id="474ff-157">Year 2</span></span> | <span data-ttu-id="474ff-158">(9 000 – 1 000) ÷ 4 = 2 000</span><span class="sxs-lookup"><span data-stu-id="474ff-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="474ff-159">7 000</span><span class="sxs-lookup"><span data-stu-id="474ff-159">7,000</span></span>                                 |
| <span data-ttu-id="474ff-160">År 3</span><span class="sxs-lookup"><span data-stu-id="474ff-160">Year 3</span></span> | <span data-ttu-id="474ff-161">(7 000 – 1 000) ÷ 3 = 2 000</span><span class="sxs-lookup"><span data-stu-id="474ff-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="474ff-162">5 000</span><span class="sxs-lookup"><span data-stu-id="474ff-162">5,000</span></span>                                 |
| <span data-ttu-id="474ff-163">År 4</span><span class="sxs-lookup"><span data-stu-id="474ff-163">Year 4</span></span> | <span data-ttu-id="474ff-164">(5 000 – 1 000) ÷ 2 = 2 000</span><span class="sxs-lookup"><span data-stu-id="474ff-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="474ff-165">3 000</span><span class="sxs-lookup"><span data-stu-id="474ff-165">3,000</span></span>                                 |
| <span data-ttu-id="474ff-166">År 5</span><span class="sxs-lookup"><span data-stu-id="474ff-166">Year 5</span></span> | <span data-ttu-id="474ff-167">(3 000 – 1 000) ÷ 1 = 2 000</span><span class="sxs-lookup"><span data-stu-id="474ff-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="474ff-168">1 000</span><span class="sxs-lookup"><span data-stu-id="474ff-168">1,000</span></span>                                 |






