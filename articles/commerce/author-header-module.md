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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885484"
---
# <a name="header-module"></a><span data-ttu-id="b0281-103">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b0281-104">Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0281-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b0281-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b0281-105">Overview</span></span>

<span data-ttu-id="b0281-106">En topptekstmodul er en spesialcontainer som brukes til å være vert for alle modulene som skal vises i toppteksten på en side.</span><span class="sxs-lookup"><span data-stu-id="b0281-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="b0281-107">Den kan for eksempel inkludere områdelogoen, koblinger til navigasjonshierarkiet, koblinger til andre sider på området og søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="b0281-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="b0281-108">En topptekstmodul optimaliseres automatisk for enheten som området vises på (det vil si en skrivebordsenhet eller mobilenhet).</span><span class="sxs-lookup"><span data-stu-id="b0281-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="b0281-109">På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).</span><span class="sxs-lookup"><span data-stu-id="b0281-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="b0281-110">Egenskaper for en topptekst</span><span class="sxs-lookup"><span data-stu-id="b0281-110">Properties of a header</span></span>

<span data-ttu-id="b0281-111">I likhet med generiske containere støtter en topptekstmodul egenskapene **topptekst** og **bredde**.</span><span class="sxs-lookup"><span data-stu-id="b0281-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="b0281-112">En topptekstmodul har flere spor.</span><span class="sxs-lookup"><span data-stu-id="b0281-112">A header module has multiple slots.</span></span> <span data-ttu-id="b0281-113">Det finnes for eksempel spor for en informasjonsmelding, navigasjonsmeny, logo, søkefelt, handlekurvikon, ønsketlisteikon og kontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="b0281-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="b0281-114">Hvert spor støtter et bestemt sett med moduler.</span><span class="sxs-lookup"><span data-stu-id="b0281-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="b0281-115">Moduler som er tilgjengelige i en overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-115">Modules that are available in a header module</span></span>

