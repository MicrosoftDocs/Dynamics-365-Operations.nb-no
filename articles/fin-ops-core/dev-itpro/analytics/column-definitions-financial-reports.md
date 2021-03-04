---
title: Kolonnedefinisjoner i finansrapporter
description: Denne artikkelen gir informasjon om kolonnedefinisjoner. En kolonnedefinisjon er en rapportkomponent eller byggeblokk som angir innholdet i kolonner i en rapport. Grunnleggende kolonnedefinisjoner kan i likhet med raddefinisjoner brukes på flere rapporter.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 611e5cdfd2289bb2c690a72659e9ba47d6309cfe
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687236"
---
# <a name="column-definitions-in-financial-reports"></a>Kolonnedefinisjoner i finansrapporter

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om kolonnedefinisjoner. En kolonnedefinisjon er en rapportkomponent eller byggeblokk som angir innholdet i kolonner i en rapport. Grunnleggende kolonnedefinisjoner kan i likhet med raddefinisjoner brukes på flere rapporter.

## <a name="create-and-modify-a-column-definition"></a>Opprette og endre en kolonnedefinisjon

En kolonnedefinisjon kan inneholde to til 255 kolonner.

### <a name="create-a-column-definition"></a>Opprette en kolonnedefinisjon

1. I navigasjonsruten i Rapportutforming klikker du **Kolonnedefinisjoner**.
2. Klikk **Ny** på **Fil**-menyen, og klikk deretter **Kolonnedefinisjon**.
3. Legg til innholdet i kolonnedefinisjonen.

### <a name="open-a-column-definition"></a>Åpne en kolonnedefinisjon

1. I navigasjonsruten i Rapportutforming klikker du **Kolonnedefinisjoner**.
2. Dobbeltklikk en kolonnedefinisjon for å åpne den.

### <a name="add-a-column-to-a-column-definition"></a>Legge til en kolonne i en kolonnedefinisjon

1. I Rapportutforming klikker du **Kolonnedefinisjoner**, og deretter åpner du kolonnedefinisjonen som skal endres.
2. Merk kolonnen der en ny kolonne skal settes inn.
3. På **Rediger**-menyen klikker du **Sett inn kolonne**. Den nye kolonnen vises til venstre for kolonnen som du valgte.

### <a name="delete-a-column-from-a-column-definition"></a>Slette en kolonne fra en kolonnedefinisjon

1. Klikk **Kolonnedefinisjoner** i Rapportutforming, og åpne deretter kolonnedefinisjonen som skal endres.
2. Velg kolonnen du vil slette.
3. Klikk **Slett kolonne** på **Rediger**-menyen.

## <a name="contents-of-a-column-definition"></a>Innhold i en kolonnedefinisjon
En kolonnedefinisjon inneholder følgende informasjon:

- En kolonne med beskrivelsene for raddefinisjonen
- Beløpskolonner som viser data fra de økonomiske dataene eller beregninger som er basert på andre data i kolonnedefinisjonen
- Formateringskolonner
- Attributtkolonner

Denne informasjonen vises i følgende områder i kolonnedefinisjonen:

- Overskriftsområdet i kolonnedefinisjonen inneholder overskriftsteksten og formatering som vises i rapporten. Et hode kan gjelde for én datakolonne, kan strekke seg over flere kolonner eller kan gjelde for kolonner på en betinget basis. Kolonnedefinisjonen kan inneholde så mange kolonnehoderader som du trenger.

    > [!NOTE]
    > Kolonnehoder gjelder for hver kolonne med data i rapporten. Rapporthoder gjelder for hele rapporten. Du definerer topptekster i rapporter i kategorien **Topptekst og bunntekst** i rapportdefinisjonen.

- Detaljradene for kolonnen er radene under radoverskriftene i kolonnedefinisjonen. Detaljradene for kolonnen definerer informasjonen som er inkludert i rapporten. Tabellen nedenfor viser og beskriver detaljradene for kolonnen.

    | Navn på detaljrad for kolonne                                                | Beskrivelse                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Kolonnetype                                                           | (Obligatorisk) Angi datatypen i kolonnen.                                                     |
    | Registerkode/attributtkategori                                          | Angi informasjon om økonomiske data for kolonner av typene **FD** og **ATTR**.                       |
    | Perioder dekket for regnskapsårsperiode                                    | Angi informasjon om økonomiske data for kolonner av typen **FD**.                                     |
    | Formel                                                               | Angi en beregningsformel for kolonnene av typen **CALC**.                                        |
    | Kolonnebredde ekstra mellomrom foran kolonneformat overstyre utskriftskontroll | Angi alternativer for spesielt format.                                                                        |
    | Kolonnebegrensninger                                                   | Begrens dataene.                                                                                         |
    | Rapporteringsenhet                                                        | Begrense kolonnen slik at den viser data bare for den angitte rapporteringsenheten.                      |
    | Valutavisning Valutafilter                                      | Formater valuta.                                                                                       |
    | Dimensjonsfilter                                                      | Angi et filter for å begrense dataene til bestemte rapportenheter for økonomiske data.                           |
    | Attributtfilter                                                      | Angi et filter for å begrense de økonomiske dataene.                                                       |
    | Startdato sluttdato                                                   | Begrens de økonomiske dataene til bestemte datoer.                                                         |
    | Justering                                                         | Venstrejuster, midtstill eller høyrejustere den beskrivende teksten som er angitt i raddefinisjonen. |

## <a name="column-restrictions-in-a-column-definition"></a>Kolonnebegrensninger i en kolonnedefinisjon
Du kan bruke kolonnebegrensninger for å angi hvordan en kolonnedefinisjon bruker data eller beregner informasjon. Du kan også begrense en rapportkolonne til en bestemt enhet eller for bestemte datoer.

> [!NOTE]
> En **Kolonnebegrensning**-kode overstyrer alle innstillinger i konflikt som er tilordnet i raddefinisjonen.

### <a name="column-restrictions-cell"></a>Kolonnebegrensninger-celle

**Kolonnebegrensninger**-cellen kan inneholde koder som begrenser eller skjuler informasjon, for eksempel radformatering, detaljer og beløp for den aktuelle kolonnen.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Legge til kolonnebegrensning i en kolonnedefinisjon

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk **Kolonnebegrensninger**-cellen for kolonnen som skal begrenses.
3. I dialogboksen **Kolonnebegrensninger** velger du én eller flere koder i listen, og deretter klikker du **OK**.

### <a name="column-restriction-codes"></a>Kolonnebegrensningskoder

Tabellen nedenfor beskriver kodene for kolonnebegrensning.

