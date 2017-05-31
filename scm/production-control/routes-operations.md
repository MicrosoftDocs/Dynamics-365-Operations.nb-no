---
title: Ruter og operasjoner
description: "Dette emnet gir informasjon om ruter og operasjoner. En rute definerer prosessen med å produsere et produkt eller en produktvariant. Den beskriver hvert trinn (operasjon) i produksjonsprosessen, og rekkefølgen disse trinnene må utføres i. For hvert trinn definerer ruten også nødvendige operasjonsressurser, nødvendig oppstillingstid og operasjonstid, og hvordan kostnader skal beregnes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3abc4e6f648ecc10105346ce181d8bc752d95f17
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="routes-and-operations"></a>Ruter og operasjoner

[!include[banner](../includes/banner.md)]


Dette emnet gir informasjon om ruter og operasjoner. En rute definerer prosessen med å produsere et produkt eller en produktvariant. Den beskriver hvert trinn (operasjon) i produksjonsprosessen, og rekkefølgen disse trinnene må utføres i. For hvert trinn definerer ruten også nødvendige operasjonsressurser, nødvendig oppstillingstid og operasjonstid, og hvordan kostnader skal beregnes.

<a name="overview"></a>Oversikt
--------

En rute beskriver rekkefølgen for operasjonene som kreves for å produsere et produkt eller en produktvariant. For hver operasjon definerer ruten også operasjonsressurser som kreves, tiden som kreves for å definere og utføre operasjonen, og hvordan kostnader skal beregnes. Du kan bruke samme rute for å produsere flere produkter, eller du kan definere en unik rute for hvert produkt eller produktvariant. Du kan også ha flere ruter for samme produkt. I dette tilfellet varierer ruten som brukes, avhengig av faktorer som antallet som skal produseres. Definisjonen av en rute i Microsoft Dynamics 365 for Operations består av fire separate elementer som sammen beskriver produksjonsprosessen:

-   **Rute** – En rute som definerer strukturen til produksjonsprosessen. Den definerer med andre ord rekkefølgen av operasjonene.
-   **Operasjon** – En operasjon angir et navngitt trinn i en rute som **Montering**. Den samme operasjonen kan forekomme i flere ruter og kan ha forskjellige operasjonsnumre.
-   **Operasjonsrelasjon** – En operasjonsrelasjon definerer operasjonsegenskaper for en operasjon, for eksempel oppstillingstid og operasjonstid, kostnadskategorier, parametere for forbruk og ressurskrav. Operasjonsrelasjonen aktiverer operasjonsegenskapene som skal variere for en operasjon, avhengig av ruten som operasjonen brukes i eller produktene som produseres.
-   **Ruteversjon** – En ruteversjon definerer ruten som brukes til å produsere et produkt eller en produktvariant. Ruteversjoner aktivere ruter som skal brukes på nytt på tvers av produkter eller endres over tid. De kan også aktivere forskjellige ruter som skal brukes til å produsere det samme produktet. I dette tilfellet varierer ruten som brukes, avhengig av faktorer som lokasjon eller antallet som skal produseres.

## <a name="routes"></a>Ruter
En rute beskriver rekkefølgen for operasjonene som brukes for å produsere et produkt eller en produktvariant. Hver operasjon er tilordnet et operasjonsnummer og en etterfølgende operasjon. Rekkefølgen på operasjonene danner et rutenettverk som representeres av et styrt diagram som har ett eller flere startpunkter og ett enkelt sluttpunkt. I Dynamics 365 for Operations skilles det mellom ruter basert på strukturtypen. De to rutetypene er enkle ruter og rutenettverk. I Parametere for produksjonskontroll kan du angi om bare enkle ruter kan brukes eller om de mer kompliserte rutenettverkene kan brukes.

### <a name="simple-routes"></a>Enkle ruter

En enkel rute er sekvensielle, og det er bare ett startpunkt for ruten.  

