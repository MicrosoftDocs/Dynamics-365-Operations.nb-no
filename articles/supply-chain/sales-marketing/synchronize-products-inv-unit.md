---
title: Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service
description: Denne artikkelen omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887261"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Synkronisere produkter med lagerenhet fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]

Denne artikkelen omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter med lagerenhet fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen er basert på **Field Service-produkter (Supply Chain Management til Field Service)**-malen. Hvis du vil ha mer informasjon, kan du se [Synkronisere produkter i Supply Chain Management til produkter i Field Service](field-service-product.md).

Denne artikkelen beskriver bare forskjellene mellom de to malene: 
- **Field Service-produkter med lagerenhet (Supply Chain Management til Sales)**
- **Field Service-produkter (Supply Chain Management til Field Service)** 

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Field Service-produkter med lagerenhet (Supply Chain Management til Sales)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- Produkter

Den brukte **Field Service-produkter med lagerenhet (Supply Chain Management til Field Service)**-malen inkluderer én tilordning som ikke er inkludert i **Field Service-produkter (Supply Chain Management til Field Service)**-malen. Denne tilordningen sikrer at lagerenheten som er nødvendig for synkronisering av lagernivået, er inkludert.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service-produkter med lagerenhet(Supply Chain Management til Field Service): Produkter

[![Maltilordning i Dataintegrering.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]