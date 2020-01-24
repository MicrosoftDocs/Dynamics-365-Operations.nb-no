---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696767"
---
# <a name="cart-module"></a><span data-ttu-id="f88c1-103">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f88c1-104">Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f88c1-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f88c1-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f88c1-105">Overview</span></span>

<span data-ttu-id="f88c1-106">En handlekurvmodul er container som brukes til å være vert for alle modulene som kreves for å vise varer som er i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="f88c1-106">A cart module is container that is used to host all the modules that are required to showcase items that are in the cart.</span></span> <span data-ttu-id="f88c1-107">Det inkluderer for eksempel alle varene som er lagt til i handlekurven, ordresammendrag og kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="f88c1-107">For example, it includes all the items that have been added to the cart, the order summary, and promotional codes.</span></span>

<span data-ttu-id="f88c1-108">Handlekurvmodul gjengir data basert på handlekurv-IDen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-108">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="f88c1-109">Handlekurv-IDen er en informasjonskapsel i leseren som er tilgjengelig på hele området.</span><span class="sxs-lookup"><span data-stu-id="f88c1-109">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="f88c1-110">Egenskaper og spor for handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-110">Cart module properties and slots</span></span>

<span data-ttu-id="f88c1-111">Som en container styrer en handlekurvmodul enkelte grunnleggende egenskaper, for eksempel overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="f88c1-111">As a container, a cart module controls some basic properties, such as the heading and the width.</span></span> <span data-ttu-id="f88c1-112">Overskriften er vanligvis tekst, for eksempel **Handlepose**, **Handlekurv** eller **varer i handlekurven**.</span><span class="sxs-lookup"><span data-stu-id="f88c1-112">The heading is typically text such as **Shopping bag**, **Your cart**, or **Items in your cart**.</span></span> <span data-ttu-id="f88c1-113">Breddeinnstillingen bestemmer om modulene i beholderen må passe i denne beholderen, eller om de kan fylle skjermen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-113">The width setting determines whether the modules inside the container must fit within that container, or whether they can fill the screen.</span></span>

<span data-ttu-id="f88c1-114">Handlekurvsiden er delt inn i flere områder: handlekurvlinjeelementer, ordresammendrag og kasse og "finn i butikk"-funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="f88c1-114">The cart page is divided into multiple regions: cart line items, order summary and checkout, and "find in store" functionality.</span></span> <span data-ttu-id="f88c1-115">Hver region er tilordnet et spor i handlevognmodulen, og hvert spor godtar et forhånds definert sett med moduler.</span><span class="sxs-lookup"><span data-stu-id="f88c1-115">Each region is mapped to a slot in the cart module, and every slot accepts a predefined set of modules.</span></span>

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="f88c1-116">Moduler som kan brukes i handlekurvmodulen</span><span class="sxs-lookup"><span data-stu-id="f88c1-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="f88c1-117">**Linjeelementer for handlekurv** – Denne modulen viser et sammendrag av hver vare som er lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="f88c1-117">**Cart line items** – This module shows a summary of every item that has been added to the cart.</span></span> <span data-ttu-id="f88c1-118">Informasjonen omfatter produkttittelen, valgte dimensjoner, pris, antall og rabatter.</span><span class="sxs-lookup"><span data-stu-id="f88c1-118">The information includes the product title, selected dimensions, price, quantity, and discounts.</span></span> <span data-ttu-id="f88c1-119">Denne modulen støtter også handlinger som "fjern fra kurv" og "legg til i ønskeliste".</span><span class="sxs-lookup"><span data-stu-id="f88c1-119">This module also supports actions such as "remove from cart" and "add to wish list."</span></span> <span data-ttu-id="f88c1-120">For hver linjevare finnes det et alternativ for å levere varen eller plukke den opp fra butikken.</span><span class="sxs-lookup"><span data-stu-id="f88c1-120">For each line item, there is an option to ship the item or pick it up from the store.</span></span> <span data-ttu-id="f88c1-121">Dette alternativet må konfigureres separat i plukkingen i butikkmodulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-121">This option must be configured separately in the pick up in store module.</span></span>
- <span data-ttu-id="f88c1-122">**Ordresammendrag** – Denne modulen viser et ordresammendrag.</span><span class="sxs-lookup"><span data-stu-id="f88c1-122">**Order summary** – This module shows an order summary.</span></span> <span data-ttu-id="f88c1-123">Informasjonen omfatter delsum, forsendelse, avgifter og sparing.</span><span class="sxs-lookup"><span data-stu-id="f88c1-123">The information includes the subtotal, shipping, taxes, and savings.</span></span> <span data-ttu-id="f88c1-124">En overskrift kan konfigureres for denne modulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-124">A heading can be configured for this module.</span></span>
- <span data-ttu-id="f88c1-125">**Promokode** – Denne modulen lar kundene løse inn kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="f88c1-125">**Promo code** – This module lets the customer redeem promotional codes.</span></span> <span data-ttu-id="f88c1-126">En kampanjekode kan brukes eller fjernes.</span><span class="sxs-lookup"><span data-stu-id="f88c1-126">A promotional code can be applied or removed.</span></span>
- <span data-ttu-id="f88c1-127">**Kasse** – Denne modulen starter utsjekkingshandlingen og omdirigerer brukeren til utsjekkingssiden.</span><span class="sxs-lookup"><span data-stu-id="f88c1-127">**Checkout** – This module initiates the checkout action and redirects the user to the checkout page.</span></span> <span data-ttu-id="f88c1-128">Tre koblinger må konfigureres for denne modulen:</span><span class="sxs-lookup"><span data-stu-id="f88c1-128">Three links must be configured for this module:</span></span>

    - <span data-ttu-id="f88c1-129">**Kasse** – Denne koblingen tvinger kunder til å logge seg på hvis de ikke allerede er logget på.</span><span class="sxs-lookup"><span data-stu-id="f88c1-129">**Checkout** – This link forces customers to sign in if they aren't already signed in.</span></span>
    - <span data-ttu-id="f88c1-130">**Sjekk ut som gjest** – Med denne koblingen kan anonyme kunder legge inn ordrer.</span><span class="sxs-lookup"><span data-stu-id="f88c1-130">**Guest checkout** – This link lets anonymous customers place orders.</span></span> <span data-ttu-id="f88c1-131">Den vises bare når kunder ikke er logget på.</span><span class="sxs-lookup"><span data-stu-id="f88c1-131">It's shown only when customers aren't signed in.</span></span>
    - <span data-ttu-id="f88c1-132">**Tilbake til shopping** – Med denne koblingen kan kunder til å gå til startsiden og en annen side, slik at de kan fortsette å handle.</span><span class="sxs-lookup"><span data-stu-id="f88c1-132">**Back to shopping** – This link lets customers go to the home page or any other page, so that they can continue to shop.</span></span>

