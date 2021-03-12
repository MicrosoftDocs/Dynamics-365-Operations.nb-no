---
title: Utgående sortering
description: Dette emnet inneholder informasjon om utgående sortering. Denne funksjonaliteten gjør det enklere å håndtere små containere og hjelper lagerarbeidere å planlegge og organisere pallkapasitet på lastebilen.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963416"
---
# <a name="outbound-sorting"></a>Utgående sortering

[!include [banner](../includes/banner.md)]

Denne funksjonaliteten gjør det enklere å håndtere små containere og hjelper lagerarbeidere å planlegge og organisere pallkapasitet på lastebilen. Når du bruker utgående sortering, kan du sortere pakkede containere til riktig pall etter at de har vært på en pakkestasjon. Du kan også bygge et emballasjehierarki.

Med denne funksjonaliteten kan du bygge paller fra containere som er pakket gjennom pakkefunksjonaliteten. Containeren sendes ikke til den endelige forsendelseslokasjonen, fordi den er i den opprinnelige pakkeflyten. I stedet kan arbeidere lukke containeren og flytte den til en sorteringstypeplassering. De kan deretter sortere containere til plasseringer, der hver har et nummerskilt (LP). Når containerne er sortert, kan det opprettes arbeid for å sende hele nummerskiltet til endelig forsendelsessone eller endelige stadielokasjoner basert på lokasjonsdirektiver eller dine egne behov. I tillegg kan handlingen med å lukke sorteringsposisjonen umiddelbart flytte lageret til den endelige forsendelseslokasjonen og plukke den til ordren.

## <a name="turn-on-the-outbound-sorting-feature"></a>Aktivere Utgående sortering-funksjonen

Før du kan bruke funksjonen må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Utgående sortering*

## <a name="setup"></a>Installasjon

I dette scenariet må du bruke standard **USMF**-demodata og lager *62*. Du må også fullføre oppsettet som er beskrevet i følgende underdeler.

### <a name="set-up-a-wave-template"></a>Definere en bølgemal

Dette oppsettet behandler automatisk bølgen og oppretter arbeid når en linje frigis til lageret.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. I mallisten velger du **Lager 62**.
1. I hurtigfanen **Generelt** kontrollerer du at alternativet **Behandle bølge ved frigivelse til lager** er satt til *Ja*.

### <a name="set-up-a-worker"></a>Angi en arbeider

Pakkestasjonen regnes som en lokasjon. Lagerarbeidere som logger på pakkestasjonen, ser og fungerer bare på forsendelser og containere som er planlagt ved denne bestemte pakkelokasjonen. En bruker som logger på Microsoft Dynamics 365, må konfigureres som en arbeider i Lagerstyring. Hvis brukerens navn ikke vises i listen over arbeidsbrukere, kan du bruke følgende fremgangsmåte for å legge det til.

> [!NOTE]
> Disse trinnene forutsetter at brukeren allerede finnes i systemet og er knyttet til som en ansatt eller arbeider i **Human Resources**-modulen.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**.
1. Velg **Ny**.
1. I **Arbeider**-feltet velger du målbrukeren i listen over ansatte.
1. Velg **Velg**.
1. Velg **Lagre** i handlingsruten.
1. I hurtigfanen **Brukere** velger du **Ny** for å opprette en konto for en mobilenhet, og angi følgende verdier for den:

    - **Bruker-ID:** Angi en unik ID.
    - **Brukernavn:** Angi et navn på ID-en.
    - **Standardlager:** *62*
    - **Menynavn:** *Hoved*

1. Velg **Lagre** i handlingsruten.
1. Dialogboksen **Angi passord** vises, der du kan opprette et enkelt passord som brukeren kan bruke til å logge på mobilappen. Angi følgende verdier:

    - **Passord:** Angi et enkelt passord.
    - **Bekreft passord:** Skriv inn det samme passordet på nytt.

1. Velg **Angi passord**.

    Et varsel i Handlingssenteret informerer deg om at passordet er angitt for brukeren du opprettet.

### <a name="create-a-location-type"></a>Opprette en lokasjonstype

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonstyper**.
1. I handlingsruten velger du **Ny** for å opprette en lokasjonstype, og deretter angir du følgende verdier for den:

    - **Plasseringstype:** *SORTER*
    - **Beskrivelse:** *Sorter*

