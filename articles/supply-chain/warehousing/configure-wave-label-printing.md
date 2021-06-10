---
title: Bølgeetikettutskrift
description: Dette emnet beskriver bølgeetikettutskrift og forklarer hvordan du konfigurerer den.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 14a32f7fc4608ef8910646f80786a188c46dc89d
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102620"
---
# <a name="wave-label-printing"></a>Bølgeetikettutskrift

[!include [banner](../includes/banner.md)]

Bølgeetikettutskrift gir en alternativ tilnærming til etikettutskrift ved å introdusere en ny bølgetrinnmetode som lar deg opprette og skrive ut etiketter direkte fra bølgemalen under bølgekjøring. Etikettene vil derfor allerede være tilgjengelige før de ansatte kjører arbeidsordren på en mobil enhet. Arbeidere kan deretter knytte de nødvendige etikettene til under plukking i stedet for etter plukking.

Bølgeetikettutskrift bruker Zebra Programming Language (ZPL) til å opprette etikettoppsett. Et etikettoppsett er delt inn i tre inndelinger (topptekst, brødtekst og bunntekst) for å tillate etiketter som har gjentatt struktur. Maler for bølgeetiketter forteller systemet hvilket etikettoppsett som skal brukes. Brukere kan angi hvilken skriver som skal brukes. De kan også skrive ut etiketter på flere skrivere samtidig, i henhold til hva de trenger. Siden for **Bølgeetikettlogg** viser en oversikt over alle etiketter som er opprettet ved hjelp av dette oppsettet.

Du kan skrive ut og sortere etiketter basert på arbeidshoder, du kan skrive ut pauseetiketter per arbeidshode, og du kan skrive ut containerinnholdsetiketter, saksetiketter og andre lignende etiketter.

> [!NOTE]
> Denne funksjonaliteten erstatter ikke eksisterende etikettutskriftsfunksjoner som er basert på dokumentruting.

Bølgeetikettutskriftt gir følgende forbedringer:

- Skriv ut etiketter i henhold til antallet kartonger på én enkelt arbeidslinje, uten containerbruk. (En "kartong" er en enhet som er angitt på linjer for sekvensgrupper for enhet.)
- Skriv ut flere forskjellige etikettsekvenser (for eksempel kartong- og palletiketter).
- Inkluder etikettopplisting (for eksempel 1/124, 2/124, ... 124/124), og definer området for opplistingen (for eksempel arbeidslinje, lastlinje eller forsendelse).
- Opprett og skriv ut en fraktbrev-ID på etiketter før fraktbrevet genereres.
- Opprett en unik SSCC (serial shipping container code) for hver kartong, og ta den med på hver etikett.
- Opprett GS1-kompatible nummerserier for fraktbrev-IDer og SSCCer.
- Skriv ut etiketter både fra mobile enheter og den rike klienten.
- Annuller etiketter (for eksempel i scenarioer med plukk med mangler), og skrive dem ut på nytt.
- Rydde opp i bølgeetikettloggen.
- Forbedringer i dokumentrutingsoppsett deles mellom dokumentrutingsoppsett og bølgeetikettoppsett. (Hvis du vil ha mer informasjon, se [Dokumentrutingsoppsett for nummerskiltetiketter](../warehousing/document-routing-layout-for-license-plates.md).)

Disse forbedringene gjør det mer effektivt å merke kartonger før lagring på paller. De er spesielt nyttige for firmaer som leverer til store forhandlere som bekrefter ordremottak automatisk ved å skanne hver kartong separat.

> [!NOTE]
> Du kan implementere konfigurasjonsscenarioene som er beskrevet i dette emnet, enten separat eller i kombinasjon, avhengig av dine forretningsbehov. Du kan utforme flere bølgeetikettmaler som fungerer i rekkefølge (som illustrert i scenario 3). Du kan for eksempel bruke scenario 1 til å skrive ut kartongetiketter og scenario 2 for å skrive ut palletiketter (hvis paller på lager varierer i størrelse og sammensetning).

## <a name="turn-on-the-wave-label-printing-feature"></a>Aktivere funksjonen Bølgeetikettutskrift

Før du kan bruke *Bølgeetikettutskrift*-funksjonen, må den aktiveres i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Bølgeetikettutskrift*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Scenario 1: Bølgeetikettutskrift der det genereres en enkelt bølgeetikett

Dette scenariet viser hvordan et firma kan skrive ut forsendelsesetiketter for en stor forhandler som automatisk bekrefter ordremottak ved å skanne hver kartong separat.

Dette scenariet viser ende-til-ende-flyten.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Kontrollere at bølgeetikettmetoden er tilgjengelig

Det kan hende du må generere metodene for bølgebehandling på nytt for å gjøre metoden for bølgeetikettutskrift tilgjengelig.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.
1. Bekreft at **waveLabelPrinting** er i listen. Hvis den ikke er det, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.

