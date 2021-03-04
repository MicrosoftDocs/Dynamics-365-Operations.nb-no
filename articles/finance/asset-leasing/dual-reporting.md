---
title: Dobbel rapportering
description: Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446582"
---
# <a name="dual-reporting"></a>Dobbel rapportering

[!include [banner](../includes/banner.md)]

Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie. Det er nødvendig å ha erfaring med posteringslag i Microsoft Dynamics 365 Finance, og dette gjør det enklere å forstå eksemplet.

## <a name="example"></a>Eksempel

Det følgende eksemplet gjør rede for en leieavtale under italiensk lovbestemt rapportering, ved hjelp av både kontantprinsippmetoden og IFRS-rapporteringsmetoder. Firmaet må opprette tre tablåer for å følge både de italienske lovbestemte kravene og IFRS 16-kravene. Det kreves ett tablå for IFRS 16, ett tablå for lovbestemte krav og ett tablå for å tilbakeføre lovbestemte posteringer automatisk. Tablåene blir opprettet som vist i følgende tabeller.

**IFRS 16-tablå**

IFRS 16-tablået konfigureres slik at det er i samsvar med IFRS 16-regnskapsstandarden. Alle oppføringer som posteres i dette tablået, posteres på et egendefinert lag.

| Navn                                    | Beskrivelse    |
|-----------------------------------------|----------------|
| Registertype                               | IFRS 16        |
| Tablåbeskrivelse                        | IFRS 16        |
| Posteringslag                           | Tilpasset lag 1 |
| Leietype                              | Finance        |
| Regnskapsrammeverk                    | IFRS 16        |
| Konfigurasjon av leieperiode / levetid         | 0,00           |
| Konfigurasjon av nåværende verdi / virkelig verdi på aktivum | 0,00           |
| Korttidsterskel                    | 12             |
| Lavverditerskel                     | 5 000,00       |
| Betal til leverandør                           | Nr.             |

**Lovbestemt tablå**

Det lovbestemte tablået er et kontantprinsipptablå der firmaet gjør rede for leieutgiftene som kontantbeløpet som betales hver måned i leie. Dette tablået produserer ikke en bruksrettseiendel eller leieforpliktelse.

| Navn                                    | Beskrivelse |
|-----------------------------------------|-------------|
| Registertype                               | Lovbestemt   |
| Tablåbeskrivelse                        | Lokal GAAP  |
| Posteringslag                           | Gjeldende     |
| Leietype                              | Automatisk   |
| Regnskapsrammeverk                    | Kontantgrunnlag  |
| Konfigurasjon av leieperiode / levetid         | 0,00        |
| Konfigurasjon av nåværende verdi / virkelig verdi på aktivum | 0,00        |
| Korttidsterskel                    | 0           |
| Lavverditerskel                     | 0           |
| Betal til leverandør                           | Nr.          |

**Lovbestemt tilbakeføringstablå**

Det lovbestemte tilbakeføringstablået konfigureres på samme måte som det lovbestemte tablået.

| Navn                                    | Beskrivelse                    |
|-----------------------------------------|--------------------------------|
| Registertype                               | Lovbestemt – tilbakeføring           |
| Tablåbeskrivelse                        | Tablå for å tilbakeføre lovbestemt tablå |
| Posteringslag                           | Tilpasset lag 1                 |
| Leietype                              | Automatisk                      |
| Regnskapsrammeverk                    | Kontantgrunnlag                     |
| Konfigurasjon av leieperiode / levetid         | 0,00                           |
| Konfigurasjon av nåværende verdi / virkelig verdi på aktivum | 0,00                           |
| Korttidsterskel                    | 0                              |
| Lavverditerskel                     | 0                              |
| Betal til leverandør                           | Nr.                             |

I dette eksemplet er det opprettet en leieavtale som har følgende innstillinger i fanene **Generelt** og **Linjer i betalingsplan**.

**Fanen Generelt**

| Felt                      | Verdi            |
|----------------------------|------------------|
| Trinnvis lånerente | 5 %               |
| Startdato          | 01.01.2020         |
| Leiegruppe                | Bygninger        |
| Leverandør                     | 1001             |
| Aktivaets gjennomsnittsverdi    | 245 000          |
| Aktivalevetid          | 120              |
| Annuitetstype               | Vanlig annuitet |
| Sammensetningsintervall       | Månedlig          |

