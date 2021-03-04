---
title: Begreper for permisjon og fravær
description: Dette emnet beskriver begreper for permisjon og fravær og hvordan avspaseringssaldoer fastsettes.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462142"
---
# <a name="leave-and-absence-concepts"></a>Begreper for permisjon og fravær

Begreper og termer som er beskrevet i dette emnet, kan hjelpe deg med å finne ut hvordan en ansatt belønnes med avspasering, og hvordan den ansattes tidssaldoer beregnes. Hvis du vil ha mer informasjon om permisjons- og fraværsadministrasjon, kan du se [Administrasjon av permisjon og fravær](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Permisjonsplandetaljer

### <a name="start-date"></a>Startdato

Startdatoen er datoen som avsetningsbehandlingen starter på. Startdatoen fungerer også som merkedato for å beregne overføringsbeløp.

## <a name="accruals"></a>Avsetninger

Avsetninger bestemmer når og hvor ofte en ansatt belønnes med avspasering. Retningslinjer om når avsetningene skal tildeles og policyer om fordeling, defineres i **Avsetninger**-delen når du definerer permisjons- og fraværsplanen.

### <a name="accrual-frequency"></a>Avsetningsfrekvens

Avsetningsfrekvensen definerer hvor ofte permisjon avsettes eller tildeles. Følgende alternativer er tilgjengelige:

- Daglig
- Ukentlig
- Annenhver uke
- Halvmånedlig
- Månedlig
- Kvartalsvis
- Hvert halvår
- Årlig
- Ingen

### <a name="accrual-period-basis"></a>Avsetningsperiodegrunnlag

Avsetningsperiodegrunnlaget fastsetter datoen som brukes til å beregne avsetningsperioder. Følgende alternativer er tilgjengelige:

- **Startdato for plan**
- **Spesifikk dato for ansatt** – Når dette alternativet er valgt, fastsetter verdien kilden til den opprinnelige datoverdien som brukes til å beregne avsetningsperioder. Følgende alternativer er tilgjengelige:

    - Egendefinert
    - Jubileumsdato
    - Opprinnelig ansettelsesdato
    - Ansiennitetsdato
    - Arbeiderens justerte startdato
    - Arbeiderens startdato

### <a name="accrual-award-date"></a>Belønningsdato for avsetning

Belønningsdatoen for avsetning bestemmer når en ansatt tildeles fri. Følgende alternativer er tilgjengelige:

- **Sluttdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den siste dagen i belønningsperioden.

    Hvis du vil avsette riktig tid, må avsetningsprosessen inkludere hele perioden. Avsetningsperioden er for eksempel fra 1. januar 2018 til og med 31. januar 2018. For at januar skal tas med i dette tilfelle, må avsetningen kjøres for 1. februar 2018.

- **Startdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den første dagen i belønningsperioden.

### <a name="accrual-policy-on-enrollment"></a>Avsetningspolicy ved registrering

Avsetningspolicyen ved registrering angir hvordan avsetning beregnes når ansatte registreres i midten av en avsetningsperiode. Følgende alternativer er tilgjengelige:

- **Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager. Denne differansen brukes når avsetninger behandles.
- **Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.
- **Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.

### <a name="accrual-policy-on-unenrollment"></a>Avsetningspolicy ved avregistrering

Avsetningspolicyen ved avregistrering angir hvordan avsetning beregnes når ansatte avregistreres i midten av en avsetningsperiode. Følgende alternativer er tilgjengelige:

- **Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager. Denne differansen brukes når avsetninger behandles.
- **Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.
- **Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.

## <a name="accrual-schedule"></a>Avsetningsplan

Avsetningsplanen bestemmer hvordan en ansatt skal avsette avspasering, og hvor mye den ansatte skal avsette og overføre. Lag kan opprettes slik at avspasering tildeles basert på forskjellige nivåer.

### <a name="months-of-service"></a>Måneder med jobberfaring

**Måneder med jobberfaring**-verdien definerer det minste antallet måneder som ansatte må arbeide for å være berettiget til avsetninger. Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.

### <a name="hours-worked"></a>Arbeidstimer

**Arbeidstimer**-verdien definerer det minste antallet timer som ansatte må arbeide per avsetningsperiode for å være berettiget til avsetninger. Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.

### <a name="accrual-amount"></a>Avsetningsbeløp

Avsetningsbeløpet er antallet timer eller dager som ansatte skal avsette per periode. Perioden er basert på avsetningsfrekvensen.

### <a name="minimum-balance"></a>Minste saldo

En negativ verdi kan brukes for minimumssaldoen hvis ansatte kan be om mer permisjon enn de har tilgjengelig.

### <a name="maximum-carry-forward"></a>Maksimal overføring

Avsetningsprosessen justerer permisjonssaldoer som overskrider maksimal overføringssaldo på merkedagen til startdatoen.

### <a name="grant-amount"></a>Tildelingsbeløp

Tildelingsbeløpet er det opprinnelige antallet timer eller dager som ansatte gis når de registrerer seg for permisjonsplanen første gang. Beløpet avsettes ikke for hver avsetningsperiode.

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

Avsetninger behandles 1. januar 2019 (1.1.2019), slik at hele perioden er inkludert.

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

Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.

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

Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.

**Resultater**

| Avsetningsbeløp | Minste saldo | Maksimal overføring | Forespørselsbeløp | Gjeldende saldo (per 1.1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Gjeldende saldo (7) = avsetningsbeløp (5 x 3) – forespurt beløp (8)

### <a name="forecasted-balance"></a>Prognosesaldo

*Prognosesaldo* er hvor mye permisjon som er tilgjengelig på en bestemt dato. Avsetninger og overføringsjusteringer er anslått frem til denne datoen.

Følgende formel brukes:

Mandag prognosesaldo = gjeldende saldo – forespørsler + avsetninger – overføringsjustering

### <a name="forecasted-balance-examples"></a>Eksempler på prognosesaldoer

#### <a name="annual-plan"></a>Årsplan

**Oppsett av plan**

| Startdato for plan | Registreringsdato | Avsetningsfrekvens | Avsetningsperiodegrunnlag | Belønningsdato for avsetning    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Årlig            | Startdato for plan      | Slutt på avsetningsperiode |

Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.

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

Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.

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

Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.

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
| Jeannette Nicholson | 0,00              | 1/6/2018        | 1/6/2018   | 1,00           | 1/9/2018        | 3,00    |
| Jay Norman          | 0,00              | 15/6/2018       | 15/6/2018  | 1,00           | 1/9/2018        | 2.00    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]