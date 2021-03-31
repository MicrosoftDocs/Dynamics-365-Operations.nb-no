---
title: Laste opp videoer
description: Dette emnet beskriver hvordan du laster opp videoer i områdebyggeren for Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d74e7116d68074bfc917784a8f51f85d5682c5d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213848"
---
# <a name="upload-videos"></a><span data-ttu-id="c7327-103">Laste opp videoer</span><span class="sxs-lookup"><span data-stu-id="c7327-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7327-104">Dette emnet beskriver hvordan du laster opp videoer i områdebyggeren for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7327-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="c7327-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c7327-105">Overview</span></span>

<span data-ttu-id="c7327-106">Med mediebiblioteket for Commerce-områdebygger kan du laste opp videoer.</span><span class="sxs-lookup"><span data-stu-id="c7327-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="c7327-107">Du bør alltid laste opp den versjonen av en video med den høyeste bithastigheten og oppløsningen, fordi videoen automatisk vil bli konvertert til å passe for forskjellige visningsporter og deres stoppunkter.</span><span class="sxs-lookup"><span data-stu-id="c7327-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="c7327-108">Videoinformasjon som angis under opplasting</span><span class="sxs-lookup"><span data-stu-id="c7327-108">Video information specified during upload</span></span>

<span data-ttu-id="c7327-109">Når du laster opp en video, kan følgende informasjon angis.</span><span class="sxs-lookup"><span data-stu-id="c7327-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="c7327-110">**Tittel, beskrivelse, nøkkelord**: metadata for videoen.</span><span class="sxs-lookup"><span data-stu-id="c7327-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="c7327-111">**Generer undertekster automatisk**: angir om teksting for hørselshemmede skal genereres automatisk for videoen.</span><span class="sxs-lookup"><span data-stu-id="c7327-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="c7327-112">**Teksting for hørselshemmede**: angir hvilken teksting for hørselshemmede som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="c7327-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="c7327-113">**Vanlig lyd**: angir det vanlige lydsporet som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="c7327-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="c7327-114">**Miniatyrbilde**: angir miniatyrbildet for videoen.</span><span class="sxs-lookup"><span data-stu-id="c7327-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="c7327-115">Bildet blir generert automatisk hvis det ikke angis.</span><span class="sxs-lookup"><span data-stu-id="c7327-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="c7327-116">**Beskrivende lyd**: angir det beskrivende lydsporet som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="c7327-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="c7327-117">Laste opp en video</span><span class="sxs-lookup"><span data-stu-id="c7327-117">Upload a video</span></span>

<span data-ttu-id="c7327-118">Hvis du vil laste opp en video i områdebygger, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c7327-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7327-119">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="c7327-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="c7327-120">Velg **Last opp \> Last opp medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="c7327-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="c7327-121">I Filutforsker-vinduet går du til og velger én eller flere videofiler du vil laste opp, og velger deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="c7327-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="c7327-122">I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="c7327-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="c7327-123">Angi en valgfri beskrivelse og nøkkelord, og velg en kategori hvis ønskelig.</span><span class="sxs-lookup"><span data-stu-id="c7327-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="c7327-124">Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="c7327-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="c7327-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7327-125">Select **OK**.</span></span>

<span data-ttu-id="c7327-126">Hvis du laster opp flere typer aktiva samtidig (for eksempel bilder og videoer), vil du i dialogboksen **Last opp medieelement** bare kunne angi nøkkelord, om filene skal publiseres umiddelbart etter opplastingen, og om teksting for hørselshemmede skal genereres automatisk for videofiler.</span><span class="sxs-lookup"><span data-stu-id="c7327-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="c7327-127">Alle anleggsmidlene vil dele de samme nøkkelordene.</span><span class="sxs-lookup"><span data-stu-id="c7327-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7327-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c7327-128">Additional resources</span></span>

[<span data-ttu-id="c7327-129">Oversikt over digital anleggsmiddelbehandling</span><span class="sxs-lookup"><span data-stu-id="c7327-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c7327-130">Laste opp bilder</span><span class="sxs-lookup"><span data-stu-id="c7327-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c7327-131">Laste opp filer</span><span class="sxs-lookup"><span data-stu-id="c7327-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="c7327-132">Beskjære bilder</span><span class="sxs-lookup"><span data-stu-id="c7327-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c7327-133">Tilpasse bildefokuspunkter</span><span class="sxs-lookup"><span data-stu-id="c7327-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="c7327-134">Last opp og betjen statiske filer</span><span class="sxs-lookup"><span data-stu-id="c7327-134">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]