---
title: Ruter og operasjoner
description: "Dette emnet inneholder informasjon om rutene og operasjonene. En rute definerer prosessen med å produsere et produkt eller en produktvariant. Den beskriver hvert trinn (drift) i produksjonsprosessen, og disse trinnene må utføres i rekkefølgen. For hvert trinn definerer ruten også nødvendige operasjonsressurser, nødvendige oppstillingstid og kjøretid, og hvordan kostnader skal beregnes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Ruter og operasjoner

Dette emnet inneholder informasjon om rutene og operasjonene. En rute definerer prosessen med å produsere et produkt eller en produktvariant. Den beskriver hvert trinn (drift) i produksjonsprosessen, og disse trinnene må utføres i rekkefølgen. For hvert trinn definerer ruten også nødvendige operasjonsressurser, nødvendige oppstillingstid og kjøretid, og hvordan kostnader skal beregnes.

<a name="overview"></a>Oversikt
--------

En rute beskriver rekkefølgen av operasjonene som kreves for å produsere et produkt eller en produktvariant. For hver operasjon definerer ruten til operasjonsressurser som kreves, tiden som kreves for å definere og utføre operasjonen, og hvordan kostnader skal beregnes. Du kan bruke samme rute for å produsere flere produkter, eller du kan definere en unik rute for hvert produkt eller produktvariant. Du kan selv ha flere ruter til samme produkt. I dette tilfellet ruten som brukes, varierer, avhengig av faktorer som antallet som må produseres. Definisjonen av en rute i Microsoft Dynamics 365 for operasjoner består av fire separate elementer som beskriver sammen produksjonsprosessen:

-   **Ruten** – en rute som definerer strukturen til produksjonsprosessen. Med andre ord definerer den rekkefølgen av operasjonene.
-   **Operasjonen** – en operasjon angir et navngitt trinn i en rute som **samlingen**. Den samme operasjonen kan forekomme i flere ruter og kan ha forskjellige operasjonsnumre.
-   **Operasjonsrelasjon** – en aktivitetsplan definerer operasjonsegenskaper for en operasjon, for eksempel oppstillingstid og kjøretid, kostnadskategorier, parametere for forbruk og ressurskrav. Operasjonsrelasjonen kan operasjonelle egenskapene for en operasjon for å variere, avhengig av ruten som brukes i operasjonen eller produktene som produseres.
-   **Ruteversjonen** – en ruteversjon definerer ruten som brukes til å produsere et produkt eller en produktvariant. Ruteversjoner aktivere ruter som skal brukes på nytt på tvers av produkter eller endret seg over tid. De kan også aktivere forskjellige ruter som skal brukes til å produsere det samme produktet. I dette tilfellet er ruten som brukes avhenger av faktorer som plasseringen eller antallet som må produseres.

## <a name="routes"></a>Ruter
En rute beskriver rekkefølgen av operasjonene som brukes til å produsere et produkt eller en produktvariant. Hver operasjon er tilordnet et operasjonsnummer og en etterfølgende operasjon. Rekkefølgen på operasjonene danner et nettverk for ruten som representeres av et styrt diagram som har én eller flere startpunkter og en enkelt sluttpunkt. I Dynamics 365 for operasjoner skiller ruter basert på typen struktur. To typer ruter er enkle ruter og ruten nettverk. Du kan angi om bare enkle ruter kan brukes, eller om de mer kompliserte Rutenettverk kan brukes i produksjonsparameterne kontroll.

### <a name="simple-routes"></a>Enkle ruter

En enkel rute er sekvensielle, og det er bare et utgangspunkt for ruten.  

