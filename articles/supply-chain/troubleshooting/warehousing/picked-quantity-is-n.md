---
title: Plukket antall er ikke tilstrekkelig under følgeseddelgenerering
description: Når du genererer en følgeseddel, inneholder den utgående lasten et plukket antall som ikke samsvarer med det opprettede arbeidsantallet på lastlinjen.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249150"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="37796-103">Plukket antall er ikke tilstrekkelig under følgeseddelgenerering</span><span class="sxs-lookup"><span data-stu-id="37796-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="37796-104">Feilkode: SYS54073</span><span class="sxs-lookup"><span data-stu-id="37796-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="37796-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="37796-105">Symptoms</span></span>

<span data-ttu-id="37796-106">Når du genererer en følgeseddel, inneholder den utgående lasten et plukket antall som ikke samsvarer med det opprettede arbeidsantallet på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="37796-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="37796-107">Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="37796-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="37796-108">Siden %1 er plukket, er det ikke nok å oppdatere %2 når resten må være %3.</span><span class="sxs-lookup"><span data-stu-id="37796-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="37796-109">Derfor kan du ikke generere følgeseddelen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="37796-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="37796-110">Årsak</span><span class="sxs-lookup"><span data-stu-id="37796-110">Cause</span></span>

<span data-ttu-id="37796-111">Følgeseddelen kan ikke genereres i gjeldende tilstand, fordi det kan hende at én av følgende betingelser finnes:</span><span class="sxs-lookup"><span data-stu-id="37796-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="37796-112">Det relaterte arbeidet er ennå ikke plukket og flyttet til den endelige forsendelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="37796-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="37796-113">Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="37796-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="37796-114">Lastlinjeantall, antall for arbeid opprettet og plukket antall samsvarer ikke.</span><span class="sxs-lookup"><span data-stu-id="37796-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="37796-115">Løsning</span><span class="sxs-lookup"><span data-stu-id="37796-115">Resolution</span></span>

<span data-ttu-id="37796-116">Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes.</span><span class="sxs-lookup"><span data-stu-id="37796-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="37796-117">Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="37796-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="37796-118">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="37796-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="37796-119">Juster lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="37796-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="37796-120">Tilbakefør alle plukkregistreringer, og gjør om plukking.</span><span class="sxs-lookup"><span data-stu-id="37796-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="37796-121">Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer</span><span class="sxs-lookup"><span data-stu-id="37796-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="37796-122">Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="37796-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="37796-123">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="37796-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="37796-124">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="37796-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="37796-125">I hurtigfanen **Lastlinjer** velger du lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="37796-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="37796-126">Legg merke til verdien i feltet **Antall for arbeid opprettet**.</span><span class="sxs-lookup"><span data-stu-id="37796-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="37796-127">I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="37796-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="37796-128">Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="37796-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="37796-129">Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="37796-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="37796-130">Juster lastlinjeantallet</span><span class="sxs-lookup"><span data-stu-id="37796-130">Adjust the load line quantity</span></span>

<span data-ttu-id="37796-131">Bruk fremgangsmåten nedenfor til å justere lastlinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="37796-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="37796-132">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="37796-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="37796-133">Velg lasten som følgeseddelen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="37796-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="37796-134">I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="37796-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="37796-135">I fanen  **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="37796-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="37796-136">Velg **Reduser plukket antall** for å justere det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="37796-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="37796-137">Angi feltet **Reduser lastlinje** for å gjenspeile justeringer på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="37796-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="37796-138">Tilbakefør alle plukkregistreringer, og gjør om plukking</span><span class="sxs-lookup"><span data-stu-id="37796-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="37796-139">Problemet kan oppstå fordi noen brukte plukkregistrering til å lukke en lastlinje uten arbeid.</span><span class="sxs-lookup"><span data-stu-id="37796-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="37796-140">I dette tilfellet må manuell plukkregistrering tilbakeføres, og plukking må deretter fullføres ved hjelp av mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="37796-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="37796-141">Bruk fremgangsmåten nedenfor til å tilbakeføre plukkregistreringen.</span><span class="sxs-lookup"><span data-stu-id="37796-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="37796-142">Gå til **Kunder \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="37796-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="37796-143">Velg salgsordren du ikke kan postere en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="37796-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="37796-144">I fanen **Salgsordrelinjer** velger du salgsordrelinjen som plukkregistreringen ble utført for.</span><span class="sxs-lookup"><span data-stu-id="37796-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="37796-145">Velg **Oppdater linje \> Plukk** for å fjerne merket for varene.</span><span class="sxs-lookup"><span data-stu-id="37796-145">Select **Update line \> Pick** to unpick the items.</span></span>
