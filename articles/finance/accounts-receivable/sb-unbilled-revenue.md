---
title: Ufakturert inntekt
description: Denne artikkelen forklarer hvordan du definerer varer og kontoer for å bruke funksjonen for ufakturert inntekt i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: adf6f06ee454f368fa194315a87cfdec9e5e13da
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644175"
---
# <a name="unbilled-revenue"></a>Ufakturert inntekt

Denne artikkelen beskriver funksjonen for ufakturert inntekt der du kan ta med beløp for hele faktureringsplaner på balansen. Disse beløpene er inkludert i en konto for ufakturert inntekt og en motkonto for ufakturert inntekt, og kontrakten faktureres gjennom avdrag.

## <a name="set-up-unbilled-revenue"></a>Konfigurer ufakturert inntekt

Hvis du vil konfigurere ufakturert inntekt, gjør du følgende.

- På siden **Parametere for regelmessig kontraktfakturering** angir du feltene i delen **Ufakturert inntekt**.
- Funksjonen for ufakturert inntekt kan brukes for varer der feltet **Varetype** er satt til **Standard**. Den kan også brukes til utsatte varer. Hvis du vil bruke ufakturert inntekt med kortsiktig funksjonalitet, konfigurerer du kortsiktige alternativer på siden **Parametere for regelmessig kontraktfakturering**.

Hvis du vil konfigurere varer som skal bruke ufakturert inntekt, gjør du følgende.

1. Velg **Legg til** på siden **Oppsett for ufakturert inntekt** på fanen **Varer**.
2. Velg varekoden i **Varekode** på den nye linjen.
3. I feltet **Varerelasjon** velger du varerelasjonen.
4. Gjenta disse trinnene for å legge til flere linjer.
5. Velg **Lagre**.

Hvis du vil konfigurere varer og kontoene for ufakturert inntekt, gjør du følgende.

1. Velg **Legg til** på siden **Oppsett for ufakturert inntekt** på fanen **Kontoer**.
2. Velg varekoden i **Varekode** på den nye linjen.
3. I feltet **Varerelasjon** velger du varerelasjonen.
4. Velg kontoene for ufakturert inntekt, ufakturert rabatt og motkonto for ufakturert inntekt. Hvis du vil bruke de kortsiktige kontoene, må du sette feltet **Kortsiktig ufakturert metode** til **Rullende perioder** eller **Fast år** på siden **Parametere for regelmessig kontraktfakturering**.
5. Gjenta disse trinnene for å legge til flere linjer.
6. Velg **Lagre**.

## <a name="use-unbilled-revenue"></a>Bruk ufakturert inntekt

1. Opprett en faktureringsplan på siden **Alle faktureringsplaner**.
2. Hvis varen ikke er konfigurert til å bruke ufakturert inntekt, velger du **Ufakturert inntekt**-avmerkingsboksen på faktureringsplanlinjen.
3. Angi alternativet **Ufakturert inntekt** til **Ja**. Se deretter gjennom og rediger ufakturert inntekt, ufakturert rabatt og motkontoene for ufakturert inntekt.
4. Velg **Opprett journaloppføring** under **Behandling av ufakturert inntekt** for å opprette den innledende journaloppføringen for ufakturert inntekt. Dette trinnet må være fullført før faktureringsplanen faktureres.
5. Når den innledende journaloppføringen er opprettet, velger du **Generer faktura** for å opprette salgsordrer og postere fakturaene for faktureringsplanene.
6. Når fakturaene er postert, kan du se gjennom revisjonsinformasjonen på fanen **Fornying** på siden **Alle faktureringsplaner**.

### <a name="milestone-billing"></a>Milepælfakturering

Milepælfakturering fungerer med ufakturert inntekt under følgende betingelser:

