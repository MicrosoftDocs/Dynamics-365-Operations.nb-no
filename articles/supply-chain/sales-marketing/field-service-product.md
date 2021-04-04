---
title: Synkronisere produkter i Supply Chain Management til produkter i Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d3dc21a39c9866d09e500e2f14ff810bac7d57fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261051"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="b38a4-103">Synkronisere produkter i Supply Chain Management til produkter i Field Service</span><span class="sxs-lookup"><span data-stu-id="b38a4-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b38a4-104">Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b38a4-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="b38a4-105">Den brukte **Field Service-produkter (Supply Chain Management til Field Service)**-malen er basert på **Produkter (Supply Chain Management til Sales) – direkte**-malen fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="b38a4-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="b38a4-106">Hvis du vil ha mer informasjon, kan du se [Produkter (Supply Chain Management til Sales) – direkte](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="b38a4-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="b38a4-107">Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Supply Chain Management til Field Service)**- og **Produkter (Supply Chain Management til Sales) – direkte**-malene.</span><span class="sxs-lookup"><span data-stu-id="b38a4-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b38a4-108">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="b38a4-108">Templates and tasks</span></span>

<span data-ttu-id="b38a4-109">**Navnet på malen i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="b38a4-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="b38a4-110">Field Service-produkter (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="b38a4-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="b38a4-111">**Navnet på oppgaven i Dataintegrasjonprosjektet**</span><span class="sxs-lookup"><span data-stu-id="b38a4-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="b38a4-112">Produkter - produkter</span><span class="sxs-lookup"><span data-stu-id="b38a4-112">Products - Products</span></span>

<span data-ttu-id="b38a4-113">**Field Service-produkter (Supply Chain Management til Field Service)**-malen inneholder én tilordning som ikke er inkludert i **Produkter (Supply Chain Management til Sales) – direkte**-malen.</span><span class="sxs-lookup"><span data-stu-id="b38a4-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="b38a4-114">Denne tilordningen sikrer at det obligatoriske Field Service-spesifikke feltet **Serviceprodukttype** er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="b38a4-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="b38a4-115">Følgende verditilordning brukes.</span><span class="sxs-lookup"><span data-stu-id="b38a4-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="b38a4-116">I Supply Chain Management beregnes **Field Service-produkttype**-verdien i **Salgbare frigitte produkter**-dataenheten på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="b38a4-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="b38a4-117">**Beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Sann</span><span class="sxs-lookup"><span data-stu-id="b38a4-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="b38a4-118">**Ikke-beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Usann</span><span class="sxs-lookup"><span data-stu-id="b38a4-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="b38a4-119">**Service:** Produkttype = Service</span><span class="sxs-lookup"><span data-stu-id="b38a4-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b38a4-120">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="b38a4-120">Template mapping in Data integration</span></span>

<span data-ttu-id="b38a4-121">Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="b38a4-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="b38a4-122">Field Service-produkter (Supply Chain Management til Field Service): Produkter – produkter</span><span class="sxs-lookup"><span data-stu-id="b38a4-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="b38a4-123">[![Maltilordning i Dataintegrering](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="b38a4-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]