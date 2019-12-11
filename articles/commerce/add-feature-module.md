---
title: Funksjonsmodul
description: Dette emnet dekker funksjonsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785292"
---
# <a name="feature-module"></a><span data-ttu-id="463eb-103">Funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="463eb-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="463eb-104">Dette emnet dekker funksjonsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="463eb-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="463eb-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="463eb-105">Overview</span></span>

<span data-ttu-id="463eb-106">En funksjonsmodul brukes til å markedsføre produkter eller kampanjer ved hjelp av en kombinasjon av bilder og tekst.</span><span class="sxs-lookup"><span data-stu-id="463eb-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="463eb-107">En forhandler kan for eksempel legge til en funksjonsmodul på en produktdetaljside for å fremheve funksjonene til produktet.</span><span class="sxs-lookup"><span data-stu-id="463eb-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="463eb-108">En funksjonsmodul styres av data fra CMS (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="463eb-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="463eb-109">Det er en frittstående modul som ikke er avhengig av andre moduler på siden.</span><span class="sxs-lookup"><span data-stu-id="463eb-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="463eb-110">En funksjonsmodul kan være plassert på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, salg eller funksjoner).</span><span class="sxs-lookup"><span data-stu-id="463eb-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="463eb-111">Eksempler på funksjonsmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="463eb-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="463eb-112">En funksjonsmodul kan brukes på følgende sider:</span><span class="sxs-lookup"><span data-stu-id="463eb-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="463eb-113">En produktdetaljside for å vise produktfunksjoner</span><span class="sxs-lookup"><span data-stu-id="463eb-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="463eb-114">Startsiden for å fremme produkter</span><span class="sxs-lookup"><span data-stu-id="463eb-114">The home page, to promote products</span></span>
- <span data-ttu-id="463eb-115">En kategoriside for å utheve en kategori med produkter</span><span class="sxs-lookup"><span data-stu-id="463eb-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="463eb-116">Egenskaper for funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="463eb-116">Feature module properties</span></span>

