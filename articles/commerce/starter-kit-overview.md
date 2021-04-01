---
title: Oversikt over modulbibliotek
description: Dette emnet viser en oversikt over modulbiblioteket for Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcb0c2317315308de51d8247d23a930f10c3de6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234299"
---
# <a name="module-library-overview"></a><span data-ttu-id="72043-103">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="72043-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="72043-104">Dette emnet viser en oversikt over modulbiblioteket for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="72043-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="72043-105">Modulbiblioteket for Dynamics 365 Commerce er en samling moduler som kan brukes til å bygge et webområde for e-handel.</span><span class="sxs-lookup"><span data-stu-id="72043-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="72043-106">Moduler har både brukergrensesnittaspekter (UI) og funksjonelle virkemåteaspekter.</span><span class="sxs-lookup"><span data-stu-id="72043-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="72043-107">Temaer kan brukes på modulene i modulbiblioteket for å endre utseende og virkemåte.</span><span class="sxs-lookup"><span data-stu-id="72043-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="72043-108">Temaene bruker gjennomgripende stilark (CSS).</span><span class="sxs-lookup"><span data-stu-id="72043-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="72043-109">Et tema for et fiktivt e-handelsområde med navnet "Fabrikam" leveres som en del av modulbiblioteket og kan brukes som referanse.</span><span class="sxs-lookup"><span data-stu-id="72043-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="72043-110">Modulbibliotekmoduler</span><span class="sxs-lookup"><span data-stu-id="72043-110">Module library modules</span></span>

<span data-ttu-id="72043-111">Følgende modultyper finnes i modulbiblioteket:</span><span class="sxs-lookup"><span data-stu-id="72043-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="72043-112">**Containermodul** – En containermodul er en enkel modul som fungerer som vert for andre moduler.</span><span class="sxs-lookup"><span data-stu-id="72043-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="72043-113">Den kontrollerer oppsettet til modulene som er i det.</span><span class="sxs-lookup"><span data-stu-id="72043-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="72043-114">**Markedsføringsmoduler** – Markedsføringsmoduler omfatter moduler for innholdsblokk, tekstblokk, videospiller og karusell.</span><span class="sxs-lookup"><span data-stu-id="72043-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="72043-115">Alle disse modulene kan brukes til å vise innhold.</span><span class="sxs-lookup"><span data-stu-id="72043-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="72043-116">De kan plasseres på en hvilken som helst side og er drevet av data fra et innholdsbehandlingssystem (CMS).</span><span class="sxs-lookup"><span data-stu-id="72043-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="72043-117">**Topptekst- og bunntekstmoduler** – Topptekst- og bunntekstmoduler vises i topp- og bunnteksten på alle områdesider.</span><span class="sxs-lookup"><span data-stu-id="72043-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="72043-118">Disse modulene kan konfigureres som obligatoriske via egenskaper.</span><span class="sxs-lookup"><span data-stu-id="72043-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="72043-119">**Søkemoduler** – Produkter kan oppdages ved hjelp av søkemodulen i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="72043-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="72043-120">Søkeresultatene vises på søkeresultatsiden.</span><span class="sxs-lookup"><span data-stu-id="72043-120">Search results appear on the search results page.</span></span> <span data-ttu-id="72043-121">Produkter kan også oppdages på kategorisider, som er dedikerte sider for hver kategori som støttes i kanalnavigeringshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="72043-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="72043-122">I tillegg kan presiseringsmoduler brukes til å filtrere resultater på søkeresultat- og kategorisider ytterligere.</span><span class="sxs-lookup"><span data-stu-id="72043-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="72043-123">**Moduler for produktdetaljside** – Produktdetaljsider bruker flere moduler til å vise produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="72043-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="72043-124">Kjøpsboksmodulen lar kundene vise produkter og legge dem til handlekurven.</span><span class="sxs-lookup"><span data-stu-id="72043-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="72043-125">Andre moduler, som modulen for tekniske spesifikasjoner, viser produktdetaljene.</span><span class="sxs-lookup"><span data-stu-id="72043-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="72043-126">Modulen for vurderinger og omtale kan brukes til å vise og gi vurderinger.</span><span class="sxs-lookup"><span data-stu-id="72043-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="72043-127">**Modulen Kjøpe på Internett og hente i butikk** – Modulen Kjøpe på Internett og hente i butikk er integrert med Bing-kart.</span><span class="sxs-lookup"><span data-stu-id="72043-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="72043-128">Den kan brukes til å finne nærliggende butikker der kunder kan plukke opp produkter de har kjøpt.</span><span class="sxs-lookup"><span data-stu-id="72043-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="72043-129">**Innkjøpsmoduler** – Innkjøpsmoduler inkluderer handlekurvmodulen, som kan brukes til å legge varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="72043-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="72043-130">I kassemodulen registreres leveringsadresse, leveringsalternativer, gavekort, fordelsprogram og kredittkortinformasjon, slik at en ordre kan behandles.</span><span class="sxs-lookup"><span data-stu-id="72043-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="72043-131">Etter at en ordre er lagt inn, kan ordrebekreftelsesmodulen brukes til å vise bekreftelsesdetaljene.</span><span class="sxs-lookup"><span data-stu-id="72043-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="72043-132">**Kontobehandlingsmoduler** – Påloggingsmodulen lar kundene logge seg på en eksisterende konto, og registreringsmodulen lar dem opprette en ny konto.</span><span class="sxs-lookup"><span data-stu-id="72043-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="72043-133">Når en konto er opprettet, kan du bruke ordrehistorikkmodulen til å vise de siste ordrene, og ordredetaljmodulen kan brukes til å vise ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="72043-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="72043-134">**Anbefalinger-modulen** – Anbefalinger vises ved hjelp av produktplasseringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="72043-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="72043-135">Denne modulen støtter algoritmer og redigeringslister som kan vises på alle sider.</span><span class="sxs-lookup"><span data-stu-id="72043-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72043-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="72043-136">Additional resources</span></span>

[<span data-ttu-id="72043-137">Containermodul</span><span class="sxs-lookup"><span data-stu-id="72043-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="72043-138">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="72043-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="72043-139">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="72043-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="72043-140">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="72043-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="72043-141">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="72043-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="72043-142">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="72043-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="72043-143">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="72043-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]