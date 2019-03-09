---
title: Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "347842"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.
> - Integrasjon av faktiske data er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere.
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Dataflyt for Project Service Automation og Finance and Operations

Project Service Automation og Finance and Operations-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjektutgiftstransaksjonskategorier mellom Finance and Operations og Project Service Automation.

Hvis prosjektutgiftskategoriene styres i Finance and Operations, er integreringsflyten først fra Finance and Operations til Project Service Automation. Integrasjons-ID-ene for prosjektutgiftskategorier oppdateres deretter via synkronisering fra Project Service Automation til Finance and Operations.

Hvis prosjektutgiftskategoriene styres i Project Service Automation, er integreringsflyten først fra Project Service Automation til Finance and Operations. Prosjektkategoriene må allerede være konfigurert i Finance and Operations før synkronisering fra Project Service Automation. Synkronier deretter fra Finance and Operations tilbake til Project Service Automation, og deretter fra Project Service Automation til Finance and Operations igjen. På denne måten kan du sørge for at kategoriene kobles, og at ingen duplikater opprettes.

> [!NOTE]
> Reiseregningskategoriene for prosjektet styres vanligvis i Finance and Operations. Men hvis de ikke styres i Finance and Operations, eller hvis utgiftskategorier allerede er opprettet i Project Service Automation, må du først synkronisere ved å bruke malen for prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops). Synkroniser deretter ved å bruke malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA). Du kan deretter kjøre synkroniseringen fra Project Service Automation til Finance and Operations én gang til.
>
> Hvis du synkroniserer først fra Project Service Automation, må følgende krav oppfylles i Finance and Operations før synkroniseringen kjøres:
>
> - Den delte kategorien som samsvarer med prosjektkategorien som er definert i Project Service Automation, må finnes, og den må være aktivert for både **Prosjekt** og **Utgift**.
> - For hver juridiske enhet i Finance and Operations som det må integreres med, må følgende prosjektkategorier finnes:
>
>     - **Prosjektkategori** finnes. 
>     - **Bruk i utgift** er aktivert.
>     - **Aktiv i journal** er aktivert.
>     - **Transaksjonstype** er satt til **Utgift**.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Synkronisering av prosjektutgiftskategori fra Finance and Operations til Project Service Automation

### <a name="template-and-task"></a>Mal og oppgave

For å få tilgang til malen velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Finance and Operations til Project Service Automation:

- **Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA)
- **Navnet på oppgaven i prosjektet:** Synkroniser kategorier til PSA

### <a name="entity-set"></a>Enhetssett

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Integreringsenhet for kategorier | Transaksjonskategorier     |

### <a name="entity-flow"></a>Enhetsflyt

Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier.

### <a name="power-query"></a>Power Query

Når du synkroniserer til Project Service Automation, må du bruke Microsoft Power Query for Excel til å angi faktureringstypen på transaksjonskategorien. Malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA) har en standardkolonne og tilordning. Hvis du oppretter din egen mal, må du legge til en betinget kolonne i Power Query. Følg disse trinnene.

1. Klikk på pilen for å åpne tilordningen av prosjektutgiftskategorioppgaven i malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA).
2. Klikk på koblingen **Avansert spørring og filtrering** for å åpne Power Query.
2. Velg **Legg til betinget kolonne**.
3. Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**.
4. Angi følgende betingelse: **hvis CATEGORYID ikke er lik null, så 19235001, ellers null**.
5. Klikk på **OK** i kolonnen.
6. Husk å tilordne den nye kolonnen på siden for tilordning.

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance and Operations til Project Service Automation.

[![Tilordning av mal](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Synkronisering av prosjektutgiftskategori fra Project Service Automation til Finance and Operations

### <a name="template-and-task"></a>Mal og oppgave

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Project Service Automation til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops)
- **Navnet på oppgaven i prosjektet:** Synkroniser kategorier til Fin Ops

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Transaksjonskategorier     | Integreringsenhet for kategorier |

### <a name="entity-flow"></a>Enhetsflyt

Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier. Synkronisering tilbake til Finance and Operations oppdaterer prosjektkategorien i Finance and Operations med integrasjons-ID-en fra Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.

> [!NOTE]
> Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
