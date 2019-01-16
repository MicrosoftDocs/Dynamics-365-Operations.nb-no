---
title: Synkronisere arbeidsordrer fra Finance and Operations til Field Service
description: "Dette emnet beskriver malene og den underliggende oppgaven som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="704a7-103">Synkronisere arbeidsordrer med prosjekt fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="704a7-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="704a7-104">Dette emnet beskriver malene og den underliggende oppgaven som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="704a7-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="704a7-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="704a7-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="704a7-106">Den brukte **Field Service-produkter (Finance and Operations til Field Service)**-malen er basert på **Produkter (Finance and Operations til Sales) – direkte**-malen fra kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="704a7-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="704a7-107">Hvis du vil ha mer informasjon, se [Produkter (Finance and Operations til Sales) – direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="704a7-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="704a7-108">Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Finance and Operations til Field Service)**- og **Field Service-produkter (Finance and Operations til Field Service)**-malene.</span><span class="sxs-lookup"><span data-stu-id="704a7-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="704a7-109">Den viktigste forskjellen er at denne malen inneholder tilordning av prosjektnummeret som er tilordnet arbeidsordren i Field Service. Dette sikrer at salgsordren som opprettes i Finance and Operations, inneholder prosjektnummeret, og at fakturering kan skje på det relaterte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="704a7-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="704a7-110">I tillegg til dette bruker malen avansert spørring og filtrering.</span><span class="sxs-lookup"><span data-stu-id="704a7-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="704a7-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="704a7-111">Templates and tasks</span></span>

<span data-ttu-id="704a7-112">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="704a7-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="704a7-113">Arbeidsordrer med prosjekt (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="704a7-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="704a7-114">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="704a7-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="704a7-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="704a7-115">WorkOrderHeader</span></span>
- <span data-ttu-id="704a7-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="704a7-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="704a7-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="704a7-117">WorkOrderProduct</span></span>
- <span data-ttu-id="704a7-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="704a7-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="704a7-119">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="704a7-119">Field Service CRM solution</span></span>
<span data-ttu-id="704a7-120">Feltet **Eksternt prosjekt** er lagt til arbeidsordreenheten.</span><span class="sxs-lookup"><span data-stu-id="704a7-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="704a7-121">Dette feltet er et oppslag og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="704a7-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="704a7-122">Når **systemstatusen** endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="704a7-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="704a7-123">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="704a7-123">Template mapping in Data integration</span></span>

<span data-ttu-id="704a7-124">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="704a7-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="704a7-125">Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="704a7-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="704a7-126">[![Maltilordning i Dataintegrering](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="704a7-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="704a7-127">Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="704a7-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="704a7-128">[![Maltilordning i Dataintegrering](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="704a7-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="704a7-129">Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="704a7-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="704a7-130">[![Maltilordning i Dataintegrering](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="704a7-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="704a7-131">Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="704a7-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="704a7-132">[![Maltilordning i Dataintegrering](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="704a7-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

