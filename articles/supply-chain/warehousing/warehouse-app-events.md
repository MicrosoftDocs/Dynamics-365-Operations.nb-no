---
title: Lagerapphendelser
description: Dette emnet beskriver behandling av lagerapphendelser som brukes til å behandle hendelsesmeldinger for lagerappen som en del av en satsvis jobb.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d63cdea8917bed762bf8d970a408e5931aec48b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837399"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="a0a2a-103">Behandling av lagerapphendelse</span><span class="sxs-lookup"><span data-stu-id="a0a2a-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0a2a-104">Satsvise jobber som kjører i Supply Chain Management, kan bruke data fra en kø for behandling av hendelser som utstedes av mobilappen Lagerstyring, for å reagere etter behov på signaliserte hendelser.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the Warehouse Management mobile app to react as needed to the signaled events.</span></span> <span data-ttu-id="a0a2a-105">Denne funksjonen legger til relevante hendelser i køen som svar på bestemte typer handlinger utført av arbeidere ved hjelp av appen.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="a0a2a-106">Et eksempel er at når du bruker funksjonen *Opprette og behandle overføringsordre fra lagerappen*, blir overføringsordrehodet og -linjene opprettet og oppdatert i serverdelen når systemet kjører den satsvise jobben **Behandle lagerapphendelser**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-106">An example is when using the *Create and process transfer orders from the warehouse app* feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="a0a2a-107">Aktivere funksjonen Behandle lagerapphendelser</span><span class="sxs-lookup"><span data-stu-id="a0a2a-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="a0a2a-108">Før du kan bruke denne funksjonen, må du aktivere den i systemet.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="a0a2a-109">Administratorer kan bruke siden for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="a0a2a-110">Funksjonen Behandle lagerapphendelser er oppført som :</span><span class="sxs-lookup"><span data-stu-id="a0a2a-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="a0a2a-111">**Modul** – lagerstyring</span><span class="sxs-lookup"><span data-stu-id="a0a2a-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="a0a2a-112">**Funksjonsnavn** – Behandle lagerapphendelser</span><span class="sxs-lookup"><span data-stu-id="a0a2a-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="a0a2a-113">Konfigurere en satsvis jobb for å behandle lagerapphendelser</span><span class="sxs-lookup"><span data-stu-id="a0a2a-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="a0a2a-114">Behandle lagerapphendelser</span><span class="sxs-lookup"><span data-stu-id="a0a2a-114">Process warehouse app events</span></span>

<span data-ttu-id="a0a2a-115">Konfigurer en planlagt satsvis jobb for å behandle lagerapphendelsene for oppretting og linjeoppdateringer for overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="a0a2a-116">Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle lagerapphendelser**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="a0a2a-117">Dialogboksen Behandle lagerapphendelser åpnes.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="a0a2a-118">Vis hurtigfanen **Kjør i bakgrunnen**, og sett **Satsvis behandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="a0a2a-119">På hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="a0a2a-120">Dialogboksen **Definer regelmessighet** åpnes.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="a0a2a-121">Angi kjøretidsplanen etter behov for firmaet.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="a0a2a-122">Velg **OK** for å gå tilbake til dialogboksen **Behandle lagerapphendelser**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="a0a2a-123">Velg **OK** i dialogboksen **Behandle lagerapphendelser** for å legge til den satsvise jobben i den satsvise køen.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="a0a2a-124">Spørre etter lagerapphendelser</span><span class="sxs-lookup"><span data-stu-id="a0a2a-124">Query warehouse app events</span></span>

<span data-ttu-id="a0a2a-125">Du kan vise hendelseskøen og hendelsesmeldingene som genereres av mobilappen Lagerstyring, ved å gå til **Lagerstyring \> Forespørsler og rapporter \> Logger for mobilenheter \> Lagerapphendelser**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-125">You can view the event queue and events messages generated by the Warehouse Management mobile app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="a0a2a-126">Standardprosess for hendelseskø</span><span class="sxs-lookup"><span data-stu-id="a0a2a-126">The standard event queue process</span></span>

<span data-ttu-id="a0a2a-127">Køen for lagerapphendelser vil vanligvis bli brukt med følgende beskrevet flyt:</span><span class="sxs-lookup"><span data-stu-id="a0a2a-127">The warehouse app events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="a0a2a-128">En hendelse blir lagt til i køen med en hendelsesmelding.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="a0a2a-129">Den nye meldingen har i utgangspunktet hendelsestilstanden **Venter**, noe som betyr at den satsvise jobben **Behandle lagerapphendelser** ikke vil hente og behandle denne meldingen.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="a0a2a-130">Så snart meldingstilstanden er oppdatert til **I kø**, vil den satsvise jobben **Behandle lagerapphendelser** hente og behandle hendelsen.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="a0a2a-131">Den satsvise jobben oppdaterer hendelsestilstandene til **Fullført** eller **Mislykket**, avhengig av om den forespurte prosessen var mulig.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="a0a2a-132">Når alle relaterte hendelsesmeldinger er **Fullført**, slettes hendelsen fra køen.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="a0a2a-133">Hvis du vil ha et detaljert eksempel, kan du se [Opprette overføringsordre fra lagerapprosess](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="a0a2a-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="a0a2a-134">Håndtere hendelsesfeil</span><span class="sxs-lookup"><span data-stu-id="a0a2a-134">Handle event errors</span></span>

<span data-ttu-id="a0a2a-135">Som en del av behandling av lagerhendelser, kan det hende at den ønskede meldingsaktiviteten ikke mottar prosesser fra den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="a0a2a-136">I slike tilfeller blir hendelsesmeldingen endret til **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="a0a2a-137">Du kan bruke informasjonen til **loggen for den satsvise jobben** til å finne ut hvorfor og gjøre nødvendige tiltak for å løse eventuelle problemer.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="a0a2a-138">Hvis du vil ha et detaljert eksempel, kan du se [Opprette overføringsordre fra lagerapp](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="a0a2a-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="a0a2a-139">Slik tilbakestiller du en mislykket hendelsesmelding for en lagerapp:</span><span class="sxs-lookup"><span data-stu-id="a0a2a-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="a0a2a-140">Gå til **Lagerstyring \> Forespørsler og rapporter \> Loger for mobilenheter \> Lagerapphendelser**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="a0a2a-141">I hurtigfanen **Hendelsesmeldinger for lagrapp** finner du og velger en relevant hendelse som vises **Mislykket** i kolonnen **Hendelsestilstand**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="a0a2a-142">Velg **Tilbakestill** fra verktøylinjen **Hendelsesmeldinger for lagerapp**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="a0a2a-143">Fortsett å arbeide til alle relevante meldinger er tilbakestilt.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="a0a2a-144">Du kan også fjerne en **Mislykket** hendelsesmelding ved hjelp av **Slett**-alternativet på verktøylinjen **Hendelsesmeldinger for lagerapp**.</span><span class="sxs-lookup"><span data-stu-id="a0a2a-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]