- Hvis den overordnede varen med milepæl er ufakturert (det er merket av for **Ufakturert inntekt**), og underordnede varer med milepæler (merket er fjernet for **Ufakturert inntekt**), må start- og sluttdatoene for den overordnede varen angis. Disse datoene brukes til å opprette den første journaloppføringen.
- Hvis den overordnede varen med milepæl er ufakturert (merket fjernet for **Ufakturert inntekt**), og underordnede varer med milepæler (det er merket av for **Ufakturert inntekt**), må sluttdatoen være angitt bare for underordnede varer som du vil opprette innledende journaloppføring for.

Hver underordnede vare for milepæl kan behandles separat. Sluttdatoene kan angis når du er klar til å opprette den innledende journaloppføringen.

> [!NOTE]
> Hvis den innledende journaloppføringen for den overordnede varen eller underordnede varer for milepæl allerede er opprettet, eller det allerede er opprettet en faktura, kan du ikke redigere start- og sluttdatoene.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Ufakturert inntekt med lineære utsettelser

Følg denne fremgangsmåten for å bruke ufakturert inntekt med lineære utsettelsesplaner.

1. Opprett en faktureringsplan på siden **Alle faktureringsplaner**.
2. Legg til en vare i faktureringsplanlinjene.
3. Velg **Utsettelser** for linjen.
4. Følg denne fremgangsmåten på siden **Transaksjonsutsettelse**:

    1. Sett **Utsatt**-alternativet til **Ja**.
    2. Endre kontoene etter behov.
    3. I **Tidsplan**-delen velger du **Lineær** og redigerer andre verdier etter behov.
    4. Velg **OK**.

5. Velg **Ufakturert inntekt** for linjen, og følg deretter denne fremgangsmåten:

    1. Angi alternativet **Ufakturert inntekt** til **Ja**.
    2. Velg kontoene som skal bruke ufakturert inntekt, ufakturert rabatt og motkonto for ufakturert inntekt.

6. Velg **Opprett journaloppføring** under **Behandling av ufakturert inntekt** i faktureringsplanen. Du kan også bruke siden **Massebehandling av ufakturert inntekt** til å opprette journaloppføringen.
7. Utsettelsesplanen opprettes. Du kan se gjennom detaljene på siden **Alle utsettelsesplaner**. Når utsettelsesplanen er opprettet, kan du redigere forskjellige verdier for linjevaren i faktureringsplanen. Du kan for eksempel redigere enhetsprisen, antallet eller datoene.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Ufakturert inntekt med hendelsesbaserte utsettelser

Følg denne fremgangsmåten for å bruke ufakturert inntekt med hendelsesbaserte utsettelsesplaner.

1. Opprett en faktureringsplan på siden **Alle faktureringsplaner**.
2. Legg til en vare i faktureringsplanlinjene.
3. Velg **Utsettelser** for linjen.
4. Følg denne fremgangsmåten på siden **Transaksjonsutsettelse**:

    1. Sett **Utsatt**-alternativet til **Ja**.
    2. Endre kontoene etter behov.
    3. Velg **Hendelsesbasert**, **Mal**, **Tildelingstype** og **Utløpskonto** i **Tidsplan**-delen.
    4. Velg **OK**.

5. Velg **Ufakturert inntekt** for linjen, og følg deretter denne fremgangsmåten:

    - Angi alternativet **Ufakturert inntekt** til **Ja**.
    - Velg kontoene som skal bruke ufakturert inntekt, ufakturert rabatt og motkonto for ufakturert inntekt.

6. Velg **Opprett journaloppføring** under **Behandling av ufakturert inntekt** i faktureringsplanen. Du kan også bruke siden **Massebehandling av ufakturert inntekt** til å opprette journaloppføringen.
7. Utsettelsesplanen opprettes. Du kan se gjennom detaljene på siden **Alle utsettelsesplaner**. Når utsettelsesplanen er opprettet, kan du redigere forskjellige verdier for linjevaren i faktureringsplanen. Du kan for eksempel redigere enhetsprisen, antallet eller datoene. Utsettelsesplanen beregnes på nytt basert på de nye verdiene.