### <a name="configure-a-wave-template"></a>Konfigurere en bølgemal

Med bølgemaler kan du koble bestemte forekomster av bølgemetoder til en tilsvarende bølgeetikettmal.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. Velg en mal, for eksempel **62 Standardforsendelse**.
1. I hurtigfanen **Metoder** flytter du metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder**.
1. I kolonnen **Valgte metoder** velger du metoden **Bølgeetikettutskrift** og setter feltet **Bølgetrinnkode** til *PrintLabel*. For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Opprette et oppsett for bølgeetikett

Etikettoppsettet kontrollerer hvilken informasjon som skrives ut på etiketten, og hvordan den er satt opp. Her angir du ZPL-koden som sendes til skriveren.

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetikettoppsett**.
1. Opprett en post som har følgende innstillinger:

    - **Etikettoppsett-ID:** *Kartong*
    - **Beskrivelse:** *Kartong (SSCC)*

1. Velg **Lagre** i handlingsruten.
1. I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.

    Siden for **Radinnstillinger for bølgeetikett** vises. Her kan du konfigurere den dynamiske delen av etiketten.

1. Legg til en rad som har følgende innstillinger:

    - **Rad-ID:** *WaveLabel*
    - **Navn på radtabell:** *WHSWaveLabel*
    - **Startposisjon for rad:** *0*

        Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.

    - **Radhøyde:** *0*

        Dette feltet definerer høyden på hver rad (i punkter) i henhold til ZPL-standarden. Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter. Fordi det bare er én rad i dette eksemplet, kan du sette verdien til *0* (null).

    - **Rader per side:** *1*

        Dette feltet definerer antallet rader som kan skrives ut på hver etikett.

        > [!NOTE]
        > Dette oppsettet vil føre til at det skrives ut en egen ZPL-etikett for hver post i bølgeetikettabellen.

1. Lukk siden.
1. I handlingsruten velger du **Rediger spørring**.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Arbeidstype*
    - **Kriterier:** *Plukk*

    Denne spørringen sikrer at bare arbeidslinjer av plukktypen blir skrevet ut på etiketten, ikke plasser-arbeidslinjer.

1. Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du fanen **Sammenkoblinger**, velger tabellen **Arbeidslinjer** og kobler **Forsendelser**-tabellen til den.
1. Lukk dialogboksen for redigeringsprogram for spørring.
1. Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen**, **brødtekstdelen** og **bunntekstdelen**. I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten. Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten. Her er et eksempel:

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten. Her er et eksempel:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Dette oppsettet skriver bare ut én kopi av hver etikett. Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n**-verdien for **\^PQn**-delen i bunnteskten til det nødvendige antallet eksemplarer. Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.

Etiketten er nå klar til bruk.

### <a name="create-a-wave-label-type"></a>Opprette en type bølgeetikett

Bølgeetiketttyper brukes til å koble bølgeetikettmaler til en enhet på enhetssekvensgruppelinjer.

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetiketttyper**.
1. Legg til bølgeetikettype som har følgende innstillinger:

    - **Etikettype:** *Kartong*
    - **Beskrivelse:** *Kartong*

### <a name="set-up-unit-sequence-groups"></a>Konfigurer sekvensgrupper for enheter

Deretter definerer du enhetsseriegruppen for bølgeetikettypen.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Sekvensgrupper for enhet**.
1. Velg gruppen **Ea Box PL**.
1. For **Boks** angir du feltet **Bølgenivåtype** til *Kartong*.

### <a name="create-a-wave-label-template"></a>Opprette en mal for bølgeetikett

Deretter oppretter du bølgeetikettmalen for bølgeetikettypen.

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter**.
1. Legg til en bølgenivåmal, og angi følgende verdier i toppteksten:

    - **Etikettmalnavn:** *Kartongetiketter*
    - **Beskrivelse:** *Kartongetiketter*
    - **Bølgetrinnkode:** *PrintLabel*
    - **Lager:** *62*

1. I hurtigfanen **Generelt** angir du feltet **Bølgeetiketttype**-feltet til *Kartong*.
1. I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en ny rad med følgende innstillinger:

    - **Etikettoppsett-ID:** *Kartong*
    - **Skrivernavn:** Velg en passende ZPL-skriver.
    - **Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)

1. Velg **Lagre** i handlingsruten.
1. Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto. På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**. Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Forsendelser*
    - **Avledet tabell:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angi det aktuelle kundekontonummeret.

    Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.

