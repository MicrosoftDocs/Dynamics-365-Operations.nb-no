---
title: Kampanjebannermodul
description: Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025626"
---
# <a name="promo-banner-module"></a><span data-ttu-id="b0cb1-103">Kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="b0cb1-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b0cb1-104">Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b0cb1-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b0cb1-105">Overview</span></span>

<span data-ttu-id="b0cb1-106">Kampanjebannermoduler brukes til å vise meldinger med innebygd informasjon på en side.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="b0cb1-107">De kan brukes til å vise kampanjer på hele området som vises på alle sider av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="b0cb1-108">Kampanjebannermoduler støtter en tekstmelding og en kobling.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="b0cb1-109">Hvis det legges til flere meldinger i en kampanjebannermodul, blir den en roterende karusellbanner som lar kundene gå gjennom alle meldingene.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="b0cb1-110">Kampanjebannermoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="b0cb1-111">Eksempler på bruk av kampanjebannere i e-handel</span><span class="sxs-lookup"><span data-stu-id="b0cb1-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="b0cb1-112">Kampanjebannere kan brukes i områdehodet til å vise kampanjer eller meldinger på hele området, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="b0cb1-113">"Årlige salg avsluttes om 10 dager"</span><span class="sxs-lookup"><span data-stu-id="b0cb1-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="b0cb1-114">"Gjør store besparelse på skolestartsalget.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-114">"Save big with back to school sale.</span></span> <span data-ttu-id="b0cb1-115">Handle nå. "</span><span class="sxs-lookup"><span data-stu-id="b0cb1-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="b0cb1-116">Egenskaper for kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="b0cb1-116">Promo banner module properties</span></span>

| <span data-ttu-id="b0cb1-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="b0cb1-117">Property name</span></span>             | <span data-ttu-id="b0cb1-118">Value</span><span class="sxs-lookup"><span data-stu-id="b0cb1-118">Value</span></span>                              | <span data-ttu-id="b0cb1-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b0cb1-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="b0cb1-120">Bannermeldinger</span><span class="sxs-lookup"><span data-stu-id="b0cb1-120">Banner messages</span></span>           | <span data-ttu-id="b0cb1-121">Tekst og koblinger</span><span class="sxs-lookup"><span data-stu-id="b0cb1-121">Text and links</span></span>                     | <span data-ttu-id="b0cb1-122">En matrise med tekst og koblinger.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-122">An array of text and links.</span></span> |
| <span data-ttu-id="b0cb1-123">Automatisk avspilling</span><span class="sxs-lookup"><span data-stu-id="b0cb1-123">Autoplay</span></span>                  | <span data-ttu-id="b0cb1-124">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b0cb1-124">**True** or **False**</span></span>              | <span data-ttu-id="b0cb1-125">En verdi som angir om meldinger gås gjennom automatisk hvis flere meldinger er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="b0cb1-126">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="b0cb1-126">Slide transition interval</span></span> | <span data-ttu-id="b0cb1-127">Et tall i millisekunder (ms)</span><span class="sxs-lookup"><span data-stu-id="b0cb1-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="b0cb1-128">Intervallet som brukes til å bla gjennom meldinger.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="b0cb1-129">Tillat forkastelse</span><span class="sxs-lookup"><span data-stu-id="b0cb1-129">Allow dismiss</span></span>             | <span data-ttu-id="b0cb1-130">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b0cb1-130">**True** or **False**</span></span>              | <span data-ttu-id="b0cb1-131">Hvis verdien settes til **Sann**, kan kundene forkaste varselet.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="b0cb1-132">Vis karusellflipper</span><span class="sxs-lookup"><span data-stu-id="b0cb1-132">Show carousel flipper</span></span>     | <span data-ttu-id="b0cb1-133">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="b0cb1-133">**True** or **False**</span></span>              | <span data-ttu-id="b0cb1-134">En verdi som angir om karusellflipperne skal vises, slik at kunder manuelt kan gå gjennom flere bannerelementer.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="b0cb1-135">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="b0cb1-135">Text alignment</span></span>            | <span data-ttu-id="b0cb1-136">**Høyre**, **Venstre** eller **Midtstilt**</span><span class="sxs-lookup"><span data-stu-id="b0cb1-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="b0cb1-137">Tekstjusteringen i kampanjebannermodulen.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="b0cb1-138">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="b0cb1-138">Link</span></span>                      | <span data-ttu-id="b0cb1-139">En URL</span><span class="sxs-lookup"><span data-stu-id="b0cb1-139">A URL</span></span>                              | <span data-ttu-id="b0cb1-140">URL-adresse for valgfri kobling.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="b0cb1-141">Legge til en kampanjebannermodul på en side</span><span class="sxs-lookup"><span data-stu-id="b0cb1-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="b0cb1-142">Hvis du vil legge til en kampanjebannermodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b0cb1-143">Opprett en sidemal som heter **Kampanjebannermal**.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="b0cb1-144">Under **Sideoppsett** legger du til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="b0cb1-145">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="b0cb1-146">Bruk malen du nettopp opprettet, for å opprette en side som heter **Kampanjebannerside**.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="b0cb1-147">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="b0cb1-148">I ruten til høyre setter du **Bredde**-verdien til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="b0cb1-149">Under **Sideoppsett** legger du til en kampanjebannermodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="b0cb1-150">Legg til en eller flere bannermeldinger i innstillingene for bannermodulen.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="b0cb1-151">Hver melding kan inneholde tekst sammen med en kobling.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-151">Each message can have text together with a link.</span></span> <span data-ttu-id="b0cb1-152">Du kan redigere de andre egenskapene hvis du vil tilpasse modulen ytterligere.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="b0cb1-153">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-153">Save and preview the page.</span></span> <span data-ttu-id="b0cb1-154">Øverst på siden vil du se et varsel som angir teksten du la til.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="b0cb1-155">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="b0cb1-156">Et kampanjebanner brukes vanligvis i sporet for sideoverskrift eller et spor for underoverskrift.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b0cb1-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b0cb1-157">Additional resources</span></span>

[<span data-ttu-id="b0cb1-158">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="b0cb1-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b0cb1-159">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="b0cb1-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b0cb1-160">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b0cb1-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b0cb1-161">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="b0cb1-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="b0cb1-162">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="b0cb1-162">Video player module</span></span>](add-video-player.md)
