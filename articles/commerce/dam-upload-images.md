---
title: Laste opp bilder
description: Dette emnet beskriver hvordan du laster opp bilder i områdebyggeren for Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 51571ce221714598b2e2d39c76cb69dcb57cc52b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213800"
---
# <a name="upload-images"></a><span data-ttu-id="3c515-103">Laste opp bilder</span><span class="sxs-lookup"><span data-stu-id="3c515-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c515-104">Dette emnet beskriver hvordan du laster opp bilder i områdebyggeren for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c515-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="3c515-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="3c515-105">Overview</span></span>

<span data-ttu-id="3c515-106">Med mediebiblioteket for Commerce-områdebygger kan du laste opp bilder, enten enkeltvis eller flere samtidig ved hjelp av mapper.</span><span class="sxs-lookup"><span data-stu-id="3c515-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="3c515-107">Du bør alltid laste opp den versjonen av bildet med høyest oppløsning og kvalitet, fordi bildeskaleringskomponenten automatisk vil optimalisere bildet for forskjellige visningsporter og deres stoppunkter.</span><span class="sxs-lookup"><span data-stu-id="3c515-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="3c515-108">Bildeinformasjon som angis under opplasting</span><span class="sxs-lookup"><span data-stu-id="3c515-108">Image information specified during upload</span></span>

<span data-ttu-id="3c515-109">Når du laster opp et bilde, kan følgende informasjon angis.</span><span class="sxs-lookup"><span data-stu-id="3c515-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="3c515-110">**Tittel, alt-tekst, beskrivelse, nøkkelord**: metadata for bildet eller bildene.</span><span class="sxs-lookup"><span data-stu-id="3c515-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="3c515-111">Tittel og alt-tekst er obligatoriske verdier.</span><span class="sxs-lookup"><span data-stu-id="3c515-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="3c515-112">**Velg kategori**:</span><span class="sxs-lookup"><span data-stu-id="3c515-112">**Select category**:</span></span>
    - <span data-ttu-id="3c515-113">**Ingen**: brukes for beskrivelse av bilde eller bilder i e-handel.</span><span class="sxs-lookup"><span data-stu-id="3c515-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="3c515-114">**Produkt, kategori, kunde, ansatt, katalog**: brukes for Dynamics 365 Commerce omni-kanalbilde eller -bilder.</span><span class="sxs-lookup"><span data-stu-id="3c515-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="3c515-115">**Publiser aktiva etter opplasting**: Når det er merket av i denne avmerkingsboksen, publiseres bildet eller bildene umiddelbart etter opplastingen.</span><span class="sxs-lookup"><span data-stu-id="3c515-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="3c515-116">Bilderessurser med en kategori som er tilordnet, blir også automatisk merket med kategorien som et nøkkelord for å hjelpe å søke etter anleggsmidler for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="3c515-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="3c515-117">Navnekonvensjoner for omni-kanals bilder</span><span class="sxs-lookup"><span data-stu-id="3c515-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="3c515-118">Hvis du har konfigurert mediebiblioteket som omnikanal-bildeserver, kan du bruke bildekategorier til å angi hvilken kategori den opplastede bildet tilhører.</span><span class="sxs-lookup"><span data-stu-id="3c515-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="3c515-119">Det finnes også en navngivningskonvensjon som bør følges for å sikre at bilder hentes riktig av andre kanaler, for eksempel salgssted.</span><span class="sxs-lookup"><span data-stu-id="3c515-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="3c515-120">Standard navnekonvensjon varierer avhengig av kategorien:</span><span class="sxs-lookup"><span data-stu-id="3c515-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="3c515-121">Katalogbilder må ha navnet "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="3c515-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="3c515-122">Kategori bilder bør ha navnet "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="3c515-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="3c515-123">Kundebilder bør gis navnet "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="3c515-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="3c515-124">Bilde for ansatte bør ha navnet "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="3c515-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="3c515-125">Produktbilder bør ha navnet "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="3c515-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="3c515-126">001 er bildesekvensen, og det kan være 001, 002, 003, 004 eller 005</span><span class="sxs-lookup"><span data-stu-id="3c515-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="3c515-127">Produktvariantbilder bør ha navnet "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="3c515-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="3c515-128">Laste opp et bilde</span><span class="sxs-lookup"><span data-stu-id="3c515-128">Upload an image</span></span>

<span data-ttu-id="3c515-129">Hvis du vil laste opp et bilde i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="3c515-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3c515-130">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="3c515-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3c515-131">Velg **Last opp \> Last opp medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="3c515-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="3c515-132">I Filutforsker-vinduet går du til og velger én eller flere bildefiler du vil laste opp, og velger deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="3c515-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="3c515-133">I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="3c515-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="3c515-134">Angi en valgfri beskrivelse og nøkkelord, og velg en kategori hvis ønskelig.</span><span class="sxs-lookup"><span data-stu-id="3c515-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="3c515-135">Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="3c515-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="3c515-136">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c515-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="3c515-137">Laste opp en mappe med bilder</span><span class="sxs-lookup"><span data-stu-id="3c515-137">Upload a folder of images</span></span>

<span data-ttu-id="3c515-138">Hvis du vil masseopplaste en mappe med bilde i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="3c515-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3c515-139">Velg **Mediebibliotek** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="3c515-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3c515-140">Velg **Last opp \> Last opp mappe** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="3c515-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="3c515-141">I Filutforsker-vinduet går du til og velger en mappe du vil laste opp, og velger deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="3c515-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="3c515-142">I dialogboksen **Last opp medieelementer** angir du valgfrie nøkkelord og velger en kategori hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="3c515-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="3c515-143">Hvis du vil publisere bildene i mappen like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.</span><span class="sxs-lookup"><span data-stu-id="3c515-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="3c515-144">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c515-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c515-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3c515-145">Additional resources</span></span>

[<span data-ttu-id="3c515-146">Oversikt over digital anleggsmiddelbehandling</span><span class="sxs-lookup"><span data-stu-id="3c515-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3c515-147">Laste opp video</span><span class="sxs-lookup"><span data-stu-id="3c515-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="3c515-148">Laste opp filer</span><span class="sxs-lookup"><span data-stu-id="3c515-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="3c515-149">Beskjære bilder</span><span class="sxs-lookup"><span data-stu-id="3c515-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3c515-150">Tilpasse bildefokuspunkter</span><span class="sxs-lookup"><span data-stu-id="3c515-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="3c515-151">Last opp og betjen statiske filer</span><span class="sxs-lookup"><span data-stu-id="3c515-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]