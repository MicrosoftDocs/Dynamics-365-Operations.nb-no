---
title: Systemkrav for skydistribusjoner
description: I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for distribusjoner i skyen.
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="cba39-103">Systemkrav for skydistribusjoner</span><span class="sxs-lookup"><span data-stu-id="cba39-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cba39-104">I dette emnet finner du systemkravene for den gjeldende versjonen av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for distribusjoner i skyen.</span><span class="sxs-lookup"><span data-stu-id="cba39-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="cba39-105">Før du installerer Finance and Operations, om nødvendig, kontroller at systemet du arbeider med, oppfyller eller overskrider minimumskravene til nettverk, maskinvare og programvare.</span><span class="sxs-lookup"><span data-stu-id="cba39-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="cba39-106">Nettlesere som støttes</span><span class="sxs-lookup"><span data-stu-id="cba39-106">Supported web browsers</span></span>
<span data-ttu-id="cba39-107">Webprogrammet kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:</span><span class="sxs-lookup"><span data-stu-id="cba39-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="cba39-108">Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10</span><span class="sxs-lookup"><span data-stu-id="cba39-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="cba39-109">Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="cba39-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="cba39-110">Google Chrome (nyeste offentlig tilgjengelig versjon) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller på Google Nexus 10-nettbrett</span><span class="sxs-lookup"><span data-stu-id="cba39-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="cba39-111">Apple Safari (nyeste offentlig tilgjengelig versjon) i Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) eller på Apple iPad</span><span class="sxs-lookup"><span data-stu-id="cba39-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="cba39-112">Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted.</span><span class="sxs-lookup"><span data-stu-id="cba39-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="cba39-113">En forhåndsversjon av Chrome-tillegget må installeres for å kunne ta skjermbilder med Oppgaveopptaker, og ta dem med i genererte Microsoft Word-dokumenter.</span><span class="sxs-lookup"><span data-stu-id="cba39-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="cba39-114">Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="cba39-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="cba39-115">Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer.</span><span class="sxs-lookup"><span data-stu-id="cba39-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="cba39-116">ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.</span><span class="sxs-lookup"><span data-stu-id="cba39-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="cba39-117">Rapportutforming for finansrapportering startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="cba39-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="cba39-118">Det krever et 64-biters kompatibelt operativsystem.</span><span class="sxs-lookup"><span data-stu-id="cba39-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="cba39-119">Hvis du bruker Chrome, må du installere et ClickOnce-tillegg for å kunne laste ned klienten for rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="cba39-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="cba39-120">Hvis du bruker Chrome i inkognitomodus, må du kontrollere at ClickOnce-tillegget også er aktivert for inkognitomodus.</span><span class="sxs-lookup"><span data-stu-id="cba39-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="cba39-121">Hvis du vil forhåndsvise PDF-filer, anbefaler vi at du bruker nettlesere som Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows 10 eller Google Chrome (siste offentlig tilgjengelige versjon) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-nettbrett.</span><span class="sxs-lookup"><span data-stu-id="cba39-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="cba39-122">Støttede nettlesere for Skybasert salgssted for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="cba39-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="cba39-123">Retail Cloud POS kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:</span><span class="sxs-lookup"><span data-stu-id="cba39-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="cba39-124">Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10</span><span class="sxs-lookup"><span data-stu-id="cba39-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="cba39-125">Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="cba39-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="cba39-126">Chrome (nyeste offentlig tilgjengelige versjon) i Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="cba39-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="cba39-127">Nettverkskrav</span><span class="sxs-lookup"><span data-stu-id="cba39-127">Network requirements</span></span>
-   <span data-ttu-id="cba39-128">Finance and Operations er utformet for nettverk som har en ventetid på 250 til 300 millisekunder (ms) eller mindre.</span><span class="sxs-lookup"><span data-stu-id="cba39-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="cba39-129">Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cba39-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="cba39-130">Vi anbefaler at du tester nettverksventetiden på <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="cba39-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="cba39-131">Båndbreddekrav for Finance and Operations er avhengig av scenariet.</span><span class="sxs-lookup"><span data-stu-id="cba39-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="cba39-132">De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kbps).</span><span class="sxs-lookup"><span data-stu-id="cba39-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="cba39-133">For scenarier som har krav til høy nyttelast, for eksempel arbeidsområder eller scenarier med omfattende tilpassing, anbefales imidlertid mer båndbredde.</span><span class="sxs-lookup"><span data-stu-id="cba39-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="cba39-134">Generelt er Finance and Operations optimalisert for Internett.</span><span class="sxs-lookup"><span data-stu-id="cba39-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="cba39-135">Antall rundturer fra en nettleserklient til Azure-datasenteret er svært lite, og hele nyttelasten er komprimert.</span><span class="sxs-lookup"><span data-stu-id="cba39-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="cba39-136">Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav.</span><span class="sxs-lookup"><span data-stu-id="cba39-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="cba39-137">Samtidig bruk av en bestemt plassering er svært vanskelig å beregne.</span><span class="sxs-lookup"><span data-stu-id="cba39-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="cba39-138">Kunder som er bekymret for krav til båndbredde, bør bruke en forhåndsversjon av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cba39-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="cba39-139">.NET Framework-krav</span><span class="sxs-lookup"><span data-stu-id="cba39-139">.NET Framework requirements</span></span>
<span data-ttu-id="cba39-140">Finance and Operations krever Microsoft .NET Framework versjon 4.6.2 for alle ClickOnce-programmer, for eksempel dokumentrutingsagenten.</span><span class="sxs-lookup"><span data-stu-id="cba39-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="cba39-141">Hvis du vil lese installasjonsinstruksjonene, kan du se [Installere .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="cba39-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="cba39-142">Microsoft Office-programmer som støttes</span><span class="sxs-lookup"><span data-stu-id="cba39-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="cba39-143">Følgende Microsoft Office-programmer støttes i skyen og lokale installasjonene av Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cba39-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="cba39-144">Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert.</span><span class="sxs-lookup"><span data-stu-id="cba39-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="cba39-145">Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="cba39-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="cba39-146">Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.</span><span class="sxs-lookup"><span data-stu-id="cba39-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="cba39-147">Krav for moderne salgssted for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="cba39-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="cba39-148">Hvis moderne salgssted for detaljhandel skal bruke en frakoblet database, må datamaskinen oppfylle alle systemkrav for Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cba39-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="cba39-149">En frakoblet database for moderne salgssted for detaljhandel virker på Microsoft SQL Server 2012 med Service Pack 3 eller senere, Microsoft SQL Server 2014 med Service Pack 2 eller senere og Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="cba39-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="cba39-150">Vi anbefaler at du alltid bruke den nyeste versjonen som er tilgjengelig, og at du installerer alle de nyeste oppdateringspakkene.</span><span class="sxs-lookup"><span data-stu-id="cba39-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="cba39-151">Operativsystemer som støttes</span><span class="sxs-lookup"><span data-stu-id="cba39-151">Supported operating systems</span></span>

