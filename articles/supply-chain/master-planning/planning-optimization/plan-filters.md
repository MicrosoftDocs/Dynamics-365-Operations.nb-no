---
title: Bruke filtre på en plan
description: Dette emnet beskriver hvordan du bruker filtre på en plan når planleggingsoptimaliserings-funksjonaliteten brukes.
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
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
ms.openlocfilehash: 9d1431cc8db6fb28d1f1ec73ee07dd15e78f82e8
ms.sourcegitcommit: 65f4b8a751670a7fe9ef4cb8b218213f792d57a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945425"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="fe750-103">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="fe750-103">Apply filters to a plan</span></span>

<span data-ttu-id="fe750-104">Når planleggingsoptimaliserings-funksjonaliteten brukes, kan du bruke et filter på en plan.</span><span class="sxs-lookup"><span data-stu-id="fe750-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="fe750-105">**Planfilteret** blir alltid brukt under kjøring av en hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="fe750-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="fe750-106">Et **planfilter** er nyttig når du vil begrense en plan til en bestemt gruppe varer og kontrollere at ingen andre varer er inkludert som en del av den resulterende hovedplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="fe750-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="fe750-107">Hvis det brukes et **planfilter**, og et kjøretidsfilter brukes også i kjøringen av hovedplanlegging, blir bare skjæringspunktet mellom de to filtrene tatt med i planleggingskjøringen.</span><span class="sxs-lookup"><span data-stu-id="fe750-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="fe750-108">Du tilgang til **planfilteret** fra **Hovedplaner** når planleggingsoptimalisering brukes.</span><span class="sxs-lookup"><span data-stu-id="fe750-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="fe750-109">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="fe750-109">Example scenario</span></span>

<span data-ttu-id="fe750-110">Et planfilter er definert som inkluderer varer A, B og C. Hovedplanlegging kjøres deretter for den samme planen, men forskjellige kjøretidsfiltre brukes:</span><span class="sxs-lookup"><span data-stu-id="fe750-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="fe750-111">**Kjøretidsfilter som inkluderer vare D** : ingen varer er planlagt fordi det ikke er noe skjæringspunkt mellom planfilteret og kjøretidsfilteret.</span><span class="sxs-lookup"><span data-stu-id="fe750-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="fe750-112">**Kjøretidsfilter som inkluderer vare A og D** : bare vare A er inkludert i planleggingskjøringen, fordi vare D ikke er del av planfilteret.</span><span class="sxs-lookup"><span data-stu-id="fe750-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="fe750-113">**Kjøretidsfilter som inkluderer vare B** : bare vare B er inkludert i planleggingskjøringen, og de forrige planleggingsutdataene for vare A beholdes.</span><span class="sxs-lookup"><span data-stu-id="fe750-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="fe750-114">**Kjøretidsfilter som inkluderer alle varer (tomt filter)** : varer A, B og C inkluderes i planleggingskjøringen, og de tidligere planleggingsutdataene for varer A og B blir overskrevet.</span><span class="sxs-lookup"><span data-stu-id="fe750-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="fe750-115">Du bør unngå å angi et planfilter for planen som er valgt som **gjeldende dynamiske hovedplan** på siden **Parametere for hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="fe750-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="fe750-116">Hvis ikke vil funksjonaliteten for den dynamiske hovedplanen bli begrenset til de filtrerte varene.</span><span class="sxs-lookup"><span data-stu-id="fe750-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="fe750-117">Hvis for eksempel nettobehovene er oppdatert for en vare som ikke er en del av planfilteret, vil det ikke bli generert noe resultat.</span><span class="sxs-lookup"><span data-stu-id="fe750-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="fe750-118">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="fe750-118">Related resources</span></span>

[<span data-ttu-id="fe750-119">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="fe750-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="fe750-120">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="fe750-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="fe750-121">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="fe750-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="fe750-122">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="fe750-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="fe750-123">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="fe750-123">Cancel a planning job</span></span>](cancel-planning-job.md)