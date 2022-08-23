---
title: Kvalitetskontroll
description: Denne artikkelen inneholder informasjon om funksjonen Kvalitetskontroll. Denne funksjonen gjør det mulig for lagermedarbeidere å utføre stikkprøver for kvalitet når de mottar varer i mottakssonen.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: bc0e911eeccd1d4700f1f4daefd5fe1a4935cd80
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218720"
---
# <a name="quality-check"></a>Kvalitetskontroll

[!include [banner](../includes/banner.md)]

Funksjonen *Kvalitetskontroll* gjør det mulig for lagermedarbeidere å utføre stikkprøver for kvalitet når de mottar varer i mottakssonen. Disse stikkprøvene er nyttige når ansatte undersøker emballasje eller andre lett gjenkjennelige deler av en vare. Funksjonen hjelper medarbeidere med å ta et raskt blikk på å se om noe er åpenbart feil eller skadet før de lagrer beholdningen på plasseringsstsedet.

Denne funksjonen er et alternativ til standard kvalitetskontrollprosess. Den gir større fleksibilitet og raskere behandling.

Når du bruker denne funksjonen, skjer ankomsten og kvalitetskontrollen på følgende måte:

1. Når en forsendelse ankommer, registrerer en lagerarbeider ankomsten. Arbeideren skanner også et nummerskilt for å registrere lokasjonen.
1. Arbeideren utfører en hurtig kvalitetskontroll og registrerer resultatet (bestått eller mislykket) for dette nummerskiltet.
1. En av følgende handlinger inntreffer:

    - Hvis kvalitetskontrollen bestås, godtas nummerskiltet og rutes til en mottakslokasjon, som vanlig.
    - Hvis kvalitetskontrollen mislykkes, avvises nummerskiltet og eksisterende plasseringsarbeid for det blir omadressert til en alternativ lokasjon for videre inspeksjon. Det opprettes en ny kvalitetsordre. Hvis du vil vise kvalitetsordren som ble opprettet fra den mislykkede kvalitetskontrollen, går du til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.

Denne prosessen kan også konfigureres slik at alle skannede nummerskilt sendes umiddelbart til kvalitetskontrollokasjonen.

## <a name="turn-the-quality-check-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Kvalitetskontroll

Du må aktivere funksjonen *Kvalitetskontroll* for systemet for å kunne bruke funksjonaliteten som beskrives i denne artikkelen. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Kvalitetskontroll* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-the-feature-for-the-example-scenario"></a>Konfigurer funksjonen for eksempelscenarioet

