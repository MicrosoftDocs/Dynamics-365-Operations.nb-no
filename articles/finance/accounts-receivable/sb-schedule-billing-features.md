---
title: Funksjoner for faktureringsplan
description: Denne artikkelen beskriver funksjonene for faktureringsplaner, for eksempel prissettingsmetoder, eskaleringer og rabatter, justeringsdatoer, fordeling, tilbakeføring av fakturering og deling av varegrupper.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: b6cfebc2bbfe06e118bfc96f9ae0df6323805e39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853590"
---
# <a name="billing-schedule-features"></a>Funksjoner for faktureringsplan

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjonene for faktureringsplaner og faktureringsplanlinjer. Den beskriver de ulike metodene som brukes til prissetting, hvordan du bruker eskaleringer og rabatter, og hvordan du tilbakefører en faktureringsperiode. Den inneholder også eksempler på fordelingsberegninger og delte varegrupper.

## <a name="pricing-methods"></a>Prissettingsmetoder

Du kan bruke en av følgende prissettingsmetoder til å beregne enhetsprisen for en vare:

* Leilighet
* Standard
* Lag
* Flatt lag

### <a name="flat-pricing"></a>Flat prissetting

Når metoden for flat prissetting brukes, kan enhetsprisen for et linjeelement i faktureringsplanen på siden **Alle faktureringsplaner** redigeres til en hvilken som helst verdi du ønsker. Verdien for **Prisenhet** er alltid **1**. Derfor er verdiene for **Enhetspris** og **Nettobeløp** for en vare de samme.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standardprissetting (uten forretningsavtale)

Når standard prissettingsmetode brukes uten en forretningsavtale, definerer du enhetsprisen for et linjeelement i faktureringsplanen ved å velge **Behandling av produktinformasjon** på siden **Frigi produktdetaljer**. Enhetsprisen vises i delen **Grunnleggende salgspris**. Den beregnes som *Pris* &divide; *Prisantall*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standardprissetting (med forretningsavtale)

Eksemplene nedenfor viser standard prissettingsberegninger når det finnes en forretningsavtale. Du kan opprette forretningsavtaler fra siden **Frigi produktdetaljer**.

Begge eksemplene bruker en vare med følgende prisgrupper.

| Antall fra | Antall til | U av M | Pris | Prisenhet |
|---|---|---|---|---|
| 0 | 100 | Hver | 1.50 | 1 |
| 100 | 200 | Hver | 1.25 | 1 |
| 200 | 999999 | Hver | 1.00 | 1 |

**Eksempel 1**

Fakturaantallet er 250, og standard prissettingsmetode brukes. Siden antallet er i prisintervallet 200–999 999, er enhetsprisen 1,00. 

Nettobeløpet beregnes på følgende måte:

*Nettobeløp* = (*Antall* &times; *Pris*) &divide; *Prisenhet* = (250 &times; 1,00) &divide; 1 = 250

**Eksempel 2**

Fakturaantallet er 100, og standard prissettingsmetode brukes. Siden fakturaantallet er i prisintervallet 0–100, er enhetsprisen 1,50.

> [!NOTE]
> Fakturaantallet er i området 0–100 i stedet for i området 100–200, fordi i virkemåten for standard antallssamsvar vil et antall samsvare hvis det er *større enn eller likt* "fra"-antallet og *mindre enn* "til"-antallet.

Nettobeløpet beregnes på følgende måte:

*Nettobeløp* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Lagprissetting

For følgende eksempele har en vare følgende prisgrupper.

| Antall fra | Antall til | U av M | Pris | Prisenhet |
|---|---|---|---|---|
| 0 | 100 | Hver | 1.50 | 10 |
| 100 | 200 | Hver | 1.25 | 10 |
| 200 | 999999 | Hver | 1.00 | 10 |

Hvis fakturaantallet er 250 og nivåprissettingsmetoden brukes, beregnes prisene på varene på følgende måte, basert på prissettingsgruppene:

- **De første 100 varene:** 100 &times; 1,50 = 150,00
- **Den neste 100 varene:** 100 &times; 1,25 = 125,00
- **Gjenstående varer:** 50 &times; 1,00 = 50,00

Nettobeløpet beregnes på følgende måte:

*Nettobeløp* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Når nettobeløpet er beregnet, beregnes enhetsprisen ved å dele nettobeløpet på antallet:

*Enhetspris* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Flat nivåprissetting

For følgende eksempele har en vare følgende prisgrupper.

| Antall fra | Antall til | U av M | Flatt lagbeløp | Prisenhet |
|---|---|---|---|---|
| 0 | 50 | Hver | 100.00 | 50 |
| 50 | 200 | Hver | 150.00 | 200 |

