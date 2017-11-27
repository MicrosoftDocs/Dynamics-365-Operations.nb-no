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

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="e706b-103">Tilbakestille data for finansrapportering etter gjenoppretting av en database</span><span class="sxs-lookup"><span data-stu-id="e706b-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e706b-104">Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="e706b-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="e706b-105">Hvis du gjenoppretter Finance and Operations-databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø, må du følge trinnene i dette emnet for å sikre at data for finansrapportering bruker den gjenopprettede Finance and Operations-databasen på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="e706b-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="e706b-106">Fremgangsmåten i denne prosessen støttes for Dynamics 365 for Operations-versjonen fra mai 2016 (appbuild 7.0.1265.23014 og finansrapporteringsbuild 7.0.10000.4) og nyere versjoner.</span><span class="sxs-lookup"><span data-stu-id="e706b-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="e706b-107">Hvis du har en tidligere versjon av Finance and Operations, kan du kontakte vårt kundestøtteteam for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="e706b-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="e706b-108">Eksportere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="e706b-108">Export report definitions</span></span>
<span data-ttu-id="e706b-109">Eksporter først rapportutformingene i Rapportutforming ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="e706b-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="e706b-110">Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="e706b-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="e706b-111">Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="e706b-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="e706b-112">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="e706b-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="e706b-113">Velg rapportdefinisjonene som skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="e706b-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="e706b-114">Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.</span><span class="sxs-lookup"><span data-stu-id="e706b-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="e706b-115">Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, klikker du deretter den aktuelle kategorien og velger elementene som skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="e706b-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="e706b-116">Trykk og hold inne Ctrl-tasten for å velge flere varer i en kategori. Når du velger rapporter som skal eksporteres, velges de tilhørende radene, kolonnene, trærne og dimensjonssettene.</span><span class="sxs-lookup"><span data-stu-id="e706b-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="e706b-117">Klikk på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="e706b-117">Click **Export**.</span></span>
5.  <span data-ttu-id="e706b-118">Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.</span><span class="sxs-lookup"><span data-stu-id="e706b-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="e706b-119">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e706b-119">Click **Save**.</span></span>

<span data-ttu-id="e706b-120">Filen kan kopieres eller lastet opp til en sikker plassering, slik at den kan importeres til et annet miljø på et annet tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="e706b-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="e706b-121">Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [overføre data med kommandolinjeverktøyet AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="e706b-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="e706b-122">Microsoft tilbyr ingen lagringskonto som en del av Finance and Operations-avtalen.</span><span class="sxs-lookup"><span data-stu-id="e706b-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="e706b-123">Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="e706b-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="e706b-124">Vær oppmerksom på virkemåten til D-stasjonen på virtuelle Azure-maskiner.</span><span class="sxs-lookup"><span data-stu-id="e706b-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="e706b-125">Ikke lagre eksporterte byggeblokkgrupper her permanent.</span><span class="sxs-lookup"><span data-stu-id="e706b-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="e706b-126">Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="e706b-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="e706b-127">Stoppe tjenester</span><span class="sxs-lookup"><span data-stu-id="e706b-127">Stop services</span></span>
<span data-ttu-id="e706b-128">Bruk Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og stopp følgende Windows-tjenester ved hjelp av Services.msc:</span><span class="sxs-lookup"><span data-stu-id="e706b-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="e706b-129">Webpubliseringstjenesten (for alle AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="e706b-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="e706b-130">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="e706b-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="e706b-131">Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="e706b-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="e706b-132">Disse tjenestene vil ha åpne tilkoblinger til Dynamics 365 for Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="e706b-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="e706b-133">Tilbakestill</span><span class="sxs-lookup"><span data-stu-id="e706b-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="e706b-134">Finn og last ned den siste MinorVersionDataUpgrade.zip-pakken</span><span class="sxs-lookup"><span data-stu-id="e706b-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="e706b-135">Finn den nyeste MinorVersionDataUpgrade.zip-pakken ved hjelp av instruksjonene i [Last ned den nyeste distribuerbare dataoppgraderingspakken](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="e706b-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="e706b-136">Retningslinjene forklarer hvordan du finner og laster ned riktig versjon av dataoppgraderingspakken.</span><span class="sxs-lookup"><span data-stu-id="e706b-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="e706b-137">En oppgradering er ikke nødvendig for å laste ned MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="e706b-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e706b-138">Du må bare fullføre trinnene i delen "Last ned den nyeste distribuerbare dataoppgraderingspakken" uten å utføre noen av de andre trinnene i artikkelen for å hente en kopi av MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="e706b-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="e706b-139">Kjøre skript på Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="e706b-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="e706b-140">Kjør skriptene nedenfor på Finance and Operations-databasen (ikke mot finansrapporteringsdatabasen).</span><span class="sxs-lookup"><span data-stu-id="e706b-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="e706b-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="e706b-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="e706b-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="e706b-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="e706b-143">Disse skriptene sikrer at innstillinger for brukere, roller og endringssporing er riktige.</span><span class="sxs-lookup"><span data-stu-id="e706b-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="e706b-144">Kjøre PowerShell-kommando for å tilbakestille databasen</span><span class="sxs-lookup"><span data-stu-id="e706b-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="e706b-145">På AOS-datamaskinen, utfør følgende kommandoer i PowerShell som administrator for å tilbakestille integrering mellom Finance and Operations og finansiell rapportering:</span><span class="sxs-lookup"><span data-stu-id="e706b-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="e706b-146">Etter å ha utført kommandoen bes du om å skrive «Y» for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="e706b-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="e706b-147">Forklaring av parameterne:</span><span class="sxs-lookup"><span data-stu-id="e706b-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="e706b-148">Gyldige verdier for -Reason er: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="e706b-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="e706b-149">Parameteren -ReasonDetail er fritekst.</span><span class="sxs-lookup"><span data-stu-id="e706b-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="e706b-150">Reason og reasonDetail blir registrert i telemetri / miljøovervåking.</span><span class="sxs-lookup"><span data-stu-id="e706b-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="e706b-151">Starte tjenester</span><span class="sxs-lookup"><span data-stu-id="e706b-151">Start services</span></span>
<span data-ttu-id="e706b-152">Bruk Services.msc til å starte tjenestene du stoppet tidligere:</span><span class="sxs-lookup"><span data-stu-id="e706b-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="e706b-153">Webpubliseringstjenesten (for alle AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="e706b-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="e706b-154">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="e706b-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="e706b-155">Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="e706b-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="e706b-156">Importere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="e706b-156">Import report definitions</span></span>
<span data-ttu-id="e706b-157">Importer rapportutformingene fra Rapportutforming ved hjelp av filen som opprettes under eksporten:</span><span class="sxs-lookup"><span data-stu-id="e706b-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="e706b-158">Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="e706b-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="e706b-159">Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="e706b-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e706b-160">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="e706b-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="e706b-161">Velg **Standard**-byggeblokken, og klikk på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="e706b-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="e706b-162">Velg filen som inneholder de eksporterte rapportdefinisjonene, og klikk på **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="e706b-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="e706b-163">I dialogboksen Importer velger rapportdefinisjonene som skal importers:</span><span class="sxs-lookup"><span data-stu-id="e706b-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="e706b-164">Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.</span><span class="sxs-lookup"><span data-stu-id="e706b-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="e706b-165">Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du rapporter, rader, kolonner, trær eller dimensjonssett som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="e706b-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="e706b-166">Klikk på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="e706b-166">Click **Import**.</span></span>





