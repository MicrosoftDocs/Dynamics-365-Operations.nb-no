---
title: Antallet du prøver å oppdatere, overskrider det mottatte/leverte antallet.
description: Når du genererer en følgeseddel, inneholder den utgående lasten et antall som overskrider arbeidsantallet som ble plukket og reservert for salgsordren.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249151"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="21e7e-103">Antallet du prøver å oppdatere, overskrider det mottatte/leverte antallet</span><span class="sxs-lookup"><span data-stu-id="21e7e-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="21e7e-104">Feilkode: SYS7676</span><span class="sxs-lookup"><span data-stu-id="21e7e-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="21e7e-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="21e7e-105">Symptoms</span></span>

<span data-ttu-id="21e7e-106">Når du genererer en følgeseddel, inneholder den utgående lasten et antall som overskrider arbeidsantallet som ble plukket og reservert for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="21e7e-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="21e7e-107">Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="21e7e-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="21e7e-108">Antallet du prøver å oppdatere, er større enn det mottatte/leverte antallet.</span><span class="sxs-lookup"><span data-stu-id="21e7e-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="21e7e-109">Derfor kan du ikke generere følgeseddelen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="21e7e-110">Årsak</span><span class="sxs-lookup"><span data-stu-id="21e7e-110">Cause</span></span>

<span data-ttu-id="21e7e-111">Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="21e7e-112">Dette problemet kan for eksempel oppstå hvis belastningslinjeantallet, antall for arbeid opprettet eller det plukkede antallet ikke er nøyaktig.</span><span class="sxs-lookup"><span data-stu-id="21e7e-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="21e7e-113">Løsning</span><span class="sxs-lookup"><span data-stu-id="21e7e-113">Resolution</span></span>

<span data-ttu-id="21e7e-114">Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes.</span><span class="sxs-lookup"><span data-stu-id="21e7e-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="21e7e-115">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="21e7e-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="21e7e-116">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="21e7e-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="21e7e-117">Juster lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="21e7e-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="21e7e-118">Tilbakefør alle plukkregistreringer, og gjør om plukking.</span><span class="sxs-lookup"><span data-stu-id="21e7e-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="21e7e-119">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer</span><span class="sxs-lookup"><span data-stu-id="21e7e-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="21e7e-120">Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="21e7e-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="21e7e-121">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="21e7e-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="21e7e-122">Velg lasten som forsendelsen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="21e7e-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="21e7e-123">I hurtigfanen **Lastlinjer** velger du lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="21e7e-124">Legg merke til verdien i feltet **Antall for arbeid opprettet**.</span><span class="sxs-lookup"><span data-stu-id="21e7e-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="21e7e-125">I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="21e7e-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="21e7e-126">Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="21e7e-127">Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="21e7e-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="21e7e-128">Juster lastlinjeantallet</span><span class="sxs-lookup"><span data-stu-id="21e7e-128">Adjust the load line quantity</span></span>

<span data-ttu-id="21e7e-129">Bruk fremgangsmåten nedenfor til å justere lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="21e7e-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="21e7e-130">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="21e7e-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="21e7e-131">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="21e7e-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="21e7e-132">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="21e7e-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="21e7e-133">I fanen  **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="21e7e-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="21e7e-134">Velg **Reduser plukket antall** for å justere det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="21e7e-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="21e7e-135">Angi feltet **Reduser lastlinje** for å gjenspeile justeringer på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="21e7e-136">Tilbakefør alle plukkregistreringer, og gjør om plukking</span><span class="sxs-lookup"><span data-stu-id="21e7e-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="21e7e-137">Hvis noen brukte plukkregistrering til å lukke en lastlinje uten arbeid, kan det oppstå et avvik mellom lastlinjeantallet og det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="21e7e-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="21e7e-138">I dette tilfellet må manuell plukkregistrering tilbakeføres, og plukking må deretter fullføres ved hjelp av mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="21e7e-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="21e7e-139">Bruk fremgangsmåten nedenfor til å tilbakeføre plukkregistreringen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="21e7e-140">Gå til **Kunder \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="21e7e-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="21e7e-141">Velg salgsordren du ikke kan postere en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="21e7e-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="21e7e-142">I fanen **Salgsordrelinjer** velger du salgsordrelinjen som plukkregistreringen ble utført for.</span><span class="sxs-lookup"><span data-stu-id="21e7e-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="21e7e-143">Velg **Oppdater linje \> Plukk** for å fjerne merket for varene.</span><span class="sxs-lookup"><span data-stu-id="21e7e-143">Select **Update line \> Pick** to unpick the items.</span></span>
