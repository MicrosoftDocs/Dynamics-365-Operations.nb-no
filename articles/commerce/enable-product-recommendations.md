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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770145"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="16934-103">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="16934-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="16934-104">Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="16934-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="16934-105">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="16934-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="16934-106">Anbefalinger, forhåndssjekk</span><span class="sxs-lookup"><span data-stu-id="16934-106">Recommendations pre-check</span></span>
<span data-ttu-id="16934-107">Før du aktiverer bør du være oppmerksom på at produktanbefalinger bare støttes for økonomi/drift-kunder som støtter bygg 10.0.6 og har migrert lagringsplassen til BDL.</span><span class="sxs-lookup"><span data-stu-id="16934-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="16934-108">Kontroller også at RetailSale-mål er aktivert.</span><span class="sxs-lookup"><span data-stu-id="16934-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="16934-109">Hvis du vil lære mer om denne konfigureringsprosessen, går du [hit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="16934-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="16934-110">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="16934-110">Turn on recommendations</span></span>

<span data-ttu-id="16934-111">Gjør følgende for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="16934-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="16934-112">Gå til **Retail** &gt; **Produktanbefalinger** &gt; **Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="16934-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="16934-113">Velg **Anbefalingslister** i listen over delte parametere for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="16934-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="16934-114">Sett alternativet **Aktiver anbefalinger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="16934-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="16934-116">Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="16934-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="16934-117">Opptil flere timer kan være nødvendig før listene er tilgjengelige og kan sees ved salgsstedet (POS) eller i Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="16934-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="16934-118">Konfigurere parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="16934-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="16934-119">Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier.</span><span class="sxs-lookup"><span data-stu-id="16934-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="16934-120">Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten.</span><span class="sxs-lookup"><span data-stu-id="16934-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="16934-121">Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="16934-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="16934-122">Vis anbefalinger på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="16934-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="16934-123">Når du har aktivert anbefalinger i backoffice, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen via oppsettverktøyet.</span><span class="sxs-lookup"><span data-stu-id="16934-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="16934-124">Hvis du vil lære mer om denne prosessen, går du [hit.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="16934-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="16934-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="16934-125">Additional resources</span></span>

[<span data-ttu-id="16934-126">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="16934-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="16934-127">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="16934-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="16934-128">Legge til anbefalingspanel til POS-enheter</span><span class="sxs-lookup"><span data-stu-id="16934-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


