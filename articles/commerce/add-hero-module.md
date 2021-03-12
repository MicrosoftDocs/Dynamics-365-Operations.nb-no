---
title: Innholdsblokkmodul
description: Dette emnet dekker innholdsblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6359c915d053bb00c969b166325f675c0003ead
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980363"
---
# <a name="content-block-module"></a><span data-ttu-id="9ab14-103">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="9ab14-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9ab14-104">Dette emnet dekker innholdsblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9ab14-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9ab14-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="9ab14-105">Overview</span></span>

<span data-ttu-id="9ab14-106">En innholdsblokkmodul brukes til å markedsføre produkter eller kampanjer ved hjelp av en kombinasjon av bilder og tekst.</span><span class="sxs-lookup"><span data-stu-id="9ab14-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="9ab14-107">En forhandler kan for eksempel legge til en innholdsblokkmodul på startsiden for et område for e-handel for å fremme et nytt produkt og tiltrekke oppmerksomheten til kundene.</span><span class="sxs-lookup"><span data-stu-id="9ab14-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="9ab14-108">En innholdsblokkmodul styres av data fra CMS (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="9ab14-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="9ab14-109">Det er en frittstående modul som ikke er avhengig av andre moduler på siden.</span><span class="sxs-lookup"><span data-stu-id="9ab14-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="9ab14-110">En innholdsblokkmodul kan være plassert på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, salg eller funksjoner).</span><span class="sxs-lookup"><span data-stu-id="9ab14-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="9ab14-111">Eksempler på innholdsblokkmodul i e-handel</span><span class="sxs-lookup"><span data-stu-id="9ab14-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="9ab14-112">En innholdsblokkmodul kan brukes på startsiden for et e-handelsområde for å utheve kampanjer og nye produkter.</span><span class="sxs-lookup"><span data-stu-id="9ab14-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="9ab14-113">En innholdsblokkmodul kan brukes på en produktdetaljside for å vise produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="9ab14-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="9ab14-114">Flere innholdsblokkmoduler kan plasseres i en karusellmodul for å utheve flere produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="9ab14-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="9ab14-115">Innholdsblokkmoduler og temaer</span><span class="sxs-lookup"><span data-stu-id="9ab14-115">Content block modules and themes</span></span>

<span data-ttu-id="9ab14-116">Innholdsblokkmoduler kan støtte ulike oppsett og stiler basert på et tema.</span><span class="sxs-lookup"><span data-stu-id="9ab14-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="9ab14-117">For eksempel støtter Fabrikam-temaet tre oppsettsvariasjoner av en innholdsblokkmodul: hovedbanner, funksjon og flis.</span><span class="sxs-lookup"><span data-stu-id="9ab14-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="9ab14-118">Hovedbanneroppsettet viser et bilde på bakgrunnen med tekstoverlegg.</span><span class="sxs-lookup"><span data-stu-id="9ab14-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="9ab14-119">Funksjonsoppsettet viser et bilde og tekst side ved side.</span><span class="sxs-lookup"><span data-stu-id="9ab14-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="9ab14-120">Flisoppsettet tillater flere innholdsblokker i flisformat.</span><span class="sxs-lookup"><span data-stu-id="9ab14-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="9ab14-121">I tillegg kan temaet vise forskjellige egenskaper for hvert oppsett.</span><span class="sxs-lookup"><span data-stu-id="9ab14-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="9ab14-122">En temautvikler kan bygge flere oppsett med flere stiler ved hjelp av innholdsblokkmodulen.</span><span class="sxs-lookup"><span data-stu-id="9ab14-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="9ab14-123">Bildet nedenfor viser et eksempel på en innholdsblokkmodul med et hovedbanneroppsett.</span><span class="sxs-lookup"><span data-stu-id="9ab14-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Eksempel på en hovedbannermodul](./media/Hero.PNG)

<span data-ttu-id="9ab14-125">Bildet nedenfor viser et eksempel på en innholdsblokkmodul med et funksjonsoppsett.</span><span class="sxs-lookup"><span data-stu-id="9ab14-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Eksempler på funksjonsmoduler](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="9ab14-127">Egenskaper for innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="9ab14-127">Content block module properties</span></span>

