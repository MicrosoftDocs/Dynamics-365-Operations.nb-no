---
title: Plukklinjegruppering
description: Dette emnet gir en oversikt over plukklinjegruppering.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828279"
---
# <a name="pick-line-grouping"></a>Plukklinjegruppering

[!include [banner](../includes/banner.md)]

Plukklinjegruppering gjør at flere arbeidslinjer som har samme vare og lokasjon, kan kombineres til én plukking som presenteres for brukeren på mobilenheten. Derfor kan lagermedarbeidere motta så effektive instruksjoner som mulig, men den nødvendige separasjonen av arbeidslinjer (for ulike beholdere, ordrer og så videre) kan fortsatt opprettholdes i systemet.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Aktivere funksjonen for plukklinjegruppering

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonen og aktivere den om nødvendig. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Plukklinjegruppering*

## <a name="set-up-pick-line-grouping"></a>Definere plukklinjegruppering

### <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I feltet **Menyelementnavn** angir du *Linjeplukking for salgsgruppe*.
1. I **Tittel**-feltet angir du *Linjeplukking for salgsgruppe*. Denne tittelen vises på menyen på mobilenheten.
1. Velg *Arbeid* i feltet **Modus**.
1. Angi alternativet **Bruk eksisterende arbeid** til *Ja*.
1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - Velg **Brukerstyrt** i feltet *Styrt av*.
    - Sett alternativet **Generer nummerskilt** til *Ja*.
    - Sett alternativet **Gruppeplukking** til *Ja*.
    - Godta standardverdiene for de resterende alternativene.

1. Følg denne fremgangsmåten for å konfigurere gyldige arbeidsklasser for menyelementet på mobilenheten:

    1. Velg **Ny** i hurtigfanen **Arbeidsklasser**.
    2. I feltet **Arbeidsklasse-ID** kan du velge *Salg* eller *Salgsordreplukking*, avhengig av lageret du skal bruke. I dette scenarioet velger du *Salgsordreplukking*.

        Feltet **Arbeidsordretype** settes automatisk til *Salgsordrer*.

### <a name="set-up-a-mobile-device-menu"></a>Definere en mobilenhetsmeny

Følg denne fremgangsmåten for å legge til menyelementet du nettopp opprettet, på **Utgående**-menyen.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. I handlingsruten velger du **Rediger**.
1. Listeruten viser alle eksisterende menyer på mobilenheten. Velg *Utgående* i listen.
1. I listen **Tilgjengelige menyer og menyelementer** finner og velger du menyelementet *Linjeplukking for salgsgruppe* du nettopp opprettet.
1. Velg høyre pil for å flytte menyelementet *Linjeplukking for salgsgruppe* til **Menystruktur**-listen.
1. Bruk pil opp og pil ned til å flytte menyelementet til ønsket plassering i menystrukturen.
1. Velg **Lagre** i handlingsruten.

### <a name="set-up-a-work-template"></a>Konfigurere en arbeidsmal

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Velg *Salgsordrer* i feltet **Arbeidsordretype**.
1. I rutenettet **Oversikt** finner og velger du arbeidsmalen som skal brukes med denne funksjonen. I dette scenarioet velger du malen *51 Plukk til trinn*.
1. I handlingsruten velger du **Rediger spørring**.
1. I **Sortering**-fanen i dialogboksen for redigeringsprogram for spørring velger du **Legg til**, og deretter angir du følgende verdier for den nye raden:

    - I **Tabell**-kolonnen velger du *Midlertidige arbeidstransaksjoner*.
    - I **Avledet tabell**-kolonnen velger du *Midlertidige arbeidstransaksjoner*.
    - Velg *Varenummer* i **Felt**-kolonnen.
    - I kolonnen **Søkeretning** velger du *Stigende*.

1. Velg **OK** for å lukke dialogboksen og lagre valget ditt.
1. Du får følgende melding: «Grupperingen blir tilbakeført – vil du fortsette?» Klikk på **Ja** for å fortsette.

> [!IMPORTANT]
> For at grupperingsfunksjonaliteten for plukklinjen skal fungere, må arbeidslinjene sorteres etter vare-ID. Hvis linjer som har de samme elementene, ikke er i rekkefølge etter hverandre, grupperes de ikke.

## <a name="example"></a>Eksempel

### <a name="create-picking-work"></a>Opprett plukkarbeid

