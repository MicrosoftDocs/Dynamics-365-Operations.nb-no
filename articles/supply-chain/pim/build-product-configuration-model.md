---
title: Oversikt over produktkonfigurasjon
description: Behovet for å konfigurere produkter som dekker spesielle behov, er i ferd med å blir regelen i stedet for unntaket, både i relasjoner for bedrift-til-bedrift og firma-til-kunde.
author: cvocph
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e0e98cf1a953355515f9145483aed8cbaa2ad2
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653654"
---
# <a name="product-configuration-overview"></a>Oversikt over produktkonfigurasjon

[!include [banner](../includes/banner.md)]

Behovet for å konfigurere produkter som dekker spesielle behov, er i ferd med å blir regelen i stedet for unntaket, både i relasjoner for bedrift-til-bedrift og firma-til-kunde.

En produsent som støtter konfigurer-til-ordre-scenarier har mulighet til bedre å ivareta kundens behov. Ved å lagre halvferdige varer i form av generelle komponenter i stedet for ferdige produkter, kan produsenten dessuten redusere kapitalen som er bundet til lager.  

En vellykket flytting fra et oppsett for produksjon-til-lager til et oppsett for konfigurer-til-ordre krever nøye analyse av produktstrukturen, identifikasjon av produktfamilier og komponentoppdeling. Hvis du vil redusere antall deler og minimere antall varer som inngår i prosessen, er det svært viktig at du forstår produktgrensesnittet og at du utformer for gjenbruk.  

Det finnes flere modelleringsprinsipper for produktkonfigurasjon, for eksempel regelbasert, dimensjonsbasert og begrensningsbasert modellering. Undersøkelser viser at metoden begrensningsbaserte kan redusere antall kodelinjer i modeller med omtrent 50 prosent sammenlignet med andre modelleringsprinsipper. Denne metoden kan derfor redusere de totale eierskapskostnadene (TCO). Ved å flytte fra en regelbasert modell som er basert på X++-kode, til en begrensningsbasert, trenger du ikke lenger en utviklerlisens for å vedlikeholde produktmodeller.

## <a name="product-configuration"></a>Produktkonfigurasjon
Industrialiseringsperioden har ført til gode resultater for produksjon av produkter av høy kvalitet og med mange funksjoner til rimelige priser. Stordriftsfordeler har gjort det mulig for de fleste i den industrialiserte verden til å kjøpe biler, TV-er, husholdningsapparater og andre varer, som de fleste av oss anser som en nødvendig del av vårt dagligliv.  

Siden mange produkter har blitt varer, har det oppstått et behov for å skille dem. Det umiddelbare svaret fra produsenter på denne utfordringen har vært å opprette varianter av hvert produkt, slik at kunder som flere alternativer. Denne strategien har ført til økte prognoseutfordringer, og også en økning i lagerkostnaden og usolgt produkter som er foreldet.  

Ved å ta i bruk en konfigurer-til-ordre-filosofi, har produsenter en mulighet til å oppfylle kundens behov for unike produkter og samtidig redusere eller eliminere foreldede lagervarer. Når en produksjon-til-lager-filosofi flyttes til en konfigurer-til-ordre-filosofi, er én umiddelbar utfordring som oppstår at behovet for korte leveringstider må balanseres mot lav lagernivåer.  

Nøkkelen til suksess her er å analysere produktporteføljen nøye og se etter mønstre i både produktfunksjoner og prosesser. Målet er å identifisere generelle komponenter som kan produseres av det samme utstyret og brukes i alle varianter.  

Det nye funksjonssettet for produktkonfigurasjon inneholder et brukergrensesnitt (UI) som gir en visuell oversikt over modellstrukturen for produktkonfigurasjonen samt en forklarende begrensningssyntaks som ikke trenger å være komplisert. Det er derfor enklere å komme i gang for firmaer som vil støtte en konfigurasjonsfremgangsmåte. Som avsnittene nedenfor beskriver, krever en produktdesigner ikke lenger støtten til en utvikler for å bygge en produktkonfigurasjonsmodell, test den og frigi den til salgsorganisasjonen.

## <a name="building-a-product-configuration-model"></a>Bygge en produktkonfigurasjonsmodell
Det er flere fremgangsmåter som en bruker kan bruke for å bygge en produktkonfigurasjonsmodell. Ett alternativ er å følge en sekvensiell flyt ved først å opprette alle referansedataene, for eksempel produktstandarder, spesifikke produkter og driftsressurser, og deretter inkludere dem som komponenter, stykklistelinjer, ruteoperasjoner og andre elementer i produktkonfigurasjonsmodellen. Du kan også velge en mer interaktiv tilnærming ved å først opprette modellen og deretter legge til referansedata ved behov.

### <a name="components"></a>Komponenter

En produktkonfigurasjonsmodell består av én eller flere komponenter som er knyttet sammen gjennom delkomponentrelasjoner. Komponentene defineres én gang og kan deretter brukes mange ganger i én eller flere produktkonfigurasjonsmodeller. Komponentene er de viktigste byggeblokkene i en produktkonfigurasjonsmodell, og nesten all informasjon om modellen er knyttet til dem..

