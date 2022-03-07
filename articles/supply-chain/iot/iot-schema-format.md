---
title: Skjemaformater for IoT Hub-meldinger
description: Dette emnet beskriver hvordan du bør utforme et meldingsskjema som du kan bruke i IoT-intelligens.
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecf4a70d69d24ea75f5448339057e7017cb93af
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652054"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Skjemaformater for IoT Hub-meldinger

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du bør utforme et meldingsskjema som du kan bruke i IoT-intelligens.

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