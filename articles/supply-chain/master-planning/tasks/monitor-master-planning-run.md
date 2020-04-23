---
title: Overvåke en kjøring av hovedplanlegging
description: Dette emnet beskriver hvordan produksjonsplanleggerne kan se om det pågår en hovedplanlegging.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 159043f37b067df26fdd1de5610eafd663bf6a57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209565"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="07962-103">Overvåke en kjøring av hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="07962-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="07962-104">Bruke et Gantt-diagram til å visualisere fremdriften for hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="07962-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="07962-105">På siden **Vis fremdrift for hovedplanlegging** kan du vise detaljer om historisk hovedplanlegging som kjøres som et Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="07962-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="07962-106">Denne funksjonaliteten kan hjelpe deg med å forstå tiden som brukes på de forskjellige fasene av hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="07962-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="07962-107">For en gjeldende aktiv planleggingsjobb kan du bruke siden **Vis fremdrift for hovedplanlegging** til å spore fremdriften og vise den estimerte gjenværende tiden.</span><span class="sxs-lookup"><span data-stu-id="07962-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="07962-108">Aktivere og bruke fremdrifsvisualiseringsfunksjonen for hovedplan</span><span class="sxs-lookup"><span data-stu-id="07962-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="07962-109">Hvis du vil bruke denne funksjonen, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="07962-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="07962-110">I arbeidsområdet **Funksjonsbehandling** i **Ny**-kategorien velger du **Fremdrifsvisualisering for hovedplan** i listen.</span><span class="sxs-lookup"><span data-stu-id="07962-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="07962-111">Hvis funksjonen ikke vises i **Ny**-kategorien, ser du i kategoriene **Ikke aktivert** og **Alle**.</span><span class="sxs-lookup"><span data-stu-id="07962-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="07962-112">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="07962-112">Select **Enable now**.</span></span> <span data-ttu-id="07962-113">Du kan også velge **Tidsplan**, og deretter velge tidspunktet når du vil at funksjonen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="07962-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="07962-114">Siden **Vis fremdrift for hovedplanlegging** kan vise både historiske planleggingsjobber og aktive planleggingsjobber.</span><span class="sxs-lookup"><span data-stu-id="07962-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="07962-115">Hvis du vil vise historiske planleggingsjobber, kan du velge mellom to alternativer.</span><span class="sxs-lookup"><span data-stu-id="07962-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="07962-116">Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**, og velg deretter **Historikk** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="07962-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="07962-117">Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**</span><span class="sxs-lookup"><span data-stu-id="07962-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="07962-118">Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**, og klikk **Historikk** på hovedplanlegging-flisen.</span><span class="sxs-lookup"><span data-stu-id="07962-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="07962-119">Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**</span><span class="sxs-lookup"><span data-stu-id="07962-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="07962-120">Hvis du vil vise aktive planleggingsjobber, kan du velge mellom to alternativer.</span><span class="sxs-lookup"><span data-stu-id="07962-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="07962-121">Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**, og velg **Uferdig planleggingsprosess** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="07962-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="07962-122">Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**.</span><span class="sxs-lookup"><span data-stu-id="07962-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="07962-123">Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**, og klikk **Vis fremdrift** på hovedplanlegging-flisen.</span><span class="sxs-lookup"><span data-stu-id="07962-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="07962-124">Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**</span><span class="sxs-lookup"><span data-stu-id="07962-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="07962-125">Merk at du bare kan vise aktive jobber når en planleggingsjobb behandles.</span><span class="sxs-lookup"><span data-stu-id="07962-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="07962-126">Analysere en hovedplanlegging-jobb</span><span class="sxs-lookup"><span data-stu-id="07962-126">Analyze a master planning job</span></span>

<span data-ttu-id="07962-127">I Gantt-diagrammet kan du utvide hver av de følgende planleggingsprosessene for å vise flere detaljer om tiden som er brukt:</span><span class="sxs-lookup"><span data-stu-id="07962-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="07962-128">Initialisering</span><span class="sxs-lookup"><span data-stu-id="07962-128">Initializing</span></span>
- <span data-ttu-id="07962-129">Sletter og setter inn data</span><span class="sxs-lookup"><span data-stu-id="07962-129">Deleting and inserting data</span></span>
- <span data-ttu-id="07962-130">Dekningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="07962-130">Coverage planning</span></span>
- <span data-ttu-id="07962-131">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="07962-131">Delays</span></span>
- <span data-ttu-id="07962-132">Handlingsmeldinger</span><span class="sxs-lookup"><span data-stu-id="07962-132">Action messages</span></span>
- <span data-ttu-id="07962-133">Sluttbehandling</span><span class="sxs-lookup"><span data-stu-id="07962-133">Finalization</span></span>
- <span data-ttu-id="07962-134">Automatisk autorisering</span><span class="sxs-lookup"><span data-stu-id="07962-134">Auto-firming</span></span>

