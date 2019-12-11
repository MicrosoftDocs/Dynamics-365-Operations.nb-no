---
title: Innholdsrik blokkmodul
description: Dette emnet dekker innholdsrike blokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785427"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="794c1-103">Innholdsrik blokkmodul</span><span class="sxs-lookup"><span data-stu-id="794c1-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="794c1-104">Dette emnet dekker innholdsrike blokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="794c1-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="794c1-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="794c1-105">Overview</span></span>

<span data-ttu-id="794c1-106">En innholdsrik blokkmodul er en spesialcontainer som én eller flere innholdsrike blokkelementer kan plasseres i.</span><span class="sxs-lookup"><span data-stu-id="794c1-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="794c1-107">Innholdsrike blokkmoduler brukes til tekstinnhold på en side.</span><span class="sxs-lookup"><span data-stu-id="794c1-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="794c1-108">Dette innholdet kan enten være informasjon eller kampanje.</span><span class="sxs-lookup"><span data-stu-id="794c1-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="794c1-109">Innholdsrike blokkmoduler drives av data fra innholdsbehandlingssystemet (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="794c1-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="794c1-110">De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="794c1-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="794c1-111">Eksempler på innholdsrike blokkmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="794c1-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="794c1-112">Innholdsrike blokkmoduler kan brukes på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="794c1-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="794c1-113">For å vise produktfunksjoner på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="794c1-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="794c1-114">Til informasjonsformål på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="794c1-114">For informational purposes on any page.</span></span> <span data-ttu-id="794c1-115">De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.</span><span class="sxs-lookup"><span data-stu-id="794c1-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="794c1-116">Legge til egendefinerte meldinger på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="794c1-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="794c1-117">(for eksempel "Gratis levering ved bestilling over 500 kroner").</span><span class="sxs-lookup"><span data-stu-id="794c1-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="794c1-118">For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").</span><span class="sxs-lookup"><span data-stu-id="794c1-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="794c1-119">Egenskaper for innholdsrik blokkmodul</span><span class="sxs-lookup"><span data-stu-id="794c1-119">Content rich block module properties</span></span>

| <span data-ttu-id="794c1-120">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="794c1-120">Property name</span></span>     | <span data-ttu-id="794c1-121">Verdi</span><span class="sxs-lookup"><span data-stu-id="794c1-121">Value</span></span>                                 | <span data-ttu-id="794c1-122">Egenskap</span><span class="sxs-lookup"><span data-stu-id="794c1-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="794c1-123">Antall kolonner</span><span class="sxs-lookup"><span data-stu-id="794c1-123">Number of columns</span></span> | <span data-ttu-id="794c1-124">Et tall fra **1** til **4**</span><span class="sxs-lookup"><span data-stu-id="794c1-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="794c1-125">Antall kolonner i den innholdsrike blokken.</span><span class="sxs-lookup"><span data-stu-id="794c1-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="794c1-126">Det kan være opptil fire kolonner.</span><span class="sxs-lookup"><span data-stu-id="794c1-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="794c1-127">Bredde</span><span class="sxs-lookup"><span data-stu-id="794c1-127">Width</span></span>             | <span data-ttu-id="794c1-128">**Fyll container** eller **Fyll skjerm**</span><span class="sxs-lookup"><span data-stu-id="794c1-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="794c1-129">Hvis verdien er satt til **Fyll container**, er elementene i containeren begrenset til bredden på containeren.</span><span class="sxs-lookup"><span data-stu-id="794c1-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="794c1-130">Hvis verdien er satt til **Fyll skjerm**, er ikke elementene begrenset til containerbredden, men de kan gå i fullskjermmodus.</span><span class="sxs-lookup"><span data-stu-id="794c1-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="794c1-131">Du kan endre verdien for å oppnå det ønskede oppsettet.</span><span class="sxs-lookup"><span data-stu-id="794c1-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="794c1-132">Egenskaper for innholdsrik blokkelementmodul</span><span class="sxs-lookup"><span data-stu-id="794c1-132">Content rich block item module properties</span></span>