1. Velg **Lagre** i handlingsruten.

### <a name="set-up-warehouse-management-parameters"></a>Definere lagerstyringsparametere

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I fanen **Generelt** i hurtigfanen **Lokasjonstyper** angir du feltet for **sorteringslokasjonstype** til *SORTER*.
1. Velg **Lagre** i handlingsruten.

### <a name="set-up-a-location-profile"></a>Konfigurere en lokasjonsprofil

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Lokasjonsprofil-ID:** *Sortering*
    - **Navn:** *Sortering*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Lokasjonsformat:** *ASRB* (Aisle-Rack-Shelf-Bin)
    - **Plasseringstype:** *SORTER*
    - **Bruk sporing av nummerskilt:** *Ja*
    - **Tillat kombinerte varer:** *Ja* (når du setter dette alternativet til *Ja*, settes alternativet **Tillat kombinerte lagerpartier** automatisk til *Ja*, og dette kan ikke endres uavhengig av hverandre.)

1. Velg **Lagre**.

### <a name="set-up-a-location"></a>Konfigurere en lokasjon

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**.
1. Fjern merket for **Generer kontrollsifre for lokasjon** i hodet.
1. I handlingsruten velger du **Ny** for å opprette en lokasjon, og deretter angir du følgende verdier for den:

    - **Lager:** *62*
    - **Lokasjon:** *SORT*
    - **Lokasjonsprofil-ID:** *SORTERING*

1. Velg **Lagre**.

### <a name="set-up-an-outbound-sorting-template"></a>Definere en utgående sorteringsmal

Den utgående sorteringsmalen bestemmer om arbeidet skal opprettes fra sorteringslokasjonen, og om sortering skal utføres manuelt eller automatisk.

I dette scenariet skal du opprette en utgående sorteringsmal for å bygge paller etter pakkstasjonen.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Utgående sorteringsmal**.
1. Velg **Ny** i handlingsruten.
1. I toppteksten på den nye malen angir du følgende verdier:

    - **ID for utgående sorteringsmal:** *AutoWork*
    - **Beskrivelse:** *Opprettelse av automatisk arbeid*
    - **Type utgående sorteringsmal:** *Container*
    - **Lager:** *62*
    - **Lokasjon:** *SORT*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Sorteringsbekreftelse:** *Posisjonsskanning*
    - **Opprett arbeid ved posisjonslukking:** *Ja*

        Hvis dette valget settes til *Ja* når posisjonen er lukket, opprettes arbeid for å flytte lageret til den endelige leveringslokasjonen. Hvis det settes til *Nei*, plukkes lageret umiddelbart til ordren når posisjonen lukkes.

    - **Stillingstilordning:** *Automatisk*

        Hvis dette feltet settes til *Manuell*, må brukeren alltid angi hvilken posisjon lageret skal sorteres til. Hvis det er satt til *Automatisk*, vil systemet automatisk sende lageret til en posisjon automatisk når det er mulig, basert på inndelingene i sorteringsmalen.

1. Velg **Lagre** for å gjøre **Rediger spørring**-knappen på handlingsruten tilgjengelig.
1. I handlingsruten velger du **Rediger spørring**.
1. I redigeringsprogrammet i fanen **Sortering** legger du til en linje med følgende verdier:

    - **Tabell:** *Forsendelser*
    - **Avledet tabell:** *Forsendelser*
    - **Felt:** *Transportørtjeneste*

        Når du har valgt denne verdien, kan du få følgende melding: Feltet Transportørtjeneste er ikke et indeksfelt. Vil du legge til sortering på dette? Velg **Ja**.

    - **Søkeretning:** *Stigende*

1. Velg **OK**.
1. Du kan få følgende melding: "Gruppering vil bli tilbakestilt, vil du fortsette?" Velg **Ja**.

    Knappen for **Inndelinger for utgående sortereringmal** i handlingsruten blir tilgjengelig.

1. Velg alternativet for **Inndelinger for utgående sortereringmal** i handlingsruten.
1. I **Sorteringskriterier for utgående**-dialogboksen angir du følgende verdier:

    - **Referansetabellnavn:** *Forsendelser*
    - **Referansefeltnavn:** *Transportørtjeneste*
    - **Grupper etter-feltet:** Merk av i denne avmerkingsboksen for å gruppere forsendelser etter transportørservice.

