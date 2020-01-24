---
title: Videospillermodul
description: Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885907"
---
# <a name="video-player-module"></a><span data-ttu-id="e2343-103">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="e2343-103">Video player module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e2343-104">Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2343-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e2343-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e2343-105">Overview</span></span>

<span data-ttu-id="e2343-106">Videospillermoduler brukes til å støtte videoavspilling.</span><span class="sxs-lookup"><span data-stu-id="e2343-106">Video player modules are used to support video playback.</span></span> <span data-ttu-id="e2343-107">To videospillermoduler finnes i startpakken for butikk: modulen for omgivelsesvideospiller og videospillermodulen.</span><span class="sxs-lookup"><span data-stu-id="e2343-107">Two video player modules are provided in the store starter kit: the ambient video player module and the video player module.</span></span> <span data-ttu-id="e2343-108">Begge spillerne støtter MP4-medietypen.</span><span class="sxs-lookup"><span data-stu-id="e2343-108">Both players support the .mp4 media type.</span></span>

## <a name="ambient-video-player-module"></a><span data-ttu-id="e2343-109">Omgivelsesvideospillermodul</span><span class="sxs-lookup"><span data-stu-id="e2343-109">Ambient video player module</span></span>

<span data-ttu-id="e2343-110">Omgivelsesvideospillermodulen støtter korte informasjonsvideoer.</span><span class="sxs-lookup"><span data-stu-id="e2343-110">The ambient video player module supports short informational videos.</span></span> <span data-ttu-id="e2343-111">Den bør brukes for videoer som er mindre enn fem sekunder lange.</span><span class="sxs-lookup"><span data-stu-id="e2343-111">It should be used for videos that are less than five seconds long.</span></span> <span data-ttu-id="e2343-112">Denne spilleren støtter funksjoner for begrenset videoavspilling, for eksempel avspilling og pause.</span><span class="sxs-lookup"><span data-stu-id="e2343-112">This player supports limited video playback capabilities, such as play and pause.</span></span>

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a><span data-ttu-id="e2343-113">Eksempler på videospillermoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="e2343-113">Examples of ambient video player modules in e-Commerce</span></span>

- <span data-ttu-id="e2343-114">Kort informasjonsvideoer som uthever nye produkter på startsiden</span><span class="sxs-lookup"><span data-stu-id="e2343-114">Short informational videos that highlight new products on the home page</span></span>
- <span data-ttu-id="e2343-115">Korte informasjonsvideoer som fremhever produktfunksjoner på en produktdetaljside</span><span class="sxs-lookup"><span data-stu-id="e2343-115">Short informational videos that highlight product features on a product details page</span></span>

### <a name="ambient-video-player-module-properties"></a><span data-ttu-id="e2343-116">Egenskaper for omgivelsesvideospillermodul</span><span class="sxs-lookup"><span data-stu-id="e2343-116">Ambient video player module properties</span></span>

