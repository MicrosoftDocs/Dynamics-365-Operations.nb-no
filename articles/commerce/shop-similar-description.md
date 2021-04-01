---
title: Aktivere "kjøp med lignende beskrivelse"-anbefalinger
description: Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende beskrivelse" i Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234395"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="de3c9-103">Aktivere anbefalinger av typen Kjøp lignende beskrivelse</span><span class="sxs-lookup"><span data-stu-id="de3c9-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de3c9-104">Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende beskrivelse" i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="de3c9-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="de3c9-105">Anbefalingsfunksjonen "kjøp med lignende beskrivelse" i Dynamics 365 Commerce bruker kunstig intelligens og maskinlæring (AI og ML) for å levere anbefalinger for produkter med lignende beskrivelser som produktet kunden ser etter.</span><span class="sxs-lookup"><span data-stu-id="de3c9-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="de3c9-106">Ved å gjøre anbefalinger av typen "kjøp med lignende beskrivelse" tilgjengelig for alle handelskanaler i Commerce, kan forhandlere hjelpe kunder med å enkelt finner det de ønsker.</span><span class="sxs-lookup"><span data-stu-id="de3c9-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="de3c9-107">Funksjonaliteten til anbefalinger av typen "kjøp med lignende beskrivelse" bruker produktnavnet og -beskrivelsen av utvalgte produkter til å finne og anbefale visuelt lignende produkter i en forhandlers produktkatalog.</span><span class="sxs-lookup"><span data-stu-id="de3c9-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="de3c9-108">Anbefalinger av typen "kjøp med lignende beskrivelse" er tilgjengelige både på salgsstedet og i e-handelsopplevelser.</span><span class="sxs-lookup"><span data-stu-id="de3c9-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="de3c9-109">Eksempelscenarioer</span><span class="sxs-lookup"><span data-stu-id="de3c9-109">Example scenarios</span></span>

<span data-ttu-id="de3c9-110">Følgende eksempelscenarier viser anbefalingstypene som funksjonaliteten "kjøp med lignende beskrivelse" kan tilby:</span><span class="sxs-lookup"><span data-stu-id="de3c9-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="de3c9-111">En kunde ser et par retro hornbriller og mottar anbefalinger for andre briller med lignende utforming i sammenheng med forhandlerens bransje.</span><span class="sxs-lookup"><span data-stu-id="de3c9-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="de3c9-112">En kunde bruker "kjøp med lignende beskrivelse"-anbefalinger til å oppdage kaffesmaker som ligner på en smak de har kjøpt fra forhandleren tidligere.</span><span class="sxs-lookup"><span data-stu-id="de3c9-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="de3c9-113">Opprette "kjøp med lignende beskrivelse"-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="de3c9-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="de3c9-114">Produktanbefalinger støttes bare for Commerce-brukere som har migrert beholdningen til Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="de3c9-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="de3c9-115">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="de3c9-115">Prerequisites</span></span>

<span data-ttu-id="de3c9-116">Før "kjøp med lignende beskrivelse"-anbefalinger kan vises til kunder, må du fullføre følgende forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="de3c9-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="de3c9-117">[Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="de3c9-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="de3c9-118">Kontroller at medieserveren støtter HTTPS-kall.</span><span class="sxs-lookup"><span data-stu-id="de3c9-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="de3c9-119">Aktivere funksjonen for "kjøp med lignende beskrivelse"-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="de3c9-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="de3c9-120">Hvis du vil aktivere anbefalingsfunksjonen "kjøp med lignende beskrivelse" i Commerce Headquarters, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="de3c9-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="de3c9-121">I listen over tilgjengelige funksjoner i arbeidsområdet for **Funksjonsbehandling** kan du søke etter og velge **kjøp med lignende beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="de3c9-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="de3c9-122">Velg **Aktiver** i høyre rute.</span><span class="sxs-lookup"><span data-stu-id="de3c9-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="de3c9-123">Når du slår på funksjonen, begynner systemet å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="de3c9-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="de3c9-124">Det kan ta opptil en dag for disse listene å bli tilgjengelige og synlige på Internett og salgsstedsterminaler.</span><span class="sxs-lookup"><span data-stu-id="de3c9-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="de3c9-125">Hvis du deaktiverer funksjonen, påvirkes ikke andre typer produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="de3c9-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="de3c9-126">Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="de3c9-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="de3c9-127">Legge til en Kjøp med lignende beskrivelse-knapp på produktdetaljersiden</span><span class="sxs-lookup"><span data-stu-id="de3c9-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="de3c9-128">Når du har aktivert anbefalingsfunksjonen "kjøp med lignende beskrivelse" i Commerce Headquarters, kan du legge til en knapp for **kjøp med lignende beskrivelse** i kjøpeboksen på en side med produktdetaljer (PDP).</span><span class="sxs-lookup"><span data-stu-id="de3c9-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="de3c9-129">En kunde som velger denne knappen, blir tatt med til en dedikert **Kjøp med lignende beskrivelse**-side som viser visuelt lignende produkter.</span><span class="sxs-lookup"><span data-stu-id="de3c9-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="de3c9-130">Kunden kan deretter bruke velgere til å filtrere varene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="de3c9-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="de3c9-131">Hvis du vil legge til en **Kjøp med lignende beskrivelse**-knapp for en PDP ved å bruke Commerce-områdebygger, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="de3c9-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de3c9-132">Åpne en eksisterende områdebyggerside som inneholder en kjøpeboksmodul.</span><span class="sxs-lookup"><span data-stu-id="de3c9-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="de3c9-133">Velg produktsamlingsmodulen i den venstre kjøpeboksmodulen.</span><span class="sxs-lookup"><span data-stu-id="de3c9-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="de3c9-134">I den høyre ruten merker du av for **Aktiver kobling til kjøp med lignende beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="de3c9-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="de3c9-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="de3c9-135">Select **Save**.</span></span>
1. <span data-ttu-id="de3c9-136">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="de3c9-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="de3c9-137">Etter at siden er publisert, vil PDP inkludere en **Kjøp med lignende beskrivelse**-knapp.</span><span class="sxs-lookup"><span data-stu-id="de3c9-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="de3c9-138">Den følgende illustrasjonen viser avmerkingsboksen **Aktiver kobling til kjøp med lignende beskrivelse** og knappen **Kjøp med lignende beskrivelse** i et eksempel-PDP i områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="de3c9-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Avmerkingsboksen Aktiver kobling til kjøp med lignende beskrivelse og knappen Kjøp med lignende beskrivelse på en PDP i områdebyggeren](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="de3c9-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="de3c9-140">Additional resources</span></span>

[<span data-ttu-id="de3c9-141">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="de3c9-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="de3c9-142">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="de3c9-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="de3c9-143">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="de3c9-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="de3c9-144">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="de3c9-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="de3c9-145">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="de3c9-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="de3c9-146">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="de3c9-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="de3c9-147">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="de3c9-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]