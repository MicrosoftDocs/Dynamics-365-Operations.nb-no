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
ms.openlocfilehash: 16c9ca145aff97f0af242da4cf662367f1f4ca3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211454"
---
# <a name="footer-module"></a><span data-ttu-id="f3711-103">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3711-104">Dette emnet dekker bunntekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3711-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f3711-105">Bunntekstmodulen er en spesialcontainer som brukes til å være vert for modulene som vises i bunnteksten på siden.</span><span class="sxs-lookup"><span data-stu-id="f3711-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="f3711-106">Den kan for eksempel inneholde koblinger til ulike sider på området, for eksempel sider for **Kontakt oss** og **Butikkpolicyer**.</span><span class="sxs-lookup"><span data-stu-id="f3711-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="f3711-107">Bildet nedenfor viser et eksempel på en bunntekstmodul på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="f3711-107">The following image shows an example of a footer module on a site page.</span></span>

![Eksempel på en bunntekstmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="f3711-109">Egenskaper for bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-109">Footer module properties</span></span> 

<span data-ttu-id="f3711-110">I likhet med de fleste containere støtter en bunntekstmodul egenskaper for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="f3711-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="f3711-111">Den støtter også tillegging av flere bunntekstkategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="f3711-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="f3711-112">Hver bunntekstkategorimodul som legges til, gjengis som en kolonne i bunntekstmodulen.</span><span class="sxs-lookup"><span data-stu-id="f3711-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="f3711-113">Moduler som er tilgjengelige i en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-113">Modules available in a footer module</span></span>

<span data-ttu-id="f3711-114">**Bunntekstelementer** – En modul for bunntekstelementer kan inneholde en overskrift, et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="f3711-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="f3711-115">Overskriften kan enten brukes alene eller sammen med et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="f3711-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="f3711-116">Hver kobling i bunnteksten kan konfigureres slik at den har bare tekst (for eksempel "Kontakt oss"- og "Personvern"-koblinger), eller slik at den har både tekst og et bilde (for eksempel koblinger til sosiale medier).</span><span class="sxs-lookup"><span data-stu-id="f3711-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="f3711-117">**Til toppen** – En Til toppen-modul gir en kobling for rask navigering til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="f3711-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="f3711-118">Et mål kreves.</span><span class="sxs-lookup"><span data-stu-id="f3711-118">A destination is required.</span></span> <span data-ttu-id="f3711-119">Standard målverdi er \#, som fører brukeren til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="f3711-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="f3711-120">Opprette en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-120">Create a footer module</span></span>

1. <span data-ttu-id="f3711-121">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="f3711-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f3711-122">I dialogboksen **Nytt fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3711-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f3711-123">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f3711-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f3711-124">I dialogboksen **Legg til modul** velger du **Bunntekstkategori**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3711-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f3711-125">I **Bunntekstkategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f3711-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f3711-126">I dialogboksen **Legg til modul** velger du **Bunntekstelement**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3711-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f3711-127">Velg **Bunntekstelement**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du overskriften, koblingen, koblingsteksten og bildet etter behov.</span><span class="sxs-lookup"><span data-stu-id="f3711-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="f3711-128">Gjenta trinn 5 til og med 7 for hvert element for å legge til flere bunntekstelementer.</span><span class="sxs-lookup"><span data-stu-id="f3711-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="f3711-129">For å legge til "Til toppen"-kobling i bunnteksten velger du ellipsen (**…**) i **Bunntekstkategori**-sporet, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f3711-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f3711-130">I dialogboksen **Legg til modul** velger du **Til toppen**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3711-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f3711-131">Velg **Til toppen**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du teksten og andre modulegenskaper etter behov.</span><span class="sxs-lookup"><span data-stu-id="f3711-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="f3711-132">Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="f3711-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f3711-133">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="f3711-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f3711-134">I **Bunntekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="f3711-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f3711-135">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="f3711-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f3711-136">Ved å legge til fragmentet i sidemaler garanteres det at bunnteksten gjengis på hver side.</span><span class="sxs-lookup"><span data-stu-id="f3711-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3711-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f3711-137">Additional resources</span></span>

[<span data-ttu-id="f3711-138">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="f3711-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f3711-139">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="f3711-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f3711-140">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f3711-141">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f3711-142">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="f3711-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f3711-143">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f3711-144">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f3711-145">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f3711-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]