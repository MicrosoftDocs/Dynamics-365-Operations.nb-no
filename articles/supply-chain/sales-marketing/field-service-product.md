---
title: Synkronisere produkter i Finance and Operations til produkter i Field Service
description: "Dette emnet beskriver malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: nb-no
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="38099-103">Synkronisere produkter i Finance and Operations til produkter i Field Service</span><span class="sxs-lookup"><span data-stu-id="38099-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="38099-104">Dette emnet beskriver malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="38099-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="38099-105">Den brukte **Field Service-produkter (Fin and Ops til Field Service)**-malen er basert på **Produkter (Fin and Ops til Sales) – direkte**-malen fra kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="38099-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="38099-106">Hvis du vil ha mer informasjon, se [Produkter (Fin and Ops til Sales) – direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="38099-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="38099-107">Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Fin and Ops til Field Service)**- og **Produkter (Fin and Ops til Sales) – direkte**-malene.</span><span class="sxs-lookup"><span data-stu-id="38099-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="38099-108">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="38099-108">Templates and tasks</span></span>

<span data-ttu-id="38099-109">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="38099-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="38099-110">Field Service-produkter (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="38099-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="38099-111">**Navnet på oppgaven i Dataintegrasjonprosjektet:**</span><span class="sxs-lookup"><span data-stu-id="38099-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="38099-112">Produkter - produkter</span><span class="sxs-lookup"><span data-stu-id="38099-112">Products - Products</span></span>

<span data-ttu-id="38099-113">**Field Service-produkter (Fin and Ops til Field Service)**-malen inneholder én tilordning som ikke er inkludert i **Produkter (Fin and Ops til Sales) – direkte**-malen.</span><span class="sxs-lookup"><span data-stu-id="38099-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="38099-114">Denne tilordningen sikrer at det obligatoriske Field Service-spesifikke feltet **Serviceprodukttype** er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="38099-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="38099-115">Følgende verditilordning brukes.</span><span class="sxs-lookup"><span data-stu-id="38099-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="38099-116">I Finance and Operations beregnes **Field Service-produkttype**-verdien i **Salgbare frigitte produkter**-dataenheten på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="38099-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="38099-117">**Beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Sann</span><span class="sxs-lookup"><span data-stu-id="38099-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="38099-118">**Ikke-beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Usann</span><span class="sxs-lookup"><span data-stu-id="38099-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="38099-119">**Service:** Produkttype = Service</span><span class="sxs-lookup"><span data-stu-id="38099-119">**Service:** Product type = Service</span></span>

