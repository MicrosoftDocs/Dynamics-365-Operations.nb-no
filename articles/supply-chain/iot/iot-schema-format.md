---
title: Skjemaformater for IoT Hub-meldinger
description: Denne artikkelen beskriver hvordan du bør utforme et meldingsskjema som du kan bruke i IoT-intelligens.
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
ms.openlocfilehash: 705a2150042f9b65f1f4528d6f2699f7306996f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887464"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Skjemaformater for IoT Hub-meldinger

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du bør utforme et meldingsskjema som du kan bruke i IoT-intelligens.

## <a name="message-requirements"></a>Meldingskrav

Følgende regler gjelder for overvåking av meldinger i IoT-intelligens:

+ Meldingsskjemaer må være i JSON-format (JavaScript Object Notation).
+ En UNIX **timestamp**-egenskap, der verdien angis i millisekunder (ms), må finnes i meldingen for Microsoft Azure IoT-hub.
+ En melding spores bare hvis den inneholder alle egenskapene som er definert i scenariooppsettet. Hvis du for eksempel definerer egenskapene **id**, **tidsstempel** og **verdi**, overvåkes følgende melding.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Denne meldingsikonet overvåkes ikke, fordi **verdi**-egenskapen mangler.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT-intelligens ignorerer egenskaper i meldingen som ikke er definert i scenariokonfigurasjonen. Hvis du for eksempel definerer egenskapene **id**, **tidsstempel** og **verdi**, vil IoT-intelligens overvåke alle følgende meldinger.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT-intelligens ignorerer stille meldinger som ikke samsvarer med konfigurasjonskriteriene for scenarier.
+ Du kan definere og bruke flere typer meldingsskjemaer.
+ Ikke alle typer meldingsskjemaer må defineres. Bare skjemaer som skal brukes for IoT-intelligensscenariene, må defineres.

## <a name="id-value-pair-schema"></a>Skjema for ID-verdipar

Et ID-verdipar er et felles mønster for meldingsskjemaer for IoT-intelligens. Ved å bruke et ID-verdipar, sikrer du at meldingsskjemaet er det samme i alle scenariene. Her er for eksempel en melding for **Nedetid for utstyr** eller **Produksjonsforsinkelser**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Her er en melding for **Produktkvalitet**-scenarioet.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Begge de forrige meldingene inneholder **id**- og **verdi**-egenskaper. **ID**-verdiene kan tilordnes i tabellen **Signaldataverdier** under scenariooppsett. For scenarioet **Nedetid for utstyr** tilordner du verdien **IoTInt.Machine1225.PartOut**. For scenarioet **Produktkvalitet** tilordner du verdien **IoTInt.Machine1225.Temperature**.

Hvis du vil ha mer informasjon, kan du se i [Azure IoT Hub-dokumentasjon](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]