---
title: Sekvensiere produksjonsjobber for prosessproduksjon
description: Denne fremgangsmåten bruker malingsprodukter som eksempel for å vise hvordan du sorterer planlagte ordrer i henhold til prioriteten for farge og pakkestørrelse.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db2c881f60b6e5251e2bcdf198da9e1c9f39a0e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434366"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="539e7-103">Sekvensiere produksjonsjobber for prosessproduksjon</span><span class="sxs-lookup"><span data-stu-id="539e7-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="539e7-104">Denne fremgangsmåten bruker malingsprodukter som eksempel for å vise hvordan du sorterer planlagte ordrer i henhold til prioriteten for farge og pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="539e7-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="539e7-105">Demonstrasjonsdatafirmaet USPI brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="539e7-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="539e7-106">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="539e7-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="539e7-107">Kjøre hovedplanlegging for USPI</span><span class="sxs-lookup"><span data-stu-id="539e7-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="539e7-108">Gå til Hovedplanlegging > Hovedplanlegging > Kjør > Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="539e7-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="539e7-109">Klikk rullegardinknappen i feltet Hovedplan for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="539e7-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="539e7-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539e7-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="539e7-111">Velg MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="539e7-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="539e7-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="539e7-112">Click OK.</span></span>
    * <span data-ttu-id="539e7-113">Dette starter hovedplanlegging, inkludert sekvensprosessen.</span><span class="sxs-lookup"><span data-stu-id="539e7-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="539e7-114">Denne prosessen kan ta noen minutter.</span><span class="sxs-lookup"><span data-stu-id="539e7-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="539e7-115">Vise planlagte bestillinger for malingsprodukter</span><span class="sxs-lookup"><span data-stu-id="539e7-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="539e7-116">Gå til Hovedplanlegging > Hovedplanlegging > Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="539e7-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="539e7-117">Vis faktaboks for varedetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="539e7-118">Vis faktaboks for Tidsplandetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="539e7-119">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="539e7-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="539e7-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="539e7-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="539e7-121">Velg MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="539e7-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="539e7-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539e7-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="539e7-123">Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P300.</span><span class="sxs-lookup"><span data-stu-id="539e7-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="539e7-124">Lås opp for å gå til høyre for å vise ordredato og leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="539e7-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="539e7-125">Legg merke til at disse varene har ordredatoen I dag, og leveringsdatoene for de planlagte ordrene er ikke i rekkefølge etter prioritet for farge og pakkestørrelse, som vist i produktnavnet.</span><span class="sxs-lookup"><span data-stu-id="539e7-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="539e7-126">Du kan holder musepekeren over et varenummer for å se varenavn og prioritet.</span><span class="sxs-lookup"><span data-stu-id="539e7-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="539e7-127">Sekvens for planlagte ordre for maling</span><span class="sxs-lookup"><span data-stu-id="539e7-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="539e7-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="539e7-128">Close the page.</span></span>
2. <span data-ttu-id="539e7-129">Gå til Hovedplanlegging > Hovedplanlegging > Sekvenserte planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="539e7-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="539e7-130">Vis faktaboks for varedetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="539e7-131">Vis faktaboks for Tidsplandetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="539e7-132">Obs!  Her ser du at startdato/-klokkeslett for de planlagte ordrene er i rekkefølge i henhold til farge og pakkestørrelse i en tidsperiode på 28 dager.</span><span class="sxs-lookup"><span data-stu-id="539e7-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="539e7-133">Disse periodene er definert av et tall i feltet Kampanje.</span><span class="sxs-lookup"><span data-stu-id="539e7-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="539e7-134">Skjemaet Sekvensert planlagt ordre fungerer som det vanlige planlagte bestillingsskjemaet, og produksjonsplanleggeren kan bekrefte planlagte ordre her.</span><span class="sxs-lookup"><span data-stu-id="539e7-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="539e7-135">Merk alle rader.</span><span class="sxs-lookup"><span data-stu-id="539e7-135">Mark all rows.</span></span>
6. <span data-ttu-id="539e7-136">Klikk Godta.</span><span class="sxs-lookup"><span data-stu-id="539e7-136">Click Accept.</span></span>
    * <span data-ttu-id="539e7-137">Dette vil oppdatere de planlagte ordrene med den valgte sekvenshandlingen Utsett eller Forskudd.</span><span class="sxs-lookup"><span data-stu-id="539e7-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="539e7-138">Kontroller rekkefølgen for de planlagte ordrene</span><span class="sxs-lookup"><span data-stu-id="539e7-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="539e7-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="539e7-139">Close the page.</span></span>
2. <span data-ttu-id="539e7-140">Gå til Hovedplanlegging > Hovedplanlegging > Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="539e7-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="539e7-141">Vis faktaboks for varedetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="539e7-142">Vis faktaboks for Tidsplandetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="539e7-143">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="539e7-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="539e7-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="539e7-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="539e7-145">Velg MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="539e7-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="539e7-146">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539e7-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="539e7-147">Bruk hurtigfilteret til å filtrere på feltet Varenummer med verdien P300.</span><span class="sxs-lookup"><span data-stu-id="539e7-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="539e7-148">Legg merke til at ordrene nå er i rekkefølge i henhold til prioriteten for farge og størrelse, og de planlagte ordrene starter på den tidligste ordredatoen og leveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="539e7-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="539e7-149">Valider Ordredato-kolonnen eller Startdato i faktaboksen Tidsplandetaljer.</span><span class="sxs-lookup"><span data-stu-id="539e7-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

