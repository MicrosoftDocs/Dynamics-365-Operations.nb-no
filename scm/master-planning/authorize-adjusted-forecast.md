---
title: Godkjenne en justert prognose
description: "Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Godkjenne en justert prognose

Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller.

Ikke alle prognosedata må autoriseres umiddelbart. Du kan angi i start- og sluttdatoene for perioden som prognosen er autorisert for. Denne funksjonen lar deg låse bestemt perioder. 

Start- og sluttdatoene du angir må samsvare med de start- og sluttdatoene for kategorien som prognosen er generert i. Systemet håndhever denne begrensningen, og justerer automatisk datoer, hvis justering er nødvendig. 

I **Detaljer** -kategorien på siden **Autorisasjon** kan du vise detaljer om prognosen som sist ble generert. 

Du kan velge firmaene og prognosemodellene for å autorisere prognosen for bruk. Rutenettet omfatter som standard alle firmaene som prognosebehov er opprettet for. Prognosemodellen som samsvarer med den gjeldende prognoseplanen som er angitt i hovedplanleggingsparametere, er forhåndsutfylt for hvert firma. Du kan imidlertid endre denne prognosemodellen til en hvilken som helst prognosemodell som tilhører selskapet. Hvis ingen prognosebehovsdata er generert for et selskap som er valgt, får du en advarsel ved importen. 

Det er svært viktig at du forstår hvordan avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** fungerer. Hvis du har foretatt manuelle justeringer til statistisk grunnlinjen prognose, er de justerte verdiene autorisert for bruk, selv om det er merket. Endringene forkastes imidlertid etter godkjenning. Neste gang det opprettes en prognose, er denne prognosen derfor bare en statistisk prognose og har ikke noen manuell overstyring, selv om **Overfør manuelle justeringer til behovsprognosen** er valgt. Derfor kan du betrakte avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** som en mekanisme som lar deg beholde eller forkaste alle manuelle endringer.

<a name="see-also"></a>Se også
--------

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


