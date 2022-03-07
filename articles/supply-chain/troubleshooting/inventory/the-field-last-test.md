---
title: Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes
description: Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026790"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes

KB-nummer: 4612803

## <a name="symptoms"></a>Symptomer

**Sist testet dato**-feltet oppdateres ikke når flere kvalitetsordrer opprettes.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Sist testet dato er ikke knyttet til kvalitetsordrer. Den lagrer datoen da de ferdige varene først ble kjøpt eller produsert. Denne datoen brukes til å beregne den anbefalte holdbarhetsdatoen.