1. Velg **OK** for å lagre innstillingene og lukke dialogboksen.

### <a name="set-up-container-packing-policies"></a>Definere policyer for containerpakking

1. Gå til **Lagerstyring \> Oppsett \> Containere \> Policyer for containerpakking**.
1. Velg **Ny** i handlingsruten.
1. I toppteksten på den nye policyen angir du følgende verdier:

    - **Policy for containerpakking:** *Sorter*
    - **Beskrivelse:** *Sorter*

1. Angi følgende verdier i **Oversikt**-hurtigfanen:

    - **Lager:** *62*
    - **Standardlokasjon for sortering:** *SORTER*
    - **Vekt/enhet:** *kg*
    - **Policy for containerlukking:** *Automatisk frigivelse*
    - **Policy for containerfrigivelse:** *Tilordne container til utgående sorteringsposisjon*

1. Velg **Lagre**.

### <a name="set-up-packing-profiles"></a>Definere pakkeprofiler

Opprett en ny pakkeprofil som skal brukes sammen med sorteringsfunksjonen.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.
1. I handlingsruten velger du **Ny** for å opprette en linje, og deretter angir du følgende verdier for den:

    - **Pakkeprofil-ID:** *Sorter*
    - **Beskrivelse:** *Sorter*
    - **Policy for containerpakking:** *Sorter*
    - **Modus for container-ID:** *Automatisk*
    - **Containertype:** *Boks-Stor*
    - **Opprett container automatisk ved containerlukking:** Fjernet (= *Nei*)

1. Velg **Lagre**.

### <a name="set-up-work-classes"></a>Konfigurere arbeidsklasser

Definer en arbeidsklasse som skal brukes sammen med sortering.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.
1. I handlingsruten velger du **Ny** for å opprette en arbeidsklasse for sortering, og deretter angir du følgende verdier for den:

    - **Arbeidsklasse-ID:** *Sorter*
    - **Beskrivelse:** *Sorter*
    - **Arbeidsordretype:** *Sortert lagerplukking*

1. Velg **Lagre**.

### <a name="set-up-mobile-device-menu-items"></a>Definere en mobilenhetsmenyelementer

#### <a name="set-up-a-new-pallet-menu-item"></a>Definere et nytt pallemenyelement

Opprett et menyelement for mobilenhet for å bygge paller under sortering.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Navn på menyelement:** *Palleversjon*
    - **Tittel:** *Palleversjon*
    - **Modus:** *Indirekte*
    - **Bruke eksisterende arbeid:** *Nei*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Aktivitetskode:** *Utgående sortering*

        Når dette feltet er satt til *Utgående sortering*, vises feltet **ID for utgående sorteringsmal**.

    - **Bruk prosessveiledning:** *Ja*

        Når feltet **Aktivitetskode** er satt til *Utgående sortering*, settes dette alternativet automatisk til *Ja*.

    - **ID for utgående sorteringsmal:** *AutoWork*

1. Velg **Lagre**.

#### <a name="set-up-a-new-loading-menu-item"></a>Definere et nytt lastemenyelement

Deretter oppretter du et menyelement som lar brukere flytte de sorterte lagervarene til forsendelseslokasjonen.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Navn på menyelement:** *Last fra sortering*
    - **Tittel:** *Last fra sortering*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*

1. På **Generelt**-hurtigfanen settes **Styrt av**-feltet til *Brukerstyrt*.
1. På hurtigfanen **Arbeidsklasser** velger du **Ny**, og angi deretter følgende verdier:

    - **Arbeidsklasse-ID:** *SORTER*
    - **Arbeidsordretype:** *Sortert lagerplukking*

1. Velg **Lagre**.

### <a name="set-up-the-mobile-device-menu"></a>Definere mobilenhetsmeny

Du må nå legge til de nye menyelementene på mobilenhetsmenyen.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Utgående**-menyen.
1. I handlingsruten velger du **Rediger**.
1. I kolonnen **Tilgjengelige menyer og menyelementer** finner og velger du **Palleversjon**.
1. Velg høyre pil-knappen for å flytte **Palleversjon** til kolonnen **Menystruktur**.
1. Bruk pil opp og pil ned for å plassere menyelementet **Palleversjon** i ønsket posisjon på mobilenhetmenyen.
1. Velg **Lagre**.
1. Gjenta denne fremgangsmåten for å legge til menyen **Last fra sortering** på **Utgående**-menyen.

