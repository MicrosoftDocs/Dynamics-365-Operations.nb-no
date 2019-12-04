---
title: Oversikt over planleggingsoptimalisering
description: Dette emnet gir en oversikt over funksjoner i planleggingsoptimalisering.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: aae9ea56fc2174df56274776993c68b11c0521d0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774020"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="planning-optimization-overview"></a><span data-ttu-id="1e864-103">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="1e864-103">Planning Optimization overview</span></span>

<span data-ttu-id="1e864-104">Tilleggsfunksjonen for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management gjør at beregningen av hovedplanlegging skjer utenfor Dynamics 365 Supply Chain Management og den tilknyttede SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="1e864-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="1e864-105">Fordelene som er knyttet til planleggingsoptimaliserings-funksjonaliteten, omfatter forbedret ytelse og minimal virkning på SQL-database under kjøringer av hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="1e864-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="1e864-106">Du kan utføre raske planleggingskjøringer selv under kontortimer, slik at planleggere umiddelbart kan reagere på behovs- eller parameterendringer.</span><span class="sxs-lookup"><span data-stu-id="1e864-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="1e864-107">Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS) og aktivere funksjonaliteten for planleggingsoptimalisering i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e864-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="1e864-108">Hvis du vil ha mer informasjon, se [Kom i gang med planleggingsoptimalisering](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="1e864-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="1e864-109">Følgende illustrasjon viser fordelen med å kjøre planleggingsoptimalisering i kontortiden.</span><span class="sxs-lookup"><span data-stu-id="1e864-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Fordel med å kjøre planleggingsoptimalisering i kontortiden](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="1e864-111">Ytelsen er forbedret</span><span class="sxs-lookup"><span data-stu-id="1e864-111">Improved performance</span></span>

<span data-ttu-id="1e864-112">Planleggingsoptimalisering kan brukes i situasjoner som omfatter langvarige hovedplaner.</span><span class="sxs-lookup"><span data-stu-id="1e864-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="1e864-113">Den er spesielt utformet for svært raske beregninger som involverer svært store mengder data.</span><span class="sxs-lookup"><span data-stu-id="1e864-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="1e864-114">Fordi den er bygd som en hyperskalerbar multi-instanstjeneste, kan flere forekomster fungere sammen samtidig for å beregne planen.</span><span class="sxs-lookup"><span data-stu-id="1e864-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="1e864-115">I tillegg fjerner planleggingstjenesten belastningen på hovedplanlegging fra systemet ditt og fungerer med en datastrøm som minimerer belastningen på serveren.</span><span class="sxs-lookup"><span data-stu-id="1e864-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="1e864-116">Planleggingsoptimalisering kan hjelpe deg med å oppnå følgende mål:</span><span class="sxs-lookup"><span data-stu-id="1e864-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="1e864-117">Forbedre planleggingsytelsen gjennom en kortere kjøretid.</span><span class="sxs-lookup"><span data-stu-id="1e864-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="1e864-118">Redusere innvirkningen på andre prosesser under kjøring av hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="1e864-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="1e864-119">Utføre ofte brukte planleggingskjøringer.</span><span class="sxs-lookup"><span data-stu-id="1e864-119">Do more frequent planning runs.</span></span> <span data-ttu-id="1e864-120">(Du er ikke begrenset til daglige kjøringer.)</span><span class="sxs-lookup"><span data-stu-id="1e864-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="1e864-121">Være sikker på at den fremtidige forretningsveksten ikke vil belaste planleggingssystemet.</span><span class="sxs-lookup"><span data-stu-id="1e864-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="1e864-122">Arkitektur og dataflyt</span><span class="sxs-lookup"><span data-stu-id="1e864-122">Architecture and data flow</span></span>

<span data-ttu-id="1e864-123">Når planleggingsoptimaliserings-tillegget installeres fra LCS, opprettes det en sikker forbindelse til planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="1e864-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="1e864-124">Tjenesten befinner seg i samme datasenterland eller -område som den tilknyttede forekomsten av Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e864-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="1e864-125">Når planleggingsoptimalisering er definert, sendes hoveddata og transaksjonsdata fra Supply Chain Management til planleggingsoptimaliseringstjenesten når hovedplanlegging kjøres.</span><span class="sxs-lookup"><span data-stu-id="1e864-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="1e864-126">Hvis tillegget for planleggingsoptimalisering er avinstallert, fjernes alle relaterte data i planleggingsoptimaliseringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="1e864-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="1e864-127">Dataflyt på høyt nivå for regenerering</span><span class="sxs-lookup"><span data-stu-id="1e864-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="1e864-128">Supply Chain Management-klienten sender et signal for å be om en planleggingskjøring fra planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="1e864-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="1e864-129">Planleggingsoptimalisering ber om de nødvendige dataene via den integrerte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1e864-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="1e864-130">SQL-databasen sender den forespurte informasjonen om oppsett, hoved- og transaksjonsdata til planleggingsoptimalisering via koblingen.</span><span class="sxs-lookup"><span data-stu-id="1e864-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="1e864-131">Koblingen oversetter informasjon mellom Supply Chain Management tjenesten for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="1e864-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="1e864-132">Planleggingsoptimaliseringstjenesten inneholder planleggingsrelaterte data i minnet, og utfører de nødvendige beregningene.</span><span class="sxs-lookup"><span data-stu-id="1e864-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="1e864-133">Planleggingsresultatet sendes til Supply Chain Management-databasen via koblingen.</span><span class="sxs-lookup"><span data-stu-id="1e864-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="1e864-134">Resultatene omfatter informasjon som for eksempel planlagte bestillinger og utligningsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="1e864-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="1e864-135">Planleggingsoptimalisering sender et signal til Supply Chain Management for å angi at planleggingsutførelsen er fullført.</span><span class="sxs-lookup"><span data-stu-id="1e864-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="1e864-136">Den sender også eventuelle relevante meldinger og advarsler.</span><span class="sxs-lookup"><span data-stu-id="1e864-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="1e864-137">Følgende illustrasjon viser dataflyten.</span><span class="sxs-lookup"><span data-stu-id="1e864-137">The following illustration shows the data flow.</span></span>

![Dataflyt for regenerering](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="1e864-139">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="1e864-139">Related resources</span></span>

[<span data-ttu-id="1e864-140">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="1e864-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1e864-141">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="1e864-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1e864-142">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="1e864-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1e864-143">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="1e864-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1e864-144">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="1e864-144">Cancel a planning job</span></span>](cancel-planning-job.md)
