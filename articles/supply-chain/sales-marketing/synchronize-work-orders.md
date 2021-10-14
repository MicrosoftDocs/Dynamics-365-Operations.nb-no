---
title: Synkronisere arbeidsordrer med prosjekt fra Field Service til Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 03/12/2019
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
ms.openlocfilehash: f0b3214aba5882a585664030d6c1aebe34de455c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572535"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Synkronisere arbeidsordrer med prosjekt fra Field Service til Supply Chain Management

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgave som brukes til å synkronisere arbeidsordrer med et prosjektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Den brukte **Arbeidsordrer med prosjekt (Field Service til Supply Chain Management)**-malen er basert på **Arbeidsordrer (Field Service til Supply Chain Management)**-malen. Hvis du vil ha mer informasjon, kan du se [Synkronisere arbeidsordrer i Field Service til salgsordrer i Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Dette emnet beskriver bare forskjellene mellom de to malene:
- **Arbeidsordrer med prosjekt (Field Service til Supply Chain Management)**
- **Arbeidsordrer (Field Service til Supply Chain Management)**

Den viktigste forskjellen er at denne malen inneholder tilordning av prosjektnummeret som er tilordnet arbeidsordren i Field Service. Dette sikrer at salgsordren som opprettes i Supply Chain Management, inneholder prosjektnummeret, og at fakturering kan skje på det relaterte prosjektet. I tillegg til dette bruker malen avansert spørring og filtrering.

## <a name="templates-and-tasks"></a>Maler og oppgaver

**Navnet på malen i Dataintegrasjon:**

- Arbeidsordrer med prosjekt (Field Service til Supply Chain Management)

**Navnet på oppgaven i Dataintegrasjonprosjektet:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
Feltet **Eksternt prosjekt** er lagt til arbeidsordreenheten. Dette feltet er et oppslag, og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i Supply Chain Management. Når **systemstatusen** endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderHeader

[![Maltilordning i dataintegrering, Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderHeaderProject

[![Maltilordning i dataintegrering, Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderProduct

[![Maltilordning i dataintegrering, Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderService

[![Maltilordning i dataintegrering, Arbeidsordrer med prosjekt (Field Service til Supply Chain Management): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]