| <span data-ttu-id="e2343-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="e2343-117">Property name</span></span>     | <span data-ttu-id="e2343-118">Verdi</span><span class="sxs-lookup"><span data-stu-id="e2343-118">Value</span></span>                 | <span data-ttu-id="e2343-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e2343-119">Description</span></span> |
|-------------------|-----------------------|-------------|
| <span data-ttu-id="e2343-120">Autokjør</span><span class="sxs-lookup"><span data-stu-id="e2343-120">Autoplay</span></span>          | <span data-ttu-id="e2343-121">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-121">**True** or **False**</span></span> | <span data-ttu-id="e2343-122">Når verdien settes til **Sann**, spilles videoen automatisk.</span><span class="sxs-lookup"><span data-stu-id="e2343-122">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="e2343-123">Demp</span><span class="sxs-lookup"><span data-stu-id="e2343-123">Mute</span></span>              | <span data-ttu-id="e2343-124">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-124">**True** or **False**</span></span> | <span data-ttu-id="e2343-125">Når verdien settes til **Sann**, dempes lyden.</span><span class="sxs-lookup"><span data-stu-id="e2343-125">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="e2343-126">For denne spilleren er standardverdien **Sann**.</span><span class="sxs-lookup"><span data-stu-id="e2343-126">For this player, the default value is **True**.</span></span> <span data-ttu-id="e2343-127">I Google Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="e2343-127">In the Google Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="e2343-128">Løkke</span><span class="sxs-lookup"><span data-stu-id="e2343-128">Loop</span></span>              | <span data-ttu-id="e2343-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-129">**True** or **False**</span></span> | <span data-ttu-id="e2343-130">Når verdien settes til **Sann**, gjentas videoen i en løkke.</span><span class="sxs-lookup"><span data-stu-id="e2343-130">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="e2343-131">Medier</span><span class="sxs-lookup"><span data-stu-id="e2343-131">Media</span></span>             |  <span data-ttu-id="e2343-132">Filbane og -navn for video.</span><span class="sxs-lookup"><span data-stu-id="e2343-132">Video file path and name</span></span> | <span data-ttu-id="e2343-133">Videofilen som spilles av videospilleren.</span><span class="sxs-lookup"><span data-stu-id="e2343-133">The video file that is played by the video player.</span></span> |
| <span data-ttu-id="e2343-134">Avspillingskontroller</span><span class="sxs-lookup"><span data-stu-id="e2343-134">Playback controls</span></span> | <span data-ttu-id="e2343-135">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-135">**True** or **False**</span></span> | <span data-ttu-id="e2343-136">Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen.</span><span class="sxs-lookup"><span data-stu-id="e2343-136">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="e2343-137">Hvis verdien er satt til **Usann**, vises ikke knappen spill av / pause, men brukerne kan fremdeles stoppe og fortsette videoen ved hjelp av tastaturet.</span><span class="sxs-lookup"><span data-stu-id="e2343-137">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |

## <a name="video-player-module"></a><span data-ttu-id="e2343-138">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="e2343-138">Video player module</span></span>

<span data-ttu-id="e2343-139">Videospillermodulen kan brukes til å vise videoer på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="e2343-139">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="e2343-140">Den støtter alle avspillingsfunksjoner, for eksempel spill av, pause, fullstørrelsesmodus og teksting for hørselshemmede.</span><span class="sxs-lookup"><span data-stu-id="e2343-140">It supports all playback capabilities, such as play, pause, full-size mode, and closed captions.</span></span> <span data-ttu-id="e2343-141">Videospillermodulen støtter også tilpassing av teksting for hørselshemmede for å oppfylle Microsofts tilgjengelighetsstandarder.</span><span class="sxs-lookup"><span data-stu-id="e2343-141">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="e2343-142">Du kan for eksempel tilpasse skriftstørrelsen og bakgrunnsfargen.</span><span class="sxs-lookup"><span data-stu-id="e2343-142">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="e2343-143">Videospiller-modulen støtter også sekundære lydspor.</span><span class="sxs-lookup"><span data-stu-id="e2343-143">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="e2343-144">Når en video er lastet opp, kan du også laste opp et sekundært lydspor.</span><span class="sxs-lookup"><span data-stu-id="e2343-144">When a video is uploaded, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="e2343-145">Videospiller-modulen kan deretter spille av det sekundære lydsporet hvis en bruker velger det.</span><span class="sxs-lookup"><span data-stu-id="e2343-145">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="e2343-146">Eksempler på omgivelsesvideospillermoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="e2343-146">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="e2343-147">Instruksjonsvideoer på produktdetaljsider eller markedsføringssider</span><span class="sxs-lookup"><span data-stu-id="e2343-147">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="e2343-148">Kampanjevideoer eller videoer om policyer på en hvilken som helst markedsføringsside</span><span class="sxs-lookup"><span data-stu-id="e2343-148">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="e2343-149">Markedsføringsvideoer som fremhever produktfunksjoner på sider med produktdetaljer eller markedsføringssider</span><span class="sxs-lookup"><span data-stu-id="e2343-149">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="e2343-150">Egenskaper for videospillermodul</span><span class="sxs-lookup"><span data-stu-id="e2343-150">Video player module properties</span></span>