| Kolonnebegrensningskode | Beskrivelse |
|-------------------------|-------------|
| SU                      | Skjul understreking for en kolonne der en understrekingskommando (**---**) eller en kommando for dobbel understreking (**===**) er angitt i raddefinisjonen. Du vil kanskje for eksempel ikke understreke beløpene som produseres av en prosentberegning. |
| ST                      | Skjul totaler, slik at bare detaljene vises i kolonnen (for eksempel en statistisk kolonne). |
| SD                      | Skjul detaljer, slik at bare **TOT**- og **CAL**-rader (fra raddefinisjonen) vises i kolonnen. |
| DR                      | Begrens beløpene i en **FD**-kolonne til debetbeløp. |
| CR                      | Begrens beløpene i en **FD**-kolonne til kreditbeløp. |
| ADJ                     | Begrens beløpene i kolonnen til justeringsbeløpene for perioden, hvis disse beløpene er tilgjengelige. |
| XAD                     | Begrens beløpene i kolonnen, slik at justeringsbeløpene for perioden utelates. |
| OF                      | Begrens beløpene i kolonnen, slik at bare posterte transaksjoner tas med, hvis disse transaksjonene er tilgjengelige. |
| UPT                     | Begrens beløpene i kolonnen, slik at bare uposterte transaksjoner tas med, hvis disse transaksjonene er tilgjengelige.<p><strong>Obs!</strong>  Ikke alle leverandører støtter uposterte transaksjoner. </p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Begrense en kolonne til en rapporteringsenhet

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk **Rapporteringsenhet**-cellen for kolonnen som skal begrenses.
3. I dialogboksen **Valg av rapporteringsenhet**, i **Rapporteringstre**-listen, velger du et tre.
4. Vis eller skjul listen over enheter, velg en rapporteringsenhet og klikk deretter **OK**.

## <a name="format-column-headers"></a>Formatere kolonneoverskrifter
Du kan legge til, endre og slette overskriftene som vises øverst i kolonnene i en rapport. Du kan også konfigurere betingede kolonneoverskrifter som strekker seg over flere kolonner, basert på den **Periode**-feltet fra kolonnedefinisjoner og **Basisperiode**-feltet fra rapportdefinisjoner. Basisperiodefunksjonen bidrar til å spare tid når du oppretter akkumulerer prognoserapporter.

### <a name="create-and-manage-column-headers"></a>Opprette og behandle kolonneoverskrifter

Du kan bruke dialogboksen **Kolonneoverskrift** for å legge til, endre og slette overskriftene som vises øverst i kolonnene i en rapport. Tabellen nedenfor beskriver feltene i dialogboksen **Kolonneoverskrift**.

| Felt                 | Beskrivelse |
|-----------------------|-------------|
| Tekst for kolonneoverskrift    | Denne teksten vises i kolonneoverskriften. Du kan skrive inn tekst direkte i dette feltet, eller klikke **Sett inn autotekst** for å velge et alternativ som oppdaterer kolonneoverskriften hver gang rapporten blir generert. Hvis du vil ta med flere autotekstkoder, klikker du **Sett inn autotekst** på nytt, og deretter klikker du en annen kode i listen. |
| Formateringsalternativer        | Bruk formatering på en kolonneoverskrift, for eksempel boks eller understreking. |
| Spre fra Spre til | Definer kolonnen eller kolonnene som overskriften gjelder for. |
| Justering         | Angi hvordan overskriften skal justeres for kolonnen eller kolonneserien som er angitt i feltene **Spre fra** og **Spre til**. |

### <a name="create-a-column-header"></a>Opprette en kolonneoverskrift

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk en hodecelle.
3. I dialogboksen **Kolonneoverskrift** skriver du inn overskriften. Du kan også klikke **Sett inn autotekst** og velg et alternativ.
4. I feltet **Formateringsalternativer** velger du et format for overskriften.
5. I feltet **Spre fra** skriver du inn bokstaven på kolonnen som overskriften skal starte over. I feltet **Spre til** skriver du inn bokstaven på kolonnen som overskriften skal slutte over.
6. Under **Justering** velger du om kolonneoverskriften skal være venstrejustert, midtstilt eller høyrejustert.
7. Klikk **OK**.

### <a name="add-a-column-header-row"></a>Legge til en rad for kolonneoverskrift

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Velg en celle i overskriftsraden.
3. På **Rediger**-menyen klikker du **Sett inn rad**. Den nye raden settes inn over raden du valgte i trinn 2.

> [!NOTE]
> Hvis du har fire eller flere rader i rapporttopptekstene i en rapport, overlapper topptekstene når rapporten eksporteres til et Excel-regneark. Hvis du vil vise alle overskrifter i rapporten, kan du øke toppmargen i rapportdefinisjonen.

### <a name="delete-a-column-header-row"></a>Slette en rad for kolonneoverskrift

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. I overskriften merker du cellen som skal slettes.
3. På **Rediger**-menyen klikker du **Slett rad**.

### <a name="create-an-automatically-generated-header"></a>Opprette en automatisk generert overskrift

Rapportutforming kan automatisk generere kolonneoverskrifter, basert på autotekstkoder. Autotekstkoder er variabler som oppdateres hver gang en rapport genereres. En kolonneoverskrift kan inneholde disse kodene for å angi rapportinformasjon som kan variere, for eksempel datoer eller periodenumre. Du kan derfor bruke én kolonnedefinisjon for flere rapportdefinisjoner, tidsperioder og rapporteringstrær. Siden autotekstkoder avhenger av kalenderinformasjonen fra detaljradene for kolonnedefinisjonen, støttes de bare for kolonnene **CALC** og **FD**. Hvordan en autotekstkode vises i kolonneoverskriften har innvirkning på hvordan denne informasjonen vises i rapporten. I dialogboksen **Kolonneoverskrift** vises autotekstkodene med store og små bokstaver. Derfor vises teksten i små og store bokstaver i rapporten. I et standard kalenderår løser for eksempel **\@CalMonthLong** måned **7** til **juli**. Hvis navnet på måneden skal være i store bokstaver (for eksempel **JULI**), skriver du inn autotekstkoden med store bokstaver i feltet **Kolonnehodetekst**. Angi for eksempel **\@CALMONTHLONG**. Du kan blande koder og tekst. Du skriver for eksempel inn følgende overskrift: **Periode \@FiscalPeriod-\@FiscalYear fra \@StartDate til \@EndDate**. Rapportoverskriften som genereres ligner på følgende tekst: **Periode 1-02 fra 01.01.02 til 01.31.02**.

> [!NOTE]
> Formatet på noe av teksten, for eksempel den lange datoen, avhenger av de regionale innstillingene på serveren. Hvis du vil endre disse innstillingene, klikker du **Start**, **Kontrollpanel** og deretter **Område og språk**. Tabellen nedenfor viser en liste over tilgjengelige alternativer for autotekst for kolonneoverskrifter.


