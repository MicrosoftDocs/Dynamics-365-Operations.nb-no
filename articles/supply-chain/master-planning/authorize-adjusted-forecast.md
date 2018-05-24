---
title: Autoriser en justert prognose
description: "Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 64838fd20349c21bf3c0a3b9a3c68d4f19f60745
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="authorize-an-adjusted-forecast"></a>Autoriser en justert prognose

[!include [banner](../includes/banner.md)]

Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller.

Ikke alle prognosedata må autoriseres umiddelbart. Du kan angi i start- og sluttdatoene for perioden som prognosen er autorisert for. Denne funksjonen lar deg låse bestemt perioder. 

Start- og sluttdatoene du angir, må samsvare med start- og sluttdatoene for perioden som prognosen er generert i. Systemet håndhever denne begrensningen, og justerer automatisk datoene hvis justering er nødvendig. 

I **Detaljer** -kategorien på siden **Autorisasjon** kan du vise detaljer om prognosen som sist ble generert. 

Du kan velge firmaene og prognosemodellene for å autorisere prognosen for bruk. Rutenettet omfatter som standard alle firmaene som prognosebehov er opprettet for. Prognosemodellen som samsvarer med den gjeldende prognoseplanen som er angitt i hovedplanleggingsparametere, er forhåndsutfylt for hvert firma. Du kan imidlertid endre denne prognosemodellen til en hvilken som helst prognosemodell som tilhører selskapet. Hvis ingen prognosebehovsdata er generert for et selskap som er valgt, får du en advarsel ved importen. 

Det er svært viktig at du forstår hvordan avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** fungerer. Hvis du har foretatt manuelle justeringer i den statistiske basislinjeprognosen, er de justerte verdiene autorisert for bruk, selv om denne avmerkingsboksen er deaktivert. Endringene forkastes imidlertid etter godkjenning. Neste gang det opprettes en prognose, er denne prognosen derfor bare en statistisk prognose og har ikke noen manuell overstyring, selv om **Overfør manuelle justeringer til behovsprognosen** er valgt. Derfor kan du betrakte avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** som en mekanisme som lar deg beholde eller forkaste alle manuelle endringer.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)

[Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md)




