---
title: "Systemgruppering i en åpen arbeidsliste"
description: "Dette emnet beskriver hvordan du filtrerer den åpne arbeidslisten på en mobilenhet."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="e7783-103">Systemgruppering i en åpen arbeidsliste</span><span class="sxs-lookup"><span data-stu-id="e7783-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e7783-104">Ved hjelp av et felt for systemgruppering, kan du filtrere en åpen arbeidslisten uten å måtte redigere menyelementet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="e7783-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="e7783-105">Der det er aktuelt, fungerer systemgrupperinger for å filtrere en arbeidslisten i et enkelt arbeidshodefelt.</span><span class="sxs-lookup"><span data-stu-id="e7783-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="e7783-106">Du kan ikke bruke systemgruppering til å filtrere på linjenivåfelter.</span><span class="sxs-lookup"><span data-stu-id="e7783-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="e7783-107">Definere systemgruppering i en åpen arbeidsliste</span><span class="sxs-lookup"><span data-stu-id="e7783-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="e7783-108">Bruk disse trinnene til å definere systemgruppering i en åpen arbeidsliste.</span><span class="sxs-lookup"><span data-stu-id="e7783-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="e7783-109">Velg **modus: indirekte** og **Aktivitetskode: Vis åpen arbeidsliste** fra et menyelement for mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="e7783-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="e7783-110">Følgende alternativer blir tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="e7783-110">The following options become available.</span></span> <span data-ttu-id="e7783-111">Disse alternativene er nødvendig for systemgruppring på en åpen arbeidsliste.</span><span class="sxs-lookup"><span data-stu-id="e7783-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="e7783-112">Alternativ</span><span class="sxs-lookup"><span data-stu-id="e7783-112">Option</span></span>        | <span data-ttu-id="e7783-113">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e7783-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="e7783-114">Tillat systemgruppering</span><span class="sxs-lookup"><span data-stu-id="e7783-114">Allow system grouping</span></span>   | <span data-ttu-id="e7783-115">Aktiverer systemgruppering for et valgt menyelement for arbeidsliste.</span><span class="sxs-lookup"><span data-stu-id="e7783-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="e7783-116">Systemgrupperingsfelt</span><span class="sxs-lookup"><span data-stu-id="e7783-116">System grouping field</span></span>   | <span data-ttu-id="e7783-117">Bare tilgjengelig hvis **Tillat systemarbeid** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e7783-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="e7783-118">Velg feltet som bestemmer hvordan plukkarbeid grupperes for arbeidere.</span><span class="sxs-lookup"><span data-stu-id="e7783-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="e7783-119">Hvis du for eksempel felger **ShipmentId**-feltet vil arbeideren skanne forsendelses-IDen for å gruppere plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="e7783-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="e7783-120">Alt arbeid for forsendelsen tilordnes deretter til arbeideren.</span><span class="sxs-lookup"><span data-stu-id="e7783-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="e7783-121">Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet.</span><span class="sxs-lookup"><span data-stu-id="e7783-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="e7783-122">Bruk **Systemgrupperingsetikett**-feltet for å informere om hva som skal skannes.</span><span class="sxs-lookup"><span data-stu-id="e7783-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="e7783-123">Systemgrupperingsetikett</span><span class="sxs-lookup"><span data-stu-id="e7783-123">System grouping label</span></span>   | <span data-ttu-id="e7783-124">Bare tilgjengelig hvis **Tillat systemarbeid** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e7783-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="e7783-125">Angi informasjon til arbeideren om hva som skal skannes når plukkarbeid grupperes.</span><span class="sxs-lookup"><span data-stu-id="e7783-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="e7783-126">Hvis du for eksempel bruker **ShipmentId**-feltet til å gruppere plukkarbeid etter forsendelse, kan du angi Forsendelses-ID i feltet.</span><span class="sxs-lookup"><span data-stu-id="e7783-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="e7783-127">Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet.</span><span class="sxs-lookup"><span data-stu-id="e7783-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="e7783-128">Du må også velge feltet du vil gruppere etter i **Systemgruppering**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7783-128">You must also select the field to group by in the **System grouping** field.</span></span>|

