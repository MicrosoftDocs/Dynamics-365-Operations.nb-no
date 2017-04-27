---
title: Systemkrav
description: I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Operations.
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Systemkrav

I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Operations.

<a name="supported-web-browsers"></a>Nettlesere som støttes
----------------------

Webprogrammet Microsoft Dynamics 365 for Operations kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:

-   Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
-   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
-   Google Chrome (nyeste offentlig tilgjengelig versjon) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller på Google Nexus 10-nettbrett
-   Apple Safari (nyeste offentlig tilgjengelig versjon) i Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) eller på Apple iPad

Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted. **Merknader:**

-   Hvis du vil ta skjermbilder som genereres fra Oppgaveopptaker, og ta dem med i Microsoft Word-dokumenter, må du ha en Chrome-tillegget installert. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program. Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer. ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.
-   Rapportutforming for finansrapportering startes som et ClickOnce-program. Det krever et 64-biters kompatibelt operativsystem. Hvis du bruker Chrome, må du installere et ClickOnce-tillegg for å kunne laste ned klienten for rapportutforming. Hvis du bruker Chrome i inkognitomodus, må du kontrollere at ClickOnce-tillegget også er aktivert for inkognitomodus.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Støttede nettlesere for Skybasert salgssted for detaljhandel

Skybasert salgssted for detaljhandel for Microsoft Dynamics 365 for Operations kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:

-   Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
-   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
-   Chrome (nyeste offentlig tilgjengelige versjon) i Windows 10, Windows 8.1 eller Windows 7

## <a name="network-requirements"></a>Nettverkskrav
-   Dynamics 365 for Operations er utformet for nettverk med ventetid på mindre enn 150 millisekunder (ms). Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Dynamics 365 for Operations. Vi anbefaler at du tester nettverksventetiden på <http://www.azurespeed.com>.
-   Båndbreddekrav for Dynamics 365 for Operations er avhengig av scenariet. De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kbps). For scenarier som har krav til høy nyttelast, for eksempel arbeidsområder eller scenarier med omfattende tilpassing, anbefales imidlertid mer båndbredde.

Generelt er Dynamics 365 for Operations optimalisert for Internett. Antall rundturer fra en nettleserklient til Azure-datasenteret er svært lite, og hele nyttelasten er komprimert. **Advarsel! ** Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav. Samtidig bruk av en bestemt plassering er svært vanskelig å beregne. Kunder som er bekymret for krav til båndbredde kan bruke en forhåndsversjon av Dynamics 365 for Operations.

## <a name="net-framework-requirements"></a>.NET Framework-krav
Dynamics 365 for Operations krever .NET Framework versjon 4.6.2 for alle ClickOnce-programmer, for eksempel dokumentrutingsagenten. Hvis du vil lese installasjonsinstruksjonene, kan du se [Installere .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Microsoft Office-programmer som støttes
-   Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert. Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.

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
    -   Utgavene Windows 7 Professional, Enterprise og Ultimate **Obs! ** Windows 7 støttes bare hvis Internet Explorer 11 er installert manuelt på systemet.
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

## <a name="requirements-for-development-on-local-vms"></a>Krav for utvikling på lokale virtuelle maskiner
Hvis du vil ha informasjon om kravene til utvikling på lokale virtuelle maskiner (VM-er), kan du se [Virtuelle maskiner som kjører lokalt](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Se også
--------

[Få en evalueringsversjon av Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


