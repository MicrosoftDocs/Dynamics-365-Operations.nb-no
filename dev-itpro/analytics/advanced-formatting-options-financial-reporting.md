---
title: Avanserte formateringsalternativer i finansrapportering
description: "Når du lager en rapport i finansrapportering, finnes det flere formateringsfunksjoner, inkludert filtre for dimensjoner, begrensninger for kolonner og rapporteringsenheter, rader som ikke skal skrives ut, og IF/THEN/ELSE-setninger i beregninger."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 631fec1dc135565e6d38e7faf193a7a898b508cb
ms.lasthandoff: 03/29/2017


---

# <a name="advanced-formatting-options-in-financial-reporting"></a>Avanserte formateringsalternativer i finansrapportering

Når du lager en rapport i finansrapportering, finnes det flere formateringsfunksjoner, inkludert filtre for dimensjoner, begrensninger for kolonner og rapporteringsenheter, rader som ikke skal skrives ut, og IF/THEN/ELSE-setninger i beregninger. 

Tabellen nedenfor beskriver de avanserte formateringsfunksjonene som er tilgjengelige når du utformer rapporter.

| Funksjon                   | Beskrivelse                                                                                                                                                                                                                                                                                                                     |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensjonsfilter           | Hvis du vil ha tilgang til bestemte datasett, kan du bruke dimensjoner i raddefinisjonen og kolonnedefinisjonen. Mange rapporter bruker bare det naturlige segmentet i radformatet. Rader kan imidlertid endres slik at de inkluderer dimensjonsverdier. Dimensjonsfiltre i kolonnedefinisjonen brukes til å få tilgang til bestemte dimensjonsverdier. |
| Begrensning for rapporteringsenhet | Du kan konfigurere en rapportrad slik at den bare viser informasjon som er koblet til en bestemt rapporteringsenhet.                                                                                                                                                                                                                      |
| Rader som ikke skal skrives ut (NP)     | Rader som ikke skal skrives ut er nyttige i mange rapporter. Hvis flere beregninger er nødvendige for å få en verdi, kan disse beregningene skjules på den utskrevne rapporten. Rader som ikke skrives ut er også nyttig for feilsøking i forbindelse med rapportutforming og avansert celleplassering.                                                    |
| Kolonnebegrensning         | Kolonnebegrensningen i raddefinisjonen er nyttig for å skjule verdier som bare er relevant i noen rader i rapporten. Når prosentberegninger blir utført på en rad, vil kolonnebegrensningen hindre at totalkolonner eller andre kolonner skrives ut når disse tallene ikke gjelder.                              |
| Kolonneskift               | Du kan legge til kolonneskift i en raddefinisjon for å vise rapportinformasjon side ved side. Du kan legge til flere kolonneskift i én enkelt raddefinisjon, og kolonneoverskrifter gjentas øverst i hver kolonne etter kolonneskiftet. Merknader for en rapport vises mellom kolonneskiftene.                              |
| IF/THEN/ELSE-setning     | Du kan endre beregningene i en raddefinisjon eller en kolonnedefinisjon.                                                                                                                                                                                                                                                         |

## <a name="advanced-cell-placement"></a>Avansert celleplassering
Avansert celleplassering, eller *fremtvinging*, omfatter plassering av bestemte verdier i bestemte celler. Fremtvinging brukes for eksempel ofte til å flytte den riktige saldoen i et kontantstrømutdrag. Du kan bruke fremtvinging til følgende formål:

-   Flytte verdier fra Microsoft Excel til bestemte celler.
-   Hardkode bestemte verdier i en rapport.
-   Endre fortegn ved å kopiere en verdi fra en tidligere celle og multipliseres med verdien -1.

**Obs!**  I mange tilfeller må du konfigurere rapportdefinisjonen slik at kolonneberegninger utføres før radberegninger. Følg fremgangsmåten nedenfor for å fullføre denne konfigurasjonen.

1.  Åpne rapportdefinisjonen i Rapportutforming.
2.  I kategorien **Innstillinger**, under **Beregningsprioritet**, velger du **Utfør kolonneberegning først og deretter rad**.

