---
title: Scenario for nedetid for ressurser
description: Denne artikkelen beskriver scenarioet for nedetid for ressurser, som lar deg bruke sensordata for å overvåke tilgjengeligheten av ressursene dine.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689436"
---
# <a name="the-asset-downtime-scenario"></a>Scenario for nedetid for ressurser

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Scenarioet for nedetid for ressurser genererer en post for vedlikeholdsnedetid hvis det ikke mottas noe signal fra en maskin innenfor en definert tidsterskel siden det forrige signalet ble mottatt. Scenarioet krever at du monterer en sensor på maskinen som regelmessig sender et signal til Azure IoT Hub når maskinen er i drift, men som ikke sender et signal når maskinen ikke er i drift.

## <a name="set-up-the-asset-downtime-scenario"></a>Sett opp scenarioet for nedetid for ressurser

Følg disse trinnene for å sette opp scenarioet for *nedetid for ressurser* i Supply Chain Management.

1. Gå til **Aktivastyring \> Oppsett \> Sensordataintelligens \> Scenarioer** for å åpne **Scenarioer**-siden.
2. I scenarioboksen **Nedetid for ressurser** velger du **Konfigurer** for å åpne installasjonsveiseren for dette scenarioet.
3. På **Sensorer**-siden velger du **Ny** for å legge til en sensor i rutenettet. Angi deretter følgende felter for den:

    - **Sensor-ID** – Angi ID-en til sensoren du bruker. (Hvis du bruker Raspberry PI Azure IoT online-simulator og har konfigurert den som beskrevet i [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md), angir du *AssetDownTime*.)
    - **Sensorbeskrivelse** – Angi en beskrivelse av sensoren.

4. Gjenta det forrige trinnet for hver ekstra sensor du vil legge til nå. Du kan gå tilbake og legge til flere sensorer når som helst.
5. Velg **Neste**.
6. Velg posten for én av sensorene du nettopp la til, på siden **Tilordning av forretningsoppføring**, i delen **Sensorer**.
7. I delen **Tilordning av forretningsoppføring** velger du **Ny** for å legge til en rad i rutenettet.
8. I den nye raden angir du feltet **Forretningsoppføring** til ressursen du bruker den valgte sensoren til å overvåke. (Hvis du bruker demodataene, velger du *AK-101, Air Knife for Line 1*.)
9. Velg **Neste**.
10. På siden **Terskel for ressursnedetid** definerer du hvor lenge systemet skal vente før systemet skal sende en varsling om nedetid for ressurser. Terskelen kan defineres på to måter:

    - **Standardterskel (minutter)** – Angi dette feltet for å definere standardterskelen. Denne verdien gjelder for alle ressurser der feltet **Varslingsterskel (minutter)** er satt til to minutter eller mindre. Minimumsverdien er *2* (minutter).
    - **Terskel for å fastslå at maskinen ikke svarer (i minutter)** – For hver ressurs i rutenettet som du ikke vil bruke standardterskelen for, angir du en overstyringsverdi i dette feltet. Ressurser som er satt til å bruke en terskel på to minutter eller mindre, bruker i stedet innstillingen **Standardterskel (minutter)**.
11. Velg **Neste**.
12. I rutenettet på siden **Aktiver sensorer** velger du sensoren du har konfigurert, og velger deretter **Aktiver**. For hver aktiverte kontakt i rutenettet vises det en hake i **Aktiv**-kolonnen.
13. Velg **Fullfør**.

## <a name="work-with-the-asset-downtime-scenario"></a>Arbeid med scenarioet for nedetid for ressurser

Hvis det ikke mottas noe sensorsignal fra en ressurs innenfor terskelen som er definert i scenariokonfigurasjonen, vil systemet opprette en post for vedlikeholdsnedtid for denne ressursen. Arbeidsledere må gå gjennom nedetidspostene regelmessig (for eksempel én gang i løpet av hvert arbeidsskift) og bruke riktige årsakskoder og sluttidspunkt for hver nedetidregistrering. Følg denne fremgangsmåten for å vise postene for vedlikeholdsnedetid for en ressurs:

1. Gå til **Aktivastyring > Aktiva > Alle aktiva**.
2. Finn og velg ressursen du vil undersøke. (Hvis du bruker med demodataene, velger du *AK-101*.)
3. Gå til handlingsruten, åpne **Ressurs**-fanen, gå til **Arbeidsordre**-gruppen, og velg **Vedlikeholdsnedetid** for å åpne siden med poster om vedlikeholdsnedetid for den valgte ressursen.
