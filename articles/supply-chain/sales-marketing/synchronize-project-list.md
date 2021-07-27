---
title: Synkronisere prosjektliste fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
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
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: eb98f266a217fc16c56c38e2480b85f529fb1862
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359843"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Synkronisere prosjektliste fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av prosjekter fra Supply Chain Management til Field Service.

**Mal i Dataintegrasjon**
- Prosjekter (Supply Chain Management til Field Service)

**Oppgave i Dataintegrasjonprosjektet**:
- Prosjekter

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:
- Kontoer (Sales til Supply Chain Management) 

## <a name="entity-set"></a>Enhetssett
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Prosjekter                |

## <a name="entity-flow"></a>Enhetsflyt
Prosjekter opprettes i Supply Chain Management. Prosjekter med **Prosjekttype** satt til **Tid og materialer** og **Prosjektstadium** satt til **Pågår**, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto. Listen over **Eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Supply Chain Management-prosjekter.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
**Eksternt prosjekt**-enheten får alle prosjektene fra Supply Chain Management. Feltet **Eksternt prosjekt** er lagt til **Arbeidsordre**-enheten. Dette er et oppslagsfelt, så ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i Supply Chain Management. Når **Systemstatus** endrer **Åpen – pågår(690,970,000)** til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon
### <a name="supply-chain-management"></a>Supply Chain Management
Aktivere endringssporing for dataenhetsprosjekter.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Prosjekter (Supply Chain Management til Field Service): Prosjekter

[![Maltilordning i Dataintegrering.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]