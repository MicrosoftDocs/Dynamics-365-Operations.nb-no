---
title: "Konfigurere og distribuere i lokale miljøer"
description: "Dette emnet gir informasjon om hvordan du planlegger, setter opp og distribuerer et lokalt miljø."
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: nb-no
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Konfigurere og distribuere i lokale miljøer

Dette dokumentet beskriver hvordan du planlegger distribusjonen, konfigurerer den nødvendige infrastrukturen, og distribuerer Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokale).

## <a name="finance-and-operations-components"></a>Komponenter i Finance and Operations

Finance and Operations-programmet består av tre hovedkomponenter:

- AOS (Application Object Server)
- Business Intelligence (BI)
- Financial Reporting/Management Reporter

Disse komponentene avhenger av følgende systemprogramvare:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1, som har følgende funksjoner:

    - Fulltekstindekssøk er aktivert.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Programmet kjører ikke hvis fulltekstsøk ikke er aktivert.

- SQL Server Management Studio
- Frittstående Microsoft Azure Service Fabric
- Windows PowerShell 5.0 eller senere
- Active Directory Federation Services (AD FS) på Windows Server 2016

  Domenekontrolleren må være Windows Server 2012 R2 eller senere med domenefunksjonsnivået 2012 R2, eller høyere

  Hvis du vil ha mer informasjon om domenefunksjonsnivået, kan du se: 
  - [Hva er funksjonsnivåer for Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Forstå funksjonsnivåer i Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations-biter distribueres via Microsoft Dynamics Lifecycle Services (LCS). Før du kan distribuere, må du kjøpe lisensnøkler gjennom kanalen for [bedriftsavtaler](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) og definere et lokalt prosjekt i LCS. Distribusjoner kan bare startes gjennom LCS. Hvis du vil ha mer informasjon om hvordan du konfigurerer lokale prosjekter i LCS, se [Opprette et lokalt prosjekt i Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Godkjenning

Det lokale programmet fungerer sammen med AD FS. For å samhandle med LCS må du også konfigurere Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Frittstående Service Fabric

Finance and Operations bruker frittstående Service Fabric. Hvis du ønsker mer informasjon, se [dokumentasjon for Service Fabric](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktur

Finance and Operations er utviklet for bruk på en hyperkonsentrert arkitektur. Maskinvarekonfigurasjonen omfatter følgende komponenter:

- Frittstående Service Fabric-klynge som er basert på Windows Server 2016 virtuelle maskiner (VM-er)
- SQL Server (både klynge-SQL og Alltid på støttes)
- AD FS for godkjenning
- Server Message Block (SMB) versjon 3 fildeling for lagring
- Valgfritt: Microsoft Office Server 2017

Hvis du vil ha mer informasjon, se [Systemkrav](../get-started/system-requirements.md) og Retningslinjer for størrelse.

### <a name="hardware-layout"></a>Oppsett av maskinvare

Planlegg infrastrukturen og Service Fabric-klyngen, basert på de anbefalte størrelsene i [Størrelsesangivelse for maskinvare for lokale miljøer](../get-started/hardware-sizing-on-premises-environments.md). Hvis du vil ha mer informasjon om hvordan du planlegger Service Fabric-klyngen, se [Planlegge og klargjøre distribusjonen av den frittstående Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Tabellen nedenfor viser et eksempel på maskinvareoppsettet. Dette eksemplet brukes gjennom hele emnet for å illustrere oppsettet.

> [!NOTE]
> Den primære noden i Service Fabric-klyngen må ha minst tre noder. I dette eksemplet er **OrchestratorType** angitt som den primær nodetypen.

| Maskinens formål                                 | Maskinnavn    | IP-adresse    |
|-------------------------------------------------|-----------------|---------------|
| Domenekontroller                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Filserver                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Alltid på-klynge                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Kunde                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric-klynge/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric-klynge/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric-klynge/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric-klynge/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric-klynge/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric-klynge/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric-klynge/Management Reporter-node | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric-klynge/SSRS-node                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Definere

### <a name="prerequisites"></a>Forutsetninger

Før du starter oppsettet, må følgende forutsetninger oppfylles. Oppsettet av disse forutsetningene er utenfor området for dette dokumentet.

- Active Directory Domain Services (AD DS) er installert og konfigurert på nettverket ditt.
- AD FS er distribuert.
- SQL Server, SSRS og Management Studio er installert.

### <a name="overview"></a>Oversikt

Følgende må fullføres for å sette opp infrastrukturen for Finance and Operations.

1. Planlegg domenenavn og DNS-soner
2. Planlegg og skaff deg sertifikater
3. Planlegg brukere og tjenestekontoer
4. Opprett DNS-soner og legg til A-oppføringer
5. Legg til VM-er i domenet
6. Legg til nødvendig programvare for VM-er
7. Last ned installasjonsskript fra LCS
8. Beskriv konfigurasjonen
9. Installer sertifikater
10. Sett opp en frittstående Service Fabric-klynge
11. Konfigurer LCS-tilkobling for tenanten
12. Sett opp fillagring
13. Sett opp SQL Server
14. Konfigurer databasene
15. Krypter legitimasjon
16. Definer SSRS
17. Konfigurer AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>Planlegg domenenavn og DNS-soner

Vi anbefaler at du bruker et offentlig registrert domenenavn til produksjonsinstallasjonen av AOS. På den måten kan den åpnes utenfor nettverket, hvis det kreves ekstern tilgang.

For eksempel hvis domenet til firmaet ditt er contoso.com, kan sonen for Finance and Operations (lokalt) være d365ffo.onprem.contoso.com, og vertsnavnene kan være på følgende måte:

- ax.d365ffo.onprem.contoso.com for AOS-maskiner
- sf.d365ffo.onprem.contoso.com for Service Fabric-klyngen

### <a name="plan-and-acquire-your-certificates"></a>Planlegg og skaff deg sertifikater

Secure Sockets Layer-sertifikater (SSL) kreves for å sikre en Service Fabric-klynge og alle programmene som er distribuert. For produksjons- og sandkasseoppgaver anbefaler vi at du får sertifikater fra en sertifiseringsinstans (CA) som [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) eller [GlobalSign](https://www.globalsign.com/en/ssl/). Hvis domenet er konfigurert med [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), kan du opprette sertifikatene via AD CS. Hvert sertifikat må inneholde en privat nøkkel som ble opprettet for nøkkelutveksling, og det må kunne eksporteres til en fil for personlig informasjonsutveksling (*.pfx).

Egensignerte sertifikater kan brukes bare for testing. Installasjonsskriptene inkluderer skript som genererer og eksporterer selvsignerte sertifikater. Som vi har nevnt, må disse sertifikatene brukes bare for testformål.

| Formål                                      | Forklaring | Tilleggskrav |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL-sertifikat                   | Dette sertifikatet brukes til å kryptere data som overføres over et nettverk mellom en forekomst av SQL Server og et klientprogram. | <p>Domenenavnet til sertifikatet må samsvare med det fullt kvalifiserte domenenavnet (FQDN) for SQL Server-forekomsten eller -lytteren.</p><p>Hvis SQL-lytteren er plassert på maskinen DAX7SQLAOSQLA, er for eksempel sertifikatets DNS-navn DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Service Fabric Server-sertifikat            | Dette sertifikatet brukes til å sikre node-til-node-kommunikasjonen mellom Service Fabric-nodene. Dette sertifikatet brukes også som serversertifikatet som vises til klienten som kobles til klyngen. | <p>Domenenavnet til sertifikatet må samsvare med DNS-sonen der AOS og Service Fabric ligger.</p><p>Domenenavnet til sertifikatet kan for eksempel være \*.onprem.contoso.com eller \*.contoso.com.</p><p>Hvis du bruker et sertifikat med jokertegn, gjelder jokertegnet bare for ett nivå. Et underdomene, alternativt navn for emne (SAN), må utlignes mot sertifikatet hvis det er mer enn ett nivå, for eksempel \*.contoso.com i det forrige eksemplet.</p> |
| Service Fabric Client-sertifikat            | Dette sertifikatet brukes av klienter for å vise og behandle Service Fabric-klyngen. | |
| Encipherment-sertifikat                     | Dette sertifikatet brukes til å kryptere sensitiv informasjon, for eksempel passordet for SQL Server og passordet for brukerkontoer. | <p>Nøkkelbruken for sertifikatet må inneholde datakryptering (10), og bør ikke omfatte servergodkjenning eller klientgodkjenning.</p><p>Hvis du vil ha mer informasjon, se [Behandle hemmeligheter i Service Fabric-programmer](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL-sertifikat                          | <p>Dette sertifikatet brukes som serversertifikatet som vises til klienten for AOS-nettstedet. Det brukes også til å aktivere sertifikater av typen Windows Communication Foundation (WCF) / Simple Object Access Protocol (SOAP).</p><p>Service Fabric Server-sertifikatet kan brukes her hvis det er et jokertegn sertifikat.</p> | <p>Domenenavnet til sertifikatet må samsvare med DNS-sonen der AOS og Service Fabric ligger.</p><p>Domenenavnet til sertifikatet kan for eksempel være \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com eller \*.contoso.com.</p><p>Hvis du bruker et sertifikat med jokertegn, gjelder jokertegnet bare for ett nivå. Et underdomene, SAN, må utlignes mot sertifikatet hvis det er mer enn ett nivå, for eksempel \*.contoso.com i det forrige eksemplet.</p> |
| Godkjenningssertifikat for økt           | Dette sertifikatet brukes av AOS for å sikre en brukers øktinformasjon. | Dette er også **Fildeling**-sertifikatet som brukes ved distribusjon fra LCS. |
| Sertifikat for datakryptering og datasignering | Disse sertifikatene brukes av AOS til å kryptere sensitiv informasjon. | |
| Finansrapportering-klientsertifikat       | Dette sertifikatet brukes til å sikre kommunikasjonen mellom Finansrapportering-tjenestene og AOS. | |
| Rapporteringssertifikat                        | Dette sertifikatet brukes til å sikre kommunikasjonen mellom SSRS og AOS. | |
| Lokalt agentsertifikat           | <p>Dette sertifikatet brukes til å sikre kommunikasjonen mellom en lokal agent som ligger lokalt, og LCS.</p><p>Dette sertifikatet kan den lokale agenten bruke til å agere på vegne av din Azure AD-tenant, og til å kommunisere med LCS for å styre og overvåke distribusjoner.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Planlegg brukere og tjenestekontoer

Du må opprette flere bruker- eller tjenestekontoer for at Finance and Operations (lokalt) skal fungere. Du må opprette en kombinasjon av gruppeadministrerte tjenestekontoer (gMSAs), domenekontoer og SQL-kontoer. Tabellen nedenfor viser brukerkontoene, formålene og eksempelnavnen som skal brukes i dette emnet.

| Brukerkonto                                            | Type           | Formål | Brukernavn |
|---------------------------------------------------------|----------------|---------|-----------|
| Finansrapportering-programtjenestekonto         | gMSA           |         | Contoso\\svc-FRAS$ |
| Finansrapportering-prosesstjenestekonto             | gMSA           |         | Contoso\\svc-FRPS$ |
| Finansrapportering, Click Once Designer-tjenestekonto | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS-tjenestekonto                                     | gMSA           | Denne brukeren skal opprettes for fremtidig korrektur. Vi planlegger å aktivere AOS for å fungere med gMSA i kommende versjoner. Når du oppretter denne brukeren under oppsettet, kan du sikre en problemfri overgang til gMSA. | Contoso\\svc-AXSF$ |
| AOS-tjenestekonto                                     | Domenekonto | AOS bruker denne brukeren i GA-utgivelsen. | Contoso\\AXServiceUser |
| AOS SQL DB-administratorbruker                                   | SQL-bruker       | Finance and Operations bruker denne brukeren til å godkjenne med SQL\*. Denne brukeren vil også bli erstattet av gMSA-brukeren i kommende versjoner. | AXDBAdmin |
| Tjenestekonto for lokal distribusjonsagent                  | gMSA           | Denne kontoen brukes at den lokale agenten til å styre distribusjonen i forskjellige noder. | Contoso\\Svc-LocalAgent$ |

\* SQL-brukernavnet og passordet for SQL-godkjenning er sikret, fordi de er kryptert og lagret i den delte filressursen.

### <a name="create-dns-zones-and-add-a-records"></a>Opprett DNS-soner og legg til A-oppføringer

DNS er integrert med AD DS, og lar deg organisere, administrere og finne ressurser i et nettverk. Opprett en sone for DNS-oppslag fremover A-poster for AOS-vertsnavnet og Service Fabric-klyngen. I dette eksempeloppsettet er DNS-sonenavnet d365ffo.onprem.contoso.com, og A-postene/vertsnavnene er som følger:

- **ax**.d365ffo.onprem.contoso.com for AOS-maskiner
- **sf**.d365ffo.onprem.contoso.com for Service Fabric-klyngen

#### <a name="add-a-dns-zone"></a>Legg til en DNS-sone

Bruk fremgangsmåten nedenfor for å legge til en DNS-sone.

1. Logg deg på domenekontrollermaskinen, klikk **Start**, og start DNS Manager ved å skrive **dnsmgmt.msc**.
2. Høyreklikk domenekontrollernavnet, og klikk deretter **Ny sone** \> **Neste**.
3. Velg **Primærsone**.
4. La det være merket av for **Lagre sonen i Active Directory (bare tilgjengelig hvis DNS-serveren er en skrivbar domenekontroller)**, og klikk deretter **Neste**.
5. Velg **Til alle DNS-servere som kjører på domenekontrollere i dette domenet: Contoso.com**, og klikk deretter **Neste**.
6. Velg **Sone for videresendt oppslag**, og klikk deretter **Neste**.
7. Skriv inn sonenavnet for oppsettet, og klikk deretter **Neste**. Skriv for eksempel inn **d365ffo.onprem.contoso.com**.
8. Velg **Ikke tillat dynamiske oppdateringer**, og klikk deretter **Neste**.

#### <a name="set-up-an-a-record-for-aos"></a>Definere en A-post for AOS

I den nye DNS-sonen oppretter du én A-post som heter **ax.d365ffo.onprem.contoso.com** for **hver** Service Fabric-klyngenode av typen **AOSNodeType**. Ikke opprett A-poster for de andre nodetypene.

1. Høyreklikk den nye sonen, og klikk deretter **Ny vert**.
2. Angi navnet og IP-adressen til Service Fabric-noden (f.eks. 10.179.108.12), og klikk deretter **Legg til vert**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Definere en A-post for Orchestrator

I den nye DNS-sonen oppretter du en A-post som heter **sf.d365ffo.onprem.contoso.com** for **hver** Service Fabric-klyngenode av typen **OrchestratorType**. Ikke opprett A-poster for de andre nodetypene.

1. Høyreklikk den nye sonen, og klikk deretter **Ny vert**.
2. Angi navnet og IP-adressen til Service Fabric-noden (f.eks. 10.179.108.15), og klikk deretter **Legg til vert**.

#### <a name="join-vms-to-the-domain"></a>Legg til VM-er i domenet

Legg til hver av VM-ene i domenet ved å fullføre trinnene i [Koble Windows Server 2016 til et Active Directory-domene](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Du kan også bruke Windows PowerShell-skriptet.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Når VM-ene er knyttet til domenet, kan du legge til AOS-tjenestekontoer (Contoso\svc-AXSF$, $ Contoso\svc-AXSF) i den lokale administratorgruppen. Du kan se artikkelen [Legge til et medlem i lokal gruppe](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) om hvordan du gjør dette.

#### <a name="disable-user-access-control"></a>Deaktivere brukertilgangskontroll 

Kjør følgende skript for å deaktivere brukertilgangskontrollen på **hver** Service Fabric-node.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Du må starte noden på nytt når skriptet er fullført vellykket.

#### <a name="add-prerequisite-software-to-vms"></a>Legg til nødvendig programvare for VM-er

Tabellen nedenfor viser den nødvendige programvaren som må brukes på maskiner med hver nodetype.

> [!NOTE]
> Du må starte datamaskinen på nytt når du har installert komponentene.

| Nodetype | Komponent | Kommando |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC-driver | Se [Microsoft ODBC-driver 13.1 for SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework versjon 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework versjon 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internet Information Services (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ omdistribueringspakker for Microsoft Visual Studio 2013 | Se [Microsoft Visual C++ omdistribueringspakker for Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Omdistribuering for Microsoft Access-databasemotor 2010 | Se [Omdistribuering for Microsoft Access-databasemotor 2010](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework versjon 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework versjon 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 i **opprinnelig** modus | |
| MR        | .NET Framework versjon 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework versjon 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ omdistribueringspakker for Microsoft Visual Studio 2013 | Se [Microsoft Visual C++ omdistribueringspakker for Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Last ned installasjonsskript fra LCS

Vi tilbyr flere skript for å forbedre oppsettsopplevelsen. Følg disse trinnene for å laste ned oppsettskriptene fra LCS.

1. Logg på LCS (<https://lcs.dynamics.com/v2>).
2. På instrumentbordet, klikk flisen **Delt aktivabibliotek**.
3. Klikk kategorien **Modell**.
4. I rutenettet, velger du raden **Dynamics 365 for Operations - lokale distribusjonsskript**.
5. Klikk **Versjoner**, og last ned den nyeste versjonen av skriptene.

### <a name="describe-your-configuration"></a>Beskriv konfigurasjonen

Denne delen gir informasjon om skriptene som må du kjøre. Skriptene omtales i rekkefølgen du må kjøre dem i. Du kan kjøre skriptene ved å fylle ut malfilen på $(downloadPath)\\ConfigTemplate.xml. Filen ConfigTemplate.xml beskriver strukturen for Service Fabric-klyngene, sertifikatene som brukes til å konfigurere dem, og kontoene som må ha tilgang til de aktuelle sertifikatene. I eksemplet som følger, fylles verdiene inn for eksempel infrastrukturen som er beskrevet i dette emnet. Malfilen brukes i neste del.

#### <a name="create-the-domain-account-for-a-service-user"></a>Opprette domenekontoen for en tjenestebruker

Kjør følgende kommando for å opprette en domenebrukerkonto, contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>Opprette gMSA-er

1. Endre katalogen til **$(DownloadPath)**, og kjør følgende Windows PowerShell-kommando.

    > [!NOTE]
    > Dette skriptet oppretter ikke brukerne. I stedet skriver det ut kommandoene som må kjøres på domenekontrollermaskinen manuelt.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopier utdataene for kommandoen til et Windows PowerShell-vindu. Kontroller at linjeskiftene er fjernet, og kjør linjene på Active Directory-domenekontrollermaskinen ved hjelp av utvidede rettigheter (høyreklikk, og klikk deretter **Kjør som administrator**).
3. Kjør følgende skript i Active Directory-domenekontrollermaskinen til å validere at kontoene har blitt opprettet. Pass på at du kjører skriptet når du har erstattet mønsteret som samsvarer med navnekonvensjonen for tjenestekontoene.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Kjør skriptet Export-AddGMSAsONVMScript.ps1 på klientmaskinen. Dette skriptet genererer skript som kjøres på hver Service Fabric VM og legger dem til i en mappe som tilsvarer hvert VM-navn.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Stopp IIS

Bruke Remote Desktop Protocol (RDP) til å koble hver Service Fabric VM og fullfør de manuelle trinnne i [Starte eller stoppe Web Server (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). Eventuelt kan du bruke følgende Windows PowerShell-skript ved hjelp av RDP til å koble til hver Service Fabric VM.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS-funksjonen skal være installert, men deaktivert fordi det er noen avhengigheter til IIS-DLLene i produktet._

### <a name="install-certificates"></a>Installer sertifikater

1. Hvis du har kjøpt sertifikatene som ble nevnt tidligere i dette emnet fra en gyldig sertifiseringsinstans, fyller du ut PFX-filnavnet og avtrykket for sertifikatene i filen ConfigTemplate.xml. Angi **generateSelfSignedCert**-attributtet til **False** og **exportable**-attributtet til **False**. Kopier PFX-filene til $(DownloadPath)\\InfrastructureScripts\\Certs-mappen.
2. Hvis du bruker selvsignerte sertifikater (bare for testeformål), kan du kjøre følgende skript. Hvis du vil lage egensignerte sertifikater, i filen ConfigTemplate.xml må du kontrollere at **generateSelfSignedCert** er satt til **True** og **exportable** er satt til **True**. Skriptet vil oppdatere XML-filen med avtrykket for sertifikatet.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Eksport de nye sertifikatene med den private nøkkelen (PFX-filen). Bruk følgende skript til å generere og kjøre eksportkommandoene i Windows PowerShell. PFX filene blir plassert i Certs-mappen.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Sertifikatet må være installert og må ligge i mappen cert:\\CurrentUser\\My. Sertifikatene må også kunne eksporteres.

    Hvis du bruker selvsignerte sertifikater, går du til neste del. Du trenger ikke fullføre denne prosedyren.

4. Når du har eksportert eller kopiert PFX-filene til $(DownloadPath)\\InfrastructureScripts\\Certs-mappen, kjører du følgende kommandoer for å generere skript som skal plasseres i mappene som samsvarer med de virtuelle maskinene.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopier skriptene i hver mappe til de virtuelle maskiner som samsvarer med navnet på mappen.
6. Kjør følgende skriptene i rekkefølgen de vises på hver VM.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Sett opp en frittstående Service Fabric-klynge

1. Kjør følgende kommando for å generere filen ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Hvis du vil ha mer informasjon, se, [Trinn 1B: Opprette en maskin med flere klynger](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Sikre en frittstående klynge på Windows ved hjelp av X.509-sertifikater](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) og [Opprette en frittstående klynge som kjører på Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Last ned den [frittstående Service Fabric-installasjonspakken](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) på en av Service Fabric-nodene. Etter zip-filen er lastet ned, opphever du sperringen ved å høyreklikke zip-filen, og deretter klikke **Egenskaper**. I dialogboksen velger du den **Fjern blokkering** merket nederst til høyre.
3. Kopier zip-filen til en av nodene i Service Fabric-strukturen, og pakk den ut.
4. Kjør følgende kommandoer for å opprette en innkommende brannmurregel på port 443 og 445 i alle nodene.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Kjør følgende kommandoer for å opprette en innkommende brannmurregel på port 80 bare for SSRS-noden.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopier filen ClusterConfig.json til den utpakkede installasjonslokasjonen for frittstående Service Fabric.
7. Navigere til den utpakkede installasjonslokasjonen i Windows PowerShell ved hjelp av utvidede rettigheter, og kjør følgende kommando for å teste ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Hvis testen er vellykket, må du kjøre følgende kommando for å distribuere klyngen.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Når klyngen er opprettet, åpner du Service Fabric-utforskeren på en hvilken som helst klientmaskin for å validere installasjonen:

    1. Installerer Service Fabric-klientsertifikatet i CurrentUser\\My hvis det ikke allerede er installert.
    2. Gå til **Internet Explorer-innstillinger** \> **Kompatibilitetsmodus**, og fjern merket for **Vis intranettområder i kompatibilitetsmodus**.
    3. Gå til `https://sf.d365ffo.onprem.contoso.com:19080`, der sf.d365ffo.onprem.contoso.com er vertsnavnet til Service Fabric-klyngen som er angitt i sonen. Hvis DNS-navneløsing ikke er konfigurert, kan du bruke IP-adressen til maskinen.
    4. Velg klientsertifikatet. Siden **Service Fabric-utforsker** vises.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Konfigurer LCS-tilkobling for tenanten

Distribusjon og vedlikehold av Finance and Operations styres via LCS ved hjelp av en lokal agent. Hvis du vil opprette en tilkobling fra LCS til Finance and Operations-tenanten, må du konfigurere et sertifikat som lar den lokale agenten agere på vegne av din Azure AD-tenant (for eksempel Contoso.Onmicrosoft.com).

Bruk sertifikatet for den lokale agenten som du kjøpte fra en sertifiseringsinstans, eller det selvsignerte sertifikatet som du genererte ved hjelp av skript.

Bare brukerkontoer som har den katalogrollen Global administrator, kan legge til sertifikater for å godkjenne LCS. Som standard blir personen som registrerer seg for Microsoft Office 365 for organisasjonen, den globale administratoren for katalogen.

> [!NOTE]
> Du må konfigurere sertifikatet nøyaktig én gang per tenant. Alle lokale miljøer kan bruke det samme sertifikatet til å koble til LCS.

1. Last ned og installere den nyeste versjonen av Azure PowerShell på en klientmaskin. Hvis du vil ha mer informasjon, se [Installere og konfigurere Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Logg på [kundens Azure-portal](https://portal.azure.com) for å kontrollere at du har katalogrollen for globale administrator.
3. Kjør dette skriptet fra $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Sett opp fillagring

Du må sette opp to høyt tilgjengelige SMB 3.0-filressurser. Hvis du vil ha informasjon om hvordan du aktiverer SMB 3.0, se[SMB sikkerhetsforbedringer](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Sikker dialektforhandling kan ikke registrere eller forhindre nedgraderinger fra SMB 2.0 eller 3.0 til SMB 1.0. På grunn av dette, og for at du skal kunne nytte av alle egenskapene i SMB-kryptering, anbefaler vi sterkt at du deaktiverer SMB 1.0-serveren

> [!NOTE]
> For å sikre at dataene er beskyttet når de hviler i miljøet ditt, må BitLocker-harddiskkryptering være aktivert på alle maskiner. Hvis du vil ha informasjon om hvordan du aktiverer BitLocker, se [BitLocker: Distribusjon av Windows Server 2012 og senere](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- En delt filressurs som inneholder brukerdokumenter som lastes opp til AOS (for eksempel \\\\DAX7SQLAOFILE1\\aos-storage).
- En delt filressurs som inneholder de siste bygg- og konfigurasjonsfilene for å styre distribusjonen (for eksempel \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Behold banen for denne delte filressursen så kort som mulig for å unngå å overskride maksimum banelengde for filene som skal plasseres i den delte ressursen.

1. Kjør følgende kommando på maskinen med den delte filressursen.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Sett opp den delte filressursen \\\\DAX7SQLAOFILE1\\aos-storage

2. I Server Manager velger du **Fil- og lagringstjenester** \> **Delte ressurser**.
3. Klikk **Oppgaver** \> **Ny delt ressurs** for å opprette en ny delt ressurs med navnet **aos-storage**.
4. Gi **Endre**-tillatelser for hver maskin i Service Fabric-klyngen unntatt **OrchestratorNodeType**.
5. Gi **Endre**-tillatelser for AOS-domenebrukeren (contoso\\AXServiceUser) og gMSA-brukeren (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Sett opp den delte filressursen \\\\DAX7SQLAOFILE1\\agent

6. Gå tilbakt til Server Manager, og velg **Fil- og lagringstjenester** \> **Delte ressurser**.
7. Klikk **Oppgaver** \> **Ny delt ressurs** for å opprette en ny delt ressurs med navnet **agent**.
8. Gi **Alle-tillatelser** for gMSA-brukeren for den lokal distribusjonsagenten (contoso\\LocalAgent-svc$).

### <a name="set-up-sql-server"></a>Sett opp SQL Server

1. Install SQL Server 2016 SP1 med høy tilgjengelighet, enten som SQL-klynger som inneholder en Storage Area Network (SAN) eller i en Alltid på-konfigurasjon.  Kontroller at **Databasemotor, Rapporteringstjenester, Fulltekstsøk** og **Administrasjonsverktøy** allerede er installert.
> [!NOTE]
> Kontroller at SQL Alltid på på er konfigurert i henhold til [Siden Velg første datasynkronisering (Alltid på tilgjengelighetsgruppeveivisere)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), og følg [Slik klargjører du sekundære databaser manuelt](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Kjøre SQL-tjenesten som en domenebruker.
3. Hent et SSL-sertifikat fra en sertifiseringsinstans for å konfigurere Finance and Operations. For testing kan du opprette og bruke et egensignert sertifikat.

**Selvsignert sertifikat for klynge-SQL-forekomst**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Selvsignert sertifikat for Alltid på-SQL-forekomst**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Ved hjelp av sertifikatet kan du fullføre trinnene under [Slik aktiverer du SSL-kryptering for en forekomst av SQL Server ved hjelp av Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) for å konfigurere SSL på SQL Server.
5. Følg denne fremgangsmåten for hver node i klyngen. Pass på at du gjøre endringer i den ikke-aktive noden, og kjør en failover på den når det er gjort endringer.

    1. Importer sertifikatet til LocalMachine\\My.
    2. Gi sertifikattillatelser til tjenestekontoen som brukes til å kjøre SQL-tjenesten. I Microsoft Management Console (MMC), høyreklikk sertifikatet (certlm.msc), og klikk deretter **Oppgaver** \> **Administrere privatnøkler**.
    3. Legg til sertifikatavtrykket i HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. I Microsoft SQL Server Configuration Manager, angi **ForceEncryption** til **Ja**.

6. Eksporter den offentlige nøkkelen for sertifikatet (CER-filen), og installer den i hver Service Fabric-node.

### <a name="configure-the-orchestratordata-database"></a>Konfigureree OrchestratorData-databasen

1.  Opprett en tom database, og gi den navnet **OrchestratorData**. Denne databasen brukes av den lokale agenten til å styre distribusjoner.
2.  Gi den lokale agenten gMSA-tillatelser (svc-LocalAgent$) **db\_owner** til databasen:

    1. Utvid servernavnet i treet, utvid **Sikkerhet** \> **Pålogging**, og deretter høyreklikke og velge **Ny pålogging**.

        ![Ny pålogging-kommandoen](./media/OPSetup_01_NewLogin.png)


    2. Slå opp tjenestekontoen **svc-LocalAgent$**. Klikk **Plasseringer**, og velg **Hele katalogen**, og klikk deretter **Objekttyper**, og velg **Tjenestekonto**.

        ![Velg Bruker, Tjenestekonto eller dialogboksen Gruppe](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Angi **Tilordne ServerRole** til **Offentlig**.
    4. Tilordne databaserolletillatelsen **db\_owner** til OrchestratorData-databasen.

### <a name="configure-the-finance-and-operations-database"></a>Konfigurere Finance og Operations-databasen

1. Logg på LCS (<https://lcs.dynamics.com/v2>).
2. På instrumentbordet, klikk flisen **Delt aktivabibliotek**.
3. Klikk kategorien **Modell**. 
4. I rutenettet klikker du raden **Dynamics 365 for Operations (lokalt), Enterprise edition - demodata** for å laste ned zip-filen.
5. Zip-filen inneholder tomme .bak-filer og .bak-filer med demodata. Velg aktuell .bak-fil basert på dine behov. Hvis du for eksempel trenger demodata, gjenoppretter du filen AxBootstrapDB_Demodata.bak. 
6. Gjenopprett databasen AxBootstrapDB_DemoData.bak.
7. Endre navnet på databasen til **AXDBRAIN**.
8. Kjør følgende spørringer på den gjenopprettede databasen.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Oppdater databasefilene:

    1. Høyreklikk databasen, og klikk deretter **Egenskaper**.
    2. Klikk **Filer** for å endre filegenskapene til databasen.
    3. I feltet **Opprinnelig størrelse (MB)** angir du en verdi som er større enn 5120.

        ![Dialogboksen Databaseegenskaper](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. For **AXDBBuild\_Data**, angir du feltet **Autogrowth/Maximize** til **200** megabyte (MB).
    5. For **AXDBBuild\_Log**, angir du feltet **Autogrowth/Maximize** til **500** MB.

        ![Dialogboksen Change Autogrowth](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Opprett en ny bruker med SQL-godkjenning aktivert (axdbadmin).
6. Bruk informasjonen i tabellen nedenfor til å tilordne brukere og databaseroller.

    | Bruker             | Type    | Databaserolle |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Gi svc-AXSF$-brukeren og axdbadmin SQL-brukeren tilgang til følgende roller i tempdb-databasen:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. I Management Studio, kjør følgende Transact SQL (T-SQL)-kommandoer:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Kjør følgende kommando:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Konfigurere databasen for finansrapportering

1.  Opprett en tom database, og gi den navnet **FinancialReporting**.
2.  Bruk informasjonen i tabellen nedenfor til å tilordne brukere og databaseroller.

    | Bruker             | Type | Databaserolle |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Krypter legitimasjon

1. På en hvilken som helst klientmaskin, må du installere krypteringssertifikatet i LocalMachine\\Mitt sertifikatlager.
2. Gi den gjeldende brukeren lesetilgang til den private nøkkelen til dette sertifikatet.
3. Opprett filen Credentials.json som vist her.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** er det kryptert domenebrukerpassordet for AOS-domenebrukeren (contoso\\axserviceuser).
    - **SqlUser** er den krypterte SQL-brukeren (axdbadmin) som har tilgang til Finance and Operations-databasen (AXDBRAIN), og **SqlPassword** er det krypterte SQL-passordet.

4. Kopier .json-filen til delte SMB-filressursen, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Oppdater Credentials.json-filen med krypterte verdier.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. I Credentials.json, erstatt **\<encryptedDomainUserPassword\>** med det kryptert domenepassordet.
    2. Erstatt **\<encryptedSqlUser\>** med den krypterte Finance and Operations SQL-brukeren.
    3. Erstatt **\<encryptedSqlPassword\>** med det krypterte Finance and Operations SQL-passordet.
    
### <a name="set-up-ssrs"></a>Definer SSRS

1.  Før du begynner, må du kontrollere at forutsetningene som er oppført i begynnelsen av dette emnet, er installert.
2.  Følg fremgangsmåten for å [Konfigurere sikkerhet for SQL Server Reporting Services for en lokal distribusjon](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>Konfigurer AD FS

Før du kan fullføre denne prosedyren, må AD FS distribueres på Windows Server 2016. Hvis du vil ha informasjon om hvordan du distribuerer AD FS, se [Distribusjonsveiledning for Windows Server 2016 og for 2012 R2 AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations krever ytterligere konfigurasjon enn standardkonfigurasjonen for AD FS. For trinnene nedenfor, kjører Windows PowerShell på en maskin med AD FS-rolletjenesten installert. Brukerkontoen må ha tillatelse til å administrere AD FS. Brukeren må for eksempel ha en domeneadministratorkonto.

1. Konfigurere AD FS-IDen slik at den samsvarer med AD FS-tokenutstederen.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Du bør deaktivere Windows Integrated Authentication (WIA) for tilkoblinger for intranett-godkjenning med mindre du har konfigurert AD FS for blandede miljøer. Hvis du vil ha mer informasjon om hvordan du konfigurerer WIA slik at det kan brukes med AD FS, se [Konfigurere nettlesere for å bruke Windows Integrated Authentication (WIA) med AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. For pålogging må brukerens e-postadresse være akseptabele godkjenningsinndata.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

For at AD FS skal kunne stole på Finance and Operations for utveksling av godkjenning, må diverse programoppføringer være registrert i AD FS under en AD FS-programgruppe. For raskere installasjonsprosess med færre feil kan du bruke følgende skript for registrering. Kopier skriptet Publish-ADFSApplicationGroup.ps1 og D365FO-OP-katalogen til en maskin der AD FS-rolletjenesten er installert. Deretter kan du kjøre skriptet med en brukerkonto, for eksempel en administratorkonto, som har tillatelse til å administrere AD FS. Hvis du vil ha mer informasjon om hvordan du bruker skriptet, kan du se i dokumentasjonen som er oppført i skriptet. Noter klient-ID-ene som er angitt i utdataene, fordi du vil bli spurt om denne informasjonen i LCS i et senere trinn.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS-administrasjonskonsollen skal ligne på illustrasjonen nedenfor. Åpne Serverbehandling ved å klikke **Verktøy** \> **AD FS-administrasjon**, og deretter nederst i trevisningen til venstre, klikker du **Programgrupper**. Dobbeltklikk programgruppen for å vise flere detaljer.

![Egenskaper for programgruppe](./media/OPSetup_05_ApplicatioGroupProperties.png)

Til slutt, for en tilstandssjekk, må du kontrollere at du har tilgang til URL-en for AD FS OpenID-konfigurasjonen på en Service Fabric-node av typen **AOSNodeType** ved å gå til `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` i en nettleser. Hvis du får en melding om at området ikke er sikkert, har du ikke lagt til AD FS SSL-sertifikatet i lageret for klarerte rotsertifiseringsinstanser. Dette trinnet er beskrevet i distribusjonsveiledningen for AD FS. Hvis du har tilgang til URL-en, returneres en en JavaScript Object Notation-fil (JSON) som inneholder AD FS-konfigurasjonen, og du vil se at AD FS URL-adressen din er klarert.

Med dette er oppsettet av infrastrukturen fullført. Delene nedenfor beskriver hvordan du navigerer til [LCS](https://lcs.dynamics.com) for å definere koblingen og distribuere Dynamics 365 for Finance and Operations-miljøet.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Konfigurere kobling og installere lokal agent

1. Logg på [LCS](https://lcs.dynamics.com/) og åpne det lokale implementeringsprosjektet.
2. På hamburgermenyen klikker du **Prosjektinnstillinger**.

    ![Prosjektinnstillinger-kommandoen](./media/OPSetup_06_ProjectSettings.png)

3. Klikk **Lokale koblinger**.
4. Klikk på **Legg til** for å opprette en ny kobling.
5. På kategorien **Konfigurer vertsinfrastruktur** laster du ned agentinstallasjonsprogrammet.

    ![Knappen Last ned agentinstallasjonsprogram på kategorien Konfigurer vertsinfrastruktur](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Kontroller at zip-filen ikke er blokkert. Høyreklikk filen, klikk **Egenskaper**, og velg deretter **Fjern blokkering**.
7. Pakk ut agentinstallasjonsprogrammet på en av Service Fabric-nodene av typen **OrchestratorType**.
8. På kategorien **Konfigurer agent** angir du konfigurasjonsinnstillingene.
9. Lagre konfigurasjonen, og klikk deretter **Last ned konfigurasjoner** for å laste ned konfigurasjonsfilen localagent-config.json.

    ![Last ned konfigurasjoner-knappen i kategorien Konfigurer agent](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopier filen localagent-config.json til datamaskinen der agentinstallasjonspakken finnes.
11. I et ledetekstvindu kjører du følgende kommando ved å navigere til mappen som inneholder agentinstallasjonsprogrammet.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Brukeren som kjører denne kommandoen, må ha **db\_owner**-tillatelser til OrchestratorData-databasen.
    
12. Gå tilbake til den lokale koblingen i LCS når den lokale agenten er installert.
13. På kategorien **Valider installasjon** klikker du knappen **Meldingsagent**. Dette tester LCS-tilkoblingen til den lokale agenten. Når tilkoblingen er opprettet, vil siden se ut som grafikken nedenfor.

     ![Valider agent](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Distribuere Dynamics 365 for Finance and Operations-miljøet (lokalt)

1. Gå til det lokale prosjektet i LCS, gå til **Miljø**, **Sandkasse**, og klikk på **Konfigurer**.
2. Velg **Miljøtopologi** og gå gjennom veiviseren for å starte distribusjonen.
3. Den lokale agenten plukker opp distribusjonsforespørselen, starter distribusjonen og kommuniserer tilbake til LCS når alt er klart.

