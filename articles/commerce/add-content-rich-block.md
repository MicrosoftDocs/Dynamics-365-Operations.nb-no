---
title: Tekstblokkmodul
description: Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025603"
---
# <a name="text-block-module"></a><span data-ttu-id="081c4-103">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="081c4-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="081c4-104">Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="081c4-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="081c4-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="081c4-105">Overview</span></span>

<span data-ttu-id="081c4-106">En tekstblokkmodul er en modul som brukes til å legge til tekstinnhold.</span><span class="sxs-lookup"><span data-stu-id="081c4-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="081c4-107">Dette innholdet kan være informasjon eller kampanje.</span><span class="sxs-lookup"><span data-stu-id="081c4-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="081c4-108">Tekstblokkmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="081c4-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="081c4-109">De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="081c4-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="081c4-110">Eksempler på tekstblokkmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="081c4-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="081c4-111">Tekstblokkmoduler kan brukes på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="081c4-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="081c4-112">For å vise produktfunksjoner på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="081c4-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="081c4-113">Til informasjonsformål på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="081c4-113">For informational purposes on any page.</span></span> <span data-ttu-id="081c4-114">De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.</span><span class="sxs-lookup"><span data-stu-id="081c4-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="081c4-115">Legge til egendefinerte meldinger på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="081c4-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="081c4-116">(for eksempel "Gratis levering ved bestilling over 500 kroner").</span><span class="sxs-lookup"><span data-stu-id="081c4-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="081c4-117">For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").</span><span class="sxs-lookup"><span data-stu-id="081c4-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="081c4-118">Egenskaper for tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="081c4-118">Text block module properties</span></span>

| <span data-ttu-id="081c4-119">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="081c4-119">Property name</span></span>     | <span data-ttu-id="081c4-120">Value</span><span class="sxs-lookup"><span data-stu-id="081c4-120">Value</span></span>                                            | <span data-ttu-id="081c4-121">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="081c4-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="081c4-122">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="081c4-122">Rich text</span></span>         | <span data-ttu-id="081c4-123">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="081c4-123">Rich text</span></span>                                        | <span data-ttu-id="081c4-124">Avsnittstekst.</span><span class="sxs-lookup"><span data-stu-id="081c4-124">Paragraph text.</span></span> <span data-ttu-id="081c4-125">Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst.</span><span class="sxs-lookup"><span data-stu-id="081c4-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="081c4-126">Egendefinert klassenavn</span><span class="sxs-lookup"><span data-stu-id="081c4-126">Custom class name</span></span> | <span data-ttu-id="081c4-127">Et CSS-klassenavn (Cascading Style Sheets)</span><span class="sxs-lookup"><span data-stu-id="081c4-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="081c4-128">Navnet på en egendefinert CSS-klasse som en utvikler tilbyr for å formatere denne modulen.</span><span class="sxs-lookup"><span data-stu-id="081c4-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="081c4-129">Klassenavnet bør defineres i temapakken.</span><span class="sxs-lookup"><span data-stu-id="081c4-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="081c4-130">Skriftstørrelse</span><span class="sxs-lookup"><span data-stu-id="081c4-130">Font size</span></span>         | <span data-ttu-id="081c4-131">**Liten**, **middels**, **stor** eller **ekstra stor**</span><span class="sxs-lookup"><span data-stu-id="081c4-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="081c4-132">Skriftstørrelse for innholdet.</span><span class="sxs-lookup"><span data-stu-id="081c4-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="081c4-133">Legge til en tekstblokkmodul på en side</span><span class="sxs-lookup"><span data-stu-id="081c4-133">Add a text block module to a page</span></span>

<span data-ttu-id="081c4-134">Hvis du vil legge til en tekstblokkmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="081c4-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="081c4-135">Opprett en sidemal som heter **Innholdsmal**.</span><span class="sxs-lookup"><span data-stu-id="081c4-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="081c4-136">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="081c4-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="081c4-137">Fullfør redigeringen av malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="081c4-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="081c4-138">Bruk innholdsmalen du nettopp opprettet, for å opprette en side som heter **Innholdsside**.</span><span class="sxs-lookup"><span data-stu-id="081c4-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="081c4-139">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="081c4-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="081c4-140">I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="081c4-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="081c4-141">Legg til en tekstblokkmodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="081c4-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="081c4-142">I egenskapsruten for tekstblokkmodulen legger du til tekst i feltet **Rik tekst**.</span><span class="sxs-lookup"><span data-stu-id="081c4-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="081c4-143">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="081c4-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="081c4-144">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="081c4-144">Additional resources</span></span>

[<span data-ttu-id="081c4-145">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="081c4-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="081c4-146">Kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="081c4-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="081c4-147">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="081c4-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="081c4-148">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="081c4-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="081c4-149">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="081c4-149">Video player module</span></span>](add-video-player.md)