[![Enkel rute](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Hvis du bruker bare enkle ruter i produksjonsparameterne kontroll, genererer Dynamics 365 for operasjoner automatisk operasjonsnumrene (10, 20, 30 og så videre) når du definerer ruten.

### <a name="route-networks"></a>Rutenettverk

Hvis du bruker mer komplekse Rutenettverk i produksjonsparameterne kontroll, kan du definere ruter som har flere første punkt og operasjoner som kan kjøres parallelt.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Merknader:**

-   Hver operasjon kan ha bare én etterfølgende operasjon, og hele ruten må slutte i én enkelt operasjon.
-   Det er ingen garanti for at flere operasjoner med samme etterfølgende operasjon (for eksempel operasjoner 30 og 40 i den foregående illustrasjonen) faktisk kjøres parallelt. Tilgjengelighet og ressurskapasiteter kan legge begrensninger på måten operasjoner planlegges.
-   Du kan ikke bruke 0 (null) som operasjonsnummeret. Dette nummeret er reservert, og brukes til å angi at den siste operasjonen i ruten har ingen etterfølgende operasjon.

### <a name="parallel-operations"></a>Parallelle operasjoner

Noen ganger kreves en kombinasjon av flere operasjonsressurser som har forskjellige egenskaper som for å utføre en operasjon. For eksempel kreve en samling operasjon en maskin og et verktøy med én arbeider for hver to maskiner kan ha oppsyn med operasjonen. I dette eksemplet kan modelleres ved hjelp av parallelle operasjoner, der én operasjon er angitt som den primære operasjonen, og den andre er sekundære.  

[![Ruten som har primære og sekundære operasjoner](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Vanligvis den primære operasjonen representerer flaskehalsressurs og fastsetter operasjonstiden for sekundære operasjoner. Men som involverer begrenset kapasitet under planleggingen, ressurser som er planlagt for både den primære operasjonen og sekundære operasjoner må være tilgjengelig og har ledig kapasitet på samme tid.  

Både den primære operasjonen og sekundære operasjoner må ha det samme operasjonsnummeret (30 i den foregående illustrasjonen).  

I eksemplet ovenfor er ressursbehov for den primære operasjonen (30), maskin, mens ressurskravene for sekundære operasjoner (30' og 30'') er verktøyet og arbeideren. En 50 % belastning kan garantere at planlagte arbeideren kan har oppsyn med to maskiner samtidig.

### <a name="approval-of-routes"></a>Godkjenning av ruter

En rute må være godkjent før den kan brukes i planleggingen eller produksjon. Godkjenning angir at ruten utformingen er fullført. Den samme utgitt produkt eller frigitt produktvariant kan ha flere godkjente ruter. Godkjenning av en rute oppstår vanligvis når den første aktuelle ruteversjonen godkjent. I enkelte bedrifter er scenarier, godkjenning av ruten og ruteversjonen separate aktiviteter som kan omfatte eiere annen prosess.  

Hver rute kan være godkjente eller ikke godkjente separat. Legg imidlertid merke til at når en rute er godkjent, er også alle tilknyttede ruteversjoner ikke er godkjent. I produksjonsparametrene kontroll kan du angi om ruter ikke kan godkjent, og om godkjente ruter kan endres.  

Hvis du må holde en logg som poster som godkjenner hver rute, kan du kreve elektroniske signaturer for godkjenning av rute. Brukerne må bekrefte sin identitet ved hjelp av en [elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Operasjoner
En operasjon er et trinn i produksjonsprosessen. I Dynamics 365 for operasjoner har hver operasjon en ID og en enkel beskrivelse. Tabellene nedenfor viser vanlige eksempler på operasjoner fra en maskin shop.

| Operasjon  | beskrivelse        |
|------------|--------------------|
| PipeCut    | Datakanalen kutting       |
| TIGweld    | TIG sveisesymbol        |
| JigAssy    | Jig-samlingen       |
| Inspeksjon | Kvalitetskontroll |

Operasjonsegenskaper for operasjonen, for eksempel oppstillingstid og kjøretid, ressurskrav, kostnadsinformasjon og beregning av forbruk, er angitt i operasjonsrelasjonen. (Hvis du vil ha mer informasjon om operasjonsrelasjoner, se den neste delen.)

## <a name="operation-relations"></a>Operasjonsrelasjoner
Følgende operasjonsegenskaper for en operasjon som vedlikeholdes på operasjonsrelasjonen:

-   Kostnadskategorier
-   Forbruk-parametere
-   Behandlingstider
-   Behandling av antall
-   Ressursbehov
-   Notater og instruksjoner

Du kan definere flere operasjonsrelasjoner for samme operasjon. Imidlertid hver operasjonsrelasjonen gjelder for én operasjon, og lagrer egenskaper som er spesifikke for en rute, frigitt produkt eller et sett med frigitte produkter som er knyttet til en gruppe. Derfor kan den samme operasjonen brukes i flere ruter som har ulike egenskaper for drift. I tillegg kan du enklere å vedlikeholde hoveddataene Hvis du bruker standard operasjoner som har samme operasjonsegenskaper, uavhengig av ruten som brukes og produkter som blir produsert. Omfanget av operasjonsrelasjonen er definert gjennom den **Varekode**, **vare relasjon**, **Route koden** og **Route relasjonen** egenskaper, som vist i følgende tabell.

| Varekode | Varerelasjon         | Rutekode | Ruterelasjon   | Omfanget av operasjonsrelasjonen                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabell     | &lt;Vare-ID&gt;       | Rute      | &lt;Rute-ID&gt; | Operasjonsegenskaper for en operasjon, når den brukes i ruten der **rutenummer**=&lt;rute-ID&gt; til å produsere det endelige produktet der **varenummer**=&lt;vare-ID-&gt;.                                                                                                                        |
| Tabell     | &lt;Vare-ID&gt;       | Alle        |                  | Standard operasjonsegenskaper for en operasjon, når den brukes til å produsere det endelige produktet der **varenummer**=&lt;vare-ID-&gt;. Med andre ord, gjelder disse operasjonelle egenskapene når det er ingen rute-spesifikke Operasjonsrelasjon for utgitt produkt.                                     |
| Gruppere     | &lt;Gruppe-ID for varen&gt; | Rute      | &lt;Rute-ID&gt; | Operasjonsegenskaper for en operasjon, når den brukes i ruten der **rutenummer**=&lt;rute-ID&gt; til å produsere frigitte produkter som er tilknyttet varegruppe &lt;vare-IDen&gt;, med mindre det er en rute-spesifikke Operasjonsrelasjon for utgitt produkt.                         |
| Gruppere     | &lt;Gruppe-ID for varen&gt; | Alle        |                  | Standard operasjonsegenskaper for en operasjon, når den brukes til å produsere frigitte produkter som er tilknyttet varegruppe &lt;vare-IDen&gt;, med mindre det finnes en mer spesifikk operasjonsrelasjonen.                                                                                                  |
| Alle       |                       | Rute      | &lt;Rute-ID&gt; | Standard operasjonsegenskaper for operasjonen når den brukes i ruten der **rutenummer**=&lt;rute-ID&gt;. Med andre ord, gjelder disse operasjonelle egenskapene når det ikke er noen Operasjonsrelasjon for denne ruten som er spesifikk for en frigitt produkt eller den tilknyttede varegruppe. |
| Alle       |                       | Alle        |                  | Standard operasjonsegenskaper for en operasjon. Disse operasjonelle egenskapene gjelder når det ikke finnes en mer spesifikk operasjonsrelasjonen.                                                                                                                                                                |

Du kan også angi at en aktivitetsplan er spesifikk for et område. På denne måten kan operasjonsegenskaper for en operasjon variere, avhengig av plasseringen (det vil si webområde) der operasjonen utføres. Du kan også angi ulike operasjonsegenskaper for hver produktkonfigurasjon for konfigurerte varer.  

Operasjonsrelasjoner gir deg mye fleksibilitet når du definerer din ruter. Muligheten til å definere egenskaper for standard bidrar også til å redusere mengden hoveddata som du må vedlikeholde. Men denne fleksibiliteten betyr også at at du må være oppmerksom på omgivelsene som du endrer en operasjonsrelasjonen i.  

**Merk:** fordi de operasjonelle egenskapene lagres i operasjonsrelasjoner per operasjon per rute, alle forekomster av den samme operasjonen (for eksempel samling) har den samme Oppstillingstid, Operasjonstid, ressurskrav og så videre. Hvis to forekomster av en operasjon må utføres i samme rute, men har forskjellige operasjonstid, må du derfor opprette to forskjellige operasjoner, for eksempel Assembly1 og Assembly2.

### <a name="modifying-product-specific-routes"></a>Endre produkt-spesifikke ruter

Når du åpner den **ruten** siden fra den **utgitt Produktbeskrivelse** siden ruteversjoner som er knyttet til det valgte frigitt produktet vises. I denne sammenhengen for hver operasjon, viser Dynamics 365 for operasjoner operasjonsegenskaper fra operasjonsrelasjonen som best passer ruteversjonen. Du vil legge merke til at listen over operasjoner som inneholder den **Varekode** og **Route koden** egenskaper fra operasjonsrelasjonen. Derfor kan du bestemme hvilke operasjonsrelasjonen skal vises.  

På den **Route** siden, kan du endre operasjonsegenskaper for operasjonen, for eksempel operasjonstiden eller kostnadskategorier. Endringene er lagret på operasjonsrelasjonen gjelder ruten og frigitt produkt som er referert til i den gjeldende ruteversjonen. Hvis operasjonsrelasjonen vises ikke er spesifikke for ruten og frigitt produkt, før endringene er lagret, opprettes det en kopi av operasjonsrelasjonen i systemet. Dette eksemplaret *er* gjelder ruten og frigitt produkt. Derfor endringene påvirker ikke andre ruter eller frigitte produkter. Kontrollere hvilke operasjonsrelasjonen blir endret på den **rute** side, se på den **Varekode** og **Route kode** felt.  

Du kan manuelt opprette en operasjon som er spesifikk for en rute og frigitt produkt ved hjelp av den **Kopier og Rediger relasjon** funksjon.  

**Merk:** Hvis du legger til en ny operasjon til en rute på den **Route** siden, opprettes en aktivitetsplan bare for gjeldende utgitt produkt. Derfor, hvis ruten er også brukt til å produsere andre frigitte produkter, ingen aktuelle operasjonsrelasjonen vil de frigitte produktene, og ruten kan ikke lenger brukes for de frigitte produktene.

### <a name="maintaining-operation-relations-per-route"></a>Vedlikeholde operasjonsrelasjoner per rute

Når du åpner den **Route detaljer** siden fra den **ruter** listeside, vises en liste over alle operasjonsrelasjonene som gjelder for den valgte ruten. Derfor kan du enkelt kontrollere hvilke operasjonsegenskaper brukes for hvilke produkter. Du kan endre både standard egenskapsverdier og produktspesifikke egenskapsverdier.  

Hvis du legger til en ny Operasjonsrelasjon på den **Route detaljer** siden den **rute koden** feltet settes automatisk til **rute**, og **Route relasjon** -feltet er satt til rutenummeret for den gjeldende ruten.

### <a name="maintaining-operation-relations-per-operation"></a>Vedlikeholde operasjonsrelasjoner per operasjon

Fra den **operasjoner** siden, kan du åpne den **operasjonsrelasjoner** siden. På denne siden kan du endre alle operasjonsrelasjoner for en bestemt operasjon. Du kan også endre operasjonsrelasjoner som inneholder standardverdiene.  

Hvis virksomheten din bruker standard operasjoner og operative parametere er den samme på tvers av alle produkter og prosesser, den **operasjonsrelasjoner** siden gir en praktisk måte å vedlikeholde standard operasjonsegenskaper av disse operasjonene.

### <a name="applying-operation-relations"></a>Bruke operasjonsrelasjoner

I noen tilfeller må Dynamics 365 for operasjoner finner operasjonsegenskaper for en operasjon. For eksempel når en bestilling er opprettet, må operasjonelle egenskapene for hver operasjon kopieres fra operation relations til produksjonsruten. I slike tilfeller søker Dynamics 365 for operasjoner relevante operasjonsrelasjoner fra den mest spesifikke-kombinasjonen til den minst spesifikke kombinasjonen.  

Når Dynamics 365 for operasjoner Søk etter de mest relevante operasjonsrelasjonen for en frigitt produkt, en aktivitetsplan som samsvarer med vare-IDen til det endelige produktet er foretrukket over en aktivitetsplan at treff-gruppen for vare-ID. I sin tur foretrekkes en aktivitetsplan som samsvarer med gruppe-IDen til varen fremfor standard operasjonsrelasjonen. Søket gjøres i følgende rekkefølge:

1.  **Varekode**=**tabell** og **element relasjonen**=&lt;vare-ID&gt;
2.  **Varekode**=**gruppe** og **element relasjonen**=&lt;vare gruppe-ID&gt;
3.  **Varekode**=**alle**
4.  **Distribuere koden**=**Route** og **Route relasjonen**=&lt;rute-ID&gt;
5.  **Distribuere koden**=**alle**
6.  **Konfigurasjon av**=&lt;konfigurasjons-ID&gt;
7.  **Configuration**=
8.  **Området**=&lt;område-ID&gt;
9.  **Site**=

En operasjon bør derfor brukes bare én gang for hver rute. Alle forekomster av denne operasjonen skal ha samme operasjonsrelasjonen Hvis operasjonen forekommer flere ganger i samme rute, og du ikke har andre egenskaper (for eksempel operasjonstid) for hver forekomst.

## <a name="route-versions"></a>Ruteversjoner
Forskjellige ruteversjoner tilrettelegger for variasjoner i produksjonen av produkter, eller gir deg større kontroll over produksjonsprosessen. De definerer hvilken rute som skal brukes når en bestemt utgitt produkt eller produktvariant for utgitt produseres. Til å definere hvilke ruteversjoner som brukes for en frigitt produkt, kan du bruke følgende begrensninger:

-   Produktdimensjoner (størrelse, farge, stil eller konfigurasjon)
-   Produksjonsantall
-   Område for produksjon
-   Produksjonsdato

Når du skal produsere produktet på et bestemt område i et bestemt antall, eller i en bestemt periode, kan du angi en bestemt ruteversjon som standard ruteversjonen. Vær oppmerksom på at bare én aktiv rute er tillatt for et gitt utgitt produkt og et gitt sett med begrensninger.  

Du kan kreve at gyldighetsperioden for en ruteversjon alltid angis i produksjonsparameterne kontroll.

### <a name="approval-of-route-versions"></a>Godkjenning av ruteversjoner

Før en ruteversjon kan brukes i planleggingen eller produksjonsprosess, må være godkjent. Når du godkjenner en ruteversjon, kan du også godkjenne relaterte ruten. Vær oppmerksom på at en ruteversjon kan godkjennes bare hvis relaterte ruten også er godkjent.

### <a name="activating-the-default-route-version"></a>Aktivere ruteversjonen standard

Når du aktiverer en ruteversjon, angir du den standard ruteversjonen som master planlegging skal bruke, eller som skal brukes til å opprette produksjonsordrer. Du kan ha bare én aktiv ruteversjon for et gitt sett med betingelser (for eksempel punktum, område eller antall). Hvis versjonen som du prøver å aktivere er i konflikt med en versjon som allerede er aktiv, får du en feilmelding. Hvis du vil hindre at en tvetydig aktivering, må du deretter deaktivere motstridende versjonen eller endre begrensninger (vanligvis periode) på ruteversjonen.

### <a name="electronic-signatures"></a>Elektroniske signaturer

Hvis du må holde en logg som poster som godkjenner og aktiverer hver ruteversjon, kan du kreve elektroniske signaturer for disse aktivitetene. Brukere som kan godkjenne og aktivere ruteversjoner må bekrefte sin identitet ved hjelp av en [elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Produkt-endring som bruker saksadministrasjon

Produktet Endre bokstavtype for godkjenning og aktivering av nye eller endrede ruter og ruteversjoner gir deg en enkel måte å vise en oversikt over ruten versjon begrensninger. Du kan også godkjenne og aktivere alle ruter som er knyttet til en bestemt endring i én operasjon, og dokumentere resultatene i produktet endrer bokstavtype.

## <a name="maintaining-routes"></a>Vedlikeholde ruter
Avhengig av dine forretningsbehov kanskje kan du å redusere arbeidet som kreves for å opprettholde definisjonene prosessen.

### <a name="making-routes-independent-of-resources"></a>Gjør ruter som er uavhengige av ressurser

I mange systemer må operasjoner ressursen eller ressursgruppen som utfører en operasjon angis i ruten. Imidlertid i Dynamics 365 for operasjoner, kan du definere et sett med krav som en ressurs for operasjoner må oppfylle for å kunne brukes for operasjonen. Derfor trenger bestemte operasjoner ressursen eller ressursgruppen som skal brukes ikke være bestemt før operasjonen faktisk er planlagt. Denne funksjonen er spesielt nyttig når du har mange arbeidere eller maskiner som kan utføre den samme operasjonen.  

Du angir for eksempel at en operasjon krever en ressurs for operasjoner av den **maskin** type som har et **Stamping** muligheten til 20 tonn. Planleggingsmotoren vil deretter løse disse kravene til en bestemte operasjoner ressursen eller ressursgruppen når operasjonen planlegges. Fordi du kan bare angi disse kravene i stedet for å binde operasjonen til en bestemt maskin, har mye mer fleksibilitet. I tillegg er vedlikehold enklere når ressurser er flyttet eller nye ressurser er lagt til.  

Hvis du vil ha mer informasjon om de ulike typene ressurskrav og hvordan du bruker dem, kan du se operasjoner ressurskrav og [ressursfunksjoner](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Dele ruter på tvers av områder

Hvis du gir det samme produktet på mer enn ett område for produksjon og trinnene for produksjon av produktet er den samme på alle områder, kan du utforme en delt rute som brukes på tvers av alle produksjonsområder ofte. Hvis du vil opprette en delt rute, ikke angi et område på selve ruten. Du må imidlertid fremdeles opprette en ruteversjon som knytter ruten delt produktet hvert område.  

Du må også kontrollere at ressurskravene for hver operasjon i ruten ikke kall for bestemte operasjonsressurser eller ressursgrupper, men i stedet er uttrykt i egenskapene til de nødvendige ressursene. Planleggingsmotoren vil deretter kunne tildele ressursene aktuelle operasjoner fra området som produksjonen er planlagt på. Hvis det er små forskjeller i kjøretiden, eller hvis oppstillingstiden for en bestemt operasjon som er spesifikk for et område, kan du angi denne informasjonen ved å legge til en ekstra Operasjonsrelasjon for dette området.  

Hvis du vil dra full nytte av fordelene med delte ruter, bør du også bruke ressursforbruk på tilsvarende stykklister (BOM). Når du setter flagg for ressursforbruk på stykklistelinjen, lager og lokasjon som skal forbrukes råvarer fra utledes fra operasjoner-ressursen blir operasjonen planlagt på. Derfor trenger lager og lokasjon ikke å være bestemt før produksjonen faktisk er planlagt. På denne måten kan du gjøre både Stykklisten og ruten uavhengig av den fysiske plasseringen der produktet er produsert.

### <a name="standard-operation-relations"></a>Standard operasjonsrelasjoner

Hvis virksomheten din bruker standardiserte operasjoner i hele produksjonen, og hvis det er liten eller ingen variasjon i Oppstillingstid, Operasjonstid, beregning av forbruk, kostnadsberegningen, og så videre, kan du dra nytte i å opprette standard operasjonsrelasjoner for alle operasjoner. I dette tilfellet skal du unngå å opprette operasjonsrelasjoner som er spesifikke for en hvilken som helst rute eller utgitt produkt.  

Hvis du også express ressurskrav i form av ferdigheter og muligheter, og gjør din ruter uavhengig av området, kan du å holde det pågående vedlikeholdet av forretningsprosessene til et minimum.  

Når du bruker denne fremgangsmåten, den **operasjonsrelasjoner** siden, blir den primære mål for vedlikehold av operasjonstid og andre egenskaper.

### <a name="resource-specific-process-times"></a>Ressurs-spesifikke behandlingstider

Hvis du ikke angir en operasjoner ressursen eller ressursgruppen som en del av ressurskravene for en operasjon, kan gjeldende ressurser operere med ulike hastigheter. Tiden som kreves for å behandle en operasjon kan derfor variere. Hvis du vil løse dette problemet, kan du bruke den **formelen** på selve operasjonsrelasjonen til å angi hvordan Behandlingstiden beregnes. Følgende alternativer er tilgjengelige:

-   **Standard** – (standard alternativ) beregningen bruker bare feltene fra operasjonsrelasjonen og multipliserer den angitte operasjonstiden med ordreantallet.
-   **Kapasitet** – beregningen omfatter den **kapasitet** felt fra operations-ressurs. Derfor er tiden ressurs-avhengige. Verdien som er angitt på operasjoner-ressurs er kapasitet per time. Denne verdien multipliseres med ordreantallet og **faktor** verdi fra operasjonsrelasjonen.
-   **Satsvis** – en satsvis kapasiteten beregnes ved hjelp av informasjon fra operasjonsrelasjonen. Antall satsvise jobber, og derfor behandlingstiden kan deretter beregnes basert på ordreantallet.
-   **Ressursen satsvis** – dette alternativet er stort sett den samme som den **satsvise** alternativet. Beregningen omfatter imidlertid den **Batch kapasitet** felt fra operations-ressurs. Derfor er tiden ressurs-avhengige.


<a name="see-also"></a>Se også
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


