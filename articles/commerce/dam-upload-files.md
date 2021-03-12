---
title: Laste opp andre filer enn bilder og videoer
description: Dette emnet beskriver hvordan du laster opp binære filer som ikke er bilder og videoer, i Microsoft Dynamics 365 Commerce-områdebygger.
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
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995776"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="638bc-103">Laste opp andre filer enn bilder og videoer</span><span class="sxs-lookup"><span data-stu-id="638bc-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="638bc-104">Dette emnet beskriver hvordan du laster opp filer som ikke er bilder og videoer, i Microsoft Dynamics 365 Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="638bc-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="638bc-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="638bc-105">Overview</span></span>

<span data-ttu-id="638bc-106">Mediebiblioteket for Commerce-områdebygger støtter opplasting av andre binære ressurser enn bilder eller videoer.</span><span class="sxs-lookup"><span data-stu-id="638bc-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="638bc-107">Du kan for eksempel laste opp Microsoft Excel, Microsoft Word Microsoft PowerPoint eller PDF-filer.</span><span class="sxs-lookup"><span data-stu-id="638bc-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="638bc-108">Følgende dokumenttyper støttes:</span><span class="sxs-lookup"><span data-stu-id="638bc-108">The following document types are supported:</span></span>
- <span data-ttu-id="638bc-109">7Z</span><span class="sxs-lookup"><span data-stu-id="638bc-109">7Z</span></span>
- <span data-ttu-id="638bc-110">AVI</span><span class="sxs-lookup"><span data-stu-id="638bc-110">AVI</span></span>
- <span data-ttu-id="638bc-111">CS</span><span class="sxs-lookup"><span data-stu-id="638bc-111">CS</span></span>
- <span data-ttu-id="638bc-112">CSS</span><span class="sxs-lookup"><span data-stu-id="638bc-112">CSS</span></span>
- <span data-ttu-id="638bc-113">DOC</span><span class="sxs-lookup"><span data-stu-id="638bc-113">DOC</span></span>
- <span data-ttu-id="638bc-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="638bc-114">DOCX</span></span>
- <span data-ttu-id="638bc-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="638bc-115">EPUB</span></span>
- <span data-ttu-id="638bc-116">GIF</span><span class="sxs-lookup"><span data-stu-id="638bc-116">GIF</span></span>
- <span data-ttu-id="638bc-117">INDD</span><span class="sxs-lookup"><span data-stu-id="638bc-117">INDD</span></span>
- <span data-ttu-id="638bc-118">JAR</span><span class="sxs-lookup"><span data-stu-id="638bc-118">JAR</span></span>
- <span data-ttu-id="638bc-119">JPG</span><span class="sxs-lookup"><span data-stu-id="638bc-119">JPG</span></span>
- <span data-ttu-id="638bc-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="638bc-120">JPEG</span></span>
- <span data-ttu-id="638bc-121">JS</span><span class="sxs-lookup"><span data-stu-id="638bc-121">JS</span></span>
- <span data-ttu-id="638bc-122">MP3</span><span class="sxs-lookup"><span data-stu-id="638bc-122">MP3</span></span>
- <span data-ttu-id="638bc-123">MP4</span><span class="sxs-lookup"><span data-stu-id="638bc-123">MP4</span></span>
- <span data-ttu-id="638bc-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="638bc-124">MPEG</span></span>
- <span data-ttu-id="638bc-125">MPG</span><span class="sxs-lookup"><span data-stu-id="638bc-125">MPG</span></span>
- <span data-ttu-id="638bc-126">ODP</span><span class="sxs-lookup"><span data-stu-id="638bc-126">ODP</span></span>
- <span data-ttu-id="638bc-127">ODS</span><span class="sxs-lookup"><span data-stu-id="638bc-127">ODS</span></span>
- <span data-ttu-id="638bc-128">ODT</span><span class="sxs-lookup"><span data-stu-id="638bc-128">ODT</span></span>
- <span data-ttu-id="638bc-129">PDF</span><span class="sxs-lookup"><span data-stu-id="638bc-129">PDF</span></span>
- <span data-ttu-id="638bc-130">PNG</span><span class="sxs-lookup"><span data-stu-id="638bc-130">PNG</span></span>
- <span data-ttu-id="638bc-131">PPT</span><span class="sxs-lookup"><span data-stu-id="638bc-131">PPT</span></span>
- <span data-ttu-id="638bc-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="638bc-132">PPTX</span></span>
- <span data-ttu-id="638bc-133">PS</span><span class="sxs-lookup"><span data-stu-id="638bc-133">PS</span></span>
- <span data-ttu-id="638bc-134">QXP</span><span class="sxs-lookup"><span data-stu-id="638bc-134">QXP</span></span>
- <span data-ttu-id="638bc-135">RAR</span><span class="sxs-lookup"><span data-stu-id="638bc-135">RAR</span></span>
- <span data-ttu-id="638bc-136">RTF</span><span class="sxs-lookup"><span data-stu-id="638bc-136">RTF</span></span>
- <span data-ttu-id="638bc-137">SVG</span><span class="sxs-lookup"><span data-stu-id="638bc-137">SVG</span></span>
- <span data-ttu-id="638bc-138">TAR</span><span class="sxs-lookup"><span data-stu-id="638bc-138">TAR</span></span>
- <span data-ttu-id="638bc-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="638bc-139">TGZ</span></span>
- <span data-ttu-id="638bc-140">TXT</span><span class="sxs-lookup"><span data-stu-id="638bc-140">TXT</span></span>
- <span data-ttu-id="638bc-141">WMV</span><span class="sxs-lookup"><span data-stu-id="638bc-141">WMV</span></span>
- <span data-ttu-id="638bc-142">XLS</span><span class="sxs-lookup"><span data-stu-id="638bc-142">XLS</span></span>
- <span data-ttu-id="638bc-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="638bc-143">XLSX</span></span>
- <span data-ttu-id="638bc-144">XML</span><span class="sxs-lookup"><span data-stu-id="638bc-144">XML</span></span>
- <span data-ttu-id="638bc-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="638bc-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="638bc-146">Last opp en fil</span><span class="sxs-lookup"><span data-stu-id="638bc-146">Upload a file</span></span>

<span data-ttu-id="638bc-147">Hvis du vil laste opp en fil til Commerce-områdebygger, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="638bc-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="638bc-148">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="638bc-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="638bc-149">Velg **Last opp \> Last opp medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="638bc-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="638bc-150">I Filutforsker velger du én eller flere filer, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="638bc-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="638bc-151">I dialogboksen **Last opp medieelement** skriver du inn tittel, beskrivelse og metadata for nøkkelord etter behov.</span><span class="sxs-lookup"><span data-stu-id="638bc-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="638bc-152">Hvis du vil publisere filene like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="638bc-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="638bc-153">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="638bc-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="638bc-154">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="638bc-154">Additional resources</span></span>

[<span data-ttu-id="638bc-155">Oversikt over digital anleggsmiddelbehandling</span><span class="sxs-lookup"><span data-stu-id="638bc-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="638bc-156">Laste opp bilder</span><span class="sxs-lookup"><span data-stu-id="638bc-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="638bc-157">Laste opp video</span><span class="sxs-lookup"><span data-stu-id="638bc-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="638bc-158">Beskjære bilder</span><span class="sxs-lookup"><span data-stu-id="638bc-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="638bc-159">Tilpasse bildefokuspunkter</span><span class="sxs-lookup"><span data-stu-id="638bc-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="638bc-160">Last opp og betjen statiske filer</span><span class="sxs-lookup"><span data-stu-id="638bc-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
