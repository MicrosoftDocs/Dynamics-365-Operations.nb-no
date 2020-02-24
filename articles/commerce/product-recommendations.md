---
title: Oversikt over produktanbefalinger
description: Dette emnet inneholder generell informasjon om produktanbefalinger. Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, og til og med produkter de ikke opprinnelig hadde tenkt å kjøpe.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024985"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="f5f06-104">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="f5f06-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5f06-105">Microsoft Dynamics 365 Commerce kan brukes til å vise produktanbefalinger på webområdet for e-handel og salgsstedsenheten.</span><span class="sxs-lookup"><span data-stu-id="f5f06-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="f5f06-106">Produktanbefalinger er varer som en kunde kan være interessert i.</span><span class="sxs-lookup"><span data-stu-id="f5f06-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="f5f06-107">Anbefalingene er basert på kjøpstendensene for andre kunder i nettbutikker og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="f5f06-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="f5f06-108">Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, samtidig som de får en god handleopplevelse.</span><span class="sxs-lookup"><span data-stu-id="f5f06-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="f5f06-109">Krysssalg og ettersalg kan til og med brukes til å hjelpe kunder med å finne flere produkter enn de opprinnelig hadde til hensikt å kjøpe.</span><span class="sxs-lookup"><span data-stu-id="f5f06-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="f5f06-110">Når anbefalinger brukes til å hjelpe med produktoppdaging, kan de opprette flere konverteringsmuligheter, øke salgsinntektene og til og med bidra til å forbedre kundetilfredsheten og -loyaliteten.</span><span class="sxs-lookup"><span data-stu-id="f5f06-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="f5f06-111">I Commerce er produktanbefalinger basert på Microsofts anbefalinger fra teknologi for maskinlæring i stor skala.</span><span class="sxs-lookup"><span data-stu-id="f5f06-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="f5f06-112">Scenarier</span><span class="sxs-lookup"><span data-stu-id="f5f06-112">Scenarios</span></span>

<span data-ttu-id="f5f06-113">Produktanbefalingene er tilgjengelige for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="f5f06-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="f5f06-114">**På en hvilken som helst butikkside for weblesing eller startside i e-handel**: Hvis kunder eller butikkmedarbeidere besøker en butikkside, kan anbefalingsmotoren foreslå produkter i listene **Nye**, **Bestselgere** og **Tendenser**.</span><span class="sxs-lookup"><span data-stu-id="f5f06-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="f5f06-115">**På Produktdetaljer-siden:** Hvis kunder eller butikkmedarbeidere besøker en **Produktdetaljer**-side, foreslår anbefalingsmotoren ekstra varer som også sannsynligvis blir kjøpt.</span><span class="sxs-lookup"><span data-stu-id="f5f06-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="f5f06-116">Disse elementene vises i listen **Folk liker også**.</span><span class="sxs-lookup"><span data-stu-id="f5f06-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="f5f06-117">**På transaksjonssiden eller utsjekkingssiden:** Anbefalingsmotoren foreslår varer basert på hele listen med elementer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="f5f06-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="f5f06-118">Disse varene vises i listen **Ofte kjøpt sammen**.</span><span class="sxs-lookup"><span data-stu-id="f5f06-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="f5f06-119">**Tilpassede anbefalinger:** Forhandlere kan tilby påloggede kunder en tilpasset **Plukkinger for deg**-liste i tillegg til ny funksjonalitet som tillater tilpassing av eksisterende listescenarioer basert på den aktuelle kunden.</span><span class="sxs-lookup"><span data-stu-id="f5f06-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="f5f06-120">Hvis du vil ha mer informasjon, kan du se funksjonsdokumentasjonen: [Aktivere personlige anbefaleringer.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="f5f06-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="f5f06-121">Anbefalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="f5f06-121">Recommendation service</span></span>

<span data-ttu-id="f5f06-122">Produktanbefalinger bruker maskinlæringsteknologi for anbefalinger på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="f5f06-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="f5f06-123">Data i formatet som anbefalingstjenesten krever, trekkes ut fra den operative Commerce-databasen og sendes til enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="f5f06-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="f5f06-124">Anbefalingstjenesten bruker dataene til å lære opp anbefalingsmodeller for listene **Folk liker også**, **Ofte kjøpt sammen**, **Nye**, **Bestselgere** og **Tendenser**.</span><span class="sxs-lookup"><span data-stu-id="f5f06-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5f06-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f5f06-125">Additional resources</span></span>

[<span data-ttu-id="f5f06-126">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="f5f06-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="f5f06-127">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="f5f06-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="f5f06-128">Oversikt over produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="f5f06-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="f5f06-129">Opprette kuraterte produktanbefalingslister</span><span class="sxs-lookup"><span data-stu-id="f5f06-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="f5f06-130">Behandle resultater for AI-ML-basert produktanbefaling</span><span class="sxs-lookup"><span data-stu-id="f5f06-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="f5f06-131">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="f5f06-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