| Alternativ og kode for autotekst                | Beskrivelse |
|-----------------------------------------|-------------|
| Navn på måned (@CalMonthLong)              | Skriv ut navnet på gjeldende måned i kolonneoverskriften. Hvis du vil runde av beløpene i rapporten til tusener, millioner eller milliarder, eller hvis du angir kolonnebredden i rapporten til færre enn ni tegn, blir månedsnavnet forkortet til de første tre tegnene. |
| Forkortet månedsnavn (@CalMonthShort) | Skriv ut det forkortede navnet på måneden for den valgte regnskapsperioden. |
| Periodenummer (@FiscalPeriod)           | Skriv ut det numerisk formatet av regnskapsperioden som er angitt for den aktuelle kolonnen. Hvis kolonnen strekker seg over flere perioder, blir den siste perioden i intervallet skrevet ut. |
| Periodebeskrivelse (@FiscalPeriodName)  | Skriv ut beskrivelsen for regnskapsperioden som er identifisert i de økonomiske dataen. |
| Regnskapsår (@FiscalYear)               | Skriv ut regnskapsåret for kolonnen i numerisk format. |
| Kalenderår (@CalYear)                | Skriv ut kalenderåret for kolonnen i numerisk format. |
| Startdato (@StartDate)                 | Skriv ut startdatoen for kolonnen. |
| Sluttdato (@EndDate)                     | Skriv ut sluttdatoen for kolonnen. |
| Enhetsnavn fra tre (@UnitName)         | Hvis du begrenser en kolonne til en bestemt enhet i rapporteringstreet, kan du skrive ut enhetsnavnet i kolonneoverskriften. |
| Enhetsbeskrivelse (@UnitDesc)            | Hvis du begrenser en kolonne til en bestemt enhet i rapporteringstreet, kan du skrive ut enhetsbeskrivelsen i kolonneoverskriften. |
| Registerkode (@BookCode)                   | Skriv ut registerkoden som er angitt i kolonnen. |
| Tom linje (@Blank)                     | Sette inn en tom linje i kolonneoverskriften. |

### <a name="create-a-conditional-spanning-header"></a>Opprette en betinget overskrift som strekker seg over flere kolonner

En betinget overskrift som strekker seg over flere kolonner kan strekke seg over flere kolonner basert på bestemte periodedata. Hvis du for eksempel har en budsjettrapport for regnskapsåret og vil vise de faktiske budsjettene for de siste månedene sammen med de forventede budsjettene for kommende måneder, kan du for eksempel bruke et betinget overskrift som strekker seg over flere kolonner for automatisk å oppdatere overskriften i rapporten. Vær oppmerksom på følgende situasjoner når du oppretter et betinget spredningshode:

- Stoppbetingelser (**Spre til**-feltet) som samsvares før en startbetingelse (**Spre fra**-feltet), ignoreres. Hvis for eksempel kolonne B har spre-betingelsen definert som BASE+1 til BASE, er BASE i kolonne C og BASE+1 er i kolonne D. I dette tilfellet ignoreres stoppbetingelsen i kolonne C, og utskriften av overskriften starter i kolonne D.
- Hvis du angir kolonneoverskrifter som overlapper hverandre, kan de overlappe når de skrives ut på rapporten. Rapporten genereres, men følgende advarsel vises i feltet **Status for rapportkø**: "Kolonneoverskrifter bruker av basisoverlapping med andre kolonneoverskriftene og kan føre til overlappende tekst." Overskriftsdefinisjonen for kolonne B er for eksempel B til BASE+1, og overskriftsdefinisjonen for kolonne D er BASE+1 til F. I dette tilfellet skrives overskriften ut oppå hverandre og kan ikke leses. Når BASE brukes i definisjon for **Spre fra / Spre til**, må du passe på å vise rapporten som genereres, for å se om overskriftene overlapper hverandre.
- Hvis du angir BASE i spredefinisjonen på en kolonne som ikke skal skrives ut (**NP**), blir den ignorert, uavhengig av hva som er definert i kolonnedefinisjonen. Dette scenariet er samme som ikke å opprette en definisjon for kolonneoverskrift.
- For betingede utskriftskolonner (**P&lt;B**, **P&gt;=B**), fungerer overskrifter som strekker seg over flere kolonner som en vanlig definisjon for kolonnetopptekst. Hvis betingelsen for eksempel er usann, vil alle etterfølgende kolonnetreff for spre-betingelsen starte utskriften av overskriften.

#### <a name="create-a-conditional-spanning-header"></a>Opprette en betinget overskrift som strekker seg over flere kolonner

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk en hodecelle.
3. I dialogboksen **Kolonneoverskrift** skriver du inn overskriften. Du kan også klikke **Sett inn autotekst** og velg et alternativ.
4. I feltet **Formateringsalternativer** velger du en formateringsstil for overskriften.
5. Angi en periode i forhold til basisperioden som angis når rapporten genereres. I feltene **Spre fra** og **Spre til** angir du én av følgende verdier: **BASE**, **BASE-X** eller **BASE+X**, der X er antall perioder fra basisperioden. Hvis du for eksempel angir **BASE** i **Spre fra**-feltet, starter den betingede kolonneoverskriften som strekker seg over flere kolonner, i kolonneoverskriften der rapportdefinisjonen **Basisperiode**-verdi er lik kolonnedefinisjonens **BASE**-verdi. Den avslutter i kolonnen som er angitt i **Spre til**-feltet. Hvis spredningen er BASE til M og rapportdefinisjonens **Basisperiode**-verdi er **4**, starter derfor overskriften i kolonnen er perioden er satt til **4** og slutter ved kolonne M. Overskrifter starter og stopper bare på utskriftskolonner.
6. Under **Justering** velger du om kolonneoverskriften skal være venstrejustert, midtstilt eller høyrejustert.
7. Klikk **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Eksempel på en betinget overskrift som strekker seg over flere kolonner

En bruker oppretter en rapport for en dynamisk seks måneders prognose. Brukeren vil at ordet "Faktisk" skal skrives ut over kolonnene som inneholder faktiske data, og at ordet "Budsjett" skal skrives ut over kolonnene som inneholder budsjettprognoser. Hver måned når rapporten kjøres, finnes det én faktiske kolonne til og én mindre budsjettkolonne. Selv om brukeren kan endre kolonnedefinisjonen manuelt hver gang rapporten blir generert, for å justere overskriftene, kan brukeren spare tid og arbeid ved å bestemmer seg for å opprette betingede overskrifter som strekker seg over flere kolonner som automatisk oppretter overskrifter over de aktuelle kolonnene hver gang rapporten kjøres. Brukeren åpner Rapportutforming, klikker **Kolonnedefinisjon** i navigasjonsruten, og åpner kolonnedefinisjonen for rapporten. Brukeren angir følgende informasjon: Basisperioden i rapportdefinisjonen er 4.

