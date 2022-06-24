---
title: Massedistribusjon av forseglede Commerce-selvbetjeningskomponenter
description: Denne artikkelen forklarer hvordan du bruker rammeverket for installasjonsprogrammer for selvbetjeningskomponenter til stille installasjon og vedlikehold av distribusjoner.
author: jashanno
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: a679d78db3ad5bd9cccbd4ab6a7026bd07890f55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898585"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Massedistribusjon av forseglede Commerce-selvbetjeningskomponenter

[!include [banner](../includes/banner.md)]

Denne artikkelen gjelder det forseglede rammeverket, installasjonsprogrammer for komponenter som gis ut hver måned og begynner med versjon 10.0.18, og som gjøres tilgjengelig i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Vær oppmerksom på at de første utgivelsene av disse nye installasjonsprogrammene betegnes som **(Forhåndsversjon)**. Det eneste formålet med denne betegnelsen er imidlertid å holde de nye installasjonsprogrammene atskilt, mens Microsoft fastsetter om det finnes ytterligere funksjonskrav for å bruke dem. Det betyr ikke at installasjonsprogrammene er ugyldige for produksjon. Microsoft planlegger å avskrive de gamle (eldre) installasjonsprogrammene i eller rundt oktober 2023, basert på utgivelsen av disse nye installasjonsprogrammene. 

Denne artikkelen forklarer hvordan du bruker de nye installasjonsprogrammene til å utføre stille installasjon og vedlikeholdsoppdateringer via kommandolinjeargumenter. Disse argumentene lar deg foreta massedistribusjon på flere ulike måter.

> [!NOTE]
> De nye selvbetjente, forseglede installasjonsprogrammene blir ikke tilgjengelige i Headquarters og kan bare lastes ned via LCS.

## <a name="delimiters-for-mass-deployment"></a>Skilletegn for massedistribusjon

Tabellen nedenfor viser skilletegnene som kan brukes i kommandolinjekjøringen.


