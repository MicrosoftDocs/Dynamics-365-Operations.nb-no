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
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026783"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Du kan ikke oppdatere anslått enhetskostnad når du importerer behovsprognoseposter

KB-nummer: 4614109

## <a name="symptoms"></a>Symptomer

Når du bruker dataenheter til å importere behovsprognoseposter, oppdateres ikke verdien for **anslått enhetskostnad** for eksisterende poster slik at den samsvarer med de importerte dataene.

## <a name="cause"></a>Årsak

**Anslått enhetskostnad** er et skrivebeskyttet felt. Verdien er basert på produktenhetskostnaden og kan ikke angis direkte ved import.

## <a name="resolution"></a>Oppløsning

Fordi feltet er skrivebeskyttet, kan du ikke importere verdier for det. Verdien blir beregnet i henhold til den eksisterende forretningslogikken.
