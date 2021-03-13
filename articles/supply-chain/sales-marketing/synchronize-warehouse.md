---
title: Synkronisere lagre fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0c0c1bafb5b36bb9ddc00061e0040a199c8c033d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010853"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="21dba-103">Synkronisere lagre fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="21dba-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="21dba-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="21dba-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="21dba-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="21dba-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="21dba-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="21dba-106">Templates and tasks</span></span>
<span data-ttu-id="21dba-107">Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av lagre fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="21dba-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="21dba-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="21dba-108">**Template in Data integration**</span></span>
- <span data-ttu-id="21dba-109">Lagre (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="21dba-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="21dba-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="21dba-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="21dba-111">Lager</span><span class="sxs-lookup"><span data-stu-id="21dba-111">Warehouse</span></span>

## <a name="table-set"></a><span data-ttu-id="21dba-112">Tabellsett</span><span class="sxs-lookup"><span data-stu-id="21dba-112">Table set</span></span>
| <span data-ttu-id="21dba-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="21dba-113">Field Service</span></span>    | <span data-ttu-id="21dba-114">Forsyningskjedeadministrasjon</span><span class="sxs-lookup"><span data-stu-id="21dba-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="21dba-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="21dba-115">msdyn_warehouses</span></span> | <span data-ttu-id="21dba-116">Lagre</span><span class="sxs-lookup"><span data-stu-id="21dba-116">Warehouses</span></span>                             |

## <a name="table-flow"></a><span data-ttu-id="21dba-117">Tabellflyt</span><span class="sxs-lookup"><span data-stu-id="21dba-117">Table flow</span></span>
<span data-ttu-id="21dba-118">Lagre som opprettes og vedlikeholdes i Supply Chain Management, kan synkroniseres til Field Service via et Microsoft Dataverse-dataintegreringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="21dba-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="21dba-119">Lagrene du vil synkronisere til Field Service, kan styres med avansert spørring og filtrering på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="21dba-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="21dba-120">Lagre som synkroniseres fra Supply Chain Management, opprettes i Field Service med kolonnen **Vedlikeholdes eksternt** satt til **Ja**, og posten gjøres skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="21dba-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** column set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="21dba-121">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="21dba-121">Field Service CRM solution</span></span>
<span data-ttu-id="21dba-122">For å støtte integrasjon mellom Field Service og Supply Chain Management, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen.</span><span class="sxs-lookup"><span data-stu-id="21dba-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="21dba-123">I løsningen er kolonnen **Vedlikeholdes eksternt** lagt til i tabellen **Lager (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="21dba-123">In the solution, the **Is Maintained Externally** column has been added to the **Warehouse (msdyn_warehouses)** table.</span></span> <span data-ttu-id="21dba-124">Denne kolonnen brukes til å identifisere om lageret håndteres fra Supply Chain Management, eller om det bare finnes i Field Service.</span><span class="sxs-lookup"><span data-stu-id="21dba-124">This column helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="21dba-125">Innstillingene for denne kolonnen inkluderer følgende:</span><span class="sxs-lookup"><span data-stu-id="21dba-125">The settings for this column include:</span></span>
- <span data-ttu-id="21dba-126">**Ja** – Lageret kommer fra Supply Chain Management og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="21dba-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="21dba-127">**Nei** – Lageret ble registrert direkte i Field Service og vedlikeholdes her.</span><span class="sxs-lookup"><span data-stu-id="21dba-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="21dba-128">Kolonnen **Vedlikeholdes eksternt** gjør det mulig å kontrollere synkroniseringen av lagernivåer, justeringer, overføringer og bruk av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="21dba-128">The **Is Externally Maintained** column helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="21dba-129">Det er bare lagre med **Vedlikeholdes eksternt** satt til **Ja** som kan brukes til å synkronisere direkte til det samme lageret i det andre systemet.</span><span class="sxs-lookup"><span data-stu-id="21dba-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="21dba-130">Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt** = Nei) og så tilordne dem til et enkelt lager med funksjonen for avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="21dba-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="21dba-131">Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="21dba-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="21dba-132">I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="21dba-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="21dba-133">For mer informasjon, se [Synkronisere lagerjusteringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="21dba-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="21dba-134">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="21dba-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="21dba-135">Dataintegrasjonsprosjekt</span><span class="sxs-lookup"><span data-stu-id="21dba-135">Data Integration project</span></span>
<span data-ttu-id="21dba-136">Før synkronisering av lagrene må du huske å oppdatere avansert spørring og filtrering for prosjektet, slik at det bare inneholder lagrene du vil hente fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="21dba-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="21dba-137">Vær oppmerksom på at du trenger lageret i Field Service for bruk i arbeidsordrer, justeringer og overføringer.</span><span class="sxs-lookup"><span data-stu-id="21dba-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="21dba-138">For å kontroller at **Integreringsnøkkel** finnes for **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="21dba-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="21dba-139">Gå til Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="21dba-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="21dba-140">Velg fanen **Tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="21dba-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="21dba-141">Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="21dba-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="21dba-142">Velg fanen **Integreringsnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="21dba-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="21dba-143">Finn msdyn_warehouses og bekreft at nøkkelen **msdyn_name (navn)** blir lagt til.</span><span class="sxs-lookup"><span data-stu-id="21dba-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="21dba-144">Hvis den ikke vises, kan du legge den til ved å klikke **Legg til nøkkel**, og deretter klikke **Lagre** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="21dba-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="21dba-145">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="21dba-145">Template mapping in Data integration</span></span>

<span data-ttu-id="21dba-146">Følgende illustrasjon viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="21dba-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="21dba-147">Lagre (Supply Chain Management til Field Service): Lagre</span><span class="sxs-lookup"><span data-stu-id="21dba-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="21dba-148">[![Maltilordning i Dataintegrering](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="21dba-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
