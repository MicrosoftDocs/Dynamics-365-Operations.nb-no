---
title: Generere en statistisk grunnlinje prognose
description: Denne artikkelen inneholder informasjon om parametere og filtre som brukes i beregningen av behovsprognose.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Generere en statistisk grunnlinje prognose

Denne artikkelen inneholder informasjon om parametere og filtre som brukes i beregningen av behovsprognose. 

Når du oppretter en basislinjeprognose, må du først angi parameterne og filtrene som brukes i beregningen. Du kan for eksempel opprette en basislinjeprognose som beregner behov basert på transaksjonsdata fra det siste året for et bestemt firma, for kommende måned, og for en utvalgt gruppe varer. 

Hvis du vil generere en behovsprognose, kan du gå til **Master planning &gt;prognose &gt;prognoser for behov &gt;Generer statistisk grunnlinje prognose**. 

Prognoseperioden kan velges på tidspunktet for generering av prognosen. Tilgjengelige verdier er: dag, uke og måned. 

Antall perioder å generere en prognose for settes i feltet** Prognosehorisont**. 

Når prognosestrategien er satt til **Kopier over historisk behov**, ignoreres slutten av den historiske horisonten. Kopieres antallet bøtter som er angitt i den **prognose horisonten** feltet til prognosekrav fra datoen som er angitt den **fra datoen** felt under **historiske horisonten**. Når du kopierer historisk behov fra en bestemt dato fremover, kan produksjonsplanleggere gjøre planen for neste kvartal på to måter:

-   Ved å kopiere behov fra samme kvartal i fjor.
-   Ved å kopiere behov fra forrige kvartal.

For å unngå forvirring i produksjonsplanene, kan et bestemt antall prognoseperioder låses. Dette nummeret angis **Låsningshorisont** feltet. På siden **Justert behovsprognose **er cellene for låste perioder deaktivert, for å gi en visuell indikasjon på at disse verdiene ikke skal endres. 

Startdatoen for behovsprognose for basislinje behøver ikke være gjeldende dato eller en dato i fremtiden. Hvis du vil angi en annen startdato, kan du bruke feltet **Startdato for basislinjeprognose - Fra-dato**. I juni, kan brukerne for eksempel generere en prognose for neste år. Fordi prognoseperioder mellom slutten av historiske behov og starten på basislinjen mangler, er det ikke sikkert at forutsigelser blir nøyaktige. Hvis du bruker Microsoft Dynamics 365 for operasjoner etterspørselen prognoser for tjenesten, er det fire måter du kan fylle kunnskapshullene mangler. Du kan velge metoden du vil bruke, ved å angi manglende\_verdien\_erstatning parameter i den **etterspørselen prognoser parametere** siden. 

Den **prognose, planlagte startdatoen** - **fra datoen** har feltet settes til begynnelsen av en prognose filsamling, for eksempel i USA, en søndag Hvis forecasting bucket er uken. Systemet justerer automatisk den **prognose, planlagte startdatoen** - **fra datoen** -feltet til samsvar for starten for en prognose filsamling. 

Den **prognose, planlagte startdatoen** - **fra datoen** feltet kan settes til en dato i fortiden. Det er altså mulig å generere en behovsprognose i fortid. Dette er nyttig fordi du kan la brukere endre de prognose serviceparametere slik at den statistisk prognosen generert tidligere samsvarer med det faktiske historiske behovet. Brukere kan deretter fortsette å bruke disse parameterinnstillingene til å generere en statistisk basislinjeprognose for fremtiden. 

Manuelle justeringer i tidligere behovsprognose gjentakelser kan brukes automatisk på den nye basislinjeprognosen hvis den boksen **Overfør manuelle justeringer til behovsprognosen** er merket. Hvis merket er fjernet, legges ikke de manuelle justeringene til i basislinje prognosen, men de slettes ikke. Manuelle justeringer i en prognose kan slettes bare ved prognose importen, ved å deaktivere den boksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen**. Manuelle justeringer lagres på tidspunktet for godkjenning. Derfor, hvis en bruker gjør manuelle justeringer i prognosen, men ikke godkjenne prognosen tilbake til Dynamics 365 for operasjoner, endringene går tapt. Hvis du vil ha mer informasjon om manuelle justeringer og hvordan de fungerer, kan du se [godkjenning justerte prognosen](authorize-adjusted-forecast.md). 

En behovsprognosegenerering kan ha et navn og merknader som hjelper brukere med å identifisere prognosen som genereres. Disse verdiene vises i prognosens genereringshistorikk på siden **Genereringshistorikk for statistisk basislinjeprognose**. 

Konsernintern planleggingsgruppe, varefordelingsnøkler og andre filtre kan brukes på tidspunktet for generering av prognosen. Disse kan brukes til å forbedre ytelsen eller til å dele dataene i håndterbare deler. Vær imidlertid oppmerksom på at ikke genereres en behovsprognose for medlemmene i en varefordelingsnøkkel som ikke er knyttet til en konsernintern planleggingsgruppe, selv om varefordelingsnøkkelen er valgt i spørringen. 

**Tips!**: Brukere kan noen ganger motta feilmeldinger når de genererer en behovsprognose eller prognosegenerering fullføres uten øktlogg. Dette kan skje på grunn av overflødige data i spørringen som tidligere ble brukt for generering av prognose. For å løse dette problemet klikk **Velg** for å åpne siden **Spørring**, klikk **Tilbakestill**, og generer deretter den basislinjeprognosen på nytt. 

Hvis prognosen ikke er generert for et stort antall elementer, men for eksempel for én vare eller en varetildelingsnøkkel samtidig, og deretter for å få bedre ytelse, kan du velge den **bruker forespørsel-svarmodus** merket i den **Master planlegging - Setup - etterspørselen prognoser** - **etterspørselen prognoser parametere - Azure maskin læring** kategorien.

<a name="see-also"></a>Se også
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


