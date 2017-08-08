---
title: Systemkrav
description: I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for distribusjoner i skyen og lokalt.
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: nb-no
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Systemkrav

[!include[banner](../includes/banner.md)]


I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for distribusjoner i skyen og lokalt. Før du installerer Finance and Operations, om nødvendig, kontroller at systemet du arbeider med, oppfyller eller overskrider minimumskravene til nettverk, maskinvare og programvare.


## <a name="supported-microsoft-office-applications"></a>Microsoft Office-programmer som støttes
Følgende Office-programmer støttes i skyen og lokale installasjonene av Finance and Operations.
-   Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert. Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Systemkravene som er spesifikke for skydistribusjoner
## <a name="network-requirements"></a>Nettverkskrav
-   Finance and Operations er utformet for nettverk med ventetid på 250 til 300 millisekunder (ms) eller mindre. Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Finance and Operations. Vi anbefaler at du tester nettverksventetiden på <http://www.azurespeed.com>.
-   Båndbreddekrav for Finance and Operations er avhengig av scenariet. De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kbps). For scenarier som har krav til høy nyttelast, for eksempel arbeidsområder eller scenarier med omfattende tilpassing, anbefales imidlertid mer båndbredde.

Generelt er Finance and Operations optimalisert for Internett. Antall rundturer fra en nettleserklient til Azure-datasenteret er svært lite, og hele nyttelasten er komprimert. 

> [!WARNING]
> Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav. Samtidig bruk av en bestemt plassering er svært vanskelig å beregne. Kunder som er bekymret for krav til båndbredde kan bruke en forhåndsversjon av Finance and Operations.

## <a name="net-framework-requirements"></a>.NET Framework-krav
Finance and Operations krever .NET Framework versjon 4.6.2 for alle ClickOnce-programmer, for eksempel dokumentrutingsagenten. Hvis du vil lese installasjonsinstruksjonene, kan du se [Installere .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Nettlesere som støttes
Webprogrammet kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:


-   Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
-   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
-   Google Chrome (nyeste offentlig tilgjengelig versjon) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller på Google Nexus 10-nettbrett
-   Apple Safari (nyeste offentlig tilgjengelig versjon) i Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) eller på Apple iPad

Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted. 

> [!NOTE]
> -   En forhåndsversjon av Chrome-tillegget må installeres for å kunne ta skjermbilder med Oppgaveopptaker, og ta dem med i genererte Microsoft Word-dokumenter. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program. Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer. ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.
> -   Rapportutforming for finansrapportering startes som et ClickOnce-program. Det krever et 64-biters kompatibelt operativsystem. Hvis du bruker Chrome, må du installere et ClickOnce-tillegg for å kunne laste ned klienten for rapportutforming. Hvis du bruker Chrome i inkognitomodus, må du kontrollere at ClickOnce-tillegget også er aktivert for inkognitomodus.
> -   Hvis du vil forhåndsvise PDF-filer, anbefaler vi at du bruker nettlesere som Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows 10 eller Google Chrome (siste offentlig tilgjengelige versjon) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-nettbrett.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Støttede nettlesere for Skybasert salgssted for detaljhandel

Retail Cloud POS kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:

-   Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
-   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
-   Chrome (nyeste offentlig tilgjengelige versjon) i Windows 10, Windows 8.1 eller Windows 7

## <a name="retail-modern-pos-requirements"></a>Krav for moderne salgssted for detaljhandel
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Moderne salgssted for detaljhandel er et 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.
-   Moderne salgssted for detaljhandel støttes bare på utgavene Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Minimumskrav til systemet

-   Den minste oppløsningen som støttes er 1 280 × 1 024.
-   Datamaskinen som kjører moderne salgssted for detaljhandel må oppfylle disse kravene:
    -   Den må, som minimum en dual core-prosessor som kjører på ikke mindre enn 2 GHz (gigahertz).
    -   Den må, ha minimum 3 GB (gigabyte) RAM.
    -   Den må ha Internett-tilgang.

