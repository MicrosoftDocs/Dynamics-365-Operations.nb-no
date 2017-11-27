---
title: Oversikt over personlige produktanbefalinger
description: Dette emnet inneholder informasjon om Dynamics 365 for Retail-produktanbefalingene som kan vises salgsstedsenheten.
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 942d6225a46b108ea39d3b8e4376b644c128ae6d
ms.contentlocale: nb-no
ms.lasthandoff: 11/14/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="e5439-103">Oversikt over personlige produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e5439-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="e5439-104">Denne funksjonen er for tiden tilgjengelig bare for sandkasse og produksjons (høy tilgjengelighet) -distribusjonstopologier.</span><span class="sxs-lookup"><span data-stu-id="e5439-104">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="e5439-105">Produktanbefalingene kan vises i Dynamics 365 for Retail på salgsstedsenheten.</span><span class="sxs-lookup"><span data-stu-id="e5439-105">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="e5439-106">Anbefalingene er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="e5439-106">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="e5439-107">For forhandlere med store kataloger bidrar anbefalinger kunden med å oppdage produkter.</span><span class="sxs-lookup"><span data-stu-id="e5439-107">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="e5439-108">Ved å presentere produkter som er rettet mot en kundes interesser og kjøpsvaner, kan produktanbefalinger bidra til mersalg og kryssalg for forhandlere og forbedring av kundebevaring.</span><span class="sxs-lookup"><span data-stu-id="e5439-108">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="e5439-109">I Dynamics 365 for Retail er produktanbefalingene drevet av kognitive tjenester og Microsoft Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="e5439-109">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="e5439-110">Scenarier</span><span class="sxs-lookup"><span data-stu-id="e5439-110">Scenarios</span></span>
---------

<span data-ttu-id="e5439-111">Produktanbefalingene er aktivert for følgende POS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="e5439-111">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="e5439-112">De er tilgjengelige i Cloud POS eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="e5439-112">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="e5439-113">På **Produktdetaljer**-siden:</span><span class="sxs-lookup"><span data-stu-id="e5439-113">On the **Product details** page:</span></span>

-   <span data-ttu-id="e5439-114">Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingsmotoren flere varer som sannsynligvis kjøpes sammen.</span><span class="sxs-lookup"><span data-stu-id="e5439-114">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="e5439-115">Hvis den butikkansatte legger til en kunde i transaksjonen og deretter går til en **Produktdetaljer**-side, gir anbefalingsmotoren anbefalinger ved hjelp av kundens transaksjonshistorikk.</span><span class="sxs-lookup"><span data-stu-id="e5439-115">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="e5439-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="e5439-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="e5439-117">På **Transaksjon**-siden:</span><span class="sxs-lookup"><span data-stu-id="e5439-117">On the **Transaction** page:</span></span>

-   <span data-ttu-id="e5439-118">Anbefalingsmotoren foreslår varer basert på hele varelisten i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="e5439-118">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="e5439-119">Hvis den butikkansatte legger til en kunde i transaksjonen, gir anbefalingsmotoren personlige anbefalinger ved hjelp av kundens transaksjonshistorikk og varelistsen i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="e5439-119">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="e5439-120">For å vise anbefalinger i **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e5439-120">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="e5439-121">**Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="e5439-121">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="e5439-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="e5439-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="e5439-123">På **Kundedetaljer**-siden:</span><span class="sxs-lookup"><span data-stu-id="e5439-123">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="e5439-124">Anbefalingsmotoren foreslår varer basert på bruker-ID og varene på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="e5439-124">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="e5439-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="e5439-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="e5439-126">Konfigurere Dynamics 365 for Retail for å aktivere POS-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="e5439-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="e5439-127">Hvis du vil sette opp produktanbefalinger, må du gjøre følgende.</span><span class="sxs-lookup"><span data-stu-id="e5439-127">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="e5439-128">Kontroller at du har valgt riktig **Juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="e5439-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="e5439-129">Gå til **Enhetslager**, velger **Detaljhandelsalg**, og klikk deretter på **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="e5439-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="e5439-130">Dette bruker demonstrasjonsdataene (eller dataene) fra den operative databasen og flytter dem til enhetsbutikken.</span><span class="sxs-lookup"><span data-stu-id="e5439-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="e5439-131">Valgfritt: Hvis du vil vise anbefalinger på transaksjonsskjermbildet, går du til **Skjermvisning**, velg din skjermvisning, start **Skjermvisningdesigner**, og slipp **anbefalinger**-kontrollen der det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e5439-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="e5439-132">Gå til **Forhandlerparametere**, velg **Maskinlæring**, velg **Ja** under **Aktiver POS-anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="e5439-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="e5439-133">Hvis du vil se anbefalinger på POS, kjør global konfigurasjonsjobb **1110**.</span><span class="sxs-lookup"><span data-stu-id="e5439-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="e5439-134">For å gjenspeile endringer i utforming av POS-skjermoppsettet, kan du kjøre kanalkonfigurasjonsjobb **1070**.</span><span class="sxs-lookup"><span data-stu-id="e5439-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="e5439-135">[]()Hvordan fungerer det?</span><span class="sxs-lookup"><span data-stu-id="e5439-135">[]()How does it work?</span></span>
<span data-ttu-id="e5439-136">Når du oppdaterer den **Enhetslager**, følgende handlinger finner sted.</span><span class="sxs-lookup"><span data-stu-id="e5439-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="e5439-137">Data i formatet som kreves av de kognitive tjenestene er trukket ut fra Dynamics 365 for Retail operativ database og sendes til enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="e5439-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="e5439-138">Dataene brukes av Azure Data Factory (ADF) til å rense data ved hjelp av strukturskript som en del av ADF-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e5439-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="e5439-139">Rensede data lagres i blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="e5439-139">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="e5439-140">Data fra blob-lagring brukes av kognitive services API til å lære opp en anbefalingsmodell.</span><span class="sxs-lookup"><span data-stu-id="e5439-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="e5439-141">Når du slår på **Aktiver anbefalinger** og kjører konfigurasjonjobbene, følgende handlinger finner sted.</span><span class="sxs-lookup"><span data-stu-id="e5439-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="e5439-142">Modellens legitimasjon og ID hentes fra API-en og lagres i Dynamics 365 for Retail operativ database, i filen web.config for AOS og også i detaljhandelsserveren.</span><span class="sxs-lookup"><span data-stu-id="e5439-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="e5439-143">Modellens legitimasjon og ID gjøres tilgjengelig for CRT slik at kall til produktanbefalinger fra Cloud POS og MPOS i tilkoblet modus kan opprettholdes.</span><span class="sxs-lookup"><span data-stu-id="e5439-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="e5439-144">Se også</span><span class="sxs-lookup"><span data-stu-id="e5439-144">See also</span></span>
--------

[<span data-ttu-id="e5439-145">Legge til en kontroll for anbefalinger på transaksjonssiden på en salgsstedsenhet</span><span class="sxs-lookup"><span data-stu-id="e5439-145">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




