---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261427"
---
# <a name="cart-module"></a><span data-ttu-id="a8cc3-103">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8cc3-104">Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a8cc3-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="a8cc3-105">Overview</span></span>

<span data-ttu-id="a8cc3-106">En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="a8cc3-107">Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="a8cc3-108">Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="a8cc3-109">Den støtter også koblingen **Tilbake til shopping**.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="a8cc3-110">Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="a8cc3-111">Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="a8cc3-112">Egenskaper og spor for handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-112">Cart module properties and slots</span></span>

<span data-ttu-id="a8cc3-113">Handlekurvmodulen har egenskapen **Overskrift** som kan settes til verdier som **Handlepose** og **Varer i handlekurven**.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="a8cc3-114">Moduler som kan brukes i handlekurvmodulen</span><span class="sxs-lookup"><span data-stu-id="a8cc3-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="a8cc3-115">**Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="a8cc3-116">Meldingene drives av innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="a8cc3-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="a8cc3-117">Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="a8cc3-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="a8cc3-118">**Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="a8cc3-119">Den lar brukere angi en plassering for å finne butikker i nærheten.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="a8cc3-120">Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="a8cc3-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="a8cc3-121">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="a8cc3-121">Module properties</span></span>

<span data-ttu-id="a8cc3-122">Handlekurvmoduler har følgende innstillinger som kan konfigureres under **Områdeinnstillinger \> Utvidelser**:</span><span class="sxs-lookup"><span data-stu-id="a8cc3-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="a8cc3-123">**Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="a8cc3-124">En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="a8cc3-125">**Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="a8cc3-126">Denne lagerkontrollen utføres for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="a8cc3-127">Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="a8cc3-128">Hvis du vil ha informasjon om hvordan du konfigurerer lagerinnstillinger i back office, kan du se [Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="a8cc3-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="a8cc3-129">**Lagerbuffer** – Denne egenskapen brukes til å angi et bufferantall for lageret.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="a8cc3-130">Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="a8cc3-131">Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="a8cc3-132">Derfor, når salget skjer raskt i flere kanaler og lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="a8cc3-133">**Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="a8cc3-134">Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="a8cc3-135">Samhandling med Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="a8cc3-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="a8cc3-136">Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="a8cc3-137">Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="a8cc3-138">Legge til en handlekurvmodul på en side</span><span class="sxs-lookup"><span data-stu-id="a8cc3-138">Add a cart module to a page</span></span>

<span data-ttu-id="a8cc3-139">Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a8cc3-140">Opprett et fragment kalt **Handlekurvfragment**, og legg til en handlekurvmodul i det nye fragmentet.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="a8cc3-141">Legg til en overskrift i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="a8cc3-142">Legg til en butikkvelgermodul i handlekurvmodulen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="a8cc3-143">Lagre fragmentet, fullfør redigeringen, og publiser deretter fragmentet.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="a8cc3-144">Opprett en mal som heter **Handlekurvmal**, og legg til handlekurvfragmentet som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="a8cc3-145">Lagre malen, fullfør redigeringen, og publiser deretter malen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="a8cc3-146">Opprett en side som bruker den nye malen.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="a8cc3-147">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-147">Save and preview the page.</span></span>
1. <span data-ttu-id="a8cc3-148">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="a8cc3-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8cc3-149">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a8cc3-149">Additional resources</span></span>

[<span data-ttu-id="a8cc3-150">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="a8cc3-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a8cc3-151">Containermodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a8cc3-152">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="a8cc3-153">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a8cc3-154">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a8cc3-155">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a8cc3-156">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a8cc3-157">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a8cc3-158">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="a8cc3-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="a8cc3-159">Beregne lagertilgjengelighet for detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="a8cc3-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
