---
title: Justere resultater for AI-ML-basert produktanbefaling
description: Dette emnet beskriver hvordan du skreddersyr produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd9271c680b1f4248d6e60036f3e79d204dc3c2
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154347"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="6db5d-103">Justere resultater for AI-ML-basert produktanbefaling</span><span class="sxs-lookup"><span data-stu-id="6db5d-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6db5d-104">Dette emnet beskriver hvordan du justerer produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.</span><span class="sxs-lookup"><span data-stu-id="6db5d-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="6db5d-105">Når produktanbefalinger er aktivert, vil standardinnstillingene tre i kraft. Disse parameterne vil fungere for mange behov.</span><span class="sxs-lookup"><span data-stu-id="6db5d-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="6db5d-106">Det er best å planlegge å bruke litt tid på å vurdere om resultatene passer til salgsbevegelsen til produktene.</span><span class="sxs-lookup"><span data-stu-id="6db5d-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="6db5d-107">Vi foreslår å evaluere resultatene i noen dager før du endrer parameterne etter behov, før ny testing.</span><span class="sxs-lookup"><span data-stu-id="6db5d-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="6db5d-108">Forstå parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="6db5d-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="6db5d-109">Før du endrer parameterne, kan du lære om hvordan de påvirker resultatene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6db5d-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="6db5d-110">"Tendenser"-liste</span><span class="sxs-lookup"><span data-stu-id="6db5d-110">"Trending" product list</span></span>

<span data-ttu-id="6db5d-111">"Tendenser"-listen har to parametere som kan endres:</span><span class="sxs-lookup"><span data-stu-id="6db5d-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Eksempel på standardparametere for "Tendenser"-liste](./media/exampletrendingparameters.png)

1. <span data-ttu-id="6db5d-113">**Inkluder nye produkter fra siste X dager** – Produkter som er lagt til innen det angitte antallet dager før gjeldende dato, kan brukes til å velge produktkandidater.</span><span class="sxs-lookup"><span data-stu-id="6db5d-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="6db5d-114">Standardverdien i bildet foreslår at produkter som gamle har 180 dager, kan brukes i produktlisten for tendenser.</span><span class="sxs-lookup"><span data-stu-id="6db5d-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="6db5d-115">**Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="6db5d-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="6db5d-116">Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for trendvarer.</span><span class="sxs-lookup"><span data-stu-id="6db5d-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="6db5d-117">Produktliste for bestselgere</span><span class="sxs-lookup"><span data-stu-id="6db5d-117">"Best selling" product list</span></span>