### <a name="attributes"></a>Attributter

Hver komponent har én eller flere attributter som identifiserer de tilhørende egenskapene. Attributtene er hva brukerne velger under konfigurasjonsprosessen. Attributter kontrollere både relasjoner i og mellom komponenter gjennom inkludering i begrensninger eller beregninger. Attributtene kan brukes til å bestemme hvilke fysiske deler det konfigurerte produktet består av gjennom betingelser som brukes på stykklistelinjer. Et attributt kan også angi egenskapen for en stykklistelinje gjennom en tilordningsmekanisme. Det finnes en liknende funksjon for ruteoperasjoner når det gjelder både inkludering og innstillinger for egenskap.

>[!NOTE]
> Når du oppretter attributtyper, må du unngå å opprette en stort antall verdier for attributtypedomene. Dette kan føre til redusert ytelse for produktkonfiguratoren. 

### <a name="expression-constraints"></a>Uttrykksrestriksjoner

Bruk av en begrensningsbasert produktkonfigurasjonsmodell betyr at det finnes noen begrensninger når brukeren velger verdier for de forskjellige attributtene. Slike begrensninger kan implementeres som uttrykksbegrensninger ved hjelp av OML (Optimization Modeling Language). Det kan også implementeres en begrensning i form av en tabellbegrensning.

### <a name="table-constraints"></a>Tabellbegrensninger

Tabellbegrensninger kan være brukerdefinerte eller systemdefinerte.  

En brukerdefinert tabellbegrensning bygges av brukeren. Brukeren velger en kombinasjon av attributtyper til å representere kolonnene i tabellen, og deretter angis verdier fra områdene til de valgte attributtypene, slik at de utgjør radene i tabellbegrensningen.  

En systemdefinert tabellbegrensning defineres ved å velge hvilken tabell som skal brukes som referanse, og deretter velges feltene fra denne tabellen, slik at de utgjøre kolonnene i begrensningen. Radene i tabellbegrensningen er radene i Supply Chain Management-tabellen som finnes under konfigurasjonen.  

En tabellbegrensning inkluderes i en produktkonfigurasjonsmodell ved å referere til tabellbegrensningsdefinisjonen og tilordne de aktuelle attributtene i modellen til kolonnene i tabellbegrensningen.

### <a name="calculations"></a>Beregninger

Beregninger representerer en mekanisme for å utføre aritmetiske operasjoner i en konfigurasjonsmodell. En beregning kan for eksempel bestemme lengden på en bestemt type råvare eller behandlingstiden for en poleringsoperasjon. Beregninger er viktig og angir verdien for et målattributt etter at alle attributtverdiene som er inkludert i beregningsuttrykket, blir tilgjengelige.

### <a name="subcomponents"></a>Underkomponenter

Delkomponenter representerer nodene i strukturen for produktkonfigurasjonsmodellen. For hver delkomponentrelasjon må det være angitt en referanse til en produktstandard som er satt til restriksjonsbasert konfigurasjon for variantkonfigurasjonsteknologi.

### <a name="user-requirements"></a>Brukerkrav

Et bruker behov har alle bestanddelene til en delkomponent. Den eneste forskjellen er at et brukerbehov ikke er bundet til en produktstandard. Den praktisk effekten av denne forskjellen er at alle stykklistelinjer eller ruteoperasjon som er definert i forbindelse med et brukerkrav, skjules i den overordnede strukturen for komponentstykkliste eller ruten. Dette ligner virkemåten til en fantomstykkliste.

### <a name="bom-lines"></a>Stykklistelinjer

Stykklistelinjer inkluderes for å identifisere produksjonsstykklisten for hver komponent. En stykklistelinje må referere til en vare, og alle vareegenskaper kan settes til en fast verdi eller tilordnes et attributt.

### <a name="route-operations"></a>Ruteoperasjoner

Ruteoperasjoner er inkludert for å identifisere produksjonsruten. En ruteoperasjon må referere til en definert operasjon, og alle operasjonsegenskaper kan settes til en fast verdi. Alle egenskaper unntatt ressursbehov, kan tilordnes et attributt i stedet for en verdi.

## <a name="validating-and-testing-a-product-configuration-model"></a>Validere og teste en produktkonfigurasjonsmodell
Validering av en produktkonfigurasjonsmodell kan oppstå på flere nivåer i modellen og kan derfor dekker ulike områder. Det er det laveste nivået er for én enkelt uttrykksbegrensning. I slike tilfeller utføres validering vanligvis av produktdesigner for å kontrollere at syntaksen i et uttrykk er riktig.  

På samme måte kan en betingelse for en stykklistelinje eller ruteoperasjon valideres isolert.  

Validering kan også gjøres for en brukerdefinert definisjon av tabellbegrensning. I slike tilfeller kan brukeren bekrefte at verdiene som er angitt for hvert felt, er i området for de tilsvarende attributtypene.  

