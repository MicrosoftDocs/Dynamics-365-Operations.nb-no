---
title: Lønn basert på registreringer
description: Dette emnet forklarer hvordan lønn beregnes basert på arbeiderregistreringer.
author: johanhoffmann
manager: tfehr
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8e92759bd567a973a0d3bce7b8b99be1edbc0e1e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434394"
---
# <a name="pay-based-on-registrations"></a>Lønn basert på registreringer

[!include [banner](../includes/banner.md)]

Dette emnet forklarer i detalj hvordan lønn beregnes basert på arbeiderregistreringer. Det inneholder eksempler som viser hvordan de forskjellige kombinasjonene av oppsettalternativer som er tilgjengelige for beregningen, påvirker resultatet. Her er noen av områdene som vil bli dekket:

- Fleksitid
- Overtid
- Pauser
- Vekslekoder
- Lønnsposter
- Lønnsavtaler
- Parametere for timeregistrering
- Fravær

## <a name="the-use-of-flex-time"></a>Bruken av fleksitid

Fleksitid er definert i tidsprofilene som brukes i Timeregistrering. Det finnes to fleksiprofiltyper: **Fleksi+** og **Fleksi-**. Når en arbeider registrerer tid i perioden Fleksi+, økes arbeiderens fleksisaldo med timene som ble brukt. Arbeideren får ikke noen kompensasjon for timene som ble brukt i løpet av perioden i Fleksi+. Arbeideren kan imidlertid ta fri i periodene Fleksi-, og få kompensasjon for timene fra sin fleksisaldo. Fritid i fleksiperiodene regnes derfor som fravær av systemet.

## <a name="scenarios-based-on-flex-periods"></a>Scenarier som er basert på fleksiperioder

De to scenariene nedenfor er basert på en fleksiprofil som representerer en arbeidsdag. I begge scenariene beregnes lønn i henhold til fleksiperioden der arbeideren stempler inn og ut.

### <a name="flex-profile-for-one-workday"></a>Fleksiprofil for én arbeidsdag

| Profiltype  | Start    | Slutt      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 AM | 06:00 AM | Mandag  |
| Fleksi+         | 06:00 AM | 07:00 AM | Mandag  |
| Stemple inn      | 07:00 AM | 07:00 AM | Mandag  |
| Normaltid | 07:00 AM | 02:30 PM | Mandag  |
| Fleksi-         | 02:30 PM | 03:30 PM | Mandag  |
| Utstempling     | 03:30 PM | 03:30 PM | Mandag  |
| Overtid     | 03:30 PM | 06:00 AM | Tirsdag |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Scenario 1: En arbeider registrerer innstempling i en Fleksi+ periode og utstempling i en Fleksi- periode

Arbeiderens registreringer for dagen ser slik ut.

| Journalregistreringstype | Start    | Slutt      |
|---------------------------|----------|----------|
| Stemple inn                  | 06:30 AM | 06:30 AM |
| Produksjonsjobb            | 06:30 AM | 02:45 PM |
| Utstempling                 | 02:45 PM | 02:45 PM |

Arbeiderens registreringer for dagen beregnes og overføres til lønn på **Godkjenn**-siden (**Timeregistrering** &gt; **Gjennomgå og godkjenn** &gt; **Godkjenn**). Når registreringene er beregnet, kan resultatet av beregningen vises i kategorien **Tider**. 

For å forstå dette scenariet kan du se følgende felt.

| Fleksi + | Fleksi - | Tidspunkt | Lønnstid |
|--------|--------|------|----------|
| 0.50   | 0,75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Beregning av Fleksi+

I henhold til fleksiprofilen er tiden mellom 06:00 AM og 07:00 AM en periode av typen Fleksi+. Hvis arbeideren stempler inn kl. 06:30 AM, får han/hun derfor 0,5 timer. Denne tiden legges til arbeiderens fleksikontoen.

#### <a name="calculation-of-flex-"></a>Beregning av Fleksi-

I henhold til fleksiprofilen begynner Fleks- perioden kl. 02:30 PM og slutter kl. 03:30 PM. Hvis arbeideren stempler ut kl. 02:45 PM, registreres de 45 minuttene (0,75 timer) som gjenstår i perioden Fleksi-, som lønnstid, og den samme tiden trekkes fra arbeiderens fleksikonto. De 45 minuttene inkluderes i lønnstid fordi arbeideren vil få lønn for de gjenværende 45 minuttene i perioden Fleksi-. Hvis arbeideren er fraværende i løpet av perioden Fleksi-, trekkes de 45 minuttene fra arbeiderens fleksikonto.

#### <a name="calculation-of-time"></a>Beregning av tid

Tiden blir beregnet som tiden mellom innstempling og utstempling, det vil si 06:30 AM til 14:45 PM, tilsvarende 8,25 timer.

#### <a name="calculation-of-pay-time"></a>Beregning av lønnstid

Lønnstid er tiden en arbeider gis lønn. I dette scenarioet er arbeideren på jobb i 8,25 timer (**Tid**). **Lønnstid** beregnes imidlertid som 8,50 timer, fordi arbeideren får lønn i perioden Fleksi- etter utstempling. Lønnstid er lik planlagt arbeidstid fordi Fleksi+ tid legges til arbeiderens fleksikonto, ikke til lønnstid. Fraværstiden i perioden Fleksi- kompenseres for av lønnstiden og trekkes fra arbeiderens fleksikonto.