1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogrammet for spørringen for hele etikettmalen.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Sortering**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Linje-ID for referanselast (post-ID)*
    - **Søkeretning:** *Stigende*

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. En meldingsboks ber deg bekrefte gjenopprettingsoperasjonen for gruppering. Klikk på **Ja** for å fortsette.
1. Velg **Malgruppe for bølgeetikett** i handlingsruten.
1. I dialogboksen **Malgruppe for bølgeetikett** velger du raden der feltet **Referansefeltnavn** er satt til *Linje-ID for referanselast*, og deretter merker du av for **Etikettversjons-ID** for denne raden.

    > [!NOTE]
    > Dette oppsettet vil opprette én etikettsekvens ("Kartong 1 av X") per lastlinje gjennom bølgen, uansett oppsett for arbeidsgruppering. Denne etikettsekvensen kan skrives ut på etikettoppsettet.

### <a name="configure-number-sequence-extensions"></a>Konfigurere nummerserieutvidelser

Nummerserieutvidelser kontrollerer GS1-samsvar for bestemte nummerserier. Denne konfigurasjonen er valgfri for det gjeldende scenariet. Du finner mer informasjon og konfigurasjonsinstruksjoner under [Konfigurere nummerserieutvidelser](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Opprette en salgsordre og frigi den til lageret

1. Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.
1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Lager:** *62*

1. Legg til to salgsordrelinjer som har følgende innstillinger:

    - Salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *9024*
        - **Enhet:** *ea* (9024 ea = 376 Box = 47 PL)

    - Salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *9016*
        - **Enhet:** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Varene og antallene som beskrives her, er bare eksempler. De må bruke enhetsseriegruppen du definerte tidligere, riktige enhetskonverteringer fra *ea* til *Box* til *PL* må være definert for dem, og de må ha lager i lageret *62*. Hvis du vil ha mer informasjon, kan du se [Måleenhet og lagringspolicyer](unit-measure-stocking-policies.md).

1. Velg salgsordrelinjen 1. Deretter, i delen **Salgsordrelinje** på menyen **Lager**, velger du **Reservasjoner**.
1. På **Reservasjon**-siden i handlingsruten velger du **Reserver parti**, og deretter lukker du siden.
1. Gjenta trinn 4 og 5 for salgsordrelinje 2.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Følgende hendelser skjer:

    - Systemet behandler den opprettede forsendelsen ved hjelp av malen som inneholder etikettutskriftstrinnet. Etikettoppsettet blir brukt til å definere etikettens format, og resultatet blir en etikett som skrives ut på skriveren som er valgt i etikettmalen.
    - Bølgeetiketter genereres og skrives ut. Antallet etiketter vil tilsvare antallet kartonger (i dette eksemplet er 376 Box-etiketter for linje 1 og 322 Box-etiketter for linje 2).
    - En ny fraktbrev-ID genereres for forsendelsene. Hvis du konfigurerte nummerserieutvidelsene, vil bølgeetikett-IDene følge **SSCC-18**-nummerformatet. 

Du kan vise og skrive ut bølgeetiketter på nytt fra følgende sider. På handlingsruten for hver side, i fanen **Forsendelser** i gruppen **Beslektet informasjon**, velger du **Bølgeetiketter**.

- Alle forsendelser \> Forsendelsesdetaljer
- Alle laster \> Lastdetaljer
- Alle bølger
- Bølgeetiketter
- Historikk for bølgeetikett

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Scenario 2: Bølgeetikettutskrift for containerbruk (uten bølgeetikettposter)

I dette scenariet kan du skrive ut bølgeetiketter ved containerbruk for automatisk å dele varer inn i kartonger, som dermed ikke krever en bølgeetikettpost. I dette tilfellet fungerer container-IDen som en plassholder for SSCC.

Her er hovedforskjellen mellom dette scenariet og scenario 1:

- **Maler for bølgeetiketter:** Du velger ikke en bølgeetikettype på bølgeetikettmalen, og du trenger ikke en etikettversjonsgruppering. Ellers vil du konfigurere bølgeetikettmalen og koble til bølgemalen på samme måte som beskrevet i scenario 1. Du må la bølgeetikettypen være tom for å hindre at bølgeetiketter blir generert.
- **Oppsett av bølgeetiketter:** Du konfigurerer radinnstillingene for bølgeetikettoppsett for arbeidslinjer i stedet for bølgeetikettposter. Du må konfigurere radinnstillingen for etikettoppsettet ved hjelp av **WHSWorkLine**-tabellen i stedet for **WHSWaveLabel**-tabellen. **Rader per side**-innstillingen kontrollerer antallet rader som brødtekstdelen vil ha. 

Denne konfigurasjonen egner seg også for forretningsscenarioer der flere ulike varer pakkes inn i én boks med etikett eller på en pall, og denne pakkeprosessen kan defineres av arbeidsopprettelsen (for eksempel arbeid som er gruppert etter forsendelse).

Dette scenariet viser ende-til-ende-flyten.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Kontrollere at bølgeetikettmetoden er tilgjengelig

Det kan hende du må generere metodene for bølgebehandling på nytt for å gjøre metoden for bølgeetikettutskrift tilgjengelig.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.
1. Bekreft at **waveLabelPrinting** er i listen. Hvis den ikke er det, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.

### <a name="set-up-a-wave-template"></a>Definere en bølgemal

Med bølgemaler kan du koble bestemte forekomster av bølgemetoder til en tilsvarende bølgeetikettmal.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. Velg en mal, for eksempel **63 Containerbruk**.
1. I hurtigfanen **Metoder** flytter du metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder**.
1. I kolonnen **Valgte metoder** velger du metoden **Bølgeetikettutskrift** og setter feltet **Bølgetrinnkode** til *PrintLabel*. For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Opprette et oppsett for bølgeetikett

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetikettoppsett**.
1. Opprett en post som har følgende innstillinger:

    - **Etikettoppsett-ID:** *Kartong*
    - **Beskrivelse:** *Kartong (SSCC)*

1. Velg **Lagre** i handlingsruten.
1. I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.

    Siden for **Radinnstillinger for bølgeetikett** vises. Her kan du konfigurere den dynamiske delen av etiketten.

1. Legg til en rad som har følgende innstillinger:

    - **Rad-ID:** *WorkLine*
    - **Navn på radtabell:** *WHSWorkLine*
    - **Startposisjon for rad:** *500*

        Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.

    - **Radhøyde:** *-50*

        Dette feltet definerer høyden på hver rad. Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter.

    - **Rader per side:** *5*

        Dette feltet definerer antallet rader som kan skrives ut på hver etikett.

        > [!NOTE]
        > Dette oppsettet vil skrive ut flere ZPL-etiketter per arbeid, der hver side kan inneholde opptil fem arbeidslinjer. Hvis for eksempel en etikett skrives ut for en container med 12 linjer, skrives tre etiketter ut. Hvis du vil skrive ut en egen etikett for hver plukklinje, setter du denne verdien til *1*.

1. Lukk siden.
1. I handlingsruten velger du **Rediger spørring**.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Arbeidstype*
    - **Kriterier:** *Plukk*

1. Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du fanen **Sammenkoblinger**, velger tabellen **Arbeidslinjer** og kobler **Forsendelser**-tabellen til den.
1. Lukk dialogboksen for redigeringsprogram for spørring.
1. Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen**, **brødtekstdelen** og **bunntekstdelen**. I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten. Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten. Her er et eksempel:

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten. Her er et eksempel:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Dette oppsettet skriver bare ut én kopi av hver etikett. Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n**-verdien for **\^PQn**-delen i bunnteskten til det nødvendige antallet eksemplarer. Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.

Etiketten er nå klar til bruk.

### <a name="create-a-wave-label-template"></a>Opprette en mal for bølgeetikett

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter**.
1. Legg til en bølgenivåmal, og angi følgende verdier i toppteksten:

    - **Etikettmalnavn:** *Containeretiketter*
    - **Beskrivelse:** *Containeretiketter*
    - **Bølgetrinnkode:** *PrintLabel*
    - **Lager:** *63*

1. I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en rad med følgende innstillinger:

    - **Etikettoppsett-ID:** *Container*
    - **Skrivernavn:** Velg en passende ZPL-skriver.
    - **Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)

