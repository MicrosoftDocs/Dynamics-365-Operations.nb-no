---
title: "Overvåke prognosenøyaktighet"
description: "Denne artikkelen beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 for Finance and Operations beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d1025619d799cb94af73571f8ca78eca578782f4
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="b76b0-103">Overvåke prognosenøyaktighet</span><span class="sxs-lookup"><span data-stu-id="b76b0-103">Monitor forecast accuracy</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b76b0-104">Denne artikkelen beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 for Finance and Operations beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene.</span><span class="sxs-lookup"><span data-stu-id="b76b0-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="b76b0-105">Finance and Operations beregner følgende typer prognosenøyaktighet:</span><span class="sxs-lookup"><span data-stu-id="b76b0-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="b76b0-106">Historisk prognosenøyaktighet, ved å sammenligne den historiske prognosen som hovedplanlegging bruker, med historisk behov.</span><span class="sxs-lookup"><span data-stu-id="b76b0-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="b76b0-107">For å vise verdiene (både absolutte verdier og prosentverdier) for historisk prognosenøyaktighet klikk **Vis nøyaktighet** på siden **Detaljer om behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="b76b0-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="b76b0-108">Den beregnede nøyaktigheten for prognosemodellen som brukes til å generere prediksjoner.</span><span class="sxs-lookup"><span data-stu-id="b76b0-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="b76b0-109">Du kan vise nøyaktighet i prosent under **Modelldetaljer - MAPE** på siden **Detaljer om behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="b76b0-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="b76b0-110">**Obs!** Hvis du bruker Finance and Operations behovsprognose og Microsoft Azure Machine Learning-tjenesten, er beregning av intern modellnøyaktighet basert på testdatasettet.</span><span class="sxs-lookup"><span data-stu-id="b76b0-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="b76b0-111">Hvis du vil angi størrelsen på testdatasettet, kan du angi **TEST\_SET\_SIZE\_PERCENT**-parameteren på siden **Parametere for behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="b76b0-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="b76b0-112">For eksempel hvis du setter verdien til **20**, vil de siste 20 prosentene av historiske data bli brukt til å beregne den interne modellnøyaktigheten.</span><span class="sxs-lookup"><span data-stu-id="b76b0-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="b76b0-113">Se også</span><span class="sxs-lookup"><span data-stu-id="b76b0-113">See also</span></span>
--------

[<span data-ttu-id="b76b0-114">Godkjenne den justerte prognosen</span><span class="sxs-lookup"><span data-stu-id="b76b0-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b76b0-115">Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose</span><span class="sxs-lookup"><span data-stu-id="b76b0-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