| Tidspunkt              | Registreringstype | Lønnstid (timer)      |
|-------------------|-------------------|-----------------------|
| 6:30 AM – 7:00 AM | Fleksi+             | 0                     |
| 7:00 AM – 2:45 PM | Normaltid     | 7,75                  |
| 2:45 PM – 3:30 PM | Fleksi-             | 0,75 (fraværsperioden) |
|                   | Sum             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Scenario 2: En arbeider jobber i hele perioden Fleksi-, og jobber også overtid

Arbeiderens registreringer for dagen ser slik ut.

| Journalregistreringstype | Start    | Slutt      |
|---------------------------|----------|----------|
| Stemple inn                  | 06:30 AM | 06:30 AM |
| Produksjonsjobb            | 06:30 AM | 05:00 PM |
| Utstempling                 | 05:00 PM | 05:00 PM |

Når du har beregnet journalregistreringene på **Godkjenn** -siden, kan du vise resultatet av beregningen i kategorien **Timer**. For å forstå dette scenariet kan du se følgende felt.

| Fleksi + | Fleksi - | Tidspunkt  | Lønnstid | Lønn overtid |
|--------|--------|-------|----------|--------------|
| 0.50   | 0.00   | 10,50 | 10,00    | 1.50         |

#### <a name="calculation-of-flex"></a>Beregning av Fleksi+

I henhold til fleksiprofilen er tiden mellom 06:00 AM og 07:00 AM en periode av typen Fleksi+. Hvis arbeideren stempler inn kl. 06:30 AM, får han/hun derfor 0,5 timer av Fleksi + tid på fleksisaldoen.

#### <a name="calculation-of-flex-"></a>Beregning av Fleksi-

Fordi arbeideren jobber i perioden Fleksi-, beregnes ikke Fleksi-. Fleksi- beregnes bare hvis arbeideren er fraværende under perioden Fleksi-. Hvis arbeideren jobber i perioden Fleksi-, får hun lønnssatsen som er definert for standardtid. Hvis arbeideren er fraværende i løpet av perioden Fleksi-, trekkes de 45 minuttene fra fleksikontoen hennes.

#### <a name="calculation-of-time"></a>Beregning av tid

Tiden blir beregnet som tiden mellom innstempling og utstempling, det vil si 06:30 AM til 05:00 PM, tilsvarende 10,50 timer.

#### <a name="calculation-of-pay-time"></a>Beregning av lønnstid

I dette scenarioet er arbeideren på jobb i 10,50 timer (**Tid**). **Lønnstid** beregnes imidlertid som 10,00 timer, fordi arbeideren ikke har lønn i perioden Fleksi +.

#### <a name="calculation-of-pay-overtime"></a>Beregning av lønn overtid

| Tidspunkt               | Registreringstype | Lønnstid (timer) |
|--------------------|-------------------|------------------|
| 6:30 AM – 7:00 AM  | Fleksi+             | 0                |
| 7:00 AM – 2:30 PM  | Normaltid     | 7,50             |
| 2:30 PM – 3:30 PM  | Fleksi-             | 1,00             |
| 3:30 PM – 05:00 PM | Overtid          | 1.50             |
|                    | Sum             | 10,00            |

### <a name="generation-of-pay-items"></a>Generering av lønnsposter

Arbeiderregistreringer for dagen kan overføres fra **Godkjenn**-siden. Under overføringsprosessen genereres lønnsposter og overførte registreringer. Lønnsposter representerer en spesifikasjon av lønnstid til normaltid, overtid, betalt pausetid og så videre.

Hvis du vil åpne listen over lønnsposter, velger du **Timeregistrering** &gt; **Gjennomgå og godkjenn** &gt; **Godkjenn**. Velg deretter **Forespørsel** &gt; **Overførte registreringer**.

Lønnspostene danner grunnlaget for en arbeider lønn. Du kan generere en fil som inneholder informasjon fra lønnspostene, og overføre filen til et lønningssystem.

Som en del av overføringsprosessen, overføres tid og kostnad fra produksjon og prosjektaktiviteter til produksjon og prosjektjournaler for å ta hensyn til tids- og kostnadsforbruk. De overførte registreringene er grunnlaget for tids- og kostpris per time for produksjonsordrer og prosjekter. Du kan åpne de overførte registreringene fra **Forespørsel**-menyen på **Godkjenn**-siden.

For scenario 2 genereres for eksempel følgende lønnsposter.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats  | Total kostnad |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1 201     | 10,0      | 10    | 100        |
| Overtid      | 1301     | 1.50      | 5     | 7,50       |
|               |          |           | Sum | 107,50     |

Lønnsposten for standardtid har en lønnsenhet på 10 timer som dekker normaltid, fleksitid og overtid. Normaltid, fleksitid og overtid konsolideres til én lønnspost fordi alle typene beregnes som normaltid, basert på standardinnstillingene for en parameter på siden **Beregningsparametere** (**Timeregistrering** &gt; **Oppsett** &gt; **Beregningsparametere**). Overtiden beregnes over standardtiden ved å bruke en ekstra sats på 5.

Hvis du ønsker å skille klart mellom normaltid og overtid, slik at lønnsenhetene for lønnstypene bare dekker det faktiske tidsforbruket på normaltid og overtid, må lønnsenhetene for normaltid beregnes som 8,50, og lønnsenhetene for overtid må beregnes som 1,50.

