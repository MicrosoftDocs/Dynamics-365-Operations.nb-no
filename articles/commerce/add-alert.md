---
title: Kampanjebannermodul
description: Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796252"
---
# <a name="promo-banner-module"></a><span data-ttu-id="8d3db-103">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="8d3db-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d3db-104">Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d3db-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8d3db-105">Kampanjebannermoduler brukes til å vise meldinger med innebygd informasjon på en side.</span><span class="sxs-lookup"><span data-stu-id="8d3db-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="8d3db-106">De kan brukes til å vise kampanjer på hele området som vises på alle sider av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="8d3db-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="8d3db-107">Kampanjebannermoduler støtter en tekstmelding og en kobling.</span><span class="sxs-lookup"><span data-stu-id="8d3db-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="8d3db-108">Hvis det legges til flere meldinger i en kampanjebannermodul, blir den en roterende karusellbanner som lar kundene gå gjennom alle meldingene.</span><span class="sxs-lookup"><span data-stu-id="8d3db-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="8d3db-109">Kampanjebannermoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="8d3db-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="8d3db-110">Eksempler på bruk av kampanjebannere i e-handel</span><span class="sxs-lookup"><span data-stu-id="8d3db-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="8d3db-111">Kampanjebannere kan brukes i områdehodet til å vise kampanjer eller meldinger på hele området, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="8d3db-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="8d3db-112">"Årlige salg avsluttes om 10 dager"</span><span class="sxs-lookup"><span data-stu-id="8d3db-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="8d3db-113">"Gjør store besparelse på skolestartsalget.</span><span class="sxs-lookup"><span data-stu-id="8d3db-113">"Save big with back to school sale.</span></span> <span data-ttu-id="8d3db-114">Handle nå. "</span><span class="sxs-lookup"><span data-stu-id="8d3db-114">Shop Now."</span></span>

<span data-ttu-id="8d3db-115">"Nyttårssalget er her!"</span><span class="sxs-lookup"><span data-stu-id="8d3db-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="8d3db-116">Bildet nedenfor viser et eksempel på en kampanjebanner.</span><span class="sxs-lookup"><span data-stu-id="8d3db-116">The following image shows an example of a promo banner.</span></span>