## <a name="designing-the-report"></a>Utforme rapporten
Når du utformer en rapport, bør du opprette alle detaljradene først for å sikre at verdiene hentes inn som forventet. Legg deretter til **NP**-formatoverstyringer (ikke skriv ut) for å skjule detaljene som inneholder de endelige verdiene. **Viktig!**  Når du bruker **CAL**-formatkoden i raddefinisjonen, kan du ikke drille ned i transaksjonsdetaljen. For å tvinge, formler som bruker følgende format: &lt;målkolonnen&gt;=&lt;kommer kolonnen&gt;. &lt;rad koden&gt; skille noen flere plasseringer for en rad med et komma og et mellomrom. Her er et eksempel: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Eksempler på avanserte formateringsalternativer
Eksemplene nedenfor viser hvordan du formaterer raddefinisjonen og kolonnedefinisjonen for å fremtvinge en grunnleggende kontantstrømrapport (eksempel 1) og en statistisk rapport (eksempel 2).

### <a name="example-1-basic-forcing"></a>Eksempel 1: Grunnleggende fremtvinging

Tabellen nedenfor viser et eksempel på en raddefinisjon som bruker grunnleggende fremtvinging.

| Radkode | Beskrivelse                      | Formatkode | Relaterte formler/rader/enheter | Formatoverstyring | Normal saldo | Utskriftskontroll | Kolonnebegrensning | Radmodifikator               | Kobling til finansdimensjoner |
|----------|----------------------------------|-------------|-----------------------------|-----------------|----------------|---------------|--------------------|----------------------------|------------------------------|
| 1000      | Kontanter i begynnelsen av perioden (NP) |             |                             |                 |                |               |                    | Konto modifikator = \[/BB\] | + Segment2 = \[1100\]         |
| 130      | Kontanter i begynnelsen av perioden      | CAL         | C=C.100,F=D.100             |                 |                |               |                    |                            |                              |
| 160      |                                  |             |                             |                 |                |               |                    |                            |                              |
| 190      |                                  |             |                             |                 |                |               |                    |                            |                              |

Tabellen nedenfor viser et eksempel på en kolonnedefinisjon som bruker grunnleggende fremtvinging i raden.

|                              | A   | B    | K        | D      | E      | F    |
|------------------------------|-----|------|----------|--------|--------|------|
| Overskrift 1                     |     |      |          |        |        |      |
| Overskrift 2                     | A   | B    | K        | D      | E      | F    |
| Overskrift 3                     |     |      |          |        |        |      |
| Kolonnetype                  | ROW | DESC | FD       | FD     | FD     | CALC |
| Registerkode/attributtkategori |     |      | FAKTISK   | FAKTISK | FAKTISK |      |
| Regnskapsår                  |     |      | BASE     | BASE   | BASE   |      |
| Periode                       |     |      | BASE     | BASE   | BASE   |      |
| Perioder som er dekket              |     |      | PERIODIC | YTD/BB | YTD    |      |
| Formel                      |     |      |          |        |        | E-D  |
| Kolonnebredde                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Eksempel 2: Statistiske rapporter

Tabellen nedenfor viser et eksempel på en raddefinisjon som bruker fremtvinging for en statistisk rapport.

| Radkode | Beskrivelse               | Formatkode | Relaterte formler/rader/enheter     | Formatoverstyring      | Normal saldo | Utskriftskontroll | Kolonnebegrensning | Radmodifikator | Kobling til finansdimensjoner               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|---------------|--------------------|--------------|--------------------------------------------|
| 50       | Statistisk informasjon   | REM         |                                 |                      |                |               |                    |              |                                            |
| 1000      | Antall ansatte – USA            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 115      | Antall ansatte – internasjonalt | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 130      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 190      | Salg i USA                  |             |                                 |                      | K              |               |                    |              | + Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Internasjonale salg       |             |                                 |                      | K              |               |                    |              | + Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 280      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 310      | Salg i USA                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |               |                    |              |                                            |
| 340      | Internasjonale salg       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |               |                    |              |                                            |