| <span data-ttu-id="463eb-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="463eb-117">Property name</span></span>     | <span data-ttu-id="463eb-118">Verdier</span><span class="sxs-lookup"><span data-stu-id="463eb-118">Values</span></span> | <span data-ttu-id="463eb-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="463eb-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="463eb-120">Bilde</span><span class="sxs-lookup"><span data-stu-id="463eb-120">Image</span></span>             | <span data-ttu-id="463eb-121">Bildefil</span><span class="sxs-lookup"><span data-stu-id="463eb-121">Image file</span></span> | <span data-ttu-id="463eb-122">Et bilde kan brukes til å markedsføre produktet eller kampanjen.</span><span class="sxs-lookup"><span data-stu-id="463eb-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="463eb-123">Et bilde kan lastes opp til bildegalleriet, eller det kan brukes et eksisterende bilde.</span><span class="sxs-lookup"><span data-stu-id="463eb-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="463eb-124">Overskrift</span><span class="sxs-lookup"><span data-stu-id="463eb-124">Heading</span></span>           | <span data-ttu-id="463eb-125">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="463eb-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="463eb-126">Alle funksjonsmoduler kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="463eb-126">Every feature module can have a heading.</span></span> <span data-ttu-id="463eb-127">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="463eb-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="463eb-128">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="463eb-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="463eb-129">Avsnitt</span><span class="sxs-lookup"><span data-stu-id="463eb-129">Paragraph</span></span>         | <span data-ttu-id="463eb-130">Avsnittstekst</span><span class="sxs-lookup"><span data-stu-id="463eb-130">Paragraph text</span></span> | <span data-ttu-id="463eb-131">Funksjonsmoduler støtter avsnittstekst i rikt tekstformat.</span><span class="sxs-lookup"><span data-stu-id="463eb-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="463eb-132">Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst, og hyperkoblinger.</span><span class="sxs-lookup"><span data-stu-id="463eb-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="463eb-133">Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen.</span><span class="sxs-lookup"><span data-stu-id="463eb-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="463eb-134">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="463eb-134">Link</span></span>              | <span data-ttu-id="463eb-135">Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori**</span><span class="sxs-lookup"><span data-stu-id="463eb-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="463eb-136">Funksjonsmoduler støtter én eller flere "handlingsoppfordring"-koblinger.</span><span class="sxs-lookup"><span data-stu-id="463eb-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="463eb-137">Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett.</span><span class="sxs-lookup"><span data-stu-id="463eb-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="463eb-138">ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="463eb-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="463eb-139">Koblinger kan konfigureres slik at de åpnes i en ny fane.</span><span class="sxs-lookup"><span data-stu-id="463eb-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="463eb-140">Bildeplassering</span><span class="sxs-lookup"><span data-stu-id="463eb-140">Image placement</span></span>   | <span data-ttu-id="463eb-141">**Høyre**, **Venstre**, **Topp**eller **Bunn**</span><span class="sxs-lookup"><span data-stu-id="463eb-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="463eb-142">Denne egenskapen angir plasseringen av bildet i forhold til teksten.</span><span class="sxs-lookup"><span data-stu-id="463eb-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="463eb-143">Hvis for eksempel **Høyre** er valgt, vises bildet til høyre for teksten.</span><span class="sxs-lookup"><span data-stu-id="463eb-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="463eb-144">Kolonnestørrelse for bilde</span><span class="sxs-lookup"><span data-stu-id="463eb-144">Image column size</span></span> | <span data-ttu-id="463eb-145">En verdi fra **1** til **12**</span><span class="sxs-lookup"><span data-stu-id="463eb-145">A value from **1** through **12**</span></span> | <span data-ttu-id="463eb-146">Denne egenskapen angir størrelse på bildet i forhold til teksten.</span><span class="sxs-lookup"><span data-stu-id="463eb-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="463eb-147">Størrelsen uttrykkes som et antall kolonner på siden.</span><span class="sxs-lookup"><span data-stu-id="463eb-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="463eb-148">Det finnes 12 kolonner på en side.</span><span class="sxs-lookup"><span data-stu-id="463eb-148">There are 12 columns on a page.</span></span> <span data-ttu-id="463eb-149">Som standard har bildet og teksten samme størrelse (seks kolonner hver).</span><span class="sxs-lookup"><span data-stu-id="463eb-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="463eb-150">Størrelsen kan imidlertid justeres etter behov.</span><span class="sxs-lookup"><span data-stu-id="463eb-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="463eb-151">Legge til en funksjonsmodul på en ny side</span><span class="sxs-lookup"><span data-stu-id="463eb-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="463eb-152">Hvis du vil legge til en funksjonsmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="463eb-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="463eb-153">Gå til **Maler**, og opprett en sidemal kalt **funksjonsmal**.</span><span class="sxs-lookup"><span data-stu-id="463eb-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="463eb-154">I **Hoved**-sporet på standardsiden legger du til en funksjonsmodul.</span><span class="sxs-lookup"><span data-stu-id="463eb-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="463eb-155">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="463eb-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="463eb-156">Bruk funksjonsmalen du nettopp opprettet, for å opprette en side som heter **funksjonsside**.</span><span class="sxs-lookup"><span data-stu-id="463eb-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="463eb-157">På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="463eb-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="463eb-158">I dialogboksen **Legg til modul** under **Velg moduler** velger du en funksjonsmodul, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="463eb-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="463eb-159">I disposisjonstreet til venstre velger du funksjonsmodulen.</span><span class="sxs-lookup"><span data-stu-id="463eb-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="463eb-160">Velg **Legg til et bilde** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="463eb-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="463eb-161">Velg enten et eksisterende bilde, eller last opp et nytt bilde.</span><span class="sxs-lookup"><span data-stu-id="463eb-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="463eb-162">Velg **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="463eb-162">Select **Heading**.</span></span>
1. <span data-ttu-id="463eb-163">I dialogboksen **Overskrift** legger du til overskiftsteksten, velger overskiftsnivået og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="463eb-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="463eb-164">Under **Rik tekst** legger du til tekst etter behov.</span><span class="sxs-lookup"><span data-stu-id="463eb-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="463eb-165">Velg **Legg til handlingskobling**.</span><span class="sxs-lookup"><span data-stu-id="463eb-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="463eb-166">I dialogboksen **Handlingskobling** legger du til koblingstekst, en URL-adresse for kobling og en ARIA-etikett for koblingen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="463eb-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="463eb-167">Lagre siden, og forhåndsvis endringene.</span><span class="sxs-lookup"><span data-stu-id="463eb-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="463eb-168">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="463eb-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="463eb-169">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="463eb-169">Additional resources</span></span>

[<span data-ttu-id="463eb-170">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="463eb-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="463eb-171">Varselmodul</span><span class="sxs-lookup"><span data-stu-id="463eb-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="463eb-172">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="463eb-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="463eb-173">Innholdsrik blokk-modul</span><span class="sxs-lookup"><span data-stu-id="463eb-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="463eb-174">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="463eb-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="463eb-175">Hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="463eb-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="463eb-176">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="463eb-176">Video player module</span></span>](add-video-player.md)
