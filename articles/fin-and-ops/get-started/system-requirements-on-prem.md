---
title: Systemkrav for lokale installasjoner
description: I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for distribusjoner i skyen og lokalt.
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73fefd43c9de917dc6c98b2a6893b36a5c0ccdc5
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Systemkrav for lokale installasjoner

[!include[banner](../includes/banner.md)]

I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for distribusjoner i skyen og lokalt. Før du installerer Finance and Operations, om nødvendig, kontroller at systemet du arbeider med, oppfyller eller overskrider minimumskravene til nettverk, maskinvare og programvare.

## <a name="network-requirements"></a>Nettverkskrav
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokalt) kan arbeide på nettverk som bruker Internet Protocol versjon 4 (IPv4) eller Internet Protocol versjon 6 (IPv6). Vurder nettverksmiljøet når du planlegger systemet, og bruk retningslinjene nedenfor.

### <a name="network-response-time"></a>Responstid på nettverket
Tabellen nedenfor viser minimumskravene til nettverk for tilkoblingen mellom webleseren og Application Object Server (AOS) og forbindelsen mellom AOS og databasen i det lokale systemet.

| Verdi     | Nettleser til AOS                      | AOS til database |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Båndbredde | 50 kilobyte per sekund (KBps) per bruker | 100 megabyte per sekund (MBps) |
| Ventetid   | Mindre enn 250 – 300 millisekunder (ms)     | Mindre enn 1 ms (bare lokalt nettverk [LAN]). AOS og databasen må plasseres sammen. |

- Finance and Operations (lokalt) er utformet for nettverk som har en ventetid på 250 til 300 millisekunder (ms) eller mindre. Dette er ventetiden fra en nettleserklient til datasenteret som er vert for Finance and Operations.
- Båndbreddekrav for Finance and Operations (lokalt) er avhengig av scenariet. Vanlige scenarier krever en båndbredde på mer enn 50 kilobyte kBps mellom leseren og Finance and Operations-serveren. For scenarier som har krav til høy nyttelast, for eksempel arbeidsområder eller scenarier med omfattende tilpassing, anbefales imidlertid mer båndbredde. Den bestemte mengden båndbredde er avhengig av bruk.

Distribusjoner der AOS- og Microsoft SQL Server-databasen er i forskjellige datasentre, støttes ikke. AOS og SQL Server-databasen må plasseres sammen. 

Vanligvis er Finance and Operations optimalisert for å redusere rundturer fra nettleser til server. Antall rundturer fra en nettleserklient til datasenteret er svært lite, enten null eller én for hver brukerinteraksjon, og hele nyttelasten er komprimert.

> [!WARNING]
> Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav. Samtidig bruk av en bestemt plassering er svært vanskelig å beregne. Vi foreslår at du bruker reell simulering mot et ikke-produksjonsmiljø for Finance and Operations som den beste ytelsesmålingen for den bestemte saken. 

### <a name="lan-environments"></a>LAN-miljøer
I miljøer med lokalt nettverk (LAN), er Microsoft Remote Desktop i Microsoft Windows Server ikke nødvendig for å koble til Finance and Operations. Eksternt skrivebord kan imidlertid være nødvendig for å vedlikeholde operasjoner på de virtuelle maskinene som utgjør serverdistribusjonene.

### <a name="wan-environments"></a>WAN-miljøer
I miljøer regionnett (WAN), er Remote Desktop i Windows Server ikke nødvendig for å koble til Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Krav til Internett-tilkobling
Finance and Operations (lokalt) krever ikke Internett-tilkobling fra sluttbrukerens arbeidsstasjoner. Noen funksjoner vil imidlertid ikke være tilgjengelige uten Internett-tilkobling.

|                    |   |
|--------------------|---|
| **Nettleserklient** | Et intranettscenario uten Internett-tilkobling er et utformingspoeng for det lokale installasjonsalternativet. Noen funksjoner som krever skytjenester, vil ikke være tilgjengelige, for eksempel hjelp og oppgaveveiledningsbiblioteker i Microsoft Dynamics Lifecycle Services (LCS). |
| **Server**         | AOS eller Microsoft Azure Service Fabric-laget må kunne kommunisere med LCS. Den lokale nettleserbaserte klienten krever ikke Internett-tilgang. |
| **Telemetri**      | Telemetridata kan gå tapt hvis det er lange avbrudd i tilkoblingen. Avbrudd i tilkoblingen til LCS påvirker ikke den lokale programfunksjonaliteten. |
| **LCS**            | Tilkobling til LCS kreves for distribusjon, kodedistribusjon og vedlikehold av operasjoner. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Overføre telemetridata til skyen
Mesteparten av telemetridataene er lagret lokalt og kan åpnes ved hjelp av Hendelsesliste i Microsoft Windows. En undergruppe av telemetrihendelser overføres til en Microsoft-pipelinen for telemetrt i skyen for diagnostikk. Kundedata og data som kan identifisere brukeren, er ikke en del av telemetridataene som sendes til Microsoft. VM-navn sendes til Microsoft for å hjelpe til miljøadministrasjon og diagnose fra LCS-portalen.

