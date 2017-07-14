---
title: "Overvåke prognosenøyaktighet"
description: "Denne artikkelen beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 for Finance and Operations beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 56d3f0312e684ab076f9116ac6638bcd67b52e58
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Overvåke prognosenøyaktighet
<a id="monitor-forecast-accuracy" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 for Finance and Operations beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene.

Finance and Operations beregner følgende typer prognosenøyaktighet:

-   Historisk prognosenøyaktighet, ved å sammenligne den historiske prognosen som hovedplanlegging bruker, med historisk behov. For å vise verdiene (både absolutte verdier og prosentverdier) for historisk prognosenøyaktighet klikk **Vis nøyaktighet** på siden **Detaljer om behovsprognose**.
-   Den beregnede nøyaktigheten for prognosemodellen som brukes til å generere prediksjoner. Du kan vise nøyaktighet i prosent under **Modelldetaljer - MAPE** på siden **Detaljer om behovsprognose**. 

**Obs!** Hvis du bruker Finance and Operations behovsprognose og Microsoft Azure Machine Learning-tjenesten, er beregning av intern modellnøyaktighet basert på testdatasettet. Hvis du vil angi størrelsen på testdatasettet, kan du angi **TEST\_SET\_SIZE\_PERCENT**-parameteren på siden **Parametere for behovsprognose**. For eksempel hvis du setter verdien til **20**, vil de siste 20 prosentene av historiske data bli brukt til å beregne den interne modellnøyaktigheten.


Se også
<a id="see-also" class="xliff"></a>
--------

[Godkjenne den justerte prognosen](authorize-adjusted-forecast.md)

[Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose](remove-historical-outliers-calculating-demand-forecast.md)




