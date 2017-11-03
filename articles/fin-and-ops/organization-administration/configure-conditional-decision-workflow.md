---
title: Konfigurere en betinget beslutning i en arbeidsflyt
description: "Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

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






