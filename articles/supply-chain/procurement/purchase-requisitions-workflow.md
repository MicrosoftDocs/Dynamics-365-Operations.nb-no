---
title: Arbeidsflyten for innkjøpsrekvisisjon
description: Arbeidsflytprosessen flytter innkjøpsrekvisisjoner gjennom vurderingsprosessen, fra den innledende statusen Utkast til den endelige statusen Godkjent. Når en innkjøpsrekvisisjon sendes til gjennomgang, starter arbeidsflytprosessen. Når en innkjøpsrekvisisjon er godkjent, kan en bestilling genereres for innkjøpsrekvisisjonslinjene og sendes til leverandøren for å bli oppfylt.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a9dceb3f9e71163dcaf8b8763317110ef019844
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434254"
---
# <a name="purchase-requisition-workflow"></a>Arbeidsflyten for innkjøpsrekvisisjon

[!include [banner](../includes/banner.md)]

Arbeidsflytprosessen flytter innkjøpsrekvisisjoner gjennom vurderingsprosessen, fra den innledende statusen Utkast til den endelige statusen Godkjent. Når en innkjøpsrekvisisjon sendes til gjennomgang, starter arbeidsflytprosessen. Når en innkjøpsrekvisisjon er godkjent, kan en bestilling genereres for innkjøpsrekvisisjonslinjene og sendes til leverandøren for å bli oppfylt.

Før en innkjøpsrekvisisjon kan sendes til gjennomgang, må en arbeidsflyt konfigureres. Arbeidsflytprosessen kan inneholde ett eller flere gjennomgangstrinn i en hvilken som helst rekkefølge. Arbeidsflytprosessen kan også konfigureres slik at den hopper over gjennomgangsoppgavene og godkjenner innkjøpsrekvisisjonen automatisk. Du kan konfigurere arbeidsflyten til å sende innkjøpsrekvisisjonen som ett enkelt dokument, eller du kan distribuere individuelle innkjøpsrekvisisjonslinjene til de riktige kontrollørene. Du kan også opprette et scenario der innkjøpsrekvisisjonen rutes som ett dokument til noen kontrollører, og valgte innkjøpsrekvisisjonslinjer rutes til andre kontrollører.  

Hvis innkjøpsrekvisisjonslinjene vurderes enkeltvis, må vurderingsprosessen fullføres for alle innkjøpsrekvisisjonslinjene før arbeidsflyten kan gå til neste trinn i arbeidsflytprosessen, og før vurderingsprosessen for innkjøpsrekvisisjonen i sin helhet kan fullføres. Når innkjøpsrekvisisjonen, inkludert alle linjer, har gått gjennom vurderingsprosessen, oppdateres den overordnede statusen for innkjøpsrekvisisjonen til **Godkjent**.  

Du kan konfigurere arbeidsflyten slik at den representerer forretningsprosessen for innkjøpsrekvisisjonene i organisasjonen. Vurder følgende spørsmål når du konfigurerer arbeidsflytprosessen for innkjøpsrekvisisjon:

-   Hvilke utgifter må gjennomgås?
-   Hvilke utgifter kan godkjennes automatisk?
-   Hvem må gå gjennom og godkjenne utgiftsforespørsler? Hvilken rolle er disse brukerne tilordnet?
-   Hvilken prosess må følges hvis kontrolløren ikke er tilgjengelig?

Eksemplene nedenfor viser to måter du kan konfigurere en arbeidsflyt for innkjøpsrekvisisjoner på.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Eksempel 1: Rute en innkjøpsrekvisisjon som ett dokument til gjennomgang
Illustrasjonen nedenfor viser hvordan en innkjøpsrekvisisjon kan flyte gjennom vurderingsprosessen som ett dokument. Linjene i innkjøpsrekvisisjonen rutes ikke enkeltvis. I dette eksemplet er følgende roller inkludert i arbeidsflytprosessen:

-   **Bestiller** – brukeren som ber om varene eller tjenestene. Bestilleren kan klargjøre innkjøpsrekvisisjonen, eller en annen arbeider kan klargjøre innkjøpsrekvisisjonen på vegne av bestilleren. Denne arbeideren er klargjøreren. Klargjøreren er ansvarlig for å behandle innkjøpsrekvisisjonen gjennom hele vurderingsprosessen. Bare klargjøreren for innkjøpsrekvisisjonen kan endre den.

**Obs!** En arbeider må få de nødvendige tillatelsene til å opprette en innkjøpsrekvisisjon på vegne av noen andre. Bruk siden **Tillatelse for innkjøpsrekvisisjon** til å definere disse tillatelsene.

-   **Innkjøpsagent** – brukeren som foretar en gjennomgang av innkjøp og kan godkjenne dokumentet.
-   **Bestillerens leder** – brukeren som foretar en ledergjennomgang og kan se gjennom og godkjenne dokumentet.

![Vurderingsprosess for arbeidsflyt for innkjøpsrekvisisjon](./media/purchreqworkflowoverview_submission.gif)  
I dette eksemplet omfatter arbeidsflytprosessen for innkjøpsrekvisisjonen følgende trinn:

1.  Klargjøreren sender en innkjøpsrekvisisjon til gjennomgang.
2.  Innkjøpsagenten mottar en melding. Varslingen ber innkjøpsagenten om å kontrollere informasjonen i innkjøpsrekvisisjonen. Hvis det mangler nødvendig informasjon, kan innkjøpsagenten legge til informasjonen eller returnere innkjøpsrekvisisjonen til klargjøreren for å få den lagt til. Når all nødvendig informasjon er fylt ut, kan innkjøpsrekvisisjonen flyttes videre til neste trinn i vurderingsprosessen.
3.  Bestillerens leder går gjennom innkjøpsrekvisisjonen. Innkjøpsrekvisisjonen kan for eksempel rutes til bestillerens leder hvis beløpet i innkjøpsrekvisisjonen overskrider bestillerens forbruksgrense for innkjøpsrekvisisjoner. Bestillerens leder kan godkjenne eller avvise innkjøpsrekvisisjonen eller returnere den til klargjøreren for å få den endret.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Eksempel 2: Rute enkeltlinjer i innkjøpsrekvisisjonen til gjennomgang
Illustrasjonen nedenfor viser hvordan enkeltlinjene i innkjøpsrekvisisjonen kan rutes gjennom arbeidsflyten. Prosessen for hver linje er vanligvis lik prosessen for en innkjøpsrekvisisjon som gås gjennom som ett dokument. Hver linje må imidlertid gå gjennom hele arbeidsflytprosessen enkeltvis før arbeidsflyten kan fullføres for innkjøpsrekvisisjonen i sin helhet.  

I dette eksemplet registrerer en arbeider en forespørsel om plakater og t-skjorter for en markedsføringskampanje. Kostnaden for plakatene deles mellom markedsføringsavdelingen og salgsavdelingen. Hvis kostnaden for plakater eller t-skjorter overskrider signeringsgrensefullmakten til avdelingsledere, må gruppelederen også gå gjennom innkjøpsrekvisisjonen.  

I dette eksemplet er følgende roller inkludert i arbeidsflytprosessen:

-   **Bestiller** – brukeren som ber om varene eller tjenestene. Bestilleren kan klargjøre innkjøpsrekvisisjonen, eller en annen arbeider kan klargjøre innkjøpsrekvisisjonen på vegne av bestilleren. Denne arbeideren er klargjøreren. Klargjøreren er ansvarlig for å behandle innkjøpsrekvisisjonen gjennom hele vurderingsprosessen. Bare klargjøreren for innkjøpsrekvisisjonen kan endre den.

**Obs!** En arbeider må få de nødvendige tillatelsene til å opprette en innkjøpsrekvisisjon på vegne av noen andre. Bruk siden **Tillatelse for innkjøpsrekvisisjon** til å definere disse tillatelsene.

-   **Innkjøpsagent** – brukeren som foretar en gjennomgang av innkjøp og kan godkjenne dokumentet.
-   **Bestillerens leder** – brukeren som foretar en ledergjennomgang og kan se gjennom og godkjenne dokumentet.
-   **Avdelingsleder** – brukeren som foretar en utgiftsgjennomgang og kan se gjennom og godkjenne dokumentet.
-   **Gruppeleder** – brukeren som foretar en signaturfullmaktsgjennomgang og kan se gjennom og godkjenne dokumentet.

![Vurderingsprosess for arbeidsflyt for innkjøpsrekvisisjonslinje](./media/purchreqlineworkflowoverview.gif)  
I dette eksemplet omfatter arbeidsflytprosessen for innkjøpsrekvisisjonslinjene følgende trinn:

1.  Klargjøreren sender en innkjøpsrekvisisjon til gjennomgang. Hver linje rutes til kontrolløren som er konfigurert til å motta den i arbeidsflytprosessen.
2.  Innkjøpsagenten mottar en melding. I varslingen bes innkjøpsagenten om å kontrollere informasjonen i innkjøpsrekvisisjonen og innkjøpsrekvisisjonslinjene. Når innkjøpsrekvisisjonen åpnes av innkjøpsagenten, vises alle linjene, men en visuell indikator viser hvilke linjer som er sendt til innkjøpsagenten for gjennomgang. Hvis det mangler nødvendig informasjon, kan innkjøpsagenten legge til informasjonen eller returnere en innkjøpsrekvisisjonslinje til klargjøreren for å få den lagt til. Når all nødvendig informasjon er fylt ut, kan innkjøpsrekvisisjonslinjen flyttes videre til neste trinn i vurderingsprosessen. Innkjøpsrekvisisjonslinjer kan fortsette gjennom vurderingsprosessen uavhengig av hverandre.
3.  Bestillerens linjeleder går gjennom og godkjenner innkjøpsrekvisisjonslinjene. Godkjenningen kan for eksempel rutes til bestillerens leder hvis beløpet på en innkjøpsrekvisisjonslinje overskrider bestillerens forbruksgrense for innkjøpsrekvisisjonslinjer. Lederen kan godkjenne eller avvise den ene av eller begge innkjøpsrekvisisjonslinjene.
4.  Avdelingslederen for markedsføringsavdelingen går gjennom innkjøpsrekvisisjonslinjene for både plakatene og t-skjortene. Salgsavdelingslederen går gjennom innkjøpsrekvisisjonslinjen bare for plakatene fordi det er den eneste kostnaden salgsavdelingen blir belastet med.
5.  Gruppelederen går gjennom og godkjenner innkjøpsrekvisisjonslinjen for t-skjortene bare hvis det kreves godkjenning av gruppeleder. Dette kan for eksempel være at beløpet på innkjøpsrekvisisjonslinjen overskrider avdelingslederens godkjenningsgrense. Gruppelederen trenger ikke å godkjenne innkjøpsrekvisisjonslinjene for plakatene.

