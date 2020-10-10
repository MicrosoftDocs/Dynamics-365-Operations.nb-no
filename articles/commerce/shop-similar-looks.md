---
title: Aktiver anbefalinger av typen "kjøp lignende utseende"
description: Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende utseende" i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818380"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="3f6f4-103">Aktiver anbefalinger av typen "kjøp lignende utseende"</span><span class="sxs-lookup"><span data-stu-id="3f6f4-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f6f4-104">Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende utseende" i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f6f4-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="3f6f4-105">Overview</span></span>

<span data-ttu-id="3f6f4-106">Anbefalingsfunksjonen "kjøp lignende utseende" i Dynamics 365 Commerce bruker kraften i kunstig intelligens og maskinlærin (AI og ML) for å levere anbefalinger for visuelt liknende produkter til kunder.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="3f6f4-107">Ved å gjøre anbefalinger av typen "kjøp lignende utseende" tilgjengelig for alle handelskanaler i Commerce, kan forhandlere øke kundetilfredsheten ved å bidra til at kundene enkelt finner det de ønsker.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="3f6f4-108">Funksjonaliteten til anbefalinger av typen "kjøp lignende utseende" bruker produktbilder av utvalgte produktvarianter for å finne og anbefale visuelt lignende produkter i en forhandlers produktkatalog.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="3f6f4-109">Anbefalinger av typen "kjøp lignende utseende" er tilgjengelige både ved salgssted og e-handel.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="3f6f4-110">Eksempelscenarioer</span><span class="sxs-lookup"><span data-stu-id="3f6f4-110">Example scenarios</span></span>

- <span data-ttu-id="3f6f4-111">En kunde ser på en genser med svarte striper og får en anbefaling om en lignende genser i rødt.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="3f6f4-112">Kunden velger det anbefalte produktet i stedet for det opprinnelig viste produktet, og mottar deretter anbefalinger for liknende produkter i rødt.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="3f6f4-113">En kunde bruker anbefalinger av typen "kjøp lignende utseende" for å finne samsvarende øreringer for en ring som kunden er interessert i å kjøpe.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="3f6f4-114">Aktivere anbefalinger av typen "kjøp lignende utseende" i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="3f6f4-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="3f6f4-115">Produktanbefalinger støttes bare for Commerce-brukere som har migrert beholdningen til Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3f6f4-116">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="3f6f4-116">Prerequisites</span></span>

<span data-ttu-id="3f6f4-117">Før forhandlere kan begynne å vise anbefalinger av typen "kjøp lignende utseende" for kunder, er det to nødvendige trinn:</span><span class="sxs-lookup"><span data-stu-id="3f6f4-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="3f6f4-118">[Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="3f6f4-119">Kontroller at medieserveren støtter HTTPS-kall.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="3f6f4-120">For at anbefalingsmotoren kan få tilgang til produktbildene, må forhandlere generere URL-adressene for produktene.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="3f6f4-121">Følg denne fremgangsmåten for å generere URL-adresser for produkter i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3f6f4-122">Gå til **Produktbilder**.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="3f6f4-123">Velg **Definer mal for medier** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="3f6f4-124">I egenskapsruten **Definer mal for medier**, under **URL-adresser for medier**, velger du **Generer URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="3f6f4-125">Når du aktiverer anbefalingsfunksjonen "kjøp likt utseende", starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="3f6f4-126">Det kan være nødvendig med opptil én dag før disse listene er tilgjengelige og synlige på Internett og salgsstedsterminaler.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="3f6f4-127">Hvis du vil aktivere anbefalingsfunksjonen "kjøp lignende utseende" i Commerce Headquarters, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3f6f4-128">Gå til **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="3f6f4-129">I listen over tilgjengelige funksjoner kan du søke etter og velge **Kjøp lignende utseende**.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="3f6f4-130">Velg **Aktiver** i høyre rute for å aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="3f6f4-131">Illustrasjonen nedenfor viser funksjonen **Kjøp lignende utseende** på siden **Funksjonsbehandling** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Funksjonen Kjøp lignende utseende på siden Funksjonsbehandling i Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="3f6f4-133">Når de foregående oppgavene er fullført, forbedres POS-terminaler automatisk med et kontekstavhengig **Kjøp lignende produkter**-panelet.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="3f6f4-134">Ved å velge **Se mer** kan brukere av salgsstedsterminaler tas til en dedikert "kjøp likt utseende"-side som kan filtreres ytterligere.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="3f6f4-135">Hvis du slår av anbefalingsfunksjonen "kjøp lignende utseende", påvirkes ingen andre typer produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="3f6f4-136">Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3f6f4-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="3f6f4-137">Legge til en knapp for kjøp lignende utseende på sider med produktdetaljer ved hjelp av Commerce-områdebygger</span><span class="sxs-lookup"><span data-stu-id="3f6f4-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="3f6f4-138">Når du har aktivert anbefalingsfunksjonen "kjøp likt utseende" i Commerce Headquarters, kan forhandlere bruke et alternativ i Commerce-områdebygger til å legge til knapp for **kjøp lignende utseende** i kjøpeboksen på en side med produktdetaljer (PDP).</span><span class="sxs-lookup"><span data-stu-id="3f6f4-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="3f6f4-139">En kunde som velger denne knappen, blir tatt med til en dedikert "kjøp likt utseende"-side som returnerer visuelt lignende produkter.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="3f6f4-140">Der kan kunden kan bruke velgere til å filtrere varene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="3f6f4-141">Hvis du vil legge til en **Kjøp lignende utseende**-knapp for en PDP ved å bruke Commerce-områdebygger, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3f6f4-142">Åpne en eksisterende områdebyggerside som inneholder en kjøpeboksmodul.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="3f6f4-143">Velg produktsamlingsmodulen i den venstre kjøpeboksmodulen.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="3f6f4-144">I den høyre navigasjonsruten merker du av for **Aktiver kobling til kjøp lignende utseende**.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="3f6f4-145">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="3f6f4-146">Etter at siden er publisert, vil PDP inkludere en **Kjøp lignende utseende**-knapp.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="3f6f4-147">Den følgende illustrasjonen viser avmerkingsboksen **Aktiver kobling til kjøp lignende utseende** og knappen **Kjøp lignende utseende** i et eksempel-PDP i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="3f6f4-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Avmerkingsboksen Aktiver kobling til kjøp lignende utseende og knappen Kjøp lignende utseende i et PDP i områdebyggeren.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="3f6f4-149">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3f6f4-149">Additional resources</span></span>

[<span data-ttu-id="3f6f4-150">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f6f4-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3f6f4-151">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="3f6f4-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="3f6f4-152">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f6f4-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3f6f4-153">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f6f4-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="3f6f4-154">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="3f6f4-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="3f6f4-155">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="3f6f4-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3f6f4-156">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="3f6f4-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3f6f4-157">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="3f6f4-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3f6f4-158">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="3f6f4-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3f6f4-159">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f6f4-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
