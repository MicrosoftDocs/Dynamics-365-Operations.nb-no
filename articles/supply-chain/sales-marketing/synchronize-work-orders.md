---
title: Synkronisere arbeidsordrer fra Finance and Operations til Field Service
description: "Dette emnet beskriver malene og den underliggende oppgaven som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Synkronisere arbeidsordrer med prosjekt fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og den underliggende oppgaven som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Den brukte **Field Service-produkter (Finance and Operations til Field Service)**-malen er basert på **Produkter (Finance and Operations til Sales) – direkte**-malen fra kundeemne til kontanter. Hvis du vil ha mer informasjon, se [Produkter (Finance and Operations til Sales) – direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emnet beskriver bare forskjellene mellom **Field Service-produkter (Finance and Operations til Field Service)**- og **Field Service-produkter (Finance and Operations til Field Service)**-malene.

Den viktigste forskjellen er at denne malen inneholder tilordning av prosjektnummeret som er tilordnet arbeidsordren i Field Service. Dette sikrer at salgsordren som opprettes i Finance and Operations, inneholder prosjektnummeret, og at fakturering kan skje på det relaterte prosjektet. I tillegg til dette bruker malen avansert spørring og filtrering.

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Arbeidsordrer med prosjekt (Field Service til Finance and Operations)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
Feltet **Eksternt prosjekt** er lagt til arbeidsordreenheten. Dette feltet er et oppslag og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations. Når **systemstatusen** endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderHeader

[![Maltilordning i Dataintegrering](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderHeaderProject

[![Maltilordning i Dataintegrering](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderProduct

[![Maltilordning i Dataintegrering](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Arbeidsordrer med prosjekt (Field Service til Finance and Operations): WorkOrderService

[![Maltilordning i Dataintegrering](./media/FSWOP4.png)](./media/FSWOP4.png)

