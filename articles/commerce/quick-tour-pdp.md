---
title: Oversikt over produktdetaljsider
description: Dette emnet gir en oversikt over produktdetaljsider (PDP-er) i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792225"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="3ff47-103">Oversikt over produktdetaljsider</span><span class="sxs-lookup"><span data-stu-id="3ff47-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ff47-104">Dette emnet gir en oversikt over produktdetaljsider (PDP-er) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3ff47-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3ff47-105">En PDP gir detaljert informasjon om et produkt og lar kundene velge produktalternativer, for eksempel størrelse, stil og farge.</span><span class="sxs-lookup"><span data-stu-id="3ff47-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="3ff47-106">En PDP bør vise all produktinformasjonen som en kunde må ha for å ta en kjøpsbeslutning.</span><span class="sxs-lookup"><span data-stu-id="3ff47-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="3ff47-107">Illustrasjonen nedenfor viser et eksempel på en PDP.</span><span class="sxs-lookup"><span data-stu-id="3ff47-107">The following illustration shows an example of a PDP.</span></span>

![Eksempel på en produktdetaljside](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="3ff47-109">Moduler for topptekst og bunntekst</span><span class="sxs-lookup"><span data-stu-id="3ff47-109">Header and footer modules</span></span>

<span data-ttu-id="3ff47-110">Toppen av en PDP har en topptekst som viser alle produktkategoriene og andre sider som forhandleren vil at kunder skal bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="3ff47-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="3ff47-111">Bunnen på siden har en bunntekst som inneholder hurtigkoblinger til ulike emner som kan være av interesser for kunder.</span><span class="sxs-lookup"><span data-stu-id="3ff47-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="3ff47-112">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="3ff47-112">Buy box module</span></span>

<span data-ttu-id="3ff47-113">Den viktigste modulen på en PDP er kjøpsboksmodulen, som vises som første element i hoveddelen på siden.</span><span class="sxs-lookup"><span data-stu-id="3ff47-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="3ff47-114">En kjøpsboksmodul viser viktig produktinformasjon, for eksempel produktnavnet, produktbeskrivelsen, produktprisen, produktbilder og produktklassifiseringer.</span><span class="sxs-lookup"><span data-stu-id="3ff47-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="3ff47-115">Modulen for kjøpsboks lar kunden velge produktalternativer (for eksempel størrelse, stil og farge) og legger til produktet i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="3ff47-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="3ff47-116">Den gjør også det mulig for kunden å kjøpe produktet på Internett og hente det i en butikk.</span><span class="sxs-lookup"><span data-stu-id="3ff47-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="3ff47-117">Modulen for kjøp på Internett og henting i butikk bruker integrasjon med Bing-kart-API til å finne nærliggende butikker eller butikker i en annen lokasjon som kunden angir.</span><span class="sxs-lookup"><span data-stu-id="3ff47-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="3ff47-118">En kjøpsboksmodul krever en produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="3ff47-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="3ff47-119">Denne IDen er avledet fra sidekonteksten.</span><span class="sxs-lookup"><span data-stu-id="3ff47-119">This ID is derived from the page context.</span></span> <span data-ttu-id="3ff47-120">Hvis en kjøpsboksmodul legges til en side der sidekonteksten ikke inneholder en produkt-ID, gjengis ikke informasjonen riktig.</span><span class="sxs-lookup"><span data-stu-id="3ff47-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="3ff47-121">Produktspesifikasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="3ff47-121">Product specifications module</span></span>

<span data-ttu-id="3ff47-122">Modulen for produktspesifikasjoner kan brukes til å vise flere detaljer om produktet.</span><span class="sxs-lookup"><span data-stu-id="3ff47-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="3ff47-123">Disse detaljene hentes fra produktattributter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="3ff47-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="3ff47-124">Modulen for produktspesifikasjoner viser alle attributter der **visible** -egenskapen er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="3ff47-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="3ff47-125">Det krever en produkt-ID for å hente produktattributter.</span><span class="sxs-lookup"><span data-stu-id="3ff47-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="3ff47-126">Anbefalingsmodul</span><span class="sxs-lookup"><span data-stu-id="3ff47-126">Recommendations module</span></span>

<span data-ttu-id="3ff47-127">Anbefalingsmodulen er en viktig modul på en PDP.</span><span class="sxs-lookup"><span data-stu-id="3ff47-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="3ff47-128">Mens kunder søker etter produkter skal flere produktalternativer presenteres for dem, slik at de kan finne det riktige produktet og foreta et kjøp.</span><span class="sxs-lookup"><span data-stu-id="3ff47-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="3ff47-129">Anbefalinger hjelper kundene å finne relatert innhold på en enkel måte og fortsette å handle.</span><span class="sxs-lookup"><span data-stu-id="3ff47-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="3ff47-130">Ulike typer anbefalingslister er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3ff47-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="3ff47-131">Listen **Folk liker også** er basert på maskinopplæring.</span><span class="sxs-lookup"><span data-stu-id="3ff47-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="3ff47-132">Den bruker transaksjonsloggen for andre kunder til å gi anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="3ff47-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="3ff47-133">Denne listen er generert av anbefalingstjenesten og ligner på listene "Kunder som har kjøpt denne varen, kjøpte også...".</span><span class="sxs-lookup"><span data-stu-id="3ff47-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="3ff47-134">Det kreves en produkt-ID for å generere denne listen.</span><span class="sxs-lookup"><span data-stu-id="3ff47-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="3ff47-135">En **beslektet**-liste kan konfigureres for et produkt i Commerce.</span><span class="sxs-lookup"><span data-stu-id="3ff47-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="3ff47-136">For en brun reiseveske kan for eksempel flere reisevesker av skinn eller som er utformet for reiseformål, konfigureres for den tilknyttede listen.</span><span class="sxs-lookup"><span data-stu-id="3ff47-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="3ff47-137">Andre typer relaterte lister, for eksempel **Tilbehør** og **Mer som dette**, kan også konfigureres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="3ff47-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="3ff47-138">Det kreves en produkt-ID for å generere denne listen.</span><span class="sxs-lookup"><span data-stu-id="3ff47-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="3ff47-139">Hvis den legges til på en startside, der sidekonteksten ikke inneholder en produkt-ID, vil listen derfor være tom.</span><span class="sxs-lookup"><span data-stu-id="3ff47-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="3ff47-140">Algoritmisk genererte anbefalingslister, for eksempel **Stjerneskudd**, **Bestselgere** og **Ny**, kan brukes på PDPer.</span><span class="sxs-lookup"><span data-stu-id="3ff47-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="3ff47-141">Selv om disse listene ikke er direkte relatert til produktet på PDP, er de en annen måte å finne produkter på som kan ha interesse for kundene.</span><span class="sxs-lookup"><span data-stu-id="3ff47-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="3ff47-142">Denne typen lister krever ikke en produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="3ff47-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="3ff47-143">De er generiske lister som genereres basert på handlemønstre på tvers av området.</span><span class="sxs-lookup"><span data-stu-id="3ff47-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="3ff47-144">Redaksjonelle lister er manuelt kuraterte lister.</span><span class="sxs-lookup"><span data-stu-id="3ff47-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="3ff47-145">En forhandler kan for eksempel bestemme deg for å kuratere lister over produkter som vedkommende vil vise.</span><span class="sxs-lookup"><span data-stu-id="3ff47-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="3ff47-146">Vurderings- og omtalemoduler</span><span class="sxs-lookup"><span data-stu-id="3ff47-146">Ratings and reviews modules</span></span>

<span data-ttu-id="3ff47-147">Tre moduler kan brukes til å vise og legge til omtaler:</span><span class="sxs-lookup"><span data-stu-id="3ff47-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="3ff47-148">**Omtaler** – Denne modulen viser vurderinger og omtaler som er levert av andre kunder.</span><span class="sxs-lookup"><span data-stu-id="3ff47-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="3ff47-149">Kunder kan sortere og filtrere omtalene.</span><span class="sxs-lookup"><span data-stu-id="3ff47-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="3ff47-150">I denne modulen kan kunder også like eller mislike omtaler og rapportere problemer.</span><span class="sxs-lookup"><span data-stu-id="3ff47-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="3ff47-151">**Skriv omtale** – I denne modulen kan kundene skrive sine egne omtaler av et produkt.</span><span class="sxs-lookup"><span data-stu-id="3ff47-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="3ff47-152">**Vurderingshistogram** – Denne modulen inneholder et histogram som viser vurderingstendensen for et produkt.</span><span class="sxs-lookup"><span data-stu-id="3ff47-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="3ff47-153">Hvis du vil ha mer informasjon, se [Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ff47-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="3ff47-154">Markedsføringsmoduler</span><span class="sxs-lookup"><span data-stu-id="3ff47-154">Marketing modules</span></span>

<span data-ttu-id="3ff47-155">Hvis markedsføringsinnhold er unikt for et bestemt produkt, kan hvilke som helst markedsføringsmoduler legges til i PDP.</span><span class="sxs-lookup"><span data-stu-id="3ff47-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="3ff47-156">Du kan legge til markedsføringsmoduler i en PDP ved å "supplere" siden.</span><span class="sxs-lookup"><span data-stu-id="3ff47-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="3ff47-157">Hvis du vil ha mer informasjon, kan du se [Supplere en produktside](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="3ff47-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ff47-158">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3ff47-158">Additional resources</span></span>

[<span data-ttu-id="3ff47-159">Oversikt over startside</span><span class="sxs-lookup"><span data-stu-id="3ff47-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="3ff47-160">Oversikt over sider for handlekurv og kasse</span><span class="sxs-lookup"><span data-stu-id="3ff47-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="3ff47-161">Oversikt over kontobehandlingssider</span><span class="sxs-lookup"><span data-stu-id="3ff47-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="3ff47-162">Supplere en produktdetaljside</span><span class="sxs-lookup"><span data-stu-id="3ff47-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