1. Velg **Lagre** i handlingsruten.
1. Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto. På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**. Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Forsendelser*
    - **Avledet tabell:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angi det aktuelle kundekontonummeret.

    Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.

### <a name="configure-number-sequence-extensions"></a>Konfigurere nummerserieutvidelser

Nummerserieutvidelser kontrollerer GS1-samsvar for bestemte nummerserier. Denne konfigurasjonen er valgfri for det gjeldende scenariet. Du finner mer informasjon og konfigurasjonsinstruksjoner under [Konfigurere nummerserieutvidelser](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Opprette en salgsordre og frigi den til lageret

1. Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.
1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Lager:** *63*

1. Legg til fem salgsordrelinjer:

    - Salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *10*

    - Salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *20*

    - Salgsordrelinje 3:

        - **Varenummer:** *L0006*
        - **Antall:** *20*

    - Salgsordrelinje 4:

        - **Varenummer:** *L0100*
        - **Antall:** *40*

    - Salgsordrelinje 5:

        - **Varenummer:** *L0101*
        - **Antall:** *50*

    > [!NOTE]
    > Varene og antallene som beskrives her, er bare eksempler. De må ha lager i det angitte lageret.

1. Velg salgsordrelinjen 1. Deretter, i delen **Salgsordrelinje** på menyen **Lager**, velger du **Reservasjoner**.
1. På **Reservasjon**-siden i handlingsruten velger du **Reserver parti**, og deretter lukker du siden.
1. Gjenta trinn 4 og 5 for hver ekstra salgsordrelinje.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Følgende hendelser skjer:

    - Systemet behandler den opprettede forsendelsen ved hjelp av malen som inneholder etikettutskriftstrinnet. Etikettoppsettet blir brukt til å definere etikettens format, og sluttresultatet blir en etikett som har fem linjer og som skrives på skriveren som er valgt i etikettmalen.
    - En ny fraktbrev-ID genereres for forsendelsene. Hvis du konfigurerte nummerserieutvidelsene, vil bølgeetikett-IDene følge **SSCC-18**-nummerformatet. 

Du kan skrive ut disse bølgeetikettene på nytt ved å gå til **Lagerstyring \> Forespørsler og rapporter \> Bølgeetikettlogg**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Scenario 3: Utskrift av bølgeetiketter for etiketter med flere nivåer

Dette scenariet viser hvordan du bruker utskriftsfunksjonaliteten for bølgeetiketter når lagerprosessene krever flere nivåer av leveringsetiketter. Det kan for eksempel hende at separate etiketter må skrives ut for kartonger og paller, og en pauseetikett må kanskje skrives ut for en hel forsendelse. Pauseetiketter er en separat type etikett som kan brukes som en skiller mellom rulleringer og containere, for eksempel etiketter for forsendelses-IDen og en strekkode, slik at etikettene enkelt kan sorteres etter at de er skrevet ut.

Hovedforskjellen mellom konfigurasjonen av dette scenariet og konfigurasjonen av scenario 1, i tillegg til at pauseetiketter aktiveres, er at flere bølgeetikettyper må knyttes til bølgeetikettmaler og linjer for sekvensgrupper for enhet. Du kan oppnå denne konfigurasjonen ved å definere følgende elementer i dette scenariet:

- **Bølgebehandlingsmetoder:** Du merker bølgeetikettmetoden som "kan gjentas", legger den til to (eller flere) ganger til bølgemalen og angir ulike bølgetrinnkoder.
- **Maler for bølgeetiketter:** Du konfigurerer bølgeetikettmalene og kobler dem til bølgemalen. Hver bølgeetikettmal har sin egen bølgeetikettype.
- **Bølgeetikettoppsett:** Du oppretter flere bølgeetikettoppsett. Det vil være et separat etikettoppsett for hvert "lag" med etiketter, og det vil også være et pauseetikettoppsett.

Dette scenariet viser ende-til-ende-flyten.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.

### <a name="set-up-a-wave-process-method"></a>Definere en metode for bølgeprosess

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.
1. Bekreft at **waveLabelPrinting** er i listen. Hvis den ikke er det, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.
1. For **waveLabelPrinting**-metoden merker du av for at **metoden kan gjentas**.

### <a name="set-up-a-wave-template"></a>Definere en bølgemal

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
2. Velg en mal, for eksempel **62 Standardforsendelse**.
3. I hurtigfanen **Metoder** flytter du metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder**.
4. I kolonnen **Valgte metoder** tilordner du verdien **Bølgetrinnkode**, for eksempel *Kartong*, til metoden **Bølgeetikettutskrift**. For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).
5. Flytt metoden **Bølgeetikettutskrift** til kolonnen **Valgte metoder** enda en gang.
6. I kolonnen **Valgte metoder** tilordner du en annen **Bølgetrinnkode**-verdi, for eksempel *Palle*, til den andre **Bølgeetikettutskrift**-metoden. For mer informasjon om bølgetrinnkoder, se [Bølgetrinnkoder](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Opprette tre oppsett for bølgeetikett

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetikettoppsett**.
1. Opprett en post som har følgende innstillinger:

    - **Etikettoppsett-ID:** *Kartong*
    - **Beskrivelse:** *Kartong (SSCC)*

1. Velg **Lagre** i handlingsruten.
1. I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.

    Siden for **Radinnstillinger for bølgeetikett** vises. Her kan du konfigurere den dynamiske delen av etiketten.

1. Legg til en rad som har følgende innstillinger:

    - **Rad-ID:** *WaveLabel*
    - **Navn på radtabell:** *WHSWaveLabel*
    - **Startposisjon for rad:** *0*

        Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.

    - **Radhøyde:** *0*

        Dette feltet definerer høyden på hver rad (i punkter) i henhold til ZPL-standarden. Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter. Fordi det bare er én rad i dette eksemplet, kan du sette verdien til *0* (null).

    - **Rader per side:** *1*

        Dette feltet definerer antallet rader som kan skrives ut på hver etikett.

        > [!NOTE]
        > Dette oppsettet vil føre til at det skrives ut en egen ZPL-etikett for hver post i bølgeetikettabellen.

1. Lukk siden.
1. I handlingsruten velger du **Rediger spørring**.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Arbeidstype*
    - **Kriterier:** *Plukk*

    Denne spørringen sikrer at bare arbeidslinjer av plukktypen blir skrevet ut på etiketten, ikke plasser-arbeidslinjer.

1. Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du fanen **Sammenkoblinger**, velger tabellen **Arbeidslinjer** og kobler **Forsendelser**-tabellen til den. 
1. Lukk dialogboksen for redigeringsprogram for spørring.
1. Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen**, **brødtekstdelen** og **bunntekstdelen**. I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten. Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten. Her er et eksempel:

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten. Her er et eksempel:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Dette oppsettet skriver bare ut én kopi av hver etikett. Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n**-verdien for **\^PQn**-delen i bunnteskten til det nødvendige antallet eksemplarer. Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.

1. Den første etiketten er nå klar til bruk.
1. Opprett en oppsettpost nummer to som har følgende innstillinger:

    - **Etikettoppsett-ID:** *Pall*
    - **Beskrivelse:** *Pall*

1. Velg **Lagre** i handlingsruten.
1. I handlingsruten velger du alternativet for **Radinnstillinger for bølgeetikett**.

    Siden for **Radinnstillinger for bølgeetikett** vises. Her kan du konfigurere den dynamiske delen av etiketten.

1. Legg til en rad som har følgende innstillinger:

    - **Rad-ID:** *WaveLabel*
    - **Navn på radtabell:** *WHSWaveLabel*
    - **Startposisjon for rad:** *0*

        Dette feltet angir den loddrette plasseringen der raden vil begynne på etiketten.

    - **Radhøyde:** *0*

        Dette feltet definerer høyden på hver rad (i punkter) i henhold til ZPL-standarden. Radhøyden er positiv for vannrette etiketter og negativ for loddrette etiketter. Fordi det bare er én rad i dette eksemplet, kan du sette verdien til *0* (null).

    - **Rader per side:** *1*

        Dette feltet definerer antallet rader som kan skrives ut på hver etikett.

        > [!NOTE]
        > Dette oppsettet fører til at det skrives ut en egen ZPL-etikett for hver post i bølgeetikettabellen.

1. Lukk siden.
1. I handlingsruten velger du **Rediger spørring**.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Arbeidstype*
    - **Kriterier:** *Plukk*

    Denne spørringen sikrer at bare arbeidslinjer av plukktypen blir skrevet ut på etiketten, ikke plasser-arbeidslinjer.

1. Hvis du vil ha muligheten til å skrive ut fraktbrev-IDen, velger du fanen **Sammenkoblinger**, velger tabellen **Arbeidslinjer** og kobler **Forsendelser**-tabellen til den.
1. Lukk dialogboksen for redigeringsprogram for spørring.
1. Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen**, **brødtekstdelen** og **bunntekstdelen**. I **topptekstdelen** i feltet for **etikettopptekst** angir du koden for den nødvendige toppteksten. Hvis du for eksempel bruker Zebra-skrivere, kan du bruke følgende kode.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. I **brødtekstdelen** i feltet for **etikettbrødtekst** angir du ZPL-kode for den nødvendige brødteksten. Her er et eksempel:

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. I **brødtekstdelen** i feltet for **etikettbunntekst** angir du ZPL-kode for den nødvendige bunnteksten. Her er et eksempel:

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Dette oppsettet skriver bare ut én kopi av hver etikett. Hvis du trenger flere kopier (for eksempel én kopi for hver side av pallen), setter du **n**-verdien for **\^PQn**-delen i bunnteskten til det nødvendige antallet eksemplarer. Hvis du for eksempel vil skrive ut fire eksemplarer av hver etikett, angir du **\^PQ4**.

1. Den andre etiketten er nå klar til bruk.
1. Opprett en tredje oppsettpost som har følgende innstillinger:

    - **Etikettoppsett-ID:** *Pause*
    - **Beskrivelse:** *Pauseetikett*

1. Velg **Lagre** i handlingsruten.
1. Hurtigfanen for **Skrivertekstoppsett** har tre inndelinger der du kan skrive skriverkode: **topptekstdelen**, **brødtekstdelen** og **bunntekstdelen**. I **topptekstdelen** i feltet for **etikettopptekst** angir du ZPL-koden for den nødvendige toppteksten. Her er et eksempel:

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Denne gangen er ikke brødtekst nødvendig. Skriv derfor bare inn den påkrevde teksten i **bunntekstdelen**. Her er et eksempel:

    ```plaintext
    ^XZ
    ```

    Den tredje etiketten er nå klar til bruk.

    > [!NOTE]
    > Denne tredje etiketten er en pauseetikett som vil bli brukt som skille mellom etiketter.

### <a name="create-two-wave-label-types"></a>Opprette to bølgeetikettyper

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Bølgeetiketttyper**.
1. Opprett en post som har følgende innstillinger:

    - **Etikettype:** *Kartong*
    - **Beskrivelse:** *Kartong*

1. Opprett en post nummer to som har følgende innstillinger:

    - **Etikettype:** *Pall*
    - **Beskrivelse:** *Pall*

### <a name="set-up-unit-sequence-groups"></a>Konfigurer sekvensgrupper for enheter

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Sekvensgrupper for enhet**.
1. Velg eller opprett en **EA Box pl**-gruppe.
1. For **Boks** angir du feltet **Bølgenivåtype** til *Kartong*.
1. For **PL**-linjen angir du feltet **Bølgenivåtype** til *Pall*.

### <a name="create-wave-label-templates"></a>Opprette maler for bølgeetikett

1. Gå til **Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter**.
1. Opprett en etikettmal som har følgende innstillinger:

    - **Etikettmalnavn:** *Kartongetiketter*
    - **Beskrivelse:** *Kartongetiketter*
    - **Bølgetrinnkode:** *Kartong*
    - **Lager:** *62*

1. På hurtigfanen **Generelt**, i feltet **Bølgeetiketttype**, velger du en verdi, for eksempel *Kartong*.
1. I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en rad med følgende innstillinger:

    - **Etikettoppsett-ID:** *Kartong*
    - **Skrivernavn:** Velg en passende ZPL-skriver.
    - **Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)