Tabellen nedenfor viser et eksempel på en kolonnedefinisjon som bruker fremtvinging for en statistisk rapport.

|                              | A   | B    | K      | D            | E     | F            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Overskrift 1                     | A   | B    | K      | D            | E     | F            |
| Overskrift 2                     | -   | -    | År til dato    | Årlig salg | Stab | $ per person |
| Overskrift 3                     |     |      |        |              |       |              |
| Kolonnetype                  | ROW | DESC | FD     | CALC         | CALC  | CALC         |
| Registerkode/attributtkategori |     |      | FAKTISK |              |       |              |
| Regnskapsår                  |     |      | BASE   |              |       |              |
| Periode                       |     |      | BASE   |              |       |              |
| Perioder som er dekket              |     |      | YTD    |              |       |              |
| Formel                      |     |      |        |              |       | E-D          |
| Kolonnebredde                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Begrense en rad til en bestemt rapporteringsenhet
Når en rapportrad er begrenset til en bestemt rapporteringsenhet, viser denne raden de koblede dataene bare for den navngitte rapporteringsenheten og ignorerer dataene for andre rapporteringsenheter i rapporteringstreet. Du kan for eksempel opprette en rad som inneholder detaljer for de totale driftsutgiftene for en bestemt avdeling. Rapporten kan inneholde dupliserte data hvis rapporten inneholder både et rapporteringstre og en raddefinisjon som inneholder mer enn bare den naturlige kontoen. Du har for eksempel et rapporteringstre som viser de seks avdelingene i organisasjonen, og du har også en raddefinisjon som viser en bestemt kombinasjon av en konto og en avdeling i raden. Når du genererer rapporten, vil den bestemte kombinasjonen av en konto og en avdeling skrives ut på alle nivåer av rapporteringstreet, selv om denne avdelingen kanskje ikke samsvare med hva som er i treet. Denne virkemåten oppstår fordi raden overstyrer det som vanligvis filtreres ut av rapportdefinisjonen. Én metode for å unngå duplisering av data er å begrense en rad til en bestemt rapporteringsenhet. **Obs!**  Hvis en rad inneholder dimensjoner og du begrenser denne raden til en underordnet rapporteringsenhet, inkluderes raden for den underordnede enheten og dens overordnede enheter, men det oppstår ingen duplisering.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Begrense en rad til en rapporteringsenhet

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter velger du raddefinisjonen som skal endres.
2.  Dobbeltklikk den aktuelle **Relaterte formler/rader/enheter**-cellen.
3.  I dialogboksen **Valg av rapporteringsenhet**, i **Rapporteringstre**-feltet , velger du treet som er tilordnet i rapportdefinisjonen.
4.  Velg en rapporteringsenhet, og klikk deretter **OK**. Begrensningen vises i cellen i raddefinisjonen.
5.  Dobbeltklikk cellen i kolonnen **Kobling til finansdimensjoner** i den begrensede raden, og skriver deretter inn en kobling til systemet for økonomiske data.

## <a name="selecting-print-control-in-a-row-definition"></a>Velge utskriftkontroll i en raddefinisjon
Du kan angi kontrollkoder for utskrift for hver kolonne ved hjelp av **Utskriftskontroll**-cellen.

### <a name="add-print-control-codes-to-a-report-row"></a>Legge til kontrollkoder for utskrift i en rapportrad

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  Dobbeltklikk cellen **Utskriftskontroll**.
3.  I dialogboksen **Utskriftkontroll** velger du en kontrollkode for utskrift eller trykker og holder CTRL--tasten for å velge flere koder. Du kan også skrive inn kontrollkoder for utskrift direkte i **Utskriftskontroll**-cellen. Bruk komma for å atskill flere kontrollkoder for utskrift.
4.  Velg alternativer for betinget utskrift.
5.  Klikk **OK**.

### <a name="regular-print-control-codes"></a>Vanlige kontrollkoder for utskrift

Tabellen nedenfor beskriver vanlige kontrollkoder for utskrift for en raddefinisjon.

