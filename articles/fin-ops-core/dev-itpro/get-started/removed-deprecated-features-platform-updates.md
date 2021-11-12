---
title: Fjernede eller avskrevne Platform-funksjoner
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.
author: sericks007
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0065f5c101237de49ae362ecd3378ec5046dbf4b
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725055"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjernede eller avskrevne Platform-funksjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="feature-removal-effective-october-2021"></a>Fjerning av funksjoner gjelder fra oktober 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-rapporter i Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Alle aktiviteter og all overvåking vil bli utført internt, av plattformen, gjennom automasjon. Dette krever ikke manuell inngripen.|
| **Erstattet med en annen funksjon?**   | Ja, det er nå et automatisert system som gjør disse funksjonene foreldet. |
| **Berørte produktområder**         | SQL-rapporter: Gjeldende DTU, Gjeldende DTU-detaljer, Hent låsedetaljer, Liste over gjeldende planveiledning, Hent liste over spørrings-IDer, Hent SQL-spørringsplanen for en gitt plan-ID, Hent spørringsplaner og utførelsesstatus, Hent begrensningskonfigurasjon, Hent ventestatistikk, Vis dyreste spørringer |
| **Distribusjonsalternativ**              | Skydistribusjon – påvirker Microsoft-administrerte produksjonsmiljøer og sandkassemiljøer på lag 2 til og med lag 5. |
| **Status**                         | Fjernet |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-handlinger i LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi avskriver noen SQL-handlinger i LCS. Alle aktiviteter og all overvåking vil bli utført internt, av plattformen, gjennom automasjon. Dette krever ikke manuell inngripen. |
| **Erstattet med en annen funksjon?**   | Ja, det er nå et automatisert system som gjør disse funksjonene foreldet. |
| **Berørte produktområder**         | SQL-handlinger: Opprett en planhåndbok for å fremtvinge plan-ID, Opprett en planhåndbok for å legge til tabellreferanser, Fjern planveiledning, Deaktiver/aktiver sidelåser og låsskalering, Oppdater statistikk i en tabell, Bygg indeks på nytt, Opprett indeks |
| **Distribusjonsalternativ**              | Skydistribusjon – påvirker Microsoft-administrerte produksjonsmiljøer og sandkassemiljøer på lag 2 til og med lag 5. |
| **Status**                         | Fjernet |


## <a name="feature-deprecation-effective-october-2021"></a>Varsel om funksjonsavvik gjelder fra oktober 2021

### <a name="show-related-document-attachments-feature"></a>Funksjonen "Vis tilknyttede dokumentvedlegg"

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen returnerte uventede resultater. |
| **Erstattet med en annen funksjon?**   | Nei. Eventuelle ytterligere planer med hensyn til denne funksjonaliteten vil bli kommunisert gjennom prosessen for standard lanseringsbølge. |
| **Berørte produktområder**         | Webklient - Erfaring med dokumentvedlegg |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.23 av Finance and Operations-apper

### <a name="ondbsynchronize-event"></a>OnDBSynchronize-hendelse

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Det er ingen kontroll for å utføre denne hendelsen. |
| **Erstattet med en annen funksjon?**   | Ja, flytt eksisterende metoder abonnert på av **OnDBSynchronize**-hendelsen til en SysSetup-utvidet klasse. |
| **Berørte produktområder**         | Databasesynkronisering |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet. Planlagt fjerningsdato er oktober 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>API for SystemNotificationsManager.AddNotification

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Microsoft krever tilleggsparametere når du legger til varsler. |
| **Erstattet med en annen funksjon?**   | Ja, API for **SystemNotificationsManager.AddSystemNotification()**. Denne API-en krever at du uttrykkelig angir ExpirationDateTime og RuleID for genererte varslinger. |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet. Planlagt fjerningsdato er april 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.21 av Finance and Operations-apper

