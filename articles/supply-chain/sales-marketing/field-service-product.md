---
title: Synkronisere produkter i Finance and Operations til produkter i Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562701"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Synkronisere produkter i Finance and Operations til produkter i Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

Den brukte **Field Service-produkter (Fin and Ops til Field Service)**-malen er basert på **Produkter (Fin and Ops til Sales) – direkte**-malen fra kundeemne til kontanter. Hvis du vil ha mer informasjon, se [Produkter (Fin and Ops til Sales) – direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Fin and Ops til Field Service)**- og **Produkter (Fin and Ops til Sales) – direkte**-malene.

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Field Service-produkter (Fin and Ops til Field Service)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- Produkter - produkter

**Field Service-produkter (Fin and Ops til Field Service)**-malen inneholder én tilordning som ikke er inkludert i **Produkter (Fin and Ops til Sales) – direkte**-malen. Denne tilordningen sikrer at det obligatoriske Field Service-spesifikke feltet **Serviceprodukttype** er riktig angitt.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Følgende verditilordning brukes.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

I Finance and Operations beregnes **Field Service-produkttype**-verdien i **Salgbare frigitte produkter**-dataenheten på følgende måte:

- **Beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Sann
- **Ikke-beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Usann
- **Service:** Produkttype = Service

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service-produkter (Fin and Ops til Field Service): Produkter – produkter

[![Maltilordning i Dataintegrering](./media/FSProduct.png)](./media/FSProduct.png)
