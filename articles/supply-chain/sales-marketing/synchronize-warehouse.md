---
title: Synkronisere lagre fra Finance and Operations til Field Service
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="f0fb5-103">Synkronisere lagre fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="f0fb5-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0fb5-104">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f0fb5-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="f0fb5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f0fb5-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="f0fb5-106">Templates and tasks</span></span>
<span data-ttu-id="f0fb5-107">Følgende mal og underliggende oppgaver brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f0fb5-108">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="f0fb5-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="f0fb5-109">Lagre (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="f0fb5-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="f0fb5-110">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="f0fb5-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="f0fb5-111">Lager</span><span class="sxs-lookup"><span data-stu-id="f0fb5-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="f0fb5-112">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="f0fb5-112">Entity set</span></span>
| <span data-ttu-id="f0fb5-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="f0fb5-113">Field Service</span></span>    | <span data-ttu-id="f0fb5-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0fb5-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="f0fb5-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="f0fb5-115">msdyn_warehouses</span></span> | <span data-ttu-id="f0fb5-116">Lagre</span><span class="sxs-lookup"><span data-stu-id="f0fb5-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="f0fb5-117">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="f0fb5-117">Entity flow</span></span>
<span data-ttu-id="f0fb5-118">Lagre som opprettes og vedlikeholdes i Finance and Operations, kan synkroniseres til Field Service via et Common Data Service (CDS)-dataintegreringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="f0fb5-119">De ønskede lagrene som synkroniseres til Field Service, kan styres med avansert spørring og filtrering på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="f0fb5-120">Lagre som synkroniseres fra Finance and Operations, opprettes i Field Service med feltet Vedlikeholdes eksternt satt til Ja og posten gjøres skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="f0fb5-121">Field Service CRM-løsningen For å støtte integrasjon mellom Field Service og Finance and Operations, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="f0fb5-122">Løsningen inneholder følgende endringer.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-122">The solution includes the following changes.</span></span>
<span data-ttu-id="f0fb5-123">Feltet **Vedlikeholdes eksternt** er lagt til i **Lager (msdyn_warehouses)**-enheten.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="f0fb5-124">Dette feltet brukes til å identifisere om lageret håndteres fra Operations, eller om det bare finnes i Field Service.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="f0fb5-125">Ja – Lageret kommer fra Finance and Operations, og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="f0fb5-126">Nei – Lageret ble registrert direkte i Field Service og vedlikeholdes her.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="f0fb5-127">Feltet **Vedlikeholdes eksternt** gjør det mulig å kontrollere synkroniseringen av lagernivåer, justeringer, overføringer og bruk av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="f0fb5-128">Det er bare lagre med **Vedlikeholdes eksternt** = Ja som kan brukes til å synkronisere direkte til det samme lageret i det andre systemet.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="f0fb5-129">Obs!  Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt** = Nei) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="f0fb5-130">Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="f0fb5-131">I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="f0fb5-132">Se tilleggsinformasjon i Synkronisere lagerjusteringer fra Field Service til Finance and Operations og Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f0fb5-133">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="f0fb5-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="f0fb5-134">I dataintegrasjonsprosjektet</span><span class="sxs-lookup"><span data-stu-id="f0fb5-134">In the Data Integration project</span></span>
<span data-ttu-id="f0fb5-135">Før synkronisering av lagrene må du huske å oppdatere avansert spørring og filtrering for prosjektet slik at det bare inneholder lagrene du vil hente fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="f0fb5-136">Vær oppmerksom på at du trenger lageret i Field Service for bruk i arbeidsordrer, justeringer og overføringer.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="f0fb5-137">Kontroller at **Integration-nøkkelen** finnes for **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="f0fb5-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="f0fb5-138">Gå til Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="f0fb5-138">Go to Data Integration</span></span>
2. <span data-ttu-id="f0fb5-139">Velg fanen **Tilkoblingssett**</span><span class="sxs-lookup"><span data-stu-id="f0fb5-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="f0fb5-140">Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="f0fb5-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="f0fb5-141">Velg fanen **Integreringsnøkkel**</span><span class="sxs-lookup"><span data-stu-id="f0fb5-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="f0fb5-142">Finn msdyn_warehouses og kontroller at nøkkelen **msdyn_name (navn)** blir lagt til.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="f0fb5-143">Hvis den ikke vises, kan du legge den ved å klikke **Legg til nøkkel**, og klikke **Lagre** øverst på siden</span><span class="sxs-lookup"><span data-stu-id="f0fb5-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f0fb5-144">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="f0fb5-144">Template mapping in Data integration</span></span>

<span data-ttu-id="f0fb5-145">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="f0fb5-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="f0fb5-146">Lagre (Finance and Operations til Field Service): Lager</span><span class="sxs-lookup"><span data-stu-id="f0fb5-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="f0fb5-147">[![Maltilordning i Dataintegrering](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="f0fb5-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

