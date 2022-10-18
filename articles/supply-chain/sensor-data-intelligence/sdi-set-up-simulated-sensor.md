---
title: Konfigurer en simulert sensor for testing
description: Denne artikkelen beskriver hvordan du setter opp en simulator som du kan bruke til å teste sensordataintelligens uten å installere fysiske sensorer.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc8bd020a53214abab28ec51ffc6d6be74979932
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643983"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Konfigurer en simulert sensor for testing

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Hvis du vil teste sensordataintelligens uten å installere noen fysiske sendorer, kan du bruke tjenesten *Raspberry PI Azure IoT online-simulator* til å etterligne sensorsignaler og sende dem til IoT-løsningen din (Tingenes Internett) på Microsoft Azure. Hvis du vil ha mer informasjon om simulatoren, kan du se [Koble Raspberry Pi online-simulatoren til Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Videoinstruksjoner

Følgende video viser hvordan du konfigurerer en simulert sensor for testing. Resten av delene i denne artikkelen inneholder de samme instruksjonene i et tekstbasert format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Opprette en enhet i Azure IoT Hub

Først må du konfigurere en enhet for å godkjenne sensorsignalene til Azure IoT Hub.

1. I Azure går du til listen over ressurser for ressursgruppen du opprettet for bruk med sensordataintelligens. (Hvis du vil ha mer informasjon, kan du se [Distribuer en IoT-løsning på Azure](sdi-deploy-iot-solution-on-azure.md).)
1. I ressurslisten finner du posten der **Type**-feltet er satt til *IoT Hub*. I **Navn**-kolonnen velger du navnet for å åpne detaljsiden for ressursen.
1. Velg **Enheter** i navigasjonsruten til venstre.
1. På **Enheter**-siden velger du **Legg til enhet**.
1. På siden **Opprett en enhet** angir du følgende felter:

    - **Enhets-ID** – Angi et navn på den nye enheten (for eksempel *Min IoT-enhet*).
    - **Godkjenningstype** – Velg *Symmetriske nøkler*.
    - **Generer nøkler automatisk** – Merk av i denne boksen.
    - **Koble denne enheten til en IoT-hub** – Velg *Aktiver*.

1. Velg **Lagre** for å gå tilbake til **Enheter**-siden.
1. Finn den nye enheten i listen. I kolonnen **Enhets-ID**-kolonnen velger du navnet for å åpne detaljsiden for enheten. Hvis du ikke ser den nye enheten i listen, oppdaterer du siden.
1. Kopier verdien for **Primær tilkoblingsstreng** (for eksempel ved å klikke på knappen **Kopier til utklippstavlen**). Du trenger denne verdien senere når du setter opp Raspberry Pi IoT-simulatoren for å etterligne sensorsignaler. Vurder derfor å lime den inn i en tekstfil nå.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Legg til Azure-tilkoblingsstrengen i Raspberry Pi IoT-simulatoren

Følg denne fremgangsmåten for å legge til tilkoblingsstrengen fra enheten i Azure IoT Hub i skriptet i Raspberry -tjenesten.

1. Åpne [Raspberry Pi IoT-simulatoren for](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. I koderedigeringsruten finner du linjen som inneholder følgende kommando.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Erstatt hjelpeteksten, inkludert parentesene, med verdien for **Primær tilkoblingsstreng** du kopierte i den forrige delen. Resultatet skal ligne følgende eksempel.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Legg til ID-ene og verdiene for sensoren i nyttelasten i Raspberry PI IoT-simulatoren

Du må nå konfigurere Raspberry Pi IoT-simulatoren med simulerte sensorer og verdiene de skal sende som nyttelaster.

- I koderedigeringen i Raspberry Pi IoT-simulatoren finner du `getMessage`-funksjonen. Rediger den slik at den samsvarer med følgende kode. (Sensorene er definert på `cb()`-linjene.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Sensor-ID-ene som er definert i koderedigeringen for Raspberry PI IoT-simulatoren, må være identiske med sensor-ID-ene du skal angi senere for scenarioene i Supply Chain Management. Eksempelkoden over bruker sensor-ID-er som kan leses av mennesker. I et faktisk scenario vil imidlertid sensor-ID-ene være GUID-verdier (globalt unik identifikator) som leveres av sensorprodusenten. De lesbare sensor-ID-ene som brukes i denne eksempelkoden, brukes også i eksemplene i [scenarioet for produktkvalitet](sdi-scenario-product-quality.md), [scenarioet for vedlikehold av ressurser](sdi-scenario-asset-maintenance.md), [scenarioet for produksjonsforsinkelser](sdi-scenario-production-delays.md) og [maskinstatusscenarioet](sdi-scenario-equipment-downtime.md)). Bruk derfor denne koden hvis du vil gå gjennom disse scenarioene.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Rediger intervallet for sending av sensorsignaler

Du må nå angi intervallet som Raspberry Pi IoT-simulatoren skal følge for å sende de etterlignede sensorsignalene.

1. Finn følgende funksjonsaktivering i koderedigeringen i Raspberry Pi IoT-simulatoren.

    `setInterval(sendMessage, 2000);`

2. Som standard sender Raspberry Pi IoT-simulatoren et sensorsignal hver 2000. millisekund (hvert andre sekund). Du kan justere verdien etter behov.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Kjør Raspberry Pi IoT-simulatoren

- Velg **Kjør** for å starte simulatoren og begynne å sende simulerte sensordata.
