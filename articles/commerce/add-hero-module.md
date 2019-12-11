---
title: Hovedbannermodul
description: Dette emnet dekker hovedbannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785402"
---
# <a name="hero-module"></a><span data-ttu-id="486e0-103">Hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="486e0-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="486e0-104">Dette emnet dekker hovedbannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="486e0-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="486e0-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="486e0-105">Overview</span></span>

<span data-ttu-id="486e0-106">En hovedbannermodul brukes til å markedsføre produkter eller kampanjer ved hjelp av en kombinasjon av bilder og tekst.</span><span class="sxs-lookup"><span data-stu-id="486e0-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="486e0-107">En forhandler kan for eksempel legge til en hovedbannermodul på startsiden for et område for e-handel for å fremme et nytt produkt og tiltrekke oppmerksomheten til kundene.</span><span class="sxs-lookup"><span data-stu-id="486e0-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="486e0-108">En hovedbannermodul styres av data fra CMS (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="486e0-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="486e0-109">Det er en frittstående modul som ikke er avhengig av andre moduler på siden.</span><span class="sxs-lookup"><span data-stu-id="486e0-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="486e0-110">En hovedbannermodul kan være plassert på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, salg eller funksjoner).</span><span class="sxs-lookup"><span data-stu-id="486e0-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="486e0-111">Eksempler på hovedbannermodul i e-handel</span><span class="sxs-lookup"><span data-stu-id="486e0-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="486e0-112">En hovedbannermodul kan brukes på startsiden for et e-handelsområde for å utheve kampanjer og nye produkter.</span><span class="sxs-lookup"><span data-stu-id="486e0-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="486e0-113">En hovedbannermodul kan brukes på en produktdetaljside for å vise produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="486e0-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="486e0-114">Flere hovedbannermoduler kan plasseres i en karusellmodul for å utheve flere produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="486e0-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="486e0-115">Egenskaper for hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="486e0-115">Hero module properties</span></span>

| <span data-ttu-id="486e0-116">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="486e0-116">Property name</span></span>  | <span data-ttu-id="486e0-117">Verdier</span><span class="sxs-lookup"><span data-stu-id="486e0-117">Values</span></span> | <span data-ttu-id="486e0-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="486e0-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="486e0-119">Bilde</span><span class="sxs-lookup"><span data-stu-id="486e0-119">Image</span></span>          | <span data-ttu-id="486e0-120">Bildefil</span><span class="sxs-lookup"><span data-stu-id="486e0-120">Image file</span></span> | <span data-ttu-id="486e0-121">Et bilde kan brukes til å vise et produkt eller en kampanje.</span><span class="sxs-lookup"><span data-stu-id="486e0-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="486e0-122">Et bilde kan lastes opp til bildegalleriet, eller det kan brukes et eksisterende bilde.</span><span class="sxs-lookup"><span data-stu-id="486e0-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="486e0-123">Overskrift</span><span class="sxs-lookup"><span data-stu-id="486e0-123">Heading</span></span>        | <span data-ttu-id="486e0-124">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="486e0-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="486e0-125">Alle hovedbannermoduler kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="486e0-125">Every hero module can have a heading.</span></span> <span data-ttu-id="486e0-126">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="486e0-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="486e0-127">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="486e0-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="486e0-128">Avsnitt</span><span class="sxs-lookup"><span data-stu-id="486e0-128">Paragraph</span></span>      | <span data-ttu-id="486e0-129">Avsnittstekst</span><span class="sxs-lookup"><span data-stu-id="486e0-129">Paragraph text</span></span> | <span data-ttu-id="486e0-130">Hovedbannermoduler støtter avsnittstekst i rikt tekstformat.</span><span class="sxs-lookup"><span data-stu-id="486e0-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="486e0-131">Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst, og hyperkoblinger.</span><span class="sxs-lookup"><span data-stu-id="486e0-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="486e0-132">Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen.</span><span class="sxs-lookup"><span data-stu-id="486e0-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="486e0-133">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="486e0-133">Link</span></span>           | <span data-ttu-id="486e0-134">Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori**</span><span class="sxs-lookup"><span data-stu-id="486e0-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="486e0-135">Hovedbannermoduler støtter én eller flere "handlingsoppfordring"-koblinger.</span><span class="sxs-lookup"><span data-stu-id="486e0-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="486e0-136">Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett.</span><span class="sxs-lookup"><span data-stu-id="486e0-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="486e0-137">ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="486e0-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="486e0-138">Koblinger kan konfigureres slik at de åpnes i en ny fane.</span><span class="sxs-lookup"><span data-stu-id="486e0-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="486e0-139">Tekstplassering</span><span class="sxs-lookup"><span data-stu-id="486e0-139">Text placement</span></span> | <span data-ttu-id="486e0-140">**Øverst til venstre**, **Øverst til høyre**, **Øverst i midten**, **Nederst til venstre**, **Nederst til høyre**, **Nederst i midten**, **Midtstilt til venstre**, **Midtstilt til høyre** eller **Midtstilt i midten**</span><span class="sxs-lookup"><span data-stu-id="486e0-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="486e0-141">Denne egenskapen angir plasseringen av bildet i forhold til teksten.</span><span class="sxs-lookup"><span data-stu-id="486e0-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="486e0-142">Hvis for eksempel **Høyre** er valgt, vises bildet til høyre for teksten.</span><span class="sxs-lookup"><span data-stu-id="486e0-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="486e0-143">Teksttema</span><span class="sxs-lookup"><span data-stu-id="486e0-143">Text theme</span></span>     | <span data-ttu-id="486e0-144">**Lys** eller **Mørk**</span><span class="sxs-lookup"><span data-stu-id="486e0-144">**Light** or **Dark**</span></span> | <span data-ttu-id="486e0-145">Du kan definere et fargevalg for teksten basert på bakgrunnsbildet.</span><span class="sxs-lookup"><span data-stu-id="486e0-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="486e0-146">Hvis bildet for eksempel har en mørk bakgrunn, kan du bruke et lyst tema for å få teksten til å være mer synlig, og for å imøtekomme fargekontrastforhold for tilgjengelighetsformål.</span><span class="sxs-lookup"><span data-stu-id="486e0-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="486e0-147">Gradering</span><span class="sxs-lookup"><span data-stu-id="486e0-147">Gradient</span></span>       | <span data-ttu-id="486e0-148">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="486e0-148">**True** or **False**</span></span> | <span data-ttu-id="486e0-149">En gradering kan brukes på bildet for å imøtekomme fargekontrastforhold for tilgjengelighetsformål.</span><span class="sxs-lookup"><span data-stu-id="486e0-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="486e0-150">Legge til en hovedbannermodul på en ny side</span><span class="sxs-lookup"><span data-stu-id="486e0-150">Add a hero module to a new page</span></span>

