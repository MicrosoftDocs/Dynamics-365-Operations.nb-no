---
title: Konfigurere en betingede beslutninger i en arbeidsflyt
description: Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fa708b4ac1f17a9ed6852a9eeb3e764b750a4a4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070964"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Konfigurere en betingede beslutninger i en arbeidsflyt

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.

En betinget beslutning er et punkt der en arbeidsflyt deles opp i to grener. Når du skal konfigurere en betinget beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den betingede beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.

## <a name="name-a-decision"></a>Navngi en beslutning

Følg denne fremgangsmåten for å angi et navn for en betinget beslutning.

1. Klikk på **Grunnleggende innstillinger** i ruten til venstre.
2. I feltet **Navn** angir du et unikt navn på den betingede beslutningen.

## <a name="set-conditions"></a> Angi betingelser

Systemet avgjør hvilken gren som skal brukes ved evaluering av det sendte dokumentet for å fastslå om det oppfyller angitte betingelser.

1. Klikk på **Grunnleggende innstillinger** i ruten til venstre.
2. Klikk på **Legg til betingelse**.
3. Angi en betingelse.
4. Angi eventuelle ekstra betingelser som kreves.
5. Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:

    1. Klikk på **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.
    2. Velg en post i **Valider betingelse**-området i skjemaet.
    3. Klikk på **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.
    4. Klikk på **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]