---
title: Antallet kan ikke reduseres når en salgsordre annulleres
description: Antallet kan ikke reduseres når en salgsordre annulleres.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230842"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="3b420-103">Antallet kan ikke reduseres når en salgsordre annulleres</span><span class="sxs-lookup"><span data-stu-id="3b420-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="3b420-104">Feilkode: SYS138831</span><span class="sxs-lookup"><span data-stu-id="3b420-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="3b420-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="3b420-105">Symptoms</span></span>

<span data-ttu-id="3b420-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="3b420-106">The system shows the following error message:</span></span>

> <span data-ttu-id="3b420-107">Antallet kan ikke reduseres.</span><span class="sxs-lookup"><span data-stu-id="3b420-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="3b420-108">Antall lagertransaksjoner i ordre er for lavt fordi en utleveringsordre eller produksjonsordre refererer til antallet eller delen av den, eller fordi antallet eller delen av den er merket mot andre transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="3b420-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="3b420-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="3b420-109">Cause</span></span>

<span data-ttu-id="3b420-110">Hvis arbeid er knyttet til en salgsordre, kan du ikke annullere salgsordren før arbeidet er annullert og tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="3b420-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="3b420-111">Dette kravet gjelder selv om arbeidet som er knyttet til salgsordren, er lukket.</span><span class="sxs-lookup"><span data-stu-id="3b420-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="3b420-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="3b420-112">Resolution</span></span>

<span data-ttu-id="3b420-113">Du kan løse dette problemet ved å fullføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="3b420-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="3b420-114">Avbryt åpent arbeid.</span><span class="sxs-lookup"><span data-stu-id="3b420-114">Cancel open work.</span></span>
1. <span data-ttu-id="3b420-115">Slett belastningen.</span><span class="sxs-lookup"><span data-stu-id="3b420-115">Delete the load.</span></span>
1. <span data-ttu-id="3b420-116">Reduser det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="3b420-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="3b420-117">Avbryte åpent arbeid</span><span class="sxs-lookup"><span data-stu-id="3b420-117">Cancel open work</span></span>

<span data-ttu-id="3b420-118">Følg denne fremgangsmåten for å avbryte åpent arbeid.</span><span class="sxs-lookup"><span data-stu-id="3b420-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="3b420-119">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="3b420-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="3b420-120">I **Arbeids-ID**-feltet angir du IDen for arbeidet du vil avbryte, og som for øyeblikket har **Arbeidstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="3b420-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="3b420-121">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b420-121">Select **OK**.</span></span>
1. <span data-ttu-id="3b420-122">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="3b420-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="3b420-123">Slette belastningen</span><span class="sxs-lookup"><span data-stu-id="3b420-123">Delete the load</span></span>

<span data-ttu-id="3b420-124">Følg denne fremgangsmåten for å slette en belastning.</span><span class="sxs-lookup"><span data-stu-id="3b420-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="3b420-125">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3b420-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3b420-126">Åpne den relevante salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3b420-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="3b420-127">Velg **Lager \> Arbeidsdetaljer** i hurtigfanen **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="3b420-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="3b420-128">Velg **Avbryt arbeid** i **Arbeid**-gruppen i **Arbeid**-fanen i handlingsruten på **Arbeid**-siden.</span><span class="sxs-lookup"><span data-stu-id="3b420-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="3b420-129">Bekreft at **Arbeidsstatus**-feltet er satt til *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="3b420-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="3b420-130">Lukk **Arbeid**-siden.</span><span class="sxs-lookup"><span data-stu-id="3b420-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="3b420-131">Velg **Lager \> Lastdetaljer** i hurtigfanen **Salgsordrelinjer** på siden for salgsordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="3b420-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="3b420-132">Velg deretter **Slett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3b420-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="3b420-133">Velg **Ja** for å bekrefte at du vil slette belastningen.</span><span class="sxs-lookup"><span data-stu-id="3b420-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="3b420-134">Lukk **Belastning**-siden.</span><span class="sxs-lookup"><span data-stu-id="3b420-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="3b420-135">Redusere det plukkede antallet</span><span class="sxs-lookup"><span data-stu-id="3b420-135">Reduce the picked quantity</span></span>

<span data-ttu-id="3b420-136">Etter at alt arbeid er avbrutt, følger du fremgangsmåten nedenfor for å redusere det plukkede antallet.</span><span class="sxs-lookup"><span data-stu-id="3b420-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="3b420-137">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3b420-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3b420-138">Åpne den relevante salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3b420-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="3b420-139">Velg **Oppdater linje \> Plukk** på verktøylinjen i hurtigfanen **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="3b420-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="3b420-140">Velg linjen der **Avgangsstatus**-feltet er satt til *Plukket* i **Transaksjoner**-delen på **Plukk**-siden.</span><span class="sxs-lookup"><span data-stu-id="3b420-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="3b420-141">Velg **Legg til plukklinje** på verktøylinjen i **Transaksjoner**-delen.</span><span class="sxs-lookup"><span data-stu-id="3b420-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="3b420-142">Velg **Bekreft plukking av alle** på verktøylinjen i **Plukklinjer**-delen.</span><span class="sxs-lookup"><span data-stu-id="3b420-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="3b420-143">Lukk **Plukk**-siden.</span><span class="sxs-lookup"><span data-stu-id="3b420-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="3b420-144">Velg **Avbryt** i **Vedlikehold**-gruppen i **Salgsordre**-fanen i handlingsruten på siden for salgsordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="3b420-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="3b420-145">Velg **Ja** for å bekrefte at du vil avbryte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3b420-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