<span data-ttu-id="6db5d-118">Avhengig av virksomheten kan bestselgerlisten gi forskjellige resultater enn tendenser, selv om begge bruker transaksjonsdata til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="6db5d-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="6db5d-119">Siden bestselgere ikke er avkuttet basert på sortimentdato, kan bestselgere fremdeles utheve svært populære, eldre produkter som kan ha blitt slettet fra trendlisten.</span><span class="sxs-lookup"><span data-stu-id="6db5d-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="6db5d-120">Produktlisten for "Bestselgere" har én parameter som kan endres:</span><span class="sxs-lookup"><span data-stu-id="6db5d-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Eksempel standardparameter for bestselgerliste](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="6db5d-122">**Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="6db5d-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="6db5d-123">Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for bestselgere.</span><span class="sxs-lookup"><span data-stu-id="6db5d-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="6db5d-124">Legge til eller fjerne produkter fra anbefalingslister manuelt</span><span class="sxs-lookup"><span data-stu-id="6db5d-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="6db5d-125">For listene "Nye produkter", "Tendenser" og "Bestselgere"</span><span class="sxs-lookup"><span data-stu-id="6db5d-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="6db5d-126">Gå til **Retail og Commerce** > **Produktanbefalinger** > **Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="6db5d-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="6db5d-127">Velg **Anbefalingslister** i listen over delte parametere.</span><span class="sxs-lookup"><span data-stu-id="6db5d-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="6db5d-128">Velg listen du vil legge til eller fjerne produkter fra.</span><span class="sxs-lookup"><span data-stu-id="6db5d-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="6db5d-129">Hvis du vil legge til produkter i tabellen, velger du **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="6db5d-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="6db5d-130">Under Produkt-kolonnen søker du etter et produkt etter **navn** eller **produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="6db5d-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Eksempel på å søke etter et produkt i den listen over nye produkter](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="6db5d-132">Velg ett av to alternativer under Linjetype-kolonnen:</span><span class="sxs-lookup"><span data-stu-id="6db5d-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="6db5d-133">**Inkluder** – tvinger frem et produkt til fronten av listen</span><span class="sxs-lookup"><span data-stu-id="6db5d-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="6db5d-134">**Ekskluder** – fjerner et produkt fra å vises i listen</span><span class="sxs-lookup"><span data-stu-id="6db5d-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Eksempel på å inkludere eller ekskludere et produkt fra listen over nye produkter](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="6db5d-136">Når du endrer **Visningsrekkefølge**, endres visningsrekkefølgen for produkter merket **inkluder**, i listen.</span><span class="sxs-lookup"><span data-stu-id="6db5d-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="6db5d-137">Hvis to produkter har samme verdi for **visningsrekkefølge**, kan den endelige rekkefølgen for disse to resultatene avvike fra backoffice.</span><span class="sxs-lookup"><span data-stu-id="6db5d-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="6db5d-138">Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="6db5d-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="6db5d-139">For "Folk liker også"- eller "Ofte kjøpt sammen"-lister</span><span class="sxs-lookup"><span data-stu-id="6db5d-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="6db5d-140">Når det gjelder "Ofte kjøpt sammen"- eller "Folk liker også"-lister brukes maskinopplæring til å analysere forbrukskjøpsmønstre til å anbefale relaterte produkter som ofte kjøpes sammen for et unikt seed-produkt.</span><span class="sxs-lookup"><span data-stu-id="6db5d-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="6db5d-141">Et *seed-produkt* er produktet du vil generere resultater for.</span><span class="sxs-lookup"><span data-stu-id="6db5d-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="6db5d-142">I forbindelse med manuell justering av anbefalingslister, legger du til eller fjerner resultater for dette produktet.</span><span class="sxs-lookup"><span data-stu-id="6db5d-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="6db5d-143">Følg disse trinnene for å legge til eller fjerne resultater for et seed-produkt manuelt:</span><span class="sxs-lookup"><span data-stu-id="6db5d-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="6db5d-144">Velg **seed-produkt**.</span><span class="sxs-lookup"><span data-stu-id="6db5d-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="6db5d-145">Under **Produkt**-kolonnen søker du etter et produkt etter **Navn** eller **Produktnummer**.
![Eksempel på søk etter produkt på listen Ofte kjøpt sammen](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="6db5d-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="6db5d-146">Velg ett av to alternativer under **Linjetype**-kolonnen:</span><span class="sxs-lookup"><span data-stu-id="6db5d-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="6db5d-147">**Inkluder** – tvinger frem et produkt til fronten av listen</span><span class="sxs-lookup"><span data-stu-id="6db5d-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="6db5d-148">**Ekskluder** – fjerner et produkt fra å vises i listen</span><span class="sxs-lookup"><span data-stu-id="6db5d-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="6db5d-149">![Eksempel på å inkludere eller ekskludere et produkt på listen Ofte kjøpt sammen](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="6db5d-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="6db5d-150">Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg Fjern.</span><span class="sxs-lookup"><span data-stu-id="6db5d-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6db5d-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6db5d-151">Additional resources</span></span>

[<span data-ttu-id="6db5d-152">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="6db5d-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6db5d-153">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="6db5d-153">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="6db5d-154">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="6db5d-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6db5d-155">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="6db5d-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="6db5d-156">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="6db5d-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="6db5d-157">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="6db5d-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="6db5d-158">Legge til anbefalinger i transaksjonsskjermbildet</span><span class="sxs-lookup"><span data-stu-id="6db5d-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="6db5d-159">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="6db5d-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6db5d-160">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="6db5d-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="6db5d-161">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="6db5d-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
