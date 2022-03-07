---
title: Manglende feltinnstillinger når varemodellgrupper kopieres til en annen juridisk enhet
description: Feltinnstillinger mangler når varemodellgrupper kopieres til en annen juridisk enhet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026774"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Manglende feltinnstillinger når varemodellgrupper kopieres til en annen juridisk enhet

KB-nummer: 4612800

## <a name="symptoms"></a>Symptomer

Når du kopierer varemodellgrupper til en annen juridisk enhet (firma) ved hjelp av *beholdningspolicyer for varemodellgruppe*, mangler noen feltinnstillinger (for eksempel lagermodellen og beskrivelsen) i den nye modellgruppen i den juridiske enheten for mål.

## <a name="resolution"></a>Oppløsning

Hvis du vil opprette en fullstendig kopi av en varemodellgruppe til en annen juridisk enhet, må du også velge både lagerpolicyer for varemodellgrupper (`InventInventoryPolicyEntity`) og policyer for kostnadsflytantagelse (`InventCostFlowAssumptionPolicyEntity`) som er knyttet til varemodellgruppen.
