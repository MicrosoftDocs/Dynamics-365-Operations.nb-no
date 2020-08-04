---
title: Scenariooppsett for IoT-intelligens
description: Dette emnet beskriver hvordan du konfigurerer et scenario i Supply Chain Management for IoT-intelligens.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597174"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Scenariooppsett for IoT-intelligens

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer et scenario i Supply Chain Management for IoT-intelligens. Før du kan sette opp scenarioene, må du [konfigurere LCS](iot-lcs-setup.md).

I dette emnet skal du konfigurere  **Nedetid for utstyr** til å generere et varsel i Supply Chain Management når en maskin går ned.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurere  **Nedetid for utstyr** i Supply Chain Management

 **Nedetid for utstyr** tilordner et signal om at en del er ute til en maskinvarslingsterskel. Maskinen blir bare overvåket når den er valgt for  og er satt til å kjøre i Supply Chain Management. Hvis klokkeslettet da maskinen sist mottok signalet om del som er ute, er større enn varselterskelen, utløses varslingen **Maskin nede**. Hvis manskinen fortsatt kjører når neste **PartOut**-signal mottas, utløses varslingen **Maskin oppe**. Hvis en maskin forblir nede i 30 min, utløses en ny varsling av typen **Maskin nede**.

 **Nedetid for utstyr** har følgende avhengigheter:

+ En produksjonsordre må kjøre på en tilordnet maskin for at et varsel skal kunne utløses.
+ Et signal som representerer en tilordnet maskins signal for del ute, må sendes til IoT-huben med et unikt egenskapsnavn.
+ En egenskap for millisekundstidsstempel for Unix må finnes i IoT-hubmeldingen.

Hvis du vil konfigurere , gjør du følgende:

