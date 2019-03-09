---
title: Kostnadsberegning for produksjonsordrer
description: Denne artikkelen inneholder informasjon om kostnadsestimat for produksjonen. Kostnadsestimat for produksjonen gir deg forventede kostnader til materialer og kapasitetsforbruk som går med i produksjon av en vare i produksjonsforslagets antall.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93546fc170757ee2c39144842bae12d78400fd32
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2019
ms.locfileid: "350487"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="05307-104">Kostnadsberegning for produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="05307-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05307-105">Denne artikkelen inneholder informasjon om kostnadsestimat for produksjonen.</span><span class="sxs-lookup"><span data-stu-id="05307-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="05307-106">Kostnadsestimat for produksjonen gir deg forventede kostnader til materialer og kapasitetsforbruk som går med i produksjon av en vare i produksjonsforslagets antall.</span><span class="sxs-lookup"><span data-stu-id="05307-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="05307-107">Når du oppretter en produksjonsordre, må du beregne produksjonskostnader.</span><span class="sxs-lookup"><span data-stu-id="05307-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="05307-108">Formålet er å gi et estimat for vare- og ruteforbruk for produksjonsprosessen, fordi disse estimatene brukes som grunnlaget for fremtidige planleggings- og produksjonsprosesser.</span><span class="sxs-lookup"><span data-stu-id="05307-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="05307-109">Kostnadsberegning for produksjon</span><span class="sxs-lookup"><span data-stu-id="05307-109">Production cost estimation</span></span>
<span data-ttu-id="05307-110">Estimater for produksjonskostnader er basert på følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="05307-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="05307-111">Antallet for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="05307-111">The quantity on the production order</span></span>
-   <span data-ttu-id="05307-112">Komponentene i produksjonsstykklistene</span><span class="sxs-lookup"><span data-stu-id="05307-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="05307-113">Ruteoperasjonene i produksjonsruten</span><span class="sxs-lookup"><span data-stu-id="05307-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="05307-114">De indirekte kostnadene som gjelder for komponenter og operasjoner</span><span class="sxs-lookup"><span data-stu-id="05307-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="05307-115">De aktive kostnadsdataene på beregningsdatoen</span><span class="sxs-lookup"><span data-stu-id="05307-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="05307-116">Hvis det finnes en fantomvarelinje i produksjonsstykklisten, gjenspeiler beregningene fantomvarens komponenter og rutingoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="05307-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="05307-117">Du kan bruke estimeringsoppgaven til å omberegne kostnadsestimater, slik at de gjenspeiler oppdatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="05307-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="05307-118">Den oppdaterte informasjonen kan for eksempel være endringer i antallet i produksjonsordren, komponentene i produksjonsstykklisten, ruteoperasjonene i produksjonsruten, de indirekte kostnadene som gjelder for disse komponentene og operasjonene, eller de aktive kostnadsdataene på omberegningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="05307-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="05307-119">Beregningene av kostnadsestimatet foreslår også en salgspris for produksjonsvaren basert på kostnader pluss påslag.</span><span class="sxs-lookup"><span data-stu-id="05307-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="05307-120">Beregningene av kostnadsestimatet kan om ønskelig også brukes på referanseordrer som gjenspeiler andre produksjonsordrer som er knyttet til produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="05307-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="05307-121">Vise de estimerte kostnadene</span><span class="sxs-lookup"><span data-stu-id="05307-121">View the estimated costs</span></span>
<span data-ttu-id="05307-122">Når du har kjørt anslag, kan du vise resultatene på siden **Prisberegning**.</span><span class="sxs-lookup"><span data-stu-id="05307-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="05307-123">Anslaget beregner følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="05307-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="05307-124">**Produksjonskostnad** – Produksjonskostnaden er den øverste linjen i estimatet.</span><span class="sxs-lookup"><span data-stu-id="05307-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="05307-125">Den viser de samlede kostnadene fra kjøring av produksjonsordren og samlet salgspris for produksjonen.</span><span class="sxs-lookup"><span data-stu-id="05307-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="05307-126">Det er summen av alle kostnadslinjer i estimatet.</span><span class="sxs-lookup"><span data-stu-id="05307-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="05307-127">**Rute- eller kostnader** – Rute- eller ressurskostnadene er kostnadene for produksjonsoperasjonene.</span><span class="sxs-lookup"><span data-stu-id="05307-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="05307-128">De inkluderer kostnadene for elementer som oppstillingstid, operasjonstid og administrasjonskostnader.</span><span class="sxs-lookup"><span data-stu-id="05307-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="05307-129">**Materialkostnader** – Materialkostnader er kostnadene og prisene fra stykklistekomponenter som kreves for å produsere varen.</span><span class="sxs-lookup"><span data-stu-id="05307-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="05307-130">Disse kostnadene er på forhånd fastsatt og registrert i systemet.</span><span class="sxs-lookup"><span data-stu-id="05307-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="05307-131">Annen bruk av kostnadsestimater</span><span class="sxs-lookup"><span data-stu-id="05307-131">Other uses of cost estimation</span></span>
<span data-ttu-id="05307-132">Et kostnadsestimat gir også følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="05307-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="05307-133">Nyttige pristilbud.</span><span class="sxs-lookup"><span data-stu-id="05307-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="05307-134">Estimater for ordrens lønnsomhet</span><span class="sxs-lookup"><span data-stu-id="05307-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="05307-135">Estimater for råvareforbruk</span><span class="sxs-lookup"><span data-stu-id="05307-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="05307-136">Sammenligninger av kostnadsinformasjon fra tidligere produksjoner</span><span class="sxs-lookup"><span data-stu-id="05307-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="05307-137">Budsjett- og prognoseinformasjon</span><span class="sxs-lookup"><span data-stu-id="05307-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="05307-138">Estimater for produksjonsstørrelsen som kreves for å beholde en bestemt kostnad</span><span class="sxs-lookup"><span data-stu-id="05307-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




