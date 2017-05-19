---
title: Oversikt over arbeidsflytsystem
description: Dette emnet beskriver arbeidsflytsystemet i Microsoft Dynamics 365 for Operations.
author: sericks007
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5432e67ffa41e6a38b19c9fe5bb12c5acb2c345c
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="workflow-system-overview"></a>Oversikt over arbeidsflytsystem

[!include[banner](../includes/banner.md)]


Dette emnet beskriver arbeidsflytsystemet i Microsoft Dynamics 365 for Operations.

<a name="what-is-workflow"></a>Hva er arbeidsflyt?
-----------------

Begrepet *arbeidsflyt* kan defineres på to måter: som et system og en forretningsprosess.
### <a name="workflow-is-a-system"></a>Workflow er et system

Arbeidsflyt er et system som installeres med Dynamics 365 for Operations, og som kjøres på Application Object Server (AOS). Arbeidsflytsystemet inneholder funksjonalitet du kan bruke til å opprette enkle arbeidsflyter eller forretningsprosesser.

### <a name="workflow-is-a-business-process"></a>Arbeidsflyt er en forretningsprosess

En arbeidsflyt representerer en forretningsprosess. Det definerer hvordan et dokument går eller flyttes gjennom systemet ved å vise hvem som må utføre en oppgave, ta avgjørelser eller godkjenne et dokument. Illustrasjonen nedenfor viser for eksempel en arbeidsflyt for reiseregninger. 

![Arbeidsflyt med elementer som er tilordnet til brukere](./media/workflow_user.gif) 

Hvis du vil forstå denne arbeidsflyten bedre, kan vi anta at Erik sender en reiseregningsrapport på NOK 42 000. I denne situasjonen må Henrik gå gjennom kvitteringene som Erik sendte til ham. Deretter må Dag og Jorunn godkjenne reiseregningsrapporten. La oss nå anta at Erik sender en reiseregningsrapport på NOK 11 000. I denne situasjonen må Henrik se gjennom kvitteringene, og Dag, Jorunn og Karen må godkjenne reiseregningsrapporten.

## <a name="benefits-of-using-the-workflow-system"></a> Fordeler ved bruk av arbeidsflytsystemet

Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:
-   **Konsekvente prosesser** – Du kan definere hvordan bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter, skal behandles. Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.
-   **Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for arbeidsflytforekomster. Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.
-   **Sentralisert arbeidsliste** – Brukere kan vise en sentralisert arbeidsliste som viser arbeidsflytoppgavene og -godkjenningene som er tilordnet til dem.


## <a name="workflow-content"></a>Arbeidsflytinnhold

+ [Arbeidsflytarkitektur](workflow-system-architecture.md)
+ [Arbeidsflytelementer](workflow-elements.md)
+ [Arbeidsflythandlinger](workflow-actions.md)
+ [Opprette en arbeidsflyt](create-workflow.md)
+ [Konfigurere egenskaper for arbeidsflyt](configure-workflow-properties.md)
+ [Konfigurere en manuell oppgave i en arbeidsflyt](configure-manual-task-workflow.md)
+ [Konfigurere en automatisert oppgave i en arbeidsflyt](configure-automated-task-workflow.md)
+ [Konfigurere en godkjenningsprosess i en arbeidsflyt](configure-approval-process-workflow.md)
+ [Konfigurere et godkjenningstrinn i en arbeidsflyt](configure-approval-step-workflow.md)
+ [Konfigurere en manuell beslutning i en arbeidsflyt](configure-manual-decision-workflow.md)
+ [Konfigurere en betinget beslutning i en arbeidsflyt](configure-conditional-decision-workflow.md)
+ [Konfigurere en parallell aktivitet i en arbeidsflyt](configure-parallel-activity-workflow.md)
+ [Konfigurere en parallell avdeling i en arbeidsflyt](configure-parallel-branch-workflow.md)
+ [Konfigurere en arbeidsflyt for linjeelement](configure-line-item-workflow.md)

