---
title: Bruke analyserapporter i Microsoft Dynamics 365 for Talent - Attract
description: Dette emnet beskriver analyserapportene for å få innsikt i ansettelsesprosesser i Microsoft Dynamics 365 for Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: f69c45e885d789d05a081064f30ccd6ce6bfec52
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742895"
---
# <a name="use-analytic-reports"></a><span data-ttu-id="2a1d9-103">Bruke analyserapporter</span><span class="sxs-lookup"><span data-stu-id="2a1d9-103">Use analytic reports</span></span>

<span data-ttu-id="2a1d9-104">Analyserapporter i Attract har en standardløsning for å få innsikt i ansettelsesprosesser.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-104">Analytic reports in Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="2a1d9-105">Tilgjengelige funksjoner omfatter:</span><span class="sxs-lookup"><span data-stu-id="2a1d9-105">Availabe features include:</span></span>

- <span data-ttu-id="2a1d9-106">**Jobbanalyse:** Klikk på kategorien **Analyse** i en jobb for å vise målene for jobbens søkere.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="2a1d9-107">**Analysehub:** Klikk på **Analyse** i venstre navigasjon for å vise aggregerte mål på tvers av jobber.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="2a1d9-108">**Brukerspesifikk sikkerhet:** – Tilgang til rapporter er underlagt Attract-[rollen](security-attract.md) og jobbdeltakerrollen.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="2a1d9-109">**Kryssfiltrering:** Klikk på visuelle effekter i en rapport for å vise andre mål filtrert etter valgte data.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="2a1d9-110">Denne funksjonen er for øyeblikket i [forhåndsvisning](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="2a1d9-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="2a1d9-111">Hvis du vil prøve den, må du ha [**tillegget for omfattende ansettelse**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="2a1d9-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="2a1d9-112">Alle offentlige forhåndsvisningsrapporter vises på engelsk.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="2a1d9-113">Rapporter oppdateres hver 3. time.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="2a1d9-114">Det siste oppdateringstidspunktet (i den lokale tidssonen) er plassert øverst i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="2a1d9-115">Oppdateringstidene er tilnærmet og varierer avhengig av datavolum og ressursbelastning i ditt område.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="2a1d9-116">Jobbanalyse</span><span class="sxs-lookup"><span data-stu-id="2a1d9-116">Job Analytics</span></span>

<span data-ttu-id="2a1d9-117">Jobbanalyse-rapporter er et øyeblikksbilde av ansettelsesprosessen for en jobb.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="2a1d9-118">Viktige mål omfatter:</span><span class="sxs-lookup"><span data-stu-id="2a1d9-118">Key metrics include:</span></span>

- <span data-ttu-id="2a1d9-119">Aktive søkere etter stadium</span><span class="sxs-lookup"><span data-stu-id="2a1d9-119">Active applicants by stage</span></span>
- <span data-ttu-id="2a1d9-120">Søkerkilde</span><span class="sxs-lookup"><span data-stu-id="2a1d9-120">Applicant source</span></span>
- <span data-ttu-id="2a1d9-121">Søkertype (intern eller ekstern)</span><span class="sxs-lookup"><span data-stu-id="2a1d9-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="2a1d9-122">Analysehub</span><span class="sxs-lookup"><span data-stu-id="2a1d9-122">Analytics Hub</span></span>

<span data-ttu-id="2a1d9-123">Analysehub rapporterer samlede data på tvers av jobber for å oppdage trender i ansettelsesprosessen.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="2a1d9-124">Attract omfatter to standardrapporter: Sammendrag av pipeline og traktanalyse.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="2a1d9-125">Sammendrag av pipeline</span><span class="sxs-lookup"><span data-stu-id="2a1d9-125">Pipeline Summary</span></span>

<span data-ttu-id="2a1d9-126">Rapporten Sammendrag av pipeline samler data for åpne jobber.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="2a1d9-127">Viktige mål omfatter:</span><span class="sxs-lookup"><span data-stu-id="2a1d9-127">Key metrics include:</span></span>

- <span data-ttu-id="2a1d9-128">Søkere på tvers av alle jobber etter stadium</span><span class="sxs-lookup"><span data-stu-id="2a1d9-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="2a1d9-129">Søkerkilde</span><span class="sxs-lookup"><span data-stu-id="2a1d9-129">Applicant source</span></span>
- <span data-ttu-id="2a1d9-130">Åpne jobber etter ansiennitetsnivå</span><span class="sxs-lookup"><span data-stu-id="2a1d9-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="2a1d9-131">Traktanalyse</span><span class="sxs-lookup"><span data-stu-id="2a1d9-131">Funnel Analysis</span></span>

<span data-ttu-id="2a1d9-132">Rapporten Traktanalyse samler data for jobber som er lukket som besatt.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="2a1d9-133">Viktige mål omfatter:</span><span class="sxs-lookup"><span data-stu-id="2a1d9-133">Key metrics include:</span></span>

- <span data-ttu-id="2a1d9-134">Tiden det tar å ansette</span><span class="sxs-lookup"><span data-stu-id="2a1d9-134">Time to hire</span></span>
- <span data-ttu-id="2a1d9-135">Konverteringsmål (ved peking)</span><span class="sxs-lookup"><span data-stu-id="2a1d9-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="2a1d9-136">Frekvens for å godta tilbud</span><span class="sxs-lookup"><span data-stu-id="2a1d9-136">Offer acceptance rate</span></span>

<span data-ttu-id="2a1d9-137">Obs! For rapportering av mest mulig nøyaktig tid det tar å ansette, anbefales det at du bruker [Tilbudsbehandling](offer-setup.md), en funksjon som er tilgjengelig i tillegget for omfattende ansettelse.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="2a1d9-138">Prøv å holde pekeren over visuelle effekter for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="2a1d9-139">Hvis du for eksempel holder pekeren over de visuelle effektene for **Aktive søkere**, vises de gjennomsnittlige dagene i stadium.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="2a1d9-140">Ved å analysere denne informasjonen kan du få innsikt som er viktig for å redusere tiden det tar å ansette, og rekrutterere kan fokusere på måter de kan redusere tiden som brukes i hvert stadium.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="2a1d9-141">Brukerspesifikk sikkerhet</span><span class="sxs-lookup"><span data-stu-id="2a1d9-141">User-specific security</span></span>

<span data-ttu-id="2a1d9-142">Attract-rapporter er tilgjengelige for Administrator-, Les alt-, Rekrutterer- og Ansettelsesansvarlig-[rollene](security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="2a1d9-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="2a1d9-143">Ikke-tilordnede brukere har ikke tilgang til noen av analyserapportsidene (Jobbanalyse eller Analysehub).</span><span class="sxs-lookup"><span data-stu-id="2a1d9-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="2a1d9-144">Jobbanalyse-rapporter viser data for den valgte jobben.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="2a1d9-145">Analysehub-rapporter samler data på tvers av alle jobber som en bruker kan vise.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="2a1d9-146">Brukere som kan vise både Mine jobber og Alle jobber på jobbsiden, har de samme visningene tilgjengelig i Analysehub.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="2a1d9-147">Kryssfilter</span><span class="sxs-lookup"><span data-stu-id="2a1d9-147">Cross-filter</span></span>

<span data-ttu-id="2a1d9-148">En av de flotte funksjonene i Power BI er måten alle visuelle effekter på en rapportside er sammenkoblet på.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="2a1d9-149">Hvis du velger et datapunkt i en av de visuelle effektene, endres alle de andre visuelle effektene på siden som inneholder disse dataene, basert på det merkede området.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="2a1d9-150">Finn ut mer og se et eksempel i [Hvordan visuelle effekter kryssfiltrerer hverandre i en Power BI-rapport](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="2a1d9-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="2a1d9-151">Eksporter til Excel</span><span class="sxs-lookup"><span data-stu-id="2a1d9-151">Export to Excel</span></span>

<span data-ttu-id="2a1d9-152">Hvis du vil vise rapportdata i Excel, kan du klikke på Alternativer-menyen (tre prikker) i en visuell effekt og velge **Eksporter underliggende data**.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="2a1d9-153">Eksporterte data eksporteres som filtrert, og brukertillatelser i Attract respekteres.</span><span class="sxs-lookup"><span data-stu-id="2a1d9-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="2a1d9-154">Hvis du vil ha mer informasjon, kan du se [Eksportere data fra visuelle effekter](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="2a1d9-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
