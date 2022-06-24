---
title: Strategier for containerpakking
description: Denne artikkelen beskriver forskjellene mellom strategier for containerpakking og gir eksempler.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 46b4a007dafbd99e5f9b7231c07a148f8101d2a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862373"
---
# <a name="container-packing-strategies"></a>Strategier for containerpakking

[!include [banner](../includes/banner.md)]

En *containerpakkestrategi* er en strategi som du kan bruke til å definere varetilordninger på tvers av containere. Denne artikkelen forklarer forskjellene mellom strategiene *Pakk i alle åpne containere* og *Pakk bare i gjeldende container*.

- **Pakk inn i alle åpne containere** – Systemet må kontrollere alle åpne containere som allerede er opprettet i løpet av containerbruksyklusen, for å sikre at varen får plass i én av dem. Under pakkingen kontrollerer systemet hver vare for å bestemme om den får plass i en av containerne som ble opprettet tidligere. Hvis varen ikke passer i en eksisterende container, oppretter systemet en ny container og fortsetter til den er ferdig med å pakke hele ordren.

    For eksempel krever *n* bestilte varer containerbruk. Hver gang systemet behandler en vare som ikke passer inn i en eksisterende container, vil den gjøre totalt (\[(*n* – 1) × (*n* + 1)\] ÷ 2) kontroller for å evaluere om varen passer i de eksisterende containerne.

- **Pakk bare i gjeldende container** – Systemet må bare kontrollere containeren som ble opprettet sist, for å sørge for at varen passer i den. Under pakkingen kontrollerer systemet hver vare for å bestemme om den får plass i containeren som ble opprettet sist. Hvis varen ikke passer i containeren, oppretter systemet en ny container og fortsetter til den er ferdig med å pakke hele ordren.

    For eksempel krever *n* bestilte varer containerbruk. I verste fall vil systemet gjøre totalt (*n* – 1) kontroller for å evaluere om varen passer i containerne.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Eksempel på flyten for containerpakkestrategier

Du definerer følgende varer for containerbruk.

| Element | Fysiske dimensjoner (bredde × dybde × høyde) | Tykkelse |
|---|---|---|
| HDMI-kabel 6' | 1 × 1 × 1 | 1 |
| HDMI-kabel 12' | 2 × 1 × 1 | 1 |
| HDMI-kabel 18' | 3 × 1 × 1 | 2 |

Du angir også følgende boks som skal brukes til pakking.

| Container | Fysiske dimensjoner (lengde × bredde × høyde) | Tykkelse | Volum |
|---|---|---|---|
| Middels boks | 6 × 3 × 2 | 10 | 100 |

Til slutt definerer du en ordre som har følgende produkter og antall.

| Salgsordrelinje | Antall |
|---|---|
| HDMI-kabel 12' | 9 |
| HDMI-kabel 18' | 8 |
| HDMI-kabel 6' | 13 |

Tabellen nedenfor oppsummerer hvordan containerbruk fungerer når du bruker *Pakk i alle åpne containere*-strategien, og når du bruker *Pakk bare i gjeldende container*-strategien.

| Pakk inn i alle åpne containere | Pakk i gjeldende container |
|---|---|
| <p>HDMI-kabel 12':</p><ol><li>Opprett en ny container, CONT0001.</li><li>Sett 9 ea inn i containeren CONT0001.</li></ol> | <p>HDMI-kabel 12':</p><ol><li>Opprett en ny container, CONT0001.</li><li>Sett 9 ea inn i containeren CONT0001.</li></ol> |
| <p>HDMI-kabel 18':</p><ol><li>Kontroller om varen får plass i container CONT0001.</li><li>Opprett en ny container, CONT0002.</li><li>Sett 5 ea inn i containeren CONT0002.</li><li>Opprett en ny container, CONT0003.</li><li>Sett 3 ea inn i containeren CONT0003.</li></ol> | <p>HDMI-kabel 18':</p><ol><li>Kontroller om varen får plass i container CONT0001.</li><li>Opprett en ny container, CONT0002.</li><li>Sett 5 ea inn i containeren CONT0002.</li><li>Opprett en ny container, CONT0003.</li><li>Sett 3 ea inn i containeren CONT0003.</li></ol> |
| <p>HDMI-kabel 6':</p><ol><li>Kontroller om varen får plass i container CONT0001.</li><li>Sett 1 ea inn i containeren CONT0001.</li><li>Kontroller om varen får plass i container CONT0002.</li><li>Kontroller om varen får plass i container CONT0003.</li><li>Sett 4 ea inn i containeren CONT0003.</li><li>Opprett en ny container, CONT0004.</li><li>Sett 8 ea inn i containeren CONT0004.</li></ol> | <p>HDMI-kabel 6':</p><ol><li>Kontroller om varen får plass i container CONT0003.</li><li>Sett 4 ea inn i containeren CONT0003.</li><li>Opprett en ny container, CONT0004.</li><li>Sett 9 ea inn i containeren CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Eksempelscenario: Pakke enkeltordrer per container

