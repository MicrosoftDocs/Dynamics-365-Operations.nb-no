---
title: Oversikt over produktanbefalinger
description: Dette emnet inneholder generell informasjon om produktanbefalinger. Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, og til og med produkter de ikke opprinnelig hadde tenkt å kjøpe.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1b01589322c26b6a7b69d1b992b03603f5f3d29a
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404354"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="80795-104">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="80795-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80795-105">Microsoft Dynamics 365 Commerce kan brukes til å vise produktanbefalinger på webområdet for e-handel og salgsstedsenheten.</span><span class="sxs-lookup"><span data-stu-id="80795-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="80795-106">Produktanbefalinger er varer som en kunde kan være interessert i.</span><span class="sxs-lookup"><span data-stu-id="80795-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="80795-107">Anbefalingene er basert på kjøpstendensene for andre kunder i nettbutikker og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="80795-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="80795-108">Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, samtidig som de får en god handleopplevelse.</span><span class="sxs-lookup"><span data-stu-id="80795-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="80795-109">Krysssalg og ettersalg kan til og med brukes til å hjelpe kunder med å finne flere produkter enn de opprinnelig hadde til hensikt å kjøpe.</span><span class="sxs-lookup"><span data-stu-id="80795-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="80795-110">Når anbefalinger brukes til å hjelpe med produktoppdaging, kan de opprette flere konverteringsmuligheter, øke salgsinntektene og til og med bidra til å forbedre kundetilfredsheten og -loyaliteten.</span><span class="sxs-lookup"><span data-stu-id="80795-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="80795-111">I e-handel er produktanbefalinger basert på Microsofts anbefalinger fra teknologi for maskinlæring i stor skala.</span><span class="sxs-lookup"><span data-stu-id="80795-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="80795-112">Anbefalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="80795-112">Recommendation service</span></span>

<span data-ttu-id="80795-113">Produktanbefalingstjenesten benytter kunstig intelligens og maskinopplæring (AI-ML)-teknologier på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="80795-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="80795-114">Data i formatet som anbefalingstjenesten krever, trekkes ut fra den operative Commerce-databasen og sendes til Azure Data Lake Storage eller enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="80795-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="80795-115">Anbefalingstjenesten bruker de lagrede dataene til å lære opp anbefalingsmodeller for listene **Folk liker også**, **Ofte kjøpt sammen**, **Nye**, **Bestselgere** og **Tendenser**.</span><span class="sxs-lookup"><span data-stu-id="80795-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="80795-116">Scenarier</span><span class="sxs-lookup"><span data-stu-id="80795-116">Scenarios</span></span>

<span data-ttu-id="80795-117">Produktanbefalingene er tilgjengelige for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="80795-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="80795-118">**På en hvilken som helst butikkside for weblesing eller startside i e-handel**: Hvis kunder eller butikkmedarbeidere besøker en butikkside, kan anbefalingsmotoren foreslå produkter i listene **Nye**, **Bestselgere** og **Tendenser**.</span><span class="sxs-lookup"><span data-stu-id="80795-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="80795-119">**På Produktdetaljer-siden:** Hvis kunder eller butikkmedarbeidere besøker en **Produktdetaljer**-side, foreslår anbefalingsmotoren ekstra varer som også sannsynligvis blir kjøpt.</span><span class="sxs-lookup"><span data-stu-id="80795-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="80795-120">Disse elementene vises i listen **Folk liker også**.</span><span class="sxs-lookup"><span data-stu-id="80795-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="80795-121">**På transaksjonssiden eller utsjekkingssiden:** Anbefalingsmotoren foreslår varer basert på hele listen med elementer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="80795-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="80795-122">Disse varene vises i listen **Ofte kjøpt sammen**.</span><span class="sxs-lookup"><span data-stu-id="80795-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="80795-123">**Tilpassede anbefalinger:** Forhandlere kan tilby påloggede kunder en tilpasset **Plukkinger for deg**-liste i tillegg til ny funksjonalitet som tillater tilpassing av eksisterende listescenarioer basert på den aktuelle kunden.</span><span class="sxs-lookup"><span data-stu-id="80795-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="80795-124">Hvis du vil finne ut mer, kan du se [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="80795-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="80795-125">Typer produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="80795-125">Types of product recommendations</span></span>

