---
title: Produksjonsplanlegging
description: Dette emnet beskriver planlegging for produksjon, og forklarer hvordan du endrer planlagte produksjonsordrer ved å bruke planleggingsoptimalisering.
author: ChristianRytt
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ffee79f152141297ceb24e2d7a40523eac18ffaf
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129759"
---
# <a name="production-planning"></a>Produksjonsplanlegging

Planleggingsoptimalisering støtter flere produksjonsscenarioer. Hvis du går over fra den eksisterende, innebygde hovedplanleggingsmotoren, er det viktig å være oppmerksom på noen endrede virkemåter.

Følgende video gir en kort innføring i noen av begrepene som omhandles i dette emnet: [Dynamics 365 Supply Chain Management: Planlegge optimaliseringsforbedringer](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funksjonen for systemet

Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Planlagte produksjonsordrer for planleggingsoptimalisering*.

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

For å sikre at planleggingsoptimalisering har informasjonen den trenger til å beregne riktig resultat, må du ta med alle produkter som har en hvilken som helst tilknytning til produkter i hele stykklistestrukturen for den planlagte bestillingen. Når det gjelder planleggingsscenarioer som omfatter produksjon, anbefaler vi derfor at du unngår filtrerte kjøringer av hovedplanlegging.

Selv om avhengige underordnede varer automatisk blir oppdaget og tatt med i kjøringer av hovedplanlegging når den innebygde hovedplanleggingsmotoren brukes, utfører ikke planleggingsoptimalisering denne handlingen for øyeblikket.

Hvis for eksempel én bolt fra stykklistestrukturen for produkt A også brukes til å produsere produkt B, må alle produkter i stykklistestrukturen for produktene A og B tas med i filteret. Siden det kan bli komplekst å sikre at alle produkter er en del av filteret, anbefaler vi at du unngår filtrerte kjøringer av hovedplanlegging når produksjonsordrer er involvert. Ellers gir hovedplanlegging uønskede resultater.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Grunner til å unngå filtrerte kjøringer av hovedplanlegging

Når du kjører filtrert hovedplanlegging for et produkt, oppdager ikke planleggingsoptimalisering (i motsetning til den innebygde hovedplanleggingsmotoren) alle delproduktene og råvarene i stykklistestrukturen til dette produktet, og tar dem derfor ikke med i kjøringen av hovedplanleggingen. Selv om planleggingsoptimalisering finner det første nivået i stykklistestrukturen til produktet, laster den ikke inn noen produktinnstillinger (for eksempel standard ordretype eller varedekning) fra databasen.

Data for kjøringen lastes inn på forhånd i planleggingsoptimalisering, og filtrene brukes. Dette betyr at hvis et delprodukt eller en råvare som er tatt med i et bestemt produkt, ikke er en del av filteret, registreres ikke informasjon om det/den for kjøringen. Hvis delproduktet eller råvaren også er inkludert i et annet produkt, fjerner en filtrert kjøring som bare omfatter det opprinnelige produktet og komponentene, eksisterende planlagt behov som er opprettet for dette andre produktet.

Denne logikken kan føre til at filtrerte kjøringer av hovedplanlegging kan gi uventede resultater. De følgende delene gir eksempler som illustrerer de uventede resultatene som kan forekomme.

### <a name="example-1"></a>Eksempel 1

Ferdigvaren *FG* består av følgende komponenter:

- råvaren *R*
- delproduktet *S1*, som består av delproduktet *S2*

Det finnes lagerbeholdning for råvaren *R*, mens delprodukt *S1* ikke finnes på lageret.

Når du foretar en filtrert kjøring av hovedplanlegging for ferdigvaren *FG*, får du en planlagt produksjonsordre for ferdigvaren *FG*, et bestillingsforslag for råvaren *R* og et bestillingsforslag for delproduktet *S1*. Dette er et uønsket resultat, fordi planleggingsoptimalisering har ignorert eksisterende forsyning for råvare *R*, og delproduktet *S1* må produseres ved hjelp av *S2* i stedet for å bestilles direkte. Dette skjedde fordi planleggingsoptimalisering bare har listen over komponenter for ferdigvaren *FG* uten relatert informasjon, for eksempel eksisterende forsyning av komponentene eller standard ordreinnstillinger.

### <a name="example-2"></a>Eksempel 2

Basert på forrige eksempel ser vi at en ytterligere ferdigvare, *FG2*, også bruker også delproduktet *S1*. Det finnes en planlagt bestilling for ferdigvaren *FG2*, og det finnes planlagt behov for alle komponentene, inkludert *S1*.

Du beslutter å rette de uønskede resultatene av den filtrerte kjøringen av hovedplanlegging i forrige eksempel, ved å legge til alle delproduktene og råvarene fra stykklistestrukturen til ferdigvaren *FG* i filteret og deretter kjøre en full, ny generering.

Når du kjører den fulle, nye genereringen, sletter systemet alle eksisterende resultater for alle de inkluderte produktene, og genererer resultatene på nytt basert på de nye beregningene. Dette betyr at eksisterende planlagt behov for produktet *S1* slettes og deretter opprettes på nytt, der det bare tas hensyn til krav til ferdigvaren *FG*, mens kravene til ferdigvaren *FG2* ignoreres. Dette skjer fordi at når du kjører planleggingsoptimalisering, blir ikke det planlagte behovet for andre planlagte produksjonsordrer tatt med, bare det planlagte behovet som genereres under kjøringen, brukes.

> [!NOTE]
> Hvis den eksisterende planlagte ordren for ferdigvare *FG2* har statusen *Godkjent*, blir det godkjente planlagte behovet tatt med, selv når det overordnede produktet ikke blir lagt til i filteret.

Med mindre du legger til alle komponentene i ferdigvaren *FG*, ferdigvaren *FG2* og alle andre produkter som disse komponentene er en del av (sammen med komponentene deres), gir derfor den filtrerte kjøringen av hovedplanleggingen uønskede resultater.

Siden det kan bli komplekst å sikre at alle produkter er en del av filteret, anbefaler vi at du unngår filtrerte kjøringer av hovedplanlegging når produksjonsordrer er involvert.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