## <a name="retail-hardware-station-requirements"></a>Krav til maskinvarestasjon for detaljhandel
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Maskinvarestasjon for detaljhandel er et 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.
-   Maskinvarestasjon for detaljhandel støttes på følgende operativsystemer:
    -   Utgavene Windows 7 Professional, Enterprise og Ultimate 
    
    > [!NOTE]
    > Windows 7 støttes bare hvis Internet Explorer 11 installeres manuelt på systemet.

    -   Utgavene Windows 8.1 Update 1 Professional, Enterprise og Embedded
    -   Utgavene Windows 10 Pro, Enterprise og Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimumskrav til systemet

Datamaskinen må oppfylle alle systemkrav for installasjon og bruk av følgende elementer:

-   Internet Information Services (IIS)
-   Tredjepartsmaskinvare

## <a name="retail-store-scale-unit-requirements"></a>Krav for skalaenhet for detaljhandel
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Skalaenhet for detaljhandel er et 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.
-   Skalaenhet for detaljhandel støttes på følgende operativsystemer:
    -   Utgavene Windows 7 Professional, Enterprise og Ultimate
    -   Utgavene Windows 8.1 Update 1 Professional, Enterprise og Embedded
    -   Utgavene Windows 10 Pro, Enterprise og Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimumskrav til systemet

-   4 GB RAM
-   1,6 GHz maksimal CPU-hastighet per kjerne (to kjerner er minimum)
-   Minst 10 GB ledig plass (kanaldatabasen kan kreve svært mye plass)

### <a name="recommended-system-requirements"></a>Anbefalte systemkrav

-   6 GB RAM
-   2,4 GHz i7 (eller tilsvarende) maksimal CPU-hastighet per kjerne (fire kjerner anbefales)
-   Minst 10 GB ledig plass (kanaldatabasen kan kreve svært mye plass)

## <a name="connector-requirements"></a>Krav til kobling
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Koblingen for Microsoft Dynamics AX har to separate installasjonsprogram, den **Async Server Connector-tjeneste** og **Real-time service for Dynamics AX 2012 R3**.
-   Begge komponentene er 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.
-   Begge komponentene støttes på følgende operativsystemer:
    -   Utgavene Windows 7 Professional, Enterprise og Ultimate
    -   Utgavene Windows 8.1 Update 1 Professional, Enterprise og Embedded
    -   Utgavene Windows 10 Pro, Enterprise og Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimumskrav til systemet

-   2 GB RAM, 4 GB RAM anbefales
-   1,6 GHz maksimal CPU-hastighet per kjerne (to kjerner er minimum)
-   Minst 10 GB ledig plass (kanaldatabasen kan kreve svært mye plass)

## <a name="requirements-for-development-on-local-vms"></a>Krav for utvikling på lokale virtuelle maskiner
Hvis du vil ha informasjon om kravene til utvikling på lokale virtuelle maskiner (VM-er), kan du se [Virtuelle maskiner som kjører lokalt](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Systemkrav for lokale installasjoner

## <a name="network-requirements"></a>Nettverkskrav
Finance and Operations (lokalt) kan fungere på nettverk som bruker Internet Protocol versjon 4 (IPv4) eller Internet Protocol versjon 6 (IPv6). Vurder nettverksmiljøet når du planlegger systemet, og bruk retningslinjene nedenfor.

### <a name="network-response-time"></a>Responstid på nettverket
Tabellen nedenfor viser minimumskravene til nettverk for tilkoblingen mellom webleseren og Application Object Server (AOS) og forbindelsen mellom AOS og databasen i det lokale systemet.

| Verdi     | Nettleser til AOS | AOS til database                                            |
|-----------|--------------------|------------------------------------------------------------|
| Båndbredde | 50 kBps per bruker   | 100 MBps                                                   |
| Ventetid   | < 250-300 ms       | < 1 ms (bare LAN). AOS og databasen må plasseres sammen. |

- Finance and Operations (lokalt) er utformet for nettverk som har en ventetid på 250 til 300 millisekunder (ms) eller mindre. Dette er ventetiden fra en nettleserklient til datasenteret som er vert for Finance and Operations.
- Båndbreddekrav for Finance and Operations (lokalt) er avhengig av scenariet. Vanlige scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kBps) mellom leseren og Finance and Operations-serveren. For scenarier som har krav til høy nyttelast, for eksempel arbeidsområder eller scenarier med omfattende tilpassing, anbefales imidlertid mer båndbredde, avhengig av bruken.
Distribusjoner der AOS- og SQL Server-databasen er i forskjellige datasentre, støttes ikke. AOS- og SQL Server-databasen må plasseres sammen. Vanligvis er Finance and Operations optimalisert for å redusere rundturer fra nettleser til server. Antall rundturer fra en nettleserklient til datasenteret er svært lite, enten null eller én for hver brukerinteraksjon, og hele nyttelasten er komprimert.

