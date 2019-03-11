---
title: Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver
description: Dette emnet beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.
author: perlynne
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e7c36fb912f35252d6e40d17477ac2962cbc23
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "325417"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.

Instruksjonene som lagermedarbeidere mottar på en mobil enhet, bestemmes av arbeidsmalene som du definerer i Microsoft Dynamics 365 for Finance and Operations for å definere de ulike lagerprosesser og -oppgaver. Arbeidsmaler avgjør hvordan arbeidet skal utføres for hver lagerprosess. Ved å koble et lokasjonsdirektiv til arbeidsmaler kan du bidra til å garantere at arbeid skjer i bestemte fysiske områder på lagrene.

## <a name="work-templates"></a>Arbeidsmaler
Siden **Arbeidsmaler** lar deg definere arbeidsoperasjoner som må utføres på lageret. Vanligvis består lageroperasjoner av to handlinger: en lagerarbeider plukker opp beholdning på en lokasjon og plasserer den plukkede beholdningen på en annen lokasjon. 

Arbeidsmaler består av et hode og tilhørende linjer. Hver arbeidsmal gjelder en bestemt *arbeidsordretype*. Mange arbeidsordretyper assosieres med kildedokumenter, for eksempel bestillinger eller salgsordrer. Imidlertid representerer andre arbeidsordretyper egne lagerprosesser, for eksempel syklustelling. *Arbeidspulje-ID* gir deg muligheten til å organisere arbeidet i grupper. 

Innstillingene i arbeidshodedefinisjonen kan brukes til å bestemme når et nytt stykke arbeid skal opprettes. Du kan for eksempel angi et maksimalt antall plukklinjer og maksimalt forventet plukktid. Deretter, hvis arbeidet for en salgsordreplukkingsprosess overskrider en av disse verdiene, deles dette arbeidet inn i to stykker arbeid. 

Arbeidslinjene representerer de fysiske oppgavene som kreves for å behandle arbeidet. For eksempel for en prosess for utgående lager, kan det være en arbeidslinje for å plukke opp varene i lageret og en annen linje for å plassere disse varene i et oppsamlingsområde. Det kan deretter være en ekstra linje for å plukke varene fra oppsamling og en annen linje for å plassere varene i en lastebil som en del av lastingsprosessen. Du kan angi en *direktivkode* på arbeidsmallinjene. En direktivkode er koblet til et lokasjonsdirektiv, og bidrar derfor til å sikre at lagerarbeidet blir behandlet på riktig lokasjon i lageret. 

Du kan definere en spørring til å kontrollere når en bestemt arbeidsmal brukes. Du kan for eksempel angi en begrensning slik at en bestemt mal kan brukes for arbeid bare i et bestemt lager. Du kan også ha flere maler som brukes til å opprette arbeid for utgående ordrebehandling, avhengig av salgsopprinnelsen. Systemet bruker **Serienummer**-feltet for å bestemme rekkefølgen som de tilgjengelig arbeidsmalene vurderes i. Hvis du har en bestemt spørring etter en bestemt arbeidsmal, bør du derfor gi den et lavt sekvensnummer. Denne spørringen vil deretter bli evaluert før andre, mer generelle spørringer. 

Hvis du vil stoppe eller pause en arbeidsprosess, kan du bruke innstillingen **Stopp arbeid** for arbeidslinjen. I så fall vil arbeideren som utfører arbeidet, ikke bli bedt om å utføre neste arbeidslinjetrinn. For å flytte til neste trinn må denne arbeideren eller en annen arbeider velge arbeidet på nytt. Du kan også skille oppgavene i et stykke arbeid ved å bruke en annen *arbeidsklasse-ID* på arbeidsmallinjene.

## <a name="location-directives"></a>Lokasjonsdirektiver
Lokasjonsdirektiver er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. I en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varene blir plukket og hvor de plukkede varene skal plasseres. Lokasjonsdirektiver består av et hode og tilknyttede linjer, og du oppretter dem på siden **Lokasjonsdirektiver**. 

I hodet må hvert lokasjonsdirektiv må være knyttet til en *arbeidsordretype* som angir typen lagertransaksjon som direktivet som skal brukes for, for eksempel salgsordrer, etterfylling eller råvareplukking. *Arbeidstypen* angir om lokasjonsdirektivet skal brukes for å plukke eller plassere arbeid eller en annen lagerprosess, for eksempel telle eller lagerstatusendringer. Du må også angi et *område* og et *lager*. En *direktivkode* som du angir i hodet, kan brukes til å koble lokasjonsdirektivet til én eller flere maler for arbeid. 