-   <span data-ttu-id="cba39-152">Moderne salgssted for detaljhandel er et 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="cba39-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="cba39-153">Moderne salgssted for detaljhandel støttes bare på utgavene Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).</span><span class="sxs-lookup"><span data-stu-id="cba39-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="cba39-154">Minimumskrav til systemet</span><span class="sxs-lookup"><span data-stu-id="cba39-154">Minimum system requirements</span></span>

-   <span data-ttu-id="cba39-155">Den minste oppløsningen som støttes er 1 280 × 1 024.</span><span class="sxs-lookup"><span data-stu-id="cba39-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="cba39-156">Datamaskinen som kjører moderne salgssted for detaljhandel må oppfylle disse kravene:</span><span class="sxs-lookup"><span data-stu-id="cba39-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="cba39-157">Den må, som minimum en dual core-prosessor som kjører på ikke mindre enn 2 GHz (gigahertz).</span><span class="sxs-lookup"><span data-stu-id="cba39-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="cba39-158">Den må ha minimum 3 GB (gigabyte) RAM.</span><span class="sxs-lookup"><span data-stu-id="cba39-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="cba39-159">Den må ha Internett-tilgang.</span><span class="sxs-lookup"><span data-stu-id="cba39-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="cba39-160">Krav til maskinvarestasjon for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="cba39-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="cba39-161">Operativsystemer som støttes</span><span class="sxs-lookup"><span data-stu-id="cba39-161">Supported operating systems</span></span>

-   <span data-ttu-id="cba39-162">Maskinvarestasjon for detaljhandel er et 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="cba39-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="cba39-163">Maskinvarestasjon for detaljhandel støttes på følgende operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="cba39-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="cba39-164">Utgavene Windows 7 Professional, Enterprise og Ultimate</span><span class="sxs-lookup"><span data-stu-id="cba39-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="cba39-165">Windows 7 støttes bare hvis Internet Explorer 11 installeres manuelt på systemet.</span><span class="sxs-lookup"><span data-stu-id="cba39-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="cba39-166">Utgavene Windows 8.1 Update 1 Professional, Enterprise og Embedded</span><span class="sxs-lookup"><span data-stu-id="cba39-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="cba39-167">Utgavene Windows 10 Pro, Enterprise og Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="cba39-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="cba39-168">Minimumskrav til systemet</span><span class="sxs-lookup"><span data-stu-id="cba39-168">Minimum system requirements</span></span>