Til slutt kan du gjøre validering for en fullstendig produktkonfigurasjonsmodell for å kontrollere at den fullstendige syntaksen er riktig og at alle navne- og modelleringskonvensjoner overholdes.

### <a name="testing"></a>Testing

Testing av en modell ligner på kjøring av en faktisk konfigurasjonsøkt. Brukeren kan gå gjennom konfigurasjonssidene og kontrollere at modellstrukturen støtter konfigurasjonsprosessen. Brukeren kan kontrollere at attributtverdiene er riktige og at attributtbeskrivelsene veileder brukeren for å velge de riktige verdiene. Når en testøkt er fullført, prøver systemet å opprette stykklisten og ruten som tilsvarer de valgte attributtverdiene, og viser en feilmelding hvis noe går galt.

### <a name="the-configuration-page"></a>Konfigurasjonssiden

Hvis du vil navigere mellom komponenter, klikker du **Neste** eller klikker en komponent i modelltreet for produktkonfigurasjon for å fokusere på den.

## <a name="finalizing-a-model-for-configuration"></a>Fullfører en modell for konfigurasjon
Når en produktkonfigurasjonsmodell er klar til å brukes i konfigurere-til-ordre-scenarier, må en versjon opprettes. Det er imidlertid flere alternativer som kan forbedre modelleringsopplevelsen.

### <a name="user-interface"></a>Brukergrensesnitt

Brukergrensesnittet for konfigurasjon kan endres ved å introdusere attributtgrupper i én eller flere delkomponenter. En slik gruppering kan utheve relasjonene mellom bestemte attributter og gjøre det enklere for brukeren å identifisere området av produktet som er i fokus.

### <a name="templates"></a>Maler

Én eller flere konfigurasjonsmaler kan opprettes for å øke hastigheten på konfigurasjonsprosessen. Maler kan også opprettes for å fremme spesifikke attributtkombinasjonene, for eksempel når en salgskampanje fokuserer på et bestemt sett med produktfunksjoner.

### <a name="translations"></a>Oversettelser

Hvis produktet skal selges i forskjellige land/områder, kan det opprettes oversettelser for all tekst som vises i brukergrensesnittet for konfigurasjon. Denne teksten inneholder ikke bare navn- og beskrivelsesfelt, men også verdier for attributtekst.

### <a name="versions"></a>Versjoner

Det siste og viktigste trinnet i sluttbehandlingsprosessen er å opprette en versjon for produktkonfigurasjonsmodellen. Versjonen representerer relasjonen mellom produktstandarden, som kan velges for konfigurasjon i en ordre eller tilbudslinjen, og produktkonfigurasjonsmodellen. En versjon må være godkjent og aktivert før den kan brukes i en konfigurasjonsprosess.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Utvide en produktkonfigurasjonsmodell via API
En dedikert API (application programming interface) er implementert, slik at partnere og andre som har en utviklerlisens, kan utvide funksjonaliteten i en produktkonfigurasjonsmodell. Hovedmålet er å opprette en mekanisme som lar partnere og kunder som bruker den eksisterende produktkonfiguratoren, overføre koden som er innebygd i produktkonfiguratormodeller til API-en. På denne måten kan de overføre modellene fra Produktkonfigurator til en produktkonfigurasjon. Nye partnere og kunder kan imidlertid også dra nytte av å bruke API-en til å utvide nye produktkonfigurasjonsmodeller.

### <a name="pcadaptor-class"></a>PCAdaptor-klasse

API-en er implementert ved hjelp av et sett med **PCAdaptor**-klasser som avdekker datastrukturen i produktkonfigurasjonsmodellene. En forekomst av **PCAdaptor**-klassen må opprettes for hver modell som skal utvides. Når en konfigurasjonsøkt er fullført, ser systemet etter en forekomst av denne klassen, og kjører den hvis det blir funnet.  

Flytdiagrammet nedenfor gir en oversikt over prosessen.  

[![Flytdiagram](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Flytdiagram for produktkonfigurasjons-API

## <a name="product-configuration"></a>Produktkonfigurasjon
Produktkonfigurasjonen kan utføres fra følgende steder:

-   Salgsordrelinje
-   Salgstilbudslinje
-   Bestillingslinje
-   Produksjonsordrelinje
-   Varebehovslinje (prosjekt)

Formålet med konfigurasjonen er å opprette en spesifikk variant av produktet som oppfyller kundens behov. Det opprettes en unik konfigurasjons-ID for hver ny konfigurasjon. Denne ID-en kan spore gjennom lageret.

### <a name="multiple-sites-and-intercompany"></a>Flere områder og konserninterne

Hvis konfigurasjonen utføres på et område, eller med et firma, som er forskjellig fra området eller firmaet der produksjonen skal foregå, blir stykklisten og ruten opprettet for og plassert på leverandørområdet hos leveringsfirmaet. Produktvarianten lanseres i alle firmaene som deltar i forsyningskjeden.