| Kontrollkode for utskrift | Tolkning av kontrollkoden for utskrift         | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Rad som ikke skal skrives ut                                 | Hindre at beløpene i raden blir skrevet ut på rapporten, og utelater beløpene fra beregninger. Hvis du vil inkludere en kolonne som ikke skrives ut, i en beregning, kan du referere kolonnen direkte i beregningsformelen. Rad 240, som ikke skal skrives ut, er for eksempel er inkludert i følgende beregning: **230+240+250**. Rad 240, som ikke skal skrives ut, er imidlertid ikke inkludert i følgende beregning: **230:250**. |
| CS                 | Valutasymbol: Bruke valutaformat i denne raden | Inkluderer valutasymbolet i alle ikke-prosentbeløp. Prosentverdier får aldri et valutasymbol.                                                                                                                                                                                                                                                                                                |
| XD                 | Skjul rad i detaljert kontorapport            | Skjuler visning av kontoer i detaljerte konto- og transaksjonsrapporter. Denne utskriftskontrollen er nyttig når en rad inneholder flere kontoer som ikke vises i den detaljerte konto- eller transaksjonsrapporten.                                                                                                                                                           |
| X0                 | Skjuler rad hvis alle er nuller                        | Utelater en rad fra rapporten hvis alle celler i raden er tomme eller inneholde nuller. Denne utskriftskontrollen har bare betydning når alternativet for å skjule nullsaldo ikke er valgt i rapportdefinisjonen.                                                                                                                                                                                            |
| B0                 | Lar nullkolonner være tomme                         | Lar kolonner være tomme i en rad som inneholder nullbeløp.                                                                                                                                                                                                                                                                                                                                                      |
| XR                 | Skjul opprulling                                  | Skjuler en opprulling. Hvis rapporten bruker et rapporteringstre, rulles ikke beløpene i denne raden opp til etterfølgende overordnede noder.                                                                                                                                                                                                                                                                               |
| SR                 | Skjul avrunding                                | Hindrer at beløpene i denne raden avrundes.                                                                                                                                                                                                                                                                                                                                                          |
| XT                 | Skjuler rad i detaljert transaksjonsrapport        | Skjuler visning av transaksjoner i detaljert transaksjonsrapport. Denne utskriftskontrollen er nyttig når en rad inneholder flere kontoer som ikke vises i en detaljert transaksjonsrapport.                                                                                                                                                                                                             |

### <a name="conditional-print-control-codes"></a>Kontrollkoder for betinget utskrift

Tabellen nedenfor beskriver betingede kontrollkoder for utskrift for en raddefinisjon.

| Kontrollkode for utskrift | Beskrivelse                                  |
|--------------------|----------------------------------------------|
| (ingen)             | Nullstill utvalget for betinget utskrift.       |
| DR                 | Skriv ut bare debetsaldoer for denne raden.  |
| CR                 | Skriv ut bare kreditsaldoer for denne raden. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Cellen Kolonnebegrensning i en raddefinisjon
Cellen **Kolonnebegrensning** i en raddefinisjon har mange funksjoner. Avhengig av hvilken type rad, kan du bruke cellen **Kolonnebegrensning** for å angi én av følgende funksjoner:

