---
title: "Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service"
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Synkronisere informasjon om lagernivå fra Finance and Operations til Field Service 

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere lagernivåinformasjon fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere lagerbeholdningsnivåer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Navnet på malen i Dataintegrasjon:**
- Produktbeholdning (Finance and Operations til Field Service)
  
**Navnet på oppgaven i Dataintegrasjonprosjektet**:
- Produktbeholdning

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av lagernivåer kan inntreffe:
- Lagre (Finance and Operations til Field Service) 
- Field Service-produkter med lagerenhet (Finance and Operations til Sales) 

## <a name="entity-set"></a>Enhetssett

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS-lagerbeholdning etter lager     |

## <a name="entity-flow"></a>Enhetsflyt
Lagernivåinformasjon fra Finance and Operations sendes til Field Service for valgte produkter. Lagernivåinformasjonen omfatter: 
- Antall på lager (gjeldende registrert fysisk antall som finnes på lageret)
- Antall i ordre/bestilling (totalt registrert antall i ordre – det vil si salgsordrer)
- Bestilt antall (totalt registrert bestilt antall – det vil si kjøpsordrer)

Denne informasjonen blir registrert per frigitt produkt for hvert lager og synkroniseres basert på endringssporing, når lagernivået endres.

I Field Service oppretter integrasjonsløsningen lagerjournaler for delta, for å få nivåene i Field Service til å samsvare med nivåene i Finance and Operations.

Finance and Operations fungerer som malen for lagernivåer. Så det er viktig å definere integrering for arbeidsordrer, overføringer og justeringer fra Field Service til Finance and Operations hvis denne funksjonen brukes i Field Service, sammen med synkronisering av lagernivåer fra Finance and Operations.

Produktene og lagrene der lagernivåer styres fra Finance and Operations, kan kontrolleres med avansert spørring og filtrering (Power Query).

Obs!  Det er mulig å opprette flere lagre i Field Service (med Vedlikeholdes eksternt = Nei) og så tilordne dem til et enkelt lager i Finance and Operations, med funksjonen for avansert spørring og filtrering. Dette brukes i situasjoner der du vil at Field Service skal styre det detaljerte lagernivået og bare sende oppdateringer til Finance and Operations. I dette tilfellet vil ikke Field Service få lagernivåoppdateringer fra Finance and Operations. Se tilleggsinformasjon i Synkronisere lagerjusteringer fra Field Service til Finance and Operations og Synkronisere arbeidsordrer i Field Service til salgsordrer knyttet til prosjekt i Finance and Operations.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
Den eksterne produktlagerenheten er en ny enhet som bare brukes for serverdelen i integreringen. Den mottar lagernivåverdiene fra Finance and Operations i integreringen og endrer deretter disse verdiene til manuelle lagerjournaler, som deretter endrer lagerproduktene på lageret. 

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="in-the-data-integration-project"></a>I dataintegrasjonsprosjektet
Bruk filtre med avansert spørring og filtrering for å kontrollere at bare ønskede produkter og lagre sender lagernivåinformasjon fra Finance and Operations til Field Service.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Produktbeholdning (Finance and Operations til Field Service): Produktbeholdning

[![Maltilordning i Dataintegrering](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

