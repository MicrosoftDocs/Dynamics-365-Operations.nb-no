---
title: Direkteoverføring fra produksjonsordrer til utleveringsporter
description: Dette emnet beskriver hvordan du styrer prosessen for direkteoverføring av materiale som er rapportert ferdig, fra en produksjonslinje til en utleveringsport.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockOpportunityPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8691bb6702028070810a1503add33985de5ede3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "329028"
---
# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Direkteoverføring fra produksjonsordrer til utleveringsporter

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du styrer prosessen for direkteoverføring av materiale som er rapportert ferdig, fra en produksjonslinje til en utleveringsport.

<a name="introduction"></a>Introduksjon
------------

Direkteoverføring fra produksjon til en utgående lokasjon er relevant for produsenter som produserer stort volum, og ideelt sett vil sende de ferdige produktene så snart de er rapportert som ferdige fra produksjonslinjene. Hensikten er å levere produkter til distribusjonssentre som er fysisk plassert nær kundeetterspørselen, i stedet for å bygge opp lager på området for produksjon.

Hvis det ikke er umiddelbar etterspørsel etter et produkt, må det plasseres i lagerlokasjoner på produksjonsstedet. Denne prosessen kalles også *opportunistisk direkteoverføring*, noe som innebærer at det, hvis det er behov for levering av produktet, skal denne muligheten brukes i stedet for å sette produktet til intern lagring.

Eksemplet nedenfor viser tre varianter av en flyt som starter på slutten av produksjonslinjen (2).

Et produkt som er rapportert som fullført til produksjonsutleveringsstedet (3), og en truckfører vil hente pallen på dette stedet (3).

-   Hvis det er planlagt en aktivitet (6) for overføring produktet fra produksjon (1) til et distribusjonssenter (7), vil deretter truckføreren bli henvist av systemet til å sette pallen ved en rampedør (4).
-   Hvis en lastebil er allerede tilordnet rampedøren, blir truckføreren bedt om å laste produktet rett på lastebilen.
-   Hvis det ikke er noen planlagt aktiviteten for overføring av produktet, blir truckføreren bedt om å plassere produktet et sted på det interne lageret (5).