**Fanen Linjer i betalingsplan**

| Felt             | Verdi      |
|-------------------|------------|
| Startdato        | 01.01.2020   |
| Periodeintervall   | Måneder     |
| Perioder           | 24         |
| Sluttdato          | 31.12.2020 |
| Betalingsfrekvens | Månedlig    |
| Betalingsbeløp    | 1 000      |

Hvis du vil gjøre rede for denne leien under to rammeverk, bruker du et gjeldende posteringslag og et egendefinert posteringslag. Følgende tabell viser et eksempel på hver journaloppføring som kreves for å representere økonomien riktig under hver rapporteringsstandard. En detaljert beskrivelse av hver journaloppføring for den første måneden av leieavtalen gis etterpå.

<table>
<thead>
<tr>
<th rowspan='3'>Kontonummer</th>
<th rowspan='3'>Beskrivelse</th>
<th colspan='3'>Lovbestemt tablå (gjeldende lag)</th>
<th rowspan='3'>Gjeldende lag totalt</th>
<th>Tilbakeføringstablå (egendefinert lag)</th>
<th colspan='4'>IFRS 16-tablå (egendefinert lag)</th>
<th rowspan='3'>Gjeldende lag + egendefinert lag totalt</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Leieutgift</td>
<td>1 000,00</td>
<td></td>
<td></td>
<td>1 000,00</td>
<td>-1 000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankgebyr</td>
<td></td>
<td>3,00</td>
<td></td>
<td>3,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3,00</td>
</tr>
<tr>
<td>3</td>
<td>Mva-utgift</td>
<td></td>
<td>5,00</td>
<td></td>
<td>5,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5,00</td>
</tr>
<tr>
<td>4</td>
<td>Avregningskonto</td>
<td>-1 000,00</td>
<td>1 000,00</td>
<td></td>
<td>0,00</td>
<td>1 000,00</td>
<td></td>
<td>-1 000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Leverandørreskontro</td>
<td></td>
<td>-1 008,00</td>
<td>1 008,00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Bruksrettseiendel</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22 794,00</td>
<td></td>
<td></td>
<td></td>
<td>22 793,90</td>
</tr>
<tr>
<td>7</td>
<td>Forpliktelse for finansiell leie</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22 794,00</td>
<td>1 000,00</td>
<td>-94,97</td>
<td></td>
<td>-21 888,87</td>
</tr>
<tr>
<td>8</td>
<td>Renteutgift</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Kontanter</td>
<td></td>
<td></td>
<td>-1 008,00</td>
<td>-1 008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1 008,00</td>
</tr>
<tr>
<td>10</td>
<td>Avskrivningskostnad</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Akkumulert avskrivning</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Som den foregående tabellen viser kreves det tre tablåer for å rapportere både under lovbestemt rapportering og IFRS-rapportering.

- Det lovbestemte tablået registrerer leiebetalingen i henhold til reglene for kontantprinsippregnskap under det gjeldende laget.
- Det lovbestemte tilbakeføringstablået tilbakestiller lovbestemte journaloppføringer.
- IFRS 16-tablået oppretter journaloppføringene som kreves under IFRS 16.

Du trenger bare å angi en leieavtale én gang. Du kan deretter åpne **Tablåer**-siden for å se alle tablåene som er knyttet til leieavtalen.

> [!NOTE]
> Når du oppretter tablåene, må alle tre knyttes til samme leiepost.

Den første journaloppføringen registrerer leieutgiften under det lovbestemte tablået. Du kan opprette betalingene i en bunke eller ved å velge betalingsplanen i det lovbestemte tablået.

I dette eksemplet produseres følgende journaloppføring for det lovbestemte tablået fra betalingsplanen.

### <a name="lease-payment--1312020--je-100"></a>Leiebetaling – 31.01.2020 – JE 100

| Kontotype | Kontonummer | Lag   | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Finans       | 1              | Gjeldende | Leieutgift       | 1 000,00 |          |
| Finans       | 4              | Gjeldende | Avregningskonto    |          | 1 000,00 |

En regnskapsassistent bruker standard Dynamics 365-funksjonalitet til å opprette en faktura for å betale leien utenfor Aktivaleie. I stedet for å velge **Leieutgift** som debetkonto velger regnskapsassistenten en avregningskonto for å generere følgende oppføring.