> [!NOTE]
> Systemvalutaen må angis hvis hodearbeidsflyten for en innkjøpsrekvisisjon krever godkjenninger knyttet til signeringsgrenser.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Konfigurere en arbeidsflyt for innkjøpsrekvisisjoner
Hvis du vil rute en innkjøpsrekvisisjon til gjennomgang, må du konfigurere arbeidsflytprosessene for innkjøpsrekvisisjon. Arbeidsflytprosessen du definerer, styrer interaksjonen mellom brukeren som bad om varene (bestilleren), og kontrolløren og godkjenneren i arbeidsflyten. Ruting av innkjøpsrekvisisjonen avhenger av hvilke betingelser som angis i arbeidsflytkonfigurasjonen. Disse betingelsene bestemmer for eksempel når innkjøpsrekvisisjonen skal rutes, brukeren eller rollen som den skal sendes til, og handlingene som brukere kan utføre.  

Eksemplene i dette emnet viser hvordan en innkjøpsrekvisisjon kan rutes gjennom en arbeidsflyt som ett dokument eller som enkeltlinjer i innkjøpsrekvisisjonen. Du kan også konfigurere en arbeidsflyt for innkjøpsrekvisisjoner som gjenspeiler den interne kontrollgjennomgangen av innkjøpsrekvisisjoner som er definert for organisasjonen.  

Deltakerne eller kontrollørene som er tilordnet en oppgave i en arbeidsflyt, kan være medlemmer av en bestemt brukergruppe, brukere som har en bestemt sikkerhetsrolle, brukere som er knyttet til avsenderen i et lederhierarki, eller navngitte brukere eller brukere som har ansvar for bestemte utgifter.

### <a name="purchase-requisition-expenditure-reviewers"></a>Kontrollører av innkjøpsrekvisisjonsutgifter

Du kan definere konfigurasjoner for utgiftskontrollør for å sende utgifter til gjennomgang dynamisk, basert på brukeren som er tilordnet til en prosjektrolle eller en finansdimensjon der utgiften belastes. Arbeidsflytprosessen bruker den angitte eieren av prosjektrollen eller finansdimensjonen til å avgjøre hvem utgiften skal sendes til.  

Du kan definere én eller flere konfigurasjoner for utgiftskontrollør og deretter velge en konfigurasjon når du oppretter en arbeidsflyt. Du kan konfigurere verdiene for utgiftskontrollør for hver juridisk enhet i organisasjonen. Når du har definert konfigurasjonene for utgiftskontrollør, tilordner du konfigurasjonen til arbeidsflytoppgaven.  

Du trenger ikke å definere en konfigurasjon for utgiftskontrollør. Du kan i stedet tilordne bestemte brukere eller brukergrupper som kontrollører når du definerer arbeidsflyten. Hvis du imidlertid har en kompleks organisasjon, kan du øke effektiviteten til godkjenningsprosessen når du angir utgiftskontrollører. Hvis du setter opp utgiftskontrollører, trenger du heller ikke oppdatere kontrollørtilordningene for arbeidsflyt hver gang en kontrollør skifter jobbrolle.  

Du kan definere utgiftskontrollører på siden **Kontrollører av innkjøpsrekvisisjonsutgifter**. Opprett en konfigurasjon for utgiftskontrollør, og angi verdiene for hver juridiske enhet i organisasjonen. For rekvisisjoner som er tilordnet til et prosjekt, kan du angi hvilken rolle som er ansvarlig for å se gjennom rekvisisjonene: prosjektleder, prosjektkontroller eller prosjektsalgssjef. Utgifter sendes til brukeren som er tilordnet til den angitte rollen. Du kan også sende utgiften til eieren av finansdimensjonen ved å merke av for den aktuelle finansdimensjonen i kategorien **Organisasjonsdistribusjoner**.  

Hvis du vil bruke en av utgiftskontrollørene som du definerer i en arbeidsflyt, må du angi alternativet **Type deltaker** til **Utgiftsdeltakere** i **Tildeling**-egenskapene for det aktuelle arbeidsflytelementet.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Opprette en rekvisisjon for forbruk](tasks/create-requisition-consumption.md)

[Definere arbeidsflyter for forretningsprosesser for innkjøpsrekvisisjoner](https://www.microsoft.com/download/details.aspx?id=101821)

[Arbeidsflyter for innkjøp og leverandører](procurement-sourcing-workflows.md)

[Oversikt over innkjøpsrekvisisjon](purchase-requisitions-overview.md)



