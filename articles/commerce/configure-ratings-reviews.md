---
title: Konfigurere vurderinger og anmeldelser
description: Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5161755b9e15e93fbb5eeb6404ea0820f7068ea7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796081"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="e3c7d-103">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="e3c7d-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3c7d-104">Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e3c7d-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e3c7d-105">Overview</span></span>

<span data-ttu-id="e3c7d-106">Vurderinger og evalueringer på e-handelswebområder hjelper kunder med å lære om produkter før de tar en avgjørelse, ved å vise dem hva andre kunder mener om disse produktene.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="e3c7d-107">For webområder for e-handel er også vurderinger og gjennomganger en mekanisme for å samle kundetilbakemeldinger om produkter.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="e3c7d-108">Konfigurere et område for å vise vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="e3c7d-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="e3c7d-109">Konfigurasjonsverdier for vurderinger og omtaler, for eksempel leie-ID, kontroll av tekstlengde og kontroll av tittellengde, konfigureres på områdenivå.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="e3c7d-110">Følg denne fremgangsmåten for å konfigurere et område for å vise vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="e3c7d-111">Gå til **Hjem \> Områder**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="e3c7d-112">Velg navnet på området ditt.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="e3c7d-113">Gå til **Områdeinnstillinger \> Tillegg**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="e3c7d-114">I feltet for **Maksimal lengde for vurderingstekst** angir du maksimalt antall tegn som vurderingsteksten kan ha (for eksempel **1000**).</span><span class="sxs-lookup"><span data-stu-id="e3c7d-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="e3c7d-115">I feltet for **Maksimal lengde for vurderingstittel** angir du maksimalt antall tegn som vurderingstittelen kan ha (for eksempel **55**).</span><span class="sxs-lookup"><span data-stu-id="e3c7d-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="e3c7d-116">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="e3c7d-117">Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurere et område for å vise vurderinger og omtaler](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="e3c7d-119">Koble en produktvurdering til omtaledelen i en PDP</span><span class="sxs-lookup"><span data-stu-id="e3c7d-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="e3c7d-120">En produktvurdering vises under produkttittelen øverst i PDP.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="e3c7d-121">Produktvurderingen kan konfigureres slik at den er koblet til **Vurderinger**-delen av samme PDP.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="e3c7d-122">Følg denne fremgangsmåten for å koble en produktomtale til **Vurderinger**-delen i PDPen:</span><span class="sxs-lookup"><span data-stu-id="e3c7d-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="e3c7d-123">Åpne PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="e3c7d-124">Gå til **Innstillinger for kjøpsboks-containermodul**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="e3c7d-125">Under **Kjøpsboks** velger du **Produktvurderinger**, og deretter merker du av for **Koble klikket til modul med full vurdering**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="e3c7d-126">Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Koble en produktvurdering til omtaledelen i en PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="e3c7d-128">Konfigurere koblingen for siden for personvern og policy</span><span class="sxs-lookup"><span data-stu-id="e3c7d-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="e3c7d-129">Følg disse trinnene for å konfigurere koblingen for siden for personvern og policy.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="e3c7d-130">Gå til **Hjem \> Områder**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="e3c7d-131">Velg navnet på området ditt.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="e3c7d-132">Gå til **Områdeinnstillinger \> Tillegg**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="e3c7d-133">I kategorien **Ruter**, under **Personvernpolicy for vurderinger og omtaler**, velger du **Legg til kobling**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="e3c7d-134">Hvis det allerede er angitt en kobling, og du vil erstatte den, velger du koblingen.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="e3c7d-135">Velg koblingen for siden for personvern og policy i dialogboksen **Legg til en kobling**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="e3c7d-136">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="e3c7d-137">Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3c7d-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurere koblingen for siden for personvern og policy](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="e3c7d-139">Konfigurere vurderings- og omtalemoduler på sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="e3c7d-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="e3c7d-140">Hvis du vil ha informasjon om hvordan du konfigurerer vurderings- og omtalemoduler på sider med produktdetaljer, kan du se [Vurderings- og omtalemoduler](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="e3c7d-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3c7d-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e3c7d-141">Additional resources</span></span>

[<span data-ttu-id="e3c7d-142">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="e3c7d-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="e3c7d-143">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="e3c7d-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="e3c7d-144">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="e3c7d-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="e3c7d-145">Konfigurere vurderings- og omtalemoduler på sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="e3c7d-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="e3c7d-146">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="e3c7d-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]