Denne delen inneholder retningslinjer og et eksempel som viser hvordan du definerer funksjonen *Kvalitetskontroll* og klargjør eksempeldata foreksempel scenarioet som er oppgitt senere i denne artikkelen.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette [eksempelscenarioet](#example-scenario) ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

### <a name="quality-check-template"></a><a name="quality-template"></a>Mal for kvalitetskontroll

Kvalitetskontrollmalen definerer reglene for å utføre stikkprøver for kvalitet på det tidspunktet du mottar.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Kvalitetskontrollmal**.
1. Velg **Ny** for å legge til en mal i rutenettet.
1. Angi følgende verdier for å definere den nye malen:

    - **Navn på kvalitetskontrollmal:** *Dock-kontroll*

        Angi et navn som identifiserer policyene som brukes for denne malen.

    - **Godkjenningspolicy:** *Spør bruker*

        Angi om brukere skal bli bedt om å godta eller avvise kvaliteten på beholdningen mens de behandler arbeidet, eller om kvaliteten skal avvises automatisk. De tilgjengelige alternativene er *Avvis automatisk* og *Spør bruker*.

    - **Policy for kvalitetsbehandling:** *Opprett kvalitetsordre*

        Velg policyen som skal brukes når kvaliteten på beholdningen avvises. Følgende alternativer er tilgjengelige:

        - *Opprett bare arbeid* – Opprett bare arbeid for å gjøre beholdningsbevegelser enklere.
        - *Opprett kvalitetsordre* – Opprett en kvalitets ordre for å forenkle kvalitetstester.

    - **Testgruppe:** *Omslutning*

        Angi testgruppen som skal brukes i kvalitetsordren som opprettes. Testgrupper blir definert i **Lagerstyring**-modulen.

        La alternativet **Destruktiv tekst** være slått av for testgruppen. Dette alternativet definerer om prøven skal ødelegges som del av testene i testgruppen. Når en destruktiv test brukes, genererer system en beholdningstransaksjon der en kvalitetsordre opprettes for en vare. Den nye lagertransaksjonen forutsier lagerreduksjonen for testantallet. Beholdningsreduksjonen skjer når kvalitetsordren er fullført gjennom valideringstrinnet. Lagertransaksjonen identifiseres som en kvalitetsordre.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Arbeidsklasse – kvalitetskontroll

Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som lagermedarbeidere kan behandle på en mobil enhet.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.
1. Velg **Ny** for å opprette en arbeidsklasse.
1. I hodet angir du følgende verdier:

    - **Arbeidsklasse-ID:** *Kvalitetskontroll*

        Angi et navn som identifiserer arbeidsklassen.

    - **Beskrivelse:** *Kvalitetskontroll*

        Angi en kort beskrivelse som angir hva arbeidsklassen brukes for.

    - **Arbeidsordretype:** *Kvalitetskontroll*

        Velg typen arbeidsordre som opprettes av arbeidsklassen. Når du definerer arbeid for kvalitetskontroll, velger du alltid *Kvalitet i kvalitetskontroll*.

1. På hurtigfanen **Gyldige plasseringslokasjonstyper** lar du feltet **Lokasjonstype** være tomt.

    Hvis du velger en lokasjonstype, begrenser du lokasjonene der varer kan legges etter at de er plukket. Dette feltet brukes når et lokasjonsdirektiv forsøker å løse lokasjonen, eller når en lagermedarbeider angir lokasjonen for menyelementet for mobilenheten manuelt.

Hvis du vil ha mer informasjon om arbeidsklasser og hvordan du oppretter dem, kan du se [Opprette en arbeidsklasse](tasks/create-work-class.md).

### <a name="work-template"></a>Arbeidsmal

Med arbeidsmaler kan du definere arbeidsoperasjoner som må utføres på lageret. Vanligvis består lageroperasjoner av to handlinger: en lagerarbeider plukker opp beholdning på en lokasjon og plasserer den plukkede beholdningen på en annen lokasjon. En arbeidsmal for kvalitetskontroll definerer arbeidsoperasjonene for å utføre kvalitetskontroller.

#### <a name="purchase-orders"></a>Bestillinger

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. I hodet setter du *Arbeidsordretype*-feltet til **Bestillinger**.
1. I handlingsruten velger du **Rediger**.
1. Velg en arbeidsmal som skal inneholde et kvalitetskontrolltrinn. I **Oversikt**-delen i **Arbeidsmal**-feltet velger du *51 bestillingsmottak*.
1. I delen **Arbeidsmaldetaljer** ser du at rutenettet har to eksisterende linjer: én for *plukking* og én for *plassering*.
1. i delen **Arbeidsmaldetaljer** velger du **Ny** for å legge til en rad for kvalitetskontroll i rutenettet. Legg merke til at **Linjenummer**-feltet for den nye linjen er satt til *3*.
1. På den nye linjen angir du følgende verdier. Godta standardverdiene for de resterende feltene.

    - **Arbeidstype:** *Kvalitetskontroll*
    - **Arbeidsklasse-ID:** *Kjøp*
    - **Navn på kvalitetskontrollmal:** *Dock-kontroll*

        Velg den unike IDen for arbeidsklassen. Du bruker denne verdien til å konfigurere menyelementene på den mobile enheten og typene arbeid som disse menyelementene kan behandle.

1. I handlingsruten velger du **Lagre** for å lagre arbeidet så langt.

    Du mottar en informasjonsmelding som sier "Ugyldig – kvalitetskontroll må komme direkte etter en plukking". Derfor må du endre **Linjenummer**-verdien for linjen du nettopp la til.

1. Følg disse trinnene for å endre **Linjenummer**-verdien for den nye linjen:

    1. I delen **Arbeidsmaldetaljer** velger du linjen hvor **Arbeidstype**-feltet er satt til *Kvalitetskontroll*.
    2. Velg knappen **Flytt opp** eller **Flytt ned** for å flytte *Kvalitetskontroll*-linjen slik at den er etter *Plukl*-linjen.

1. Velg **Lagre** i handlingsruten.

#### <a name="quality-in-quality-check"></a>Kvalitet i kvalitetskontroll

Deretter oppretter du en arbeidsmal for kvalitetskontrollen.

1. I hodet på **Arbeidsmaler**-siden endrer du verdien på **Arbeidsordretype**-feltet til *Kvalitetskontroll*.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet i **Oversikt**-delen.
1. I den nye raden angir du følgende verdier:

    - **Arbeidsmal:** *51 kvalitetskontroll*

        Angi et navn for malen.

    - **Beskrivelse av arbeidsmal:** *51 kvalitetskontroll*

1. I handlingsruten velger du **Lagre** for å gjøre **Arbeidsmaldetaljer**-delen tilgjengelig.
1. Mens den nye malen fortsatt er valgt i **Oversikt**-delen, velger du **Ny** i delen **Arbeidsmaldetaljer** for å legge til en rad i rutenettet der.
1. I den nye raden angir du følgende verdier:

    - **Arbeidstype:** *Plukk*
    - **Arbeidsklasse-ID:** *Kvalitetskontroll*

        Velg navnet på [arbeidsklassen](#work-class) som du opprettet tidligere for kvalitetskontrollarbeid.

1. I delen **Arbeidsmaldetaljer** velger du **Ny** igjen for å legge til en annen rad.
1. I den nye raden angir du følgende verdier:

    - **Arbeidstype:** *Plasser*
    - **Arbeidsklasse-ID:** *Kvalitetskontroll*

        Velg navnet på [arbeidsklassen](#work-class) som du opprettet tidligere for kvalitetskontrollarbeid.

1. Velg **Lagre** i handlingsruten.

Hvis du vil ha mer informasjon om arbeidsmaler, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).

### <a name="location-directive--quality-failures"></a>Lokasjonsdirektiv – kvalitetsfeil

Lokasjonsdirektiver er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. I en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varene blir plukket og hvor de plukkede varene skal plasseres. Du må konfigurere en lokasjonsdirektivregel for å definere hvordan mislykkede kvalitetskontroller skal behandles.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I den venstre ruten angir du **Arbeidsordretype**-feltet til *Bestillinger* for å arbeide med lokasjonsdirektiver av denne typen.
1. Velg **Ny** i handlingsruten for å opprette et lokasjonsdirektiv for kvalitetskontroller.
1. I hodet angir du følgende verdier:

    - **Sekvensnummer:** Godta standardverdien.
    - **Navn:** *51 til kvalitet*

1. Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen. Godta standardverdiene for de resterende feltene.

    - **Arbeidstype:** *Plasser*
    - **Område:** *5*
    - **Lager:** *51*

1. I handlingsruten velger du **Lagre** for å lagre direktivet og gjøre hurtigfanen **Linjer** tilgjengelig.
1. På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier. Godta standardverdiene for de resterende feltene.

    - **Fra-antall:** *1*
    - **Til-antall:** *1000000*

1. I handlingsruten velger du **Lagre** for å lagre den nye linjen og gjøre hurtigfanen **Handlinger for lokasjonsdirektiv** tilgjengelig.
1. Mens den nye linjen fremdeles er valgt på hurtigfanen **Linjer**, velger du **Ny** på hurtigfanen **Handlinger for lokasjonsdirektiv** for å legge til en rad i rutenettet der, slik at du kan definere en handling for linjen.
1. I den nye raden setter du **Navn**-feltet til *Kvalitet*. Godta standardverdiene for de resterende feltene.
1. I handligsruten velger du **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.
1. Når linjen du nettopp la til, fremdeles er valgt i hurtigfanen **Handlinger for lokasjonsdirektiv**, velger du **Rediger spørring** for å åpne en dialogboks der du kan redigere spørringen for handlingen.
1. På **Område**-fanen velger du **Legg til** for å legge til en rad i spørringen.
1. I den nye raden angir du følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Avledet tabell:** *Lokasjoner*
    - **Felt:** *Lokasjon*
    - **Vilkår:** *QMS*

    *QMS*-lokasjonen er en lagerlokasjon for kvalitet.

1. Velg **OK** for å lukke dialogboksen.
1. Du må nå endre rekkefølgen til lokasjonsdirektivene for bestilling for lager *51*. Lagre det nye lokasjonsdirektivet *51 til kvalitet*, oppdater siden og velg lokasjonsdirektivet i listen. Deretter bruker du knappene **Flytt opp** og **Flytt ned** i handlingsruten til å plassere lokasjonsdirektivet for lager *51* i følgende rekkefølge. (Før du velger **Flytt opp** eller **Flytt ned**, må du velge et lokasjonsdirektiv i listen.)

    1. 51 til kvalitet
    2. 51 bestilling direkte
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Menyelementer på mobilenheten

Konfigurer et menyelement slik at mobilenheter kan utføre **Kvalitetskontroll**-funksjonen.

#### <a name="purchase-putaway"></a>Kjøpsplassering

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg menyelementet **Kjøpsplassering** i listen.
1. I handlingsruten velger du **Rediger**.
1. I **Arbeidsklasser**-delenvelger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier:

    - **Arbeidsklasse-ID:** *Kvalitetskontroll*

        Angi navnet på [arbeidsklassen](#work-class) som du opprettet tidligere for kvalitetskontrollarbeid.

    - **Arbeidsordretype:** *Kvalitetskontroll*

1. Velg **Lagre** i handlingsruten.

#### <a name="purchase-order-line-receiving"></a>Mottak av bestillingslinje

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I hodet angir du følgende verdier:

    - **Menyelementnavn:** *PO-linjemottak*
    - **Tittel:** *PO-linjemottak*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Nei*

1. Angi følgende verdier i **Generelt**-hurtigfanen. Godta standardverdiene for de resterende feltene.

    - **Arbeidsopprettingsprosess:** *Bestillingslinjemottak og -plassering*
    - **Generer nummerskilt:** *Ja*
    - **Arbeidsmal:** *51 bestillingsmottak*

1. Velg **Lagre** i handlingsruten.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Legge til menyelementet på en meny for mobilenhet

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Innkommende**-,'menyen i den venstre ruten.
1. I handlingsruten velger du **Rediger**.
1. I kolonnen **Tilgjengelige menyer og menyelementer** velger du det nye menyelementet **PO-linjemottak**.
1. Velg høyre pil-knappen for å flytte **PO-linjemottak** til kolonnen **Menystruktur**.
1. I kolonnen **Menystruktur** velger du **PO-linjemottak**, og deretter velger du pil opp eller pil ned for å flytte menyelementet til ønsket plassering på menyen på mobilenheten.
1. Velg **Lagre** i handlingsruten.

## <a name="example-scenario"></a><a name="example-scenario"></a>Eksempelscenario

Etter at du har gjort alle de tidligere beskrevne eksempeldataene tilgjengelige og konfigurert dem, kan du arbeide deg gjennom dette scenariet for å prøve ut *Kvalitetskontroll*-funksjonen. Verdiene som vises i dette scenariet, antar at du arbeider med standard demonstrasjonsdata, at du har valgt den juridiske enheten **USMF**, og at du klargjorde eksempelpostene som er beskrevet tidligere i denne artikkelen. Dette scenariet fungerer også som et eksempel som viser hvordan funksjonen kan brukes i et produksjonsmiljø.

### <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett bestilling**-dialogboksen angir du følgende verdier:

    - **Leverandørkonto:** *104*
    - **Lager:** *51*

1. Velg **OK** for å lukke dialogboksen og opprette den nye bestillingen.
1. På hurtigfanen **Bestillingslinjer** inneholder rutenettet en ny, tom linje. På denne linjen angir du følgende verdier:

    - **Varenummer:** *M9203*
    - **Antall:** *3*
    - **Enhet:** *PL*

1. Velg **Lagre** i handlingsruten.

### <a name="process-quality-check-receiving"></a>Behandle kvalitetskontrollmottak

Når bestillingen er opprettet, kan den mottas ved hjelp av menyelementet **PO-linjemottak** og funksjonaliteten i *Kvalitetskontroll*-funksjonen.

#### <a name="receive-pallet-1"></a>Motta pall 1

1. Logg på mobilappen Lagerstyring som en bruker som er aktivert for lager *51*. (Angi *51* som bruker-ID og *1* som passord.)
1. Gå til **Innkommende \> PO-linjemottak**.
1. I **PONUM**-feltet angir du bestillingsnummeret.
1. Bekreft bestillingsnummeret.
1. I **LINENUM**-feltet angir du nummeret på bestillingslinjen som mottas. Fordi ordren bare har én linje i dette scenariet, vil du angi *1* i **LINENUM**-feltet for hvert mottakstrinn.
1. Bekreft linjenummeret.
1. I **QTY**-feltet angir du antallet som skal mottas. Fordi bestillingen er for tre paller (*PL*) i dette scenariet, og det er tremottaks trinn, angir du *1* i **QTY**-feltet for hvert mottakstrinn.
1. Bekreft antallet.

    Siden **Kvalitetskontroll** som vises, har ingen oppføringsfelt. Den har bare bekreftelsesknappen (hakemerke) nederst og menyknappen (**≡**) øverst. (Meny-knappen kalles noen ganger for hamburgeren eller hamburgerknappen.) Hvis du vil ekspedere kvalitetskontrollprosessen, må brukere bare bekrefte siden **Kvalitetskontroll** når pallen består kvalitetskontrollen.

    ![Siden Kvalitetskontroll.](media/quality-check.png "Siden Kvalitetskontroll")

1. Velg bekreftelsesknappen for å bestå kvalitetskontrollen for pall 1 fra linje 1.

    Siden **Bestillinger: Plasser** som vises, viser detaljer om plasseringsarbeidet:

    - **LOC:** Plasseringen som systemet har fastslått

        Denne lokasjonen er den tilordnede plasseringslokasjonen for bestillingsmottak.

    - **LP:** Den systemgenererte nummerskilt-ID-en
    - **Vare:** *M9203*
    - **Ant.:** *1 PL: 100 per stk*

    Varebeskrivelsen vises også.

1. Bekreft plasseringsarbeidet.

    På **Oppgave**-siden for bestillingslinjemottak vises meldingen "Arbeid fullført". **LINENUM**-feltet er tilgjengelig, slik at du kan begynne å motta den neste pallen.

#### <a name="receive-pallet-2"></a>Motta pall 2

For dette scenariet vil pall 2 bli avvist.

1. I **LINENUM**-feltet angir du *1* og bekrefter linjenummeret.
1. **QTY**-feltet er nå tilgjengelig. Angi *1*, og bekreft antallet.

    Siden **Kvalitetskontroll** vises. For dette mottaket vil pallen bli avvist for kvalitet, og den vil plasseres i *QMS*-kvalitetslokasjonen.

1. Velg menyknappen (**≡**) øverst på siden, og velg deretter **Avvis** på menyen.
1. På **Oppgave**-siden som vises, angir du **QMS** som *Plassering*-lokasjon å sende pallen til for videre inspeksjon.

    Siden **Kvalitet i kvalitetskontroll: Plasser** som vises, viser detaljer om plasseringsarbeidet:

    - **LOC:** *QMS*

        Denne lokasjonen er den tilordnede plasseringslokasjonen for mottak med avvist kvalitet.

    - **LP:** Den systemgenererte nummerskilt-ID-en
    - **Vare:** *M9203*
    - **Ant.:** *1 PL: 100 per stk*

    Varebeskrivelsen vises også.

1. Bekreft plasseringsarbeidet.

    På **Oppgave**-siden for bestillingslinjemottak vises meldingen "Arbeid fullført". **LINENUM**-feltet er tilgjengelig, slik at du kan begynne å motta den neste pallen.

Du har nå fullført kvalitetskontrollen og opprettet en kvalitetsordre for den avviste pallen. Hvis du vil vise ordren som ble opprettet, går du til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.

Testing av kvalitetsordre kan nå behandles. Kvalitetstesting dekkes ikke i denne artikkelen.

Hvis du vil ha mer informasjon om kvalitetsbehandling, kan du se [Oversikt over kvalitetsbehandling](../inventory/enable-quality-management.md).

#### <a name="receive-pallet-3"></a>Motta pall 3

For dette scenariet vil pall 3 bli godtatt.

1. I **LINENUM**-feltet angir du *1* og bekrefter linjenummeret.
1. **QTY**-feltet er nå tilgjengelig. Angi *1*, og bekreft antallet.

    Siden **Kvalitetskontroll** vises. For dette mottaket vil pallen bli godtatt for kvalitet, og den vil plasseres i en samlet plasseringslokasjon.

1. Velg bekreftelsesknappen for å bestå kvalitetskontrollen.

    Siden **Bestillinger: Plasser** som vises, viser detaljer om plasseringsarbeidet:

    - **LOC:** Plasseringen som systemet har fastslått

        Denne lokasjonen er den tilordnede plasseringslokasjonen for bestillingsmottak.

    - **LP:** Den systemgenererte nummerskilt-ID-en
    - **Vare:** *M9203*
    - **Ant.:** *1 PL: 100 per stk*

    Varebeskrivelsen vises også.

1. Bekreft plasseringsarbeidet.

    På **Oppgave**-siden for bestillingslinjemottak vises meldingen "Arbeid fullført". **LINENUM**-feltet er tilgjengelig, slik at du kan begynne å motta den neste pallen.

1. Velg menyknappen (**≡**) øverst på siden, og velg deretter **Avbryt** for å gå tilbake til menyen.

Du kan nå lukke mobilappen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]