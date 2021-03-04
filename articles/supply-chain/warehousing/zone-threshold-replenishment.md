---
title: Etterfylling av soneterskel
description: Sonebasert etterfylling bruker en minimum/maksimum (min./maks.) etterfyllingsstrategi, men evaluerer hele lagersoner i stedet for bare for enkeltlokasjoner. Derfor kan lagerledere raskere finne ut når det er behov for tilleggsbeholdning i en plukksone.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6f4ddd03ec16ac43b007b904eb688563735e0941
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654178"
---
# <a name="zone-threshold-replenishment"></a>Etterfylling av soneterskel

[!include [banner](../includes/banner.md)]

Sonebasert etterfylling bruker en minimum/maksimum (min./maks.) [etterfyllingsstrategi](replenishment.md), men evaluerer hele lagersoner i stedet for bare for enkeltlokasjoner. Derfor kan lagerledere raskere finne ut når det er behov for tilleggsbeholdning i en plukksone.

Oppsettet for denne funksjonen ligner på oppsettet for lokasjonsbasert etterfylling. Når du definerer en mal for min./maks. etterfylling, kan du imidlertid også angi om terskelen skal evalueres per lokasjon eller per sone. Hvis du definerer evaluering som er basert på soner, må du legge til bestemte soner i sonevalgspørringen.

Som lokasjonsbasert min./maks. etterfylling er sonebasert min./maks. etterfylling basert på oppsettet av en minimums beholdningsterskelen som utløser oppretting av etterfyllingsarbeid for utvalgte varer. Dette etterfyllingsarbeidet øker beholdningen til den angitte maksimumsterskelen for sonen.

> [!NOTE]
> Prosesser for soneetterfylling for produktvarianter støttes ikke i den gjeldende versjonen.


Til forskjell fra den lokasjonsbaserte min./maks. etterfyllingen må ikke sonebasert min./maks. etterfylling være faste lokasjoner for å vurdere om lokasjoner skal lagre en bestemt vare. Derfor gjør sonebasert etterfylling det mulig å bruke min./maks. etterfylling, selv om du ikke har faste lokasjoner for hver vare eller varevariant på lageret. Når et antall i sonen faller under den angitte minimumsterskelen, opprettes etterfyllingsarbeid. Lokasjonsdirektiver bestemmer hvilken lokasjon lageret skal plasseres i.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Aktiver funksjonen for etterfylling av soneterskel

Før du kan bruke *Etterfylling av soneterskel*-funksjonen, må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Etterfylling av soneterskel*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Konfigurere sonebasert etterfylling

Hvis du vil konfigurere sonebasert etterfylling, må du konfigurere flere deler av systemet. Denne delen introduserer de ulike innstillingene og gir informasjon om demonstrasjonsdataverdier du kan angi hvis du vil jobbe gjennom scenariet på slutten av dette emnet.

### <a name="set-up-directive-codes"></a>Konfigurere direktivkoder

Med [Direktivkoder](control-warehouse-location-directives.md) kan du være mer spesifikk når du definerer lokasjonsmalen som brukes i en arbeidsmal. Hver kode etablerer en felles verdi du kan referere til når du konfigurerer hver maltype.

#### <a name="view-and-edit-directive-codes"></a>Vise og redigere direktivkoder

Hvis du vil vise eller redigere direktivkoder, går du til **Lagerstyring \> Oppsett \> Direktivkoder**.

#### <a name="prepare-demo-data-directive-codes"></a>Forberede direktivkoder for demonstrasjonsdata

Dette eksemplet viser hvordan du klargjør en direktivkode. Hvis du planlegger å jobbe gjennom scenariet på slutten av dette emnet, bruker du demonstrasjonsdataverdiene som finnes her. Hvis ikke bruker du dine egne verdier.

1. Velg den juridiske enheten **USMF** som skal brukes sammen med demonstrasjonsdataene.
1. Gå til **Lagerstyring \> Oppsett \> Direktivkoder**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Direktivkode:** _Soneetterfyll._
    - **Beskrivelse av direktivet:** _Soneetterfylling_

1. Velg **Lagre** for å lagre den nye koden.

### <a name="set-up-replenishment-templates"></a>Konfigurer etterfyllingsmaler

