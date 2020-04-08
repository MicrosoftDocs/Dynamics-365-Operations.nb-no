---
title: Vanlige spørsmål om produktanbefalinger
description: Dette emnet inneholder informasjon om prosesser og verktøy som du kan bruke til å feilsøke problemer som er knyttet til produktanbefalinger eller de tilhørende resultatene.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2e30d29516dff6b2128e21bfa6e449e396884d00
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154396"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="fe371-103">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe371-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fe371-104">Dette emnet inneholder informasjon om prosesser og verktøy som du kan bruke til å feilsøke problemer som er knyttet til [produktanbefalinger](product-recommendations.md) eller de tilhørende resultatene.</span><span class="sxs-lookup"><span data-stu-id="fe371-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="fe371-105">Anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="fe371-105">Best practices</span></span>
<span data-ttu-id="fe371-106">Det er svært viktig å bruke konseptet med produktstandarder og varianter.</span><span class="sxs-lookup"><span data-stu-id="fe371-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="fe371-107">Fornuftig gruppering av varianter til en overordnet produktstandard hjelper listealgoritmene og tjenesten med å opprette bedre modeller.</span><span class="sxs-lookup"><span data-stu-id="fe371-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="fe371-108">I tillegg kan tjenesten bare tjene én forekomst av et produkt i stedet for å legge inn alle nært relaterte varianter i en liste.</span><span class="sxs-lookup"><span data-stu-id="fe371-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="fe371-109">Når alle nært relaterte varianter plasseres i en liste, kan det oppstå feil eller duplikate resultater.</span><span class="sxs-lookup"><span data-stu-id="fe371-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="fe371-110">Hvorfor mangler produkter fra anbefalingslistene mine?</span><span class="sxs-lookup"><span data-stu-id="fe371-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="fe371-111">Hvis en vare mangler i en produktanbefalingsliste, kan det være et problem med produktkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe371-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="fe371-112">Det kan for eksempel hende at det finnes feil produktstartdato eller -sluttdato, at en dimensjon ikke er riktig konfigurert, eller at produktet ikke er i det riktige kanalsortimentet osv.</span><span class="sxs-lookup"><span data-stu-id="fe371-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="fe371-113">Hvis en vare mangler i en anbefalingsliste som er basert på kunstig intelligens-maskinopplæring (AI-ML), kan det hende at varen ikke passer til kriteriene i anbefalingslisten, eller at det ikke er nok kjøpstransaksjoner til at anbefalingslisten kan vises dem.</span><span class="sxs-lookup"><span data-stu-id="fe371-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="fe371-114">Vi anbefaler at du kontrollerer disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="fe371-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="fe371-115">**Kontroller at produktanbefalinger er aktivert i HK.**</span><span class="sxs-lookup"><span data-stu-id="fe371-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="fe371-116">Hvis du vil ha mer informasjon om hvordan du aktiverer denne tjenesten, kan du se [Aktiver produktanbefalinger](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="fe371-117">**Kontroller at det er angitt nøkkelproduktegenskaper.**</span><span class="sxs-lookup"><span data-stu-id="fe371-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="fe371-118">Produktsortimenter må for eksempel være angitt til **Inkluder**.</span><span class="sxs-lookup"><span data-stu-id="fe371-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="fe371-119">**For nyassorterte produkter kan det ta opptil 3 timer før produktet begynner å bli vist i den nye listen.**</span><span class="sxs-lookup"><span data-stu-id="fe371-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="fe371-120">**Hvis et produkt fremdeles ikke vises i Stjerneskudd, Bestselgere, Folk liker også eller Ofte kjøpt sammen, kan det hende at produktet ikke har nok transaksjoner.**</span><span class="sxs-lookup"><span data-stu-id="fe371-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="fe371-121">I dette tilfellet kan du enten vente på at flere transaksjoner skal forekomme, standard anbefalingslisteparameterne eller bruke manuell innblanding til å endre resultatene for anbefalingsproduktlisten.</span><span class="sxs-lookup"><span data-stu-id="fe371-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="fe371-122">Hvis du vil ha mer informasjon om anbefalingsparametere, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="fe371-123">**Sørg for at produktet oppfyller anbefalingskriteriene for listen.**</span><span class="sxs-lookup"><span data-stu-id="fe371-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="fe371-124">Hvis du vil ha mer informasjon om produktanbefalingsparametere, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="fe371-125">Hvordan kan jeg forhindre at det returneres dårlige anbefalinger?</span><span class="sxs-lookup"><span data-stu-id="fe371-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="fe371-126">Anbefalingslister krever et stort volum med transaksjoner for å gi resultater.</span><span class="sxs-lookup"><span data-stu-id="fe371-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="fe371-127">Derfor er det viktig at brukerne oppgir alle historiske transaksjonsdata.</span><span class="sxs-lookup"><span data-stu-id="fe371-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="fe371-128">I tillegg har produkter uten transaksjoner eller med få transaksjoner vanligvis ikke **Folk liker også**- eller **Ofte kjøpt sammen**-resultater, og de vises ikke i anbefalingslistene **Stjerneskudd** eller **Bestselgere**.</span><span class="sxs-lookup"><span data-stu-id="fe371-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="fe371-129">Denne situasjonen kan ofte oppstå for svært nye produkter eller for gamle produkter som ikke kjøpes så ofte.</span><span class="sxs-lookup"><span data-stu-id="fe371-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="fe371-130">Populære nye elementer har ikke dette problemet.</span><span class="sxs-lookup"><span data-stu-id="fe371-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="fe371-131">Vi anbefaler at du følger disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="fe371-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="fe371-132">**Sørg for at produktet oppfyller anbefalingskriteriene for denne listen.**</span><span class="sxs-lookup"><span data-stu-id="fe371-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="fe371-133">Hvis du vil ha mer informasjon om produktanbefalingsparametere, kan du se Endre resultater for AI-ML-basert produktanbefaling.</span><span class="sxs-lookup"><span data-stu-id="fe371-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="fe371-134">**Hvis produktet er nytt, kan du vurdere å endre en anbefalingsliste til produktet har flere transaksjoner.**</span><span class="sxs-lookup"><span data-stu-id="fe371-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="fe371-135">Hvis du vil ha mer informasjon om hvordan du endrer anbefalingslisteresultater, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="fe371-136">**Sørg for at produktet oppfyller anbefalingskriteriene for denne listen.**</span><span class="sxs-lookup"><span data-stu-id="fe371-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="fe371-137">Hvis du vil ha mer informasjon om produktanbefalingsparametere, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="fe371-138">**Hvis produktet er nytt, kan du vurdere å endre en anbefalingsliste til produktet har flere transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe371-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="fe371-139">Hvis du vil ha mer informasjon om hvordan du endrer anbefalingslisteresultater, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="fe371-140">Kan jeg fjerne et produkt, men likevel se det i butikken?</span><span class="sxs-lookup"><span data-stu-id="fe371-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="fe371-141">Du kan justere lister som genereres av algoritmer, hvis et forretningsbehov oppstår.</span><span class="sxs-lookup"><span data-stu-id="fe371-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="fe371-142">Hvis et produkt fjernes fra en anbefalingsliste, vil produktet imidlertid forbli synlig i butikken.</span><span class="sxs-lookup"><span data-stu-id="fe371-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="fe371-143">Hvis du vil ha mer informasjon om hvordan du endrer produktanbefalingsresultater, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="fe371-144">Hvis du må blokkere en vare fra å bli oppdaget i butikken, må du endre verdien for **Varesortimenter** til **Utelat**.</span><span class="sxs-lookup"><span data-stu-id="fe371-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="fe371-145">Hvordan legger jeg til en liste på en e-handelsside?</span><span class="sxs-lookup"><span data-stu-id="fe371-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="fe371-146">Hvis du vil ha informasjon om hvordan du legger til produktanbefalingssider på e-handelsområdet, se [Legge til lister over produktanbefalinger på sider](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="fe371-147">Hvordan aktiverer jeg anbefalinger for salgssted?</span><span class="sxs-lookup"><span data-stu-id="fe371-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="fe371-148">Når du har aktivert produktanbefalinger, må du legge til anbefalingspanelet til salgsstedets kontrollskjerm.</span><span class="sxs-lookup"><span data-stu-id="fe371-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="fe371-149">Hvis du vil ha mer informasjon, kan du se [Legge til en kontroll for anbefalinger på transaksjonsskjermen i POS-enheter](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="fe371-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe371-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fe371-150">Additional resources</span></span>

[<span data-ttu-id="fe371-151">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe371-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fe371-152">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="fe371-152">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="fe371-153">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe371-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="fe371-154">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe371-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="fe371-155">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe371-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="fe371-156">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="fe371-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="fe371-157">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="fe371-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fe371-158">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="fe371-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="fe371-159">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="fe371-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="fe371-160">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="fe371-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
