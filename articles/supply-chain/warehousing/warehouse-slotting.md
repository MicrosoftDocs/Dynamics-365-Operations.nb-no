---
title: Lagersporing
description: Dette emnet inneholder informasjon om lagersporing. Med lagersporing kan du konsolidere behov etter vare og måleenhet fra ordrer som har statusen bestilt, reservert eller frigitt. Det hjelper lagerledere å planlegge plukklokasjoner før de frigir ordrer til lageret og oppretter plukkarbeid.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0dd1f42b7bb337ccb65b7e4bdd9d307d074ae0d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838160"
---
# <a name="warehouse-slotting"></a>Lagersporing

[!include [banner](../includes/banner.md)]

Flere lagersporingsfunksjoner er tilgjengelig for å hjelpe lagerledere å planlegge plukklokasjoner før de frigir ordrer til lageret og oppretter plukkarbeid.

Med *Lagersporing* kan du konsolidere behov etter vare og måleenhet fra ordrer som har statusen *bestilt*, *reservert* eller *frigitt*. Det genererte behovet kan deretter brukes på lokasjoner som skal brukes til plukking, basert på antall, enhet, fysiske dimensjoner, faste lokasjoner og mer. Etter at sporingsplanen er opprettet, kan etter fyllingsarbeid opprettes for å hente riktig lagermengde til hver lokasjon.

Med funksjonen *Lagersporing for overføringsordrer* kan lagerledere å etterfylle plukklokasjoner, basert på behov fra overføringsordrer som ennå ikke er frigitt til lageret. Det sikrer at plukklokasjoner vil inkludere alle varene som kreves for overføringsordrene etter at de er frigitt til lager. Denne funksjonen krever at du også aktiverer funksjonen *Lagersporingsfunksjon*.

Funksjonen *Forbedringer av lagersporingsfordeling* legger til et alternativ for mallinjene som brukes av funksjonen *Lagersporing*. Alternativet gjør det mulig for systemet å ta hensyn til den eksisterende lagerbeholdningen på en målplassering. Derfor kan det genereres færre etterfyllinger for sporing. Funksjonen *Forbedringer av lagersporingsfordeling* krever at du også aktiverer funksjonen *Lagersporing*. Den kan også brukes sammen med *Lagersporing for overføringsordrer*.

## <a name="turn-on-the-warehouse-slotting-features"></a>Aktivere lagersporingsfunksjoner

Før du kan bruke disse funksjonene, må de være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonene og aktivere dem hvis nødvendig. Aktiver følgende funksjoner etter behov:

- Lagersporingsfunksjon
- Lagersporing for overføringsordrer

    > [!IMPORTANT]
    > Funksjonen *Lagersporingsfunksjon* må være aktivert før denne funksjonen.

- Forbedringer i tildeling av lagersporing

    > [!IMPORTANT]
    > Funksjonen *Lagersporingsfunksjon* må være aktivert før denne funksjonen.

## <a name="set-up-warehouse-slotting"></a>Definere lagersporing

Hvis du vil bruke lagersporing, må du definere følgende elementer i systemet:

- Måleenhetsnivåer for sporing
- Direktivkoder
- Sporingsmaler
- Lokasjonsdirektiver

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Opprett måleenhetslag for sporing

Måleenhetslag gjør det mulig å gruppere flere måleenheter sammen for å sporing. Hvis for eksempel bokser med flere størrelser plukkes fra samme boksplukkingsområde, kan ett lag opprettes for alle størrelsene. **Det må opprettes en linje for hver måleenhet som skal være en del av laget.**

1. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Måleenhetslag for sporing**.
1. Velg **Ny**.
1. I hodet angir du følgende verdier:

    - **Måleenhetslag:** *EaBoxPl*
    - **Beskrivelse:** *Hver bokspall*

1. Velg **Lagre**.
1. På **Måleenhet**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Enhet:** *Boks*
    - **Beskrivelse:** La dette feltet stå tomt. Den fylles ut automatisk når du lagrer endringene.
    - **Enhetsklasse:** *Antall*

