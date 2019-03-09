---
title: Synkronisere produkter med lagerenhet fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "359250"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="968fd-103">Synkronisere produkter med lagerenhet fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="968fd-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="968fd-104">Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="968fd-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="968fd-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="968fd-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="968fd-106">Den brukte **Field Service-produkter (Finance and Operations til Field Service)**-malen er basert på **Produkter (Finance and Operations til Sales) – direkte**-malen fra kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="968fd-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="968fd-107">Hvis du vil ha mer informasjon, se [Produkter (Finance and Operations til Sales) – direkte](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="968fd-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="968fd-108">Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Finance and Operations til Field Service)**- og **Field Service-produkter (Finance and Operations til Field Service)**-malene.</span><span class="sxs-lookup"><span data-stu-id="968fd-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="968fd-109">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="968fd-109">Templates and tasks</span></span>

<span data-ttu-id="968fd-110">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="968fd-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="968fd-111">Field Service-produkter med lagerenhet (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="968fd-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="968fd-112">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="968fd-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="968fd-113">Produkter</span><span class="sxs-lookup"><span data-stu-id="968fd-113">Products</span></span>

<span data-ttu-id="968fd-114">**Field Service-produkter med lagerenhet (Finance and Operations til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Finance and Operations til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="968fd-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="968fd-115">Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="968fd-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="968fd-116">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="968fd-116">Template mapping in Data integration</span></span>

<span data-ttu-id="968fd-117">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="968fd-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="968fd-118">Field Service-produkter med lagerenhet (Finance and Operations til Field Service): Produkter</span><span class="sxs-lookup"><span data-stu-id="968fd-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="968fd-119">[![Maltilordning i Dataintegrering](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="968fd-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
