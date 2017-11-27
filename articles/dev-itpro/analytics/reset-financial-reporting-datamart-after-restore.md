---
title: Tilbakestille data for finansrapportering etter gjenoppretting av en database
description: Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Finance and Operations-database.
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Tilbakestille data for finansrapportering etter gjenoppretting av en database

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Finance and Operations-database.

Hvis du gjenoppretter Finance and Operations-databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø, må du følge trinnene i dette emnet for å sikre at data for finansrapportering bruker den gjenopprettede Finance and Operations-databasen på riktig måte. 
> [!Note] 
> Fremgangsmåten i denne prosessen støttes for Dynamics 365 for Operations-versjonen fra mai 2016 (appbuild 7.0.1265.23014 og finansrapporteringsbuild 7.0.10000.4) og nyere versjoner. Hvis du har en tidligere versjon av Finance and Operations, kan du kontakte vårt kundestøtteteam for å få hjelp.

## <a name="export-report-definitions"></a>Eksportere rapportdefinisjoner
Eksporter først rapportutformingene i Rapportutforming ved å gjøre følgende:

1.  Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.
2.  Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**. 

    > [!Note] 
    > For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.
    
3.  Velg rapportdefinisjonene som skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, klikker du deretter den aktuelle kategorien og velger elementene som skal eksporteres. Trykk og hold inne Ctrl-tasten for å velge flere varer i en kategori. Når du velger rapporter som skal eksporteres, velges de tilhørende radene, kolonnene, trærne og dimensjonssettene.

4.  Klikk på **Eksporter**.
5.  Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.
6.  Klikk på **Lagre**.

Filen kan kopieres eller lastet opp til en sikker plassering, slik at den kan importeres til et annet miljø på et annet tidspunkt. Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [overføre data med kommandolinjeverktøyet AzCopy](/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft tilbyr ingen lagringskonto som en del av Finance and Operations-avtalen. Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement. 
> [!WARNING]
> Vær oppmerksom på virkemåten til D-stasjonen på virtuelle Azure-maskiner. Ikke lagre eksporterte byggeblokkgrupper her permanent. Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stoppe tjenester
Bruk Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og stopp følgende Windows-tjenester ved hjelp av Services.msc:

-   Webpubliseringstjenesten (for alle AOS-datamaskiner)
-   Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)
-   Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)

Disse tjenestene vil ha åpne tilkoblinger til Dynamics 365 for Finance and Operations-databasen.

## <a name="reset"></a>Tilbakestill
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Finn og last ned den siste MinorVersionDataUpgrade.zip-pakken

Finn den nyeste MinorVersionDataUpgrade.zip-pakken ved hjelp av instruksjonene i [Last ned den nyeste distribuerbare dataoppgraderingspakken](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Retningslinjene forklarer hvordan du finner og laster ned riktig versjon av dataoppgraderingspakken. En oppgradering er ikke nødvendig for å laste ned MinorVersionDataUpgrade.zip-pakken. Du må bare fullføre trinnene i delen "Last ned den nyeste distribuerbare dataoppgraderingspakken" uten å utføre noen av de andre trinnene i artikkelen for å hente en kopi av MinorVersionDataUpgrade.zip-pakken.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Kjøre skript på Finance and Operations-databasen

Kjør skriptene nedenfor på Finance and Operations-databasen (ikke mot finansrapporteringsdatabasen).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse skriptene sikrer at innstillinger for brukere, roller og endringssporing er riktige.

### <a name="execute-powershell-command-to-reset-database"></a>Kjøre PowerShell-kommando for å tilbakestille databasen

På AOS-datamaskinen, utfør følgende kommandoer i PowerShell som administrator for å tilbakestille integrering mellom Finance and Operations og finansiell rapportering:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Etter å ha utført kommandoen bes du om å skrive «Y» for å bekrefte.

Forklaring av parameterne:

-   Gyldige verdier for -Reason er: SERVICING, BADDATA, OTHER.
-   Parameteren -ReasonDetail er fritekst.
-   Reason og reasonDetail blir registrert i telemetri / miljøovervåking.

## <a name="start-services"></a>Starte tjenester
Bruk Services.msc til å starte tjenestene du stoppet tidligere:

-   Webpubliseringstjenesten (for alle AOS-datamaskiner)
-   Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)
-   Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)

## <a name="import-report-definitions"></a>Importere rapportdefinisjoner
Importer rapportutformingene fra Rapportutforming ved hjelp av filen som opprettes under eksporten:

1.  Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.
2.  Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**. 

    > [!NOTE]
    > For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.
    
3.  Velg **Standard**-byggeblokken, og klikk på **Importer**.
4.  Velg filen som inneholder de eksporterte rapportdefinisjonene, og klikk på **Åpne**.
5.  I dialogboksen Importer velger rapportdefinisjonene som skal importers:
    -   Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du rapporter, rader, kolonner, trær eller dimensjonssett som skal importeres.

6.  Klikk på **Importer**.





