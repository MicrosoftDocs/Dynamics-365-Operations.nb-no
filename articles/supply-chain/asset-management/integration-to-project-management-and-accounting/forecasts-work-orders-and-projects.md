---
title: Prognoser, arbeidsordrer og prosjekter
description: Dette emnet beskriver prognoser og arbeidsordreintegrering med modulen Prosjektstyring og regnskap i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886822"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognoser, arbeidsordrer og prosjekter

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Aktivastyring gjøres integreringen til modulen **Prosjektstyring og regnskap** for å optimalisere kostnadskontroll, slik at brukere kan spore kostnader for prognoser ved vedlikeholdsjobbtype og arbeidsordrejobber.

To innstillinger må gjøres for å spore prognoser for vedlikeholdsjobbtype:

1. Velg et prosjekt i **Aktivastyring** > **Oppsett** > **Parametere for aktivastyring** > **Aktiva** kobling > **Prosjekt**-hurtigfanen> feltet **Vedlikeholdsprognoseprosjekt**.

2. Når du oppretter en standardlinje for vedlikeholdsjobbtype i **Standarder for vedlikeholdsjobbtype**, opprettes automatisk et aktivitetsnummer for linjen (**Aktivastyring** > **Oppsett** > **Jobber** > **Standarder for vedlikeholdsjobbtype**).

Prognoser for vedlikeholdsjobbtype har to formål: Du kan spore kostnader ved prognoser for vedlikeholdsjobbtype i modulen **Prosjektstyring og regnskap**. I tillegg overføres prognoser automatisk til et arbeidsordrejobbprosjekt når du velger en vedlikeholdsjobbtype i en arbeidsordrejobb.

Hvis du vil spore kostnader for arbeidsordrejobber, må du først definere arbeidsordreprosjekter. Se delen [Prosjektoppsett for arbeidsordre](../setup-for-work-orders/work-order-project-setup.md) hvis du vil ha en beskrivelse av fremgangsmåten.

## <a name="work-order-job-projects"></a>Arbeidsordrejobbprosjekter

Når du oppretter en arbeidsordrejobb i en arbeidsordre, bestemmes arbeidsordreprosjektet av oppsettet for det overordnede prosjektet for arbeidsordrer i **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**.

Arbeidsordrejobbprosjekter opprettes ved å bruke en kombinasjon av følgende arbeidsordreinformasjon:

- Arbeidsordretypen som er valgt i arbeidsordren 
- Den funksjonelle lokasjonen som er knyttet til aktivaet i arbeidsordrejobben
- Aktivatypen som er knyttet til aktivaet i arbeidsordrejobben  
- Det forventede start- og sluttidspunktet som er angitt for arbeidsordren  

Det er mulig at ikke all informasjonen som er nevnt ovenfor, blir funnet i en arbeidsordre. Derfor utføres søket etter et overordnede prosjekt for arbeidsordre ved å bruke den tilgjengelige kombinasjonen av data og velge prosjekt-IDen som tilsvarer arbeidsordredata.

Eksempel: I illustrasjonen nedenfor betyr oppsettet av anleggsmiddeltype "lastebilmotor" at alle arbeidsordrejobber som opprettes med denne anleggsmiddeltypen, blir et underprosjekt av prosjekt-ID "000186".

![Figur 1](media/01-integration-to-pma.png)

Formålet med prosjekt-IDen på arbeidsordrejobben og det relaterte aktivitetsnummeret (**Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** > velg arbeidsordre i liste > **Linjedetaljer** -hurtigfanen **Prosjekt-ID**-feltet og **Aktivitetsnummer**-feltet), er å spore kostnader knyttet til arbeidsordrejobben, og aktivumet som er valgt på arbeidsordrejobben, i modulen **Prosjektstyring og regnskap**. 

I figuren nedenfor vises en grafisk oversikt over arbeidsordreprosjekter og relaterte prosjektaktiviteter.

![Figur 2](media/02-integration-to-pma.png)

