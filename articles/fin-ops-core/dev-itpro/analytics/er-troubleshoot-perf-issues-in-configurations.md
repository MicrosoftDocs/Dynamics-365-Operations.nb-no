---
title: Feilsøke ytelsesproblemer i ER-konfigurasjoner
description: Denne artikkelen beskriver hvordan du finner og retter ytelsesproblemer i ER-konfigurasjoner (elektronisk rapportering).
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 28ff68309bad7a6c1b6009ba03ef4b20aceb5194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847347"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Feilsøke ytelsesproblemer i ER-konfigurasjoner

Denne artikkelen forklarer hvordan du løser ytelsesproblemer i ER-[konfigurasjoner](general-electronic-reporting.md#Configuration) ([elektronisk rapportering](general-electronic-reporting.md)).

Ytelsesundersøkelser består vanligvis av flere trinn.

1. [Samle inn](#collecting-data) data.
2. Analyser de innsamlede dataene.
3. Bruk ER-konfigurasjoner til å [gjøre endringer](#making-changes) basert på resultatene av analysen, eller bestem deg for å samle inn flere data.

## <a name="troubleshooting"></a>Feilsøking

### <a name="analyze-execution-time"></a>Analysere kjøretid

Kjøretiden kan avhenge av uforutsigbare faktorer, for eksempel andre oppgaver som kjører i samme miljø, og hurtigbufring som bruker data når den kalles opp for første gang. Du må derfor gjenta kjøringen og målingen flere ganger.

Noen ganger skyldes ikke ytelsesproblemer en ER-formatkonfigurasjon som brukes til rapportering. De skyldes i stedet X++-koden som brukes til å åpne denne ER-formatkonfigurasjonen.

1. Se på kjøretiden for rapporten i [handlingssenteret](#infolog-time) eller [hendelsesloggen](#event-log-time).
2. Sammenlign kjøretiden for rapporten med den totale kjøretiden i scenarioet.
3. Hvis kjøretiden for rapporten er mye kortere enn den totale kjøretiden, må du ta hensyn til mengden data som rapporten behandler:

    - Hvis rapporten behandler en liten mengde data, kan problemet ha å gjøre med innlastingstiden til konfigurasjonen.
    - Hvis rapporten behandler en stor mengde data, kan problemet ha å gjøre med forhåndsbehandling av X++. Bruk [Trace Parser](#analyze-trace-parser-trace) til å analysere dette tilfellet.

    Når det gjelder andre tilfeller, kan du se de neste delene.

4. Kjør flere tester som omfatter ulike datamengder, slik at du kan finne ut hvordan kjøretiden avhenger av datamengden.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Analysere Trace Parser-sporinger

Klargjør et lite eksempel, eller samle inn flere sporinger under tilfeldige deler av rapportgenereringen.

I [Trace Parser](#trace-parser) kan du deretter foreta en standard bunn-til-topp-analyse og svare på følgende spørsmål:

- Hva er de beste metodene når det gjelder tidsforbruk?
- Hvilken del av totaltiden bruker disse metodene?

Svar på de samme spørsmålene for spørringer.

Hvis du ser at metoder har prefikset «ER», kan du gå videre til neste del.

Hvis du ser at metoder eller spørringer stammer fra programserien, vurderer du generiske optimaliseringer (for eksempel ved å opprette indekser).

Analyser antall oppkall. Hvis antallet er betydelig høyere enn forventet, vurderer du å hurtigbufre de tilsvarende nodene for konfigurasjonen.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Analysere databaseoppkall

Gjør klart et eksempel som har en liten mengde data, slik at du kan samle inn en [ER-sporing](#electronic-reporting-traces).

Åpne deretter sporingen i ER-utforming av modelltilordning, og se nederst på siden. Svar på følgende spørsmål:

- Skjer det noen spørringsduplisering? Hvis det gjør det, vurderer du en av følgende rettelser:

    - [Bruk hurtigbufring](#use-caching) hvis du tror at det er flere oppkall i én overordnet post.
    - [Bruk et hurtigbufret, parameterisert beregnet felt](#cached-parameterized) hvis du tror at det er oppkall til samme post i ulike poster.
    - [Bruk en **JOIN**-datakilde](#use-join-datasource) hvis du må lese til et stort antall ulike poster fra en database.

- Svarer antall spørringer og hentede poster til den totale datamengden? Hvis et dokument for eksempel har 10 linjer, viser statistikken at rapporten henter 10 linjer eller 1 000 linjer? Hvis du har et betydelig antall hentede poster, vurderer du en av følgende rettelser:

    - [Bruk **FILTER**-funksjonen i stedet for **WHERE**-funksjonen](#filter) til å behandle data på Microsoft SQL Server-siden.
    - Bruk hurtigbufring til å unngå at de samme dataene hentes.
    - [Bruk funksjoner for innsamlede data](#collected-data) til å unngå å hente de samme dataene til summering.

### <a name="analyze-perfview-traces"></a>Analysere PerfView-sporinger

[PerfView](#perfview) er et verktøy for erfarne utviklere. Hvis du vil ha mer detaljert informasjon om følgende trinn, kan du se [Grunnleggende om undersøkelse i veggklokketid](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Samle inn en sporing ved hjelp av trådtid.
2. Ta bare med stakker som bruker **runUnattended**, for å filtrere tråden som har konfigurasjonskjøring. (Legg til **runUnattended** i inndataboksen **IncPats**.)
3. Fold all CPU-tid, nettverkstid og blokkert tid.
4. Last inn [ER-forhåndsinnstillinger for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Velg **ER** \> **Annen forhåndsinnstilling**.
6. Se på navnene:

    - Du kommer sannsynligvis til å se plattformkoden som bruker mest tid.
    - Du kan dobbelttrykke (eller dobbeltklikke) og gå opp gjennom **oppkallere**.

        Hvis du finner klasser som har prefikset «ERExpression», og hvis de er funksjoner som er knyttet til formler, kan du gjette funksjonsnavnet basert på klassenavnet, og du kan se på ER-repositoriet for å vise attributtene.

### <a name="fixes"></a>Rettelser

- Hvis du ser at mesteparten av CPU-tiden brukes på spørringer, prøver du å redusere antall spørringer:

    - [Se gjennom ER-sporingen](#analyze-database-calls) etter dupliserte spørringer.
    - Se hvor mange poster som er hentet, og vurder hvor mye data som teoretisk skulle vært hentet.

- Hvis du ser at mesteparten av CPU-tiden brukes av funksjonene som brukes, prøver du å finne ut hvor i konfigurasjonen mesteparten av ressursene brukes.
- Hvis du ser at mesteparten av CPU-tiden brukes av funksjonene for datainnsamling, vurderer du å erstatte dem med *SQL-setningsdelen GROUP BY* på modelltilordningssiden.

### <a name="collecting-data"></a><a name="collecting-data"></a>Samle inn data

Du kan samle inn tilgjengelige data på flere ulike måter, avhengig av miljøet ditt:

- Få den totale kjøretiden:

    - fra handlingssenteret
    - fra hendelsesloggen

- Profiler kjøringen:

    - ved å bruke ER-verktøy
    - ved å bruke Trace Parser
    - ved å bruke PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Samle inn data i et produksjonsmiljø

Noen ganger kan problemer bare reproduseres i et produksjonsmiljø. Du kan samle inn data på følgende måter:

- ved å bruke [Trace Parser](../perf-test/trace-trace-tutorial.md)-sporinger
- ved å bruke [ER-kjørings](trace-execution-er-troubleshoot-perf.md)sporinger
- ved å bruke den totale kjøringstiden

#### <a name="collecting-data-in-a-development-environment"></a>Samle inn data i et utviklingsmiljø

I tillegg til verktøyene som kan brukes i et produksjonsmiljø, finnes det flere verktøy du kan bruke i et utviklingsmiljø:

- Hendelseslogg (Microsoft-Dynamics-ElectronicReporting). Denne loggen kan gi deg den totale kjøretiden.
- Vanlige .NET-verktøy, for eksempel PerfView.

Et utviklingsmiljø gir deg i tillegg større fleksibilitet til å eksperimentere. Du kan for eksempel deaktivere deler av rapporter for å se hvordan kjøringstiden påvirkes.

### <a name="tools"></a><a name="tools"></a>Verktøy

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Kjøringstiden i handlingssenteret

ER kan vise kjøringstiden for konfigurasjonen i handlingssenteret. Dette alternativet fungerer bare for en bestemt bruker og et bestemt firma, og bare for interaktive økter. Følg denne fremgangsmåten for å gjøre denne funksjonen tilgjengelig.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett alternativet **Vis filgenereringstid** til **Ja** i dialogboksen **Brukerparametere**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Kjøringstiden i hendelsesloggen

1. Åpne Windows Hendelsesliste.
2. Åpne **Microsoft-Dynamics-ElectronicReporting/Operational** under **Program- og tjenestelogger**.
3. Se etter **FormatMapingRun**-hendelser der **EventID=2** siden disse hendelsene inneholder informasjon om tidsforbruk.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Trace Parser-sporinger 

Siden ER implementeres i X++, kan du bruke vanlige X++-verktøy til å analysere ytelsen. Hvis du vil ha mer informasjon, kan du se [Registrere sporinger ved hjelp av Trace Parser](../perf-test/trace-trace-tutorial.md).

Det er noen få begrensninger ved denne fremgangsmåten. Siden en del av ER implementeres i C#, blir ikke alle detaljene tilgjengelige. Du kan imidlertid vise informasjon om databruk. Lange rapportkjøringer kan i tillegg overskride begrensninger ved sporingslagring.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER-sporinger

ER kan samle inn sine egne sporinger, og det har visualiserings- og analyseverktøy for disse sporingene. Hvis du vil ha mer informasjon, kan du se [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Siden både X++ og ER implementeres over .NET-plattformen, kan du bruke vanlige .NET-verktøy. Du kan for eksempel bruke det gratis [PerfView](https://github.com/Microsoft/perfview)-verktøyet.

Du kan også samle inn data fra kommandolinjen. Windows PowerShell-skriptet nedenfor samler for eksempel inn kjøringstiden til en formatkjøring stoppes på maskinen.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Det er noen få begrensninger ved denne fremgangsmåten. Du må ha administrativ tilgang til maskinen. Du må i tillegg være en erfaren utvikler, fordi det er en bratt læringskurve forbundet med dette.

### <a name="making-changes"></a><a name="making-changes"></a>Gjøre endringer

#### <a name="use-caching"></a><a name="use-caching"></a>Bruke hurtigbufring

Selv om hurtigbufring reduserer tiden det tar å hente inn data igjen, koster det minne. Bruk hurtigbufring i tilfeller der mengden hentede data ikke er særlig stor. Hvis du vil ha mer informasjon og et eksempel som viser hvordan du bruker hurtigbufring, kan du se [Forbedre modelltilordningen basert på informasjon fra kjøringssporingen](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a>Redusere volum for data som hentes

Du kan redusere minneforbruket for hurtigbufring ved å begrense antall felt i postene i en programtabell som du henter ved kjøretid. I dette tilfellet henter du bare de feltverdiene for en programtabell du trenger i ER-modelltilordningen. Andre felt i denne tabellen hentes ikke. Derfor reduseres volumet av minne som kreves for å hurtigbufre hentede poster. Hvis du vil ha mer informasjon , kan du se [Forbedre ytelsen til ER-løsninger ved å redusere antall tabellfelt som hentes ved kjøretid](er-reduce-fetched-fields-number.md).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Bruke et hurtigbufret, parameterisert beregnet felt

Noen ganger må verdier slås opp gjentatte ganger. Eksempler omfatter kontonavn og kontonumre. Du kan spare tid ved å opprette et beregnet felt som har parametere på det øverste nivået, og deretter legge til feltet i hurtigbufferen.

Vi anbefaler at du bare bruker denne fremgangsmåten når størrelsen på de hurtigbufrede dataene er liten. Hvis du vil ha mer informasjon, kan du se [Forbedre ytelsen for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Bruke en JOIN-datakilde

En **JOIN**-datakilde gjør at flere tilkoblede poster kan hentes av én spørring. Du trenger ikke å bruke en egen spørring til å hente hver tilkoblede post. Hvis du for eksempel har 1000 linjer og henter varedata for hver linje etter relasjon, har du 1001 spørringer (= 1000 + 1). Hvis du bruker en **JOIN**-datakilde, bruker du bare én spørring til å hente de samme dataene. Hvis du vil ha mer informasjon, kan du se [Bruke JOIN-datakilder i ER-modelltilordninger til å hente data fra flere programtabeller](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Bruke FILTER-funksjonen i stedet for WHERE-funksjonen

**[FILTER](er-functions-list-filter.md)**-funksjonen kjører betingelser på SQL Server, mens **WHERE**-funksjonen henter alle data fra listen, én post om gangen, og bruker betingelsen for hver post. La oss si at du ønsker å velge én post blant 1000 poster. Hvis du bruker **WHERE**, blir alle 1000 poster hentet. Hvis du imidlertid bruker **FILTER**, blir nøyaktig én post hentet. **FILTER** kan også bruke indekser på databasesiden.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Bruke funksjoner for innsamlede data eller en datakilde for akkumulerte data

Hvis konfigurasjonen har en *GROUP BY*-komponent som viser en oversikt over tidligere hentede data etter rapport, henter komponenten alle dataene på nytt. Når du bruker funksjoner for innsamlede data, gjør du at ER kan akkumulere data under første henting. Hvis du vil ha mer informasjon, kan du se [ER Konfigurere format for å utføre telling og summering](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Skrive om deler av konfigurasjonen i X++

ER støtter oppkallemetoder for tabeller og klasser, inkludert utvidelser. Vurder å skrive om deler av modelltilordningen i X++ for å forbedre ytelsen.

ER kan bruke data fra følgende kilder:

- Klasser (datakilder for **objekt** og **klasse**)
- Tabeller (datakilder for **tabell** og **tabellposter**)

[ER-API (application programming interface)](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) gir også en måte å sende forhåndsberegnede data fra oppkallekoden på. Programserien inneholder en rekke eksempler på denne fremgangsmåten.