|      Format         |  A   | T             | K             | D             | E             | F             | G             | H             | I             | J             | K             | L             | M             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Overskrift 1            |      | Faktisk        | Budsjett        |               |               |               |               |               |               |               |               |               |               |
| Overskrift 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Overskrift 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Kolonnetype         | BSKR | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Registerkode/attributtkategori |      | FAKTISK        | BUDSJETT 2012    | FAKTISK        | BUDSJETT 2012    | FAKTISK        | BUDSJETT 2012    | FAKTISK        | BUDSJETT 2012    | FAKTISK        | BUDSJETT 2012    | FAKTISK        | BUDSJETT 2012    |
| Regnskapsår         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Periode              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Perioder som dekkes     |      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      | Tidsbestemt      |
| Kolonnebredde        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Utskriftskontroll       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Brukeren dobbeltklikker på en kolonneoverskriftscelle for å åpne dialogboksen **Kolonneoverskrift**, og skriver inn følgende informasjon:

| Felt              | Verdi                 |
|--------------------|-----------------------|
| Tekst for kolonneoverskrift | Faktisk                |
| Sett inn autotekst    | Ingen valg er gjort. |
| Formateringsalternativer     | Boks                   |
| Justering      | Ingen valg er gjort. |
| Spre fra        | T                     |
| Spre til          | BASE                  |
| Budsjettoverskrift      | BASE+1 til sluttkolonne  |

Etter at informasjonen er registrert, klikker brukeren på **OK**. Brukeren dobbeltklikker deretter på kolonneoverskriftscellen i kolonne C for å åpne dialogboksen **Kolonneoverskrift**, og skriver inn følgende informasjon.

| Felt              | Verdi                 |
|--------------------|-----------------------|
| Tekst for kolonneoverskrift | Budsjett                |
| Sett inn autotekst    | Ingen valg er gjort. |
| Formateringsalternativer     | Boks                   |
| Justering      | Ingen valg er gjort. |
| Spre fra        | C                     |
| Spre til          | BASE+2                |

Hver gang rapporten genereres vil ordet "Faktisk" skrives ut over kolonnene som inneholder faktiske data, og ordet "Budsjett" skrives ut over kolonnene som inneholder budsjettet prognoser. I tillegg vil antall kolonner justeres for hver måned.

## <a name="apply-column-justification"></a>Bruke kolonnejustering
**Justering**-cellen brukes til å angi justeringsformatering for en beskrivelseskolonne i en rapport. Dette alternativet har bare innvirkning på kolonnebeskrivelsene, ikke de faktiske verdiene.

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk **Justering**-cellen.
3. Velg én av følgende verdier i listen:

    - **Ingen** – Ingen justering brukes.
    - **Venstre** – venstrejuster kolonnebeskrivelsene.
    - **Midtstill** – Midtstill kolonnebeskrivelsene.
    - **Høyre** – høyrejuster kolonnebeskrivelsene.

## <a name="add-special-formatting-options"></a>Legge til alternativer for spesielle formatering
I kolonnedefinisjonen bruke detaljradene for formateringskolonnen spesiell formatering på merkede kolonner. Selv om noen av alternativene for **Utskriftskontroll** og **Kolonnebegrensninger** er spesifikke for **FD**-kolonner, gjelder de fleste alternativene for alle kolonnetyper. Formateringen som er angitt i kolonnedefinisjonen overstyrer imidlertid formateringen som er angitt i rapportdefinisjonen. Formateringen som er angitt i raddefinisjonen overstyrer imidlertid formateringen som er angitt i kolonnedefinisjonen. Følgende rader regnes som formateringsrader:

- Kolonnebredde
- Ekstra mellomrom før kolonnen
- Format/valutaoverstyring
- Utskriftskontroll

### <a name="changing-the-column-width"></a>Endre kolonnebredden

**Kolonnebredde**-cellen angir antall tegn som skal brukes for bredden på kolonnen i den utskrevne rapporten. Kolonnebredde er viktig for kolonner som inneholder beløp (kolonner av typen **CALC**, **WKS** eller **FD**), beskrivelser (kolonner av typen **DESC**) eller fyll (kolonner av typen **FILL**). Alternativet for **beste tilpasning** er valgt som standard, slik at bredden på hver kolonne justeres automatisk for å få plass til innholdet.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Angi bredden på en kolonne i en rapport

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. I **Kolonnebredde**-cellen skriver du inn antall mellomrom for bredden på kolonnen. Den maksimale bredden for en kolonne er 255 tegn (dette tallet omfatter kroner, komma og parenteser). Hvis du vil aktivere rapportutforming for å velge den riktige bredden for kolonnen basert på celleinnholdet, kan du eventuelt dobbeltklikke **Kolonnebredde**-cellen og deretter klikke **Beste tilpasning**.

### <a name="add-space-between-columns"></a>Legge til mellomrom mellom kolonnene

Cellen **Ekstra mellomrom før kolonne** angir bredden på skilletegnet mellom kolonner og tilstøtende kolonner i kolonnedefinisjonen. Innstillingen **Ekstra mellomrom før kolonne** påvirker alle detaljradene for kolonnen, men ikke radene for kolonneoverskriftene. Bruk dette alternativet for å skille kolonnegrupper eller legge til noen mellomrom før beskrivelsen, slik at beskrivelsekolonnen er innrykket fra de venstrejusterte titlene i rapporten. Standard antall mellomrom mellom kolonnene er to. Du kan endre denne innstillingen i kategorien **Innstillinger** i rapportdefinisjonen.

#### <a name="specify-the-space-between-columns"></a>Angi mellomrommet mellom kolonnene

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. I cellen **Ekstra mellomrom før kolonne** angir du hvor antall mellomrom som skal settes inn mellom kolonner.

### <a name="specify-a-format-currency-override"></a>Angi en overstyring av formatvaluta

Cellen **Format/valutaoverstyring** angir formateringen til desimal-, valuta- og prosentbeløpene i kolonnen. Denne formateringen overstyrer all formatering som er angitt i rapportdefinisjonen eller systemstandardene.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Tilordne en overstyring av formatvaluta til en rapportkolonne

1. Åpne kolonnedefinisjonen som skal endres, i Rapportutforming.
2. Dobbeltklikk en celle for **Format-/valutaoverstyring** i en beløpskolonne.
3. I dialogboksen **Overstyre format** velger du alternativer for formatering.

### <a name="add-a-print-control-code"></a>Legge til en kontrollkode for utskrift

Cellen **Utskriftskontroll** kan inneholde koder som justerer visningen eller utskriftsegenskapene til en kolonne. Det finnes to typer kontrollkoder for utskrift: vanlige kontrollkoder for utskrift og kontrollkoder for betinget utskrift.

#### <a name="regular-print-control-codes"></a>Vanlige kontrollkoder for utskrift

