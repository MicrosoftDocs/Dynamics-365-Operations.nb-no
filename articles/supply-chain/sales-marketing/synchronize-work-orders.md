---
title: Synkronisere arbeidsordrer med prosjekt fra Field Service til Finance and Operations
description: Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843415"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="358a1-103">Synkronisere arbeidsordrer med prosjekt fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="358a1-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="358a1-104">Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="358a1-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="358a1-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="358a1-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="358a1-106">Den brukte **Arbeidsordrer med prosjekt (Field Service til Fin and Ops)**-malen er basert på **Arbeidsordrer (Field Service til Fin and Ops)**-malen.</span><span class="sxs-lookup"><span data-stu-id="358a1-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="358a1-107">Hvis du vil ha mer inforrmasjon, se [Synkronisere arbeidsordrer i Field Service til salgsordrer i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="358a1-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="358a1-108">Dette emnet beskriver bare forskjellene mellom de to malene:</span><span class="sxs-lookup"><span data-stu-id="358a1-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="358a1-109">**Arbeidsordrer med prosjekt (Field Service til Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="358a1-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="358a1-110">**Arbeidsordrer (Field Service til Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="358a1-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="358a1-111">Den viktigste forskjellen er at denne malen inneholder tilordning av prosjektnummeret som er tilordnet arbeidsordren i Field Service. Dette sikrer at salgsordren som opprettes i Finance and Operations, inneholder prosjektnummeret, og at fakturering kan skje på det relaterte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="358a1-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="358a1-112">I tillegg til dette bruker malen avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="358a1-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="358a1-113">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="358a1-113">Templates and tasks</span></span>

<span data-ttu-id="358a1-114">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="358a1-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="358a1-115">Arbeidsordrer med prosjekt (Field Service til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="358a1-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="358a1-116">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="358a1-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="358a1-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="358a1-117">WorkOrderHeader</span></span>
- <span data-ttu-id="358a1-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="358a1-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="358a1-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="358a1-119">WorkOrderProduct</span></span>
- <span data-ttu-id="358a1-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="358a1-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="358a1-121">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="358a1-121">Field Service CRM solution</span></span>
<span data-ttu-id="358a1-122">Feltet **Eksternt prosjekt** er lagt til arbeidsordreenheten.</span><span class="sxs-lookup"><span data-stu-id="358a1-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="358a1-123">Dette feltet er et oppslag og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="358a1-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="358a1-124">Når **systemstatusen** endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="358a1-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="358a1-125">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="358a1-125">Template mapping in Data integration</span></span>

<span data-ttu-id="358a1-126">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="358a1-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="358a1-127">Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="358a1-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="358a1-128">[![Maltilordning i Dataintegrering](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="358a1-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="358a1-129">Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="358a1-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="358a1-130">[![Maltilordning i Dataintegrering](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="358a1-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="358a1-131">Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="358a1-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="358a1-132">[![Maltilordning i Dataintegrering](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="358a1-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="358a1-133">Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="358a1-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="358a1-134">[![Maltilordning i Dataintegrering](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="358a1-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
