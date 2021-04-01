---
title: Forbedre ytelsen til planleggingsmotoren
description: Dette emnet inneholder informasjon om planleggingsmotoren og hvordan du kan forbedre ytelsen.
author: ChristianRytt
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0b55d0e94b40adf232e6b5cc3a9fb422e4539340
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246771"
---
# <a name="improve-scheduling-engine-performance"></a>Forbedre ytelsen til planleggingsmotoren

[!include [banner](../includes/banner.md)]

Ressursplanleggingsmotoren brukes ved planlegging av ruter for planlagte og frigitte produksjonsordrer. Motoren ble opprinnelig utgitt som en del av Dynamics AX 2012 og har gått gjennom flere forbedringer etter utgivelsen.

[Planlegging av jobbproduksjonsproblem](https://en.wikipedia.org/wiki/Job_shop_scheduling) er et ekstremt komplekst kombinasjonsproblem der løsningstiden øker eksponentielt med antallet beslutningvariabler. Ofte kan kundene definere produksjonsruter og relaterte data på en måte som fører til et planleggingsproblem som ikke kan løses i rimelig tid, selv på den mest moderne maskinvaren. Dette emnet vil hjelpe deg med å forstå planleggingsmotoren og hvordan et bestemt oppsett kan påvirke ytelsen.

Når det gjelder å forbedre ytelsen til planleggingen, anbefaler generelle retningslinjer at du reduserer kompleksiteten til problemet som motoren må løse. Noen av hovedfaktorene som kan påvirke ytelsen omfatter:

- Ruter med mange operasjoner
- Ruter med parallelle operasjoner
- Operasjoner med flere ressurser enn én
- Operasjoner med mange gjeldende ressurser
- Bruk av harde koblinger
- Bruk av begrenset kapasitet
- Antall forskjellige kalendere som brukes
- Antall spor for arbeidstid per dag i kalenderen
- Samlet varighet for ruten
- Kjøre flere planleggingsmotorer parallelt

## <a name="overview-of-basic-scheduling-flow"></a>Oversikt over grunnleggende planleggingsflyt

Hvis du vil forstå hvordan et gitt oppsett kan påvirke ytelsen, er det viktig å forstå noe om hvordan prosessen flyter, både i motoren og i X++-koden som omgir den.

Den grunnleggende prosessen med planlegging av en ordre består av tre hovedtrinn:

- **Laste inn data** – Her blir X++-datamodellene omgjort til motorens interne datamodell i form av jobber og begrensninger.
- **Planlegge** – Dette er hovedkilden for planlegging som behandler angitt modell og begrensninger, og genererer et resultat. I denne prosessen vil motoren be om arbeidstidsinformasjon og eksisterende kapasitetsreservasjoner fra X++ etter behov.
- **Lagre data** – Motorresultatet i form av reservasjonsspor for jobbkapasitet behandles av X++-kode for å spare kapasitetsreservasjoner og oppdatere start- og sluttidspunktene for jobbene/operasjonen/ordren.

## <a name="load-data-into-the-engine"></a>Laste inn data i motoren

Planleggingsmotoren har en mer abstrakt datamodell enn Supply Chain Management-databasen fordi den er bygget som en generell motor som kan håndtere forskjellige datakilder. Konseptet med rute, sekundære operasjoner og kjøretid må settes til "oversatt" i den generelle generiske jobb- og betingelsesmodellen som motoren viser. Logikken for bygging av modellen inneholder en betydelig grad av forretningslogikk, og den er forskjellig avhengig av kildedataene. Den ansvarlige X++-klassen er `WrkCtrScheduler`, og den har avledede klasser for planlagte produksjonsordrer, frigitte produksjonsordrer og prosjektprognoser.

Tenk deg for eksempel at du kan se en rute som vises i tabellen og bildet nedenfor, som ser relativt enkel ut.

| Oper. Nei. | Prioritet | Oppstillingstid | Kjøretid | Køtid etter | Antall ressurser | Next |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Primær | 1.00 | 2.00 | | 1 | 20 |
| 10 | Sekundær&nbsp;1 | | | | 1 | 20 |
| 20 | Primær | | 3.00 | 1.00 | 3 | 0 |

![Eksempel på rutediagram](media/scheduling-engine-route.png "Eksempel på rutediagram")

Når du sender denne til motoren, deles den opp i åtte jobber, som vist i illustrasjonen nedenfor (velg bilde for å forstørre det).

[![Jobber for planleggingsmotor](media/scheduling-engine-jobs.png "Jobber for planleggingsmotor")](media/scheduling-engine-jobs-large.png)

Standardkoblingen mellom to jobber er `FinishStart`, noe som betyr at sluttidspunktet for en jobb må være før starttidspunktet for en annen jobb. Siden oppsettet må utføres av den samme ressursen som senere vil utføre prosessen, finnes det `OnSameResource`-betingelser mellom dem. Mellom jobbene for primær- og sekundæroperasjon for 10, er det `StartStart`- og `FinishFinish`-koblinger, som betyr at jobbene må starte og slutte samtidig, og det finnes `NotOnSameResource`-begrensninger som vil hindre den samme ressursen for primær og sekundær.

For operasjon 20, der antall ressurser er satt til 3, er prosessjobben delt inn i tre forskjellige jobber der alle jobbene må kjøre på nøyaktig samme tidspunkt.
I dette tilfellet er rutegruppen konfigurert til ikke å reservere kapasitet for kø etter tidspunkt, som er grunnen til at det bare er én enkelt jobb for kø etter.

Planleggingsmotoren forstår bare begrepet jobber og har ingen oppfatning av operasjoner. Dette betyr at operasjonene også deles inn i jobber når grovplanlegging utføres, selv om disse ikke vil bli beholdt i databasen.

For hver jobb vil vi også definere hva som er jobbkapasitetsbehovet (antall sekunder som kreves). Avhengig av hvordan ressurskravene er definert, kan vi også sende en liste over alle mulige ressurser som jobben kan kjøre på, og hva som er kapasitetsbehovet for den bestemte ressursen. Selv om listen over gjeldende ressurser sendes når modellen bygges, må motoren likevel sikre at ressurstildelingen er gyldig for hele jobbvarigheten.

## <a name="scheduling-engine-internals"></a>Internt i planleggingsmotorer

### <a name="scheduling-engine-interface"></a>Grensesnitt for planleggingsmotorer

Hvis du vil ha en pekepinn om hvordan motoren fungerer internt, er det best å se på funksjonaliteten den viser eksternt. I X++ er hovedgrensesnittet `WrkCtrSchedulerEngineInterface`. Det inneholder metodene som er beskrevet i underdelene nedenfor.

#### <a name="general-engine"></a>Generell motor

| **Metode** | **Formål** |
| --- | --- |
| `run` | Planlegger alle innlastede jobber og returnerer feilkoden. |
| `getJobSchedulingSequenceResult` | Henter planleggings resultatet og den første feiljobben for serien som identifiseres av en bestemt jobb. |
| `validateJobCapacityReservations` | Validerer kapasitetsreservasjonene for alle jobbene som er lagret av motoren. |
| `setReservationsTimeStamp` | Sender et tidsstempel til motoren som er angitt for alle nye kapasitetsreservasjoner for de planlagte jobbene i bufferen til motoren. |
| `addPropertyToGroupAggregation` | Legger til et egenskapsprefiks i settet med egenskaper som brukes når kapasiteten er samlet. |
| `addResource` | Legger til en ressurs i planleggingsmotorens ressursutvalg. |
| `addResourceGroup` | Legger til en ressursgruppe i planleggingsmotorens ressurgruppeutvalg. |
| `addResourceGroupMembership` | Legger til en ressurs som medlem i en ressursgruppe. |
| `addOptimizationGoal` | Legger til et mål for planleggingsoptimalisering (varighet eller prioritet). |

#### <a name="individual-jobs"></a>Enkeltjobber

| **Metode** | **Formål** |
| --- | --- |
| `addJobInfo` | Legger til en post for jobbinformasjon som informerer motoren om en jobb som skal planlegges. |
| `addConstraintJobEndsAt` | Legger til en begrensning for avslutning av en jobb på angitt dato og klokkeslett. |
| `addConstraintJobStartsAt` | Legger til en begrensning for start av en jobb på angitt dato og klokkeslett. |
| `addConstraintMaxJobDays` | Definerer en begrensning for angitt maksimalt antall dager som en jobb kan strekke seg over. |
| `addConstraintResourceRequirement` | Legger til begrensning for at jobben må planlegges på en bestemt ressurs. |
| `addJobBindPriority` | Legger til en jobbindingsprioritet for et par (jobb, begrensningsnivå). En verdi med høyere prioritet betyr at jobbvariablene vil bli bundet tidligere. Jobben vil bli behandlet før jobber med lav prioritetsverdi i samme serie. |
| `addJobCapacity` | Legger til informasjon om kapasitetsbelastning for en jobb (for eksempel nødvendig jobbkjøretid), uavhengig av hvilken ressurs jobben kjøres på. |
| `addJobResourceCapacity` | Legger til en ressurs i ressurssettet som kan brukes til å utføre en jobb, og angir kapasiteten som kreves når du kjører ressursen. |
| `addJobGoal` | Legger til informasjon om jobbmål for et bestemt begrensningsnivå (tidligste sluttidspunkt eller siste starttidspunkt). |
| `addJobResourcePriority` | Legger til prioriteten som skal brukes når en jobb planlegges på en ressurs. |
| `addJobResourceRuntime` | Angir en jobbtid som er avhengig av ressursen som jobben skal planlegges på. |
| `addJobRuntime` | Angir en jobbtid som er uavhengig av ressursen som jobben skal planlegges på. |
| `scheduleJobOnResourceGroup` | Merker en jobb for planlegging på ressursgruppenivå. |
| `setJobResourcePreemptionAllowed` | Angir om det er tillatt med innløsning for en jobb på en ressurs (hvis motoren har tillatelse til å planlegge jobben i ikke-sammenhengende kapasitetsspor). |
| `setRequiredNumberOfResources` | Angir antallet ressurser som kreves for å planlegge en jobb (bare for grovplanlegging). |

#### <a name="constraints-between-jobs"></a>Begrensninger mellom jobber

| **Metode** | **Formål** |
| --- | --- |
| `addJobLink` | Legger til en kobling (for eksempel slutt\>start) mellom to jobber. |
| `addConstraintEndsDelayed` | Definerer en begrensningen for at en jobb ikke kan avslutte før en annen jobb avslutter i tillegg til en forsinkelsestid. |
| `addConstraintJobListWorkingTimeIntersect` | Legger til en begrensning for at kapasitetssporene som er reservert for jobbene, må være på overlappingsarbeidstiden for de to ressursene som brukes av jobbene. |
| `addConstraintJobOverlap` | Legg til en begrensning som definerer hvordan jobber skal utføres i rekkefølge når et gitt antall av en vare kan flyttes mellom to ressurser mens den første ressursen fortsatt ikke er ferdigbehandlet, slik at den andre ressursen kan starte behandlingen. |
| `addConstraintNotOnSameResource` | Legger til en begrensning for at to jobber ikke skal planlegges på den samme ressursen. |
| `addConstraintOnSameResource` | Legger til en begrensning for at to jobber må bruke den samme ressursen. |
| `addJobSameReservations` | Legger til en begrensning for at en jobb må avslutte med kapasitetsreservasjoner for de samme tidsrommene som den primære jobben. |
| `setPrimaryParallelJob` | Legger til informasjon om hvilken jobb som er den primære jobben i et sett med parallelle jobber. |

### <a name="solver"></a>Problemløser

Selve motoren er først og fremst en spesialisert begrensningsproblemløser med egendefinert heuristikk. Problemløseren er basert på to hovedelementer: variabler og begrensninger.

#### <a name="variable"></a>Variabel

En variabel representerer et domene med mulige verdier. Planleggingsmotoren har to typer variabler:

- **Dato/klokkeslettvariabel** – Har et domene for alle datoer og klokkeslett, og domenet kan begrenses ved å flytte den nedre og øvre grensen for tidspunktet for variabelen nærmere hverandre.
- **Ressursvariabel** – Har et domene for gjeldende ressurser, og domenet kan begrenses ved å fjerne ressurser fra listen.

#### <a name="constraint"></a>Begrensning

En begrensning fungerer på variabler ved å begrense domenene, men det avhenger også av variabler, slik at de aktiveres når variablene endres. Prosessen for overføring av betingelser er når en begrensning utfører sin hovedfunksjon og rapporterer tilbake til hovedlogikken hvis vellykket.

En variabel regnes som bundet når den ikke kan begrenses, som for dato/klokkeslettvariabelen betyr at øvre og nedre grense er den samme, og for ressursvariabelen at den bare har én enkelt relevant ressurs. Når alle variabler er bundet, blir det funnet en løsning.

### <a name="constraint-levels"></a>Betingelsesnivåer

Når planlegging utføres som del av fasen for planlegging av materialbehov (MRP), blir ordrene planlagt bakover fra behovsdatoen. Hvis det imidlertid ikke er mulig å finne en tidsplan som starter i dag eller senere og slutter før behovsdatoen, endres planleggingsretningen til fremover fra i dag.

Denne hovedforretningsregelen håndteres ved å organisere begrensningene i nivåer. Hvis det ikke blir funnet en løsning ved bruk av begrensningene på høyeste nivå, droppes begrensningene på dette nivået, og det lavere nivået blir forsøkt. I praksis betyr det at for planlegging bakover vil modellen inneholde et nivå 1 med jobbmål for siste starttidspunkt gitt en maksimal sluttidsbetingelse (behovsdatoen), og et nivå 0 med jobbmål som er tidligste sluttidspunkt og gitt en minimumsbetingelse for starttid i dag.

### <a name="algorithm"></a>Algoritme

Hovedtrinnene i motorens algoritme er:

1. Finn serier (jobbkjeder) som kan løses separat.
1. Prøv å finne første løsning for serie for det høyeste betingelsesnivået.
    1. Sorter jobbene i rekkefølge basert på jobbmål og -prioriteter, slik at det kan finnes en startjobb.
    1. Gjenta jobbene i følgende rekkefølge:
        1. Finn alle begrensninger som må overføres, og kjør overføring.
        1. Hvis alle variablene for jobben er bundet, er det funnet en løsning for denne jobben.
        1. Hvis en av variablene ikke kan bindes uten å bryte begrensningene, kan du rulle tilbake variabelbindingen, prøve en annen verdi i domenet (for ressursvariabel) og kjøre betingelsesoverføringen på nytt.
1. Hvis ingen løsning ble funnet, fjernes alle begrensningene på gjeldende begrensningsnivå, begrensningsnivået senkes (hvis noen av de lavere nivåene er tilgjengelige) og løsningssøket prøves på nytt med det nye begrensningssettet.
1. Hvis en mulig løsning ble funnet, startes optimaliseringsfasen, som vil prøve å finne en bedre løsning til tidsavbruddet for optimaliseringen er nådd eller alle ressurskombinasjoner er oppbrukt.

Problemløseren for begrensninger kjenner ikke til detaljene i planleggingsalgoritmen. "Magien" skjer i definisjonen og kombinasjonen av de ulike begrensningene.

### <a name="determining-working-times"></a>Bestemme arbeidstider

En stor del av (interne) begrensningene i motoren styrer arbeidstiden og kapasiteten til en ressurs. Oppgaven er hovedsakelig å gå gjennom arbeidstidssporene for en ressurs fra et gitt punkt i en gitt retning, og finne et langt nok intervall der den nødvendige kapasiteten for jobbene (tid) kan få plass.

For å gjøre dette må motoren kjenne til arbeidstiden til en ressurs. I motsetning til hovedmodelldataene er arbeidstidene har *forsinket innlasting*, og det betyr at de lastes inn i motoren etter behov. Årsaken til denne fremgangsmåten er at det ofte brukes arbeidstider i Supply Chain Management for en kalender for en svært lang periode, og det finnes vanligvis mange kalendere, slik at dataene vil være ganske store å forhåndslaste.

Motoren ber om kalenderinformasjon i deler ved å starte klassemetoden `WrkCtrSchedulingInteropDataProvider.getWorkingTimes` i X++. Forespørselen gjelder for en bestemt kalender-ID i et bestemt tidsintervall. Avhengig av statusen til serverens hurtigbuffer i Supply Chain Management, kan hver av disse forespørslene ende opp i flere databasekall, noe som tar lang tid (i forhold til bare beregningstiden). Hvis kalenderen inneholder svært detaljerte definisjoner for arbeidstid med mange intervaller for arbeidstid per dag, vil dette i tillegg føre til at innlastingen tar mer tid.

Når dataene for arbeidstid lastes inn i planleggingsmotoren, beholdes dette i den interne hurtigbufferen for den bestemte kalenderen, noe som betyr at hvis andre jobber eller ressurser bruker samme kalender, kan de neste oppslagene utføres raskt fra minnet. En vanlig årsak til dårlig ytelse er hvis en separat kalender-ID brukes for hver ressurs, fordi det deretter må spørres om data for hver kalender, selv om innholdet i kalenderne kan være like.

### <a name="finite-capacity"></a>Begrenset kapasitet

Når du bruker begrenset kapasitet, blir sporene for arbeidstid fra kalenderen delt opp og redusert basert på eksisterende kapasitetsreservasjoner. Disse reservasjonene hentes også gjennom samme `WrkCtrSchedulingInteropDataProvider`-klasse som kalenderne, men bruker i stedet metoden `getCapacityReservations`. Når du planlegger under hovedplanlegging, tas det hensyn til reservasjoner for den spesifikke hovedplanen, og hvis den er aktivert på siden **Parametere for hovedplanlegging**, blir også reservasjonene fra autoriserte produksjonsordrer inkludert. Når en produksjonsordre planlegges, er det også et alternativ for å inkludere reservasjoner fra eksisterende planlagte ordrer, selv om dette ikke er like vanlig som den andre metoden.

Bruk av begrenset kapasitet vil føre til at planleggingen tar lengre tid på grunn av flere årsaker:

- Henting av kapasitetsinformasjonen fra databasen er en langsom operasjon, og hurtigbufring av kapasitetsinformasjon på serversiden er vanligvis ikke like bra som for arbeidstider, fordi de ikke deles mellom ressurser, slik som kalendere for eksempel er.
- Antallet spor for arbeidstid som gjennomgås øker på grunn av oppdelingene, og spor for en lengre tidsperiode må vanligvis undersøkes før en løsning kan finnes.
- Når planleggingen er fullført, må det utføres en kontroll av reservasjoner som er i konflikt (se delen Kjøre flere planleggingsmotorer parallelt for mer informasjon).

### <a name="examining-the-resource-combinations"></a>Undersøke ressurskombinasjonene

Hvis jobbsekvensen bare inneholder standard `FinishStart`-koblingene, noe som betyr at dette utgjør en enkel kjede uten noen forgreninger, kan det oppnås et optimalt resultat (sett fra én enkelt ordre, ikke på tvers av ordrer) ved å finne den beste løsningen for den første jobben og deretter gå videre for å finne den beste løsningen for den neste jobben. Den beste løsningen for en jobb betyr å finne ressursen som kan få fra- og til-datoen for jobben nærmest jobbmålet (i planlegging fremover betyr dette å få sluttdatoen for jobben så tidlig som mulig), og fortsatt ta hensyn til begrensningene.

Når det finnes parallelle jobber, kan det å finne en løsning innebære å undersøke ulike ressurskombinasjoner. Antallet mulige ressurskombinasjoner er produktet av antallet gjeldende ressurser for de tilkoblede parallelle jobbene. Spesielt når du planlegger en ordre bakover fra en behovsdato, kan det ta ganske lang tid for logikken å finne ut at det ikke er noen løsning på problemet som vil gjøre at de parallelle jobbene får plass før dagens dato, fordi den må kontrollere alle kombinasjonene fordi det kan finnes ressurser som hadde høyere effektivitet eller en annen kalender som kan gi et resultat. Dette betyr at hvis det ikke er angitt en grense for tidsavbrudd, kjøres den i lang tid før retningen endres til fremover.

Denne kombinasjonslogikken betyr også at å legge til flere gjeldende ressurser kan få motoren til å kjøre langsommere. Hvis det oppstår ytelsesproblemer når du har parallelle operasjoner og planlegger med uendelig kapasitet, kan dette delvis løses ved å få ruteutformingsverktøyet til å avgjøre hvilken ressurs som skal brukes og deretter tilordne ressursen direkte på operasjonen (fordi motoren i de fleste tilfeller alltid fører til valg av den samme ressursen, slik at sluttresultatet vil være det samme).

### <a name="hard-links"></a>Harde koblinger

Hvis du angir hard koblingstype mellom to jobber, sikrer du at det ikke er noen tidsforskjell mellom slutten av en jobb og starten på neste. Dette kan være svært nyttig i scenarier som når metall varmes opp i én jobb og deretter behandles i neste jobb, der det ikke er ønskelig at metallene kjøles ned.

Med standard myke koblinger og planlegging fremover og hvis ruten utgjør en enkel kjede uten noen forgreninger, kan du oppnå et resultat ved å finne en løsning for den første jobben som oppfyller sine egne begrensninger, og deretter gå videre gjennom kjeden ved å overføre sluttidspunktet fra forrige jobb til neste jobb. Hvis den gjeldende jobben ikke finner noen kapasitet, vil starttidspunktet for denne bli flyttet videre fremover, uten konsekvenser for at de foregående jobbene skal lage hull mellom jobbene. Med harde koblinger (spesielt i forbindelse med begrenset kapasitet) for samme scenario, vil det imidlertid si at én jobb som er senere i kjeden ikke kan finne kapasitet, noe som betyr at alle tidligere planlagte jobber må "dras" en etter en og dermed tidsplanlegges flere ganger. Spesielt i scenarier med høy belastning for flere ressurser kan de harde koblingene forårsake en kjedereaksjon der jobbene vil påvirke hverandre og et flere gjentakelser må utføres før resultatet stabiliseres til en mulig tidsplan.

## <a name="running-scheduling-engines-in-parallel"></a>Kjøre planleggingsmotorer parallelt

Når du utfører planlegging som en del av en hovedplanleggingskjøring der hjelpeprogrammer brukes, kan hver enkelt av trådene for hjelpeprogrammene for hovedplanlegging også hente inn oppgaver for planleggingsoppgaver for produksjonsordre. Dette betyr at flere planleggingsmotorer kan kjøre samtidig. Selv om flertrådskjøring vanligvis er en svært viktig ytelsesfordel, finnes det også noen funksjonelle negative sider når det gjelder planlegging.

I MRP blir alle produksjonsordrer for et angitt stykklistenivå planlagt i behovsdatoserien, noe som betyr at de ordrene som har den tidligste behovsdatoen skal planlegges først og dermed ha høyest sjanse for å få den tilgjengelige ressurskapasiteten. Med flere motorer som velger fra listen over ordrer som ikke er planlagt, er imidlertid serien ikke lenger sikret fordi en av dem kan fullføres raskere enn den andre.

Når du bruker begrenset kapasitet og flere motorforekomster prøver å planlegge ordrer som kan bruke de samme ressursene i samme tidsintervall, oppstår det også en kappløpssituasjon. Antallet slike kappløpssituasjoner registreres i feltet **Planleggingskonflikter** på siden for historikken for hovedplanleggingen. Logikken for konfliktløsing er som følger:

- Planlegg en ordre (uten lås), og hent kapasitetsreservasjoner.
- Ta låsen.
- Kontroller om det finnes nyere kapasitetsreservasjoner for de planlagte ressursene i tidsrommet.
  - Hvis nei, skriver du kapasiteten og frigir låsen.
  - Hvis ja, frigir du låsen og planlegger ordren på nytt fra begynnelsen.

Når du planlegger med flere motorforekomster, er ikke resultatet fullstendig deterministisk, fordi det vil være avhengig av den nøyaktige tidsberegningen for hver av trådene.

## <a name="operation-scheduling-performance"></a>Ytelse for grovplanlegging

Selv om grovplanlegging også kalles som omtrentlig kapasitetsplanlegging, er det sett fra et motorståsted, et vanskeligere problem å løse hvis det brukes begrenset kapasitet, fordi det er nødvendig med mer data for å fastslå gjennomførbarhet.

Kapasiteten til en ressursgruppe avhenger av hvilke og hvor mange ressurser som er medlemmer av ressursgruppen. En ressursgruppe i seg selv har ingen kapasitet. Ressurser har bare kapasitet når de er medlemmer av gruppen. Fordi medlemskapet i ressursgrupper kan variere over tid, må kapasiteten evalueres per dag.

I grovplanlegging brukes ressursgruppens kalender til å fastslå start- og sluttidspunktene for hver operasjon. Dette betyr at ressursgruppens kalender plasserer en grense for hvor mye tid som kan være grovplanlagt for én operasjon på én dag i én ressursgruppe. I motsetning til kalenderen for de bestemte ressursene, ignoreres effektivitetsdataene i kalenderen for ressursgruppen fordi det ganske enkelt betyr åpningstid og ikke faktisk kapasitet.

Hvis for eksempel arbeidstiden for en ressursgruppe på en bestemt dato er fra 8.00 til 16.00, kan ikke én operasjon legge til mer belastning på ressursgruppen enn det som kan få plass i 8 timer, uansett hvor stor kapasitet ressursgruppen har tilgjengelig totalt på denne dagen. Tilgjengelig kapasitet kan imidlertid begrense belastningen ytterligere.

Belastningen fra jobbplanlegging for alle ressursene som er inkludert i ressursgruppen på en bestemt dag, vurderes når tilgjengelig kapasitet for ressursgruppen på samme dag beregnes. For hver dato er beregningen:

*Tilgjengelig kapasitet for ressursgruppe = kapasitet for ressurser i gruppen basert på kalenderen &ndash; planlagt jobbelastning på ressursene i gruppen &ndash; planlagt driftsbelastning på ressursene i gruppen &ndash; planlagt driftsbelastning på ressursgruppen*

I fanen **Ressurskrav** i ruteoperasjonen, kan ressurskravene angis ved hjelp av en bestemt ressurs (i så fall planlegges operasjonen ved å bruke denne ressursen), for en ressursgruppe, for en ressurstype eller for én eller flere funksjoner, ferdighet, kurs eller sertifikat. Selv om bruk av alle disse alternativene gir en større fleksibilitet for ruteutformingen, kan det også komplisere planleggingen for motoren etter hvert som det må tas hensyn til kapasitet per "egenskap" (det abstrakte navnet som brukes i motoren for funksjonalitet, ferdighet og så videre).

Ressursgruppens kapasitet for en funksjon er summen av kapasiteten for alle ressurser i ressursgruppen som har den aktuelle funksjonen. Hvis en ressurs i gruppen har en funksjon, vurderes den uansett hvilket kapasitetsnivå som kreves.

I grovplanlegging blir den tilgjengelige kapasiteten for en bestemt funksjon for en ressursgruppe redusert når den belastes med en operasjon som krever den aktuelle funksjonen. Hvis operasjonen krever mer enn én funksjon, vil kapasiteten bli redusert for alle nødvendige funksjoner.

For hver dato er den nødvendige beregningen:

*Tilgjengelig kapasitet for en funksjon = kapasitet for funksjonen &ndash; planlagt jobbelastning på ressursene med den spesifikke muligheten, inkludert i ressursgruppen &ndash; planlagt driftsbelastning på ressursene med den spesifikke muligheten, inkludert i ressursgruppen, &ndash; planlagt driftsbelastning på selve ressursgruppen som krever den spesifikke funksjonaliteten*

Dette betyr at hvis det er belastning på en bestemt ressurs, vurderes belastningen i beregningen av ressursgruppens tilgjengelige kapasitet per funksjon, fordi belastningen på en bestemt ressurs reduserer bidraget til ressursgruppens kapasitet for en funksjon uansett om belastningen på den bestemte ressursen er for den bestemte funksjonen. Hvis det er belastning på ressursgruppenivå, blir dette bare tatt med i beregningen av ressursgruppens tilgjengelige kapasitet per funksjon hvis belastningen er fra en operasjon som krever den spesifikke funksjonen.

Logikken ovenfor er complicatd, siden dette er den samme for hver type "egenskap", slik at bruk av grovplanlegging med begrenset kapasitet krever en betydelig mengde data som kan lastes inn.

## <a name="viewing-scheduling-engine-input-and-output"></a>Vis inndata og utdata for planleggingsmotor

Hvis du vil ha detaljert informasjon om inndata og utdata for planleggingsprosessen, kan du aktivere logging ved å gå til **Organisasjonsstyring \> Oppsett \> Planlegging \> Cockpit for sporing av planlegging**.

På denne siden velger du først **Aktiver logging** i handlingsruten. Kjør deretter planleggingen for produksjonsordren. Når dette er fullført, går du tilbake til siden **Cockpit for sporing av planlegging** og velger **Deaktiver logging** i handlingsruten. Oppdater siden, og en ny linje vises i rutenettet. Velg den nye linjen, og velg **Last ned** i handlingsruten. Dette vil gi deg en ZIP-komprimert mappe som inneholder følgende filer:

- **Log.txt** – Dette er loggfilen som beskriver fremgangsmåten motoren går gjennom. Denne er svært omfattende og kan være en litt overveldende, men når den brukes som en del av eksperimenteringen med ruteoppsettet for å løse ytelsesproblemer, er det første du ser etter tidsforskjellen mellom den første og den siste linjen, fordi dette angir nøyaktig hvor mye tid som er brukt på planleggingen.
- **XmlModel.xml** – Denne inneholder modellen som er bygget i X++ og som motoren opererer på. `JobId` som er brukt i filen, samsvarer med `RecId` fra kildetabellen som inneholder jobbene (`ReqRouteJob` eller `ProdRouteJob`). Det vanlige å se etter i denne filen, er at datoene som er angitt i `ConstraintJobStartsAt` og `ConstraintJobEndsAt`, er som forventet, at `JobGoal`-egenskapen er riktig angitt og at jobbene er knyttet til hverandre via `JobLink`-begrensningene.
- **XmlSlots.xml** – Denne inneholder alle driftstider og kapasitetsreservasjoner som motoren har bedt om. Arbeidstidene og reservasjonene i kalenderen blir bare forespurt av motoren for tidsperiodene der den prøver å plassere jobbene (og en ekstra buffer), så hvis filen inneholder tid som er svært langt inn i fremtiden, kan det være en indikasjon på et problem med oppsettet. `ResourceProperty`-nodene vil vises for hver ressurs som ressursgruppen og funksjonen den er knyttet til, og hvilke perioder.
- **Result.xml** – Denne inneholder resultatet av planleggingskjøringen.

Legg merke til at sporingsfunksjonaliteten kan gi en betydelig ytelsesreduksjon, slik at den bør bare brukes til å undersøke planlegging av bestemte ordrer på en kontrollert måte. Hvis den er aktivert under en hovedplanlegging, kan den raskt nå størrelsesgrensen og stoppe.

## <a name="troubleshooting-performance"></a>Feilsøke ytelse

Som du kan forstå fra alle de forrige delene, finnes det noen fallgruver når det gjelder oppsett og bruk av planleggingsmotoren, noe som kan føre til ytelsesproblemer. Følgende sjekkliste kan brukes til feilsøking av slike problemer. Det er viktig å se på alle punktene fordi det ofte er en kombinasjon av flere faktorer som fører til problemer.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Utføre planlegging som en del av MRP når den ikke er nødvendig

Selv om ruter brukes til produksjonsstyring, for eksempel etterkalkulering og rapportering, kan det hende at det ikke er nødvendig å ta hensyn til dem under MRP. I noen tilfeller er det tilstrekkelig å angi standard leveringstid for produksjon for varen for planlegging. Hvis du vil deaktivere ruteplanlegging, setter du kapasitetshorisont til null. Hvis planlegging skal utføres, må kapasitetshorisonten nøye angis, fordi det kanskje ikke er nødvendig å ta hensyn til ruter for å få full oversikt over MRP-ens dekningshorisont.

Vær oppmerksom på at hvis ordren ikke er planlagt under MRP, må den i stedet planlegges når den planlagte bestillingen autoriseres. Dette betyr at autorisasjonsprosessen vil ta lenger tid, og avhengig av hvor mange av de foreslåtte planlagte ordrene som autoriseres, vil ytelsesgevinsten under MRP kanskje gå tapt under autoriseringen.

### <a name="route-with-unnecessary-operations"></a>Rute med unødvendige operasjoner

Når du utformer ruten, er det fristende å forsøke å utforme den virkelige verden nøyaktig med alle trinnene produksjonen går gjennom. Selv om dette kan være nyttig i noen tilfeller, er det ikke bra for ytelsen fordi modellen som motoren trenger for å arbeide, blir større (både med hensyn til jobber og begrensninger), og flere SQL-setninger blir utført for innsetting og oppdatering av jobbene og kapasitetsreservasjonene. Det er også en nedstrømseffekt av til slutt å måtte rapportere fremdriften for jobbene, som kan reduseres med automatiske posteringer. Hvis dataene ikke brukes til noe, skaper det unødvendig belastning.

Det anbefales at du bare oppretter operasjoner som er strengt nødvendige for planleggingen (som vanligvis vil være flaskehalsressurser) og/eller etterkalkuleringsformål. Du kan også gruppere mange mindre spesifikke operasjoner i én større operasjon som representerer en større del av prosessen.

### <a name="many-applicable-resources-for-an-operation"></a>Mange gjeldende ressurser for en operasjon

Antallet gjeldende ressurser for en operasjon bestemmes av ressurskravene som er angitt i operasjonsrelasjonen. Behovet kan enten gjelde for en bestemt ressurs (enkelt), eller det kan være basert på ressursens medlemskap i en ressursgruppe eller kapasitet.

Hvis det ikke utføres planlegging ved hjelp av begrenset kapasitet, og alle gjeldende ressurser har samme kalender og effektivitet, vil planleggingsmotoren alltid ende opp med å velge den samme ressursen for en operasjon, men bare etter å ha prøvd alle de aktuelle ressursene for å kontrollere om dette er "bedre" enn de andre. I slike tilfeller kan belastningen av planleggingen reduseres betydelig ved ganske enkelt å alltid tilordner en bestemt ressurs til operasjonen når ruten utformes.

### <a name="route-with-parallel-operations"></a>Rute med parallelle operasjoner

Selv om parallelle operasjoner (primær/sekundær) er et kraftig verktøy for å modellere scenarier, som når en maskin og en operatør er nødvendig for å utføre en bestemt oppgave, er det også kilde til mange ytelsesproblemer. Hvis et behov for en bestemt enkeltressurs er tilordnet både primær- og sekundæroperasjonen, er det vanligvis ikke noe problem. Men hvis det er mange mulige ressurser for hver av operasjonene, legger den til betydelig kompleksitet for grovberegning i planleggingen.

Et alternativ til å bruke parallelle operasjoner er enten å modellere parene som "virtuelle" ressurser (som deretter vil representere teamet som alltid går sammen for operasjonen), eller å ikke modellere en av operasjonene hvis den ikke representerer en flaskehals.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Rute med flere ressurser enn 1

Hvis du angir antall ressurser som kreves for en operasjon som er høyere enn én, er dette det samme som å bruke primær-/sekundæroperasjoner, fordi flere parallelle jobber sendes til motoren. I slike tilfeller finnes det imidlertid ikke et alternativ til å bruke spesifikke ressurstilordninger, fordi et antall som er større enn én, krever at mer flere enn én ressurs gjelder for operasjonen.

### <a name="excessive-use-of-finite-capacity"></a>Ubegrenset bruk av begrenset kapasitet

Bruk av begrenset kapasitet krever at motoren laster inn kapasitetsinformasjon fra en database og kan ha en databehandlingskostnad, fordi det vil være vanskeligere å finne en løsning, spesielt i miljøer der ressursene reserveres i nærheten av maksimal kapasitet. Det er derfor viktig å vurdere nøye om en ressurs virkelig trenger å bruke begrenset kapasitet, eller om de kan overreserveres. Fordi det kan være en forskjell på begrensede kapasitetsressurser i hvor viktige det er å ikke overreservere dem, anbefaler vi at å bruke flaskehalsalternativet på en ressurs i kombinasjon med en egen verdi på planen i "kapasitetshorisont for flaskehalsressurser". Bruk av flaskehalskonseptet kan føre til at den generelle begrensede kapasitetshorisonten kan reduseres.

### <a name="setting-hard-links"></a>Angi harde koblinger

Standard koblingstype for ruten er *myk*, noe som betyr at det er tillatt med en tidsforskjell mellom sluttidspunktet for én operasjon og starten på neste. Tillatelse av dette kan ha den uheldige effekten at hvis materialer eller kapasitet ikke er tilgjengelige for én av operasjonene i svært lang tid, kan produksjonen være inaktiv i en stund, noe som betyr en mulig økning av arbeidet som pågår. Dette skjer ikke med harde koblinger, fordi avslutning og start må være perfekt justert. Hvis du angir harde koblinger, blir imidlertid planleggingsproblemet vanskeligere fordi skjæringspunkter mellom arbeidstid og kapasitet må beregnes for de to ressursene for operasjonene. Hvis dette også omfatter parallelle operasjoner, legger dette til betydelig beregningstid. Hvis ressursene for de to operasjonene har forskjellige kalendere som ikke overlapper i det hele tatt, er problemet uløselig.

Det anbefales at du bruker harde koblinger bare når det er helt nødvendig, og vurder nøye om det er nødvendig for hver operasjon i ruten.

Hvis du vil redusere mengden arbeid som pågår, uten å bruke harde koblinger, er et triks å planlegge rekkefølgen to ganger og endre til motsatt retning for den andre gjennomføringen. Hvis den første tidsplanen ble utført bakover fra leveringsdatoen, bør den andre utføres fremover fra den planlagte startdatoen. Dette vil føre til at jobbene komprimeres så mye som mulig, slik at arbeidet som pågår minimeres.

### <a name="separate-calendar-for-each-resource"></a>Atskilt kalender for hver ressurs

En av de hoveddatakildene for planleggingsmotoren er kalenderinformasjon, som kan være kostbar å laste inn fra databasen. Kalendere genereres basert på maler, og det er derfor fristende å generere en kalender for hver ressurs og deretter justere informasjonen i denne kalenderen når ressursen har nedetid og andre problemer. Dette vil imidlertid føre til en alvorlig begrensning av muligheten til å bufre kalenderdataene, fordi dette må be om nye data for hver ressurs og kan være en stor kilde til ytelsesproblemer. I stedet anbefaler vi at du bruker kalenderne på nytt så mye som mulig mellom ressursene, og deretter styrer nedetiden ved å tilordne en annen kalender-ID for en periode.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Stort antall spor for arbeidstid per dag kalenderdag

Siden motoren fungerer ved å undersøke kapasiteten i tidsspor en etter en, er det nyttig å redusere antall tidsspor per kalenderdag. Dette kan for eksempel gjøres ved å vurdere om det er viktig for den resulterende tidsplanen å gjenspeile at arbeiderne har 5 minutter pause hver time.

### <a name="large-or-none-scheduling-timeouts"></a>Store (eller ingen) tidsavbrudd for tidsplaner

Planlegging av motorytelsen kan optimaliseres ved hjelp av parametere på siden **Planleggingsparametere**. Innstillingene **Tidsavbrudd for planlegging er aktivert** og **Tidsavbrudd for planleggingsoptimalisering er aktivert** må alltid settes til **Ja**. Hvis dette settes til **Nei**, kan planleggingen kjøre i det uendelige hvis det er opprettet en umulig rute med mange alternativer.

Verdien for **Maksimal planleggingstid per serie** kontrollerer styrer maksimalt antall sekunder som kan brukes til å prøve å finne en løsning for én enkelt sekvens (i de fleste tilfeller tilsvarer en serie én enkelt ordre). Verdien som brukes her, er svært avhengig av kompleksiteten i ruten og innstillingene, for eksempel begrenset kapasitet, men maksimalt 30 sekunder er et godt utgangspunkt.

Verdien for **Tidsavbrudd for optimaliseringsforsøk** styrer hvor mange sekunder som kan brukes til å finne en bedre løsning enn den som opprinnelig ble funnet. Dette vil bare påvirke ruter som bruker parallelle operasjoner når disse gjør det nødvendig å teste ulike kombinasjoner.

> [!NOTE]
> Verdiene som angis for tidsavbruddet, brukes både for planlegging av frigitte produksjonsordrer og planlagte ordrer som en del av MRP. Dermed kan det å sette svært høye verdier øke kjøretiden i MRP betydelig når det kjøres for en plan med mange planlagte produksjonsordrer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]