| Skilletegn                 | Beskrivelse |
|---------------------------|-------------|
| --AadTokenIssuerPrefix | Prefikset for utstederen av Microsoft Azure Active Directory-tokenet (Azure AD). |
| --AsyncClientAadClientId | Azure AD-klient-ID-en som Async-klient skal bruke under kommunikasjonen med Headquarters. |
| --AsyncClientAppInsightsInstrumentationKey | Instrumenteringsnøkkelen for AppInsights for Async-klient. |
| --AsyncClientCertFullPath | Den fullstendig formaterte URN-banen som bruker avtrykket som søkemåledata for plasseringen for Async-klientidentitetssertifikatet som skal brukes til autentisering i Azure AD for kommunikasjon med Headquarters. Eksempel på riktig formatert URN er `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>`. Verdien **\<MyThumbprint\>** erstattes med sertifikatavtrykket som skal brukes. Ikke bruk denne parameteren sammen med parameteren **-AsyncClientCertThumbprint**. |
| --AsyncClientCertThumbprint | Avtrykket til Async-klientidentitetssertifikatet som skal brukes til autentisering i Azure AD for kommunikasjon med Headquarters. Dette avtrykket skal brukes til å søke etter plasseringen og navnet for **LocalMachine/My store** for å finne riktig sertifikat som skal brukes. Ikke bruk denne parameteren sammen med parameteren **-AsyncClientCertFullPath**. |
| --ClientAppInsightsInstrumentationKey | Instrumenteringsnøkkelen for AppInsights for klient. |
| --CloudPosAppInsightsInstrumentationKey | Instrumenteringsnøkkelen for AppInsights for Cloud POS. |
| --Config | Konfigurasjonsfilen som skal brukes under installasjonen. Et eksempel på et filnavn er **Contoso.CommerceScaleUnit.xml**. |
| --CposAadClientId | Azure AD-klient-ID-en som Cloud POS skal bruke under enhetsaktivering. Denne parameteren kreves ikke for lokale distribusjoner. |
| --Device | Enhets-ID-en, som vist på **Enheter**-siden i Headquarters. |
| --EnvironmentId | Miljø-ID-en. |
| --HardwareStationAppInsightsInstrumentationKey | Instrumenteringsnøkkelen for AppInsights for Hardware Station. |
| --Install | En parameter som angir om komponenten som dette installasjonsprogrammet omfatter, skal installeres. Denne parameteren er ikke obligatorisk. |
| --InstallOffline | Når det gjelder Modern POS, angir denne parameteren at den frakoblede databasen også skal installeres og konfigureres. Bruk også parameteren **-SQLServerName**. Ellers prøver installasjonsprogrammet å finne en standardforekomst som oppfyller forutsetningene. |
| --Port | Porten som skal knyttes til og brukes av den virtuelle katalogen i Retail Server. Hvis du ikke angir noen port, brukes standardporten 443. |
| --Register | Kasse-ID-en, som vist på **Kasser**-siden i Headquarters. |
| --RetailServerAadClientId | Azure AD-klient-ID-en som Retail Server skal bruke under kommunikasjonen med Headquarters. |
| --RetailServerAadResourceId | Azure AD-appressurs-ID-en for Retail Server som skal brukes under enhetsaktivering. Denne parameteren kreves ikke for lokale distribusjoner. |
| --RetailServerCertFullPath | Den fullstendig formaterte URN-banen som bruker avtrykket som søkemåledata for Retail Server-identitetssertifikatet som skal brukes til autentisering i Azure AD for kommunikasjon med Headquarters. Et eksempel på riktig formatert URN er `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>`, der verdien **\<MyThumbprint\>** blir erstattet med sertifikatavtrykket som skal brukes. Ikke bruk denne parameteren sammen med parameteren **-RetailServerCertThumbprint**. |
| --RetailServerCertThumbprint | Avtrykket til Retail Server-identitetssertifikatet som skal brukes til autentisering i Azure AD for kommunikasjon med Headquarters. Dette avtrykket skal brukes til å søke etter plasseringen og navnet for **LocalMachine/My store** for å finne riktig sertifikat som skal brukes. Ikke bruk denne parameteren sammen med parameteren **-RetailServerCertFullPath**. |
| --RetailServerURL | Nettadressen til Retail Server som installasjonsprogrammet skal bruke. (Denne nettadressen kan også kalles nettadressen til Commerce Scale Unit \[CSU\].) Når det gjelder Modern POS, brukes denne verdien under enhetsaktivering. |
| --SkipAadCredentialsCheck| En bryter som angir om nødvendige kontroller for Azure AD-legitimasjon skal hoppes over. Standardverdien er **usann**. |
| --SkipCertCheck | En bryter som angir om nødvendige legitimasjonskontroller skal hoppes over. Standardverdien er **usann**. |
| --SkipIisCheck | En bryter som angir om nødvendige kontroller for Internet Information Services (IIS) skal hoppes over. Standardverdien er **usann**. |
| --SkipNetFrameworkCheck | En bryter som angir om nødvendige kontroller for .NET Framework skal hoppes over. Standardverdien er **usann**. |
| --SkipScaleUnitHealthcheck | En bryter som angir om tilstandskontrollen for installerte komponenter skal hoppes over. Standardverdien er **usann**. |
| --SkipSChannelCheck | En bryter som angir om nødvendige kontroller for sikker kanal skal hoppes over. Standardverdien er **usann**. |
| --SkipSqlFullTextCheck | En bryter som angir om validering av SQL Server-forutsetningen som krever fulltekstsøk, skal hoppes over. Standardverdien er **usann**. |
| --SkipSqlServerCheck | En bryter som angir om nødvendige kontroller for SQL Server skal hoppes over. Standardverdien er **usann**. |
| --SqlServerName | SQL Server-navnet. Hvis navnet ikke er angitt, prøver installasjonsprogrammet å finne standardforekomsten. |
| --SslcertFullPath | Den fullstendig formaterte URN-banen som bruker avtrykket som søkemåledata for sertifikatplasseringen som skal brukes til å kryptere HTTP-trafikk til storskalaenheten. Et eksempel på riktig formatert URN er `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>`, der verdien **\<MyThumbprint\>** blir erstattet med sertifikatavtrykket som skal brukes. Ikke bruk denne parameteren sammen med parameteren **-SslCertThumbprint**. |
| --SslCertThumbprint | Avtrykket til sertifikatet som skal brukes til å kryptere HTTP-trafikk til storskalaenheten. Dette avtrykket skal brukes til å søke etter plasseringen og navnet for **LocalMachine/My store** for å finne riktig sertifikat som skal brukes. Ikke bruk denne parameteren sammen med parameteren **-SslCertFullPath**. |
| --StoreSystemAosUrl | Nettadressen til Headquarters (AOS). |
| --StoreSystemChannelDatabaseId | ID-en (navnet) for kanaldatabase. |
| --TenantId | Leier-ID for Azure AD. |
| --TransactionServiceAzureAuthority | Azure AD-myndighet for Transaction Service. |
| --TransactionServiceAzureResource | Azure AD-ressurs for Transaction Service. |
| --TrustSqlServerCertificate | En bryter som angir om serversertifikatet skal klareres mens det opprettes en tilkobling til SQL Server. For å unngå sikkerhetsrisikoer må du la være å bruke verdien **true** for produksjonsdistribusjoner. Standardverdien er **usann**. |
| --Verbosity | Nivået av logging som blir forespurt under installasjonen. Denne verdien skal vanligvis ikke brukes. |
| --WindowsPhoneAppInsightsInstrumentationKey | Instrumenteringsnøkkelen for AppInsights for Hardware Station. |