Hvis du vil konfigurere systemet slik at det klart skiller mellom normaltid og overtid, må du utelate overtid fra normaltiden. Du må også endre oppsettet for lønnstypen for overtid, slik at lønnssatsen for overtid dekker alle betalinger for timene som ble brukt på overtid.

### <a name="exclude-overtime-from-the-standard-time"></a>Utelate overtid fra normaltiden

På siden **Beregningsparametere** velger du **Overtid** som profilspesifikasjonstypen, og setter alternativet **Lønnstid** til **Ingen**, som vist her.

| Reg. spesifikasjon | Type profilspesifikasjon | Beregning   |     | Betalt         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Driftstid       | Overtid                   | Normaltid | Ja | Lønnstid     | Antall  |
|                    |                            | Lønnstid      | Ja | Lønn overtid | Ja |

Når du har justert beregningsparameterne, genereres følgende lønnsposter.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats  | Total kostnad |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1 201     | 8,50      | 10    | 85,0       |
| Overtid      | 1301     | 1.50      | sept.    | 22,50      |
|               |          |           | Sum | 107,50     |

> [!NOTE]
> Beregningsparametere har en anbefalt standardinnstilling. Du bør vanligvis være forsiktig når du endrer disse parameterne. For å gjenopprette de anbefalte standardinnstillingene velger du **Gjenopprett verdier** på siden **Beregningsparametere**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Tillat et avvik fra profilene for standardlønn

På **Profiler**-siden (**Timeregistrering** &gt; **Oppsett** &gt; **Tidsprofiler** &gt; **Profiler**) kan du definere profiltyper som inneholder vekslekoder og pauser.

### <a name="switch-codes"></a>Vekslekoder

Du kan bruke vekslekoder for å tillate at arbeidere kan avvike fra profiltypen ved å endre en annen profiltype. Du kan for eksempel tillate en arbeider å endre fra Fleksi+ tid til overtid. En arbeider kan legge til en vekslekode under registreringen, eller du kan tilordne oppgaven å legge til en vekslekode til personen som godkjenner registreringene.

Før du kan bruke en vekslekode, må du definere den som en type indirekte aktivitet. Deretter må du legge vekslekoden i tidsprofilen for perioden der du vil tillate en endring av profiltypen. Du kan for eksempel følge disse trinnene for å opprette en vekslekode som gjør det mulig å endre perioden Fleksi+ fra 06:00 AM til 07:00 AM til overtid.

1. Opprett en vekslekode som heter **OTBCI (Konverter Fleksi til overtid før innstempling)**. Velg **Timeregistrering** &gt; **Administrer indirekte aktiviteter** &gt; **Indirekte aktiviteter**.
2. I **Vekslekode**-kolonnen legger du til OTBCI i Fleksi+ linjen i tidsprofilen.
3. I **Sekundær**-kolonnen legger du til **Overtid**-profiltypen.

Vurder følgende fleksiprofil som representerer en arbeidsdag.

| Profiltype  | Start    | Slutt      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 AM | 06:00 AM | Mandag  |
| Fleksi+         | 06:00 AM | 07:00 AM | Mandag  |
| Stemple inn      | 07:00 AM | 07:00 AM | Mandag  |
| Normaltid | 07:00 AM | 02:30 PM | Mandag  |
| Fleksi-         | 02:30 PM | 03:30 PM | Mandag  |
| Utstempling     | 03:30 PM | 03:30 PM | Mandag  |
| Overtid     | 03:30 PM | 06:00 AM | Tirsdag |

Arbeiderens registreringer for dagen ser slik ut.

| Journalregistreringstype | Start    | Slutt      |
|---------------------------|----------|----------|
| Stemple inn                  | 06:30 AM | 06:30 AM |
| Produksjonsjobb            | 06:30 AM | 02:45 PM |
| Utstempling                 | 05:00 PM | 05:00 PM |

Følgende lønnsposter genereres etter overføringen.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats  | Total kostnad |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1 201     | 8,50      | 10    | 85,0       |
| Overtid      | 1305     | 1.50      | sept.    | 22,50      |
|               |          |           | Sum | 107,50     |

På **Godkjenn**-siden angrer du overføringen, og deretter bruker du **Vekslekode**-menyen for å bruke **OTBCI**-vekslekoden. Når du har overført registreringene én gang til, genereres følgende lønnsposter.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats  | Total kostnad |
|---------------|----------|-----------|-------|------------|
| Normaltid | 1 201     | 8,50      | 10    | 80,0       |
| Overtid      | 1305     | 2.00      | sept.    | 30,0       |
|               |          |           | Sum | 107,50     |

> [!NOTE]
> Når du bruker vekslekoden, økes overtid med 0,5 time, fra 1,50 til 2,00. 0,5 time er konverteringen av Fleksi+ tidspunktet som er registrert, fra 06:30 AM til 07:00 til overtid.

### <a name="breaks"></a>Pauser

Pause fra arbeidet påvirker beregningen av arbeideres lønn. Pauser er definert som en type indirekte aktivitet. De kan defineres som **Betalt**, slik at pausen legges til arbeiderens lønn, eller **Ubetalt**, for å forhindre at pausen legges til arbeiderens lønn. Pauser kan også defineres som **Planlagt** eller **Registrert**.

#### <a name="planned-breaks"></a>Planlagte pauser

Hvis et firma har en fast pausetid, for eksempel en fast lunsjpause, kan pausen forhåndsdefineres i tidsprofilen. I så fall trenger ikke arbeideren registrere pausen på jobbkortsidene. I stedet gjøres pausen automatisk rede for når arbeiderens registreringer beregnes på  **Godkjenn**-siden.

