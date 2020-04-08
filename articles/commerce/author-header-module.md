---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025687"
---
# <a name="header-module"></a><span data-ttu-id="becb3-103">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="becb3-104">Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="becb3-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="becb3-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="becb3-105">Overview</span></span>

<span data-ttu-id="becb3-106">I Dynamics 365 Commerce omfatter en sideoverskrift flere moduler, for eksempel modul for topptekst, navigasjonsmeny, søk, kampanjebanner og samtykke til informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="becb3-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="becb3-107">Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, et kurvsymbol, et ønskelistesymbol, påloggingsalternativer og søkefelt.</span><span class="sxs-lookup"><span data-stu-id="becb3-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="becb3-108">En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet).</span><span class="sxs-lookup"><span data-stu-id="becb3-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="becb3-109">På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).</span><span class="sxs-lookup"><span data-stu-id="becb3-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="becb3-110">Egenskaper for en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-110">Properties of a header module</span></span>

<span data-ttu-id="becb3-111">En topptekstmodul støtter **Logobilde**, **Logokobling** og egenskaper for **Min konto-koblinger**.</span><span class="sxs-lookup"><span data-stu-id="becb3-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="becb3-112">**Logobilde**- og **Logokobling**-egenskapene brukes til å definere en logo på siden.</span><span class="sxs-lookup"><span data-stu-id="becb3-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="becb3-113">Hvis du vil ha mer informasjon, kan du se [Legge til en logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="becb3-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="becb3-114">Egenskapen **Min konto-koblinger** kan brukes til å definere kontosider som områdeeieren ønsker å vise hurtigkoblinger for i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="becb3-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="becb3-115">Moduler som er tilgjengelige i en overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-115">Modules that are available in a header module</span></span>

<span data-ttu-id="becb3-116">Følgende moduler kan brukes i en topptekstmodul:</span><span class="sxs-lookup"><span data-stu-id="becb3-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="becb3-117">**Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger.</span><span class="sxs-lookup"><span data-stu-id="becb3-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="becb3-118">Kanalnavigeringshierarkiet kan konfigureres i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="becb3-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="becb3-119">Navigasjonsmenyen har egenskapen **Navigasjonskilde** som brukes til å angi navigasjonsmenyelementer og statiske menyelementer for Retail Server som en kilde.</span><span class="sxs-lookup"><span data-stu-id="becb3-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="becb3-120">Hvis statiske menyelementer angis som en kilde, kan relative koblinger til andre sider på området angis.</span><span class="sxs-lookup"><span data-stu-id="becb3-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="becb3-121">Konfigurerte varer vises deretter som topptekstnavigasjon.</span><span class="sxs-lookup"><span data-stu-id="becb3-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="becb3-122">**Søk** – Med søkemodulen kan brukere angi søkeord for å søke etter produkter.</span><span class="sxs-lookup"><span data-stu-id="becb3-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="becb3-123">URL-adressen til standard søkeside og parameterne for søkespørringen må angis under **Områdeinnstillinger \> Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="becb3-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="becb3-124">Søkemodulen har egenskaper som lar deg skjule søkeknappen eller etiketten etter behov.</span><span class="sxs-lookup"><span data-stu-id="becb3-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="becb3-125">Søkemodulen støtter også alternativer for automatiske forslag, for eksempel søkeresultater for produkt, nøkkelord og kategori.</span><span class="sxs-lookup"><span data-stu-id="becb3-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="becb3-126">Opprette en topptekstmodul for en side</span><span class="sxs-lookup"><span data-stu-id="becb3-126">Create a header module for a page</span></span>

<span data-ttu-id="becb3-127">Hvis du vil opprette en topptekstmodul, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="becb3-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="becb3-128">Opprett et fragment kalt **Topptekstfragment**, og legg til en containermodul i den.</span><span class="sxs-lookup"><span data-stu-id="becb3-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="becb3-129">I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="becb3-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="becb3-130">Legg til moduler for kampanjebanner og samtykke til informasjonskapsler i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="becb3-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="becb3-131">Legg til en ny containermodul i fragmentet, og sett **Bredde**-egenskapen til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="becb3-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="becb3-132">Legg til en topptekstmodul i den andre containermodulen.</span><span class="sxs-lookup"><span data-stu-id="becb3-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="becb3-133">Legg til en navigasjonsmenymodul i **Navigasjonsmeny**-sporet i topptekstmodulen.</span><span class="sxs-lookup"><span data-stu-id="becb3-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="becb3-134">Konfigurer egenskapene for navigasjonsmenymodulen i egenskapsruten for navigasjonsmenymodulen.</span><span class="sxs-lookup"><span data-stu-id="becb3-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="becb3-135">Legg til en søkemodul i **Søk**-sporet i topptekstmodulen.</span><span class="sxs-lookup"><span data-stu-id="becb3-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="becb3-136">Konfigurer egenskapene for søkemodulen i egenskapsruten for søkemodulen.</span><span class="sxs-lookup"><span data-stu-id="becb3-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="becb3-137">Lagre sidefragmentet, fullfør redigeringen av det, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="becb3-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="becb3-138">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="becb3-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="becb3-139">I **Hoved**-sporet på standardsiden legger du til topptekstsidefragmentet som inneholder topptekstmodulen, i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="becb3-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="becb3-140">Lagre malen, fullfør redigeringen av den, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="becb3-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="becb3-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="becb3-141">Additional resources</span></span>

[<span data-ttu-id="becb3-142">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="becb3-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="becb3-143">Containermodul</span><span class="sxs-lookup"><span data-stu-id="becb3-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="becb3-144">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="becb3-145">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="becb3-146">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="becb3-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="becb3-147">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="becb3-148">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="becb3-149">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="becb3-149">Footer module</span></span>](author-footer-module.md)