## <a name="general-overview"></a>Generell oversikt

Det nye rammeverket for selvbetjente installasjonsprogrammer har ulike funksjoner og forbedringer. Det nye rammeverket genererer for øyeblikket bare installasjonsprogrammer for Modern POS, maskinvarestasjon og CSU (selvdriftet). Det er viktig å forstå den grunnleggende kommandolinjebruken for de forseglede installasjonsprogrammene, som skal ligne det som vises i eksemplet nedenfor. 
 
```Console
<Component Installer Name>.exe install --<Parameter Name> "<Parameter Information>"
```

Installasjonsprogrammet krever parameteren **install** (eller **uninstall** for å fjerne installasjonen) og eventuelle parametere som spesifikt gjelder installasjonen. **Parameternavn** skal omfatte alle parametere som kreves, for eksempel kasse, CSU-nettadresse eller sertifikatinformasjon. **Parameterinformasjon** skal inneholde eventuell ytterligere informasjon om parameterne.

Det forseglede rammeverket er opprettet slik at følgende endringer tillates:
- **Forseglet** – Det nye rammeverket for installasjonsprogram skiller installasjonsprogrammer for Microsoft-distribuerte basekomponenter fullstendig fra de utvidbarhetsbaserte tilpassingene. Tilpassingene installeres etterpå, men blir da frigjort fra oppdateringer (slik at oppdateringer bare tillates for Microsoft-basiskomponenten, bare for tilpassingene eller for begge).
- **Uten brukergrensesnitt** – Det finnes ikke lenger et brukergrensesnitt. Det finnes i stedet en fullstendig kommandolinjebasert kjørbar fil for hvert installasjonsprogram for komponenter. Denne endringen er en av flere viktige endringer eller funksjoner som brukes til å fokusere det nye rammeverket for installasjonsprogram på bruk med massedistribusjon.
- **Utdypet logging** – Forbedrede installasjonsprogramlogger gir bedre validering av vellykket eller mislykket installasjon, hvilke trinn som ble utført, og eventuelle advarsler eller feil som ble generert.
- **Opprydding** – I det nye rammeverket arbeider installasjonsprogrammene for komponenter hardere for å holde installasjonskataloger ryddige, ved å fjerne alt innholdet i komponentmappen før de installerer de nyere komponentene. Denne oppryddingen sikrer at det ikke finnes gjenværende filer som kan gi problemer og forhindre en vellykket installasjon.

Det finnes tre komponenter som ikke er overført til det nye rammeverket: simulatoren for virtuell ekstern enhet, Async Server Connector Service (brukes til støtte for Dynamics AX 2012 R3) og Real-time Service Replacement (brukes til støtte for Dynamics AX 2012 R3).

> [!NOTE]
> Installasjonsprogrammer lagres lokalt og beholdes.  Det er viktig å administrere eller slette de beholdte installasjonsprogrammene etter hvert, slik at de ikke kaster bort diskplass. Vi anbefaler at du beholder det gjeldende installasjonsprogrammet for basiskomponenten(e) og eventuelle installasjonsprogrammer for de nyeste versjonene av utvidelser i tilfelle du må gjenopprette fra ekstreme situasjoner.