Maler for etterfylling basert på [minimums- og maksimumsantall](tasks/set-up-min-max-replenishment-process.md) er den primære mekanismen for å opprettholde optimal nivåer på plukklokasjoner. I disse malene må du konfigurere reglene som skal brukes til å etterfylle beholdningen i lageret. Etterfyllingen som malene kan brukes til, inkluderer sonebasert etterfylling.

#### <a name="view-and-edit-replenishment-templates"></a>Vise og redigere etterfyllingsmaler

En etterfyllingsmal er et sett med regler som bestemmer når og hvordan en lokasjon fylles. Du velger en mal som skal styre når og hvordan etterfylling skal utføres. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler** for å vise eller redigere etterfyllingsmalene.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Klargjøre en etterfyllingsmal for demonstrasjonsdata

Dette eksemplet viser hvordan du klargjør en etterfyllingsmal. Hvis du planlegger å jobbe gjennom scenariet på slutten av dette emnet, bruker du demonstrasjonsdataverdiene som finnes her. Hvis ikke bruker du dine egne verdier.

1. Velg den juridiske enheten **USMF** som skal brukes sammen med demonstrasjonsdataene.
1. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**.
1. Velg **Rediger** for å legge siden inn i redigeringsmodus.
1. I handlingsruten velger du **Ny** for å legge til en rad i **Oversikt**-rutenettet.
1. I den nye raden angir du følgende verdier. Godta standardverdiene for alle de andre feltene.

    - **Etterfyllingsmal:** _Sone min./maks. etterfyll._
    - **Beskrivelse:** _Sone min./maks. etterfylling_
    - **Etterfyllingstype:** _Minimum eller maksimum_

1. Velg **Lagre**.
1. Mens den nye raden fortsatt er valgt i **Oversikt**-rutenettet, velger du **Ny** over **Detaljer for etterfyllingsmal**-rutenettet for å legge til en rad som er tilknyttet til *Sone min./maks. etterfyll.* som du akkurat har opprettet.
1. I den nye raden angir du følgende verdier:

    - **Sekvensnummer:** Angi _1_.
    - **Beskrivelse:** Angi _Velg soneetterfylling_.
    - **Etterfyllingsenhet:** Velg _ea_.
    - **Forespørselstype:** La dette feltet stå tomt.
    - **Direktivkode:** Dette feltet kobler etterfyllingsmalen til et lokasjonsdirektiv. Velg demonstrasjonsdataenes direktivkode som du opprettet tidligere (_Soneetterfyll._).
    - **Arbeidsmal:** La dette feltet stå tomt.
    - **Minimumsantall:** I dette feltet angis antallet som skal utløse etterfylling. Angi _50_.
    - **Maksimumsantall:** I dette feltet angis maksimalt antall av en vare som kan finnes i en sone. Generert etterfyllingsarbeid øker beholdningen til dette antallet. Angi _150_.
    - **Enhet:** I dette feltet angis enheten for minimums- og maksimumsverdiene. Velg _ea_.
    - **Behovsøkning:** Velg _Rund opp_.
    - **Etterfyll tomme faste lokasjoner:** Velg denne avmerkingsboksen.
    - **Etterfyll bare faste lokasjoner:** Fjern merket i denne boksen.
    - **Modus for produktspørring:** Velg _Produktspørring_.
    - **Terskelomfang for etterfylling:** Dette feltet definerer om malen skal evalueres etter sone eller en bestemt lokasjon. Velg _Sone_.
    - **Lager:** Velg _61_.

1. Velg **Velg produkter** over **Detaljer for etterfyllingsmal**-rutenettet.
1. I **Produktspørring**-dialogboksen, på **Område**-fanen, velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Tabell:** _Varer_
    - **Avledet tabell:** _Varer_
    - **Felt:** _Varenummer_
    - **Vilkår:** _A0001_

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Velg sone som skal etterfylles** over **Detaljer for etterfyllingsmal**-rutenettet.
1. I **Sonespørring**-dialogboksen, på **Område**-fanen, legger du til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Tabell:** _Lagersone_
    - **Avledet tabell:** _Lagersone_
    - **Felt:** _Sone-ID_
    - **Vilkår:** _ETASJE_

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.

### <a name="set-up-location-directives"></a>Konfigurer lokasjonsdirektiver

