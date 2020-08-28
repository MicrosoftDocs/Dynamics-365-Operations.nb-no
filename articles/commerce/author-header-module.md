---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686628"
---
# <a name="header-module"></a><span data-ttu-id="e6ff0-103">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6ff0-104">Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e6ff0-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e6ff0-105">Overview</span></span>

<span data-ttu-id="e6ff0-106">I Dynamics 365 Commerce omfatter en sideoverskrift flere moduler, for eksempel modul for topptekst, navigasjonsmeny, søk, kampanjebanner og samtykke til informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="e6ff0-107">Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, et kurvsymbol, et ønskelistesymbol, påloggingsalternativer og søkefelt.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="e6ff0-108">En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet).</span><span class="sxs-lookup"><span data-stu-id="e6ff0-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="e6ff0-109">På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).</span><span class="sxs-lookup"><span data-stu-id="e6ff0-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="e6ff0-110">Bildet nedenfor viser et eksempel på en topptekstmodul på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-110">The following image shows an example of a header module on a home page.</span></span>

![Eksempel på en topptekstmodul](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="e6ff0-112">Egenskaper for en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-112">Properties of a header module</span></span>

<span data-ttu-id="e6ff0-113">En topptekstmodul støtter **Logobilde**, **Logokobling** og egenskaper for **Min konto-koblinger**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="e6ff0-114">**Logobilde**- og **Logokobling**-egenskapene brukes til å definere en logo på siden.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="e6ff0-115">Hvis du vil ha mer informasjon, kan du se [Legge til en logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="e6ff0-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="e6ff0-116">Egenskapen **Min konto-koblinger** kan brukes til å definere kontosider som områdeeieren ønsker å vise hurtigkoblinger for i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="e6ff0-117">Moduler som er tilgjengelige i en overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-117">Modules that are available in a header module</span></span>

<span data-ttu-id="e6ff0-118">Følgende moduler kan brukes i en topptekstmodul:</span><span class="sxs-lookup"><span data-stu-id="e6ff0-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="e6ff0-119">**Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="e6ff0-120">Kanalnavigeringshierarkiet kan konfigureres i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e6ff0-121">Navigasjonsmenyen har egenskapen **Navigasjonskilde** som brukes til å angi navigasjonsmenyelementer og statiske menyelementer for Retail Server som en kilde.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="e6ff0-122">Hvis statiske menyelementer angis som en kilde, kan relative koblinger til andre sider på området angis.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="e6ff0-123">Konfigurerte varer vises deretter som topptekstnavigasjon.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="e6ff0-124">**Søk** – Med søkemodulen kan brukere angi søkeord for å søke etter produkter.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="e6ff0-125">URL-adressen til standard søkeside og parameterne for søkespørringen må angis under **Områdeinnstillinger \> Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="e6ff0-126">Søkemodulen har egenskaper som lar deg skjule søkeknappen eller etiketten etter behov.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="e6ff0-127">Søkemodulen støtter også alternativer for automatiske forslag, for eksempel søkeresultater for produkt, nøkkelord og kategori.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="e6ff0-128">**Handlekurvikon** – Handlekurvikonmodulen representerer handlekurvikonet, som viser antall varer i handlekurven på et gitt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="e6ff0-129">Hvis du vil ha mer informasjon, se [Handlekurvikonmodulen](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="e6ff0-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="e6ff0-130">Opprette en topptekstmodul for en side</span><span class="sxs-lookup"><span data-stu-id="e6ff0-130">Create a header module for a page</span></span>

<span data-ttu-id="e6ff0-131">Hvis du vil opprette en topptekstmodul, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="e6ff0-132">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="e6ff0-133">I dialogboksen **Nytt sidefragment** velger du **Beholder**-modulen, skriver inn et navn på sidefragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-134">Velg **Standardbeholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll beholder**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e6ff0-135">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6ff0-136">I dialogboksen **Legg til modul** velger du modulene **Kampanjebanner** og **Samtykke til informasjonskapsler**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-137">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6ff0-138">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-139">Velg **Beholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll beholder**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e6ff0-140">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6ff0-141">I dialogboksen **Legg til modul** velger du **Topptekst**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-142">I **Navigasjonsmeny**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6ff0-143">I dialogboksen **Legg til modul** velger du **Navigasjonsmeny**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-144">Konfigurer egenskapene for navigasjonsmeny-modulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="e6ff0-145">I **Søk**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6ff0-146">I dialogboksen **Legg til modul** velger du **Søk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-147">Konfigurer egenskapene for søkemodulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="e6ff0-148">I **Handlevogn**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6ff0-149">I dialogboksen **Legg til modul** velger du **Handlevognikon**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e6ff0-150">Konfigurer egenskapene for handlevognikon-modulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="e6ff0-151">Hvis du vil at handlekurvikonet skal vise et sammendrag av handlekurven (også kjent som en minikurv) når brukerne holder pekeren over den, velger du **Vis minikurv**.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="e6ff0-152">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="e6ff0-153">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="e6ff0-154">I **Topptekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="e6ff0-155">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="e6ff0-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6ff0-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e6ff0-156">Additional resources</span></span>

[<span data-ttu-id="e6ff0-157">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="e6ff0-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e6ff0-158">Containermodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e6ff0-159">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e6ff0-160">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e6ff0-161">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e6ff0-162">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e6ff0-163">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e6ff0-164">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e6ff0-165">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="e6ff0-165">Footer module</span></span>](author-footer-module.md)
