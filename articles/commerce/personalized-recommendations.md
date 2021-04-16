---
title: Aktivere personlige produktanbefalinger
description: Dette emnet beskriver hvordan du gjør tilpassede produktanbefalinger tilgjengelig for kunder i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804435"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="6c251-103">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="6c251-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c251-104">Dette emnet beskriver hvordan du gjør tilpassede produktanbefalinger tilgjengelig for kunder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c251-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6c251-105">I Dynamics 365 Commerce kan forhandlere få tilpassede produktanbefalinger (også kjent som personalisering).</span><span class="sxs-lookup"><span data-stu-id="6c251-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="6c251-106">På denne måten kan tilpassede anbefalinger bygges inn i kundeopplevelsen på nettet og ved salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="6c251-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="6c251-107">Når funksjonaliteten for personalisering er aktivert, kan systemet tilknytte en brukers innkjøps- og produktinformasjon, slik at de genererer indivduelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="6c251-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="6c251-108">Forhåndskrav for personlige tilpasninger</span><span class="sxs-lookup"><span data-stu-id="6c251-108">Personalization prerequisites</span></span>

<span data-ttu-id="6c251-109">Før du kan lage tilpassede produktanbefalinger som er tilgjengelige for kundene, bør du være oppmerksom på at produktanbefalinger bare støttes for Commerce-brukere som har migrert lagringsplassen til Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6c251-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="6c251-110">Før kunder kan motta personlige produktanbefalinger, må forhandlere [aktivere produktanbefalinger](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6c251-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6c251-111">Ved å aktivere produktanbefalinger aktiverer du også personalisering.</span><span class="sxs-lookup"><span data-stu-id="6c251-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="6c251-112">Hvis du imidlertid deaktiverer personalisering, deaktiverer du ikke de andre typene produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="6c251-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="6c251-113">Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6c251-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="6c251-114">Aktivere tilpassing</span><span class="sxs-lookup"><span data-stu-id="6c251-114">Turn on personalization</span></span>

<span data-ttu-id="6c251-115">Følg denne fremgangsmåten for å aktivere tilpassing.</span><span class="sxs-lookup"><span data-stu-id="6c251-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="6c251-116">I Commerce Headquarters søker du etter **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="6c251-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="6c251-117">Velg **Alle** for å vise en liste over tilgjengelige funksjoner.</span><span class="sxs-lookup"><span data-stu-id="6c251-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="6c251-118">Skriv inn **Anbefalinger** i søkeboksen.</span><span class="sxs-lookup"><span data-stu-id="6c251-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="6c251-119">Velg funksjonen **Personlige produktanbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="6c251-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="6c251-120">I egenskapsruten **Personlige produktanbefalinger** velger du **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="6c251-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Aktivere tilpassing](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="6c251-122">Når du aktiverer tilpassing, startes prosessen for generering av tilpassede produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="6c251-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="6c251-123">Det kan være nødvendig med opptil én dag før listene er tilgjengelige og synlige på Internett og salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6c251-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="6c251-124">Tilpassede lister</span><span class="sxs-lookup"><span data-stu-id="6c251-124">Personalized lists</span></span>

<span data-ttu-id="6c251-125">I tillegg til å tillate tilpassing av eksisterende, maskingenererte lister kan du bruke anbefalingstjenesten til å tilpasse produktgjenkjenningsopplevelsen både på Internett og salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6c251-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="6c251-126">Når tilpassing er aktivert, kan forhandlere vise personlige lister av typen "Plukkinger for deg" eller "Anbefalt for kunder" på salgsstedsterminaler.</span><span class="sxs-lookup"><span data-stu-id="6c251-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="6c251-127">I tillegg kan forhandlere bruke tilpassing på eksisterende produktanbefalingslister og gi bortvalgsopplevelser som følger EUs personvernforordning, til godkjente brukere.</span><span class="sxs-lookup"><span data-stu-id="6c251-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="6c251-128">Hvis du deaktiverer tilpassing, deaktiverer du også disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="6c251-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="6c251-129">"Plukkinger for deg"-lister på Internett</span><span class="sxs-lookup"><span data-stu-id="6c251-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="6c251-130">En "Plukkinger for deg"-liste er en liste basert på kunstig intelligens og maskinlæring som viser en godkjent bruker en personlig tilpasset liste over foreslåtte produkter.</span><span class="sxs-lookup"><span data-stu-id="6c251-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="6c251-131">Denne listen er basert på brukerens kjøpshistorikk i omnikanalen.</span><span class="sxs-lookup"><span data-stu-id="6c251-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="6c251-132">Tilpassede anbefalinger oppdateres dynamisk etter hvert som brukeren gjør flere kjøp.</span><span class="sxs-lookup"><span data-stu-id="6c251-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="6c251-133">Denne listetypen støtter også kategorifiltrering, slik at forhandlerne kan vise populære valg basert på navigasjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="6c251-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="6c251-134">Før "Plukkinger for deg"-listen kan vises på en e-handelsside, må følgende brukerkrav oppfylles:</span><span class="sxs-lookup"><span data-stu-id="6c251-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="6c251-135">Brukere må være logget på.</span><span class="sxs-lookup"><span data-stu-id="6c251-135">Users must be signed in.</span></span> <span data-ttu-id="6c251-136">Anonyme brukere kan ikke se tilpassede anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="6c251-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="6c251-137">Brukere må ha minst ett innkjøp på kontoen.</span><span class="sxs-lookup"><span data-stu-id="6c251-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="6c251-138">Brukere må velge å motta personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="6c251-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="6c251-139">Illustrasjonen nedenfor viser et eksempel på en "Plukkinger for deg"-liste på en nettbutikkside.</span><span class="sxs-lookup"><span data-stu-id="6c251-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

!["Plukkinger for deg"-liste på Internett](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="6c251-141">"Anbefalt for kunde"-lister på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="6c251-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="6c251-142">For å forbedre klientopplevelsen kan forhandlerne personliggjøre eksisterende kundedetaljsider ved å legge til en kontekstbasert "Anbefalt for kunde"-liste.</span><span class="sxs-lookup"><span data-stu-id="6c251-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="6c251-143">Illustrasjonen nedenfor viser et eksempel på en "Anbefalt for kunde"-liste på en salgsstedsterminal.</span><span class="sxs-lookup"><span data-stu-id="6c251-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

!["Anbefalt for kunde"-liste på salgsstedet](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="6c251-145">Bruke tilpassing på eksisterende anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="6c251-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="6c251-146">Forhandlere kan bruke tilpassing for eksisterende anbefalingslister, for eksempel "Ny", "Tendenser", "Besteselgere", "Andre liker også" og "Ofte kjøpt sammen".</span><span class="sxs-lookup"><span data-stu-id="6c251-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="6c251-147">Når tilpassing brukes på eksisterende lister, fjernes varer som en pålogget bruker tidligere har kjøpt, fra disse listene.</span><span class="sxs-lookup"><span data-stu-id="6c251-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="6c251-148">For både anonyme brukere og brukere som har valgt bort mottak av tilpasssede anbefalinger, vises standardversjoner av de eksisterende listene.</span><span class="sxs-lookup"><span data-stu-id="6c251-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="6c251-149">Derfor trenger ikke forhandlere å opprettholde separate sideopplevelser manuelt.</span><span class="sxs-lookup"><span data-stu-id="6c251-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="6c251-150">En pålogget bruker har for eksempel allerede kjøpt den svarte klokken og de brune arbeidsstøvlene som vises i listen "Tendenser – standard" i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="6c251-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="6c251-151">Derfor vil brukeren se nye produkter i stedet for disse produktene, som vist i listen "Tendenser – tilpasset".</span><span class="sxs-lookup"><span data-stu-id="6c251-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Bruke tilpassing](./media/applypersonalization.png)

<span data-ttu-id="6c251-153">Hvis du vil bruke tilpassing på en eksisterende anbefalingsliste i områdebygger for handel, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6c251-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6c251-154">Åpne en eksisterende områdebyggerside som inneholder en produktsamlingsmodul.</span><span class="sxs-lookup"><span data-stu-id="6c251-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="6c251-155">Velg produktsamlingsmodulen i den venstre navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="6c251-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="6c251-156">Velg listen i den høyre navigasjonsruten under **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="6c251-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="6c251-157">I dialogboksen **Velg produktlistekonfigurasjon**, under **Type**, velger du listetypen.</span><span class="sxs-lookup"><span data-stu-id="6c251-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="6c251-158">Merk av for **Bruk tilpassing**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c251-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Bruke tilpassing på en tendensliste](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="6c251-160">Lagre siden, fullfør redigeringen av den, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="6c251-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="6c251-161">Når siden er publisert, vil påloggede brukere se tilpassede tendenslister.</span><span class="sxs-lookup"><span data-stu-id="6c251-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c251-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6c251-162">Additional resources</span></span>

[<span data-ttu-id="6c251-163">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="6c251-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6c251-164">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="6c251-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="6c251-165">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="6c251-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6c251-166">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="6c251-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="6c251-167">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="6c251-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="6c251-168">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="6c251-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="6c251-169">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="6c251-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="6c251-170">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="6c251-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6c251-171">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="6c251-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6c251-172">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="6c251-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="6c251-173">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="6c251-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
