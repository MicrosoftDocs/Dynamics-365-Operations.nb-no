---
title: Tilpassingsanalyse av planleggingsoptimalisering
description: Dette emnet forklarer hvordan du kontrollerer gjeldende oppsett og data mot funksjonene i planleggingsoptimaliseringsfunksjonaliteten.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935881"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="47120-103">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="47120-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="47120-104">Hvis du vil se hvor kompatible gjeldende oppsett og data er med funksjonaliteten for planleggingsoptimalisering, går du til **Hovedplanlegging** \> **Oppsett** \> **Tilpassingsanalyse av planleggingsoptimalisering**, og deretter velger du **Kjør analyse**.</span><span class="sxs-lookup"><span data-stu-id="47120-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="47120-105">Hvis analysen finner noen uregelmessigheter, vises de på samme side.</span><span class="sxs-lookup"><span data-stu-id="47120-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="47120-106">(Det kan ta noen minutter å kjøre analysen.)</span><span class="sxs-lookup"><span data-stu-id="47120-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="47120-107">Hvis det blir funnet uoverensstemmelser, kan du likevel bruke planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="47120-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="47120-108">Resultatene av tilpassingsanalysen viser bare steder der planleggingstjenesten ikke respekterer det gjeldende oppsettet.</span><span class="sxs-lookup"><span data-stu-id="47120-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="47120-109">De viser med andre ord steder der noen prosesser kan bli ignorert, eller det er ikke sikkert at de støttes.</span><span class="sxs-lookup"><span data-stu-id="47120-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="47120-110">Analyseresultater: eksempel 1</span><span class="sxs-lookup"><span data-stu-id="47120-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="47120-111">**Funksjon:** produksjon</span><span class="sxs-lookup"><span data-stu-id="47120-111">**Feature:** Production</span></span>
- <span data-ttu-id="47120-112">**Problem:** varer med stykklistenivå større enn null: 56</span><span class="sxs-lookup"><span data-stu-id="47120-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="47120-113">**Forklaring:** tilpassingsanalysen fant 56 varer som har et oppsett for stykklister for produksjon.</span><span class="sxs-lookup"><span data-stu-id="47120-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="47120-114">Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter produksjon, genererer planleggingsoptimalisering bestillingsforslag i stedet for planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="47120-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="47120-115">Den vil også vise en advarsel som viser de berørte varene.</span><span class="sxs-lookup"><span data-stu-id="47120-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="47120-116">Analyseresultater: eksempel 2</span><span class="sxs-lookup"><span data-stu-id="47120-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="47120-117">**Funksjon:** handlinger</span><span class="sxs-lookup"><span data-stu-id="47120-117">**Feature:** Actions</span></span>
- <span data-ttu-id="47120-118">**Problem:** dekningsgrupper med handlingsberegning aktivert: 6</span><span class="sxs-lookup"><span data-stu-id="47120-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="47120-119">**Forklaring:** Tilpassingsanalysen fant seks dekningsgrupper der handlingsberegning er aktivert.</span><span class="sxs-lookup"><span data-stu-id="47120-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="47120-120">Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter handlinger, blir det ikke generert noen handlinger under hovedplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="47120-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="47120-121">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="47120-121">Related resources</span></span>

[<span data-ttu-id="47120-122">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="47120-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="47120-123">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="47120-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="47120-124">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="47120-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="47120-125">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="47120-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="47120-126">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="47120-126">Cancel a planning job</span></span>](cancel-planning-job.md)