Som for arbeidsmaler kan du definere en spørring for å bestemme når et bestemt lokasjonsdirektiv skal brukes. Du kan for eksempel angi at når e-handel er opprinnelsen til en salgsordre, må beholdning plukkes fra et dedikert område i lageret. Systemet bruker **Serienummer**-feltet for å bestemme rekkefølgen som de tilgjengelig lokasjonsdirektivene vurderes i. 

Lokasjonsdirektivlinjene setter tilleggsbegrensninger på bruken av reglene for lokasjonssøk. Du kan angi et minimums- og maksimumsantall som direktivet skal gjelde for, og du kan angi at direktivet skal være for en bestemt lagerenhet. Hvis måleenheten for eksempel er paller, kan varer på paller plasseres på en bestemt lokasjon. Du kan også angi om antallet kan deles på tvers av flere lokasjoner. Som lokasjonsdirektivhodet har hver lokasjonsdirektivlinje et sekvensnummer som bestemmer rekkefølgen som linjene vurderes i. 

Lokasjonsdirektiver har et ekstra detaljnivå: *lokasjonsdirektivhandlinger*. Du kan definere flere lokasjonsdirektivhandlinger for hver linje. Et serienummer brukes igjen til å bestemme rekkefølgen som handlingene er vurdert i. På dette nivået kan du definere en spørring for å definere hvordan du finner den beste plasseringen i lageret. Du kan også bruke forhåndsdefinerte innstillinger for **Strategi** for å finne en optimal lokasjon.

## <a name="location-directives-configuration-details"></a>Konfigurasjonsdetaljer for lokasjonsdirektiver 

 ### <a name="sequence-number"></a>Serienummer
 
Dette tallet indikerer rekkefølgen for behandling av et lokasjonsdirektiv for en valgt ordretype. Det kan endres ved hjelp av **Flytt opp** og **Flytt ned** på menyen.
 
 ### <a name="work-type"></a>Arbeidstype
 
Dette er typen arbeid som skal utføres. Typen arbeid som er tilgjengelig, er basert på typen lagertransaksjon som du har valgt i **Arbeidsordretype**-feltet.
-   **Plasser** - En arbeidstype lik **Plasser** betyr at lokasjonsdirektivet skal finne den mest ideelle lokasjonen å plasere beholdning som kommer inn i systemet, enten fra mottak, produksjon, eller lagerjusteringer. Det kan også brukes til å definere en plassering på en stadielokasjon eller en endelig plassering på en forsendelseslokasjon.
-   **Plukk** - En arbeidstype lik **Plukk** betyr at lageret skal finne den mest ideelle lokasjonen å fysisk reservere beholdning fra (opprette arbeid). Plukkingen kan fullføres (plukklinjen kan lukkes), selv om arbeidet ikke er fullført. Brukeren kan gjøre ferdig fysisk plukking, som er et plukketrinn. Brukeren kan deretter avbryte fra en mobilenhet og fullføre arbeidet senere. Arbeidshodet lukkes imidlertid når den endelige plasseringen er fullført. 
-   **Telling, Justeringer, Tilpasset, Endring av beholdningsstatus, Nummerskiltbygging, utskrift, Statusendring, Pakk til nestede nummerskilt** - Disse kan ikke brukes i oppsettet av lokasjonsdirektivet. Dette er en opplisting, så det er ingen filtrering knyttet til arbeidsordretypen. 

### <a name="directive-code"></a>Direktivkode

Velg direktivkoden som skal knyttes til en arbeidsmal eller etterfyllingsmal. I skjemaet **Direktivkode** kan du opprette nye koder som kan brukes for tilkoblinger mellom en arbeidsmal, en etterfyllingsmal og et lokasjonsdirektiv. Dette kan også brukes til å opprette koblingen mellom en hvilken som helst linje i en arbeidsmal og lokasjonsdirektivet (for eksempel en rampedør eller en stadieplassering).

Legg merke til at hvis koden er angitt, når arbeidet genereres, systemet søker ikke lokasjonsdirektivet etter sekvens, søket blir etter direktivkode. Dette betyr at du kan være mer spesifikk om hvilken lokasjonsmal som skal brukes for et bestemt trinn i en arbeidsmal, for eksempel oppsamling av materialer. 

### <a name="site"></a>Nettsted

Område er et obligatorisk felt fordi lokasjonsdirektivet krever området og lageret som det er gyldig for. 

### <a name="warehouse"></a>Lager

Lager er et obligatorisk felt fordi lokasjonsdirektivet krever området og lageret som det er gyldig for.

### <a name="multiple-sku"></a>Flere SKUer

