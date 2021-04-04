---
title: Planlegge arbeidsopprettelse under bølge
description: Dette emnet beskriver hvordan du definerer og bruker bølgebehandlingsmetoden for planlegging av arbeidsopprettelse.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501228"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="0d7d8-103">Planlegge arbeidsopprettelse under bølge</span><span class="sxs-lookup"><span data-stu-id="0d7d8-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0d7d8-104">Bruk funksjonen *Planlegg arbeidsopprettelse* som en del av bølgeprosessen for å øke bølgebehandlingsgjennomstrømming, ved å få systemet til å opprette arbeid ved hjelp av parallell behandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="0d7d8-105">Når funksjonaliteten er aktivert, blir planlagt arbeid opprettet automatisk, som systemet til slutt behandler for å opprette faktisk arbeid.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="0d7d8-106">Hvis antall bølgelastlinjer når en forhåndsbestemt terskel, oppretter systemet faktisk arbeid raskere ved å bruke parallell, asynkron behandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="0d7d8-107">Aktivere funksjonen Planlegg arbeidsopprettelse</span><span class="sxs-lookup"><span data-stu-id="0d7d8-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="0d7d8-108">Aktivere funksjonen i funksjonsbehandling</span><span class="sxs-lookup"><span data-stu-id="0d7d8-108">Enable the feature in feature management</span></span>

<span data-ttu-id="0d7d8-109">Før du kan bruke funksjonen *Planlegg arbeidsopprettelse*, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="0d7d8-110">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="0d7d8-111">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="0d7d8-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0d7d8-112">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="0d7d8-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0d7d8-113">**Funksjonsnavn:** *Planlegg arbeidsopprettelse*</span><span class="sxs-lookup"><span data-stu-id="0d7d8-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="0d7d8-114">Funksjonen *Organisasjonsomfattende arbeidsblokkering* må være aktivert før du kan aktivere *Planlegg arbeidsopprettelse*.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="0d7d8-115">Aktivere satsvis behandling av bølger manuelt</span><span class="sxs-lookup"><span data-stu-id="0d7d8-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="0d7d8-116">For å kunne dra nytte av en parallell, asynkron metode for opprettelse av lagerarbeid må bølgeprosessen kjøre satsvis.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="0d7d8-117">Slik konfigurerer du dette:</span><span class="sxs-lookup"><span data-stu-id="0d7d8-117">To set this up:</span></span>