| <span data-ttu-id="9ab14-128">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="9ab14-128">Property name</span></span>  | <span data-ttu-id="9ab14-129">Verdier</span><span class="sxs-lookup"><span data-stu-id="9ab14-129">Values</span></span> | <span data-ttu-id="9ab14-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9ab14-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="9ab14-131">Bilde</span><span class="sxs-lookup"><span data-stu-id="9ab14-131">Image</span></span>          | <span data-ttu-id="9ab14-132">Bildefil</span><span class="sxs-lookup"><span data-stu-id="9ab14-132">Image file</span></span> | <span data-ttu-id="9ab14-133">Et bilde kan brukes til å vise et produkt eller en kampanje.</span><span class="sxs-lookup"><span data-stu-id="9ab14-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="9ab14-134">Et bilde kan lastes opp til bildegalleriet, eller det kan brukes et eksisterende bilde.</span><span class="sxs-lookup"><span data-stu-id="9ab14-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="9ab14-135">Overskrift</span><span class="sxs-lookup"><span data-stu-id="9ab14-135">Heading</span></span>        | <span data-ttu-id="9ab14-136">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="9ab14-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="9ab14-137">Alle hovedbannermoduler kan ha en overskrift.</span><span class="sxs-lookup"><span data-stu-id="9ab14-137">Every hero module can have a heading.</span></span> <span data-ttu-id="9ab14-138">Som standard brukes **H2**-overskriftskoden for overskriften.</span><span class="sxs-lookup"><span data-stu-id="9ab14-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="9ab14-139">Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="9ab14-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="9ab14-140">Avsnitt</span><span class="sxs-lookup"><span data-stu-id="9ab14-140">Paragraph</span></span>      | <span data-ttu-id="9ab14-141">Avsnittstekst</span><span class="sxs-lookup"><span data-stu-id="9ab14-141">Paragraph text</span></span> | <span data-ttu-id="9ab14-142">Hovedbannermoduler støtter avsnittstekst i rikt tekstformat.</span><span class="sxs-lookup"><span data-stu-id="9ab14-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="9ab14-143">Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst, og hyperkoblinger.</span><span class="sxs-lookup"><span data-stu-id="9ab14-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="9ab14-144">Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen.</span><span class="sxs-lookup"><span data-stu-id="9ab14-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="9ab14-145">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="9ab14-145">Link</span></span>           | <span data-ttu-id="9ab14-146">Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori**</span><span class="sxs-lookup"><span data-stu-id="9ab14-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="9ab14-147">Hovedbannermoduler støtter én eller flere "handlingsoppfordring"-koblinger.</span><span class="sxs-lookup"><span data-stu-id="9ab14-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="9ab14-148">Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett.</span><span class="sxs-lookup"><span data-stu-id="9ab14-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="9ab14-149">ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene.</span><span class="sxs-lookup"><span data-stu-id="9ab14-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="9ab14-150">Koblinger kan konfigureres slik at de åpnes i en ny fane.</span><span class="sxs-lookup"><span data-stu-id="9ab14-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="9ab14-151">Egenskaper for innholdsblokkmodul vist med Fabrikam-temaet</span><span class="sxs-lookup"><span data-stu-id="9ab14-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="9ab14-152">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="9ab14-152">Property name</span></span>  | <span data-ttu-id="9ab14-153">Verdier</span><span class="sxs-lookup"><span data-stu-id="9ab14-153">Values</span></span> | <span data-ttu-id="9ab14-154">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9ab14-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="9ab14-155">Tekstplassering</span><span class="sxs-lookup"><span data-stu-id="9ab14-155">Text placement</span></span> | <span data-ttu-id="9ab14-156">**Venstre**, **Høyre**, **Midtstilt**</span><span class="sxs-lookup"><span data-stu-id="9ab14-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="9ab14-157">Denne egenskapen angir plasseringen av teksten i bildet.</span><span class="sxs-lookup"><span data-stu-id="9ab14-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="9ab14-158">Den gjelder bare for hovedbanneroppsettet.</span><span class="sxs-lookup"><span data-stu-id="9ab14-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="9ab14-159">Teksttema</span><span class="sxs-lookup"><span data-stu-id="9ab14-159">Text theme</span></span>     | <span data-ttu-id="9ab14-160">**Lys** eller **Mørk**</span><span class="sxs-lookup"><span data-stu-id="9ab14-160">**Light** or **Dark**</span></span> | <span data-ttu-id="9ab14-161">Du kan definere et fargevalg for teksten basert på bakgrunnsbildet.</span><span class="sxs-lookup"><span data-stu-id="9ab14-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="9ab14-162">Hvis bildet for eksempel har en mørk bakgrunn, kan du bruke et lyst tema for å få teksten til å være mer synlig, og for å imøtekomme fargekontrastforhold for tilgjengelighetsformål.</span><span class="sxs-lookup"><span data-stu-id="9ab14-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="9ab14-163">Den gjelder bare for hovedbanneroppsettet.</span><span class="sxs-lookup"><span data-stu-id="9ab14-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="9ab14-164">Bildeplassering</span><span class="sxs-lookup"><span data-stu-id="9ab14-164">Image placement</span></span>       | <span data-ttu-id="9ab14-165">**Venstre**, **Høyre**</span><span class="sxs-lookup"><span data-stu-id="9ab14-165">**Left**,  **Right**</span></span> | <span data-ttu-id="9ab14-166">Denne egenskapen angir om bildet skal være til venstre eller høyre for teksten.</span><span class="sxs-lookup"><span data-stu-id="9ab14-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="9ab14-167">Den gjelder bare for funksjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="9ab14-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="9ab14-168">Legge til en innholdsblokkmodul på en ny side</span><span class="sxs-lookup"><span data-stu-id="9ab14-168">Add a content block module to a new page</span></span>

