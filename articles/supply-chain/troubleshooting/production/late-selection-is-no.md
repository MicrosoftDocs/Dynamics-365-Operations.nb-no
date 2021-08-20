---
title: Senere valg respekteres ikke når produksjonsordrer tilbakestilles via en satsvis jobb
description: Når du bruker en regelmessig satsvis jobb til å tilbakestille statusen for en produksjonsordre, overholdes ikke sene valg.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741962"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Senere valg respekteres ikke når produksjonsordrer tilbakestilles via en satsvis jobb

KB-nummer: 4614634

## <a name="symptoms"></a>Symptomer

Når du bruker en regelmessig satsvis jobb til å tilbakestille statusen for en produksjonsordre, overholdes ikke sene valg.

## <a name="resolution"></a>Oppløsning

Den gjeldende utformingen støtter ikke bruk av sene valg for *Tilbakestill status*-prosessen.