[![Opportunistisk direkteoverføring](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Konfigurere direkteoverføring
Du konfigurerer prosessen direkteoverføring i **arbeidspolicyer**. En arbeidspolicy inneholder en arbeidsordretype, sted og produkt. I eksemplet nedenfor er direkteoverføring konfigurert for produkt X og lokasjon Y.

#### <a name="work-order-types"></a>Arbeidsordretyper

-   Arbeidsordretype: Plasser ferdigvarer
-   Arbeidsopprettelsesmetode: direkteoverføring
-   Navn på direkteoverføringspolicy: Overføringsordrer

#### <a name="inventory-locations"></a>Lagerlokasjoner

-   Lager: 51
-   Sted: Y

#### <a name="products"></a>Produkter

-   Varenummer: X

For øyeblikket kan direkteoverføring bare konfigureres for to arbeidsordretyper:

-   Plasser ferdigvarer
-   Plasser koprodukt og biprodukt

I **direkteoverføringspolicyen** angir du hvilke dokumenttyper som skal brukes for direkteoverføring. For tiden er **Overføringsordrer** den eneste dokumenttypen som støttes. Følgende eksempel viser konfigurasjonen av en policy for direkteoverføring.

### <a name="cross-docking-policy-name-transfer-order"></a>Navn på direkteoverføringspolicy: Overføringsordre

- Sekvensnummer: 10
  -   Arveidsordretype: Utstedelse for overføring
- Direkteoverføringsbehov krever en lokasjon: Usann
- Strategi for direkteoverførind: dato og klokkeslett

### <a name="sequence-number"></a>Serienummer

**Serienummer** angir prioriteten til dokumenttypen. Fortiden er **Utstedelse for overføring** den eneste typen som støttes. Serienummeret vil derfor først bli relevant når flere ordretyper støttes.

### <a name="cross-docking-policy"></a>Direkteoverføringspolicy

Direkteoverføringspolicyen angir også policyen for prioriteringen av etterspørselen etter overføringsordrer. Hvis det for eksempel finnes flere overføringsordrer for samme produkt, angis planlagt dato og klokkeslett på lasten, og sammen med overføringsordren argjør dette prioriteringen mellom ordrene. Planlagt dato og klokkeslett kan angis direkte på lasten, eller de kan angis i en **avtalesplan** som er tilknyttet lasten. Prioriteringen bestemmes av direkteoverføringsstrategien. Det er for øyeblikket bare én strategi: **dato og klokkeslett**.

### <a name="cross-docking-demand-requires-location"></a>Direkteoverføringsbehov krever en lokasjon

I direkteoverføringspolicyen, kan du angi kriterier som krever at overføringsordrer har en tilordnet lokasjon for å kvalifisere til direkteoverføring. Dette kriteriet er satt opp i feltet **Direkteoverføringsbehov krever en lokasjon**. Lokasjonen på avtaleplanen som er tilknyttet lasten, blir brukt som den endelige plasseringen for varene som blir direkteoverført. Den endelige plasseringen for varene som blir direkteoverført bestemmes av lokasjonsdirektivet for **Utstedelse for overføring** for arbeidsordretypen **Plasser**. De kan være nyttig å aktivere feltet **Direkteoverføringsbehov krever en lokasjon** i et scenario der de ferdige varene skal direkteoverføres bare hvis en lastebil er tilordnet til en rampedør. I så fall flyttes varene til lastebilen direkte fra produksjonslinjen. Når en lastebil er tilordnet rampedøren, vil en bruker tilordne plasseringen til avtaleplanen og vil derfor gjøre lokasjonen gyldig for direkteoverføring. Delene nedenfor forklarer to eksempler.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Scenario 1 – Direkteoverføring fra produksjon til overføringsordrer

Når et produkt rapportert som fullført på produksjonslinjen, overføres det til en rampedørlokasjon der det lastes inn i en lastebil og overføres til et distribusjonssenter. Bruk selskapet USMF.

1.  Aktiver en ny nummersekvens for direkteoverføring. Gå til  **nummerserier**-siden, og velg **Generer**. En veiviser fører deg gjennom prosessen.
2.  Opprett en direkteoverføringspolicy. Gå til  **direkteoverføringspolicy**-siden, og opprett en ny policy med navnet **Direkteoverføring til overføringsordre**. Legg merke til at den enste arbeidsordretypen du kan velge **Utstedelse for overføring**, og den eneste direkteoverføringsstrategien som er tilgjengelig, er **dato og klokkeslett**.
3.  Opprett en arbeidspolicy. Gå til **arbeidspolicyer**-siden, og opprett en ny policy for arbeid som heter **Direkteoverføring L0101**.
4.  Definer laster slik at de opprettes automatisk for overføringsordrer. I lagerparameterne definerer du laster slik at de opprettes automatisk når det opprettes overføringsordrer. En last er en forutsetning for å kvalifisere overføringsordren for direkteoverføring.
5.  Definer tilordning av varelast. Gå til **Tilordning av varelast**-siden, og angi en standard lastmal for **CarAudio**-varegruppen. Denne tilordningen setter automatisk inn lastmalen på lasten når overføringsordren opprettes.
6.  Opprett en overføringsordre. Opprett overføringsordren for varenummer L0101. Antall = 20.
7.  Frigi overføringsordren fra arbeidsområdet for lastplanlegging. I **Send**-kategorien velger du menyelementet Arbeidsområde for lastplanlegging, og i **Frigi**-menyen på lastlinjen, velger du **Frigi til lager**. Det finnes nå en åpen bølgelinje av typen **Utstedelse for overføring** for overføringsordren.
8.  Opprett en produksjonsordre. Gå til **produksjonsordre**-listesiden, og opprett en produksjonsordre for produkt L0101. Antall = 20. Estimer og start produksjonsordren. Legg merke til at feltet **Poster plukkliste nå** er satt til **Nei**.
9.  Ferdigmeld fra den mobile enheten. Gå til mobilenhetsportalen, og velg menyelementet **Ferdigmeld og plasser**. Ferdigmeld L0101 fra den fra den håndholdte enheten. Antall = 10. Legg merke til at plasseringslokasjonen er **RAMPEDØR**. Denne lokasjonen finner du fra lokasjonsdirektivet  **Utstedelse for overføring** for arbeidsordretypen **Plasser**. Legg også merke til at arbeid av typen **Utstedelse for overføring** er opprettet og fullført. Gå til overføringsordrens arbeidsdetaljer for å kontrollere arbeidet.
10. Nå kan du rapportere ytterligere 10 stykker fra den mobile enheten. Legg merke til at plasseringslokasjonen igjen er **RAMPEDØR**. Legg også merke til at nytt arbeid av typen **Utstedelse for overføring** er opprettet for 10 deler.
11. Nå kan du prøve å starte 20 stykker mer på produksjonsordren, og deretter prøve å ferdigmelde 20 stk. ved hjelp av den håndholdte enheten. Denne ganf forselås lokasjonen **LP-001** som plasseringslokasjon. Denne lokasjonen finner du fra lokasjonsdirektivet for **Plasser ferdigvarer**. Dette lokasjonsdirektivet brukes fordi det ikke finnes noen mulighet for direkteoverføring. Overføringsordren for LP-001 ble fullstendig oppfylt av de to aktivitetene for direkteoverføring i trinn 9 og 10. Legg merke til at arbeid av typen **Plasser ferdigvarer** ble opprettet og behandlet.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Scenario 2 - Direkteoverføring fra produksjon til overføringsordrer med en avtaleplan

Når et produkt som er rapportert som fullført på produksjonslinjen overføres en rampedørlokasjon som er identifisert av en avtaleplan for rampedørlokasjonene. Bruk selskapet USMF.

1.  Endre direkteoverføringspolicyen. Endre direkteoverføringspolicyen du opprettet i scenario 1 ved å velge **Direkteoverføringsbehov krever en lokasjon**-merket.
2.  Opprett en ny overføringsordre.
3.  Åpne **Arbeidsområde for lastplanlegging**.
4.  Fra Arbeidsområde for lastplanlegging går du til **laster**-delen, og velger **avtalesplan** på **transport**-menyen for å opprette en ny avtaleplan. Legg merke til at avtaleplanen har en referanse til overføringsordren i **ordrenummer**-feltet. I **Planlagt startdato/-klokkeslett på lokasjon**-feltet kan du angi datoen og klokkeslettet for avtalen. Dato og klokkeslett vil bli brukt når direkteoverføringsbehov prioriteres i løpet av prosessen for direkteoverføring. Datoen og tidspunktet du angir i dette feltet, oppdateres av **Dato og klokkeslett for planlagt lastforsendelse**-feltet på den tilsvarende lasten. Plasseringen på hurtigfanen **leveringsdetaljer** bestemmer lokasjonen overføringsordren sendes fra.
5.  Frigi til lageret fra **Arbeidsområde for lastplanlegging**.
6.  Opprett en produksjonsordre for varenummer **L0101**, og sett statusen til **startet**, med et antall på 20.
7.  Ferdigmeld fra den mobile enheten.
8.  Gå til mobilenhetsportalen, og velg menyelementet **Ferdigmeld og plasser**.
9.  Ferdigmeld varenummer **L0101** fra den fra den håndholdte enheten. Legg merke til at plasseringslokasjonen nå er **BAYDOOR 2**. Denne lokasjonen blir funnet fra avtaleplanen i stedet for lokasjonsdirektivet **overføringsmottak**.

### <a name="additional-information"></a>Tilleggsinformasjon

-   Direkteoverføringsscenariet støttes for parti- og seriekontrollerte varer, både med parti- og serienummerdimensjonene som er definert over, og under lokasjon i reservasjonshierarkiet. 


