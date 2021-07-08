---
title: Antallet overskrider underleveringsprosenten under generering av følgeseddel
description: Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider underleveringsprosenten.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249146"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="513c6-103">Antallet overskrider underleveringsprosenten under generering av følgeseddel</span><span class="sxs-lookup"><span data-stu-id="513c6-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="513c6-104">Feilkode: SYS24921</span><span class="sxs-lookup"><span data-stu-id="513c6-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="513c6-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="513c6-105">Symptoms</span></span>

<span data-ttu-id="513c6-106">Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="513c6-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="513c6-107">Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="513c6-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="513c6-108">Linjen underleveres med %1 prosent, men tillatt underlevering er bare %2 prosent.</span><span class="sxs-lookup"><span data-stu-id="513c6-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="513c6-109">Derfor kan du ikke generere følgeseddelen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="513c6-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="513c6-110">Årsak</span><span class="sxs-lookup"><span data-stu-id="513c6-110">Cause</span></span>

<span data-ttu-id="513c6-111">Det plukkede antallet for lasten eller forsendelsen er mindre enn det bestilte antallet og er ikke innenfor området for underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="513c6-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="513c6-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="513c6-112">Resolution</span></span>

<span data-ttu-id="513c6-113">Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes.</span><span class="sxs-lookup"><span data-stu-id="513c6-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="513c6-114">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="513c6-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="513c6-115">Juster underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="513c6-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="513c6-116">Reverser og foreta justeringer.</span><span class="sxs-lookup"><span data-stu-id="513c6-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="513c6-117">Justere underleveringsprosenten</span><span class="sxs-lookup"><span data-stu-id="513c6-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="513c6-118">Bruk fremgangsmåten nedenfor til å justere underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="513c6-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="513c6-119">Gå til **Kunder \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="513c6-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="513c6-120">Velg salgsordren du ikke kan postere en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="513c6-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="513c6-121">I fanen  **Salgsordrelinjer** velger du salgsordrelinjen for varen som overskrider underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="513c6-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="513c6-122">Velg  **Levering** i kategorien **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="513c6-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="513c6-123">Sett **Underlevering**-feltet til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at generering av følgeseddel kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="513c6-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="513c6-124">Reversere og foreta justeringer</span><span class="sxs-lookup"><span data-stu-id="513c6-124">Reverse and make adjustments</span></span>

<span data-ttu-id="513c6-125">Tilbakefør alt som er postert for lasten (for eksempel følgeseddel, forsendelsesbekreftelse og arbeid), foreta salgsordrejusteringer, frigi ordren til lageret på nytt, og fullfør forsendelsesprosedyren.</span><span class="sxs-lookup"><span data-stu-id="513c6-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="513c6-126">Bruk fremgangsmåten nedenfor til å avbryte en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="513c6-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="513c6-127">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="513c6-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="513c6-128">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Annuller følgesedler**.</span><span class="sxs-lookup"><span data-stu-id="513c6-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="513c6-129">Bruk fremgangsmåten nedenfor til å tilbakeføre en forsendelsesbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="513c6-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="513c6-130">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="513c6-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="513c6-131">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="513c6-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="513c6-132">Bruk fremgangsmåten nedenfor for å reversere arbeid.</span><span class="sxs-lookup"><span data-stu-id="513c6-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="513c6-133">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="513c6-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="513c6-134">I handlingsruten velger du **Reverser arbeid** i fanen  **Laster** i gruppen  **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="513c6-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
