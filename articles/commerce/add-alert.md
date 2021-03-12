---
title: Kampanjebannermodul
description: Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a77196be69bb71d917bf84c633199a3af3fbf478
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986035"
---
# <a name="promo-banner-module"></a><span data-ttu-id="64e5a-103">Kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="64e5a-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64e5a-104">Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="64e5a-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="64e5a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="64e5a-105">Overview</span></span>

<span data-ttu-id="64e5a-106">Kampanjebannermoduler brukes til å vise meldinger med innebygd informasjon på en side.</span><span class="sxs-lookup"><span data-stu-id="64e5a-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="64e5a-107">De kan brukes til å vise kampanjer på hele området som vises på alle sider av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="64e5a-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="64e5a-108">Kampanjebannermoduler støtter en tekstmelding og en kobling.</span><span class="sxs-lookup"><span data-stu-id="64e5a-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="64e5a-109">Hvis det legges til flere meldinger i en kampanjebannermodul, blir den en roterende karusellbanner som lar kundene gå gjennom alle meldingene.</span><span class="sxs-lookup"><span data-stu-id="64e5a-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="64e5a-110">Kampanjebannermoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="64e5a-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="64e5a-111">Eksempler på bruk av kampanjebannere i e-handel</span><span class="sxs-lookup"><span data-stu-id="64e5a-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="64e5a-112">Kampanjebannere kan brukes i områdehodet til å vise kampanjer eller meldinger på hele området, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="64e5a-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="64e5a-113">"Årlige salg avsluttes om 10 dager"</span><span class="sxs-lookup"><span data-stu-id="64e5a-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="64e5a-114">"Gjør store besparelse på skolestartsalget.</span><span class="sxs-lookup"><span data-stu-id="64e5a-114">"Save big with back to school sale.</span></span> <span data-ttu-id="64e5a-115">Handle nå. "</span><span class="sxs-lookup"><span data-stu-id="64e5a-115">Shop Now."</span></span>

<span data-ttu-id="64e5a-116">"Nyttårssalget er her!"</span><span class="sxs-lookup"><span data-stu-id="64e5a-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="64e5a-117">Bildet nedenfor viser et eksempel på en kampanjebanner.</span><span class="sxs-lookup"><span data-stu-id="64e5a-117">The following image shows an example of a promo banner.</span></span>

