---
title: Oversikt over å opprette arbeidsflyter
description: Denne artikkelen forklarer hvordan du oppretter en arbeidsflyt.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "195583"
- intro-internal
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 1343061ba06d13e68a98b05c013867af0a4d07a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864493"
---
# <a name="create-workflows-overview"></a>Oversikt over å opprette arbeidsflyter

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikkelen forklarer hvordan du oppretter en arbeidsflyt.

## <a name="open-the-workflow-editor"></a>Åpne redigeringsprogrammet for arbeidsflyt

Modulen du arbeider i bestemmer hvilke typer arbeidsflyt du kan opprette. Følg denne fremgangsmåten for å velge typen arbeidsflyt for å opprette og åpne redigeringsprogrammet for arbeidsflyt.

1. Åpne modulen du vil opprette en ny arbeidsflyt for. Hvis du for eksempel vil opprette en arbeidsflyt for innkjøpsrekvisisjoner, klikker du **Innkjøp og leverandører**.
2. Klikk på **Oppsett** &gt; **\[Arbeidsflyter for\] modulnavn**.
3. På listesiden som vises klikker du **Ny** i handlingsruten.
4. På siden **Opprett arbeidsflyt** velger du typen arbeidsflyt å opprette, og deretter klikker du **Opprett arbeidsflyt**. Redigeringsprogrammet for arbeidsflyt åpnes. Du kan nå bruke fremgangsmåtene nedenfor for utforme arbeidsflyten.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Dra arbeidsflytelementer til lerretet

**Arbeidsflytelementer**-området i redigeringsprogrammet for arbeidsflyt inneholder elementer som du kan legge til i arbeidsflyten. Hvis du vil legge til elementer i arbeidsflyten, drar du dem til arbeidsområdet.

## <a name="connect-the-elements"></a>Koble elementene

Hvis du vil koble ett arbeidsflytelement til et annet, holder du markøren over et element til du ser koblingspunkt. Klikk på et koblingspunkt, og dra det til et annet element. Pass på at du kobler alle elementene.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurere egenskapene for arbeidsflyten

Følg disse fremgangsmåtene for å konfigurere egenskapene for arbeidsflyten.

1. Klikk lerretet for å være sikker på at ingen arbeidsflytelementer er valgt.
2. Klikk på **Egenskaper** for å åpne **Egenskaper**-siden for arbeidsflyten.
3. Følg fremgangsmåten i artikkelen [Konfigurere egenskaper arbeidsflyt](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurere elementene for arbeidsflyten

Konfigurer hvert element du dro til lerretet. Hvis du vil ha informasjon om hvordan du konfigurerer hvert arbeidsflytelement, kan du se emnet nedenfor .

- [Konfigurere manuelle oppgaver i en arbeidsflyt](configure-manual-task-workflow.md)
- [Konfigurere automatiserte oppgaver i en arbeidsflyt](configure-automated-task-workflow.md)
- [Konfigurere godkjenningsprosesser i en arbeidsflyt](configure-approval-process-workflow.md)
- [Konfigurere godkjenningstrinn i en arbeidsflyt](configure-approval-step-workflow.md)
- [Konfigurere manuelle beslutninger i en arbeidsflyt](configure-manual-decision-workflow.md)
- [Konfigurere en betingede beslutninger i en arbeidsflyt](configure-conditional-decision-workflow.md)
- [Konfigurere parallelle avdelinger i en arbeidsflyt](configure-parallel-activity-workflow.md)
- [Konfigurere en parallell avdeling](configure-parallel-branch-workflow.md)
- [Konfigurere arbeidsflyter for linjeelement](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Løse eventuelle feil eller advarsler

**Feil og advarsler**-ruten, nederst i redigeringsprogrammet for arbeidsflyt, viser meldinger som er generert for arbeidsflyten. Hvis du vil finne elementet der en feil eller advarsel oppstod, dobbeltklikker du feilen eller advarselen. Du må løse alle feil og advarsler må løses før du kan aktivere arbeidsflyten.

## <a name="save-and-activate-the-workflow"></a>Lagre og aktiver arbeidsflyten.

Når du er klar til å lagre og aktivere arbeidsflyten, følger du denne fremgangsmåten.

1. Klikk på **Lagre og Lukk** for å lukke redigeringsprogrammet for arbeidsflyt og åpne siden **Lagre arbeidsflyt**.
2. Angi kommentarer om endringene du har gjort i arbeidsflyten, og klikk deretter **OK**.
3. Hvis alle problemer med feil og advarsler er løst, vises **Aktiver arbeidsflyt**-siden. Velg ett av følgende alternativer:

    - Hvis du vil aktivere denne versjonen av arbeidsflyten, klikker du **Aktiver den nye versjonen**. Når en arbeidsflyt er aktiv, kan brukere sende dokumenter til den for behandling.
    - Hvis du ikke vil aktivere denne versjonen, klikker du **Ikke aktiver den nye versjonen**. Du kan aktivere arbeidsflyten senere.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]