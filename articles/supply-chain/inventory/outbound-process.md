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
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: nb-no
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="44b15-103">Utgående prosess</span><span class="sxs-lookup"><span data-stu-id="44b15-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="44b15-104">Dette emnet gir en oversikt over utgående prosess i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="44b15-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="44b15-105">Utleveringsordrer</span><span class="sxs-lookup"><span data-stu-id="44b15-105">Output orders</span></span>

<span data-ttu-id="44b15-106">Utleveringsordrer brukes for å koble salgsordrelinjer og overføringsordrelinjer med utgående plukkingprosesser som bruker plukklister.</span><span class="sxs-lookup"><span data-stu-id="44b15-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="44b15-107">Når plukklister genereres fra enten salgsordrer eller overføringsordrer, opprettes utleveringsosrdrer og forsendelser automatisk.</span><span class="sxs-lookup"><span data-stu-id="44b15-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="44b15-108">En plukkliste har en en-til-en-relasjon med en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="44b15-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="44b15-109">Forsendelsen for overføringsordren eller pakkseddelen for salgsordren kan behandles fra forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="44b15-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="44b15-110">De følgende diagrammer viser en oversikt over prosesesen for utleveringsordrer.</span><span class="sxs-lookup"><span data-stu-id="44b15-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="44b15-111">[![Oversikt over utgående ordreprosess](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="44b15-112">Du kan sette opp utgående regler for å definere hvordan programmet skal håndtere den utgående prosessen.</span><span class="sxs-lookup"><span data-stu-id="44b15-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="44b15-113">Du kan bruke disse reglene for å kontrolere forsendelsesprosessene.</span><span class="sxs-lookup"><span data-stu-id="44b15-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="44b15-114">Spesielt kan du bruke reglene for å kontrollere hvilket stadium i prosessen en forsendelse kan sendes under.</span><span class="sxs-lookup"><span data-stu-id="44b15-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="44b15-115">Følgende innstillinger definerer hvordan utgående prosesser håndteres.</span><span class="sxs-lookup"><span data-stu-id="44b15-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="44b15-116">Plukkrutestatus for salgs- og overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="44b15-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="44b15-117">Gå til **Kundefordringer** \> **Oppsett** \> **Parametere for kundefordringer** og deretter i kategorien **Oppdateringer** velger du en verdi i feltet **Plukkrutestatus** .</span><span class="sxs-lookup"><span data-stu-id="44b15-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="44b15-118">[![Felt for plukkrutestatus for salgsordrer](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="44b15-119">Hvis feltet **Plukkrutestatus** er satt til **Fullført** vil plukkprosessenen skje automatisk som en del av prosessen for å generere plukklister.</span><span class="sxs-lookup"><span data-stu-id="44b15-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="44b15-120">Hvis feltet er satt til **Aktivert** må plukklistelinjer oppdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="44b15-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="44b15-121">Det samme oppsett gjelder for overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="44b15-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="44b15-122">Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i kategorien **Transport** velger du en verdi i feltet **Plukkrutestatus**.</span><span class="sxs-lookup"><span data-stu-id="44b15-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="44b15-123">[![Felt for plukkrutestatus for overføringsordrer](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="44b15-124">Avsluttende lagerordre</span><span class="sxs-lookup"><span data-stu-id="44b15-124">End output inventory orders</span></span>

<span data-ttu-id="44b15-125">Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i kategorien **Generelt** velger du et alternativ i feltet **Lagerordre**.</span><span class="sxs-lookup"><span data-stu-id="44b15-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="44b15-126">[![Valg for å avslutte utgående lagerordre](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="44b15-127">Noen ganger kan enkelte elementer i lager ikke plukkes som en del av plukklisteprosessen.</span><span class="sxs-lookup"><span data-stu-id="44b15-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="44b15-128">For eksempel kan denne situasjonen oppstå hvis en lagerarbeider reduserer mengdene på plukklinjer og behandler plukklisten.</span><span class="sxs-lookup"><span data-stu-id="44b15-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="44b15-129">Hvis valget **Avslutt utgående lagerordre** er satt til **Ja**, vil gjenværende uplukkede antall rapporteres tilbake til ordrenivå.</span><span class="sxs-lookup"><span data-stu-id="44b15-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="44b15-130">Hvis dette alternativet er satt til **Nei**, vil gjenværende uplukkede antall beholdes som en åpen utgående ordremengde.</span><span class="sxs-lookup"><span data-stu-id="44b15-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="44b15-131">I dette tilfellet forblir mengdene frigitt til lageret og må legges til en ny plukkliste som en del av funksjonaliteten **Åpne utgangsordrer**.</span><span class="sxs-lookup"><span data-stu-id="44b15-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="44b15-132">[![Åpne utgangsordrerkommandoen i Funksjonsmenyen](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="44b15-133">[![Funksjonsmenyen på siden Åpne utgående ordre](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="44b15-134">Reduser antall</span><span class="sxs-lookup"><span data-stu-id="44b15-134">Reduce quantity</span></span>

<span data-ttu-id="44b15-135">Den tredje parameteren du kan bruke som en del av prosessen med å generere plukklister, er **Reduser antallsparameteren**</span><span class="sxs-lookup"><span data-stu-id="44b15-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="44b15-136">Innstillingen av dette parameterer arbeider sammen med **Reservasjon**-innstillingen som utløser en reservasjonsprosess som en del av frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="44b15-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="44b15-137">[![Reduser antallsparameteren](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="44b15-138">Eksempel på en utgående prosess for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="44b15-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="44b15-139">For dette eksempelet er det en salgsordre for to elementer.</span><span class="sxs-lookup"><span data-stu-id="44b15-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="44b15-140">Under plukklistegenerering kan du velge **Redusere antall**-paremeteret.</span><span class="sxs-lookup"><span data-stu-id="44b15-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="44b15-141">Derfor frigir du og oppretter plukklinjer kun for tilgjengelig lager på stedet.</span><span class="sxs-lookup"><span data-stu-id="44b15-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="44b15-142">Plukkingen må rapporteres via en registreringsprosess for plukklister (**Plukkrutestatus** = **Aktivert**).</span><span class="sxs-lookup"><span data-stu-id="44b15-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="44b15-143">Lagerbeholdningen som ikke allerede er reservert, er reservert under plukklistegenerering.</span><span class="sxs-lookup"><span data-stu-id="44b15-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="44b15-144">Den utilgjengelige beholdningen kan enten fjernes fra salgsordren eller frigis til lageret for utgående prosess senere, når lager er tilgjengelig for plukking.</span><span class="sxs-lookup"><span data-stu-id="44b15-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="44b15-145">[![Oppdater plukklisten](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="44b15-146">Så snart alle plukklinjer er plukket på siden **Plukklisteregistrering**, er den tilknyttede forsendelsen komplett.</span><span class="sxs-lookup"><span data-stu-id="44b15-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="44b15-147">Prosessen for pakksedler for salgsordrer kan deretter initialiseres basert det på plukkede inventar.</span><span class="sxs-lookup"><span data-stu-id="44b15-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="44b15-148">[![Oppdater ugående forsendelser](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="44b15-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

