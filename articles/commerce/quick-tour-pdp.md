---
title: Oversikt over produktdetaljsider
description: Dette emnet gir en oversikt over produktdetaljsider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414749"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="0f45a-103">Oversikt over produktdetaljsider</span><span class="sxs-lookup"><span data-stu-id="0f45a-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f45a-104">Dette emnet gir en oversikt over produktdetaljsider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f45a-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0f45a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0f45a-105">Overview</span></span>

<span data-ttu-id="0f45a-106">En PDP gir detaljert informasjon om et produkt og lar kundene velge produktalternativer, for eksempel størrelse, stil og farge.</span><span class="sxs-lookup"><span data-stu-id="0f45a-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="0f45a-107">En PDP bør vise all produktinformasjonen som en kunde må ha for å ta en kjøpsbeslutning.</span><span class="sxs-lookup"><span data-stu-id="0f45a-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="0f45a-108">Illustrasjonen nedenfor viser et eksempel på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0f45a-108">The following illustration shows an example of a PDP.</span></span>

![Eksempel på en produktdetaljside](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="0f45a-110">Moduler for topptekst og bunntekst</span><span class="sxs-lookup"><span data-stu-id="0f45a-110">Header and footer modules</span></span>

<span data-ttu-id="0f45a-111">Toppen av en PDP har en topptekst som viser alle produktkategoriene og andre sider som forhandleren vil at kunder skal bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="0f45a-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="0f45a-112">Bunnen på siden har en bunntekst som inneholder hurtigkoblinger til ulike emner som kan være av interesser for kunder.</span><span class="sxs-lookup"><span data-stu-id="0f45a-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="0f45a-113">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="0f45a-113">Buy box module</span></span>

<span data-ttu-id="0f45a-114">Den viktigste modulen på en PDP er kjøpsboksmodulen, som vises som første element i hoveddelen på siden.</span><span class="sxs-lookup"><span data-stu-id="0f45a-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="0f45a-115">En kjøpsboksmodul viser viktig produktinformasjon, for eksempel produktnavnet, produktbeskrivelsen, produktprisen, produktbilder og produktklassifiseringer.</span><span class="sxs-lookup"><span data-stu-id="0f45a-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="0f45a-116">Modulen for kjøpsboks lar kunden velge produktalternativer (for eksempel størrelse, stil og farge) og legger til produktet i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="0f45a-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="0f45a-117">Den gjør også det mulig for kunden å kjøpe produktet på Internett og hente det i en butikk.</span><span class="sxs-lookup"><span data-stu-id="0f45a-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="0f45a-118">Modulen for kjøp på Internett og henting i butikk bruker integrasjon med Bing-kart-API til å finne nærliggende butikker eller butikker i en annen lokasjon som kunden angir.</span><span class="sxs-lookup"><span data-stu-id="0f45a-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="0f45a-119">En kjøpsboksmodul krever en produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="0f45a-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="0f45a-120">Denne IDen er avledet fra sidekonteksten.</span><span class="sxs-lookup"><span data-stu-id="0f45a-120">This ID is derived from the page context.</span></span> <span data-ttu-id="0f45a-121">Hvis en kjøpsboksmodul legges til en side der sidekonteksten ikke inneholder en produkt-ID, gjengis ikke informasjonen riktig.</span><span class="sxs-lookup"><span data-stu-id="0f45a-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="0f45a-122">Produktspesifikasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="0f45a-122">Product specifications module</span></span>

<span data-ttu-id="0f45a-123">Modulen for produktspesifikasjoner kan brukes til å vise flere detaljer om produktet.</span><span class="sxs-lookup"><span data-stu-id="0f45a-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="0f45a-124">Disse detaljene hentes fra produktattributter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f45a-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="0f45a-125">Modulen for produktspesifikasjoner viser alle attributter der **visible** -egenskapen er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="0f45a-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="0f45a-126">Det krever en produkt-ID for å hente produktattributter.</span><span class="sxs-lookup"><span data-stu-id="0f45a-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="0f45a-127">Anbefalingsmodul</span><span class="sxs-lookup"><span data-stu-id="0f45a-127">Recommendations module</span></span>

<span data-ttu-id="0f45a-128">Anbefalingsmodulen er en viktig modul på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0f45a-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="0f45a-129">Mens kunder søker etter produkter skal flere produktalternativer presenteres for dem, slik at de kan finne det riktige produktet og foreta et kjøp.</span><span class="sxs-lookup"><span data-stu-id="0f45a-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="0f45a-130">Anbefalinger hjelper kundene å finne relatert innhold på en enkel måte og fortsette å handle.</span><span class="sxs-lookup"><span data-stu-id="0f45a-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="0f45a-131">Ulike typer anbefalingslister er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="0f45a-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="0f45a-132">Listen **Folk liker også** er basert på maskinopplæring.</span><span class="sxs-lookup"><span data-stu-id="0f45a-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="0f45a-133">Den bruker transaksjonsloggen for andre kunder til å gi anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="0f45a-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="0f45a-134">Denne listen er generert av anbefalingstjenesten og ligner på listene "Kunder som har kjøpt denne varen, kjøpte også...".</span><span class="sxs-lookup"><span data-stu-id="0f45a-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="0f45a-135">Det kreves en produkt-ID for å generere denne listen.</span><span class="sxs-lookup"><span data-stu-id="0f45a-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="0f45a-136">En **beslektet**-liste kan konfigureres for et produkt i Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f45a-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="0f45a-137">For en brun reiseveske kan for eksempel flere reisevesker av skinn eller som er utformet for reiseformål, konfigureres for den tilknyttede listen.</span><span class="sxs-lookup"><span data-stu-id="0f45a-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="0f45a-138">Andre typer relaterte lister, for eksempel **Tilbehør** og **Mer som dette**, kan også konfigureres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f45a-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="0f45a-139">Det kreves en produkt-ID for å generere denne listen.</span><span class="sxs-lookup"><span data-stu-id="0f45a-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="0f45a-140">Hvis den legges til på en startside, der sidekonteksten ikke inneholder en produkt-ID, vil listen derfor være tom.</span><span class="sxs-lookup"><span data-stu-id="0f45a-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="0f45a-141">Algoritmisk genererte anbefalingslister, for eksempel **Stjerneskudd**, **Bestselgere** og **Ny**, kan brukes på PDPer.</span><span class="sxs-lookup"><span data-stu-id="0f45a-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="0f45a-142">Selv om disse listene ikke er direkte relatert til produktet på PDP, er de en annen måte å finne produkter på som kan ha interesse for kundene.</span><span class="sxs-lookup"><span data-stu-id="0f45a-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="0f45a-143">Denne typen lister krever ikke en produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="0f45a-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="0f45a-144">De er generiske lister som genereres basert på handlemønstre på tvers av området.</span><span class="sxs-lookup"><span data-stu-id="0f45a-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="0f45a-145">Redaksjonelle lister er manuelt kuraterte lister.</span><span class="sxs-lookup"><span data-stu-id="0f45a-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="0f45a-146">En forhandler kan for eksempel bestemme deg for å kuratere lister over produkter som vedkommende vil vise.</span><span class="sxs-lookup"><span data-stu-id="0f45a-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="0f45a-147">Vurderings- og omtalemoduler</span><span class="sxs-lookup"><span data-stu-id="0f45a-147">Ratings and reviews modules</span></span>

<span data-ttu-id="0f45a-148">Tre moduler kan brukes til å vise og legge til omtaler:</span><span class="sxs-lookup"><span data-stu-id="0f45a-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="0f45a-149">**Omtaler** – Denne modulen viser vurderinger og omtaler som er levert av andre kunder.</span><span class="sxs-lookup"><span data-stu-id="0f45a-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="0f45a-150">Kunder kan sortere og filtrere omtalene.</span><span class="sxs-lookup"><span data-stu-id="0f45a-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="0f45a-151">I denne modulen kan kunder også like eller mislike omtaler og rapportere problemer.</span><span class="sxs-lookup"><span data-stu-id="0f45a-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="0f45a-152">**Skriv omtale** – I denne modulen kan kundene skrive sine egne omtaler av et produkt.</span><span class="sxs-lookup"><span data-stu-id="0f45a-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="0f45a-153">**Vurderingshistogram** – Denne modulen inneholder et histogram som viser vurderingstendensen for et produkt.</span><span class="sxs-lookup"><span data-stu-id="0f45a-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="0f45a-154">Hvis du vil ha mer informasjon, se [Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f45a-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="0f45a-155">Markedsføringsmoduler</span><span class="sxs-lookup"><span data-stu-id="0f45a-155">Marketing modules</span></span>

<span data-ttu-id="0f45a-156">Hvis markedsføringsinnhold er unikt for et bestemt produkt, kan hvilke som helst markedsføringsmoduler legges til i PDP.</span><span class="sxs-lookup"><span data-stu-id="0f45a-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="0f45a-157">Du kan legge til markedsføringsmoduler i en PDP ved å "supplere" siden.</span><span class="sxs-lookup"><span data-stu-id="0f45a-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="0f45a-158">Hvis du vil ha mer informasjon, kan du se [Supplere en produktside](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="0f45a-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f45a-159">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0f45a-159">Additional resources</span></span>

[<span data-ttu-id="0f45a-160">Oversikt over startside</span><span class="sxs-lookup"><span data-stu-id="0f45a-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="0f45a-161">Oversikt over sider for handlekurv og kasse</span><span class="sxs-lookup"><span data-stu-id="0f45a-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="0f45a-162">Oversikt over kontobehandlingssider</span><span class="sxs-lookup"><span data-stu-id="0f45a-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="0f45a-163">Supplere en produktdetaljside</span><span class="sxs-lookup"><span data-stu-id="0f45a-163">Enrich a product details page</span></span>](enrich-product-page.md)
