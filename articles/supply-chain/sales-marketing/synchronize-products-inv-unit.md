---
title: Synkronisere produkter med lagerenhet fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2019
ms.locfileid: "836308"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c188c-103">Synkronisere produkter med lagerenhet fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="c188c-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c188c-104">Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c188c-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c188c-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="c188c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="c188c-106">Den brukte **Field Service-produkter med lagerenhet (Finance and Operations til Field Service)**-malen er basert på **Field Service-produkter (Finance and Operations til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="c188c-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c188c-107">Hvis du vil ha mer informasjon, se [Field Service-produkter (Finance and Operations til Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="c188c-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="c188c-108">Dette emnet beskriver bare forskjellene mellom de to malene:</span><span class="sxs-lookup"><span data-stu-id="c188c-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="c188c-109">**Field Service-produkter med lagerenhet (Finance and Operations til Sales)**</span><span class="sxs-lookup"><span data-stu-id="c188c-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="c188c-110">**Field Service-produkter (Finance and Operations til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="c188c-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="c188c-111">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="c188c-111">Templates and tasks</span></span>

<span data-ttu-id="c188c-112">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="c188c-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c188c-113">Field Service-produkter med lagerenhet (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="c188c-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="c188c-114">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="c188c-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c188c-115">Produkter</span><span class="sxs-lookup"><span data-stu-id="c188c-115">Products</span></span>

<span data-ttu-id="c188c-116">**Field Service-produkter med lagerenhet (Finance and Operations til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Finance and Operations til Field Service)**-malen.</span><span class="sxs-lookup"><span data-stu-id="c188c-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c188c-117">Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.</span><span class="sxs-lookup"><span data-stu-id="c188c-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c188c-118">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="c188c-118">Template mapping in Data integration</span></span>

<span data-ttu-id="c188c-119">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="c188c-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="c188c-120">Field Service-produkter med lagerenhet (Finance and Operations til Field Service): Produkter</span><span class="sxs-lookup"><span data-stu-id="c188c-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="c188c-121">[![Maltilordning i Dataintegrering](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="c188c-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
