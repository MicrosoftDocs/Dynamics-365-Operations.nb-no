---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024962"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="a8f6d-103">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8f6d-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8f6d-104">Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="a8f6d-105">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6d-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="a8f6d-106">Anbefalinger, forhåndssjekk</span><span class="sxs-lookup"><span data-stu-id="a8f6d-106">Recommendations pre-check</span></span>

<span data-ttu-id="a8f6d-107">Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Handel-kunder som har migrert lagringen til bruk av Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="a8f6d-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="a8f6d-108">Hvis du vil se trinn for aktivering av ADLS, kan du se [Slik aktiverer du ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6d-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="a8f6d-109">Kontroller også at RetailSale-mål er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="a8f6d-110">Hvis du vil lære mer om denne konfigureringsprosessen, går du [hit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="a8f6d-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="a8f6d-111">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8f6d-111">Turn on recommendations</span></span>

<span data-ttu-id="a8f6d-112">Gjør følgende for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="a8f6d-113">Gå til **Detaljhandel og handel &gt; Produktanbefalinger &gt; Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="a8f6d-114">Velg **Anbefalingslister** i listen over delte parametere.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="a8f6d-115">Sett alternativet **Aktiver anbefalinger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="a8f6d-117">Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="a8f6d-118">Opptil flere timer kan være nødvendig før listene er tilgjengelige og kan sees ved salgsstedet (POS) eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="a8f6d-119">Konfigurere parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="a8f6d-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="a8f6d-120">Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="a8f6d-121">Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="a8f6d-122">Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6d-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="a8f6d-123">Vis anbefalinger på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="a8f6d-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="a8f6d-124">Når du har aktivert anbefalinger i Handel-administrasjonskontoret, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet.</span><span class="sxs-lookup"><span data-stu-id="a8f6d-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="a8f6d-125">Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6d-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="a8f6d-126">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8f6d-126">Enable personalized recommendations</span></span>

<span data-ttu-id="a8f6d-127">Hvis du vil finne ut mer om hvordan du mottar tilpassede anbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6d-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8f6d-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a8f6d-128">Additional resources</span></span>

[<span data-ttu-id="a8f6d-129">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8f6d-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a8f6d-130">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8f6d-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a8f6d-131">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="a8f6d-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="a8f6d-132">Legge til anbefalingspanel til POS-enheter</span><span class="sxs-lookup"><span data-stu-id="a8f6d-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a8f6d-133">Oversikt over produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="a8f6d-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="a8f6d-134">Aktivere ADLS i Dynamics 365-miljøet</span><span class="sxs-lookup"><span data-stu-id="a8f6d-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

