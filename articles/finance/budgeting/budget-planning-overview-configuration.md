---
title: Oversikt over budsjettplanlegging
description: Denne artikkelen introduserer budsjettplanlegging og inneholder informasjon om hvordan du konfigurerer budsjettplanlegging og definerer budsjettplanleggingsprosesser.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a33ced073394f0f3aa1b0b2e177e4608ca5bcf6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772036"
---
# <a name="budget-planning-overview"></a>Oversikt over budsjettplanlegging

[!include [banner](../includes/banner.md)]

Denne artikkelen introduserer budsjettplanlegging og inneholder informasjon om hvordan du konfigurerer budsjettplanlegging og definerer budsjettplanleggingsprosesser.

<a name="overview-of-budget-planning"></a>Oversikt over budsjettplanlegging
---------------------------

Du utfører budsjettplanlegging når du klargjør budsjettene som en organisasjon skal implementere. En organisasjon kan konfigurere budsjettplanlegging, og deretter konfigurere budsjettplanleggingsprosesser for å oppfylle sine policyer, prosedyrer og krav til klargjøring av budsjett. 

Når du forstår konseptene og terminologien som brukes i Microsoft Dynamics 365 Finance, er det enklere for deg å implementere budsjettplanlegging i organisasjonen.

### <a name="key-terms"></a>Viktige termer

-   **Budsjettplanleggingsprosesser** –Budsjettplanleggingsprosesser fastsetter hvordan budsjettplaner kan oppdateres, rutes, vurderes og godkjennes i budsjetteringsorganisasjonshierarkiet. En budsjettplanleggingsprosess er koblet til en budsjettsyklus og en organisasjon via en juridisk enhet.
-   **Budsjettplaner** – Budsjettplaner inneholder budsjettdataene for en budsjettsyklus. Du kan ha flere budsjettplaner som brukes til ulike formål. Budsjettplaner kan for eksempel brukes til å opprette budsjettbeløp for ulike organisasjonsenheter eller de kan bidra til å utføre sammenligninger og ta veloverveide beslutninger.
-   **Budsjettplanscenarioer** – Budsjettplanscenarioer definere kategorier av data for budsjettplanene. Du kan definere budsjettplanscenarioer for å støtte monetære og andre måleenhetsklasser, for eksempel antall. Eksempler på pengemessige budsjettplanscenarioer omfatter Avdeling forrige år og Avdelingsforespørsler. Eksempler på budsjettplanleggingsscenarier som bruker antall, omfatter kundestøttesamtaler forrige år og telling av fulltidsekvivalent (FTE).
-   **Budsjettplanleggingsstadier** – Budsjettplanleggingsstadier definerer trinnene som en budsjettplan følger fra start til endelig godkjenning. Budsjettplanleggingsstadier ordnes i arbeidsflyter for budsjettplanlegging.
-   **Arbeidsflyter for budsjettplanlegging** – Arbeidsflyter for budsjettplanlegging består av og definerer budsjettplanleggingsstadier. Arbeidsflyter for budsjettplanlegging er knyttet til budsjetteringsarbeidsflyter. Budsjetteringsarbeidsflyter er automatiserte og manuelle prosesser som flytter budsjettplaner gjennom budsjettplanleggingsstadiene.

