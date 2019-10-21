---
title: Konfigurere en betingede beslutninger i en arbeidsflyt
description: Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 278773a5ad8be35f9b6dcd1ec0d0a35e32222bb1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179312"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Konfigurere en betingede beslutninger i en arbeidsflyt

[!include [banner](../includes/banner.md)]

Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.

En betinget beslutning er et punkt der en arbeidsflyt deles opp i to grener. Når du skal konfigurere en betinget beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den betingede beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.

## <a name="name-a-decision"></a>Navngi en beslutning

Følg denne fremgangsmåten for å angi et navn for en betinget beslutning.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I feltet **Navn** angir du et unikt navn på den betingede beslutningen.

## <a name="set-conditions"></a> Angi betingelser

Systemet avgjør hvilken gren som skal brukes ved evaluering av det sendte dokumentet for å fastslå om det oppfyller angitte betingelser.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. Klikk **Legg til betingelse**.
3. Angi en betingelse.
4. Angi eventuelle ekstra betingelser som kreves.
5. Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:

    1. Klikk **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.
    2. Velg en post i **Valider betingelse**-området i skjemaet.
    3. Klikk **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.
    4. Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.