[![Enkel rute](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Hvis du bruker bare enkle ruter i Parametere for produksjonskontroll, genererer Dynamics 365 for Operations automatisk operasjonsnumrene (10, 20, 30 og så videre) når du definerer ruten.

### <a name="route-networks"></a>Rutenettverk

Hvis du bruker mer komplekse rutenettverk i Parametere for produksjonskontroll, kan du definere ruter som har flere startpunkt og operasjoner som kan kjøres parallelt.  

[![Rutenettverk](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Merknader:**

-   Hver operasjon kan ha bare én etterfølgende operasjon, og hele ruten må slutte i én enkelt operasjon.
-   Det er ingen garanti for at flere operasjoner med samme etterfølgende operasjon (for eksempel operasjon 30 og 40 i den foregående illustrasjonen) faktisk kjøres parallelt. Ressurstilgjengelighet og -kapasitet kan sette begrensninger for hvordan operasjoner planlegges.
-   Du kan ikke bruke 0 (null) som operasjonsnummer. Dette nummeret er reservert og brukes til å angi at den siste operasjonen i ruten ikke har en etterfølgende operasjon.

### <a name="parallel-operations"></a>Parallelle operasjoner

Noen ganger kreves en kombinasjon av flere operasjonsressurser som har forskjellige egenskaper, for å utføre en operasjon. Det kan for eksempel hende en monteringsoperasjon krever en maskin, et verktøy og én arbeider for annenhver maskin for å ha oppsyn med operasjonen. Dette eksemplet kan modelleres ved hjelp av parallelle operasjoner, der én operasjon er angitt som den primære operasjonen og den andre er den sekundære.  

[![Rute som har primære og sekundære operasjoner](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Vanligvis representerer den primære operasjonen flaskehalsressursen og fastsetter operasjonstiden for sekundære operasjoner. Under planlegging som omfatter begrenset kapasitet, må imidlertid ressurser som planlegges for både den primære operasjonen og sekundære operasjoner være tilgjengelige og ha ledig kapasitet på samme tid.  

Både den primære operasjonen og sekundære operasjoner må ha det samme operasjonsnummeret (30 i den foregående illustrasjonen).  

I eksemplet ovenfor er ressursbehov for den primære operasjonen (30) maskin, mens ressurskravene for sekundære operasjoner (30' og 30'') er verktøyet og arbeideren. En 50 % belastning bidrar til å garantere at den planlagte arbeideren kan ha oppsyn med to maskiner samtidig.

### <a name="approval-of-routes"></a>Godkjenning av ruter

En rute må godkjennes før den kan brukes i planleggingen eller produksjonsprosessen. Godkjenning angir at ruteutformingen er fullført. Det samme frigitte produkt eller frigitte produktvarianten, kan ha flere godkjente ruter. Godkjenning av en rute skjer vanligvis når den første relevante ruteversjonen er godkjent. I enkelte forretningsscenarier er imidlertid godkjenning av ruten og ruteversjonen separate aktiviteter som kan omfatte ulike prosesseiere.  

Hver rute kan godkjennes eller ikke godkjennes separat. Legg imidlertid merke til at når en rute ikke godkjennes, blir alle tilknyttede ruteversjoner også ikke-godkjente. I Parametere for produksjonskontroll kan du angi om ruter kan angis som ikke-godkjent, og om godkjente ruter kan endres.  

Hvis du må ha en logg som registrerer hvem som godkjenner hver rute, kan du kreve elektroniske signaturer for rutegodkjenning. Brukerne må bekrefte sin identitet ved hjelp av en [elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Operasjoner
En operasjon er et trinn i produksjonsprosessen. I Dynamics 365 for Operations har hver operasjon en ID og en enkel beskrivelse. Tabellene nedenfor viser vanlige eksempler på operasjoner fra en maskinproduksjon.

| Operasjon  | beskrivelse        |
|------------|--------------------|
| PipeCut    | Rørkutting       |
| TIGweld    | TIG-sveising        |
| JigAssy    | Jigmontering       |
| Inspeksjon | Kvalitetsinspeksjon |

Operasjonsegenskapene for operasjonen, for eksempel oppstillingstid og operasjonstid, ressurskrav, kostnadsinformasjon og forbruksberegning, angis for operasjonsrelasjonen. (Se neste del for mer informasjon om operasjonsrelasjoner.)

## <a name="operation-relations"></a>Operasjonsrelasjoner
Følgende operasjonsegenskaper for en operasjon vedlikeholdes for operasjonsrelasjonen:

-   Kostnadskategorier
-   Forbruksparametre
-   Behandlingstider
-   Behandlingsantall
-   Ressursbehov
-   Notater og instruksjoner

Du kan definere flere operasjonsrelasjoner for samme operasjon. Hver operasjonsrelasjon er imidlertid spesifikk for én operasjon, og lagrer egenskaper som er spesifikke for en rute, et frigitt produkt eller et sett med frigitte produkter som er knyttet til en gruppe. Derfor kan den samme operasjonen brukes i flere ruter som har ulike operasjonsegenskaper. I tillegg kan du enklere å vedlikeholde hoveddataene hvis du bruker standardoperasjoner som har samme operasjonsegenskaper, uavhengig av ruten som brukes og produkter som blir produsert. Omfanget for operasjonsrelasjonen er definert gjennom egenskapene **Varekode**, **Varerelasjon**, **Rutekode** og **Ruterelasjon**, som vist i tabellen nedenfor.

| Varekode | Varerelasjon         | Rutekode | Ruterelasjon   | Omfang for operasjonsrelasjonen                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabell     | &lt;Vare-ID&gt;       | Rute      | &lt;Rute-ID&gt; | Operasjonsegenskapene for en operasjon, når den brukes i ruten der **Rutenummer**=&lt;rute-ID&gt; for å produsere det frigitte produktet der **Varenummer**=&lt;vare-ID&gt;.                                                                                                                        |
| Tabell     | &lt;Vare-ID&gt;       | Alle        |                  | Standard operasjonsegenskaper for en operasjon når den brukes for å produsere det frigitte produktet der **Varenummer**=&lt;vare-ID&gt;. Disse operasjonsegenskapene gjelder med andre ord når det ikke er en rutespesifikk operasjonsrelasjon for det frigitte produktet.                                     |
| Gruppere     | &lt;Varegruppe-ID&gt; | Rute      | &lt;Rute-ID&gt; | Operasjonsegenskapene for en operasjon når den brukes i ruten der **Rutenummer**=&lt;rute-ID&gt; for å produsere frigitte produkter som er tilknyttet varegruppe &lt;varegruppe-ID&gt;, med mindre det er en rutespesifikk operasjonsrelasjon for det frigitte produktet.                         |
| Gruppere     | &lt;Varegruppe-ID&gt; | Alle        |                  | Standard operasjonsegenskaper for en operasjon når den brukes til å produsere frigitte produkter som er tilknyttet varegruppe &lt;varegruppe-ID&gt;, med mindre det finnes en mer spesifikk operasjonsrelasjon.                                                                                                  |
| Alle       |                       | Rute      | &lt;Rute-ID&gt; | Standard operasjonsegenskaper for operasjonen når den brukes i ruten der **Rutenummer**=&lt;rute-ID&gt;. Disse operasjonsegenskapene gjelder med andre ord når det ikke er en rutespesifikk operasjonsrelasjon for det frigitte produktet. |
| Alle       |                       | Alle        |                  | Standard operasjonsegenskaper for en operasjon. Disse operasjonsegenskapene gjelder når det ikke finnes en mer spesifikk operasjonsrelasjon.                                                                                                                                                                |

Du kan også angi at en operasjonsrelasjon er spesifikk for et sted. På denne måten kan operasjonsegenskaper for en operasjon variere, avhengig av lokasjonen (det vil si stedet) der operasjonen utføres. For konfigurerte produkter kan du også angi ulike operasjonsegenskaper for hver produktkonfigurasjon.  

Operasjonsrelasjoner gir deg stor fleksibilitet når du definerer rutene. Muligheten til å definere standardegenskaper bidrar også til å redusere mengden hoveddata som du må vedlikeholde. Men denne fleksibiliteten betyr også at du må være oppmerksom på konteksten som du endrer en operasjonsrelasjon i.  

**Obs!** Siden de operajonsegenskapene lagres i operasjonsrelasjoner per operasjon per rute, har alle forekomster av den samme operasjonen (for eksempel Montering) samme oppstillingstid, operasjonstid, ressurskrav og så videre. Hvis to forekomster av en operasjon må utføres i samme rute, men har forskjellige operasjonstid, må du derfor opprette to forskjellige operasjoner, for eksempel Montering1 og Montering2.

### <a name="modifying-product-specific-routes"></a>Endre produktspesifikke ruter

Når du åpner **Rute**-siden fra siden **Detaljer om frigitt produkt**, vises ruteversjonene som er knyttet til det valgte frigitte produktet. I denne konteksten viser Dynamics 365 for Operations operasjonsegenskapene for hver operasjon fra operasjonsrelasjonen som samsvarer best med ruteversjonen. Du vil legge merke til at listen over operasjoner inneholder egenskapene **Varekode** og **Rutekode** fra operasjonsrelasjonen. Derfor kan du bestemme hvilken operasjonsrelasjon som vises.  

På **Rute**-siden kan du endre operasjonsegenskapene for operasjonen, for eksempel operasjonstiden eller kostnadskategoriene. Endringene lagres på operasjonsrelasjonen som er spesifikk for ruten og frigitt produkt som er referert til i gjeldende ruteversjon. Hvis operasjonsrelasjonen som vises ikke er spesifikk for ruten og det frigitte produktet, oppretter systemet en kopi av operasjonsrelasjonen før endringene lagres. Denne kopien *er* spesifikk for ruten og det frigitte produktet. Endringen påvirker derfor ikke andre ruter eller frigitte produkter. Hvis du vil kontrollere hvilken operasjonsrelasjon som endres på **Rute**-siden, kan du se på feltene **Varekode** og **Rutekode**.  

Du kan også manuelt opprette en operasjon som er spesifikk for en rute og et frigitt produkt ved hjelp av funksjonen **Kopier og rediger relasjon**.  

**Obs!** Hvis du legger til en ny operasjon i en rute på **Rute**-siden, opprettes en operasjonsrelasjon bare for gjeldende frigitte produkt. Hvis ruten også brukes til å produsere andre frigitte produkter, vil det derfor ikke finnes en gjeldende operasjonsrelasjon for disse frigitte produktene, og ruten kan ikke lenger brukes for disse frigitte produktene.

### <a name="maintaining-operation-relations-per-route"></a>Vedlikeholde operasjonsrelasjoner per rute

Når du åpner **Rutedetaljer**-siden fra listesiden **Ruter**, vises en liste over alle operasjonsrelasjonene som gjelder for den valgte ruten. Derfor kan du enkelt kontrollere hvilke operasjonsegenskaper som brukes for de ulike produktene. Du kan endre standard egenskapsverdier og produktspesifikke egenskapsverdier.  

Hvis du legger til en ny operasjonsrelasjon på siden **Rutedetaljer**, settes **Rutekode**-feltet automatisk til **Rute**, og **Ruterelasjon**-feltet setes til rutenummeret for gjeldende rute.

### <a name="maintaining-operation-relations-per-operation"></a>Vedlikeholde operasjonsrelasjoner per operasjon

Fra **Operasjoner**-siden kan du åpne siden **Operasjonsrelasjoner**. På denne siden kan du endre alle operasjonsrelasjoner for en bestemt operasjon. Du kan også endre operasjonsrelasjoner som inneholder standardverdier.  

Hvis virksomheten din bruker standardoperasjoner og operasjonsparameterne er de samme på tvers av alle produkter og prosesser, kan du enkelt vedlikeholde standard operasjonsegenskaper for disse operasjonene på siden **Operasjonsrelasjoner**.

### <a name="applying-operation-relations"></a>Bruke operasjonsrelasjoner

I noen tilfeller må Dynamics 365 for Operations først finner operasjonsegenskapene for en operasjon. Når for eksempel en bestilling opprettes, må operasjonsegenskapene for hver operasjon kopieres fra operasjonsrelasjonene til produksjonsruten. I slike tilfeller søker Dynamics 365 for Operations etter relevante operasjonsrelasjoner fra den mest spesifikke kombinasjonen til den minst spesifikke kombinasjonen.  

Når Dynamics 365 for Operations søker etter den mest relevante operasjonsrelasjonen for et frigitt produkt, vil en aktivitetsplan som samsvarer med vare-ID-en til det frigitte produktet, foretrekkes fremfor en operasjonsrelasjon som samsvarer med varegruppe-ID-en. En operasjonsrelasjon som samsvarer med varegruppe-ID-en foretrekkes fremfor standard operasjonsrelasjon. Søket utføres i følgende rekkefølge:

1.  **Varekode**=**Tabell** og **Varerelasjon**=&lt;vare-ID&gt;
2.  **Varekode**=**Gruppe** og **Varerelasjon**=&lt;varegruppe-ID&gt;
3.  **Varekode**=**Alle**
4.  **Rutekode**=**Rute** og **Ruterelasjon**=&lt;rute-ID&gt;
5.  **Rutekode**=**Alle**
6.  **Konfigurasjon**=&lt;konfigurasjons-ID&gt;
7.  **Konfigurasjon**=
8.  **Område**=&lt;område-ID&gt;
9.  **Område**=

En operasjon bør derfor brukes bare én gang for hver rute. Hvis operasjonen forekommer flere ganger i samme rute, vil alle forekomster av denne operasjonen ha samme operasjonsrelasjon, og du kan ikke ha andre egenskaper (for eksempel operasjonstid) for hver forekomst.

## <a name="route-versions"></a>Ruteversjoner
Ruteversjoner brukes for å tilrettelegge for variasjoner i produksjonen av produkter, eller gi større kontroll over produksjonsprosessen. De definerer hvilken rute som skal brukes når et bestemt frigitt produkt eller produktvariant produseres. Du kan bruke følgende begrensninger til å definere hvilken rute som brukes for et frigitt produkt:

-   Produktdimensjoner (størrelse, farge,konfigurasjon)
-   Produksjonsantall
-   Produksjonssted
-   Produksjonsdato

Når du skal produsere produktet på et bestemt sted, i et bestemt antall, eller i en bestemt periode, kan du angi en bestemt ruteversjon som standard ruteversjonen. Vær imidlertid oppmerksom på at bare én aktiv rute er tillatt for et bestemt frigitt produkt og et bestemt sett med begrensninger.  

I Parametere for produksjonskontroll kan du kreve at gyldighetsperioden for en ruteversjon alltid angis.

### <a name="approval-of-route-versions"></a>Godkjenning av ruteversjoner

Før en ruteversjon kan brukes i planleggingen eller produksjonsprosessen, må den godkjennes. Når du godkjenner en ruteversjon, kan du også godkjenne den relaterte ruten. Vær imidlertid oppmerksom på at en ruteversjon bare kan godkjennes hvis den relaterte ruten også godkjennes.

### <a name="activating-the-default-route-version"></a>Aktivere standard ruteversjonen

Når du aktiverer en ruteversjon, angir du den som standard ruteversjonen som hovedplanlegging skal bruke, eller som skal brukes til å opprette produksjonsordrer. Du kan bare ha én aktiv ruteversjon for et bestemt sett med betingelser (for eksempel periode, sted eller antall). Du får en feilmelding hvis versjonen som du prøver å aktivere, er i konflikt med en versjon som allerede er aktiv. Du må deretter deaktivere versjonen som er i konflikt, eller endre versjonsbegrensningene (vanligvis perioden) for ruteversjonen for å unngå en tvetydig aktivering.

### <a name="electronic-signatures"></a>Elektronisk signaturer

Hvis du må ha en logg som registrerer hvem som godkjenner og aktiverer hver ruteversjon, kan du kreve elektroniske signaturer for disse oppgavene. Brukere som godkjenner og aktiverer ruteversjoner må da bekrefte sin identitet ved hjelp av en [elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Produktendring som bruker saksbehandling

Produktendringssaken for godkjenning og aktivering av nye eller endrede ruter og ruteversjoner gjør det enkelt å få en oversikt over begrensningene for ruteversjonen. Du kan også godkjenne og aktivere alle ruter som er knyttet til en bestemt endring i én operasjon, og dokumentere resultatene i produktendringssaken.

## <a name="maintaining-routes"></a>Vedlikeholde ruter
Avhengig av dine forretningsbehov kan du kanskje redusere arbeidet som kreves for å opprettholde prosessdefinisjonene.

### <a name="making-routes-independent-of-resources"></a>Gjøre ruter uavhengige av ressurser

I mange systemer må operasjonsressursene eller ressursgruppen som utfører en operasjon angis i ruten. I Dynamics 365 for Operations kan du imidlertid definere et sett med krav som en operasjonsressurs må oppfylle for å kunne brukes for operasjonen. Den spesifikke operasjonsressursen eller ressursgruppen som skal brukes, trenger derfor ikke å bestemmes før operasjonen faktisk er planlagt. Denne funksjonen er spesielt nyttig når du har mange arbeidere eller maskiner som kan utføre den samme operasjonen.  

Du angir for eksempel at en operasjon krever en operasjonsressurs av typen **Maskin** som tillater **Stempling** opptil 20 tonn. Planleggingsmotoren vil deretter løse disse kravene til en bestemte operasjonsressurs eller ressursgruppe når operasjonen planlegges. Du har mye større fleksibilitet siden du kan angi disse kravene i stedet for å binde operasjonen til en bestemt maskin. I tillegg er vedlikehold enklere når ressurser flyttes eller nye ressurser legges til.  

Hvis du vil ha mer informasjon om de ulike typene ressurskrav og hvordan du bruker dem, kan du se Krav til operasjonsressurser og [Ressursfunksjoner](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Dele ruter på tvers av steder

Hvis du produserer det samme produktet på flere enn ett produksjonssted og trinnene for produksjon av produktet er de samme på alle steder, kan du ofte utforme en delt rute som brukes på tvers av alle produksjonsstedene. Hvis du vil opprette en delt rute, trenger du ikke selv å angi et sted på ruten. Du må imidlertid fortsatt opprette en ruteversjon som knytter den delte ruten til produktet på hvert sted.  

Du må også kontrollere at ressurskravene for hver operasjon på ruten ikke kaller bestemte operasjonsressurser eller ressursgrupper, men i stedet uttrykkes som egenskapene til de nødvendige ressursene. Planleggingsmotoren vil deretter kunne tildele de aktuelle operasjonsressursene fra stedet som produksjonen er planlagt på. Hvis det for eksempel er små forskjeller i operasjonstiden, eller hvis oppstillingstiden for en bestemt operasjon som er spesifikk for et sted, kan du angi denne informasjonen ved å legge til en ekstra operasjonsrelasjon for dette stedet.  

Hvis du vil dra full nytte av fordelene med delte ruter, bør du også bruke ressursforbruk på tilsvarende stykklister (BOM). Når du setter flagget for ressursforbruk på stykklistelinjen, vil lager og lokasjon som råvarer skal forbrukes fra, utledes fra operasjonsressursen som operasjonen er planlagt på. Derfor trenger lager og lokasjon ikke å bestemmes før produksjonen faktisk planlegges. På denne måten kan du gjøre både stykklisten og ruten uavhengig av den fysiske lokasjonen der produktet produseres.

### <a name="standard-operation-relations"></a>Standard operasjonsrelasjoner

Hvis virksomheten din bruker standardiserte operasjoner i hele produksjonen, og hvis det er liten eller ingen variasjon i oppstillingstid, operasjonstid, forbruksberegning, kostnadsberegningen og så videre, kan du dra nytte av å opprette standard operasjonsrelasjoner for alle operasjoner. I slike tilfeller skal du unngå å opprette operasjonsrelasjoner som er spesifikke for en rute eller et frigitt produkt.  

Hvis du også angir ressurskrav i form av kompetanser og funksjoner, og gjør rutene uavhengig av stedet, kan du bidra til å redusere det pågående vedlikeholdet av forretningsprosessene til et minimum.  

Når du bruker denne fremgangsmåten, blir siden **Operasjonsrelasjoner** det primære målet for vedlikehold av operasjonstid og andre egenskaper.

### <a name="resource-specific-process-times"></a>Ressursspesifikke behandlingstider

Hvis du ikke angir en operasjonsressurs eller ressursgruppe som en del av ressurskravene for en operasjon, kan gjeldende ressurser operere med ulike hastigheter. Tiden som kreves for å behandle en operasjon kan derfor variere. Hvis du vil løse dette problemet, kan du bruke **Formel**-feltet på operasjonsrelasjonen for å angi hvordan behandlingstiden beregnes. Følgende alternativer er tilgjengelige:

-   **Standard** – (Standardalternativ) Beregningen bruker bare feltene fra operasjonsrelasjonen og multipliserer den angitte operasjonstiden med ordreantallet.
-   **Kapasitet** – Beregningen inkluderer **Kapasitet**-feltet fra operasjonsressursen. Derfor er tiden ressursavhengige. Verdien som angis for operasjonsressursen er kapasitet per time. Denne verdien multipliseres med ordreantallet og **Faktor**-verdien fra operasjonsrelasjonen.
-   **Bunke** – En partikapasitet beregnes ved hjelp av informasjon fra operasjonsrelasjonen. Antall satsvise jobber, og derfor behandlingstiden, kan deretter beregnes basert på ordreantallet.
-   **Ressursbunke** – Dette alternativet er stort sett den samme som **Bunke**-alternativet. Beregningen inkluderer imidlertid **Bunkekapasitet**-feltet fra operasjonsressursen. Derfor er tiden ressursavhengige.


<a name="see-also"></a>Se også
--------

[Stykklister og formler](bill-of-material-bom.md)

[Kostnadskategorier som brukes i produksjonsruting](../cost-management/cost-categories-used-production-routings.md)

[Ressursfunksjoner](resource-capabilities.md)

[Oversikt over elektronisk signatur](/dynamics365/operations/organization-administration/electronic-signature-overview)




