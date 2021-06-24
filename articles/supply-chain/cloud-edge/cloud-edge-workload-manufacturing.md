---
title: Sky- og kantskalaenheter for arbeidsbelastninger for produksjonskjøring
description: Dette emnet beskriver hvordan arbeidsbelastninger for produksjonskjøringer fungerer med sky- og kantskalaenheter.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184002"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="2273c-103">Skalaenheter for sky og kant for arbeidsbelastninger for produksjonsutførelse</span><span class="sxs-lookup"><span data-stu-id="2273c-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="2273c-104">Arbeidsbelastningen for produksjonsutførelse er tilgjengelig som forhåndsversjon på dette tidspunktet.</span><span class="sxs-lookup"><span data-stu-id="2273c-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="2273c-105">Noen forretningsfunksjoner støttes ikke fullstendig i den offentlige forhåndsversjonen når arbeidsbelastningsskalaenheter brukes.</span><span class="sxs-lookup"><span data-stu-id="2273c-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="2273c-106">Ved produksjonsutførelse leverer skalaenheter følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="2273c-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="2273c-107">Maskinoperatører og produksjonsledere har tilgang til driftsproduksjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="2273c-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="2273c-108">Maskinoperatører kan holde planen oppdatert ved å kjøre separat og behandle produksjonsjobber.</span><span class="sxs-lookup"><span data-stu-id="2273c-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="2273c-109">Produksjonslederen kan justere driftsplanen.</span><span class="sxs-lookup"><span data-stu-id="2273c-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="2273c-110">Arbeidere kan få tilgang til tid og fremmøte for innstempling og utstempling på kanten for å sikre riktig beregning av arbeiderlønn.</span><span class="sxs-lookup"><span data-stu-id="2273c-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="2273c-111">Dette emnet beskriver hvordan arbeidsbelastninger for produksjonskjøringer fungerer med sky- og kantskalaenheter.</span><span class="sxs-lookup"><span data-stu-id="2273c-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="2273c-112">Produksjonslivssyklusen</span><span class="sxs-lookup"><span data-stu-id="2273c-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="2273c-113">Som den følgende illustrasjonen viser, er produksjonslivssyklusen delt inn i tre faser: *planlegge*, *kjøre* og *fullføre*.</span><span class="sxs-lookup"><span data-stu-id="2273c-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="2273c-114">[![Produksjonskjøringsfaser når ett enkelt miljø brukes](media/mes-phases.png "Produksjonskjøringsfaser når ett enkelt miljø brukes")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="2273c-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="2273c-115">_Planlegge_-fasen omfatter produktdefinisjon, planlegging, oppretting og planlegging av ordrer og frigivelse.</span><span class="sxs-lookup"><span data-stu-id="2273c-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="2273c-116">Frigivelsestrinnet viser overgangen fra _Planlegg_-fasen til _Kjøre_-fasen.</span><span class="sxs-lookup"><span data-stu-id="2273c-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="2273c-117">Når en produksjonsordre frigis, vil produksjonsordrejobbene være synlige på produksjonsgulvet og klare til kjøring.</span><span class="sxs-lookup"><span data-stu-id="2273c-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="2273c-118">Når en produksjonsjobb er merket som fullført, flyttes den fra _Kjøre_-fasen til _Fullføre_-fasen.</span><span class="sxs-lookup"><span data-stu-id="2273c-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="2273c-119">I _Fullføre_-fasen går registreringene fra *Kjøre*-fasen gjennom en godkjenningsarbeidsflyt, der de beregnes, godkjennes og overføres.</span><span class="sxs-lookup"><span data-stu-id="2273c-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="2273c-120">På dette tidspunktet fullføres produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="2273c-120">At that point, the production order is completed.</span></span> <span data-ttu-id="2273c-121">Derfor genereres grunnlaget for arbeiderens lønn.</span><span class="sxs-lookup"><span data-stu-id="2273c-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="2273c-122">Dele Kjøre-fasen i en separat arbeidsbelastning</span><span class="sxs-lookup"><span data-stu-id="2273c-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="2273c-123">Som den følgende illustrasjonen viser, blir _Kjøre_-fasen delt som en egen arbeidsbelastning når du bruker skalaenheter.</span><span class="sxs-lookup"><span data-stu-id="2273c-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="2273c-124">[![Produksjonskjøringsfaser når skalaenheter brukes](media/mes-phases-workloads.png "Produksjonskjøringsfaser når skalaenheter brukes")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="2273c-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="2273c-125">Modellen går nå fra en enkelt forekomstinstallasjon til en modell som er basert på senteret og skalaenhetene.</span><span class="sxs-lookup"><span data-stu-id="2273c-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="2273c-126">_Planlegge_- og _Fullføre_-fasene kjører som Back-Office-operasjoner på senteret, og arbeidsbelastningen for produksjonskjøring kjører på skalaenhetene.</span><span class="sxs-lookup"><span data-stu-id="2273c-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="2273c-127">Data overføres asynkront mellom senteret og skalaenhetene.</span><span class="sxs-lookup"><span data-stu-id="2273c-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="2273c-128">Når en produksjonsordre frigis på senteret, overføres alle data som kreves for å behandle produksjonsjobber, til skalaenheten.</span><span class="sxs-lookup"><span data-stu-id="2273c-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="2273c-129">Disse dataene omfatter produksjonsordrer, produksjonsruter, stykklister og produkter.</span><span class="sxs-lookup"><span data-stu-id="2273c-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="2273c-130">Data som ikke er knyttet til en produksjonsordre (for eksempel indirekte aktiviteter, fraværskoder og produksjonsparametere), overføres også fra senteret til skalaenheten.</span><span class="sxs-lookup"><span data-stu-id="2273c-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="2273c-131">Som en regel kan data som kommer fra senteret, og som overføres til skalaenheten, bare opprettes eller oppdateres på senteret.</span><span class="sxs-lookup"><span data-stu-id="2273c-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="2273c-132">En ny fraværskode eller indirekte aktivitet kan for eksempel ikke opprettes på en skalaenhet – de kan bare brukes til registrering.</span><span class="sxs-lookup"><span data-stu-id="2273c-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="2273c-133">Registreringene som gjøres på skalaenheten under kjøring, blir deretter overført til senteret, der tids- og fremmøtegodkjenning, lager og økonomiske oppdateringer behandles.</span><span class="sxs-lookup"><span data-stu-id="2273c-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="2273c-134">Produksjonskjøringsoppgaver som kan kjøres på arbeidsbelastninger</span><span class="sxs-lookup"><span data-stu-id="2273c-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="2273c-135">Følgende produksjonskjøringsoppgaver kan for øyeblikket kjøres på arbeidsbelastninger når skalaenheter brukes:</span><span class="sxs-lookup"><span data-stu-id="2273c-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="2273c-136">Innstempling, pålogging, utstempling og fravær</span><span class="sxs-lookup"><span data-stu-id="2273c-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="2273c-137">Start jobb</span><span class="sxs-lookup"><span data-stu-id="2273c-137">Start job</span></span>
- <span data-ttu-id="2273c-138">Bunt jobber</span><span class="sxs-lookup"><span data-stu-id="2273c-138">Bundle jobs</span></span>
- <span data-ttu-id="2273c-139">Rapportfremdrift</span><span class="sxs-lookup"><span data-stu-id="2273c-139">Report progress</span></span>
- <span data-ttu-id="2273c-140">Rapporter svinn</span><span class="sxs-lookup"><span data-stu-id="2273c-140">Report scrap</span></span>
- <span data-ttu-id="2273c-141">Indirekte aktivitet</span><span class="sxs-lookup"><span data-stu-id="2273c-141">Indirect activity</span></span>
- <span data-ttu-id="2273c-142">Bryt</span><span class="sxs-lookup"><span data-stu-id="2273c-142">Break</span></span>
- <span data-ttu-id="2273c-143">Ferdigmeld og plasser (krever at du også kjører arbeidsmengden for lagerkjøring på skalaenheten, se også [Ferdigmeld og plasser på en skalaenhet](#RAF))</span><span class="sxs-lookup"><span data-stu-id="2273c-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="2273c-144">Arbeide med arbeidsbelastninger for produksjonskjøring på senteret</span><span class="sxs-lookup"><span data-stu-id="2273c-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="2273c-145">Vanligvis kjøres prosessene som kreves for å kjøre arbeidsbelastninger for produksjonskjøring automatisk for å holde senteret og alle skalaenhetene synkronisert, etter behov.</span><span class="sxs-lookup"><span data-stu-id="2273c-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="2273c-146">Hvis du har problemer, kan du imidlertid manuelt utløse behandlingen av råregistreringer som mottas fra arbeidsbelastninger, eller kontrollere registreringsbehandlingsloggen.</span><span class="sxs-lookup"><span data-stu-id="2273c-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="2273c-147">Behandle råregistreringer manuelt</span><span class="sxs-lookup"><span data-stu-id="2273c-147">Manually process raw registrations</span></span>

<span data-ttu-id="2273c-148">En satsvis jobb i Supply Chain Management kjøres automatisk for å behandle alle registreringer som er mottatt fra arbeidsbelastningene.</span><span class="sxs-lookup"><span data-stu-id="2273c-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="2273c-149">Denne jobben oppretter de nødvendige produksjonsjournalene og loggbokpostene når en registrering behandles for en fullført jobb i arbeidsbelastningen.</span><span class="sxs-lookup"><span data-stu-id="2273c-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="2273c-150">Selv om jobben vanligvis kjører automatisk, kan du kjøre den manuelt når som helst ved å logge deg på senteret og gå til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling \> Råregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="2273c-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="2273c-151">Kontroller loggen for råregistreringsbehandling</span><span class="sxs-lookup"><span data-stu-id="2273c-151">Check the raw registration processing log</span></span>

<span data-ttu-id="2273c-152">Hvis du vil se gjennom registreringsbehandlingsloggen, logger du deg på senteret og går til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling \> Logg over råregistreringsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="2273c-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="2273c-153">Siden **Logg for råregistreringsbehandling** viser en liste over behandlede råregistreringer og statusen for hver registrering.</span><span class="sxs-lookup"><span data-stu-id="2273c-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="2273c-154">![Siden Logg for råregistreringsbehandling](media/mes-processing-log.png "Siden Logg for råregistreringsbehandling")</span><span class="sxs-lookup"><span data-stu-id="2273c-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="2273c-155">Du kan arbeide med en hvilken som helst registrering i listen ved å velge den og deretter velge en av følgende knapper i handlingsruten:</span><span class="sxs-lookup"><span data-stu-id="2273c-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="2273c-156">**Behandle** – Behandle den valgte registreringen manuelt.</span><span class="sxs-lookup"><span data-stu-id="2273c-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="2273c-157">Denne handlingen kan være nyttig hvis _Behandle råregistreringer_-jobben ikke er kjørt, eller hvis den mislyktes.</span><span class="sxs-lookup"><span data-stu-id="2273c-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="2273c-158">**Avbryt** – Avbryt den valgte registreringen.</span><span class="sxs-lookup"><span data-stu-id="2273c-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="2273c-159">Arbeide med arbeidsbelastninger for produksjonskjøring på en skalaenhet</span><span class="sxs-lookup"><span data-stu-id="2273c-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="2273c-160">Vanligvis kjøres prosessene som kreves for å kjøre arbeidsbelastninger for produksjonskjøring automatisk for å holde senteret og alle skalaenhetene synkronisert, etter behov.</span><span class="sxs-lookup"><span data-stu-id="2273c-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="2273c-161">Hvis du har problemer, kan du imidlertid kontrollere historikken til ordrer som er behandlet på en skalaenhet, eller kjøre jobben _Prosessoren for produksjonssenter til skalaenhetsmelding_.</span><span class="sxs-lookup"><span data-stu-id="2273c-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="2273c-162">Vis historikken for produksjonsjobber som er behandlet på en skalaenhet</span><span class="sxs-lookup"><span data-stu-id="2273c-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="2273c-163">Hvis du vil se gjennom historikken for produksjonsjobber som er behandlet på en skalaenhet, kan du logge på skalaenhetsmaskinen og gå til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelasatningsbehandling \> Behandlingslogg over produksjonsjobber**.</span><span class="sxs-lookup"><span data-stu-id="2273c-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="2273c-164">Siden **Behandlingslogg over produksjonsjobber** viser behandlingsloggen for produksjonsordrene på skalaenheten.</span><span class="sxs-lookup"><span data-stu-id="2273c-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="2273c-165">Du kan arbeide med en hvilken som helst produksjonsordre i listen ved å velge den og deretter velge en av følgende knapper i handlingsruten:</span><span class="sxs-lookup"><span data-stu-id="2273c-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="2273c-166">**Behandle** – Behandle den valgte produksjonsordren manuelt.</span><span class="sxs-lookup"><span data-stu-id="2273c-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="2273c-167">**Avbryt** – Avbryt den valgte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="2273c-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="2273c-168">Jobben Behandle produksjonssenter til skalaenhet</span><span class="sxs-lookup"><span data-stu-id="2273c-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="2273c-169">Jobben _Behandle produksjonssenter til skalaenhet_ behandler data fra senteret til skalaenheten.</span><span class="sxs-lookup"><span data-stu-id="2273c-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="2273c-170">Denne jobben startes automatisk når arbeidsbelastningen for produksjonskjøring distribueres.</span><span class="sxs-lookup"><span data-stu-id="2273c-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="2273c-171">Du kan imidlertid kjøre den manuelt når som helst ved å gå til **Produksjonskontroll \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling \> Behandle produksjonssenter til skalaenhet**.</span><span class="sxs-lookup"><span data-stu-id="2273c-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="2273c-172">Ferdigmeld og plasser på en skalaenhet</span><span class="sxs-lookup"><span data-stu-id="2273c-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="2273c-173">I gjeldende utgivelse støttes operasjoner med ferdigmeld og plasser (for ferdige produkter, koprodukter og biprodukter) av [arbeidsmengden for lagerkjøring](cloud-edge-workload-warehousing.md) (ikke arbeidsmengden for produksjonskjøring).</span><span class="sxs-lookup"><span data-stu-id="2273c-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="2273c-174">Du må derfor gjøre følgende hvis du vil bruke denne funksjonaliteten når du er koblet til en skalaenhet:</span><span class="sxs-lookup"><span data-stu-id="2273c-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="2273c-175">Installer både arbeidsmengden for lagerkjøring og arbeidsmengden for produksjonskjøring på skalaenheten.</span><span class="sxs-lookup"><span data-stu-id="2273c-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="2273c-176">Bruk mobilappen Warehouse Management til å ferdigmelde og behandle plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="2273c-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="2273c-177">Grensesnittet for produksjonsutførelse støtter ikke disse prosessene for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="2273c-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