Dette tillater flere lagerenheter (SKU) på en lokasjon, for eksempel rampedøren. Hvis du velger **Flere SKU-er**, blir plasseringslokasjonen angitt i arbeidet (som er forventet), men den vil bare kunne håndtere flere vareplasseringer (hvis arbeidet inneholder ulike SKU-er som skal plukkes og plasseres, ikke én enkelt SKU-plassering). Hvis du ikke velger **Flere SKU-er**, blir plasseringslokasjonen bare angitt hvis plasseringen har bare én type SKU. Hvis du vil bruke begge handlingene, må du angi to linjer, én med Flere SKU-er aktivert, og én med Flere SKU-er deaktivert. Disse må ha samme struktur og oppsett. For plasseringsoperasjoner må du ha lokasjonsdirektiver som er identiske, selv om du ikke skiller mellom én eller flere SKU-er i arbeids-ID-en. Du må også definere for plukking, hvis du har en ordre med mer enn én vare.

### <a name="sequence-number"></a>Serienummer

Angi rekkefølgen for behandling av lokasjonsdirektivlinjene for den valgte arbeidstypen. Du kan også endre rekkefølgen, om nødvendig, ved hjelp av **Flytt opp** og **Flytt ned**.

### <a name="fromto-quantity"></a>Fra/Til antall

Dette gir mulighet til å angi et antallsområde for når sekvensen i midten av rutenettet skal velges. Du kan angi Fra/Til område under Antall i den aktuelle enheten.

### <a name="unit"></a>Enhet

Du kan angi et minimums- og maksimumsantall som direktivet skal gjelde for, og du kan angi at direktivet skal være for en bestemt lagerenhet. Enhetsfeltet på linjen brukes bare for evaluering av antall.

Ved kontroll av om linjen i lokasjonsdirektivet gjelder, blir dette basert på antallet i den respektive enheten som er angitt på linjen i lokasjonsdirektivet. Hver gang en lokasjonsdirektivlinje nås, prøver systemet å konvertere behovsenheten til en enhet som er angitt på linjen. Hvis måleenhetkonverteringen ikke finnes, vil programmet fortsette til neste linje. 

### <a name="locate-quantity"></a>Plasser antall

Dette alternativet brukes bare til å plassere/finne antall på lageret. Det er bare for arbeidstypen plassering. Dette er de gyldige verdiene:

-   **Nummerskiltantall** - Når du vurderer om antallet er innenfor antallsområdene i "Fra" og "Til", kan du bruke antallet på nummerskiltet som mottas.
-   **Antall delt opp i enheter** - Når du vurderer om antallet er innenfor antallsområdene i "Fra" og "Til", kan du bruke antallet delt opp i enheter under den spesifikke transaksjonen.
-   **Restantall** - Når du vurderer om antallet er innenfor antallsområdene i "Fra" og "Til, kan du bruke restantallet som skal mottas på bestillingslinjen som sjekkes inn.
-   **Forventet antall** - Når du vurderer om antallet er innenfor antallsområdene i "Fra" og "Til, kan du bruke det totale tallet på bestillingslinjen, uavhengig av hva som allerede er mottatt.

### <a name="restrict-by-unit"></a>Begrens etter enhet

Dette gjør at en lokasjonsdirektivlinje kan bli gjort spesifikk for en måleenhet eller flere måleenheter. Når du reserverer antallet, hvis du vil reservere paller fra et bestemt sett med lokasjoner, vil sekvensen i midten av rutenett begrense denne bestemte sekvensen til "PL", slik at eventuelt antall som er mindre enn én pall, ikke vil velge rekkefølgen. Velg **Begrens etter enhet** for å definere enhetene. Du kan også begrense linjen til flere enn én enhet. Dette fungerer bare med lokasjonsdirektiver av plukktypen. 

### <a name="round-up-to-unit"></a>Avrund oppover til enhet

Dette feltet fungerer sammen med feltet **Begrens etter enhet**. Hvis lopkasjonsdirektivlinjen **Begrens etter enhet** er satt til "boks", vil valg av **Avrund oppover til enhet** angi at arbeidet som er generert av direktivet for plukking for råvarer, skal avrundes opp til et multiplum av én håndteringsenhet (angitt i **Begrens etter enhet**). Merk at dette fungerer bare for råvareplukking og bare med lokasjonsdirektiver av typen plukk.

### <a name="locate-packing-qty"></a>Plasser pakkeantall

Hvis et pakkeantall er angitt i en salgsordre, overføringsordre eller produksjonsordre, begrenser dette systemet til bare å velge lokasjoner med et pakkeantall på lokasjonen. Dette fungerer bare med lokasjonsdirektiver av plukktypen.

