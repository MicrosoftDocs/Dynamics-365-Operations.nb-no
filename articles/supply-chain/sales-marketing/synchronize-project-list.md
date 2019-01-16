---
title: Synkronisere prosjektliste fra Finance and Operations til Field Service
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Synkronisere prosjektliste fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Navnet på malen i Dataintegrasjon:**
- Prosjekter (Finance and Operations til Field Service)

**Navnet på oppgaven i Dataintegrasjonprosjektet**:
- Prosjekter

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:
- Kontoer (Sales til Finance and Operations) 

## <a name="entity-set"></a>Enhetssett
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Prosjekter                |

## <a name="entity-flow"></a>Enhetsflyt
Prosjekter opprettes i Finance and Operations. Prosjekter med **prosjekttype** Etter regning og **Prosjektstadium** som pågår, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto. Listen over **eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Finance and Operations-prosjekter.
Field Service CRM-løsningen Det eksterne prosjektet er en ny enhet som henter alle prosjektene fra Operations.
Feltet Eksternt prosjekt er lagt til arbeidsordreenheten. Dette feltet er et oppslag og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i Operations. Når systemstatusen endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet Eksternt prosjekt, og du kan ikke legge til, fjerne eller endre verdien.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon
### <a name="in-finance-and-operations"></a>I Finance og Operations
Aktivere endringssporing for dataenhetsprosjekter

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Prosjekter (Finance and Operations til Field Service): Prosjekter

[![Maltilordning i Dataintegrering](./media/FSProject1.png)](./media/FSProject1.png)

