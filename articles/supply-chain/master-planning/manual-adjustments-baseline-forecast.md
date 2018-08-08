---
title: Foreta manuelle justeringer i basislinjeprognosen
description: "Dette emnet forklarer hvordan du gjør manuelle justeringer i en basislinjeprognose og viser detaljer for prognosen."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a7c7d1fcaaeef7a01b43886e4d69458dbd942439
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="09fec-103">Foreta manuelle justeringer i basislinjeprognosen</span><span class="sxs-lookup"><span data-stu-id="09fec-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09fec-104">Dette emnet forklarer hvordan du gjør manuelle justeringer i en basislinjeprognose og viser detaljer for prognosen.</span><span class="sxs-lookup"><span data-stu-id="09fec-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="09fec-105">Før du gjør manuelle justeringer, er det viktig at du forstår noen nøkkelbegreper om forskjellige sider.</span><span class="sxs-lookup"><span data-stu-id="09fec-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="09fec-106">Rutenett på siden Justert behovsprognose</span><span class="sxs-lookup"><span data-stu-id="09fec-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="09fec-107">Siden **Justert behovsprognose** inneholder et rutenett med følgende struktur:</span><span class="sxs-lookup"><span data-stu-id="09fec-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="09fec-108">Den første kolonnen viser varene, varefordelingsnøkler, firmaer, og så videre som prognosen er generert for.</span><span class="sxs-lookup"><span data-stu-id="09fec-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="09fec-109">Undertittelen på siden gir en beskrivelse av gjeldende prognosedimensjoner som vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="09fec-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="09fec-110">Hvis undertittelen på siden for eksempel er **firma / område / varefordelingsnøkkel**, og en av radoverskriftene i rutenettet er **USMF / 1 / D\_Alloc**, viser denne raden prognosen for firmaet USMF, område 1, og varefordelingsnøkkel **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="09fec-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="09fec-111">Etterfølgende kolonner representerer prognoseperioder som prognosen er generert for.</span><span class="sxs-lookup"><span data-stu-id="09fec-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="09fec-112">Hver kolonneoverskrift er den første datoen i prognoseperioden som kolonnen viser.</span><span class="sxs-lookup"><span data-stu-id="09fec-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="09fec-113">Verdiene i cellene representerer prognosen for én vare, varefordelingsnøkkel og så videre, for den bestemte prognoseperioden.</span><span class="sxs-lookup"><span data-stu-id="09fec-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="09fec-114">Prognoseaggregering og -deaggregering</span><span class="sxs-lookup"><span data-stu-id="09fec-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="09fec-115">Undertittelen på siden viser nivået på prognoseaggregering.</span><span class="sxs-lookup"><span data-stu-id="09fec-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="09fec-116">Hvis undertittelen på siden for eksempel er **firma / område / tilordningsnøkkel / varenummer / farge / størrelse / konfigurasjon / stil**, er det ingen prognoseaggregering, og prognosen vises på nivået for varen og dens dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="09fec-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="09fec-117">For å endre aggregering bruk siden **Endre prognosedimensjoner** som du kan åpne fra programmenyen.</span><span class="sxs-lookup"><span data-stu-id="09fec-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="09fec-118">Hvis du vil endre prognosen, klikker du i noen av cellene som er tilgjengelige, og Skriv inn den justerte prognoseverdi.</span><span class="sxs-lookup"><span data-stu-id="09fec-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="09fec-119">Den redigerte cellen blir umiddelbart fet for å angi at prognosen som den viser, ikke er prognosen som behovsprognosetjenesten opprettet, men er justert manuelt.</span><span class="sxs-lookup"><span data-stu-id="09fec-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="09fec-120">Hvis du endrer aggregering for å la siden vise mer aggregerte data, kan du bruke siden **Behovsprognoselinjer** for å vise individuelle prognoselinjer som utgjør den aggregerte prognosen.</span><span class="sxs-lookup"><span data-stu-id="09fec-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="09fec-121">Du har for eksempel generert prognosen på varenivå, men du vet at behovet for denne varen vil øke på tvers av alle områder på grunn av en kampanje eller en annen lignende hendelse.</span><span class="sxs-lookup"><span data-stu-id="09fec-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="09fec-122">I så fall kan du sette aggregeringen til **firma / varefordelingsnøkkel / vare** på siden **Endre prognosedimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="09fec-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="09fec-123">Du kan justere den globale prognosen for varen på tvers av alle områder i rutenettet **Justert behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="09fec-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="09fec-124">Hvis du vil se effekten av endringen på tvers av alle områder, kan du åpne siden **Behovsprognoselinjer**.</span><span class="sxs-lookup"><span data-stu-id="09fec-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="09fec-125">På denne siden vises én linje for varen for hvert område, det justerte prognoseantallet og det opprinnelige prognoseantallet.</span><span class="sxs-lookup"><span data-stu-id="09fec-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="09fec-126">Når justeringen av det prognoseberegnede antall er utført på et aggregert nivå, bruker systemet avveid tildeling for å distribuere endringen mellom linjene som oppretter aggregeringen.</span><span class="sxs-lookup"><span data-stu-id="09fec-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="09fec-127">Du kan også gjøre manuelle justeringer på siden **Behovsprognoselinjer** ved å endre enten **Totalt antall**-verdien eller **Antall**-cellene i deaggregeringsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="09fec-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="09fec-128">Vise detaljer for prognosen</span><span class="sxs-lookup"><span data-stu-id="09fec-128">Viewing details of the forecast</span></span>
<span data-ttu-id="09fec-129">Du kan åpne siden **Detaljer om behovsprognose** for å vise mer informasjon om prognosen.</span><span class="sxs-lookup"><span data-stu-id="09fec-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="09fec-130">Siden **Detaljer om behovsprognose** viser følgende informasjon i grafisk format og tabellformat:</span><span class="sxs-lookup"><span data-stu-id="09fec-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="09fec-131">Det historiske behovet som prognoseforutsigelser er basert på.</span><span class="sxs-lookup"><span data-stu-id="09fec-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="09fec-132">Gjeldende prognose som brukes i hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="09fec-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="09fec-133">De nye behovsprognoseverdiene og beløpene som de er justert manuelt med.</span><span class="sxs-lookup"><span data-stu-id="09fec-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="09fec-134">Konfidensintervallet for prognoseverdiene.</span><span class="sxs-lookup"><span data-stu-id="09fec-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="09fec-135">Prognosemodellen som ble brukt til å generere prognosen.</span><span class="sxs-lookup"><span data-stu-id="09fec-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="09fec-136">Hvis du viser samlede data, vises listen over alle metodene som ble brukt for den aggregerte tidsserien.</span><span class="sxs-lookup"><span data-stu-id="09fec-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="09fec-137">Intern modellnøyaktighet (MAPE).</span><span class="sxs-lookup"><span data-stu-id="09fec-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="09fec-138">Hvis du vil ha mer informasjon om prognosenøyaktighet, se [Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="09fec-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="09fec-139">**Merknader:**</span><span class="sxs-lookup"><span data-stu-id="09fec-139">**Notes:**</span></span>