### <a name="ap-process--1312020--je-110"></a>AP-prosess – 31.01.2020 – JE 110

| Kontotype | Kontonummer | Lag   | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Finans       | 4              | Gjeldende | Avregningskonto    | 1 000,00 |          |
| Finans       | 2              | Gjeldende | Bankgebyr            | 3,00     |          |
| Finans       | 3              | Gjeldende | Mva-utgift         | 5,00     |          |
| Leverandør       | 5              | Gjeldende | Leverandørreskontro    |          | 1 008,00 |

Når utdraget er utstedt til leverandøren, følger du den vanlige betalingsprosessen. Følgende journaloppføring genereres i løpet av denne prosessen.

### <a name="cash-payment--1312020--je-120"></a>Kontantbetaling – 31.01.2020 – JE 120

| Kontotype | Kontonummer | Lag   | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Leverandør       | 5              | Gjeldende | Leverandører    | 1 008,00 |          |
| Bank         | 9              | Gjeldende | Kontanter                |          | 1 008,00 |

Nå har du gjort fullstendig rede for denne leien under lovbestemte rapporteringskrav og kan generere en råbalanse ved hjelp av det gjeldende laget. Systemet returnerer en råbalanse med følgende tall.

<table>
<thead>
<tr>
<th rowspan='3'>Kontonummer</th>
<th rowspan='3'>Beskrivelse</th>
<th colspan='3'>Lovbestemt tablå (gjeldende lag)</th>
<th rowspan='3'>Gjeldende lag totalt</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Leieutgift</td>
<td>1 000,00</td>
<td></td>
<td></td>
<td>1 000,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankgebyr</td>
<td></td>
<td>3,00</td>
<td></td>
<td>3,00</td>
</tr>
<tr>
<td>3</td>
<td>Mva-utgift</td>
<td></td>
<td>5,00</td>
<td></td>
<td>5,00</td>
</tr>
<tr>
<td>4</td>
<td>Avregningskonto</td>
<td>-1 000,00</td>
<td>1 000,00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Leverandørreskontro</td>
<td></td>
<td>-1 008,00</td>
<td>1 008,00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Bruksrettseiendel</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Forpliktelse for finansiell leie</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Renteutgift</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Kontanter</td>
<td></td>
<td></td>
<td>-1 008,00</td>
<td>-1 008,00</td>
</tr>
<tr>
<td>10</td>
<td>Avskrivningskostnad</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Akkumulert avskrivning</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Hvis du vil bruke IFRS 16-tallene til å kjøre den samme råbalansen, må lovbestemte regnskapsjournaloppføringer tilbakeføres, og IFRS 16-journaloppføringer må posteres. For å tilbakeføre lovbestemte journaloppføringer omfatter dette eksemplet et lovbestemt tilbakeføringstablå som har samme konfigurasjon som det lovbestemte tablået, men en motsatt posteringsprofil. Det lovbestemte tablået *debiterte* for eksempel en leieutgiftskonto, men tilbakeføringstablået *krediterer* denne kontoen. Disse relasjonene kan enkelt defineres i posteringskontoene for Aktivaleie på siden **Parametere for aktivaleie** (**Aktivaleie \> Oppsett \> Parametere for aktivaleie**).

Når den samme prosessen som ble brukt for det lovbestemte tablået, brukes for tilbakeføringstablået, produseres følgende journaloppføring. Forskjellen er at tilbakeføringstablået posterer tilbakeføringsoppføringene fra det lovbestemte tablået. Tilbakeføringsoppføringene gjøres også på det egendefinerte laget. Når en råbalanse kjøres på det gjeldende laget, blir ikke tilbakeføringsjournaloppføringene tatt med.

### <a name="lease-payment--1312020--je-130"></a>Leiebetaling – 31.01.2020 – JE 130

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|--------|---------------------|----------|----------|
| Finans       | 4              | Egendefinert | Avregningskonto    | 1 000,00 |          |
| Finans       | 1              | Egendefinert | Leieutgift       |          | 1 000,00 |

Nå som du har fjernet de lovbestemte journaloppføringene, skal du postere alle journaloppføringer som kreves av IFRS 16, i IFRS 16-tablået. Disse oppføringene omfatter den opprinnelige føringen av bruksrettseiendelen og gjelden, og posten for rente og avskrivning.