Distribusjonene beregnes på nytt basert på tildelingstypen som er valgt (**Prosent**, **Fullføringsprosent** eller **Like beløp**). For tildelingstypen **Variable beløp** omberegnes distribusjonen basert på prosenten som tilsvarer den opprinnelige verdien for hendelsen. Den opprinnelige enhetsprisen er for eksempel $ 100,00, og prosenten av den opprinnelige verdien er $ 55,00 (55 prosent). Hvis enhetsprisen endres til det $ 200,00, blir det variable beløpet for hendelsen $ 110,00 (fremdeles 55 prosent).

> [!NOTE]
> Hvis utsettelsesplanlinjer er gjenkjent, kan ikke faktureringsplanlinjevaren redigeres. Hvis du vil redigere linjevaren, må du først tilbakeføre de gjenkjente linjene. Faktureringsplanlinjen kan deretter oppdateres.

### <a name="unbilled-revenue-and-top-billing"></a>Ufakturert inntekt og toppfakturering

En faktureringsplan angis for tre år, og fakturaene faktureres årlig over en treårsperiode. Hele kontraktbeløpet registreres i kontoen for ufakturert inntekt som årlige fakturaer opprettes fra. Motkontoen er inntektskonto eller konto for utsatt inntekt.

Toppfakturering og ufakturert inntekt fungerer ikke sammen fordi avstemmingsproblemer kan forekomme i økonomimodulen. På siden **Varegruppeoppsett** er for eksempel varegruppe A satt opp slik at feltet **Antall topplinjer** er satt til **2**. Tre elementer er lagt til på siden **Faktureringsplan**. Alle tre varer tilhører varegruppe A. Når den innledende journaloppføringen blir opprettet for funksjonen for ufakturert inntekt, behandles beløpet for alle tre varer til den ufakturerte kontoen. Når fakturaen for faktureringsplanen opprettes, tas bare beløpene for de to øverste varene med. Derfor stemmer ikke fakturabeløpet med beløpet som ble behandlet med kontoen for ufakturert inntekt, og avstemmingsproblemer skjer i økonomimodulen.

Hvis du vil bruke ufakturert inntekt, lar du siden **Varegruppeoppsett** være tom,eller definere alle varegrupper slik at feltet **Antall topplinjer** settes til **0** (null). Hvis du vil bruke toppfakturering, er ingen handlinger for ufakturert inntekt tilgjengelige.

### <a name="examples"></a>Eksempler

Per versjon 10.0.29 blir det lagt til en ny parameter i faktureringsparametere for regelmessig kontrakt. Når den er satt til Ja, aktiverer parameteren **Bruk ufakturerte motkontoer** to nye kontoer i **Oppsett for ufakturert inntekt**. Motkontoene Oppsett for ufakturert inntekt og Motkonto for ufakturert rabatt blir tilgjengelige og brukes når fakturaplaner opprettes i en annen valuta enn regnskapsvalutaen. Bruk av motkontoene sikrer at motkontoene for ufakturert inntekt og ufakturert rabatt blir tilbakeført med de samme valutakursene som sine opprinnelige oppføringer. Den innledende prosessen **Opprett journaloppføring** er den samme med debet til ufakturert inntekt og kredit til inntekt. Hvis du bruker en rabatt, er den opprinnelige journaloppføringen den samme med en debet til Rabatt og kredit til ufakturert rabatt. 

Dette eksemplet viser hvordan du bruker ufakturert inntekt til å føre hele beløpet i en kontrakt i balansen som ufakturert inntekt. Den andre siden av oppføringen er inntekten eller utsatt inntekt. Når du fakturerer kunden, tilbakeføres ufakturert inntekt. Inntektsfæring skjer enten ved fakturering eller i henhold til den utsatte føringsplanen som ble definert.

#### <a name="assumptions"></a>Antagelser