-   Cellen kan begrense utskriften av radbeløp til en bestemt kolonne. Denne funksjonen er nyttig hvis du oppretter en tabellbalanse.
-   Cellen kan angi kolonnebeløpene som skal sorteres.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Bruke en beregningsformel i en raddefinisjon
Kan inneholde en formel for beregning i en raddefinisjon for **+**, **-**, **\***, og **/**operatorer, og også **IF/THEN/ELSE** setninger. I tillegg kan en beregning omfatte enkeltceller og absolutte beløp (faktiske tall som er inkludert i formelen). Formelen kan inneholde opptil 1 024 tegn. Beregningene kan ikke brukes på rader som inneholder celler av typen **Kobling til finansdimensjoner** (FD). Du kan imidlertid inkludere beregninger i påfølgende rader, skjule utskriften av disse radene og deretter summere beregningsradene.

### <a name="operators-in-a-calculation-formula"></a>Operatorer i en beregningsformel

En beregningsformel bruker mer komplekse operatorer enn en radtotalformel. Kan du imidlertid bruke den **\***og **/**operatorer sammen med andre operatorer til å multiplisere (\*) og del (/) beløp. Hvis du vil bruke et område eller en sum i en beregningsformel, må du bruke en krøllalfa (@) foran en radkode, med mindre du bruker en kolonne i raddefinisjonen. For å legge til beløpet i raden 100 beløpet i rad 330, kan du for eksempel bruke formelen raden totalt **100 + 330** eller formelen for beregning av **@100+@330**. **Obs!**  Du må du bruke en krøllalfa (@) foran hver radkode som du bruker i en beregningsformel. Hvis ikke, leses tallet som et absolutt beløp. Hvis du for eksempel formelen **@100+330** legger USD 330 til beløpet i rad 100. Når du refererer til en kolonne i en beregningsformel, er det ikke nødvendig å bruke en krøllalfa (@).

### <a name="create-a-calculation-formula"></a>Opprette en beregningsformel

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Dobbeltklikk **Formatkode**-cellen, og velg deretter **CAL**.
3.  I cellen **Relaterte formler/rader/enheter** skriver du inn beregningsformelen.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Eksempel på en beregningsformel for bestemte rader

I dette eksempelet formelen for beregning av **@100+@330** betyr at beløpet i 100-raden legges til beløpet i rad 330. Den totale formelen raden **340 + 370** legger til beløpet i raden 340 beløpet i rad 370. (Beløpet i rad 370 er beløpet fra beregningsformelen.)

| Radkode | Beskrivelse                 | Formatkode | Relaterte formler/rader/enheter | Utskriftskontroll | Radmodifikator | Kobling til finansdimensjoner |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Kontanter i begynnelsen av perioden |             |                            | NP            | BB           | + Konto =\[1100:1110\]       |
| 370      | Kontanter i begynnelsen av året   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Kontanter i begynnelsen av perioden | TOT         | 340+370                    |               |              |                              |