1. Velg **Lagre** i handlingsruten.
1. Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto. På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**. Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Forsendelser*
    - **Avledet tabell:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angi det aktuelle kundekontonummeret.

    Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring.

1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogrammet for spørringen for hele etikettmalen.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Sortering**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Linje-ID for referanselast (post-ID)*
    - **Søkeretning:** *Stigende*

1. Legg til en rad nummer to som har følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Leverings-ID*
    - **Søkeretning:** *Stigende*

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. En meldingsboks ber deg bekrefte gjenopprettingsoperasjonen for gruppering. Klikk på **Ja** for å fortsette.
1. Velg **Malgruppe for bølgeetikett** i handlingsruten.
1. I dialogboksen for **Malgruppe for bølgeetikett**, for raden der feltet **Referansefeltnavn** er satt til *Forsendelses-ID*, angir du følgende verdier:

    - **Skriv ut pauseetikett:** Merk av i denne avmerkingsboksen.
    - **Etikettoppsett-ID:** Velg en pauseetikett. (Merk for eksempel av for *Pause*-etikettoppsettet som du opprettet tidligere i dette scenariet.)
    - **Skrivernavn:** Velg skriveren for pauseetiketten. (Vanligvis må du velge den samme skriveren som er valgt i hurtigfanen **Maldetaljer for bølgeetikett**, for å skille mellom etiketter. Det er imidlertid mulig å bruke andre scenarier.)

