---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (27. november 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897494"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (27. november 2018)

**Build 8.1.2064**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.


## <a name="changes"></a>Endringer

### <a name="unable-to-create-a-note-in-case-management"></a>Kan ikke opprette en merknad i Saksbehandling

En endring er gjort på et problem når du prøver å redigere eller opprette en merknad i saksloggen for Saksbehandling.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Feilstavede ord i kategorien analyse i kompensasjonsarbeidsområdet 

En endring er gjort for å rette opp stavemåten for 'etnisk opprinnelse' i kompensasjonsanalysediagrammet i kompensasjonsarbeidsområdet.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Området for ansattselvbetjening viser ikke når en bruker ikke er tilordnet til en arbeider 

Det er gjort en endring når **Ansattselvbetjening**-arbeidsområdet er valgt som den første siden ved oppstart for en bruker som ikke er tilordnet en arbeider. I dette tilfellet vises standard instrumentbord.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Lønn- og fraværsfeil: Objektreferanse er ikke satt til en forekomst av et objekt

Endringer er gjort i Permisjon og fravær for å rette denne feilen etter godkjenning av lønns- og fraværsposter i **Arbeidselementer som er tilordnet til meg**-listen.

### <a name="unable-to-recall-an-image-workflow"></a>Kan ikke tilbakekalle en arbeidsflyt for bilde

Når tilbakekalling av en arbeidsflyt for bilde er utført, settes arbeidsflyten til "avbrutt", og den eksisterende forespørselen i arbeidsområdet for ansattselvbetjening kan slettes.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Ansatte eller oppdragstakere som er ansatt på nytt, vises flere ganger etter avslutning 

Med denne oppdateringen vises avsluttede ansatte som er ansatt på nytt, bare én gang i listen over avsluttede. 

## <a name="known-issue"></a>Kjent problem

- **Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene. 
- **Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket. Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert. (Dette problemet vil bli løst i neste plattformoppdatering.)