| Kontrollkode for utskrift | Oversettelse                                     | Beskrivelse |
|--------------------|-------------------------------------------------|-------------|
| NP                 | Skrives ikke ut                                     | Utelater beløpene i denne kolonnen fra rapporten som skrives ut og fra beregninger. Hvis du vil inkludere en kolonne som ikke skrives ut, i en beregning, kan du referere kolonnen direkte i beregningsformelen. Hvis kolonne C som ikke skrives ut, for eksempel er inkludert i følgende beregning: **B+C+D**. Hvis kolonne C som ikke skrives ut, imidlertid ikke er inkludert i følgende beregning: **B:D**. |
| XCR                | Endre fortegn hvis vanlig saldo for rad er kredit | Oppretter et budsjett eller en sammenlignende rapport der alle ugunstige avvik (for eksempel omsetningsunderskudd eller utgiftsoverskridelser) alltid er negative. Bruk denne koden for en **CALC**-kolonnen for å snu fortegnet for kolonnebeløpet hvis den vanlige saldoen for en bestemt rad er kredit (som angitt av en **C** i **Normal saldo**-kolonnen i raddefinisjonen).<p><strong>Obs!</strong>  For <strong>TOT</strong>- og </strong>CAL</strong>-rader som vanligvis har en kreditsaldo, må du passe på å angi en <strong>C</strong> i <strong>Normal saldo</strong>-kolonnen i raddefinisjonen.</p> |
| X0                 | Skjul kolonne hvis bare null eller tomme celler          | Utelater en **FD**-kolonne fra rapporten hvis alle celler i kolonnen er tomme eller inneholde nuller. |
| SR                 | Skjul avrunding                               | Hindrer at beløpene i denne kolonnen avrundes. |
| XR                 | Skjul opprulling                                 | Skjuler en opprulling. Hvis rapporten bruker et rapporteringstre, rulles ikke beløpene i denne kolonnen opp til etterfølgende overordnede noder. |
| RP                 | Gjenta kolonne på hver side                      | Gjenta en bestemt kolonne på hver side i en rapport. Du kan for eksempel bruke **RP**-utskriftskontrollen for å inkludere en kolonne av **ROW**-typen som trekker i radkoder på hver side. |
| WT                 |  Bryt tekst                                      |  Hvis teksten i en kolonne er for lang til at den passer i området, brytes teksten for å holde all teksten i kolonnen. |

#### <a name="conditional-print-control-codes"></a>Kontrollkoder for betinget utskrift

| Kontrollkode for betinget utskrift | Beskrivelse                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (ingen)                         | Nullstill utvalget for betinget utskrift.                                                  |
| P&lt;B                         | Viser en angitt kolonne bare hvis perioden er mindre enn basisperioden.             |
| P&gt;B                         | Viser en angitt kolonne bare hvis perioden er større enn basisperioden.             |
| P=B                            | Viser en angitt kolonne bare hvis perioden er lik basisperioden.              |
| P&lt;=B                        | Viser en angitt kolonne bare hvis perioden er mindre enn eller lik basisperioden. |
| P&gt;=B                        | Viser en angitt kolonne bare hvis perioden er mer enn eller lik basisperioden. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Legge til kontrollkoder for utskrift i en rapportkolonne

1. Åpne kolonnedefinisjonen som skal endres, i Rapportutforming.
2. Dobbeltklikk **Utskriftskontroll**-cellen.
3. I dialogboksen **Utskriftkontroll** velger du en kode i listen **Velg alternativer for utskriftskontroll**. Hvis du vil velge mer enn én kode, holder du nede CTRL-tasten mens du merker kodene.
4. Velg et alternativ i feltet **Alternativer for betinget utskrift**. Som standard er **(ingen)** valgt. Du kan bare velge én kode om gangen for betinget utskrift.
5. Klikk **OK**.

> [!TIP]
> Du kan også angi utskriftskodene direkte i cellen **Utskriftskontroll**. Atskill flere kontrollkoder for utskrift med et komma.

## <a name="column-types"></a>Kolonnetyper
Hvilken type informasjon som hver kolonne i en rapport inneholder, er angitt med verdien i **Kolonnetype**-raden i kolonnedefinisjonen. Hver kolonnedefinisjon må inneholde minst én beskrivelseskolonne (**BSKR**) og én beløpskolonne (**FD**, **RA** eller **BRGN**).

> [!NOTE]
> Kodene for Kolonnetype gjelder ikke for alle regnskapssystemer. Hvis du velger en type som ikke er gyldig for ditt regnskapssystem, vil denne kolonnen være tom i rapporten.

### <a name="specify-a-column-type"></a>Angi en kolonnetype

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk en celle i **Kolonnetype**-raden i den aktuelle kolonnen.
3. Velg en kolonnetype i listen. I tabellen nedenfor beskrives de forskjellige kolonnetypene.

    <table>
    <thead>
    <tr>
    <th>Kode for kolonnetype</th>
    <th>Beskrivelse</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>FD</td>
    <td>Vise økonomiske data når du bruker en <strong>Kobling til finansdimensjoner</strong>-kolonne i raddefinisjonen. Når du velger kolonnetypen <strong>FD</strong>, angis standardinnstillingene automatisk for følgende rader: <ul>
    <li><strong>Posteringskode/attributtkategori:</strong> FAKTISK</li>
    <li><strong>Posteringskode/attributtkategori:</strong> FAKTISK</li>
    <li><strong>Regnskapsår:</strong> BASE</li>
    <li><strong>Periode:</strong> BASE</li>
    <li><strong>Perioder som dekkes:</strong> Tidsbestemt</li>
    <li><strong>Kolonnebredde:</strong> 14</li>
    </ul>