1. For raden der feltet **Referansefeltnavn** er satt til *Linje-ID for referanselast*, merker du av for **Etikettversjons-ID**.

    > [!NOTE]
    > Dette oppsettet vil opprette én etikettsekvens ("Kartong 1 av X") per lastlinje gjennom bølgen, uansett oppsett for arbeidsgruppering. Denne etikettsekvensen kan skrives ut på et etikettoppsettet. I tillegg vil etiketter for forskjellige forsendelser skilles med den valgte pauseetiketten.

1. Velg **OK** for å lukke dialogboksen **Malgruppe for bølgeetikett**.
1. Opprett en etikettmal nummer to som har følgende innstillinger:

    - **Etikettmalnavn:** *Palletiketter*
    - **Beskrivelse:** *Palletiketter*
    - **Bølgetrinnkode:** *Pall*
    - **Lager:** *62*

1. På hurtigfanen **Generelt**, i feltet **Bølgeetiketttype**, velger du en verdi, for eksempel *Pall*.
1. I hurtigfanen for **Maldetaljer for bølgeetikett** legger du til en rad med følgende innstillinger:

    - **Etikettoppsett-ID:** *Pall*
    - **Skrivernavn:** Velg en passende ZPL-skriver.
    - **Kjør spørring:** *Ja* (Denne innstillingen er valgfri, men anbefales for optimal ytelse.)

