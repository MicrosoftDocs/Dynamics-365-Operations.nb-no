---
title: Systemkrav
description: Dette emnet viser systemkravene for gjeldende versjon av Microsoft Dynamics 365 for operasjoner.
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

Dette emnet viser systemkravene for gjeldende versjon av Microsoft Dynamics 365 for operasjoner.

<a name="supported-web-browsers"></a>Nettlesere som støttes
----------------------

Microsoft Dynamics-365 for webprogrammet for operasjoner kan kjøre i noen av følgende weblesere som kjører på operativsystemene som er angitt:

-   Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows-10
-   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
-   Google Chrome (siste offentlig tilgjengelige versjon) på Windows-10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10 tavle
-   Apple Safari (siste offentlig tilgjengelige versjon) på Mac OS X 10,10 (Yosemite), 10.11 (El Capitan) eller 10,12 (Sierra) eller Apple iPad

Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted. **Merknader:**

-   Hvis du vil spille inn bilder som genereres fra Oppgaveregistrering og inkludere dem i Microsoft Word-dokumenter, må du ha filtypen krom installert. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Redigeringsprogrammet for arbeidsflyt startes som en ClickOnce-program. Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer. Redigeringsprogrammet for arbeidsflyt ClickOnce-programmet krever en 64-biters-kompatibelt operativsystem.
-   Rapportgeneratoren for finansrapportering startes som en ClickOnce-program. Den krever en 64-biters-kompatibelt operativsystem. Hvis du bruker krom, må du installere en ClickOnce-utvidelse for å kunne laste ned rapport designer-klienten. Hvis du bruker krom i incognito modus, må du kontrollere ClickOnce-filtypen er også aktivert for incognito modus.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Støttede nettlesere for Skybasert salgssted for detaljhandel

Sky Kvitteringen for Dynamics 365 for operasjoner kan kjøre i noen av følgende weblesere som kjører på operativsystemene som er angitt:

-   Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows-10
-   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
-   Krom (siste offentlig tilgjengelige versjon) på Windows-10, Windows 8.1 eller Windows 7

## <a name="network-requirements"></a>Nettverkskrav til
-   Dynamics 365 for operasjoner er utformet for nettverk med ventetid på mindre enn 150 millisekunder (ms). Dette er ventetiden fra en klient leser til Microsoft Azure datasenteret som er vert for Dynamics 365 for operasjoner. Vi anbefaler at du tester nettverksventetid på <http://www.azurespeed.com>.
-   Båndbreddekrav for Dynamics 365 for operasjoner er avhengig av din situasjon. De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (KBps). Scenarier som har høy nyttelast krav, for eksempel arbeidsområder eller situasjoner som involverer omfattende tilpasning, anbefales mer båndbredde imidlertid.

Generelt er Dynamics 365 for operasjoner optimalisert for Internett. Antall rundturer fra en klient leser til Azure datasenteret er svært liten, og hele nyttelasten er komprimert. **Advarsel:** ikke beregne krav til båndbredde fra en klient ved å multiplisere antallet brukere med minimum båndbreddekravene. Samtidig bruk av en gitt lokasjon er veldig vanskelig å beregne. For kunder som er bekymret for krav til båndbredde, kan du bruke en forhåndsversjon av Dynamics 365 for operasjoner.

## <a name="net-framework-requirements"></a>.NET framework-krav
Dynamics 365 for operasjoner krever .NET Framework versjon 4.6.2 for alle Klikk-én gang programmer, for eksempel dokument ruting agenten. For å lese installasjonsinstrukser, kan du se [installere .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Støttede Microsoft Office-programmer
-   Hvis du vil kjøre Microsoft Excel og Word-tillegg, må du ha Microsoft Office 2016 for Windows eller Mac installert. Hvis du vil ha mer informasjon om versjonskrav til, kan du se [feilsøking av Office-integrasjon](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Hvis du vil vise dokumenter som er generert ved eksport til Excel eller Eksporter til Word-funksjonalitet, må ha Microsoft Office 2007 eller senere installert.

## <a name="retail-modern-pos-requirements"></a>Retail POS moderne krav
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Moderne Kvitteringen er et 32-biters program, men det kan kjøres på både x86 og x64 arkitekturer.
-   Moderne Priskontroll støttes bare på Windows 10 Pro, Enterprise og Enterprise lang sikt Vedlikehold gren (LTSB)-utgaver.

### <a name="minimum-system-requirements"></a>Minimum systemkrav

-   Den minste oppløsningen som støttes er 1280 × 1024.
-   Datamaskinen som kjører moderne Kvitteringen på må oppfylle disse kravene:
    -   Det må, som et minimum en dual core-prosessor som kjører på ikke mindre enn 2 GHz (gigahertz).
    -   Det må, som et minimum 3 gigabyte (GB) RAM.
    -   Den må ha Internett-tilgang.

## <a name="retail-hardware-station-requirements"></a>Detaljhandel maskinvarekrav for stasjonen
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Detaljhandel maskinvare station er et 32-biters program, men det kan kjøres på både x86 og x64 arkitekturer.
-   Detaljhandel maskinvare station støttes på følgende operativsystemer:
    -   Windows 7 Professional, Enterprise og Ultimate-utgaver **notat:** Windows 7 støttes bare hvis Internet Explorer 11 manuelt er installert på systemet.
    -   8.1 for Windows Update 1 Professional, Enterprise og innebygd utgaver
    -   Windows 10 Pro, Enterprise og LTSB for Enterprise-versjoner

### <a name="minimum-system-requirements"></a>Minimum systemkrav

Datamaskinen må oppfylle alle systemkrav for installasjon og bruk av følgende elementer:

-   Internet Information Services (IIS)
-   Tredjeparts maskinvare

## <a name="retail-store-scale-unit-requirements"></a>Retail Store skalaenheten krav
### <a name="supported-operating-systems"></a>Operativsystemer som støttes

-   Retail Store skala er et 32-biters program, men det kan kjøres på både x86 og x64 arkitekturer.
-   Retail Store skalaenheten støttes på følgende operativsystemer:
    -   Windows 7 Professional, Enterprise og Ultimate-utgaver
    -   8.1 for Windows Update 1 Professional, Enterprise og innebygd utgaver
    -   Windows 10 Pro, Enterprise og LTSB for Enterprise-versjoner

### <a name="minimum-system-requirements"></a>Minimum systemkrav

-   4 GB RAM
-   1,6 GHz maksimal CPU-hastighet per kjerne (to kjerner er minste.)
-   Minst 10 GB ledig plass (kanal-databasen kan kreve en stor mengde plass.)

### <a name="recommended-system-requirements"></a>Anbefalte systemkrav

-   6 GB RAM
-   2,4 GHz i7 (eller tilsvarende) maksimal CPU-hastighet per kjerne (fire kjerner anbefales.)
-   Minst 10 GB ledig plass (kanal-databasen kan kreve en stor mengde plass.)

## <a name="requirements-for-development-on-local-vms"></a>Krav for utviklingen av lokal VMs
Informasjon om kravene til utvikling på lokale virtuelle maskiner (VMs), kan du se [VM kjører på lokale](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Se også
--------

[Få en evalueringsversjon av Dynamics 365 for operasjoner](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


