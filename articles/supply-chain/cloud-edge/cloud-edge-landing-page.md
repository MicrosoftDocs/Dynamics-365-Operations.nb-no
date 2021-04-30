---
title: Bruk skalaenheter for å øke fleksibiliteten for arbeidsbelastninger i Supply Chain Management
description: Dette emnet inneholder informasjon om sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring.
author: cabeln
ms.date: 04/13/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c47088edd89413d196e904bc7eaa115585bf8464
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899149"
---
# <a name="use-scale-units-to-help-increase-resilience-for-supply-chain-management-workloads"></a>Bruk skalaenheter for å øke fleksibiliteten for arbeidsbelastninger i Supply Chain Management

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Skalaenhetsfunksjonen for Microsoft Dynamics 365 Supply Chain Management gjøres tilgjengelig for deg under de betingelsene som styrer bruken av tjenesten. Hvis du vil ha mer informasjon, kan du se [Juridisk informasjon om Microsoft Dynamics](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Hvis du aktiverer sky- og kantskalaenheter, bekrefter du at du forstår at noen data som er knyttet til konfigurasjonen og behandling av sky- og kantskalaenheter, kan lagres i et datasenter som er plassert i USA. Hvis du vil lære mer om databehandling for sky- og kantskalaenheter, kan du se [Databehandling under behandling av skalaenheter](#data-processing-management) senere i dette emnet.

## <a name="core-value-proposition-for-scale-units"></a>Kjerneverdiforslag for skalaenheter

Firmaer som jobber med produksjon og distribusjon, må kunne kjøre viktige forretningsprosesser hele døgnet, uten avbrudd og ved skala. Med sky- og kantskalaenheter kan firmaer kjøre viktige produksjons- og lagerprosesser uten avbrudd, selv når det gjelder nettverkstilkobling eller forsinkelsesproblemer.

Sky- og kantskalaenheter muliggjør distribusjon av arbeidsmengder for produksjon og lagerkjøring blant ulike miljøer. Denne funksjonaliteten kan bidra til å forbedre ytelsen, forhindre tjenesteavbrudd og gi maksimal oppetid. Skalaenheter leveres ved hjelp av følgende tillegg for Supply Chain Management-abonnementet:

- Cloud Scale Unit-tillegget for Dynamics 365 Supply Chain Management (*tilgjengelig april 2021*)
- Edge Scale Unit-tillegget for Dynamics 365 Supply Chain Management (*tilgjengelig snart*)

Funksjoner for arbeidsbelastninger lanseres kontinuerlig gjennom inkrementelle forbedringer.

## <a name="scale-units-and-dedicated-workloads"></a>Skalaenheter og dedikerte arbeidsbelastninger

Skalerings enheter utvider Supply Chain Management-sentermiljøet ved å legge til dedikert behandlingskapasitet. Skalaenheter kan kjøres i skyen. De kan også kjøre på kanten på det lokale anlegget.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 med skalaenheter":::

Skalaenheter gir fleksibilitet, pålitelighet og skala for de tilordnede arbeidsmengdene. Kantskalaenheter kan kobles midlertidig fra nettskymiljøet, og arbeiderne kan fortsette å jobbe i de tilordnede arbeidsmengdene på kanten.

En *arbeidsbelastning* er et definert sett med forretningsfunksjoner som kan beregnes som en faktor og delegeres til en skalaenhet. Selv om arbeidsbelastningen for lagerstyring er lansert, er arbeidsbelastningen for produksjonsutførelse fremdeles i forhåndsversjon.

Du kan konfigurere sentermiljøet og skyskalaenhetene for utvalgte arbeidsbelastninger ved hjelp av [Scale Unit Manager-portalen](https://sum.dynamics.com). Du kan også tilordne flere arbeidsbelastninger per skalaenhet. Hvis du vil ha informasjon om forutsetningene og begrensningene for skyskalaenheter i den gjeldende versjonen, kan du se [Forutsetninger og begrensninger for skyskalaenheter](#cloud-scale-unit-prerequisites) senere i dette emnet.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Dedikerte funksjoner for arbeidsbelastning for lagerstyring i en skalaenhet

Lagerstyringens arbeidsbelastning er den første distribuerte arbeidsbelastningen for skalaenheter som er lansert for allmenn tilgjengelighet.

For lagerstyring leverer skalaenheter følgende funksjoner:

- Systemet kan behandle utvalgte bølgemetoder for salgsordrer og etterfylling på forespørsel.
- Lagermedarbeidere kan kjøre lagerarbeid for salg og etterfyllings på forespørsel ved hjelp av mobilappen Lagerstyring.
- Lagerarbeidere kan be om lagerbeholdning ved hjelp av mobilappen Lagerstyring.
- Lagerarbeidere kan opprette og kjøre lagerflyttinger ved hjelp av mobilappen Lagerstyring.
- Lagerarbeidere kan registrere bestillinger og utføre plasseringer ved hjelp av mobilappen Lagerstyring.

Hvis du vil ha mer informasjon, kan du se [Arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Dedikerte funksjoner for arbeidsbelastning for produksjonskjøring i en skalaenhet

Den første lanseringen av produksjonsarbeidsbelastningen er i forhåndsversjon og leverer følgende funksjoner:

- Maskinoperatører og produksjonsledere har tilgang til driftsproduksjonsplanen.
- Maskinoperatører kan holde planen oppdatert ved å kjøre separat og behandle produksjonsjobber.
- Produksjonslederen kan justere driftsplanen.
- Arbeidere kan få tilgang til tid og fremmøte for innstempling og utstempling på kanten for å sikre riktig beregning av arbeiderlønn.

Hvis du vil ha mer informasjon, kan du se [Arbeidsbelastninger for produksjonsutførelse for sky- og kantskalaenheter](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Vurderinger før du aktiverer den distribuerte, hybride topologien for Supply Chain Management

Ved å aktivere den distribuerte, hybride topologien kan du endre skymiljøet i Supply Chain Management, slik at det fungerer som et senter. Du kan også tilknytte flere miljøer som er konfigurert som skalaenheter i skyen eller på kanten.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Forutsetninger og begrensninger for skyskalaenheter

I den gjeldende lanseringen av skalaenheter er det noen funksjoner som ennå ikke er tilgjengelige, men som kan legges til i trinnvise lanseringer over tid.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Du må være en lisensiert Supply Chain Management-kunde

For å ta i bruk den distribuerte topologien må du ha en lisens for Supply Chain Management. Det eksisterende skymiljøet vil bli senteret i den hybride topologien. Du kan deklarere både sandkassemiljøer og produksjonsmiljøer som sentermiljøer, og du kan legge til skalaenheter i henhold til tilleggene du skaffer.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Eksisterende prosjekter må administreres via den globale kommersielle versjonen av LCS

Eksisterende Microsoft Dynamics Lifecyle Services-prosjekter (LCS) må oppfylle følgende versjonskrav:

- Prosjektet må administreres via den globale kommersielle versjonen av LCS på [lcs.dynamics.com](https://lcs.dynamics.com).
- Lokale versjoner av LCS (for eksempel [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) og [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) støttes ikke.
- Governmental Cloud-versjoner av LCS støttes ikke.
- Mooncake-versjonen av LCS støttes ikke.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Det gjeldende produksjonsmiljøet må være av den selvbetjente typen i LCS

Det gjeldende produksjonsmiljøet må være tagget med **Selvbetjent**-typen i LCS. Denne typen indikerer at leieren i LCS-prosjektet allerede er konvertert, slik at det støtter Azure Service Fabric-vertsmodellen.

> [!IMPORTANT]
> Miljøtyper som kjører som infrastruktur som en tjeneste (IaaS), støttes ikke. Disse miljøene merkes vanligvis med typen **Microsoft-administrert** i LCS. Hvis du har miljøer av denne typen, kan du samarbeide med Microsoft-kontakten for å forstå tidslinjen for migrering til typen **Selvbetjent**.

Microsoft er i ferd med en overfang for alle skymiljøer i Supply Chain Management fra en IaaS-modell til en topologi som driftes i Service Fabric. Denne flyttingen gir bedre skalerbarhet og bidrar til å forenkle serviceadministrasjonen. Derfor er distribusjons- og vedlikeholdsoperasjoner raskere. På samme måte migreres servicekomponenter til konseptet med mikrotjenester, og servicevertsmodellen vil [gå over](https://docs.microsoft.com/virtualization/windowscontainers/about/containers-vs-vm) fra en VM-modell (virtuell maskin) til en lett arkitektur med beholdere.

I siste instans vil den samme Service Fabric-baserte tjenesteinfrastrukturen som er basert på beholdere, drive både sky- og kantforekomster av tjenesten, uansett om en forekomst ligger i skyen eller en skalaenhet i skyen eller på kanten.

Før du kan ta i bruk den hybride topologien som støtter skalaenheter, må prosjektleiere gå over til den Service Fabric-driftede modellen. I tillegg må ethvert miljø som fungerer som et senter, konverteres.

> [!TIP]
> Hvis du vil spørre om statusen til LCS-prosjektleieren, kan du slå opp typen miljø i [LCS](https://lcs.dynamics.com/) eller ta kontakt med partneren din eller Microsoft-kontakten.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Lokale forretningsdatamiljøer (lokale miljøer) støttes ikke som sentre for skalaenheter

Lokale miljøer kan ikke fungere som sentre for skalaenheter. Sentermiljøer må alltid være skybaserte.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Administrasjonsfunksjoner for skalaenheter er begrenset

Administrasjonsfunksjoner som kan bidra med bevegelser av arbeidsbelastninger, er begrenset. Enkente administrasjonsoperasjoner støttes ikke via selvbetjening, og du må kanskje be om støtte via en partner eller Microsoft-kontakt. Eksempler inkluderer noen arbeidsbelastningsbevegelser mellom skalaenheter og midlertidige ad hoc-bevegelser i nødscenarier.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Måledata og målinger er ennå ikke tilgjengelig

Måledata og målinger som kan hjelpe deg med å velge det beste programmet for skalaenheter, er ennå ikke tilgjengelige. Samarbeid med Microsoft-kontakten din eller implementeringspartneren for å velge det mest fordelaktige programmet.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Databehandling under administrasjon av skalaenheter

Når du aktiverer Dynamics 365-miljøet for å støtte den distribuerte, hybride topologien for sky- og kantskalaenheter, vil enkelte administrasjonstjenester bare drifts i USA, som for LCS. Denne virkemåten påvirker overføringen og lagringen av noe administrativ informasjon og konfigurasjonsinformasjon som brukes av [Scale Unit Manager-portalen](https://sum.dynamics.com). Her er noen eksempler:

- Leiernavn og ID-er
- ID-er for LCS-prosjekter
- E-postadresser til administrator og prosjekteier som brukes ved pålogging
- Miljø-ID-er for senteret og skalaenhetene
- Konfigurasjoner av arbeidsbelastninger, inkludert navn og fysiske adresser for juridiske enheter og anlegg, slik at topologien kan vises på et geografisk kart
- Innsamlet metrikk (for eksempel ventetid og produksjon) som blir vist på kartanalysesiden for å hjelpe deg med å velge den mest fordelaktige bruken av skalaenhetene dine.

Data som overføres til og lagres i datasentre i USA, blir slettet i henhold til Microsofts retningslinjer for databevaring. Personvernet ditt er viktig for Microsoft. Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.

## <a name="onboarding-in-two-stages"></a>Pålasting to stadier

Prosessen med pålastning i en distribuert, hybrid topologi har to stadier. I det første stadiet må du validere tilpasninger for å sikre at de fungerer i den distribuerte topologien som har skalaenheter. Sandkasse- og produksjonsmiljøer flyttes bare i løpet av det andre stadiet.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>Stadium 1: Evaluere tilpasninger i utviklingsmiljøer med én boks

Før du begynner å pålaste sandkasse- eller produksjonsmiljøet, anbefaler vi at du utforsker skalaenheter i et utviklingsoppsett, for eksempel miljø med én boks (kalles også et nivå 1-miljø), slik at du kan validere prosesser, tilpasninger og løsninger. I løpet av dette stadiet blir data og tilpasninger brukt i miljøene med én boks. Ett miljø tar rollen som senteret, og det andre tar rollen som en skalaenhet. Dette oppsettet gir den beste måten å identifisere og løse problemer på. Den nyeste builden for tidlig tilgang (PEAP) kan også brukes til å fullføre dette stadiet.

For stadium 1 bør du bruke [distribusjonsverktøy for skalaenheter for utviklingsmiljøer med én boks](https://github.com/microsoft/SCMScaleUnitDevTools). Ved hjelp av disse verktøyene kan du konfigurere senteret og skalere enhetene i ett eller to separate miljøer med én boks. Verktøyene leveres som binær lansering og i kildekode på GitHub. Studer wiki-en til prosjektet, som omfatter en [trinnvis bruksveiledning](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) som beskriver hvordan verktøyene brukes.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>Stadium 2: Skaffe tillegg, og distribuere dem i sandkasse- og produksjonsmiljøene

Hvis du vil klargjøre ett av sandkasse- eller produksjonsmiljøene i den nye topologien, må du anskaffe tillegg for én eller flere skyskalaenheter (og for kantskalaenheter i fremtiden). Tilleggene vil gi tilsvarende prosjekt- og miljøspor i [LCS](https://lcs.dynamics.com/), slik at skalaenhetsmiljøene kan distribueres.

> [!NOTE]
> Tilleggene for skalaenhetene er ikke sammenknyttet til et begrenset antall brukere, men kan brukes av alle brukere i det eksisterende abonnementet, basert på rollene som administratoren tilordner.

Skalaenheter tilbys i flere lagerenheter (SKU-er) og prissettingsalternativer. Derfor kan du velge det alternativet som passer best til ditt planlagte månedlige transaksjonsvolum og ytelseskrav.

SKU-en på grunnivå kalles *Grunnleggende*, og den mer utførende SKU-en kalles *Standard*. Hver SKU er forhåndslastet med et bestemt antall månedlige transaksjoner. Du kan imidlertid øke det månedlige transaksjonsbudsjettet ved å legge til overbetalingstillegg for hver SKU.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Tillegg for skyskalaenheter":::

> [!TIP]
> Samarbeid med partneren din og Microsoft for å forstå den månedlige transaksjonsstørrelsen du trenger, for å identifisere størrelsen på transaksjonen som passer best til dine behov.

Innkjøpet av hvert skalaenhetstillegg gir deg ikke bare et månedlig volum av transaksjoner, men gir deg også rett til et bestemt antall miljøspor i LCS. For hvert Cloud Scale Unit-tillegg har du rett på én ny produksjonsplass og én ny plass i sandkassen. Under introduksjonsprosessen vil det bli lagt til et nytt LCS-prosjekt som har disse plassene. Bruksrettighetene for disse plasene er bundet, slik at disse må brukes som skalaenheter som har et skysenter.

Tillegg for overforbruk gir deg ikke rett til nye miljøplasser.

Hvis du vil anskaffe flere sandkassemiljøer, kan du kjøpe ekstra vanlige sandkasseplasser. Microsoft kan deretter hjelpe deg med å aktivere disse plassene som skalaenheter for sandkasser for den hybride topologien.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Ta i bruk den distribuerte, hybride topologien for Supply Chain Management

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Velg LCS-prosjektleieren og den detaljerte pålastingsprosessen

Når du er ferdig med å planlegge hvordan du vil ta i bruk den distribuerte, hybride topologien for Supply Chain Management, bruker du [Scale Unit Manager-portalen](https://aka.ms/SCMSUM) til å starte pålastingsprosessen. I portalen velger du fanen **Dynamics 365-leiere**. Denne fanen viser listen over leiere som kontoen din er en del av, og hvor du er en eier eller miljøadministrator for et LCS-prosjekt.

Hvis leieren du leter etter, ikke finnes i listen, kan du gå til [LCS](https://lcs.dynamics.com/v2) og kontrollere at du er en miljøadministrator eller en prosjekteier for LCS-prosjektet for denne leieren. Bare Azure Active Directory-kontoer (Azure AD) fra den valgte leieren er autorisert til å fullføre registreringen.

> [!NOTE]
> Etter at du har brukt endringer på LCS, kan det ta opptil 30 minutter før listen over leiere gjenspeiler endringene.

Listen viser pålastingsstatusen for hver leier.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Liste over leiere på fanen Dynamics 365-leiere":::

Velg **Klikk her for å komme i gang** for å be om pålasting for LCS-leieren. Du må godta vilkårene. Du må også oppgi en e-postadresse for firma der Microsoft kan sende kommunikasjon som er knyttet til pålastingsprosessen.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Registreringsinnsending for en leier":::

Microsoft vil se gjennom forespørselen din og gi deg beskjed om de neste trinnene ved å sende en e-post til adressen du har oppgitt i registreringsskjemaet. Microsoft vil samarbeide nøye med deg for å aktivere skalaenheter i hybridtopologien for forretningsscenariet.

Når pålastingen er fullført, kan du bruke porten til å konfigurere skalaenheter og arbeidsbelastninger.

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Administrer skalaenheter og arbeidsbelastninger ved å bruke Scale Unit Manager-portalen

Gå til [Scale Unit Manager-portalen](https://aka.ms/SCMSUM), og logg på ved hjelp av leierkontoen. På **Konfigurer skalaenheter** kan du legge til et sentermiljø hvis det ikke allerede er oppført. Du kan deretter velge senteret du vil konfigurere med skalaenheter og arbeidsbelastninger.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Administrering av skalaenhet og arbeidsbelastning":::

Hvis du vil legge til en eller flere skalaenheter som er tilgjengelige i abonnementene, velger du **Legg til skalaenheter**.

I **Definerte arbeidsbelastninger**-fanen bruker du **Opprett arbeidsbelastning**-knappen til å legge til en arbeidsbelastning for lagerstyring i en av skalaenhetene. For hver arbeidsbelastning må du angi konteksten for prosessene som skal eies av arbeidsbelastningen. Når det gjelder arbeidsbelastninger for lagerstyring, er konteksten et bestemt lager på et bestemt område og en bestemt juridisk enhet.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Oppretting av arbeidsbelastning":::

> [!TIP]
> Over tid vil inkrementelle forbedringer legges til i Scale Unit Manager-opplevelsen for å gjøre det enklere å styre livssyklusadministrasjonen. De spesifikke egenskapene for den gjeldende versjonen er dokumentert i en håndbok for pålasting som er tilgjengelig for kunder som er i ferd med å ta i bruk den distribuerte, hybride topologien for Supply Chain Management. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
