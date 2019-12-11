---
title: Konfigurere vurderinger og anmeldelser
description: Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770487"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="b3cb5-103">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="b3cb5-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b3cb5-104">Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b3cb5-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b3cb5-105">Overview</span></span>

<span data-ttu-id="b3cb5-106">Vurderinger og evalueringer på e-handelswebområder hjelper kunder med å lære om produkter før de tar en avgjørelse, ved å vise dem hva andre kunder mener om disse produktene.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="b3cb5-107">For webområder for e-handel er også vurderinger og gjennomganger en mekanisme for å samle kundetilbakemeldinger om produkter.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="b3cb5-108">Vurderingene vises på produktlistesider, kategorilistesider, sider for søkeresultater og andre områdesider.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="b3cb5-109">Vurderingshistogrammer og produktgjennomganger vises på sider for produktdetaljer (PDPer).</span><span class="sxs-lookup"><span data-stu-id="b3cb5-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="b3cb5-110">En **Skriv en vurdering**-knapp gir kundene muligheten til å sende inn rangeringer og omtaler for et produkt.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="b3cb5-111">Vurderings- og omtalemoduler på PDPer</span><span class="sxs-lookup"><span data-stu-id="b3cb5-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="b3cb5-112">Tre moduler viser vurderings- og omtalesammendraget på PDPer:</span><span class="sxs-lookup"><span data-stu-id="b3cb5-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="b3cb5-113">Modul for skriving av vurdering</span><span class="sxs-lookup"><span data-stu-id="b3cb5-113">Write review module</span></span>
- <span data-ttu-id="b3cb5-114">Listemodul for produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="b3cb5-114">Product reviews list module</span></span>
- <span data-ttu-id="b3cb5-115">Modul for vurderingshistogrammer</span><span class="sxs-lookup"><span data-stu-id="b3cb5-115">Ratings histogram module</span></span>
 
