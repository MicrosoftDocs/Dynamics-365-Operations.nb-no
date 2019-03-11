---
title: Konfigurere arbeidsflyter for linjeelement
description: Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66e79389bba4566176330914ace462110cd0aa22
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "336112"
---
# <a name="configure-line-item-workflows"></a>Konfigurere arbeidsflyter for linjeelement

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.

Når du skal konfigurere en arbeidsflyt for linjeelement i redigeringsprogrammet for arbeidsflyt, høyreklikker du elementet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden. Du kan deretter bruke fremgangsmåten nedenfor for å konfigurere egenskapene for arbeidsflyten for linjeelementet.

## <a name="name-the-line-item-workflow-element"></a>Navnet på arbeidsflyten for linjeelement

Følg denne fremgangsmåten for å sette et navn på arbeidsflyten for linjeelement.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I **Navn**-feltet angir du et unikt navn på arbeidsflyten for linjeelement.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementer

Følg denne fremgangsmåten for å angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementene på et dokument.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. Hvis den samme arbeidsflyten skal behandle alle linjeelementene på et dokument, klikker du **Aktiver én arbeidsflyt for alle linjeelementer**. Velg deretter arbeidsflyten som skal brukes til å behandle linjeelementene.
3. Hvis en bestemt arbeidsflyt skal behandle linjeelementer som oppfyller et bestemt sett med betingelser, klikker du **Aktiver en arbeidsflyt for hvert linjeelement**. Følg denne fremgangsmåten for å definere settet med betingelser:

    1. Klikk **Legg til**.
    2. Velg betingelsen i tabellen.
    3. I kategorien **Betingelsesnavn** skriver du inn et navn for settet med betingelser som du definerer.
    4. Klikk **Legg til betingelse** for å angi en betingelse.
    5. Angi eventuelle ekstra betingelser som kreves.
    6. Hvis du vil kontrollere om settet med betingelsene du har skrevet inn, er riktig konfigurert, klikker du **Test**. På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post, og deretter klikker du **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte. Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.

    I kategorien **Arbeidsflyt** velger du arbeidsflyten som skal brukes til å behandle linjeelementer som oppfyller settet med betingelser som du har definert.
