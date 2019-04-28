---
title: Synkronisere lagre fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/14/2019
ms.locfileid: "842539"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Synkronisere lagre fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgavene brukes til å utføre synkronisering av lagrene fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Mal i Dataintegrasjon**
- Lagre (Fin and Ops til Field Service)

**Oppgave i Dataintegrasjonprosjektet**:
- Lager

## <a name="entity-set"></a>Enhetssett
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagre                             |

## <a name="entity-flow"></a>Enhetsflyt
Lagre som opprettes og vedlikeholdes i Finance and Operations, kan synkroniseres til Field Service via et Common Data Service (CDS)-dataintegreringsprosjekt. Lagrene du vil synkronisere til Field Service, kan styres med avansert spørring og filtrering på prosjektet. Lagre som synkroniseres fra Finance and Operations, opprettes i Field Service med feltet **Vedlikeholdes eksternt** satt til **Ja**, og posten gjøres skrivebeskyttet.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
For å støtte integrasjon mellom Field Service og Finance and Operations, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen. I løsningen er feltet **Vedlikeholdes eksternt** lagt til i **Lager (msdyn_warehouses)**-enheten. Dette feltet brukes til å identifisere om lageret håndteres fra Finance and Operations, eller om det bare finnes i Field Service. Innstillingene for dette feltet inkluderer:
- **Ja** – Lageret kommer fra Finance and Operations og kan ikke redigeres i Sales.
- **Nei** – Lageret ble registrert direkte i Field Service og vedlikeholdes her.

Feltet **Vedlikeholdes eksternt** gjør det mulig å kontrollere synkroniseringen av lagernivåer, justeringer, overføringer og bruk av arbeidsordrer. Det er bare lagre med **Vedlikeholdes eksternt** satt til **Ja** som kan brukes til å synkronisere direkte til det samme lageret i det andre systemet. 

> [!NOTE]
> Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt** = Nei) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering. Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations. I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations. For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon
### <a name="data-integration-project"></a>Dataintegrasjonsprosjekt
Før synkronisering av lagrene må du huske å oppdatere avansert spørring og filtrering for prosjektet, slik at det bare inneholder lagrene du vil hente fra Finance and Operations til Field Service. Vær oppmerksom på at du trenger lageret i Field Service for bruk i arbeidsordrer, justeringer og overføringer.  

For å kontroller at **Integreringsnøkkel** finnes for **msdyn_warehouses**:
1. Gå til Dataintegrering.
2. Velg fanen **Tilkoblingssett**.
3. Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre.
4. Velg fanen **Integreringsnøkkel**.
5. Finn msdyn_warehouses og bekreft at nøkkelen **msdyn_name (navn)** blir lagt til. Hvis den ikke vises, kan du legge den til ved å klikke **Legg til nøkkel**, og deretter klikke **Lagre** øverst på siden.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjon viser en tilordning av malen i Dataintegrering.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Lagre (Fin and Ops til Field Service): Lager

[![Maltilordning i Dataintegrering](./media/Warehouse1.png)](./media/Warehouse1.png)
