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
# <a name="message-processor-messages"></a>Meldinger for meldingsprosessor

[!include [banner](../includes/banner.md)]

Meldinger for meldingsprosessoren brukes når du kjører skalaenheter for sky og kant for [produksjonsarbeidsmengder](cloud-edge-workload-manufacturing.md) og [lagerstyringsarbeidsbelastninger](cloud-edge-workload-warehousing.md).

En stor datamengde utveksles mellom distribusjonsmiljøene for skalering og vektenhet for å holde dem synkronisert, men bare noen få av disse datautvekslingene behandles av *meldingsprosessoren*. Du kan vise meldingene som behandles av meldingsbehandleren, ved å gå til **Systemadministrasjon > Meldingsprosessor > Meldinger for meldingsprosessor**.

## <a name="message-grid-columns-and-filters"></a>Meldingsrutenettkolonner og -filtre

Du kan bruke feltene øverst på **Meldinger for meldingsprosessor** for å finne bestemte meldinger du er på jakt etter. De fleste av disse filtrene samsvarer med kolonneoverskriftene i meldingsrutenettet. Følgende filtre og kolonneoverskrifter er tilgjengelige:

- **Meldingstype** – Angir meldingstypen.
- **Meldingskø** – Angir navnet på køen som meldingen skal behandles i. Følgende køer finnes:
  - *Storskalaenhet til hub*
  - *Senter til skalaenhet for lagerutførelse*
  - *Senter for skalaenhet for produksjonsutførelse*
- **Meldingsstatus** – Angir meldingens status. Følgende statuser finnes:
  - *Satt i kø* – Meldingen er klar til å behandles av meldingsprosessoren.
  - *Behandlet* – Meldingen ble behandlet av meldingsprosessoren.
  - *Annullert* – Meldingen ble behandlet, men behandling mislyktes.
- **Meldingsinnhold** – Dette filteret utfører et fullstendig tekstsøk av meldingsinnholdet. (Meldingsinnhold vises ikke i rutenettet). Filteret behandler de fleste spesielle symboler (for eksempel «-») som mellomrom, og behandler alle mellomromstegn som boolske OR-operatorer. T=Dette betyr for eksempel at hvis du søker etter en bestemt `journalid`-verdi som er lik "USMF-123456", vil systemet finne alle meldinger som inneholder "USMF" eller "123456", som sannsynligvis vil være en lang liste. Derfor vil det være bedre å angi bare "123456" alene, fordi det vil gi mer spesifikke resultater.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Eksempel på meldingstype: Be om økonomisk oppdatering av lagerjustering

**Meldingstypen** *Be om økonomisk oppdatering av lagerjustering* brukes for eksempel til å opprette og postere en opptellingsjournal på huben når en arbeider bruker lagerappen til å [registrere en lagerjustering](cloud-edge-warehouse-inventory-adjustment.md) på en skaleringsenhet for lagerstyring. Fordi denne bestemte prosessen stammer fra en skalaenhet, vil **Meldingskø**-feltet vise verdien *Skalaenhet til senter*.

For denne meldingstypen registrerer en skalaenhetsarbeidsmengde meldingen som en del av en beholdingsjustering av lagerapp. Meldingsdataene overføres deretter til senteret som en del av den samme prosessen som brukes for [Commerce Data Exchange-arkitekturen](../../commerce/commerce-architecture.md). Meldingen vil bli oppdatert slik at den viser **Meldingsstatus** som *I kø*. Meldingsbehandleren prøver deretter å behandle meldingen og oppdatere **Meldingsstatus** til *Behandlet* ved vellykket eller *Avbrutt* ved feil.

## <a name="view-the-message-log-message-content-and-details"></a>Vise meldingslogg, meldingsinnhold og detaljer

Du kan finne detaljert informasjon om en melding ved å velge den i rutenettet og deretter åpne kategoriene **Logg** eller **Meldingsinnhold** under meldingsrutenettet, der hver behandlingshendelse vises.

**Meldingsinnhold** er avhengig av **Meldingstype** og vil derfor ha forskjellig tekstlengde. En vanlig meldingsinnholdstekst starter med en **{** og slutter med en **}** og imellom har feltnavn som for eksempel `journalId` etterfulgt av en **:** og en verdi som *USMF-123456*.

Verktøylinjen i kategorien **Logg** inneholder følgende knapper:

- **Logg** – Viser behandlingsresultatene. Dette er særlig nyttig for å forstå årsakene til en behandlingsfeil for meldinger som har et **Behandlingsresultat** som er *Mislykket*.
- **Bunt** – Flere meldingsbehandlingsoperasjoner kan kjøres som en del av den samme satsvise prosessen. Velg denne knappen for å vise disse detaljerte dataene. Du kan for eksempel se om det finnes avhengigheter som krever at systemet behandler bestemte meldinger i en bestemt rekkefølge.

## <a name="message-processor-batch-job"></a>Satsvis jobb for meldingsbehandler

Når du kjører en sky- og kantdistribusjon, aktiveres den satsvise jobben for *Meldingsbehandler* automatisk når det opprettes en ny melding for behandling, slik at du ikke behøver å planlegge denne jobben manuelt.

Hvis nødvendig kan du få tilgang til den satsvise jobben ved å gå til **Systemadministrasjon > Meldingsbehandling > Meldingsbehandling**.

## <a name="manually-process-or-cancel-a-message"></a>Behandle eller avbryte en melding manuelt

Om nødvendig kan du behandle eller avbryte en melding manuelt, avhengig av gjeldende status. Dette gjør du ved å merke meldingen i rutenettet og deretter velge **Behandle** eller **Avbryt** i handlingsruten

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Konfigurere forretningshendelser for å levere varsler for mislykkede behandlingsresultater

I tillegg til å filtrere på **Meldingsstatus**-verdien *Avbrutt* for å spørre om mislykkede meldinger, kan du konfigurere [Forretningshendelser](../../fin-ops-core/dev-itpro/business-events/home-page.md) på senteret for å varsle deg om mislykkede behandlingsresultater. Dette gjør du ved å aktivere forretningshendelsen *Meldingsbehandlermelding som behandles* på siden for **Forretningshendelser-katalog** (**Systemadministrasjon > Oppsett > Forretningshendelser > Forretningshendelser-katalog)**.

Som en del av aktiveringsprosessen blir du veiledet for å angi om hendelsen er spesifikk for én eller alle juridiske enheter, og angi et **sluttpunktnavn** som må defineres først.

>[!NOTE]
> Hvis for eksempel **Når en forretningshendelse oppstår** er satt til *Microsoft Power Automate* (i stedet for *HTTPS*, for eksempel) vil **sluttpunktnavn** automatisk opprettes i Supply Chain Management basert på *Microsoft Power Automate*-oppsettet.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate-eksempel

I dette eksemplet bruk **Når en forretningshendelse oppstår** med *Microsoft Power Automate* sender e-postmeldinger som inneholder infologgmeldinger og hyperkoblinger for å åpne siden **Meldinger for meldingsprosessor** for en bestemt mislykket melding på senterdistribusjonen. Om nødvendig kan du legge til ekstra logikk for å sende meldingene parallelt ved hjelp av ulike kanaler og kontrollere mottakerne basert på hendelsesdataene.

1. I [Power Automate](https://preview.flow.microsoft.com) oppretter du en ny automatisert skyflyt for flytutløseren **Når en forretningshendelse oppstår – Fin & Ops App (Dynamics 365)** etterfulgt av trinnene **Parse JSON** og **Sende en e-post**, som vist i illustrasjonen nedenfor.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automatisert skyflyt":::

1. I trinnet **Når en forretningshendelse oppstår** kan du slå opp eller angi huben **Forekomst** etterfulgt av **Kategori** og deretter **Forretningshendelse** *Meldingsbehandlermelding som behandles*, som vist i illustrasjonen nedenfor.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Når en forretningshendelse oppstår":::

1. I trinnet **Parse JSON** angir du et **Skjema** som deinferer de utvidede feltene. Du kan bruke alternativet *Last ned skjema* på siden **Forretningshendelser-katalog** i Supply Chain Management, eller du kan begynne med å lime inn eksempelskjemateksten. Denne eksempelteksten vises etter følgende illustrasjon.

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

1. I trinnet **Send en e-post** kan du velge enkeltfeltene eller begynne ved å lime inn eksempelet med e-postteksten i **Meldingstekst**-feltet. Dette eksemplet vises etter følgende illustrasjon.

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

1. Når du lagrer forretningshendelsen, aktiveres den automatisk og er klar til å brukes som en del av Supply Chain Management.