<span data-ttu-id="b0281-116">Følgende moduler kan brukes i en topptekstmodul:</span><span class="sxs-lookup"><span data-stu-id="b0281-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="b0281-117">**Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger.</span><span class="sxs-lookup"><span data-stu-id="b0281-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="b0281-118">Kanalnavigeringshierarkiet kan konfigureres i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="b0281-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="b0281-119">Konfigurerte varer vises deretter som topptekstnavigasjon.</span><span class="sxs-lookup"><span data-stu-id="b0281-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="b0281-120">I tillegg kan statiske navigasjonskoblinger konfigureres, og relative koblinger til andre sider på området for e-handel kan angis.</span><span class="sxs-lookup"><span data-stu-id="b0281-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="b0281-121">Selve hodet kan justeres fra venstre, høyre eller i midten.</span><span class="sxs-lookup"><span data-stu-id="b0281-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="b0281-122">**Handlekurvikon** – Handlekurvikonet er et spesialikon som representerer handlekurven.</span><span class="sxs-lookup"><span data-stu-id="b0281-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="b0281-123">Det vises i toppteksten og viser antallet varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="b0281-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="b0281-124">En kobling til handlekurvsiden må følge med handlekurvikonet, slik at kunder kan omadresseres til handlevognsiden når de samhandler med ikonet.</span><span class="sxs-lookup"><span data-stu-id="b0281-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="b0281-125">**Ønskelisteikon** – Ikonet for ønskeliste vises i hodet og viser antallet varer som er lagt til på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="b0281-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="b0281-126">En kobling til ønskelistesiden må følge med dette konet, slik at kunder kan omadresseres til handlevognsiden når de samhandler med ikonet.</span><span class="sxs-lookup"><span data-stu-id="b0281-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="b0281-127">**Påloggingsmodul** – Påloggingsmodulen vises i hodet.</span><span class="sxs-lookup"><span data-stu-id="b0281-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="b0281-128">Den lar kundene enten logge på kontoen eller registrere seg for en konto.</span><span class="sxs-lookup"><span data-stu-id="b0281-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="b0281-129">Hvis kunden allerede er logget på, kan modulen konfigureres til å vise koblinger til kontosiden, ordreloggsiden eller en annen side.</span><span class="sxs-lookup"><span data-stu-id="b0281-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="b0281-130">**Logomodul** – Denne modulen viser logoen som representerer forhandleren og merket.</span><span class="sxs-lookup"><span data-stu-id="b0281-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="b0281-131">Det er et bilde som har en kobling.</span><span class="sxs-lookup"><span data-stu-id="b0281-131">It's an image that has a link.</span></span> <span data-ttu-id="b0281-132">Koblingen er vanligvis konfigurert slik at den har en omadressering til startsiden, og derfor kan kundene raskt gå tilbake til startsiden fra en hvilken som helst side på området.</span><span class="sxs-lookup"><span data-stu-id="b0281-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="b0281-133">**Varsel** – Et varsel vises i toppteksten og brukes til å vise en innebygd melding som gjelder alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="b0281-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="b0281-134">Et varsel kan for eksempel vise en melding som "Årets salg avsluttes om 2 dager".</span><span class="sxs-lookup"><span data-stu-id="b0281-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="b0281-135">**Søkefelt** – Med søkefeltet kan brukere angi søkeord, slik at de kan søke etter produkter.</span><span class="sxs-lookup"><span data-stu-id="b0281-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="b0281-136">Modulen må konfigureres med URL-adressen til søkeresultatsiden.</span><span class="sxs-lookup"><span data-stu-id="b0281-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="b0281-137">Parameteren for spørringsstrengen kan konfigureres (standardverdien er **"q"**).</span><span class="sxs-lookup"><span data-stu-id="b0281-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="b0281-138">Søkefeltet har et spor for automatiske forslag der modulen for automatiske forslag skal legges til.</span><span class="sxs-lookup"><span data-stu-id="b0281-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="b0281-139">**Automatisk forslag** – Modulen for automatisk forslag viser resultater for automatiske forslag.</span><span class="sxs-lookup"><span data-stu-id="b0281-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="b0281-140">Disse resultatene kan være nøkkelord, produkter eller kategorier der søkeordet finnes.</span><span class="sxs-lookup"><span data-stu-id="b0281-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="b0281-141">Opprette en topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-141">Create a header module</span></span>

<span data-ttu-id="b0281-142">Hvis du vil opprette en topptekstmodul, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b0281-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="b0281-143">Opprett et sidefragment som inneholder en topptekstmodul.</span><span class="sxs-lookup"><span data-stu-id="b0281-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="b0281-144">Legg til moduler i sporene i hodemodulen.</span><span class="sxs-lookup"><span data-stu-id="b0281-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="b0281-145">Oppdater innstillingene for hver modul.</span><span class="sxs-lookup"><span data-stu-id="b0281-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="b0281-146">Lagre sidefragmentet.</span><span class="sxs-lookup"><span data-stu-id="b0281-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="b0281-147">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="b0281-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="b0281-148">For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.</span><span class="sxs-lookup"><span data-stu-id="b0281-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b0281-149">På standardsiden legger du til sidefragmentet som inneholder topptekstmodulen, i toppteksten i hovedsporet.</span><span class="sxs-lookup"><span data-stu-id="b0281-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="b0281-150">Lagre malen.</span><span class="sxs-lookup"><span data-stu-id="b0281-150">Save the template.</span></span> 
1. <span data-ttu-id="b0281-151">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="b0281-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0281-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b0281-152">Additional resources</span></span>

[<span data-ttu-id="b0281-153">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="b0281-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b0281-154">Containermodul</span><span class="sxs-lookup"><span data-stu-id="b0281-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b0281-155">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b0281-156">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b0281-157">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="b0281-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b0281-158">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b0281-159">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b0281-160">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="b0281-160">Footer module</span></span>](author-footer-module.md)
