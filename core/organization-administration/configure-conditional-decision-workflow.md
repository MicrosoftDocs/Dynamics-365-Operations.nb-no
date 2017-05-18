---
title: Konfigurere en betinget beslutning i en arbeidsflyt
description: "Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d3efb6106df7d66ebe9b1a061f9976b8978704b1
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurere en betinget beslutning i en arbeidsflyt

[!include[banner](../includes/banner.md)]


Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.

En betinget beslutning er et punkt der en arbeidsflyt deles opp i to grener. Når du skal konfigurere en betinget beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den betingede beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.

## <a name="name-a-decision"></a>Navngi en beslutning
Følg denne fremgangsmåten for å angi et navn for en betinget beslutning.
1.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
2.  I feltet **Navn** angir du et unikt navn på den betingede beslutningen.

## <a name="set-conditions"></a> Angi betingelser
Systemet avgjør hvilken gren som skal brukes ved evaluering av det sendte dokumentet for å fastslå om det oppfyller angitte betingelser.
1.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
2.  Klikk **Legg til betingelse**.
3.  Angi en betingelse.
4.  Angi eventuelle ekstra betingelser som kreves.
5.  Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:
    1.  Klikk **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.
    2.  Velg en post i **Valider betingelse**-området i skjemaet.
    3.  Klikk **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.
    4.  Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.






