---
title: Oversikt over elektronisk rapportering (ER)
description: Dette emnet gir en oversikt over verktøyet for Elektronisk rapportering. Det beskriver nøkkelbegreper, scenarioer som støttes, og formater som er en del av løsningen.
author: NickSelin
ms.date: 11/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b772acd4a8d0849803cefa8fc14ae3dd6e18831
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867303"
---
# <a name="electronic-reporting-er-overview"></a>Oversikt over elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over verktøyet for elektronisk rapportering (ER). Den inneholder informasjon om viktige konsepter, hvilke scenarioer ER støtter, samt en liste over formater som er utviklet og lansert som en del av ER-løsningen.

ER er et konfigurerbart verktøy som hjelper deg med å opprette og vedlikeholde forskriftsmessige elektroniske rapporteringer og betalinger. Den er basert på følgende tre begreper:

- Konfigurasjon i stedet for koding:

    - Konfigurasjoner kan utføres av en forretningsbruker og krever ikke en utvikler.
    - Datamodellen er definert i forretningstermer.
    - Visuelle redigeringsverktøy brukes til å opprette alle komponenter i ER-konfigurasjonen.
    - Språket som brukes i datatransformeringen, ligner på språket som brukes i Microsoft Excel.

- Én konfigurasjon for flere Dynamics 365 Finance-versjoner:

    - Behandle en domenespesifikk datamodell som er definert i forretningsbetingelser.
    - Isoler programversjonsdetaljer i frigivelsesavhengige datamodelltilordninger.
    - Vedlikehold én formatkonfigurasjon for flere versjoner av den gjeldende versjonen, basert på datamodellen.

- Enkel eller automatisk oppgradering:

    - Versjonskontroll av ER-konfigurasjoner støttes.
    - Microsoft Dynamics Lifecycle Services (LCS) Assets-bibliotek kan brukes som et repositorium for ER-konfigurasjoner for versjonsutveksling.
    - Lokalisering som er basert på opprinnelige ER-konfigurasjoner, kan innføres som underordnede versjoner.
    - Et ER-konfigurasjonstre leveres som et verktøy som hjelper til med å kontrollere avhengigheter for versjoner.
    - Forskjeller i lokalisering, eller deltakonfigurasjonen, registreres for å aktivere automatisk oppgradering til en ny versjon av den opprinnelige ER-konfigurasjonen.
    - Det er enkelt å løse konflikter som blir oppdaget ved automatisk oppgradering av lokaliseringsversjoner, manuelt.

Med ER-verktøyet kan du definere elektroniske formatstrukturer og deretter beskrive hvordan disse strukturene skal fylles, ved å bruke data og algoritmer. Du kan bruke et formelspråk som ligner på Excel-språket for datatransformasjon. Det introduseres et mellomliggende datamodellkonsept for å gjøre tilordningen fra database til format mer håndterbar, gjenbrukbar og uavhengig av formatendringer. Dette konseptet gjør at implementeringsdetaljer kan skjules fra formattilordningen, og gjør det mulig å bruke en enkelt datamodell på nytt for tilordning av flere formater.

Du kan bruke ER til å konfigurere formater for både innkommende og utgående elektroniske dokumenter i overensstemmelse med de juridiske kravene for ulike land og områder. ER lar deg administrere disse formatene i deres livssyklus. Du kan for eksempel innføre nye lovbestemte krav, og generere forretningsdokumenter i det riktige formatet for elektronisk utveksling av informasjon med statlige instanser, banker og andre parter.

ER-motoren er rettet mot bedriftsbrukere i stedet for utviklere. Siden du konfigurere formater, i stedet for kode, er prosessene for å opprette og justere formater for elektroniske dokumenter raskere og enklere.

ER støtter TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel og OPENXML-regnearkformatene.

## <a name="capabilities"></a>Muligheter

ER-motoren har følgende funksjoner:

- Den representerer ett felles verktøy for elektronisk rapportering i forskjellige områder, og erstatter mer enn 20 forskjellige motorer som utfører en slags elektronisk rapportering i Finance and Operations.
- Den isolerer rapportformatet fra gjeldende implementering. Med andre ord, formatet kan brukes for ulike versjoner.
- Den støtter oppretting av et tilpasset format som er basert på et opprinnelig format. Den inkluderer også funksjoner for å automatisk oppgradere det egendefinerte formatet når det opprinnelige formatet endres på grunn av krav til lokalisering/tilpassing.
- Den blir det primære standardverktøyet for å støtte for lokaliseringskrav i elektronisk rapportering, både for Microsoft og Microsoft-partnere.
- Den støtter muligheten til å distribuerte formater til partnere og kunder via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Nøkkelbegreper

