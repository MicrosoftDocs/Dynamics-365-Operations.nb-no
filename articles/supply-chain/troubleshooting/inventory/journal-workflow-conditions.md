---
title: Arbeidsflytbetingelser for lagerjournal gjelder på journalnivå, ikke linjenivå
description: Betingelser for lagerjournalarbeidsflyt gjelder bare på journalnivå, ikke på linjenivå.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477199"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Arbeidsflytbetingelser for lagerjournal gjelder på journalnivå, ikke linjenivå

## <a name="symptoms"></a>Symptomer

Du kan få dette problemet hvis du for eksempel prøver å definere en betingelse for lagerjournalarbeidsflyt for kostbeløpet. Du definerer betingelsen slik at trinn 1 bare kjøres når kostbeløpet er mindre enn 100. Deretter definerer du en ny betingelse slik at trinn 2 bare kjøres når kostbeløpet er større enn eller lik 100. Når arbeidsflyten deretter kjøres, viser arbeidsflytloggen deretter bare én linje, og den første betingelsen evalueres alltid som *sann*, uavhengig av verdien som sendes.

## <a name="workaround"></a>Løsning

I gjeldende utgivelse gjelder betingelser for lagerarbeidsflyt bare på journalnivå, ikke på linjenivå. Denne virkemåten er standard. Det anbefales at du bare angir betingelseskriteriene for attributter på journalnivå.