#### <a name="registered-breaks"></a>Registrerte pauser

Hvis et selskap ikke bruker planlagte pauser, kan ansatte registrere pauser i løpet av arbeidsdagen. Registrerte pauser kan for eksempel brukes hvis en arbeider jobber mot en fleksitidsprofil som ikke har definert innstempling og utstempling. Registrerte pauser er en type indirekte aktivitet. Arbeideren registrerer pausen på **Jobbkort**-terminalsiden eller på **Jobbkort**-enhetssiden. På begge disse sidene kan brukeren velge typen pause i en liste over forhåndsdefinerte pauseaktiviteter.

#### <a name="paid-and-unpaid-breaks"></a>Betalte og ubetalte pauser

Pauseaktiviteter kan defineres som **Betalt** eller **Ubetalt**. En betalt pause er inkludert i beregningen av lønnstid, og systemet bruker lønnstypen som er definert i lønnsavtalen for **Pause**-registreringstypen.

### <a name="example-of-a-planned-break"></a>Eksempel på en planlagt pause

Vurder den følgende tidsprofilen som inneholder en ubetalt lunsjpause.

| Profiltype  | Start    | Slutt      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 AM | 06:00 AM | Mandag  |
| Fleksi+         | 06:00 AM | 07:00 AM | Mandag  |
| Stemple inn      | 07:00 AM | 07:00 AM | Mandag  |
| Normaltid | 07:00 AM | 12:00 PM | Mandag  |
| Bryt         | 12:00 PM | 12:30 PM | Mandag  |
| Normaltid | 12:30 PM | 02:30 PM | Mandag  |
| Fleksi-         | 02:30 PM | 03:30 PM | Mandag  |
| Utstempling     | 03:30 PM | 03:30 PM | Mandag  |
| Overtid     | 03:30 PM | 06:00 AM | Tirsdag |

Arbeiderens registreringer for dagen ser slik ut.

| Journalregistreringstype | Start    | Slutt      |
|---------------------------|----------|----------|
| Stemple inn                  | 06:30 AM | 06:30 AM |
| Produksjonsjobb            | 06:30 AM | 02:45 PM |
| Utstempling                 | 05:00 PM | 05:00 PM |

Når du har beregnet journalregistreringene på **Godkjenn** -siden, kan du vise resultatet av beregningen i kategorien **Timer**. For å forstå dette scenariet kan du se følgende felt.

| Fleksi + | Fleksi - | Tidspunkt  | Lønnstid | Ubetalt pausetid | Lønn overtid |
|--------|--------|-------|----------|---------------------|--------------|
| 0.50   | 0.00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Systemet beregnet ubetalt pausetid på 0,5 timer, og denne tiden er ikke en del av lønnstiden.

### <a name="example-of-a-registered-break"></a>Eksempel på en registrert pause

Vurder den følgende tidsprofilen som ikke inneholder planlagte pauser.

| Profiltype  | Start    | Slutt      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 AM | 06:00 AM | Mandag  |
| Fleksi+         | 06:00 AM | 07:00 AM | Mandag  |
| Stemple inn      | 07:00 AM | 07:00 AM | Mandag  |
| Normaltid | 07:00 AM | 02:30 PM | Mandag  |
| Fleksi-         | 02:30 PM | 03:30 PM | Mandag  |
| Utstempling     | 03:30 PM | 03:30 PM | Mandag  |
| Overtid     | 03:30 PM | 06:00 AM | Tirsdag |

Arbeiderens registreringer for dagen ser slik ut.

| Journalregistreringstype | Start    | Slutt      |
|---------------------------|----------|----------|
| Stemple inn                  | 06:30 AM | 06:30 AM |
| Produksjonsjobb            | 06:30 AM | 05:00 PM |
| Bryt                     | 12:03 PM | 12:32 PM |
| Utstempling                 | 05:00 PM | 05:00 PM |

Når registreringene beregnes, beregnes tiden for aktivitetene.

| Journalregistreringstype | Start    | Slutt      | Tidspunkt  |
|---------------------------|----------|----------|-------|
| Stemple inn                  | 06:30 AM | 06:30 AM |       |
| Produksjonsjobb            | 06:30 AM | 05:00 PM | 10,00 |
| Bryt                     | 12:03 PM | 12:32 PM | 0.50  |
| Utstempling                 | 05:00 PM | 05:00 PM |       |

> [!NOTE]
> Tiden for pausen kjører parallelt med tidspunktet for aktiviteten (en produksjonsjobb i dette eksemplet). Dette brukes alltid for pauseaktiviteter. Når registreringene beregnes, trekkes pausetiden fra aktivitetstiden. I dette tilfellet har produksjonsjobben en varighet på 10,50 timer, men tiden blir beregnet som 10 fordi 0,5 timer pausetid er trukket fra aktivitetstiden.

Når du har beregnet journalregistreringene på **Godkjenn** -siden, kan du vise resultatet av beregningen i kategorien **Timer**. For å forstå dette scenariet kan du se følgende felt.

| Fleksi + | Fleksi - | Tidspunkt  | Lønnstid | Ubetalt pausetid | Lønn overtid |
|--------|--------|-------|----------|---------------------|--------------|
| 0.50   | 0.00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Hvis den planlagte pausen hadde vært betalt i stedet for ubetalt, ville resultatet av beregningen sett slik ut.