Til forskjell fra lokasjonsbasert min./maks. etterfylling krever sonebasert min./maks. etterfylling at du definerer både plukklokasjonsdirektiver og legger til lokasjonsdirektiver, fordi systemet evaluerer hele sonen i stedet for bare plukklokasjon for utgående arbeid.

#### <a name="view-and-edit-location-directives"></a>Vise og redigere lokasjonsdirektiver

Hvis du vil vise eller redigere lokasjonsdirektiver, går du til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.

Se neste del for eksempler som viser hvordan du kan bruke innstillingene til å opprette de påkrevde plukklokasjonsdirektivene og legge til lokasjonsdirektiver.

#### <a name="prepare-demo-data-location-directives"></a>Forberede lokasjonsdirektiver for demonstrasjonsdata

Hvis du vil forberede demonstrasjonsdata slik at de kan brukes i scenariet på slutten av dette emnet, må du opprette to lokasjonsdirektiver: ett for plukking og ett for plassering.

##### <a name="create-a-replenishment-pick-directive"></a>Opprette et plukkdirektiv for etterfylling

1. Velg den juridiske enheten **USMF** som skal brukes sammen med demonstrasjonsdataene.
1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I den venstre ruten setter du **Arbeidsordretype**-feltet til _Etterfylling_.
1. I handlingsruten velger du **Ny** for å opprette et nytt direktiv.
1. Angi følgende verdier:

    - **Sekvensnummer:** Godta standardverdien.
    - **Navn:** Angi _Soneplukking_.
    - **Arbeidstype:** Velg _Plukk_.
    - **Område:** Velg _6_.
    - **Lager:** Velg _61_.
    - **Direktivkoden:** La dette feltet stå tomt.
    - **Fler SKU:** Angi dette alternativet til _Nei_.

1. Velg **Lagre** for å opprette et direktiv med innstillingene du har konfigurert så langt.
1. På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Sekvensnummer:** Angi _1_.
    - **Fra-antall:** Angi _0_.
    - **Til-antall:** Angi _10000000_.
    - **Enhet:** La dette feltet stå tomt.
    - **Finn antall:** Velg _Ingen_.
    - **Begrens etter enhet:** Fjern merket i denne avmerkingsboksen.
    - **Rund opp til enhet:** Fjern merket i denne avmerkingsboksen.
    - **Finn emballasjeantall:** Fjern merket i denne avmerkingsboksen.
    - **Tillat oppdeling:** Merk av denne avmerkingsboksen.

1. Velg **Lagre** for å lagre den nye linjen.
1. Mens den nye linjen fremdeles er valgt i **Linjer**-rutenettet velger du **Ny** på **Handlinger for lokasjonsdirektiv**-hurtigfanen for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Sekvensnummer:** Angi _1_.
    - **Navn:** Angi _Plukk fra parti_.
    - **Fast lokasjonsbruk:** Velg _Faste og ikke-faste lokasjoner_.
    - **Tillat negativ beholdning:** Fjern merket i denne avmerkingsboksen.
    - **Parti aktivert:** Fjern merket i denne avmerkingsboksen.
    - **Strategi:** Velg _Ingen_.

1. Velg **Lagre** for å lagre den nye handlingen.
1. Mens den nye handlingen fremdeles er valgt, velger du **Rediger spørring** over **Handlinger for lokasjonsdirektiv**-rutenettet.
1. En spørringsdialogboks vises der du kan velge lokasjonene du vil etterfylle fra. På **Område**-fanen velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Tabell:** _Plasseringer_
    - **Avledet tabell:** _Lokasjoner_
    - **Felt:** _Sone-ID_
    - **Vilkår:** _BULK_

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Lagre** for å lagre lokasjonsdirektivet.

##### <a name="create-a-replenishment-put-directive"></a>Opprette et plasseringsdirektiv for etterfylling

