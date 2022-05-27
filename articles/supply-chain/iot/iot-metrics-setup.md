---
title: Konfigurere måledata for IoT-intelligens
description: Dette emnet forklarer hvordan du konfigurerer måledata for IoT-intelligens.
author: johanhoffmann
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b67292e45746ee45460141b4be32f2f8f14076ad
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674344"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Konfigurere måledata for IoT-intelligens

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Konfigurer måledata

Hvis du vil vise tidsseriediagrammene i meldingene dine i Microsoft Dynamics 365 Supply Chain Management, må du definere måleverdiene ved å følge disse trinnene.

1. Kopiere tilkoblingsstrengen for Redis Cache:

    1. I Azure-portalen går du til Redis Cache.
    2. Gå til **Innstillinger** \> **Tilgangsnøkler**.
    3. Kopier verdien i feltet **Primær tilkoblingsstreng**.

2. I Supply Chain Management går du til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenarioparametere**.
3. Lim inn tilkoblingsstrengen du kopierte tidligere, på siden **Scenarioparametere** i kategorien **Tidsserier** i feltet **Renis-tilkoblingsstreng til metrikkverdilager**. Dette trinnet gjør det mulig å visualisere målingene fra Azure IoT-hub i Supply Chain Management. Når du limer inn verdien i feltet, vises den som **\*\*\*\*\*\***.

    > [!NOTE]
    > Når du oppdaterer Redis-buffer-tilkoblingsstrengen, må du også oppdatere dette feltet.

4. Gå til **Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Måleverdinøkler**.
5. Velg **Oppdater** på siden **Måleverdinøkler**.
6. I dialogboksen **Oppdater måleverdinøkler**, legg merke til at **Kjør i bakgrunnen** er valgt i feltet. Velg **OK**.

Alle måleverdinøklene i Redis Cache hentes og legges til i listen **Måleverdinøkler**. Måleverdier vises ikke før du [aktiverer scenariene](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Konfigurere tidsserien for ressursstatus

Følg denne fremgangsmåten for å konfigurere **Ressursstatus**.

1. I Supply Chain Management går du til **Produksjonskontroll \> Produksjonsutførelse \> Ressursstatus**.
2. På siden **Ressusstatus** velger du **Konfigurer**.
2. I dialogboksen **Konfigurer** i listen **Ressurs** velger du et element som skal overvåkes.
3. Velg **Rediger**-knappen for **Tidsserie 1**.
4. I dialogboksen **Tidsserie** velger du en metrikkverdi i rutenettet. (Du kan også bruke koblingen **Oppdater måleverdinøkler** for å oppdatere de metriske nøklene fra denne dialogboksen.)
5. Velg **OK** for å gå tilbake til dialogboksen **Konfigurer**.
6. Skriv inn et visningsnavn.
7. Velg en tidsramme i feltet **Vis data fra**.
8. Velg **OK**.

Diagrammet vises.

## <a name="delete-a-metric-key"></a>Slette en metrisk nøkkel

1. I Supply Chain Management går du til **Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Måleverdinøkler**.
2. På **Måleverdinøkler**-siden velger måleverdinøkkelen du vil slette.
3. Velg **Slett**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]