| Fleksi + | Fleksi - | Tidspunkt  | Lønnstid | Betalt pausetid | Lønn overtid |
|--------|--------|-------|----------|-----------------|--------------|
| 0.50   | 0.00   | 10,50 | 10,00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Lønnsposter og betalte pauser

Når du overfører registreringer på **Godkjenn**-siden, genereres lønnsposter. En egen lønnspost genereres for betalte pauser.

Lønnssatsen for en betalt pause bestemmes av lønnstypen som er definert i lønnsavtalene for pausen. I stedet for å bruke en lønnstype, kan du definere kostprisen per time for pausen for et definert datointervall.

Tenk deg følgende tidsprofil.

| Profiltype  | Start    | Slutt      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 AM | 06:00 AM | Mandag  |
| Fleksi+         | 06:00 AM | 07:00 AM | Mandag  |
| Stemple inn      | 07:00 AM | 07:00 AM | Mandag  |
| Normaltid | 07:00 AM | 02:30 PM | Mandag  |
| Fleksi-         | 02:30 PM | 03:30 PM | Mandag  |
| Utstempling     | 03:30 PM | 03:30 PM | Mandag  |
| Overtid     | 03:30 PM | 06:00 AM | Tirsdag |

Arbeiderens registreringer for dagen ser slik ut.

| Journalregistreringstype | Start    | Slutt      | Tidspunkt |
|---------------------------|----------|----------|------|
| Stemple inn                  | 07:00 AM | 07:00 AM |      |
| Produksjonsjobb            | 07:00 AM | 03:00 PM | 7,5  |
| Pause (betalt)              | 12:00 PM | 12:30 PM | 0,5  |
| Utstempling                 | 03:00 PM | 03:00 PM |      |

I dette eksemplet er lønnstypen for standardtid satt til **1201**, og en lønnssats på **10** er definert i lønnsavtalen. Den betalte pausen har lønnstypen **1301** og en lønnssats på **8**. Når registreringene er overført, genereres følgende lønnsposter.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 7,50      | 10   |
| Fleksi-         | 1 201     | 0.50      | 10   |
| Pause (betalt)  | 1301     | 0.50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Hvordan kostnaden av betalte pauser er tildelt til prosjekter og produksjonsordrer

Timekostnaden for prosjektaktiviteter og produksjonsjobber kan settes opp slik at den blir fastslått enten ved lønnssatser som beregnes i Timeregistrering, eller kostnadskategoriene som er definert for aktivitetene.

Når du skal definere kostnadskategorien, velger du **Produksjonskontroll** &gt; **Oppsett** &gt; **Produksjonsutførelse** &gt; **Standarder for produksjonsordre**, og angir **Kostnadskategori**-feltet til **Ja** eller **Nei**.

- **Nei** – kostnaden beregnes basert på lønnssatser som er definert for registreringstypen Timeregistrering.
- **Ja** – kostnaden beregnes basert på kostnadskategorier for produksjons- og prosjektaktiviteter.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Kostnadsberegning basert på lønnssatser som beregnes i Timeregistrering

Følgende eksempel viser hvordan timeprisen beregnes når kostnaden er definert slik at den er beregnet basert på lønnssatser.

Timeprisen som brukes for produksjonsordrer og prosjekter, blir beregnet under overføringsprosessen. Hvis du vil vise timeprisen per aktivitet, kan du åpne **Godkjenn**-siden i Timeregistrering, og deretter velge **Forespørsel** &gt; **Overførte registreringer**. Du kan finne timeprisen per registrering i **Kostpriser**-kategorien.

Vurder følgende registreringer som bruker den samme tidsprofilen som det forrige eksemplet.

| Journalregistreringstype | Start    | Slutt      | Tidspunkt |
|---------------------------|----------|----------|------|
| Stemple inn                  | 07:00 AM | 07:00 AM |      |
| Behandle (ordre: 4711)     | 07:00 AM | 11:00 AM | 4    |
| Behandle (ordre: 4712)     | 11:00 AM | 03:00 PM | 3,50 |
| Pause (betalt)              | 12:00 PM | 12:30 PM | 0.50 |
| Utstempling                 | 03:00 PM | 03:00 PM |      |

Når registreringene er overført, genereres følgende overførte registreringer.

| Registreringstype     | Tidspunkt | Kostpris per time |
|-----------------------|------|---------------------|
| Innstempling              | 0.00 | 0.00                |
| Behandle (ordre: 4711) | 4,00 | 10,00               |
| Behandle (ordre: 4712) | 3,50 | 11,14               |
| Pause (betalt)          | 0.50 | 0.00                |
| Utstempling             | 0.00 | 0.00                |

Beregning av kostpris per time for den betalt pausen avhenger av en innstilling for direkte lønnskostnader. Velg **Timeregistrering** &gt; **Oppsett** &gt; **Parametere for timeregistrering**. I kategorien **Kostpris**, under **Direkte lønnskostnader** i **Normaltid**-feltet, kan du velge **Ja**, **Nei** eller **Tildeling**.

- **Ja** – denne verdien brukes for det forrige eksemplet. Kostnaden fordeles på produksjons- eller prosjektaktiviteten som kjøres parallelt med aktiviteten betalt pause. I eksemplet er denne aktiviteten produksjonsjobben for ordre 4712. Som du ser, er kostprisen per time for den betalt pausen 0 (null), og den tildeles til jobben som kjøres parallelt med pausen.

    Den betalte pausen har en varighet på 0,5 time, og lønnssatsen er 8. Den totale kostnaden for den betalte pausen er derfor 4. Den totale kostnaden fordeles deretter på prosessjobben på 3,5 timer. Derfor bidrar den betalt pausen 1,14 per time til kostnaden (4 ÷ 3,5 = 1,14).