1. I ruten til venstre på **Lokasjonsdirektiver**-siden kontrollerer du at **Arbeidsordretype**-feltet fremdeles er angitt til _Etterfylling_.
1. I handlingsruten velger du **Ny** for å opprette et nytt direktiv.
1. Angi følgende verdier:

    - **Sekvensnummer:** Godta standardverdien.
    - **Navn:** Angi _Soneplassering_.
    - **Arbeidsordretype:** Velg _Plasser_.
    - **Område:** Velg _6_.
    - **Lager:** Velg _61_.
    - **Direktivkode:** Velg _Soneetterfyll._ for å koble dette lokasjonsdirektivet med etterfyllingsmalen du opprettet tidligere, ved hjelp av koden du opprettet tidligere.
    - **Fler SKU:** Angi dette alternativet til _Nei_.

1. Velg **Lagre** for å opprette et direktiv med innstillingene du har konfigurert så langt.
1. På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Sekvensnummer:** Angi _1_.
    - **Fra-antall:** Angi _0_.
    - **Til-antall:** Angi _10000000_.
    - **Enhet:** La dette feltet stå tomt.
    - **Finn antall:** Velg _Ingen_.
    - **Begrens etter enhet:** Fjern merket i denne avmerkingsboksen.
    - **Rund opp til enhet:** Fjern merket i denne avmerkingsboksen.
    - **Finn emballasjeantall:** Fjern merket i denne avmerkingsboksen.
    - **Tillat oppdeling:** Merk av denne avmerkingsboksen.

1. Velg **Lagre** for å lagre den nye linjen.
1. Mens den nye linjen fremdeles er valgt i **Linjer**-rutenettet velger du **Ny** på **Handlinger for lokasjonsdirektiv**-hurtigfanen for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Sekvensnummer:** Angi _1_.
    - **Navn:** Angi _Soneplassering_.
    - **Fast lokasjonsbruk:** Velg _Faste og ikke-faste lokasjoner_.
    - **Tillat negativ beholdning:** Fjern merket i denne avmerkingsboksen.
    - **Parti aktivert:** Fjern merket i denne avmerkingsboksen.
    - **Strategi:** Velg _Konsolider_.

1. Velg **Lagre** for å lagre den nye handlingen.
1. Mens den nye handlingen fremdeles er valgt, velger du **Rediger spørring** over **Handlinger for lokasjonsdirektiv**-rutenettet.
1. En spørringsdialogboks vises der du kan velge sonene du vil etterfylle. Denne sonen skal være den samme sonen som er angitt i etterfyllingsmalen. På **Område**-fanen velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Tabell:** _Plasseringer_
    - **Avledet tabell:** _Lokasjoner_
    - **Felt:** _Sone-ID_
    - **Vilkår:** _ETASJE_

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Lagre** for å lagre lokasjonsdirektivet.

## <a name="scenario"></a>Scenario

Denne delen inneholder et eksempelscenario som viser hvordan du arbeider med funksjonen.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Klargjøre eksempeldataene som kreves for eksempelscenarioet

Før du begynner å jobbe gjennom scenariet, må du aktivere eksempeldata og konfigurere funksjonen som beskrevet i denne delen og i de forrige delene i dette emnet.

#### <a name="use-the-usmf-legal-entity"></a>Bruk den juridiske enheten USMF

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

#### <a name="prepare-additional-sample-data"></a>Klargjøre flere eksempeldata

