---
title: Aktiver anbefalinger av typen "kjøp lignende utseende"
description: Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende utseende" i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 06b5721c423330b8840bb546bdb144c3189c25bb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795387"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="51a90-103">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="51a90-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51a90-104">Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende utseende" i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51a90-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="51a90-105">Anbefalingsfunksjonen "kjøp lignende utseende" i Dynamics 365 Commerce bruker kraften i kunstig intelligens og maskinlærin (AI og ML) for å levere anbefalinger for visuelt liknende produkter til kunder.</span><span class="sxs-lookup"><span data-stu-id="51a90-105">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="51a90-106">Ved å gjøre anbefalinger av typen "kjøp lignende utseende" tilgjengelig for alle handelskanaler i Commerce, kan forhandlere øke kundetilfredsheten ved å bidra til at kundene enkelt finner det de ønsker.</span><span class="sxs-lookup"><span data-stu-id="51a90-106">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="51a90-107">Funksjonaliteten til anbefalinger av typen "kjøp lignende utseende" bruker produktbilder av utvalgte produktvarianter for å finne og anbefale visuelt lignende produkter i en forhandlers produktkatalog.</span><span class="sxs-lookup"><span data-stu-id="51a90-107">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="51a90-108">Anbefalinger av typen "kjøp lignende utseende" er tilgjengelige både ved salgssted og e-handel.</span><span class="sxs-lookup"><span data-stu-id="51a90-108">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="51a90-109">Eksempelscenarioer</span><span class="sxs-lookup"><span data-stu-id="51a90-109">Example scenarios</span></span>

- <span data-ttu-id="51a90-110">En kunde ser på en genser med svarte striper og får en anbefaling om en lignende genser i rødt.</span><span class="sxs-lookup"><span data-stu-id="51a90-110">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="51a90-111">Kunden velger det anbefalte produktet i stedet for det opprinnelig viste produktet, og mottar deretter anbefalinger for liknende produkter i rødt.</span><span class="sxs-lookup"><span data-stu-id="51a90-111">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="51a90-112">En kunde bruker anbefalinger av typen "kjøp lignende utseende" for å finne samsvarende øreringer for en ring som kunden er interessert i å kjøpe.</span><span class="sxs-lookup"><span data-stu-id="51a90-112">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="51a90-113">Aktivere anbefalinger av typen "kjøp lignende utseende" i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="51a90-113">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="51a90-114">Produktanbefalinger støttes bare for Commerce-brukere som har migrert beholdningen til Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="51a90-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="51a90-115">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="51a90-115">Prerequisites</span></span>

