---
title: Produksjonsplanlegging
description: Dette emnet beskriver planlegging for produksjon, og forklarer hvordan du endrer planlagte produksjonsordrer ved å bruke planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470839"
---
# <a name="production-planning"></a>Produksjonsplanlegging

Planleggingsoptimalisering støtter flere produksjonsscenarioer. Hvis du går over fra den eksisterende, innebygde hovedplanleggingsmotoren, er det viktig at du er oppmerksom på noen endrede virkemåter.

Følgende video gir en kort innføring i noen av begrepene som omhandles i dette emnet: [Dynamics 365 Supply Chain Management: Planlegge optimaliseringsforbedringer](https://youtu.be/u1pcmZuZBTw).

## <a name="planned-production-orders"></a>Planlagte produksjonsordrer

Når hovedplanleggingen oppretter planlagte bestillinger for å oppfylle behov, fastsettes ordretypen av verdien i feltet **Type planlagt bestilling**. Hvis feltet **Type planlagt bestilling** er satt til *Produksjon*, opprettes planlagte produksjonsordrer. Disse planlagte produksjonsordrene inneholder informasjon om den aktive stykklisten og rute-ID-en fra det relaterte produksjonsoppsettet.

## <a name="requirements-from-boms"></a>Behov fra stykklister

Det tas hensyn til stykklisteinformasjon under hovedplanlegging. Planresultatet omfatter materialforsyning for å dekke relatert materialbehov for produksjon.

Under hovedplanlegging brukes den gjeldende, aktive stykklisten til å fastsette hvilke materialer som trengs for produksjon. Dette trinnet utføres gjennom alle nivåer i stykklistestrukturen som er knyttet til produksjonsordren som kreves. Materialbehov oppfylles ved å bruke tilgjengelig lagerbeholdning, eksisterende bestilt forsyning og godkjente planlagte bestillinger. Hvis det kreves mer materiale et sted, opprettes det en planlagt bestilling for å dekke behovet.

## <a name="scheduling-during-firming"></a>Planlegging under autorisering

Planlagte produksjonsordrer omfatter rute-ID-en som kreves for produksjonsplanlegging. Planleggingsstøtte under planleggingskjøringen for planlagte bestillinger er imidlertid ventende. Rute-ID-en brukes til å planlegge planlagte produksjonsordrer under autorisering. Derfor kan leveringstiden for planlagte produksjonsordrer avvike fra leveringstiden for tilknyttede planlagte, autoriserte produksjonsordrer som genereres fra dem, som beskrevet her:

- **Planlagt produksjonsordre** – Leveringstiden er basert på den statiske leveringstiden fra det frigitte produktet.
- **Autorisert produksjonsordre** – Leveringstiden er basert på planlegging som bruker ruteinformasjon og relaterte ressursbegrensninger.

Hvis du vil ha mer informasjon om forventet funksjonstilgjengelighet, kan du se [Analyse for tilpassing av planleggingsoptimalisering](planning-optimization-fit-analysis.md).

Hvis du er avhengig av produksjonsfunksjonalitet som ennå ikke er tilgjengelig for planleggingsoptimalisering, kan du fortsette å bruke den innebygde hovedplanleggingsmotoren. Ingen unntak er nødvendig.

## <a name="delays"></a>Forsinkelser

Hvis leveringstiden for nødvendig materiale er lengre enn perioden mellom dagens dato og materialbehovsdatoen, blir den planlagte bestillingen for det nødvendige materialet og den tilknyttede produksjonsordren forsinket. Når det gjelder planlagte bestillinger, beregnes forsinkelsen (i dager) basert på leveringstiden fra det frigitte produktet. Forsinkelsesinformasjonen spres deretter til alle nivåer i stykklistestrukturen. Derfor kan du følge virkningen av forsinket råvare hele veien til kundesalgsordren.

## <a name="modifying-planned-orders"></a>Endre planlagte bestillinger

Når du endrer informasjon i en planlagt bestilling, får du en melding om at virkningen av manuelle endringer i planlagte bestillinger ikke gjenspeiles i resten av planen før neste hovedplanlegging kjøres.

Hvis du vil endre informasjon i en planlagt bestilling og se hvordan de relaterte materialbehovene påvirkes, følger du denne fremgangsmåten.

1. Oppdater den planlagte bestillingen.
2. Godkjenn den planlagte bestillingen.
3. Kjør hovedplanlegging.

Når du kjører hovedplanlegging, skal du ikke bruke filtre hvis planlagte produksjonsordrer er inkludert. Hvis du vil ha mer informasjon, kan du se delen [Filtre](#filters) senere i dette emnet.

> [!NOTE]
> Hvis leveringsdatoen for den planlagte bestillingen endres til en senere dato, kan behovet bli utlignet mot en ny planlagt bestilling. Dette skjer når den nye forsyningsdatoen forårsaker en forsinkelse for det utlignede behovet, men forsinkelsen kan unngås i henhold til innstillingene for leveringstid.

## <a name="explosion-page"></a>Nedbryting-siden

Du kan bruke **Nedbryting**-siden til å analysere behovet som er nødvendig for en bestemt produksjonsordre eller planlagt produksjonsordre, tilknyttet dekning og utligningsinformasjon. Informasjon på **Nedbryting**-siden oppdateres under hovedplanlegging. Du kan ikke oppdatere informasjonen direkte fra **Nedbryting**-siden.

## <a name="filters"></a><a name="filters"></a>Filtre

Når det gjelder planleggingsscenarioer som omfatter produksjon, anbefaler vi at du unngår filtrerte kjøringer av hovedplanlegging. For å sikre at planleggingsoptimalisering har informasjonen som trengs for å beregne riktig resultat, må du ta med alle produkter som har en hvilken som helst tilknytning til produkter i hele stykklistestrukturen for den planlagte bestillingen.

Selv om avhengige underordnede varer automatisk blir oppdaget og tatt med i kjøringer av hovedplanlegging når den innebygde hovedplanleggingsmotoren brukes, utfører ikke planleggingsoptimalisering denne handlingen.

Hvis for eksempel én bolt fra stykklistestrukturen for produkt A også brukes til å produsere produkt B, må alle produkter i stykklistestrukturen for produktene A og B tas med i filteret. Siden det kan bli svært komplekst å sikre at alle produkter er en del av filteret, anbefaler vi at du unngår filtrerte kjøringer av hovedplanlegging når produksjonsordrer er involvert.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]