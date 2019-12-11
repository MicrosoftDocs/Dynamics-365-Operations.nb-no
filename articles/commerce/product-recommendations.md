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
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770053"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="588b8-104">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="588b8-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="588b8-105">Microsoft Dynamics 365 Commerce kan brukes til å vise produktanbefalinger på webområdet for e-handel og salgsstedsenheten.</span><span class="sxs-lookup"><span data-stu-id="588b8-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="588b8-106">Produktanbefalinger er varer som en kunde kan være interessert i.</span><span class="sxs-lookup"><span data-stu-id="588b8-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="588b8-107">Anbefalingene er basert på kjøpstendensene for andre kunder i nettbutikker og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="588b8-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="588b8-108">Produktanbefalinger gjør at kundene enkelt og raskt kan finne produkter de vil ha, samtidig som de får en god handleopplevelse.</span><span class="sxs-lookup"><span data-stu-id="588b8-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="588b8-109">Krysssalg og ettersalg kan til og med brukes til å hjelpe kunder med å finne flere produkter enn de opprinnelig hadde til hensikt å kjøpe.</span><span class="sxs-lookup"><span data-stu-id="588b8-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="588b8-110">Når anbefalinger brukes til å hjelpe med produktoppdaging, kan de opprette flere konverteringsmuligheter, øke salgsinntektene og til og med bidra til å forbedre kundetilfredsheten og -loyaliteten.</span><span class="sxs-lookup"><span data-stu-id="588b8-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="588b8-111">I Commerce er produktanbefalinger basert på Microsofts anbefalinger fra teknologi for maskinlæring i stor skala.</span><span class="sxs-lookup"><span data-stu-id="588b8-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="588b8-112">Scenarier</span><span class="sxs-lookup"><span data-stu-id="588b8-112">Scenarios</span></span>

<span data-ttu-id="588b8-113">Produktanbefalingene er tilgjengelige for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="588b8-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="588b8-114">**På en hvilken som helst butikkside for weblesing eller startside i e-handel**: Hvis kunder eller butikkmedarbeidere besøker en butikkside, kan anbefalingsmotoren foreslå produkter i listene **Nye**, **Bestselgere** og **Tendenser**.</span><span class="sxs-lookup"><span data-stu-id="588b8-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="588b8-115">**På Produktdetaljer-siden:** Hvis kunder eller butikkmedarbeidere besøker en **Produktdetaljer**-side, foreslår anbefalingsmotoren ekstra varer som også sannsynligvis blir kjøpt.</span><span class="sxs-lookup"><span data-stu-id="588b8-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="588b8-116">Disse elementene vises i listen **Folk liker også**.</span><span class="sxs-lookup"><span data-stu-id="588b8-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="588b8-117">**På transaksjonssiden eller utsjekkingssiden:** Anbefalingsmotoren foreslår varer basert på hele listen med elementer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="588b8-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="588b8-118">Disse varene vises i listen **Ofte kjøpt sammen**.</span><span class="sxs-lookup"><span data-stu-id="588b8-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="588b8-119">Anbefalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="588b8-119">Recommendation service</span></span>

<span data-ttu-id="588b8-120">Produktanbefalinger bruker maskinlæringsteknologi for anbefalinger på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="588b8-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="588b8-121">Data i formatet som anbefalingstjenesten krever, trekkes ut fra den operative Commerce-databasen og sendes til enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="588b8-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="588b8-122">Anbefalingstjenesten bruker dataene til å lære opp anbefalingsmodeller for listene **Folk liker også**, **Ofte kjøpt sammen**, **Nye**, **Bestselgere** og **Tendenser**.</span><span class="sxs-lookup"><span data-stu-id="588b8-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="588b8-123">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="588b8-123">Additional resources</span></span>

[<span data-ttu-id="588b8-124">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="588b8-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="588b8-125">Opprette kuraterte produktanbefalingslister</span><span class="sxs-lookup"><span data-stu-id="588b8-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="588b8-126">Behandle resultater for AI-ML-basert produktanbefaling</span><span class="sxs-lookup"><span data-stu-id="588b8-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="588b8-127">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="588b8-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