- <span data-ttu-id="f88c1-133">**Innholdsrik blokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-133">**Content rich block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="f88c1-134">Meldingene drives av innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="f88c1-134">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="f88c1-135">Alle meldinger kan legges til, for eksempel "For problemer med en ordre, kontakt 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="f88c1-135">Any message can be added, such as "For issues with the order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="f88c1-136">**Hent i butikk** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="f88c1-136">**Pick up in store** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="f88c1-137">Som standard viser denne modulen butikker som er innen en 50 kilometers radius til kundenslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-137">By default, this module shows stores that are within a 50-mile radius of the customer's location.</span></span> <span data-ttu-id="f88c1-138">Radiusen for søk kan imidlertid tilpasses i modulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-138">However, the search radius can be customized in the module.</span></span> <span data-ttu-id="f88c1-139">For hver butikk utføres det en lagerkontroll, hvis lagerkontrollfunksjonaliteten er aktivert, og det vises en gjeldende på lager- eller tomt-melding.</span><span class="sxs-lookup"><span data-stu-id="f88c1-139">For each store, an inventory check is done, if the inventory check functionality is turned on, and an appropriate in-stock or out-of-stock message is shown.</span></span>
- <span data-ttu-id="f88c1-140">**Butikksøk etter Bing-kart** – Denne modulen kan brukes i hente i butikk-modulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-140">**Store search by Bing Maps** – This module can be used inside the pick up in store module.</span></span> <span data-ttu-id="f88c1-141">Den lar kunder søke etter butikker ved å angi en lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f88c1-141">It lets customers search for stores by entering a location.</span></span> <span data-ttu-id="f88c1-142">APIen (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet brukes til å konvertere lokasjonen som kunden anga, til en breddegrad og en lengdegrad.</span><span class="sxs-lookup"><span data-stu-id="f88c1-142">The Bing Maps geocoding application programming interface (API) is used to convert the location that the customer entered to a latitude and a longitude.</span></span> <span data-ttu-id="f88c1-143">Hvis denne modulen ikke brukes, vises bare butikker som er nær kundens gjeldende lokasjon, og kunden kan ikke søke etter en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f88c1-143">If this module isn't used, only stores that are near the customer's current location are shown, and the customer can't search for a different location.</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="f88c1-144">Handlekurvmodulinnstillinger</span><span class="sxs-lookup"><span data-stu-id="f88c1-144">Cart module settings</span></span>

<span data-ttu-id="f88c1-145">Handlevognmoduler har tre innstillinger som kan konfigureres:</span><span class="sxs-lookup"><span data-stu-id="f88c1-145">Cart modules have three settings that can be configured:</span></span>

- <span data-ttu-id="f88c1-146">**Maksimalt antall** – Maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="f88c1-146">**Maximum quantity** – The maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="f88c1-147">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="f88c1-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="f88c1-148">**Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager.</span><span class="sxs-lookup"><span data-stu-id="f88c1-148">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="f88c1-149">Denne lagerkontrollen utføres både for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken.</span><span class="sxs-lookup"><span data-stu-id="f88c1-149">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="f88c1-150">Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.</span><span class="sxs-lookup"><span data-stu-id="f88c1-150">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="f88c1-151">**Lagerbuffer** – Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall.</span><span class="sxs-lookup"><span data-stu-id="f88c1-151">**Inventory buffer** – Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="f88c1-152">Derfor kan en buffer defineres for lager.</span><span class="sxs-lookup"><span data-stu-id="f88c1-152">Therefore, a buffer can be defined for inventory.</span></span> <span data-ttu-id="f88c1-153">Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager.</span><span class="sxs-lookup"><span data-stu-id="f88c1-153">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="f88c1-154">Derfor, når salget skjer raskt i flere kanaler, slik at lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.</span><span class="sxs-lookup"><span data-stu-id="f88c1-154">Therefore, when sales occur quickly through several channels, so that the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="f88c1-155">Interaksjon med detaljhandelsserver</span><span class="sxs-lookup"><span data-stu-id="f88c1-155">Retail Server interaction</span></span>

<span data-ttu-id="f88c1-156">Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Retail Server.</span><span class="sxs-lookup"><span data-stu-id="f88c1-156">The cart module retrieves product information by using Retail Server APIs.</span></span> <span data-ttu-id="f88c1-157">Handlekurv-IDen fra lesereninformasjonskapselen brukes til å hente all produktinformasjon fra Retail server.</span><span class="sxs-lookup"><span data-stu-id="f88c1-157">The cart ID from the browser cookie is used to retrieve all the product information from Retail Server.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="f88c1-158">Legge til en handlekurvmodul på en side</span><span class="sxs-lookup"><span data-stu-id="f88c1-158">Add a cart module to a page</span></span>

<span data-ttu-id="f88c1-159">Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f88c1-159">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f88c1-160">Opprett et fragment kalt **handlekurvfragment**, og legg til en handlekurvmodul i den.</span><span class="sxs-lookup"><span data-stu-id="f88c1-160">Create a fragment that is named **cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="f88c1-161">I **Linjeelementer for handlekurv**-sporet i handlekurvmodulen legger du til handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-161">In the **Cart line items** slot of the cart module, add a cart line items module.</span></span>
1. <span data-ttu-id="f88c1-162">I **Ordresammendrag**-sporet legger du til en ordresammendragsmodul.</span><span class="sxs-lookup"><span data-stu-id="f88c1-162">In the **Order summary** slot, add an order summary module.</span></span>
1. <span data-ttu-id="f88c1-163">Legg til en promokodemodul i **Promokode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="f88c1-163">In the **Promo code** slot, add a promo code module.</span></span>
1. <span data-ttu-id="f88c1-164">Legg til en kassemodul i **Kasse**-modulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-164">In the **Checkout** slot, add a checkout module.</span></span>
1. <span data-ttu-id="f88c1-165">I **Finn i butikk**-sporet legger du til en plukking i butikkmodul.</span><span class="sxs-lookup"><span data-stu-id="f88c1-165">In the **Find in Store** slot, add a pick up in store module.</span></span>
1. <span data-ttu-id="f88c1-166">I hent i butikk-modulen velger du **Butikksøk**-sporet og legger til et butikksøk etter Bing-kart-modulen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-166">In the pick up in store module, select the **Store search** slot, and add a store search by Bing Maps module.</span></span>
1. <span data-ttu-id="f88c1-167">Sjekk inn fragmentet, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="f88c1-167">Check in the fragment, and publish it.</span></span>
1. <span data-ttu-id="f88c1-168">Opprett en mal som heter **handlekurvmal**, og legg til handlekurvfragmentet som du nettopp opprettet, i det.</span><span class="sxs-lookup"><span data-stu-id="f88c1-168">Create a template that is named **cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="f88c1-169">Lagre malen, sjekk den inn og publiser den.</span><span class="sxs-lookup"><span data-stu-id="f88c1-169">Save the template, check it in, and publish it.</span></span>
1. <span data-ttu-id="f88c1-170">Opprett en side som bruker den nye malen.</span><span class="sxs-lookup"><span data-stu-id="f88c1-170">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="f88c1-171">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="f88c1-171">Save and preview the page.</span></span>
1. <span data-ttu-id="f88c1-172">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="f88c1-172">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f88c1-173">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f88c1-173">Additional resources</span></span>

[<span data-ttu-id="f88c1-174">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="f88c1-174">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f88c1-175">Containermodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f88c1-176">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-176">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f88c1-177">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f88c1-178">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f88c1-179">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f88c1-180">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="f88c1-180">Footer module</span></span>](author-footer-module.md)