### <a name="initial-recognition--112020--je-140"></a>Opprinnelig føring – 01.01.2020 – JE 140

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet     | Kredit    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Finans       | 6              | Egendefinert | Bruksrettseiendel                | 22 793,90 |           |
| Finans       | 7              | Egendefinert | Forpliktelse for finansiell leie |           | 22 793,90 |

Leiebetalingen posteres som de andre leiebetalingene. Grunnen til å bruke avregningskontoen er å sikre at kontanter bare krediteres én gang.

### <a name="lease-payment--1312020--je-150"></a>Leiebetaling – 31.01.2020 – JE 150

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet    | Kredit   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Finans       | 7              | Egendefinert | Forpliktelse for finansiell leie | 1 000,00 |          |
| Finans       | 4              | Egendefinert | Avregningskonto         |          | 1 000,00 |

Journaloppføringen for renteutgift genereres fra nedbetalingsplanen for gjeld.

### <a name="interest-expense--1312020--je-160"></a>Renteutgift – 31.01.2020 – JE 160

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet | Kredit |
|--------------|----------------|--------|--------------------------|-------|--------|
| Finans       | 8              | Egendefinert | Renteutgift         | 94.97 |        |
| Finans       | 7              | Egendefinert | Forpliktelse for finansiell leie |       | 94.97  |

Journaloppføringen for avskrivningskostnad genereres fra avskrivningsplanen for aktiva.

### <a name="depreciation-expense--1312020--je-170"></a>Avskrivningskostnad – 31.01.2020 – JE 170

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet  | Kredit |
|--------------|----------------|--------|--------------------------|--------|--------|
| Finans       | 10             | Egendefinert | Avskrivningskostnad     | 949.75 |        |
| Finans       | 11             | Egendefinert | Akkumulert avskrivning |        | 949.75 |

Når alle disse journaloppføringene er opprettet og postert, vises følgende verdier for egendefinert lag 1. Vær oppmerksom på at den siste kolonnen omfatter bankgebyret, merverdiavgift (mva) og reduksjonen i kontanter fra forrige lag, men den omfatter ikke journaloppføringene for lovbestemt rapportering. Derfor oppnår du ekte funksjonalitet for dobbel rapportering. Nå trenger firmaet bare å kjøre råbalansen og kombinere det gjeldende laget og det egendefinerte laget for å opprette en IFRS-råbalanse.

| Kontonr. | Beskrivelse              | Lovbestemt tablå\-gjeldende lag\-JE\-100\-debet \(kredit\) | Lovbestemt tablå\-gjeldende lag\-JE\-110\-debet \(kredit\) | Lovbestemt tablå\-gjeldende lag\-JE\-120\-debet \(kredit\) | Gjeldende lag \- totaler | - | Tilbakeføringstablå\-egendefinert lag\-JE\-130\-debet \(kredit\) | IFRS 16-tablå\-egendefinert lag\-JE\-140\-debet \(kredit\) | IFRS 16-tablå\-egendefinert lag\-JE\-150\-debet \(kredit\) | IFRS 16-tablå\-egendefinert lag\-JE\-160\-debet \(kredit\) | IFRS 16-tablå\-egendefinert lag\-JE\-170\-debet \(kredit\) | Egendefinert lag \+ gjeldende lag \- totaler |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Leieutgift            | 1 000\.00                                         |                                                   |                                                   | 1 000\.00               |   | \-1 000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankgebyr                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | Mva-utgift              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Avregningskonto         | \-1 000\.00                                       | 1 000\.00                                         |                                                   | 0\.00                   |   | 1 000                                           |                                                | \-1 000                                        |                                                |                                                | 0\.00                                   |
| 5          | Leverandørreskontro         |                                                   | \-1 008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | Bruksrettseiendel                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Forpliktelse for finansiell leie |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22 794                                       | 1 000                                          | \-94\.97                                       |                                                | \-21 888\.87                            |
| 8          | Renteutgift         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Kontanter                     |                                                   |                                                   | \-1 008\.00                                       | \-1 008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1 008\.00                             |
| 10         | Avskrivningskostnad     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Akkumulert avskrivning |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]