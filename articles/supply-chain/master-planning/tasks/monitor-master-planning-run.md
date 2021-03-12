---
title: Overvåke en kjøring av hovedplanlegging
description: Dette emnet beskriver hvordan produksjonsplanleggerne kan se om det pågår en hovedplanlegging.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cbe2c55ef9e3ed35db30ca927f3472c750c1db5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999812"
---
# <a name="monitor-a-master-planning-run"></a>Overvåke en kjøring av hovedplanlegging

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Bruke et Gantt-diagram til å visualisere fremdriften for hovedplanlegging

På siden **Vis fremdrift for hovedplanlegging** kan du vise detaljer om historisk hovedplanlegging som kjøres som et Gantt-diagram. Denne funksjonaliteten kan hjelpe deg med å forstå tiden som brukes på de forskjellige fasene av hovedplanlegging. For en gjeldende aktiv planleggingsjobb kan du bruke siden **Vis fremdrift for hovedplanlegging** til å spore fremdriften og vise den estimerte gjenværende tiden.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>Aktivere og bruke fremdrifsvisualiseringsfunksjonen for hovedplan

Hvis du vil bruke denne funksjonen, gjør du følgende.

1. I arbeidsområdet **Funksjonsbehandling** i **Ny**-fanen velger du **Fremdrifsvisualisering for hovedplan** i listen. Hvis funksjonen ikke vises i **Ny**-fanen, ser du i fanene **Ikke aktivert** og **Alle**.
1. Velg **Aktiver nå**. Du kan også velge **Tidsplan**, og deretter velge tidspunktet når du vil at funksjonen skal aktiveres.

Siden **Vis fremdrift for hovedplanlegging** kan vise både historiske planleggingsjobber og aktive planleggingsjobber. 

Hvis du vil vise historiske planleggingsjobber, kan du velge mellom to alternativer. 

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**, og velg deretter **Historikk** i handlingsruten. Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**
1. Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**, og klikk **Historikk** på hovedplanlegging-flisen. Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**

Hvis du vil vise aktive planleggingsjobber, kan du velge mellom to alternativer. 
1. Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**, og velg **Uferdig planleggingsprosess** i handlingsruten. Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**.
1. Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**, og klikk **Vis fremdrift** på hovedplanlegging-flisen. Med den ønskede jobben valgt, velger du **Forespørsler**, og deretter velger du **Vis fremdrift**

Merk at du bare kan vise aktive jobber når en planleggingsjobb behandles.

### <a name="analyze-a-master-planning-job"></a>Analysere en hovedplanlegging-jobb

I Gantt-diagrammet kan du utvide hver av de følgende planleggingsprosessene for å vise flere detaljer om tiden som er brukt:

- Initialisering
- Sletter og setter inn data
- Dekningsplanlegging
- Forsinkelser
- Handlingsmeldinger
- Sluttbehandling
- Automatisk autorisering

Gantt-diagrammet er et nyttig verktøy hvis du vil vise virkningen av å bruke handlingsmeldinger.

#### <a name="navigation-in-the-gantt-chart"></a>Navigasjon i Gantt-diagrammet

- Hvis du vil utvide den valgte gruppen og vise detaljene, velger du plusstegnet (**+**) i trevisningen.
- Hvis du vil skjule den valgte gruppen, velger du minustegnet (**–**) i trevisningen.
- Du kan bruke tastaturet til navigasjon. Bruk **pil opp** og **pil ned** for å flytte mellom rader. Bruk **pil høyre** og **pil venstre** til å vise og skjule grupper.
- Hvis du vil åpne eller lukke alle nivåer i Gantt-diagrammet, velger du **Vis alle** eller **Skjul alle**.
- Hvis du vil vise den tilknyttede behandlingstiden, holder du pekeren over en oppgave. (Oppgaver er det laveste nivået i Gantt-diagrammet.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Vis en ekstra hovedplanleggingskjøring til å sammenligne jobber

Hvis du velger en jobb for hovedplanlegging i feltet **Vis en ekstra hovedplanleggingskjøring**, kan du vise en ekstra hovedplanlegging-kjøring i Gantt-diagrammet og sammenligne de to jobbene.

#### <a name="bom-level-display"></a>Visning på stykklistenivå

Stykklistenivåer vises på en annen måte for dekningsplanlegging, forsinkelser, handlinger og autorisering.

- **Dekningsplanlegging** – stykklistenivåer vises som forventet. De beregnes fra toppen og nedover.

    **Eksempel:** stykklistenivå 0, 1, 2

- **Forsinkelser** – stykklistenivåer vises etter hvert som stykklistenivåer for planlegging multipliseres med –1. (Med andre ord har de et negativt tegn.)

    **Eksempel:** stykklistenivå –2, –1, 0

- **Handlingsmelding** – stykklistenivåer vises som forventet. De beregnes fra toppen og nedover.

    **Eksempel:** stykklistenivå 0, 1, 2

- **Automatisk autorisering** – stykklistenivåer vises som 999 minus stykklistenivået for dekningsplanlegging.

    **Eksempel:** stykklistenivå 999, 998, 997

Følgende tabell viser en oversikt over virkemåten.

| Stykklistenivå som vises | Sluttvare | Delkomponent | Råmateriale |
|---|---|---|---|
| Dekningsplanlegging | 0 | 1 | 2 |
| Forsinkelser | 0 | –1 | –2 |
| Handlingsmelding | 0 | 1 | 2 |
| Automatisk autorisering | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Visualiser fremdriften

Hvis du viser en hovedplanleggingsjobb som for øyeblikket kjører, vises fremdriften gjennom farger i Gantt-diagrammet. Følgende farger gjelder for det blå temaet. For andre fargetemaer vil fargene være forskjellige.

- **Mørkeblå** – fullførte planleggingsoppgaver.
- **Oransje** – den pågående oppgaven.
- **Lyseblå** – estimatet for gjenstående oppgaver.

Fargen vises bare på det laveste nivået i Gantt-diagrammet. Velg **Vis alle** for å vise alle aktivitetene i hovedplanlegging-jobben. Beregningen av gjenstående oppgaver er basert på historiske hovedplanleggingsjobber.

## <a name="run-master-planning-and-track-processing-time"></a>Kjøre hovedplanlegging og spore behandlingstid

1. Velg **Hovedplanlegging** på standard instrumentbord.
1. Angi eller velg en verdi i **Plan**-feltet.
1. Velg **Kjør**.
1. Sett alternativet **Spor behandlingstid** til **Ja**.
1. Angi et tall i feltet **Antall tråder**.
1. Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .
1. I rutenettet velger du raden der **Felt**-feltet er satt til **Varenummer**.
1. Angi en verdi i **Kriterier**-feltet.
1. Velg **OK**.
