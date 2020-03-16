---
title: Opprette en permisjons- og fraværsplan
description: Opprett permisjonsplaner i Dynamics 365 Human Resources for ulike typer permisjon.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ed7a47068c451cd3ffaa26ee709599373858721b
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087306"
---
# <a name="create-a-leave-and-absence-plan"></a>Opprette en permisjons- og fraværsplan

Definer permisjons- og fraværsplaner i Dynamics 365 Human Resources for hver permisjonstype du tilbyr. Permisjons- og fraværsplaner kan avsettes med forskjellige frekvenser, for eksempel årlig, månedlig eller annenhver måned. Du kan også definere en plan som et tilskudd, der en enkelt avsetning skjer på en bestemt dato. Du kan for eksempel opprette en plan som gir flytende ferier årlig.

Med lagdelte permisjonsplaner kan de ansatte motta fordeler basert på hvor lang tid de har vært i en organisasjon. Lagdelte planer aktiverer automatisk registrering i ekstra fordelstimer.

Du kan angi maksimalt overførte beløp eller minimumssaldoer for å sikre at de ansatte bare bruker fordelstimene de er tildelt.

Med en lagdelt plan kan du for eksempel gi en fordel på 80 timer betalt avspasering (PTO) til nye ansatte. Deretter kan du gi 120 timer etter 60 måneders ansettelse.

Du kan også opprette stillingsbaserte permisjonsfordeler, for eksempel fordelstider bare for ledere.

## <a name="create-a-leave-plan"></a>Opprette en permisjonsplan

1. På siden **Permisjon og fravær** velger du **Opprett ny plan**.

2. Under **Detaljer** angir du **Navn**, **Startdato**, **Beskrivelse** og **Permisjonstype** for planen.

3. Definer avsetninger i kategorien **Avsetninger**. Avsetninger avgjør når og hvor ofte en ansatt blir tildelt avspasering. I dette trinnet definerer du policyer om når det skal gis avsetning, og retningslinjer for vurdering av fordeler.

   1. Velg en verdi fra rullegardinboksen **Avsetningsfrekvens**:

      - Daglig
      - Ukentlig
      - Annenhver uke
      - Annenhver måned
      - Månedlig
      - Kvartalsvis
      - Hvert halvår
      - Årlig
      - Ingen

   2. Velg et alternativ fra rullegardinboksen **Avsetningsperiodegrunnlag** for å bestemme startdatoen som skal brukes til beregning av avsetningsperioder:

      | Avsetningsperiodegrunnlag | Beskrivelse |
      | --- | --- |
      | **Startdato for plan** | Startdatoen for avsetningsperioden er datoen da planen er tilgjengelig. |
      | **Spesifikk dato for ansatt** | Startdatoen for avsetningsperioden avhenger av en ansatthendelse:</br><ul><li>Egendefinert (du må angi et grunnlag for en avsetningsdato for hver enkelt registrering)</li><li>Jubileumsdato</li><li>Opprinnelig ansettelsesdato</li><li>Ansiennitetsdato</li><li>Arbeiderens justerte startdato</li><li>Arbeiderens startdato</li></ul> |

   3. Velg et alternativ fra rullegardinboksen **Belønningsdato for avsetning**:

      - **Sluttdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den siste dagen i belønningsperioden. Hvis du vil avsette riktig tid, må avsetningsprosessen inkludere hele perioden. Hvis for eksempel avsetningsperioden er 1. januar 2020 til 31. januar 2020, må du kjøre avsetningen for 1. februar 2020 for å inkludere januar.

      - **Startdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den første dagen i belønningsperioden.

   4. Velg et alternativ fra rullegardinboksen **Avsetningspolicy ved registrering**: Denne verdien definerer hvordan avsetningen skal beregnes når en ansatt registreres midt i en avsetningsperiode.

      - **Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager. Denne differansen brukes når avsetninger behandles.

      - **Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.

      - **Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.

   5. Velg et alternativ fra rullegardinboksen **Avsetningspolicy ved avregistrering**: Denne verdien definerer hvordan avsetningen skal beregnes når en ansatt avregistreres midt i en avsetningsperiode.

      - **Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager. Denne differansen brukes når avsetninger behandles.

      - **Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.

      - **Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.

