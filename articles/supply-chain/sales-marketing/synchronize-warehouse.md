---
title: Synkronisere lagre fra Finance and Operations til Field Service
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Synkronisere lagre fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere lagre fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Navnet på malen i Dataintegrasjon:**
- Lagre (Finance and Operations til Field Service)

**Navnet på oppgaven i Dataintegrasjonprosjektet**:
- Lager

## <a name="entity-set"></a>Enhetssett
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagre                             |

## <a name="entity-flow"></a>Enhetsflyt
Lagre som opprettes og vedlikeholdes i Finance and Operations, kan synkroniseres til Field Service via et Common Data Service (CDS)-dataintegreringsprosjekt. De ønskede lagrene som synkroniseres til Field Service, kan styres med avansert spørring og filtrering på prosjektet. Lagre som synkroniseres fra Finance and Operations, opprettes i Field Service med feltet Vedlikeholdes eksternt satt til Ja og posten gjøres skrivebeskyttet.
Field Service CRM-løsningen For å støtte integrasjon mellom Field Service og Finance and Operations, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen. Løsningen inneholder følgende endringer.
Feltet **Vedlikeholdes eksternt** er lagt til i **Lager (msdyn_warehouses)**-enheten. Dette feltet brukes til å identifisere om lageret håndteres fra Operations, eller om det bare finnes i Field Service.
- Ja – Lageret kommer fra Finance and Operations, og kan ikke redigeres i Sales.
- Nei – Lageret ble registrert direkte i Field Service og vedlikeholdes her.

Feltet **Vedlikeholdes eksternt** gjør det mulig å kontrollere synkroniseringen av lagernivåer, justeringer, overføringer og bruk av arbeidsordrer. Det er bare lagre med **Vedlikeholdes eksternt** = Ja som kan brukes til å synkronisere direkte til det samme lageret i det andre systemet. 

Obs!  Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt** = Nei) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering. Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations. I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations. Se tilleggsinformasjon i Synkronisere lagerjusteringer fra Field Service til Finance and Operations og Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon
### <a name="in-the-data-integration-project"></a>I dataintegrasjonsprosjektet
Før synkronisering av lagrene må du huske å oppdatere avansert spørring og filtrering for prosjektet slik at det bare inneholder lagrene du vil hente fra Finance and Operations til Field Service. Vær oppmerksom på at du trenger lageret i Field Service for bruk i arbeidsordrer, justeringer og overføringer.  

Kontroller at **Integration-nøkkelen** finnes for **msdyn_warehouses**
1. Gå til Dataintegrering
2. Velg fanen **Tilkoblingssett**
3. Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre
4. Velg fanen **Integreringsnøkkel**
5. Finn msdyn_warehouses og kontroller at nøkkelen **msdyn_name (navn)** blir lagt til. Hvis den ikke vises, kan du legge den ved å klikke **Legg til nøkkel**, og klikke **Lagre** øverst på siden

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Lagre (Finance and Operations til Field Service): Lager

[![Maltilordning i Dataintegrering](./media/Warehouse1.png)](./media/Warehouse1.png)

