---
title: Butikkvelgermodul
description: Dette emnet dekker butikkvelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378214"
---
# <a name="store-selector-module"></a><span data-ttu-id="2d2a4-103">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="2d2a4-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d2a4-104">Dette emnet dekker butikkvelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2d2a4-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="2d2a4-105">Overview</span></span>

<span data-ttu-id="2d2a4-106">En butikkvelgermodul brukes til kundescenarioet "Kjøpe på Internett og hente i butikk" (BOPIS).</span><span class="sxs-lookup"><span data-stu-id="2d2a4-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="2d2a4-107">Det viser en liste over butikker der et produkt er tilgjengelig for henting, i tillegg til butikkens åpningstimer og produktbeholdninger for hver butikk.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="2d2a4-108">Butikkvelgermodulen krever konteksten for et produkt og en søkeplassering for å finne butikker.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="2d2a4-109">Ved fravær av en søkeplassering, brukes som standard kundens leserplassering, forutsatt at kunden gir samtykke.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="2d2a4-110">Modulen har en inndataboks som gir kunden muligheten til å angi en lokasjon (postnummer, poststed og delstat) for å finne butikker som er i nærheten.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="2d2a4-111">Butikkvelgermodulen er integrert med API-en (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet for å konvertere lokasjonen til en breddegrad og lengdegrad.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="2d2a4-112">En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for Commerce i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2d2a4-113">Butikkvelgermodulen kan legges til en kjøpsboksmodul på produktdetaljsiden (PDP) for å vise butikkene der et produkt er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="2d2a4-114">Den kan også legges til i en handlekurvmodul.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-114">It can also be added to a cart module.</span></span> <span data-ttu-id="2d2a4-115">Når butikkvelgermodulen legges til i en handlekurvmodul, vises hentealternativer for hvert linjeelement for handlekurven.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="2d2a4-116">I tillegg kan denne modulen med egendefinert koding legges til andre sider eller moduler via utvidelser og tilpassinger.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="2d2a4-117">For at BOPIS-scenarioet skal fungere, bør produktene konfigureres med leveringsmodusen "kundehenting".</span><span class="sxs-lookup"><span data-stu-id="2d2a4-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="2d2a4-118">Ellers vil ikke modulen vises på de respektive sidene.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="2d2a4-119">Hvis du vil ha informasjon om hvordan du konfigurerer leveringsmodus, kan du se [Definer leveringsmåter](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="2d2a4-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="2d2a4-120">Bildet nedenfor viser et eksempel på en butikkvelgermodul som brukes på en PDP.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Eksempel på en butikkvelgermodul](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="2d2a4-122">Bruk av butikkvelgermodul i e-handel</span><span class="sxs-lookup"><span data-stu-id="2d2a4-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="2d2a4-123">En butikkvelgermodul kan brukes på en produktdetaljside (PDP) for å finne nærliggende butikker der et produkt er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="2d2a4-124">En butikkvelgermodul kan brukes på en handlekurvside for å finne nærliggende butikker der et produkt i handlekurven er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="2d2a4-125">Egenskaper for butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="2d2a4-125">Store selector module properties</span></span>

| <span data-ttu-id="2d2a4-126">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="2d2a4-126">Property name</span></span>             | <span data-ttu-id="2d2a4-127">Verdi</span><span class="sxs-lookup"><span data-stu-id="2d2a4-127">Value</span></span>                 | <span data-ttu-id="2d2a4-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2d2a4-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2d2a4-129">Søkeradius</span><span class="sxs-lookup"><span data-stu-id="2d2a4-129">Search radius</span></span> | <span data-ttu-id="2d2a4-130">Tall</span><span class="sxs-lookup"><span data-stu-id="2d2a4-130">Number</span></span> | <span data-ttu-id="2d2a4-131">Definerer søkeradius for butikkene, i mil.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="2d2a4-132">Hvis ingen verdi er angitt, brukes standard søkeradius på 50 engelske mil.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="2d2a4-133">Vilkår for bruk</span><span class="sxs-lookup"><span data-stu-id="2d2a4-133">Terms of Service</span></span> | <span data-ttu-id="2d2a4-134">URL</span><span class="sxs-lookup"><span data-stu-id="2d2a4-134">URL</span></span>    |  <span data-ttu-id="2d2a4-135">URL-adressen for vilkår for bruk kreves for Bing-kart-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="2d2a4-136">Legge til en butikkvelgermodul på en side</span><span class="sxs-lookup"><span data-stu-id="2d2a4-136">Add a store selector module to a page</span></span>

<span data-ttu-id="2d2a4-137">En butikkvelgermodul trenger konteksten til et produkt, og kan derfor bare brukes i kjøpsboks- og handlemoduler.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="2d2a4-138">Butikkvelgermoduler fungerer ikke utenfor disse modulene.</span><span class="sxs-lookup"><span data-stu-id="2d2a4-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="2d2a4-139">Hvis du vil ha informasjon om hvordan du legger til en butikkvelgermodul i en kjøpsboksmodul, kan du se [Kjøpsboksmodul](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="2d2a4-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="2d2a4-140">Hvis du vil ha informasjon om hvordan du legger til en butikkvelgermodul i en handlekurvmodul, kan du se [Handlekurvmodul](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="2d2a4-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d2a4-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2d2a4-141">Additional resources</span></span>

[<span data-ttu-id="2d2a4-142">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="2d2a4-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2d2a4-143">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="2d2a4-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2d2a4-144">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="2d2a4-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2d2a4-145">Hurtiginnføring i PDP</span><span class="sxs-lookup"><span data-stu-id="2d2a4-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="2d2a4-146">Hurtiginnføring i handlekurv og kasse</span><span class="sxs-lookup"><span data-stu-id="2d2a4-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="2d2a4-147">Definer leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="2d2a4-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="2d2a4-148">Behandle Bing-kart for organisasjonen</span><span class="sxs-lookup"><span data-stu-id="2d2a4-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
