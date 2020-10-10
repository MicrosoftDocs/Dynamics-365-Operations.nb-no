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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc52dd8e14bb2e9f2f9c026ee0e058aee4cedcb
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817832"
---
# <a name="module-library-overview"></a><span data-ttu-id="d1781-103">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="d1781-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1781-104">Dette emnet viser en oversikt over modulbiblioteket for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d1781-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

## <a name="overview"></a><span data-ttu-id="d1781-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d1781-105">Overview</span></span>

<span data-ttu-id="d1781-106">Modulbiblioteket for Dynamics 365 Commerce er en samling moduler som kan brukes til å bygge et webområde for e-handel.</span><span class="sxs-lookup"><span data-stu-id="d1781-106">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="d1781-107">Moduler har både brukergrensesnittaspekter (UI) og funksjonelle virkemåteaspekter.</span><span class="sxs-lookup"><span data-stu-id="d1781-107">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="d1781-108">Temaer kan brukes på modulene i modulbiblioteket for å endre utseende og virkemåte.</span><span class="sxs-lookup"><span data-stu-id="d1781-108">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="d1781-109">Temaene bruker gjennomgripende stilark (CSS).</span><span class="sxs-lookup"><span data-stu-id="d1781-109">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="d1781-110">Et tema for et fiktivt e-handelsområde med navnet "Fabrikam" leveres som en del av modulbiblioteket og kan brukes som referanse.</span><span class="sxs-lookup"><span data-stu-id="d1781-110">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="d1781-111">Modulbibliotekmoduler</span><span class="sxs-lookup"><span data-stu-id="d1781-111">Module library modules</span></span>

<span data-ttu-id="d1781-112">Følgende modultyper finnes i modulbiblioteket:</span><span class="sxs-lookup"><span data-stu-id="d1781-112">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="d1781-113">**Containermodul** – En containermodul er en enkel modul som fungerer som vert for andre moduler.</span><span class="sxs-lookup"><span data-stu-id="d1781-113">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="d1781-114">Den kontrollerer oppsettet til modulene som er i det.</span><span class="sxs-lookup"><span data-stu-id="d1781-114">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="d1781-115">**Markedsføringsmoduler** – Markedsføringsmoduler omfatter moduler for innholdsblokk, tekstblokk, videospiller og karusell.</span><span class="sxs-lookup"><span data-stu-id="d1781-115">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="d1781-116">Alle disse modulene kan brukes til å vise innhold.</span><span class="sxs-lookup"><span data-stu-id="d1781-116">All these modules can be used to showcase content.</span></span> <span data-ttu-id="d1781-117">De kan plasseres på en hvilken som helst side og er drevet av data fra et innholdsbehandlingssystem (CMS).</span><span class="sxs-lookup"><span data-stu-id="d1781-117">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="d1781-118">**Topptekst- og bunntekstmoduler** – Topptekst- og bunntekstmoduler vises i topp- og bunnteksten på alle områdesider.</span><span class="sxs-lookup"><span data-stu-id="d1781-118">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="d1781-119">Disse modulene kan konfigureres som obligatoriske via egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d1781-119">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="d1781-120">**Søkemoduler** – Produkter kan oppdages ved hjelp av søkemodulen i toppteksten.</span><span class="sxs-lookup"><span data-stu-id="d1781-120">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="d1781-121">Søkeresultatene vises på søkeresultatsiden.</span><span class="sxs-lookup"><span data-stu-id="d1781-121">Search results appear on the search results page.</span></span> <span data-ttu-id="d1781-122">Produkter kan også oppdages på kategorisider, som er dedikerte sider for hver kategori som støttes i kanalnavigeringshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d1781-122">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="d1781-123">I tillegg kan presiseringsmoduler brukes til å filtrere resultater på søkeresultat- og kategorisider ytterligere.</span><span class="sxs-lookup"><span data-stu-id="d1781-123">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="d1781-124">**Moduler for produktdetaljside** – Produktdetaljsider bruker flere moduler til å vise produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="d1781-124">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="d1781-125">Kjøpsboksmodulen lar kundene vise produkter og legge dem til handlekurven.</span><span class="sxs-lookup"><span data-stu-id="d1781-125">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="d1781-126">Andre moduler, som modulen for tekniske spesifikasjoner, viser produktdetaljene.</span><span class="sxs-lookup"><span data-stu-id="d1781-126">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="d1781-127">Modulen for vurderinger og omtale kan brukes til å vise og gi vurderinger.</span><span class="sxs-lookup"><span data-stu-id="d1781-127">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="d1781-128">**Modulen Kjøpe på Internett og hente i butikk** – Modulen Kjøpe på Internett og hente i butikk er integrert med Bing-kart.</span><span class="sxs-lookup"><span data-stu-id="d1781-128">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="d1781-129">Den kan brukes til å finne nærliggende butikker der kunder kan plukke opp produkter de har kjøpt.</span><span class="sxs-lookup"><span data-stu-id="d1781-129">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="d1781-130">**Innkjøpsmoduler** – Innkjøpsmoduler inkluderer handlekurvmodulen, som kan brukes til å legge varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="d1781-130">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="d1781-131">I kassemodulen registreres leveringsadresse, leveringsalternativer, gavekort, fordelsprogram og kredittkortinformasjon, slik at en ordre kan behandles.</span><span class="sxs-lookup"><span data-stu-id="d1781-131">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="d1781-132">Etter at en ordre er lagt inn, kan ordrebekreftelsesmodulen brukes til å vise bekreftelsesdetaljene.</span><span class="sxs-lookup"><span data-stu-id="d1781-132">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="d1781-133">**Kontobehandlingsmoduler** – Påloggingsmodulen lar kundene logge seg på en eksisterende konto, og registreringsmodulen lar dem opprette en ny konto.</span><span class="sxs-lookup"><span data-stu-id="d1781-133">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="d1781-134">Når en konto er opprettet, kan du bruke ordrehistorikkmodulen til å vise de siste ordrene, og ordredetaljmodulen kan brukes til å vise ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="d1781-134">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="d1781-135">**Anbefalinger-modulen** – Anbefalinger vises ved hjelp av produktplasseringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="d1781-135">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="d1781-136">Denne modulen støtter algoritmer og redigeringslister som kan vises på alle sider.</span><span class="sxs-lookup"><span data-stu-id="d1781-136">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1781-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d1781-137">Additional resources</span></span>

[<span data-ttu-id="d1781-138">Containermodul</span><span class="sxs-lookup"><span data-stu-id="d1781-138">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d1781-139">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="d1781-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d1781-140">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="d1781-140">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d1781-141">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="d1781-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d1781-142">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="d1781-142">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d1781-143">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="d1781-143">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d1781-144">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="d1781-144">Footer module</span></span>](author-footer-module.md)