### <a name="set-up-location-directives"></a>Konfigurer lokasjonsdirektiver

*Lokasjonsdirektiver* er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. Du må nå opprette en regel for å behandle sorteringsarbeidet.

#### <a name="set-up-a-single-sku-directive"></a>Definere et enkelt-SKU-direktiv

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I venstre rute endrer du verdien på feltet **Arbeidsordretype** til *Sortert lagerplukking*.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Sekvens:** *1*
    - **Navn:** *Rampedør*

1. Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen:

    - **Arbeidstype:** *Plasser*
    - **Område:** *6*
    - **Lager:** *62*
    - **Flere SKUer:** *Nei*

1. Velg **Lagre** for å gjøre verktøylinjen på **Linjer**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Linjer** velger du **Ny**, og angi deretter følgende verdier på den nye linjen: Godta standardverdiene for alle de andre feltene.

    - **Sekvens:** *1*
    - **Fra:** *0*
    - **Til:** *1,000,000*

1. Velg **Lagre** for å gjøre verktøylinjen på **Handlinger for lokasjonsdirektiv**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny**, og angi deretter følgende verdier på den nye linjen: Godta standardverdiene for alle de andre feltene.

    - **Sekvens:** *1*
    - **Navn:** *Rampedør*

1. Velg **Lagre**.
1. I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.
1. I redigeringsprogrammet for spørring, i fanen **Område**, finner du raden der feltet **Felt** er satt til *Lokasjon*. Sett **Vilkår**-feltet for denne raden til *Rampedør*.
1. Velg **OK** for å lagre innstillingene og lukke redigeringsprogrammet for spørring.

#### <a name="set-up-a-multiple-sku-directive"></a>Definere et flere-SKU-direktiv

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I venstre rute endrer du verdien på feltet **Arbeidsordretype** til *Sortert lagerplukking*.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Sekvens:** *2*
    - **Navn:** *Rampedør, flere*

1. Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen:

    - **Arbeidstype:** *Plasser*
    - **Område:** *6*
    - **Lager:** *62*
    - **Flere SKUer:** *Ja*

1. Velg **Lagre** for å gjøre verktøylinjen på **Linjer**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Linjer** velger du **Ny**, og angi deretter følgende verdier på den nye linjen: Godta standardverdiene for alle de andre feltene.

    - **Sekvens:** *1*
    - **Fra:** *0*
    - **Til:** *1,000,000*

1. Velg **Lagre** for å gjøre verktøylinjen på **Handlinger for lokasjonsdirektiv**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny**, og angi deretter følgende verdier på den nye linjen: Godta standardverdiene for alle de andre feltene.

    - **Sekvens:** *1*
    - **Navn:** *Rampedør, flere*

1. Velg **Lagre**.
1. I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.
1. I redigeringsprogrammet for spørring, i fanen **Område**, finner du raden der feltet **Felt** er satt til *Lokasjon*. Sett **Vilkår**-feltet for denne raden til *Rampedør*.
1. Velg **OK** for å lagre innstillingene og lukke redigeringsprogrammet for spørring.

### <a name="set-up-work-templates"></a>Konfigurer arbeidsmaler

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Endre verdien på feltet **Arbeidsordretype** til *Sortert lagerplukking*.
1. I handlingsruten velger du **Ny** for å opprette en arbeidsmal.
1. Angi følgende verdier i fanen **Oversikt**:

    - **Sekvens:** *1*
    - **Arbeidsmal:** *Sorter*
    - **Beskrivelse av arbeidsmal:** *Sorter*

1. Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-hurtigfanen tilgjengelig.
1. På **Arbeidsmaldetaljer**-hurtigfanen velger du **Ny** for å legge til en linje, og angi deretter følgende verdier for den:

    - **Arbeidstype:** *Plukk*
    - **Arbeidsklasse-ID:** *SORTER*

1. Velg **Ny** på nytt for å legge til en ny linje, og angi deretter følgende verdier for den:

    - **Arbeidstype:** *Plasser*
    - **Arbeidsklasse-ID:** *SORTER*