- Den 1. januar i inneværende år signerer en kunde en treårskontrakt for $ 390.
- Kontrakten omfatter to deler: lisenser og en vedlikeholdsavtale.
- Salgsprisen på lisensgebyret er $ 300, og kunden blir fakturert $ 100 den 1. januar hvert kontraktsår. Lisensgebyret på $ 300 blir tatt som inntekt når kontrakten signeres.
- Salgsprisen på vedlikeholdsgebyret er $ 90, og kunden blir fakturert $ 30 den 1. januar hvert kontraktsår. Vedlikeholdsgebyret på $ 90 blir utsatt, og $ 2,50 føres hver måned i kontraktens levetid.
- Kunden blir fakturert $ 130 på begynnelsen (1. januar) av hvert av de tre årene av kontrakten.

#### <a name="steps"></a>Trinn

1. Definer de to frigitte varene som ufakturerte varer. Bruk siden **Oppsett for ufakturert inntekt** til å definere varer og kontoer som bruker ufakturert inntekt.
2. I dette eksemplet utsettes vedlikeholdsgebyret. Varen krever en utsettelsesmal, som defineres på siden **Maler for utsettelse**. Malen har en **månedlig** periodefrekvens og en føringsperiodelengde på 36 måneder. Derfor er inntekten per måned $ 2,50.
3. På siden **Varer som er utsatt som standard** angir du feltet **Vedlikeholdsgebyr** til **Vare som kan utsettes**. Dette trinnet og det neste vil føre til at vedlikeholdsgebyrvaren blir utsatt når den selges eller inkluderes i en faktureringsplan.
4. Velg **Standarder for utsettelse** \> **Mal**, og legg til varen for vedlikeholdsgebyret og den lineære malen fra trinn 2. Varen for vedlikeholdsgebyr vil være koblet til en utsettelsesplan på 36 måneder.
5. Opprett en faktureringsplan som inneholder de to varene som ikke fakturert. Faktureringsplanen for kontrakten er konfigurert med følgende varer.

    | Vare | Startdato | Sluttdato | Beløp | Faktureringshyppighet | Utsettelsesvare | Ufakturert inntekt | Beskrivelse |
    |---|---|---|---|---|---|---|---|
    | Lisens | 01. januar 2022 | 31. desember 2024 | $ 100,00 | Årlig | Nei | Ja | Kunden blir fakturert $ 100,00 hvert år. Totalen på $ 300,00 blir registrert på forhånd som ufakturert inntekt på balansen og som inntekt på resultat. Hver faktura vil redusere det ufakturerte beløpet. |
    | Vedlikehold | 01. januar 2022 | 31. desember 2024 | $ 30,00 | Årlig | Ja | Ja | Kunden blir fakturert $ 30,00 hvert år. Totalen på $ 90,00 blir registrert på forhånd som ufakturert inntekt og utsatt inntekt på balansen. Hver faktura vil redusere det ufakturerte beløpet. Utsatt inntekt blir gjenkjent månedlig i løpet av 36 måneder. |

6. På siden **Alle faktureringsplaner** bruker du prosessen **Opprett journaloppføring** til å postere kontraktverdien til balansen som ufakturert inntekt.

Det opprettes to journaloppføringer, én for hver linje i faktureringsplanen.

| Konto | Debetbeløp | Kredittbeløp |
|---|---|---|
| Konto for ufakturert inntekt | $ 300,00 | |
| Inntektskonto | | $ 300,00 |

| Konto | Debetbeløp | Kredittbeløp |
|---|---|---|
| Konto for ufakturert inntekt | $ 90,00 | |
| Utsatt inntekt | | $ 90,00 |

Kontrakten krever at fakturaen for kunden opprettes ved begynnelsen av hvert år. Bruk prosessen **Generer faktura** til å opprette fakturaen. Når fakturaen opprettes, posteres følgende fakturabilag.

| Konto| Debetbeløp | Kredittbeløp |
|---|---|---|
| Konto for ufakturert inntekt | | $ 130,00 |
| Kundereskontro | $ 130,00 | |

Den samme journaloppføringen blir opprettet med fakturaer som posteres i begynnelsen av de neste to årene. Kontoen for ufakturert inntekt reduseres årlig under prosessen **Generer faktura**. Motkontoen for ufakturert inntekt brukes til å balansere kontoen for ufakturert inntekt når forskjellige valutakurser brukes. 