1. Velg **Ny** for å legge til en ny linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Enhet:** *ea*
    - **Beskrivelse:** La dette feltet stå tomt. Den fylles ut automatisk når du lagrer endringene.
    - **Enhetsklasse:** *Antall*

1. Velg **Ny** for å legge til en tredje linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Enhet:** *PL*
    - **Beskrivelse:** La dette feltet stå tomt. Den fylles ut automatisk når du lagrer endringene.
    - **Enhetsklasse:** *Antall*

1. Velg **Lagre** for å lagre laget.

### <a name="create-a-directive-code-for-slotting"></a>Opprette en direktivkode for sporing

Du må velge direktivkoden som skal knyttes til en mal.

1. Gå til **Lagerstyring \> Oppsett \> Direktivkoder**.
1. Velg **Ny** i handlingsruten.
1. I **Direktivkode**-feltet angir du *Sporing*.
1. I **Direktivbeskrivelse**-feltet angir du *Sporing*.

### <a name="set-up-slotting-templates"></a>Definere sporingsmaler

Hver sporingsmal styrer hvordan beholdningen tilordnes lokasjoner for et bestemt lager. Hver mal må inneholde en linje for hver sporingsspesifikasjon. Bruk fremgangsmåtene i denne delen til å definere sporingsmaler.

1. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Sporingsmaler**.
1. Velg **Ny** for å opprette en mal.

Deretter må du definere maltoppteksten, sporingsspesifikasjoner og lokasjonsdirektiver som forklart nedenfor. Oppsettet for sporing for overføringsordrer ligner oppsettet for sporing for salgsordrer, men **Behovstype**-feltet angir *Overføringsordrer* i stedet for *Salgsordre*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Definere hodet for en sporingsmal for salgsordre

1. Angi følgende verdier i toppteksten for malen:

    - **Sporingsmal:** _61_
    - **Beskrivelse:** _61_
    - **Behovstype:** *Salgsordre*

        > [!NOTE]
        > For øyeblikket er *Salgsordrer* og *Overføringsordrer* de eneste behovstypene som støttes. Du kan bare velge *Overføringsordrer* hvis funksjonen *Lagersporing for overføringsordrer* er aktivert.

    - **Behovsstrategi:** _Bestilt_

        Følgende verdier er tilgjengelige i dette feltet:

        - **Bestilt** – hele det bestilte antallet på salgsordren skal vurderes som behov.
        - **Reservert** – bare antallet for salgsordrelinjen som er reservert (fysisk og bestilt), skal vurderes som behov.
        - **Frigitt** – Det frigitte antallet skal vurderes som behov.

    - **Lager:** _61_
    - **Tillat at bølgebehov bruker ikke-reservert antall:** _Ja_

Du kan også angi en spørring for å begrense omfanget av behovet som evalueres.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Definer sporingsspesifikasjoner for hver mal

For hver salgsordremal du oppretter, følger du disse trinnene for å legge til en linje for hver sporingsspesifikasjon.