![Eksempel på en kampanjebannermodul](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="8d3db-118">Egenskaper for kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="8d3db-118">Promo banner module properties</span></span>

| <span data-ttu-id="8d3db-119">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="8d3db-119">Property name</span></span>             | <span data-ttu-id="8d3db-120">Verdi</span><span class="sxs-lookup"><span data-stu-id="8d3db-120">Value</span></span>                              | <span data-ttu-id="8d3db-121">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8d3db-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="8d3db-122">Bannermeldinger</span><span class="sxs-lookup"><span data-stu-id="8d3db-122">Banner messages</span></span>           | <span data-ttu-id="8d3db-123">Tekst og koblinger</span><span class="sxs-lookup"><span data-stu-id="8d3db-123">Text and links</span></span>                     | <span data-ttu-id="8d3db-124">En matrise med tekst og koblinger.</span><span class="sxs-lookup"><span data-stu-id="8d3db-124">An array of text and links.</span></span> |
| <span data-ttu-id="8d3db-125">Automatisk avspilling</span><span class="sxs-lookup"><span data-stu-id="8d3db-125">Autoplay</span></span>                  | <span data-ttu-id="8d3db-126">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="8d3db-126">**True** or **False**</span></span>              | <span data-ttu-id="8d3db-127">En verdi som angir om meldinger gås gjennom automatisk hvis flere meldinger er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="8d3db-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="8d3db-128">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="8d3db-128">Slide transition interval</span></span> | <span data-ttu-id="8d3db-129">Et tall i millisekunder (ms)</span><span class="sxs-lookup"><span data-stu-id="8d3db-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="8d3db-130">Intervallet som brukes til å bla gjennom meldinger.</span><span class="sxs-lookup"><span data-stu-id="8d3db-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="8d3db-131">Tillat forkastelse</span><span class="sxs-lookup"><span data-stu-id="8d3db-131">Allow dismiss</span></span>             | <span data-ttu-id="8d3db-132">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="8d3db-132">**True** or **False**</span></span>              | <span data-ttu-id="8d3db-133">Hvis verdien settes til **Sann**, kan kundene forkaste varselet.</span><span class="sxs-lookup"><span data-stu-id="8d3db-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="8d3db-134">Vis karusellflipper</span><span class="sxs-lookup"><span data-stu-id="8d3db-134">Show carousel flipper</span></span>     | <span data-ttu-id="8d3db-135">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="8d3db-135">**True** or **False**</span></span>              | <span data-ttu-id="8d3db-136">En verdi som angir om karusellflipperne skal vises, slik at kunder manuelt kan gå gjennom flere bannerelementer.</span><span class="sxs-lookup"><span data-stu-id="8d3db-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="8d3db-137">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="8d3db-137">Text alignment</span></span>            | <span data-ttu-id="8d3db-138">**Høyre**, **Venstre** eller **Midtstilt**</span><span class="sxs-lookup"><span data-stu-id="8d3db-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="8d3db-139">Tekstjusteringen i kampanjebannermodulen.</span><span class="sxs-lookup"><span data-stu-id="8d3db-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="8d3db-140">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="8d3db-140">Link</span></span>                      | <span data-ttu-id="8d3db-141">En URL</span><span class="sxs-lookup"><span data-stu-id="8d3db-141">A URL</span></span>                              | <span data-ttu-id="8d3db-142">URL-adresse for valgfri kobling.</span><span class="sxs-lookup"><span data-stu-id="8d3db-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="8d3db-143">Legge til en kampanjebannermodul på en side</span><span class="sxs-lookup"><span data-stu-id="8d3db-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="8d3db-144">Hvis du vil legge til en kampanjebannermodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8d3db-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8d3db-145">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="8d3db-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="8d3db-146">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Kampanjebannermal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d3db-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="8d3db-147">Under **Sideoppsett** legger du til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="8d3db-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="8d3db-148">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="8d3db-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="8d3db-149">Bruk malen du nettopp opprettet, for å opprette en side som heter **Kampanjebannerside**.</span><span class="sxs-lookup"><span data-stu-id="8d3db-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="8d3db-150">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="8d3db-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="8d3db-151">I ruten til høyre setter du **Bredde**-verdien til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="8d3db-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="8d3db-152">Under **Sideoppsett** legger du til en kampanjebannermodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="8d3db-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="8d3db-153">Legg til en eller flere bannermeldinger i innstillingene for bannermodulen.</span><span class="sxs-lookup"><span data-stu-id="8d3db-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="8d3db-154">Hver melding kan inneholde tekst sammen med en kobling.</span><span class="sxs-lookup"><span data-stu-id="8d3db-154">Each message can have text together with a link.</span></span> <span data-ttu-id="8d3db-155">Du kan redigere de andre egenskapene hvis du vil tilpasse modulen ytterligere.</span><span class="sxs-lookup"><span data-stu-id="8d3db-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="8d3db-156">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="8d3db-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="8d3db-157">Øverst på siden vil du se et varsel som angir teksten du la til.</span><span class="sxs-lookup"><span data-stu-id="8d3db-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="8d3db-158">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="8d3db-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="8d3db-159">Et kampanjebanner brukes vanligvis i sporet for sideoverskrift eller et spor for underoverskrift.</span><span class="sxs-lookup"><span data-stu-id="8d3db-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8d3db-160">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d3db-160">Additional resources</span></span>

[<span data-ttu-id="8d3db-161">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="8d3db-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8d3db-162">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="8d3db-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8d3db-163">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="8d3db-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="8d3db-164">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="8d3db-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="8d3db-165">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="8d3db-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]