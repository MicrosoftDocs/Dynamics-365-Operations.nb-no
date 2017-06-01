---
title: Tilbakestille data for finansrapportering etter gjenoppretting av en database
description: Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Operations-database.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d227452e48914170404f0ee5163a05e6b875e69f
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Tilbakestille data for finansrapportering etter gjenoppretting av en database

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Operations-database. 

Det finnes flere scenarier der du kanskje må gjenopprette din Dynamics 365 for Operations-database fra en sikkerhetskopi eller kopierer databasen fra et annet miljø. Når dette skjer, må du også følge riktig fremgangsmåte for å sikre at dataene for finansrapportering bruker den gjenopprettede Dynamics 365 for Operations-databasen på riktig måte. Hvis du har spørsmål om hvordan du tilbakestiller data for finansrapportering av en annen grunn enn gjenoppretting av en Dynamics 365 for Operations-database, kan du se [Tilbakestille data for Management Reporter](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for mer informasjon. Legg merke til at fremgangsmåten i denne prosessen støttes for Dynamics 365 for Operations-versjonen fra mai 2016 (appbuild 7.0.1265.23014 og finansrapporteringsbuild 7.0.10000.4) og nyere versjoner. Hvis du har en tidligere versjon av Dynamics 365 for Operations, kan du kontakte vårt kundestøtteteam for å få hjelp.

## <a name="export-report-definitions"></a>Eksportere rapportdefinisjoner
Eksporter først rapportutformingene i Rapportutforming ved å gjøre følgende:

1.  Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.
2.  Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**. **Obs!** For Dynamics 365 for Operations støttes bare én byggeblokkgruppe, **Standard**.
3.  Velg rapportdefinisjonene som skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, klikker du deretter den aktuelle kategorien og velger elementene som skal eksporteres. Hvis du vil velge flere elementer i en kategori, trykker du og holder nede CTRL-tasten. Når du velger rapporter å eksportere, velges tilhørende rader, kolonner, trær og dimensjonssett.

4.  Klikk på **Eksporter**.
5.  Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.
6.  Klikk på **Lagre**.

Filen kan kopieres eller lastet opp til en sikker plassering, slik at den kan importeres til et annet miljø på et annet tidspunkt. Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [overføre data med kommandolinjeverktøyet AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft tilbyr ingen lagringskonto som en del av Dynamics 365 for Operations-avtalen. Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement. 
> [!WARNING]
> Vær oppmerksom på virkemåten til D-stasjonen på virtuelle Azure-maskiner. Ikke lagre eksporterte byggeblokkgrupper her permanent. Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stoppe tjenester
Bruk Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og stopp følgende Windows-tjenester ved hjelp av Services.msc:

-   Webpubliseringstjenesten (for alle AOS-datamaskiner)
-   Partistyringstjenesten for Microsoft Dynamics 365 for Operations (bare for ikke-private AOS-datamaskiner)
-   Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)

Disse tjenestene vil ha åpne tilkoblinger til Dynamics 365 for Operations-databasen.

## <a name="reset"></a>Tilbakestill
#### <a name="locate-the-latest-dataupgradezip-package"></a>Finn den nyeste DataUpgrade.zip-pakken

Finn den nyeste DataUpgrade.zip-pakken ved hjelp av instruksjonene i [Laste ned DataUpgrade.zip-skriptet](..\migration-upgrade\upgrade-data-to-latest-update.md). Retningslinjene forklarer hvordan du finner riktig versjon av dataoppgraderingspakken for ditt miljø.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Kjøre skript på Dynamics 365 for Operations-databasen

Kjør skriptene nedenfor på Dynamics 365 for Operations-databasen (ikke mot finansrapporteringsdatabasen).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse skriptene sikrer at innstillinger for brukere, roller og endringssporing er riktige.

#### <a name="execute-powershell-command-to-reset-database"></a>Kjøre PowerShell-kommando for å tilbakestille databasen

Kjør følgende kommando, direkte på AOS-datamaskinen, for å tilbakestille integreringen mellom Dynamics 365 for Operations og finansrapportering:

1.  Åpne Windows PowerShell som Administrator.
2.  Utfør: F:
3.  Utfør: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Utfør: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Utfør: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;min årsak til tilbakestilling&gt;”
    -   Du blir bedt om å skrive inn "Y" for å bekrefte.

Forklaring av parameterne:

-   Gyldige verdier for -Reason er: SERVICING, BADDATA, OTHER.
-   Parameteren -ReasonDetail er fritekst.
-   Reason og reasonDetail blir registrert i telemetri / miljøovervåking.

## <a name="start-services"></a>Starte tjenester
Bruk Services.msc til å starte tjenestene du stoppet tidligere:

-   Webpubliseringstjenesten (for alle AOS-datamaskiner)
-   Partistyringstjenesten for Microsoft Dynamics 365 for Operations (bare for ikke-private AOS-datamaskiner)
-   Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)

## <a name="import-report-definitions"></a>Importere rapportdefinisjoner
Importer rapportutformingene fra Rapportutforming ved hjelp av filen som opprettes under eksporten:

1.  Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.
2.  Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**. 
    > [!NOTE]
    > For Dynamics 365 for Operations støttes bare én byggeblokkgruppe, **Standard**.
3.  Velg **Standard**-byggeblokken, og klikk på **Importer**.
4.  Velg filen som inneholder de eksporterte rapportdefinisjonene, og klikk på **Åpne**.
5.  I dialogboksen Importer velger rapportdefinisjonene som skal importers:
    -   Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du rapporter, rader, kolonner, trær eller dimensjonssett som skal importeres.

6.  Klikk på **Importer**.