Følgende tabell viser fakturaene og enhetsprisene for de ulike antallene som kjøpes. Nettobeløpet beregnes først, og deretter beregnes enhetsprisen.

| Faktura | Antall innkjøpt | Enhetspris | Nettobeløp |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Eskaleringer og rabatter

En *eskalering* er en prisøkning for en fremtidig faktureringsperiode som fakturaen ennå ikke er opprettet for. En *rabatt* er en prisreduksjon for en fremtidig faktureringsperiode som fakturaen ennå ikke er opprettet for.

I abonnementsfakturering kan ikke eskaleringer og rabatter brukes i ettertid for en faktureringsplan. Du kan for eksempel ikke bruke en eksalering på en faktureringsplan tre måneder i fortiden og behandle den. Du kan med andre ord ikke bruke en prisøkning som skjedde for tre måneder siden.

Du kan bruke en eskalering eller rabatt på en faktureringsplan eller faktureringsplanlinje på et av følgende steder:

- Listesiden **Alle/Aktive faktureringsplaner**
- En spesifikk faktureringsplan
- En spesifikk faktureringsplanlinje

### <a name="apply-an-escalation-or-discount"></a>Bruk en eskalering eller rabatt

Følg denne fremgangsmåten for å bruke en eskalering eller rabatt i en faktureringsplan.

1. Velg en faktureringsplan eller en faktureringsplanlinje.
2. Velg **Eskalering og rabatt** enten på fanen **Eskalering og rabatt** eller på faktureringsplanlinjen.
3. Hvis en forbrukerprisindeks brukes til å beregne eskaleringen eller rabatten, velger du en verdi i feltet **Beregning av forbrukerprisindeks**.
4. Velg **Ny** for å legge til en eskalerings- eller rabattlinje.
5. For en rabatt merker du av for **Rabatt**. For en eskalering lar du merket for **Rabatt** være fjernet.
6. Angi feltene **Startdato** og **Frekvens**.
7. For utsatte varer som bruker funksjonen for ufakturert inntekt, angir du **Sluttdato**-feltet.
8. Angi feltet **Prosent**, **Beløp** eller **Tidsplan for forbrukerprisindeks**.
9. Angi **Sluttdato**-feltet.
10. Velg **OK**.
11. Gjenta trinn 4 til og med 10 for hver ekstra eskalerings- eller rabattlinje du trenger.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Felter på siden Faktureringsplanlinjer

Siden **Faktureringsplanlinjer** inneholder følgende felter.

| Felt | Beskrivelse |
|---|---|
| Varenummer | Varenummeret for faktureringsplanlinjen. Dette feltet er bare tilgjengelig når siden er åpnet fra en vare på en faktureringsplanlinje. |
| Beregning for konsumprisindeks | <p>Velg metoden som brukes til å beregne eskalering av forbrukerprisindeksen:</p><ul><li>**Tidligere forbrukerprisindeks** – Bruk verdien for den forrige forbrukerprisindeksen i beregningen av eskaleringen.</li><li>**Basisforbrukerprisindeks** – Bruk verdien for basisforbrukerprisindeksen i beregningen av eskaleringen.</li></ul> |
| **Linje**-rutenettet | |
| Rabatt | <p>Merk av for å angi om endringen i beløpet er en eskalering eller rabatt:</p><ul><li>**Valgt** – Endringen bruker en rabatt på faktureringsplanen eller faktureringsplanlinjen.</li><li>**Ikke avmerket** – Endringen gjelder en eskalering av en faktureringsplan eller en planleggingslinje.</li></ul><p>Innstillingen for denne boksen kan ikke endres for varer som bruker funksjonen for ufakturert inntekt. I tillegg kan rabatter ikke brukes på varer som bruker inntektsdeling.</p> |
| Startdato | Velg startdatoen for eskaleringen eller rabatten. |
| Frekvens | Velg frekvensen for eskaleringen eller rabatten: **Ingen**, **Månedlig**, **Kvartalsvis**, **Hvert halvår** eller **Årlig**. |
| Prosent | Angi prosentverdien for eskaleringen eller rabatten. |
| Beløp | Angi beløpet for eskaleringen eller rabatten. |
| Tidsplan for konsumprisindeks | Velg tidsplanen for forbrukerprisindeksen som brukes for beregningene. |
| Sluttdato | <p>Velg sluttdatoen for eskaleringen eller rabatten.</p><p>**Merk:** Dette feltet er obligatorisk for varer som bruker funksjonen for ufakturert inntekt.</p> |
| Nummer på utsettelsesplan | <p>Nummeret på utsettelsesplanen.</p><p>Dette feltet er bare tilgjengelig når siden er åpnet fra en faktureringsplanlinje.</p> |
| Journalpartinummer | <p>Journalpartinummeret.</p><p>Dette feltet er bare tilgjengelig når siden er åpnet fra en faktureringsplanlinje.</p> |
| Totalt rabattbeløp | <p>Summen av rabattbeløp for alle linjene i rutenettet.</p><p>Dette feltet er bare tilgjengelig når siden er åpnet fra en faktureringsplanlinje.</p> |
| Gjeldende kortsiktig ufakturert inntektsbeløp | <p>Det gjeldende kortsiktige ufakturerte inntektsbeløpet.</p><p>Dette beløpet vises når en kortsiktig henvisningsmetode er valgt på siden **Parametere for gjentakende kontraktfakturering**, og når kontoene for linjeelementet er satt opp på siden **Oppsett av ufakturert inntekt**.</p> |
| Gjeldende langsiktig ufakturert inntektsbeløp | <p>Det gjeldende langsiktige ufakturerte inntektsbeløpet.</p><p>Dette beløpet vises når en kortsiktig henvisningsmetode er valgt på siden **Parametere for gjentakende kontraktfakturering**, og når kontoene for linjeelementet er satt opp på siden **Oppsett av ufakturert inntekt**.</p> |

