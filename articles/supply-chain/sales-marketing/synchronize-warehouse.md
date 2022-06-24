---
title: Synkronisere lagre fra Supply Chain Management til Field Service
description: Denne artikkelen omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
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
ms.openlocfilehash: 7fac40ebd8a1f7994997e12f1231e5522a0c0e24
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865070"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Synkronisere lagre fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]



Denne artikkelen omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av lagre fra Supply Chain Management til Field Service.

**Mal i Dataintegrasjon**
- Lagre (Supply Chain Management til Field Service)

**Oppgave i Dataintegrasjonprosjektet**:
- Lager

## <a name="table-set"></a>Tabellsett
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagre                             |

## <a name="table-flow"></a>Tabellflyt
Lagre som opprettes og vedlikeholdes i Supply Chain Management, kan synkroniseres til Field Service via et Microsoft Dataverse-dataintegreringsprosjekt. Lagrene du vil synkronisere til Field Service, kan styres med avansert spørring og filtrering på prosjektet. Lagre som synkroniseres fra Supply Chain Management, opprettes i Field Service med kolonnen **Vedlikeholdes eksternt** satt til **Ja**, og posten gjøres skrivebeskyttet.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
For å støtte integrasjon mellom Field Service og Supply Chain Management, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen. I løsningen er kolonnen **Vedlikeholdes eksternt** lagt til i tabellen **Lager (msdyn_warehouses)**. Denne kolonnen brukes til å identifisere om lageret håndteres fra Supply Chain Management, eller om det bare finnes i Field Service. Innstillingene for denne kolonnen inkluderer følgende:
- **Ja** – Lageret kommer fra Supply Chain Management og kan ikke redigeres i Sales.
- **Nei** – Lageret ble registrert direkte i Field Service og vedlikeholdes her.

Kolonnen **Vedlikeholdes eksternt** gjør det mulig å kontrollere synkroniseringen av lagernivåer, justeringer, overføringer og bruk av arbeidsordrer. Det er bare lagre med **Vedlikeholdes eksternt** satt til **Ja** som kan brukes til å synkronisere direkte til det samme lageret i det andre systemet. 

> [!NOTE]
> Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt** = Nei) og så tilordne dem til et enkelt lager med funksjonen for avansert spørring og filtrering. Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Supply Chain Management. I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Supply Chain Management. For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon
### <a name="data-integration-project"></a>Dataintegrasjonsprosjekt
Før synkronisering av lagrene må du huske å oppdatere avansert spørring og filtrering for prosjektet, slik at det bare inneholder lagrene du vil hente fra Supply Chain Management til Field Service. Vær oppmerksom på at du trenger lageret i Field Service for bruk i arbeidsordrer, justeringer og overføringer.  

For å kontroller at **Integreringsnøkkel** finnes for **msdyn_warehouses**:
1. Gå til Dataintegrering.
2. Velg fanen **Tilkoblingssett**.
3. Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre.
4. Velg fanen **Integreringsnøkkel**.
5. Finn msdyn_warehouses og bekreft at nøkkelen **msdyn_name (navn)** blir lagt til. Hvis den ikke vises, kan du legge den til ved å klikke **Legg til nøkkel**, og deretter klikke **Lagre** øverst på siden.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjon viser en tilordning av malen i Dataintegrering.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Lagre (Supply Chain Management til Field Service): Lagre

[![Maltilordning i Dataintegrering.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]