> [!WARNING]
> Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav. Samtidig bruk av en bestemt plassering er svært vanskelig å beregne. Vi foreslår at du bruker reelle simulering mot et-produksjonsmiljø for økonomi og operasjoner som den beste måler ytelse for den bestemte saken. 

### <a name="lan-environments"></a>LAN-miljøer
I miljøer med lokalt nettverk (LAN), er Microsoft Remote Desktop i Microsoft Windows Server ikke nødvendig for å koble til Finance and Operations. Det kan imidlertid være nødvendig for å vedlikeholde operasjoner på de virtuelle maskinene som utgjør serverdistribusjonene.

### <a name="wan-environments"></a>WAN-miljøer
I miljøer regionnett (WAN), er Remote Desktop i Windows Server ikke nødvendig for å koble til Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Krav til Internett-tilkobling
Finance and Operations (lokalt) krever ikke Internett-tilkobling fra sluttbrukerens arbeidsstasjoner. Noen funksjoner vil imidlertid ikke være tilgjengelige uten Internett-tilkobling.

| Nettleserklient | Et intranettscenario uten Internett-tilkobling er et utformingspoeng for det lokale installasjonsalternativet. Noen funksjoner som krever skytjenester, vil ikke være tilgjengelige, for eksempel hjelp og oppgaveveiledningsbiblioteker i LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server         | AOS eller Service Fabric-laget må kunne kommunisere med LCS. Den lokale nettleserbaserte klienten krever ikke Internett-tilgang.                                                                                |
| Telemetri      | Telemetridata kan gå tapt hvis det er lange avbrudd i tilkoblingen. Avbrudd i tilkoblingen til LCS påvirker ikke den lokale programfunksjonaliteten.                                                |
| LCS            | Tilkobling til LCS kreves for distribusjon, kodedistribusjon og vedlikehold av operasjoner.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Overføre telemetridata til skyen
Mesteparten av telemetrien er lagret lokalt og kan åpnes ved hjelp av Hendelsesliste i Microsoft Windows. En undergruppe av telemetrihendelser overføres til en Microsoft-pipelinen for telemetrt i skyen for diagnostikk. Kundedata og og data som kan identifisere sluttbrukeren, er ikke en del av telemetrien som sendes til Microsoft. VM-navn sendes til Microsoft for å hjelpe til miljøadministrasjon og diagnose fra LCS-portalen.

## <a name="domain-requirements"></a>Domenekrav
Vurder følgende domenekrav når du installerer Finance and Operations (lokalt):

- Virtuelle maskiner som er vert for komponenter i Finance and Operations (lokalt), må tilhøre et Active Directory-domene. Active Directory Domain Services (AD DS) må være konfigurert i opprinnelig modus.
- Virtuelle maskiner som kjører komponenter i Finance and Operations (lokalt), må ha tilgang til hverandre konfigurert i Active Directory Domain Services. 
- Domenekontrolleren må kjøres på Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>Krav til maskinvare
Denne delen beskriver maskinvaren som kreves for å kjøre Finance and Operations (lokalt).
Avhengig av systemkonfigurasjonen, sammensetningen av data, og programmene og funksjonene som du vil bruke, kan de faktiske maskinvarekravene variere. Her er noen av faktorene som kan påvirke valget av aktuell maskinvare for Finance and Operations (lokalet):

