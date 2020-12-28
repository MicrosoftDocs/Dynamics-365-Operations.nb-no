---
title: Tekstblokkmodul
description: Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414579"
---
# <a name="text-block-module"></a><span data-ttu-id="b580b-103">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b580b-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b580b-104">Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b580b-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b580b-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b580b-105">Overview</span></span>

<span data-ttu-id="b580b-106">En tekstblokkmodul er en modul som brukes til å legge til tekstinnhold.</span><span class="sxs-lookup"><span data-stu-id="b580b-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="b580b-107">Dette innholdet kan være informasjon eller kampanje.</span><span class="sxs-lookup"><span data-stu-id="b580b-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="b580b-108">Tekstblokkmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="b580b-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="b580b-109">De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="b580b-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="b580b-110">Eksempler på tekstblokkmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="b580b-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="b580b-111">Tekstblokkmoduler kan brukes på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="b580b-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="b580b-112">For å vise produktfunksjoner på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="b580b-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="b580b-113">Til informasjonsformål på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="b580b-113">For informational purposes on any page.</span></span> <span data-ttu-id="b580b-114">De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.</span><span class="sxs-lookup"><span data-stu-id="b580b-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="b580b-115">Legge til egendefinerte meldinger på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="b580b-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="b580b-116">(for eksempel "Gratis levering ved bestilling over 500 kroner").</span><span class="sxs-lookup"><span data-stu-id="b580b-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="b580b-117">For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").</span><span class="sxs-lookup"><span data-stu-id="b580b-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="b580b-118">Bildet nedenfor viser et eksempel på en tekstblokkmodul som brukes på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="b580b-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Eksempel på en tekstblokkmodul](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="b580b-120">Egenskaper for tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b580b-120">Text block module properties</span></span>

| <span data-ttu-id="b580b-121">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="b580b-121">Property name</span></span>     | <span data-ttu-id="b580b-122">Verdi</span><span class="sxs-lookup"><span data-stu-id="b580b-122">Value</span></span>                                            | <span data-ttu-id="b580b-123">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b580b-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="b580b-124">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="b580b-124">Rich text</span></span>         | <span data-ttu-id="b580b-125">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="b580b-125">Rich text</span></span>                                        | <span data-ttu-id="b580b-126">Avsnittstekst.</span><span class="sxs-lookup"><span data-stu-id="b580b-126">Paragraph text.</span></span> <span data-ttu-id="b580b-127">Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst.</span><span class="sxs-lookup"><span data-stu-id="b580b-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="b580b-128">Egendefinert klassenavn</span><span class="sxs-lookup"><span data-stu-id="b580b-128">Custom class name</span></span> | <span data-ttu-id="b580b-129">Et CSS-klassenavn (Cascading Style Sheets)</span><span class="sxs-lookup"><span data-stu-id="b580b-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="b580b-130">Navnet på en egendefinert CSS-klasse som en utvikler tilbyr for å formatere denne modulen.</span><span class="sxs-lookup"><span data-stu-id="b580b-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="b580b-131">Klassenavnet bør defineres i temapakken.</span><span class="sxs-lookup"><span data-stu-id="b580b-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="b580b-132">Skriftstørrelse</span><span class="sxs-lookup"><span data-stu-id="b580b-132">Font size</span></span>         | <span data-ttu-id="b580b-133">**Liten**, **middels**, **stor** eller **ekstra stor**</span><span class="sxs-lookup"><span data-stu-id="b580b-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="b580b-134">Skriftstørrelse for innholdet.</span><span class="sxs-lookup"><span data-stu-id="b580b-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="b580b-135">Legge til en tekstblokkmodul på en side</span><span class="sxs-lookup"><span data-stu-id="b580b-135">Add a text block module to a page</span></span>

<span data-ttu-id="b580b-136">Hvis du vil legge til en tekstblokkmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="b580b-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b580b-137">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="b580b-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b580b-138">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Innholdsmal**.</span><span class="sxs-lookup"><span data-stu-id="b580b-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="b580b-139">I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b580b-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b580b-140">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b580b-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b580b-141">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="b580b-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b580b-142">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="b580b-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b580b-143">I **Velg en mal**-dialogboksen velger du **Innholdsmal**.</span><span class="sxs-lookup"><span data-stu-id="b580b-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="b580b-144">Under **Sidenavn** angir du **Innholdsside**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b580b-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="b580b-145">På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b580b-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b580b-146">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b580b-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b580b-147">I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="b580b-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="b580b-148">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b580b-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b580b-149">I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b580b-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="b580b-150">I egenskapsruten for tekstblokkmodulen legger du til tekst i feltet **Rik tekst**.</span><span class="sxs-lookup"><span data-stu-id="b580b-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="b580b-151">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="b580b-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b580b-152">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="b580b-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b580b-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b580b-153">Additional resources</span></span>

[<span data-ttu-id="b580b-154">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="b580b-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b580b-155">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="b580b-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b580b-156">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="b580b-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b580b-157">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b580b-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="b580b-158">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="b580b-158">Video player module</span></span>](add-video-player.md)

