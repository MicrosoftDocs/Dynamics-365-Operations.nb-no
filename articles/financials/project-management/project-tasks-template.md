---
title: Synkroniser prosjektaktiviteter fra Project Service Automation
description: "Dette emnet beskriver malen og underliggende oppgave som brukes til å synkronisere prosjektoppgaver direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: nb-no
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Synkroniser prosjektaktiviteter fra Project Service Automation direkte til prosjektaktiviteter i Finance and Operations

Dette emnet beskriver malen og underliggende oppgave som brukes til å synkronisere prosjektoppgaver direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations.

> [!NOTE]
> Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflyt for Project Service Automation til Finance and Operations

Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalen som er tilgjengelig med dataintegreringsfunksjonen muliggjør dataflyt om prosjektoppgaver fra Project Service Automation til Finance and Operations.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mal og oppgave

Hvis du vil åpne malen, velg **Prosjekter** i Microsoft PowerApps Admin Center, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektoppgaver fra Project Service Automation til Finance and Operations:

-**Navnet på malen i Dataintegrasjon:** Prosjektoppgaver (PSA til Fin and Ops) -**Navnet på oppgaven i prosjektet:** Prosjektoppgaver

Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.

## <a name="entity-set"></a>Enhetssett

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Prosjektoppgaver                           | Integreringsenhet for prosjektoppgave.   |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektaktiviteter administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query til å filtrere data hvis disse betingelsene er oppfylt:

- Du har ressursspesifikke poster i en prosjektoppgave.

Hvis du må bruke Power Query, følger du disse retningslinjene:

- Prosjektoppgaver-malen (PSA til Fin and Ops) har et standardfilter for å utelate ressursspesifikke poster fra en prosjektoppgave ved å angi filteret i **IsLineTask** til **Usann**. Hvis du oppretter din egen mal, må du legge til dette filteret.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