1. På **Sporingsmaldetaljer**-hurtigfanen velger du **Ny** for å opprette en mallinje.
1. På den nye linjen angir du følgende verdier:

    - **Sekvens:** _1_
    - **Beskrivelse:** _Fast lokasjon_
    - **Minimumsantall:** _1_

        Dette feltet definerer minimumsantall for behov som er nødvendig for linjen.

    - **Maksimalt antall:** _1000000_

        Dette feltet definerer maksimumsantall for behov som er gyldig for linjen.

    - **Enhet:** La dette feltet stå tomt.

        Dette feltet definerer måleenheten som minimums- og maksimumsantallet viser til.

    - **Måleenhetslag:** _EaBoxPl_

        Dette feltet definerer måleenheten for behov som er gyldig for linjen. (Hvis du vil ha mer informasjon, kan du se delen [Opprett måleenhetslag for sporing](#unit-tiers) tidligere i dette emnet.)

    - **Tilordne sporkriterier:** _Vurder antall_

        Følgende verdier er tilgjengelige i dette feltet:

        - **Anta tom** – dette systemet bør anta at alle lokasjonene i plukkområdet er tomme og bør ikke kontrollere disse lokasjonene for beholdning.
        - **Vurder antall** – systemet bør kontrollere lokasjonene i plukkområdet for beholdning og bør hoppe over eventuelle lokasjoner som ikke er tomme.
        - **Vurder beholdning** – Systemet bør kontrollere om en mållokasjon inneholder ikke-reserverte antall for varen på behovslinjen. Hvis antallet er stort nok til å oppfylle minst én enhet for behovs injen, reduseres den genererte sporingsplanposten med det tilgjengelige antallet. Hvis for eksempel behovet er 10 esker, og én eske er på lager, vil behovet som finnes, være ni esker. Hvis behovet er 10 esker, og én eske er på lager, vil behovet som finnes, være 10 esker. Denne verdien er bare tilgjengelig når funksjonen *Forbedringer i tildeling av lagersporing* er aktivert.

    - **Direktivkode:** _Sporing_

        Dette feltet definerer lokasjonsdirektivet som brukes til å finne plukklokasjonen for etterfyllingsarbeidet.

    - **Overflytlokasjon:** La dette feltet stå tomt.

        Dette feltet definerer den lokasjonen som det er satt inn hvis det ikke finnes en lokasjon for antallet når linjen behandles.

    - **Tillat la være:** _Ja_

        Hvis dette alternativet er satt til *Ja*, hvis et behov ikke kan spores, opprettes det bevegelsesarbeid for å få beholdning ut av lokasjoner der det er beholdning, men der ingenting var ble sporet. Malen kjøres deretter på nytt. Denne gangen ignorerer beholdningen på lokasjonene. Denne funksjonaliteten fungerer best når **Tilordne sporkriterier** er satt til _Vurder antall_.

    - **Fast lokasjonsbruk:** _Bare faste lokasjoner for produktet_

        Følgende verdier er tilgjengelige i dette feltet:

        - **Faste og ikke-faste lokasjoner** – systemet bør ikke begrenses til å bruke bare faste lokasjoner.
        - **Bare faste lokasjoner for produktet** – systemet skal bare spore til lokasjoner som er faste lokasjoner for produktet.
        - **Bare faste lokasjoner for produktvarianten** – systemet skal bare spore til lokasjoner som er faste lokasjoner for produktvarianten.

> [!NOTE]
> Hvis sporingsmalen inneholder minst én linje der feltet **Tilordne sporkriterier** er satt til å *Vurder beholdning*, vil ikke Tillat-vinduer være tillatt for noen linjer i malen.

1. Velg **Lagre**.
1. Velg **Ny** for å opprett en ny mallinje.
1. På den nye linjen angir du følgende verdier:

    - **Sekvens:** _2_
    - **Beskrivelse:** _Annet_
    - **Minimumsantall:** _1_
    - **Maksimumsantall:** _1000000_
    - **Enhet:** La dette feltet stå tomt.
    - **Måleenhetslag:** _EaBoxPl_
    - **Tilordne sporkriterier:** _Vurder antall_
    - **Direktivkode:** _Sporing_
    - **Overflytlokasjon:** La dette feltet stå tomt.
    - **Tillat la være:** _Ja_
    - **Bruk faste lokasjoner:** _Faste og ikke-faste lokasjoner_

    I spørringen for den andre linjen vil du nå angi kriteriene som brukes til å bestemme hvilke lokasjoner behovet etter linjen kan spores til.

1. Velg linjen der **Sekvens**-feltet er satt til *2*.
1. Velg **Rediger spørring**.
1. På **Område**-fanen velger du **Legg til** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Avledet tabell:** *Lokasjoner*
    - **Felt:** *ID for lokasjonsprofil*
    - **Kriterier:** *Plukk-06* (Velg dobbelt plusstegn \[**++**\] i feltet for å utvide listen, og velg deretter *Plukk-06* - *Plukkområde 6*.)

1. Velg **OK**.

#### <a name="set-up-location-directives"></a>Konfigurer lokasjonsdirektiver

Minst ett lokasjonsdirektiv må være satt opp for å støtte sporingsplukkinger. Bruk fremgangsmåtene i denne delen til å definere et nytt *lokasjonsdirektiv for etterfylling* for sporingsplukkinger.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I den venstre ruten i **Arbeidsordretype**-feltet velger du *Etterfylling*.
1. Velg **Ny** i handlingsruten.
1. I toppteksten for det nye lokasjonsdirektivet angir *61 Sporingsplukk* i **Navn**-feltet.
1. I feltet **Sekvensnummer** godtar du standardverdien.

##### <a name="configure-the-location-directives-fasttab"></a>Konfigurer Lokasjonsdirektiv-hurtigfanen

1. Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen. Godta standardverdiene for alle de andre feltene.

    - **Arbeidstype:** _Plukk_
    - **Område:** _6_
    - **Lager:** _61_
    - **Direktivkode:** _Sporing_

1. Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.

##### <a name="configure-the-lines-fasttab"></a>Konfigurere Linjer-hurtigfanen

1. På hurtigfanen **Linjer** velger du **Ny** for å opprette en linje.
1. På den nye linjen angir du følgende verdier.

    - **Fra-antall:** _0_
    - **Til antall:** _1000000_

1. Godta standardverdiene for de resterende feltene.
1. Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Konfigurer Handlinger for lokasjonsdirektiv-hurtigfanen

1. På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny** for å opprette en linje.
1. På den nye linjen angir du følgende verdier. Godta standardverdiene for alle de andre feltene.

    - **Sekvensnummer:** Godta standardverdien.
    - **Navn:** _Bulk_
    - **Strategi:** _Ingen_

1. Godta standardverdiene for de resterende feltene.
1. Velg **Lagre** for å aktivere **Rediger spørring**-knappen.

##### <a name="edit-the-query"></a>Rediger spørringen

1. I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.
1. På **Område**-fanen velger du **Legg til** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Avledet tabell:** *Lokasjoner*
    - **Felt:** *Sone-ID*
    - **Kriterier:** *Bulk* (Velg dobbelt plusstegn \[**++**\] i feltet for å utvide listen, og velg deretter *Bulk*.)

1. Velg **OK**.

## <a name="scenario"></a>Scenario

### <a name="set-up-the-scenario"></a>Definer scenariet

I dette scenariet bruker du de innebygde eksempeldataene, og oppretter postene som er beskrevet i denne delen.

#### <a name="use-the-usmf-sample-data"></a>Bruke USMF-eksempeldataene

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

#### <a name="create-demand"></a>Opprette behov

Følg denne fremgangsmåten for å opprette behovet du vil bruke sporing på.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du _US-007_.
1. I **Lager**-feltet velger du _61_.
1. Velg **OK**.
1. Den nye salgsordren åpnes. Det inneholder en tom linje på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Vare:** _L0101_
    - **Antall:** _20_

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Vare:** _T0100_
    - **Antall:** _8_

1. Velg **Lagre**.
1. Velg **Ny** for å opprette en ny salgsordre.
1. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du _US-008_.
1. I **Lager**-feltet velger du _61_.
1. Den nye salgsordren åpnes. Det inneholder en tom linje på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Vare:** _T0100_
    - **Antall:** _1_

1. Velg **Lagre**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Gå gjennom et vanlig sporingsscenario

Når alle forutsetningselementene er på plass, som beskrevet i den forrige delen, er du klar til å prøve ut funksjonen ved å jobbe gjennom hver øvelse i denne delen.

#### <a name="generate-demand"></a>Generer behov

1. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Sporingsmaler**, og velg sporingsmalen du opprettet tidligere.
1. Velg **Generelt behov** i handlingsruten. Denne kommandoen evaluerer alle behov som er i systemet, og som samsvarer med sporingsmalspørringen. Det totale behovet på tvers av alle ordrer konsolideres deretter på én linje per antall/måleenhet. En informasjonsmelding vises når prosessen er fullført.

#### <a name="slotting-demand"></a>Sporingsbehov

*Sporingsbehovet* viser resultatene av behovsgenerering, basert på oppsettet til sporingsmalen.

- I handlingsruten velger **Sporingsbehov** for å vise resultatene fra **Generelt behov**-kommandoen. Linjene i sporingsbehov kan redigeres. Du kan slette en linje, legge til en ny linje eller redigere linjedetaljene.

> [!NOTE]
> Du kan redigere behovet manuelt, eller du kan importere den fra et eksternt system ved hjelp av dataadministrasjon. Det som er oppgitt i sporingsbehov, vil bli brukt i neste trinn, uansett hvor den kom fra.

#### <a name="locate-demand"></a>Finn behov

Etter at behov er generert, må du bruke **Finn behov**-kommandoen til å generere *sporingsplanen*.

- Velg **Finn behov** i handlingsruten. Sporingsprosessen kjører. En informasjonsmelding vises når prosessen er fullført.

#### <a name="slotting-plan"></a>Sporingsplan

Sporingsplanen viser lokasjonen som hver vare/antall ble tilordnet til, om overflyt ble brukt, om det ble opprettet en arbeidslinje og mallinjen som ble brukt. *Alle etterspørsler som ikke kunne spores, er uthevet i rødt.*

- I handlingsruten velger **Sporingsplan** for å vise resultatene.

> [!NOTE]
> - Prosessene **Generer behov**, **Finn behov** og **Kjør etterfylling** er nå i en sandkasse. (Disse prosessene er tilgjengelige fra handlingsruten på siden **Sporingsmaler**.)
> - Prosessene **Generer behov**, **Finn behov** og **Kjør etterfylling** for å sikre at de ikke kan utløses samtidig. Ellers kan dataene som brukes, bli slettes.
> - Prosessene **Generer behov** og **Finn behov** viser en advarsel hvis kjøringen ikke genererte poster, eller hvis postene mangler informasjon.
> - Når du velger **Sporingsplan**, har ikke siden knappene **Ny**, **Rediger** eller **Slett** i handlingsruten, fordi datakilden ikke kan redigeres.
> - Når du velger **Kjør etterfylling**, validerer systemet den valgte spormalen og prosessene.

#### <a name="create-replenishment"></a>Opprett etterfylling

Etter at sporingsplanen er opprettet, må du opprette *Etterfyllingsarbeid*, basert på planen.

- Velg **Kjør etterfylling** i handlingsruten. En informasjonsmelding vises når prosessen er fullført. Denne meldingen angir antallet hoder som ble opprettet for build-ID-en for arbeid.

Lokasjonsdirektiver som vil bli brukt, identifiseres basert på direktivkoden som er angitt på hver mallinje.

## <a name="tips"></a>Tips!

### <a name="set-up-automatic-slotting"></a>Definere automatisk sporing

Når alle nødvendige elementer er på plass, kan du konfigurere sporing til å kjøre automatisk ved å følge disse trinnene.

1. Gå til **Lagerstyring \> Etterfylling \> Kjør sporing**.
1. Angi sporingstrinn som skal kjøres. Velg ett eller flere av følgende sporingstrinn:

    - Generer behov
    - Finn behov
    - Opprett etterfyllingsarbeid

    > [!NOTE]
    > Sporingstrinnene er progressive. Hvis du vil velge *Finn behov*, må du først velge *Generer behov*.

1. Angi hvilken sporingsmal som skal brukes.
1. Angi at regelmessigheten skal kjøres automatisk hvis du vil.

For øvelsene i scenarioet må du **ikke** sette opp automatisk sporing.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]