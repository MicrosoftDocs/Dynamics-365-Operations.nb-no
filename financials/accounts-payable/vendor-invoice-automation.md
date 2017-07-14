---
title: "Automatisering av leverandørfaktura"
description: "Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg."
author: twheeloc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 5bfde00f88a12711c2519aaea19dd7a48196a828
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017

---
# Automatisering av leverandørfaktura
<a id="vendor-invoice-automation" class="xliff"></a>

Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg.

Organisasjoner som ønsker å strømlinjeforme leverandørprosessene for (AP), identifiserer ofte fakturabehandling som ett av de øverste prosessområdene som bør være mer effektivt. I mange tilfeller setter disse organisasjonene behandling av papirfakturaer ut til en tredjepartsleverandør av tjenester for optisk tegngjenkjenning (OCR). Deretter mottar de maskinlesbare fakturametadata sammen med et skannet bilde av hver faktura. For å få hjelp med automatisering bygges deretter en løsning for den siste delen for å aktivere forbruk av disse artefakterene i faktureringssystemet. Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tilbyr nå denne automatiseringen for den siste delen rett fra esken, gjennom en løsning for automatisering av fakturaer.

## Løsningskontekst
<a id="solution-context" class="xliff"></a>

Fakturaautomatiseringsløsningen gjør det mulig å bruke et standardgrensesnitt som kan godta fakturametadata for fakturahodet og fakturalinjene, og også vedlegg som gjelder for fakturaen. Eksterne systemer som kan generere artefakter som samsvarer med dette grensesnittet, kan sende feeden til Finance and Operations for automatisk behandling av fakturaer og vedlegg.

Illustrasjonen nedenfor viser et eksempelscenario for integrasjon der Contoso samarbeider med en OCR-tjenesteleverandør for leverandørfakturabehandling. Contosos leverandører sender fakturaer til tjenesteleverandøren via e-post. Ved hjelp av OCR-behandling genererer tjenesteleverandøren fakturametadata (hode og/eller linjer) og et skannet bilde på fakturaen. Et lag med integrasjon omformer deretter disse artefaktene slik at Finance and Operations kan bruke dem.

![Eksempelscenario for integrasjon](media/vendor_invoice_automation_01.png)

Flere varianter av det forrige scenariet er mulig hvis fakturaintegrasjon er nødvendig. Migrering av data er et annet brukstilfelle der dette grensesnittet kan brukes til å opprette fakturaer og vedlegg i Finance and Operations.

### Løsningskomponenter
<a id="solution-components" class="xliff"></a>

Løsningsavtrykket består av følgende komponenter:

+ Dataenheter for fakturahodet, fakturalinjene og fakturavedlegg
+ Unntaksbehandling for fakturaer
+ Et visningsprogram for vedlegg side ved side i fakturaer

Resten av dette emnet inneholder detaljerte beskrivelser av disse løsningskomponentene.

## Dataenheter
<a id="data-entities" class="xliff"></a>

En datapakke er arbeidsenheten som må sendes til Finance and Operations, slik at fakturahoder, fakturalinjer og fakturavedlegg kan opprettes. Følgende dataenheter brukes for artefaktene som utgjør datapakken:

+ Leverandørfakturahode
+ Leverandørfakturalinje
+ Dokumentvedlegg for leverandørfaktura

Dokumentvedlegg for leverandørfaktura er en ny dataenhet som lanseres som en del av denne funksjonen. Enheten for leverandørfakturahode er blitt endret slik at den støtter vedlegg. Enheten for leverandørfakturalinje er ikke endret for denne funksjonen.

Dette emnet gir ikke en detaljert definisjon av en datapakke. Det forklarer heller ikke hvordan du oppretter datapakker. Hvis du vil ha denne informasjonen, kan du se [Rammeverk for dataenheter og pakker](/dynamics365/en-us/unified-operations/dev-itpro/data-entities/data-entities-data-packages).

Bruk følgende fremgangsmåte for å raskt generere testdata som inkluderer fakturaer og vedlegg.