[![Budsjettplanleggingsterminologi](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Vanlige oppgaver

Du kan bruke budsjettplanlegging til å utføre følgende oppgaver:

-   Opprett budsjettplaner for å definere de forventede inntektene og utgiftene for en budsjettsyklus.
-   Analyser og oppdater budsjettplaner for flere scenarier.
-   Rute budsjettplanene automatisk sammen med regneark, begrunnelsesdokumenter og andre vedlegg, for gjennomgang og godkjenning.
-   Konsolider flere budsjettplaner fra et lavere nivå i organisasjonen til én overordnet budsjettplan på et høyere nivå i organisasjonen. Du kan også utvikle én budsjettplan på et høyere nivå i organisasjonen og fordele budsjettet på lavere nivåer i organisasjonen.

Budsjettplanlegging er integrert med andre moduler. Du kan derfor hente inn informasjon fra tidligere budsjetter, faktiske utgifter, anleggsmidler og personaladministrasjon. Siden budsjettplanlegging også er integrert med Microsoft Excel og Microsoft Word, kan du bruke disse programmene til å arbeide med budsjettplanleggingsdata. En budsjettansvarlig kan for eksempel eksportere en avdelings budsjettforespørsel fra et budsjettplanscenario til et Excel-regneark. Dataene kan analyseres, oppdateres og legges i diagram i regnearket, og publiseres deretter tilbake til budsjettplanlinjene.

## <a name="configuring-budget-planning"></a>Konfigurere budsjettplanlegging
Siden **Budsjettplanleggingskonfigurasjon** inneholder de fleste innstillingene som kreves for å konfigurere budsjettplanlegging. Avsnittene nedenfor beskriver noen viktige faktorer du bør vurdere når du konfigurerer budsjettplanlegging. Når du har fullført konfigurasjonen, kan du konfigurere budsjettplanleggingsprosesser.

### <a name="create-a-budget-planning-schema"></a>Opprette et budsjettplanleggingsskjema

Et valgfritt men anbefalt første trinn, er å opprette et skjema som viser organisasjonens fremgangsmåte for å formulere et budsjett. Du kan bruke en valgfri metode for å opprette dette skjemaet. Illustrasjonen nedenfor viser et generelt eksempel, der separate arbeidsflyter for budsjettplanlegging er opprettet for forskjellige nivåer i organisasjonen. Stadier defineres innenfor hver arbeidsflyt, og bestemte scenarier tilordnes hvert stadium for å inneholde budsjettdataene. Oppgaver utføres for å flytte dataene fra ett stadium til det neste. Beløp kan for eksempel tildeles eller samles til ulike kontoer, godkjenninger eller andre gjennomganger. I dette eksemplet angir kursiv et scenario som ikke kan redigeres i løpet av stadiet, eller data som er historisk eller har blitt godkjent på et tidligere stadium og derfor ikke bør endres. 

[![Generisk skjema for budsjettplanlegging](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

I eksemplet nedenfor beregner firmaets hovedkontor beløpene for opprinnelig budsjett og distribuerer dem til salgsavdelingen. Salgsavdelingene vil deretter beregne og sende sine prognoser til hovedkontor, der budsjettansvarlig samler og justerer prognosen. Til slutt sender budsjettansvarlig de justerte budsjettbeløpene til økonomisjefen for gjennomgang, endelige justeringer og godkjenning. 

[![Eksempel på budsjettplanleggingsskjema](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Organisasjonshierarki for budsjettplanlegging

På siden **Organisasjonshierarki** kan du angi et organisasjonshierarki som en budsjettplanleggingshierarki for hver budsjettplanleggingsprosess. Budsjettplanleggingshierarkiet trenger ikke samsvarer med standard organisasjonshierarki som brukes til andre formål. Siden dette hierarkiet brukes til å samle og distribuere data, vil du kanskje det har en annen struktur. I eksempelskjemaet er salgsavdelingen under et hovedkontornivå som inkluderer budsjettet- og økonomiavdeling. Denne strukturen avviker sannsynlig fra strukturen som brukes til å administrere driften for salgsavdelingene. Bare ett organisasjonshierarki kan tilordnes hver budsjettplanleggingsprosess. 

Hvis du vil ha mer informasjon, kan du se [Organisasjoner og organisasjonshierarkier](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Brukersikkerhet

Budsjettplanlegging kan følge én av to sikkerhetsmodeller for å definere brukertillatelser. Hvis du vil angi sikkerhetsmodellen, kan du angi en budsjettplanleggingsparameter på siden **Budsjettplanleggingskonfigurasjon**.

### <a name="budget-planning-workflows-stages"></a>Arbeidsflytstadier for budsjettplanlegging

Arbeidsflyter for budsjettplanlegging brukes sammen med budsjetteringsarbeidsflyter for å administrere opprettingen og utviklingen av budsjettplaner.

En arbeidsflyt for budsjettplanlegging består av et sett med etterfølgende trinn som en budsjettplan beveger seg gjennom. Hver arbeidsflyt for budsjettplanlegging er knyttet til en budsjetteringsarbeidsflyt. Arbeidsflyter for budsjettering er én av arbeidsflyttypene som brukes i Finance and Operations. Arbeidsflyten for budsjettering ruter budsjettplanene, sammen med regneark, begrunnelser og vedlegg, gjennom organisasjonen for vurdering og godkjenning. 

Du oppretter arbeidsflyten for budsjettplanlegging i inndelingen **Arbeidsflytstadier** på siden **Budsjettplanleggingskonfigurasjon**. Der kan du velge stadiene og arbeidsflyten for budsjettering som skal brukes, og du kan også konfigurere tilleggsinnstillinger. 

En anbefalt fremgangsmåte er å opprette en budsjettplanleggingsarbeidsflyt for hvert nivå i et budsjetteringshierarki. Deretter tilordner du en arbeidsflyt for budsjettering som inneholder elementer som samsvarer med stadiene i arbeidsflyten for budsjettplanlegging. I eksemplskjemaet som vises tidligere i denne artikkelen, blir én budsjettplanleggingsarbeidsflyt opprettet for salgsavdelingene, og en annen blir opprette for hovedkontor. En arbeidsflyt for budsjettering flytter budsjettplanene gjennom stadiene. 

Du oppretter budsjetteringsarbeidsflyten for budsjettplanlegging på siden **Budsjetteringsarbeidsflyter**. Prosessen ligner på prosessen for å opprette andre arbeidsflyter. Illustrasjonen nedenfor viser et eksempel på en arbeidsflyt for Hovedkontor. 

[![Arbeidsflyt for budsjettering for budsjettplanlegging](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Arbeidsflyten inneholder elementer for tilordning til salgsavdelinger og samling av deres bidrag, gjennomgang av budsjettansvarlig, godkjenning av økonomisjef og stadieoverganger mellom hvert trinn. 

Du tilordner arbeidsflyten for budsjettering til hver arbeidsflyt for budsjettplanlegging i inndelingen **Arbeidsflytstadier** på siden **Budsjettplanleggingskonfigurasjon**.

### <a name="parameters-scenarios-and-stages"></a>Parametere, scenarier og stadier

De innledende innstillingene på siden **Budsjettplanleggingskonfigurasjon** lar deg opprette noen byggeblokker for senere konfigurasjonstrinn:

-   **Parametere** – Parametere, definere sikkerhetsreglene som du vil bruke for budsjettplaner og standard finansdimensjoner som skal brukes når brukerne driller ned i beløp for budsjettplanscenariet.
-   **Scenarier** – Scenarier omfatter datakategoriene du vil bruke for budsjettplanene. Du kan definere budsjettplanscenarioer for å støtte monetære og andre måleenhetsklasser, for eksempel antall. I en budsjettplan, representerer scenarier én versjon av dataene for budsjettplanlegging. Eksempler på pengemessige budsjettplanscenarioer omfatter salg i foregående år og signerte kontrakter. Eksempler på scenarier som bruker antall, omfatter antall salgssamtaler og telling av fulltidsekvivalent (FTE).
-   **Stadier** – Stadier definer trinnene som en budsjettplan følger, fra start til endelig godkjenning. Eksempler på budsjettplanleggingsstadier omfatter opprulling for hovedkontor, gjennomgang av økonomisjef og endelig godkjenning.

### <a name="allocation-schedules"></a>Fordelingsplaner

I budsjettplanlegging kan du tilordne beløpene eller antallene i budsjettplanlinjer fra én scenario et annet scenario, eller til samme scenario. Du kan for eksempel tildele til samme scenario hvis du vil bruke endringene for finansdimensjonene eller datoene for beløpene i dette scenariet. En tildeling gjøres i en budsjettplan eller fra én budsjettplan til en annen. 

Tildelingsplaner tildeler budsjettplanlinjer automatisk under arbeidsflytbehandling. Du kan utføre tildelinger ved å bruke en av følgende fordelingsmetoder i **Tildelingsmetode**-listen:

- <strong>Tilordne på tvers av perioder</strong> – Du kan bruke en periodetildelingsnøkkel for å tildele budsjettplanlinjer fra kildebudsjettplanscenarioet på tvers av perioder i målscenariet. <strong>Obs!</strong> Før du kan tildele på tvers av perioder, må du konfigurere periodetildelingsnøkler på siden *<strong><em></em>Kategorier for periodetildeling</strong>*.
- <strong>Tildel til dimensjoner</strong> – Budsjettplanlinjene tildeles kildebudsjettplanscenariet på tvers av finansdimensjonene i målscenariet. <strong>Obs!</strong> Før du kan tildele til dimensjoner, må du konfigurere budsjettfordelingsbetingelser på siden *<strong><em>Budsjettfordelingsbetingelser</em></strong>*.
- **Aggreger** – Budsjettplanlinjene aggregeres fra kildebudsjettplanscenariet i de tilknyttede budsjettplanene til målscenariet i den overordnede budsjettplanen.
- **Distribuer** – Budsjettplanlinjene distribueres fra kildebudsjettplanscenariet i den overordnede budsjettplanen til målscenariet i de tilknyttede budsjettplanene.
- **Bruk finansfordelingsregler** – Budsjettplanlinjene distribueres fra kildebudsjettplanscenariet i til målbudsjettplanscenariet basert på den valgte finansfordelingsregelen.
- **Kopier fra budsjettplan** – Du kan velge en annen budsjettplan som skal brukes som kilde for tildelingen.

### <a name="stage-allocations"></a>Stadiefordelinger

Stadiefordelinger brukes til å tildele budsjettplanlinjer automatisk under arbeidsflytbehandling. Når stadiefordelinger brukes, kan budsjettplanlinjer i målscenariet opprettes og endres uten tilsyn av budsjettplanklargjøreren eller kontrolløren.

Når du definerer en stadiefordeling, kan du knytte arbeidsflyten for budsjettplanlegging og stadiet til fordelingsplanen. Arbeidsflyten for budsjettplanlegging må være knyttet til en arbeidsflyt for budsjettering, som bruker den automatiserte arbeidsflytoppgaven *<strong><em>Fordeling for budsjettplanleggingsstadium</em></strong>*. Når arbeidsflyten når det angitte stadiet, skjer fordelingen automatisk. Denne automatiserte oppgaven kan brukes til å opprette budsjettplanlinjer i et nytt scenario. 

I eksempelskjemaet som vises tidligere i denne artikkelen, blir det utført en tildeling for å overføre beløp fra en budsjettplan og scenarier i grunnlinjestadiet for hovedkontoret til en annen budsjettplan og scenarier i estimatstadiet for salgsavdeling. Illustrasjonen nedenfor viser den aktuelle delen av eksempelskjemaet.

[![Stadiefordeling](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

I eksempelskjemaet utføres i tillegg en aggregering fra budsjettplaner og scenarioer i innsendtstadiet for salgsavdeling til en overordnet plan i opprullingsstadiet for hovedkontor. Illustrasjonen nedenfor viser den aktuelle delen av eksempelskjemaet.

[![Samling](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteter

Du kan eventuelt bruke budsjettplanprioritetene til å definere kategorier og målsettinger for budsjettplanene som er konfigurert. Du kan også bruke prioriteter til å organisere, klassifisere og evaluere flere budsjettplaner. Du kan for eksempel opprette en budsjettplanleggingsprioritet for helse og sikkerhet, og deretter evaluere budsjettplaner som er tilordnet den prioriteringen. Du kan også tilordne et nummer for å rangere budsjettplaner på tvers av alle budsjettplaner.

### <a name="columns-and-layouts"></a>Kolonner og oppsett

Budsjettall vises på en budsjettplan i rader og kolonner. Du må først definere kolonnene, og deretter kan du opprette et oppsett for å definere presentasjonen av kolonnene. 

Hvis du vil definere en kolonne, velger du et budsjettplanscenario. Linjebeløp fra scenariet vises på budsjettplanen. Du kan velge en periode for å filtrere beløpet, og du kan også bruke filtre som er basert på finanskontoen. 

Når du definerer et oppsett, kan du velge et finansdimensjonssett for å opprette budsjettplanradene som du vil vise, og velge kolonnene som oppsettelementer. Du kan opprette flere oppsett, slik at en budsjettplan viser dataene på forskjellige stadier i budsjettplanleggingsprosessen. 

I tillegg til kolonner for budsjettbeløp, kan du definere kolonner for prosjektet, foreslått prosjekt, aktiva og foreslåtte anleggsmiddelfelt fra budsjettplanen. Du kan også definere en kolonne for budsjetterte stillinger. Dette alternativet er nyttig når du må analysere personalbudsjetter. 

For eksempelskjemaet kan det hende du vil opprette kolonner for PY-salgs-, kontrakts-, og prognosescenarier (illustrasjonen nedenfor viser den aktuelle delen av skjemaet). Du kan deretter velge ut én eller alle scenariene inn i separate kolonner for hvert kvartal av regnskapsåret, slik at salgsavdelingslederen nøyaktig kan angi prognosebeløp for hver periode.

[![Kolonner](./media/columns.png)](./media/columns.png) 

Du kan også angi om hvert oppsettelement (kolonne) kan redigeres, og om de er tilgjengelige i alle regnearkmaler som opprettes for dette oppsettet. I oppsettet som brukes for estimatstadiet i eksempelskjemaet, kan prognosekolonnene redigeres, mens kolonnene for PY-salg og kontrakter.

> [!NOTE] 
> Som standard vil du være begrenset til 36 kolonner med mindre du utvider budsjetteringsplanleggingen med trinnene i [Utvide budsjettplanleggingsoppsettet](./extending-budget-planning-layout.md).

### <a name="templates"></a>Maler

I **Oppsett**-delen av siden **Budsjettplanleggingskonfigurasjon** kan du også generere, vise eller laste opp Excel-maler. Disse malene er arbeidsbøkene som er knyttet til hver budsjettplanen for å gi tilgang til flere funksjoner for analyse, diagrammer og dataregistrering. 

Du kan generere, vise eller laste opp en mal for hvert oppsett. Når det genereres en mal, låses oppsettet og kan ikke redigeres. Denne låsen bidrar til å garantere at malformatet samsvarer med oppsettet for budsjettplanen og inneholder de samme dataene. Når det genereres en mal, kan den vises og redigeres. Du kan for eksempel legge til diagrammer i malen eller tilpasse utseendet.

> [!NOTE] 
> Malen må lagres til en plassering som brukeren har tilgang til, slik at den kan lastes opp i oppsettet når redigering er fullført. Da brukes malen med budsjettplaner som bruker oppsettet.

### <a name="descriptions"></a>Beskrivelser

Beskrivelsene som du kan tilordne i delen **Oppsett**, brukes til å vise navnet på en finansdimensjon som er inkludert i et oppsett. En organisasjon vil for eksempel kanskje vise hovedkontonavnet ved siden av hovedkontonummeret i en budsjettplan, men vil kanskje utelate navnene på andre finansdimensjoner for å unngå en uoversiktlig visning.

## <a name="setting-up-budget-planning-processes"></a>Definere budsjettplanleggingsprosesser

Når du er ferdig med å konfigurere budsjettplanlegging, kan du definere budsjettplanleggingsprosesser på siden **Budsjettplanleggingsprosess**. Budsjettplanleggingsprosesser er sett med regler som fastsetter hvordan budsjettplaner kan oppdateres, rutes, vurderes og godkjennes i budsjetteringsorganisasjonshierarkiet. 

For hver budsjettplanleggingsprosess velger du først en budsjettsyklus og en finanskonto. Hver budsjettplanleggingsprosess er relatert til bare én budsjettsyklusen og finanskonto. Velg deretter budsjettorganisasjonshierarkiet i hurtigfanen **Prosessadministrasjoner for budsjettplanlegging**, og tilordne en arbeidsflyt for budsjettplanlegging til alle ansvarssentre i organisasjonen som vises i rutenettet. 

Hvis du vil tilordne eller endre arbeidsflyten for budsjettplanlegging for lignende typer ansvarssentre, klikker du **Tilordne arbeidsflyt**, og deretter velger du den aktuelle organisasjonstypen og arbeidsflyten for budsjettplanlegging du vil bruke. ID-en for budsjetteringsarbeidsflyt som er tilknyttet hver budsjettplanleggingsarbeidsflyt, legges automatisk til i rutenettet. 

Når du definerer stadiereglene og -malene i hurtigfanen **Stadiumsregler og oppsett for budsjettplanlegging**, kan du definere et annet sett med regler og standardoppsett for hvert budsjettplanleggingsstadium. Estimatstadiet for salgsavdelingen kan for eksempel la brukere endre linjene i en budsjettplan, men hindre at brukere legger til linjer. Innsendingsstadiet kan la brukerne vise linjene, men ikke legge til eller endre dem, fordi arbeidet på dette stadiet er fullført, og endringer i budsjettplanene må hindres. Hvis du vil velge oppsettene som er tilgjengelige for budsjettplaner, klikker du **Alternative oppsett**. 

Du kan også velge budsjettplanleggingsprioriteter i hurtigkategorien **Prioritetsbegrensninger for budsjettplan**. Prioriteter kan deretter velges for budsjettplaner. 

Det siste trinnet er å aktivere budsjettplanleggingsprosessen via **Handlinger**-menyen. En budsjettplanleggingsprosess kan ikke brukes før den er aktivert. 

På **Handlinger**-menyen kan du også opprette en ny prosess ved å kopiere en eksisterende prosess. Denne funksjonen er nyttig for organisasjoner som følger den samme prosessflyten hver enkelt budsjettsyklus og gjøre noen få eller ingen endringer. 

En annen nyttig kommando på **Handlinger**-menyen er **Vis budsjettprosesstatus**. Denne kommandoen viser grafisk budsjettplanene i en prosess, sammen med relevante data, for eksempel planens arbeidsflytstatusen, sammendrag etter beløp og enhet, og ettklikksnavigering for budsjettplanene.

[![Status for budsjettplanleggingsprosess](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)