4. Definer avsetningsplanen i kategorien **Avsetningsplan**. Avsetningsplanen bestemmer følgende:

   - Hvordan en ansatt avsetter avspasering
   - Hvilke beløp den ansatte skal avsette
   - Hvilke beløp som skal overføres

   Du kan opprette lag for å tildele avspasering basert på forskjellige nivåer.

   Hvis du har timebaserte ansatte, kan du belønne dem med fridager basert på antall arbeidstimer i stedet for ansiennitet i organisasjonen. Data for arbeidstimer lagres vanligvis i et system for tid og fremmøte. Du kan importere vanlige timer og overtidstimer som er arbeidet fra systemet for tid og fremmøte, og bruke dem som grunnlag for bonusen til en ansatt.

   1. Velg et alternativ fra rullegardinboksen **Avsetningstype**:

      - **Måneder med jobberfaring** – Baser avsetningsplanen på antall måneder med jobberfaring.

      - **Arbeidstimer** – Baser avsetningsplanen på arbeidstimer. Hvis du vil ha mer informasjon om avsetninger for arbeidstimer, kan du se [Avsette fridager basert på arbeidstimer](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Hvis du vil ha mer informasjon om avsetningssaldoer, kan du se [Avsette fridager basert på arbeidstimer](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Angi verdier i avsetningsplantabellen:

      - **Måneder med jobberfaring** – Det minste antallet måneder som ansatte må arbeide for å være berettiget til avsetninger. Hvis du ikke krever et minimum, setter du verdien til 0.

      - **Arbeidstimer** – Det minste antallet timer som ansatte må arbeide per avsetningsperiode for å være berettiget til avsetninger. Hvis du ikke krever et minimum, setter du verdien til 0.

      - **Avsetningsbeløp** – Antallet timer eller dager som ansatte skal avsette per periode. Perioden er basert på avsetningsfrekvensen.

      - **Minimumssaldo** – Du kan bruke en negativ for minimumssaldoen hvis ansatte kan be om mer permisjon enn de har tilgjengelig.

      - **Maksimal overføring** – Avsetningsprosessen justerer permisjonssaldoer som overskrider maksimal overføringssaldo på merkedagen til startdatoen.

      - **Tildelingsbeløp** – Det opprinnelige antallet timer eller dager som ansatte gis når de registrerer seg for permisjonsplanen første gang. Beløpet avsettes ikke for hver avsetningsperiode.

5. Velg **Lagre**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Avsette tid basert på arbeidstimer

Hvis du har timebaserte ansatte, kan du belønne dem med fridager basert på antall arbeidstimer i stedet for ansiennitet i organisasjonen. Data for arbeidstimer lagres vanligvis i et system for tid og fremmøte. Du kan importere vanlige timer og overtidstimer som er arbeidet fra systemet for tid og fremmøte, og bruke dem som grunnlag for bonusen til en ansatt.

Når du velger arbeidstimer som avsetningstype, kan du bruke to typer timer for avsetningen: vanlig og overtid. Avsetningsbehandling for planer av arbeidstimer bruker avsetningsfrekvensen, sammen med periodebasisen, til å bestemme timene som skal avsettes.

### <a name="annual-accrual-frequency"></a>Årlig avsetningsfrekvens

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Månedlig avsetningsfrekvens

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 31/8/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Avsetningsfrekvens annenhver måned

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 81                  | 6                  |        
| 31/8/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Ukentlig avsetningsfrekvens

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 31/8/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Tilordnede permisjonsplaner for ansatte

I den ansattes tilordnede permisjonsplaner vises nivågrunnlaget og typen timer for planer basert på arbeidstimer. De faktiske arbeidstimene for avsetningsperiodene per gjeldende vises dato også for aktive planer.

### <a name="loading-data"></a>Laster inn data

Du kan importere faktiske timer ved hjelp av enheten **Antall arbeidstimer for permisjon og fravær** i databehandling. Hvis du bruker arbeidstidskalendre, validerer importen at normaltimer som er utført, ikke overstiger de planlagte timene på en dag definert av kalenderen. Importen validerer også at antallet arbeidstimer for en gitt dag ikke overskrider 24 timer. 

Du trenger følgende informasjon for å importere faktisk antall timer som skal brukes i denne avsetningsprosessen for permisjon:

- Personalnummer 
- Arbeidsdag
- Type
- Timeantall

En enkelt dato kan bare ha én av hver type knyttet til seg.

| Personalnummer       | Arbeidsdag           | Type                  | Timeantall                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6/8/2018             | Vanlig               | 8                    |       
| 000337                | 7/8/2018             | Vanlig               | 8                    |
| 000337                | 7/8/2018             | Overtid              | 3                    |
| 000337                | 8/8/2018             | Vanlig               | 8                    |
| 000337                | 7/8/2018             | Vanlig               | 8                    |
| 000337                | 9/8/2018             | Vanlig               | 8                    |

## <a name="enrollments-and-balances"></a>Registreringer og saldoer

### <a name="enrollment-date"></a>Registreringsdato

Registreringsdatoen bestemmer når en ansatt kan begynne å avsette avspasering. Hvis for eksempel en ansatt registreres i en ferieplan 15. juni 2018, kan vedkommende ikke avsette avspasering før 15. juni 2018.

### <a name="current-balance"></a>Gjeldende saldo

Gjeldende saldo er hvor mye permisjon som er tilgjengelig for avspaseringsforespørsler. Dette beløpet inkluderer avsetninger godkjente forespørsler og justeringer til og med den gjeldende datoen.

### <a name="current-balance-examples"></a>Eksempler på gjeldende saldo

#### <a name="annual-plan"></a>Årsplan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Årlig            | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 1. januar 2019 (1.1.2019), for å inkludere hele perioden.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Forespørselsbeløp | Gjeldende saldo (per 1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Gjeldende saldo (160) = avsetningsbeløp (200) – forespurt beløp (40)

#### <a name="semimonthly-plan"></a>Halvmånedlig plan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/2/2018        | Halvmånedlig       | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 1. mai 2018 (1.5.2018), for å inkludere hele perioden.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Forespørselsbeløp | Gjeldende saldo (per 1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Gjeldende saldo (22) = avsetningsbeløp (5 x 6) – forespurt beløp (8)

#### <a name="monthly-plan"></a>Månedlig plan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/2/2018        | Halvmånedlig       | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 1. mai 2018 (1.5.2018), for å inkludere hele perioden.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Forespørselsbeløp | Gjeldende saldo (per 1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Gjeldende saldo (7) = avsetningsbeløp (5 x 3) – forespurt beløp (8)

### <a name="forecasted-balance"></a>Anslått saldo

*Prognosesaldo* er hvor mye permisjon som er tilgjengelig på en bestemt dato. Avsetninger og overføringsjusteringer er anslått frem til denne datoen.

Human Resources bruker følgende formel:

Mandag prognosesaldo = gjeldende saldo – forespørsler + avsetninger – overføringsjustering

### <a name="forecasted-balance-examples"></a>Eksempler på prognosesaldoer

#### <a name="annual-plan"></a>Årsplan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Årlig            | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 15. februar 2019 (15.2.2019), for å inkludere hele perioden.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Gjeldende saldo | Prognosesaldo (per 15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Prognosesaldo (40) = avsetningsbeløp (20) + gjeldende saldo (40) – overføringsjustering (20)

#### <a name="semimonthly-plan"></a>Halvmånedlig plan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/2/2018        | Halvmånedlig       | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 15. februar 2019 (15.2.2019), for å inkludere hele perioden.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Gjeldende saldo | Prognosesaldo (per 15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Prognosesaldo (35) = avsetningsbeløp (5 x 3) + gjeldende saldo (40) – overføringsjustering (20)

#### <a name="monthly-plan"></a>Månedlig plan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/2/2018        | Halvmånedlig       | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 15. februar 2019 (15.2.2019), for å inkludere hele perioden.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Gjeldende saldo | Prognosesaldo (per 15.2.2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Prognosesaldo (30) = avsetningsbeløp (10 x 1) + gjeldende saldo (40) – overføringsjustering (20)

### <a name="proration-balance-examples"></a>Eksempler på fordelingssaldo

#### <a name="prorated-monthly-plan"></a>Fordelt månedlig plan

**Oppsett av plan**

| Startdato for plan | Avsetningsfrekvens | Avsetningsperiodegrunnlag |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Månedlig           | Startdato for plan      |

**Resultater**

| Ansatt            | Måneder med jobberfaring | Registreringsdato | Startdato | Avsetningsbeløp | Behandle avsetning | Beholdning |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1/6/2018        | 1/6/2018   | 1,00           | 1/9/2018        | 3,00    |
| Jay Norman          | 0,00              | 15/6/2018       | 15/6/2018  | 1,00           | 1/9/2018        | 2.53    |

#### <a name="full-accrual-monthly-plan"></a>Full avsetning, månedlig plan

**Oppsett av plan**

| Startdato for plan | Avsetningsfrekvens | Avsetningsperiodegrunnlag |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Månedlig           | Startdato for plan      |

**Resultater**

| Ansatt            | Måneder med jobberfaring | Registreringsdato | Startdato | Avsetningsbeløp | Behandle avsetning | Beholdning |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1/6/2018        | 1/6/2018   | 1,00           | 1/9/2018        | 3,00    |
| Jay Norman          | 0,00              | 15/6/2018       | 15/6/2018  | 1,00           | 1/9/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Ingen avsetning, månedlig plan

**Oppsett av plan**

| Startdato for plan | Avsetningsfrekvens | Avsetningsperiodegrunnlag |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Månedlig           | Startdato for plan      |

**Resultater**

| Ansatt            | Måneder med jobberfaring | Registreringsdato | Startdato | Avsetningsbeløp | Behandle avsetning | Beholdning |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1/6/2018        | 1/6/2018   | 1,00           | 1/9/2018        | 3.00    |
| Jay Norman          | 0.00              | 15/6/2018       | 15/6/2018  | 1.00           | 1/9/2018        | 2.00    |

## <a name="configure-preview-features"></a>Konfigurere forhåndsversjonsfunksjoner

Hvis du har aktivert forhåndsversjonsfunksjoner for permisjon og fravær, må du konfigurere innstillinger for dem også.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. **Forhåndsversjonsfunksjon: Konfigurer flere permisjonstyper for en enkel permisjons- og fraværsplan**. Du kan definere en permisjonstype for hver post i avsetningsplantabellen.

   > [!IMPORTANT]
   > Du kan ikke deaktivere denne funksjonen etter at du har aktivert den.

2. **Forhåndsversjonsfunksjon: Bruk fulltidsekvivalens**. Hvis du aktiverer denne forhåndsversjonsfunksjonen, bruker Human Resources fulltidsekvivalensen (FTE) som er definert for stillingen, til å fordele en ansatts avsetning. Hvis for eksempel FTE er 0,5 og avsetningsbeløpet er 10, vil den ansatte avsette 5. Du kan bare bruke denne funksjonen hvis du aktiverer flere permisjonstyper.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)
- [Avsette permisjons- og fraværsplaner](hr-leave-and-absence-accrue.md)