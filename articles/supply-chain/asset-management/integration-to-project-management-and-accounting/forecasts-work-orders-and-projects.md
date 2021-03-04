---
title: Prognoser, arbeidsordrer og prosjekter
description: Dette emnet beskriver prognoser og arbeidsordreintegrering med modulen Prosjektstyring og regnskap i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9e6d20d1538ea68570d6dcc49da001ad76b8042b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434296"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognoser, arbeidsordrer og prosjekter

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring bidrar integreringen med modulen **Prosjektstyring og regnskap** til å optimalisere kostnadskontroll, slik at brukere kan spore kostnader for prognoser ved vedlikeholdsjobbtype og arbeidsordrejobber.

Sporing av prognoser for vedlikeholdsjobbtype krever to innstillinger:

1. Velg et prosjekt i **Aktivabehandling** > **Oppsett** > **Aktivabehandlingsparametere**, og deretter velger du et prosjekt i kategorien **Aktiva** > på hurtigfanen **Prosjekt** i feltet **Vedlikeholdsprognoseprosjekt**.

2. Når du oppretter en standardlinje for vedlikeholdsjobbtype, opprettes automatisk et aktivitetsnummer for linjen på siden **Standarder for vedlikeholdsjobbtype** (**Aktivastyring** > **Oppsett** > **Jobber** > **Standarder for vedlikeholdsjobbtype**).

Prognoser for vedlikeholdsjobbtype har to formål: 

- Du kan spore kostnader ved prognoser for vedlikeholdsjobbtype i modulen **Prosjektstyring og regnskap**. 
- Prognoser overføres automatisk til et arbeidsordrejobbprosjekt når du velger en vedlikeholdsjobbtype i en arbeidsordrejobb.

Hvis du vil spore kostnader for arbeidsordrejobber, må du først definere arbeidsordreprosjekter. Hvis du vil ha mer informasjon, kan du se [Prosjektoppsett for arbeidsordre](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Arbeidsordrejobbprosjekter

Når du oppretter en arbeidsordrejobb i en arbeidsordre, bestemmes arbeidsordreprosjektet av oppsettet for det overordnede prosjektet for arbeidsordrer på siden **Prosjektoppsett for arbeidsordre** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**).

Arbeidsordrejobbprosjekter opprettes ved å bruke en kombinasjon av følgende arbeidsordreinformasjon:

- Arbeidsordretypen som er valgt i arbeidsordren 
- Den funksjonelle lokasjonen som er knyttet til aktivaet i arbeidsordrejobben
- Aktivatypen som er knyttet til aktivumet i arbeidsordrejobben  
- De forventede start- og sluttidspunktene som er angitt for arbeidsordren  

Noe av denne informasjonen finnes kanskje ikke i en arbeidsordre. Derfor utføres søket etter et overordnede prosjekt for arbeidsordre ved å bruke den tilgjengelige kombinasjonen av data og velge prosjekt-IDen som tilsvarer arbeidsordredata.

I illustrasjonen nedenfor, på grunn av hvordan aktivatypen **Lastebilmotor** er konfigurert, vil for eksempel alle arbeidsordrejobber som opprettes med aktivatypen **Lastebilmotor**, være et underprosjekt med prosjekt-ID-000186.

![Figur 1](media/01-integration-to-pma.png)

Formålet med prosjekt-ID/en i arbeidsordrejobben og det relaterte aktivitetsnummeret, er å spore kostnader som er knyttet til arbeidsordrejobben, og aktivumet som er valgt for det, i modulen **Prosjektstyring og regnskap**. (Hvis du vil vise prosjekt-ID-en og aktivitetsnummeret, velger du **Aktivabehandling** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer**, og deretter velger du arbeidsordren. I hurtigfanen **Linjedetaljer** viser feltet **Prosjekt-ID** prosjekt-ID-en, og feltet **Aktivitetsnummer** viser aktivitetsnummeret.) Hvis du vil ha mer informasjon om kostnadskontroll i Aktivastyring, kan du se [Kostnads- og datokontroll](../controlling-and-reporting/cost-and-date-control.md).

Illustrasjonen nedenfor vises en grafisk oversikt over arbeidsordreprosjekter og relaterte prosjektaktiviteter.

![Figur 2](media/02-integration-to-pma.png)

Når en ny arbeidsordrejobb blir opprettet i en arbeidsordre, opprettes det automatisk et arbeidsordreprosjekt for jobben. Finansdimensjonene for anleggsmiddelet som er relatert til arbeidsordrejobben, overføres automatisk til arbeidsordreprosjektet.

