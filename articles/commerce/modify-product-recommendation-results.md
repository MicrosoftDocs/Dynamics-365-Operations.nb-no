---
title: Justere resultater for AI-ML-basert produktanbefaling
description: Dette emnet beskriver hvordan du skreddersyr produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9e370faed7feb0640959a9fcc4b608f18f9ffc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263952"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="79a41-103">Justere resultater for AI-ML-basert produktanbefaling</span><span class="sxs-lookup"><span data-stu-id="79a41-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="79a41-104">Dette emnet beskriver hvordan du justerer produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.</span><span class="sxs-lookup"><span data-stu-id="79a41-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="79a41-105">Når produktanbefalinger er aktivert, vil standardinnstillingene tre i kraft. Disse parameterne vil fungere for mange behov.</span><span class="sxs-lookup"><span data-stu-id="79a41-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="79a41-106">Det er best å planlegge å bruke litt tid på å vurdere om resultatene passer til salgsbevegelsen til produktene.</span><span class="sxs-lookup"><span data-stu-id="79a41-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="79a41-107">Vi foreslår å evaluere resultatene i noen dager før du endrer parameterne etter behov, før ny testing.</span><span class="sxs-lookup"><span data-stu-id="79a41-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="79a41-108">Forstå parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="79a41-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="79a41-109">Før du endrer parameterne, kan du lære om hvordan de påvirker resultatene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="79a41-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="79a41-110">"Tendenser"-liste</span><span class="sxs-lookup"><span data-stu-id="79a41-110">"Trending" product list</span></span>

<span data-ttu-id="79a41-111">"Tendenser"-listen har to parametere som kan endres:</span><span class="sxs-lookup"><span data-stu-id="79a41-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Eksempel på standardparametere for "Tendenser"-liste](./media/exampletrendingparameters.png)

1. <span data-ttu-id="79a41-113">**Inkluder nye produkter fra siste X dager** – Produkter som er lagt til innen det angitte antallet dager før gjeldende dato, kan brukes til å velge produktkandidater.</span><span class="sxs-lookup"><span data-stu-id="79a41-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="79a41-114">Standardverdien i bildet foreslår at produkter som gamle har 180 dager, kan brukes i produktlisten for tendenser.</span><span class="sxs-lookup"><span data-stu-id="79a41-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="79a41-115">**Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="79a41-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="79a41-116">Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for trendvarer.</span><span class="sxs-lookup"><span data-stu-id="79a41-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="79a41-117">Produktliste for bestselgere</span><span class="sxs-lookup"><span data-stu-id="79a41-117">"Best selling" product list</span></span>