- **Tildeling** – den betalte pausen fordeles likt til jobbene som er registrert for dagen. Hvis denne verdien brukes for det forrige eksemplet, genereres følgende overførte registreringer.

    | Registreringstype     | Tidspunkt | Kostpris per time |
    |-----------------------|------|---------------------|
    | Innstempling              | 0.00 | 0.00                |
    | Behandle (ordre: 4711) | 4,00 | 10,53               |
    | Behandle (ordre: 4712) | 3,50 | 10,53               |
    | Pause (betalt)          | 0.50 | 0.00                |
    | Utstempling             | 0.00 | 0.00                |

    Den totale behandlingstiden for to produksjonsjobbet er 7,5 timer, og den totale kostnaden for den betaltr pausen er 4. Derfor beregnes kostnaden for pausen som 0,53 (= 4 ÷ 7,5).

- **Nei** – kostnaden for den betalte pausen øker ikke timekostnaden for prosessaktiviteter.

    | Registreringstype     | Tidspunkt | Kostpris per time |
    |-----------------------|------|---------------------|
    | Innstempling              | 0.00 | 0.00                |
    | Behandle (ordre: 4711) | 4,00 | 10,00               |
    | Behandle (ordre: 4712) | 3,50 | 10,00               |
    | Pause (betalt)          | 0.50 | 0.00                |
    | Utstempling             | 0.00 | 0.00                |

## <a name="absence"></a>Fravær

Fraværskoder brukes til å registrere fraværsperioden for en arbeider. I likhet med pauser og vekslekoder er en fraværskode en type indirekte aktivitet. Fraværstid kan være planlagt eller registrert, og fravær kan være lovlig eller ulovlig. Legeavtale, seminar eller jurytjeneste er eksempler på gyldig fravær. Ugyldig fravær er fravær uten god grunn, for eksempel når en arbeider kommer for sent. Gyldig fravær fører normalt ikke til trekk i lønn for en arbeider, mens ugyldig fravær fører til fratrekk.

### <a name="planned-absence"></a>Planlagt fravær

Du kan opprette planlagt fravær for arbeidere på siden **Opprett planlagt fravær** (**Timeregistrering** &gt; **Opprett planlagt fravær**). Der registreres det planlagte fraværet som en fraværsjobb for en angitt dato og et tidsintervall.

Jobben er basert på en spørring. Du kan derfor opprette planlagt fravær for flere arbeidere, for eksempel arbeidere som tilhører den samme beregningsgruppen. Hvis det er planlagt fravær for en enkelt arbeider, kan registreringen angis enten fra **Fremmøte**-siden eller siden **Tidsregistreringsarbeidere**.

- Du kan angi en fraværsregistrering fra **Fremmøte**-siden ved å velge **Timeregistrering** &gt; **Forespørsler og rapporter** &gt; **Fremmøte** &gt; **Fremmøte**, og deretter velge **Fraværsregistrering**.
- For å angi en fraværsregistrering fra siden *<strong><em>Tidsregistreringsarbeidere</em></strong>* velger du <strong>Timeregistrering</strong> &gt; <strong>Oppsett</strong> &gt; <strong>Tidsregistreringsarbeidere</strong>, og deretter, i <strong>Tid</strong>-kategorien under <strong>Tidstilordning</strong>, velger du <strong>Fraværsregistreringer</strong>.

Du kan bruke rapporten **Planlagt fravær** til å se en oversikt over planlagt fravær for ansatte. Du åpner denne rapporten ved å velge **Timeregistrering** &gt; **Forespørsler og rapporter** &gt; **Fraværsrapporter** &gt; **Planlagt fravær**.

### <a name="registered-absence"></a>Registrert fravær

Vanligvis anses arbeidere fraværende hvis de ikke er på arbeid i en angitt periode mellom planlagt innstemplingstidspunkt og planlagt utstemplingstidspunkt. Hvis arbeidere stempler inn senere enn planlagt, eller hvis de stempler ut tidligere enn planlagt, blir de bedt om å velge en fraværskode for å angi årsaken til fraværet. En fraværskode kan settes opp slik at den er tilgjengelig for registrering. Bare gjeldende koder vil være tilgjengelige i listen.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Scenarier som er basert på ulike kombinasjoner av arbeidstimeregistreringer

Eksemplene nedenfor viser lønnsposter og oppføringer for godkjenning som er generert for arbeidere basert på deres registreringer. Alle disse scenariene er basert på følgende tidsprofil:

| Profiltype  | Start    | Slutt      | Dag     |
|---------------|----------|----------|---------|
| Overtid     | 00:00 AM | 06:00 AM | Mandag  |
| Fleksi+         | 06:00 AM | 07:00 AM | Mandag  |
| Stemple inn      | 07:00 AM | 07:00 AM | Mandag  |
| Normaltid | 07:00 AM | 02:30 PM | Mandag  |
| Fleksi-         | 02:30 PM | 03:30 PM | Mandag  |
| Utstempling     | 03:30 PM | 03:30 PM | Mandag  |
| Overtid     | 03:30 PM | 06:00 AM | Tirsdag |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Scenario 1: Arbeideren stempler inn senere enn planlagt