Når en ny arbeidsordrejobb blir opprettet i en arbeidsordre, opprettes det automatisk et arbeidsordreprosjekt for jobben. Finansdimensjonene for anleggsmiddelet som er relatert til arbeidsordrejobben, overføres automatisk til arbeidsordreprosjektet. Prosjektaktiviteten som er opprettet for en arbeidsordrejobb, har relatert informasjon som er knyttet til den for vedlikeholdsjobbtype, variant av vedlikeholdsjobbtype og handel. Disse dataene er nyttige hvis du for eksempel oppretter en bestilling fra en arbeidsordre (se [Innkjøp](../work-orders/procurement.md)), eller hvis du bruker modulen **Prosjektstyrings- og Regnskap** for tidsregistrering.  

Hvis anleggsmiddelet ble installert på et arbeidssted, og dette anleggsmiddelet senere installeres på et annet arbeidssted, oppdateres finansdimensjonene som er knyttet til det nye arbeidsstedet, automatisk i anleggsmiddelet. Når du deretter oppretter en arbeidsordrejobb for anleggsmiddelet, får arbeidsordreprosjektet for arbeidsordrejobben automatisk finansdimensjonene som nå er knyttet til anleggsmiddelet. Dette betyr at når du bruker arbeidssteder, kan kostnader alltid spores på arbeidssteder der et aktivum ble installert på et gitt tidspunkt. Den automatiske oppdateringen av finansdimensjoner sikrer fullstendig sporing av kostnader for prosjektkontroll og -rapportering.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Arbeidsordreprosjekter, livsløpstilstander for arbeidsordre, prosjektstadier og prosjekttyper

For å sikre riktig bruk av livsløpstilstander for arbeidsordre og tilknyttede prosjektstadier på arbeidsordrer, bør du vurdere avhengighetene i relasjon til modulen **Prosjektstyring og regnskap**:

- I modulen **Prosjektstyring og regnskap** er prosjektstadier definert for prosjekttyper i **Parametere for prosjektstyring og regnskap**.  
- I **Parametere for prosjektstyring og regnskap**må du huske å merke av i relevante avmerkingsbokser for prosjektstadiet for alle prosjekttypene du skal bruke. I figuren nedenfor er de fem stadiene **Opprettet** - **Estimert** - **Planlagt** - **Pågår** - **Fullført** valgt for prosjekttypene "tid og materialer" og "intern". Disse fem stadiene er relevante for både interne vedlikeholdsjobber og servicevedlikeholdsjobber.  
- I **Aktivastyring** defineres prosjekttyper av prosjektgruppene du definerer i skjemaet **Prosjektoppsett for arbeidsordre** > koblingen **Prosjektgruppe**.  
- Oppsettet av prosjektgrupper i **Prosjektoppsett for arbeidsordre** brukes når du oppretter arbeidsordrer. Når en ny arbeidsordre blir opprettet, opprettes det automatisk et arbeidsordreprosjekt for et arbeidsordren.  
- Hver livssyklus for arbeidsordre må ha et tilknyttet prosjektstadium.  
- Prosjektstadiet som er knyttet til en livsløpstilstand for arbeidsordre, må defineres som en aktiv fase for prosjektgruppen som er definert i arbeidsordreprosjektet. Arbeidsordreprosjektet opprettes automatisk i en arbeidsordre.  
- Når du oppretter en ny arbeidsordre, er den automatiske tilordningen av et arbeidsordreprosjekt basert på oppsettet i **Prosjektoppsett for arbeidsordre** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**).  

Tilknytninger mellom arbeidsordreprosjektgrupper, tilknyttede prosjekttyper, prosjektstadier og livssyklustilstander for arbeidsordre vises i figurene nedenfor.  

![Figur 3](media/03-integration-to-pma.png)

![Figur 4](media/04-integration-to-pma.png)

![Figur 5](media/05-integration-to-pma.png)

Se [Prosjektoppsett for arbeidsordre](../setup-for-work-orders/work-order-project-setup.md) for informasjon om hvordan du definerer arbeidsordreprosjekter, og [Livssyklustilstander for arbeidsordre](../setup-for-work-orders/work-order-lifecycle-states.md) for informasjon om hvordan du oppretter livssyklustilstander for arbeidsordre.

Figuren nedenfor viser en grafisk oversikt over ulike prosjektene som er opprettet i **Aktivastyring**-modulen, for å tillate integrering med modulen **Prosjektstyring og regnskap**, i tillegg til arbeidsprosessene som prosjektene er relatert til.

![Figur 6](media/06-integration-to-pma.png)