1. Velg **Lagre** i handlingsruten.
1. Valgfritt: Hvis du definerer en kundespesifikk etikettutforming, må du opprette en spørring for å finne kundens konto. På hurtigfanen **Maldetaljer for bølgeetikett** velger du **Rediger spørring**. Deretter, i dialoglogboksen for redigeringsprogrammet, i tabellen **Område**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Forsendelser*
    - **Avledet tabell:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angi det aktuelle kundekontonummeret.

    Når du er ferdig, velger du **OK** for å lukke dialogboksen redigeringsprogrammet for spørring. 

1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogrammet for spørringen for hele etikettmalen.
1. I dialogboksen for redigeringsprogrammet, i tabellen **Sortering**, legger du til en rad med følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Linje-ID for referanselast (post-ID)*
    - **Søkeretning:** *Stigende*

1. Legg til en rad nummer to som har følgende innstillinger:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Leverings-ID*
    - **Søkeretning:** *Stigende*

1. Velg **OK** for å lukke dialogboksen for redigeringsprogrammet for spørring.
1. En meldingsboks ber deg bekrefte gjenopprettingsoperasjonen for gruppering. Klikk på **Ja** for å fortsette.
1. Velg **Malgruppe for bølgeetikett** i handlingsruten.
1. I dialogboksen for **Malgruppe for bølgeetikett**, for raden der feltet **Referansefeltnavn** er satt til *Forsendelses-ID*, angir du følgende verdier:

    - **Skriv ut pauseetikett:** Merk av i denne avmerkingsboksen.
    - **Etikettoppsett-ID:** Velg en pauseetikett. (Merk for eksempel av for *Pause*-etikettoppsettet som du opprettet tidligere i dette scenariet.)
    - **Skrivernavn:** Velg skriveren for pauseetiketten. (Vanligvis må du velge den samme skriveren som er valgt i hurtigfanen **Maldetaljer for bølgeetikett**, for å skille mellom etiketter. Det er imidlertid mulig å bruke andre scenarier.)

