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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="efd70-103">Manglende feltinnstillinger når varemodellgrupper kopieres til en annen juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="efd70-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="efd70-104">KB-nummer: 4612800</span><span class="sxs-lookup"><span data-stu-id="efd70-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="efd70-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="efd70-105">Symptoms</span></span>

<span data-ttu-id="efd70-106">Når du kopierer varemodellgrupper til en annen juridisk enhet (firma) ved hjelp av *beholdningspolicyer for varemodellgruppe*, mangler noen feltinnstillinger (for eksempel lagermodellen og beskrivelsen) i den nye modellgruppen i den juridiske enheten for mål.</span><span class="sxs-lookup"><span data-stu-id="efd70-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="efd70-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="efd70-107">Resolution</span></span>

<span data-ttu-id="efd70-108">Hvis du vil opprette en fullstendig kopi av en varemodellgruppe til en annen juridisk enhet, må du også velge både lagerpolicyer for varemodellgrupper (`InventInventoryPolicyEntity`) og policyer for kostnadsflytantagelse (`InventCostFlowAssumptionPolicyEntity`) som er knyttet til varemodellgruppen.</span><span class="sxs-lookup"><span data-stu-id="efd70-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
