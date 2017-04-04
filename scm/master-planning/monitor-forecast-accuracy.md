---
title: "Skjermen prognosen nøyaktighet"
description: "Denne artikkelen beskriver hvilke typer prognosetransaksjoner nøyaktigheten at Microsoft Dynamics 365 for operasjonene beregnes, og forklarer hvordan du kan vise de nøyaktige verdiene."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Skjermen prognosen nøyaktighet

Denne artikkelen beskriver hvilke typer prognosetransaksjoner nøyaktigheten at Microsoft Dynamics 365 for operasjonene beregnes, og forklarer hvordan du kan vise de nøyaktige verdiene.

Dynamics 365 for operasjoner beregner følgende typer prognosen nøyaktighet:

-   Historisk prognosenøyaktighet, ved å sammenligne den historiske prognosen som hovedplanlegging bruker, med historisk behov. For å vise verdiene (både absolutte verdier og prosentverdier) for historisk prognosenøyaktighet klikk **Vis nøyaktighet** på siden **Detaljer om behovsprognose**.
-   Den beregnede nøyaktigheten for prognosemodellen som brukes til å generere prediksjoner. Du kan vise nøyaktighet i prosent under **Modelldetaljer - MAPE** på siden **Detaljer om behovsprognose**. 

**Merk:** Hvis du bruker Dynamics-365 for operasjoner behov prognostisering Microsoft Learning hvis maskinen Azure service, beregning av intern modell nøyaktighet er basert på datasettet test. Hvis du vil angi størrelsen på test-datasett, kan du angi de **TEST\_SATT\_størrelse\_PROSENT** parameter i den **etterspørselen prognoser parametere** siden. For eksempel hvis du setter verdien til **20**, vil de siste 20 prosentene av historiske data bli brukt til å beregne den interne modellnøyaktigheten.


<a name="see-also"></a>Se også
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