Når raden i en raddefinisjon, har formatkoden **CAL** og du angir en matematisk beregning i cellen **Relaterte formler/rader/enheter**, må du også angi bokstaven for den tilknyttede kolonnen og raden i rapporten. Angi for eksempel **A.120** for å representere kolonne A, rad 120. Du kan også bruke en krøllalfa (@) for å angi alle kolonner. Angi for eksempel **@120**til å representere alle kolonnene i raden 120. En matematisk beregning som ikke har en kolonnebokstav eller krøllalfa (@) antas for å være et reelt tall. **Merk:** Hvis du bruker en etikett rad kode refererer til en rad, må du bruke et punktum (.) som skilletegn mellom kolonnebokstav og etiketten (for eksempel **A.GROSS\_MARGIN/A.SALES**). Hvis du bruker en krøllalfa (@), kreves ikke et skilletegn (for eksempel **@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Eksempel på en beregningsformel for en bestemt rad

I dette eksemplet betyr formelen **E=C.340** at beregningen i cellen i kolonne C, rad 340, bare utføres på kolonne E. **Obs!**  Når du refererer til en kolonne i en beregningsformel, er det ikke nødvendig å bruke en krøllalfa (@).

| Radkode | Beskrivelse                 | Formatkode | Relaterte formler/rader/enheter | Utskriftskontroll | Radmodifikator | Kobling til finansdimensjoner |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Kontanter i begynnelsen av perioden |             |                            | NP            | BB           | + Konto =\[1100:1110\]       |
| 370      | Kontanter i begynnelsen av året   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Kontanter i begynnelsen av perioden | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Endre et tall i merkede kolonner

Når du endrer et tall eller en beregning i en bestemt rad i en kolonne, men ikke vil påvirke andre kolonner i rapporten, kan du angi **CAL** (beregning) i **Formatkode**-kolonnen i raddefinisjonen.

-   Hvis du vil utføre beregninger i alle rapportkolonner (**FD**), må du ikke angi en kolonnetildeling.
-   Hvis du vil begrense en formel til bestemte kolonner, angir du kolonnebokstaven, et likhetstegn (**=**), og deretter formelen.
-   Du kan angi flere kolonner. Når du bruker en krøllalfa (@) med en bestemt kolonneplassering, er krøllalfaen (@) knyttet til raden.
-   Du kan angi flere kolonneformler i én rad. Atskill formlene med komma.

### <a name="calculation-examples"></a>Beregningseksempler

| Beregning            | Handlingen som opprettes                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | For hver kolonne multipliseres verdien i rad 130 med 0,75. Resultatet settes deretter inn i gjeldende rad for hver kolonne. |
| B=@130\*.75            | Den samme beregningen utføres bare i kolonne B.                                                                      |
| A, B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE-setninger i en raddefinisjon

**IF/THEN/ELSE**-setninger kan legges til alle gyldige beregninger og brukes med **CAL**-formatet. Du angir **IF/THEN/ELSE**-beregningsformler i cellen i kolonnen **Relaterte formler/rader/enheter**. **IF/THEN/ELSE** beregning av formler som bruker følgende format: Hvis &lt;SANN/USANN-setningen&gt; DERETTER &lt;formelen&gt; ELSE &lt;formelen&gt; den **ELSE &lt;formelen&gt;** en del av setningen er valgfri.

#### <a name="if-statements"></a>IF-setninger

Setningen som etterfølger **IF**-setning kan være alle setninger som kan evalueres som sann eller usann. Setningen som etterfølger **IF**-setningen kan omfatte en enkel evaluering, eller den kan være en komplisert oppgave som kan inneholde flere uttrykk. Her er noen eksempler:

-   **Hvis A.200&gt;0** (enkel evalueringen)
-   **Hvis A.200&gt;0 og A.200&lt;10 000** (komplisert oppgave)
-   **Hvis A.200&gt;10000 eller ((A.340/B.1200)\*2 &lt;1200)** (komplekse-setning som inneholder flere uttrykk)

Begrepet **Perioder** i en **IF**-setning, representerer antall perioder for rapporten. Denne termen brukes vanligvis til å beregne et gjennomsnitt hittil i år. Hvis du for eksempel kjører en rapport for periode 7 hittil i år, betyr setningen **B.150/Perioder** at verdien i rad 150 i kolonne B, divideres med 7.

#### <a name="then-and-else-formulas"></a>THEN- og ELSE-formler

**THEN**- og **ELSE**-formler kan være alle gyldige beregninger, fra svært enkel verditilordninger til komplekse formler. Hvis du for eksempel setningen **hvis A.200&gt;0 og A=B.200** betyr "Hvis verdien i celle i kolonne A, rad 200 er mer enn 0 (null), plasserer verdien i cellen i kolonne B i rad 200 til celle i kolonne A i gjeldende rad." Den foregående **IF/THEN**-setning legger til en verdi i én kolonne i gjeldende rad. Du kan imidlertid også bruke en krøllalfa (@) i sann/usann-evalueringer eller formelen for å representere alle kolonner. Her er noen andre eksempler som er beskrevet i følgende deler:

-   **Hvis A.200 &gt;0 og B.200**: Hvis verdien i celle A.200 er positivt, legges verdien fra cellen B.200 i hver kolonne i gjeldende rad.
-   **Hvis A.200 &gt;DERETTER 0 @200**: Hvis verdien i celle A.200 er positivt, verdien fra hver kolonne i rad 200 plasseres i den tilsvarende kolonnen i gjeldende rad.
-   **Hvis @200&gt;DERETTER 0 @200**: Hvis verdien i raden 200 i gjeldende kolonne er positivt, verdien fra rad 200 plasseres i samme kolonne i gjeldende rad.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Begrense en beregning for en rapporteringsenhet i en raddefinisjon

Hvis du vil begrense en beregning til en enkelt rapportering enhet i et tre rapportering, slik at det endelige beløpet ikke er fremhevet til en overordnet enhet, kan du bruke den **@Unit**kode i den **relaterte formler/rader/enheter** celle i raddefinisjonen. Den **@Unit**koden som er oppført i kolonne B i rapportering treet, **navn på**. Når du bruker den **@Unit**koden, verdiene ikke er fremhevet, men beregningen blir evaluert på alle nivåer av rapportering treet. **Obs!**  Hvis du vil bruke denne funksjonen, må et rapporteringstre være tilknyttet raddefinisjonen. Beregningsraden kan referere til en beregningsrad eller en rad med økonomiske data. Beregningen registreres i cellen **Relaterte formler/rader/enheter** i raddefinisjonen og typebegrensningen for de økonomiske dataene. Beregningen må bruke en betinget beregning som starter med en **Hvis @Unit**konstruksjon. Her er et eksempel: Hvis @Unit(salg) DERETTER @100ELSE 0 denne beregningen inkluderer beløp fra rad 100 i hver kolonne i rapporten, men bare for salgsenheten. Hvis flere enheter har navnet SALG, vises beløpet i hver av disse enhetene. Rad 100 kan også være en rad med økonomiske data og kan defineres som en rad som ikke skal skrives ut. I slike tilfeller vil ikke beløpet vises i alle enheter i treet. Du kan også begrense beløpet til én enkelt kolonne i rapporten, for eksempel kolonne H, ved hjelp av en kolonnebegrensning for bare å skrive ut verdien i denne kolonnen i rapporten. Du kan inkludere **OR**-kombinasjoner i en **IF**-setning. Her er et eksempel: Hvis @Unit(salg) eller @Unit(SALESWEST), DERETTER 5 ELSE @100kan du angi en enhet i en beregningstype begrensning på én av følgende måter:

-   Angi et enhetsnavn for å inkludere enheter som samsvarer. For eksempel **Hvis @Unit(salg)** gjør at beregningen for en hvilken som helst enhet som heter salg, selv om det finnes flere enheter for salg i rapportering treet.
-   Angi navnet på firmaet og enhetsnavnet for å begrense beregningen til bestemte enheter i et bestemt firma. Angi for eksempel **Hvis @Unit(ACME: salg**) til å begrense beregningen til mva-enheter i selskapet ACME.
-   Angi den fullstendige hierarkikoden fra rapporteringstreet for å begrense beregningen til en bestemt enhet. Angi for eksempel **Hvis @Unit(sammendrag ^ ACME ^ VESTLANDET ^ salg)**. **Obs!**  Hvis du vil finne den fullstendige hierarkikoden, høyreklikker du i definisjonen for rapporteringstreet, og deretter velger du **Kopier ID for rapporteringsenhet (H-kode)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Begrense en beregning til en rapporteringsenhet

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Dobbeltklikk **Formatkode**-cellen, og velg deretter **CAL**.
3.  Klikk på **relaterte formler/rader/enheter** celle, og angi deretter en betinget beregning som starter med en **Hvis @Unit**konstruksjon.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE-setninger i en kolonnedefinisjon

En **IF/THEN/ELSE**-setning gjør det mulig for alle beregninger å være avhengig av resultatene fra andre kolonner. Du kan referere til andre kolonner, men du kan ikke referere til en rapportcelle i **IF**-setningen. Alle beregninger må brukes på hele kolonnen. For eksempel setningen **Hvis B&gt;100 og andre B-C\*1,25** betyr "Hvis beløpet i kolonne B er mer enn 100, setter du verdien fra kolonne B i den **Beregning** kolonnen. Hvis beløpet i kolonne B ikke er større enn 100, multipliser verdien i kolonne C med 1,25 og sette resultatet inn i **CALC**-kolonnen. " Etterfølg alltid **IF**-setning med en logisk setning som kan evalueres som sann eller usann. Formlene som du bruker for både **THEN**- og **ELSE**-setningen, kan inneholde referanser til flere kolonner, og disse formlene kan være så komplisert som du har behov for. **Obs!**  Du kan ikke sette resultatene av en beregning inn i andre kolonner. Resultatet må være i kolonnen som inneholder formelen.


