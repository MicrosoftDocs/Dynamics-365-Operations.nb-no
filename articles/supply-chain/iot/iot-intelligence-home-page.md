---
title: Startside for IoT-intelligens
description: Denne artikkelen inneholder koblinger til informasjon om IoT-intelligens.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b43681b036379a6f95103d4bb17cbde018724552
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877631"
---
# <a name="iot-intelligence-home-page"></a>Startside for IoT-intelligens

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Denne funksjonen er for øyeblikket bare tilgjengelig i følgende land/områder:
>
> - USA
> - EU (Den europeiske union)
> - AU (Australia)
> - CA (Canada)
> - UK (Storbritannia)

IoT-intelligens er et tillegg for Microsoft Dynamics 365 Supply Chain Management. Den integrerer IoT-signaler med data i Supply Chain Management for å gi praktisk innsikt.

IoT Intelligenc støtter følgende scenarier:

- **Produksjonsforsinkelser** – Dette scenariet sammenligner faktisk syklustid med planlagt syklustid. Supply Chain Management varsler deg når produksjon ikke er planlagt, slik at du kan gripe inn for å maksimere driftseffektivitet og unngå forsinkelser i ordren.
- **Nedtid på utstyr** – Dette scenariet sammenligner målt oppetid med brukerdefinerte parametere. Supply Chain Management varsler deg når en avbruddsterskel blir overskredet, slik at du kan utføre handlinger, for eksempel planlegge en produksjonsordre på nytt eller opprette en vedlikeholdsarbeidsordre.
- **Produktkvalitet** – Dette scenariet sammenligner sensoravlesninger, for eksempel fuktighet og temperatur, med brukerdefinerte kvalitetsmetrikk. Supply Chain Management varsler deg når det oppstår et avvik, slik at du kan gripe inn for å vedlikeholde kvalitetsstandarder og redusere avfall.

Illustrasjonen nedenfor viser interaksjonen mellom Azure IoT Hub, IoT-intelligence og Supply Chain Management.

![IoT Hub, IoT-intelligens og Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Sporing og vedlikehold

- [Overvåkingsscenarioer i Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Deaktivere et scenario](iot-scenario-setup.md#disable-a-scenario)
- [Endre et kjørende scenario for IoT-intelligens](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simuleringsalternativer](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]