---
title: Synkronisere produkter i Supply Chain Management til produkter i Field Service
description: Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/09/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c05e79ac5ef0ddf9f1476cbb9647e1306134f615ccf1936f472bfa78fc6b5957
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754542"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Synkronisere produkter i Supply Chain Management til produkter i Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og den underliggende oppgaven som brukes til å synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

Den brukte **Field Service-produkter (Supply Chain Management til Field Service)**-malen er basert på **Produkter (Supply Chain Management til Sales) – direkte**-malen fra Kundeemne til kontanter. Hvis du vil ha mer informasjon, kan du se [Produkter (Supply Chain Management til Sales) – direkte](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Supply Chain Management til Field Service)**- og **Produkter (Supply Chain Management til Sales) – direkte**-malene.

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon**

- Field Service-produkter (Supply Chain Management til Field Service)

**Navnet på oppgaven i Dataintegrasjonprosjektet**

- Produkter - produkter

**Field Service-produkter (Supply Chain Management til Field Service)**-malen inneholder én tilordning som ikke er inkludert i **Produkter (Supply Chain Management til Sales) – direkte**-malen. Denne tilordningen sikrer at det obligatoriske Field Service-spesifikke feltet **Serviceprodukttype** er riktig angitt.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Følgende verditilordning brukes.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

I Supply Chain Management beregnes **Field Service-produkttype**-verdien i **Salgbare frigitte produkter**-dataenheten på følgende måte:

- **Beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Sann
- **Ikke-beholdning:** produkttype = produkter og varemodellgruppe, lagerført produkt = Usann
- **Service:** Produkttype = Service

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service-produkter (Supply Chain Management til Field Service): Produkter – produkter

[![Maltilordning i Dataintegrering.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]