## <a name="migration"></a>Overgang

Overgangen fra de gamle selvbetjente installasjonsprogrammene for komponenter til de nye krever at du avinstallerer de gamle komponentene.

- **Modern POS** – Det nye rammeverket for installasjonsprogram gjorde at programmet fikk en ny programsignatur-ID. Du må derfor avinstallere gamle komponenter fullstendig før du installerer den nye Modern POS-komponenten. På grunn av kravet om full avinstallasjon må du foreta enhetsaktivering på nytt. (Denne nye aktiveringen av enheten er bare nødvendig én gang så lenge avinstallasjon ikke gjøres på nytt.)
- **Maskinvarestasjon** – Som et IIS-nettsted krever det nye rammeverket for installasjonsprogram at basismappestrukturen blir omarbeidet. Du må derfor avinstallere gamle komponenter fullstendig før du installerer den nye maskinvarestasjonskomponenten.
- **Commerce Scale Unit (CSU, selvdriftet)** – Som en serie med IIS-nettsteder krever det nye rammeverket for installasjonsprogram at basismappestrukturen blir omarbeidet.  Du må derfor avinstallere gamle komponenter fullstendig før du installerer den nye CSU-komponenten (selvdriftet).

## <a name="modern-pos"></a>Moderne salgssted

### <a name="before-you-begin"></a>Før du begynner

Det er helt avgjørende at du fjerner den gamle, selvbetjente Modern POS-komponenten. Hvis du vil ha mer informasjon, kan du se overgangstrinnene tidligere i denne artikkelen.

### <a name="examples-of-silent-deployment"></a>Eksempler på stille distribusjon

Denne delen viser eksempler på kommandoer som brukes til å installere Modern POS.

#### <a name="silently-install-modern-pos"></a>Stille installasjon av Modern POS

Kommandoen nedenfor installerer (eller oppdaterer) Modern POS stille. Den har standard kommandostruktur som brukes til stille vedlikehold av komponenter som for øyeblikket er installert. Strukturen bruker de grunnleggende verdiene **&lt;InstallerName&gt;.exe**.

Følgende grunnleggende kommando viser de tilgjengelige alternativene hvis en installasjon forespørres. Vi anbefaler på det sterkeste at du bruker denne kommandoen når du tester eller bruker installasjonsprogrammet for første gang.

```Console
CommerceModernPOS.exe --help install
```

> [!NOTE]
> En konfigurasjonsfil kreves ikke for Modern POS. Installasjonsprogrammet har nå parametere (vist tidligere i denne artikkelen) for de ulike verdiene som brukes under enhetsaktivering.

Kommandoen nedenfor angir alle parameterne som skal brukes under enhetsaktivering etter at programmet Modern POS er installert. I dette eksemplet brukes kassen **Houston-3**, som er en vanlig verdi i demodataene for Dynamics 365 Commerce.

```Console
CommerceModernPOS.exe install --Register "Houston-3" --Device "Houston-3" --RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Kommandoen nedenfor angir parameterne som skal brukes til å installere og konfigurere den frakoblede databasen. SQL Server angis sammen med konfigurasjonsfilen som skal brukes.

```Console
CommerceModernPOS.exe install --InstallOffline --SQLServerName "SQLExpress" --Config "ModernPOS.Houston-3.xml"
```

Du kan kombinere disse begrepene på ulike måter for å oppnå installasjonsresultatene du ønsker.

## <a name="hardware-station"></a>Maskinvarestasjon

### <a name="before-you-begin"></a>Før du begynner

Det er helt avgjørende at du fjerner den gamle, selvbetjente maskinvarestasjonskomponenten. Hvis du vil ha mer informasjon, kan du se overgangstrinnene tidligere i denne artikkelen. Det finnes ikke lenger et informasjonsverktøy for forhandlerkonto. Informasjonen om forhandlerkonto blir i stedet installert når en POS-terminal sammenkobles med maskinvarestasjonen. Vi anbefaler på det sterkeste at du kjører følgende kommando når du tester dette installasjonsprogrammet for første gang:

```Console
CommerceHardwareStation.exe --help install
```

### <a name="examples-of-silent-deployment"></a>Eksempler på stille distribusjon

Denne delen viser eksempler på kommandoer som brukes til å installere maskinvarestasjonen.

#### <a name="silently-install-hardware-station"></a>Stille installasjon av maskinvarestasjon

Kommandoen nedenfor installerer (eller oppdaterer) maskinvarestasjonen stille. Den har standard kommandostruktur som brukes til vedlikehold av komponenter som for øyeblikket er installert. Strukturen bruker de grunnleggende verdiene **&lt;InstallerName&gt;.exe**.

Følgende grunnleggende kommando kjører installasjonsprogrammet for den kjørbare filen.

```Console
HardwareStation.exe install --Port 443 --StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" --StoreSystemChannelDatabaseID "Houston" --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> En konfigurasjonsfil kreves ikke for maskinvarestasjonen. Installasjonsprogrammet har nå parametere (vist tidligere i denne artikkelen) for de ulike verdiene som kreves.