1. Logg på forekomsten av Finance and Operations.
1. Gå til **Leverandører** > **Fakturaer** > **Ventende leverandørfakturaer**.
1. Opprett fakturaer som har linjer og vedlegg.

    > [!NOTE]
    > Vedleggene må være hodevedlegg. Enheten for dokumentvedlegg for leverandørfaktura støtter for øyeblikket ikke linjevedlegg.

1. Åpne arbeidsområdet **Databehandling**.
1. Opprett en eksportjobb som inkluderer enhetene for leverandørfakturahode, leverandørfakturalinje og dokumentvedlegg for leverandørfaktura.
1. Eksporter dataene.
1. Last ned de eksporterte dataene som en pakke. Du kan nå bruke pakken til å importere data til målforekomster for testformål.

### Bestemme den juridiske enheten for en faktura
<a id="determining-the-legal-entity-for-an-invoice" class="xliff"></a>

Fakturaer som importeres via datapakker, kan knyttes til den juridiske enheten som de hører til, på to måter:

+ Importjobben som behandler fakturaen, importerer den til det samme firmaet der jobben er planlagt i arbeidsområdet **Databehandling**. Med andre ord bestemmer firmaet for jobben hvilket firma som fakturaen tilhører.
+ Når datapakken som inneholder fakturaer, sendes til Finance and Operations, kan oppkalleren (det vil si integrasjonprogrammet som kjøres utenfor Finance and Operations) eksplisitt nevne firma-ID-en i HTTP-forespørselen. I så fall overstyres firmakonteksten der behandlingsjobben kjører i Finance and Operations, og fakturaene importeres til firmaet som ble sendt via HTTP-forespørselen.

> [!NOTE]
> Dette er standard virkemåte for databehandling. Det er beskrevet her, i forbindelse med fakturaer, bare å gi komplett informasjon.

## Behandling av unntak
<a id="exception-processing" class="xliff"></a>

I situasjoner der leverandørfakturaer kommer til Finance and Operations via integrasjon, må det være enkelt for et teammedlem i leverandører å behandle unntak eller mislykkede fakturaer og opprette ventende fakturaer fra mislykkede fakturaer. Denne unntaksbehandlingen for leverandørfakturaer er nå en del av Finance and Operations.

### Side med liste over unntak
<a id="exceptions-list-page" class="xliff"></a>

Den nye listesiden for fakturaunntak er tilgjengelig på **Leverandører** > **Fakturaer** > **Importfeil** > **Leverandørfakturaer som ikke ble importert**. Denne siden viser alle hodepostene for leverandørfakturaer fra oppsamlingstabellen for dataenheten for leverandørfakturahode. Vær oppmerksom på at du kan vise de samme postene fra arbeidsområdet **Databehandling**, der du også kan utføre de samme handlingene som er angitt i funksjonen for unntaksbehandling. Imidlertid er brukergrensesnittet i funksjonen for unntaksbehandling optimalisert for en funksjonell bruker.

![Side med liste over unntak](media/vendor_invoice_automation_02.png)

Denne listesiden inneholder følgende felt som kommer inn via feeden:

+ **Firma** – firmaet som fakturaen tilhører
+ **Feilmelding** – feilmeldingen som rammeverket for databehandling utsteder for å forklare hvorfor fakturaen ikke kan opprettes
+ **Nummer** – fakturanummeret
+ **Fakturakonto**
+ **Navn** – leverandørens navn
+ **Leverandørkonto**
+ **Bestilling** – bestillingsnummeret for fakturaen
+ **Posteringsdato**
+ **Fakturadato**
+ **Fakturabeskrivelse**
+ **Valuta**
+ **Logg**
+ **Linjereferanse** – identifikatoren som kommer fra det eksterne systemet

    > [!NOTE]
    > Linjereferansen ikke er IDen for fakturaen.

Denne listesiden har også en forhåndsvisningsrute som kan brukes på følgende måter:

+ Vis hele feilmeldingen, slik at du ikke trenger å utvide **Feilmelding**-kolonnen i rutenettet.
+ Vis hele listen over vedlegg for fakturaen, hvis vedlegg fulgte med fakturaen.