Prosjektaktiviteten som opprettes for en arbeidsordrejobb, har relatert informasjon som er knyttet til den. Denne informasjonen gjelder for vedlikeholdsjobbtypen, variant av vedlikeholdsjobbtypen og handel. Dette er nyttig hvis du for eksempel oppretter en bestilling fra en arbeidsordre (se [Innkjøp](../work-orders/procurement.md)), eller hvis du bruker modulen **Prosjektstyrings- og Regnskap** for tidsregistrering.

Hvis anleggsmiddelet ble installert på et arbeidssted, men senere installeres på et annet arbeidssted, oppdateres finansdimensjonene som er knyttet til det nye arbeidsstedet, automatisk i anleggsmiddelet. Når du deretter oppretter en arbeidsordrejobb for anleggsmiddelet, får arbeidsordreprosjektet for arbeidsordrejobben automatisk finansdimensjonene som nå er knyttet til anleggsmiddelet. Når du bruker arbeidssteder, kan kostnader derfor alltid spores på arbeidssteder der et aktivum ble installert på et gitt tidspunkt. Den automatiske oppdateringen av finansdimensjoner bidrar til å sikre fullstendig sporing av kostnader for prosjektkontroll og -rapportering.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Arbeidsordreprosjekter, livsløpstilstander for arbeidsordre, prosjektstadier og prosjekttyper

For å bidra til å sikre riktig bruk av livsløpstilstander for arbeidsordre og tilknyttede prosjektstadier på arbeidsordrer, bør du vurdere avhengighetene i relasjon til modulen **Prosjektstyring og regnskap**:

- I modulen **Prosjektstyring og regnskap** er prosjektstadier definert for prosjekttyper på siden **Parametere for prosjektstyring og regnskap**.  
- På siden **Parametere for prosjektstyring og regnskap** må du huske å merke av i avmerkingsbokser for relevante prosjektfaser for alle prosjekttypene du vil bruke. I illustrasjonene nedenfor er de fem trinnene stadiene (**Opprettet**, **Estimert**, **Planlagt**, **Pågår** og **Fullført**) valgt for prosjekttypene **Tid og materialer** og **Intern**. Disse fem stadiene er relevante for både interne vedlikeholdsjobber og servicevedlikeholdsjobber.
- I modulen **Aktivastyring** defineres prosjekttyper av prosjektgruppene som du definerte på siden **Prosjektoppsett for arbeidsordre** > kategorien **Prosjektgruppe** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**).  
- Oppsettet av prosjektgrupper på siden **Prosjektoppsett for arbeidsordre** brukes når du oppretter arbeidsordrer. Når en ny arbeidsordre blir opprettet, opprettes det automatisk et arbeidsordreprosjekt for et arbeidsordren.  
- Hver livssyklustilstand for arbeidsordre må ha et tilknyttet prosjektstadium.  
- Prosjektstadiet som er knyttet til en livsløpstilstand for arbeidsordre, må defineres som en aktiv fase for prosjektgruppen som er definert i arbeidsordreprosjektet. Arbeidsordreprosjektet opprettes automatisk i en arbeidsordre.
- Når du oppretter en ny arbeidsordre, er den automatiske tilordningen av et arbeidsordreprosjekt basert på oppsettet på siden **Prosjektoppsett for arbeidsordre**.  

Illustrasjonene nedenfor viser tilknytningene mellom arbeidsordreprosjektgrupper, tilknyttede prosjekttyper, prosjektstadier og livssyklustilstander for arbeidsordre.

![Figur 3](media/03-integration-to-pma.png)

![Figur 4](media/04-integration-to-pma.png)

![Figur 5](media/05-integration-to-pma.png)

Hvis du vil ha mer informasjon om hvordan du definerer arbeidsordreprosjekter, kan du se [Prosjektoppsett for arbeidsordre](../setup-for-work-orders/work-order-project-setup.md). Hvis du vil ha mer informasjon om hvordan du oppretter livssyklustilstander for arbeidsordrer, kan du se [i Livssyklustilstand for arbeidsordre](../setup-for-work-orders/work-order-lifecycle-states.md).

Illustrasjonen nedenfor viser en grafisk oversikt over de ulike prosjektene som er opprettet i modulen **Aktivastyring** for å muliggjøre integrering med modulen **Prosjektstyring og regnskap**. Den viser også arbeidsprosessene som prosjektene er relatert til.

![Figur 6](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]