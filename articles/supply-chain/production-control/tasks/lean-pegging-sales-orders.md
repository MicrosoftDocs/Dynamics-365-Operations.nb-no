---
title: Lean-utligning fra salgsordrer
description: Denne prosedyren fokuserer på å validere utligningstreet fra en salgslinje der varen produseres med Kanbaner.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457e7128bed2232a3e092b31136f768940482741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994185"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="f9324-103">Lean-utligning fra salgsordrer</span><span class="sxs-lookup"><span data-stu-id="f9324-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9324-104">Denne prosedyren fokuserer på å validere utligningstreet fra en salgslinje der varen produseres med Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="f9324-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="f9324-105">Alle Kanban-jobbene planlegges etter valideringen av utligningstreet.</span><span class="sxs-lookup"><span data-stu-id="f9324-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="f9324-106">Dette er nyttig for ordrescenarier der ordremottakeren må sikre at produksjonen kan starte umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="f9324-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="f9324-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f9324-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f9324-108">Denne prosedyren er ment for avanserte ordremottakere som jobber i et lean-firma.</span><span class="sxs-lookup"><span data-stu-id="f9324-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="f9324-109">Opprette en salgsordre for en Kanban-styrt vare</span><span class="sxs-lookup"><span data-stu-id="f9324-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="f9324-110">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f9324-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="f9324-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9324-111">Click New.</span></span>
3. <span data-ttu-id="f9324-112">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9324-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="f9324-113">Bruk US-001.</span><span class="sxs-lookup"><span data-stu-id="f9324-113">Use US-001.</span></span>  
4. <span data-ttu-id="f9324-114">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f9324-114">Click OK.</span></span>
5. <span data-ttu-id="f9324-115">Skriv inn L0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="f9324-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="f9324-116">Sett verdien for Antall til 30.</span><span class="sxs-lookup"><span data-stu-id="f9324-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="f9324-117">Det er viktig at antallet er høyere enn 24 for å utløse Kanban-regelen for hendelse.</span><span class="sxs-lookup"><span data-stu-id="f9324-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="f9324-118">Åpne et utligningstre</span><span class="sxs-lookup"><span data-stu-id="f9324-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="f9324-119">Klikk på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="f9324-119">Click Product and supply.</span></span>
2. <span data-ttu-id="f9324-120">Klikk på Vis utligningstre.</span><span class="sxs-lookup"><span data-stu-id="f9324-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="f9324-121">Legg merke til at utligningstreet viser alle nivåer av utligningen som kreves for salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f9324-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="f9324-122">I dette tilfellet er det to nivåer med Kanbaner og alle de nødvendige komponentene.</span><span class="sxs-lookup"><span data-stu-id="f9324-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="f9324-123">Planlegge utligningstreet</span><span class="sxs-lookup"><span data-stu-id="f9324-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="f9324-124">Velg Salgslinje 000832 \ Kanban 000558.</span><span class="sxs-lookup"><span data-stu-id="f9324-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="f9324-125">Vis delen Kanban-jobber.</span><span class="sxs-lookup"><span data-stu-id="f9324-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="f9324-126">Legg merke til at jobbstatusen for Kanban-jobben er Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="f9324-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="f9324-127">Klikk på Planlegg helt utligningstre.</span><span class="sxs-lookup"><span data-stu-id="f9324-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="f9324-128">Dette vil planlegge alle Kanban-jobber i utligningstreet, og endre jobbstatusen fra Ikke planlagt til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="f9324-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="f9324-129">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="f9324-129">Refresh the page.</span></span>
    * <span data-ttu-id="f9324-130">Legg merke til at Kanban-jobbstatusen endres fra Ikke planlagt til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="f9324-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="f9324-131">Velg Salgslinje 000832 \ Kanban 000558\ Problem for L0001\ Kanban 000559 i treet.</span><span class="sxs-lookup"><span data-stu-id="f9324-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="f9324-132">Jobben for den andre Kanbanen planlegges også fordi hele utligningstreet planlegges.</span><span class="sxs-lookup"><span data-stu-id="f9324-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="f9324-133">Legg merke til at Kanban-jobbstatusen endres fra Ikke planlagt til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="f9324-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

