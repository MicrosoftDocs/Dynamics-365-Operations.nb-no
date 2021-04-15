---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b14178431b281daa827749781dd16481f8bfb74
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799923"
---
# <a name="header-module"></a><span data-ttu-id="858ce-103">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="858ce-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="858ce-104">Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="858ce-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="858ce-105">I Dynamics 365 Commerce vises et topptekstområde som et sidefragment som inkluderer topptekst, promobanner og samtykkingsmoduler for informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="858ce-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="858ce-106">Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, en handlekurvikonmodul, et ønskelistesymbol, påloggingsalternativer og søkefelt.</span><span class="sxs-lookup"><span data-stu-id="858ce-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="858ce-107">En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet).</span><span class="sxs-lookup"><span data-stu-id="858ce-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="858ce-108">På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).</span><span class="sxs-lookup"><span data-stu-id="858ce-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="858ce-109">Bildet nedenfor viser et eksempel på en topptekstmodul på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="858ce-109">The following image shows an example of a header module on a home page.</span></span>

![Eksempel på en topptekstmodul](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="858ce-111">Egenskaper for en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="858ce-111">Properties of a header module</span></span>

<span data-ttu-id="858ce-112">En topptekstmodul støtter **Logobilde**, **Logokobling** og egenskaper for **Min konto-koblinger**.</span><span class="sxs-lookup"><span data-stu-id="858ce-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="858ce-113">**Logobilde**- og **Logokobling**-egenskapene brukes til å definere en logo på siden.</span><span class="sxs-lookup"><span data-stu-id="858ce-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="858ce-114">Hvis du vil ha mer informasjon, kan du se [Legge til en logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="858ce-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="858ce-115">Egenskapen **Min konto-koblinger** kan brukes til å definere kontosider som områdeeieren ønsker å vise hurtigkoblinger for i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="858ce-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="858ce-116">Moduler som er tilgjengelige i en overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="858ce-116">Modules that are available within a header module</span></span>

<span data-ttu-id="858ce-117">Følgende moduler kan brukes i en topptekstmodul:</span><span class="sxs-lookup"><span data-stu-id="858ce-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="858ce-118">**Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger.</span><span class="sxs-lookup"><span data-stu-id="858ce-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="858ce-119">Hvis du vil ha mer informasjon, kan du se [Navigasjonsmenymodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="858ce-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="858ce-120">**Søk** – Med søkemodulen kan brukere angi søkeord for å søke etter produkter.</span><span class="sxs-lookup"><span data-stu-id="858ce-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="858ce-121">URL-adressen til standard søkeside og parameterne for søkespørringen må angis under **Områdeinnstillinger \> Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="858ce-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="858ce-122">Søkemodulen har egenskaper som lar deg skjule søkeknappen eller etiketten etter behov.</span><span class="sxs-lookup"><span data-stu-id="858ce-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="858ce-123">Søkemodulen støtter også alternativer for automatiske forslag, for eksempel søkeresultater for produkt, nøkkelord og kategori.</span><span class="sxs-lookup"><span data-stu-id="858ce-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="858ce-124">**Handlekurvikon** – Handlekurvikonmodulen representerer handlekurvikonet, som viser antall varer i handlekurven på et gitt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="858ce-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="858ce-125">Hvis du vil ha mer informasjon, se [Handlekurvikonmodulen](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="858ce-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="858ce-126">**Områdevelger** - Områdevelgermodulen lar brukere bla gjennom forskjellige forhåndsdefinerte områder, basert på marked, regioner og nasjonale innstillinger.</span><span class="sxs-lookup"><span data-stu-id="858ce-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="858ce-127">Hvis du vil ha mer informasjon, se [Områdevelgermodul](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="858ce-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="858ce-128">**Butikkvelger** - Butikkvelgermodulen kan tas med i en hodemoduls butikkvelgerspor.</span><span class="sxs-lookup"><span data-stu-id="858ce-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="858ce-129">Det gjør det mulig for brukere å søke etter og finne nærliggende butikker.</span><span class="sxs-lookup"><span data-stu-id="858ce-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="858ce-130">Brukere kan også angi en foretrukket butikk.</span><span class="sxs-lookup"><span data-stu-id="858ce-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="858ce-131">Denne butikken vil deretter bli vist i hodet.</span><span class="sxs-lookup"><span data-stu-id="858ce-131">That store will then be shown in the header.</span></span> <span data-ttu-id="858ce-132">Når butikkvelgermodulen er inkludert i hodemodulen, må **Modus**-egenskapen angis til **Søk etter butikker**.</span><span class="sxs-lookup"><span data-stu-id="858ce-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="858ce-133">Hvis du vil ha mer informasjon, se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="858ce-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="858ce-134">Støtte for bruk av handlekurvikon-modulen i hodemoduler er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen.</span><span class="sxs-lookup"><span data-stu-id="858ce-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="858ce-135">Støtte for bruk av områdevelgermodulen i hodemoduler er tilgjengelig i Dynamics 365 Commerce 10.0.14-versjonen.</span><span class="sxs-lookup"><span data-stu-id="858ce-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="858ce-136">Støtte for bruk av butikkvelgermodulen i hodemoduler er tilgjengelig i Dynamics 365 Commerce 10.0.15-versjonen.</span><span class="sxs-lookup"><span data-stu-id="858ce-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="858ce-137">Opprette et topptekstfragment for en side</span><span class="sxs-lookup"><span data-stu-id="858ce-137">Create a header fragment for a page</span></span>

<span data-ttu-id="858ce-138">Hvis du vil opprette et topptekstfragment, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="858ce-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="858ce-139">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="858ce-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="858ce-140">I dialogboksen **Nytt fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="858ce-141">Velg **Standardbeholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll skjerm**.</span><span class="sxs-lookup"><span data-stu-id="858ce-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="858ce-142">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="858ce-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="858ce-143">I dialogboksen **Legg til modul** velger du modulene **Samtykke til informasjonskapsler**, **Topptekst** og **Promobanner**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="858ce-144">I ruten Egenskaper i modulen **Promobanner** velge rdu **Legg til melding**, og deretter velger du **Melding**.</span><span class="sxs-lookup"><span data-stu-id="858ce-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="858ce-145">I dialogboksen **Melding** legger du til tekst og koblinger for kampanjeinnholdet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="858ce-146">I ruten Egenskaper i modulen **Samtykke til informasjonskapsler** legger du til og konfigurerer tekst og en kobling til siden med nettstedspersonvern.</span><span class="sxs-lookup"><span data-stu-id="858ce-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="858ce-147">I **Navigasjonsmeny**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="858ce-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="858ce-148">I dialogboksen **Legg til modul** velger du **Navigasjonsmeny**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="858ce-149">I ruten Egenskape rfor navigasjonsmenymodulen velger du **Retail Server** under **Kilde til navigasjonsmeny**.</span><span class="sxs-lookup"><span data-stu-id="858ce-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="858ce-150">I ruten Egenskaper for navigasjonsmenymodulen velger du **Legg til menyelement** under **Statiske menyelementer**, og deretter velger du **Menyelement**.</span><span class="sxs-lookup"><span data-stu-id="858ce-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="858ce-151">I dialogboksen **Menyelement** skriver du inn "Kontakt" under **Menyelementtekst**.</span><span class="sxs-lookup"><span data-stu-id="858ce-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="858ce-152">I dialogboksen **Menyelement** velger du **Legg til en kobling** under **Koblingsmål for menyelement**.</span><span class="sxs-lookup"><span data-stu-id="858ce-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="858ce-153">I dialogboksen **Legg til en kobling** velger du URL-adressen for nettstedets Kontakt-side, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="858ce-154">Velg **OK** i dialogboksen **Menyelement**.</span><span class="sxs-lookup"><span data-stu-id="858ce-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="858ce-155">I **Søk**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="858ce-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="858ce-156">I dialogboksen **Legg til modul** velger du **Søk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="858ce-157">Konfigurer egenskapene for søkemodulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="858ce-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="858ce-158">I **Handlevogn**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="858ce-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="858ce-159">I dialogboksen **Legg til modul** velger du **Handlevognikon**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="858ce-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="858ce-160">Konfigurer egenskapene for handlevognikon-modulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="858ce-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="858ce-161">Hvis du vil at handlekurvikonet skal vise et sammendrag av handlekurven (også kjent som en minikurv) når brukerne holder pekeren over den, velger du **Vis minikurv**.</span><span class="sxs-lookup"><span data-stu-id="858ce-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="858ce-162">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="858ce-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="858ce-163">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="858ce-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="858ce-164">I **Topptekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="858ce-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="858ce-165">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="858ce-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="858ce-166">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="858ce-166">Additional resources</span></span>

[<span data-ttu-id="858ce-167">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="858ce-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="858ce-168">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="858ce-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="858ce-169">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="858ce-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="858ce-170">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="858ce-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="858ce-171">Navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="858ce-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="858ce-172">Informasjonskapselsamtykke</span><span class="sxs-lookup"><span data-stu-id="858ce-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="858ce-173">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="858ce-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="858ce-174">Områdevelgermodul</span><span class="sxs-lookup"><span data-stu-id="858ce-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="858ce-175">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="858ce-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]