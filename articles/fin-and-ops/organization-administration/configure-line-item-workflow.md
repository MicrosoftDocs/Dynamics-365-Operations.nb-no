---
title: Kongifurere en arbeidsflyt for linjeelement
description: Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2781a0344f1de5caf0031d7c3d5b88678be153a4
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-line-item-workflow"></a>Kongifurere en arbeidsflyt for linjeelement

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.

Når du skal konfigurere en arbeidsflyt for linjeelement i redigeringsprogrammet for arbeidsflyt, høyreklikker du elementet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden. Du kan deretter bruke fremgangsmåten nedenfor for å konfigurere egenskapene for arbeidsflyten for linjeelementet.

## <a name="name-the-lineitem-workflow-element"></a>Navnet på arbeidsflyten for linjeelement
Følg denne fremgangsmåten for å sette et navn på arbeidsflyten for linjeelement.

1.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
2.  I **Navn**-feltet angir du et unikt navn på arbeidsflyten for linjeelement.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementer
Følg denne fremgangsmåten for å angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementene på et dokument.

1.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
2.  Hvis den samme arbeidsflyten skal behandle alle linjeelementene på et dokument, klikker du **Aktiver én arbeidsflyt for alle linjeelementer**. Velg deretter arbeidsflyten som skal brukes til å behandle linjeelementene.
3.  Hvis en bestemt arbeidsflyt skal behandle linjeelementer som oppfyller et bestemt sett med betingelser, klikker du **Aktiver en arbeidsflyt for hvert linjeelement**. Følg denne fremgangsmåten for å definere settet med betingelser:
    1.  Klikk **Legg til**.
    2.  Velg betingelsen i tabellen.
    3.  I kategorien **Betingelsesnavn** skriver du inn et navn for settet med betingelser som du definerer.
    4.  Klikk **Legg til betingelse** for å angi en betingelse.
    5.  Angi eventuelle ekstra betingelser som kreves.
    6.  Hvis du vil kontrollere om settet med betingelsene du har skrevet inn, er riktig konfigurert, klikker du **Test**. På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post, og deretter klikker du **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte. Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.

    I kategorien **Arbeidsflyt** velger du arbeidsflyten som skal brukes til å behandle linjeelementer som oppfyller settet med betingelser som du har definert.




