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
ms.openlocfilehash: 06d7ff272ecb79abded3c3d3ade1f6bc0ef1f095
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742361"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Synkronisere produkter i Finance and Operations til produkter i Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

Den brukte **Field Service-produkter (Fin and Ops til Field Service)**-malen er basert på **Produkter (Fin and Ops til Sales) – direkte**-malen fra kundeemne til kontanter. Hvis du vil ha mer informasjon, se [Produkter (Fin and Ops til Sales) – direkte](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

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
