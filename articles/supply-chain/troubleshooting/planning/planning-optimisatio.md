---
title: Planlagt bestilling opprettes når det finnes et innkjøp innen negative dager
description: Hvis dekningskoden er Min/maks, oppretter Planleggingsoptimalisering et bestillingsforslag når det finnes et innkjøp innen negative dager.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026785"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="8da4c-103">Planlagt bestilling opprettes når det finnes et innkjøp innen negative dager</span><span class="sxs-lookup"><span data-stu-id="8da4c-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="8da4c-104">KB-nummer: 4614298</span><span class="sxs-lookup"><span data-stu-id="8da4c-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="8da4c-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="8da4c-105">Symptoms</span></span>

<span data-ttu-id="8da4c-106">Hvis dekningskoden er *Min/maks*, oppretter Planleggingsoptimalisering et bestillingsforslag når det finnes et innkjøp innen negative dager.</span><span class="sxs-lookup"><span data-stu-id="8da4c-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="8da4c-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="8da4c-107">Resolution</span></span>

<span data-ttu-id="8da4c-108">Planleggingsoptimalisering støtter ikke negative dager.</span><span class="sxs-lookup"><span data-stu-id="8da4c-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="8da4c-109">Det sikrer imidlertid alltid at planlagte bestillinger ikke blir planlagt innen leveringstiden i forhold til gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="8da4c-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="8da4c-110">Leveringstiden for innkjøpet er for eksempel 10 dager, og en bestilling forventes å ankomme åtte dager fra i dag.</span><span class="sxs-lookup"><span data-stu-id="8da4c-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="8da4c-111">I dette tilfellet vil bestillingen brukes som forsyning for etterspørsel som er fem dager fra i dag.</span><span class="sxs-lookup"><span data-stu-id="8da4c-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="8da4c-112">Vi anbefaler derfor at du justerer leveringstiden for å dekke alle (eller nesten alle) scenariene.</span><span class="sxs-lookup"><span data-stu-id="8da4c-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