1. <span data-ttu-id="0d7d8-118">Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="0d7d8-119">Angi *Ja* for **Behandle bølger satsvis** i **Generelt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="0d7d8-120">Du kan eventuelt også velge en dedikert **Satsvis gruppe for bølgebehandling** for å unngå at behandlingen av den satsvise køen kjører samtidig som andre prosesser.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="0d7d8-121">Angi **Vent på lås (ms)**, som brukes når systemet behandler flere bølger samtidig.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="0d7d8-122">Det anbefales en verdi på *60000* for de fleste større bølgeprosessene.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="0d7d8-123">Aktivere den nye bølgetrinnmetoden for eksisterende bølgemaler manuelt</span><span class="sxs-lookup"><span data-stu-id="0d7d8-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="0d7d8-124">Begynn med å opprette den nye bølgetrinnmetoden og aktivere den for parallell, asynkron oppgavebehandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="0d7d8-125">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="0d7d8-126">Velg  **Generer metoder på nytt** og legg merke til at metoden *WHSScheduleWorkCreaveStepMethod* er lagt til i listen over bølgeprosessmetoder du kan bruke i forsendelsesbølgemalene.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="0d7d8-127">Velg posten med **Metodenavn** *WHSScheduleWorkCreationWaveStepMethod*, og velg **Oppgavekonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="0d7d8-128">Du kan legge til en ny rad i rutenettet ved å velg **Ny** i handlingsruten og bruke følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="0d7d8-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="0d7d8-129">**Lager** – Velg lageret du vil bruke til behandling av planlegging av arbeidsopprettelse.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="0d7d8-130">**Maksimalt antall satsvise oppgaver** – Angi et maksimalt antall satsvise oppgaver.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="0d7d8-131">Denne verdien skal i de fleste tilfeller være i området 8–16, men vi anbefaler at du eksperimenterer med den optimale innstillingen basert på scenarioene dine.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="0d7d8-132">**Satsvis gruppe for bølgebehandling** – Velg en dedikert satsvis gruppe for bølgebehandling for å optimalisere behandlingen av den satsvise køen.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="0d7d8-133">Du er nå klar til å oppdatere en eksisterende bølgemal (eller opprette en ny) for å bruke bølgebehandlingsmetoden *Planlegg arbeidsopprettelse*.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="0d7d8-134">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="0d7d8-135">Velg **Rediger** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="0d7d8-136">I listeruten velger du bølgemalen du vil oppdatere (hvis du tester ved hjelp av demonstrasjonsdata, kan du bruke *24 Standardforsendelse*).</span><span class="sxs-lookup"><span data-stu-id="0d7d8-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="0d7d8-137">Utvid hurtigfanen **Metoder**, og velg raden der **Navn** er *Planlegg arbeidsopprettelse* i rutenettet **Gjenstående metoder**.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="0d7d8-138">Velg pilen som peker mot kolonnen **Valgte metoder** for å flytte den valgte raden til denne kolonnen.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="0d7d8-139">(Du kan bare ha én valgt metode om gangen som bruker enten *WHSScheduleWorkCreationWaveStepMethod* eller *createWork*, slik at den eksisterende raden der **Metodenavn** er *createWork*, flyttes automatisk til rutenettet **Gjenstående metoder**.)</span><span class="sxs-lookup"><span data-stu-id="0d7d8-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="0d7d8-140">Angi terskeldata for behandling av bølgeoppgave</span><span class="sxs-lookup"><span data-stu-id="0d7d8-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="0d7d8-141">Systemet oppretter standard terskeldata for behandling av bølgeoppgave første gang en bølgeprosess kjører ved hjelp av oppgavebasert behandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="0d7d8-142">Dataene brukes til å styre når bølgebehandling skal kjøre asynkront og være oppgavebasert, som gjør det mulig å behandle og opprette arbeid parallelt.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="0d7d8-143">Standarddataene bruker først en terskelverdi på 15 for det minste antallet lastlinjer (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="0d7d8-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="0d7d8-144">Dette betyr at når systemet behandler en bølge med flere enn 15 lastlinjer, bruker det asynkron oppgavebehandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="0d7d8-145">Du kan sette inn / oppdatere disse dataene manuelt i tabellen **WHSWaveTaskProcessingThresholdParameters** i testmiljøet, men hvis du må endre denne innstillingen i et produksjonsmiljø, må du kontakte Microsoft Kundestøtte for å be om oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="0d7d8-146">Arbeide med funksjonen</span><span class="sxs-lookup"><span data-stu-id="0d7d8-146">Work with the feature</span></span>

<span data-ttu-id="0d7d8-147">Når funksjonen *Planlegg arbeidsopprettelse* er aktivert, oppretter bølgebehandling planlagt arbeid, som til slutt blir brukt av den nye prosessen for arbeidsopprettelse.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="0d7d8-148">Under arbeidsopprettelse blir arbeidet blokkert ved hjelp av funksjonen *Organisasjonsomfattende arbeidsblokkering*.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="0d7d8-149">Følgende flytdiagram viser hvordan planlagt arbeid blir opprettet under bølgebehandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Planlegg arbeidsoppretting](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="0d7d8-151">Planlagt arbeid</span><span class="sxs-lookup"><span data-stu-id="0d7d8-151">Planned work</span></span>

<span data-ttu-id="0d7d8-152">Siden **Detaljer om planlagt arbeid** (**Lagerstyring \> Arbeid \> Detaljer om planlagt arbeid**) viser informasjon om det planlagte arbeidet, som opprinnelig ble opprettet under bølgebehandling.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="0d7d8-153">Følgende verdier for **Prosesstatus** er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="0d7d8-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="0d7d8-154">**Satt i kø** – Det planlagte arbeidet venter på å bli brukt til å opprette arbeid.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="0d7d8-155">**Fullført** – Det planlagte arbeidet har blitt brukt til å opprette arbeid.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="0d7d8-156">**Mislykket** – Bølgebehandlingen har mislyktes.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="0d7d8-157">Merk at det planlagte arbeidet kan være i tilstanden **Mislykket** med eller uten tilknyttet faktisk arbeid.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="0d7d8-158">Når den faktiske prosessen for arbeidsopprettelse mislykkes, forblir statusen for faktisk arbeid *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="0d7d8-159">Satsvis jobb for prosessen for arbeidsopprettelse</span><span class="sxs-lookup"><span data-stu-id="0d7d8-159">Batch job for the work creation process</span></span>

<span data-ttu-id="0d7d8-160">Hvis du vil vise de satsvise jobbene for bølgebehandling, velger du **Satsvise jobber** i handlingsruten på **Alle bølger**-siden.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="0d7d8-161">Her kan du vise alle detaljene om den satsvise oppgaven for hver ID for satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="0d7d8-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]