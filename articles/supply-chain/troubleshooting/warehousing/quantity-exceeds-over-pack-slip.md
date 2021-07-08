---
title: Antallet overskrider overleveringsprosenten under generering av følgeseddel
description: Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider overleveringsprosenten.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249148"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="16001-103">Antallet overskrider overleveringsprosenten under generering av følgeseddel</span><span class="sxs-lookup"><span data-stu-id="16001-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="16001-104">Feilkode: SYS24920</span><span class="sxs-lookup"><span data-stu-id="16001-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="16001-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="16001-105">Symptoms</span></span>

<span data-ttu-id="16001-106">Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="16001-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="16001-107">Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="16001-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="16001-108">Linjen overleveres med %1 prosent, men tillatt overlevering er bare %2 prosent.</span><span class="sxs-lookup"><span data-stu-id="16001-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="16001-109">Derfor kan du ikke generere følgeseddelen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="16001-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="16001-110">Årsak</span><span class="sxs-lookup"><span data-stu-id="16001-110">Cause</span></span>

<span data-ttu-id="16001-111">Det plukkede antallet for lasten eller forsendelsen er mer enn det bestilte antallet og er ikke innenfor området for overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="16001-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="16001-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="16001-112">Resolution</span></span>

<span data-ttu-id="16001-113">Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes.</span><span class="sxs-lookup"><span data-stu-id="16001-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="16001-114">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="16001-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="16001-115">Juster lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="16001-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="16001-116">Justere overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="16001-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="16001-117">Reverser og foreta justeringer.</span><span class="sxs-lookup"><span data-stu-id="16001-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="16001-118">Juster lastlinjeantallet</span><span class="sxs-lookup"><span data-stu-id="16001-118">Adjust the load line quantity</span></span>

<span data-ttu-id="16001-119">Bruk fremgangsmåten nedenfor til å justere lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="16001-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="16001-120">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="16001-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="16001-121">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="16001-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="16001-122">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="16001-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="16001-123">I fanen  **Lastlinjer** velger du lastlinjen for varen som overskrider overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="16001-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="16001-124">Velg **Reduser plukket antall** for å justere det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="16001-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="16001-125">Velg  **Ordre** i kategorien **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="16001-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="16001-126">Angi **Antall**-feltet til det plukkede antallet (det vil si til verdien til feltet **Antall for arbeid opprettet**), slik at generering av følgeseddel kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="16001-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="16001-127">Justere overleveringsprosenten</span><span class="sxs-lookup"><span data-stu-id="16001-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="16001-128">Bruk fremgangsmåten nedenfor til å justere overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="16001-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="16001-129">Gå til **Kunder \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="16001-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="16001-130">Velg salgsordren du ikke kan postere en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="16001-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="16001-131">I fanen  **Salgsordrelinjer** velger du salgsordrelinjen for varen som overskrider overleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="16001-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="16001-132">Velg  **Levering** i kategorien **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="16001-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="16001-133">Sett **Overlevering**-feltet til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at generering av følgeseddel kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="16001-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="16001-134">Reversere og foreta justeringer</span><span class="sxs-lookup"><span data-stu-id="16001-134">Reverse and make adjustments</span></span>

<span data-ttu-id="16001-135">Tilbakefør alt som er postert for lasten (for eksempel følgeseddel, forsendelsesbekreftelse og arbeid), foreta salgsordrejusteringer, frigi ordren til lageret på nytt, og fullfør forsendelsesprosedyren.</span><span class="sxs-lookup"><span data-stu-id="16001-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="16001-136">Bruk fremgangsmåten nedenfor til å avbryte en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="16001-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="16001-137">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="16001-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="16001-138">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Annuller følgesedler**.</span><span class="sxs-lookup"><span data-stu-id="16001-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="16001-139">Bruk fremgangsmåten nedenfor til å tilbakeføre en forsendelsesbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="16001-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="16001-140">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="16001-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="16001-141">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="16001-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="16001-142">Bruk fremgangsmåten nedenfor for å reversere arbeid.</span><span class="sxs-lookup"><span data-stu-id="16001-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="16001-143">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="16001-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="16001-144">I handlingsruten velger du **Reverser arbeid** i fanen  **Laster** i gruppen  **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="16001-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