## <a name="proration-examples"></a>Eksempler på fordeling

Beregninger for fordeling kan være basert på antall dager eller antall måneder. Metoden som brukes til fordelingsberegningen, er angitt på siden **Parametere for gjentakende kontraktfakturering**. Fordelingsmetoden påvirker hvordan beløpene beregnes for en faktureringsplan i følgende situasjoner:

- Innledende oppretting
- Bruk av en eskalering eller rabatt
- Avslutning
- Plassering eller fjerning av venting
- Tillegg av støtte eller fornyelse

Fordelingsmetoden påvirker også beregningene i rapporten for månedlig gjentakende omsetning.

### <a name="example-1"></a>Eksempel 1

Det årlige beløpet for en faktureringsplan er USD 5000. Startdatoen er 12. august 2019, og sluttdatoen er 22. desember 2019. Faktureringsfrekvensen er årlig. Det fordelte beløpet beregnes på følgende måter, avhengig av om beregningsmetoden er daglig eller månedlig:

- **Daglig**

    - *Antall dager* = *Sluttdato* – *Startdato* + 1 = 133 dager
    - *Antall dager i året* = 11. august 2020 – 12. august 2019 + 1 = 366 dager
    - *Fordelt beløp* = 5000 &times; (133 &divide; 366) = 1816,94

- **Månedlig**

    - *Andel i startmåned* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Midterste måneder* = 3
    - *Andel i sluttmåned* = 22 &divide; 31
    - Fordelt beløp = 5000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Eksempel 2

Det årlige beløpet for en faktureringsplan er USD 12 000. Startdatoen er 1. august 2019, og sluttdatoen er 31. desember 2019. Faktureringsfrekvensen er årlig. Det fordelte beløpet beregnes på følgende måter, avhengig av beregningsmetoden:

- **Daglig**

    - *Antall dager* = *Sluttdato* – *Startdato* + 1 = 153 dager
    - *Antall dager i året* = 31. juli 2020 – 1. august 2019 + 1 = 366 dager
    - *Fordelt beløp* = 12 000 &times; (153 &divide; 366) = 5016,39

- **Månedlig (hele måneden)**

    - *Antall måneder* = 5
    - *Total antall måneder* = 12
    - *Fordelt beløp* = (12 000 &times; 5) &divide; 12 = 5000

## <a name="reversing-a-period-billing"></a>Tilbakeføring av en periodefakturering

For dette eksemplet har en faktureringsplan bare én linje:

- Fakturering utføres månedlig i 12 måneder fra januar til desember.
- Fakturaer er opprettet for alle perioder frem til april.

Du ønsker å tilbakeføre fakturaen for april.

Hvis det ennå ikke er opprettet en salgsfaktura for fakturaperioden i april, kan du slette salgsordren. I dette tilfellet ville statusen **Fakturert** for detaljen blitt fjernet. Siden det er opprettet en faktura for faktureringsperioden, kan imidlertid ikke statusen **Fakturert** for detaljen fjernes. Hvis du vil tilbakeføre faktureringen for april, må du derfor opprette en motpostering av kreditnota for linjen.

1. På siden **Alle faktureringsplaner** oppretter du en planlinje for den samme varen.
2. Endre **Antall**-verdien for varen til den negative verdien av det opprinnelige antallet.
3. Angi feltet **Faktureringsfrekvens** til **Én gang**.
4. Oppdater start- og sluttdatoene slik at de samsvarer med datoene for faktureringsdetaljlinjen du vil opprette en kreditnota for. I dette eksemplet kan du sette startdatoen til 1. april 2019 og sluttdatoen til 30. april 2019.
5. Lagre endringene.
6. Åpne siden **Generer faktura**, og opprett salgsordren som har kreditnotaen for den angitte perioden.
7. Valgfritt: Poster fakturaen.

