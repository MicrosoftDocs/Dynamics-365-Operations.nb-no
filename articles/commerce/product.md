---
title: Legge til produktanbefalinger i POS
description: Dette emnet beskriver hvordan du bruker produktanbefalinger på en salgsstedsenhet (POS).
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48533596c5bdc73dd8c815166e7dde0ca2f3cb4d
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127819"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="d4b6d-103">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="d4b6d-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4b6d-104">Det mest sentrale i produktanbefalinger et transformasjonsrettet forretningsprogram som strekker seg over alle handelsområder for å skape rike, engasjerende og tilpassede produktgjenkjenningsopplevelser.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="d4b6d-105">Hvis du vil implementere denne funksjonen på salgsstedet, følger du fremgangsmåten for [hvordan du legger til anbefalinger i POS-enhetene.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="d4b6d-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="d4b6d-106">Hvis du vil ha mer informasjon om funksjoner for produktanbefalinger, kan du lese [oversikt over produktanbefalinger.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="d4b6d-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="d4b6d-107">Scenarier</span><span class="sxs-lookup"><span data-stu-id="d4b6d-107">Scenarios</span></span>

<span data-ttu-id="d4b6d-108">Produktanbefalingene er aktivert for følgende POS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="d4b6d-109">De er tilgjengelige i Cloud POS eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="d4b6d-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="d4b6d-110">På **Produktdetaljer**-siden:</span><span class="sxs-lookup"><span data-stu-id="d4b6d-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="d4b6d-111">Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingstjenesten flere varer som sannsynligvis kjøpes sammen.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="d4b6d-112">[![Anbefalinger på siden Produktdetaljer](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="d4b6d-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="d4b6d-113">På **Transaksjon**-siden:</span><span class="sxs-lookup"><span data-stu-id="d4b6d-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="d4b6d-114">Anbefalingsmotoren foreslår varer basert på hele listen med varer i handlekurven, som ofte kjøpes sammen.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4b6d-115">For å vise anbefalinger på **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d4b6d-116">**Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="d4b6d-117">[![Anbefalinger på siden Transaksjoner](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="d4b6d-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="d4b6d-118">Konfigurere Commerce for å aktivere anbefalinger for salgssted</span><span class="sxs-lookup"><span data-stu-id="d4b6d-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="d4b6d-119">Gjør følgende for å konfigurere produktanbefalinger:</span><span class="sxs-lookup"><span data-stu-id="d4b6d-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="d4b6d-120">Kontroller at tjenesten er oppdatert til **10.0.6-builden**.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="d4b6d-121">Følg instruksjonene om hvordan du [aktiverer produktanbefalinger](../commerce/enable-product-recommendations.md) for din virksomhet.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="d4b6d-122">Valgfritt: Hvis du vil vise anbefalinger på transaksjonsskjermbildet, går du til **Skjermvisning**, velg din skjermvisning, start **Skjermvisningdesigner**, og slipp **anbefalinger**-kontrollen der det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="d4b6d-123">Gå til **Handelsparametere**, velg **Maskinlæring**, velg **Ja** under **Aktiver POS-anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="d4b6d-124">Hvis du vil se anbefalinger på POS, kjør global konfigurasjonsjobb **1110**.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="d4b6d-125">For å gjenspeile endringer i utforming av POS-skjermoppsettet, kan du kjøre kanalkonfigurasjonsjobb **1070**.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="d4b6d-126">Feilsøke problemer der du allerede har aktivert produktanbefalingene</span><span class="sxs-lookup"><span data-stu-id="d4b6d-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="d4b6d-127">Gå til **Handelsparametere** \> **Anbefalingsliste** \> **Deaktiver produktanbefalingene** og kjør **Global konfigurasjon for jobben \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="d4b6d-128">Hvis du har lagt **kontroll for anbefalinger** til din transaksjonsskjerm ved hjelp av **utforming av skjermoppsett**, må fjerne den også.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="d4b6d-129">Hvis du har flere spørsmål, kan du gå til [Vanlige spørsmål om produktanbefalinger](../commerce/faq-recommendations.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="d4b6d-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4b6d-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d4b6d-130">Additional resources</span></span>

[<span data-ttu-id="d4b6d-131">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="d4b6d-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d4b6d-132">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="d4b6d-132">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d4b6d-133">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="d4b6d-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d4b6d-134">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="d4b6d-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d4b6d-135">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="d4b6d-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d4b6d-136">Legge til lister over anbefalinger på et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="d4b6d-136">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="d4b6d-137">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="d4b6d-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d4b6d-138">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="d4b6d-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d4b6d-139">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="d4b6d-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d4b6d-140">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="d4b6d-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d4b6d-141">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="d4b6d-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
