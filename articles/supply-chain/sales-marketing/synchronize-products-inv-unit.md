---
title: Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 911c5cc79ae359bbb77d31f366ccfeabf282a33e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434552"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="f05e4-103">Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="f05e4-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f05e4-104">Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="f05e4-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="f05e4-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="f05e4-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="f05e4-106">Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen er basert på **Field Service-produkter (Supply Chain Management til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="f05e4-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="f05e4-107">Hvis du vil ha mer informasjon, kan du se [Synkronisere produkter i Supply Chain Management til produkter i Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="f05e4-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="f05e4-108">Dette emnet beskriver bare forskjellene mellom de to malene:</span><span class="sxs-lookup"><span data-stu-id="f05e4-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="f05e4-109">**Field Service-produkter med lagerenhet (Supply Chain Management til Sales)**</span><span class="sxs-lookup"><span data-stu-id="f05e4-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="f05e4-110">**Field Service-produkter (Supply Chain Management til Field Service)**</span><span class="sxs-lookup"><span data-stu-id="f05e4-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="f05e4-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="f05e4-111">Templates and tasks</span></span>

<span data-ttu-id="f05e4-112">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="f05e4-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="f05e4-113">Field Service-produkter med lagerenhet (Supply Chain Management til Sales)</span><span class="sxs-lookup"><span data-stu-id="f05e4-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="f05e4-114">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="f05e4-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="f05e4-115">Produkter</span><span class="sxs-lookup"><span data-stu-id="f05e4-115">Products</span></span>

<span data-ttu-id="f05e4-116">Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Supply Chain Management til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="f05e4-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="f05e4-117">Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f05e4-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f05e4-118">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="f05e4-118">Template mapping in Data integration</span></span>

<span data-ttu-id="f05e4-119">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="f05e4-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="f05e4-120">Field Service-produkter med lagerenhet(Supply Chain Management til Field Service): Produkter</span><span class="sxs-lookup"><span data-stu-id="f05e4-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="f05e4-121">[![Maltilordning i Dataintegrering](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="f05e4-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
