---
title: Synkronisere prosjektliste fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/14/2019
ms.locfileid: "842610"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Synkronisere prosjektliste fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver
Følgende mal og underliggende oppgavene brukes til å utføre synkronisering av prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Mal i Dataintegrasjon**
- Prosjekter (Fin and Ops til Field Service)

**Oppgave i Dataintegrasjonprosjektet**:
- Prosjekter

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:
- Kontoer (Sales til Fin and Ops) 

## <a name="entity-set"></a>Enhetssett
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Prosjekter                |

## <a name="entity-flow"></a>Enhetsflyt
Prosjekter opprettes i Finance and Operations. Prosjekter med **Prosjekttype** satt til **Tid og materialer** og **Prosjektstadium** satt til **Pågår**, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto. Listen over **Eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Finance and Operations-prosjekter.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service
**Eksternt prosjekt**-enheten får alle prosjektene fra Finance and Operations. Feltet **Eksternt prosjekt** er lagt til **Arbeidsordre**-enheten. Dette er et oppslagsfelt, så ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations. Når **Systemstatus** endrer **Åpen – pågår(690,970,000)** til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon
### <a name="finance-and-operations"></a>Finance and Operations
Aktivere endringssporing for dataenhetsprosjekter.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Prosjekter (Fin and Ops til Field Service): Prosjekter

[![Maltilordning i Dataintegrering](./media/FSProject1.png)](./media/FSProject1.png)
