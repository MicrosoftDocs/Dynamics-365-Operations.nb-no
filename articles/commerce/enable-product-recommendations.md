---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127888"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="8ae02-103">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ae02-104">Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="8ae02-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="8ae02-105">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8ae02-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="8ae02-106">Anbefalinger, forhåndssjekk</span><span class="sxs-lookup"><span data-stu-id="8ae02-106">Recommendations pre-check</span></span>

<span data-ttu-id="8ae02-107">Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Handel-kunder som har migrert lagringen til bruk av Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="8ae02-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="8ae02-108">Hvis du vil se trinn for aktivering av ADLS, kan du se [Slik aktiverer du ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8ae02-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="8ae02-109">Kontroller også at RetailSale-mål er aktivert.</span><span class="sxs-lookup"><span data-stu-id="8ae02-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="8ae02-110">Hvis du vil lære mer om denne konfigureringsprosessen, går du [hit.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="8ae02-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="8ae02-111">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-111">Turn on recommendations</span></span>

<span data-ttu-id="8ae02-112">Gjør følgende for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="8ae02-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="8ae02-113">Gå til **Detaljhandel og handel &gt; Produktanbefalinger &gt; Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="8ae02-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="8ae02-114">Velg **Anbefalingslister** i listen over delte parametere.</span><span class="sxs-lookup"><span data-stu-id="8ae02-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="8ae02-115">Sett alternativet **Aktiver anbefalinger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8ae02-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="8ae02-117">Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="8ae02-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="8ae02-118">Opptil flere timer kan være nødvendig før listene er tilgjengelige og kan sees ved salgsstedet (POS) eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ae02-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="8ae02-119">Konfigurere parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="8ae02-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="8ae02-120">Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier.</span><span class="sxs-lookup"><span data-stu-id="8ae02-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="8ae02-121">Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten.</span><span class="sxs-lookup"><span data-stu-id="8ae02-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="8ae02-122">Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="8ae02-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="8ae02-123">Vis anbefalinger på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="8ae02-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="8ae02-124">Når du har aktivert anbefalinger i Handel-administrasjonskontoret, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet.</span><span class="sxs-lookup"><span data-stu-id="8ae02-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="8ae02-125">Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="8ae02-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="8ae02-126">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-126">Enable personalized recommendations</span></span>

<span data-ttu-id="8ae02-127">Hvis du vil finne ut mer om hvordan du mottar tilpassede anbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8ae02-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ae02-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8ae02-128">Additional resources</span></span>

[<span data-ttu-id="8ae02-129">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8ae02-130">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="8ae02-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8ae02-131">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8ae02-132">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8ae02-133">Legge til lister over anbefalinger på et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="8ae02-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="8ae02-134">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="8ae02-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8ae02-135">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="8ae02-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8ae02-136">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="8ae02-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8ae02-137">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="8ae02-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8ae02-138">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="8ae02-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8ae02-139">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae02-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

