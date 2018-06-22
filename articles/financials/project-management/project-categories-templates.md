---
title: Synkronisere utgiftskategorier for prosjekt fra Project Service Automation
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.

> [!NOTE]
> Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Dataflyt for Project Service Automation og Finance and Operations

Project Service Automation og Finance and Operations-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjektutgiftstransaksjonskategorier mellom Finance and Operations og Project Service Automation.

Hvis prosjektutgiftskategorier styres i Finance and Operations, er integreringsflyten først fra Finance and Operations til Project Service Automation og deretter oppdatering av integrerings-IDene for prosjektutgiftskategorier ved å synkronisere fra Project Service Automation til Finance and Operations.

Hvis prosjektutgiftskategoriene styres i Project Service Automation, er integreringsflyten først fra Project Service Automation til Finance and Operations. Prosjektkategoriene må allerede være konfigurert i Finance and Operations før synkronisering fra Project Service Automation. Synkronier deretter fra Finance and Operations tilbake til Project Service Automation og deretter fra Project Service Automation til Finance and Operations igjen. Dette sikrer at kategoriene er koblet og duplikater ikke opprettes.

> [!NOTE]
> Reiseregningskategoriene for prosjektet vil vanligvis styres i Finance and Operations. Hvis dette ikke er din situasjon, eller du allerede har opprettet i utgiftskategorier i Project Service Automation, må du først synkronisere med prosjektutgiftstransaksjonskategoriene (PSA til Fin and Ops) og deretter synkronisere med prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA). Du kan deretter kjøre synkroniseringen fra PSA til Fin and Ops én gang til.

> Hvis det først synkroniseres fra Project Service Automation, må prosjektkategoriene allerede være definert i Finance and Operations, og prosjektkategorier som må synkroniseres med Project Service Automation-transaksjonskategorier må være angitt som **Aktiv i journaler**.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Maler og oppgaver

For å få tilgang til tilgjengelige maler velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Finance and Operations til Project Service Automation:

-  **Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA)
-  **Navnet på oppgaven i prosjektet:** Synkroniser kategorier til PSA

## <a name="entity-set"></a>Enhetssett

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Integreringsenhet for kategorier    | Transaksjonskategorier        |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query til å angi faktureringstypen på transaksjonskategorien når du synkroniserer til Project Service Automation. Malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA) har en standardkolonne og tilordning som allerede finnes. Hvis du oppretter din egen mal, må du legge til en betinget kolonne i Power Query.
- Åpne Avansert syntaks for filtrering og spørring-skjemaet i tilordningen av prosjektutgiftskategorioppgaven.
- Velg **Legg til betinget kolonne**.
- Gi den nye kolonnen et navn, for eksempel Faktureringstype.
- Angi følgende betingelse: Hvis **CATEGORYID ikke er lik null, så 19235001, ellers null**.
- Klikk på **OK** i kolonnen.
- Husk å tilordne den nye kolonnen på siden for tilordning.

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance and Operations til Project Service Automation.

[![Tilordning av mal](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Project Service Automation til Finance and Operations:

-**Navnet på malen i Dataintegrasjon:** Prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops) -**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til Fin Ops

## <a name="entity-set"></a>Enhetssett

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Transaksjonskategorier          | Integreringsenhet for kategorier  | 

## <a name="entity-flow"></a>Enhetsflyt

Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier. Synkronisering tilbake til Finance and Operations oppdaterer integrasjons-ID-en fra Project Service Automation i Finance and Operations-prosjektkategorien.

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.

> [!NOTE]
> Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

