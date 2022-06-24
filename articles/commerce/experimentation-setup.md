---
title: Konfigurere et eksperiment
description: Denne artikkelen beskriver hvordan konfigurerer et eksperiment i en tredjepartstjeneste.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946172"
---
# <a name="set-up-an-experiment"></a>Konfigurere et eksperiment

Når du [definerer en hypotese og fastslår hvilke suksessmåledata du vil bruke](experimentation-identify.md), må du konfigurere eksperimentet i tredjepartstjenesten. Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate artikler.

[ ![Brukerreise for eksperimentering – konfigurere.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Konfigurere eksperimentet i tredjepartstjenesten
Nå bør du ha valgt tredjepartstjenesten for å kjøre og overvåke eksperimentet og konfigurert eksperimenteringskoblingen. Disse forutsetningene er oppført i [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).

Følg trinnene som er nødvendige for å opprette eksperimentet i tredjepartstjenesten. Hvis koblingen er riktig konfigurert, vil den fullstendige listen over eksperimenter du konfigurerer i tredjepartstjenesten, vises i Commerce-områdebygger i løpet av omtrent 5 minutter.

## <a name="set-up-your-success-metrics"></a>Konfigurere suksessmåledata
Alle eksperimenter trenger måledata for å måle virkningen av variasjonene og validere hypotesen. Følg fremgangsmåten nedenfor for å aktivere beregningen av måledataene i tredjepartstjenesten ved hjelp av hendelser fra livetelemetrihendelser fra Dynamics 365 Commerce.

Gjør følgende for å konfigurere suksessmåledataene for de medfølgende modulene.

1. I Commerce-områdebygger velger du kategorien **Sider** i venstre navigasjonsrute, og deretter velger du siden du vil samle inn måledata for. 
1. Gå til delen **Hendelses-ID-er som skal spores** i egenskapsruten til høyre for siden eller modulen du vil spore.
1. Velg **Vis**. Det vises en liste over alle ID-er for klikkhendelser. Kopier hendelsen du vil spore, og lim inn hendelsesnøkkelen i den angitte plasseringen i tredjepartstjenesten. Hvis du trenger mer enn én hendelse, kopierer du nøklene én om gangen. 
1. For sidevisninger bruker du SHA-256-nummerverdien for sidenavnet i områdekonfiguratoren som er tilføyd med `.PageView`. Hendelses-ID-en for `Homepage.PageView` kan for eksempel være `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Utfør eventuelle andre trinn for å spore måledata som kreves i tredjepartstjenesten.

Følg denne fremgangsmåten for å instrumentere klikkhendelsene for egendefinerte modulklikk:

1. Klargjør et **TelemetryContent**-objekt for modulen ved hjelp av funksjonen nedenfor. Denne funksjonen tar sidenavnet, modulnavnet og det SDK-angitte standard telemetriobjektet som inndata.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Nedenfor finner du et eksempel: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Opprett nyttelastdataene som inneholder informasjon om hva som må registreres. For knapper og andre statiske kontroller kan du inkludere **tekst**, som for eksempel "Kjøp nå" eller "Søk". Og for komponenter med klikk, for eksempel klikke på et produktkort, kan du sende **recid**, som er post-ID-en til produktet eller produkt-ID-en.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Som et eksempel for statiske kontroller kan du sende knappetekststrengen som vist nedenfor:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Som et eksempel på produktklikk kan du sende recordId for produktet som vist nedenfor:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Kall opp **OnClick**-funksjonen for å registrere hendelsen.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Nedenfor finner du et eksempel:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Forrige trinn
[Identifisere en hypotese og fastslå måledataene for et eksperiment](experimentation-identify.md) 


## <a name="next-step"></a>Neste trinn
[Koble til og redigere et eksperiment](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