1. Velg **Lagre**.

## <a name="scenario"></a>Scenario

Dette scenariet simulerer en situasjon der pakkede containere automatisk skal sorteres til forskjellige posisjoner (paller) etter pakkestasjonen, avhengig av transportørtjenesten. Etter at alle varer fra lasten er pakket og sortert etter adresse, flyttes pallene til rampedøren.

### <a name="create-sales-orders-and-picking-work"></a>Opprette salgsordrer og plukkarbeid

#### <a name="create-sales-order-1"></a>Opprett salgsordre 1

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-005*
    - **Lager:** *62*

1. Velg **OK** for å lukke dialogboksen.

    Den nye salgsordren åpnes.

1. Bytt til **Topptekst**-visningen.
1. På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:

    - **Transportør:** *Luftlast*
    - **Transportørtjeneste:** *Lufttransport*

1. Gå til **Linjer**-visningen.
1. Hvis en ny, tom linje ikke automatisk legges til i rutenettet i **Salgsordrelinjer**-hurtigfanen, velger du **Legg til linje** for å legge til en linje.
1. Angi følgende verdier på den nye ordrelinjen:

    - **Varenummer:** *A0001*
    - **Antall:** *2*

1. Mens den nye ordrelinjen fremdeles er valgt på hurtigfanen **Salgsordrelinjer**, velger du **Reservasjon** på menyen **Lager**.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere det fulle antallet på den valgte linjen i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren. Skriv ned nummeret på bølge-ID og forsendelses-ID.

#### <a name="sales-order-2"></a>Salgsordre 2

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-006*
    - **Lager:** *62*

1. Velg **OK** for å lukke dialogboksen.
1. Den nye salgsordren åpnes. Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. Angi følgende verdier på denne ordrelinjen:

    - **Vare:** *A0001*
    - **Antall:** *1*

1. På hurtigfanen **Linjedetaljer**, i fanen **Levering** setter du feltet **Leveringsmåte** til *Flowe-STD*.
1. På hurtigfanen **Salgsordrelinjer** velger du **Legg til linje**, og angi deretter følgende verdier på den andre ordrelinjen:

    - **Vare:** *A0002*
    - **Antall:** *1*

1. På hurtigfanen **Linjedetaljer**, i fanen **Levering**, endrer du verdien i feltet **Leveringsmåte** til *Air C-Air*.
1. I hurtigfanen **Salgsordrelinjer** velger du den første ordrelinjen. Velg deretter **Reservasjon** på **Lager**-menyen over rutenettet.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere det fulle antallet på den valgte linjen i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. I hurtigfanen **Salgsordrelinjer** velger du den andre ordrelinjen. Velg deretter **Reservasjon** på **Lager**-menyen over rutenettet.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere det fulle antallet på den valgte linjen i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren. Merk at to bølge-ID-numre og to forsendelses-ID-numre er opprettet, én for hver leveringsmåte for salgsordrelinjene.

#### <a name="get-the-work-ids-from-the-work-details"></a>Hente arbeids-IDene fra arbeidsdetaljene

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. Siden viser arbeids-IDene som er opprettet fra salgsordrer. Bruk bølge-IDene og forsendelses-IDene fra salgsordrene som du opprettet, for å finne arbeids-IDen for hver bølge og forsendelse. Noter deg arbeids-IDene, fordi du trenger dem i de neste trinnene. Legg merke til at to arbeids-IDer er opprettet for den andre salgsordren. Hvis ulike varer er plukket fra forskjellige lokasjoner, genereres separate arbeids-IDer.

### <a name="pick-items-for-the-sales-orders"></a>Plukke varer for salgsordrene

Fullfør det opprettede arbeidet ved å bruke den mobile enheten til å flytte elementene til pakkestasjonen.

