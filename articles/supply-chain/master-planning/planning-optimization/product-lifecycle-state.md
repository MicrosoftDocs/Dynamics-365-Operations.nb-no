---
title: Utelat produkter som har spesifikke produktstatuser
description: Dette emnet forklarer hvordan du utelater produkter basert på statusen deres når planleggingsoptimaliseringsfunksjonaliteten brukes.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 030bdea7c03dd5eb3347c1d43acd1aeabdf566602872dd8ef5aab6d16b06f503
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739041"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Utelat produkter som har spesifikke produktstatuser

[!include [banner](../../includes/banner.md)]

Frigitte produkter og frigitte produktversjoner omfatter et felt for **produktstatus**. I dette feltet kan du kontrollere, blant annet hvilke produkter som er inkludert under hovedplanlegging. Du kan legge til, fjerne og redigere statuser etter behov ved å gå til **Produktinformasjonsbehandling \> Oppsett \> Produktstatus**. For hver produktstatus setter du alternativet **Er aktiv for planlegging** til *Ja* hvis produkter som har denne statusen, skal inkluderes under hovedplanlegging. Når alternativet er satt til *Nei*, blir tilknyttede produkter og varianter utelatt fra all hovedplanlegging og alle beregninger på stykklistenivå.

Frigitte produkter og varianter der feltet **Produktstatus** er tomt, behandles som om de har en produktstatus der alternativet **Er aktiv for planlegging** er satt til *Ja*. De blir med andre ord inkludert under hovedplanlegging.

> [!NOTE]
> For å unngå unødvendige forsyningsforslag anbefaler vi sterkt at du knytter alle foreldede, frigitte produkter og varianter til en produktstatus der alternativet **Er aktiv for planlegging** er satt til *Nei*. Denne fremgangsmåten er spesielt viktig når du arbeider med produktkonfigurasjonsvarianter som ikke kan brukes på nytt, fordi det vil bidra til å forhindre avfall.

## <a name="related-resources"></a>Relaterte ressurser

Hvis du vil ha mer informasjon om produktstatuser, kan du se [Oversikt over produktstatus](../../pim/product-lifecycle.md).

Hvis du vil ha mer informasjon som omfatter fremgangsmåte for å bruke produktstatuser til å utelate produkter fra hovedplanlegging og stykklistenivåberegninger, kan du se [Opprette en produktstatus for å utelukke produkter fra hovedplanlegging](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]