---
title: Videospillermodul
description: Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 0612682d310362c7523bf08db40faf51c80ea2e3
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411165"
---
# <a name="video-player-module"></a><span data-ttu-id="9b920-103">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="9b920-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9b920-104">Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9b920-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9b920-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="9b920-105">Overview</span></span>

<span data-ttu-id="9b920-106">Videospillermodulen brukes til å støtte videoavspilling.</span><span class="sxs-lookup"><span data-stu-id="9b920-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="9b920-107">Den kan legges til på en hvilken som helst side, forutsatt at videoinnhold lastes opp til og er tilgjengelig i innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="9b920-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="9b920-108">Videospillermodulen støtter MP4-medietypen.</span><span class="sxs-lookup"><span data-stu-id="9b920-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="9b920-109">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="9b920-109">Video player module</span></span>

<span data-ttu-id="9b920-110">Videospillermodulen kan brukes til å vise videoer på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="9b920-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="9b920-111">Den støtter alle avspillingsfunksjoner, for eksempel spill av, pause, fullstørrelsesmodus, lydbeskrivelser og teksting for hørselshemmede.</span><span class="sxs-lookup"><span data-stu-id="9b920-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="9b920-112">Videospillermodulen støtter også tilpassing av teksting for hørselshemmede for å oppfylle Microsofts tilgjengelighetsstandarder.</span><span class="sxs-lookup"><span data-stu-id="9b920-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="9b920-113">Du kan for eksempel tilpasse skriftstørrelsen og bakgrunnsfargen.</span><span class="sxs-lookup"><span data-stu-id="9b920-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="9b920-114">Videospiller-modulen støtter også sekundære lydspor.</span><span class="sxs-lookup"><span data-stu-id="9b920-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="9b920-115">Når en video er lastet opp til CMS, kan du også laste opp et sekundært lydspor.</span><span class="sxs-lookup"><span data-stu-id="9b920-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="9b920-116">Videospiller-modulen kan deretter spille av det sekundære lydsporet hvis en bruker velger det.</span><span class="sxs-lookup"><span data-stu-id="9b920-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="9b920-117">Eksempler på omgivelsesvideospillermoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="9b920-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="9b920-118">Instruksjonsvideoer på produktdetaljsider eller markedsføringssider</span><span class="sxs-lookup"><span data-stu-id="9b920-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="9b920-119">Kampanjevideoer eller videoer om policyer på en hvilken som helst markedsføringsside</span><span class="sxs-lookup"><span data-stu-id="9b920-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="9b920-120">Markedsføringsvideoer som fremhever produktfunksjoner på sider med produktdetaljer eller markedsføringssider</span><span class="sxs-lookup"><span data-stu-id="9b920-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="9b920-121">Bildet nedenfor viser et eksempel på en videospillermodul på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="9b920-121">The following image shows an example of a video player module on a home page.</span></span>

