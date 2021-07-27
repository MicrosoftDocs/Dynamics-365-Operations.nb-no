---
title: Fakturaautomatisering for skannede dokumenter
description: Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217c5d6d6df88eccf377fbf604eb0a1eb0ba7c9c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344812"
---
# <a name="invoice-automation-for-scanned-documents"></a>Fakturaautomatisering for skannede dokumenter

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvilke dataenheter som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, inkludert fakturaer med vedlegg.

Organisasjoner som ønsker å strømlinjeforme leverandørprosessene for (AP), identifiserer ofte fakturabehandling som ett av de øverste prosessområdene som bør være mer effektivt. I mange tilfeller setter disse organisasjonene behandling av papirfakturaer ut til en tredjepartsleverandør av tjenester for optisk tegngjenkjenning (OCR). Deretter mottar de maskinlesbare fakturametadata sammen med et skannet bilde av hver faktura. For å få hjelp med automatisering bygges deretter en løsning for den siste delen for å aktivere forbruk av disse artefakterene i faktureringssystemet. Nå er denne automatiseringen for den siste delen aktivert som standard, gjennom en løsning for automatisering av fakturaer.

## <a name="solution-context"></a>Løsningskontekst

Fakturaautomatiseringsløsningen gjør det mulig å bruke et standardgrensesnitt som kan godta fakturametadata for fakturahodet og fakturalinjene, og også vedlegg som gjelder for fakturaen. Eksterne systemer som kan generere artefakter som samsvarer med dette grensesnittet, kan sende feeden for automatisk behandling av fakturaer og vedlegg.

Illustrasjonen nedenfor viser et eksempelscenario for integrasjon der Contoso samarbeider med en OCR-tjenesteleverandør for leverandørfakturabehandling. Contosos leverandører sender fakturaer til tjenesteleverandøren via e-post. Ved hjelp av OCR-behandling genererer tjenesteleverandøren fakturametadata (hode og/eller linjer) og et skannet bilde på fakturaen. Et lag med integrasjon omformer deretter disse artefaktene slik at de kan brukes.

![Eksempelscenario for integrasjon.](media/vendor_invoice_automation_01.png)

Flere varianter av det forrige scenarioet er mulig hvis fakturaintegrasjon er nødvendig. Migrering av data er et annet brukstilfelle der dette grensesnittet kan brukes til å opprette fakturaer og vedlegg.

### <a name="solution-components"></a>Løsningskomponenter

Løsningsavtrykket består av følgende komponenter:

+ Dataenheter for fakturahodet, fakturalinjene og fakturavedlegg
+ Unntaksbehandling for fakturaer
+ Et visningsprogram for vedlegg side ved side i fakturaer

Resten av dette emnet inneholder detaljerte beskrivelser av disse løsningskomponentene.

## <a name="data-entities"></a>Dataenheter

En datapakke er arbeidsenheten som må sendes, slik at fakturahoder, fakturalinjer og fakturavedlegg kan opprettes. Følgende dataenheter brukes for artefaktene som utgjør datapakken:

+ Leverandørfakturahode
+ Leverandørfakturalinje
+ Dokumentvedlegg for leverandørfaktura

Dokumentvedlegg for leverandørfaktura er en ny dataenhet som lanseres som en del av denne funksjonen. Enheten for leverandørfakturahode er blitt endret slik at den støtter vedlegg. Enheten for leverandørfakturalinje er ikke endret for denne funksjonen.

Hvis du vil ha mer informasjon om datapakker, kan du se [Oversikt over databehandling](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). Hvis du vil ha informasjon om hvordan du oppretter datapakker ved hjelp av arbeidsområdet for databehandling, kan du se [Behandle og bruke datapakker i løsningen for Dynamics 365 Finance and Operations-apper](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).

Bruk følgende fremgangsmåte for å raskt generere testdata som inkluderer fakturaer og vedlegg.

