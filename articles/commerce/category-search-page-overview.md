---
title: Oversikt over standard kategorimålside og søkeresultatside
description: Dette emnet gir en oversik over standard kategorimålside og søkeresultatside i Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414610"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="a5a1b-103">Oversikt over standard kategorimålside og søkeresultatside</span><span class="sxs-lookup"><span data-stu-id="a5a1b-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5a1b-104">Dette emnet gir en oversik over standard kategorimålside og søkeresultatside i Microsoft Dynamics 365 Commerce e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="a5a1b-105">Standard kategorimålside</span><span class="sxs-lookup"><span data-stu-id="a5a1b-105">Default category landing page</span></span>

<span data-ttu-id="a5a1b-106">Standard kategorimålside er siden som brukere av webområder vanligvis kommer til når de velger en kategori i navigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="a5a1b-107">Kategorisiden lar deg bla gjennom, og du kan også sortere og presisere de kategoriserte produktene.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Standard kategorimålside](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="a5a1b-109">Øverst på siden er det en topptekst som viser alle produktkategoriene og andre sider som varehandelslederen har kategorisert.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="a5a1b-110">Konfigurasjon utføres som en del av konfigurasjonen av kanalnavigeringshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="a5a1b-111">På bunnen av siden er det en bunntekst som inneholder hurtigkoblinger til ulike emner som en kunde kan være interessert i.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="a5a1b-112">Følgende komponenter er grunnleggende for en kategori:</span><span class="sxs-lookup"><span data-stu-id="a5a1b-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="a5a1b-113">**Produktplasseringsfliser** viser produktene som varehandelslederen har definert i en kategori som en del av konfigurasjonen av navigasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="a5a1b-114">**Sammendrag av presiseringer og valg** er filtre som angir antall, og som kan brukes til å finjustere varer.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="a5a1b-115">Varehandelslederen konfigurerer dem som en del av konfigurasjonen av metadataene som er relatert til kanalkategorier og produktattributter.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="a5a1b-116">**Sorteringsalternativer** brukes av besøkende på webområder til å sortere produktene.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="a5a1b-117">Som standard er følgende sorteringsalternativer tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="a5a1b-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="a5a1b-118">Pris: – lav til høy</span><span class="sxs-lookup"><span data-stu-id="a5a1b-118">Price – low to high</span></span>
    - <span data-ttu-id="a5a1b-119">Pris: – høy til lav</span><span class="sxs-lookup"><span data-stu-id="a5a1b-119">Price – high to low</span></span>
    - <span data-ttu-id="a5a1b-120">Produktnavn – \[A–Å\]</span><span class="sxs-lookup"><span data-stu-id="a5a1b-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="a5a1b-121">Produktnavn – – \[Å–A\]</span><span class="sxs-lookup"><span data-stu-id="a5a1b-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="a5a1b-122">Vurderinger – lav til høy</span><span class="sxs-lookup"><span data-stu-id="a5a1b-122">Ratings – low to high</span></span>
    - <span data-ttu-id="a5a1b-123">Vurderinger – høy til lav</span><span class="sxs-lookup"><span data-stu-id="a5a1b-123">Ratings – high to low</span></span>

- <span data-ttu-id="a5a1b-124">**Sidenummerering** lar besøkende på webområdet flytte fra én side med kategoriserte produktresultater til en annen side.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="a5a1b-125">**Totalt antall** inneholder totalt antall produkter som er definert i en kategori.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="a5a1b-126">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="a5a1b-126">Enrich a category landing page</span></span>

<span data-ttu-id="a5a1b-127">Hvis du vil at en kategorimålside skal ha en mer skreddersydd opplevelse for en bestemt kategori, kan du "supplere" kategorimålsiden for denne kategorien.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="a5a1b-128">Du kan for eksempel legge til en markedsføringsvideo og enkelte kategoribeskrivelser for å få en kundes oppmerksomhet.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="a5a1b-129">Hvis du vil ha mer informasjon, se [Supplere en kategorimålside](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="a5a1b-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Supplere kategorimålside](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="a5a1b-131">Automatisk foreslå og søke på resultatsider</span><span class="sxs-lookup"><span data-stu-id="a5a1b-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="a5a1b-132">Brukere av webområder kan utforske et område enten ved å gå til en kategori fra navigasjonshierarkiet eller ved å skrive inn et søkeord i søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="a5a1b-133">Så snart brukerne begynner å skrive inn søkefeltet, får de oppleve den dyptgående funksjonaliteten for automatiske foreslag som foreslår søkeord.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="a5a1b-134">Her er noen av forslagstypene som kan vises:</span><span class="sxs-lookup"><span data-stu-id="a5a1b-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="a5a1b-135">**Nøkkelord** brukes til å finne frem til varer på tvers av alle produkter som er assortert til kanalen.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="a5a1b-136">**Produkter** gir deg direkte koblinger til siden for produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="a5a1b-137">**Søkeforslag for kategoriområde** viser ulike kategorier og lar brukere søke etter nøkkelordet i en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Dyptgående automatiske forslag](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="a5a1b-139">Når brukere velger et av nøkkelordene eller kategorisøkforslag for område, eller når det ikke er forslag til søkeordet de legger inn, omdirigeres de til en søkeresultatside.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="a5a1b-140">Brukerne kan deretter bla gjennom, sortere og begrense listen over søkeresultater for å finne ønsket element.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Søkemålside](./media/SearchLanding.png)

<span data-ttu-id="a5a1b-142">Følgende komponenter er grunnleggende for en søkeresultatside:</span><span class="sxs-lookup"><span data-stu-id="a5a1b-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="a5a1b-143">**Produktplasseringsfliser** viser produktene for brukerens søk.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="a5a1b-144">Som standard er disse flisene sortert etter skydrevet søkerelevanssum for brukersøket.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="a5a1b-145">**Sammendrag av presiseringer og valg** er filtre som angir antall, og som kan brukes til å finjustere varer.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="a5a1b-146">Varehandelslederen konfigurerer dem som en del av konfigurasjonen av metadataene for "kanalkategorier og produktattributter".</span><span class="sxs-lookup"><span data-stu-id="a5a1b-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="a5a1b-147">**Sorteringsalternativer** brukes av besøkende på webområder til å sortere produktene.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="a5a1b-148">Som standard er følgende sorteringsalternativer tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="a5a1b-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="a5a1b-149">Pris: – lav til høy</span><span class="sxs-lookup"><span data-stu-id="a5a1b-149">Price – low to high</span></span>
    - <span data-ttu-id="a5a1b-150">Pris: – høy til lav</span><span class="sxs-lookup"><span data-stu-id="a5a1b-150">Price – high to low</span></span>
    - <span data-ttu-id="a5a1b-151">Produktnavn – \[A–Å\]</span><span class="sxs-lookup"><span data-stu-id="a5a1b-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="a5a1b-152">Produktnavn – – \[Å–A\]</span><span class="sxs-lookup"><span data-stu-id="a5a1b-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="a5a1b-153">Vurderinger – lav til høy</span><span class="sxs-lookup"><span data-stu-id="a5a1b-153">Ratings – low to high</span></span>
    - <span data-ttu-id="a5a1b-154">Vurderinger – høy til lav</span><span class="sxs-lookup"><span data-stu-id="a5a1b-154">Ratings – high to low</span></span>
    - <span data-ttu-id="a5a1b-155">Standard</span><span class="sxs-lookup"><span data-stu-id="a5a1b-155">Default</span></span>

- <span data-ttu-id="a5a1b-156">**Sidenummerering** lar besøkende på webområdet flytte fra én side med kategoriserte produktresultater til en annen side.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="a5a1b-157">**Totalt antall** inneholder totalt antall produkter som er definert i en kategori, og som samsvarer med søkevilkårene.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="a5a1b-158">Disse skydrevne søkefunksjonene er tilgjengelige fra versjon 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="a5a1b-159">Kontroller at det under **Handelsparametere > Konfigurasjonsparametere** finnes en oppføring for ProductSearch. UseAzureSearch satt til true.</span><span class="sxs-lookup"><span data-stu-id="a5a1b-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="a5a1b-160">![Konfigurasjonsparametere for skydrevet søk](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="a5a1b-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5a1b-161">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a5a1b-161">Additional resources</span></span>

[<span data-ttu-id="a5a1b-162">Oversikt over skybaserte søk</span><span class="sxs-lookup"><span data-stu-id="a5a1b-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="a5a1b-163">Oversikt over startside</span><span class="sxs-lookup"><span data-stu-id="a5a1b-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="a5a1b-164">Oversikt over produktdetaljsider</span><span class="sxs-lookup"><span data-stu-id="a5a1b-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="a5a1b-165">Oversikt over sider for handlekurv og kasse</span><span class="sxs-lookup"><span data-stu-id="a5a1b-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="a5a1b-166">Oversikt over kontobehandlingssider</span><span class="sxs-lookup"><span data-stu-id="a5a1b-166">Account management pages overview</span></span>](quick-tour-account-management.md)

