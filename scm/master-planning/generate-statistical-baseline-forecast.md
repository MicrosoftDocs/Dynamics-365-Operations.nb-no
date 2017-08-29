---
title: Generer en statistisk basislinjeprognose
description: Denne artikkelen inneholder informasjon om parametere og filtre som brukes i beregningen av behovsprognose.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 93646e37ee511d433097bb284fccc73c230aee32
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>Generer en statistisk basislinjeprognose

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om parametere og filtre som brukes i beregningen av behovsprognose. 

Når du oppretter en basislinjeprognose, må du først angi parameterne og filtrene som brukes i beregningen. Du kan for eksempel opprette en basislinjeprognose som beregner behov basert på transaksjonsdata fra det siste året for et bestemt firma, for kommende måned, og for en utvalgt gruppe varer. 

For å generere en behovsprognose går du til **Hovedplanlegging &gt; Prognose &gt; Behovsprognose &gt; Generer statistisk basislinjeprognose**. 

Prognoseperioden kan velges på tidspunktet for generering av prognosen. Tilgjengelige verdier er: dag, uke og måned. 

Antall perioder å generere en prognose for settes i feltet **Prognosehorisont**. 

Når prognosestrategien er satt til **Kopier over historisk behov**, ignoreres slutten av den historiske horisonten. Systemet kopierer antall perioder som er angitt i feltet **Prognosehorisont** for å prognostisere behov, fra og med datoen som er angitt **Fra-dato** feltet under **Historisk horisont**. Når du kopierer historisk behov fra en bestemt dato fremover, kan produksjonsplanleggere gjøre planen for neste kvartal på to måter:

-   Ved å kopiere behov fra samme kvartal i fjor.
-   Ved å kopiere behov fra forrige kvartal.

For å unngå forvirring i produksjonsplanene, kan et bestemt antall prognoseperioder låses. Dette nummeret angis **Låsningshorisont** feltet. På siden **Justert behovsprognose** er cellene for låste perioder deaktivert, for å gi en visuell indikasjon på at disse verdiene ikke skal endres. 

Startdatoen for behovsprognose for basislinje behøver ikke være gjeldende dato eller en dato i fremtiden. Hvis du vil angi en annen startdato, kan du bruke feltet **Startdato for basislinjeprognose - Fra-dato**. I juni, kan brukerne for eksempel generere en prognose for neste år. Fordi prognoseperioder mellom slutten av historiske behov og starten på basislinjen mangler, er det ikke sikkert at forutsigelser blir nøyaktige. Hvis du bruker behovsprognosetjenesten for Microsoft Dynamics 365 for Finance and Operations, er det fire måter som du kan fylle ut manglene på. Du kan velge metoden du vil ha ved å angi parameteren MISSING\_VALUE\_SUBSTITUTION på siden **Parametere for behovsprognose**. 

Feltet **Startdato for basislinjeprognose** - **Fra-dato** må være satt til begynnelsen av en prognoseperioden, for eksempel i USA en søndag, hvis prognoseperioden er uken. Systemet justerer automatisk feltet **Startdato for basislinjeprognose** - **Fra-dato** slik at det samsvarer med begynnelsen av en prognoseperiode. 

Feltet **Startdato for basislinjeprognose** - **Fra-dato** kan settes til en dato i fortiden. Det er altså mulig å generere en behovsprognose i fortid. Dette er nyttig fordi du kan la brukere endre de prognose serviceparametere slik at den statistisk prognosen generert tidligere samsvarer med det faktiske historiske behovet. Brukere kan deretter fortsette å bruke disse parameterinnstillingene til å generere en statistisk basislinjeprognose for fremtiden. 

Manuelle justeringer i tidligere behovsprognose gjentakelser kan brukes automatisk på den nye basislinjeprognosen hvis den boksen **Overfør manuelle justeringer til behovsprognosen** er merket. Hvis merket er fjernet, legges ikke de manuelle justeringene til i basislinje prognosen, men de slettes ikke. Manuelle justeringer i en prognose kan slettes bare ved prognose importen, ved å deaktivere den boksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen**. Manuelle justeringer lagres på tidspunktet for godkjenning. Hvis en bruker gjør manuelle justeringer i prognosen, men ikke godkjenner prognosen tilbake til Dynamics 365 for Finance and Operations, går derfor endringene tapt. Hvis du vil ha mer informasjon om manuelle justeringer og hvordan de fungerer, kan du se [Godkjenne den justerte prognosen](authorize-adjusted-forecast.md). 

En behovsprognosegenerering kan ha et navn og merknader som hjelper brukere med å identifisere prognosen som genereres. Disse verdiene vises i prognosens genereringshistorikk på siden **Genereringshistorikk for statistisk basislinjeprognose**. 

Konsernintern planleggingsgruppe, varefordelingsnøkler og andre filtre kan brukes på tidspunktet for generering av prognosen. Disse kan brukes til å forbedre ytelsen eller til å dele dataene i håndterbare deler. Vær imidlertid oppmerksom på at ikke genereres en behovsprognose for medlemmene i en varefordelingsnøkkel som ikke er knyttet til en konsernintern planleggingsgruppe, selv om varefordelingsnøkkelen er valgt i spørringen. 

**Tips!**: Brukere kan noen ganger motta feilmeldinger når de genererer en behovsprognose eller prognosegenerering fullføres uten øktlogg. Dette kan skje på grunn av overflødige data i spørringen som tidligere ble brukt for generering av prognose. For å løse dette problemet klikk **Velg** for å åpne siden **Spørring**, klikk **Tilbakestill**, og generer deretter den basislinjeprognosen på nytt. 

Hvis prognosen ikke genereres for et stort sett av varer, men, for eksempel for én vare eller en varefordelingsnøkkel om gangen, kan du deretter for å få bedre ytelse merke av for **Bruk modus for forespørselssvar** i kategorien **Hovedplanlegging - Oppsett - Behovsprognose** - **Parametere for behovsprognose - Azure Machine Learning**.

<a name="see-also"></a>Se også
--------

[Oppsett av behovsprognose](demand-forecasting-setup.md)

[Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)

[Godkjenne den justerte prognosen](authorize-adjusted-forecast.md)