1. På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Salgsplukking**.
1. I **ID**-feltet angir du arbeids-IDen som ble opprettet for salgsordre 1.
1. Velg **OK**.
1. På siden **Salgsordrer - Plukk** angir du et målnummerskilt som ble opprettet for salgsordre 1. Legg merke til at plukklokasjon (*bulk-001*), vare (*A0001*) og antall (*2 stk*) vises.
1. Velg **OK**.
1. Se gjennom informasjonen på siden **Salgsordrer - Plasser**. **Loc**-feltet bør angi at de plukkede varene skal overføres til *Pakke*-lokasjonen.
1. Velg **OK**.

    På siden **Skann en arbeids-ID/nummerskilt-ID** får du meldingen "Arbeid fullført"-melding, som viser at arbeids-IDen fra salgsordre 1 er fullført.

    Du skal nå plukke salgsordre 2.

1. I **ID**-feltet angir du arbeids-IDen som ble opprettet for salgsordre 2, der linje 1 har vare *A0001*.
1. Velg **OK**.
1. Angi et målnummerskilt på siden **Salgsordrer - Plukk**. Legg merke til at plukklokasjon (*bulk-001*), vare (*A0001*) og antall (*1 stk*) vises.
1. Velg **OK**.
1. Se gjennom informasjonen på siden **Salgsordrer - Plasser**. **Loc**-feltet bør angi at de plukkede varene skal overføres til *Pakke*-lokasjonen.
1. Velg **OK**.

    På siden **Skann en arbeids-ID/nummerskilt-ID** mottar du en "Arbeid fullført"-meldingen. Denne meldingen angir at arbeids-IDen fra linje 1 i salgsordre 2 er fullført.

1. I **ID**-feltet angir du arbeids-IDen som ble opprettet for salgsordre 2, der linje 2 har vare *A0002*.
1. Velg **OK**.
1. Angi et målnummerskilt på siden **Salgsordrer - Plukk**. Legg merke til at plukklokasjon (*bulk-002*), vare (*A0001*) og antall (*1 stk*) vises.
1. Velg **OK**.
1. Se gjennom informasjonen på siden **Salgsordrer - Plasser**. **Loc**-feltet bør angi at de plukkede varene skal overføres til *Pakke*-lokasjonen.
1. Velg **OK**.

    På siden **Skann en arbeids-ID/nummerskilt-ID** mottar du en "Arbeid fullført"-meldingen. Denne meldingen angir at arbeids-IDen fra linje 2 i salgsordre 2 er fullført.

### <a name="pack-sales-orders-into-containers"></a>Pakkesalgsordrer i containere

#### <a name="pack-sales-order-1-into-containers"></a>Pakkesalgsordre 1 i containere

1. Gå til **Lagerstyring \> Pakking og containerbruk \> Pakke**.

    Dialogboksen **Velg pakkstasjon** vises. Som standard bør feltet **Arbeider** settes til navnet på arbeideren du konfigurerte tidligere.

1. Angi følgende verdier for å vise og arbeide med forsendelser og containere som er planlagt på den bestemte pakkelokasjonen:

    - **Område:** *6*
    - **Lager:** *62*
    - **Plassering:** *Pakke*
    - **Pakkeprofil-ID:** *Sorter*

1. Velg **OK** for å lukke dialogboksen.
1. På siden **Pakke** i feltet **Lisensplate eller forsendelse** angir du målnummerskiltet for salgsordre 1. Deretter velger du **Tab**- eller **Enter**-tasten på tastaturet for å gå ut av feltet.
1. I handlingsruten velger du **Ny container**.
1. Godta alle standardinnstillingene, og velg **OK**. Noter container-IDen.
1. Angi følgende verdier på **Varepakking**-hurtigfanen:

    - **Antall:** *1*
    - **Identifikator:** Vare *A0001*

1. I handlingsruten velger du **Lukk container**.
1. I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.
1. Velg **OK**. Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.
1. Opprett en andre container for å legge til den andre varen fra målnummerskiltet for salgsordre 1 i en ny container.
1. I handlingsruten velger du **Ny container**.
1. Godta alle standardinnstillingene, og velg **OK**. Noter container-IDen.
1. Angi følgende verdier på **Varepakking**-hurtigfanen:

    - **Antall:** *1*
    - **Identifikator:** Vare *A0001*

1. I handlingsruten velger du **Lukk container**.
1. I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.
1. Velg **OK**. Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.

#### <a name="pack-sales-order-2-into-containers"></a>Pakkesalgsordre 2 i containere

