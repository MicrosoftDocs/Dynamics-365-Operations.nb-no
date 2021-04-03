---
title: Grensesnitt for materialhåndteringsutstyr (MHAX)
description: Dette emnet beskriver hvordan du konfigurerer MHAX-systemer (Material Handling Equipment Interface) slik at du kan koble til systemer for ekstern fysisk materialhåndtering (MH).
author: Mirzaab
manager: tfehr
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ea021529d7417fb3170c859c7fffcb2cfd23a43f
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571848"
---
# <a name="material-handling-equipment-interface-mhax"></a>Grensesnitt for materialhåndteringsutstyr (MHAX)

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Du kan bruke *grensesnittet for materialhåndteringsutstyr* (MHAX) til å koble systemer for ekstern fysisk materialhåndtering (MH) til et lager som administreres av avansert lagerstyring (WMS) i Microsoft Dynamics 365 Supply Chain Management. Grensesnittet mellom WMS- og MH-systemene består av to køer: én for utgående hendelser (WMS til MH) og én for innkommende hendelser (MH til WMS). WMS-systemet genererer utgående hendelser basert på arbeidslinjer som opprettes under ulike arbeidsopprettings- og utføringsprosesser. MH-systemet måler deretter WMS-systemet regelmessig for nye hendelser og behandler svarene. Når MH-systemet er ferdig med å behandle hendelsene i henhold til arbeidsinstruksjoner, sender det innkommende hendelser, for eksempel fullføring av arbeidslinje og plukking med mangler.

Illustrasjonen nedenfor viser de ulike elementene og rekkefølgen som prosessene forekommer i når du bruker MHAX-integrering.

![MHAX-komponenter og -samhandlinger](media/mhax-components.png "MHAX-komponenter og -samhandlinger")

Her er en forklaring på samhandlingen som vises i den forrige illustrasjonen:

1. Når arbeid opprettes eller utføres, opprettes utgående hendelser i utgående kø.
2. MH-utstyret kobler til MH-utstyrstjenesten, søker etter nye hendelser som er relevante for den og behandler disse hendelsene.
3. Når MH-utstyret er klart til å rapportere tilbake, kobles det til tjenesten på nytt og sender innkommende hendelser. Disse hendelsene behandles umiddelbart av købehandleren.
4. Basert på de innkommende hendelsesdataene, kan købehandleren kjøre eksisterende arbeid, endre eller opprette nytt arbeid.

## <a name="turn-on-the-mhax-feature"></a>Aktivere MHAX-funksjonen

Før du kan bruke MHAX-funksjonen må du aktivere både funksjonen og konfigurasjonsnøkkelen.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
2. I arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** aktiverer du funksjonen som kalles *Grensesnitt for materialhåndteringsutstyr*.
3. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
5. Utvid **Handel \> Lager- og transportstyring**, og merk deretter av for **Grensesnitt for materialhåndteringsutstyr**.
6. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>Angi MHAX-parametere

Du må definere noen generelle parametere på siden **Parametere for grensesnitt for materialhåndteringsutstyr** for å konfigurere funksjonen.

1. Gå til **Grensesnitt for materialhåndteringsutstyr \> Oppsett \> Parametere for grensesnitt for materialhåndteringsutstyr**.
2. Angi følgende felt i fanen **Generelt**:

    - **Bruker-ID** – Velg en arbeider. Denne arbeideren vil bli brukt til å kjøre alle arbeidsoperasjoner (plukkinger og plasseringer) som behandles via den innkommende køen.
    - **Aktiver innkommende meldings-ID** – Når dette alternativet er satt til *Ja*, og hvis en duplikat av innkommende meldings-ID mottas, vil meldingen avvises, og en feilmelding vil angi at meldingen allerede finnes. Hvis du setter alternativet til *Nei*, vil dupliserte innkommende meldings-ID-er være tillatt.

3. I fanen **Nummerserier** velger du nummerseriene som skal brukes til å generere unike ID-er for varer i innkommende kø, varer i utgående kø og arbeidslinjepar.

## <a name="outbound-events"></a>Utgående hendelser

På bestemte punkter under oppretting eller utføring av arbeidsprosesser bestemmer systemet om det må generere utgående hendelser som skal sendes til MH-systemet. Hvis et abonnement er konfigurert for et bestemt punkt under lagerbehandling, genererer systemet hendelsen i henhold til oppsettet for abonnementet.