I det siste trinnet opprettes journaloppføringen for føring hver måned for å føre utsatt inntekt fra vedlikeholdsgebyret. Journaloppføringen kan opprettes ved hjelp av siden **Føringsbehandling**. Du kan også opprette den ved å velge **Føre** for linjene på sidene **Utsettelsesplan**.

| Hovedkonto | Debetbeløp | Kredittbeløp |
|---|---|---|
| Utsatt inntekt | $ 2,50 | |
| Inntekt | | $ 2,50 |

Denne journaloppføringen opprettes hver gang føringsprosessen kjøres for denne utsatte varen (totalt 36 ganger).

#### <a name="short-term-fixed-year"></a>Kortsiktig: fast år

Du kan bruke ufakturert inntekt sammen med kortsiktig funksjonalitet ved å angi feltet **Kortsiktig ufakturert** på siden **Parametere for regelmessig kontraktfakturering**. Følgende eksempel viser beregningene som utføres når ufakturert inntekt brukes sammen med kortsiktig ufakturertmetode **Fast år**.

Det opprettes en faktureringsplan med følgende kriterier:

- **Startdato:** 1. juni 2020
- **Sluttdato:** 31. desember 2021
- **Enhetspris:** $ 100
- **Hyppighet:** månedlig

På siden **Alle faktureringsplaner** opprettes den første journaloppføringen ved hjelp av prosessen **Opprett journaloppføring**. Nåværende kortsiktige og langsiktige beløp beregnes på følgende måte:

- **Gjeldende kortsiktig ufakturert inntektsbeløp:** $ 700
- **Gjeldende langsiktig ufakturert inntektsbeløp:** $ 1200

Fakturaen opprettes for faktureringsperioden fra 1. juni 2020 til 30. november 2020. Nåværende kortsiktige og langsiktige beløp beregnes på følgende måte:

- **Gjeldende kortsiktig ufakturert inntektsbeløp:** $ 100
- **Gjeldende langsiktig ufakturert inntektsbeløp:** $ 1200

Fakturaen opprettes for faktureringsperioden fra 1. desember 2020 til 31. desember 2020. Nåværende kortsiktige og langsiktige beløp beregnes på følgende måte:

- **Gjeldende kortsiktig ufakturert inntektsbeløp:** $ 1200
- **Gjeldende langsiktig ufakturert inntektsbeløp:** $ 0

#### <a name="short-term-rolling-periods"></a>Kortsiktig: rullende perioder

Du kan bruke ufakturert inntekt sammen med kortsiktig funksjonalitet ved å angi kortsiktig ufakturert metode på siden **Parametere for regelmessig kontraktfakturering**. Følgende eksempel viser beregningene som utføres når ufakturert inntekt brukes sammen med kortsiktig ufakturertmetode **Rullende perioder**.

Det opprettes en faktureringsplan med følgende kriterier:

- **Startdato:** 1. juni 2020
- **Sluttdato:** 31. desember 2021
- **Enhetspris:** $ 100
- **Hyppighet:** månedlig

På siden **Alle faktureringsplaner** opprettes den første journaloppføringen ved hjelp av prosessen **Opprett journaloppføring**. Nåværende kortsiktige og langsiktige beløp beregnes på følgende måte:

- **Gjeldende kortsiktig ufakturert inntektsbeløp:** $ 1200
- **Gjeldende langsiktig ufakturert inntektsbeløp:** $ 700

Fakturaen opprettes for faktureringsperioden fra 1. juni 2020 til 30. november 2020. Nåværende kortsiktige og langsiktige beløp beregnes på følgende måte:

- **Gjeldende kortsiktig ufakturert inntektsbeløp:** $ 1200
- **Gjeldende langsiktig ufakturert inntektsbeløp:** $ 100

Fakturaen opprettes for faktureringsperioden fra 1. desember 2020 til 31. desember 2020. Nåværende kortsiktige og langsiktige beløp beregnes på følgende måte:

