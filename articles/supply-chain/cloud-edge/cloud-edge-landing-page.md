---
title: Sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring
description: Dette emnet inneholder informasjon om sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 28301cdfb86d00ea6f04e996fe7fb1485e83b2d4
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104970"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sky- og kantskalaenheter muliggjør distribusjon av arbeidsmengder for produksjon og lagerkjøring blant ulike miljøer. Denne funksjonaliteten kan bidra til å forbedre ytelsen, forhindre tjenesteavbrudd og gi maksimal oppetid. Den leveres av følgende tilleggsprogrammer:

- Cloud Scale Unit-tillegget for Dynamics 365 Supply Chain Management
- Edge Scale Unit-tillegget for Dynamics 365 Supply Chain Management

Firmaer som jobber med produksjon og distribusjon, må kunne kjøre viktige forretningsprosesser hele døgnet, uten avbrudd og ved skala. Med sky- og kantskalaenheter kan firmaer kjøre viktige produksjons- og lagerprosesser uten avbrudd, selv når det gjelder nettverkstilkobling eller forsinkelsesproblemer.

## <a name="public-preview-information"></a>Informasjon om offentlig forhåndsversjon

Forhåndsversjonen gir ett miljø som fungerer som et skybasert senter for Dynamics 365 Supply Chain Management-miljøet ditt og ett miljø som fungerer som en skyskalaenhet.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Forhåndsversjonstilgjengelighet

Forhåndsversjonen for sky- og kantskalaenheter blir tilgjengelig for eksisterende kunder av Supply Chain Management i oktober 2020.