<span data-ttu-id="79a41-118">Avhengig av virksomheten kan bestselgerlisten gi forskjellige resultater enn tendenser, selv om begge bruker transaksjonsdata til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="79a41-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="79a41-119">Siden bestselgere ikke er avkuttet basert på sortimentdato, kan bestselgere fremdeles utheve svært populære, eldre produkter som kan ha blitt slettet fra trendlisten.</span><span class="sxs-lookup"><span data-stu-id="79a41-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="79a41-120">Produktlisten for "Bestselgere" har én parameter som kan endres:</span><span class="sxs-lookup"><span data-stu-id="79a41-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Eksempel standardparameter for bestselgerliste](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="79a41-122">**Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="79a41-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="79a41-123">Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for bestselgere.</span><span class="sxs-lookup"><span data-stu-id="79a41-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="79a41-124">Legge til eller fjerne produkter fra anbefalingslister manuelt</span><span class="sxs-lookup"><span data-stu-id="79a41-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="79a41-125">For listene "Nye produkter", "Tendenser" og "Bestselgere"</span><span class="sxs-lookup"><span data-stu-id="79a41-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="79a41-126">Gå til **Retail og Commerce** > **Produktanbefalinger** > **Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="79a41-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="79a41-127">Velg **Anbefalingslister** i listen over delte parametere.</span><span class="sxs-lookup"><span data-stu-id="79a41-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="79a41-128">Velg listen du vil legge til eller fjerne produkter fra.</span><span class="sxs-lookup"><span data-stu-id="79a41-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="79a41-129">Hvis du vil legge til produkter i tabellen, velger du **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="79a41-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="79a41-130">Under Produkt-kolonnen søker du etter et produkt etter **navn** eller **produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="79a41-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Eksempel på å søke etter et produkt i den listen over nye produkter](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="79a41-132">Velg ett av to alternativer under Linjetype-kolonnen:</span><span class="sxs-lookup"><span data-stu-id="79a41-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="79a41-133">**Inkluder** – tvinger frem et produkt til fronten av listen</span><span class="sxs-lookup"><span data-stu-id="79a41-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="79a41-134">**Ekskluder** – fjerner et produkt fra å vises i listen</span><span class="sxs-lookup"><span data-stu-id="79a41-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Eksempel på å inkludere eller ekskludere et produkt fra listen over nye produkter](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="79a41-136">Når du endrer **Visningsrekkefølge**, endres visningsrekkefølgen for produkter merket **inkluder**, i listen.</span><span class="sxs-lookup"><span data-stu-id="79a41-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="79a41-137">Hvis to produkter har samme verdi for **visningsrekkefølge**, kan den endelige rekkefølgen for disse to resultatene avvike fra backoffice.</span><span class="sxs-lookup"><span data-stu-id="79a41-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="79a41-138">Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="79a41-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="79a41-139">For "Folk liker også"- eller "Ofte kjøpt sammen"-lister</span><span class="sxs-lookup"><span data-stu-id="79a41-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="79a41-140">Når det gjelder "Ofte kjøpt sammen"- eller "Folk liker også"-lister brukes maskinopplæring til å analysere forbrukskjøpsmønstre til å anbefale relaterte produkter som ofte kjøpes sammen for et unikt seed-produkt.</span><span class="sxs-lookup"><span data-stu-id="79a41-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="79a41-141">Et *seed-produkt* er produktet du vil generere resultater for.</span><span class="sxs-lookup"><span data-stu-id="79a41-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="79a41-142">I forbindelse med manuell justering av anbefalingslister, legger du til eller fjerner resultater for dette produktet.</span><span class="sxs-lookup"><span data-stu-id="79a41-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="79a41-143">Følg disse trinnene for å legge til eller fjerne resultater for et seed-produkt manuelt:</span><span class="sxs-lookup"><span data-stu-id="79a41-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="79a41-144">Velg **seed-produkt**.</span><span class="sxs-lookup"><span data-stu-id="79a41-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="79a41-145">Under **Produkt**-kolonnen søker du etter et produkt etter **Navn** eller **Produktnummer**.
![Eksempel på søk etter produkt på listen Ofte kjøpt sammen](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="79a41-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="79a41-146">Velg ett av to alternativer under **Linjetype**-kolonnen:</span><span class="sxs-lookup"><span data-stu-id="79a41-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="79a41-147">**Inkluder** – tvinger frem et produkt til fronten av listen</span><span class="sxs-lookup"><span data-stu-id="79a41-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="79a41-148">**Ekskluder** – fjerner et produkt fra å vises i listen</span><span class="sxs-lookup"><span data-stu-id="79a41-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="79a41-149">![Eksempel på å inkludere eller ekskludere et produkt på listen Ofte kjøpt sammen](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="79a41-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="79a41-150">Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg Fjern.</span><span class="sxs-lookup"><span data-stu-id="79a41-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="79a41-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="79a41-151">Additional resources</span></span>

[<span data-ttu-id="79a41-152">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="79a41-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="79a41-153">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="79a41-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="79a41-154">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="79a41-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="79a41-155">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="79a41-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="79a41-156">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="79a41-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="79a41-157">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="79a41-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="79a41-158">Legge til produktanbefalinger på salgssted</span><span class="sxs-lookup"><span data-stu-id="79a41-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="79a41-159">Legge til anbefalinger i transaksjonsskjermbildet</span><span class="sxs-lookup"><span data-stu-id="79a41-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="79a41-160">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="79a41-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="79a41-161">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="79a41-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="79a41-162">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="79a41-162">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]