### <a name="structure-of-outbound-events"></a>Struktur for utgående hendelser

Hver utgående hendelse identifiseres entydig av en utgående kø-ID. Den utgående transaksjonstypen bestemmer hendelsestypen. Lageret og ID-en for abonnementet som genererte hendelsen, registreres også på hendelsen.

Hvis du vil videresende data til MH-systemet, inneholder den utgående hendelsen 10 felt for data (**data01** til **data10**). Disse datafeltene har en 1-1-tilordning (1:1) til eksisterende databasefelt. Spesielt blir de hentet fra felt i arbeidslinjen og arbeidshodetabeller. Feltene kan velges fritt. Du definerer dem når du oppretter abonnementet.

I tillegg til de 10 datafeltene som har 1:1-tilordning til eksisterende databasefelt, kan hendelsen inneholde et ekstra datafelt som kalles *nyttelast*. Innholdet i dette feltet genereres av egendefinert X++-kode som er kjent som en *nyttelastgenerator*. Alle nyttelastgeneratorer som skal brukes, defineres i abonnementet.

For å sikre at MH-systemet bare mottar hver utgående kø-ID én gang, brukes et statusfelt til å angi om en hendelse er klar til å sendes til det eksterne systemet, eller om den allerede er sendt.

### <a name="outbound-queue-subscriptions"></a>Abonnementer for utgående kø

Før det genereres hendelser, må det konfigureres et abonnement til å gi MHAX-funksjonen informasjon om og hvordan hendelser skal genereres. Genererte hendelser merkes av abonnements-ID-en. Derfor kan flere MH-systemer koble seg til det samme WMS-systemet, men holde hendelsene separate. Når MHAX-tjenesten spørres om nye hendelser, er et abonnement et av de tilgjengelige alternativene for å hente hendelsene.

Hvis du vil opprette et abonnement, kan du gå til **Grensesnitt for materialhåndteringsutstyr \> Oppsett \> Abonnementer**. Følgende parametere er tilgjengelige for hvert abonnement:

- **Abonnements-ID** – Et unikt navn som identifiserer abonnementet.
- **Beskrivelse** – En fritekstbeskrivelse av abonnementet.
- **Lager** – De bestemte lagrene som hendelsene skal filtreres etter.
- **Utgående transaksjonstype** – Hendelsestypen som abonnementet skal inneholde.
- **Nyttelastgenerator** – En valgfri kodetype som kan angi tilleggsinformasjon i feltet **Nyttelast** for den utgående hendelsen.

En spørring kan knyttes til hvert abonnement. Denne spørringen filtrerer arbeidslinjer og -hoder for å begrense arbeidet som vil bruke abonnementet til å generere hendelser, ytterligere. Hvis du vil legge til en spørring i et abonnement, merker du av for **Kjør spørring** for det relevante abonnementet på siden **Abonnementer**, og deretter velger du **Rediger spørring** i handlingsruten. Standard redigeringsprogram for Supply Chain Management vises.

I tillegg inneholder abonnementet en *abonnementstilordning* som tilordner felt fra arbeidshodet eller arbeidslinjen til noen av eller alle de 10 gratisdatafeltene for den utgående hendelsen etter behov. Hvis du vil returnere informasjon til MHAX-tjenesten, inkluderer du vanligvis arbeidslinjepost-ID-en eller *IDen for arbeidslinjepar*. (ID-en for arbeidslinjeparet er en ny egenskap som gjør at systemet kan bruke en enkelt returkommando til å behandle plukkings- og plasseringslinjer.) De gjenværende feltene er avhengige av bruken av store og små bokstaver. Det finnes noen eksempler senere i dette emnet.

Hvis du vil definere et abonnementstilordning, velger du det relevante abonnementet på siden **Abonnementer**, og deretter velger du **Abonnementstilordning** på handlingssiden. I dialogboksen **Abonnementstilordning** som vises, kan du tilordne en tabell og et felt for hvert tilgjengelige datafelt etter behov.

### <a name="outbound-event-types"></a>Utgående hendelsestyper

Denne delen beskriver de forskjellige hendelsestypene som er tilgjengelige. (Hendelsestyper kalles også *transaksjonstyper*.) Det forklarer også når hver hendelsestype opprettes i WMS-systemet.