1. På siden **Pakke** i feltet **Lisensplate eller forsendelse** angir du målnummerskiltet for linje 1 for salgsordre 2. Deretter velger du **Tab**- eller **Enter**-tasten på tastaturet for å gå ut av feltet.
1. I handlingsruten velger du **Ny container**.
1. Godta alle standardinnstillingene, og velg **OK**. Noter container-IDen.
1. Angi følgende verdier på **Varepakking**-hurtigfanen:

    - **Antall:** *1*
    - **Identifikator:** Vare *A0001*

1. I handlingsruten velger du **Lukk container**.
1. I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.
1. Velg **OK**. Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.
1. I feltet **Lisensplate eller forsendelse** angir du målnummerskiltet for linje 2 for salgsordre 2. Deretter velger du **Tab**- eller **Enter**-tasten på tastaturet for å gå ut av feltet.
1. I handlingsruten velger du **Ny container**.
1. Godta alle standardinnstillingene, og velg **OK**. Noter container-IDen.
1. Angi følgende verdier på **Varepakking**-hurtigfanen:

    - **Antall:** *1*
    - **Identifikator-felt:** Vare *A0002*

1. I handlingsruten velger du **Lukk container**.
1. I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.
1. Velg **OK**. Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.

Hvis du vil vise containerdetaljene, går du til **Lagerstyring \> Pakking og containerbruk \> Containere** og søker etter container-IDene som ble opprettet under pakking.

### <a name="sort-the-containers"></a>Sortere containerne

> [!IMPORTANT]
> Når du får tilgang til **Palleversjon** i menyelementet på mobilappen for å utføre utgående sortering, vil du se en knapp som er merket som **Full**. *Ikke bruk **Full**-knappen til å sortere eller lukke posisjonen.*
>
> **Full**-knappen er angitt som standard og kan ikke deaktiveres eller fjernes fra siden. Den brukes ikke for funksjonen *Utgående sortering*.

#### <a name="sort-the-first-container"></a>Sortere den første containeren

1. På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Palleversjon**.
1. I **LP/Con**-feltet angir du den første container-IDen som er tilknyttet salgsordre 1.
1. Velg **OK**.
1. Fordi det ikke finnes noen sorteringsposisjoner, må du angi en. I **Sporteringsposisjon-ID**-feltet angir du *SP01*.
1. Fordi ingen nummerskilt er knyttet til sorteringsposisjon *SP01*, må du angi et. I feltet **Nummerskilt** angir du *PLP01*.
1. Velg **OK**.
1. Siden validering av sorteringsposisjon er slått på, må du angi ID for sorteringsposisjon på nytt. I **Sporteringsposisjon-ID**-feltet angir du *SP01*.
1. Velg **OK**.

    Du mottar en Arbeid fullført-melding.

> [!TIP]
> Hvis du vil vise sorteringsposisjonen og nummerskiltet i den, går du til **Lagerstyring \> Pakking og containerbruk \> Posisjonstilordninger for utgående sortering**.
>
> Siden **Posisjonstilordninger for utgående sortering** viser alle sorteringsposisjonene som for øyeblikket er aktive. Feltet **Transaksjoner for sorteringsposisjon** viser nummerskiltet som er knyttet til hver sorteringsplassering, og containerne som finnes i sorteringsposisjonen. Legg merke til at det allerede finnes én sorteringsposisjon, og at hurtigfanen **Kriterier for sorteringsposisjon** viser et vilkår for **Forsendelse – Transportørtjeneste - Fly**.

#### <a name="sort-the-remaining-containers"></a>Sortere de resterende containerne

1. På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Palleversjon**.
1. I **LP/Con**-feltet angir du den andre container-IDen som er tilknyttet salgsordre 1.
1. Velg **OK**. Siden sorteringsmalen er satt opp til å sortere automatisk, og det allerede finnes en sorteringsposisjon som har samsvarende vilkår, blir du automatisk dirigert til riktig sorteringsposisjon.
1. Velg **OK**.
1. Bekreft sorteringsposisjons-IDen for å angi at lageret er på riktig sted. I **Sporteringsposisjon-ID**-feltet angir du *SP01*.
1. Velg **OK**.

    Arbeid er fullført på den andre containeren fra salgsordre 1. Du skal nå sortere de gjenstående containerne fra salgsordre 2.