### <a name="main-data-flow"></a>Hoveddataflyt

[![ER-hoveddataflyt.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Komponenter

ER støtter følgende typer komponenter:

- Datamodell
- Modelltilordning
- Format
- Metadata

For mer informasjon, se [Komponenter i elektronisk rapportering](er-overview-components.md).


#### <a name="component-versioning"></a>Versjonskontroll av komponenter

Versjonskontroll støttes for ER-komponenter. Følgende arbeidsflyt leveres for å behandle endringer i ER-komponenter:

1. Versjonen som opprinnelig opprettes, er merket som en **Utkast**-versjon. Denne versjonen kan redigeres og er tilgjengelig for testkjøringer.
2. **Utkast**-versjonen kan konverteres til en **Fullført**-versjon. Denne versjonen kan brukes i lokale rapporteringsprosesser.
3. **Fullført**-versjonen kan konverteres til en **Delt**-versjon. Denne versjonen er publisert på LCS og kan brukes i globale rapporteringsprosesser.
4. **Delt**-versjonen kan konverteres til en **Avsluttet**-versjon. Denne versjonen kan deretter slettes.

Versjoner som har statusen **Fullført** eller **Delt**, er tilgjengelig for annen datautveksling. Følgende handlinger kan utføres på en komponent som har disse statusene:

- Komponenten kan serialiseres i XML-format og eksporteres som en fil i XML-format.
- Komponenten kan serialiseres på nytt fra en XML-fil og importeres til programmet som en ny versjon av en ER-komponent.

#### <a name="component-date-effectivity"></a>Datogyldighet for komponent

ER-komponentversjoner har datogyldighet. Du kan angi **Gyldig fra**-datoen for en ER-komponent for å angi startdatoen som komponenten er gyldig fra for rapporteringsprosesser. Øktdatoen for programmet brukes for å definere om en komponent er gyldig for kjøring. Hvis flere enn én versjon er gyldig for en bestemt dato, brukes den nyeste versjonen for rapporteringsprosessen.

#### <a name="component-access"></a>Komponenttilgang

Tilgang til ER-formatkomponenter avhenger av innstillingen for ISO-kode for land/område. Når denne innstillingen er tom for en valgt versjon av en formatkonfigurasjon, er en formatkomponent tilgjengelig fra et firma ved kjøretid. Når denne innstillingen inneholder ISO-koder for land/område, er en formatkomponent bare tilgjengelig fra firmaene som har en primæradresse som er definert for én av ISO-kodene for land/område for formatkomponenten.

Forskjellige versjoner av en dataformatkomponent kan ha ulike innstillinger for ISO-koder for land/område.

#### <a name="configuration"></a><a name="Configuration"></a>Konfigurasjon

En ER-konfigurasjon ER er hylsteret til for en bestemt ER-komponent. Den komponenten kan være enten en datamodellkomponent eller en formatkomponent. En konfigurasjon kan inneholde forskjellige versjoner av en ER-komponent. Hver konfigurasjon er merket som eid av en bestemt konfigurasjonsleverandør. **Utkast**-versjonen av en komponent i en konfigurasjon kan redigeres når eieren av konfigurasjonen er valgt som en aktive leverandør i ER-innstillingene i programmet.

Hver modellkonfigurasjon inneholder en datamodellkomponent. En ny formatkonfigurasjon kan utledes fra en bestemt datamodellkonfigurasjon. I konfigurasjonstreet vises formatkonfigurasjonen som opprettes, som et underordnet element av den opprinnelige datamodellkonfigurasjonen.

Formatkonfigurasjonen som opprettes, inneholder en formatkomponent. Datamodellkomponenten for den opprinnelige modellkonfigurasjonen settes automatisk inn i formatkomponenten for den underordnede formatkonfigurasjonen som standard datakilde.

En ER-konfigurasjon er delt for firmaer i programmet.

#### <a name="provider"></a><a name="Provider"></a>Leverandør

ER-leverandør er parts-ID-en som brukes til å angi forfatteren (eier) av hver ER-konfigurasjon. ER lar deg administrere listen over konfigurasjonsleverandører. Formatkonfigurasjoner som leveres for elektroniske dokumenter som en del av Finance and Operations-løsningen, er merket som eid av konfigurasjonsleverandøren **Microsoft**.

Hvis du vil finne ut hvordan du registrerer en ny ER-leverandør, kan du spille inn oppgaveveiledningen **ER Opprette en konfigurasjonsleverandør og merke den som aktiv** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

#### <a name="repository"></a><a name="Repository"></a>Repositorium

Et ER-repositorium lagrer ER-konfigurasjoner. Følgende typer ER-repositorier støttes: 

- LCS-delt bibliotek
- LCS-prosjekt
- Filsystem
- RCS
- Operations-ressurser
- Globalt repositorium

Et **LCS-delt bibliotek**-repositorium gir tilgang til listen over konfigurasjoner i det delte aktivabiblioteket i Lifecycle Services (LCS). Denne typen ER-repositorium kan bare registreres for Microsoft-leverandøren. Fra det delte LCS-aktivabiblioteket kan du importere den nyeste versjonen av ER-konfigurasjoner til den gjeldende forekomsten.

**LCS-prosjekt**-repositoriet gir tilgang til listen over konfigurasjoner for et bestemt LCS-prosjekt (aktivabibliotek for LCS-prosjekt), som ble valgt under registrering av repositoriet. ER lar deg laste opp delte konfigurasjoner fra gjeldende forekomst til et spesifikt **LCS-prosjekt**-repositorium. Du kan også importere konfigurasjoner fra et **LCS-prosjekt**-repositorium til gjeldende forekomst av Finance and Operations-appene dine.

Et **Filsystem**-repositorium gir tilgang til listen over konfigurasjonene som er lagret som XML-filer i den bestemte mappen på det lokale filsystemet på maskinen som er vert for AOS-tjenesten. Nødvendig mappe blir valgt i fasen for registrering av repositoriet. Du kan importere konfigurasjoner fra et **Filsystem**-repositorium til gjeldende forekomst. 

Legg merke til at denne typen repositorium er tilgjengelig i følgende miljøer:

- Skybaserte miljøer distribuert for utviklingsformål (som inneholder testmodeller av vedlagte serier)
- Lokalt distribuerte miljøer

Hvis du vil ha mer informasjon, kan du se [Importere elektroniske rapporteringskonfigurasjoner](./electronic-reporting-import-ger-configurations.md).

Et **RCS**-repositorium gir tilgang til listen over konfigurasjoner for en bestemt forekomst av [RCS-konfigurasjonstjenesten](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) som ble valgt under registrering av repositoriet. Med ER kan du importere fullførte eller delte konfigurasjoner fra den valgte forekomsten av RCS til den gjeldende forekomsten, slik at du kan bruke dem til elektronisk rapportering.

Hvis du vil ha mer informasjon, kan du se [Importere elektroniske rapporteringskonfigurasjoner fra RCS](./rcs-download-configurations.md).

Et **globalt repositorium** gir tilgang til listen over konfigurasjoner i det globale repositoriet i [konfigurasjonstjenesten](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Denne typen ER-repositorium kan bare registreres for Microsoft-leverandøren. Fra det globale repositoriet kan du importere den nyeste versjonen av ER-konfigurasjoner til den gjeldende forekomsten.

Hvis du vil ha mer informasjon, kan du se [Importere ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](./er-download-configurations-global-repo.md).

Et **Operasjonsressurser**-repositorium gir tilgang til listen over konfigurasjoner som Microsoft, som ER-konfigurasjonsleverandør, opprinnelig gir ut som en del av programløsningen. Disse konfigurasjonene kan importeres til den gjeldende forekomsten og brukes til elektronisk rapportering eller avspilling av eksempeloppgaveveiledninger. De kan også brukes til tilleggslokaliseringer og tilpassinger. Legg merke til at de nyeste versjonene fra Microsoft ER-konfigurasjoner må importeres fra det delte LCS-aktivabiblioteket ved hjelp av det tilsvarende ER-repositoriet.

Nødvendige repositorier for **LCS-prosjekt**, **Filsystem** og **Forskriftsmessig konfigurasjonstjeneste (RCS)** kan registreres individuelt for hver enkelt konfigurasjonsleverandør for gjeldende forekomst. Hvert repositorium kan reserveres for en bestemt konfigurasjonsleverandør.

## <a name="supported-scenarios"></a>Scenarier som støttes

### <a name="building-a-data-model"></a>Bygge en datamodell

ER tilbyr en modellutforming som du kan bruke for å bygge en datamodell for et bestemt forretningsområde. Alle områdespesifikke forretningsenheter og relasjoner mellom dem, kan være representert i en datamodell som en hierarkisk struktur. 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme domenespesifikk datamodell** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="translating-data-model-content"></a>Oversette datamodellinnhold

Datamodellinnhold (etiketter og beskrivelser) kan oversettes til andre språk som programmene støtter. Du vil kanskje oversette datamodellinnhold av følgende årsaker:

- Gjøre innholdet tydeligere under utformingen for formatutviklere som snakker andre3 språk, som skal bruke datamodellen for datatilordning av formatkomponenter.
- Gjøre innholdet mer brukervennlig ved kjøretid ved å presentere spørsmål og hjelp for kjøretidsparameterne, og konfigurerte valideringsmeldinger (feil og advarsler) på foretrukket språk for påloggede brukere.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Konfigurere datamodelltilordninger for utgående dokumenter

ER inneholder en modelltilordningsutforming som lar brukere tilordne datamodeller som de har utformet, til bestemte programdatakilder. Basert på tilordningen, importeres dataene i kjøretid fra valgte datakilder til datamodellen. Datamodellen brukes deretter som en abstrakt datakilde ER-formater som genererer utgående elektroniske dokumenter. 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Definere modelltilordning og velge datakilder** og **ER Tilordningen datamodell til valgte datakilder** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Konfigurere datatilordninger modell for innkommende dokumenter

ER inneholder en modelltilordningsutforming som lar brukere tilordne datamodeller som de har utformet, til bestemte mål. Datamodeller kan for eksempel tilordnes til oppdaterbare datakomponenter (tabeller, data-enheter og visninger). Basert på tilordningen, oppdateres data under kjøring ved hjelp av dataene fra datamodellen. Som abstrakt lagring av ER-formatet, er datamodellen fylt med data som er importert fra et innkommende elektronisk dokument. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Lagre en utformet modellkomponent som en modellkonfigurasjon

ER kan lagre en utformet datamodell sammen med tilknyttede datatilordninger som en modellkonfigurasjon for gjeldende forekomst. Illustrasjonen nedenfor viser et eksempel på denne typen datamodellkonfigurasjon (konfigurasjon for betalingsmodell).

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Tilordningen datamodell til valgte datakilder** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Bygge et format som bruker en datamodell som basis

ER støtter at en formatutforming som du kan bruke til å bygge formatet for et elektronisk dokument for et valgt forretningsområde ved å velge modellkomponenten som basis. Samme ER-formatutforming lar deg tilordne et format som du oppretter for en valgt datamodelltilordning for området som en datakilde. 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme områdespesifikt format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Bygge en konfigurasjon for å generere elektroniske dokumenter i OPENXML-regnearkformat

ER-formatutformingen kan brukes til å bygge et elektronisk dokument i OPENXML-regnearkformat. 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Opprette en konfigurasjon for rapporter i OPENXML-format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) . Som en del av trinnet for import av mal i oppgaveveiledningen, kan du bruke Excel-filen [Mal for betalingsrapport (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) som mal.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Bygge en konfigurasjon for å generere elektroniske dokumenter i et Word-dokumentformat

ER-formatutformingen kan brukes til å bygge et elektronisk dokument i et Word-dokumentformat. Illustrasjonen nedenfor viser et eksempel på denne typen format. Legg merke til at dette formatet bruker den eksisterende ER-konfigurasjonen som opprinnelig ble utformet for å generere rapportutdataene i OPENXML-formatet, på nytt.

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen ER Utforme en konfigurasjon for generering av rapporter i Microsoft WORD (en del av forretningsprosessen 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)) . Som en del av trinnet for import av mal i oppgaveveiledningen, kan du bruke følgende Word-filer som maler for ER-formatet:

- [Mal for betalingsrapport (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Bundet mal for betalingsrappor (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Bygge en konfigurasjon for å importere data fra innkommende elektroniske dokumenter

ER-formatutformingen kan brukes til å beskrive et elektronisk dokument som er planlagt for import av data i enten XML-eller tekstformat. Formatet som uformes, brukes til å analysere et innkommende dokument. Utforming av ER-formattilordning kan brukes til å definere bindingen av elementene i formatet som er utformet, til datamodellen. 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen Opprette nødvendige ER-konfigurasjoner for å importere data fra en ekstern fil (en del av forretningsprosessen 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)) . Bruk følgende filer til å spille av denne håndboken:

- [ER-datamodellkonfigurasjon (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER-formatkonfigurasjon (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Eksempel på innkommende dokument i XML-format (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Eksempel fra arbeidsboken for behandling av data for innkommende dokument (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Lagre en utformet formatkomponent i en formatkonfigurasjon

ER kan lagre et utformet format sammen med de konfigurerte datatilordningene som en formatkonfigurasjon for gjeldende forekomst. Den forrige illustrasjonen viser et eksempel på denne typen formatkonfigurasjon (**BBS (Storbritannia)**, som er underordnet av **Betalingsmodell**-konfigurasjonen). Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme områdespesifikt format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Konfigurere Finance til å begynne å bruke opprettet format internt

Programmet kan konfigureres til å begynne å bruke et opprettet format til å generere elektroniske rapporter. Referansen til den opprettede formatkonfigurasjonen må defineres i innstillingene for et bestemte område. Hvis du for eksempel vil begynne å bruke en ER-formatkonfigurasjon for elektroniske leverandørbetalinger i BBS-format, må formatkonfigurasjonen refereres i bestemte betalingsmåter.

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Bruk format for å generere elektronisk dokument for betaling** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

## <a name="handling-er-components"></a>Behandle ER-komponenter

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Publisere ER-komponent i LCS for å tilby den eksternt (lokalisering)

Eieren av en komponent (modell eller format) som er opprettet, kan bruke ER for å publisere den fullførte versjonen komponenten til LCS. Et repositorium av typen **LCS-prosjekt** for gjeldende ER-konfigurasjonsleverandør er nødvendig. Når statusen for den fullførte versjonen av en komponent endres fra **FULLFØRT** til **DELT**, publiseres denne versjonen i LCS. Når en komponent er publisert til LCS, blir eieren av denne komponenten en leverandør av tjenesten for å støtte komponenten. Hvis formatkomponenten for eksempel er utformet for å generere et juridisk påkrevd elektronisk dokument (for eksempel i henhold til lokaliseringsscenario), antas det at formatet holdes i samsvar med juridiske endringer, og at leverandøren vil utstede nye versjoner av komponenten hver gang nye juridisk krav oppstår. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Laste opp en konfigurasjon til Lifecycle Services** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importere en ER-komponent fra LCS til bruk internt

ER lar deg importere ER-komponenter fra LCS til gjeldende forekomst. Et repositorium av typen **LCS-prosjekt** kreves. Når en ER-komponent er importert fra LCS til gjeldende forekomst, blir eieren av forekomsten forbruker av tjenesten, som tilbys av eieren (forfatter) av den importerte komponenten. Hvis en formatkomponent for eksempel er utformet for å generere et bestemt elektronisk dokument fra programmet, som har et spesifikt format for land/områder (lokaliseringsscenario), antas det at tjenesteforbrukeren kan hente eventuelle oppdateringer som gjøres for formatet, slik at det overholder juridisk krav. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Importere en konfigurasjon fra Lifecycle Services** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Bygge et format ved å velge et annet format som basis (tilpasning)

ER lar deg opprette (avlede) en ny komponent fra gjeldende versjon av en komponent (basis) som ble importert fra LCS. En bruker vil for eksempel avlede et nytt format for å implementere noen spesielle krav til et elektronisk dokument (for eksempel et tilleggsfelt eller en omfattende beskrivelse) for å støtte et tilpassingsscenario. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Oppgrader format ved innføring av ny basisversjon av det** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Oppgradere et format ved å velge en ny versjon av basisformat (rebasere)

ER lar deg automatisk innføre endringer av den nyeste versjonen av basiskomponenten i gjeldende utkastversjon av den avledede komponenten. Denne prosessen kalles *rebasering*. En ny forskriftsmessig endringer som ble introdusert i den nyeste versjonen av formatet som ble importert fra LCS, kan for eksempel slå sammen automatisk i den tilpassede versjon av dette formatet av det elektroniske dokumentet. Endringer som ikke kan slås sammen automatisk anses som konflikter. Disse konfliktene presenteres for manuell løsing i utformingsverktøyet for den aktuelle komponenten. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Oppgrader format ved innføring av ny basisversjon av det formatet** (en del av forretningsprosessen **7.5.5.3 Anskaffe/utvikle endrede komponenter for IT-tjeneste/-løsning (10683)**).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Liste over ER-konfigurasjoner som er utgitt i Finans

Listen over ER-konfigurasjoner for Finance oppdateres hele tiden. Åpne det [globale repositoriet](er-download-configurations-global-repo.md) for å se gjennom listen over ER-konfigurasjoner som støttes for øyeblikket. I hurtigfanen **Avviklingsdetaljer** kan du gå gjennom informasjonen om konfigurasjonene som er avviklet eller ikke lenger vedlikeholdes. 

![Innhold i det globale repositoriet på siden Konfigurasjonsrepositorium.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Tilleggsressurser

- [Opprette konfigurasjoner for elektronisk rapportering (ER)](electronic-reporting-configuration.md)
- [Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