Arbeideren stempler inn klokken 08:30 AM. Fordi det planlagte innstemplingstidspunktet er 07:00 AM, er han 1,50 time for sent til arbeidet. Fordi 1,50 time regnes som fraværstid, blir arbeideren bedt om å velge en fraværskode. Arbeideren forlater arbeidet kl. 03:30 PM, som er planlagt utstemplingstidspunkt. Når arbeiderens registreringer er beregnet og godkjent, vises fraværsregistreringen, sammen med fraværskoden som arbeideren valgte ved innstempling, for tiden mellom 07:00 AM og 08:30 AM.

I tidsprofilen kan du konfigurere registreringstypen **Innstempling** slik at det er en toleranse når arbeidere er for sent på jobb. Hvis du for eksempel setter inn en toleranse på 5, blir arbeideren bare bedt om å angi en fraværskode hvis han stempler inn etter 07:05 AM.

Fordi arbeideren ikke har en god grunn til å komme for sent, velger han i dette tilfellet en fraværskode som er definert for ugyldig fravær. En fraværskode vurderes som gjeldende for ugyldig fravær hvis innstillingen for fratrekk i overtid er aktivert for fraværsgruppen som fraværskoden er knyttet til. Hvis du vil angi innstillingen, velger du **Timeregistrering** &gt; **Oppsett** &gt; **Grupper** &gt; **Fraværsgrupper**, og merker deretter av for **Trekk fra overtid**.

Slik vises arbeiderens registreringer for dagen på **Godkjenn**-siden etter beregning.

| Journalregistreringstype         | Start    | Slutt      | Tidspunkt |
|-----------------------------------|----------|----------|------|
| Fravær (ugyldig - sent til arbeid) | 07:00 AM | 08:30 AM | 1.5  |
| Stemple inn                          | 08:30 AM | 08:30 AM |      |
| Produksjonsjobb                    | 07:30 AM | 03:30 PM | 7.0  |
| Utstempling                         | 03:30 PM | 03:30 PM |      |

Her er den resulterende lønnsposten når registreringene er overført.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 7.00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Scenario 2: Arbeideren stempler ut før det planlagte utstemplingstidspunktet i en standard tidsperiode

Arbeideren stempler inn 07:00 AM og stempler ut tidlig kl. 01:00 PM. Ettersom 01:00 PM er før planlagt utstempling kl. 03:30 PM, og 01:00 AM er i en standard tidsperiode, blir arbeideren bedt om å velge en fraværskode. Arbeideren velger en fraværskode for en legetime, som er definert som gyldig fravær. Lønnssatsen for gyldig fravær er definert i lønnsavtalene for **Fravær**-registreringstypen (**Timeregistrering** &gt; **Oppsett** &gt; **Lønn** &gt; **Lønnsavtaler**).

Slik vises arbeiderens registreringer for dagen på **Godkjenn**-siden etter beregning.

| Journalregistreringstype              | Start    | Slutt      | Tidspunkt |
|----------------------------------------|----------|----------|------|
| Stemple inn                               | 07:00 AM | 07:00 AM |      |
| Produksjonsjobb                         | 07:00 AM | 01:00 PM | 4.0  |
| Utstempling                              | 01:00 PM | 01:00 PM |      |
| Fravær (gyldig – legetime) | 01:00 PM | 03:30 PM | 3.5  |

Her er den resulterende lønnsposten når registreringene er overført.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Scenario 3: Arbeideren stempler ut før det planlagte utstemplingstidspunktet i en Fleksi- tidsperiode

Arbeideren stempler inn klokken 07:00 AM og stempler klokken 02:15 PM, som er i den planlagte Fleksi- perioden. Tiden mellom det faktiske utstemplingtidspunktet og det planlagte utstemplingstidspunktet regnes ikke som fravær, og arbeideren blir ikke bedt om å velge en fraværskode. Beløpet trekkes fra arbeiderens fleksikonto, og arbeideren får lønn i løpet av den gjenværende delen av Fleksi- perioden, fra 02:15 til 03:30 PM.

Slik vises arbeiderens registreringer for dagen på **Godkjenn**-siden etter beregning.

| Journalregistreringstype | Start    | Slutt      | Tidspunkt |
|---------------------------|----------|----------|------|
| Stemple inn                  | 07:00 AM | 07:00 AM |      |
| Produksjonsjobb            | 07:00 AM | 02:15 PM | 7,25 |
| Utstempling                 | 02:15 PM | 02:15 PM |      |

Her er den resulterende lønnsposten når registreringene er overført.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Scenario 4: Arbeideren stempler inn sent og stemper ut etter før det planlagte utstemplingstidspunktet i en overtidsperiode

Arbeideren stempler inn sent klokken 09:30 AM, og deretter, for å kompensere for sent fremmøte, arbeider han overtid og stempler ut klokken 05:00 PM. Fordi arbeideren kom for sent og kompenserte ved å arbeide lenger, vil ikke firmaet gi arbeideren overtidsbetaling for timene han har arbeidet mellom den planlagte utstemplingen kl. 03:30 PM og den faktiske utstemplingen kl. 05:00 PM, selv om denne perioden er definert som overtid i tidsprofilen.

For å håndtere denne situasjonen kan du definere fraværskoden til å redusere overtidstimene med timer med ugyldig fravær som arbeideren har samme dag. Velg **Timeregistrering** &gt; **Oppsett** &gt; **Grupper** &gt; **Fraværsgrupper**, og merker deretter av for **Trekk fra overtid** for å trekke fra overtid fra timer med ugyldig fravær.

