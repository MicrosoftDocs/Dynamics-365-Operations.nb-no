---
title: Tilbakestille data for finansrapportering etter gjenoppretting av en database
description: Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Finance and Operations-database.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: nb-no
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="8f146-103">Tilbakestille data for finansrapportering etter gjenoppretting av en database</span><span class="sxs-lookup"><span data-stu-id="8f146-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8f146-104">Dette emnet beskriver hvordan du tilbakestiller data for finansrapportering etter gjenoppretting av en Microsoft Dynamics 365 for Finance and Operations-database.</span><span class="sxs-lookup"><span data-stu-id="8f146-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="8f146-105">Hvis du gjenoppretter Finance and Operations-databasen fra en sikkerhetskopi eller kopierer databasen fra et annet miljø, må du følge trinnene i dette emnet for å sikre at data for finansrapportering bruker den gjenopprettede Finance and Operations-databasen på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="8f146-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="8f146-106">Fremgangsmåten i denne prosessen støttes for Dynamics 365 for Operations-versjonen fra mai 2016 (appbuild 7.0.1265.23014 og finansrapporteringsbuild 7.0.10000.4) og nyere versjoner.</span><span class="sxs-lookup"><span data-stu-id="8f146-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="8f146-107">Hvis du har en tidligere versjon av Finance and Operations, kan du kontakte vårt kundestøtteteam for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="8f146-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="8f146-108">Eksportere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="8f146-108">Export report definitions</span></span>
<span data-ttu-id="8f146-109">Eksporter først rapportutformingene i Rapportutforming ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="8f146-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="8f146-110">Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="8f146-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="8f146-111">Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="8f146-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="8f146-112">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="8f146-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="8f146-113">Velg rapportdefinisjonene som skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="8f146-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="8f146-114">Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.</span><span class="sxs-lookup"><span data-stu-id="8f146-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="8f146-115">Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, klikker du deretter den aktuelle kategorien og velger elementene som skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="8f146-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="8f146-116">Hvis du vil velge flere elementer i en kategori, trykker du og holder nede CTRL-tasten.</span><span class="sxs-lookup"><span data-stu-id="8f146-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="8f146-117">Når du velger rapporter å eksportere, velges tilhørende rader, kolonner, trær og dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="8f146-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="8f146-118">Klikk på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="8f146-118">Click **Export**.</span></span>
5.  <span data-ttu-id="8f146-119">Skriv inn et filnavn, og velger en sikkert plassering der du vil lagre de eksporterte rapportdefinisjonene.</span><span class="sxs-lookup"><span data-stu-id="8f146-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="8f146-120">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8f146-120">Click **Save**.</span></span>