Denne delen presenterer et scenario der systemet er konfigurert til å konsolidere flere ordrer til én forsendelse. Derfor blir containerbruken utført fra salgsordren for å sikre at hver ordre som inneholder flere produkter, blir pakket i sin egen container.

Ved hjelp av denne funksjonaliteten kan du håndtere scenarier der du bare må pakke én salgsordre inn i hver container, slik at distribusjonssenteret kan direkteoverføre fulle containere mellom butikker. I tillegg til detaljhandelsscenarier (ordre per detaljhandel og forsendelse til et distribusjonssenter for direkteoverføring) brukes også denne teknikken i lean/forsyningskjeder (salgsordre per just-in-time-produksjonslinje).

Dette scenariet viser hvordan du kan redusere antall containere som blir evaluert under pakking, ved å bruke *Pakk bare i gjeldende container*-strategi for containerbruk.

### <a name="prerequisites"></a>Forutsetninger

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Slå på funksjonen Konsolider forsendelser i systemet

Dette scenariet bruker funksjonen *Konsolider forsendelser*. Hvis funksjonen ikke allerede er tilgjengelig i systemet, må du aktivere den ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

Dette scenarioet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.

### <a name="inspect-or-create-container-types"></a>Kontrollere eller opprette containertyper

Følg denne fremgangsmåten for å kontrollere containertypene eller opprette nye containertyper etter behov.

1. Gå til **Warehouse Management** \> **Oppsett** \> **Containere** \> **Containertyper**.
1. Kontroller at hver av de følgende containertypene er tilgjengelige i demodataene. Rediger eller opprett containertyper etter behov.

    - Containertype 1:

        - **Containertypekode:** *Boks-Stor*
        - **Beskrivelse:** *Stor boks*
        - **Maksimal nettovekt:** *100*
        - **Volum:** *400*
        - **Lengde:** *4*
        - **Bredde:** *10*
        - **Høyde:** *10*

    - Containertype 2:

        - **Containertypekode:** *Boks-Medium*
        - **Beskrivelse:** *Middels boks*
        - **Maksimal nettovekt:** *50*
        - **Volum:** *200*
        - **Lengde:** *2*
        - **Bredde:** *10*
        - **Høyde:** *10*

    - Containertype 3:

        - **Containertypekode:** *Boks-Liten*
        - **Beskrivelse:** *Liten boks*
        - **Maksimal nettovekt:** *20*
        - **Volum:** *100*
        - **Lengde:** *1*
        - **Bredde:** *10*
        - **Høyde:** *10*

### <a name="inspect-or-create-container-groups"></a>Kontrollere eller opprette containergrupper

Følg denne fremgangsmåten for å kontrollere containergruppene eller opprette nye containergrupper etter behov.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containergrupper**.
1. Kontroller at følgende containergruppe er tilgjengelig i demodataene. Hvis den ikke er tilgjengelige, velger du **Ny** for å opprette den.

    - **Containergruppe-ID:** *Bokser*
    - **Beskrivelse:** *Boksstørrelser*

1. I hurtigkategorien **Detaljer** for *Bokser*-containergruppen kontrollerer du at følgende linjer finnes. Hvis de ikke finnes, velger du **Ny** for å legge dem til.

    - Linje 1:

        - **Sekvensnummer:** *1*
        - **Containertype:** *Boks-Stor*
        - **Containerutnyttelsesprosent:** *100*

    - Linje 2:

        - **Sekvensnummer:** *2*
        - **Containertype:** *Boks-Medium*
        - **Containerutnyttelsesprosent:** *100*

    - Linje 3:

        - **Sekvensnummer:** *3*
        - **Containertype:** *Boks-Liten*
        - **Containerutnyttelsesprosent:** *100*

### <a name="create-a-new-container-build-template"></a>Opprette en ny mal for containerversjon