## <a name="domain-requirements"></a>Domenekrav
Vurder følgende domenekrav når du installerer Finance and Operations (lokalt):

- Virtuelle maskiner som er vert for komponenter i Finance and Operations (lokalt), må tilhøre et Active Directory-domene. Active Directory Domain Services (AD DS) må være konfigurert i opprinnelig modus.
- Virtuelle maskiner som kjører Finance and Operations (lokalt)-komponenter, må ha tilgang til hverandre. Denne tilgangen er konfigurert i AD DS. 
- Domenekontrolleren må være Microsoft Windows Server 2012 R2 eller senere med domenefunksjonsnivået 2012 R2, eller høyere.

## <a name="hardware-requirements"></a>Krav til maskinvare
Denne delen beskriver maskinvaren som kreves for å kjøre Finance and Operations (lokalt).

Avhengig av systemkonfigurasjonen, sammensetningen av data, og programmene og funksjonene som du vil bruke, kan de faktiske maskinvarekravene variere. Her er noen av faktorene som kan påvirke valget av aktuell maskinvare for Finance and Operations (lokalet):

- Antallet transaksjoner per time
- Antallet samtidige brukere

## <a name="minimum-infrastructure-requirements"></a>Minimumskrav til infrastruktur
Finance and Operations (lokalt) bruker Service Fabric som vert for AOS, partier, databehandling, Management Reporter og orkestreringstjenester for miljøet. 

SQL Server må være definert i et oppsett for HADRON høy tilgjengelighet som inneholder minst to noder for produksjon for bruk.

Illustrasjonen nedenfor viser minimum anbefalt antall noder i Service Fabric-klyngen.

