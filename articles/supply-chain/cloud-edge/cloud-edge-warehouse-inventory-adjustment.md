---
title: Lagerbeholdningsjustering
description: Dette emnet gir informasjon om lagerjusteringsjournalen og -behandlingen når du bruker skaleringsenheter.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026139"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="62722-103">Lagerbeholdningsjustering</span><span class="sxs-lookup"><span data-stu-id="62722-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="62722-104">Funksjonen for lagerjusteringsjournal brukes når du kjører skaleringsenheter for sky og kant for [produksjonsarbeidsbelastninger](cloud-edge-workload-manufacturing.md) og [lagerstyringsarbeidsbelastninger](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="62722-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="62722-105">Når en arbeider utfører lagerjustering ved hjelp av lagerappen mot en arbeidsmengde for lagerstyring for skaleringsenhet, må den fysiske lageroppdateringen behandles av den satsvise jobben **Lagerjusteringsjournal**, som du kjører og planlegger ved å gå til **Lagerstyring > Periodiske oppgaver > Lagerjusteringsjournal**.</span><span class="sxs-lookup"><span data-stu-id="62722-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="62722-106">Følgende arbeidsprosesser for lagerapp bruker for øyeblikket **Lagerjusteringsjournal** på arbeidsbelastninger for skalaenhet:</span><span class="sxs-lookup"><span data-stu-id="62722-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="62722-107">Justering inn/ut</span><span class="sxs-lookup"><span data-stu-id="62722-107">Adjustment in/out</span></span>
- <span data-ttu-id="62722-108">Syklustelling</span><span class="sxs-lookup"><span data-stu-id="62722-108">Cycle counting</span></span>
- <span data-ttu-id="62722-109">Nummerskiltlasting</span><span class="sxs-lookup"><span data-stu-id="62722-109">License plate loading</span></span>

<span data-ttu-id="62722-110">Flere lagertransaksjoner opprettes som en del av hver lagerjusteringsprosess, fordi senterets og skalaenhetens distribusjoner deler lagerposter.</span><span class="sxs-lookup"><span data-stu-id="62722-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="62722-111">Eksempel på lagerjustering</span><span class="sxs-lookup"><span data-stu-id="62722-111">Inventory adjustment example</span></span>

<span data-ttu-id="62722-112">I dette eksemplet har en lagerarbeider brukt lagerappen til å registrere tilføyingen av lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="62722-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="62722-113">For det første oppretter arbeidsbelastningen for skalaenhet en lagerjusteringstransaksjon for den positive fysiske justeringen, som deretter synkroniseres til senteret og resulterer i en økning av lagerbeholdningen i senteret.</span><span class="sxs-lookup"><span data-stu-id="62722-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="62722-114">Type</span><span class="sxs-lookup"><span data-stu-id="62722-114">Type</span></span>                                    | <span data-ttu-id="62722-115">Storskalaenhet</span><span class="sxs-lookup"><span data-stu-id="62722-115">Scale unit</span></span> | <span data-ttu-id="62722-116">Retning</span><span class="sxs-lookup"><span data-stu-id="62722-116">Direction</span></span> | <span data-ttu-id="62722-117">Hub</span><span class="sxs-lookup"><span data-stu-id="62722-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="62722-118">Lagerbeholdningsjustering</span><span class="sxs-lookup"><span data-stu-id="62722-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="62722-119">+1</span><span class="sxs-lookup"><span data-stu-id="62722-119">+1</span></span>         | ->        | <span data-ttu-id="62722-120">+1</span><span class="sxs-lookup"><span data-stu-id="62722-120">+1</span></span>  |

<span data-ttu-id="62722-121">Senteret behandler deretter en opptellingsjournalpostering, som mottas via [meldinger for meldingsprosessor](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="62722-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="62722-122">Dette oppdaterer den ekstra lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="62722-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="62722-123">For å hindre dobbel lagerbeholdning oppretter senteret en mottransaksjon som en del av denne prosessen, og fjerner den tidligere registrerte lagerbeholdningen som er relatert til lagerjusteringen.</span><span class="sxs-lookup"><span data-stu-id="62722-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="62722-124">Type</span><span class="sxs-lookup"><span data-stu-id="62722-124">Type</span></span>                                    | <span data-ttu-id="62722-125">Storskalaenhet</span><span class="sxs-lookup"><span data-stu-id="62722-125">Scale unit</span></span> | <span data-ttu-id="62722-126">Retning</span><span class="sxs-lookup"><span data-stu-id="62722-126">Direction</span></span> | <span data-ttu-id="62722-127">Hub</span><span class="sxs-lookup"><span data-stu-id="62722-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="62722-128">Opptelling</span><span class="sxs-lookup"><span data-stu-id="62722-128">Counting</span></span>                                | <span data-ttu-id="62722-129">+1</span><span class="sxs-lookup"><span data-stu-id="62722-129">+1</span></span>         | <-        | <span data-ttu-id="62722-130">+1</span><span class="sxs-lookup"><span data-stu-id="62722-130">+1</span></span>  |
| <span data-ttu-id="62722-131">Lagerjustering (motregning)</span><span class="sxs-lookup"><span data-stu-id="62722-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="62722-132">-1</span><span class="sxs-lookup"><span data-stu-id="62722-132">-1</span></span>         | <-        | <span data-ttu-id="62722-133">-1</span><span class="sxs-lookup"><span data-stu-id="62722-133">-1</span></span>  |

<span data-ttu-id="62722-134">Når en skalaenhet har opprettet en **Lagerjusteringsjournal** i senteret, kan du gå gjennom både **Opptellingsjournal** og **Motposteringsjournalen**, som opprettes av senteret som en del av justeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="62722-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="62722-135">Du kan gå gjennom hver av disse journaloppføringene og transaksjonene i Supply Chain Management ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="62722-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="62722-136">Logg deg på skaleringsenheten.</span><span class="sxs-lookup"><span data-stu-id="62722-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="62722-137">Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerjusteringsjournal**.</span><span class="sxs-lookup"><span data-stu-id="62722-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="62722-138">På siden **Lagerjusteringsjournal** finner og åpner du journalen som registrerte endringene i lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="62722-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="62722-139">**Journallinjer**-delen viser hver justering som registreres av denne journalen.</span><span class="sxs-lookup"><span data-stu-id="62722-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="62722-140">Logg deg på senteret.</span><span class="sxs-lookup"><span data-stu-id="62722-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="62722-141">Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerjusteringsjournal**.</span><span class="sxs-lookup"><span data-stu-id="62722-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="62722-142">På siden **Lagerjusteringsjournal** skal du se den samme journalen oppført hvis senteret og skalaenheten er synkronisert.</span><span class="sxs-lookup"><span data-stu-id="62722-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="62722-143">Åpne journalen.</span><span class="sxs-lookup"><span data-stu-id="62722-143">Open the journal.</span></span> <span data-ttu-id="62722-144">Hvis [meldinger for meldingsprosessor](cloud-edge-message-processor-messages.md) er behandlet, vil du se koblinger til **Opptellingsjournal** og **Motposteringsjournal** i hodet.</span><span class="sxs-lookup"><span data-stu-id="62722-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="62722-145">**Opptellingsjournalen** bør vise de samme dimensjonsverdiene som journallinjene.</span><span class="sxs-lookup"><span data-stu-id="62722-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="62722-146">**Motposteringsjournal** skal vise motregningen, som fjerner den doble lagerjusteringen.</span><span class="sxs-lookup"><span data-stu-id="62722-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="62722-147">Når all synkronisering og behandling er fullført, synkroniseres **Opptellingsjournal** og **Motposteringsjournal** tilbake til skalaenheten.</span><span class="sxs-lookup"><span data-stu-id="62722-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="62722-148">Disse kan også vises fra den relevante **Lagerjusteringsjournal**-siden.</span><span class="sxs-lookup"><span data-stu-id="62722-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