Før du kan definere plukklinjegruppering, må du opprette noe kvalifisert utgående arbeid.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. Velg *US-004* i **Kundekonto**-feltet.
1. På hurtigfanen **Generelt**, i **Lager**-feltet, velger du *51*.
1. Velg **OK**.
1. Legg til følgende seks linjer i hurtigfanen **Salgsordrelinjer**:

    - **Linje 1:** I **Varenummer**-feltet velger du *M9200*. I feltet **Antall** angi *3*.
    - **Linje 2:** I **Varenummer**-feltet velger du *M9201*. I feltet **Antall** angi *3*.
    - **Linje 3:** I **Varenummer**-feltet velger du *M9202*. I feltet **Antall** angi *2*.
    - **Linje 4:** I **Varenummer**-feltet velger du *M9200*. I feltet **Antall** angi *1*.
    - **Linje 5:** I **Varenummer**-feltet velger du *M9200*. I feltet **Antall** angi *3*.
    - **Linje 6:** I **Varenummer**-feltet velger du *M9202*. I feltet **Antall** angi *7*.

    Her er et sammendrag av totalt antall for hver vare:

    - **Vare M9200:** *7* hver
    - **Vare M9201:** *3* hver
    - **Vare M9202:** *9* hver

1. Før du frigir ordrene til lageret, må du kontrollere at plukklokasjonene har nok beholdning for alle varene på alle ordrene. Se gjennom **Lokasjonsdirektiv**-innstillingen for å bestemme hvilke plukklokasjoner som skal brukes for plukking av salgsordre. Hvis du bruker demonstrasjonsdatamiljøet Contoso for lager *51*, bekrefter du at det finnes tilgjengelig beholdning.

    Du må nå reservere beholdningen for hver linje.

1. I hurtigfanen **Salgsordrelinjer** velger du en av linjene som må reserveres.
1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. I handlingsruten på **Reservasjon**-siden velger du **Reserver parti** for å gjøre reservasjonen gjeldende. Lukk deretter siden.
1. Gjenta trinn 8 til og med 10 for de gjenstående linjene som må reserveres.

    Du må nå frigi salgsordren til lageret.

1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Du får en melding om at det er opprettet en forsendelse og en bølge, og at bølgen er sendt for å bli kjørt i en bunke.

    Når bølgen og alle nedstrøms jobber er fullført, opprettes en arbeids-ID for arbeid som har seks linjer. Linjene sorteres etter varenummer.

1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid** for å vise arbeidet som ble opprettet. Noter verdien for **Arbeids-ID**, fordi du kommer til å få behov for den i neste fremgangsmåte.

### <a name="initiate-picking-from-the-mobile-device"></a>Starte plukking fra mobilenheten

1. Logg på mobilenheten som en bruker som er aktivert for lager *51*.
1. På mobilenheten velger du menyen som inneholder det nye menyelementet for mobilenhet. I dette scenarioet velger du **Utgående**.
1. Velg menyelementet **Linjeplukking for salgsgruppe** for å starte plukkingen.
1. Angi **Arbeids-ID**-verdien du noterte i forrige fremgangsmåte.

    Du skal se et plukktrinn der alle plukklinjer for varen *M9200* er gruppert, og du skal få en instruks om å plukke *7* hver av varen *M9200*.

    > [!IMPORTANT]
    > På mobilenheten er plukkarbeidet for de tre plukkarbeidslinjene samlet i ett plukktrinn for brukeren.

1. Bekreft plukktrinnet.
1. Gå til arbeidssiden for arbeids-ID-en, og legg merke til at alle tre plukklinjer for varen *M9200* ble lukket samtidig.
1. Gå tilbake til mobilenheten, og fortsett å plukke. Arbeidslinje 4 for vare *M9201* skal vises. Siden det bare var én arbeidslinje i ordren, er det ingenting å samle.
1. Bekreft plukktrinnet.
1. Det siste plukktrinnet på mobilenheten samler de to siste plukklinjene fra arbeidsordren.
1. Fullfør plukktrinnet for *9* hver av varen *M9202*.
1. Bekreft plasseringstrinnet og eventuelle ekstra plukkings-/plasseringspar for å fullføre arbeidet.

> [!IMPORTANT]
>
> - Arbeidslinjer kan bare grupperes hvis de er i rekkefølge.
> - Følgende funksjonalitet støttes ikke:
>
>   - Faktisk vekt-varer
>
>    Hvis det er noen faktisk vekt-varer på arbeidet, får du en feilmelding før du begynner å plukke.
>
>   - Stykkplukking
>   - Arbeidslinjer som har uferdig etterfyllingsarbeid
>   - Overplukking
>   - Ny tildeling av vare for plukking med mangler


[!INCLUDE[footer-include](../../includes/footer-banner.md)]