- Antallet transaksjoner per time.
- Antallet samtidige brukere.

## <a name="minimum-infrastructure-requirements"></a>Minimumskrav til infrastruktur
Finance and Operations (lokalt) bruker Microsoft Azure Service Fabric som vert for AOS, partier, databehandling, Management Reporter og orkestreringstjenester for miljøet. Microsoft SQL Server Reporting Services (SSRS) lagres ikke i Service Fabric-klyngen.
SQL Server må være definert i et oppsett for HADRON høy tilgjengelighet som inneholder minst to noder for produksjon for bruk.
Illustrasjonen nedenfor viser minimum anbefalt antall noder i Service Fabric-klyngen.

[![Anbefalt antall noder for Service Fabric-klynge](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Krav til prosessor og RAM
Tabellen nedenfor viser hvor mange prosessorer og hvor mye RAM som kreves for hver av rollene som er nødvendig for å kjøre dette distribusjonsalternativet. Hvis du vil ha mer informasjon, kan du lese minimumskravene anbefalingen for frittstående Service Fabric-klynge, [Planlegge og klargjøre Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Hvis annen Microsoft-programvare er installert på samme datamaskin, må systemet også oppfylle kravene til maskinvare for denne programvaren. Vi anbefaler at du begrenser andre serverprogrammer på samme datamaskin som AOS til 1 gigabyte (GB) RAM.

**Endre størrelse etter rolle og topologi**

| Topologi   | Rolle (nodetype)              | Anbefalte prosessorkjerner | Anbefalt minne (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Produksjon | AOS, databehandling, parti   | 8                           | 24                      |
|            | Administrasjonsreporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| Sandkasse    | AOS, databehandling, parti   | 4                           | 24                      |
|            | Administrasjonsreporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**Minste størrelse estimater for produksjons- og sandkassedistribusjoner**\*

| Topologi                                  | Rolle                          | Antall forekomster |
|-------------------------------------------|-------------------------------|---------------------|
| Produksjon                                | AOS, (databehandling, parti)  | 3                   |
|                                           | Administrasjonsreporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Sandkasse                                   | AOS, databehandling, parti   | 2                   |
|                                           | Administrasjonsreporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator                  | 3                   |
| *Sammendrag av produksjons- og sandkassetopologier* |                               | 16                  |

\*Tallene blir validert av kundene våre som kjører testversjoner, og kan bli justert etter behov basert på tilbakemeldingen.

\*\*Orchestrator er angitt som primær nodetypen og brukes til å kjøre Service Fabric-tjenestene også.

**SQL Server i bakgrunnen og AD startestimater**

[![SQL Server i bakgrunnen og AD startestimater](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server-størrelser er svært avhengige av arbeidsoppgaver. Hvis du vil ha mer informasjon, se delen [Størrelsesangivelse for maskinvare for lokale miljøer](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Lagring

- **AOS** - Finance and Operations (lokalt) bruker en delt ressurs for Server Message Block (SMB) 3.0 til å lagre ustrukturerte data. Hvis du vil ha mer informasjon, se [Lagringsplasser direkte i Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – aktuelle alternativer:
    - Et oppsett for høyt tilgjengelig SSD (solid-state drive).
    - En lagringsnettverk (SAN) optimalisert for OLTP-gjennomstrømninger.
    - Høy ytelse direktetilknyttet lagring (DAS) 
- **SQL og IOPS for databehandling** – lagring for både databehandling og SQL Server må ha minst 2000 inndata/utdata-operasjoner per sekund (IOPS). Produksjon IOPS avhenger av mange faktorer. Hvis du vil ha mer informasjon, se delen "Størrelsesangivelse for maskinvare for lokale miljøer". 
- **IOPS for virtuell maskin** – hver virtuelle maskin må ha minst 100 IOPS for skriving.

## <a name="virtual-host-requirements"></a>Krav for virtuell vert
Når du definerer de virtuelle vertene for et Finance and Operations-miljø (lokalt), kan du se følgende veiledninger: [Planlegge og klargjøre Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) og [Beskrive en Service Fabric-klynge](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Hver virtuelle vert bør ha nok kjerner for infrastrukturen som skaleres. Flere avanserte konfigurasjoner er mulig, der SQL Server ligger på maskinvaren, men der alt annet er virtualisert. Hvis SQL Server er virtualisert, må diskundersystemet være et fast SAN eller tilsvarende. I alle tilfeller må du kontrollere at det grunnleggende oppsettet for virtuell vert er svært tilgjengelig og med høy redundans. I alle tilfeller, når virtualisering blir brukt, må ingen VM-øyeblikksbilder tas.

## <a name="software-requirements-for-all-server-computers"></a>Krav til programvare for alle serverdatamaskiner
Følgende programvare må være installert på en datamaskin før komponenter i Finance and Operations (lokalt) kan installeres:

- Microsoft .NET Framework 4.5.1 eller høyere
- Service Fabric. For mer informasjon, se [Planlegge og klargjøre Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Støttede serveroperativsystemer
Tabellen nedenfor viser serveroperativsystemer som støttes for komponenter i Finance and Operations.

| Operativsystem                                     | Notater                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter eller Standard | Disse kravene er for databasen og Service Fabric-klyngen som er vert for AOS. |

## <a name="software-requirements-for-database-servers"></a>Krav til programvare for databaseservere

- Bare 64-biters versjoner av SQL Server 2016 støttes.
- I et produksjonsmiljø anbefaler vi at du installerer den nyeste samleoppdateringen (CU) for versjonen av SQL Server du bruker.
- Finance and Operations (lokalt) støtter Unicode-samlinger ikke skiller mellom store/små bokstaver, skiller mellom aksenter, skiller mellom kana, og ikke skiller på bredde. Samlingen må samsvare med de nasjonale Windows-innstillingene for datamaskiner som kjører AOS-forekomster. Hvis du oppretter en ny installasjon, anbefaler vi at du velger Windows-sortering i stedet for SQL Server-sortering. Hvis du vil ha mer informasjon om hvordan du velger en sortering for en SQL Server-database, kan du se [dokumentasjonen for SQL Server](/sql/sql-server/sql-server-technical-documentation).
Tabellen nedenfor viser SQL Server-versjoner som støttes for Finance and Operations-databasene. Hvis du vil ha mer informasjon, se minimum maskinvarekrav for [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Behov                                                      | Notater                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition eller Enterprise Edition | For maskinvarekravene for SQL Server 2016 kan du se [Krav til maskinvare og programvare for installasjon av SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Krav til programvare for klientdatamaskiner
Webprogrammet Finance and Operations kan kjøres på enhver enhet med en HTML5.0-kompatibel nettleser. Spesifikke kombinasjoner av enhet/nettleser som Microsoft har bekreftet, omfatter:

- Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
- Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
- Google Chrome (nyeste offentlig tilgjengelig versjon) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller på Google Nexus 10-nettbrett
- Apple Safari (nyeste offentlig tilgjengelig versjon) i Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) eller på Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Krav til programvare for Active Directory Federation Services 
Active Directory Federation Services (AD FS) på Windows Server 2016

Domenekontrolleren må være Windows Server 2012 R2 eller senere med domenefunksjonsnivået 2012 R2, eller høyere

Hvis du vil ha mer informasjon om domenefunksjonsnivået, kan du se: 
- [Hva er funksjonsnivåer for Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Forstå funksjonsnivåer i Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Krav til maskinvare og programvare for Retail-komponenter
Finance and Operations (lokalt) inkluderer ikke Retail-komponenter på dette tidspunktet.

<a name="see-also"></a>Se også
--------

[Få en evalueringskopi av Dynamics 365 for Finance and Operations, Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

