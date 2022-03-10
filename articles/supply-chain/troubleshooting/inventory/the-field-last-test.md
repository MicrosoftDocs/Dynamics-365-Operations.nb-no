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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742034"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Sist testet dato-feltet oppdateres ikke når flere kvalitetsordrer opprettes

KB-nummer: 4612803

## <a name="symptoms"></a>Symptomer

**Sist testet dato**-feltet oppdateres ikke når flere kvalitetsordrer opprettes.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Sist testet dato er ikke knyttet til kvalitetsordrer. Den lagrer datoen da de ferdige varene først ble kjøpt eller produsert. Denne datoen brukes til å beregne den anbefalte holdbarhetsdatoen.
