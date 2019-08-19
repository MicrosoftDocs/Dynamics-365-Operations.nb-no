---
title: Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: 6b56eb545f87c31ef30d6a897f48539068583486
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843439"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service 

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere lagerbeholdningsnivåer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Mal i Dataintegrasjon**
- Produktbeholdning (Fin and Ops til Field Service)
  
**Oppgave i Dataintegrasjonprosjektet**:
- Produktbeholdning

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av lagernivåer kan inntreffe:
- Lagre (Fin and Ops til Field Service) 
- Field Service-produkter med lagerenhet (Fin and Ops til Sales) 

## <a name="entity-set"></a>Enhetssett

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS-lagerbeholdning etter lager     |

## <a name="entity-flow"></a>Enhetsflyt
Lagernivåinformasjon fra Finance and Operations sendes til Field Service for valgte produkter. Lagernivåinformasjonen inkluderer: 
- Antall på lager (gjeldende registrert fysisk antall som finnes på lageret)
- Antall i ordre/bestilling (totalt registrert antall i ordre, for eksempel salgsordrer)
- Bestilt antall (totalt registrert bestilt antall, for eksempel kjøpsordrer)

Denne informasjonen blir registrert per frigitt produkt for hvert lager og synkroniseres basert på endringssporing, når lagernivået endres.

I Field Service oppretter integrasjonsløsningen lagerjournaler for delta, slik at nivåene i Field Service samsvarer med nivåene i Finance and Operations.

Finance and Operations fungerer som malen for lagernivåer. Så det er viktig å definere integrering for arbeidsordrer, overføringer og justeringer fra Field Service til Finance and Operations hvis denne funksjonen brukes i Field Service, sammen med synkronisering av lagernivåer fra Finance and Operations.

Produktene og lagrene der lagernivåer styres fra Finance and Operations, kan kontrolleres med avansert spørring og filtrering (Power Query).

> [!NOTE]
> Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt = Nei**) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering. Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations. I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations. For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
Enheten **Eksternt produktlager** brukes bare for serverdelen i integreringen. Denne enheten mottar lagernivåverdiene fra Finance and Operations i integreringen og endrer deretter disse verdiene til manuelle lagerjournaler, som deretter endrer lagerproduktene på lageret.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="data-integration"></a>Dataintegrering
For at prosjektet skal fungere må du kontrollere at integreringsnøkkelen er oppdatert for msdynce_externalproductinventories.
1.  Gå til **Dataintegrering > Tilkoblingssett**.
2.  Velg tilkoblingssettet som brukes.
3.  I kategorien **Integreringsnøkkel** kontrollerer du at følgende nøkler er lagt til msdynce_externalproductinventories:
      - msdynce_productnumber (produktnummer)
      - msdynce_warehouseid (lager-ID)
      
### <a name="data-integration-project"></a>Dataintegrasjonsprosjekt
Du kan bruke filtre med avansert spørring og filtrering slik at bare bestemte produkter og lagre sender lagernivåinformasjon fra Finance and Operations til Field Service.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Produktbeholdning (Fin and Ops til Field Service): Produktbeholdning

[![Maltilordning i Dataintegrering](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