Følgende kommando angir alle parameterne som kreves for å hoppe over de nødvendige kontrollene under en standardinstallasjon. 

> [!NOTE]
> Vi anbefaler at du ikke hopper over kontroller uten grundig testing på forhånd, eller i utviklingssituasjoner.

```Console
HardwareStation.exe install --SkipFirewallUpdate --SkipOPOSCheck --SkipVersionCheck --SkipURLCheck --Config "HardwareStation.Houston.xml"
```

Det er vanlig å kombinere disse begrepene på ulike måter for å oppnå installasjonsresultatene du ønsker.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (selvdriftet)

Vi anbefaler på det sterkeste at du kjører følgende kommando når du tester dette installasjonsprogrammet for første gang:

```Console
CommerceStoreScaleUnitSetup.exe --help install
```

### <a name="before-you-begin"></a>Før du begynner

Det er helt avgjørende at du fjerner den gamle, selvbetjente CSU-komponenten (selvdriftet). Hvis du vil ha mer informasjon, kan du se overgangstrinnene tidligere i denne artikkelen.

### <a name="examples-of-silent-deployment"></a>Eksempler på stille distribusjon

Denne delen viser eksempler på kommandoer som brukes til å installere CSU (selvdriftet).

#### <a name="silently-install-csu-self-hosted"></a>Stille installasjon av CSU (selvdriftet)

Kommandoen nedenfor installerer (eller oppdaterer) CSU (selvdriftet). Den har standard kommandostruktur som brukes til stille vedlikehold av komponenter som for øyeblikket er installert. Strukturen bruker de grunnleggende verdiene **&lt;InstallerName&gt;.exe**.

Sammenlignet med de andre selvbetjente installasjonsprogrammene er Commerce Scale Unit (CSU) mer kompleks og krever en forholdsvis stor mengde tilleggsinformasjon. Følgende kommando er minimumskommandoen (med parametere) som kreves for å kjøre installasjonsprogrammet for den kjørbare filen når det ikke finnes en konfigurasjonsfil.

```Console
CommerceScaleUnit.exe install --port 446 --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Det kreves likevel en konfigurasjonsfil for CSU (selvdriftet).

Kommandoen nedenfor er en mer grundig kommando som kjører installeringsprogrammet for den kjørbare filen med noen alternative parametere.

```Console
CommerceScaleUnit.exe install --Port 446 --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Verbosity 0 --Config "Contoso.StoreSystemSetup.xml"
```

Følgende kommando angir parametere som kreves for å hoppe over de nødvendige kontrollene under en standardinstallasjon. 

> [!NOTE]
> Vi anbefaler at du ikke hopper over kontroller uten grundig testing på forhånd, eller i utviklingssituasjoner.


```Console
CommerceScaleUnit.exe installer --skipscaleunithealthcheck --skipcertcheck --skipaadcredentialscheck --skipschannelcheck --skipiischeck --skipnetcorebundlecheck --skipsqlservercheck --skipnetframeworkcheck --skipversioncheck --skipurlcheck --Config "Contoso.StoreSystemSetup.xml" --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate
```

Du kan kombinere disse begrepene på ulike måter for å oppnå installasjonsresultatene du ønsker.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