1. Logg på Supply Chain Management.
2. Aktiver funksjonsflagget for IoT-intelligens. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurer måleverdiene. Hvis du vil ha mer informasjon, kan du se [Konfigurere måleverdier](iot-metrics-setup.md#configure-metrics).
4. Gå til **Produksjonskontroll**.
5. Gå til **Konfigurer \> IoT-Intelligence \> Scenariobehandling**.
6. Klikk **Konfigurer** i flisen **Nedetid for utstyr**. Konfigurasjonsveiviseren starter med siden **Definisjon av sensorskjema for utstyr**. Målet her er å konfigurere skjemaet i Supply Chain Management slik at det samsvarer med JSON-formatet til IoT-meldingene. Flere meldingsskjemaer kan defineres. Hvis du vil ha mer informasjon, kan du se [Meldingsskjemaformater for IoT-hub](iot-schema-format.md). I dette eksemplet inneholder meldingslasten en gruppe meldinger med dette formatet:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Legg til en rad i tabellen.

    1. Sett **Skjemanavn** til **ID**.
    2. Sett **Skjemabane** til **/payload[\*]/id**.
    3. Sett **Beskrivelse** til **Meldings-ID**.

8. Legg til en rad i tabellen.

    1. Sett **Skjemanavn** til **Tidsstempel**.
    2. Sett **Skjemabane** til **/payload[\*]/timestamp**.
    3. Sett **Beskrivelse** til **Meldingstidsstempel**.

9. Legg til en rad i tabellen.

    1. Sett **Skjemanavn** til **Verdi**.
    2. Sett **Skjemabane** til **/payload[\*]/value**.
    3. Sett **Beskrivelse** til **Meldingsverdi**.

    Du trenger ikke å definere alle egenskapene i meldingen, men bare de du trenger. I dette eksemplet har du ikke opprettet en rad for **Rottidsstempel**. Banen til **Rottidsstempel** vil være **/timestamp**.
  
10. Klikk **Neste** for å gå til siden **Tilordning av sensorskjema for utstyr**.
11. I raden for **Ressurs-ID for utstyr** setter du **Skjemanavn** til **ID**. De gyldige verdiene vises i en rullegardintabell.
12. I raden for **UTC-tidspunkt** setter du **Skjemanavn** til **Tidsstempel**. De gyldige verdiene vises i en rullegardintabell.
13. I raden for **Delprodusert signal** setter du **Skjemanavn** til **Verdi**. De gyldige verdiene vises i en rullegardintabell.
14. Klikk **Neste** for siden **Konfigurasjon av ressurs-ID for utstyr**.
15. I dette trinnet tilordner du meldingsverdiene for IoT-huben til ressursene for Supply Chain Management.

    1. I tabellen **Signaldataverdier** legger du til en ny rad og angir **IoTInt.Machine1225.PartOut** i kolonnen **Verdi**. Verdien **IoTInt.Machine1225.PartOut** kommer fra egenskapen JSON **id** i IoT-hubmeldingen.
    2. Klikk **Lagre**.
    3. I tabellen **Tilordning av forretningspost** klikker du **Ny**. Standardverdien for **typen forretningspost** fylles ut automatisk, og du trenger ikke endre den.
    4. I kolonnen **Forretningspost** velger du maskinressursen for Supple Chain Management som denne signalverdien sendes fra.
    5. Klikk **Lagre**.
    6. Gjenta disse trinnene ved å legge til en ny tilordning av forretningspost for **Machine1226**. Du kan tilordne flere signaldataverdier til én post i Supply Chain Management.

16. Bruk kolonnen **Valgte** til å velge hvilke maskiner du vil behandle. Du trenger ikke definere alle signalverdiene, og du behøver ikke å velge alle maskiner.
17. Klikk **Neste** for å gå til siden **Konfigurasjon av delprodusert signal**.
18. I tabellen **Signaldataverdier** legger du til en rad og setter **Verdi** til **Sann**. Verdien **Sann** kommer fra egenskapen JSON **value** i IoT-hubmeldingen. Du kan legge til så mange verdier du trenger i .
19. Klikk **Lagre**.
20. Klikk **Neste** for å gå til siden **Terskal for nedetid for utstyr**. De oppførte maskinene er de som tidligere var tilordnet til signalverdier. I dette trinnet definerer du en terskel for å fastslå om en maskin er nede. Hvis du for eksempel setter terskelen til 10, genererer Supply Chain Management en varsling hvis det ikke vises en melding om en del ute fra en maskin på 10 minutter.
21. Klikk **Neste** for å gå til siden **Aktiver scenario**. Aktiver/deaktiver glidebryteren for å aktivere .
22. Klikk **Fullfør**.

Scenariooppsettet er fullført. IoT-intelligens starter behandlingen av IoT-hubmeldingene automatisk.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurere  **Produktkvalitet** i Supply Chain Management

 **Produktkvalitet** genererer en varsling hvis et attributt for en vare er utenfor et bestemt område. En sensor kan for eksempel sende vekten for hver vare til IoT-huben. I Supply Chain Management blir det generert en varsling hvis varen er for tung eller for lett.

 har disse avhengighetene:

+ En produksjonsordre må kjøre på en tilordnet maskin og produsere et produkt med et tilordnet partiattributt for at et varsel skal kunne utløses.
+ Et signal som representerer partiattributtet, må sendes til IoT-huben med et unikt egenskapsnavn.
+ En egenskap for millisekundstidsstempel for Unix må finnes i IoT-hubmeldingen.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurere  **Produksjonsforsinkelser** i Supply Chain Management

 **Produksjonsforsinkelser** genererer en varsling hvis produksjonsgjennomstrømningen faller under en terskelverdi. I dette scenarioet sendes det et **PartOut**-signal til IoT-hub for hver vare som produseres. I Supply Chain Management beregnes ordreforsinkelsen på grunnlag av hvor lenge produksjonsordren er planlagt å kjøres, hvor mange varer som skal produseres, hvor lenge jobben har kjørt og hvor mange **PartOuts**-signaler som mottas. Det vil bli generert en forsinkelsesvarsling hvis antallet **PartOuts**-signaler for jobben faller under terskelverdien for den forventede verdien.

 har disse avhengighetene:

+ En produksjonsordre må kjøre på en tilordnet maskin for at et varsel skal kunne utløses.
+ Et signal som representerer en tilordnet maskins signal for del ute, må sendes til IoT-huben med et unikt egenskapsnavn.
+ En egenskap for millisekundstidsstempel for Unix må finnes i IoT-hubmeldingen.

## <a name="how-to-disable-a-scenario"></a>Deaktivere et scenario

Hvis du vil deaktivere et scenario, gjør du følgende:

1. I Supply Chain Management går du til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenariobehandling**.
2. Klikk **Konfigurer** i .
3. Klikk **Neste** for å gå til den siste veiviserkategorien.
4. Veksle glidebryteren for å deaktivere .
