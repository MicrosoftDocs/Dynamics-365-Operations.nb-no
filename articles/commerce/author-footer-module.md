---
title: Bunntekstmodul
description: Dette emnet dekker bunntekstmoduler og hvordan du redigerer dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269642"
---
# <a name="footer-module"></a><span data-ttu-id="ec336-103">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="ec336-104">Dette emnet dekker bunntekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ec336-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ec336-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ec336-105">Overview</span></span>

<span data-ttu-id="ec336-106">Bunntekstmodulen er en spesialcontainer som brukes til å være vert for modulene som vises i bunnteksten på siden.</span><span class="sxs-lookup"><span data-stu-id="ec336-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="ec336-107">Den kan for eksempel inneholde koblinger til ulike sider på området, for eksempel sider for **Kontakt oss** og **Butikkpolicyer**.</span><span class="sxs-lookup"><span data-stu-id="ec336-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="ec336-108">Egenskaper for bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-108">Footer module properties</span></span> 

<span data-ttu-id="ec336-109">I likhet med de fleste containere støtter en bunntekstmodul egenskaper for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="ec336-109">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="ec336-110">Den støtter også tillegging av flere bunntekstkategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="ec336-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="ec336-111">Hver bunntekstkategorimodul som legges til, gjengis som en kolonne i bunntekstmodulen.</span><span class="sxs-lookup"><span data-stu-id="ec336-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="ec336-112">Moduler som er tilgjengelige i en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-112">Modules available in a footer module</span></span>

<span data-ttu-id="ec336-113">**Bunntekstelementer** – En modul for bunntekstelementer kan inneholde en overskrift, et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="ec336-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="ec336-114">Overskriften kan enten brukes alene eller sammen med et bilde og en kobling.</span><span class="sxs-lookup"><span data-stu-id="ec336-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="ec336-115">Hver kobling i bunnteksten kan konfigureres slik at den har bare tekst (for eksempel "Kontakt oss"- og "Personvern"-koblinger), eller slik at den har både tekst og et bilde (for eksempel koblinger til sosiale medier).</span><span class="sxs-lookup"><span data-stu-id="ec336-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="ec336-116">**Til toppen** – En Til toppen-modul gir en kobling for rask navigering til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="ec336-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="ec336-117">Et mål kreves.</span><span class="sxs-lookup"><span data-stu-id="ec336-117">A destination is required.</span></span> <span data-ttu-id="ec336-118">Standard målverdi er #, som tar brukeren til toppen av siden.</span><span class="sxs-lookup"><span data-stu-id="ec336-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="ec336-119">Forfatte en bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-119">Author a footer module</span></span>

1. <span data-ttu-id="ec336-120">I navigasjonsruten velger du **Fragmenter**, og deretter velger du **Nytt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="ec336-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ec336-121">I dialogboksen **Nytt sidefragment** velger du bunntekstmodulen, skriver inn et navn på sidefragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec336-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ec336-122">I disposisjonstreet til venstre velger du ellipseknappen (**...**) for bunntekstmodulen, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ec336-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ec336-123">I dialogboksen **Legg til modul** velger du bunntekstkategorimodulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec336-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="ec336-124">I disposisjonstreet velger du ellipseknappen for bunntekstkategorien, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ec336-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ec336-125">I dialogboksen **Legg til modul** velger du bunntekstelementmodulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec336-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="ec336-126">I disposisjonstreet velger du bunntekstelementmodulen.</span><span class="sxs-lookup"><span data-stu-id="ec336-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="ec336-127">Deretter, i egenskapsruten til høyre, konfigurerer du overskriften, koblingen, koblingsteksten og bildet etter behov.</span><span class="sxs-lookup"><span data-stu-id="ec336-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="ec336-128">Gjenta trinn 5 til og med 7 for å legge til flere bunntekstelementer.</span><span class="sxs-lookup"><span data-stu-id="ec336-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="ec336-129">For å legge til "Til toppen"-kobling i bunnteksten velger du ellipseknappen for bunntekstkategorimodulen, og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ec336-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ec336-130">I dialogboksen **Legg til modul** velger du Til toppen-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec336-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="ec336-131">I disposisjonstreet velger du Til toppen-modulen.</span><span class="sxs-lookup"><span data-stu-id="ec336-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="ec336-132">I egenskapsruten til høyre konfigurerer du deretter Til toppen-modulen slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="ec336-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="ec336-133">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn sidefragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="ec336-133">Select **Save**, select **Finish editing** to check in the page fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="ec336-134">Følg denne fremgangsmåten for hver sidemal som er opprettet for området.</span><span class="sxs-lookup"><span data-stu-id="ec336-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="ec336-135">I **Hoved**-sporet på standardsiden, i bunntekstmodulen, legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="ec336-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="ec336-136">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="ec336-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="ec336-137">Ved å legge til sidefragmentet i sidemaler garanteres det at bunnteksten gjengis på hver side.</span><span class="sxs-lookup"><span data-stu-id="ec336-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec336-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ec336-138">Additional resources</span></span>

[<span data-ttu-id="ec336-139">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="ec336-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ec336-140">Containermodul</span><span class="sxs-lookup"><span data-stu-id="ec336-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ec336-141">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ec336-142">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ec336-143">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="ec336-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ec336-144">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ec336-145">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ec336-146">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="ec336-146">Footer module</span></span>](author-footer-module.md)
