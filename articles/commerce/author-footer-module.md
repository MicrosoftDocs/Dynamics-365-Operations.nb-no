---
title: Bunntekstmodul
description: Dette emnet dekker bunntekstmoduler og hvordan du redigerer dem i Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979953"
---
# <a name="footer-module"></a><span data-ttu-id="bde99-103">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="bde99-104">Dette emnet dekker bunntekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bde99-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bde99-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="bde99-105">Overview</span></span>

<span data-ttu-id="bde99-106">Bunntekstmodulen er en spesialcontainer som brukes til å være vert for modulene som vises i bunnteksten på siden.</span><span class="sxs-lookup"><span data-stu-id="bde99-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="bde99-107">Den kan for eksempel inneholde koblinger til ulike sider på området, for eksempel sider for **Kontakt oss** og **Butikkpolicyer**.</span><span class="sxs-lookup"><span data-stu-id="bde99-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="bde99-108">Bildet nedenfor viser et eksempel på en bunntekstmodul på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="bde99-108">The following image shows an example of a footer module on a site page.</span></span>

![Eksempel på en bunntekstmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="bde99-110">Egenskaper for bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-110">Footer module properties</span></span> 

<span data-ttu-id="bde99-111">I likhet med de fleste containere støtter en bunntekstmodul egenskaper for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="bde99-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="bde99-112">Den støtter også tillegging av flere bunntekstkategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="bde99-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="bde99-113">Hver bunntekstkategorimodul som legges til, gjengis som en kolonne i bunntekstmodulen.</span><span class="sxs-lookup"><span data-stu-id="bde99-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="bde99-114">Moduler som er tilgjengelige i en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-114">Modules available in a footer module</span></span>

<span data-ttu-id="bde99-115">**Bunntekstelementer** – En modul for bunntekstelementer kan inneholde en overskrift, et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="bde99-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="bde99-116">Overskriften kan enten brukes alene eller sammen med et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="bde99-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="bde99-117">Hver kobling i bunnteksten kan konfigureres slik at den har bare tekst (for eksempel "Kontakt oss"- og "Personvern"-koblinger), eller slik at den har både tekst og et bilde (for eksempel koblinger til sosiale medier).</span><span class="sxs-lookup"><span data-stu-id="bde99-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="bde99-118">**Til toppen** – En Til toppen-modul gir en kobling for rask navigering til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="bde99-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="bde99-119">Et mål kreves.</span><span class="sxs-lookup"><span data-stu-id="bde99-119">A destination is required.</span></span> <span data-ttu-id="bde99-120">Standard målverdi er \#, som fører brukeren til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="bde99-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="bde99-121">Opprette en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-121">Create a footer module</span></span>

1. <span data-ttu-id="bde99-122">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="bde99-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="bde99-123">I dialogboksen **Nytt fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="bde99-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="bde99-124">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="bde99-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bde99-125">I dialogboksen **Legg til modul** velger du **Bunntekstkategori**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="bde99-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bde99-126">I **Bunntekstkategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="bde99-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bde99-127">I dialogboksen **Legg til modul** velger du **Bunntekstelement**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="bde99-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bde99-128">Velg **Bunntekstelement**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du overskriften, koblingen, koblingsteksten og bildet etter behov.</span><span class="sxs-lookup"><span data-stu-id="bde99-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="bde99-129">Gjenta trinn 5 til og med 7 for hvert element for å legge til flere bunntekstelementer.</span><span class="sxs-lookup"><span data-stu-id="bde99-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="bde99-130">For å legge til "Til toppen"-kobling i bunnteksten velger du ellipsen (**…**) i **Bunntekstkategori**-sporet, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="bde99-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="bde99-131">I dialogboksen **Legg til modul** velger du **Til toppen**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="bde99-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bde99-132">Velg **Til toppen**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du teksten og andre modulegenskaper etter behov.</span><span class="sxs-lookup"><span data-stu-id="bde99-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="bde99-133">Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="bde99-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bde99-134">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="bde99-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="bde99-135">I **Bunntekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="bde99-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="bde99-136">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="bde99-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bde99-137">Ved å legge til fragmentet i sidemaler garanteres det at bunnteksten gjengis på hver side.</span><span class="sxs-lookup"><span data-stu-id="bde99-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bde99-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bde99-138">Additional resources</span></span>

[<span data-ttu-id="bde99-139">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="bde99-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bde99-140">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="bde99-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bde99-141">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bde99-142">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bde99-143">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="bde99-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bde99-144">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bde99-145">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bde99-146">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="bde99-146">Footer module</span></span>](author-footer-module.md)
