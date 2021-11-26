---
title: Startside for IoT-intelligens
description: Dette emnet inneholder koblinger til informasjon om IoT-intelligence.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782687"
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

+ **Produksjonsforsinkelser** – Dette scenariet sammenligner faktisk syklustid med planlagt syklustid. Supply Chain Management varsler deg når produksjon ikke er planlagt, slik at du kan gripe inn for å maksimere driftseffektivitet og unngå forsinkelser i ordren.
+ **Nedtid på utstyr** – Dette scenariet sammenligner målt oppetid med brukerdefinerte parametere. Supply Chain Management varsler deg når en avbruddsterskel blir overskredet, slik at du kan utføre handlinger, for eksempel planlegge en produksjonsordre på nytt eller opprette en vedlikeholdsarbeidsordre.
+ **Produktkvalitet** – Dette scenariet sammenligner sensoravlesninger, for eksempel fuktighet og temperatur, med brukerdefinerte kvalitetsmetrikk. Supply Chain Management varsler deg når det oppstår et avvik, slik at du kan gripe inn for å vedlikeholde kvalitetsstandarder og redusere avfall.

Illustrasjonen nedenfor viser interaksjonen mellom Azure IoT Hub, IoT-intelligence og Supply Chain Management.

![IoT Hub, IoT-intelligens og Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Installasjon

Du kan sette opp og konfigurere IoT-intelligens uten å skrive noen kode. Her er de grunnleggende trinnene.

1. [Konfigurer Azure-ressurser](iot-azure-setup.md) – Opprett en IoT Hub, en Redis Cache og en Key Vault som du kan få tilgang til fra Supply Chain Management.
2. [Meldingsskjemaformater for IoT Hub](iot-schema-format.md) – Konfigurer enhetene til å sende meldinger til IoT Hub, og definer JSON-meldingsformatet (JavaScript Object Notation).
3. Aktiver IoT-intelligens-funksjonsflagget i Funksjonsadministrasjon. 
4. [Installer IoT-intelligens-tillegget i Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Installer tillegget i LCS, og konfigurer Azure-hemmeligheter.
5. [Definere metrikk](iot-metrics-setup.md) – Definer mål i Supply Chain Management.
6. [Scenariooppsett](iot-scenario-setup.md) – Sett opp scenariene i Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Sporing og vedlikehold

+ [Overvåkingsscenarioer i Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Deaktivere et scenario](iot-scenario-setup.md#disable-a-scenario)
+ [Avinstallere tillegget](iot-lcs-setup.md#uninstall-addin)
+ [Endre et kjørende scenario for IoT-intelligens](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simuleringsalternativer](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]