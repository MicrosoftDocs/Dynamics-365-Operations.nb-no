---
title: Deaktiver regler i konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for regler for deaktivering av konsekvenskontroll for detaljhandelstransaksjon i Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586303"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Deaktiver regler i konsekvenskontroll for detaljhandelstransaksjon 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Forhandlere kan ha forretningsscenarier og -prosesser som er unike for dem. Derfor gjelder ikke alle reglene som er inkludert som standard i konsekvenskontrollen for detaljhandelstransaksjon, for alle forhandlere. Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Retail funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.

Hvis du vil vise listen over regler som er tilgjengelige i konsekvenskontrollen for detaljhandelstransaksjon i miljøet ditt, og i tillegg vise statusen for hver regel, går du til **Detaljhandel \> Hovedkvarteroppsett \> Parameter \> Detaljhandelsparametere** og velger kategorien **Transaksjonsvalidering**.

Som standard er statusen for alle regler satt til **Aktivert**. Derfor brukes alle reglene til å validere detaljhandelstransaksjoner før de hentes inn i detaljhandelsutdragene. Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**. Deaktiverte regler tas ikke med når detaljhandelstransaksjoner valideres under prosessen for beregning av utdrag.

Hvis du vil omgå hele valideringsprosessen, uavhengig av reglene som er aktivert, går du til **Detaljhandel \> Hovedkvarteroppsett \> Parametere \> Detaljhandelsparametere**, og deretter setter du verdien for alternativet **Deaktiver konsekvenskontroll for detaljhandelstransaksjoner** i kategorien **Transaksjonsvalidering** til **Ja**. Når dette alternativet er satt til **Nei**, kan det ikke settes tilbake til **Ja** fra brukergrensesnittet.