Når du har valgt den juridiske enheten **USMF**, legger du til de ekstra eksempeldataene som kreves, som beskrevet under [Konfigurere sonebasert etterfylling](#setup) tidligere i dette emnet.

#### <a name="check-your-on-hand-inventory"></a>Kontrollere lagerbeholdningen

Følg denne fremgangsmåten for å kontrollere at systemet inneholder nok beholdning til å støtte eksempelscenariet.

1. Kontroller at det er lagerbeholdning for vare *A0001* på to forskjellige lokasjoner i plukksonen (*ETASJE*) som er angitt i etterfyllingsmalen. Den totale beholdningen må imidlertid være mindre enn det påkrevde minimumsantallet (*50*) som er angitt i etterfyllingsmalen. På denne måten kan du simulere hvordan beregningen skal skje for hele sonen i stedet for bare for én enkel lokasjon. **Bruk noen av lagerprosessene til å justere beholdningen etter behov.**
1. Kontroller at det er nok beholdning for vare *A0001* til en partilokasjon som er angitt i lokasjonsdirektivet for soneplukking, der etterfyllingsarbeidet skal plukke varene fra sone-ID *PARTI*. Den totale beholdningen må være mer enn det påkrevde maksimumsantallet (*150*) som er angitt i etterfyllingsmalen.
1. Valgfritt, men anbefalt: Følg denne fremgangsmåten for å opprette en justeringsjournal for beholdning:

    1. Gå til **Lagerstyring \> Journaloppføringer \> Varer \> Beholdningsjustering**.
    1. Velg **Ny**.
    1. I dialogboksen **Opprett beholdningsjournal** velger du *61* i **Lager**-feltet.
    1. Velg **OK**.
    1. På **Journallinjer**-hurtigfanen bruker du **Ny**-knappen til å legge til tre linjer i rutenettet og angir følgende verdier. Når du er ferdig med å konfigurere hver linje, velger du **Lagre**.

        - **Linje 1:**

            - **Varenummer:** *A0001*
            - **Område:** *6*
            - **Lager:** *61*
            - **Lokasjon:** *02A01R1S1B*
            - **Nummerskilt:** Velg et eksisterende nummerskilt i listen, eller opprett et nytt nummerskilt.
            - **Antall:** *1000*

        - **Linje 2:**

            - **Varenummer:** *A0001*
            - **Område:** *6*
            - **Lager:** *61*
            - **Lokasjon:** *07A01R2S1B*
            - **Nummerskilt:** Velg et eksisterende nummerskilt i listen, eller opprett et nytt nummerskilt.
            - **Antall:** *15*

        - **Linje 3:**

            - **Varenummer:** *A0001*
            - **Område:** *6*
            - **Lager:** *61*
            - **Lokasjon:** *07A01R1S1B*
            - **Nummerskilt:** Velg et eksisterende nummerskilt i listen, eller opprett et nytt nummerskilt.
            - **Antall:** *10*

    1. Velg **Valider** i handlingsruten. Løs eventuelle feil som blir funnet før du går videre til neste trinn.
    1. Velg **Bokfør** i handlingsruten for å postere beholdningen til lageret.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Eksempelscenario: Kjør sonebasert min./maks. etterfylling

Etter at alle de nødvendige eksempeldataene er på plass, kan du utløse etterfylling ved å følge denne fremgangsmåten.

1. Gå til **Lagerstyring \> Etterfylling \> Etterfyllinger**.
1. På hurtigkategorien **Poster som skal inkluderes** i **Etterfylling**-dialogboksen velger du **Filter**.
1. I **Forespørsel**-dialogboksen på **Område**-fanen redigerer du standard tabellrad på følgende måte:

    - **Tabell:** Velg _Etterfyllingsmaler_.
    - **Avledet tabell:** Velg _Etterfyllingsmaler_.
    - **Felt:** Velg _Etterfyllingsmal_.
    - **Vilkår:** Velg _Sone min./maks. etterfyll._. Denne etterfyllingsmalen er etterfyllingsmalen du opprettet mens du forberedt demonstrasjonsdataene for dette scenariet.

1. Velg **OK** for å lagre spørringen og gå til bake til **Etterfylling**-dialogboksen.
1. Velg **OK** for å kjøre etterfyllingsmalen.

Etterfyllingsarbeid opprettes nå for å plukkebeholdning fra *PARTI*-sonen og etterfyll den med *ETASJE*-sonen.

## <a name="notes-and-tips"></a>Merknader og tips

Her er noen få merknader og tips om hvordan du arbeider med funksjonen:

- Hvis du vil definere etterfyllingsarbeid som går til ønsket sone, kan du koble linjene for etterfyllingsmaler og lokasjonsdirektiver på en av følgende måter:

    - Rediger lokasjonsdirektivets hovedspørring og filtrer de valgte linjene for etterfyllingsmal.
    - Bruk en direktivkode på linjen for etterfyllingsmalen, og samsvar den til lokasjonsdirektivet for plassering.

- Hvis du bruker dynamiske lokasjoner, vil etterfyllingsarbeid bli opprettet enten for den første tilgjengelige lokasjonen eller for en lokasjon som allerede inneholder beholdningen, hvis handlingen for lokasjonsdirektivet er definert til å bruke **Konsolidering**-strategien.
- Hvis du bruker faste lokasjoner i stedet for soner, bør du bruke [standard min./maks. etterfylling](tasks/set-up-min-max-replenishment-process.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]