![Eksempel på en videospillermodul](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="9b920-123">Egenskaper for videospillermodul</span><span class="sxs-lookup"><span data-stu-id="9b920-123">Video player module properties</span></span>

| <span data-ttu-id="9b920-124">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="9b920-124">Property name</span></span>         | <span data-ttu-id="9b920-125">Verdi</span><span class="sxs-lookup"><span data-stu-id="9b920-125">Value</span></span>                               | <span data-ttu-id="9b920-126">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9b920-126">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="9b920-127">Automatisk avspilling</span><span class="sxs-lookup"><span data-stu-id="9b920-127">Auto play</span></span>             | <span data-ttu-id="9b920-128">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-128">**True** or **False**</span></span>               | <span data-ttu-id="9b920-129">Når verdien settes til **Sann**, spilles videoen automatisk.</span><span class="sxs-lookup"><span data-stu-id="9b920-129">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="9b920-130">Demp</span><span class="sxs-lookup"><span data-stu-id="9b920-130">Mute</span></span>                  | <span data-ttu-id="9b920-131">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-131">**True** or **False**</span></span>               | <span data-ttu-id="9b920-132">Når verdien settes til **Sann**, dempes lyden.</span><span class="sxs-lookup"><span data-stu-id="9b920-132">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="9b920-133">For denne spilleren er standardverdien **Usann**.</span><span class="sxs-lookup"><span data-stu-id="9b920-133">For this player, the default value is **False**.</span></span> <span data-ttu-id="9b920-134">I Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="9b920-134">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="9b920-135">Løkke</span><span class="sxs-lookup"><span data-stu-id="9b920-135">Loop</span></span>                  | <span data-ttu-id="9b920-136">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-136">**True** or **False**</span></span>               | <span data-ttu-id="9b920-137">Når verdien settes til **Sann**, gjentas videoen i en løkke.</span><span class="sxs-lookup"><span data-stu-id="9b920-137">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="9b920-138">Medier</span><span class="sxs-lookup"><span data-stu-id="9b920-138">Media</span></span>                 | <span data-ttu-id="9b920-139">Filbane og -navn for video.</span><span class="sxs-lookup"><span data-stu-id="9b920-139">Video file path and name</span></span> | <span data-ttu-id="9b920-140">Videofilen som spilles av i videospilleren.</span><span class="sxs-lookup"><span data-stu-id="9b920-140">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="9b920-141">Spille av fullskjerm</span><span class="sxs-lookup"><span data-stu-id="9b920-141">Play fullscreen</span></span>       | <span data-ttu-id="9b920-142">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-142">**True** or **False**</span></span>               | <span data-ttu-id="9b920-143">Når verdien settes til **Sann**, spilles videoen automatisk i fullskjermmodus.</span><span class="sxs-lookup"><span data-stu-id="9b920-143">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="9b920-144">Utløser for avspilling/pause</span><span class="sxs-lookup"><span data-stu-id="9b920-144">Play pause trigger</span></span>    | <span data-ttu-id="9b920-145">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-145">**True** or **False**</span></span>               | <span data-ttu-id="9b920-146">Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen.</span><span class="sxs-lookup"><span data-stu-id="9b920-146">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="9b920-147">Kontroller for videospiller</span><span class="sxs-lookup"><span data-stu-id="9b920-147">Video player controls</span></span> | <span data-ttu-id="9b920-148">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-148">**True** or **False**</span></span>               | <span data-ttu-id="9b920-149">Når verdien settes til **Sann**, vises alle videospillerkontroller.</span><span class="sxs-lookup"><span data-stu-id="9b920-149">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="9b920-150">Disse kontrollene inkluderer knapper for spill av og pause, en fremdriftsindikator og alternativer for teksting for hørselshemmede.</span><span class="sxs-lookup"><span data-stu-id="9b920-150">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="9b920-151">Skjul plakatbilde</span><span class="sxs-lookup"><span data-stu-id="9b920-151">Hide poster image</span></span>     | <span data-ttu-id="9b920-152">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="9b920-152">**True** or **False**</span></span>               | <span data-ttu-id="9b920-153">En video kan ha en plakatramme.</span><span class="sxs-lookup"><span data-stu-id="9b920-153">A video can have a poster frame.</span></span> <span data-ttu-id="9b920-154">Når verdien for denne egenskapen er satt til **Sann**, er plakatrammen skjult.</span><span class="sxs-lookup"><span data-stu-id="9b920-154">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="9b920-155">Maskenivå</span><span class="sxs-lookup"><span data-stu-id="9b920-155">Mask level</span></span>            | <span data-ttu-id="9b920-156">Et tall fra **0** til **100**</span><span class="sxs-lookup"><span data-stu-id="9b920-156">A number from **0** through **100**</span></span> | <span data-ttu-id="9b920-157">Masken som brukes på videoen for styling.</span><span class="sxs-lookup"><span data-stu-id="9b920-157">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="9b920-158">Legge til en videospillermodul på en side</span><span class="sxs-lookup"><span data-stu-id="9b920-158">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="9b920-159">Før du oppretter en videospillermodul, må du først laste opp en video til mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="9b920-159">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="9b920-160">Hvis du vil legge til en videospillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="9b920-160">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9b920-161">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="9b920-161">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="9b920-162">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Videospillermal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-162">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-163">I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9b920-163">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b920-164">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-164">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-165">På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9b920-165">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b920-166">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-166">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-167">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9b920-167">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b920-168">I dialogboksen **Legg til modul** velger du **Videospiller**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-168">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-169">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="9b920-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="9b920-170">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="9b920-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="9b920-171">I **Velg en mal**-dialogboksen velger du videospillermalen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="9b920-171">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="9b920-172">Under **Sidenavn** angir du **Videospillerside**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-172">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-173">På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9b920-173">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b920-174">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-175">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9b920-175">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9b920-176">I dialogboksen **Legg til modul** velger du **Videospiller**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-176">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-177">Velg **Legg til en video** i egenskapsruten for videospillermodulen.</span><span class="sxs-lookup"><span data-stu-id="9b920-177">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="9b920-178">Velg en video i dialogboksen **Medievelger**, og velg deretter **Last opp nytt medieelement** .</span><span class="sxs-lookup"><span data-stu-id="9b920-178">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="9b920-179">I Filutforsker velger du en videofil, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="9b920-179">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="9b920-180">I **Last opp medieelement**-dialogboksen skriver du inn en tittel og annen informasjon etter behov, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b920-180">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="9b920-181">I **Medievelger**-dialogboksen velger du **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="9b920-181">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="9b920-182">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="9b920-182">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9b920-183">Du skal se videomodulen på siden.</span><span class="sxs-lookup"><span data-stu-id="9b920-183">You should see the video module on the page.</span></span> <span data-ttu-id="9b920-184">Du kan endre flere innstillinger for å tilpasse virkemåten til modulen.</span><span class="sxs-lookup"><span data-stu-id="9b920-184">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="9b920-185">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="9b920-185">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9b920-186">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9b920-186">Additional resources</span></span>

[<span data-ttu-id="9b920-187">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="9b920-187">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9b920-188">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="9b920-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="9b920-189">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="9b920-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="9b920-190">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="9b920-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9b920-191">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="9b920-191">Content block module</span></span>](add-hero-module.md)