| <span data-ttu-id="794c1-133">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="794c1-133">Property name</span></span> | <span data-ttu-id="794c1-134">Verdi</span><span class="sxs-lookup"><span data-stu-id="794c1-134">Value</span></span>          | <span data-ttu-id="794c1-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="794c1-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="794c1-136">Avsnitt</span><span class="sxs-lookup"><span data-stu-id="794c1-136">Paragraph</span></span>     | <span data-ttu-id="794c1-137">Avsnittstekst</span><span class="sxs-lookup"><span data-stu-id="794c1-137">Paragraph text</span></span> | <span data-ttu-id="794c1-138">Teksten som følger med alle innholdsrike blokkelementer.</span><span class="sxs-lookup"><span data-stu-id="794c1-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="794c1-139">Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst.</span><span class="sxs-lookup"><span data-stu-id="794c1-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="794c1-140">Legge til en innholdsrik blokkmodul på en side</span><span class="sxs-lookup"><span data-stu-id="794c1-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="794c1-141">Hvis du vil legge til en innholdsrik blokkmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="794c1-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="794c1-142">Opprett en sidemal som heter **Innholdsmal**.</span><span class="sxs-lookup"><span data-stu-id="794c1-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="794c1-143">I **Hoved**-sporet på standardsiden legger du til en innholdsrik blokkmodul.</span><span class="sxs-lookup"><span data-stu-id="794c1-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="794c1-144">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="794c1-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="794c1-145">Bruk innholdsmalen du nettopp opprettet, for å opprette en side som heter **Innholdsside**.</span><span class="sxs-lookup"><span data-stu-id="794c1-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="794c1-146">I **Hoved**-sporet på den nye siden legger du til en innholdsrik blokkmodul.</span><span class="sxs-lookup"><span data-stu-id="794c1-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="794c1-147">I egenskapene til den innholdsrike blokkmodulen angir du antall kolonner til **2**.</span><span class="sxs-lookup"><span data-stu-id="794c1-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="794c1-148">I den innholdsrike blokkmodulen velger du **Legg til en modul**, og deretter legger til et innholdsrikt blokkelement (for eksempel **element1**).</span><span class="sxs-lookup"><span data-stu-id="794c1-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="794c1-149">Legg til avsnittstekst i det nye innholdsrike blokkelementet.</span><span class="sxs-lookup"><span data-stu-id="794c1-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="794c1-150">I den innholdsrike blokkmodulen velger du **Legg til en modul**, og deretter legger til et innholdsrikt blokkelement (for eksempel **element2**).</span><span class="sxs-lookup"><span data-stu-id="794c1-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="794c1-151">Legg til avsnittstekst i det nye innholdsrike blokkelementet.</span><span class="sxs-lookup"><span data-stu-id="794c1-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="794c1-152">Lagre siden, og forhåndsvis endringene.</span><span class="sxs-lookup"><span data-stu-id="794c1-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="794c1-153">Du skal se to riktekstblokker i en visning med to spalter.</span><span class="sxs-lookup"><span data-stu-id="794c1-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="794c1-154">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="794c1-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="794c1-155">Hvis du legger til et tredje innholdsrikt blokkelement, blir det stablet under de to elementene som du har lagt til tidligere.</span><span class="sxs-lookup"><span data-stu-id="794c1-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="794c1-156">Ved å endre antallet kolonner og elementer i containeren, kan du oppnå forskjellige oppsett for tekstinnhold.</span><span class="sxs-lookup"><span data-stu-id="794c1-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="794c1-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="794c1-157">Additional resources</span></span>

[<span data-ttu-id="794c1-158">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="794c1-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="794c1-159">Varselmodul</span><span class="sxs-lookup"><span data-stu-id="794c1-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="794c1-160">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="794c1-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="794c1-161">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="794c1-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="794c1-162">Funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="794c1-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="794c1-163">Hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="794c1-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="794c1-164">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="794c1-164">Video player module</span></span>](add-video-player.md)