<span data-ttu-id="b3cb5-116">Illustrasjonen nedenfor viser hvordan vurderings- og evalueringsmodulene ser ut på en PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vurderings- og omtalemoduler på en PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="b3cb5-118">Hvis du vil ha informasjon om hvordan du optimaliserer PDP-maler og -oppsett slik at du kan dele konfigurasjonene for vurderings- og omtalemoduler mellom flere PDPer på e-handelsområdet, se [Oversikt over maler og oppsett](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b3cb5-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="b3cb5-119">Illustrasjonen nedenfor viser hvordan dialogboksen **Legg til modul** viser rangerings- og omtalemoduler i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Dialogboksen Legg til modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="b3cb5-121">Modul for omtaleskriving</span><span class="sxs-lookup"><span data-stu-id="b3cb5-121">Write review module</span></span>

<span data-ttu-id="b3cb5-122">Modulen for omtaleskriving inkluderer en **Skriv en vurdering**-knapp som lar brukere logge på, tilordne en vurdering og skrive en omtale av et produkt.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="b3cb5-123">Denne modulen lar også brukere redigere en vurdering eller omtale som de tidligere har sendt.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="b3cb5-124">Denne modulen vises vanligvis over listemodulene for vurderingshistogram og produktevalueringer på en PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="b3cb5-125">Følgende illustrasjon viser dialogboksen **Skriv en gjennomgang** som vises når en kunde velger **Skriv en vurdering**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="b3cb5-126">Kunden kan bruke denne dialogboksen til å sende inn en vurdering og en omtale.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Dialogboksen Skriv en vurdering](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="b3cb5-128">Tabellen nedenfor viser egenskapen for Skriv en vurdering-modulen som må konfigureres i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="b3cb5-129">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="b3cb5-129">Property name</span></span> | <span data-ttu-id="b3cb5-130">Verdi</span><span class="sxs-lookup"><span data-stu-id="b3cb5-130">Value</span></span>        | <span data-ttu-id="b3cb5-131">Egenskapsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b3cb5-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="b3cb5-132">Navn</span><span class="sxs-lookup"><span data-stu-id="b3cb5-132">Name</span></span>          | <span data-ttu-id="b3cb5-133">Skriv vurdering</span><span class="sxs-lookup"><span data-stu-id="b3cb5-133">Write review</span></span> | <span data-ttu-id="b3cb5-134">Navnet på Skriv en vurdering-modulen</span><span class="sxs-lookup"><span data-stu-id="b3cb5-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="b3cb5-135">Modul for vurderingshistogrammer</span><span class="sxs-lookup"><span data-stu-id="b3cb5-135">Ratings histogram module</span></span>

<span data-ttu-id="b3cb5-136">Modul for vurderingshistogrammer viser vurderingshistogrammet.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="b3cb5-137">Denne modulen vises vanligvis mellom Skriv vurdering-modulen og listemodulen for produktvurderinger på en PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="b3cb5-138">Histogrammodulen for vurderinger krever ingen konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="b3cb5-139">Du trenger bare å legge til modulen i PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="b3cb5-140">Illustrasjonene nedenfor viser hvordan en PDP-mal ser ut i Dynamics 365 Commerce når modulene for vurderinger og gjennomgang er konfigurert for visning på PDPer.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP-mal når vurderinger og omtaler er konfigurert for visning på PDPer](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="b3cb5-142">Listemodul for produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="b3cb5-142">Product reviews list module</span></span>

<span data-ttu-id="b3cb5-143">Listemodulen for produktvurderinger viser en liste over produktvurderinger sammen med alternativer for sortering, filtrering og paginering.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="b3cb5-144">Denne modulen vises vanligvis etter vurderingshistogrammodulen på en PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="b3cb5-145">Tabellen nedenfor viser egenskapene for listemodulen for produktvurderinger som må konfigureres i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="b3cb5-146">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="b3cb5-146">Property name</span></span>              | <span data-ttu-id="b3cb5-147">Verdi</span><span class="sxs-lookup"><span data-stu-id="b3cb5-147">Value</span></span> | <span data-ttu-id="b3cb5-148">Egenskapsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b3cb5-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="b3cb5-149">Omtaler som vises på hver side</span><span class="sxs-lookup"><span data-stu-id="b3cb5-149">Reviews shown on each page</span></span> | <span data-ttu-id="b3cb5-150">10</span><span class="sxs-lookup"><span data-stu-id="b3cb5-150">10</span></span>    | <span data-ttu-id="b3cb5-151">Antall omtaler som skal vises om gangen på en PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="b3cb5-152">Knappene **Neste** og **Forrige** er inkludert, slik at brukerne kan bla gjennom sidene med gjennomganger.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="b3cb5-153">Vurderingshistogram – sammendragsvisning</span><span class="sxs-lookup"><span data-stu-id="b3cb5-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="b3cb5-154">Listemodulen for produktvurderinger inneholder et spor der du kan legge til en vurderingshistogrammodul.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="b3cb5-155">Illustrasjonen nedenfor viser hvordan du kan legge til et vurderingshistogram i listemodulen for produktvurderinger i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Legge til en histogrammodul i en listemodulen for produktvurderinger](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="b3cb5-157">Konfigurere et område for å vise vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="b3cb5-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="b3cb5-158">Konfigurasjonsverdier for vurderinger og omtaler, for eksempel leie-ID, kontroll av tekstlengde og kontroll av tittellengde, konfigureres på områdenivå.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="b3cb5-159">Følg denne fremgangsmåten for å konfigurere et område for å vise vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="b3cb5-160">Gå til **Hjem \> Områder**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="b3cb5-161">Velg navnet på området ditt.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="b3cb5-162">Gå til **Områdebehandling \> Utvidelsesmulighet**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="b3cb5-163">I feltet for **Maksimal lengde for vurderingstekst** angir du maksimalt antall tegn som vurderingsteksten kan ha (for eksempel **1000**).</span><span class="sxs-lookup"><span data-stu-id="b3cb5-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="b3cb5-164">I feltet for **Maksimal lengde for vurderingstittel** angir du maksimalt antall tegn som vurderingstittelen kan ha (for eksempel **55**).</span><span class="sxs-lookup"><span data-stu-id="b3cb5-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="b3cb5-165">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="b3cb5-166">Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurere et område for å vise vurderinger og omtaler](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="b3cb5-168">Koble en produktvurdering til omtaledelen i en PDP</span><span class="sxs-lookup"><span data-stu-id="b3cb5-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="b3cb5-169">En produktvurdering vises under produkttittelen øverst i PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="b3cb5-170">Produktvurderingen kan konfigureres slik at den er koblet til **Vurderinger**-delen av samme PDP.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="b3cb5-171">Følg denne fremgangsmåten for å koble en produktomtale til **Vurderinger**-delen i PDPen:</span><span class="sxs-lookup"><span data-stu-id="b3cb5-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="b3cb5-172">Åpne PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="b3cb5-173">Gå til **Innstillinger for kjøpsboks-containermodul**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="b3cb5-174">Under **Kjøpsboks** velger du **Produktvurderinger**, og deretter merker du av for **Koble klikket til modul med full vurdering**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="b3cb5-175">Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Koble en produktvurdering til omtaledelen i en PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="b3cb5-177">Konfigurere koblingen for siden for personvern og policy</span><span class="sxs-lookup"><span data-stu-id="b3cb5-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="b3cb5-178">Følg disse trinnene for å konfigurere koblingen for siden for personvern og policy.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="b3cb5-179">Gå til **Hjem \> Områder**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="b3cb5-180">Velg navnet på området ditt.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="b3cb5-181">Gå til **Områdebehandling \> Utvidelsesmulighet**</span><span class="sxs-lookup"><span data-stu-id="b3cb5-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="b3cb5-182">I kategorien **Ruter**, under **Personvernpolicy for vurderinger og omtaler**, velger du **Legg til kobling**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="b3cb5-183">Hvis det allerede er angitt en kobling, og du vil erstatte den, velger du koblingen.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="b3cb5-184">Velg koblingen for siden for personvern og policy i dialogboksen **Legg til en kobling**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="b3cb5-185">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="b3cb5-186">Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3cb5-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurere koblingen for siden for personvern og policy](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="b3cb5-188">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b3cb5-188">Additional resources</span></span>

[<span data-ttu-id="b3cb5-189">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="b3cb5-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="b3cb5-190">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="b3cb5-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="b3cb5-191">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="b3cb5-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="b3cb5-192">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="b3cb5-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