<span data-ttu-id="07962-135">Gantt-diagrammet er et nyttig verktøy hvis du vil vise virkningen av å bruke handlingsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="07962-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="07962-136">Navigasjon i Gantt-diagrammet</span><span class="sxs-lookup"><span data-stu-id="07962-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="07962-137">Hvis du vil utvide den valgte gruppen og vise detaljene, velger du plusstegnet (**+**) i trevisningen.</span><span class="sxs-lookup"><span data-stu-id="07962-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="07962-138">Hvis du vil skjule den valgte gruppen, velger du minustegnet (**–**) i trevisningen.</span><span class="sxs-lookup"><span data-stu-id="07962-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="07962-139">Du kan bruke tastaturet til navigasjon.</span><span class="sxs-lookup"><span data-stu-id="07962-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="07962-140">Bruk **pil opp** og **pil ned** for å flytte mellom rader.</span><span class="sxs-lookup"><span data-stu-id="07962-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="07962-141">Bruk **pil høyre** og **pil venstre** til å vise og skjule grupper.</span><span class="sxs-lookup"><span data-stu-id="07962-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="07962-142">Hvis du vil åpne eller lukke alle nivåer i Gantt-diagrammet, velger du **Vis alle** eller **Skjul alle**.</span><span class="sxs-lookup"><span data-stu-id="07962-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="07962-143">Hvis du vil vise den tilknyttede behandlingstiden, holder du pekeren over en oppgave.</span><span class="sxs-lookup"><span data-stu-id="07962-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="07962-144">(Oppgaver er det laveste nivået i Gantt-diagrammet.)</span><span class="sxs-lookup"><span data-stu-id="07962-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="07962-145">Vis en ekstra hovedplanleggingskjøring til å sammenligne jobber</span><span class="sxs-lookup"><span data-stu-id="07962-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="07962-146">Hvis du velger en jobb for hovedplanlegging i feltet **Vis en ekstra hovedplanleggingskjøring**, kan du vise en ekstra hovedplanlegging-kjøring i Gantt-diagrammet og sammenligne de to jobbene.</span><span class="sxs-lookup"><span data-stu-id="07962-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="07962-147">Visning på stykklistenivå</span><span class="sxs-lookup"><span data-stu-id="07962-147">BOM-level display</span></span>

