---
title: Synkronisere lagre fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 94fb6720152cbf6aec58d2b8d9d02fc5343c05e2
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251184"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="35282-103">Synkronisere lagre fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="35282-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="35282-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="35282-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="35282-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="35282-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="35282-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="35282-106">Templates and tasks</span></span>
<span data-ttu-id="35282-107">Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av lagre fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="35282-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="35282-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="35282-108">**Template in Data integration**</span></span>
- <span data-ttu-id="35282-109">Lagre (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="35282-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="35282-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="35282-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="35282-111">Lager</span><span class="sxs-lookup"><span data-stu-id="35282-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="35282-112">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="35282-112">Entity set</span></span>
| <span data-ttu-id="35282-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="35282-113">Field Service</span></span>    | <span data-ttu-id="35282-114">Forsyningskjedeadministrasjon</span><span class="sxs-lookup"><span data-stu-id="35282-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="35282-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="35282-115">msdyn_warehouses</span></span> | <span data-ttu-id="35282-116">Lagre</span><span class="sxs-lookup"><span data-stu-id="35282-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="35282-117">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="35282-117">Entity flow</span></span>
<span data-ttu-id="35282-118">Lagre som opprettes og vedlikeholdes i Supply Chain Management, kan synkroniseres til Field Service via et Common Data Service (CDS)-dataintegreringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="35282-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="35282-119">Lagrene du vil synkronisere til Field Service, kan styres med avansert spørring og filtrering på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="35282-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="35282-120">Lagre som synkroniseres fra Supply Chain Management, opprettes i Field Service med feltet **Vedlikeholdes eksternt** satt til **Ja**, og posten gjøres skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="35282-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="35282-121">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="35282-121">Field Service CRM solution</span></span>
<span data-ttu-id="35282-122">For å støtte integrasjon mellom Field Service og Finance and Operations, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen.</span><span class="sxs-lookup"><span data-stu-id="35282-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="35282-123">I løsningen er feltet **Vedlikeholdes eksternt** lagt til i **Lager (msdyn_warehouses)**-enheten.</span><span class="sxs-lookup"><span data-stu-id="35282-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="35282-124">Dette feltet brukes til å identifisere om lageret håndteres fra Supply Chain Management, eller om det bare finnes i Field Service.</span><span class="sxs-lookup"><span data-stu-id="35282-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="35282-125">Innstillingene for dette feltet inkluderer:</span><span class="sxs-lookup"><span data-stu-id="35282-125">The settings for this field include:</span></span>
- <span data-ttu-id="35282-126">**Ja** – Lageret kommer fra Supply Chain Management og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="35282-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="35282-127">**Nei** – Lageret ble registrert direkte i Field Service og vedlikeholdes her.</span><span class="sxs-lookup"><span data-stu-id="35282-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="35282-128">Feltet **Vedlikeholdes eksternt** gjør det mulig å kontrollere synkroniseringen av lagernivåer, justeringer, overføringer og bruk av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="35282-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="35282-129">Det er bare lagre med **Vedlikeholdes eksternt** satt til **Ja** som kan brukes til å synkronisere direkte til det samme lageret i det andre systemet.</span><span class="sxs-lookup"><span data-stu-id="35282-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="35282-130">Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt** = Nei) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="35282-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="35282-131">Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="35282-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="35282-132">I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="35282-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="35282-133">For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="35282-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="35282-134">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="35282-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="35282-135">Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="35282-135">Data Integration project</span></span>
<span data-ttu-id="35282-136">Før synkronisering av lagrene må du huske å oppdatere avansert spørring og filtrering for prosjektet, slik at det bare inneholder lagrene du vil hente fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="35282-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="35282-137">Vær oppmerksom på at du trenger lageret i Field Service for bruk i arbeidsordrer, justeringer og overføringer.</span><span class="sxs-lookup"><span data-stu-id="35282-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="35282-138">For å kontroller at **Integreringsnøkkel** finnes for **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="35282-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="35282-139">Gå til Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="35282-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="35282-140">Velg fanen **Tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="35282-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="35282-141">Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="35282-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="35282-142">Velg fanen **Integreringsnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="35282-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="35282-143">Finn msdyn_warehouses og bekreft at nøkkelen **msdyn_name (navn)** blir lagt til.</span><span class="sxs-lookup"><span data-stu-id="35282-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="35282-144">Hvis den ikke vises, kan du legge den til ved å klikke **Legg til nøkkel**, og deretter klikke **Lagre** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="35282-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="35282-145">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="35282-145">Template mapping in Data integration</span></span>

<span data-ttu-id="35282-146">Følgende illustrasjon viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="35282-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="35282-147">Lagre (Supply Chain Management til Field Service): Lagre</span><span class="sxs-lookup"><span data-stu-id="35282-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="35282-148">[![Maltilordning i Dataintegrering](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="35282-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
