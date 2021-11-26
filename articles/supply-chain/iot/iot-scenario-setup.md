---
title: Scenariooppsett for IoT-intelligens
description: Dette emnet forklarer hvordan du konfigurerer scenarier for IoT-intelligens i Microsoft Dynamics 365 Supply Chain Management.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e8c65cebe64f86dcf158668e8a4f5600c158a1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782433"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Scenariooppsett for IoT-intelligens

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer scenarier for IoT-intelligens i Microsoft Dynamics 365 Supply Chain Management. Før du kan definere scenarioene, må du [konfigurere Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

I dette emnet skal du konfigurere **Nedetid for utstyr**, slik at et varsel genereres i Supply Chain Management når en maskin går ned. Emnet viser også hvordan du konfigurerer **Produktkvalitet**-scenarioet, slik at det genereres et varsel hvis et attributt for en vare er utenfor et bestemt område, og hvordan du konfigurerer **Produksjonsforsinkelser**-scenarioet, slik at det genereres et varsel hvis produksjonsgjennomstrømningen faller under en terskelverdi.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurere  Nedetid for utstyr i Supply Chain Management

**Nedetid for utstyr** tilordner et signal om **PartOut** til en maskinvarslingsterskel. Maskinen blir bare overvåket når den er valgt for scenarioet, og når den er satt til **Kjører** i Supply Chain Management. Hvis klokkeslettet da maskinen sist mottok signalet **PartOut**, er større enn varselterskelen, utløses varslingen **Maskin nede**. Hvis maskinen fortsatt kjører, utløses varslingen **Maskin oppe** når neste **PartOut**-signal mottas. Hvis en maskin forblir nede i 30 minutter, utløses en ny varsling av typen **Maskin nede**.

**Nedetid for utstyr** har følgende avhengigheter:

+ Et varsel kan bare utløses hvis en produksjonsordre kjører på en tilordnet maskin.
+ Et signal som representerer en tilordnet maskins **PartOut**-signal, må sendes til IoT-huben, og et unikt egenskapsnavn må inkluderes.
+ En UNIX **timestamp**-egenskap, der verdien angis i millisekunder (MS), må finnes i meldingen for Azure IoT-hub.

For å konfigurere gjør du følgende.

1. Logg på Supply Chain Management.
2. Aktiver funksjonsflagget for IoT-intelligens. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurer måleverdiene. Hvis du vil ha mer informasjon, kan du se [Konfigurere måleverdier](iot-metrics-setup.md#configure-metrics).
4. Gå til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenariobehandling**.
6. På flisen **Utstyr** velger du **Konfigurer** for å åpne konfigurasjonsveiviseren.

   Den første siden i veiviseren er siden **Definisjon av sensorskjema for utstyr**. På denne siden er målet å sette opp skjemaet i Supply Chain Management, slik at det samsvarer med JSON-formatet (JavaScript Object Notation) i IoT-hub-meldingene. Flere meldingsskjemaer kan defineres. Hvis du vil ha mer informasjon, kan du se [Skjemaformater for IoT-hub-meldinger](iot-schema-format.md). I dette eksemplet inneholder meldingslasten en gruppe meldinger som har følgende format.

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

7. Legg til en rad i tabellen, og angi følgende verdier:

    1. Sett **Skjemanavn**-feltet til **ID**.
    2. Sett feltet **Skjemabane** til **/payload\[\*\]/id**.
    3. Sett **Beskrivelse**-feltet til **Meldings-ID**.

8. Legg til en ny rad i tabellen, og angi følgende verdier:

    1. Sett **Skjemanavn**-feltet til **Tidsstempel**.
    2. Sett feltet **Skjemabane** til **/payload\[\*\]/timestamp**.
    3. Sett **Beskrivelse**-feltet til **Meldingstidsstempel**.

9. Legg til en ny rad i tabellen, og angi følgende verdier:

    1. Sett **Skjemanavn**-feltet til **Verdi**.
    2. Sett feltet **Skjemabane** til **/payload\[\*\]/value**.
    3. Sett **Beskrivelse**-feltet til **Meldingsverdi**.

    > [!NOTE]
    > Du trenger ikke å definere alle egenskapene i meldingen. Definer bare de egenskapene du trenger. I de foregående trinnene opprettet du ikke en rad for **Rottidsstempel**. Banen til **Rottidsstempel** vil være **/timestamp**.

10. Velg **Neste** for å gå til siden **Tilordning av sensorskjema for utstyr**.
11. I raden for **Ressurs-ID for utstyr** i feltet **Skjemanavn** velger du **ID**.
12. I raden for **UTC-tidspunkt** i feltet **Skjemanavn** velger du **Tidsstempel**.
13. I raden for **Delprodusert signal** i feltet **Skjemanavn** velger du **Verdi**.
14. Velg **Neste** for å gå til siden **Konfigurasjon av ressurs-ID for utstyr**.
15. Følg disse trinnene for å tilordne verdiene i IoT-hubenmeldingen til ressursene for Supply Chain Management:

    1. I tabellen **Signaldataverdier** legger du til en ny rad. I feltet **Verdi** angir du **IoTInt.Machine1225.PartOut**. Denne verdien kommer fra JSON **id**-egenskapen i IoT-hubmeldingen.
    2. Velg **Lagre**.
    3. I tabellen **Tilordning av forretningspost** velger du **Ny**. En standardverdi for feltet for **forretningsposttype** fylles ut automatisk, og du trenger ikke endre den.
    4. I feltet **Forretningspost** velger du maskinressursen for Supply Chain Management som signalverdien sendes fra.
    5. Velg **Lagre**.
    6. Gjenta disse trinnene for å legge til en ny tilordning av forretningspost for **Machine1226**. Du kan tilordne flere signaldataverdier til én post i Supply Chain Management.

16. Bruk kolonnen **Valgt** for å velge maskinene du vil behandle. Du trenger ikke definere alle signalverdiene, og du behøver ikke å velge alle maskiner.
17. Velg **Neste** for å gå til siden **Konfigurasjon av delprodusert signal**.
18. I tabellen **Signaldataverdier** legger du til en rad og setter **Verdi**-feltet til **Sann**. Denne verdien kommer fra JSON **value**-egenskapen i IoT-hubmeldingen. Du kan legge til så mange verdier du trenger i scenarioet.
19. Velg **Lagre**.
20. Velg **Neste** for å gå til siden **Terskal for nedetid for utstyr**. De oppførte maskinene er de som tidligere var tilordnet til signalverdier. På denne siden kan du definere en terskel for å fastslå om en maskin er nede. Hvis du for eksempel setter terskelen til **10**, genererer Supply Chain Management en varsling hvis det ikke mottas et **PartOut**-signal fra en maskin på 10 minutter.
21. Velg **Neste** for å gå til siden **Aktiver scenario**. Sett alternativet til å aktivere scenarioet.
22. Velg **Fullfør**.

Scenariooppsettet er nå fullført. IoT-intelligens starter behandlingen av IoT-hubmeldingene automatisk.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurere  Produktkvalitet i Supply Chain Management

 **Produktkvalitet** genererer en varsling hvis et attributt for en vare er utenfor et bestemt område. En sensor kan for eksempel sende vekten for hver vare til IoT-huben. Hvis et element er for tungt eller for lett, blir det generert en varsling i Supply Chain Management.

**Produktkvalitet**-scenarioet har følgende avhengigheter:

+ Et varsel utløses bare hvis en produksjonsordre kjører på en tilordnet maskin og produserer et produkt med et tilordnet partiattributt.
+ Et signal som representerer partiattributtet, må sendes til IoT-huben, og et unikt egenskapsnavn må inkluderes.
+ En UNIX **timestamp**-egenskap, der verdien angis i millisekunder, må finnes i meldingen for IoT Hub.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurere  Produksjonsforsinkelser i Supply Chain Management

**Produksjonsforsinkelser** genererer en varsling hvis produksjonsgjennomstrømningen faller under en terskelverdi. I dette scenarioet sendes det et **PartOut**-signal til IoT-hub for hver vare som produseres. I Supply Chain Management beregnes forsinkelsen på grunnlag av hvor lenge produksjonsordren er planlagt å kjøre, antall varer som skal produseres, hvor lenge jobben har vært aktiv, og antall **PartOut**-signaler som er mottatt. Det vil bli generert en forsinkelsesvarsling hvis antallet **PartOut**-signaler for jobben faller under terskelverdien.

**Produktforsinkelser**-scenarioet har følgende avhengigheter:

+ Et varsel kan bare utløses hvis en produksjonsordre kjører på en tilordnet maskin.
+ Et signal som representerer en tilordnet maskins **PartOut**-signal, må sendes til Azure IoT-huben, og et unikt egenskapsnavn må inkluderes.
+ En UNIX **timestamp**-egenskap, der verdien angis i millisekunder, må finnes i meldingen for IoT Hub.

## <a name="disable-a-scenario"></a>Deaktivere et scenario

Hvis du vil deaktivere et scenario, gjør du følgende.

1. I Supply Chain Management går du til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenariobehandling**.
2. Velg **Konfigurer** under flis for scenarioet.
3. Velg **Neste** for å gå til den siste veivisersiden.
4. Sett alternativet til å deaktivere scenarioet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]