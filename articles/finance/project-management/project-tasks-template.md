---
title: Synkronisere prosjektoppgaver direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver malen og den underliggende oppgaven som brukes til å synkronisere prosjektoppgavene direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 977037f0e2b313ebf05a3e1616d34567f82e82d7
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250398"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere prosjektoppgaver direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malen og den underliggende oppgaven som brukes til å synkronisere prosjektoppgavene direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i versjon 8.0.
> - Hvis du bruker Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du kan konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefalte vi at du også installerer KB 4131710.
> - Integrasjon av faktiske data er tilgjengelig i versjon 8.0.1 eller nyere.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflyt for Project Service Automation til Finance

Project Service Automation til Finance-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance. Integreringsmalen som er tilgjengelig med dataintegreringsfunksjonen muliggjør dataflyt om prosjektoppgaver fra Project Service Automation til Finance.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.

[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mal og oppgave

For å få tilgang til malen velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektoppgaver fra Project Service Automation til Finance:

- **Navnet på malen i Dataintegrering:** Prosjektoppgaver (PSA til Fin and Ops)
- **Navnet på oppgaven i prosjektet:** Prosjektoppgaver

Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.

## <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finans                             |
|----------------------------|-------------------------------------|
| Prosjektoppgaver              | Integreringsenhet for prosjektoppgave |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektaktiviteter administreres i Project Service Automation, og de synkroniseres til Finance som prosjektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query for Excel til å filtrere data hvis denne betingelsen er oppfylt:

- Du har ressursspesifikke poster i en prosjektoppgave.

Hvis du må bruke Power Query, følger du disse retningslinjene:

- Prosjektoppgaver-malen (PSA til Fin and Ops) har et standardfilter som utelater ressursspesifikke poster fra en prosjektoppgave ved å angi filteret i **IsLineTask** til **Usann**. Hvis du oppretter din egen mal, må du legge til dette filteret.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance.

[![Tilordning av mal](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
