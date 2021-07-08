---
title: Meldinger for meldingsprosessor
description: Dette emnet inneholder informasjon om funksjonen for meldinger for meldingsprosessor for arbeidsbelastningen for skalaenhet.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 86f15831f11dc9fdcada9639858fd3b18cdc7503
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271107"
---
# <a name="message-processor-messages"></a><span data-ttu-id="a5fc1-103">Meldinger for meldingsprosessor</span><span class="sxs-lookup"><span data-stu-id="a5fc1-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5fc1-104">Meldinger for meldingsprosessoren brukes når du kjører skalaenheter for sky og kant for [produksjonsarbeidsmengder](cloud-edge-workload-manufacturing.md) og [lagerstyringsarbeidsbelastninger](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="a5fc1-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="a5fc1-105">En stor datamengde utveksles mellom distribusjonsmiljøene for skalering og vektenhet for å holde dem synkronisert, men bare noen få av disse datautvekslingene behandles av *meldingsprosessoren*.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="a5fc1-106">Du kan vise meldingene som behandles av meldingsbehandleren, ved å gå til **Systemadministrasjon > Meldingsprosessor > Meldinger for meldingsprosessor**.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="a5fc1-107">Meldingsrutenettkolonner og -filtre</span><span class="sxs-lookup"><span data-stu-id="a5fc1-107">Message grid columns and filters</span></span>

<span data-ttu-id="a5fc1-108">Du kan bruke feltene øverst på **Meldinger for meldingsprosessor** for å finne bestemte meldinger du er på jakt etter.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="a5fc1-109">De fleste av disse filtrene samsvarer med kolonneoverskriftene i meldingsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="a5fc1-110">Følgende filtre og kolonneoverskrifter er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="a5fc1-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="a5fc1-111">**Meldingstype** – Angir meldingstypen.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="a5fc1-112">**Meldingskø** – Angir navnet på køen som meldingen skal behandles i.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="a5fc1-113">Følgende køer finnes:</span><span class="sxs-lookup"><span data-stu-id="a5fc1-113">The following queues are provided:</span></span>
  - <span data-ttu-id="a5fc1-114">*Storskalaenhet til hub*</span><span class="sxs-lookup"><span data-stu-id="a5fc1-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="a5fc1-115">*Senter til skalaenhet for lagerutførelse*</span><span class="sxs-lookup"><span data-stu-id="a5fc1-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="a5fc1-116">*Senter for skalaenhet for produksjonsutførelse*</span><span class="sxs-lookup"><span data-stu-id="a5fc1-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="a5fc1-117">**Meldingsstatus** – Angir meldingens status.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="a5fc1-118">Følgende statuser finnes:</span><span class="sxs-lookup"><span data-stu-id="a5fc1-118">The following states exists:</span></span>
  - <span data-ttu-id="a5fc1-119">*Satt i kø* – Meldingen er klar til å behandles av meldingsprosessoren.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="a5fc1-120">*Behandlet* – Meldingen ble behandlet av meldingsprosessoren.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="a5fc1-121">*Annullert* – Meldingen ble behandlet, men behandling mislyktes.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="a5fc1-122">**Meldingsinnhold** – Dette filteret utfører et fullstendig tekstsøk av meldingsinnholdet.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="a5fc1-123">(Meldingsinnhold vises ikke i rutenettet). Filteret behandler de fleste spesielle symboler (for eksempel «-») som mellomrom, og behandler alle mellomromstegn som boolske OR-operatorer.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="a5fc1-124">T=Dette betyr for eksempel at hvis du søker etter en bestemt `journalid`-verdi som er lik "USMF-123456", vil systemet finne alle meldinger som inneholder "USMF" eller "123456", som sannsynligvis vil være en lang liste.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="a5fc1-125">Derfor vil det være bedre å angi bare "123456" alene, fordi det vil gi mer spesifikke resultater.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="a5fc1-126">Eksempel på meldingstype: Be om økonomisk oppdatering av lagerjustering</span><span class="sxs-lookup"><span data-stu-id="a5fc1-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="a5fc1-127">**Meldingstypen** *Be om økonomisk oppdatering av lagerjustering* brukes for eksempel til å opprette og postere en opptellingsjournal på huben når en arbeider bruker lagerappen til å [registrere en lagerjustering](cloud-edge-warehouse-inventory-adjustment.md) på en skaleringsenhet for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="a5fc1-128">Fordi denne bestemte prosessen stammer fra en skalaenhet, vil **Meldingskø**-feltet vise verdien *Skalaenhet til senter*.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="a5fc1-129">For denne meldingstypen registrerer en skalaenhetsarbeidsmengde meldingen som en del av en beholdingsjustering av lagerapp.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="a5fc1-130">Meldingsdataene overføres deretter til senteret som en del av den samme prosessen som brukes for [Commerce Data Exchange-arkitekturen](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="a5fc1-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="a5fc1-131">Meldingen vil bli oppdatert slik at den viser **Meldingsstatus** som *I kø*.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="a5fc1-132">Meldingsbehandleren prøver deretter å behandle meldingen og oppdatere **Meldingsstatus** til *Behandlet* ved vellykket eller *Avbrutt* ved feil.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="a5fc1-133">Vise meldingslogg, meldingsinnhold og detaljer</span><span class="sxs-lookup"><span data-stu-id="a5fc1-133">View the message log, message content, and details</span></span>