Hvis du vil opprette en ny containerversjonsmal, følger du fremgangsmåten nedenfor.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Mal for build for container**.
1. Velg **Ny** for å opprette en containerversjonsmal med følgende innstillinger:

    - **Sekvensnummer:** *1*
    - **Containermal-ID:** *Boks*
    - **Containergruppe-ID:** *Bokser*
    - **Grunnleggende spørringstyper:** *Salgstildelingslinje*
    - **Bølgetrinnkode:** *234*
    - **Tillat oppdeling av plukking:** *Ja*
    - **Pakkestrategi for container:** *Pakk bare i gjeldende container*
    - **Pakk etter direktivenhet:** *Nei*

1. Mens raden for den nye malen fremdeles er valgt, velger du **Rediger spørring** i handlingsruten.
1. En standard dialogboks for Power Query-redigering vises. I kategorien **Sortering** velger du **Legg til** for å legge til en rad som har følgende innstillinger:

    - **Tabell:** *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
    - **Felt:** *Ordrenummer*
    - **Søkeretning:** *Stigende*

    > [!IMPORTANT]
    > For å unngå å måtte sjekke alle åpne containerne og for å gjøre prosessen raskere ved å kontrollere én container om gangen, bruker du strategien *Pakk bare i gjeldende container* i tillegg til å sortere etter ordrenummer. Denne kombinasjonen vil fungere som en arbeidspause i en arbeidsmal.

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. Mens raden for den nye malen fremdeles er valgt, velger du **Begrensninger for containerkombinasjoner** i handlingsruten.

    Nå legger du til en begrensning som setter varer fra en enkelt ordre inn i en enkelt container. Varer fra en hvilken som helst annen ordre blir plassert i en separat container.

1. Velg **Ny** for å opprette en kombinasjonsbegrensning med følgende innstillinger:

    - **Tabell:** *Salgsordrer*
    - **Velg felt:** *SalesId* (Feltet vil vises som *Salgsordre* i rutenettet.)

1. Velg **OK** for å legge til begrensningen.
1. Lukk siden.

### <a name="set-up-a-wave-template-for-containerization"></a>Definere en bølgemal for containerbruk

Hvis du vil konfigurere en bølgemal, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. I listeruten setter du **Bølgemaltype**-feltet til *Forsendelse*.
1. Velg **63 Containerbruk**-malen i listen.
1. I handlingsruten velger du **Rediger**.
1. På hurtigfanen **Metoder**, i kolonnen **Valgte metoder**, finner du følgende linje:

    - **Metodenavn:** *containerbruk*
    - **Navn:** *Containerbruk*

1. Sett feltet **Bølgetrinnkode** for linjen til *234*.

### <a name="set-up-a-work-template"></a>Konfigurere en arbeidsmal

Hvis du vil konfigurere en arbeidsmal, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Sett feltet **Arbeidsordretype** til *Salgsordrer*.
1. I rutenettet **Oversikt** finner og velger du arbeidsmalen som skal brukes for pakking av enkeltordrer per container. I dette scenarioet velger du malen **63 Plukk til container**.
1. I handlingsruten velger du **Rediger spørring**.
1. En standard dialogboks for Power Query-redigering vises. I kategorien **Sortering** legger du til følgende linjer:

    - Linje 1:

        - **Tabell:** *Midlertidige arbeidstransaksjoner*
        - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
        - **Felt:** *Leverings-ID*
        - **Søkeretning:** *Stigende*

    - Linje 2:

        - **Tabell:** *Midlertidige arbeidstransaksjoner*
        - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
        - **Felt:** *Ordrenummer*
        - **Søkeretning:** *Stigende*

    - Linje 3:

        - **Tabell:** *Midlertidige arbeidstransaksjoner*
        - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
        - **Felt:** *Container-ID*
        - **Søkeretning:** *Stigende*

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. Du får følgende melding: «Grupperingen blir tilbakeført – vil du fortsette?» Klikk på **Ja** for å fortsette.
1. Selv om malen **63 Plukk til container** er valgt, velger du **Arbeidshodeskift** i handlingsruten.

    Du bruker nå innstillinger til å bryte arbeidet, slik at hver container i ordren er koblet til én arbeidsordre.

1. Merk av for **Grupper etter dette feltet** for hver rad på siden **Arbeidshodeskift** (**Forsendelses-ID**, **Ordrenummer** og **Container-ID**).
1. Lukk siden.

### <a name="set-up-shipment-consolidation-policies"></a>Konfigurere policyer for forsendelseskonsolidering

