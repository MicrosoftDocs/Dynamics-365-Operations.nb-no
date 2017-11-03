---
title: Vedlikehold planlagte ordrer
description: Denne artikkelen gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8931908fbf643a8154da70d2ad065ea47d2aa4e6
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="2aafc-104">Vedlikehold planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="2aafc-104">Maintain planned orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2aafc-105">Denne artikkelen gir informasjon om hvordan du behandler planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="2aafc-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="2aafc-106">Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="2aafc-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="2aafc-107">Du kan administrere planlagte bestillinger fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt bestilling** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Overføringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="2aafc-108">Du kan bruke **Status**-feltet til å spore fremdriften.</span><span class="sxs-lookup"><span data-stu-id="2aafc-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="2aafc-109">Følgende verdier brukes:</span><span class="sxs-lookup"><span data-stu-id="2aafc-109">The following values are used:</span></span>

-   <span data-ttu-id="2aafc-110">Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen **Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="2aafc-111">Hvis du velger ikke å autorisere en planlagt bestilling, kan du gi den statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="2aafc-112">Når du velger å autorisere en planlagt bestilling, kan du gi den statusen **Godkjent**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="2aafc-113">Denne statusen innebærer at du godkjenner autoriseringen av den planlagte bestillingen, men den er ikke autorisert ennå.</span><span class="sxs-lookup"><span data-stu-id="2aafc-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="2aafc-114">**Obs!** En godkjent planlagt bestilling overføres i gjeldende tilstand til neste hovedplanberegning.</span><span class="sxs-lookup"><span data-stu-id="2aafc-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="2aafc-115">Du kan autorisere planlagte bestillinger ved å klikke **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="2aafc-116">Du kan autorisere følgende planlagte bestillinger:</span><span class="sxs-lookup"><span data-stu-id="2aafc-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="2aafc-117">Den planlagte bestillingen som er merket.</span><span class="sxs-lookup"><span data-stu-id="2aafc-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="2aafc-118">Flere planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="2aafc-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="2aafc-119">Planlagte bestillinger som genereres gjennom en nedbryting fra siden **Nedbryting**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="2aafc-120">Klikk **Planlagte bestillinger**, merk den planlagte bestillingen, og klikk deretter **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="2aafc-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="2aafc-121">Når en planlagt bestilling autoriseres, flyttes den til bestillingsdelen i den aktuelle modulen.</span><span class="sxs-lookup"><span data-stu-id="2aafc-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="2aafc-122">**Obs!** Du kan høyreklikke en planlagt bestilling med en bestemt status og filtrere etter andre planlagte bestillinger med samme status.</span><span class="sxs-lookup"><span data-stu-id="2aafc-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="2aafc-123">Denne funksjonen er nyttig hvis du for eksempel vil filtrere etter alle planlagte bestillinger med statusen **Godkjent**, slik at du deretter kan autorisere dem.</span><span class="sxs-lookup"><span data-stu-id="2aafc-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="2aafc-124">Se også</span><span class="sxs-lookup"><span data-stu-id="2aafc-124">See also</span></span>
--------

[<span data-ttu-id="2aafc-125">Hovedplaner</span><span class="sxs-lookup"><span data-stu-id="2aafc-125">Master plans</span></span>](master-plans.md)




