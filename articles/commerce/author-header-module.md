---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697281"
---
# <a name="header-module"></a><span data-ttu-id="0f86a-103">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-103">Header module</span></span>

<span data-ttu-id="0f86a-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="0f86a-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="0f86a-105">Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f86a-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0f86a-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0f86a-106">Overview</span></span>

<span data-ttu-id="0f86a-107">En topptekstmodul er en spesialcontainer som brukes til å være vert for alle modulene som skal vises i toppteksten på en side.</span><span class="sxs-lookup"><span data-stu-id="0f86a-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="0f86a-108">Den kan for eksempel inkludere områdelogoen, koblinger til navigasjonshierarkiet, koblinger til andre sider på området og søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="0f86a-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="0f86a-109">En topptekstmodul optimaliseres automatisk for enheten som området vises på (det vil si en skrivebordsenhet eller mobilenhet).</span><span class="sxs-lookup"><span data-stu-id="0f86a-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="0f86a-110">På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).</span><span class="sxs-lookup"><span data-stu-id="0f86a-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="0f86a-111">Egenskaper for en topptekst</span><span class="sxs-lookup"><span data-stu-id="0f86a-111">Properties of a header</span></span>

<span data-ttu-id="0f86a-112">I likhet med generiske containere støtter en topptekstmodul egenskapene **topptekst** og **bredde**.</span><span class="sxs-lookup"><span data-stu-id="0f86a-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="0f86a-113">En topptekstmodul har flere spor.</span><span class="sxs-lookup"><span data-stu-id="0f86a-113">A header module has multiple slots.</span></span> <span data-ttu-id="0f86a-114">Det finnes for eksempel spor for en informasjonsmelding, navigasjonsmeny, logo, søkefelt, handlekurvikon, ønsketlisteikon og kontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="0f86a-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="0f86a-115">Hvert spor støtter et bestemt sett med moduler.</span><span class="sxs-lookup"><span data-stu-id="0f86a-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="0f86a-116">Moduler som er tilgjengelige i en overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-116">Modules that are available in a header module</span></span>

