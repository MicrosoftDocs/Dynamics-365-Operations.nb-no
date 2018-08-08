---
title: "Utgående prosess"
description: "Dette emnet gir en oversikt over utgående prosess i Lagerstyring."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5ac3260f128acbc819d7207f68f17adb085da11c
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="outbound-process"></a><span data-ttu-id="99170-103">Utgående prosess</span><span class="sxs-lookup"><span data-stu-id="99170-103">Outbound process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99170-104">Dette emnet gir en oversikt over utgående prosess i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="99170-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="99170-105">Utleveringsordrer</span><span class="sxs-lookup"><span data-stu-id="99170-105">Output orders</span></span>

<span data-ttu-id="99170-106">Utleveringsordrer brukes for å koble salgsordrelinjer og overføringsordrelinjer med utgående plukkingprosesser som bruker plukklister.</span><span class="sxs-lookup"><span data-stu-id="99170-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="99170-107">Når plukklister genereres fra enten salgsordrer eller overføringsordrer, opprettes utleveringsosrdrer og forsendelser automatisk.</span><span class="sxs-lookup"><span data-stu-id="99170-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="99170-108">En plukkliste har en en-til-en-relasjon med en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="99170-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="99170-109">Forsendelsen for overføringsordren eller pakkseddelen for salgsordren kan behandles fra forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="99170-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="99170-110">De følgende diagrammer viser en oversikt over prosesesen for utleveringsordrer.</span><span class="sxs-lookup"><span data-stu-id="99170-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="99170-111">[![Oversikt over utgående ordreprosess](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="99170-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="99170-112">Du kan sette opp utgående regler for å definere hvordan programmet skal håndtere den utgående prosessen.</span><span class="sxs-lookup"><span data-stu-id="99170-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="99170-113">Du kan bruke disse reglene for å kontrolere forsendelsesprosessene.</span><span class="sxs-lookup"><span data-stu-id="99170-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="99170-114">Spesielt kan du bruke reglene for å kontrollere hvilket stadium i prosessen en forsendelse kan sendes under.</span><span class="sxs-lookup"><span data-stu-id="99170-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="99170-115">Følgende innstillinger definerer hvordan utgående prosesser håndteres.</span><span class="sxs-lookup"><span data-stu-id="99170-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="99170-116">Plukkrutestatus for salgs- og overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="99170-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="99170-117">Gå til **Kundefordringer** \> **Oppsett** \> **Parametere for kundefordringer** og deretter i kategorien **Oppdateringer** velger du en verdi i feltet **Plukkrutestatus** .</span><span class="sxs-lookup"><span data-stu-id="99170-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="99170-118">[![Felt for plukkrutestatus for salgsordrer](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="99170-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="99170-119">Hvis feltet **Plukkrutestatus** er satt til **Fullført** vil plukkprosessenen skje automatisk som en del av prosessen for å generere plukklister.</span><span class="sxs-lookup"><span data-stu-id="99170-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="99170-120">Hvis feltet er satt til **Aktivert** må plukklistelinjer oppdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="99170-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="99170-121">Det samme oppsett gjelder for overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="99170-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="99170-122">Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i kategorien **Transport** velger du en verdi i feltet **Plukkrutestatus**.</span><span class="sxs-lookup"><span data-stu-id="99170-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="99170-123">[![Felt for plukkrutestatus for overføringsordrer](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="99170-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="99170-124">Avsluttende lagerordre</span><span class="sxs-lookup"><span data-stu-id="99170-124">End output inventory orders</span></span>

<span data-ttu-id="99170-125">Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i kategorien **Generelt** velger du et alternativ i feltet **Lagerordre**.</span><span class="sxs-lookup"><span data-stu-id="99170-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="99170-126">[![Valg for å avslutte utgående lagerordre](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="99170-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="99170-127">Hvis lagerarbeideren reduserer antallet på plukklisten, fjernes de tilsvarende lagerantallene fra forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="99170-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="99170-128">Når plukklisten oppdateres på et tidspunkt, blir de gjenstående antallene rapportert tilbake til ordren hvis alternativet **Avslutt utleveringslagerordre** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="99170-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="99170-129">Hvis alternativet **Avslutt utleveringslagerordre** er satt til **Nei**, beholdes de gjenstående antallene som en åpen utgående ordremengde og må legges til en ny plukkliste som en del av funksjonen **Åpne utleveringsordrer**.</span><span class="sxs-lookup"><span data-stu-id="99170-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="99170-130">[![Åpne utgangsordrerkommandoen i Funksjonsmenyen](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="99170-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="99170-131">[![Funksjonsmenyen på siden Åpne utgående ordre](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="99170-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="99170-132">Reduser antall</span><span class="sxs-lookup"><span data-stu-id="99170-132">Reduce quantity</span></span>

<span data-ttu-id="99170-133">Den tredje parameteren du kan bruke som en del av prosessen med å generere plukklister, er **Reduser antallsparameteren**</span><span class="sxs-lookup"><span data-stu-id="99170-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="99170-134">Innstillingen av dette parameterer arbeider sammen med **Reservasjon**-innstillingen som utløser en reservasjonsprosess som en del av frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="99170-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="99170-135">[![Reduser antallsparameteren](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="99170-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="99170-136">Eksempel på en utgående prosess for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="99170-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="99170-137">For dette eksempelet er det en salgsordre for to elementer.</span><span class="sxs-lookup"><span data-stu-id="99170-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="99170-138">Under plukklistegenerering kan du velge **Redusere antall**-paremeteret.</span><span class="sxs-lookup"><span data-stu-id="99170-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="99170-139">Derfor frigir du og oppretter plukklinjer kun for tilgjengelig lager på stedet.</span><span class="sxs-lookup"><span data-stu-id="99170-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="99170-140">Plukkingen må rapporteres via en registreringsprosess for plukklister (**Plukkrutestatus** = **Aktivert**).</span><span class="sxs-lookup"><span data-stu-id="99170-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="99170-141">Lagerbeholdningen som ikke allerede er reservert, er reservert under plukklistegenerering.</span><span class="sxs-lookup"><span data-stu-id="99170-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="99170-142">Den utilgjengelige beholdningen kan enten fjernes fra salgsordren eller frigis til lageret for utgående prosess senere, når lager er tilgjengelig for plukking.</span><span class="sxs-lookup"><span data-stu-id="99170-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="99170-143">[![Oppdater plukklisten](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="99170-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="99170-144">Så snart alle plukklinjer er plukket på siden **Plukklisteregistrering**, er den tilknyttede forsendelsen komplett.</span><span class="sxs-lookup"><span data-stu-id="99170-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="99170-145">Prosessen for pakksedler for salgsordrer kan deretter initialiseres basert det på plukkede inventar.</span><span class="sxs-lookup"><span data-stu-id="99170-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="99170-146">[![Oppdater ugående forsendelser](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="99170-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