<span data-ttu-id="07962-148">Stykklistenivåer vises på en annen måte for dekningsplanlegging, forsinkelser, handlinger og autorisering.</span><span class="sxs-lookup"><span data-stu-id="07962-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="07962-149">**Dekningsplanlegging** – stykklistenivåer vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="07962-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="07962-150">De beregnes fra toppen og nedover.</span><span class="sxs-lookup"><span data-stu-id="07962-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="07962-151">**Eksempel:** stykklistenivå 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="07962-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="07962-152">**Forsinkelser** – stykklistenivåer vises etter hvert som stykklistenivåer for planlegging multipliseres med –1.</span><span class="sxs-lookup"><span data-stu-id="07962-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="07962-153">(Med andre ord har de et negativt tegn.)</span><span class="sxs-lookup"><span data-stu-id="07962-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="07962-154">**Eksempel:** stykklistenivå –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="07962-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="07962-155">**Handlingsmelding** – stykklistenivåer vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="07962-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="07962-156">De beregnes fra toppen og nedover.</span><span class="sxs-lookup"><span data-stu-id="07962-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="07962-157">**Eksempel:** stykklistenivå 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="07962-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="07962-158">**Automatisk autorisering** – stykklistenivåer vises som 999 minus stykklistenivået for dekningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="07962-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="07962-159">**Eksempel:** stykklistenivå 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="07962-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="07962-160">Følgende tabell viser en oversikt over virkemåten.</span><span class="sxs-lookup"><span data-stu-id="07962-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="07962-161">Stykklistenivå som vises</span><span class="sxs-lookup"><span data-stu-id="07962-161">BOM level that is shown</span></span> | <span data-ttu-id="07962-162">Sluttvare</span><span class="sxs-lookup"><span data-stu-id="07962-162">End item</span></span> | <span data-ttu-id="07962-163">Delkomponent</span><span class="sxs-lookup"><span data-stu-id="07962-163">Subcomponent</span></span> | <span data-ttu-id="07962-164">Råmateriale</span><span class="sxs-lookup"><span data-stu-id="07962-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="07962-165">Dekningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="07962-165">Coverage planning</span></span> | <span data-ttu-id="07962-166">0</span><span class="sxs-lookup"><span data-stu-id="07962-166">0</span></span> | <span data-ttu-id="07962-167">1</span><span class="sxs-lookup"><span data-stu-id="07962-167">1</span></span> | <span data-ttu-id="07962-168">2</span><span class="sxs-lookup"><span data-stu-id="07962-168">2</span></span> |
| <span data-ttu-id="07962-169">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="07962-169">Delays</span></span> | <span data-ttu-id="07962-170">0</span><span class="sxs-lookup"><span data-stu-id="07962-170">0</span></span> | <span data-ttu-id="07962-171">–1</span><span class="sxs-lookup"><span data-stu-id="07962-171">–1</span></span> | <span data-ttu-id="07962-172">–2</span><span class="sxs-lookup"><span data-stu-id="07962-172">–2</span></span> |
| <span data-ttu-id="07962-173">Handlingsmelding</span><span class="sxs-lookup"><span data-stu-id="07962-173">Action message</span></span> | <span data-ttu-id="07962-174">0</span><span class="sxs-lookup"><span data-stu-id="07962-174">0</span></span> | <span data-ttu-id="07962-175">1</span><span class="sxs-lookup"><span data-stu-id="07962-175">1</span></span> | <span data-ttu-id="07962-176">2</span><span class="sxs-lookup"><span data-stu-id="07962-176">2</span></span> |
| <span data-ttu-id="07962-177">Automatisk autorisering</span><span class="sxs-lookup"><span data-stu-id="07962-177">Auto-firming</span></span> | <span data-ttu-id="07962-178">999</span><span class="sxs-lookup"><span data-stu-id="07962-178">999</span></span> | <span data-ttu-id="07962-179">998</span><span class="sxs-lookup"><span data-stu-id="07962-179">998</span></span> | <span data-ttu-id="07962-180">997</span><span class="sxs-lookup"><span data-stu-id="07962-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="07962-181">Visualiser fremdriften</span><span class="sxs-lookup"><span data-stu-id="07962-181">Visualize progress</span></span>

<span data-ttu-id="07962-182">Hvis du viser en hovedplanleggingsjobb som for øyeblikket kjører, vises fremdriften gjennom farger i Gantt-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="07962-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="07962-183">Følgende farger gjelder for det blå temaet.</span><span class="sxs-lookup"><span data-stu-id="07962-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="07962-184">For andre fargetemaer vil fargene være forskjellige.</span><span class="sxs-lookup"><span data-stu-id="07962-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="07962-185">**Mørkeblå** – fullførte planleggingsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="07962-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="07962-186">**Oransje** – den pågående oppgaven.</span><span class="sxs-lookup"><span data-stu-id="07962-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="07962-187">**Lyseblå** – estimatet for gjenstående oppgaver.</span><span class="sxs-lookup"><span data-stu-id="07962-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="07962-188">Fargen vises bare på det laveste nivået i Gantt-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="07962-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="07962-189">Velg **Vis alle** for å vise alle aktivitetene i hovedplanlegging-jobben.</span><span class="sxs-lookup"><span data-stu-id="07962-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="07962-190">Beregningen av gjenstående oppgaver er basert på historiske hovedplanleggingsjobber.</span><span class="sxs-lookup"><span data-stu-id="07962-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="07962-191">Kjøre hovedplanlegging og spore behandlingstid</span><span class="sxs-lookup"><span data-stu-id="07962-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="07962-192">Velg **Hovedplanlegging** på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="07962-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="07962-193">Angi eller velg en verdi i **Plan**-feltet.</span><span class="sxs-lookup"><span data-stu-id="07962-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="07962-194">Velg **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="07962-194">Select **Run**.</span></span>
1. <span data-ttu-id="07962-195">Sett alternativet **Spor behandlingstid** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="07962-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="07962-196">Angi et tall i feltet **Antall tråder**.</span><span class="sxs-lookup"><span data-stu-id="07962-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="07962-197">Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .</span><span class="sxs-lookup"><span data-stu-id="07962-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="07962-198">I rutenettet velger du raden der **Felt**-feltet er satt til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="07962-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="07962-199">Angi en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="07962-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="07962-200">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="07962-200">Select **OK**.</span></span>