Listesiden støtter følgende handlinger:

+ **Rediger** – åpne unntaksposten i redigeringsmodus, slik at du kan løse problemene.
+ **Alternativer** – få tilgang til standardalternativene som er tilgjengelige på listesider. Du kan bruke alternativet **Legg til i arbeidsområde** for å feste unntakslistesiden til arbeidsområdet som en liste eller flis.

### Side for unntaksdetaljer
<a id="exception-details-page" class="xliff"></a>

Når du starter redigeringsmodus, vises siden for unntaksdetaljer for fakturaen som har problemer. Hvis det ikke finnes vedlegg, vises fakturaen og standardvedlegget side ved side på siden for unntaksdetaljer.

![Side for unntaksdetaljer](media/vendor_invoice_automation_03.png)

I den forrige illustrasjonen var det ikke noen linjer for leverandørfakturahodet som kom inn. Linjedelen er derfor tom.

Siden for unntaksdetaljer støtter følgende operasjon:

+ **Opprett ventende faktura** – Når du har løst problemene på fakturaen som en del av behandling av unntak, kan du klikke denne knappen for å opprette den ventende fakturaen. Opprettelse av ventende fakturaer skjer i bakgrunnen (som en asynkron operasjon).

### Unntaksbehandling for delte tjenester i forhold til organisasjonsbasert unntaksbehandling
<a id="shared-service-vs-organization-based-exception-processing" class="xliff"></a>

Unntakslistesiden støtter standard sikkerhetsbegreper som arbeidsområdet **Databehandling** støtter for behandling av oppsamlingsposter. Fakturaimportjobben kan sikres på følgende måter:

+ Etter brukerrolle
+ Etter bruker
+ Etter juridisk enhet

![Importjobb som er sikret etter brukerrolle og juridisk enhet](media/vendor_invoice_automation_04.png)

Hvis sikkerheten er konfigurert for fakturaimportjobben, bruker unntakslistesiden disse innstillingene. Brukere vil kunne se bare fakturaunntakspostene som dette oppsettet tillater dem å se.

For eksempel har Contoso besluttet å behandle fakturaunntak etter juridisk enhet. Derfor konfigureres sikkerhet på fakturaimportjobben på en slik måte at en bruker i juridisk enhet A bare kan se fakturaunntak i juridisk enhet A, mens en bruker i juridisk enhet B bare kan se fakturaunntak i juridisk enhet B. Dette oppsettet gjør mulig arbeidsdeling for behandlingen av fakturaunntak.

Contoso kan også bestemme å ikke overholder noen sikkerhet, slik at de samme brukerne kan behandle fakturaunntak for alle juridiske enheter. Dette oppsettet gjør et scenario med delte tjenester mulig for behandling av fakturaunntak.

## Et visningsprogram for vedlegg side ved side i fakturaer
<a id="side-by-side-attachment-viewer" class="xliff"></a>

For å hjelpe deg med å vise vedlegg for leverandørfakturaer, gir følgende sider som skal brukes i faktureringsprosessen, nå et visningsprogram for vedlegg:

+ **Unntaksbehandling**
+ **Ventende leverandørfakturaer**-siden (også tilgjengelig i fakturavurderingsprosessen)
+ **Fakturajournal**-forespørselssiden (for posterte fakturaer)

Her er den viktigste funksjonaliteten som visningsprogrammet for vedlegg inneholder:

+ Vis alle vedleggstyper som dokumentbehandling støtter (filer, bilder, URL-adresser og merknader).
+ Vis TIFF-filer med flere sider.
+ Utfør følgende handlnger med bildefiler:
  + Uthev deler av bildet.
  + Blokker deler av bildet.
  + Legg til merknader i bildet.
  + Zoom inn og ut på bildet.
  + Panorer bildet.
  + Angre og gjør om handlinger.
  + Tilpass bildet til størrelse.