#### <a name="work-creation-events"></a>Hendelser for arbeidsoppretting

Arbeidsopprettingshendelser opprettes etter at arbeid er generert av appen. Denne virkemåten gjelder for de fleste typer arbeidsopprettingsprosesser, spesielt for oppretting av plukk- og etterfyllingsarbeid. Hvis arbeid opprettes i statusen *Åpen*, som angir at arbeidet er klart til å kjøres av en arbeider, genereres det vanligvis en arbeidsopprettingshendelse. I tillegg genereres det hendelser for arbeidsoppretting for grunnleggende bevegelsesarbeid (ikke bevegelse etter malarbeid), selv om arbeidsforløpet ikke er opprettet som åpent arbeid.

Et merkbart unntak til denne virkemåten er syklustellingsarbeid, som for øyeblikket ikke har støtte for funksjonalitet. Lagertellinger i MH-systemet er utenfor MHAX-området, og resultatene av opptellinger må importeres til en lageropptellingsjournal.

Når arbeidet er opprettet, behandler MHAX-tjenesten arbeidslinjene som genereres, og tilordner en ID for arbeidslinjepar til alle genererte arbeidslinjer for hvert arbeidshode. Målsettingen er å gruppere alle plukkarbeidslinjene med de etterfølgende plassert under én ID for arbeidslinjepar. (Gruppene tilsvarer plukkings-/plasseringspar i arbeidsmaler.) På denne måten kan én ID brukes til å rapportere fullføring av arbeid for alle relaterte plukk- og plasseringslinjer. Grupperingsprosessen starter med den første linjen, og fortsetter deretter med den samme ID-en til den får et etterfølgende par med arbeidslinjer for plassert/plukking. Den kjørende ID-en tilordnes til den plasserte linjen i dette paret. En ny ID som deretter brukes for plukklinjen til paret videre. Denne prosessen fortsetter til den har behandlet alle linjer som tilhører arbeidshodet.

Som en spesiell funksjon for opprettingshendelser, vil hendelsene som genereres, ha statusen *Blokkert* i stedet for den vanlige statusen *Klar*, som brukes til å sende dem til MH-systemet, hvis alternativet **Blokkert bølge** er satt til *Ja* i arbeidshodet. Flagget **Blokkert bølge** i arbeidshodet angir at arbeidshodet ennå ikke er klart til å kjøres av arbeidere, kanskje på grunn av uferdig etterfyllingsarbeid. Når merket er fjernet for flagget **Sperret bølge**, oppheves blokkering av hendelser som allerede er generert, og de er tilgjengelige for MH-systemet for å hente fra køen.

#### <a name="work-initiation-events"></a>Hendelser for arbeidsstart

Arbeidsstartshendelser utløses når arbeidsstatusen endres fra *Åpen* til *Pågår* under en arbeidsoppdatering.

#### <a name="work-completion-events"></a>Hendelser for arbeidsfullføring

Arbeidsfullføringshendelser utløses når arbeidsstatusen endres fra *Pågår* til *Lukket* under en arbeidsoppdatering.

#### <a name="work-cancellation-events"></a>Hendelser for arbeidsannullering

Arbeidsannulleringshendelser utløses når arbeidsstatusen endres fra alle stautser bortsett fra *Annullert*, til *Annullert* under en arbeidsoppdatering. I tillegg slettes alle andre hendelser som er relatert til arbeidshodet, fra køen for alle abonnementer. På denne måten hindres eksterne systemer i å behandle hendelser som ikke kreves.

#### <a name="pickput-completion-events"></a>Fullføringshendelser for plukking/plassering

Fullføringshendelser for plukking/plassering utløses når statusen for plukkings-/plasseringslinjen endres fra *Pågår* til *Lukket* under en arbeidslinjeoppdatering.

### <a name="monitor-the-outbound-queue"></a>Overvåke den utgående køen

Hvis du vil gå gjennom den utgående køen, går du til **Grensesnitt for materialhåndteringsutstyr \> Felles \> Utgående kø**. Siden **Utgående kø** viser alle utgående køvarer og statusen til køen. Velg en køvare for å vise detaljene. Disse detaljene omfatter varens transaksjonstype, abonnementet den brukte, og verdier for hvert datafelt (**data01** via **data10**) og nyttelasten.

