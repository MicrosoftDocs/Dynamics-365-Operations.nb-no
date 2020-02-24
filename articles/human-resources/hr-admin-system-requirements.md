---
title: Systemkrav
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72379e91ace61f5e33ac6cab259b5c32902c7b3b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010020"
---
# <a name="system-requirements"></a><span data-ttu-id="862d7-102">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="862d7-102">System requirements</span></span>

<span data-ttu-id="862d7-103">Denne artikkelen beskriver kravene til Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="862d7-103">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="862d7-104">Det beskriver også landene og områdene der Human Resources er tilgjengelig, og informasjon om språk og lokalisering for Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="862d7-104">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="862d7-105">Nettlesere som støttes</span><span class="sxs-lookup"><span data-stu-id="862d7-105">Supported web browsers</span></span>

<span data-ttu-id="862d7-106">Human Resources kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene:</span><span class="sxs-lookup"><span data-stu-id="862d7-106">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="862d7-107">Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10</span><span class="sxs-lookup"><span data-stu-id="862d7-107">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="862d7-108">Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="862d7-108">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="862d7-109">Google Chrome (nyeste offentlig tilgjengelig versjon)</span><span class="sxs-lookup"><span data-stu-id="862d7-109">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="862d7-110">Apple Safari (nyeste offentlig tilgjengelig versjon)</span><span class="sxs-lookup"><span data-stu-id="862d7-110">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="862d7-111">Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted.</span><span class="sxs-lookup"><span data-stu-id="862d7-111">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="862d7-112">Hvis du vil ta skjermbilder som genereres fra Oppgaveopptaker, og inkludere dem i Microsoft Word-dokumenter, må du ha Chrome-tillegget installert.</span><span class="sxs-lookup"><span data-stu-id="862d7-112">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="862d7-113">Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="862d7-113">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="862d7-114">Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer.</span><span class="sxs-lookup"><span data-stu-id="862d7-114">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="862d7-115">ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.</span><span class="sxs-lookup"><span data-stu-id="862d7-115">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="862d7-116">Hvis du vil forhåndsvise PDF-filer, anbefaler vi at du bruker moderne nettlesere som Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows 10 eller Google Chrome (siste offentlig tilgjengelige versjon) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-nettbrett.</span><span class="sxs-lookup"><span data-stu-id="862d7-116">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="862d7-117">Nettverkskrav</span><span class="sxs-lookup"><span data-stu-id="862d7-117">Network requirements</span></span>
> * <span data-ttu-id="862d7-118">Human Resources er utformet for nettverk med ventetid på 250 til 300 millisekunder (ms) eller mindre.</span><span class="sxs-lookup"><span data-stu-id="862d7-118">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="862d7-119">Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="862d7-119">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="862d7-120">Vi anbefaler at du tester nettverksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test av ventetid for Azure").</span><span class="sxs-lookup"><span data-stu-id="862d7-120">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="862d7-121">Krav til båndbredde for Human Resources avhenger av scenarioet.</span><span class="sxs-lookup"><span data-stu-id="862d7-121">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="862d7-122">De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kbps).</span><span class="sxs-lookup"><span data-stu-id="862d7-122">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="862d7-123">Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav.</span><span class="sxs-lookup"><span data-stu-id="862d7-123">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="862d7-124">Samtidig bruk av en bestemt plassering er svært vanskelig å beregne.</span><span class="sxs-lookup"><span data-stu-id="862d7-124">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="862d7-125">Kunder som er bekymret for krav til båndbredde, kan bruke en prøveversjon av Human Resources.</span><span class="sxs-lookup"><span data-stu-id="862d7-125">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="862d7-126">Microsoft Office-programmer som støttes</span><span class="sxs-lookup"><span data-stu-id="862d7-126">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="862d7-127">Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert.</span><span class="sxs-lookup"><span data-stu-id="862d7-127">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="862d7-128">Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](../dev-itpro/office-integration/office-integration-troubleshooting.md "Feilsøke Office-integrering").</span><span class="sxs-lookup"><span data-stu-id="862d7-128">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="862d7-129">Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.</span><span class="sxs-lookup"><span data-stu-id="862d7-129">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="862d7-130">Regional tilgjengelighet, språk og lokalisering</span><span class="sxs-lookup"><span data-stu-id="862d7-130">Regional availability, languages, and localization</span></span>

<span data-ttu-id="862d7-131">Du kan laste ned en PDF-fil med landene, områdene og språkene Human Resources støtter, på [Internasjonal tilgjengelighet for Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="862d7-131">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="862d7-132">Selv om brukergrensesnittet er lokalisert til andre språk, lagres alle brukerdata på språket de ble lagt inn på.</span><span class="sxs-lookup"><span data-stu-id="862d7-132">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="862d7-133">Du kan opprette e-postmeldinger og maler på andre språk, men data som planleggingsinformasjon er bare tilgjengelig på engelsk for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="862d7-133">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="862d7-134">Hvis du er utvikler og interessert i å lage lands- eller områdespesifikke tilpasninger, eller hvis du vil opprette en løsning for et land eller område som ikke støttes av Microsoft for øyeblikket, kan du se [Globalisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="862d7-134">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>
