---
title: Du kan ikke oppdatere anslått enhetskostnad når du importerer behovsprognoseposter
description: Når du bruker dataenheter til å importere behovsprognoseposter, oppdateres ikke kostprisen for eksisterende poster slik at den samsvarer med de importerte dataene.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765376"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Du kan ikke oppdatere anslått enhetskostnad når du importerer behovsprognoseposter

KB-nummer: 4614109

## <a name="symptoms"></a>Symptomer

Når du bruker dataenheter til å importere behovsprognoseposter, oppdateres ikke verdien for **anslått enhetskostnad** for eksisterende poster slik at den samsvarer med de importerte dataene.

## <a name="cause"></a>Årsak

**Anslått enhetskostnad** er et skrivebeskyttet felt. Verdien er basert på produktenhetskostnaden og kan ikke angis direkte ved import.

## <a name="resolution"></a>Oppløsning

Fordi feltet er skrivebeskyttet, kan du ikke importere verdier for det. Verdien blir beregnet i henhold til den eksisterende forretningslogikken.
