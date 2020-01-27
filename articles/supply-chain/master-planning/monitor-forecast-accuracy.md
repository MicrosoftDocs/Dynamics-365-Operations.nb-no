---
title: Overvåke prognosenøyaktighet
description: Dette emnet beskriver typene prognosenøyaktighet som Dynamics 365 Supply Chain Management beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bc3673ba69a072d07b749ad41a1697d35abd48
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935543"
---
# <a name="monitor-forecast-accuracy"></a>Overvåke prognosenøyaktighet

[!include [banner](../includes/banner.md)]

Dette emnet beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 Supply Chain Management beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene.

Supply Chain Management beregner følgende typer prognosenøyaktighet:

-   Historisk prognosenøyaktighet, ved å sammenligne den historiske prognosen som hovedplanlegging bruker, med historisk behov. For å vise verdiene (både absolutte verdier og prosentverdier) for historisk prognosenøyaktighet klikk **Vis nøyaktighet** på siden **Detaljer om behovsprognose**.
-   Den beregnede nøyaktigheten for prognosemodellen som brukes til å generere prediksjoner. Du kan vise nøyaktighet i prosent under **Modelldetaljer - MAPE** på siden **Detaljer om behovsprognose**. 

> [!NOTE]
> Hvis du bruker behovsprognose og Microsoft Azure Machine Learning, er beregning av intern modellnøyaktighet basert på testdatasettet. Hvis du vil angi størrelsen på testdatasettet, kan du angi **TEST\_SET\_SIZE\_PERCENT**-parameteren på siden **Parametere for behovsprognose**. For eksempel hvis du setter verdien til **20**, vil de siste 20 prosentene av historiske data bli brukt til å beregne den interne modellnøyaktigheten.


<a name="additional-resources"></a>Tilleggsressurser
--------

[Autorisere en justert prognose](authorize-adjusted-forecast.md)

[Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose](remove-historical-outliers-calculating-demand-forecast.md)