<span data-ttu-id="51a90-116">Før forhandlere kan begynne å vise anbefalinger av typen "kjøp lignende utseende" for kunder, er det to nødvendige trinn:</span><span class="sxs-lookup"><span data-stu-id="51a90-116">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="51a90-117">[Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="51a90-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="51a90-118">Kontroller at medieserveren støtter HTTPS-kall.</span><span class="sxs-lookup"><span data-stu-id="51a90-118">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="51a90-119">For at anbefalingsmotoren kan få tilgang til produktbildene, må forhandlere generere URL-adressene for produktene.</span><span class="sxs-lookup"><span data-stu-id="51a90-119">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="51a90-120">Følg denne fremgangsmåten for å generere URL-adresser for produkter i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="51a90-120">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="51a90-121">Gå til **Produktbilder**.</span><span class="sxs-lookup"><span data-stu-id="51a90-121">Go to **Product images**.</span></span>
1. <span data-ttu-id="51a90-122">Velg **Definer mal for medier** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="51a90-122">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="51a90-123">I egenskapsruten **Definer mal for medier**, under **URL-adresser for medier**, velger du **Generer URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="51a90-123">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="51a90-124">Når du aktiverer anbefalingsfunksjonen "kjøp likt utseende", starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="51a90-124">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="51a90-125">Det kan være nødvendig med opptil én dag før disse listene er tilgjengelige og synlige på Internett og salgsstedsterminaler.</span><span class="sxs-lookup"><span data-stu-id="51a90-125">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="51a90-126">Hvis du vil aktivere anbefalingsfunksjonen "kjøp lignende utseende" i Commerce Headquarters, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="51a90-126">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="51a90-127">Gå til **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="51a90-127">Go to **Feature management**.</span></span>
1. <span data-ttu-id="51a90-128">I listen over tilgjengelige funksjoner kan du søke etter og velge **Kjøp lignende utseende**.</span><span class="sxs-lookup"><span data-stu-id="51a90-128">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="51a90-129">Velg **Aktiver** i høyre rute for å aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="51a90-129">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="51a90-130">Illustrasjonen nedenfor viser funksjonen **Kjøp lignende utseende** på siden **Funksjonsbehandling** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="51a90-130">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Funksjonen Kjøp lignende utseende på siden Funksjonsbehandling i Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="51a90-132">Når de foregående oppgavene er fullført, forbedres POS-terminaler automatisk med et kontekstavhengig **Kjøp lignende produkter**-panelet.</span><span class="sxs-lookup"><span data-stu-id="51a90-132">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="51a90-133">Ved å velge **Se mer** kan brukere av salgsstedsterminaler tas til en dedikert "kjøp likt utseende"-side som kan filtreres ytterligere.</span><span class="sxs-lookup"><span data-stu-id="51a90-133">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="51a90-134">Hvis du slår av anbefalingsfunksjonen "kjøp lignende utseende", påvirkes ingen andre typer produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="51a90-134">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="51a90-135">Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="51a90-135">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="51a90-136">Legge til en knapp for kjøp lignende utseende på sider med produktdetaljer ved hjelp av Commerce-områdebygger</span><span class="sxs-lookup"><span data-stu-id="51a90-136">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="51a90-137">Når du har aktivert anbefalingsfunksjonen "kjøp likt utseende" i Commerce Headquarters, kan forhandlere bruke et alternativ i Commerce-områdebygger til å legge til knapp for **kjøp lignende utseende** i kjøpeboksen på en side med produktdetaljer (PDP).</span><span class="sxs-lookup"><span data-stu-id="51a90-137">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="51a90-138">En kunde som velger denne knappen, blir tatt med til en dedikert "kjøp likt utseende"-side som returnerer visuelt lignende produkter.</span><span class="sxs-lookup"><span data-stu-id="51a90-138">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="51a90-139">Der kan kunden kan bruke velgere til å filtrere varene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="51a90-139">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="51a90-140">Hvis du vil legge til en **Kjøp lignende utseende**-knapp for en PDP ved å bruke Commerce-områdebygger, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="51a90-140">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="51a90-141">Åpne en eksisterende områdebyggerside som inneholder en kjøpeboksmodul.</span><span class="sxs-lookup"><span data-stu-id="51a90-141">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="51a90-142">Velg produktsamlingsmodulen i den venstre kjøpeboksmodulen.</span><span class="sxs-lookup"><span data-stu-id="51a90-142">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="51a90-143">I den høyre navigasjonsruten merker du av for **Aktiver kobling til kjøp lignende utseende**.</span><span class="sxs-lookup"><span data-stu-id="51a90-143">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="51a90-144">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="51a90-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="51a90-145">Etter at siden er publisert, vil PDP inkludere en **Kjøp lignende utseende**-knapp.</span><span class="sxs-lookup"><span data-stu-id="51a90-145">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="51a90-146">Den følgende illustrasjonen viser avmerkingsboksen **Aktiver kobling til kjøp lignende utseende** og knappen **Kjøp lignende utseende** i et eksempel-PDP i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="51a90-146">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Avmerkingsboksen Aktiver kobling til kjøp lignende utseende og knappen Kjøp lignende utseende i et PDP i områdebyggeren.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="51a90-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="51a90-148">Additional resources</span></span>

[<span data-ttu-id="51a90-149">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="51a90-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="51a90-150">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="51a90-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="51a90-151">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="51a90-151">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="51a90-152">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="51a90-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="51a90-153">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="51a90-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="51a90-154">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="51a90-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="51a90-155">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="51a90-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="51a90-156">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="51a90-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="51a90-157">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="51a90-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="51a90-158">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="51a90-158">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
