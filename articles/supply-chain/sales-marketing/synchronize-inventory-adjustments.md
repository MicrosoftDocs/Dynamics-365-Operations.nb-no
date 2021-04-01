---
title: Synkronisere lageroverføringer og -justeringer fra Field Service til Supply Chain Management
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagerjusteringer og -overføringer fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: fce407a66c339f2ece4bbc37b30243a2ed172d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251895"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Synkronisere lageroverføringer og -justeringer fra Field Service til Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagerjusteringer og -overføringer fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere lagerjusteringer og -overføringer fra Field Service til Supply Chain Management.

**Maler i Dataintegrasjon**
- Lagerjustering (Field Service til Supply Chain Management)
- Lageroverføringer (Field Service til Supply Chain Management)

**Oppgaver i Dataintegrasjonprosjektene**:
- Lagerjusteringer
- Lageroverføringer

## <a name="table-set"></a>Tabellsett
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Overskrifter og linjer i Dataverse-lagerjusteringsjournal |
| msdyn_inventoryadjustmentproducts | Overskrifter og linjer i Dataverse-lageroverføringsjournal   |

## <a name="table-flow"></a>Tabellflyt
Lagerjusteringer og -overføringer som er gjort i Field Service, synkroniseres til Supply Chain Management etter at **Posteringsstatus** endres fra **Opprettet** til **Postert**. Når dette skjer, låses justeringen eller overføringsordren, og den blir skrivebeskyttet. Dette betyr at justeringer og overføringer kan posteres i Supply Chain Management, men de kan ikke endres. Du kan definere en satsvis jobb i Supply Chain Management for å postere justeringene og overføringene av lagerjournaler som er generert under integreringen. Se forutsetningene under for mer informasjon om hvordan du aktiverer den satsvise jobben.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service 
Kolonnen **Lagerenhet** er lagt til i **Produkt**-tabellen. Denne kolonnen er nødvendig siden salgs- og lagerenheten ikke alltid er den samme i Supply Chain Management, og lagerenheten kreves for lagerbeholdningen i Supply Chain Management.
Når du angir produktet for et lagerjusteringsprodukt for både lagerjusteringer og lageroverføringer, hentes enheten fra lagerproduktverdien. Hvis en verdi blir funnet, låses **Enhet**-kolonnen på lagerjusteringsproduktet.

**Posteringsstatus**-kolonnen er lagt til i tabellene **Lagerjustering** og **Lageroverføring**. Denne kolonnen brukes som filter når en justering eller overføring sendes til Supply Chain Management. Standarden for denne kolonnen er Opprettet (1), men den sendes ikke til Supply Chain Management. Når du oppdaterer verdien til Postert (2), sendes den til Supply Chain Management, men etter det vil du ikke lenger kunne endre justeringen eller overføringen eller legge til nye linjer.

Kolonnen **Nummerserie** er lagt til tabellen **Lagerjusteringsprodukt**. Denne kolonnen sikrer at integreringen har et unikt nummer, slik at integreringen kan opprette og oppdatere justeringen. Når du oppretter det første lagerjusteringsproduktet, opprettes det en ny post i tabellen **P2C Autonummer** for å vedlikeholde nummerserien og prefikset som brukes.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="supply-chain-management"></a>Supply Chain Management
Integreringslagerjournalene som genereres i integreringen, kan posteres automatisk med en satsvis jobb. Dette aktiveres fra **Lagerstyring > Periodiske oppgaver > Dataverse-integrering > Poster lagerjournaler for integrering**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Lagerjustering (Field Service til Supply Chain Management): Lagerjustering

[![Maltilordning i Dataintegrering](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Lageroverføring (Field Service til Supply Chain Management): Lageroverføring

[![Maltilordning i Dataintegrering](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]