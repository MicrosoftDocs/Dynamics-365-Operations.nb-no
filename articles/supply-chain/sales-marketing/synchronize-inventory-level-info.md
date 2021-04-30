---
title: Synkronisere informasjon om lagernivå fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
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
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910286"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Synkronisere informasjon om lagernivå fra Supply Chain Management til Field Service 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere lagernivåinformasjon fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere lagerbeholdningsnivåer fra Supply Chain Management til Field Service.

**Mal i Dataintegrasjon**
- Produktbeholdning (Supply Chain Management til Field Service)
  
**Oppgave i Dataintegrasjonprosjektet**:
- Produktbeholdning

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av lagernivåer kan inntreffe:
- Lagre (Supply Chain Management til Field Service) 
- Field Service-produkter med lagerenhet (Supply Chain Management til Sales) 

## <a name="entity-set"></a>Enhetssett

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Dataverse-lagerbeholdning etter lager     |

## <a name="entity-flow"></a>Enhetsflyt
Lagernivåinformasjon fra Finance and Operations sendes til Field Service for valgte produkter. Lagernivåinformasjonen inkluderer: 
- Antall på lager (gjeldende registrert fysisk antall som finnes på lageret)
- Antall i ordre/bestilling (totalt registrert antall i ordre, for eksempel salgsordrer)
- Bestilt antall (totalt registrert bestilt antall, for eksempel kjøpsordrer)

Denne informasjonen blir registrert per frigitt produkt for hvert lager og synkroniseres basert på endringssporing, når lagernivået endres.

I Field Service oppretter integrasjonsløsningen lagerjournaler for delta, slik at nivåene i Field Service samsvarer med nivåene i Supply Chain Management.

Supply Chain Management fungerer som malen for lagernivåer. Så det er viktig å definere integrering for arbeidsordrer, overføringer og justeringer fra Field Service til Supply Chain Management hvis denne funksjonen brukes i Field Service, sammen med synkronisering av lagernivåer fra Supply Chain Management.

Produktene og lagrene der lagernivåer styres fra Supply Chain Management, kan kontrolleres med avansert spørring og filtrering (Power Query).

> [!NOTE]
> Det er mulig å opprette flere lagre i Field Service (med **Vedlikeholdes eksternt = Nei**) og så tilordne dem til et enkelt lager i Supply Chain Management, med funksjonen for avansert spørring og filtrering. Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Supply Chain Management. I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Supply Chain Management. For tilleggsinformasjon se [Synkronisere lagerjusteringer fra Field Service til Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
Enheten **Eksternt produktlager** brukes bare for serverdelen i integreringen. Denne enheten mottar lagernivåverdiene fra Supply Chain Management i integreringen og endrer deretter disse verdiene til manuelle lagerjournaler, som deretter endrer lagerproduktene på lageret.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="data-integration"></a>Dataintegrering
For at prosjektet skal fungere må du kontrollere at integreringsnøkkelen er oppdatert for msdynce_externalproductinventories.
1.  Gå til **Dataintegrering > Tilkoblingssett**.
2.  Velg tilkoblingssettet som brukes.
3.  I fanen **Integreringsnøkkel** kontrollerer du at følgende nøkler er lagt til msdynce_externalproductinventories:
      - msdynce_productnumber (produktnummer)
      - msdynce_warehouseid (lager-ID)
      
### <a name="data-integration-project"></a>Dataintegrasjonsprosjekt
Du kan bruke filtre med avansert spørring og filtrering slik at bare bestemte produkter og lagre sender lagernivåinformasjon fra Supply Chain Management til Field Service.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Produktbeholdning (Supply Chain Management til Field Service): Produktbeholdning

[![Maltilordning i Dataintegrering](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]