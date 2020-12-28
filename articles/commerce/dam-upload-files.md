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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4acd3bec32cdfe627f6eb33dd5dc652f7cff74a8
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594218"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="048e0-103">Laste opp andre filer enn bilder og videoer</span><span class="sxs-lookup"><span data-stu-id="048e0-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="048e0-104">Dette emnet beskriver hvordan du laster opp filer som ikke er bilder og videoer, i Microsoft Dynamics 365 Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="048e0-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="048e0-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="048e0-105">Overview</span></span>

<span data-ttu-id="048e0-106">Mediebiblioteket for Commerce-områdebygger støtter opplasting av andre binære ressurser enn bilder eller videoer.</span><span class="sxs-lookup"><span data-stu-id="048e0-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="048e0-107">Du kan for eksempel laste opp Microsoft Excel, Microsoft Word Microsoft PowerPoint eller PDF-filer.</span><span class="sxs-lookup"><span data-stu-id="048e0-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="048e0-108">Følgende dokumenttyper støttes:</span><span class="sxs-lookup"><span data-stu-id="048e0-108">The following document types are supported:</span></span>
- <span data-ttu-id="048e0-109">7Z</span><span class="sxs-lookup"><span data-stu-id="048e0-109">7Z</span></span>
- <span data-ttu-id="048e0-110">AVI</span><span class="sxs-lookup"><span data-stu-id="048e0-110">AVI</span></span>
- <span data-ttu-id="048e0-111">CS</span><span class="sxs-lookup"><span data-stu-id="048e0-111">CS</span></span>
- <span data-ttu-id="048e0-112">CSS</span><span class="sxs-lookup"><span data-stu-id="048e0-112">CSS</span></span>
- <span data-ttu-id="048e0-113">DOC</span><span class="sxs-lookup"><span data-stu-id="048e0-113">DOC</span></span>
- <span data-ttu-id="048e0-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="048e0-114">DOCX</span></span>
- <span data-ttu-id="048e0-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="048e0-115">EPUB</span></span>
- <span data-ttu-id="048e0-116">GIF</span><span class="sxs-lookup"><span data-stu-id="048e0-116">GIF</span></span>
- <span data-ttu-id="048e0-117">INDD</span><span class="sxs-lookup"><span data-stu-id="048e0-117">INDD</span></span>
- <span data-ttu-id="048e0-118">JAR</span><span class="sxs-lookup"><span data-stu-id="048e0-118">JAR</span></span>
- <span data-ttu-id="048e0-119">JPG</span><span class="sxs-lookup"><span data-stu-id="048e0-119">JPG</span></span>
- <span data-ttu-id="048e0-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="048e0-120">JPEG</span></span>
- <span data-ttu-id="048e0-121">JS</span><span class="sxs-lookup"><span data-stu-id="048e0-121">JS</span></span>
- <span data-ttu-id="048e0-122">MP3</span><span class="sxs-lookup"><span data-stu-id="048e0-122">MP3</span></span>
- <span data-ttu-id="048e0-123">MP4</span><span class="sxs-lookup"><span data-stu-id="048e0-123">MP4</span></span>
- <span data-ttu-id="048e0-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="048e0-124">MPEG</span></span>
- <span data-ttu-id="048e0-125">MPG</span><span class="sxs-lookup"><span data-stu-id="048e0-125">MPG</span></span>
- <span data-ttu-id="048e0-126">ODP</span><span class="sxs-lookup"><span data-stu-id="048e0-126">ODP</span></span>
- <span data-ttu-id="048e0-127">ODS</span><span class="sxs-lookup"><span data-stu-id="048e0-127">ODS</span></span>
- <span data-ttu-id="048e0-128">ODT</span><span class="sxs-lookup"><span data-stu-id="048e0-128">ODT</span></span>
- <span data-ttu-id="048e0-129">PDF</span><span class="sxs-lookup"><span data-stu-id="048e0-129">PDF</span></span>
- <span data-ttu-id="048e0-130">PNG</span><span class="sxs-lookup"><span data-stu-id="048e0-130">PNG</span></span>
- <span data-ttu-id="048e0-131">PPT</span><span class="sxs-lookup"><span data-stu-id="048e0-131">PPT</span></span>
- <span data-ttu-id="048e0-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="048e0-132">PPTX</span></span>
- <span data-ttu-id="048e0-133">PS</span><span class="sxs-lookup"><span data-stu-id="048e0-133">PS</span></span>
- <span data-ttu-id="048e0-134">QXP</span><span class="sxs-lookup"><span data-stu-id="048e0-134">QXP</span></span>
- <span data-ttu-id="048e0-135">RAR</span><span class="sxs-lookup"><span data-stu-id="048e0-135">RAR</span></span>
- <span data-ttu-id="048e0-136">RTF</span><span class="sxs-lookup"><span data-stu-id="048e0-136">RTF</span></span>
- <span data-ttu-id="048e0-137">SVG</span><span class="sxs-lookup"><span data-stu-id="048e0-137">SVG</span></span>
- <span data-ttu-id="048e0-138">TAR</span><span class="sxs-lookup"><span data-stu-id="048e0-138">TAR</span></span>
- <span data-ttu-id="048e0-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="048e0-139">TGZ</span></span>
- <span data-ttu-id="048e0-140">TXT</span><span class="sxs-lookup"><span data-stu-id="048e0-140">TXT</span></span>
- <span data-ttu-id="048e0-141">WMV</span><span class="sxs-lookup"><span data-stu-id="048e0-141">WMV</span></span>
- <span data-ttu-id="048e0-142">XLS</span><span class="sxs-lookup"><span data-stu-id="048e0-142">XLS</span></span>
- <span data-ttu-id="048e0-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="048e0-143">XLSX</span></span>
- <span data-ttu-id="048e0-144">XML</span><span class="sxs-lookup"><span data-stu-id="048e0-144">XML</span></span>
- <span data-ttu-id="048e0-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="048e0-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="048e0-146">Last opp en fil</span><span class="sxs-lookup"><span data-stu-id="048e0-146">Upload a file</span></span>

<span data-ttu-id="048e0-147">Hvis du vil laste opp en fil til Commerce-områdebygger, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="048e0-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="048e0-148">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="048e0-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="048e0-149">Velg **Last opp \> Last opp medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="048e0-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="048e0-150">I Filutforsker velger du én eller flere filer, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="048e0-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="048e0-151">I dialogboksen **Last opp medieelement** skriver du inn tittel, beskrivelse og metadata for nøkkelord etter behov.</span><span class="sxs-lookup"><span data-stu-id="048e0-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="048e0-152">Hvis du vil publisere filene like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="048e0-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="048e0-153">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="048e0-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="048e0-154">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="048e0-154">Additional resources</span></span>

[<span data-ttu-id="048e0-155">Oversikt over digital anleggsmiddelbehandling</span><span class="sxs-lookup"><span data-stu-id="048e0-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="048e0-156">Laste opp bilder</span><span class="sxs-lookup"><span data-stu-id="048e0-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="048e0-157">Laste opp video</span><span class="sxs-lookup"><span data-stu-id="048e0-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="048e0-158">Beskjære bilder</span><span class="sxs-lookup"><span data-stu-id="048e0-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="048e0-159">Tilpasse bildefokuspunkter</span><span class="sxs-lookup"><span data-stu-id="048e0-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="048e0-160">Last opp og betjen statiske filer</span><span class="sxs-lookup"><span data-stu-id="048e0-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