Slik vises arbeiderens registreringer for dagen på **Godkjenn**-siden etter beregning.

| Journalregistreringstype         | Start    | Slutt      | Tidspunkt |
|-----------------------------------|----------|----------|------|
| Fravær (ugyldig - sent til arbeid) | 07:00 AM | 09:30 AM | 1.5  |
| Stemple inn                          | 09:30 AM | 09:30 AM |      |
| Produksjonsjobb                    | 09:30 AM | 05:00 PM | 7,5  |
| Utstempling                         | 05:30 PM | 05:30 PM |      |

Hvis det er merket av for **Trekk fra overtid** for den valgte fraværskoden, trekkes overtidsbetalingen fra med timene arbeideren var borte ulovlig. I dette tilfellet genereres følgende lønnsposter når registreringene er overført.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 9.00      | 10   |
| Overtid      | 1301     | 0,5       | sept.   |

Her trekkes 1,5 timer med ugyldig fravær, fra 07:00 AM til 09:30 AM, fra 2 timer med overtid, fra 03:30 PM til 05:30 PM. Resultatet av registreringen er 1,5 timer normaltid og 0,5 timer overtid.

Derimot, hvis merket for **Trekk fra overtid** er fjernet for den valgte fraværskoden, gis overtidsbetalingen til arbeideren, selv om han kom for sent og hadde et ugyldig fravær. I dette tilfellet genereres følgende lønnsposter når registreringene er overført.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 7,50      | 10   |
| Overtid      | 1301     | 2,0       | sept.   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Scenario 5: Arbeideren stempler ut før det planlagte utstemplingstidspunktet, og kan konvertere fraværsperioden til en Fleksi- periode

Følgende eksempel viser hvordan en arbeiders fleksikonto kan reduseres ved å konverterte fraværsperioden til en Fleksi- periode.

Arbeideren stempler inn 07:00 AM og stempler ut 01:00 PM. Hun har inngått en avtale med sin overordnede om at hun kan gå hjem for helgen hvis hun trekker disse timene fra fleksikontoen. Når arbeideren stempler ut klokken 01:00 PM, blir hun bedt om å velge en fraværskode, fordi fraværsperioden for den gjenstående delen av arbeidsdagen som påvirkes, ikke er i en planlagt Fleksi- periode. For å konvertere den gjenstående delen av arbeidsdagen til en Fleksi- periode, kan arbeideren velge en fraværskode som er konfigurert til å redusere hennes fleksikonto.

Hvis du vil redusere saldoen for fleksible timer for arbeidere som registrerer fravær for en arbeidsdag, velger du **Timeregistrering** &gt; **Oppsett** &gt; **Grupper** &gt; **Fraværsgrupper**, og merker av for **Reduser fleksi**.

Slik vises arbeiderens registreringer for dagen på **Godkjenn**-siden før beregning.

| Journalregistreringstype | Start    | Slutt      | Tidspunkt |
|---------------------------|----------|----------|------|
| Stemple inn                  | 07:00 AM | 07:00 AM |      |
| Produksjonsjobb            | 07:00 AM | 01:00 PM | 6,0  |
| Utstempling                 | 01:00 PM | 01:00 PM |      |

Hvis arbeideren velger en fraværskode for ugyldig fravær, ser den resulterende lønnsposten slik ut etter at registreringen er overført.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 6,00      | 10   |

Hvis arbeideren velger en fraværskode for gyldig fravær, og fraværskoden er konfigurert til å redusere hennes fleksikonto, ser de resulterende lønnspostene slik ut når registreringer overføres.

| Lønnstype     | Lønnstype | Lønnsenheter | Sats |
|---------------|----------|-----------|------|
| Normaltid | 1 201     | 8,50      | 10   |

I dette tilfellet reduseres arbeiderens fleksisaldo med antall timer mellom det faktiske utstemplingstidspunktet og det planlagte utstemplingstidspunktet (det vil si 2,5 timer fra 01:00 PM til 03:30 PM).

> [!NOTE]
> Vi anbefaler ikke at du merker av for både **Trekk fra fleksi** og **Trekk fra overtid** for en fraværskode, fordi dette oppsettet vil trekke fra de ugyldige timene fra arbeiderens overtidstimer og samtidig redusere arbeiderens fleksikonto.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Scenario 6: Det finnes ingen planlagt fravær for dagen, og ingen arbeiders fremmøte for dagen

Hvis arbeideren ikke kommer på jobb i en arbeidsdag, og det er ingen planlagt fravær for arbeideren denne dagen, brukes en standardkode for fravær for beregning av arbeiderens registreringer. Hvis du vil definere standard fraværskoder, velger du **Timeregistrering** &gt; **Parametere for timeregistrering**. Du kan deretter velge en fraværskode i følgende felt:

- Sett inn fleksitid automatisk
- Sett inn fravær automatisk

Når de daglige registreringene er beregnet for en arbeider som er aktivert for fleksible timer, brukes fraværskoden som er angitt i feltet **Sett inn fleksitid automatisk**, som en standard fraværskode. Hvis arbeideren ikke er aktivert for fleksible timer, brukes fraværskoden som er angitt i feltet **Sett inn fravær automatisk**. Hvis et firma har en kombinasjon av arbeidere som er aktivert for fleksible timer og arbeidere som ikke er aktivert for fleksible timer, må begge parametere defineres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]