### <a name="skype-for-business-online-support"></a>Støtte for Skype for Business Online

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Skype for Business Online er trukket tilbake. Hvis du vil ha mer informasjon, kan du se [Skype Business Online-tjenesten er trukket tilbake](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Erstattet med en annen funksjon?**   | Ikke i øyeblikket, men vi kan vurdere å legge til tilstedeværelse fra Teams i fremtiden.|
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet. Innstillingen **Skype-aktivert** er slått av fra og med versjon 10.0.21. Fjerning av denne innstillingen er rettet mot april 2022. Funksjonen vil imidlertid slutte å fungere etter at Skype-teamet avslutter tjenesten. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Varsel om funksjonsavvik gjelder fra august 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-rapporter i Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Alle aktiviteter og all overvåking vil bli utført internt, av plattformen, gjennom automasjon. Dette krever ikke manuell inngripen.|
| **Erstattet med en annen funksjon?**   | Ja, det er nå et automatisert system som gjør disse funksjonene foreldet. |
| **Berørte produktområder**         | SQL-rapporter: Gjeldende DTU, Gjeldende DTU-detaljer, Hent låsedetaljer, Liste over gjeldende planveiledning, Hent liste over spørrings-IDer, Hent SQL-spørringsplanen for en gitt plan-ID, Hent spørringsplaner og utførelsesstatus, Hent begrensningskonfigurasjon, Hent ventestatistikk, Vis dyreste spørringer |
| **Distribusjonsalternativ**              | Skydistribusjon – påvirker Microsoft-administrerte produksjonsmiljøer og sandkassemiljøer på lag 2 til og med lag 5. |
| **Status**                         | Avskrevet: Planlagt fjerningsdato er oktober 2021. |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-handlinger i LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi avskriver noen SQL-handlinger i LCS. Alle aktiviteter og all overvåking vil bli utført internt, av plattformen, gjennom automasjon. Dette krever ikke manuell inngripen. |
| **Erstattet med en annen funksjon?**   | Ja, det er nå et automatisert system som gjør disse funksjonene foreldet. |
| **Berørte produktområder**         | SQL-handlinger: Opprett en planhåndbok for å fremtvinge plan-ID, Opprett en planhåndbok for å legge til tabellreferanser, Fjern planveiledning, Deaktiver/aktiver sidelåser og låsskalering, Oppdater statistikk i en tabell, Bygg indeks på nytt, Opprett indeks |
| **Distribusjonsalternativ**              | Skydistribusjon – påvirker Microsoft-administrerte produksjonsmiljøer og sandkassemiljøer på lag 2 til og med lag 5. |
| **Status**                         | Avskrevet: Planlagt fjerningsdato er oktober 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Varsel om funksjonsavvik gjelder fra mai 2021

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Globaliseringsportal i Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi avskriver globaliseringsportalen i LCS fordi denne funksjonen har blitt erstattet av andre LCS-baserte tjenester. |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonen erstattes av LCS [Problemsøk](../lifecycle-services/issue-search-lcs.md) og [Dynamics-tjenesten for innsending av forskriftsmessige varsler](../lcs-solutions/submit-localization-alerts.md). |
| **Berørte produktområder**         | Globaliseringsportal i LCS|
| **Distribusjonsalternativ**              | Skydistribusjon |
| **Status**                         | Avskrevet: Planlagt fjerningsdato er mai 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Funksjonen ble fjernet 28. januar 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Satsvis jobb for å håndtere defragmentering av SQL-indeks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Denne funksjonen ble fjernet for å redusere de indirekte kostnadene ved drift, overvåking og vedlikehold av indeksbehandling foretatt av kunder. |
| **Erstattet med en annen funksjon?**   | Indeksbehandlingen blir i fremtiden foretatt av Microsoft-tjenester. Dette skjer kontinuerlig uten å påvirke arbeidsmengden til brukerne. |
| **Berørte produktområder**         | Finance and Operations-apper|
| **Distribusjonsalternativ**              | Skydistribusjon – påvirker Microsoft-administrerte produksjonsmiljøer og sandkassemiljøer på lag 2 til og med lag 5. |
| **Status**                         | Dette funksjonen er fjernet. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.17 av Finance and Operations-apper


### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å støtte de siste versjonene av Visual Studio må det gjøres enkelte endringer i X++-utvidelser for Visual Studio. Disse endringene er ikke kompatible med Visual Studio 2015. |
| **Erstattet med en annen funksjon?**   | Visual Studio 2017 vil erstatte Visual Studio 2015 som den distribuerte og påkrevde versjonen. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: De forrige X++-verktøyene blir fjernet fra Visual Studio 2015 ved oppdatering, og de oppdaterte verktøyene blir ikke installert i Visual Studio 2015. Vertsbaserte builder påvirkes ikke. Når det gjelder virtuelle maskiner for build, må kompileringskontrollen (builddefinisjonen) oppdateres manuelt for å endre avhengigheten fra MSBuild 14.0 (Visual Studio 2015) til MSBuild 15.0 (Visual Studio 2017) som beskrevet under [Oppdatere et eldre forløp i Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Brukeravatar 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Brukeravataren som vises til høyre i navigasjonsfeltet, ble hentet ved hjelp av en API fra Dynamics 365-hodekontrollen, som er avskrevet. |
| **Erstattet med en annen funksjon?**   | Brukerne får i stedet se initialene sine i en sirkel i navigasjonsfeltet. Dette er det samme visualobjektet som brukes på utviklingsmaskiner. |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Fjernet fra og med versjon 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Avskrivning av Enterprise Portal (EP)  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Metadataartefaktene som er knyttet til Dynamics AX 2012 Enterprise Portal (EP) er avskrevet fordi EP aldri ble støttet i Finance and Operations-appene. |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: All EP-kode er planlagt å fjernes i oktober 2021-versjonen. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.15 av Finance and Operations-apper

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-støtte for Dynamics 365 er avskrevet

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med desember 2020 er Microsoft Internet Explorer 11-støtte for alle Dynamics 365-produkter avskrevet, og Internet Explorer 11 støttes ikke etter august 2021.<br><br>Dette vil påvirke kunder som bruker Dynamics 365-produkter som er utformet for bruk via et Internet Explorer 11-grensesnitt. Etter august 2021 støttes ikke Internet Explorer 11 for slike Dynamics 365-produkter. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler at kundene går over til Microsoft Edge.|
| **Berørte produktområder**         | Alle Dynamics 365-produkter |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet: Internet Explorer 11 støttes ikke etter august 2021.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio-tillegg for å bruke hurtigreparasjoner for metadata

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Hurtigreparasjoner for metadata støttes ikke lenger med [Én versjon](../../fin-ops/get-started/one-version.md)-tjenesteoppdateringene som ble introdusert i juli 2018 med versjon 8.1. |
| **Erstattet med en annen funksjon?**   | Individuelle hurtigreparasjoner for metadata er ikke tilgjengelige for versjoner som støttes. Kumulative kvalitetsoppdateringer brukes i stedet. |
| **Berørte produktområder**         | Visual Studio-tillegg |
| **Distribusjonsalternativ**              | Virtuelle maskiner for utvikling |
| **Status**                         | Med versjon 10.0.15 er ikke tillegget lenger inkludert i Visual Studio-verktøyene. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.14 av Finance and Operations-apper

### <a name="online-users-page"></a>Siden Påloggede brukere 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dette er en eldre side som ble bygd for tidligere klient/server-arkitektur. Informasjonen på denne siden er ikke alltid nøyaktig, noe som kan være forvirrende og villedende. |
| **Erstattet med en annen funksjon?**   | Vi viser en ny side i en fremtidig oppdatering.|
| **Berørte produktområder**         | Systemadministrasjon |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Innen oktober 2021 blir dette skjemaet fjernet.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.13 av Finance and Operations-apper


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Egendefinert kode definert i SSRS-rapportegenskaper 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vanligvis tilbyr egendefinert kode begrensede fordeler og krever samtidig betydelige ressurser og databehandling for å støtte. Egendefinert kode brukes hovedsakelig av rapportforfattere for å kalle felles metoder fra en egendefinert kodesamling. Skybaserte tjenester støtter imidlertid ikke referanser til egendefinerte samlinger for SSRS-rapporter. |
| **Erstattet med en annen funksjon?**   | Rapportforfattere kan velge å fortsette å referere til offentlige .NET-API-er for matematiske operasjoner, konverteringsoperasjoner og formateringsoperasjoner fra et hvilket som helst tekstboksuttrykk. Hvis du vil ha mer informasjon, kan du se [Legge til kode i en rapport (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Berørte produktområder**         | Delsett av apprapportutforminger som er definert i RDL, som inneholder egendefinert kode. |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Med versjon 10.0.13 vil kompilatoren begynne å sende en advarsel for forekomster der egendefinert kode oppdages i en SSRS-rapportdefinisjon. Du kan løse problemet ved å åpne rapportutformingsdefinisjonen og fjerne alle egendefinerte kodeartefakter. Denne advarselen vil bli erstattet med en kompilatorfeil i en fremtidig oppdatering.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Oppgradering av tre jQuery-komponentbiblioteker 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Tre jQuery-komponentbiblioteker oppdateres for sikkerhetsreparasjoner og for å vedlikeholde valuta.   
| **Erstattet med en annen funksjon?**   | Følgende biblioteker blir berørt: jQuery (til versjon 3.5.0 fra versjon 2.1.4), jQuery-grensesnitt (til versjon 1.12.1 fra versjon 1.11.4), jQuery qTip (til versjon 3.0.3 fra 2.2.1). Migreringsveiledning er gitt på Internett av jQuery.  |
| **Berørte produktområder**         | Utvidbare kontroller, spesielt egendefinert JavaScript-kode med avskrevne eller fjernede APIer |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Med versjon 10.0.13/Platform Update 37 kan kunder valgfritt flytte til de nyeste bibliotekene ved å aktivere funksjonen "Oppgradering av tre jQuery-komponentbiblioteker". Flytting til de nye bibliotekene blir obligatoriske med april 2021-versjonen som gir tid for migrering av berørte APIer.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>API for eksisterende rutenettkontroll / forceLegacyGrid()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Den eksisterende rutenettkontrollen blir erstattet av den nye rutenettkontrollen. |
| **Erstattet med en annen funksjon?**   | Den [nye rutenettkontrollen](../..//fin-ops/get-started/grid-capabilities.md) |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | I versjon 10.0.13 er den nye rutenettkontrollen generelt tilgjengelig, og kunder kan eventuelt slå på denne funksjonen. Den nye rutenettkontrollen vil bli aktivert som standard med versjonen for oktober 2021 og er for øyeblikket obligatorisk i april 2022. Når den nye rutenettkontrollen blir obligatorisk, støttes ikke API-et **forceLegacyGrid()** lenger. |

### <a name="personalization-without-saved-views"></a>Tilpasning uten lagrede visninger 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Undersystemet for tilpasning har blitt oppgradert med funksjonen for lagrede visninger, så det har bedre ytelse og tilbyr flere funksjoner. |
| **Erstattet med en annen funksjon?**   | Lagrede visninger |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | I versjon 10.0.13 / Platform Update 37 er funksjonen for lagrede visninger generelt tilgjengelig, og kunder kan eventuelt aktivere denne funksjonen. Funksjonen for lagrede visninger blir obligatorisk i oktober 2021-versjonen. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.12 av Finance and Operations-apper

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Skjemautvidelser for rutenett- eller gruppekontroll som inneholder ugyldige feltreferanser

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Egenskapen datagruppe i rutenett- eller gruppekontroller brukes til automatisk å vise alle felt i en feltgruppe. Et rutenett eller en gruppekontroll som er lagt til via en utvidelse, kan inneholde felt som ikke lenger er definert i feltgruppen, eller de kan mangle felt som er definert i feltgruppen. Dette kan føre til inkonsekvent virkemåte ved kjøring. Plattformoppdateringer for versjon 10.0.12 av Finance and Operations-apper kategoriserer nå dette problemet som en kompilerings-*advarsel*. Du kan løse dette problemet ved å åpne skjemautvidelsen og lagre den.
| **Erstattet med en annen funksjon?**   | Denne kompilatoradvarselen vil bli erstattet med en kompilatorfeil i en fremtidig oppdatering. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | En kompilatoradvarsel er introdusert i plattformoppdateringer for versjon 10.0.12 av Finance and Operations-apper. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.11 av Finance and Operations-apper

### <a name="explicit-safe-lists-for-self-service-environments"></a>Eksplisitte hvitelister for selvbetjeningsmiljøer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Prosessen for å flytte IP til hvitelister er endret. Selvbetjening støtter ikke lenger IP-hvitlisting. |
| **Erstattet med en annen funksjon?**   | Hvis du vil ha mer informasjon, kan du se [Konfigurere betinget tilgang for Azure Active Directory](/appcenter/general/configuring-aad-conditional-access).|
| **Berørte produktområder**         | Sikkerhet |
| **Distribusjonsalternativ**              | Sky |
| **Status**                         | Avviklet: Denne funksjonen er fullstendig avviklet for selvbetjent distribusjon. |

### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å støtte de siste versjonene av Visual Studio må det gjøres enkelte endringer i X++-utvidelser for Visual Studio. Disse endringene er ikke kompatible med Visual Studio 2015. |
| **Erstattet med en annen funksjon?**   | Visual Studio 2017 vil erstatte Visual Studio 2015 som den distribuerte og påkrevde versjonen. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Virtual Machines distribuert på versjon 10.0.13 (Platform update 37) eller senere inneholder Visual Studio 2017. Versjon 10.0.16 (Platform update 40) er den endelige versjonen med støtte for Visual Studio 2015. Virtual machines med bare Visual Studio 2015 vil ikke kunne oppdatere til versjon 10.0.17 (Platform update 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Feltgrupper med ugyldige feltreferanser

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Feltgrupper i definisjoner av tabellmetadata kan inneholde feltreferanser som ikke er gyldige. Hvis disse feltgruppene er distribuert, kan dette føre til kjøretidsfeil for kjøring i Financial Reporting og Microsoft SQL Server Reporting Services (SSRS). Platform Update 23 innførte en kompilator-*advarsel* som muliggjorde håndtering av dette sikkerhetsproblemet. Plattformoppdateringer for versjon 10.0.11 av Finance and Operations-apper kategoriserer dette problemet som en kompilerings *feil*.<p>Følg fremgangsmåten nedenfor for å løse problemet.</p><ol><li>Fjern den ugyldige feltreferansen fra definisjonen for tabellfeltgruppen.</li><li>Kompiler på nytt.</li><li>Kontroller at eventuelle feil er tatt hånd om.</li></ol> |
| **Erstattet med en annen funksjon?**   | Denne kompileringsfeilen erstatter kompileringsadvarselen permanent.  |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Kompilatoradvarselen er en kompilatorfeil i plattformoppdateringer for versjon 10.0.11 av Finance and Operations-apper. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-lisenser opprettet ved hjelp av SHA1-nummeralgoritmen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Prosessen med å opprette uavhengige programvareleverandørlisenser (ISV) er endret. Hvis du vil ha mer informasjon, kan du se [Uavhengig programvareleverandørlisensiering (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Erstattet med en annen funksjon?**   | Ja. Bruk Windows PowerShell til å opprette lisenser. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: ISV-lisenser som ble opprettet ved hjelp av SHA1-nummeralgoritmen. Denne algoritmen er avhengig av sertifikater som ble opprettet ved hjelp av MakeCert-verktøyet, og dette verktøyet er avskrevet.<br><br>Avskrevet: Bruken av SHA1 for sikkerhet eller nummerering. SHA1 vil slutte å fungere tidlig i 2021. Derfor bør den ikke lenger brukes.<br><br>Fjernet: Støtte for Transport Layer Security (TLS)1.0 og TLS 1.1, innkommende eller utgående forespørsler. |

## <a name="platform-update-32"></a>Plattform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dette var et sikkerhetsproblem fordi endringsforespørselen kunne sendes til en utilsiktet bruker. Dette var også et bruksproblem, fordi det tvang brukeren til å finne ut hvem arbeidsflytavsenderen var, og manuelt velge dem.  |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Arbeidsflyt |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Rullegardinlisten for brukervalg ble fjernet fra dialogboksen for forespørselsendring i Platform Update 32. Forespørsler om forespørselsendring sendes automatisk til avsenderen som planlagt. Hvis du vil ha mer informasjon om denne funksjonaliteten, kan du se [Handlinger i godkjenningsprosesser i en arbeidsflyt](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Innebygde koblinger med detaljer som ikke lenger støttes i paginerte dokumenter som er gjengitt av den skybaserte tjenesten 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | URL-adresser for navigasjon som er innebygd i dokumenter som er gjengitt av tjenesten, kan inneholde sensitive forretningsdata. Vi fjerner støtte for innebygde gjennomgangskoblinger i dokumenter som et sikkerhetstiltak for å beskytte kundens data bedre. Brukere vil også dra nytte av forbedret ytelse samtidig som de får dokumenter på en proaktiv måte som følge av denne endringen.  |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Rapportering |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Denne funksjonen fjernes aktivt fra tjenesten.<br><br>Modern-klienten har mange alternativer for å produsere visninger som omfatter automatisk genererte koblinger som hjelp til å navigere i programmet. Paginerte dokumenter som er gjengitt av tjenesten, anbefales for ekstern kommunikasjon som sendes via e-post, arkiveres og skrives ut for mottakere. Vi har forbedret opplevelsen for forhåndsvisning av dokumenter direkte i Web-leseren, som gir direkte tilgang til lokale skrivere. Hvis du vil ha mer informasjon, se [Forhåndsvise PDF-dokumenter med et innebygd visningsprogram](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
