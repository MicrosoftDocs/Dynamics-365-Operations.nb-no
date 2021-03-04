---
title: Plukklinjegruppering
description: Dette emnet gir en oversikt over plukklinjegruppering.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434742"
---
# <a name="pick-line-grouping"></a>Plukklinjegruppering

[!include [banner](../includes/banner.md)]

I plukklinjegruppering kan flere arbeidslinjer som har samme vare og lokasjon, kombineres til én enkelt plukking som presenteres for brukeren på en mobilenhet. Derfor kan lagermedarbeidere motta de mest effektive instruksjonene som er mulige, men den nødvendige separasjon av arbeidslinjer i systemet opprettholdes også (for eksempel for ulike beholdere og ordrer).

## <a name="set-up-pick-line-grouping"></a>Definere plukklinjegruppering

### <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet

1. Gå til **Lagerstyrings \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**, og opprett et nytt menyelement som heter **Linjeplukking for salgsgruppe – brukerstyrt**.
2. Angi følgende verdier under **Menyelementer på mobilenheten**:

    - I **Menyelementnavn**-feltet angir du **Salgsplukking - gruppelinje**.
    - I **Tittel**-feltet angir du **Salgsplukking - gruppelinje**.
    - Velg **Arbeid** i feltet **Modus**.
    - Angi alternativet **Bruk eksisterende arbeid** til **Ja**.

3. I hurtigfanen **Generelt** kan du angir følgende verdier:

    - Velg **Brukerstyrt** i feltet **Styrt av**.
    - Sett alternativet **Generer nummerskilt** til **Ja**.
    - Sett alternativet **Gruppeplukking** til **Ja**.

4. I hurtigfanen **Arbeidsklasser** følger du denne fremgangsmåten for å konfigurere gyldige arbeidsklasser for menyelementet for mobilenheten:

    1. Velg **Ny**.
    2. I feltet **Arbeidsklasse-ID** velger du **Salg** eller **Salgsordreplukking**, avhengig av lageret du skal bruke.
    3. Velg **Salgsordrer** i feltet **Arbeidsordretype**.

### <a name="set-up-a-mobile-device-menu"></a>Definere en mobilenhetsmeny

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**. 
1. Legg til menyelementet du nettopp opprettet, i ønsket meny.

### <a name="set-up-a-work-template"></a>Konfigurere en arbeidsmal

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Finn arbeidsmalen som skal brukes med denne funksjonen. I dette eksemplet kan du velge standard Contoso-arbeidsmal **51 Plukk til trinn**.
1. Velg **Rediger spørring** på menyen.
1. Velg **Legg til** i kategorien **Sortering**, og angi deretter følgende verdier:

    - I **Tabell**-feltet velger du **Midlertidige arbeidstransaksjoner**.
    - I **Avledet tabell**-feltet velger du **Midlertidige arbeidstransaksjoner**.
    - Velg **Varenummer** i feltet **Felt**.
    - I feltet **Søkeretning** velger du **Stigende**.

> [!NOTE]
> For at grupperingsfunksjonaliteten for plukklinjen skal fungere, må arbeidslinjene sorteres etter vare-ID. Hvis linjer som har de samme elementene, ikke er i rekkefølge etter hverandre, grupperes de ikke.

## <a name="example"></a>Eksempel

### <a name="create-picking-work"></a>Opprett plukkarbeid

Før du kan definere plukklinjegruppering, må du opprette noe kvalifisert utgående arbeid.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
2. Velg **Ny** for å opprette en salgsordre. 
3. Velg en kunde i **Kundekonto**-feltet. 
4. På hurtigfanen **Generelt**, i **Lager**-feltet, velger du **51**. Velg deretter **OK**.
5. Legg til følgende seks linjer under **Salgsordrelinjer**:

    - **Linje 1:** I **Varenummer**-feltet velger du **M9200**. I feltet **Antall** angi **3**.
    - **Linje 2:** I **Varenummer**-feltet velger du **M9201**. I feltet **Antall** angi **3**. 
    - **Linje 3:** I **Varenummer**-feltet velger du **M9202**. I feltet **Antall** angi **2**. 
    - **Linje 4:** I **Varenummer**-feltet velger du **M9200**. I feltet **Antall** angi **1**. 
    - **Linje 5:** I **Varenummer**-feltet velger du **M9200**. I feltet **Antall** angi **3**.
    - **Linje 6:** I **Varenummer**-feltet velger du **M9202**. I feltet **Antall** angi **7**. 

    Her er et sammendrag av totalt antall for hver vare:

    - **Vare M9200:** 7 hver
    - **Vare M9201:** 3 hver
    - **Vare M9202:** 9 hver

6. Før du frigir ordrene til lageret, må du kontrollere at plukklokasjonene har nok beholdning for alle varene på alle ordrene. Se gjennom **Lokasjonsdirektiv**-innstillingen for å bestemme hvilke plukklokasjoner som skal brukes for plukking av salgsordre.
7. Reserver beholdningen, og frigi den til lageret. Det opprettes en arbeids-ID som har seks linjer. Linjene sorteres etter varenummer.

### <a name="run-the-mobile-device-flow"></a>Kjør flyten for mobilenhet

1. På mobilenheten velger du menyen som inneholder det nye menyelementet for mobilenhet.
1. Velg menyelementet **Salgsplukking – gruppelinje**, og start plukkingen.

    Når du har valgt menyen og angitt arbeids-ID, ser du plukktrinnet der alle plukklinjene for vare M9200 er gruppert. Du får en instruksjon om å plukke 7 hver av vare M9200.

1. Bekreft plukktrinnet. 
1. Gå til klientskjermen for arbeidet som pågår, og legg merke til at alle tre plukklinjer for vare M9200 ble lukket samtidig.

    Arbeidslinje 4 presenteres.

1. Bekreft plukktrinnet.

    Det siste plukktrinnet på mobilenheten samler de to siste plukklinjene fra arbeidsordren.

1. Fullfør plukktrinnet for 9 hver av vare M9202.
1. Bekreft plasseringstrinnet og eventuelle ekstra plukkings-/plasseringspar for å fullføre arbeidet.

> [!NOTE]
> - Arbeidslinjer kan bare grupperes hvis de er i rekkefølge.
> - Følgende funksjonalitet støttes ikke:
>
>    - Faktisk vekt-varer. Hvis det er noen faktisk vekt-varer på arbeidet, får du en feilmelding før du begynner å plukke.
>    - Stykkplukking.
>    - Arbeidslinjer som har uferdig etterfyllingsarbeid.
>    - Overplukking.
>    - Ny tildeling av vare for plukking med mangler


[!INCLUDE[footer-include](../../includes/footer-banner.md)]