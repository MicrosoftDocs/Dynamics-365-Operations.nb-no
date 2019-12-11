---
title: Oversikt over produktdetaljsider
description: Dette emnet gir en oversikt over produktdetaljsider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697871"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="fd111-103">Oversikt over produktdetaljsider</span><span class="sxs-lookup"><span data-stu-id="fd111-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fd111-104">Dette emnet gir en oversikt over produktdetaljsider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd111-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd111-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="fd111-105">Overview</span></span>

<span data-ttu-id="fd111-106">En PDP gir detaljert informasjon om et produkt og lar kundene velge produktalternativer, for eksempel størrelse, stil og farge.</span><span class="sxs-lookup"><span data-stu-id="fd111-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="fd111-107">En PDP bør vise all produktinformasjonen som en kunde må ha for å ta en kjøpsbeslutning.</span><span class="sxs-lookup"><span data-stu-id="fd111-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="fd111-108">Illustrasjonen nedenfor viser et eksempel på en PDP.</span><span class="sxs-lookup"><span data-stu-id="fd111-108">The following illustration shows an example of a PDP.</span></span>

![Eksempel på en produktdetaljside](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="fd111-110">Moduler for topptekst og bunntekst</span><span class="sxs-lookup"><span data-stu-id="fd111-110">Header and footer modules</span></span>

<span data-ttu-id="fd111-111">Toppen av en PDP har en topptekst som viser alle produktkategoriene og andre sider som forhandleren vil at kunder skal bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="fd111-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="fd111-112">Bunnen på siden har en bunntekst som inneholder hurtigkoblinger til ulike emner som kan være av interesser for kunder.</span><span class="sxs-lookup"><span data-stu-id="fd111-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="fd111-113">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="fd111-113">Buy box module</span></span>

<span data-ttu-id="fd111-114">Den viktigste modulen på en PDP er kjøpsboksmodulen.</span><span class="sxs-lookup"><span data-stu-id="fd111-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="fd111-115">Det er derfor det første elementet i hoveddelen av siden.</span><span class="sxs-lookup"><span data-stu-id="fd111-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="fd111-116">En kjøpsboksmodul er en containermodul som er vert for flere moduler som inneholder den viktigste informasjonen om produktet.</span><span class="sxs-lookup"><span data-stu-id="fd111-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="fd111-117">Denne informasjonen inkluderer produktnavnet, produktbildene, beskrivelsen, prisen og produktvurderingene.</span><span class="sxs-lookup"><span data-stu-id="fd111-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="fd111-118">Modulen for kjøpsboks lar kunden velge produktalternativer (for eksempel størrelse, stil og farge) og legger til produktet i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="fd111-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="fd111-119">Den gjør også det mulig for kunden å kjøpe produktet på Internett og hente det i en butikk.</span><span class="sxs-lookup"><span data-stu-id="fd111-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="fd111-120">Modulen for kjøp på Internett og henting i butikk bruker integrasjon med Bing-kart-API til å finne nærliggende butikker eller butikker i en annen lokasjon som kunden angir.</span><span class="sxs-lookup"><span data-stu-id="fd111-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="fd111-121">En kjøpsboksmodul krever en produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="fd111-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="fd111-122">Denne IDen er avledet fra sidekonteksten.</span><span class="sxs-lookup"><span data-stu-id="fd111-122">This ID is derived from the page context.</span></span> <span data-ttu-id="fd111-123">Hvis en kjøpsboksmodul legges til en side der sidekonteksten ikke inneholder en produkt-ID, gjengis ikke informasjonen riktig.</span><span class="sxs-lookup"><span data-stu-id="fd111-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="fd111-124">Produktspesifikasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="fd111-124">Product specifications module</span></span>

<span data-ttu-id="fd111-125">Modulen for produktspesifikasjoner kan brukes til å vise flere detaljer om produktet.</span><span class="sxs-lookup"><span data-stu-id="fd111-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="fd111-126">Disse detaljene hentes fra produktattributter i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="fd111-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="fd111-127">Modulen for produktspesifikasjoner viser alle attributter der **visible** -egenskapen er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="fd111-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="fd111-128">Det krever en produkt-ID for å hente produktattributter.</span><span class="sxs-lookup"><span data-stu-id="fd111-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="fd111-129">Anbefalingsmodul</span><span class="sxs-lookup"><span data-stu-id="fd111-129">Recommendations module</span></span>

<span data-ttu-id="fd111-130">Anbefalingsmodulen er en viktig modul på en PDP.</span><span class="sxs-lookup"><span data-stu-id="fd111-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="fd111-131">Mens kunder søker etter produkter skal flere produktalternativer presenteres for dem, slik at de kan finne det riktige produktet og foreta et kjøp.</span><span class="sxs-lookup"><span data-stu-id="fd111-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="fd111-132">Anbefalinger hjelper kundene å finne relatert innhold på en enkel måte og fortsette å handle.</span><span class="sxs-lookup"><span data-stu-id="fd111-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="fd111-133">Ulike typer anbefalingslister er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="fd111-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="fd111-134">Listen **Folk liker også** er basert på maskinopplæring.</span><span class="sxs-lookup"><span data-stu-id="fd111-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="fd111-135">Den bruker transaksjonsloggen for andre kunder til å gi anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="fd111-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="fd111-136">Denne listen er generert av anbefalingstjenesten og ligner på listene "Kunder som har kjøpt denne varen, kjøpte også...".</span><span class="sxs-lookup"><span data-stu-id="fd111-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="fd111-137">Det kreves en produkt-ID for å generere denne listen.</span><span class="sxs-lookup"><span data-stu-id="fd111-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="fd111-138">En **beslektet**-liste kan konfigureres for et produkt i Retail.</span><span class="sxs-lookup"><span data-stu-id="fd111-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="fd111-139">For en brun reiseveske kan for eksempel flere reisevesker av skinn eller som er utformet for reiseformål, konfigureres for den tilknyttede listen.</span><span class="sxs-lookup"><span data-stu-id="fd111-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="fd111-140">Andre typer relaterte lister, for eksempel **Tilbehør** og **Mer som dette**, kan også konfigureres i Retail.</span><span class="sxs-lookup"><span data-stu-id="fd111-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="fd111-141">Det kreves en produkt-ID for å generere denne listen.</span><span class="sxs-lookup"><span data-stu-id="fd111-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="fd111-142">Hvis den legges til på en startside, der sidekonteksten ikke inneholder en produkt-ID, vil listen derfor være tom.</span><span class="sxs-lookup"><span data-stu-id="fd111-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="fd111-143">Algoritmisk genererte anbefalingslister, for eksempel **Stjerneskudd**, **Bestselgere** og **Ny**, kan brukes på PDPer.</span><span class="sxs-lookup"><span data-stu-id="fd111-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="fd111-144">Selv om disse listene ikke er direkte relatert til produktet på PDP, er de en annen måte å finne produkter på som kan ha interesse for kundene.</span><span class="sxs-lookup"><span data-stu-id="fd111-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="fd111-145">Denne typen lister krever ikke en produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="fd111-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="fd111-146">De er generiske lister som genereres basert på handlemønstre på tvers av området.</span><span class="sxs-lookup"><span data-stu-id="fd111-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="fd111-147">Redaksjonelle lister er manuelt kuraterte lister.</span><span class="sxs-lookup"><span data-stu-id="fd111-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="fd111-148">En forhandler kan for eksempel bestemme deg for å kuratere lister over produkter som vedkommende vil vise.</span><span class="sxs-lookup"><span data-stu-id="fd111-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="fd111-149">Vurderings- og omtalemodul</span><span class="sxs-lookup"><span data-stu-id="fd111-149">Ratings and reviews module</span></span>

<span data-ttu-id="fd111-150">Modulen for vurderinger og omtaler viser vurderinger og omtaler som er levert av andre kunder.</span><span class="sxs-lookup"><span data-stu-id="fd111-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="fd111-151">Den gjør også det mulig for en kunde å skrive sine egne gjennomganger av produktet.</span><span class="sxs-lookup"><span data-stu-id="fd111-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="fd111-152">I tillegg inneholder den et histogram som viser vurderingstrenden for produktet.</span><span class="sxs-lookup"><span data-stu-id="fd111-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="fd111-153">Hvis du vil ha mer informasjon, se [Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fd111-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="fd111-154">Markedsføringsmoduler</span><span class="sxs-lookup"><span data-stu-id="fd111-154">Marketing modules</span></span>

<span data-ttu-id="fd111-155">Hvis markedsføringsinnhold er unikt for et bestemt produkt, kan hvilke som helst markedsføringsmoduler legges til i PDP.</span><span class="sxs-lookup"><span data-stu-id="fd111-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="fd111-156">Du kan legge til markedsføringsmoduler i en PDP ved å "supplere" siden.</span><span class="sxs-lookup"><span data-stu-id="fd111-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="fd111-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fd111-157">Additional resources</span></span>

[<span data-ttu-id="fd111-158">Oversikt over startsiden</span><span class="sxs-lookup"><span data-stu-id="fd111-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="fd111-159">Oversikt over standard kategorimålside og søkeresultatside</span><span class="sxs-lookup"><span data-stu-id="fd111-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="fd111-160">Oversikt over sider for handlekurv og kasse</span><span class="sxs-lookup"><span data-stu-id="fd111-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="fd111-161">Oversikt over kontobehandlingssider</span><span class="sxs-lookup"><span data-stu-id="fd111-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
