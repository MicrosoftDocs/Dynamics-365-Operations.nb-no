---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025442"
---
# <a name="cart-module"></a><span data-ttu-id="1e002-103">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="1e002-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1e002-104">Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e002-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1e002-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="1e002-105">Overview</span></span>

<span data-ttu-id="1e002-106">En handlekurvmodul brukes til å vise varene som er lagt til i handlekurven før kunden går videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="1e002-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="1e002-107">Det inkluderer for eksempel alle varene som er lagt til i handlekurven og et ordresammendrag.</span><span class="sxs-lookup"><span data-stu-id="1e002-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="1e002-108">Den lar også kunden bruke eller fjerne kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="1e002-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="1e002-109">Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest.</span><span class="sxs-lookup"><span data-stu-id="1e002-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="1e002-110">Den støtter også koblingen **Tilbake til shopping**.</span><span class="sxs-lookup"><span data-stu-id="1e002-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="1e002-111">Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="1e002-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="1e002-112">Handlekurvmodul gjengir data basert på handlekurv-IDen.</span><span class="sxs-lookup"><span data-stu-id="1e002-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="1e002-113">Handlekurv-IDen er en informasjonskapsel i leseren som er tilgjengelig på hele området.</span><span class="sxs-lookup"><span data-stu-id="1e002-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="1e002-114">Egenskaper og spor for handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="1e002-114">Cart module properties and slots</span></span>

<span data-ttu-id="1e002-115">Handlekurvmodulen har egenskapen **Overskrift** som kan settes til verdier som **Handlepose** og **Varer i handlekurven**.</span><span class="sxs-lookup"><span data-stu-id="1e002-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="1e002-116">Moduler som kan brukes i handlekurvmodulen</span><span class="sxs-lookup"><span data-stu-id="1e002-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="1e002-117">**Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="1e002-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="1e002-118">Meldingene drives av innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="1e002-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="1e002-119">Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="1e002-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="1e002-120">**Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="1e002-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="1e002-121">Den lar brukere angi en plassering for å finne butikker i nærheten.</span><span class="sxs-lookup"><span data-stu-id="1e002-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="1e002-122">Butikkvelgermodulen er integrert med API-en (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet for å konvertere lokasjonen til en breddegrad og lengdegrad.</span><span class="sxs-lookup"><span data-stu-id="1e002-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="1e002-123">En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for detaljhandel i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="1e002-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="1e002-124">Denne modulen støtter to egenskaper, **Søkeradius** og **Vilkår for bruk-kobling**.</span><span class="sxs-lookup"><span data-stu-id="1e002-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="1e002-125">Egenskapen **Søkeradius** definerer søkeradiusen for butikker i engelske mil.</span><span class="sxs-lookup"><span data-stu-id="1e002-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="1e002-126">Hvis ingen verdi er angitt, brukes standard søkeradius, 50 engelske mil.</span><span class="sxs-lookup"><span data-stu-id="1e002-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="1e002-127">Hvis Bing-kart eller en ekstern tjeneste brukes, kan egenskapen **Vilkår for bruk-kobling** brukes til å angi en kobling til vilkårene for bruk.</span><span class="sxs-lookup"><span data-stu-id="1e002-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="1e002-128">Det kreves en vilkår for bruk-kobling for Bing-kart-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="1e002-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="1e002-129">Handlekurvmodulinnstillinger</span><span class="sxs-lookup"><span data-stu-id="1e002-129">Cart module settings</span></span>

<span data-ttu-id="1e002-130">Handlekurvmoduler har følgende innstillinger som kan konfigureres under **Områdeinnstillinger \> Utvidelser**:</span><span class="sxs-lookup"><span data-stu-id="1e002-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="1e002-131">**Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="1e002-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="1e002-132">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="1e002-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="1e002-133">**Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager.</span><span class="sxs-lookup"><span data-stu-id="1e002-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="1e002-134">Denne lagerkontrollen utføres både for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken.</span><span class="sxs-lookup"><span data-stu-id="1e002-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="1e002-135">Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.</span><span class="sxs-lookup"><span data-stu-id="1e002-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="1e002-136">**Lagerbuffer** – Denne egenskapen brukes til å angi et bufferantall for lageret.</span><span class="sxs-lookup"><span data-stu-id="1e002-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="1e002-137">Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall.</span><span class="sxs-lookup"><span data-stu-id="1e002-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="1e002-138">Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager.</span><span class="sxs-lookup"><span data-stu-id="1e002-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="1e002-139">Derfor, når salget skjer raskt i flere kanaler og lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.</span><span class="sxs-lookup"><span data-stu-id="1e002-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="1e002-140">**Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="1e002-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="1e002-141">Denne ruten kan konfigureres på områdenivået.</span><span class="sxs-lookup"><span data-stu-id="1e002-141">This route can be configured at the site level.</span></span> <span data-ttu-id="1e002-142">Denne konfigurasjonen gjør at forhandlerne kan ta kunden tilbake til startsiden eller en annen side på området.</span><span class="sxs-lookup"><span data-stu-id="1e002-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="1e002-143">Samhandling med Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="1e002-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="1e002-144">Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1e002-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="1e002-145">Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1e002-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="1e002-146">Legge til en handlekurvmodul på en side</span><span class="sxs-lookup"><span data-stu-id="1e002-146">Add a cart module to a page</span></span>

<span data-ttu-id="1e002-147">Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="1e002-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1e002-148">Opprett et fragment kalt **Handlekurvfragment**, og legg til en handlekurvmodul i den.</span><span class="sxs-lookup"><span data-stu-id="1e002-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="1e002-149">Legg til en overskrift i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="1e002-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="1e002-150">Legg til en butikkvelgermodul i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="1e002-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="1e002-151">Lagre fragmentet, fullfør redigeringen av det, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="1e002-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="1e002-152">Opprett en mal som heter **Handlekurvmal**, og legg til handlekurvfragmentet som du nettopp opprettet, i det.</span><span class="sxs-lookup"><span data-stu-id="1e002-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="1e002-153">Lagre malen, fullfør redigeringen av den, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="1e002-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="1e002-154">Opprett en side som bruker den nye malen.</span><span class="sxs-lookup"><span data-stu-id="1e002-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="1e002-155">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="1e002-155">Save and preview the page.</span></span>
1. <span data-ttu-id="1e002-156">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="1e002-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e002-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1e002-157">Additional resources</span></span>

[<span data-ttu-id="1e002-158">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="1e002-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1e002-159">Containermodul</span><span class="sxs-lookup"><span data-stu-id="1e002-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1e002-160">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="1e002-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1e002-161">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="1e002-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1e002-162">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="1e002-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1e002-163">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="1e002-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1e002-164">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="1e002-164">Footer module</span></span>](author-footer-module.md)