Når du går gjennom linjene for faktureringsplanen, vil du se at den nye linjen har en kobling til kreditnotaen. Den opprinnelige linjen vil fortsatt ha en kobling til den opprinnelige fakturaen fra april.

## <a name="split-item-group-examples"></a>Eksempler på deling av varegrupper

For dette eksemplet er følgende oppsett på plass:

- På siden **GParametere for gjentakende kontraktfakturering** er det merket av for **Del etter varegruppe**, og feltet **Unik plantype** er satt til **Kunde**.
- Tre varegrupper er opprettet: **PREFIKS**, **DATAHUB** og **SPP**.
- Kunden US-001 har flere faktureringsplaner der varegruppen er PREFIKS eller DATAHUB.
- Kunden US-002 har flere faktureringsplaner der varegruppen er PREFIKS eller SPP.

| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---|
| SCH001 | US-001 | PREFIKS |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | PREFIKS |
| SCH004 | US-002 | SPP |

Kunden US-001 kjøper en fornyelsesvare som tilhører PFEFIKS-varegruppen. Denne transaksjonen er en ny salgsordre.

| Salgsordrenr. | Kunde | Hovedvare | Fornyingsvare | Fornyingsvaregruppe | Faktureringsplannummer |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PREFIKS | SCH001 |

Når fakturaen for salgsordren posteres, legges fornyelsesvaren til i den eksisterende faktureringsplanen (SCH001) for kunden. Denne faktureringsplanen bruker PREFIKS-varegruppen. Alle fornyelsesvarer som tilhører den samme varegruppen, plasseres i samme faktureringsplan.

**Hode**
 
| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---| 
| SCH001 | US-001 | PREFIKS |

**Linje**

| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---|
| SCH001 | US-001 | D0002 |

Kunden US-001 kjøper nå en fornyelsesvare som tilhører SPP-varegruppen. Denne transaksjonen er en ny salgsordre.

| Salgsordrenr. | Kunde | Hovedvare | Fornyingsvare | Fornyingsvaregruppe | Faktureringsplannummer |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

For øyeblikket har ikke kunden US-001 en faktureringsplan som bruker SPP-varegruppen. Derfor opprettes det en ny faktureringsplan.

**Hode**

| Faktureringsplannummer| Kunde | Varegruppe |
|---|---|---|
| SCH005 | US-001 | SPP |

**Linje**

| Faktureringsplannummer | Kunde | Varegruppe |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Flere faktureringsplaner for samme sluttbruker og kunde

For dette eksemplet er følgende oppsett på plass:

- På siden **GParametere for gjentakende kontraktfakturering** er det merket av for **Del etter varegruppe**, og feltet **Unik plantype** er satt til **Sluttbruker**.
- På siden **Sluttbrukere** defineres følgende relasjon mellom kunde og sluttbruker.

    | Kundekonto | Sluttbrukerkonto |
    |---|---|
    | US-001 | US-221 |

Flere faktureringsplaner opprettes for kombinasjonen av kunde og sluttbruker. Siden **Del etter varegruppe** er valgt på siden **Parametere for gjentakende kontraktfakturering**, kan det opprettes flere faktureringsplaner for samme relasjon mellom kunde og sluttbruker.

| Faktureringsplannummer | Kunde | Sluttbrukerkonto | Øverste varegruppe |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

På siden **Vareoppsett** oppretter du relasjoner mellom støtte- og fornyelsesvarer.

| Varekode | Varerelasjon | Støttevare | Fornyingsvare | Fornyingsvaregruppe |
|---|---|---|---|---|
| Tabell | D001 | ITEM27 | D007 | IG1 |
| Tabell | D002 | ITEM28 | D005 | IG2 |
| Tabell | D003 | ITEM29 | D006 | IG3 |

Du oppretter nå en salgsordre for kunden US-001. Denne salgsordren inneholder varer fra siden **Vareoppsett**. Når du oppretter salgsordren, åpner du siden **Støtte- og fornyelsesprosess** og angir feltet **Sluttbrukerkonto** og eventuell annen nødvendig informasjon for fornyelsesvaren.

Når fakturaen for transaksjonen er opprettet og postert, opprettes det forskjellige faktueringsplaner for kombinasjonen av kunde/sluttbruker og varegruppe. Flere enn én linje i den samme salgsordren kan tilordnes til samme faktureringsplan.

| Salgsordrenr. | Kunde | Sluttbrukerkonto | Hovedvare | Støttevare | Fornyingsvare | Faktureringsplannummer |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