Hvis du vil ha tilgang til forhåndsversjoen for oktober 10.0.15/Platform Update 39 for distribusjon i miljøet for [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), må du være del av forhåndsversjonsprogrammet for tidlig tilgang (også kalt PEAP) for Supply Chain Management. Du kan bli med i PEAP hvis du allerede er medlem av [Dynamics Insider Program](https://experience.dynamics.com/insider). Velg programmet som heter Finance and Operations: Forhåndsversjonsprogram for tidlig tilgang (PEAP).

> [!IMPORTANT]
> Skalaenhetsfunksjonen for Supply Chain Management blir bare tilgjengelig hvis du godtar [vilkårene for Cloud + Edge-forhåndsversjonen for Finance and Operations](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Databehandling for forhåndsversjonen

Under den offentlige forhåndsversjonen vil enkelte administrasjonstjenester bare bli driftet i USA. Når funksjonen imidlertid blir allment tilgjengelig, vil disse administrasjonstjenestene være tilgjengelige i alle de samme områdene som støttes av Supply Chain Management. Dette påvirker overføring og lagring av administrativ informasjon som brukes av skalaenhetsbehandling, inkludert:

- Leiernavn og ID-er
- ID-er for LCS-prosjekter
- Administrator-e-post som brukes til å logge på
- Miljø-ID-er for senter og skalaenheter
- Arbeidsbelastningskonfigurasjoner
- Innsamlede måledata (for eksempel ventetid og gjennomstrømming) som vises på kartanalysesiden

Data som overføres til og lagres i datasentrene i USA, blir slettet når forhåndsversjonsmiljøet avsluttes.

### <a name="sign-up-for-the-preview"></a>Registrere deg for forhåndsvisning

Hvis du vil registrere deg for Cloud- og Edge-forhåndsversjonen for Supply Chain Management, må organisasjonen din allerede ha et aktivert Supply Chain Management-skymiljø.

Skalaenhetsfunksjonene er for tiden i offentlig forhåndsversjon. Når du registrerer deg, må du bruke en brukerkonto på den bestemte leieren. Du må også være en prosjekteier eller en miljøadministrator i LCS for et aktivt Dynamics 365 LCS-prosjekt i den leieren.

Når du registrerer deg for forhåndsversjonen, velger du en leier og går gjennom registreringstrinnene. Så snart Microsoft kan tildele forhåndsversjonskapasiteten, sender vi deg en e-post som inneholder klargjøringsdetaljer og kampanjekodene for to miljøer (et senter og en skalaenhet) for det riktige LCS-prosjektet. Deretter kan du distribuere de to miljøene som sandkassemiljøer med lag 2. Disse miljøene vil være gyldige i 60 dager fra opprettelsesdatoen til kampanjekodene. Du må ikke bruke de to miljøene før trinnet som er beskrevet i det neste avsnittet, er fullført.

Når du har bekreftet med Microsoft at de to miljøene er distribuert ved hjelp av kampanjekodene, blir et av miljøene konfigurert til å fungere som et senter, og det andre blir konfigurert til å fungere som en skalaenhet. Du kan deretter konfigurere skalaenhetene og distribuere valgte arbeidsbelastninger for lagerstyring og produksjon ved å bruke [Scale Unit Manager-portalen](https://aka.ms/SCMSUM).

Forhåndsversjonsmiljøer blir automatisk slettet etter 60 dager. De kan imidlertid bli slettet tidligere hvis det ser ut til at de ikke brukes. Når forhåndsversjonsmiljøet er slettet, kan du registrere deg og sette deg i kø for en ny forhåndsversjonsdistribusjon.

Hvis du vil registrere deg for forhåndsversjonen, går du til [Scale Unit Manager-portalen](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Begrensninger som gjelder under forhåndsversjonsperioden

> [!IMPORTANT]
> For den første fasen av forhåndsversjonsprogrammet for denne funksjonen støtter Microsoft bare sentre som har skyskalaenheter, ikke sentre med kantskalaenheter. Kantskalaenheter installeres lokalt og forventes å bli tilgjengelige i en kommende fase av programmet.

siden sky- og kantskalaenheter er en forhåndsversjonsfunksjon, er tjenester som er tilknyttet disse, for øyeblikket tilgjengelige i begrensede land og områder. Hvis du aktiverer sky- og kantskalaenheter, bekrefter du at du forstår at noen data som er knyttet til konfigurasjonen og behandling av sky- og kantskalaenheter, kan lagres i et datasenter som er plassert i USA. Hvis du aktiverer sky- og kantskalaenheter, godtar du også [vilkårene for Cloud- + Edge-forhåndsversjon for Finance and Operations](https://Aka.ms/SCMCnETerms). Hvis du vil ha mer informasjon om sky- og kantskalaenheter, kan du se [dokumentasjonen](https://aka.ms/scmcne).

Personvernet ditt er viktig for Microsoft. Les [personvernerklæringen](https://aka.ms/privacy) for å finne ut mer.

> [!IMPORTANT]
> Noen forretningsfunksjoner støttes ikke fullstendig i den offentlige forhåndsversjonen når arbeidsbelastninger brukes på skalaenheter. Hvis du vil ha mer informasjon om de funksjonelle arbeidsbelastningene, kan du se avsnittene senere i dette emnet.

## <a name="scale-units-and-dedicated-workloads"></a>Skalaenheter og dedikerte arbeidsbelastninger

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 med skalaenheter":::

Skalerings enheter utvider Supply Chain Management-sentermiljøet ved å legge til dedikert behandlingskapasitet. Skalaenheter kan kjøres i skyen. De kan også kjøre på kanten på det lokale anlegget. Skalaenheter kan midlertidig kobles fra sentermiljøet. Når de er koblet til, mottar skalaenheter all informasjonen som kreves for å kjøre den dedikerte behandlingen for tildelte arbeidsbelastninger.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Skalaenhetsalternativer i offentlig forhåndsversjon":::

For den offentlige forhåndsversjonen kan du konfigurere et sentermiljø med valgte arbeidsbelastninger på en skyskalaenhet ved hjelp Scale Unit Manager-portalen. Forhåndsversjonsdeltakere som har tilgang til et lokalt forretningsdatamiljø (LBD), kan også konfigurere LBD-miljøet som en kantskalaenhet.

En arbeidsbelastning er et definert sett med forretningsfunksjoner som kan beregnes som en faktor og delegeres til en skalaenhet. Forhåndsversjonsfunksjonen er for øyeblikket to typer arbeidsbelastninger:

- Produksjonsutførelse
- Lagerstyring

Du kan tilordne én av hver type arbeidsbelastning per skalaenhet. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Dedikerte funksjoner for arbeidsbelastning for produksjonskjøring i en skalaenhet

Når det gjelder produksjonskjøring, gir sky- og kantskalaenheter følgende funksjoner, selv når kantenhetene ikke er koblet til skyen:

- Maskinoperatører og produksjonsledere har tilgang til driftsproduksjonsplanen.
- Maskinoperatører kan holde planen oppdatert ved å kjøre separat og behandle produksjonsjobber.
- Produksjonslederen kan justere driftsplanen.
- Arbeidere kan få tilgang til tid og fremmøte for innstempling og utstempling på kanten for å sikre riktig beregning av arbeiderlønn.

Hvis du vil ha mer informasjon, kan du se [detaljer for arbeidsbelastning for produksjonsskalaenhet](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Dedikerte funksjoner for arbeidsbelastning for lagerstyring i en skalaenhet

Når det gjelder lagerstyring, gir sky- og kantskalaenheter følgende funksjoner, selv når kantenhetene ikke er koblet til skyen:

- Behandling av valgte bølgemetoder er aktivert for salgsordrer og etterfylling på forespørsel.
- Lagermedarbeidere kan kjøre lagerarbeid for salg og etterfyllings på forespørsel ved hjelp av lagerappen.
- Lagerarbeidere kan be om lagerbeholdning ved hjelp av lagerappen.
- Lagerarbeidere kan opprette og kjøre lagerflyttinger ved hjelp av lagerappen.
- Lagerarbeidere kan registrere bestillinger og utføre plasseringer ved hjelp av lagerappen.

Hvis du vil ha mer informasjon, kan du se [detaljer for arbeidsbelastning for lagerskalaenhet](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Innføring av skalaenheter for Supply Chain Management-miljøet

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Distribuer forhåndsversjonen for sky- og kantskalaenheter

Følgende illustrasjon viser registreringen og klargjøringsflyten for den offentlige forhåndsversjonen for skyskalaenheter.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Registreringstrinn for forhåndsversjon":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Velg LCS-prosjektleieren og den detaljerte forhåndsversjonsprosessen

I den offentlige forhåndsversjonen viser [Scale Unig Manager-portalen](https://aka.ms/SCMSUM) listen over leiere som kontoen din er en del av, og hvor du er en eier eller miljøadministrator for et LCS-prosjekt.

Hvis leieren du leter etter, ikke finnes i listen, kan du gå til [LCS](https://lcs.dynamics.com/v2) og kontrollere at du er en miljøadministrator eller en prosjekteier for LCS-prosjektet for denne leieren. Vær oppmerksom på at bare Azure Active Directory-kontoer (Azure AD) fra den valgte leieren er autorisert til å fullføre registreringen.

> [!NOTE]
> Etter at du har brukt endringer på LCS, kan det ta opptil 30 minutter før listen over leiere gjenspeiler endringene.

Listen viser registreringsstatusen for hver leier.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Registreringsalternativ for en leier":::

Velg **Klikk på her for å registrere deg**-kobling for å registrere en LCS-leier som skal delta i forhåndsversjonen. Du må godta vilkårene. Du må også oppgi en e-postadresse for firma som Microsoft kan sende kommunikasjon som er knyttet til registreringsprosessen for forhåndsversjonen, til.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Registreringsinnsending for en leier":::

Microsoft vil se gjennom forespørselen din og gi deg beskjed om de neste trinnene ved å sende en e-post til adressen du har oppgitt i registreringsskjemaet.

Når du har fått tilgang til forhåndsversjonsprogrammet, mottar du to kampanjekoder for LCS-prosjektet. Du kan nå bruke disse kampanjekodene til å distribuere to miljøer i LCS. Miljøene må bruke PEAP-utgaven 10.0.15 eller nyere. Når du er ferdig med å bruke kampanjekodene, må du varsle Microsoft (som beskrevet) slik at vi kan fullføre aktiveringen av miljøene for forhåndsversjonsfunksjonene. Microsoft gir deg beskjed når dette konfigurasjonstrinnet er fullført.

Du kan nå starte å konfigurere skalaenheter og arbeidsbelastninger i forhåndsversjonsmiljøet.

> [!IMPORTANT]
> Når du konfigurerer skyskalaenheter, kan du [utføre alle de nødvendige trinnene i Scale Unit Manager-portalen](#scale-unit-manager-portal).
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Administrer skalaenheter og arbeidsbelastninger ved å bruke Scale Unit Manager-portalen

Gå til [Scale Unit Manager-portalen](https://aka.ms/SCMSUM), og logg på ved hjelp av leierkontoen. På **Konfigurer skalaenheter** kan du legge til et sentermiljø hvis det ikke allerede er oppført. Du kan deretter velge senteret du vil konfigurere med skalaenheter og arbeidsbelastninger.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Administrering av skalaenhet og arbeidsbelastning":::

Hvis du vil legge til en eller flere skalaenheter som er tilgjengelige i topologien, velger du **Legg til skalaenheter**. I forhåndsversjonen skal du se skyskalaenheten du distribuerte fra en av kampanjekodene du mottok som en del av forhåndsversjonsprogrammet.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

I **Definerte arbeidsbelastninger**-fanen bruker du **Opprett arbeidsbelastning**-knappen til å legge til en arbeidsbelastning for lagerstyring eller produksjonskjøring i en av skalaenhetene. For hver arbeidsbelastning må du angi konteksten for prosessene som skal eies av arbeidsbelastningen. Når det gjelder arbeidsbelastninger for lagerstyring, er konteksten et bestemt lager på et bestemt område og en bestemt juridisk enhet. For arbeidsbelastninger for produksjonskjøring er konteksten et bestemt område i en juridisk enhet.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Oppretting av arbeidsbelastning":::

> [!IMPORTANT]
> Med Scale Unit Manager-portalen i forhåndsversjonen kan du ikke fjerne arbeidsbelastninger fra skalaenheter eller oppheve tilordning av en skalaenhet fra en senter etter at tilordningen er opprettet. Hvis du må fjerne en tilordning, kontakter du kontaktpersonen for administrasjonen av forhåndsversjonsprogrammet.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->