1. Logg på forekomsten.
1. Gå til **Leverandører** > **Fakturaer** > **Ventende leverandørfakturaer**.
1. Opprett fakturaer som har linjer og vedlegg.

    > [!NOTE]
    > Vedleggene må være hodevedlegg. Enheten for dokumentvedlegg for leverandørfaktura støtter for øyeblikket ikke linjevedlegg.

1. Åpne arbeidsområdet **Databehandling**.
1. Opprett en eksportjobb som inkluderer enhetene for leverandørfakturahode, leverandørfakturalinje og dokumentvedlegg for leverandørfaktura.
1. Eksporter dataene.
1. Last ned de eksporterte dataene som en pakke. Du kan nå bruke pakken til å importere data til målforekomster for testformål.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Bestemme den juridiske enheten for en faktura

Fakturaer som importeres via datapakker, kan knyttes til den juridiske enheten som de hører til, på to måter:

+ Importjobben som behandler fakturaen, importerer den til det samme firmaet der jobben er planlagt i arbeidsområdet **Databehandling**. Med andre ord bestemmer firmaet for jobben hvilket firma som fakturaen tilhører.
+ Når datapakken som inneholder fakturaer, sendes til Finance, kan oppkalleren (det vil si integrasjonsprogrammet som kjøres utenfor Finance) eksplisitt nevne firma-ID-en i HTTP-forespørselen. I så fall overstyres firmakonteksten der behandlingsjobben kjører i Finance, og fakturaene importeres til firmaet som ble sendt via HTTP-forespørselen.

> [!NOTE]
> Dette er standard virkemåte for databehandling. Det er beskrevet her, i forbindelse med fakturaer, bare å gi komplett informasjon.

## <a name="exception-processing"></a>Behandling av unntak

I situasjoner der leverandørfakturaer kommer til Finance and Operations via integrasjon, må det være enkelt for et teammedlem i leverandører å behandle unntak eller mislykkede fakturaer og opprette ventende fakturaer fra mislykkede fakturaer. Denne unntaksbehandlingen for leverandørfakturaer er nå en del av Finance and Operations.

### <a name="vendor-invoices-that-failed-to-import-list-page"></a>Leverandørfakturaer som ikke kunne importere listeside

Den nye listesiden for fakturaunntak er tilgjengelig på **Leverandører** > **Fakturaer** > **Importfeil** > **Leverandørfakturaer som ikke ble importert**. Denne siden viser alle hodepostene for leverandørfakturaer fra oppsamlingstabellen for dataenheten for leverandørfakturahode. Merk at du kan vise de samme postene fra arbeidsområdet **Dataadministrasjon**. Du kan også utføre de samme handlingene som er angitt i funksjonen for unntaksbehandling, fra arbeidsområdet **Dataadministrasjon**. Funksjonen for unntakshåndtering er optimalisert for en funksjonsbruker, som gjør det enklere å bruke den.

![Side med liste over unntak.](media/vendor_invoice_automation_02.png)

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

Listesiden støtter følgende handlinger:

+ **Rediger** – åpne unntaksposten i redigeringsmodus, slik at du kan løse problemene.
+ **Alternativer** – få tilgang til standardalternativene som er tilgjengelige på listesider. Du kan bruke alternativet **Legg til i arbeidsområde** for å feste unntakslistesiden til arbeidsområdet som en liste eller flis.

### <a name="vendor-invoices-that-failed-to-import-details-page"></a>Leverandørfakturaer som ikke kunne importere detaljside

Når du starter redigeringsmodus, åpnes siden **Leverandørfakturaer som ikke kunne importere detaljer** for fakturaen som har problemer. Hvis det er problemer med en faktura som har et vedlegg, vises ikke vedlegget. Tilknytningen må legges ved fakturaen på nytt.

På siden **Leverandørfakturaer som ikke kunne importere detaljer** kan du opprette en ventende faktura. Når du har løst problemene på en faktura som en del av behandling av et unntak, kan du velge knappen **Opprett ventende faktura** for å opprette den ventende fakturaen. Den ventende fakturaen opprettes i bakgrunnen. 