### <a name="allow-split"></a>Tillat deling

Dette angir om et lokasjonsdirektiv har tillatelse til å dele antallet som mottas eller antallet som reserveres, på tvers av flere lagerlokasjoner, eller om hele antallet må være plassert på én enkelt lokasjon eller reservert fra én lokasjon for å kunne opprette arbeid. 

### <a name="sequence-number"></a>Serienummer

Dette tallet er rekkefølgen for behandling av lokasjonsdirektivet for den valgte arbeidstypen. Du kan endre rekkefølgen om nødvendig. Vær forsiktig med å bruke unike rekkefølgenumre, siden behandlingen alltid kjører i rekkefølge. 

### <a name="name"></a>Navn

Angi et navn på lokasjonsdirektivhandlingen. Vær nøyaktig når du angir et navn.

### <a name="fixed-location-usage"></a>Bruk av fast lokasjon 

-   **Faste og ikke-faste lokasjoner** - Lokasjonsdirektivet tar alle lokasjoner i betraktning.
-   **Bare faste lokasjoner for produktet** - Lokasjonsdirektivet tar bare faste lokasjoner for produkter i betraktning.
-   **Bare faste lokasjoner for produktvarianten** - Lokasjonsdirektivet tar bare faste lokasjoner for produktvarianter i betraktning.

### <a name="allow-negative-inventory"></a>Tillat negativ beholdning

Velg dette for å tillate negativ beholdning på den angitte lagerlokasjonen i lokasjonsdirektiver. 

### <a name="batch-enabled"></a>Parti aktivert 

Velg dette for å bruke partistrategier for varene som er partiaktivert. Hvis en linje nås der **Parti aktivert** er angitt med en ikke-partivare, fortesetter prosessen til neste handlingslinje. 

### <a name="strategy"></a>Strategi

-   **Konsolider** - Denne strategien brukes til å konsolidere varer på en bestemt lokasjon når det allerede finnes like varer. Dette fungerer bare med lokasjonsdirektiver av plasseringstypen. Vanlige oppsett for plassering skal konsolideres på den første handlingslinjen, og på den andre skal det forsøkes å plassere uten konsolidering. Konsolidering av varer gjør senere plukking mer effektivt.
-   **Samsvar pakkeantall** - Denne strategien brukes til å kontrollere om en plukklokasjon har det angitte pakkeantallet. Dette fungerer bare for lokasjonsdirektiver av plukktypen. 
-   **FEFO-partireservering** - Denne strategien brukes når beholdningen plasseres ved hjelp av en utløpsdato for parti og tilordnes partireserveringen. Du kan bare bruke denne strategien for partiaktiverte varer. Dette fungerer bare for lokasjonsdirektiver av plukktypen. 
-   **Avrund oppover til fullstendig nummerskilt** - Denne strategien brukes til å avrunde lagerantallet oppover for å tilsvare nummerskiltantallet som er tilordnet varene som skal plukkes. Du kan bare bruke denne strategien for etterfyllingstypen av lokasjonsdirektiver av typen plukk. 
-   **Tom plassering med innkommende arbeid** - Denne strategien brukes til å finne tomme lokasjoner. Lokasjonen anses som tom hvis den ikke har fysisk beholdning og ikke forventet innkommende arbeid. Denne strategien brukes bare for et lokasjonsdirektiv av plasseringstypen. 

### <a name="example-of-the-use-of-location-directives"></a>Eksempel på bruk av lokasjonsdirektiver

I dette eksemplet vurderes det en bestillingsprosess der lokasjonsdirektivet må finne ledig kapasitet i et lager for lagervarer som nettopp er registrert i mottakssonen. Først må du prøve å finne ledig kapasitet i lageret ved å konsolidere med eksisterende lagerbeholdning. Hvis konsolidering ikke er mulig, må du finne en ledig lokasjon. 

I dette scenariet må du definere to lokasjonsdirektivhandlinger. Den første handlingen i sekvensen må bruke strategien **Konsolider** og andre må bruke strategien **Tom lokasjon uten innkommende arbeid**. Med mindre du definerer en tredje handling for å håndtere et overflytscenario er to resultater mulig når det er ikke mer kapasitet i lageret: arbeid kan opprettes selv om ingen lokasjoner defineres, eller arbeidsopprettingsprosessen kan mislykkes. Resultatet bestemmes av oppsettet på siden **Feil med lokasjonsdirektiv** der du kan bestemme om du vil velge alternativet **Stopp arbeid ved feil med lokasjonsdirektiv** for hver arbeidsordretype.
