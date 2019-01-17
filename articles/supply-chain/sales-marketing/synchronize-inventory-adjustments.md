---
title: "Synkronisere lageroverføringer og -justeringer fra Field Service til Finance and Operations"
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere beholdningsjusteringer og -overføringer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Synkronisere lagerjusteringer fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere beholdningsjusteringer og -overføringer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere beholdningsjusteringer og -overføringer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

**Navn på malene i Dataintegrasjon:**
- Lagerjustering (Field Service til Finance and Operations)
- Lageroverføringer (Field Service til Finance and Operations)

**Navn på oppgavene i Dataintegrasjonprosjektene**:
- Lagerjusteringer
- Lageroverføringer

## <a name="entity-set"></a>Enhetssett
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Overskrifter og linjer i CDS-lagerjusteringsjournal |
| msdyn_inventoryadjustmentproducts | Overskrifter og linjer i CDS-lageroverføringsjournal   |

## <a name="entity-flow"></a>Enhetsflyt
Lagerjusteringer og -overføringer som er gjort i Field Service, synkroniseres til Finance and Operations når **posteringsstatusen** endres fra Opprettet til Postert. Når dette skjer, låses justerings- eller overføringsordren og blir skrivebeskyttet siden justeringer og overføringer kan posteres i Finance and Operations og derfor ikke kan endres.
Du kan definere en satsvis jobb i Finance and Operations for å postere automatisk lagerjournalene for justeringene og overføringene som genereres med integreringen. Se forutsetning under for mer informasjon om hvordan du aktiverer den satsvise jobben.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service 
Feltet Lagerenhet er lagt til produktenheten. Dette feltet er nødvendig ettersom salgs- og lagerenheten ikke alltid er den samme i Operations, og for lagerbeholdningen i Operations trenger vi lagerenheten.
Når du angir produktet for et lagerjusteringsprodukt for både lagerjusteringer og lageroverføringer, hentes enheten fra verdien for lagerprodukt for produkter. Hvis en verdi blir funnet, låses Enhet-feltet for lagerjusteringsproduktet.

Posteringsstatusfeltet er lagt til både enheten for lagerjustering og enheten for lageroverføring. Dette feltet brukes som filter for når en justering eller overføring sendes til Operations. Feltet settes som standard til Opprettet (1), og blir dermed ikke sendt til Operations. Når du endrer det til Postert (2), sendes det til Operations, men du vil da ikke lenger kunne endre noe i justeringen eller overføringen eller legge til nye linjer i den.
Feltet Nummerserie er lagt til produktenheten for lagerjustering. Dette feltet gjør at integreringen har et unikt nummer, slik at integreringen vet når opprettinger og oppdateringer skal gjøres. Når du oppretter det første lagerjusteringsproduktet, opprettes det en ny post i P2C Autonummer-enheten for å vedlikeholde nummerserien og prefikset som brukes.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="in-finance-and-operations"></a>I Finance og Operations
Integreringslagerjournalene som genereres i integreringen, kan posteres automatisk med en satsvis jobb. Dette aktiveres fra: Lagerstyring > Periodiske oppgaver > CDS-integrering > Poster lagerjournaler for integrering

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Lagerjustering (Field Service til Finance and Operations): Lagerjustering

[![Maltilordning i Dataintegrering](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Lageroverføring (Field Service til Finance and Operations): Lageroverføring

[![Maltilordning i Dataintegrering](./media/FSTrans1.png)](./media/FSTrans1.png)