1. For raden der feltet **Referansefeltnavn** er satt til *Linje-ID for referanselast*, merker du av for **Etikettversjons-ID**.

    > [!NOTE]
    > Dette oppsettet vil opprette én etikettsekvens ("Kartong 1 av X") per lastlinje gjennom bølgen, uansett oppsett for arbeidsgruppering. Denne etikettsekvensen kan skrives ut på et etikettoppsettet. I tillegg vil etiketter for forskjellige forsendelser skilles med den valgte pauseetiketten.

### <a name="configure-number-sequence-extensions"></a>Konfigurere nummerserieutvidelser

Nummerserieutvidelser kontrollerer GS1-samsvar for bestemte nummerserier. Denne konfigurasjonen er valgfri for det gjeldende scenariet. Du finner mer informasjon og konfigurasjonsinstruksjoner under [Konfigurere nummerserieutvidelser](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Opprette en salgsordre og frigi den til lageret

1. Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.
1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Lager:** *62*

1. Legg til to salgsordrelinjer:

    - Salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *9024*
        - **Enhet:** *ea* (9024 ea = 376 Box = 47 PL)

    - Salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *9016*
        - **Enhet:** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Varene og antallene som beskrives her, er bare eksempler. De må bruke enhetsseriegruppen du definerte tidligere, riktige enhetskonverteringer fra *ea* til *Box* til *PL* må være definert for dem, og de må ha lager i lageret *62*. Hvis du vil ha mer informasjon, kan du se [Måleenhet og lagringspolicyer](unit-measure-stocking-policies.md).

1. Velg salgsordrelinjen 1. Deretter, i delen **Salgsordrelinje** på menyen **Lager**, velger du **Reservasjoner**.
1. På **Reservasjon**-siden i handlingsruten velger du **Reserver parti**, og deretter lukker du siden.
1. Gjenta trinn 4 og 5 for salgsordrelinje 2.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Følgende hendelser skjer: 

    - Systemet behandler den opprettede forsendelsen ved hjelp av malen som inneholder etikettutskriftstrinnet. Etikettoppsettet blir brukt til å definere etikettens format, og resultatet blir en etikett som skrives ut på skriveren som er valgt i etikettmalen.
    - Bølgeetiketter genereres og skrives ut. Antallet etiketter vil tilsvare antallet kartonger (i dette eksemplet er 376 Box-etiketter for linje 1, 322 Box-etiketter for linje 2, 47 PL-etiketter for linje 1, 47 PL-etiketter for linje 2 og to pauseetiketter som har forsendelses-IDen).
    - En ny fraktbrev-ID genereres for forsendelsene. Hvis du konfigurerte nummerserieutvidelsene, vil bølgeetikett-IDene følge **SSCC-18**-nummerformatet. 

Du kan vise og skrive ut bølgeetiketter på nytt fra følgende sider:

- Alle forsendelser \> Forsendelsesdetaljer
- Alle laster \> Lastdetaljer
- Alle bølger
- Bølgeetiketter
- Historikk for bølgeetikett

For de fleste av disse sidene kan du finne den relevante funksjonen ved å velge **Bølgeetiketter** i **Relatert informasjon**-gruppen i fanen **Forsendelser** i handlingsruten.

## <a name="additional-resources"></a>Tilleggsressurser

- [Skrive ut og annullere bølgeetiketter på nytt](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]