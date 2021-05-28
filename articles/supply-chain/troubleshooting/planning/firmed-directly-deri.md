---
title: Direkte avledede autoriserte ordrer behandles av en Til vurdering-arbeidsflyt
description: Direkte avledede autoriserte ordrer behandles av en arbeidsflyt som har statuen Til vurdering.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026787"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="1e96f-103">Direkte avledede autoriserte ordrer behandles av en Til vurdering-arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="1e96f-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="1e96f-104">KB-nummer: 4612450</span><span class="sxs-lookup"><span data-stu-id="1e96f-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="1e96f-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="1e96f-105">Symptoms</span></span>

<span data-ttu-id="1e96f-106">Direkte avledede autoriserte ordrer behandles av en arbeidsflyt som har statuen *Til vurdering*.</span><span class="sxs-lookup"><span data-stu-id="1e96f-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="1e96f-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="1e96f-107">Resolution</span></span>

<span data-ttu-id="1e96f-108">Når endringssporing er aktivert, er statusen *Til vurdering* tilordnet til autoriserte avledede ordrer (bestillinger fra underleverandør).</span><span class="sxs-lookup"><span data-stu-id="1e96f-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="1e96f-109">Hvis en bestilling er avledet (en underleverandørbestilling), blir den bare sendt til en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="1e96f-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="1e96f-110">Hvis en bestilling er et autorisert bestillingsforslag, godkjennes det automatisk for å sikre at planleggingsmotoren ikke oppretter nye planlagte bestillinger mens bestillingen fremdeles har *Utkast*-status.</span><span class="sxs-lookup"><span data-stu-id="1e96f-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