| <span data-ttu-id="e2343-151">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="e2343-151">Property name</span></span>         | <span data-ttu-id="e2343-152">Verdi</span><span class="sxs-lookup"><span data-stu-id="e2343-152">Value</span></span>                               | <span data-ttu-id="e2343-153">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e2343-153">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="e2343-154">Automatisk avspilling</span><span class="sxs-lookup"><span data-stu-id="e2343-154">Auto play</span></span>             | <span data-ttu-id="e2343-155">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-155">**True** or **False**</span></span>               | <span data-ttu-id="e2343-156">Når verdien settes til **Sann**, spilles videoen automatisk.</span><span class="sxs-lookup"><span data-stu-id="e2343-156">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="e2343-157">Demp</span><span class="sxs-lookup"><span data-stu-id="e2343-157">Mute</span></span>                  | <span data-ttu-id="e2343-158">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-158">**True** or **False**</span></span>               | <span data-ttu-id="e2343-159">Når verdien settes til **Sann**, dempes lyden.</span><span class="sxs-lookup"><span data-stu-id="e2343-159">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="e2343-160">For denne spilleren er standardverdien **Usann**.</span><span class="sxs-lookup"><span data-stu-id="e2343-160">For this player, the default value is **False**.</span></span> <span data-ttu-id="e2343-161">I Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="e2343-161">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="e2343-162">Løkke</span><span class="sxs-lookup"><span data-stu-id="e2343-162">Loop</span></span>                  | <span data-ttu-id="e2343-163">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-163">**True** or **False**</span></span>               | <span data-ttu-id="e2343-164">Når verdien settes til **Sann**, gjentas videoen i en løkke.</span><span class="sxs-lookup"><span data-stu-id="e2343-164">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="e2343-165">Medier</span><span class="sxs-lookup"><span data-stu-id="e2343-165">Media</span></span>                 | <span data-ttu-id="e2343-166">Filbane og -navn for video.</span><span class="sxs-lookup"><span data-stu-id="e2343-166">Video file path and name</span></span> | <span data-ttu-id="e2343-167">Videofilen som spilles av i videospilleren.</span><span class="sxs-lookup"><span data-stu-id="e2343-167">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="e2343-168">Avspillingskontroller</span><span class="sxs-lookup"><span data-stu-id="e2343-168">Playback controls</span></span>     | <span data-ttu-id="e2343-169">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-169">**True** or **False**</span></span>               | <span data-ttu-id="e2343-170">Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen.</span><span class="sxs-lookup"><span data-stu-id="e2343-170">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="e2343-171">Hvis verdien er satt til **Usann**, vises ikke knappen spill av / pause, men brukerne kan fremdeles stoppe og fortsette videoen ved hjelp av tastaturet.</span><span class="sxs-lookup"><span data-stu-id="e2343-171">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |
| <span data-ttu-id="e2343-172">Spille av fullskjerm</span><span class="sxs-lookup"><span data-stu-id="e2343-172">Play fullscreen</span></span>       | <span data-ttu-id="e2343-173">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-173">**True** or **False**</span></span>               | <span data-ttu-id="e2343-174">Når verdien settes til **Sann**, spilles videoen automatisk i fullskjermmodus.</span><span class="sxs-lookup"><span data-stu-id="e2343-174">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="e2343-175">Kontroller</span><span class="sxs-lookup"><span data-stu-id="e2343-175">Controls</span></span>              | <span data-ttu-id="e2343-176">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-176">**True** or **False**</span></span>               | <span data-ttu-id="e2343-177">Når verdien settes til **Sann**, vises alle kontroller.</span><span class="sxs-lookup"><span data-stu-id="e2343-177">When the value is set to **True**, all controls are shown.</span></span> <span data-ttu-id="e2343-178">Disse kontrollene inkluderer knapper for spill av og pause, en fremdriftsindikator og teksting for hørselshemmede.</span><span class="sxs-lookup"><span data-stu-id="e2343-178">These controls include play and pause buttons, a progress indicator, and closed captions.</span></span> |
| <span data-ttu-id="e2343-179">Skjul plakatramme</span><span class="sxs-lookup"><span data-stu-id="e2343-179">Hide poster frame</span></span>     | <span data-ttu-id="e2343-180">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="e2343-180">**True** or **False**</span></span>               | <span data-ttu-id="e2343-181">En video kan ha en plakatramme.</span><span class="sxs-lookup"><span data-stu-id="e2343-181">A video can have a poster frame.</span></span> <span data-ttu-id="e2343-182">Når verdien for denne egenskapen er satt til **Sann**, er plakatrammen skjult.</span><span class="sxs-lookup"><span data-stu-id="e2343-182">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="e2343-183">Maskenivå</span><span class="sxs-lookup"><span data-stu-id="e2343-183">Mask level</span></span>            | <span data-ttu-id="e2343-184">Et tall fra **0** til **100**</span><span class="sxs-lookup"><span data-stu-id="e2343-184">A number from **0** through **100**</span></span> | <span data-ttu-id="e2343-185">Masken som brukes på videoen for styling.</span><span class="sxs-lookup"><span data-stu-id="e2343-185">The mask that is applied to the video for styling.</span></span> |
| <span data-ttu-id="e2343-186">Fullskjermikonstil</span><span class="sxs-lookup"><span data-stu-id="e2343-186">Fullscreen icon style</span></span> | <span data-ttu-id="e2343-187">**Firkant** eller **Pil**</span><span class="sxs-lookup"><span data-stu-id="e2343-187">**Square** or **Arrow**</span></span>             | <span data-ttu-id="e2343-188">Stilen som brukes på fullskjermsikonet som vises i videospilleren.</span><span class="sxs-lookup"><span data-stu-id="e2343-188">The style of the full-screen icon that is shown in the video player.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="e2343-189">Legge til en videospillermodul på en side</span><span class="sxs-lookup"><span data-stu-id="e2343-189">Add a video player module to a page</span></span>