1. I **LP/Con**-feltet angir du container-IDen til containeren fra salgsordre 2 som inneholder vare *A0001*. Fordi transportørtjenesten er forskjellig, blir du bedt om å angi en ny sorteringsposisjon og tilordne et nummerskilt til denne posisjonen. Bruk sorteringsposisjon *SP02* og nummerskilt *PLP02*.
1. Velg **OK**.
1. Bekreft sorteringsposisjonen ved å angi *SP02* i feltet **Sporteringsposisjon**.
1. Velg **OK**.

    Arbeidet er fullført på containeren.

1. I **LP/Con**-feltet angir du container-IDen til den gjenværende containeren fra salgsordre 2 som inneholder vare *A0002*. Fordi transportørtjenesten er den samme som transportørtjenesten for salgsordre 1, viser systemet den eksisterende sorteringsposisjonen som har samsvarende kriterier.
1. Velg **OK**.
1. Bekreft sorteringsposisjonen ved å angi *SP01* i feltet **Sporteringsposisjon**.
1. Velg **OK**.

    Arbeidet er fullført på containeren.

### <a name="close-the-outbound-sorting-positions"></a>Lukke den utgående sorteringsposisjonen

Når hele lageret er sortert, må posisjonen lukkes før arbeidet kan opprettes. Sortert lagerplukkingsarbeid vil bli opprettet for å ta lageret til rampedøren.

#### <a name="close-a-position-from-the-mobile-device"></a>Lukke en posisjon fra den mobile enheten

1. På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Palleversjon**.
1. I **LP/con**-feltet angir du en container-ID som ble sortert for å sortere posisjonen *SP01*.
1. Velg **OK**.
1. Du får følgende melding: "Containeren er allerede sortert til posisjon SP01. Vil du lukke posisjonen?" Velg **Lukk**.

    Arbeidet er fullført.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Lukke en posisjon fra utgående sorteringsposisjonstilordninger

1. Gå til **Lagerstyring \> Pakking og containerbruk \> Posisjonstilordninger for utgående sortering**.
1. I venstre kolonne velger du **SP02**. Denne utgående sorteringsposisjonsraden er den du vil lukke.
1. I handlingsruten velger du **Lukk posisjon**. Sorteringsposisjons posten er lukket og vises ikke lenger.

    > [!TIP]
    > Hvis du vil vise alle poster med lukkede posisjoner, merker du av for **Vis lukket**.

### <a name="sorted-inventory-picking"></a>Sortert lagerhenting

Du må fylle ut det sorterte lagerplukkingsarbeidet. Når det er fullført, blir lageret plukket lageret til salgsordren. På dette tidspunktet gjelder alle andre lagerprosesser.

1. På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).
1. I hovedmenyen velger du **Utgående**.
1. På menyen **Utgående** velger du **Last fra sortering**.
1. Angi mål-IDen for nummerskilt fra den første sorteringsposisjonen, *SP01*. Angi **ID**-feltet til *PLP01*.
1. Velg **OK**.
1. Siden **Sortert lagerplukking: Plukk** viser plukkarbeidet som må utføres. Plukk fra *SORTER*-lokasjonen og målnummerskiltet *PLP01*, som har flere varer og et antall på *3*.
1. Velg **OK**.
1. Siden **Sortert lagerplukking: Plasser** viser plasseringsarbeidet som må utføres. Plasser til *Rampedør*-lokasjonen og målnummerskilt *PLP01*, som har flere varer og et antall på *3*.
1. Velg **OK**.

    Arbeidet er fullført.

1. Angi målnummerskilt-ID-en fra den andre sorteringsposisjonen, *SP02*. Angi **ID**-feltet til *PLP02*.
1. Velg **OK**.
1. Siden **Sortert lagerplukking: Plukk** viser plukkarbeidet som må utføres. Plukk fra *SORTER*-lokasjonen og målnummerskiltet *PLP02*, som har flere varer og et antall på *1*.
1. Velg **OK**.
1. Siden **Sortert lagerplukking: Plasser** viser plasseringsarbeidet som må utføres. Plasser til *Rampedør*-lokasjonen og målnummerskilt *PLP02*, som har flere varer og et antall på *1*.
1. Velg **OK**.

    Arbeidet er fullført.

På dette tidspunktet og fremover gjelder alle andre lagerprosesser.
