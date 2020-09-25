---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761230"
---
# <a name="header-module"></a><span data-ttu-id="b1982-103">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="b1982-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b1982-104">Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1982-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1982-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b1982-105">Overview</span></span>

<span data-ttu-id="b1982-106">I Dynamics 365 Commerce vises et topptekstområde som et sidefragment som inkluderer topptekst, promobanner og samtykkingsmoduler for informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="b1982-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="b1982-107">Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, en handlekurvikonmodul, et ønskelistesymbol, påloggingsalternativer og søkefelt.</span><span class="sxs-lookup"><span data-stu-id="b1982-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="b1982-108">En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet).</span><span class="sxs-lookup"><span data-stu-id="b1982-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="b1982-109">På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).</span><span class="sxs-lookup"><span data-stu-id="b1982-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="b1982-110">Bildet nedenfor viser et eksempel på en topptekstmodul på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="b1982-110">The following image shows an example of a header module on a home page.</span></span>

![Eksempel på en topptekstmodul](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="b1982-112">Egenskaper for en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="b1982-112">Properties of a header module</span></span>

<span data-ttu-id="b1982-113">En topptekstmodul støtter **Logobilde**, **Logokobling** og egenskaper for **Min konto-koblinger**.</span><span class="sxs-lookup"><span data-stu-id="b1982-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="b1982-114">**Logobilde**- og **Logokobling**-egenskapene brukes til å definere en logo på siden.</span><span class="sxs-lookup"><span data-stu-id="b1982-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="b1982-115">Hvis du vil ha mer informasjon, kan du se [Legge til en logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="b1982-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="b1982-116">Egenskapen **Min konto-koblinger** kan brukes til å definere kontosider som områdeeieren ønsker å vise hurtigkoblinger for i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="b1982-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="b1982-117">Moduler som er tilgjengelige i en overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="b1982-117">Modules that are available within a header module</span></span>

<span data-ttu-id="b1982-118">Følgende moduler kan brukes i en topptekstmodul:</span><span class="sxs-lookup"><span data-stu-id="b1982-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="b1982-119">**Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger.</span><span class="sxs-lookup"><span data-stu-id="b1982-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="b1982-120">Hvis du vil ha mer informasjon, kan du se [Navigasjonsmenymodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="b1982-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="b1982-121">**Søk** – Med søkemodulen kan brukere angi søkeord for å søke etter produkter.</span><span class="sxs-lookup"><span data-stu-id="b1982-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="b1982-122">URL-adressen til standard søkeside og parameterne for søkespørringen må angis under **Områdeinnstillinger \> Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="b1982-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="b1982-123">Søkemodulen har egenskaper som lar deg skjule søkeknappen eller etiketten etter behov.</span><span class="sxs-lookup"><span data-stu-id="b1982-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="b1982-124">Søkemodulen støtter også alternativer for automatiske forslag, for eksempel søkeresultater for produkt, nøkkelord og kategori.</span><span class="sxs-lookup"><span data-stu-id="b1982-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="b1982-125">**Handlekurvikon** – Handlekurvikonmodulen representerer handlekurvikonet, som viser antall varer i handlekurven på et gitt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="b1982-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="b1982-126">Hvis du vil ha mer informasjon, se [Handlekurvikonmodulen](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="b1982-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="b1982-127">Opprette et topptekstfragment for en side</span><span class="sxs-lookup"><span data-stu-id="b1982-127">Create a header fragment for a page</span></span>

<span data-ttu-id="b1982-128">Hvis du vil opprette et topptekstfragment, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b1982-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="b1982-129">Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.</span><span class="sxs-lookup"><span data-stu-id="b1982-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b1982-130">I dialogboksen **Nytt fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b1982-131">Velg **Standardbeholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll skjerm**.</span><span class="sxs-lookup"><span data-stu-id="b1982-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="b1982-132">I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b1982-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1982-133">I dialogboksen **Legg til modul** velger du modulene **Samtykke til informasjonskapsler**, **Topptekst** og **Promobanner**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="b1982-134">I ruten Egenskaper i modulen **Promobanner** velge rdu **Legg til melding**, og deretter velger du **Melding**.</span><span class="sxs-lookup"><span data-stu-id="b1982-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="b1982-135">I dialogboksen **Melding** legger du til tekst og koblinger for kampanjeinnholdet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="b1982-136">I ruten Egenskaper i modulen **Samtykke til informasjonskapsler** legger du til og konfigurerer tekst og en kobling til siden med nettstedspersonvern.</span><span class="sxs-lookup"><span data-stu-id="b1982-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="b1982-137">I **Navigasjonsmeny**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b1982-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1982-138">I dialogboksen **Legg til modul** velger du **Navigasjonsmeny**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1982-139">I ruten Egenskape rfor navigasjonsmenymodulen velger du **Retail Server** under **Kilde til navigasjonsmeny**.</span><span class="sxs-lookup"><span data-stu-id="b1982-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="b1982-140">I ruten Egenskaper for navigasjonsmenymodulen velger du **Legg til menyelement** under **Statiske menyelementer**, og deretter velger du **Menyelement**.</span><span class="sxs-lookup"><span data-stu-id="b1982-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="b1982-141">I dialogboksen **Menyelement** skriver du inn "Kontakt" under **Menyelementtekst**.</span><span class="sxs-lookup"><span data-stu-id="b1982-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="b1982-142">I dialogboksen **Menyelement** velger du **Legg til en kobling** under **Koblingsmål for menyelement**.</span><span class="sxs-lookup"><span data-stu-id="b1982-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="b1982-143">I dialogboksen **Legg til en kobling** velger du URL-adressen for nettstedets Kontakt-side, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="b1982-144">Velg **OK** i dialogboksen **Menyelement**.</span><span class="sxs-lookup"><span data-stu-id="b1982-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="b1982-145">I **Søk**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b1982-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1982-146">I dialogboksen **Legg til modul** velger du **Søk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1982-147">Konfigurer egenskapene for søkemodulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="b1982-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="b1982-148">I **Handlevogn**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="b1982-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1982-149">I dialogboksen **Legg til modul** velger du **Handlevognikon**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1982-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1982-150">Konfigurer egenskapene for handlevognikon-modulen i egenskapsruten etter behov.</span><span class="sxs-lookup"><span data-stu-id="b1982-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="b1982-151">Hvis du vil at handlekurvikonet skal vise et sammendrag av handlekurven (også kjent som en minikurv) når brukerne holder pekeren over den, velger du **Vis minikurv**.</span><span class="sxs-lookup"><span data-stu-id="b1982-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="b1982-152">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="b1982-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b1982-153">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="b1982-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b1982-154">I **Topptekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.</span><span class="sxs-lookup"><span data-stu-id="b1982-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b1982-155">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="b1982-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1982-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b1982-156">Additional resources</span></span>

[<span data-ttu-id="b1982-157">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="b1982-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b1982-158">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="b1982-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b1982-159">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="b1982-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b1982-160">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="b1982-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b1982-161">Navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="b1982-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="b1982-162">Informasjonskapselsamtykke</span><span class="sxs-lookup"><span data-stu-id="b1982-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="b1982-163">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="b1982-163">Footer module</span></span>](author-footer-module.md)