### <a name="clean-up-the-outbound-queue"></a>Rydde i utgående kø

Til slutt vil den utgående køen bli full av køvarer som allerede er sendt. Hvis du vil fjerne disse varene, kan du gå til **Grensesnitt for materialhåndteringsutstyr \> Periodiske oppgaver \> Opprydding \> Rydde i utgående kø**.

## <a name="inbound-events"></a>Innkommende hendelser

Denne delen beskriver de forskjellige typene innkommende hendelser som MH-systemet kan rapportere tilbake til WMS-systemet. Det forklarer også at data må leveres av MH-systemet, og hva hver innkommende hendelse gjør i WMS-systemet.

### <a name="structure-of-inbound-events"></a>Struktur for innkommende hendelser

Når en innkommende hendelse sendes, må det eksterne systemet forsyne den innkommende transaksjonstypen sammen med opptil 10 parametere (**data01** til **data10**). Valgfri validering kan sikre at MHAX-tjenesten ikke har mottatt den samme innkommende hendelsen mer enn én gang. For at denne valideringen skal kunne aktiveres, må hver innkommende hendelse ha en unik meldings-ID. Hvis det mottas en duplikat meldings-ID, og hvis alternativet **Aktiver innkommende meldings-ID** er satt til *Ja* på siden **Parametere for grensesnitt for materialhåndteringsutstyr**, avvises meldingen. En feilmelding vil si at meldingen allerede finnes.

I tillegg til de innkommende datafeltene tilordner systemet en unik ID for innkommende kø til hendelsen.

### <a name="inbound-event-types"></a>Innkommende hendelsestyper

Denne delen beskriver innkommende hendelsestyper (transaksjonstyper) som støttes, og dataene som må angis for at hendelser skal behandles.

#### <a name="work-confirm-events"></a>Hendelser for arbeidsbekrefelse

Hendelser for arbeidsbekreftelse krever at de innkommende datafeltene inneholder følgende informasjon:

- **data01** – ID-en for arbeidslinjeparet.
- **data02** – ID-en for arbeidslinjepost (`RecId`-verdi).

    > [!NOTE]
    > *Enten* feltet **data01** *eller* feltet **data02** må være til stede.

- **data03** – ID-en til nummerskiltet det skal plukkes fra.
- **data04** – ID-en for arbeidshodets målnummerskilt.

Hvis ID-en for arbeidslinjeparet er angitt, kjøres alle plukkings, plasserings- eller tilpassingarbeidslinjer som er merket av ID-en for arbeidslinjepar, og som har statusen *Åpen* eller *Pågår*, sekvensielt. Hvis det finnes en ID for en arbeidslinjepost (`RecId`-verdi), må arbeidslinjen være en plukkings-, plasserings- eller tilpassingsarbeidslinje med statusen *Åpen* eller *Pågår*.

Plukkingslinjer fra lisenskontrollerte lokasjoner krever at **data03** angir nummerskiltet det skal plukkes fra, uansett om linjene er merket av ID-en for arbeidslinjepost eller ID-en for arbeidslinjepar. Feltet **data04** må angi arbeidshodets målnummerskilt for plukkingen.

