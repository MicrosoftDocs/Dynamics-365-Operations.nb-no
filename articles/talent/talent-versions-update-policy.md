---
title: Systemkrav og oppdateringspolicy for Talent
description: Dette emnet viser kravene for Dynamics 365 for Talent. Oppdateringspolicyen blir også gjennomgått.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 64362ae9e4ebb63ca6da2cd2f41376d1d9047694
ms.sourcegitcommit: c6af2de37309b574dcb69c9caad436b55136600f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2019
ms.locfileid: "768491"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="8f14a-104">Systemkrav og oppdateringspolicy for Talent</span><span class="sxs-lookup"><span data-stu-id="8f14a-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f14a-105">Dette emnet viser kravene for Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="8f14a-105">This topic lists requirements for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="8f14a-106">Oppdateringspolicyen blir også gjennomgått.</span><span class="sxs-lookup"><span data-stu-id="8f14a-106">The update policy is outlined, as well.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="8f14a-107">Nettlesere som støttes</span><span class="sxs-lookup"><span data-stu-id="8f14a-107">Supported web browsers</span></span>

<span data-ttu-id="8f14a-108">Microsoft Dynamics 365 for Talent-webprogrammet kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:</span><span class="sxs-lookup"><span data-stu-id="8f14a-108">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="8f14a-109">Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10</span><span class="sxs-lookup"><span data-stu-id="8f14a-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="8f14a-110">Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f14a-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="8f14a-111">Google Chrome (nyeste offentlig tilgjengelig versjon)</span><span class="sxs-lookup"><span data-stu-id="8f14a-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="8f14a-112">Apple Safari (nyeste offentlig tilgjengelig versjon)</span><span class="sxs-lookup"><span data-stu-id="8f14a-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="8f14a-113">Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted.</span><span class="sxs-lookup"><span data-stu-id="8f14a-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="8f14a-114">Hvis du vil ta skjermbilder som genereres fra Oppgaveopptaker, og inkludere dem i Microsoft Word-dokumenter, må du ha Chrome-tillegget installert.</span><span class="sxs-lookup"><span data-stu-id="8f14a-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="8f14a-115">Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="8f14a-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="8f14a-116">Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer.</span><span class="sxs-lookup"><span data-stu-id="8f14a-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="8f14a-117">ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.</span><span class="sxs-lookup"><span data-stu-id="8f14a-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="8f14a-118">Hvis du vil forhåndsvise PDF-filer, anbefaler vi at du bruker moderne nettlesere som Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows 10 eller Google Chrome (siste offentlig tilgjengelige versjon) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-nettbrett.</span><span class="sxs-lookup"><span data-stu-id="8f14a-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="8f14a-119">Nettverkskrav</span><span class="sxs-lookup"><span data-stu-id="8f14a-119">Network requirements</span></span>
> * <span data-ttu-id="8f14a-120">Dynamics 365 for Talent er utformet for nettverk med ventetid på 250 til 300 millisekunder (ms) eller mindre.</span><span class="sxs-lookup"><span data-stu-id="8f14a-120">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="8f14a-121">Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="8f14a-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="8f14a-122">Vi anbefaler at du tester nettverksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test av ventetid for Azure").</span><span class="sxs-lookup"><span data-stu-id="8f14a-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="8f14a-123">Krav til båndbredde for Dynamics 365 for Talent avhenger av scenarioet.</span><span class="sxs-lookup"><span data-stu-id="8f14a-123">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="8f14a-124">De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kbps).</span><span class="sxs-lookup"><span data-stu-id="8f14a-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="8f14a-125">Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav.</span><span class="sxs-lookup"><span data-stu-id="8f14a-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="8f14a-126">Samtidig bruk av en bestemt plassering er svært vanskelig å beregne.</span><span class="sxs-lookup"><span data-stu-id="8f14a-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="8f14a-127">Kunder som er bekymret for krav til båndbredde, kan bruke en prøveversjon av Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="8f14a-127">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="8f14a-128">Microsoft Office-programmer som støttes</span><span class="sxs-lookup"><span data-stu-id="8f14a-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="8f14a-129">Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert.</span><span class="sxs-lookup"><span data-stu-id="8f14a-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="8f14a-130">Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](../dev-itpro/office-integration/office-integration-troubleshooting.md "Feilsøke Office-integrering").</span><span class="sxs-lookup"><span data-stu-id="8f14a-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="8f14a-131">Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.</span><span class="sxs-lookup"><span data-stu-id="8f14a-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="update-policy"></a><span data-ttu-id="8f14a-132">Oppdateringspolicy</span><span class="sxs-lookup"><span data-stu-id="8f14a-132">Update policy</span></span>

<span data-ttu-id="8f14a-133">Microsoft Dynamics 365 for Talent betjenes som et skytilbud.</span><span class="sxs-lookup"><span data-stu-id="8f14a-133">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="8f14a-134">Oppdateringer til Dynamics 365 for Talent er kontinuerlig og brukes automatisk av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f14a-134">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="8f14a-135">Oppdateringer utgis regelmessig til alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="8f14a-135">Updates are released on a regular cadence, updates will be made to all environments.</span></span>  <span data-ttu-id="8f14a-136">Dynamics 365 for Talent støttes i henhold til [Microsoft Support Lifecycle-policyen](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), som gir konsekvente og forutsigbare retningslinjer for tilgjengelighet av produktstøtte.</span><span class="sxs-lookup"><span data-stu-id="8f14a-136">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
