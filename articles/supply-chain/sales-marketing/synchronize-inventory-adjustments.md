---
title: Synkronisere lageroverføringer og -justeringer fra Field Service til Supply Chain Management
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagerjusteringer og -overføringer fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 9f3bfe950446a6e87e34c32d2593cba0af84d8e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838987"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="dae28-103">Synkronisere lageroverføringer og -justeringer fra Field Service til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dae28-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dae28-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagerjusteringer og -overføringer fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="dae28-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="dae28-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="dae28-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="dae28-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="dae28-106">Templates and tasks</span></span>
<span data-ttu-id="dae28-107">Følgende mal og underliggende oppgaver brukes til å synkronisere lagerjusteringer og -overføringer fra Field Service til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dae28-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="dae28-108">**Maler i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="dae28-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="dae28-109">Lagerjustering (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="dae28-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="dae28-110">Lageroverføringer (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="dae28-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="dae28-111">**Oppgaver i Dataintegrasjonprosjektene**:</span><span class="sxs-lookup"><span data-stu-id="dae28-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="dae28-112">Lagerjusteringer</span><span class="sxs-lookup"><span data-stu-id="dae28-112">Inventory Adjustments</span></span>
- <span data-ttu-id="dae28-113">Lageroverføringer</span><span class="sxs-lookup"><span data-stu-id="dae28-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="dae28-114">Tabellsett</span><span class="sxs-lookup"><span data-stu-id="dae28-114">Table set</span></span>
| <span data-ttu-id="dae28-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="dae28-115">Field Service</span></span>                     | <span data-ttu-id="dae28-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dae28-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="dae28-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="dae28-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="dae28-118">Overskrifter og linjer i Dataverse-lagerjusteringsjournal</span><span class="sxs-lookup"><span data-stu-id="dae28-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="dae28-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="dae28-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="dae28-120">Overskrifter og linjer i Dataverse-lageroverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="dae28-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="dae28-121">Tabellflyt</span><span class="sxs-lookup"><span data-stu-id="dae28-121">Table flow</span></span>
<span data-ttu-id="dae28-122">Lagerjusteringer og -overføringer som er gjort i Field Service, synkroniseres til Supply Chain Management etter at **Posteringsstatus** endres fra **Opprettet** til **Postert**.</span><span class="sxs-lookup"><span data-stu-id="dae28-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="dae28-123">Når dette skjer, låses justeringen eller overføringsordren, og den blir skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="dae28-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="dae28-124">Dette betyr at justeringer og overføringer kan posteres i Supply Chain Management, men de kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="dae28-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="dae28-125">Du kan definere en satsvis jobb i Supply Chain Management for å postere justeringene og overføringene av lagerjournaler som er generert under integreringen.</span><span class="sxs-lookup"><span data-stu-id="dae28-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="dae28-126">Se forutsetningene under for mer informasjon om hvordan du aktiverer den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="dae28-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="dae28-127">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="dae28-127">Field Service CRM solution</span></span> 
<span data-ttu-id="dae28-128">Kolonnen **Lagerenhet** er lagt til i **Produkt**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="dae28-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="dae28-129">Denne kolonnen er nødvendig siden salgs- og lagerenheten ikke alltid er den samme i Supply Chain Management, og lagerenheten kreves for lagerbeholdningen i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dae28-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="dae28-130">Når du angir produktet for et lagerjusteringsprodukt for både lagerjusteringer og lageroverføringer, hentes enheten fra lagerproduktverdien.</span><span class="sxs-lookup"><span data-stu-id="dae28-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="dae28-131">Hvis en verdi blir funnet, låses **Enhet**-kolonnen på lagerjusteringsproduktet.</span><span class="sxs-lookup"><span data-stu-id="dae28-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="dae28-132">**Posteringsstatus**-kolonnen er lagt til i tabellene **Lagerjustering** og **Lageroverføring**.</span><span class="sxs-lookup"><span data-stu-id="dae28-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="dae28-133">Denne kolonnen brukes som filter når en justering eller overføring sendes til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dae28-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="dae28-134">Standarden for denne kolonnen er Opprettet (1), men den sendes ikke til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dae28-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="dae28-135">Når du oppdaterer verdien til Postert (2), sendes den til Supply Chain Management, men etter det vil du ikke lenger kunne endre justeringen eller overføringen eller legge til nye linjer.</span><span class="sxs-lookup"><span data-stu-id="dae28-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="dae28-136">Kolonnen **Nummerserie** er lagt til tabellen **Lagerjusteringsprodukt**.</span><span class="sxs-lookup"><span data-stu-id="dae28-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="dae28-137">Denne kolonnen sikrer at integreringen har et unikt nummer, slik at integreringen kan opprette og oppdatere justeringen.</span><span class="sxs-lookup"><span data-stu-id="dae28-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="dae28-138">Når du oppretter det første lagerjusteringsproduktet, opprettes det en ny post i tabellen **P2C Autonummer** for å vedlikeholde nummerserien og prefikset som brukes.</span><span class="sxs-lookup"><span data-stu-id="dae28-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="dae28-139">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="dae28-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="dae28-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dae28-140">Supply Chain Management</span></span>
<span data-ttu-id="dae28-141">Integreringslagerjournalene som genereres i integreringen, kan posteres automatisk med en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="dae28-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="dae28-142">Dette aktiveres fra **Lagerstyring > Periodiske oppgaver > Dataverse-integrering > Poster lagerjournaler for integrering**.</span><span class="sxs-lookup"><span data-stu-id="dae28-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dae28-143">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="dae28-143">Template mapping in Data integration</span></span>

<span data-ttu-id="dae28-144">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="dae28-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="dae28-145">Lagerjustering (Field Service til Supply Chain Management): Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="dae28-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="dae28-146">[![Maltilordning i Dataintegrering](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="dae28-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="dae28-147">Lageroverføring (Field Service til Supply Chain Management): Lageroverføring</span><span class="sxs-lookup"><span data-stu-id="dae28-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="dae28-148">[![Maltilordning i Dataintegrering](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="dae28-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]