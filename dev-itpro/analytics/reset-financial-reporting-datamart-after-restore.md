---
title: "Tilbakestill økonomisk rapportering oppstillingsdatabasen etter gjenoppretting av en database"
description: "Dette emnet beskriver hvordan du tilbakestiller økonomisk rapportering oppstillingsdatabasen etter gjenoppretting av en Microsoft Dynamics-365 for operasjoner databasen."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Tilbakestill økonomisk rapportering oppstillingsdatabasen etter gjenoppretting av en database

Dette emnet beskriver hvordan du tilbakestiller økonomisk rapportering oppstillingsdatabasen etter gjenoppretting av en Microsoft Dynamics-365 for operasjoner databasen. 

Det finnes flere scenarier der du må kanskje gjenopprette din Dynamics 365 for operasjoner databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø. Når dette skjer, må du også følgende fremgangsmåte for å sikre at økonomisk rapportering oppstillingsdatabasen er riktig ved hjelp av den gjenopprettede Dynamics 365 for operasjoner databasen. Hvis du har spørsmål om hvordan du tilbakestiller økonomisk rapportering oppstillingsdatabasen grunn utenfor gjenoppretter en Dynamics 365 for operasjoner-databasen, kan du se den [tilbakestiller Management Reporter oppstillingsdatabasen](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for mer informasjon. Legg merke til at trinnene i denne prosessen støttes for Dynamics 365 for operasjonen mai 2016 release (App build 7.0.1265.23014 og finansiell rapportering build 7.0.10000.4) og nyere versjoner. Hvis du har en tidligere versjon av Dynamics 365 for operasjoner, kontakt vår kundestøtte for å få hjelp.

## <a name="export-report-definitions"></a>Eksportere rapportdefinisjoner
Først, eksportere rapport utformingene i rapportgeneratoren, ved å gjøre følgende:

1.  Rapportgeneratoren, gå til **selskapet**&gt;**byggeblokk grupper**.
2.  Velg byggeblokk gruppen du vil eksportere, og klikk **eksportere**. **Merk:** For Dynamics 365 for operasjoner, støttes bare en byggeblokk-gruppen, **standard**.
3.  Velg hvilke rapportdefinisjoner skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, klikker du deretter den aktuelle kategorien og velger elementene som skal eksporteres. Hvis du vil velge flere elementer i en kategori, trykker du og holder nede CTRL-tasten. Når du velger rapporter for å eksportere, merkes de tilhørende rader, kolonner, trær og dimensjonssett.

4.  Klikk **eksportere**.
5.  Skriv inn et filnavn og velger et sikkert sted der du vil lagre de eksporterte rapportdefinisjonene.
6.  Click **Save**.

Filen kan kopieres eller lastet opp til et sikkert sted, slik at det skal importeres til et annet miljø på et annet tidspunkt. Du finner informasjon om hvordan du bruker en Microsoft Azure lagring konto i [overføre data med AzCopy for verktøyet](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Merk:** Microsoft gir ikke en konto for lagring som en del av Dynamics-365 for operasjoner avtale. Du må kjøpe en konto for lagring, eller du kan bruke en lagring konto fra et eget Azure abonnement. **Viktig:** Vær oppmerksom på virkemåten til D-stasjonen på Azure virtuelle maskiner. Ikke holde eksporterte byggeblokk-grupper her permanent. Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [forstå midlertidig stasjon på Windows Azure virtuelle maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stopp tjenester
Bruke eksternt skrivebord til å koble til alle datamaskinene i miljøet og stoppe følgende Windows-tjenester ved hjelp av services.msc:

-   World wide web-publiseringstjenesten (for alle AOS-datamaskiner)
-   Microsoft Dynamics-365 for operasjoner satsvise Management Service (for ikke-private AOS datamaskiner bare)
-   Tjenesten for Management Reporter 2012 prosessen (for BI datamaskiner)

Disse tjenestene må åpne tilkoblinger til Dynamics-365 for databasen for operasjoner.

## <a name="reset"></a>Tilbakestill
#### <a name="locate-the-latest-dataupgradezip-package"></a>Finn den nyeste DataUpgrade.zip-pakken

Finn den nyeste DataUpgrade.zip-pakken ved hjelp av instruksjonene i [laste ned skriptet DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). Retningslinjene forklarer hvordan du finner riktig versjon av oppgraderingspakken data for ditt miljø.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Kjøre skript mot Dynamics 365 for databasen for operasjoner

Kjøre skriptene nedenfor mot Dynamics-365 for operasjoner databasen (ikke mot økonomiske rapporteringsdatabasen).

-   DataUpgrade.zip\\AosService\\skript\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\skript\\GrantAzViewChangeTracking.sql

Disse skriptene sikrer at brukere, roller og endringssporing innstillingene er riktige.

#### <a name="execute-powershell-command-to-reset-database"></a>Kjøre PowerShell-kommando for å nullstille databasen

Kjør følgende kommando, direkte på AOS-datamaskinen for å tilbakestille integreringen mellom Dynamics 365 for operasjoner og finansiell rapportering:

1.  Åpne Windows PowerShell som Administrator.
2.  Kjøre: F:
3.  Kjør: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Kjør: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Kjør: Reset-DatamartIntegration-andre grunn - ReasonDetail "&lt;grunnen min for å tilbakestille&gt;"
    -   Du blir bedt om å skrive inn "Y" for å bekrefte.

Forklaring av parameterne:

-   Gyldige verdier for - årsaken er: Vedlikehold, BADDATA, OTHER.
-   ReasonDetail - parameteren er fri tekst.
-   Årsak og reasonDetail blir registrert i overvåking av telemetry/miljø.

## <a name="start-services"></a>Start tjenester
Bruk services.msc for å starte tjenestene du stoppet tidligere:

-   World wide web-publiseringstjenesten (for alle AOS-datamaskiner)
-   Microsoft Dynamics-365 for operasjoner satsvise Management Service (for ikke-private AOS datamaskiner bare)
-   Tjenesten for Management Reporter 2012 prosessen (for BI datamaskiner)

## <a name="import-report-definitions"></a>Importere rapportdefinisjoner
Importere utformingene rapport fra rapportgeneratoren, ved hjelp av filen opprettes under eksport:

1.  Rapportgeneratoren, gå til **selskapet**&gt;**byggeblokk grupper**.
2.  Velg byggeblokk gruppen du vil eksportere, og klikk **eksportere**. **Merk:** For Dynamics 365 for operasjoner, støttes bare en byggeblokk-gruppen, **standard**.
3.  Velg den **standard** bygger blokk, og klikk **Import**.
4.  Velg filen som inneholder definisjonene for eksporterte rapporten, og klikk **åpne**.
5.  I dialogboksen Importer velger rapportdefinisjonene som skal importers:
    -   Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du rapporter, rader, kolonner, trær eller dimensjonssett som skal importeres.

6.  Click **Import**.