-   <span data-ttu-id="09fec-140">Konfidensintervallet som vises i delen **Prognose** på siden, representerer forskjellen mellom den øvre grensen for konfidensintervallet og den nedre grensen for konfidensintervallet.</span><span class="sxs-lookup"><span data-stu-id="09fec-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="09fec-141">Hvis du vil se verdiene for øvre og nedre grense, holder du musepekeren over diagrammet i delen **Grafisk presentasjon av historisk behov og prognose**.</span><span class="sxs-lookup"><span data-stu-id="09fec-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="09fec-142">Hvis du bruker Finance and Operations behovsprognose og Microsoft Azure Machine Learning Service, kan du angi konfidensnivåprosenten som prognosen som genereres, skal ha.</span><span class="sxs-lookup"><span data-stu-id="09fec-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="09fec-143">Konfidensintervallet består av et verdiområde som fungerer som gode estimater for behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="09fec-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="09fec-144">En konfidensnivåprosent på 95 angir at det er 5 prosent risiko for at behovsprognosen faller utenfor området for konfidensintervallet.</span><span class="sxs-lookup"><span data-stu-id="09fec-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="09fec-145">Du kan også gjøre manuelle justeringer i prognosen på siden **Detaljer om behovsprognose** ved å endre verdiene i **Prognose**-raden i delen **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="09fec-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="09fec-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="09fec-146">Additional resources</span></span>
--------

[<span data-ttu-id="09fec-147">Overvåke prognosenøyaktighet</span><span class="sxs-lookup"><span data-stu-id="09fec-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="09fec-148">Generere en statistisk basislinjeprognose</span><span class="sxs-lookup"><span data-stu-id="09fec-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)




