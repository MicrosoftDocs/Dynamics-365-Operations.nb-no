---
title: "Overvåke prognosenøyaktighet"
description: "Denne artikkelen beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 for Operations beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 580b45263b45e6ef730b0fac32575fcdd9c358b6
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Overvåke prognosenøyaktighet

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver typene prognosenøyaktighet som Microsoft Dynamics 365 for Operations beregner, og forklarer hvordan du kan vise nøyaktighetsverdiene.

Dynamics 365 for Operations beregner følgende typer prognosenøyaktighet:

-   Historisk prognosenøyaktighet, ved å sammenligne den historiske prognosen som hovedplanlegging bruker, med historisk behov. For å vise verdiene (både absolutte verdier og prosentverdier) for historisk prognosenøyaktighet klikk **Vis nøyaktighet** på siden **Detaljer om behovsprognose**.
-   Den beregnede nøyaktigheten for prognosemodellen som brukes til å generere prediksjoner. Du kan vise nøyaktighet i prosent under **Modelldetaljer - MAPE** på siden **Detaljer om behovsprognose**. 

**Obs!** Hvis du bruker Dynamics 365 for Operations behovsprognose og Microsoft Azure Machine Learning-tjenesten, er beregning av intern modellnøyaktighet basert på testdatasettet. Hvis du vil angi størrelsen på testdatasettet, kan du angi **TEST\_SET\_SIZE\_PERCENT**-parameteren på siden **Parametere for behovsprognose**. For eksempel hvis du setter verdien til **20**, vil de siste 20 prosentene av historiske data bli brukt til å beregne den interne modellnøyaktigheten.


<a name="see-also"></a>Se også
--------

[Godkjenne den justerte prognosen](authorize-adjusted-forecast.md)

[Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose](remove-historical-outliers-calculating-demand-forecast.md)