[![Anbefalt antall noder for Service Fabric-klynge](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Krav til prosessor og RAM
Tabellene nedenfor viser hvor mange prosessorer og hvor mye RAM som kreves for hver av rollene som er nødvendig for å kjøre dette distribusjonsalternativet. Hvis du vil ha mer informasjon, kan du se de anbefalte minimumskravene for frittstående Service Fabric-klynge i [Planlegge og klargjøre Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Hvis annen Microsoft-programvare er installert på samme datamaskin, må systemet også oppfylle kravene til maskinvare for denne programvaren. Hvis andre serverprogrammer er installert på samme datamaskin, anbefaler vi at du begrenser andre serverprogrammer til 1 gigabyte (GB) RAM.

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

**Minste størrelse estimater for produksjons- og sandkassedistribusjoner\***

| Topologi                                        | Rolle                          | Antall forekomster |
|-------------------------------------------------|-------------------------------|---------------------|
| Produksjon                                      | AOS, (databehandling, parti)  | 3                   |
|                                                 | Administrasjonsreporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| Sandkasse                                         | AOS, databehandling, parti   | 2                   |
|                                                 | Administrasjonsreporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *Sammendrag av produksjons- og sandkassetopologier* |                               | *16*                |

\*Tallene i denne tabellen blir validert av kundene våre som kjører testversjoner, og kan bli justert etter behov basert på tilbakemeldingen.

\*\* Orchestrator er angitt som primær nodetypen og brukes også til å kjøre Service Fabric-tjenestene.

**Startestimater for SQL Server i bakgrunnen og AD DS**

<table>
<thead>
<tr>
<th></th>
<th>Rolle</th>
<th>VM-er/forekomster</th>
<th>Kjerner</th>
<th>Totalt antall kjerner</th>
<th>Minne per forekomst (GB)</th>
<th>Totalt minne (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Felles infrastruktur</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Filserver/lagringsnettverk/svært tilgjengelig lagring</td>
<td colspan="5"><p>Serverdellagringen må være basert på solid-state-stasjoner (SSDer) på et lagringsnettverk (SAN).</p>
<p>Størrelse og inndata/utdata-operasjoner per sekund (IOPS) er basert på størrelsen på arbeidsmengden.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Sammendrag for felles infrastruktur</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Server-størrelser er svært avhengige av arbeidsoppgaver. Hvis du vil ha mer informasjon, se [Størrelsesangivelse for maskinvare for lokale miljøer](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Lagring

- **AOS** - Finance and Operations (lokalt) bruker en delt ressurs for Server Message Block (SMB) 3.0 til å lagre ustrukturerte data. Hvis du vil ha mer informasjon, se [Lagringsplasser direkte i Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Følgende alternativer er gyldige:

    - Et høyt tilgjengelig SSD-oppsett
    - Et SAN som er optimalisert for elektronisk transaksjonsbehandling (OLTP)
    - Høy ytelse direktetilknyttet lagring (DAS) 

- **SQL Server og IOPS for databehandling** – lagring for både databehandling og SQL Server må ha minst 2000 IOPS. Produksjon IOPS avhenger av mange faktorer. Hvis du vil ha mer informasjon, se [Størrelsesangivelse for maskinvare for lokale miljøer](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – hver VM må ha minst 100 IOP for skriving.

## <a name="virtual-host-requirements"></a>Krav for virtuell vert
Når du definerer de virtuelle vertene for et Finance and Operations-miljø (lokalt), kan du se følgende veiledninger: [Planlegge og klargjøre Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) og [Beskrive en Service Fabric-klynge](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Hver virtuelle vert bør ha nok kjerner for infrastrukturen som skaleres. Flere avanserte konfigurasjoner er mulig, der SQL Server ligger på maskinvaren, men der alt annet er virtualisert. Hvis SQL Server er virtualisert, må diskundersystemet være et fast SAN eller tilsvarende. I alle tilfeller må du kontrollere at det grunnleggende oppsettet for virtuell vert er svært tilgjengelig og med høy redundans. I alle tilfeller, når virtualisering blir brukt, må ingen VM-øyeblikksbilder tas.

## <a name="software-requirements-for-all-server-computers"></a>Krav til programvare for alle serverdatamaskiner
Følgende programvare må være installert på en datamaskin før komponenter i Finance and Operations (lokalt) kan installeres:

- Microsoft .NET Framework versjon 4.5.1 eller senere
- Service Fabric

For mer informasjon, se [Planlegge og klargjøre Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Støttede serveroperativsystemer
Tabellen nedenfor viser serveroperativsystemer som støttes for komponenter i Finance and Operations.

| Operativsystem                                     | Notater |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter eller Standard | Disse kravene er for databasen og Service Fabric-klyngen som er vert for AOS. |

## <a name="software-requirements-for-database-servers"></a>Krav til programvare for databaseservere

- Bare 64-biters versjoner av SQL Server 2016 støttes.
- I et produksjonsmiljø anbefaler vi at du installerer den nyeste samleoppdateringen (CU) for versjonen av SQL Server du bruker.
- Finance and Operations (lokalt) støtter Unicode-samlinger ikke skiller mellom store/små bokstaver, skiller mellom aksenter, skiller mellom kana, og ikke skiller på bredde. Samlingen må samsvare med de nasjonale Windows-innstillingene for datamaskiner som kjører AOS-forekomster. Hvis du oppretter en ny installasjon, anbefaler vi at du velger Windows-sortering i stedet for SQL Server-sortering. Hvis du vil ha mer informasjon om hvordan du velger en sortering for en SQL Server-database, kan du se [dokumentasjonen for SQL Server](/sql/sql-server/sql-server-technical-documentation).

Tabellen nedenfor viser SQL Server-versjoner som støttes for Finance and Operations-databasene. Hvis du vil ha mer informasjon, se minimum maskinvarekrav for [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Behov                                                      | Notater |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition eller Enterprise Edition | For maskinvarekravene for SQL Server 2016 kan du se [Krav til maskinvare og programvare for installasjon av SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Programvarekrav for Application Object Server (AOS) 
- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Programvarekrav for Reporting Server (BI)
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Krav til programvare for klientdatamaskiner
Webprogrammet Finance and Operations kan kjøres på enhver enhet med en HTML 5.0-kompatibel nettleser. Her er noen av de spesifikke kombinasjonene av enhet/nettleser som Microsoft har bekreftet:

- Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
- Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
- Google Chrome (nyeste offentlig tilgjengelig versjon) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller på Google Nexus 10-nettbrett
- Apple Safari (nyeste offentlig tilgjengelig versjon) i Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) eller på Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Krav til programvare for Active Directory Federation Services 
Active Directory Federation Services (AD FS) på Windows Server 2016 kreves.

Domenekontrolleren må være Windows Server 2012 R2 eller senere med domenefunksjonsnivået 2012 R2, eller høyere. Hvis du vil ha mer informasjon om domenefunksjonsnivået, kan du se følgende sider:

- [Hva er funksjonsnivåer for Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Forstå funksjonsnivåer i Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Microsoft Office-programmer som støttes
Følgende Microsoft Office-programmer støttes i skyen og lokale installasjonene av Finance and Operations:

-   Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert. Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Krav til maskinvare og programvare for Retail-komponenter
Finance and Operations (lokalt) inkluderer ikke Retail-komponenter på dette tidspunktet.

