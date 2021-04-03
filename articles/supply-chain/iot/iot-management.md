---
title: Overvåke og behandle IoT-intelligens
description: Dette emnet forklarer hvordan du overvåker og administrerer IoT-intelligens.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a037cb31e297926b1bcb66bff91bdd7eb5c40b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264854"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Overvåke og behandle IoT-intelligens

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du overvåker og administrerer IoT-intelligens.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Overvåkingsscenarioer i Microsoft Dynamics 365 Supply Chain Management

Du kan overvåke behandling av IoT-intelligens fra flere steder:

+ **Moduler \> Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Varslinger** – Vis listen over uløste varslinger.
+ **Moduler \> Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Lukkede varslinger** – Vis listen over varslinger som er løst eller forkastet.
+ **Moduler \> Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Måleverdinøkler** – Vis måleverdinøklene for tidsoversiktsdiagrammet **Ressursstatus**.
+ **Moduler \> Produksjonskontroll \> Produksjonsutførelse \> Ressursstatus** – Spor spesifikke måleverdier ved hjelp av dialogboksen **Konfigurer**. Hvis et scenario oppdager et unntak, viser en varsling detaljer om unntaket.
+ **Arbeidsområder \> Produksjonsstyring \> Varslinger** – Vis listen over uløste varslinger.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Endre et kjørende scenario for IoT-intelligens

Når et scenario kjøres, kan du gjøre disse endringene:

+ Legge til nye definisjoner for sensorskjema.
+ Velge nye dataverdier for signaler.
+ Avbryte valget av eksisterende signaldataverdier.
+ Legge til og tilordne nye signaldataverdier.
+ Oppdatere terskelverdier.

Når et scenario kjøres, kan du ikke gjøre disse endringene:

+ Slette eller endre skjemadefinisjoner som for tiden brukes av et aktivert scenario.
+ Endre de valgte skjemabanene for det aktiverte .

## <a name="simulation-options"></a>Simuleringsalternativer

Du kan simulere fabrikkmaskinsignaler. Hvis du vil ha mer informasjon, kan du se disse emnene:

+ [Koble IoT DevKit AZ3166 til Azure IoT-hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Koble Raspberry PI online-simulator til Azure IoT-hub (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Oversikt over løsningsakselerator for enhetssimulering](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]