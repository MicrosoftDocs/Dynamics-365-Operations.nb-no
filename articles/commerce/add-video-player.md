---
title: Videospillermodul
description: Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025667"
---
# <a name="video-player-module"></a><span data-ttu-id="b9124-103">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="b9124-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b9124-104">Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9124-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b9124-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b9124-105">Overview</span></span>

<span data-ttu-id="b9124-106">Videospillermodulen brukes til å støtte videoavspilling.</span><span class="sxs-lookup"><span data-stu-id="b9124-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="b9124-107">Den kan legges til på en hvilken som helst side, forutsatt at videoinnhold lastes opp til og er tilgjengelig i innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="b9124-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="b9124-108">Videospillermodulen støtter MP4-medietypen.</span><span class="sxs-lookup"><span data-stu-id="b9124-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="b9124-109">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="b9124-109">Video player module</span></span>

<span data-ttu-id="b9124-110">Videospillermodulen kan brukes til å vise videoer på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="b9124-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="b9124-111">Den støtter alle avspillingsfunksjoner, for eksempel spill av, pause, fullstørrelsesmodus, lydbeskrivelser og teksting for hørselshemmede.</span><span class="sxs-lookup"><span data-stu-id="b9124-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="b9124-112">Videospillermodulen støtter også tilpassing av teksting for hørselshemmede for å oppfylle Microsofts tilgjengelighetsstandarder.</span><span class="sxs-lookup"><span data-stu-id="b9124-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="b9124-113">Du kan for eksempel tilpasse skriftstørrelsen og bakgrunnsfargen.</span><span class="sxs-lookup"><span data-stu-id="b9124-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="b9124-114">Videospiller-modulen støtter også sekundære lydspor.</span><span class="sxs-lookup"><span data-stu-id="b9124-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="b9124-115">Når en video er lastet opp til CMS, kan du også laste opp et sekundært lydspor.</span><span class="sxs-lookup"><span data-stu-id="b9124-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="b9124-116">Videospiller-modulen kan deretter spille av det sekundære lydsporet hvis en bruker velger det.</span><span class="sxs-lookup"><span data-stu-id="b9124-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="b9124-117">Eksempler på omgivelsesvideospillermoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="b9124-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="b9124-118">Instruksjonsvideoer på produktdetaljsider eller markedsføringssider</span><span class="sxs-lookup"><span data-stu-id="b9124-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="b9124-119">Kampanjevideoer eller videoer om policyer på en hvilken som helst markedsføringsside</span><span class="sxs-lookup"><span data-stu-id="b9124-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="b9124-120">Markedsføringsvideoer som fremhever produktfunksjoner på sider med produktdetaljer eller markedsføringssider</span><span class="sxs-lookup"><span data-stu-id="b9124-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="b9124-121">Egenskaper for videospillermodul</span><span class="sxs-lookup"><span data-stu-id="b9124-121">Video player module properties</span></span>

