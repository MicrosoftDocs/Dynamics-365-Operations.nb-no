---
title: Synkronisere arbeidsordrer med prosjekt fra Field Service til Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ebf23c5c831e9dad5d13c72f82eb3eeb30da853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434217"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="95c28-103">Synkronisere arbeidsordrer med prosjekt fra Field Service til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="95c28-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="95c28-104">Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="95c28-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="95c28-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="95c28-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="95c28-106">Den brukte **Arbeidsordrer med prosjekt (Field Service til Supply Chain Management)**-malen er basert på **Arbeidsordrer (Field Service til Supply Chain Management)**-malen.</span><span class="sxs-lookup"><span data-stu-id="95c28-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="95c28-107">Hvis du vil ha mer informasjon, kan du se [Synkronisere arbeidsordrer i Field Service til salgsordrer i Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="95c28-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="95c28-108">Dette emnet beskriver bare forskjellene mellom de to malene:</span><span class="sxs-lookup"><span data-stu-id="95c28-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="95c28-109">**Arbeidsordrer med prosjekt (Field Service til Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="95c28-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="95c28-110">**Arbeidsordrer (Field Service til Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="95c28-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="95c28-111">Den viktigste forskjellen er at denne malen inneholder tilordning av prosjektnummeret som er tilordnet arbeidsordren i Field Service. Dette sikrer at salgsordren som opprettes i Supply Chain Management, inneholder prosjektnummeret, og at fakturering kan skje på det relaterte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="95c28-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="95c28-112">I tillegg til dette bruker malen avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="95c28-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="95c28-113">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="95c28-113">Templates and tasks</span></span>

<span data-ttu-id="95c28-114">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="95c28-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="95c28-115">Arbeidsordrer med prosjekt (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="95c28-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="95c28-116">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="95c28-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="95c28-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="95c28-117">WorkOrderHeader</span></span>
- <span data-ttu-id="95c28-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="95c28-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="95c28-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="95c28-119">WorkOrderProduct</span></span>
- <span data-ttu-id="95c28-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="95c28-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="95c28-121">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="95c28-121">Field Service CRM solution</span></span>
<span data-ttu-id="95c28-122">Feltet **Eksternt prosjekt** er lagt til arbeidsordreenheten.</span><span class="sxs-lookup"><span data-stu-id="95c28-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="95c28-123">Dette feltet er et oppslag, og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="95c28-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="95c28-124">Når **systemstatusen** endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="95c28-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="95c28-125">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="95c28-125">Template mapping in Data integration</span></span>

<span data-ttu-id="95c28-126">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="95c28-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="95c28-127">Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="95c28-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="95c28-128">[![Maltilordning i Dataintegrering](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="95c28-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="95c28-129">Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="95c28-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="95c28-130">[![Maltilordning i Dataintegrering](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="95c28-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="95c28-131">Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="95c28-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="95c28-132">[![Maltilordning i Dataintegrering](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="95c28-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="95c28-133">Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="95c28-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="95c28-134">[![Maltilordning i Dataintegrering](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="95c28-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
