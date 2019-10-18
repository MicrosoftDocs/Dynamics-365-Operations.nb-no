---
title: Selge og returnere produkter som ikke er en del av butikksortimentet
description: Med Dynamics 365 Retail kan du selge og returnere produktene utenfor sortimenter.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ae6bac983ddb4d4a217fe83c8f68c5a87ccd6a47
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024945"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="c0b30-103">Selge og returnere produkter som ikke er en del av butikksortimentet</span><span class="sxs-lookup"><span data-stu-id="c0b30-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0b30-104">Et vanlig scenario for alle forhandlere er å selge produkter til kundene eller godta returer fra kunder, selv om de ikke fører de bestemte produktene i butikken (dvs. produktene er ikke assorterte til butikken).</span><span class="sxs-lookup"><span data-stu-id="c0b30-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="c0b30-105">Her er noen vanlige scenarier:</span><span class="sxs-lookup"><span data-stu-id="c0b30-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="c0b30-106">En forhandler fører ikke alle produktene i en bestemt butikk.</span><span class="sxs-lookup"><span data-stu-id="c0b30-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="c0b30-107">De gjenstående produktene er satt på lageret.</span><span class="sxs-lookup"><span data-stu-id="c0b30-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="c0b30-108">Den butikkansatte kan hjelpe kunden med å søke etter varer i lageret, legge dem til i handlekurven og fullføre utsjekkingen ved å velge en leveringsmetode, for eksempel levering til en adresse fra lageret, eller la kunden plukke opp produktet fra det gjeldende lageret, eller fra et annet lager.</span><span class="sxs-lookup"><span data-stu-id="c0b30-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="c0b30-109">En forhandler fører ikke bestemte produkter i butikken eller har dem ikke på lager i butikken kunden besøkte, men produktene er tilgjengelige i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="c0b30-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="c0b30-110">Butikkmedarbeideren kan hjelpe kunden med å søke etter produktene i den andre butikken, legge dem til i handlekurven og fullføre utsjekkingen ved å velge en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="c0b30-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="c0b30-111">En forhandler har mange butikker i og rundt et bestemt poststed, og vil ikke tvinge kundene til å returnere varer til den samme butikken som de ble kjøpt i.</span><span class="sxs-lookup"><span data-stu-id="c0b30-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="c0b30-112">Kunder kan i stedet returnere varer til alle butikker.</span><span class="sxs-lookup"><span data-stu-id="c0b30-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="c0b30-113">Vanlige scenarier er tilgjengelige for forhandlere ved hjelp av Retail.</span><span class="sxs-lookup"><span data-stu-id="c0b30-113">Those common scenarios are available for retailers using Retail.</span></span> <span data-ttu-id="c0b30-114">Med Retail kan du:</span><span class="sxs-lookup"><span data-stu-id="c0b30-114">With Retail, you can:</span></span>

+ <span data-ttu-id="c0b30-115">Søke etter eller bla gjennom produkter i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="c0b30-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="c0b30-116">Søke etter eller bla gjennom alle frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="c0b30-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="c0b30-117">Opprette hentesalgstransaksjoner eller kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="c0b30-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="c0b30-118">Velge leveringsalternativer for kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="c0b30-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="c0b30-119">Plukke produkter i den gjeldende butikken eller annen butikk.</span><span class="sxs-lookup"><span data-stu-id="c0b30-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="c0b30-120">Annullere en ordre i den gjeldende butikken eller annen butikk.</span><span class="sxs-lookup"><span data-stu-id="c0b30-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="c0b30-121">Returnere en ordre med eller uten mottaket i den gjeldende butikken eller annen butikk.</span><span class="sxs-lookup"><span data-stu-id="c0b30-121">Return an order with or without the receipt at the current store or another store.</span></span>
