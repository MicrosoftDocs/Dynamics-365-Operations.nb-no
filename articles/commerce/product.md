---
title: Produktanbefalinger på salgssted
description: Dette emnet beskriver hvordan du bruker produktanbefalinger på en salgsstedsenhet (POS).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057447"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="5ec0e-103">Produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="5ec0e-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ec0e-104">Det mest sentrale i produktanbefalinger et transformasjonsrettet forretningsprogram som strekker seg over alle handelsområder for å skape rike, engasjerende og tilpassede produktgjenkjenningsopplevelser.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="5ec0e-105">Hvis du vil implementere denne funksjonen på salgsstedet, følger du fremgangsmåten for [hvordan du legger til anbefalinger i POS-enhetene.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="5ec0e-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="5ec0e-106">Hvis du vil ha mer informasjon om funksjoner for produktanbefalinger, kan du lese [oversikt over produktanbefalinger.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="5ec0e-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="5ec0e-107">Scenarier</span><span class="sxs-lookup"><span data-stu-id="5ec0e-107">Scenarios</span></span>

<span data-ttu-id="5ec0e-108">Produktanbefalingene er aktivert for følgende POS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="5ec0e-109">De er tilgjengelige i Cloud POS eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="5ec0e-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="5ec0e-110">På **Produktdetaljer**-siden:</span><span class="sxs-lookup"><span data-stu-id="5ec0e-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="5ec0e-111">Hvis en butikkansatt besøker en **Produktdetaljer**-side når vedkommende ser på tidligere transaksjoner på tvers av forskjellige kanaler, foreslår anbefalingstjenesten flere varer som sannsynligvis kjøpes sammen.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="5ec0e-112">[![Anbefalinger på siden Produktdetaljer](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="5ec0e-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="5ec0e-113">På **Transaksjon**-siden:</span><span class="sxs-lookup"><span data-stu-id="5ec0e-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="5ec0e-114">Anbefalingsmotoren foreslår varer basert på hele listen med varer i handlekurven, som ofte kjøpes sammen.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ec0e-115">For å vise anbefalinger på **Transaksjon**-siden må forhandler oppdatere skjermvisningen i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5ec0e-116">**Anbefalinger**-kontrollen må slippes på **Transaksjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="5ec0e-117">[![Anbefalinger på siden Transaksjoner](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="5ec0e-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="5ec0e-118">Konfigurere Commerce for å aktivere anbefalinger for salgssted</span><span class="sxs-lookup"><span data-stu-id="5ec0e-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="5ec0e-119">Gjør følgende for å konfigurere produktanbefalinger:</span><span class="sxs-lookup"><span data-stu-id="5ec0e-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="5ec0e-120">Kontroller at tjenesten er oppdatert til **10.0.6-builden**.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="5ec0e-121">Følg instruksjonene om hvordan du [aktiverer produktanbefalinger](../commerce/enable-product-recommendations.md) for din virksomhet.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="5ec0e-122">Valgfritt: Hvis du vil vise anbefalinger på transaksjonsskjermbildet, går du til **Skjermvisning**, velg din skjermvisning, start **Skjermvisningdesigner**, og slipp **anbefalinger**-kontrollen der det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="5ec0e-123">Gå til **Handelsparametere**, velg **Maskinlæring**, velg **Ja** under **Aktiver POS-anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="5ec0e-124">Hvis du vil se anbefalinger på POS, kjør global konfigurasjonsjobb **1110**.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="5ec0e-125">For å gjenspeile endringer i utforming av POS-skjermoppsettet, kan du kjøre kanalkonfigurasjonsjobb **1070**.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="5ec0e-126">Feilsøke problemer der du allerede har aktivert produktanbefalingene</span><span class="sxs-lookup"><span data-stu-id="5ec0e-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="5ec0e-127">Gå til **Handelsparametere** \> **Anbefalingsliste** \> **Deaktiver produktanbefalingene** og kjør **Global konfigurasjon for jobben \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="5ec0e-128">Hvis du har lagt **kontroll for anbefalinger** til din transaksjonsskjerm ved hjelp av **utforming av skjermoppsett**, må fjerne den også.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="5ec0e-129">Hvis du har flere spørsmål, kan du gå til [Vanlige spørsmål om produktanbefalinger](../commerce/faq-recommendations.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="5ec0e-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ec0e-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5ec0e-130">Additional resources</span></span>

[<span data-ttu-id="5ec0e-131">Legge til en kontroll for anbefalinger på transaksjonsskjermen på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="5ec0e-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="5ec0e-132">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5ec0e-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="5ec0e-133">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5ec0e-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