<span data-ttu-id="0f86a-117">Følgende moduler kan brukes i en topptekstmodul:</span><span class="sxs-lookup"><span data-stu-id="0f86a-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="0f86a-118">**Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger.</span><span class="sxs-lookup"><span data-stu-id="0f86a-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="0f86a-119">Kanalnavigeringshierarkiet kan konfigureres i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="0f86a-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="0f86a-120">Konfigurerte varer vises deretter som topptekstnavigasjon.</span><span class="sxs-lookup"><span data-stu-id="0f86a-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="0f86a-121">I tillegg kan statiske navigasjonskoblinger konfigureres, og relative koblinger til andre sider på området for e-handel kan angis.</span><span class="sxs-lookup"><span data-stu-id="0f86a-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="0f86a-122">Selve hodet kan justeres fra venstre, høyre eller i midten.</span><span class="sxs-lookup"><span data-stu-id="0f86a-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="0f86a-123">**Handlekurvikon** – Handlekurvikonet er et spesialikon som representerer handlekurven.</span><span class="sxs-lookup"><span data-stu-id="0f86a-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="0f86a-124">Det vises i toppteksten og viser antallet varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="0f86a-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="0f86a-125">En kobling til handlekurvsiden må følge med handlekurvikonet, slik at kunder kan omadresseres til handlevognsiden når de samhandler med ikonet.</span><span class="sxs-lookup"><span data-stu-id="0f86a-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="0f86a-126">**Ønskelisteikon** – Ikonet for ønskeliste vises i hodet og viser antallet varer som er lagt til på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="0f86a-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="0f86a-127">En kobling til ønskelistesiden må følge med dette konet, slik at kunder kan omadresseres til handlevognsiden når de samhandler med ikonet.</span><span class="sxs-lookup"><span data-stu-id="0f86a-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="0f86a-128">**Påloggingsmodul** – Påloggingsmodulen vises i hodet.</span><span class="sxs-lookup"><span data-stu-id="0f86a-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="0f86a-129">Den lar kundene enten logge på kontoen eller registrere seg for en konto.</span><span class="sxs-lookup"><span data-stu-id="0f86a-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="0f86a-130">Hvis kunden allerede er logget på, kan modulen konfigureres til å vise koblinger til kontosiden, ordreloggsiden eller en annen side.</span><span class="sxs-lookup"><span data-stu-id="0f86a-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="0f86a-131">**Logomodul** – Denne modulen viser logoen som representerer forhandleren og merket.</span><span class="sxs-lookup"><span data-stu-id="0f86a-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="0f86a-132">Det er et bilde som har en kobling.</span><span class="sxs-lookup"><span data-stu-id="0f86a-132">It's an image that has a link.</span></span> <span data-ttu-id="0f86a-133">Koblingen er vanligvis konfigurert slik at den har en omadressering til startsiden, og derfor kan kundene raskt gå tilbake til startsiden fra en hvilken som helst side på området.</span><span class="sxs-lookup"><span data-stu-id="0f86a-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="0f86a-134">**Varsel** – Et varsel vises i toppteksten og brukes til å vise en innebygd melding som gjelder alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="0f86a-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="0f86a-135">Et varsel kan for eksempel vise en melding som "Årets salg avsluttes om 2 dager".</span><span class="sxs-lookup"><span data-stu-id="0f86a-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="0f86a-136">**Søkefelt** – Med søkefeltet kan brukere angi søkeord, slik at de kan søke etter produkter.</span><span class="sxs-lookup"><span data-stu-id="0f86a-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="0f86a-137">Modulen må konfigureres med URL-adressen til søkeresultatsiden.</span><span class="sxs-lookup"><span data-stu-id="0f86a-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="0f86a-138">Parameteren for spørringsstrengen kan konfigureres (standardverdien er **"q"**).</span><span class="sxs-lookup"><span data-stu-id="0f86a-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="0f86a-139">Søkefeltet har et spor for automatiske forslag der modulen for automatiske forslag skal legges til.</span><span class="sxs-lookup"><span data-stu-id="0f86a-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="0f86a-140">**Automatisk forslag** – Modulen for automatisk forslag viser resultater for automatiske forslag.</span><span class="sxs-lookup"><span data-stu-id="0f86a-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="0f86a-141">Disse resultatene kan være nøkkelord, produkter eller kategorier der søkeordet finnes.</span><span class="sxs-lookup"><span data-stu-id="0f86a-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="0f86a-142">Opprette en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-142">Create a header module</span></span>

<span data-ttu-id="0f86a-143">Hvis du vil opprette en topptekstmodul, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="0f86a-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="0f86a-144">Opprett et sidefragment som inneholder en topptekstmodul.</span><span class="sxs-lookup"><span data-stu-id="0f86a-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="0f86a-145">Legg til moduler i sporene i hodemodulen.</span><span class="sxs-lookup"><span data-stu-id="0f86a-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="0f86a-146">Oppdater innstillingene for hver modul.</span><span class="sxs-lookup"><span data-stu-id="0f86a-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="0f86a-147">Lagre sidefragmentet.</span><span class="sxs-lookup"><span data-stu-id="0f86a-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="0f86a-148">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="0f86a-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="0f86a-149">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="0f86a-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="0f86a-150">På standardsiden legger du til sidefragmentet som inneholder topptekstmodulen, i toppteksten i hovedsporet.</span><span class="sxs-lookup"><span data-stu-id="0f86a-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="0f86a-151">Lagre malen.</span><span class="sxs-lookup"><span data-stu-id="0f86a-151">Save the template.</span></span> 
1. <span data-ttu-id="0f86a-152">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="0f86a-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f86a-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0f86a-153">Additional resources</span></span>

[<span data-ttu-id="0f86a-154">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="0f86a-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0f86a-155">Containermodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0f86a-156">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0f86a-157">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0f86a-158">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0f86a-159">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0f86a-160">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0f86a-161">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="0f86a-161">Footer module</span></span>](author-footer-module.md)