<span data-ttu-id="e2343-190">Hvis du vil legge til en videospillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e2343-190">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e2343-191">Opprett en sidemal som heter **videospillermal**.</span><span class="sxs-lookup"><span data-stu-id="e2343-191">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="e2343-192">I **Hoved**-sporet på standardsiden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="e2343-192">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="e2343-193">I containermodulen legger du til videospiller og omgivelsesvideospillermoduler.</span><span class="sxs-lookup"><span data-stu-id="e2343-193">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="e2343-194">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="e2343-194">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="e2343-195">Bruk videospillermalen du nettopp opprettet, for å opprette en side som heter **videospillerside**.</span><span class="sxs-lookup"><span data-stu-id="e2343-195">Use the video player template that you just created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="e2343-196">I **Hoved**-sporet på den nye siden legger du til en omgivelsesvideospillermodul.</span><span class="sxs-lookup"><span data-stu-id="e2343-196">In the **Main** slot of the new page, add an ambient video player module.</span></span>
1. <span data-ttu-id="e2343-197">I innstillingene for omgivelsesvideospillermodul går du til **Media** og laster opp en videofil.</span><span class="sxs-lookup"><span data-stu-id="e2343-197">In the settings for the ambient video player module, go to **Media**, and upload a video file.</span></span> <span data-ttu-id="e2343-198">Du kan endre **Autokjør**, **Løkke** og andre egenskaper etter behov.</span><span class="sxs-lookup"><span data-stu-id="e2343-198">You can change the **Autoplay**, **Loop**, and other properties as you require.</span></span>
1. <span data-ttu-id="e2343-199">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="e2343-199">Save and preview the page.</span></span>
1. <span data-ttu-id="e2343-200">I **Hoved**-sporet på den nye siden legger du til en videospillermodul.</span><span class="sxs-lookup"><span data-stu-id="e2343-200">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="e2343-201">I innstillingene for videospillermodul går du til **Media** og laster opp en videofil.</span><span class="sxs-lookup"><span data-stu-id="e2343-201">In the settings for the video player module, go to **Media**, and upload a video file.</span></span>
1. <span data-ttu-id="e2343-202">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="e2343-202">Save and preview the page.</span></span> <span data-ttu-id="e2343-203">Du skal se begge videomodulene på siden.</span><span class="sxs-lookup"><span data-stu-id="e2343-203">You should see both video modules on the page.</span></span> <span data-ttu-id="e2343-204">Du kan endre flere innstillinger for å tilpasse virkemåten til hver modul.</span><span class="sxs-lookup"><span data-stu-id="e2343-204">You can change additional settings to customize the behavior of each module.</span></span>
1. <span data-ttu-id="e2343-205">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="e2343-205">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2343-206">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e2343-206">Additional resources</span></span>

[<span data-ttu-id="e2343-207">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="e2343-207">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e2343-208">Varselmodul</span><span class="sxs-lookup"><span data-stu-id="e2343-208">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e2343-209">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="e2343-209">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e2343-210">Innholdsrik blokk-modul</span><span class="sxs-lookup"><span data-stu-id="e2343-210">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e2343-211">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="e2343-211">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e2343-212">Funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="e2343-212">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e2343-213">Hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="e2343-213">Hero module</span></span>](add-hero-module.md)