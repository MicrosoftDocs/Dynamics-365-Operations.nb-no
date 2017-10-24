---
title: Opprette en arbeidsflyt
description: Dette emnet forklarer hvordan du oppretter en arbeidsflyt.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, UnifiedOperations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4d57e47fe7f38a43ecfdfbdd701d7e6a7d7800d6
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-workflow"></a>Opprette en arbeidsflyt

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du oppretter en arbeidsflyt.

<a name="open-the-workflow-editor"></a>Åpne redigeringsprogrammet for arbeidsflyt
------------------------

Microsoft Dynamics 365 for Finance and Operations-modulen som du arbeider i, bestemmer hvilke typer arbeidsflyt som du kan opprette. Følg denne fremgangsmåten for å velge typen arbeidsflyt for å opprette og åpne redigeringsprogrammet for arbeidsflyt.

1.  Åpne modulen du vil opprette en ny arbeidsflyt for. Hvis du for eksempel vil opprette en arbeidsflyt for innkjøpsrekvisisjoner, klikker du **Innkjøp og leverandører**.
2.  Klikk **Oppsett** &gt; **\[Arbeidsflyter for\] modulnavn**.
3.  På listesiden som vises klikker du **Ny** i handlingsruten.
4.  På siden **Opprett arbeidsflyt** velger du typen arbeidsflyt å opprette, og deretter klikker du **Opprett arbeidsflyt**. Redigeringsprogrammet for arbeidsflyt åpnes. Du kan nå bruke fremgangsmåtene nedenfor for utforme arbeidsflyten.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Dra arbeidsflytelementer til lerretet
**Arbeidsflytelementer**-området i redigeringsprogrammet for arbeidsflyt inneholder elementer som du kan legge til i arbeidsflyten. Hvis du vil legge til elementer i arbeidsflyten, drar du dem til arbeidsområdet.

## <a name="connect-the-elements"></a>Koble elementene
Hvis du vil koble ett arbeidsflytelement til et annet, holder du markøren over et element til du ser koblingspunkt. Klikk et koblingspunkt, og dra det til et annet element. Pass på at du kobler alle elementene.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurere egenskapene for arbeidsflyten
Følg disse fremgangsmåtene for å konfigurere egenskapene for arbeidsflyten.

1.  Klikk lerretet for å være sikker på at ingen arbeidsflytelementer er valgt.
2.  Klikk **Egenskaper** for å åpne **Egenskaper**-siden for arbeidsflyten.
3.  Følg fremgangsmåten i emnet [Konfigurere egenskapene for en arbeidsflyt](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurere elementene for arbeidsflyten
Konfigurer hvert element du dro til lerretet. Hvis du vil ha informasjon om hvordan du konfigurerer hvert arbeidsflytelement, kan du se emnet nedenfor .

-   [Konfigurere en manuell oppgave](configure-manual-task-workflow.md)
-   [Konfigurere en automatisert oppgave](configure-automated-task-workflow.md)
-   [Konfigurere en godkjenningsprosess](configure-approval-process-workflow.md)
-   [Konfigurere et godkjenningstrinn](configure-approval-step-workflow.md)
-   [Konfigurere en manuell beslutning](configure-manual-decision-workflow.md)
-   [Konfigurere en betinget beslutning](configure-conditional-decision-workflow.md)
-   [Konfigurere en parallell aktivitet](configure-parallel-activity-workflow.md)
-   [Konfigurere en parallell avdeling](configure-parallel-branch-workflow.md)
-   [Konfigurere en arbeidsflyt for linjeelement](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Løse eventuelle feil eller advarsler
**Feil og advarsler**-ruten, nederst i redigeringsprogrammet for arbeidsflyt, viser meldinger som er generert for arbeidsflyten. Hvis du vil finne elementet der en feil eller advarsel oppstod, dobbeltklikker du feilen eller advarselen. Du må løse alle feil og advarsler må løses før du kan aktivere arbeidsflyten.

## <a name="save-and-activate-the-workflow"></a>Lagre og aktiver arbeidsflyten.
Når du er klar til å lagre og aktivere arbeidsflyten, følger du denne fremgangsmåten.

1.  Klikk **Lagre og Lukk** for å lukke redigeringsprogrammet for arbeidsflyt og åpne siden **Lagre arbeidsflyt**.
2.  Angi kommentarer om endringene du har gjort i arbeidsflyten, og klikk deretter **OK**.
3.  Hvis alle problemer med feil og advarsler er løst, vises **Aktiver arbeidsflyt**-siden. Velg ett av følgende alternativer:
    -   Hvis du vil aktivere denne versjonen av arbeidsflyten, klikker du **Aktiver den nye versjonen**. Når en arbeidsflyt er aktiv, kan brukere sende dokumenter til den for behandling.
    -   Hvis du ikke vil aktivere denne versjonen, klikker du **Ikke aktiver den nye versjonen**. Du kan aktivere arbeidsflyten senere.






