---
title: Oppgrader Dynamics AX 2012 til Dynamics 365 for Finance and Operations, Enterprise edition
description: "Dette emnet beskriver prosessen som kunder som kjører Microsoft Dynamics AX 2012, kan bruke til å flytte data og kode til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: nb-no
ms.lasthandoff: 06/15/2017

---

# Oppgradere Microsoft Dynamics AX 2012 til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition
<a id="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition" class="xliff"></a>

[!include[banner](../includes/banner.md)]

I plattformoppdatering 8 inneholder Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, en oppgraderingsbane som kunder som kjører Microsoft Dynamics AX 2012 kan bruke til å flytte data og kode til Finance and Operations. Oppgraderingsprosessen er bygd på følgende elementer:

- Verktøy som hjelper deg å bringe eksisterende egendefinerte programkode videre fra AX 2012.
- En dataoppgraderingsprosess som du kan bruke til å videreføre databasen. Derfor kan du oppgradere hele transaksjonsloggen.

## Oversikt
<a id="overview" class="xliff"></a>

Hele oppgraderingsprosessen kan vises som tre overordnede faser: analysere, kjøre, og validere.

Diagrammet nedenfor viser den komplette oppgraderingsprosessen, og aktivitetene vi anser som en del av hver fase. 

![Oppgraderingsprosess](./media/upgrade-process.png)

## Analyser
<a id="analyze" class="xliff"></a>

Aktivitetene i analysefasen hjelper det å estimere innsatsen som kreves for oppgraderingen. De gjør det også enklere å forberede en prosjektplan. Disse aktivitetene kan gjøres før du kjøper Finance and Operations. De hjelper deg med å ta en informert innkjøpsbeslutning ved hjelp av et datapunkt om arbeid og ressurser som kreves.

### Registrere deg for en offentlig Forhåndsvisning i LCS
<a id="sign-up-for-a-public-preview-in-lcs" class="xliff"></a>

Hvis du vil utføre analyseaktiviteter før du kjøper Finance and Operations, kan du registrere deg for en offentlig forhåndsvisning. Med den offentlige forhåndsvisningen kan du distribuere dine egne Finance and Operations-miljøer. Det gir deg også tilgang til verktøyene i Microsoft Dynamics Lifecycle Services (LCS) som brukes til å evaluere AX 2012-miljøet ditt og din eksisterende egendefinerte kode.

Hvis du har et eksisterende prosjekt i LCS for AX 2012, må du fremdeles registrere deg for enda et nytt prosjekt for å evaluere Finance and Operations.