<span data-ttu-id="80795-126">Følgende tabell beskriver ulike typer automatiserte produktanbefalinger som er tilgjengelige for forhandlere som skal implementeres i Dynamics 365 Commerce-løsningen via [produktsamlingsmodulen](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="80795-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="80795-127">Forhandlere kan også vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="80795-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="80795-128">Produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="80795-128">Product collection module</span></span>  | <span data-ttu-id="80795-129">Type</span><span class="sxs-lookup"><span data-stu-id="80795-129">Type</span></span> | <span data-ttu-id="80795-130">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="80795-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="80795-131">Nye</span><span class="sxs-lookup"><span data-stu-id="80795-131">New</span></span>                        | <span data-ttu-id="80795-132">Algoritme</span><span class="sxs-lookup"><span data-stu-id="80795-132">Algorithmic</span></span> | <span data-ttu-id="80795-133">Denne modulen viser en liste over de nyeste produktene som nylig er assortert til kanaler og kataloger.</span><span class="sxs-lookup"><span data-stu-id="80795-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="80795-134">Bestselgere</span><span class="sxs-lookup"><span data-stu-id="80795-134">Best selling</span></span>               | <span data-ttu-id="80795-135">Algoritme</span><span class="sxs-lookup"><span data-stu-id="80795-135">Algorithmic</span></span> | <span data-ttu-id="80795-136">Denne modulen viser en liste over produkter som er rangert etter det høyeste salgstallet.</span><span class="sxs-lookup"><span data-stu-id="80795-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="80795-137">Populære</span><span class="sxs-lookup"><span data-stu-id="80795-137">Trending</span></span>                   | <span data-ttu-id="80795-138">Algoritme</span><span class="sxs-lookup"><span data-stu-id="80795-138">Algorithmic</span></span> | <span data-ttu-id="80795-139">Denne modulen viser en oversikt over produkter med høyest ytelse for en gitt periode, rangert etter det høyeste salgstallet.</span><span class="sxs-lookup"><span data-stu-id="80795-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="80795-140">Kjøpes ofte sammen</span><span class="sxs-lookup"><span data-stu-id="80795-140">Frequently bought together</span></span> | <span data-ttu-id="80795-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="80795-141">AI-ML</span></span> | <span data-ttu-id="80795-142">Denne modulen anbefaler en liste over produkter som vanligvis kjøpes sammen med innholdet fra forbrukeres gjeldende handlevogn.</span><span class="sxs-lookup"><span data-stu-id="80795-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="80795-143">Andre liker også</span><span class="sxs-lookup"><span data-stu-id="80795-143">People also like</span></span>           | <span data-ttu-id="80795-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="80795-144">AI-ML</span></span> | <span data-ttu-id="80795-145">Denne modulen anbefaler produkter for et angitt seed-produkt, basert på forbrukskjøpsmønstre.</span><span class="sxs-lookup"><span data-stu-id="80795-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="80795-146">Plukkinger for deg</span><span class="sxs-lookup"><span data-stu-id="80795-146">Picks for you</span></span>              | <span data-ttu-id="80795-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="80795-147">AI-ML</span></span> | <span data-ttu-id="80795-148">Denne modulen anbefaler en personlig liste over produkter basert på kjøpsmønstre til den påloggede brukeren.</span><span class="sxs-lookup"><span data-stu-id="80795-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="80795-149">For en gjestebruker vil denne listen være skjult.</span><span class="sxs-lookup"><span data-stu-id="80795-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="80795-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="80795-150">Additional resources</span></span>

[<span data-ttu-id="80795-151">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="80795-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="80795-152">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="80795-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="80795-153">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="80795-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="80795-154">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="80795-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="80795-155">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="80795-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="80795-156">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="80795-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="80795-157">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="80795-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="80795-158">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="80795-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="80795-159">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="80795-159">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="80795-160">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="80795-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