<span data-ttu-id="486e0-151">Hvis du vil legge til en hovedbannermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="486e0-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="486e0-152">Gå til **Maler**, og opprett en sidemal kalt **hovedbannermal**.</span><span class="sxs-lookup"><span data-stu-id="486e0-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="486e0-153">I **Hoved**-sporet på standardsiden legger du til en hovedbannermodul.</span><span class="sxs-lookup"><span data-stu-id="486e0-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="486e0-154">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="486e0-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="486e0-155">Bruk hovedbannermalen du nettopp opprettet, for å opprette en side som heter **hovedbannerside**.</span><span class="sxs-lookup"><span data-stu-id="486e0-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="486e0-156">På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="486e0-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="486e0-157">I dialogboksen **Legg til modul** under **Velg moduler** velger du hovedbannermodulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="486e0-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="486e0-158">I disposisjonstreet til venstre velger du hovedbannermodulen.</span><span class="sxs-lookup"><span data-stu-id="486e0-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="486e0-159">Velg **Legg til et bilde** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="486e0-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="486e0-160">Velg enten et eksisterende bilde, eller last opp et nytt bilde.</span><span class="sxs-lookup"><span data-stu-id="486e0-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="486e0-161">Velg **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="486e0-161">Select **Heading**.</span></span>
1. <span data-ttu-id="486e0-162">I dialogboksen **Overskrift** legger du til overskiftsteksten, velger overskiftsnivået og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="486e0-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="486e0-163">Under **Rik tekst** legger du til tekst etter behov.</span><span class="sxs-lookup"><span data-stu-id="486e0-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="486e0-164">Velg **Legg til handlingskobling**.</span><span class="sxs-lookup"><span data-stu-id="486e0-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="486e0-165">I dialogboksen **Handlingskobling** legger du til koblingstekst, en URL-adresse for kobling og en ARIA-etikett for koblingen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="486e0-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="486e0-166">Lagre siden, og forhåndsvis endringene.</span><span class="sxs-lookup"><span data-stu-id="486e0-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="486e0-167">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="486e0-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="486e0-168">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="486e0-168">Additional resources</span></span>

[<span data-ttu-id="486e0-169">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="486e0-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="486e0-170">Varselmodul</span><span class="sxs-lookup"><span data-stu-id="486e0-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="486e0-171">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="486e0-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="486e0-172">Innholdsrik blokk-modul</span><span class="sxs-lookup"><span data-stu-id="486e0-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="486e0-173">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="486e0-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="486e0-174">Funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="486e0-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="486e0-175">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="486e0-175">Video player module</span></span>](add-video-player.md)
