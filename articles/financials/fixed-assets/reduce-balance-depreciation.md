---
title: Redusere saldoavskriving
description: Denne artikkelen gir en oversikt over redusert saldoverdimetode for avskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e36a7e1a5d83a95de53b70b8e3c3b667aae9c6c0
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="bc199-103">Redusere saldoavskriving</span><span class="sxs-lookup"><span data-stu-id="bc199-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc199-104">Denne artikkelen gir en oversikt over redusert saldoverdimetode for avskrivning.</span><span class="sxs-lookup"><span data-stu-id="bc199-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="bc199-105">Når du definerer en avskrivningsprofil for anleggsmiddel og velger Saldoverdi i Metode-feltet på Avskrivningsprofiler-siden, avskrives anleggsmidler som har denne avskrivningsprofilen tilordnet, med den samme prosenten i hver avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="bc199-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="bc199-106">Hvis du vil definere redusert saldoavskrivning, må du også foreta valg i feltene til hurtigfanen Generelt på siden Avskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="bc199-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="bc199-107">Først velger du et år i Avskrivningsår-feltet.</span><span class="sxs-lookup"><span data-stu-id="bc199-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="bc199-108">Avhengig av hva du har valgt, vises forskjellige alternativer i Periodefrekvens-feltet, som forklart i avsnittene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bc199-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="bc199-109">Du må også skrive inn en verdi i Prosent-feltet avskrivningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="bc199-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="bc199-110">Hvis du velger Full avskrivning, utføres den gjenværende avskrivningen i den siste avskrivningsperioden, og det kan være et stort beløp.</span><span class="sxs-lookup"><span data-stu-id="bc199-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="bc199-111">Noen land/regioner bytter ikke til lineær avskrivningsmetode.</span><span class="sxs-lookup"><span data-stu-id="bc199-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="bc199-112">Når beløpet fra den alternative metoden er større enn eller lik beløpet i den primære avskrivningsprofilen og det brukte avskrivningsbeløpet er beløpet for den alternative metoden, utføres bytte.</span><span class="sxs-lookup"><span data-stu-id="bc199-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="bc199-113">Siden et anleggsmiddel aldri helt avskrives basert på en prosentberegning, må du velge Full avskrivning for å få full avskrivning for et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="bc199-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="bc199-114">Velge et avskrivningsår</span><span class="sxs-lookup"><span data-stu-id="bc199-114">Select a depreciation year</span></span>
<span data-ttu-id="bc199-115">Du kan velge enten Kalender eller Regnskapsår i Avskrivningsår-feltet på siden Avskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="bc199-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="bc199-116">Valget definerer alternativene som er tilgjengelige i Periodefrekvens-feltet.</span><span class="sxs-lookup"><span data-stu-id="bc199-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="bc199-117">Standardvalget er Kalender.</span><span class="sxs-lookup"><span data-stu-id="bc199-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="bc199-118">Kalender</span><span class="sxs-lookup"><span data-stu-id="bc199-118">Calendar</span></span>

