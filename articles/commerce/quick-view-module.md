---
title: Hurtigvisningsmodul
description: Dette emnet dekker hurtigvisningsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097058"
---
# <a name="quick-view-module"></a><span data-ttu-id="f050b-103">Hurtigvisningsmodul</span><span class="sxs-lookup"><span data-stu-id="f050b-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f050b-104">Dette emnet dekker hurtigvisningsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f050b-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f050b-105">Med hurtigvisningsmodulen kan brukere raskt vise produktinformasjon når de blar gjennom produkter på en listeside og legger til én eller flere produkter i handlekurven fra listesiden, uten å måtte gå til produktdetaljersiden (PDP).</span><span class="sxs-lookup"><span data-stu-id="f050b-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="f050b-106">Modulen for hurtigvisning gir en oversikt over produktinformasjonen som brukerne trenger for å ta en avgjørelse om å legge til i handlekurv.</span><span class="sxs-lookup"><span data-stu-id="f050b-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="f050b-107">Den inneholder også en kobling til PDP-en, slik at brukere kan vise flere produktdetaljer og innkjøpsalternativer.</span><span class="sxs-lookup"><span data-stu-id="f050b-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="f050b-108">Modulen for hurtigvisning støttes av modulene for [produktsamling](product-collection-module-overview.md) og [søkeresultater](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="f050b-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f050b-109">Hurtigvisningsmodulen er tilgjengelig fra Commerce versjon 10.0.17-versjonen.</span><span class="sxs-lookup"><span data-stu-id="f050b-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="f050b-110">Illustrasjonen nedenfor viser et eksempel på en hurtigvisningsmodul på en produktlisteside.</span><span class="sxs-lookup"><span data-stu-id="f050b-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Eksempel på en hurtigvisningsmodul på en produktlisteside](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="f050b-112">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="f050b-112">Module properties</span></span>

<span data-ttu-id="f050b-113">Modulen for hurtigvisning støtter noen av de samme funksjonene som kjøpsboksmodulen.</span><span class="sxs-lookup"><span data-stu-id="f050b-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="f050b-114">Derfor ligner egenskapene til en hurtigvisningsmodul egenskapene til en kjøpsboksmodul.</span><span class="sxs-lookup"><span data-stu-id="f050b-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="f050b-115">Egenskap</span><span class="sxs-lookup"><span data-stu-id="f050b-115">Property</span></span> | <span data-ttu-id="f050b-116">Verdier</span><span class="sxs-lookup"><span data-stu-id="f050b-116">Values</span></span> | <span data-ttu-id="f050b-117">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f050b-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="f050b-118">Overskriftsetikett</span><span class="sxs-lookup"><span data-stu-id="f050b-118">Heading tag</span></span> | <span data-ttu-id="f050b-119">**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**</span><span class="sxs-lookup"><span data-stu-id="f050b-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="f050b-120">Denne egenskapen definerer overskriftsetiketten for produkttittelen.</span><span class="sxs-lookup"><span data-stu-id="f050b-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="f050b-121">Hvis hurtigvisningsmodulen er øverst på siden, bør denne egenskapen settes til **H1** for å oppfylle tilgjengelighetsstandardene.</span><span class="sxs-lookup"><span data-stu-id="f050b-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="f050b-122">Tillat egendefinert pris</span><span class="sxs-lookup"><span data-stu-id="f050b-122">Allow custom price</span></span> | <span data-ttu-id="f050b-123">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="f050b-123">**True** or **False**</span></span> | <span data-ttu-id="f050b-124">Hvis denne egenskapen er satt til **Sann**, kan brukeren angi en egendefinert pris.</span><span class="sxs-lookup"><span data-stu-id="f050b-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="f050b-125">Minstepris</span><span class="sxs-lookup"><span data-stu-id="f050b-125">Minimum price</span></span> | <span data-ttu-id="f050b-126">Heltall</span><span class="sxs-lookup"><span data-stu-id="f050b-126">Integer</span></span> | <span data-ttu-id="f050b-127">Denne egenskapen gjelder bare hvis egenskapen **Tillat egendefinert pris** er satt til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="f050b-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="f050b-128">Den definerer minimumsprisen som brukeren kan angi (for eksempel USD 1).</span><span class="sxs-lookup"><span data-stu-id="f050b-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="f050b-129">Maksimumspris</span><span class="sxs-lookup"><span data-stu-id="f050b-129">Maximum price</span></span> | <span data-ttu-id="f050b-130">Heltall</span><span class="sxs-lookup"><span data-stu-id="f050b-130">Integer</span></span> | <span data-ttu-id="f050b-131">Denne egenskapen gjelder bare hvis egenskapen **Tillat egendefinert pris** er satt til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="f050b-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="f050b-132">Den definerer maksimumsprisen som brukeren kan angi (for eksempel USD 1 000).</span><span class="sxs-lookup"><span data-stu-id="f050b-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="f050b-133">Innstillinger for Commerce-områdebygger</span><span class="sxs-lookup"><span data-stu-id="f050b-133">Commerce site builder settings</span></span>

<span data-ttu-id="f050b-134">På samme måte som kjøpsboksmodulen overholder hurtigvisningsmodulen innstillingene i **Områdeinnstillinger \> Tillegg \> Legg til produkt i handlekurv**.</span><span class="sxs-lookup"><span data-stu-id="f050b-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="f050b-135">Innstillingen **Naviger til handlekurvside** ignoreres imidlertid fordi den er inkonsekvent med formålet med hurtigvisningsmodulen, som er å gjøre det mulig for brukere å bla gjennom flere produkter på en listeside og legge dem til i handlekurven uten å gå bort fra listesiden.</span><span class="sxs-lookup"><span data-stu-id="f050b-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="f050b-136">Legge til en hurtigvisningsmodul på en produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="f050b-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="f050b-137">En hurtigvisningsmodul kan legges til produktsamlings- og søkeresultatmodulene.</span><span class="sxs-lookup"><span data-stu-id="f050b-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="f050b-138">Følg denne fremgangsmåten for å legge til en hurtigvisningmodul i en produktsamlingsmodul i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="f050b-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f050b-139">Gå til **Sider**, og velg hjemmesiden for Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="f050b-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="f050b-140">Gå til en **Produktsamling**-modul på hjemmesiden, velg ellipsen (**...**), og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f050b-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f050b-141">I dialogboksen **Legg til modul** velger du **Hurtigvisning**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f050b-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f050b-142">I overskriftsruten i modulen **Hurtigvisning** velger du **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="f050b-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="f050b-143">I dialogboksen **Overskrift** angir du **Overskriftsnivå**-feltet til **H2**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f050b-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="f050b-144">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="f050b-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f050b-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f050b-145">Additional resources</span></span>

[<span data-ttu-id="f050b-146">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="f050b-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f050b-147">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="f050b-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f050b-148">Produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="f050b-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="f050b-149">Søkeresultatmodul</span><span class="sxs-lookup"><span data-stu-id="f050b-149">Search results module</span></span>](search-result-module.md)
