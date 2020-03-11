---
title: Vurderings- og omtalemoduler
description: Dette emnet dekker vurderings- og omtalemoduler som brukes på sider med produktdetaljer i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: ee2a2a781537b592fb5f80ce424a7331c4e21d41
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071884"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="0c677-103">Vurderings- og omtalemoduler</span><span class="sxs-lookup"><span data-stu-id="0c677-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c677-104">Dette emnet dekker vurderings- og omtalemoduler som brukes på sider med produktdetaljer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0c677-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0c677-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0c677-105">Overview</span></span>

<span data-ttu-id="0c677-106">Vurderinger og evalueringer på e-handelswebområder hjelper kunder med å lære om produkter før de tar en avgjørelse, og det er også en metode for å samle inn tilbakemeldinger fra kunder om produkter.</span><span class="sxs-lookup"><span data-stu-id="0c677-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="0c677-107">Vurderingene vises på produktlistesider, kategorilistesider, sider for søkeresultater og andre områdesider.</span><span class="sxs-lookup"><span data-stu-id="0c677-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="0c677-108">Vurderingshistogrammer og produktgjennomganger vises på sider for produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0c677-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="0c677-109">En **Skriv en vurdering**-knapp gir kundene muligheten til å sende inn rangeringer og omtaler for et produkt.</span><span class="sxs-lookup"><span data-stu-id="0c677-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="0c677-110">Disse PDP-funksjonene kontrolleres av vurderings- og omtalemoduler.</span><span class="sxs-lookup"><span data-stu-id="0c677-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="0c677-111">Vurderings- og omtalemoduler på PDPer</span><span class="sxs-lookup"><span data-stu-id="0c677-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="0c677-112">Tre moduler viser vurderings- og omtalesammendraget på PDPer:</span><span class="sxs-lookup"><span data-stu-id="0c677-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="0c677-113">Modul for skriving av vurdering</span><span class="sxs-lookup"><span data-stu-id="0c677-113">Write review module</span></span>
- <span data-ttu-id="0c677-114">Listemodul for produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="0c677-114">Product reviews list module</span></span>
- <span data-ttu-id="0c677-115">Modul for vurderingshistogrammer</span><span class="sxs-lookup"><span data-stu-id="0c677-115">Ratings histogram module</span></span>
 