Følg denne fremgangsmåten for å definere en policy for forsendelseskonsolidering.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. I listeruten setter du *Policytype* til **Salgsordrer**.
1. Velg **Standard** policy i listen.
1. I handlingsruten velger du **Rediger**.
1. I hurtigfanen **Konsolideringsfelt** i listen **Valgte felt** velger du raden der feltet **Feltnavn** er satt til *Ordrenummer*.
1. Velg **Fjern**-knappen ![venstre pil.](media/backward-button.png) for å flytte feltet til **Gjenværende felt**-listen.
1. Velg **Lagre** i handlingsruten.

### <a name="set-up-physical-dimensions-for-the-product"></a>Konfigurere fysiske dimensjoner for produktet

Følg denne fremgangsmåten for å definere fysiske dimensjoner for produktene som skal brukes i dette scenariet.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet der feltet **Varenummer** er satt til *A0001*.
1. I handlingsruten i fanen **Administrer lager** i gruppen **Lager** velger du **Fysiske dimensjoner**.
1. På siden **Fysiske dimensjoner** skal du se følgende linje i rutenettet:

    - **Enhet:** *stk*
    - **Bruttovekt:** *3,00*
    - **Bredde:** *2,00*
    - **Dybde:** *2,00*
    - **Høyde:** *4,00*
    - **Volum:** *16,00*

1. Lukk siden.
1. Velg produktet der feltet **Varenummer** er satt til *A0002*.
1. I handlingsruten i fanen **Administrer lager** i gruppen **Lager** velger du **Fysiske dimensjoner**.
1. På siden **Fysiske dimensjoner** skal du se følgende linje i rutenettet:

    - **Enhet:** *stk*
    - **Bruttovekt:** *4,00*
    - **Bredde:** *3,00*
    - **Dybde:** *1,00*
    - **Høyde:** *3,00*
    - **Volum:** *9,00*

### <a name="create-sales-order-1"></a>Opprett salgsordre 1

Følg fremgangsmåten nedenfor for å opprette en salgsordre.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. Det vises en dialogboks for oppretting av en ny salgsordre. Angi følgende verdier:

    - **Kundekonto:** *US-001*
    - **Lager:** *63*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Legg til følgende salgslinjer i hurtigfanen **Salgsordrelinjer**:

    - Linje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *2*

    - Linje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *2*

1. Velg den første linjen, og velg deretter **Lager \> Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti**. Lukk deretter siden.
1. Gjenta de to forrige trinnene for den andre linjen.
1. Lukk siden.

### <a name="create-sales-order-2"></a>Opprett salgsordre 2

Følg denne fremgangsmåten for å opprette en ny salgsordre.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. Det vises en dialogboks for oppretting av en ny salgsordre. Angi følgende verdier:

    - **Kundekonto:** *US-001*
    - **Lager:** *63*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Legg til følgende salgslinjer i hurtigfanen **Salgsordrelinjer**:

    - Linje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *4*

    - Linje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *4*

1. Velg den første linjen, og velg deretter **Lager \> Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti**. Lukk deretter siden.
1. Gjenta de to forrige trinnene for den andre linjen.
1. Lukk siden.

### <a name="create-the-load"></a>Opprette lasten

Følg disse trinnene for å opprette en last for hvert ordresett du har opprettet for dette , og deretter frigi det til lageret.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I fanen **Salgslinjer** finner og velger du alle salgsordrelinjene fra salgsordrene du opprettet for dette scenarioet.
1. I handlingsruten, på **Forsyning og behov**-fanen, i **Legg til**-gruppen, velg **Til ny last**. De valgte ordrelinjene legges til i en ny last.
1. I dialogboksen **Tilordning av lastmal** i feltet **Lastmal-ID** velger du en lastmal, for eksempel *40' Container*.
1. Velg **OK** for å lukke dialogboksen.
1. I delen **Laster** finner og velger du lasten du nettopp opprettet.
1. Velg **Frigivelse \> Frigi til lager**.
1. I dialogboksen **Frigi til lager** velger du **OK** for å frigi den valgte lasten til lageret.

### <a name="verify-the-shipments-and-containers"></a>Kontrollere forsendelsene og containerne

Ved hjelp av fremgangsmåten nedenfor kan du verifisere forsendelsene som er opprettet. Bruk det til å gå gjennom rekkefølgen du opprettet for dette scenariet, for å sikre at du har fått de forventede resultatene.

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Finn og velg forsendelsen som ble opprettet for belastningen som du akkurat har frigitt.
1. I handlingsruten, i kategorien **Transport**, velger du **Vis containere**.
1. Bekreft at varene fra salgsordrene ble containerbrukt i to ulike containere.

## <a name="additional-resources"></a>Tilleggsressurser

- [Containerbruk](wave-containerization.md)
