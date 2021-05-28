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
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026773"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Senere valg respekteres ikke når produksjonsordrer tilbakestilles via en satsvis jobb

KB-nummer: 4614634

## <a name="symptoms"></a>Symptomer

Når du bruker en regelmessig satsvis jobb til å tilbakestille statusen for en produksjonsordre, overholdes ikke sene valg.

## <a name="resolution"></a>Oppløsning

Den gjeldende utformingen støtter ikke bruk av sene valg for *Tilbakestill status*-prosessen.