<span data-ttu-id="9ab14-169">Hvis du vil legge til en hovedbannermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="9ab14-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9ab14-170">Gå til **Maler**, og opprett en sidemal kalt **innholdsblokkmal**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="9ab14-171">I **Hoved**-sporet på standardsiden legger du til en hovedbannermodul.</span><span class="sxs-lookup"><span data-stu-id="9ab14-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="9ab14-172">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="9ab14-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="9ab14-173">Bruk hovedbannermalen du nettopp opprettet, for å opprette en side som heter **innholdsblokkside**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="9ab14-174">På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9ab14-175">I dialogboksen **Legg til modul** under **Velg moduler** velger du hovedbannermodulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="9ab14-176">I disposisjonstreet til venstre velger du innholdsblokkmodulen.</span><span class="sxs-lookup"><span data-stu-id="9ab14-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="9ab14-177">Velg **Legg til et bilde** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="9ab14-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="9ab14-178">Velg enten et eksisterende bilde, eller last opp et nytt bilde.</span><span class="sxs-lookup"><span data-stu-id="9ab14-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="9ab14-179">Velg **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-179">Select **Heading**.</span></span>
1. <span data-ttu-id="9ab14-180">I dialogboksen **Overskrift** legger du til overskiftsteksten, velger overskiftsnivået og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="9ab14-181">Under **Rik tekst** legger du til tekst etter behov.</span><span class="sxs-lookup"><span data-stu-id="9ab14-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="9ab14-182">Velg **Legg til kobling**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="9ab14-183">I dialogboksen **Kobling** legger du til koblingstekst, en URL-adresse for kobling og en ARIA-etikett for koblingen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ab14-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="9ab14-184">Velg **Hovedbanner**-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="9ab14-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="9ab14-185">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="9ab14-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="9ab14-186">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="9ab14-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9ab14-187">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9ab14-187">Additional resources</span></span>

[<span data-ttu-id="9ab14-188">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="9ab14-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9ab14-189">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="9ab14-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="9ab14-190">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="9ab14-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="9ab14-191">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="9ab14-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9ab14-192">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="9ab14-192">Video player module</span></span>](add-video-player.md)
