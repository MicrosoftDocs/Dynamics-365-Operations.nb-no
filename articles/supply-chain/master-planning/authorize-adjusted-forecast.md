---
title: Autoriser en justert prognose
description: Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4954b70e56482e419d81485b544cb5d0b4e4a3ce
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740718"
---
# <a name="authorize-an-adjusted-forecast"></a>Autoriser en justert prognose

[!include [banner](../includes/banner.md)]

Ikke alle prognosedata må autoriseres umiddelbart. Denne artikkelen forklarer hvordan du kan angi perioden som en prognose er autorisert for. Den forklarer også hvordan du godkjenner prognosen for bestemte firmaer og prognosemodeller.

Ikke alle prognosedata må autoriseres umiddelbart. Du kan angi i start- og sluttdatoene for perioden som prognosen er autorisert for. Denne funksjonen lar deg låse bestemt perioder. 

Start- og sluttdatoene du angir, må samsvare med start- og sluttdatoene for perioden som prognosen er generert i. Systemet håndhever denne begrensningen, og justerer automatisk datoene hvis justering er nødvendig. 

I **Detaljer** -fanen på siden **Autorisasjon** kan du vise detaljer om prognosen som sist ble generert. 

Du kan velge firmaene og prognosemodellene for å autorisere prognosen for bruk. Rutenettet omfatter som standard alle firmaene som prognosebehov er opprettet for. Prognosemodellen som samsvarer med den gjeldende prognoseplanen som er angitt i hovedplanleggingsparametere, er forhåndsutfylt for hvert firma. Du kan imidlertid endre denne prognosemodellen til en hvilken som helst prognosemodell som tilhører selskapet. Hvis ingen prognosebehovsdata er generert for et selskap som er valgt, får du en advarsel ved importen. 

Det er svært viktig at du forstår hvordan avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** fungerer. Hvis du har foretatt manuelle justeringer i den statistiske basislinjeprognosen, er de justerte verdiene autorisert for bruk, selv om denne avmerkingsboksen er deaktivert. Endringene forkastes imidlertid etter godkjenning. Neste gang det opprettes en prognose, er denne prognosen derfor bare en statistisk prognose og har ikke noen manuell overstyring, selv om **Overfør manuelle justeringer til behovsprognosen** er valgt. Derfor kan du betrakte avmerkingsboksen **Lagre de manuelle justeringene som er gjort i behovsprognosen for basislinjen** som en mekanisme som lar deg beholde eller forkaste alle manuelle endringer.

## <a name="additional-resources"></a>Tilleggsressurser

- [Foreta manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)
- [Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]