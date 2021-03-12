---
title: Utelat produkter som har spesifikke produktstatuser
description: Dette emnet forklarer hvordan du utelater produkter basert på statusen deres når planleggingsoptimaliseringsfunksjonaliteten brukes.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992426"
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