| <span data-ttu-id="b9124-122">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="b9124-122">Property name</span></span>         | <span data-ttu-id="b9124-123">Verdi</span><span class="sxs-lookup"><span data-stu-id="b9124-123">Value</span></span>                               | <span data-ttu-id="b9124-124">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b9124-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="b9124-125">Automatisk avspilling</span><span class="sxs-lookup"><span data-stu-id="b9124-125">Auto play</span></span>             | <span data-ttu-id="b9124-126">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-126">**True** or **False**</span></span>               | <span data-ttu-id="b9124-127">Når verdien settes til **Sann**, spilles videoen automatisk.</span><span class="sxs-lookup"><span data-stu-id="b9124-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="b9124-128">Demp</span><span class="sxs-lookup"><span data-stu-id="b9124-128">Mute</span></span>                  | <span data-ttu-id="b9124-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-129">**True** or **False**</span></span>               | <span data-ttu-id="b9124-130">Når verdien settes til **Sann**, dempes lyden.</span><span class="sxs-lookup"><span data-stu-id="b9124-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="b9124-131">For denne spilleren er standardverdien **Usann**.</span><span class="sxs-lookup"><span data-stu-id="b9124-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="b9124-132">I Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="b9124-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="b9124-133">Løkke</span><span class="sxs-lookup"><span data-stu-id="b9124-133">Loop</span></span>                  | <span data-ttu-id="b9124-134">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-134">**True** or **False**</span></span>               | <span data-ttu-id="b9124-135">Når verdien settes til **Sann**, gjentas videoen i en løkke.</span><span class="sxs-lookup"><span data-stu-id="b9124-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="b9124-136">Medier</span><span class="sxs-lookup"><span data-stu-id="b9124-136">Media</span></span>                 | <span data-ttu-id="b9124-137">Filbane og -navn for video.</span><span class="sxs-lookup"><span data-stu-id="b9124-137">Video file path and name</span></span> | <span data-ttu-id="b9124-138">Videofilen som spilles av i videospilleren.</span><span class="sxs-lookup"><span data-stu-id="b9124-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="b9124-139">Spille av fullskjerm</span><span class="sxs-lookup"><span data-stu-id="b9124-139">Play fullscreen</span></span>       | <span data-ttu-id="b9124-140">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-140">**True** or **False**</span></span>               | <span data-ttu-id="b9124-141">Når verdien settes til **Sann**, spilles videoen automatisk i fullskjermmodus.</span><span class="sxs-lookup"><span data-stu-id="b9124-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="b9124-142">Utløser for avspilling/pause</span><span class="sxs-lookup"><span data-stu-id="b9124-142">Play pause trigger</span></span>    | <span data-ttu-id="b9124-143">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-143">**True** or **False**</span></span>               | <span data-ttu-id="b9124-144">Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen.</span><span class="sxs-lookup"><span data-stu-id="b9124-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="b9124-145">Kontroller for videospiller</span><span class="sxs-lookup"><span data-stu-id="b9124-145">Video player controls</span></span> | <span data-ttu-id="b9124-146">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-146">**True** or **False**</span></span>               | <span data-ttu-id="b9124-147">Når verdien settes til **Sann**, vises alle videospillerkontroller.</span><span class="sxs-lookup"><span data-stu-id="b9124-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="b9124-148">Disse kontrollene inkluderer knapper for spill av og pause, en fremdriftsindikator og alternativer for teksting for hørselshemmede.</span><span class="sxs-lookup"><span data-stu-id="b9124-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="b9124-149">Skjul plakatbilde</span><span class="sxs-lookup"><span data-stu-id="b9124-149">Hide poster image</span></span>     | <span data-ttu-id="b9124-150">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b9124-150">**True** or **False**</span></span>               | <span data-ttu-id="b9124-151">En video kan ha en plakatramme.</span><span class="sxs-lookup"><span data-stu-id="b9124-151">A video can have a poster frame.</span></span> <span data-ttu-id="b9124-152">Når verdien for denne egenskapen er satt til **Sann**, er plakatrammen skjult.</span><span class="sxs-lookup"><span data-stu-id="b9124-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="b9124-153">Maskenivå</span><span class="sxs-lookup"><span data-stu-id="b9124-153">Mask level</span></span>            | <span data-ttu-id="b9124-154">Et tall fra **0** til **100**</span><span class="sxs-lookup"><span data-stu-id="b9124-154">A number from **0** through **100**</span></span> | <span data-ttu-id="b9124-155">Masken som brukes på videoen for styling.</span><span class="sxs-lookup"><span data-stu-id="b9124-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="b9124-156">Legge til en videospillermodul på en side</span><span class="sxs-lookup"><span data-stu-id="b9124-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="b9124-157">Før du oppretter en videospillermodul, må du først laste opp en video til mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="b9124-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="b9124-158">Hvis du vil legge til en videospillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="b9124-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b9124-159">Opprett en sidemal som heter **videospillermal**.</span><span class="sxs-lookup"><span data-stu-id="b9124-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="b9124-160">I **Hoved**-sporet på standardsiden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="b9124-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="b9124-161">I containermodulen legger du til videospiller og omgivelsesvideospillermoduler.</span><span class="sxs-lookup"><span data-stu-id="b9124-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="b9124-162">Fullfør redigeringen av malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="b9124-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="b9124-163">Bruk videospillermalen du opprettet, for å opprette en side som heter **videospillerside**.</span><span class="sxs-lookup"><span data-stu-id="b9124-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="b9124-164">I **Hoved**-sporet på den nye siden legger du til en videospillermodul.</span><span class="sxs-lookup"><span data-stu-id="b9124-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="b9124-165">Velg **Legg til en video** i egenskapsruten for videospillermodulen.</span><span class="sxs-lookup"><span data-stu-id="b9124-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="b9124-166">Velg en video i dialogboksen **Medievelger**, og velg deretter **Last opp nytt medieelement** .</span><span class="sxs-lookup"><span data-stu-id="b9124-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="b9124-167">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="b9124-167">Save and preview the page.</span></span> <span data-ttu-id="b9124-168">Du skal se videomodulen på siden.</span><span class="sxs-lookup"><span data-stu-id="b9124-168">You should see the video module on the page.</span></span> <span data-ttu-id="b9124-169">Du kan endre flere innstillinger for å tilpasse virkemåten til modulen.</span><span class="sxs-lookup"><span data-stu-id="b9124-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="b9124-170">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="b9124-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9124-171">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b9124-171">Additional resources</span></span>

[<span data-ttu-id="b9124-172">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="b9124-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b9124-173">Kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="b9124-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b9124-174">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="b9124-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b9124-175">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b9124-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b9124-176">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b9124-176">Content block module</span></span>](add-hero-module.md)