<span data-ttu-id="bc199-119">Alternativet Kalender oppdaterer avskrivningsgrunnlaget, som vanligvis er netto bokført verdi minus svinnverdi, 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="bc199-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="bc199-120">I eksemplet på redusert saldoavskrivning senere i dette emnet, er avskrivningsgrunnlaget telleren i det første uttrykket i beregninger i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="bc199-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="bc199-121">Hvis du velger Kalender, er følgende alternativer tilgjengelige i Periodefrekvens-feltet, som definerer posteringsdatoer for avskrivningsavsetning og beløp gjennom hele kalenderåret:</span><span class="sxs-lookup"><span data-stu-id="bc199-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="bc199-122">Årlige posteringer 31. desember.</span><span class="sxs-lookup"><span data-stu-id="bc199-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="bc199-123">Månedlige posteringer av et månedlig beløp på slutten av hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="bc199-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="bc199-124">Kvartalsvise posteringer av et kvartalsvis beløp på slutten av hvert kalenderkvartal (31. mars, 30. juni, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="bc199-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="bc199-125">Halvårlige posteringer av et halvårlig beløp på slutten av hvert kalenderår (30. juni og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="bc199-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="bc199-126">Daglige posteringer av avskrivningsbeløpet for den daglige avskrivningsmetoden ved å bruke én transaksjon per dag.</span><span class="sxs-lookup"><span data-stu-id="bc199-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="bc199-127">Hvis du velger for eksempel Årlig, posteres den årlige avskrivningen bare én gang, den 31. desember i hvert år.</span><span class="sxs-lookup"><span data-stu-id="bc199-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="bc199-128">Hvis du velger Månedlig, posteres den månedlige avskrivningen hver måned som en tolvdel av det årlige avskrivningsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="bc199-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="bc199-129">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bc199-129">Fiscal</span></span>

<span data-ttu-id="bc199-130">Hvis du velger Regnskapsår i Avskrivningsår-feltet, brukes den lineære avskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="bc199-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="bc199-131">Det beregnes basert på regnskapsåret, som er definert på siden Regnskapskalendere for den økonomiske kalenderen som er valgt på finanssiden.</span><span class="sxs-lookup"><span data-stu-id="bc199-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="bc199-132">For regnskapsåret 1. juli til 30. juni starter for eksempel avskrivningsberegningen 1. juli.</span><span class="sxs-lookup"><span data-stu-id="bc199-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="bc199-133">Regnskapsåret kan være lengre eller kortere enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="bc199-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="bc199-134">Avskrivningen justeres for hver regnskapsperiode.</span><span class="sxs-lookup"><span data-stu-id="bc199-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="bc199-135">Lengden på det neste regnskapsåret baseres på regnskapsperiodene som du definerer når du oppretter et nytt regnskapsår på siden med regnskapskalendere.</span><span class="sxs-lookup"><span data-stu-id="bc199-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="bc199-136">Hvis du velger Regnskapsår, er følgende alternativer tilgjengelige i Periodefrekvens-feltet:</span><span class="sxs-lookup"><span data-stu-id="bc199-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="bc199-137">Årlige posteringer av totalbeløpet for avskrivningen som beregnes for regnskapsåret, som ett beløp på den siste dagen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="bc199-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="bc199-138">Regnskapsperioden posterer totalbeløpet for avskrivningen som beregnes for regnskapsåret, som avsettes i regnskapsperiodene som er definert for regnskapskalenderen som er valgt på finanssiden, eller for regnskapskalenderen som er valgt for tablået for et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="bc199-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="bc199-139">Eksempel på redusert saldoavskrivning</span><span class="sxs-lookup"><span data-stu-id="bc199-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="bc199-140">Anta at anskaffelsesprisen for anleggsmidler er 11 000, svinnverdien er 1000 og avskrivningsprosentfaktoren er 30.</span><span class="sxs-lookup"><span data-stu-id="bc199-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="bc199-141">Ifølge Saldoverdi-metoden beregnes 30 prosent av avskrivningsgrunnlaget (netto bokført verdi minus svinnverdi) på slutten av forrige avskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="bc199-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="bc199-142">Avskrivningen for de første tre årene vises i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bc199-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="bc199-143">Periode</span><span class="sxs-lookup"><span data-stu-id="bc199-143">Period</span></span> | <span data-ttu-id="bc199-144">Beregning av årlig avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="bc199-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="bc199-145">Netto bokverdi på slutten av året</span><span class="sxs-lookup"><span data-stu-id="bc199-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="bc199-146">År 1</span><span class="sxs-lookup"><span data-stu-id="bc199-146">Year 1</span></span> | <span data-ttu-id="bc199-147">(11 000 - 1 000) \* 30 % = 3 000</span><span class="sxs-lookup"><span data-stu-id="bc199-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="bc199-148">(11 000 - 1 000) - 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="bc199-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="bc199-149">År 2</span><span class="sxs-lookup"><span data-stu-id="bc199-149">Year 2</span></span> | <span data-ttu-id="bc199-150">(7 000 - 1 000) \* 30 % = 1 800</span><span class="sxs-lookup"><span data-stu-id="bc199-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="bc199-151">(7 000 -1 800) = 5 200</span><span class="sxs-lookup"><span data-stu-id="bc199-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="bc199-152">År 3</span><span class="sxs-lookup"><span data-stu-id="bc199-152">Year 3</span></span> | <span data-ttu-id="bc199-153">(5 200 - 1 000) \* 30 % = 1 260</span><span class="sxs-lookup"><span data-stu-id="bc199-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="bc199-154">(5 200 - 1 260) = 3 940</span><span class="sxs-lookup"><span data-stu-id="bc199-154">(5,200 - 1,260) = 3,940</span></span>               |


-