> [!NOTE]
> Disse handlingene er tilgjengelig bare for bildefiler (JPEG, TIFF, PNG og så videre). Eventuelle endringer du gjør et bilde ved hjelp av disse handlingene lagres i bildefilen. For øyeblikket inkluderer ikke visningsprogrammet for vedlegg funksjoner for versjonskontroll eller overvåking.

### Standardvedlegg
<a id="default-attachment" class="xliff"></a>

Hvis en leverandørfaktura har mer enn ett vedlegg, kan du angi ett av dokumentene som standardvedlegget på **Vedlegg**-siden. Alternativet **Er standardvedlegg** er et nytt alternativ som ble lagt til som en del av denne funksjonen. Dette alternativet vises også i dataenheten for dokumentvedlegg for leverandørfaktura. Standardvedlegget kan derfor angis via integreringer.

Bare ett dokument kan angis som standardvedlegget. Når du har opprettet et dokument som standardvedlegget, vises det automatisk i visningsprogrammet for vedlegg når fakturaen åpnes. Hvis du ikke angir noe dokument som standardvedlegget, viser ikke visningsprogrammet automatisk noen vedlegg når fakturaen åpnes.

### Vis/skjul fakturavedlegg
<a id="showhide-invoice-attachments" class="xliff"></a>

En ny knapp som er tilgjengelig på forespørselssidene **Behandling av unntak**, **Faktura som venter** og **Fakturajournal**, lar deg vise eller skjule visningsprogrammet for vedlegg.

### Sikkerhet
<a id="security" class="xliff"></a>

Følgende handlinger i visningsprogrammet for vedlegg styres via rollebasert sikkerhet:

+ Utheving
+ Blokker
+ Merknad

### Siden Ventende leverandørfakturaer
<a id="pending-vendor-invoices-page" class="xliff"></a>

Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad:

+ **Vedlikehold leverandørfakturabilde** – denne rettigheten gir lese-/skrivetilgang.
+ **Vis leverandørfakturabilde** – denne rettigheten gir skrivebeskyttet tilgang.

Følgende plikter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:

+ **Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold leverandørfakturabilde er tilordnet til denne plikten.
+ **Forespørsel om leverandørfakturastatus** – Rettigheten Vis leverandørfakturabilde er tilordnet til denne plikten.

Følgende roller gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:

+ **Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.
+ **Regnskapsassistent**, **Regnskapssjef leverandørreskontro**, **Assistent for sentraliserte leverandørbetalinger** og **Leverandørbetalingsassistent** – Plikten Forespørsel om leverandørfakturastatus er tilordnet til disse rollene.

### Side for fakturaunntaksdetaljer
<a id="invoice-exception-details-page" class="xliff"></a>

Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad.

> [!NOTE]
> Rett fra esken gir rollene som er nevnt i denne delen, skrivebeskyttet tilgang til fakturabildene i visningsprogrammet for vedlegg. Hvis en rolle også må ha skrivetilgang til bildene, kan du gi skrivetilgang til denne rollen ved hjelp av rettigheten og plikten som er beskrevet her.

+ **Vedlikehold bilde for enhet for leverandørfakturahode** – Denne rettigheten gir lese-/skrivetilgang til fakturabildene i visningsprogrammet for vedlegg.
+ **Vis bilde for enhet for leverandørfakturahode** – Denne rettigheten gir skrivebeskyttet visning av fakturabildet i visningsprogrammet for vedlegg.

Følgende plikter gir skrivebeskyttet tilgang eller til visningsprogrammet for vedlegg for disse handlingene:

+ **Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold bilde for enhet for leverandørfakturahode er tilordnet til denne plikten.

Følgende roller gir skrivebeskyttet tilgang eller til visningsprogrammet for vedlegg for disse handlingene:

+ **Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.

Hvis brukerrollen har redigeringsrettigheter på en side, har brukeren som standard også redigeringsrettigheter på visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknader. Hvis det finnes situasjoner der en bestemt rolle skal ha redigeringsrettigheter på siden, men ikke på visningsprogrammet for vedlegg, kan imidlertid de nødvendige rettighetene i listen ovenfor brukes til å dekke brukstilfellet.

