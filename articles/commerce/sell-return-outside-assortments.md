---
title: Selge og returnere produkter som ikke er en del av butikksortimentet
description: Med Dynamics 365 Commerce kan du selge og returnere produktene utenfor sortimenter.
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
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414725"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="69840-103">Selge og returnere produkter som ikke er en del av butikksortimentet</span><span class="sxs-lookup"><span data-stu-id="69840-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69840-104">Et vanlig scenario for alle forhandlere er å selge produkter til kundene eller godta returer fra kunder, selv om de ikke fører de bestemte produktene i butikken (dvs. produktene er ikke assorterte til butikken).</span><span class="sxs-lookup"><span data-stu-id="69840-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="69840-105">Her er noen vanlige scenarier:</span><span class="sxs-lookup"><span data-stu-id="69840-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="69840-106">En forhandler fører ikke alle produktene i en bestemt butikk.</span><span class="sxs-lookup"><span data-stu-id="69840-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="69840-107">De gjenstående produktene er satt på lageret.</span><span class="sxs-lookup"><span data-stu-id="69840-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="69840-108">Den butikkansatte kan hjelpe kunden med å søke etter varer i lageret, legge dem til i handlekurven og fullføre utsjekkingen ved å velge en leveringsmetode, for eksempel levering til en adresse fra lageret, eller la kunden plukke opp produktet fra det gjeldende lageret, eller fra et annet lager.</span><span class="sxs-lookup"><span data-stu-id="69840-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="69840-109">En forhandler fører ikke bestemte produkter i butikken eller har dem ikke på lager i butikken kunden besøkte, men produktene er tilgjengelige i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="69840-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="69840-110">Butikkmedarbeideren kan hjelpe kunden med å søke etter produktene i den andre butikken, legge dem til i handlekurven og fullføre utsjekkingen ved å velge en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="69840-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="69840-111">En forhandler har mange butikker i og rundt et bestemt poststed, og vil ikke tvinge kundene til å returnere varer til den samme butikken som de ble kjøpt i.</span><span class="sxs-lookup"><span data-stu-id="69840-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="69840-112">Kunder kan i stedet returnere varer til alle butikker.</span><span class="sxs-lookup"><span data-stu-id="69840-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="69840-113">Disse vanlige scenarioene er tilgjengelige for forhandlere ved hjelp av Commerce.</span><span class="sxs-lookup"><span data-stu-id="69840-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="69840-114">Med Commerce kan du:</span><span class="sxs-lookup"><span data-stu-id="69840-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="69840-115">Søke etter eller bla gjennom produkter i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="69840-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="69840-116">Søke etter eller bla gjennom alle frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="69840-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="69840-117">Opprette hentesalgstransaksjoner eller kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="69840-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="69840-118">Velge leveringsalternativer for kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="69840-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="69840-119">Plukke produkter i den gjeldende butikken eller annen butikk.</span><span class="sxs-lookup"><span data-stu-id="69840-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="69840-120">Annullere en ordre i den gjeldende butikken eller annen butikk.</span><span class="sxs-lookup"><span data-stu-id="69840-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="69840-121">Returnere en ordre med eller uten mottaket i den gjeldende butikken eller annen butikk.</span><span class="sxs-lookup"><span data-stu-id="69840-121">Return an order with or without the receipt at the current store or another store.</span></span>
