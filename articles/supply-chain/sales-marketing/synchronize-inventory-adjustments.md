---
title: Synkronisere lageroverføringer og -justeringer fra Field Service til Finance and Operations
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagerjusteringer og -overføringer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/14/2019
ms.locfileid: "842421"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Synkronisere lagerjusteringer fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagerjusteringer og -overføringer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere lagerjusteringer og -overføringer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

**Maler i Dataintegrasjon**
- Lagerjustering (Field Service til Fin and Ops)
- Lageroverføringer (Field Service til Fin and Ops)

**Oppgaver i Dataintegrasjonprosjektene**:
- Lagerjusteringer
- Lageroverføringer

## <a name="entity-set"></a>Enhetssett
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Overskrifter og linjer i CDS-lagerjusteringsjournal |
| msdyn_inventoryadjustmentproducts | Overskrifter og linjer i CDS-lageroverføringsjournal   |

## <a name="entity-flow"></a>Enhetsflyt
Lagerjusteringer og -overføringer som er gjort i Field Service, synkroniseres til Finance and Operations etter at **Posteringsstatus** endres fra **Opprettet** til **Postert**. Når dette skjer, låses justeringen eller overføringsordren, og den blir skrivebeskyttet. Dette betyr at justeringer og overføringer kan posteres i Finance and Operations, men de kan ikke endres. Du kan definere en satsvis jobb i Finance and Operations for å postere justeringene og overføringene av lagerjournaler som er generert under integreringen. Se forutsetningene under for mer informasjon om hvordan du aktiverer den satsvise jobben.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service 
Feltet **Lagerenhet** er lagt til **Produkt**-enheten. Dette feltet er nødvendig ettersom salgs- og lagerenheten ikke alltid er den samme i Finance and Operations, og lagerenheten kreves for lagerbeholdningen i Finance and Operations.
Når du angir produktet for et lagerjusteringsprodukt for både lagerjusteringer og lageroverføringer, hentes enheten fra lagerproduktverdien. Hvis en verdi blir funnet, låses **Enhet**-feltet på lagerjusteringsproduktet.

**Posteringsstatus**-feltet er lagt til både enheten **Lagerjustering** og **Lageroverføring**-enheten. Dette feltet brukes som filter når en justering eller overføring sendes til Finance and Operations. Standarden for dette feltet er Opprettet (1), men den sendes ikke til Finance and Operations. Når du oppdaterer verdien til Postert (2), sendes den til Finance and Operations, men etter det vil du ikke lenger kunne endre justeringen eller overføringen eller legge til nye linjer.

Feltet **Nummerserie** er lagt til **Lagerjusteringprodukt**-enheten. Dette feltet sikrer at integreringen har et unikt nummer, slik at integreringen kan opprette og oppdatere justeringen. Når du oppretter det første lagerjusteringsproduktet, opprettes det en ny post i **P2C Autonummer**-enheten for å vedlikeholde nummerserien og prefikset som brukes.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="finance-and-operations"></a>Finance and Operations
Integreringslagerjournalene som genereres i integreringen, kan posteres automatisk med en satsvis jobb. Dette aktiveres fra **Lagerstyring > Periodiske oppgaver > CDS-integrering > Poster lagerjournaler for integrering**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Lagerjustering (Field Service til Fin and Ops): Lagerjustering

[![Maltilordning i Dataintegrering](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Lageroverføring (Field Service til Fin and Ops): Lageroverføring

[![Maltilordning i Dataintegrering](./media/FSTrans1.png)](./media/FSTrans1.png)
