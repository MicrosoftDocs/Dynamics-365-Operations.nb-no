---
title: Synkronisere produkter med lagerenhet fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/14/2019
ms.locfileid: "842468"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Synkronisere produkter med lagerenhet fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Den brukte **Field Service-produkter med lagerenhet (Fin and Ops til Field Service)**-malen er basert på **Field Service-produkter (Fin and Ops til Field Service)**-malen. Hvis du vil ha mer informasjon, se [Field Service-produkter (Finance and Operations til Field Service)](field-service-product.md).

Dette emnet beskriver bare forskjellene mellom de to malene: 
- **Field Service-produkter med lagerenhet (Fin and Ops til Sales)**
- **Field Service-produkter (Fin and Ops til Field Service)** 

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Field Service-produkter med lagerenhet (Fin and Ops til Sales)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- Produkter

**Field Service-produkter med lagerenhet (Fin and Ops til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Fin and Ops til Field Service)**-malen. Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Field Service-produkter med lagerenhet (Fin and Ops til Field Service): Produkter

[![Maltilordning i Dataintegrering](./media/FSProduct1.png)](./media/FSProduct1.png)