![Eksempel på en kampanjebannermodul](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="64e5a-119">Egenskaper for kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="64e5a-119">Promo banner module properties</span></span>

| <span data-ttu-id="64e5a-120">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="64e5a-120">Property name</span></span>             | <span data-ttu-id="64e5a-121">Verdi</span><span class="sxs-lookup"><span data-stu-id="64e5a-121">Value</span></span>                              | <span data-ttu-id="64e5a-122">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="64e5a-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="64e5a-123">Bannermeldinger</span><span class="sxs-lookup"><span data-stu-id="64e5a-123">Banner messages</span></span>           | <span data-ttu-id="64e5a-124">Tekst og koblinger</span><span class="sxs-lookup"><span data-stu-id="64e5a-124">Text and links</span></span>                     | <span data-ttu-id="64e5a-125">En matrise med tekst og koblinger.</span><span class="sxs-lookup"><span data-stu-id="64e5a-125">An array of text and links.</span></span> |
| <span data-ttu-id="64e5a-126">Automatisk avspilling</span><span class="sxs-lookup"><span data-stu-id="64e5a-126">Autoplay</span></span>                  | <span data-ttu-id="64e5a-127">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="64e5a-127">**True** or **False**</span></span>              | <span data-ttu-id="64e5a-128">En verdi som angir om meldinger gås gjennom automatisk hvis flere meldinger er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="64e5a-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="64e5a-129">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="64e5a-129">Slide transition interval</span></span> | <span data-ttu-id="64e5a-130">Et tall i millisekunder (ms)</span><span class="sxs-lookup"><span data-stu-id="64e5a-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="64e5a-131">Intervallet som brukes til å bla gjennom meldinger.</span><span class="sxs-lookup"><span data-stu-id="64e5a-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="64e5a-132">Tillat forkastelse</span><span class="sxs-lookup"><span data-stu-id="64e5a-132">Allow dismiss</span></span>             | <span data-ttu-id="64e5a-133">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="64e5a-133">**True** or **False**</span></span>              | <span data-ttu-id="64e5a-134">Hvis verdien settes til **Sann**, kan kundene forkaste varselet.</span><span class="sxs-lookup"><span data-stu-id="64e5a-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="64e5a-135">Vis karusellflipper</span><span class="sxs-lookup"><span data-stu-id="64e5a-135">Show carousel flipper</span></span>     | <span data-ttu-id="64e5a-136">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="64e5a-136">**True** or **False**</span></span>              | <span data-ttu-id="64e5a-137">En verdi som angir om karusellflipperne skal vises, slik at kunder manuelt kan gå gjennom flere bannerelementer.</span><span class="sxs-lookup"><span data-stu-id="64e5a-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="64e5a-138">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="64e5a-138">Text alignment</span></span>            | <span data-ttu-id="64e5a-139">**Høyre**, **Venstre** eller **Midtstilt**</span><span class="sxs-lookup"><span data-stu-id="64e5a-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="64e5a-140">Tekstjusteringen i kampanjebannermodulen.</span><span class="sxs-lookup"><span data-stu-id="64e5a-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="64e5a-141">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="64e5a-141">Link</span></span>                      | <span data-ttu-id="64e5a-142">En URL</span><span class="sxs-lookup"><span data-stu-id="64e5a-142">A URL</span></span>                              | <span data-ttu-id="64e5a-143">URL-adresse for valgfri kobling.</span><span class="sxs-lookup"><span data-stu-id="64e5a-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="64e5a-144">Legge til en kampanjebannermodul på en side</span><span class="sxs-lookup"><span data-stu-id="64e5a-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="64e5a-145">Hvis du vil legge til en kampanjebannermodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="64e5a-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="64e5a-146">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="64e5a-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="64e5a-147">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Kampanjebannermal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="64e5a-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="64e5a-148">Under **Sideoppsett** legger du til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="64e5a-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="64e5a-149">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="64e5a-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="64e5a-150">Bruk malen du nettopp opprettet, for å opprette en side som heter **Kampanjebannerside**.</span><span class="sxs-lookup"><span data-stu-id="64e5a-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="64e5a-151">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="64e5a-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="64e5a-152">I ruten til høyre setter du **Bredde**-verdien til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="64e5a-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="64e5a-153">Under **Sideoppsett** legger du til en kampanjebannermodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="64e5a-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="64e5a-154">Legg til en eller flere bannermeldinger i innstillingene for bannermodulen.</span><span class="sxs-lookup"><span data-stu-id="64e5a-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="64e5a-155">Hver melding kan inneholde tekst sammen med en kobling.</span><span class="sxs-lookup"><span data-stu-id="64e5a-155">Each message can have text together with a link.</span></span> <span data-ttu-id="64e5a-156">Du kan redigere de andre egenskapene hvis du vil tilpasse modulen ytterligere.</span><span class="sxs-lookup"><span data-stu-id="64e5a-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="64e5a-157">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="64e5a-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="64e5a-158">Øverst på siden vil du se et varsel som angir teksten du la til.</span><span class="sxs-lookup"><span data-stu-id="64e5a-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="64e5a-159">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="64e5a-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="64e5a-160">Et kampanjebanner brukes vanligvis i sporet for sideoverskrift eller et spor for underoverskrift.</span><span class="sxs-lookup"><span data-stu-id="64e5a-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="64e5a-161">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="64e5a-161">Additional resources</span></span>

[<span data-ttu-id="64e5a-162">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="64e5a-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="64e5a-163">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="64e5a-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="64e5a-164">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="64e5a-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="64e5a-165">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="64e5a-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="64e5a-166">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="64e5a-166">Video player module</span></span>](add-video-player.md)