- **Gjeldende kortsiktig ufakturert inntektsbeløp:** $ 1200
- **Gjeldende langsiktig ufakturert inntektsbeløp:** $ 0

### <a name="items-with-revenue-allocation"></a>Varer med inntektstildeling

To varer som har ulik faktureringshyppighet, blir lagt til i en faktureringsplan. Begge bruker ufakturert inntekt og er utsatte varer.

- **Varenummer 1000:** Surface Pro 128GB

    - **Faktureringshyppighet:** én gang
    - **Enhetspris:** $ 1500
    - **Frittstående salgspris:** $ 1600
    - **Kontraktinntekt:** $ 1465,26

- **Varenummer S0021:** Forsikring som selges sammen med varenummer 1000

    - **Faktureringshyppighet:** månedlig i 12 måneder
    - **Enhetspris:** $ 20 per måned
    - **Frittstående salgspris:** $ 25
    - **Kontraktinntekt:** $ 264,74

Fordi begge varene bruker ufakturert inntekt og inntektstildeling, er det totale kontraktbeløpet på fornyelseslinjen 0 (null). Kolonnen **Kontraktinntekt** legges til og viser kontraktinntektsbeløpet.

Følgende tabell viser den innledende journaloppføringen for varene og fakturaen.

| Hovedkonto | Debetbeløp | Kredittbeløp |
|---|---|---|
| **Vare 1000-journaloppføring** | | | 
| Konto for ufakturert inntekt (401250) | $ 1465,26 | |
| Konto for utsatt inntekt (250600) | | $ 1465,26 |
| **Vare 0021-journaloppføring** | | | 
| Konto for ufakturert inntekt (401250) | $ 274,74 | |
| Konto for utsatt inntekt (250600) | | $ 274,74 |
| **Faktura** | | |
| Konto for ufakturert inntekt | | $ 1465,26 |
| Konto for ufakturert inntekt | | $ 274,74 |
| AR-konto (130100) | $ 1488,16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Endringer i faktureringsplanlinjen, faktureringsdetaljlinjen eller inntektstildeling

Når enhetsprisen eller antallet endres, må kontraktinntektsbeløpet for hver vare som er en del av inntektstildelingen, oppdateres. Derfor beregnes journaloppføringen på nytt.

Enhetsprisen for vare 1000 endres for eksempel fra $ 1500 til $ 1600. I dette tilfellet omberegnes kontraktinntektsbeløpet automatisk som $ 1549,47. Kontraktinntektene for varen S0021 omberegnes som $ 290,53.

Når endringen blir bekreftet og igangsatt, tilbakeføres de første journaloppføringene for begge varene, og nye journaloppføringer opprettes:

- **Vare 1000:** Den opprinnelige journaloppføringen på $ 1465,26 tilbakeføres. En ny journaloppføring på $ 1549,47 opprettes.
- **Vare S0021:** Den opprinnelige journaloppføringen på $ 274,74 tilbakeføres. En ny journaloppføring på $ 290,53 opprettes.

#### <a name="termination"></a>Avslutning

Varen S0021 har startdatoen januar 2020 og sluttdatoen i desember 2020, men avsluttes i juni 2020. Kontraktinntektsbeløpet for begge varene må omberegnes:

- **Vare 1000:** Kontraktinntektene omberegnes som $ 1567,67.
- **Vare S0021:** Kontraktinntektene omberegnes som $ 124,00.

Det opprettes en justeringsjournaloppføring for linjen som avsluttes. Journaloppføringen for linjen som tilhører samme MEA-nummer (ordning for flere elementer), tilbakeføres, og det opprettes en ny journaloppføring:

- **Vare 1000:** Den opprinnelige journaloppføringen på $ 1465,26 tilbakeføres. En justeringsjournaloppføring på $ 1549,47 opprettes.
- **Vare S0021:** Den opprinnelige journaloppføringen på $ 274,74 tilbakeføres. En ny journaloppføring på $ 124,00 opprettes.