### <a name="shared-service-vs-organization-based-exception-processing"></a>Unntaksbehandling for delte tjenester i forhold til organisasjonsbasert unntaksbehandling

Unntakslistesiden støtter standard sikkerhetsbegreper som arbeidsområdet **Databehandling** støtter for behandling av oppsamlingsposter. Fakturaimportjobben kan sikres på følgende måter:

+ Etter brukerrolle
+ Etter bruker
+ Etter juridisk enhet

![Importjobb som er sikret etter brukerrolle og juridisk enhet.](media/vendor_invoice_automation_04.png)

Hvis sikkerheten er konfigurert for fakturaimportjobben, bruker unntakslistesiden disse innstillingene. Brukere vil kunne se bare fakturaunntakspostene som dette oppsettet tillater dem å se.

For eksempel har Contoso besluttet å behandle fakturaunntak etter juridisk enhet. Derfor konfigureres sikkerhet på fakturaimportjobben på en slik måte at en bruker i juridisk enhet A bare kan se fakturaunntak i juridisk enhet A, mens en bruker i juridisk enhet B bare kan se fakturaunntak i juridisk enhet B. Dette oppsettet gjør mulig arbeidsdeling for behandlingen av fakturaunntak.

Contoso kan også bestemme å ikke overholder noen sikkerhet, slik at de samme brukerne kan behandle fakturaunntak for alle juridiske enheter. Dette oppsettet gjør et scenario med delte tjenester mulig for behandling av fakturaunntak.

## <a name="side-by-side-attachment-viewer"></a>Et visningsprogram for vedlegg side ved side i fakturaer

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

### <a name="default-attachment"></a>Standardvedlegg

Hvis en leverandørfaktura har mer enn ett vedlegg, kan du angi ett av dokumentene som standardvedlegget på **Vedlegg**-siden. Alternativet **Er standardvedlegg** er et nytt alternativ som ble lagt til som en del av denne funksjonen. Dette alternativet vises også i dataenheten for dokumentvedlegg for leverandørfaktura. Standardvedlegget kan derfor angis via integreringer.

Bare ett dokument kan angis som standardvedlegget. Når du har opprettet et dokument som standardvedlegget, vises det automatisk i visningsprogrammet for vedlegg når fakturaen åpnes. Hvis du ikke angir noe dokument som standardvedlegget, viser ikke visningsprogrammet automatisk noen vedlegg når fakturaen åpnes.

### <a name="showhide-invoice-attachments"></a>Vis/skjul fakturavedlegg

En ny knapp som er tilgjengelig på forespørselssidene **Behandling av unntak**, **Faktura som venter** og **Fakturajournal**, lar deg vise eller skjule visningsprogrammet for vedlegg.

## <a name="security"></a>Sikkerhet

Følgende handlinger i visningsprogrammet for vedlegg styres via rollebasert sikkerhet:

+ Utheving
+ Blokker
+ Merknad

### <a name="pending-vendor-invoices-page"></a>Siden Ventende leverandørfakturaer

Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad:

+ **Vedlikehold leverandørfakturabilde** – denne rettigheten gir lese-/skrivetilgang.
+ **Vis leverandørfakturabilde** – denne rettigheten gir skrivebeskyttet tilgang.

Følgende plikter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:

+ **Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold leverandørfakturabilde er tilordnet til denne plikten.
+ **Forespørsel om leverandørfakturastatus** – Rettigheten Vis leverandørfakturabilde er tilordnet til denne plikten.

Følgende roller gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:

+ **Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.
+ **Regnskapsassistent**, **Regnskapssjef leverandørreskontro**, **Assistent for sentraliserte leverandørbetalinger** og **Leverandørbetalingsassistent** – Plikten Forespørsel om leverandørfakturastatus er tilordnet til disse rollene.

### <a name="vendor-invoice-attachment"></a>Leverandørfakturavedlegg

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]