<span data-ttu-id="a5fc1-134">Du kan finne detaljert informasjon om en melding ved å velge den i rutenettet og deretter åpne kategoriene **Logg** eller **Meldingsinnhold** under meldingsrutenettet, der hver behandlingshendelse vises.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="a5fc1-135">**Meldingsinnhold** er avhengig av **Meldingstype** og vil derfor ha forskjellig tekstlengde.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="a5fc1-136">En vanlig meldingsinnholdstekst starter med en **{** og slutter med en **}** og imellom har feltnavn som for eksempel `journalId` etterfulgt av en **:** og en verdi som *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="a5fc1-137">Verktøylinjen i kategorien **Logg** inneholder følgende knapper:</span><span class="sxs-lookup"><span data-stu-id="a5fc1-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="a5fc1-138">**Logg** – Viser behandlingsresultatene.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="a5fc1-139">Dette er særlig nyttig for å forstå årsakene til en behandlingsfeil for meldinger som har et **Behandlingsresultat** som er *Mislykket*.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="a5fc1-140">**Bunt** – Flere meldingsbehandlingsoperasjoner kan kjøres som en del av den samme satsvise prosessen.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="a5fc1-141">Velg denne knappen for å vise disse detaljerte dataene.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="a5fc1-142">Du kan for eksempel se om det finnes avhengigheter som krever at systemet behandler bestemte meldinger i en bestemt rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="a5fc1-143">Satsvis jobb for meldingsbehandler</span><span class="sxs-lookup"><span data-stu-id="a5fc1-143">Message processor batch job</span></span>

<span data-ttu-id="a5fc1-144">Når du kjører en sky- og kantdistribusjon, aktiveres den satsvise jobben for *Meldingsbehandler* automatisk når det opprettes en ny melding for behandling, slik at du ikke behøver å planlegge denne jobben manuelt.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="a5fc1-145">Hvis nødvendig kan du få tilgang til den satsvise jobben ved å gå til **Systemadministrasjon > Meldingsbehandling > Meldingsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="a5fc1-146">Behandle eller avbryte en melding manuelt</span><span class="sxs-lookup"><span data-stu-id="a5fc1-146">Manually process or cancel a message</span></span>

<span data-ttu-id="a5fc1-147">Om nødvendig kan du behandle eller avbryte en melding manuelt, avhengig av gjeldende status.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="a5fc1-148">Dette gjør du ved å merke meldingen i rutenettet og deretter velge **Behandle** eller **Avbryt** i handlingsruten</span><span class="sxs-lookup"><span data-stu-id="a5fc1-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="a5fc1-149">Konfigurere forretningshendelser for å levere varsler for mislykkede behandlingsresultater</span><span class="sxs-lookup"><span data-stu-id="a5fc1-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="a5fc1-150">I tillegg til å filtrere på **Meldingsstatus**-verdien *Avbrutt* for å spørre om mislykkede meldinger, kan du konfigurere [Forretningshendelser](../../fin-ops-core/dev-itpro/business-events/home-page.md) på senteret for å varsle deg om mislykkede behandlingsresultater.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="a5fc1-151">Dette gjør du ved å aktivere forretningshendelsen *Meldingsbehandlermelding som behandles* på siden for **Forretningshendelser-katalog** (**Systemadministrasjon > Oppsett > Forretningshendelser > Forretningshendelser-katalog)**.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="a5fc1-152">Som en del av aktiveringsprosessen blir du veiledet for å angi om hendelsen er spesifikk for én eller alle juridiske enheter, og angi et **sluttpunktnavn** som må defineres først.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="a5fc1-153">Hvis for eksempel **Når en forretningshendelse oppstår** er satt til *Microsoft Power Automate* (i stedet for *HTTPS*, for eksempel) vil **sluttpunktnavn** automatisk opprettes i Supply Chain Management basert på *Microsoft Power Automate*-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="a5fc1-154">Microsoft Power Automate-eksempel</span><span class="sxs-lookup"><span data-stu-id="a5fc1-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="a5fc1-155">I dette eksemplet bruk **Når en forretningshendelse oppstår** med *Microsoft Power Automate* sender e-postmeldinger som inneholder infologgmeldinger og hyperkoblinger for å åpne siden **Meldinger for meldingsprosessor** for en bestemt mislykket melding på senterdistribusjonen.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="a5fc1-156">Om nødvendig kan du legge til ekstra logikk for å sende meldingene parallelt ved hjelp av ulike kanaler og kontrollere mottakerne basert på hendelsesdataene.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="a5fc1-157">I [Power Automate](https://preview.flow.microsoft.com) oppretter du en ny automatisert skyflyt for flytutløseren **Når en forretningshendelse oppstår – Fin & Ops App (Dynamics 365)** etterfulgt av trinnene **Parse JSON** og **Sende en e-post**, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automatisert skyflyt":::

1. <span data-ttu-id="a5fc1-159">I trinnet **Når en forretningshendelse oppstår** kan du slå opp eller angi huben **Forekomst** etterfulgt av **Kategori** og deretter **Forretningshendelse** *Meldingsbehandlermelding som behandles*, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Når en forretningshendelse oppstår":::

1. <span data-ttu-id="a5fc1-161">I trinnet **Parse JSON** angir du et **Skjema** som deinferer de utvidede feltene.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="a5fc1-162">Du kan bruke alternativet *Last ned skjema* på siden **Forretningshendelser-katalog** i Supply Chain Management, eller du kan begynne med å lime inn eksempelskjemateksten.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="a5fc1-163">Denne eksempelteksten vises etter følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Parse JSON-trinn":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="a5fc1-165">I trinnet **Send en e-post** kan du velge enkeltfeltene eller begynne ved å lime inn eksempelet med e-postteksten i **Meldingstekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="a5fc1-166">Dette eksemplet vises etter følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate send en e-post-trinnet":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="a5fc1-168">Når du lagrer forretningshendelsen, aktiveres den automatisk og er klar til å brukes som en del av Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5fc1-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