<span data-ttu-id="0c677-116">Illustrasjonen nedenfor viser hvordan vurderings- og evalueringsmodulene ser ut på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0c677-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vurderings- og omtalemoduler på en PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="0c677-118">Hvis du vil ha informasjon om hvordan du optimaliserer PDP-maler og -oppsett slik at du kan dele konfigurasjonene for vurderings- og omtalemoduler mellom flere PDPer på e-handelsområdet, se [Oversikt over maler og oppsett](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0c677-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="0c677-119">Illustrasjonen nedenfor viser hvordan dialogboksen **Legg til modul** viser rangerings- og omtalemoduler i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0c677-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="0c677-120">![Dialogboksen Legg til modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="0c677-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="0c677-121">Modul for omtaleskriving</span><span class="sxs-lookup"><span data-stu-id="0c677-121">Write review module</span></span>

<span data-ttu-id="0c677-122">Modulen for omtaleskriving inkluderer en **Skriv en vurdering**-knapp som lar brukere logge på, tilordne en vurdering og skrive en omtale av et produkt.</span><span class="sxs-lookup"><span data-stu-id="0c677-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="0c677-123">Denne modulen lar også brukere redigere en vurdering eller omtale som de tidligere har sendt.</span><span class="sxs-lookup"><span data-stu-id="0c677-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="0c677-124">Denne modulen vises vanligvis over listemodulene for vurderingshistogram og produktevalueringer på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0c677-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="0c677-125">Følgende illustrasjon viser dialogboksen **Skriv en gjennomgang** som vises når en kunde velger **Skriv en vurdering**.</span><span class="sxs-lookup"><span data-stu-id="0c677-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="0c677-126">Kunden kan bruke denne dialogboksen til å sende inn en vurdering og en omtale.</span><span class="sxs-lookup"><span data-stu-id="0c677-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="0c677-127">![Dialogboksen Skriv en vurdering](media/rnr-eCommerce-write-review-module.png) Tabellen nedenfor viser egenskapen for Skriv en vurdering-modulen som må konfigureres i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="0c677-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="0c677-128">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="0c677-128">Property name</span></span> | <span data-ttu-id="0c677-129">Verdi</span><span class="sxs-lookup"><span data-stu-id="0c677-129">Value</span></span>        | <span data-ttu-id="0c677-130">Egenskapsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c677-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="0c677-131">Navn</span><span class="sxs-lookup"><span data-stu-id="0c677-131">Name</span></span>          | <span data-ttu-id="0c677-132">Skriv vurdering</span><span class="sxs-lookup"><span data-stu-id="0c677-132">Write review</span></span> | <span data-ttu-id="0c677-133">Navnet på Skriv en vurdering-modulen</span><span class="sxs-lookup"><span data-stu-id="0c677-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="0c677-134">Modul for vurderingshistogrammer</span><span class="sxs-lookup"><span data-stu-id="0c677-134">Ratings histogram module</span></span>

<span data-ttu-id="0c677-135">Modul for vurderingshistogrammer viser vurderingshistogrammet.</span><span class="sxs-lookup"><span data-stu-id="0c677-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="0c677-136">Denne modulen vises vanligvis mellom Skriv vurdering-modulen og listemodulen for produktvurderinger på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0c677-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="0c677-137">Histogrammodulen for vurderinger krever ingen konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="0c677-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="0c677-138">Du trenger bare å legge til modulen i PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="0c677-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="0c677-139">Illustrasjonene nedenfor viser hvordan en PDP-mal ser ut i Dynamics 365 Commerce når modulene for vurderinger og gjennomgang er konfigurert for visning på PDPer.</span><span class="sxs-lookup"><span data-stu-id="0c677-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="0c677-140">![PDP-mal når vurderinger og omtaler er konfigurert for visning på PDPer](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="0c677-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="0c677-141">Listemodul for produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="0c677-141">Product reviews list module</span></span>

<span data-ttu-id="0c677-142">Listemodulen for produktvurderinger viser en liste over produktvurderinger sammen med alternativer for sortering, filtrering og paginering.</span><span class="sxs-lookup"><span data-stu-id="0c677-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="0c677-143">Denne modulen vises vanligvis etter vurderingshistogrammodulen på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0c677-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="0c677-144">Tabellen nedenfor viser egenskapene for listemodulen for produktvurderinger som må konfigureres i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="0c677-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0c677-145">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="0c677-145">Property name</span></span>              | <span data-ttu-id="0c677-146">Verdi</span><span class="sxs-lookup"><span data-stu-id="0c677-146">Value</span></span> | <span data-ttu-id="0c677-147">Egenskapsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c677-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="0c677-148">Omtaler som vises på hver side</span><span class="sxs-lookup"><span data-stu-id="0c677-148">Reviews shown on each page</span></span> | <span data-ttu-id="0c677-149">10</span><span class="sxs-lookup"><span data-stu-id="0c677-149">10</span></span>    | <span data-ttu-id="0c677-150">Antall omtaler som skal vises om gangen på en PDP.</span><span class="sxs-lookup"><span data-stu-id="0c677-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="0c677-151">Knappene **Neste** og **Forrige** er inkludert, slik at brukerne kan bla gjennom sidene med gjennomganger.</span><span class="sxs-lookup"><span data-stu-id="0c677-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="0c677-152">Vurderingshistogram – sammendragsvisning</span><span class="sxs-lookup"><span data-stu-id="0c677-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="0c677-153">Listemodulen for produktvurderinger inneholder et spor der du kan legge til en vurderingshistogrammodul.</span><span class="sxs-lookup"><span data-stu-id="0c677-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="0c677-154">Illustrasjonen nedenfor viser hvordan du kan legge til et vurderingshistogram i listemodulen for produktvurderinger i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0c677-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Legge til en histogrammodul i en listemodulen for produktvurderinger](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="0c677-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0c677-156">Additional resources</span></span>

[<span data-ttu-id="0c677-157">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="0c677-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0c677-158">Containermodul</span><span class="sxs-lookup"><span data-stu-id="0c677-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0c677-159">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="0c677-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0c677-160">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="0c677-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0c677-161">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="0c677-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0c677-162">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="0c677-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0c677-163">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="0c677-163">Footer module</span></span>](author-footer-module.md)