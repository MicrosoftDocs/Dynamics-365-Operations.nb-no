---
title: Behandle resultater for AI-ML-basert produktanbefaling
description: Dette emnet beskriver hvordan du skreddersyr produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770076"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="8d153-103">Behandle resultater for AI-ML-basert produktanbefaling</span><span class="sxs-lookup"><span data-stu-id="8d153-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8d153-104">Dette emnet beskriver hvordan du skreddersyr produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.</span><span class="sxs-lookup"><span data-stu-id="8d153-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="8d153-105">Når produktanbefalinger er aktivert, vil standardinnstillingene tre i kraft. Disse parameterne vil fungere for mange behov.</span><span class="sxs-lookup"><span data-stu-id="8d153-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="8d153-106">Det er best å planlegge å bruke litt tid på å vurdere om resultatene passer til salgsbevegelsen til produktene.</span><span class="sxs-lookup"><span data-stu-id="8d153-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="8d153-107">Vi foreslår å evaluere resultatene i noen dager før du endrer parameterne etter behov, før ny testing.</span><span class="sxs-lookup"><span data-stu-id="8d153-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="8d153-108">Forstå parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="8d153-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="8d153-109">Før du endrer parameterne, kan du lære om hvordan de påvirker resultatene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8d153-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="8d153-110">Tendenser-liste</span><span class="sxs-lookup"><span data-stu-id="8d153-110">Trending product list</span></span>

<span data-ttu-id="8d153-111">Produktlisten for **Tendenser** har to parametere som kan endres: ![Eksempel på standardparametere for Tendenser-liste](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="8d153-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="8d153-112">**Inkluder nye produkter fra siste X dager** – Produkter som er lagt til innen det angitte antallet dager før gjeldende dato, kan brukes til å velge produktkandidater.</span><span class="sxs-lookup"><span data-stu-id="8d153-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="8d153-113">Standardverdien i bildet foreslår at produkter som gamle har 180 dager, kan brukes i produktlisten for tendenser.</span><span class="sxs-lookup"><span data-stu-id="8d153-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="8d153-114">**Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="8d153-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="8d153-115">Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for trendvarer.</span><span class="sxs-lookup"><span data-stu-id="8d153-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="8d153-116">Produktliste for bestselgere</span><span class="sxs-lookup"><span data-stu-id="8d153-116">Best selling product list</span></span>

<span data-ttu-id="8d153-117">Avhengig av virksomheten kan bestselgere gi forskjellige resultater enn tendenser, selv om begge bruker transaksjonsdata til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="8d153-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="8d153-118">Siden bestselgere ikke er avkuttet basert på sortimentdato, kan bestselgere fremdeles utheve svært populære, eldre produkter som kan ha blitt slettet fra trendlisten.</span><span class="sxs-lookup"><span data-stu-id="8d153-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="8d153-119">Produktlisten for **Bestselgere** én parameter som kan endres:</span><span class="sxs-lookup"><span data-stu-id="8d153-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Eksempel standardparameter for bestselgerliste](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="8d153-121">**Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter.</span><span class="sxs-lookup"><span data-stu-id="8d153-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="8d153-122">Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for bestselgere.</span><span class="sxs-lookup"><span data-stu-id="8d153-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="8d153-123">Legge til eller fjerne produkter fra anbefalingslister manuelt</span><span class="sxs-lookup"><span data-stu-id="8d153-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="8d153-124">For nye produkter, tendenser og bestselgere</span><span class="sxs-lookup"><span data-stu-id="8d153-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="8d153-125">Gå til **Retail** > **Produktanbefalinger** > **Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="8d153-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="8d153-126">Velg **Anbefalingslister** i listen over delte parametere for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="8d153-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="8d153-127">Velg listen du vil legge til eller fjerne produkter fra.</span><span class="sxs-lookup"><span data-stu-id="8d153-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="8d153-128">Hvis du vil legge til produkter i tabellen, velger du **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="8d153-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="8d153-129">Under Produkt-kolonnen søker du etter et produkt etter **Navn** eller **Produktnummer.**
![Eksempel på søk etter produkt på listen Nytt produkt](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="8d153-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="8d153-130">Velg ett av to alternativer under Linjetype-kolonnen:</span><span class="sxs-lookup"><span data-stu-id="8d153-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="8d153-131">**Inkluder** – tvinger frem et produkt til fronten av listen</span><span class="sxs-lookup"><span data-stu-id="8d153-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="8d153-132">**Ekskluder** – fjerner et produkt fra å vises i listen ![Eksempel på å inkludere eller ekskludere et produkt fra Nytt produkt-listen](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="8d153-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="8d153-133">Når du endrer **Visningsrekkefølge**, endres visningsrekkefølgen for produkter merket **inkluder**, i listen.</span><span class="sxs-lookup"><span data-stu-id="8d153-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="8d153-134">Hvis to produkter har samme verdi for **visningsrekkefølge**, kan den endelige rekkefølgen for disse to resultatene avvike fra backoffice.</span><span class="sxs-lookup"><span data-stu-id="8d153-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="8d153-135">Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="8d153-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="8d153-136">For Folk liker også- eller Ofte kjøpt sammen-lister</span><span class="sxs-lookup"><span data-stu-id="8d153-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="8d153-137">Når det gjelder **Modell ofte kjøpt sammen**- eller **Folk liker også**-lister brukes maskinopplæring til å analysere forbrukskjøpsmønstre til å anbefale relaterte produkter som ofte kjøpes sammen for et unikt seed-produkt.</span><span class="sxs-lookup"><span data-stu-id="8d153-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="8d153-138">Et **seed-produkt** er produktet du vil generere resultater for.</span><span class="sxs-lookup"><span data-stu-id="8d153-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="8d153-139">I forbindelse med manuell justering av anbefalingslister, legger du til eller fjerner resultater for dette produktet.</span><span class="sxs-lookup"><span data-stu-id="8d153-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="8d153-140">Følg disse trinnene for å legge til eller fjerne resultater for et seed-produkt manuelt:</span><span class="sxs-lookup"><span data-stu-id="8d153-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="8d153-141">Velg **seed-produkt**.</span><span class="sxs-lookup"><span data-stu-id="8d153-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="8d153-142">Under **Produkt**-kolonnen søker du etter et produkt etter **Navn** eller **Produktnummer**.
![Eksempel på søk etter produkt på listen Ofte kjøpt sammen](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="8d153-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="8d153-143">Velg ett av to alternativer under **Linjetype**-kolonnen:</span><span class="sxs-lookup"><span data-stu-id="8d153-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="8d153-144">**Inkluder** – tvinger frem et produkt til fronten av listen</span><span class="sxs-lookup"><span data-stu-id="8d153-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="8d153-145">**Ekskluder** – fjerner et produkt fra å vises i listen</span><span class="sxs-lookup"><span data-stu-id="8d153-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="8d153-146">![Eksempel på å inkludere eller ekskludere et produkt på listen Ofte kjøpt sammen](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="8d153-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="8d153-147">Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg Fjern.</span><span class="sxs-lookup"><span data-stu-id="8d153-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8d153-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d153-148">Additional resources</span></span>

[<span data-ttu-id="8d153-149">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8d153-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8d153-150">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8d153-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8d153-151">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="8d153-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