Du kan endre disse standardinnstillingene.</td>
    </tr>
    <tr>
    <td>CALC</td>
    <td>Viser resultatet av en enkel eller kompleks beregning som er angitt i <strong>Formel</strong>-cellen. Hvis du vil ha mer informasjon, kan du se <a href="advanced-formatting-options-financial-reporting.md">Avanserte formateringsalternativer i finansrapportering</a>.</td>
    </tr>
    <tr>
    <td>DESC</td>
    <td>Viser radbeskrivelsen fra raddefinisjonen. Selv om beskrivelseskolonnen ofte er den første kolonnen i rapporten, kan det ha en hvilken som helst plassering.</td>
    </tr>
    <tr>
    <td>ROW</td>
    <td>Viser enkeltradkodene for økonomiske rader fra <strong>Radkode</strong>-kolonnen i raddefinisjonen. Hvis du vil ha mer informasjon, kan du se <a href="row-definitions-financial-reporting.md">Raddefinisjoner i finansrapportering</a>.</td>
    </tr>
    <tr>
    <td>ACCT (kontokoder)</td>
    <td>Viser segmentverdiene eller dimensjonsverdiene for de økonomiske dataene som gjelder for hver rad. For detaljrapporter for kontoer og transaksjoner, skrives den fullt kvalifiserte kontoen ut (for eksempel <strong>110140-070-0101</strong>). Hvis områder har blitt angitt i kolonnen <strong>Kobling til finansdimensjoner</strong> i en tilknyttet raddefinisjon, omsluttes området med klammeparenteser og behandles som om det var én verdi (for eksempel <strong>[110140:110700]-070-[0101:0200]</strong>). For finansrapporter og rapporter på et høyt nivå som er en kombinasjon av flere kontoer, skrives finansdatakoblingen fra raddefinisjonen ut (for eksempel <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>FILL</td>
    <td>Fyller cellen med et tegn som du omslutter med enkle anførselstegn. Hvis du ikke angir et tegn, er kolonnen tom. Hvis du vil fylle en kolonne med en ellipse (...), kan du for eksempel angi <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr>
    <td>PAGE</td>
    <td>Setter inn et loddrett sideskift i rapporten. Kolonnene som vises til høyre for kolonnen <strong>SIDE</strong>, vises på en annen side.</td>
    </tr>
    <tr>
    <td>ATTR</td>
    <td>Hvis regnskapssystemet støtter attributter, vises et konto- eller transaksjonsattributt i kolonnen. Et attributt, som må gjelde for hele kontoen, trekker ut den underliggende konto- eller transaksjonsinformasjonen fra de økonomiske dataen. Attributter på kontonivå viser data fra kontoen, og attributter på transaksjonsnivå viser data som oppstod på det tidspunktet da transaksjonen ble postert. Hvis du velger <strong>ATTR</strong> som kolonnetype, angir du en attributtkategori i detaljraden <strong>Posteringskode/attributtkategori</strong> for kolonnedefinisjonen.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Kolonnen Finansdimensjoner

Følgende **Kolonnedefinisjon**-raddefinisjoner gjelder for kolonner som har kolonnetype **FD** (beløp fra finansdimensjoner).

#### <a name="book-codeattribute-category-cell"></a>Cellen Registerkode/attributtkategori

Cellen **Registerkode/attributtkategori** angir registerkoden for dataene i **FD**-kolonnen. En kolonnedefinisjon kan inkludere flere kolonner for faktisk, budsjettert og statistikk. En kolonnedefinisjon kan også vise ulike perioder, for eksempel gjeldende eller hittil i år og forskjellige beløp. Liten over registerkoder gjenspeiler de faktiske, budsjetterte og statistisk (ikke-finansielle) alternativene som ble fastsatt i de økonomiske dataene.

#### <a name="fiscal-year-cell"></a>Cellen Regnskapsår

Cellen **Regnskapsår** identifiserer regnskapsåret som kolonnen skal inneholde. Året kan være i forhold til basisåret som angis når rapporten genereres. Følgende alternativer er tilgjengelige:

| Alternativ  | Beskrivelse                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASE    | Bruk basisåret som angis når rapporten opprettes.                                                                          |
| BASE+\# | Bruk året som er \# år etter basisåret. Hvis du vil bruke det tredje året etter basisåret, kan du for eksempel angi **BASE+3**. |
| BASE-\# | Bruk året som er \# år før basisåret. Hvis du vil bruke forrige år, kan du for eksempel angi **BASE-1**.                 |
| \#      | Angi det faktiske regnskapsåret.                                                                                                |

#### <a name="period-cell"></a>Cellen Periode

Cellen **Periode** identifiserer regnskapsperiodene som kolonnen skal inneholde. Perioden kan være i forhold til basisperioden som angis når rapporten genereres. Følgende alternativer er tilgjengelige:

| Alternativ          | Beskrivelse |
|-----------------|-------------|
| BASE            | Bruk basisperioden. |
| BASE+\#         | Bruk perioden som er \# perioder etter basisperioden. Hvis du vil bruke den tredje perioden etter basisperioden, kan du for eksempel angi **BASE+3**. |
| BASE-\#         | Bruk perioden som er \# perioder før basisperioden. Hvis du vil bruke forrige periode, kan du for eksempel angi **BASE-1**. |
| BASE-\#:BASE    | Bruk flere perioder, fra flere perioder før basisperioden til basisperioden. Hvis du vil bruke de tre tidligere periodene og basisperioden, kan du for eksempel angi **BASIS-3:BASE**. |
| BASE:BASE+\#    | Bruk flere perioder, fra basisperioden til flere perioder etter basisperioden. Hvis du vil bruke basisperioden og de følgende to periodene, kan du for eksempel angi **BASIS:BASE+2**. |
| BASE-\#:BASE+\# | Bruk flere perioder, fra flere perioder før basisperioden til flere perioder etter basisperioden. Hvis du vil bruke de tre tidligere periodene, basisperioden og de følgende to periodene, kan du for eksempel angi **BASIS-3:BASE+2**. |
| 1:BASE          | Bruk flere perioder, fra den første perioden til basisperioden. |
| \#              | Bruk alltid et bestemt periodenummer. Vi anbefaler ikke at du bruker dette alternativet, siden det reduserer fleksibiliteten til kolonnedefinisjonen. |
| \#                                      : \#           | Bruk alltid et bestemt område med perioder. Vi anbefaler ikke at du bruker dette alternativet, siden det reduserer fleksibiliteten til kolonnedefinisjonen. |

Du kan gå utover grensene for regnskapsåret i noen av spesifikasjonene for perioden, og du kan blande år i et område av perioder. Du kan for eksempel angi periodene som **BASE-5** (for å representere de siste seks periodene) og kjøre en rapport som har basisperiode 2. I dette tilfellet viser rapporten data for de to første periodene i det angitte regnskapsåret og de fire siste periodene i forrige regnskapsår.

### <a name="specify-the-periods-for-an-fd-column"></a>Angi periodene for en FD-kolonne

1. Åpne kolonnedefinisjonen som skal endres, i Rapportutforming.
2. I en **FD**-kolonne dobbeltklikker du cellen i **Periode**-raden, og deretter velger du et alternativ i listen.
3. Fullfør formelen på formellinjen over navigasjonsruten eller i **Periode**-cellen. Erstatt alle nummertegn (\#) med den aktuelle verdien.

#### <a name="periods-covered-cell"></a>Cellen Perioder som er dekket

Cellen **Perioder som er dekket** identifiserer beløpet som kolonnen skal vise. Dette beløpet er i forhold til verdien i cellene **Regnskapsår** og **Periode** for kolonnen. Følgende alternativer er tilgjengelige:

| Alternativ      | Beskrivelse                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Vis summen av aktiviteten for gjeldende periode eller periodeområde. |
| PERIODIC/BB | Vis startsaldoen for gjeldende periode eller periodeområde.   |
| YTD         | Vis summen av aktivitet hittil i år.                               |
| YTD/BB      | Vis startsaldoen for året.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Angi periodene som er dekket for en FD-kolonne

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. I en **FD**-kolonne dobbeltklikker du cellen i raden **Perioder som er dekket**, og deretter velger du et alternativ i listen.

### <a name="attribute-filter-in-a-column-definition"></a>Attributtfilter i en kolonnedefinisjon

Attributter er økonomisk dataverdier som ytterligere definerer en konto eller transaksjon. Kontoattributtene omfatter **Aktiva**, **Gjeld**, **Omsetning** og **Utgift**. Transaksjonsattributtene omfatter **Transaksjonsbeskrivelse** og **Bruk transaksjonsdato**. Attributtstøtte kan variere mellom Microsoft Dynamics ERP-systemer. Cellen **Attributtfilter** begrenser dataene i **FD**-kolonner til bestemte verdier eller områder for attributtkategorier. Selv om denne funksjonen kan brukes sammen med en **ATTR**-kolonne, er ikke **ATTR**-kolonnen nødvendig. I en **FD**-kolonne er det en grense for kontoene eller transaksjonene som rapporten vil inkludere fra attributtfilteret.

> [!NOTE]
> Hvis du vil se hvilke attributter som støttes i ERP-systemet, kan du se integrasjonsveiledningen for systemet.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Bruke et attributtfilter for en FD-kolonne i en rapport

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk **Attributtfilter**-cellen for en **FD**-kolonne.
3. Dobbeltklikk en celle i **Attributt**-kolonnen i dialogboksen **Attributtfilter**, og velg deretter filtertypen.
4. Hvis du vil begrense resultatene ytterligere, kan du angi et område i kolonnene **Fra** og **Til**. **Fra**-cellen må inneholde en positiv verdi.
5. Klikk **OK**.

#### <a name="example-of-an-attribute-filter"></a>Eksempel på et attributtfilter

Følgende eksempel viser en del av en kolonnebeskrivelse som har et kontoattributt i raden **Registerkode/attributtkategori**. Attributtfilteret for denne kolonnen angir området med verdier som skal tas med i rapporten.

|      Filter                  | A    | T                   |
|------------------------------|------|---------------------|
| Kolonnetype                  | BSKR | FD                  |
| Posteringskode/attributtkategori |      | FAKTISK              |
| Regnskapsår                  |      | BASE                |
| Periode                       |      | 1:BASE              |
| Perioder som dekkes              |      | PERIODIC            |
| ...                          |      |                     |
| Kolonnebredde                 | 30   |                     |
| ...                          |      |                     |
| Attributtfilter             |      | Referanse=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Dimensjonsfilteret i en kolonnedefinisjon

Et dimensjonsfilter brukes til å begrense **FD**-kolonnen til bestemte dimensjonsverdier. Filteret kan inkludere én dimensjon, et dimensjonsintervall eller en gruppe med dimensjoner. Filteret kan også inkludere dimensjonsverdisett. Siden dimensjonsverdier kan variere, trenger ikke et ..\\financial-dimensions\\dimension-based system samsvare med en nøyaktig lengde. Filteret brukes, uavhengig av om rapporten omfatter et rapporteringstre. Du kan bruke jokertegn (\* eller ?) i hvilken som helst posisjon. Når du angir flere kontoer, setter du inn et komma mellom kontoene, slik som i følgende eksempel: +Konto=\[1200\], +Konto=\[1100\], Avdeling=\[01?\] Hvis du vil motta alle avdelinger for en bestemt konto, kan du utelate avdelingsdimensjonen fra dimensjonsfilteret. Begge følgende dimensjonsfiltre behandles for eksempel på samme måte:

- +Konto=\[1100\],Avdeling
- +Konto=\[1100\]

Du kan også bruke hvilken som helst kombinasjon av alfanumeriske tegn for nøyaktig samsvar, og du kan angi deldimensjoner. **Lokasjon = \[10\*\]** inneholder for eksempel alle lokasjonsdimensjonsverdier som begynner med 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Bruke et dimensjonsfilter for en kolonne i en rapport

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk **Dimensjonsfilter**-cellen for en **FD**-kolonne.
3. I dialogboksen **Dimensjoner** angir du filtrene som skal brukes.
4. Klikk **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formatere en rapport med flere valutaer i en kolonnedefinisjon

En rapport med flere valutaer kan vise beløp i regnskapsvalutaen i finans, rapportering i finans, den opprinnelige transaksjonsvalutaen eller den oversatte rapporteringsvalutaen. En virksomhets regnskapsvaluta er definert i finansoppsettet. Du må ikke forveksle denne innstillingen med operativsystemets regionale innstillinger, der du kan konfigurere standard valutasymboler som skal brukes i rapporter. Følgende valutarelaterte celler er tilgjengelige i kolonnedefinisjonen:

- **Valutavisning** – Angir valutatypen (rapportering for regnskap, rapportering, transaksjon eller veksling) som transaksjonene vises i. Oversatt til en rapporteringsvalutafunksjon kalles noen ganger valutaomveksling. Valutaomveksling er muligheten til å rapportere økonomimodulbeløp i en valuta som ikke er den funksjonelle eller rapporteringvalutaen for firmaet, eller valutaen som transaksjonen ble registrert i.
- **Valutafilter** – Angi et valutafilter. Bare transaksjoner som er angitt i den valgte valutaen vises i rapporten.

> 
Følg fremgangsmåten nedenfor for å fastslå firmaets regnskapsvaluta.

1. Gå til **Firma**-menyen i Rapportutforming, og klikk **Firmaer**.
2. Velg et firma og klikk deretter **OK** i dialogboksen **Firmaer**.
3. I dialogboksen **Vis firma**, under **Regionale innstillinger**, kan du vise valutaen som er definert for det valgte firmaet.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Angi valutaen i en rapport med flere valutaer

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. Dobbeltklikk **Valutavisning**-cellen i den aktuelle **FD**-kolonnen, og velg deretter alternativet for å vise valutainformasjon: **Regnskapsvaluta for finans**, **Finansrapportering**, transaksjonsvaluta, eller velg for å oversette til en annen rapporteringsvaluta.
3. Dobbeltklikk **Valutafilter**-cellen i den aktuelle **FD**-kolonnen, og velg deretter aktuell valutakode i listen. Bare transaksjoner som er angitt i denne valgte valutaen vises i rapporten.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Eksempel for cellene Valutavisning og Valutafilter

En bruker har gjort følgende valutavalg i kolonnedefinisjonen:

- **Valutafilter:** Yen
- **Valutavisning:** Regnskapsvaluta fra Finans (amerikanske dollar)

På grunn av valutafilteret som er valgt, inneholder rapporten bare transaksjoner som ble angitt i japanske yen (JPY). På grunn av valutavisningen som er valgt, viser rapporten disse transaksjonene i regnskapsvalutaen, amerikanske dollar (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Kombinasjoner for Valutafilter og Valutavisning

Tabellen nedenfor viser rapportresultatene som kan oppstå for ulike kombinasjoner av alternativene i cellene **Valutavisning** og **Valutafilter** på grunn av valgene som ble gjort. Den funksjonelle valutaen er amerikanske dollar.


| Cellen Valutavisning                        | Cellen Valutafilter | Rapportresultat |
|----------------------------------------------|----------------------|---------------|
| Transaksjonsvaluta                 | **YEN**              | **Y6,000** – Resultatet viser bare transaksjoner som ble angitt i JPY. |
| Regnskapsvaluta fra finans | **YEN**              |**$60** – Resultatet viser bare transaksjoner som ble angitt i JPY, og disse transaksjonene vises i USD.<p><strong>Obs!</strong>  Omregningssatsen er omtrent 100 JPY per USD.</p> |
| Regnskapsvaluta fra finans | Tom                | **$2,310** – Resultatet viser alle dataene i regnskapsvalutaen som er angitt i finans.<p><strong>Merk:</strong> Dette beløpet er summen av alle transaksjoner i regnskapsvaluta.</p> |
| Transaksjonsvaluta                 | Tom                | **$2,250** – Resultatet viser alle beløp i valutaen som transaksjonen ble utført i. Dette betyr at totalen legger sammen beløp fra ulike valutaer. |

### <a name="calculation-column-in-a-column-definition"></a>Beregningskolonne i en kolonnedefinisjon

Kolonnetypen **CALC** i en kolonnedefinisjon støtter kompliserte beregninger i **Formel**-cellen, og kan inneholde operatorene **+**, **-**, **\**_ og _*/** samt **IF/THEN/ELSE**-setninger. En beregningskolonne kan også referere til andre kolonner, også etterfølgende kolonner. I tillegg kan en beregningskolonne også omfatte regnskapsåret og perioden som støtter overskrifter for kolonnen. Beregningsformelen kan inneholde opptil 1 024 tegn. Bruk overstyring av spesielt format for å uttrykke beregningsresultatet som en prosent.

> [!NOTE]
> Resultatene av beregningsformler omfatter ikke verdiene i kolonneområder som ikke skrives ut. **A:D** skriver ut **0** (null), mens **A+B+C** for verdier som ikke skal skrives ut, beregner verdien.

#### <a name="operators-in-calculation-columns"></a>Operatorer i beregningskolonner

Hvis du vil addere, subtrahere, multiplisere eller dividere kolonner, angir du kolonnebokstavene i beregningsrekkefølgen, og deretter bruker du den aktuelle operatoren til å skille hver kolonnebokstav. Tabellen nedenfor beskriver operatorene du kan bruke i en beregningskolonne.

| Operatør | Eksempelberegning | Beskrivelse |
|----------|---------------------|-------------|
| +        | A+C                 | Legger beløpet i kolonne A til beløpet i kolonne C. |
| :        | A:C A:C-D           | Legger til en serie med etterfølgende kolonner. Formelen **A:C** legger for eksempel sammen summene av kolonnene A til C, og formelen **A:C-D** legger sammen summene av kolonnene A til C, og deretter trekkes beløpet i kolonne D fra. |
| -        | A-C                 | Trekker beløpet i kolonne A fra beløpet i kolonne C.<p><strong>Merk:</strong> Du kan også bruke minustegnet (-) til å snu fortegnene i en kolonne. Bruke for eksempel <strong>-A+B</strong> for å legge det motsatte av beløpet i kolonne A til beløpet i kolonne B.</p> |
| \*       | A\*C                | Multipliserer beløpet i kolonne A med beløpet i kolonne C. |
| /        | A/C                 | Dividerer beløpet i kolonne A med beløpet i kolonne C. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Bruke en beregningsformel i en kolonnedefinisjon

1. Åpne kolonnedefinisjonen som skal endres i Rapportutforming.
2. I den aktuelle **CALC**-kolonnen skriver du inn en formel i **Formel**-cellen.

#### <a name="complex-calculations"></a>Komplekse beregninger

En kompleks beregning kan inneholde en kombinasjon av cellereferanser, operatorer, verdier og nivåer av nestede parenteser. Hvis du for eksempel vil beregne gjennomsnittet av kolonne A og B, kan du bruke beregningsformelen **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Angi rappportceller i en kolonneberegning

Du kan referere til en bestemt rapportcelle ved å skrive inn en kolonnebokstav og radkode. **B.100** refererer for eksempel til radkode 100 i kolonne B. Du kan dividere en hel kolonne med et bestemt rapportcellebeløp som er i samme kolonne. Beregningen **B/B.100** betyr for eksempel at beløpet i kolonne B skal divideres med verdien i radkode 100 i kolonne B. Hvis beregningen refererer til en kolonne som avhenger av en annen kolonne, løses denne avhengige kolonnen først. Hvis du refererer til en kolonne til en annen kolonne som refererer tilbake til den første kolonnen, vil du forårsake en sirkelreferansefeil.

> [!NOTE]
> Beregningen kan bli feil hvis du endrer beregningsprioriteten for rapporten. Du kan angi beregningsprioriteten i kategorien **Innstillinger** i rapportdefinisjonen.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Multiplisere eller dividere en kolonne med en basisrad

Du kan opprette en kolonne som viser alle verdiene i en angitt kolonne som en prosent av et grunntall. Derfor kan du vise relasjoner mellom rader, for eksempel en prosentdel av en salgsordrerad eller en prosentdel av en rad for totale utgifter. Hvis du vil multiplisere eller dividere hver rad i en bestemt kolonne med en basisrad, angir du kolonnen som skal brukes i beregningen, og deretter angir du **\*BASEROW** eller **/BASEROW**. Skriv for eksempel **C\*BASEROW** eller **C/BASEROW**.

> [!NOTE]
> Når du bruker en basisradberegning i en kolonnedefinisjon, må du sørge for at hver raddefinisjon som brukes med denne kolonnedefinisjonen, inneholder minst én basisrad for beregninger.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Dividere beløpet i en kolonne med antall perioder

Du kan dividere beløpet i en kolonne med et bestemt antall perioder. Formelen **B/Perioder** dividerer for eksempel verdien i kolonne B med antall perioder i kolonne B. Hvis beregningen strekker seg over flere kolonner, angir du antall perioder som skal brukes i beregningen. Formelen **(B+C)/Perioder** summerer for eksempel beløpene i kolonnene B og C, og dividerer deretter resultatet med periodeverdien.

## <a name="additional-resources"></a>Tilleggsressurser

[Raddefinisjoner i Utforming av finansrapport](row-definitions-financial-reporting.md)

[Avanserte formateringsalternativer i finansrapportering](advanced-formatting-options-financial-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]