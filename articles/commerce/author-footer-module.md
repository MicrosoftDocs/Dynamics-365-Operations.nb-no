---
title: Bunntekstmodul
description: Dette emnet dekker bunntekstmoduler og hvordan du redigerer dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411219"
---
# <a name="footer-module"></a><span data-ttu-id="f2f21-103">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2f21-104">Dette emnet dekker bunntekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2f21-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2f21-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f2f21-105">Overview</span></span>

<span data-ttu-id="f2f21-106">Bunntekstmodulen er en spesialcontainer som brukes til å være vert for modulene som vises i bunnteksten på siden.</span><span class="sxs-lookup"><span data-stu-id="f2f21-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="f2f21-107">Den kan for eksempel inneholde koblinger til ulike sider på området, for eksempel sider for **Kontakt oss** og **Butikkpolicyer**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="f2f21-108">Bildet nedenfor viser et eksempel på en bunntekstmodul på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="f2f21-108">The following image shows an example of a footer module on a site page.</span></span>

![Eksempel på en bunntekstmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="f2f21-110">Egenskaper for bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-110">Footer module properties</span></span> 

<span data-ttu-id="f2f21-111">I likhet med de fleste containere støtter en bunntekstmodul egenskaper for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="f2f21-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="f2f21-112">Den støtter også tillegging av flere bunntekstkategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="f2f21-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="f2f21-113">Hver bunntekstkategorimodul som legges til, gjengis som en kolonne i bunntekstmodulen.</span><span class="sxs-lookup"><span data-stu-id="f2f21-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="f2f21-114">Moduler som er tilgjengelige i en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-114">Modules available in a footer module</span></span>

<span data-ttu-id="f2f21-115">**Bunntekstelementer** – En modul for bunntekstelementer kan inneholde en overskrift, et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="f2f21-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="f2f21-116">Overskriften kan enten brukes alene eller sammen med et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="f2f21-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="f2f21-117">Hver kobling i bunnteksten kan konfigureres slik at den har bare tekst (for eksempel "Kontakt oss"- og "Personvern"-koblinger), eller slik at den har både tekst og et bilde (for eksempel koblinger til sosiale medier).</span><span class="sxs-lookup"><span data-stu-id="f2f21-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="f2f21-118">**Til toppen** – En Til toppen-modul gir en kobling for rask navigering til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="f2f21-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="f2f21-119">Et mål kreves.</span><span class="sxs-lookup"><span data-stu-id="f2f21-119">A destination is required.</span></span> <span data-ttu-id="f2f21-120">Standard målverdi er \#, som fører brukeren til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="f2f21-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="f2f21-121">Opprette en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-121">Create a footer module</span></span>

1. <span data-ttu-id="f2f21-122">Gå til **Sidefragmenter**, og velg **Ny** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="f2f21-122">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f2f21-123">I dialogboksen **Nytt sidefragment** velger du **Beholder**-modulen, skriver inn et navn på sidefragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-123">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f2f21-124">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2f21-125">I dialogboksen **Legg til modul** velger du **Bunntekstkategori**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2f21-126">I **Bunntekstkategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2f21-127">I dialogboksen **Legg til modul** velger du **Bunntekstelement**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2f21-128">Velg **Bunntekstelement**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du overskriften, koblingen, koblingsteksten og bildet etter behov.</span><span class="sxs-lookup"><span data-stu-id="f2f21-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="f2f21-129">Gjenta trinn 5 til og med 7 for hvert element for å legge til flere bunntekstelementer.</span><span class="sxs-lookup"><span data-stu-id="f2f21-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="f2f21-130">For å legge til "Til toppen"-kobling i bunnteksten velger du ellipsen (**…**) i **Bunntekstkategori**-sporet, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2f21-131">I dialogboksen **Legg til modul** velger du **Til toppen**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2f21-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2f21-132">Velg **Til toppen**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du teksten og andre modulegenskaper etter behov.</span><span class="sxs-lookup"><span data-stu-id="f2f21-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="f2f21-133">Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="f2f21-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f2f21-134">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="f2f21-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f2f21-135">I **Bunntekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="f2f21-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f2f21-136">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="f2f21-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f2f21-137">Ved å legge til sidefragmentet i sidemaler garanteres det at bunnteksten gjengis på hver side.</span><span class="sxs-lookup"><span data-stu-id="f2f21-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2f21-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f2f21-138">Additional resources</span></span>

[<span data-ttu-id="f2f21-139">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="f2f21-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f2f21-140">Containermodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f2f21-141">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f2f21-142">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f2f21-143">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f2f21-144">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f2f21-145">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f2f21-146">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2f21-146">Footer module</span></span>](author-footer-module.md)