Plasseringslinjer godtar ikke mer informasjon. De kjøres bare basert på den gjeldende arbeidslinjens lokasjon og arbeidets målnummerskilt. Hvis plasseringen må gjøres på et annet sted, endrer du stedet for arbeidslinjen som beskrevet i delen [Overstyr hendelser](#override-events) senere i dette emnet.

Egendefinerte arbeidslinjer krever, eller støtter, ikke eventuell tilleggsinformasjon i den innkommende hendelsen.

#### <a name="short-pick-events"></a>Hendelser for plukk med mangler

Hendelser for plukk med mangler krever at de innkommende datafeltene inneholder følgende informasjon:

- **data02** – ID-en for arbeidspost (`RecId`-verdi).
- **data03** – ID-en til nummerskiltet det skal plukkes fra.
- **data04** – Antallet som skal plukkes.
- **data05** – Unntakskoden for plukkingen med mangler.
- **data06** – ID-en for arbeidshodets målnummerskilt.

> [!NOTE]
> Feltet **data01** brukes ikke til plukkinger med mangler.

Denne hendelsen likner på arbeidsbekreftelseshendelsen, men gjelder bare for plukklinjer.

#### <a name="override-events"></a><a id="override-events"></a>Overstyring av hendelser

Overstyring av hendelser krever at de innkommende datafeltene inneholder følgende informasjon:

- **data01** – ID-en for arbeidspost (`RecId`-verdi).
- **data02** – Den nye lokasjons-ID-en.

Arbeidslinjen må ha statusen *Åpen* eller *Pågår*, og den nye lokasjonen må finnes.

#### <a name="license-plate-receipt-events"></a>Mottakshendelser for nummerskilt

Mottakshendelser for nummerskilt krever at de innkommende datafeltene inneholder følgende informasjon:

- **data01** – ID-en til det innkommende nummerskiltet som skal mottas.

Systemet utfører en lisensmottaksoperasjon, basert på lisensen som sendes inn som verdien for feltet **data01**.

### <a name="monitor-the-inbound-queue"></a>Overvåke den innkommende køen

Hvis du vil gå gjennom den innkommende køen, går du til **Grensesnitt for materialhåndteringsutstyr \> Felles \> Innkommende kø**. Siden **Innkommende kø** viser alle innkommende køvarer og statusen til køen. Velg en køvare for å vise detaljene. Disse detaljene omfatter varens transaksjonstype, meldings-ID-en og verdier for hvert datafelt (**data01** via **data10**).

Hvis det oppstod en feil eller en annen type loggelement da innkommende hendelser ble behandlet, kan du kontrollere loggen ved å velge **Feillogg** i handlingsruten.

### <a name="inbound-event-processing"></a>Behandling av innkommende hendelse

Innkommende hendelser skrives først til databasen, og kjøres deretter umiddelbart (synkront). Hvis det oppstår en feil under behandling, skrives hendelsen fremdeles til køen, men statusen er satt til *Feil*. MHAX-tjenesten returnerer en feilmelding til MH-systemet, og lagrer feilloggen i den innkommende hendelsesposten for senere undersøkelse.

Hendelser som har statusen *Feil*, kan behandes på nytt senere hvis feilbetingelsen er fast. Gjør følgende for å behandle feilene på nytt:

- Gå til **Grensesnitt for materialhåndteringsutstyr \> Felles \> Innkommende kø**. Velg den relevante innkommende køen, og velg deretter **Behandle på nytt** i handlingsruten.
- Gå til **Grensesnitt for materialhåndteringsutstyr \> Felles \> Behandle innkommende kø med feil på nytt**. En standard dialogboks for satsvis jobb vises. Der kan du definere et postfilter, og planlegge eller kjøre en satsvis jobb for å behandling av køen på nytt.

Alle arbeidsoperasjoner (plukkinger og plasseringer) kjøres ved å bruke arbeideren som er valgt i feltet **Bruker-ID** på siden **Parametere for grensesnitt for materialhåndteringsutstyr**.

### <a name="clean-up-the-inbound-queue"></a>Rydde i innkommende kø

Til slutt vil den innkommende køen bli full av køvarer som allerede er behandlet. Hvis du vil fjerne disse varene, kan du gå til **Grensesnitt for materialhåndteringsutstyr \> Periodiske oppgaver \> Opprydding \> Rydde i innkommende kø**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Få en rask oversikt ved hjelp av købehandlingen

Hvis du vil ha en rask oversikt over all aktiviteten som er relatert til innkommende og utgående køer, kan du gå til **Grensesnitt for materialhåndteringsutstyr \> Arbeidsområder \> Købehandling**. Siden **Købehandling** inneholder et sett med faner og fliser du kan bruke til å overvåke og utforske køene. Siden inneholder også nyttige koblinger til de fleste av de andre sidene som er nevnt i dette emnet.

## <a name="connect-to-the-mhax-service"></a>Koble til MHAX-tjenesten

MHAX blir implementert som en egendefinert tjeneste. Derfor er den tilgjengelig via SOAP- og REST-kall. Her er adressene til SOAP- og REST-endepunktene:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Hente meldinger fra utgående kø

Bruk en av følgende metoder for å hente meldinger fra den utgående køen:

- Bruk `readOutboundSubscriptionQueue` til å hente hendelsene basert på abonnements-ID-en.
- Bruk `readOutboundWarehouseQueue` til å hente hendelsene basert på hendelsestypen og lager-ID-en på tvers av flere abonnementer.