<span data-ttu-id="cba39-169">Datamaskinen må oppfylle alle systemkrav for installasjon og bruk av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="cba39-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="cba39-170">Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="cba39-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="cba39-171">Tredjepartsmaskinvare</span><span class="sxs-lookup"><span data-stu-id="cba39-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="cba39-172">Krav for skalaenhet for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="cba39-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="cba39-173">Operativsystemer som støttes</span><span class="sxs-lookup"><span data-stu-id="cba39-173">Supported operating systems</span></span>

-   <span data-ttu-id="cba39-174">Skalaenhet for detaljhandel er et 32-biters program, men det kan kjøres på både x86- og x64 arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="cba39-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="cba39-175">Skalaenhet for detaljhandel støttes på følgende operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="cba39-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="cba39-176">Utgavene Windows 7 Professional, Enterprise og Ultimate</span><span class="sxs-lookup"><span data-stu-id="cba39-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="cba39-177">Utgavene Windows 8.1 Update 1 Professional, Enterprise og Embedded</span><span class="sxs-lookup"><span data-stu-id="cba39-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="cba39-178">Utgavene Windows 10 Pro, Enterprise og Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="cba39-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="cba39-179">Minimumskrav til systemet</span><span class="sxs-lookup"><span data-stu-id="cba39-179">Minimum system requirements</span></span>

-   <span data-ttu-id="cba39-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="cba39-180">4 GB of RAM</span></span>
-   <span data-ttu-id="cba39-181">1,6 GHz maksimal CPU-hastighet per kjerne (to kjerner er minimum)</span><span class="sxs-lookup"><span data-stu-id="cba39-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="cba39-182">Minst 10 GB ledig plass (kanaldatabasen kan kreve svært mye plass)</span><span class="sxs-lookup"><span data-stu-id="cba39-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="cba39-183">Anbefalte systemkrav</span><span class="sxs-lookup"><span data-stu-id="cba39-183">Recommended system requirements</span></span>

-   <span data-ttu-id="cba39-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="cba39-184">6 GB of RAM</span></span>
-   <span data-ttu-id="cba39-185">2,4 GHz i7 (eller tilsvarende) maksimal CPU-hastighet per kjerne (fire kjerner anbefales)</span><span class="sxs-lookup"><span data-stu-id="cba39-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="cba39-186">Minst 10 GB ledig plass (kanaldatabasen kan kreve svært mye plass)</span><span class="sxs-lookup"><span data-stu-id="cba39-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="cba39-187">Krav til kobling</span><span class="sxs-lookup"><span data-stu-id="cba39-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="cba39-188">Operativsystemer som støttes</span><span class="sxs-lookup"><span data-stu-id="cba39-188">Supported operating systems</span></span>

-   <span data-ttu-id="cba39-189">Koblingen for Microsoft Dynamics AX har to separate installasjonsprogram, en for Async Server Connector-tjeneste og en for Real-time service for Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="cba39-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="cba39-190">Begge komponentene er 32-biters program, men de kan kjøres på både x86- og x64 arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="cba39-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="cba39-191">Begge komponentene støttes på følgende operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="cba39-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="cba39-192">Utgavene Windows 7 Professional, Enterprise og Ultimate</span><span class="sxs-lookup"><span data-stu-id="cba39-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="cba39-193">Utgavene Windows 8.1 Update 1 Professional, Enterprise og Embedded</span><span class="sxs-lookup"><span data-stu-id="cba39-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="cba39-194">Utgavene Windows 10 Pro, Enterprise og Enterprise LTSB</span><span class="sxs-lookup"><span data-stu-id="cba39-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="cba39-195">Microsoft Windows Server 2012 R2 og Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cba39-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="cba39-196">Minimumskrav til systemet</span><span class="sxs-lookup"><span data-stu-id="cba39-196">Minimum system requirements</span></span>
-   <span data-ttu-id="cba39-197">2 GB RAM (4 GB RAM anbefales.)</span><span class="sxs-lookup"><span data-stu-id="cba39-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="cba39-198">1,6 GHz maksimal CPU-hastighet per kjerne (to kjerner er minimum)</span><span class="sxs-lookup"><span data-stu-id="cba39-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="cba39-199">Minst 10 GB ledig plass (kanaldatabasen kan kreve svært mye plass)</span><span class="sxs-lookup"><span data-stu-id="cba39-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="cba39-200">Krav for utvikling på lokale virtuelle maskiner</span><span class="sxs-lookup"><span data-stu-id="cba39-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="cba39-201">Hvis du vil ha informasjon om kravene til utvikling på lokale virtuelle maskiner (VM-er), kan du se [Virtuelle maskiner som kjører lokalt](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="cba39-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="cba39-202">Se også</span><span class="sxs-lookup"><span data-stu-id="cba39-202">See also</span></span>

[<span data-ttu-id="cba39-203">Få en evalueringskopi av Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="cba39-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

