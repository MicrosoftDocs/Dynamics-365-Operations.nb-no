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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 87daaa3d2b516581e9925fe6b769683942893ff6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206925"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="318db-103">Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="318db-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="318db-104">Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="318db-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="318db-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="318db-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="318db-106">Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen er basert på **Field Service-produkter (Supply Chain Management til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="318db-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="318db-107">Hvis du vil ha mer informasjon, kan du se [Synkronisere produkter i Supply Chain Management til produkter i Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="318db-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="318db-108">Dette emnet beskriver bare forskjellene mellom de to malene:</span><span class="sxs-lookup"><span data-stu-id="318db-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="318db-109">**Field Service-produkter med lagerenhet (Supply Chain Management til Sales)**</span><span class="sxs-lookup"><span data-stu-id="318db-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="318db-110">**Field Service-produkter (Supply Chain Management til Field Service)**</span><span class="sxs-lookup"><span data-stu-id="318db-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="318db-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="318db-111">Templates and tasks</span></span>

<span data-ttu-id="318db-112">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="318db-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="318db-113">Field Service-produkter med lagerenhet (Supply Chain Management til Sales)</span><span class="sxs-lookup"><span data-stu-id="318db-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="318db-114">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="318db-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="318db-115">Produkter</span><span class="sxs-lookup"><span data-stu-id="318db-115">Products</span></span>

<span data-ttu-id="318db-116">Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Supply Chain Management til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="318db-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="318db-117">Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="318db-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="318db-118">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="318db-118">Template mapping in Data integration</span></span>

<span data-ttu-id="318db-119">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="318db-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="318db-120">Field Service-produkter med lagerenhet(Supply Chain Management til Field Service): Produkter</span><span class="sxs-lookup"><span data-stu-id="318db-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="318db-121">[![Maltilordning i Dataintegrering](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="318db-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]