<span data-ttu-id="8f146-121">Filen kan kopieres eller lastet opp til en sikker plassering, slik at den kan importeres til et annet miljø på et annet tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="8f146-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="8f146-122">Du finner informasjon om hvordan du bruker en Microsoft Azure-lagringskonto i [overføre data med kommandolinjeverktøyet AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="8f146-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="8f146-123">Microsoft tilbyr ingen lagringskonto som en del av Finance and Operations-avtalen.</span><span class="sxs-lookup"><span data-stu-id="8f146-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="8f146-124">Du må kjøpe en lagringskonto eller bruke en lagringskonto fra et eget Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f146-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="8f146-125">Vær oppmerksom på virkemåten til D-stasjonen på virtuelle Azure-maskiner.</span><span class="sxs-lookup"><span data-stu-id="8f146-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="8f146-126">Ikke lagre eksporterte byggeblokkgrupper her permanent.</span><span class="sxs-lookup"><span data-stu-id="8f146-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="8f146-127">Hvis du vil ha mer informasjon om midlertidige stasjoner, kan du se [Forstå den midlertidige stasjonen på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="8f146-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="8f146-128">Stoppe tjenester</span><span class="sxs-lookup"><span data-stu-id="8f146-128">Stop services</span></span>
<span data-ttu-id="8f146-129">Bruk Eksternt skrivebord til å koble til alle datamaskinene i miljøet, og stopp følgende Windows-tjenester ved hjelp av Services.msc:</span><span class="sxs-lookup"><span data-stu-id="8f146-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="8f146-130">Webpubliseringstjenesten (for alle AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="8f146-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="8f146-131">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="8f146-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="8f146-132">Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="8f146-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="8f146-133">Disse tjenestene vil ha åpne tilkoblinger til Dynamics 365 for Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="8f146-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="8f146-134">Tilbakestill</span><span class="sxs-lookup"><span data-stu-id="8f146-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="8f146-135">Finn og last ned den siste MinorVersionDataUpgrade.zip-pakken</span><span class="sxs-lookup"><span data-stu-id="8f146-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="8f146-136">Finn den nyeste MinorVersionDataUpgrade.zip-pakken ved hjelp av instruksjonene i [Last ned den nyeste distribuerbare dataoppgraderingspakken](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="8f146-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="8f146-137">Retningslinjene forklarer hvordan du finner og laster ned riktig versjon av dataoppgraderingspakken.</span><span class="sxs-lookup"><span data-stu-id="8f146-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="8f146-138">En oppgradering er ikke nødvendig for å laste ned MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="8f146-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="8f146-139">Du må bare fullføre trinnene i delen "Last ned den nyeste distribuerbare dataoppgraderingspakken" uten å utføre noen av de andre trinnene i artikkelen for å hente en kopi av MinorVersionDataUpgrade.zip-pakken.</span><span class="sxs-lookup"><span data-stu-id="8f146-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="8f146-140">Kjøre skript på Finance and Operations-databasen</span><span class="sxs-lookup"><span data-stu-id="8f146-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="8f146-141">Kjør skriptene nedenfor på Finance and Operations-databasen (ikke mot finansrapporteringsdatabasen).</span><span class="sxs-lookup"><span data-stu-id="8f146-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="8f146-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="8f146-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="8f146-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="8f146-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="8f146-144">Disse skriptene sikrer at innstillinger for brukere, roller og endringssporing er riktige.</span><span class="sxs-lookup"><span data-stu-id="8f146-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="8f146-145">Kjøre PowerShell-kommando for å tilbakestille databasen</span><span class="sxs-lookup"><span data-stu-id="8f146-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="8f146-146">Kjør følgende kommando, direkte på AOS-datamaskinen, for å tilbakestille integreringen mellom Finance and Operations og finansrapportering:</span><span class="sxs-lookup"><span data-stu-id="8f146-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="8f146-147">Åpne Windows PowerShell som Administrator.</span><span class="sxs-lookup"><span data-stu-id="8f146-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="8f146-148">Utfør: F:</span><span class="sxs-lookup"><span data-stu-id="8f146-148">Execute: F:</span></span>
3.  <span data-ttu-id="8f146-149">Utfør: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="8f146-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="8f146-150">Utfør: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="8f146-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="8f146-151">Utfør: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;min årsak til tilbakestilling&gt;”</span><span class="sxs-lookup"><span data-stu-id="8f146-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="8f146-152">Du blir bedt om å skrive inn "Y" for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="8f146-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="8f146-153">Forklaring av parameterne:</span><span class="sxs-lookup"><span data-stu-id="8f146-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="8f146-154">Gyldige verdier for -Reason er: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="8f146-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="8f146-155">Parameteren -ReasonDetail er fritekst.</span><span class="sxs-lookup"><span data-stu-id="8f146-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="8f146-156">Reason og reasonDetail blir registrert i telemetri / miljøovervåking.</span><span class="sxs-lookup"><span data-stu-id="8f146-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="8f146-157">Starte tjenester</span><span class="sxs-lookup"><span data-stu-id="8f146-157">Start services</span></span>
<span data-ttu-id="8f146-158">Bruk Services.msc til å starte tjenestene du stoppet tidligere:</span><span class="sxs-lookup"><span data-stu-id="8f146-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="8f146-159">Webpubliseringstjenesten (for alle AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="8f146-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="8f146-160">Partistyringstjenesten for Microsoft Dynamics 365 for Finance and Operations (bare for ikke-private AOS-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="8f146-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="8f146-161">Prosesstjenesten for Management Reporter 2012 (bare for BI-datamaskiner)</span><span class="sxs-lookup"><span data-stu-id="8f146-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="8f146-162">Importere rapportdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="8f146-162">Import report definitions</span></span>
<span data-ttu-id="8f146-163">Importer rapportutformingene fra Rapportutforming ved hjelp av filen som opprettes under eksporten:</span><span class="sxs-lookup"><span data-stu-id="8f146-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="8f146-164">Gå til **Firma** &gt; **Byggeblokkgrupper** i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="8f146-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="8f146-165">Velg byggeblokkgruppen du vil eksportere, og klikk på **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="8f146-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="8f146-166">For Finance and Operations støttes bare én byggeblokkgruppe, **Standard**.</span><span class="sxs-lookup"><span data-stu-id="8f146-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="8f146-167">Velg **Standard**-byggeblokken, og klikk på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="8f146-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="8f146-168">Velg filen som inneholder de eksporterte rapportdefinisjonene, og klikk på **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="8f146-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="8f146-169">I dialogboksen Importer velger rapportdefinisjonene som skal importers:</span><span class="sxs-lookup"><span data-stu-id="8f146-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="8f146-170">Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.</span><span class="sxs-lookup"><span data-stu-id="8f146-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="8f146-171">Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du rapporter, rader, kolonner, trær eller dimensjonssett som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="8f146-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="8f146-172">Klikk på **Importer**.</span><span class="sxs-lookup"><span data-stu-id="8f146-172">Click **Import**.</span></span>