Hvis du vil ha informasjon om hvordan du får en offentlig forhåndsvisning for kunder, kan du gå til https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Hvis du vil ha informasjon om hvordan du får en offentlig forhåndsvisning for partnere, kan du gå til https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Vær oppmerksom på at denne offentlige forhåndsvisningen er forskjellig fra en [30-dagers prøveversjon](https://aka.ms/D365OperationTrials). Prøveperioden på dager gir en distribuert forekomst av Finance and Operations som du kan bruke til å utforske og evaluere programmet. Analyser-aktivitetene krever imidlertid full LCS-erfaring og -verktøy.

### Velge oppgraderingsmetoder
<a id="select-the-upgrade-methodology" class="xliff"></a>
I det nye LCS-prosjektet setter du prosjektmetoden til **Oppgrader AX 2012 til Dynamics 365 for Operations**. Denne metoden er laget spesielt for AX 2012-kunder som oppgraderer. Den beskriver de tre fasene i detalj og inneholder koblinger til den tilhørende dokumentasjonen om prosessen.

![Oppgraderingsmetode(./media/methodology.png)
 
### Kjøre analyse av oppgradering
<a id="run-the-upgrade-analyzer" class="xliff"></a>
Analyseverktøyet for oppgradering kjører mot AX 2012-miljøet ditt, og identifiserer oppgaver du må gjøre for å klargjøre AX 2012-miljøet, for å gjøre oppgraderingen jevnere og rimeligere:

- **Dataopprydding** – Denne prosessen hjelper deg med å finne data som du kan fjerne uten å forårsake tap av funksjonalitet. Verktøyet identifiserer ulike typer data som du kan redusere ved å kjøre en oppryddingsprosess. For hver type data gis det en forklaring om virkningen av oppryddingen. Du bestemmer deretter om du vil kjøre oppryddingsprosessen. Deler av kostnaden med Finance and Operations-abonnementet er basert på størrelsen på databasen. Ved å redusere størrelsen reduserer du derfor denne komponenten av abonnementkostnaden og bidrar også til å redusere tiden som kreves oppgraderingens aktiveringsprosessen. En mindre database bidrar til å sikre en raskere oppgradering.
- **SQL-konfigurasjon** – Denne prosessen gjennomgår SQL-konfigurasjonen og anbefaler optimalisering. Ved å sørge for at SQL fungerer optimalt, hjelper denne prosessen med å redusere tiden som kreves for oppgraderingens aktiveringsprosess.
- **Utgåtte funksjoner** – Denne prosessen identifiserer funksjoner som du bruker, men som ikke er tilgjengelige i Finance and Operations. Prosessen kan derfor hjelpe deg å oppdage hull i funksjonalitet på et tidlig tidspunkt. Den inneholder også forslag til alternativer.

I tillegg, som en del av dette trinnet, må du installere KBXXXXXXX i AX 2012-miljøet. Denne hurtigreparasjonen inneholder en sjekkliste for føroppgradering. Du kan bruke denne sjekklisten til å angi data som kreves for oppgraderingsprosessen i AX 2012-miljøet. I én sjekklisteoppgave for føroppgradering oppgir du for eksempel Microsoft Azure Active Directory (AD Azure)-påloggingsinformasjon for hver gjeldende bruker av AX 2012, slik at hver bruker kan logge seg på Finance and Operations.

Resultatet av dette trinnet blir arbeidsflyten i oppgraderingsprosjektplanen for AX 2012-systemadministratorer.

Hvis du vil ha mer informasjon, kan du se se [Analyse: Bruke analyse av oppgradering til å planlegge overføringsarbeid](upgrade-analyzer-tool.md).

### Kjøre verktøy for estimering av kodeppgradering
<a id="run-the-code-upgrade-estimation-tools" class="xliff"></a>
Dette trinnet tar koden fra AX 2012, konverterer den til det nye formatet og gir tilbakemelding om konflikter som en utvikler må løse senere. Dette trinnet danner grunnlaget for beregningen av kostnaden av kodeoppgraderingen.

For å fullføre dette trinnet, må du eksportere koden fra AX 2012 som en modellagereksport og laste den opp til oppgraderingsverktøyet for LCS-kode. Verktøyet for kodeoppgradering fremstiller en oppgradert versjon av koden og en rapport om de gjenstående konfliktene som må løses. Utvikleren kan deretter gå gjennom både den oppgraderte koden og rapporten for å fastsette innsatsen som kreves for å oppgradere kodebasen.

Resultatet av dette trinnet utgjør arbeidsflyten i oppgraderingsprosjektplanen for Microsoft Dynamics AX-utviklere.

Hvis du vil ha mer informasjon, kan du se [Analyse: Anslå hva som må gjøres for å oppgradere kode](analyze-code-upgrade.md).

### Distribuere et demomiljø
<a id="deploy-a-demo-environment" class="xliff"></a>
Demomiljøer er standardmiljøer som inneholder demonstrasjonsdata (ikke dine egne data) og standardkoder (ingen tilpassinger). Vi anbefaler at du distribuerer et demomiljø for å evaluere de nye funksjonene, og hvis du vil utføre en grunnleggende gapanalyse av standardprosesser som brukes i AX 2012, men som kanskje er endret i Finance and Operations. Du kan enten distribuere disse demomiljøene i Azure eller laste ned dem som en virtuell maskin (VM) som du kjører på din egen maskinvare. Hvis du bruker dem i Azure, må du angi Azure-abonnementet, fordi du fremdeles bruker et prosjekt for offentlig forhåndsvisning og ennå ikke har kjøpt et Finance and Operations-abonnement.

Resultatet av dette trinnet utgjør arbeidsflyten i oppgraderingsprosjektplanen for dine funksjonelle brukere eller bedriftsbrukere.

Hvis du vil ha mer informasjon, se [Analyse: Distribuere et sandkassemiljø](analysis-sandbox.md)

### Opprette en prosjektplan
<a id="create-a-project-plan" class="xliff"></a>
En mal for en prosjektplan leveres i oppgraderingsmetoder. I dette trinnet brukes utdataene fra de forrige trinnene i analysefasen til å fylle prosjektplanen for oppgraderingsprosjektet. Prosjektplanen inneholder også alle testdetaljer: testing av dataoppgradering, overgangstesting, gjentakelser av funksjonelle beståtte tester og detaljer om de forskjellige ressurstildelingene for disse oppgavene..

På dette stadiet gir prosjektplanen et datapunkt som kan hjelpe deg med å forstå tiden og kostnadene som en oppgradering til Finance and Operations vil innebære.

## Utfør
<a id="execute" class="xliff"></a>
I Utfør-fasen går du gjennom oppgavene som du har planlagt i analysefasen. Hvis du vil flytte til den Utfør-fasen, må du kjøpe Finance and Operations, og du må ha tilgjengelige ressurser som kan arbeide med oppgraderingen.

### Bytte til LCS-implementeringsprosjektet
<a id="switch-to-the-lcs-implementation-project" class="xliff"></a>
Offentlig forhåndsvisningsprosjektet som du brukte for analysefasen, er har tjent sitt formål. Nå kan du slette det. For de gjenværende trinnene trenger du bare prosjektplanen som du opprettet i det siste trinnet i analysefasen.

Når du kjøper et abonnement på Finance and Operations, får du informasjon om hvordan du registrerer deg for et nytt LCS-prosjekt. Dette prosjektet er kjent som et implementeringsprosjekt og er det permanente LCS-prosjektets for abonnementet, så lenge du har dette abonnementet. Dette prosjektet er forskjellig fra prosjektet offentlig forhåndsvisning ved at det aministreres av Microsoft. Dette prosjektet har derfor disse egenskapene:

- Azure er vert for alle miljøer i prosjektet.
- Azure-abonnementet som er knyttet til prosjektet blir administrert av Microsoft. Derfor er det ingen separat betaling for Azure-kostnader. Kostnadene dekkes av abonnementet på Finance and Operations.
- Produksjonsmiljøet i prosjektet vedlikeholdes av Microsoft. Derfor kjøres kodedistribusjoner, oppgraderinger og vedlikehold av infrastruktur direkte fra Microsoft, ikke av ansatte. 

### Utføre de forberedende aktivitetene i AX 2012
<a id="perform-the-ax-2012-preparation-tasks" class="xliff"></a>
Utføre oppgavener som analyseverktøyet for oppgradering oppdaget, og som er dokumentert i prosjektplanen for oppgradering. Din systemansvarlig for Microsoft Dynamics AX og databaseadministrator (DBA) må fullføre disse oppgavene.

[Dataoppgradering fra AX 2012 til Dynamics 365 for Operations – sjekkliste for føroppgradering i AX 2012](prepare-data-upgrade.md)

### Utfør oppgradering
<a id="perform-code-upgrade" class="xliff"></a>
Fullfør oppgavene som ble planlagt i løpet av trinnet for estimering av kodeppgradering i analysefasen. Utviklerne må kjøre disse oppgavene.

Fra nå og fremover, bør kodeendringer i AX 2012 låses. Bare akutte kodeendringer skal tillates i AX 2012. Hvis det gjøres en endring, må den overføres manuelt til den nye kodebasen.

### Utvikle ny kode
<a id="develop-new-code" class="xliff"></a>
Fullfør oppgavene gapanalysen som ble utført under trinnet "Distribuere et demomiljø" i analysefasen. Disse oppgavene vil sannsynligvis være en blanding av funksjonelle oppgaver som definerer konfigurasjons- og utviklingsoppgavene for tilpasninger som er knyttet til nye funksjoner som blir tatt opp.

### Dataoppgradering (utviklingsmiljø)
<a id="data-upgrade-development-environment" class="xliff"></a>
Når kodeoppgraderingsoppgavene er fullført, kan du oppgradere databasen AX 2012 til Finance and Operations for første gang. Denne første oppgraderingen skjer i et utviklingsmiljø, slik at du lettere kan utbedre eller feilsøke problemer som blir funnet på dette stadiet. Et problem kan feilsøkes umiddelbart i et utviklingsmiljø, kode kan justeres og oppgraderingen kan kjøres på nytt i løpet av minutter. Større sandkassemiljøer tilbyr ikke denne fleksibiliteten, og trenger minst flere timer for å feilsøke og reparere problemer, oppdatere koden, distribuere den oppdaterte koden og kjøre oppgraderingen på nytt.

Illustrasjonen nedenfor viser prosessen. Bare ta en sikkerhetskopi av AX 2012-databasen, last den opp til Azure, gjenopprett Finance and Operations-miljøet, og kjør deretter dataoppgraderingen.

![Dataoppgradering i et utviklingsmiljø](./media/data-upgrade-dev.png)
 
Dataoppgraderingen skjer gjennom en spesiell type pakke som kan distribueres. Den samme mekanismen brukes til å distribuere ny Finance and Operations-kode fra ett miljø til et annet miljø.

Det underliggende rammeverket som brukes til å konvertere dataene i databasen under denne prosessen, er stort sett den samme som oppgraderingsrammeverket i AX 2012 som er basert på X++ satsvise jobber som kjører **ReleaseUpdatexxx**-klasser.

Hvis du vil ha mer informasjon, se [Dataoppgradering fra AX 2012 til Dynamics 365 for Operations i et utviklingsmiljø](data-upgrade-2012.md).

### Dataoppgradering (sandkassemiljøer)
<a id="data-upgrade-sandbox-environments" class="xliff"></a>
Når dataoppgraderingen i et utviklingsmiljø er fullført, kan den samme prosessen kjøres i et sandkassemiljø. Sandkassemiljøet er miljøet hvor bedrifter og funksjonelle gruppemedlemmer kan teste forretningsprosesser ved hjelp av oppgraderte AX 2012-data og kode.

Illustrasjonen nedenfor viser prosessen for kjøring av dataoppgraderingen i et sandkassemiljø. Forskjellen her er at verktøyet ryggsekk brukes i stedet for en vanlig SQL-sikkerhetskopi. Dette verktøyet er nødvendig for å konvertere mellom Microsoft SQL Server og Azure, SQL-databasen. Det er en standard SQL-verktøy, og er ikke spesifikt for Finance and Operations.

![Dataoppgradering i et sandkassemiljø](./media/data-upgrade-sandbox.png)

Hvis du vil ha mer informasjon, se [Dataoppgradering fra AX 2012 til Dynamics 365 for Operations i et utviklingsmiljø](upgrade-data-sandbox.md).
 
## Valider
<a id="validate" class="xliff"></a>
Når du går over i fasen for validering, får du tilgjengelige miljøer som inneholder den egendefinerte koden som er oppgradert, og oppgraderte data. Denne fasen beskriver prosessen med å validere og teste at det oppgraderte miljøet fungerer slik du ønsker. Den beskriver også prosessen med å forberede aktivering.

### Teste overgangen og opprette en overgangsplan
<a id="perform-cutover-testing-and-create-a-cutover-plan" class="xliff"></a>
Begrepet _overgang_ brukes for å beskrive den endelige prosessen med å aktivere det nye systemet. Denne prosessen består av aktiviteter som forekommer når AX 2012 er slått av, og før Finance and Operations er aktivert. 

Målet med testen er å øve på overgangsprosessen. På denne måten kan du bidra til å sikre at alle som er involvert i den faktiske overgangen ved aktivering, får en jevnere opplevelse.

Det finnes to primære arbeidsflyter:

- **Teknisk arbeidsflyt** – Denne arbeidsflyten er prosessen med å kjøre dataoppgraderingen. Firmaet vil håndheve en grense for hvor mye nedetid som er tillatt. I løpet av denne nedetiden vil verken AX 2012 eller Finance and Operations være tilgjengelig. Den tekniske arbeidsflyten må kanskje justere ytelsen under dataoppgraderingsprosedyren for å overholde virksomhetens nedetidsgrense. 
- **Funksjonell arbeidsflyt** – Etter dataoppgraderingen kreves flere konfigurasjonsoppgaver Finance and Operations-miljøet. Alle disse oppgavene må dokumenteres og kvantifiseres, og en ressurs må tilordnes til dem, fordi de må passe sammen med de tekniske oppgavene innenfor virksomhetens nedetidsgrense.

Hvis du vil ha mer informasjon, kan du se 
- [Validere: Testing av overgang](upgrade-cutover-testing.md)
- [Validere: Appvalideringsprosess](app-validation-process.md)

### Funksjonell testomgang
<a id="functional-test-pass" class="xliff"></a>
Fullfør en fullstendig funksjonstest av alle forretningsprosesser. Denne testen vil være en omfattende ny test av alle forretningsprosesser som involverer Finance and Operations. Disse forretningsprosessene inneholder både gamle prosesser som ble viderreført fra AX 2012 og nye prosesser som omfatter nye funksjoner som ble tatt opp for første gang i Finance and Operations. 

Avhengig av kodekvaliteten kan utbedring av problemer og ny testing kreve flere gjentakelser av den funksjonelle testomgangen. Når et problem er løst, må du teste alle prosesser som er involvert på nytt, for å sikre at nedstrøms- eller oppstrømsprosessen ikke påvirkes av endringen.

Hvis du vil ha mer informasjon, kan du se [Valider: Funksjonstesting](upgrade-functional-validation.md).

### Sjekkliste før aktivering
<a id="pre-go-live-checklist" class="xliff"></a>
Sjekklisten før aktivering er en anbefalt prosedyre som kan hjelpe deg med å redusere faren for feil under den endelige overgangen til aktivering. Én uke før aktiveringen forfaller, må du stoppe konfigurasjonsendringer i AX 2012 (det vil si under \<modulen\>\Setup). Denne begrensningen i endringer i konfigurasjonen gjelder kun fremgangsmåter. Systemansvarlige for Microsoft Dynamics AX avtaler bare å sette endringer av denne typen på vent på dette tidspunktet.

Vi anbefaler at du også fryser kodeendringer i Finance and Operations-kodebasen. Ingen flere endringer skal være tillatt, med mindre de har blitt vurdert, og har vist at de ikke blokkerer aktiveringen.  

Når konfigurasjonsbegrensning og kodefrysing er på plass, bør dataoppgraderingen kjøres for siste gang før overgangen. På denne måten kan du kontrollere at alt fungerer som forventet. 

Hvis du vil ha mer informasjon, kan du se [Validere – Gjøre klar til aktivering](upgrade-go-live-prep.md)



### Støttede oppgraderingsbaner
<a id="supported-upgrade-paths" class="xliff"></a>
Per 2017 juni, støttes oppgradering til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, versjon 0617 fra Microsoft Dynamics AX 2012 R3. Alle kumulative oppdateringer av AX 2012 R3 støttes.

Microsoft Dynamics AX 2012 R2 og Microsoft Dynamics AX 2012 RTM støttes for øyeblikket ikke. Støtte legges til senere i 2017.

Det er bare oppgradering den skydistribuerte versjonen av Finance and Operations som støttes. Oppgradering til den lokale versjonen støttes ikke. Støtte for oppgradering til den lokale versjonen legges til senere i 2017.

