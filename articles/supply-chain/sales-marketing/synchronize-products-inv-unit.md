---
title: Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 8b65e9640106c5d351270074e39c121e70917228
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251230"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen er basert på **Field Service-produkter (Supply Chain Management til Field Service)**-malen. Hvis du vil ha mer informasjon, kan du se [Field Service-produkter (Supply Chain Management til Field Service)](field-service-product.md).

Dette emnet beskriver bare forskjellene mellom de to malene: 
- **Field Service-produkter med lagerenhet (Supply Chain Management til Sales)**
- **Field Service-produkter (Supply Chain Management til Field Service)** 

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Field Service-produkter med lagerenhet (Supply Chain Management til Sales)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- Produkter

Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Supply Chain Management til Field Service)**-malen. Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service-produkter med lagerenhet(Supply Chain Management til Field Service): Produkter

[![Maltilordning i Dataintegrering](./media/FSProduct1.png)](./media/FSProduct1.png)
