---
title: Synkronisere arbeidsordrer med prosjekt fra Field Service til Finance and Operations
description: Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843415"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Synkronisere arbeidsordrer med prosjekt fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Den brukte **Arbeidsordrer med prosjekt (Field Service til Fin and Ops)**-malen er basert på **Arbeidsordrer (Field Service til Fin and Ops)**-malen. Hvis du vil ha mer inforrmasjon, se [Synkronisere arbeidsordrer i Field Service til salgsordrer i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Dette emnet beskriver bare forskjellene mellom de to malene:
- **Arbeidsordrer med prosjekt (Field Service til Fin and Ops)**
- **Arbeidsordrer (Field Service til Fin and Ops)**

Den viktigste forskjellen er at denne malen inneholder tilordning av prosjektnummeret som er tilordnet arbeidsordren i Field Service. Dette sikrer at salgsordren som opprettes i Finance and Operations, inneholder prosjektnummeret, og at fakturering kan skje på det relaterte prosjektet. I tillegg til dette bruker malen avansert spørring og filtrering.

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Arbeidsordrer med prosjekt (Field Service til Fin and Ops)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
Feltet **Eksternt prosjekt** er lagt til arbeidsordreenheten. Dette feltet er et oppslag og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations. Når **systemstatusen** endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderHeader

[![Maltilordning i Dataintegrering](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderHeaderProject

[![Maltilordning i Dataintegrering](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderProduct

[![Maltilordning i Dataintegrering](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Arbeidsordrer med prosjekt (Field Service til Fin and Ops): WorkOrderService

[![Maltilordning i Dataintegrering](./media/FSWOP4.png)](./media/FSWOP4.png)
