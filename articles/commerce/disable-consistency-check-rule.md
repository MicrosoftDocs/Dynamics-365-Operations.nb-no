---
title: Deaktivere regler i konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for deaktivering av regler i konsekvenskontroll for transaksjon i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5eb2af7e3090daabccd338d5d0bc6a6ebc4ea663
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982696"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Deaktivere regler i konsekvenskontroll for detaljhandelstransaksjon 

[!include [banner](../includes/banner.md)]

Forhandlere kan ha forretningsscenarier og -prosesser som er unike for dem. Derfor gjelder ikke alle reglene som er inkludert som standard i konsekvenskontrollen for Commerce-transaksjon, for alle forhandlere. Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Commerce funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.

Hvis du vil vise listen over regler som er tilgjengelige i konsekvenskontrollen for transaksjon i miljøet ditt, og i tillegg vise statusen for hver regel, går du til **Retail og Commerce \> Hovedkvarteroppsett \> Parameter \> Commerce-parametere** og velger fanen **Transaksjonsvalidering**.

Som standard er statusen for alle regler satt til **Aktivert**. Derfor brukes alle reglene til å validere transaksjoner før de hentes inn i handelsutdragene. Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**. Deaktiverte regler tas ikke med når transaksjoner valideres under prosessen for beregning av utdrag.

Hvis du vil omgå hele valideringsprosessen, uavhengig av reglene som er aktivert, går du til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Commerce-parametere**, og deretter setter du verdien for alternativet **Deaktiver konsekvenskontroll for Commerce-transaksjoner** i fanen **Transaksjonsvalidering** til **Ja**. Når dette alternativet er satt til **Nei**, kan det ikke settes tilbake til **Ja** fra brukergrensesnittet.
