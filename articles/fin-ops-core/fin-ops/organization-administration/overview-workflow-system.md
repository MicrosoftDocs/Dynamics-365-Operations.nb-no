---
title: Oversikt over arbeidsflytsystem
description: Denne artikkelen beskriver arbeidsflytsystemet.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13dd4335a8b939a44ea7176a90f660999c32a83a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863195"
---
# <a name="workflow-system-overview"></a>Oversikt over arbeidsflytsystem

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikkelen beskriver arbeidsflytsystemet.

## <a name="what-is-workflow"></a>Hva er arbeidsflyt?

Begrepet *arbeidsflyt* kan defineres på to måter: som et system og en forretningsprosess.

### <a name="workflow-is-a-system"></a>Workflow er et system

Workflow er et system som kjører på Application Object Server (AOS). Arbeidsflytsystemet inneholder funksjonalitet du kan bruke til å opprette enkle arbeidsflyter eller forretningsprosesser.

### <a name="workflow-is-a-business-process"></a>Arbeidsflyt er en forretningsprosess

En arbeidsflyt representerer en forretningsprosess. Det definerer hvordan et dokument går eller flyttes gjennom systemet ved å vise hvem som må utføre en oppgave, ta avgjørelser eller godkjenne et dokument. Illustrasjonen nedenfor viser for eksempel en arbeidsflyt for reiseregninger.

![Arbeidsflyt med elementer som er tilordnet til brukere.](./media/workflow_user.gif)

Hvis du vil forstå denne arbeidsflyten bedre, kan vi anta at Erik sender en reiseregningsrapport på NOK 42 000. I denne situasjonen må Henrik gå gjennom kvitteringene som Erik sendte til ham. Deretter må Dag og Jorunn godkjenne reiseregningsrapporten. La oss nå anta at Erik sender en reiseregningsrapport på NOK 11 000. I denne situasjonen må Henrik se gjennom kvitteringene, og Dag, Jorunn og Karen må godkjenne reiseregningsrapporten.

## <a name="benefits-of-using-the-workflow-system"></a> Fordeler ved bruk av arbeidsflytsystemet

Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:

- **Konsekvente prosesser** – Du kan definere hvordan bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter, skal behandles. Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.
- **Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for arbeidsflytforekomster. Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.
- **Sentralisert arbeidsliste** – Brukere kan vise en sentralisert arbeidsliste som viser arbeidsflytoppgavene og -godkjenningene som er tilordnet til dem.


## <a name="workflow-content"></a>Arbeidsflytinnhold

+ [Arkitektur i arbeidsflytsystemet](workflow-system-architecture.md)
+ [Arbeidsflytelementer](workflow-elements.md)
+ [Handlinger i godkjenningsprosesser i en arbeidsflyt](workflow-actions.md)
+ [Oversikt over å opprette arbeidsflyter](create-workflow.md)
+ [Konfigurere egenskaper for arbeidsflyt](configure-workflow-properties.md)
+ [Konfigurere manuelle oppgaver i en arbeidsflyt](configure-manual-task-workflow.md)
+ [Konfigurere automatiserte oppgaver i en arbeidsflyt](configure-automated-task-workflow.md)
+ [Konfigurere godkjenningsprosesser i en arbeidsflyt](configure-approval-process-workflow.md)
+ [Konfigurere godkjenningstrinn i en arbeidsflyt](configure-approval-step-workflow.md)
+ [Konfigurere manuelle beslutninger i en arbeidsflyt](configure-manual-decision-workflow.md)
+ [Konfigurere en betingede beslutninger i en arbeidsflyt](configure-conditional-decision-workflow.md)
+ [Konfigurere parallelle aktiviter i en arbeidsflyt](configure-parallel-activity-workflow.md)
+ [Konfigurere parallelle avdelinger i en arbeidsflyt](configure-parallel-branch-workflow.md)
+ [Konfigurere arbeidsflyter for linjeelement](configure-line-item-workflow.md)
+ [Vanlige spørsmål om arbeidsflyt](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]