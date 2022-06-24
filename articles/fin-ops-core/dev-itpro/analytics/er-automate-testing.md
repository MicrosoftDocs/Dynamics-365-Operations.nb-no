---
title: Automatisere testing med elektronisk rapportering
description: Denne artikkelen beskriver hvordan du kan bruke grunnlinjefunksjonen for elektronisk rapportering (ER) til å automatisere testing av en funksjonalitet.
author: NickSelin
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: df2baa988bb634db11d819dd84ef73eaa560bab9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892776"
---
# <a name="automate-testing-with-electronic-reporting"></a>Automatisere testing med elektronisk rapportering

[!include[banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan bruke rammeverket for elektronisk rapportering (ER) til å automatisere testing av en del funksjonalitet. Eksemplet i denne artikkelen viser hvordan du automatiserer testingen av behandling av leverandørbetaling.

Programmet bruker ER-rammeverket til å generere betalingsfiler og tilsvarende dokumenter under behandling av leverandørbetaling. ER-rammeverket består av en datamodell, modelltilordninger og formateringskomponenter som støtter betalingsbehandling for ulike betalingstyper og generering av dokumenter i forskjellige formater. Disse komponentene kan lastes ned fra Microsoft Dynamics Lifecycle Services (LCS) og importeres i forekomsten.

Du kan også tilpasse hver Microsoft-komponent og bruke den som grunnlag for en egendefinert komponent. Hvis du oppretter en egendefinert versjon, kan du gjøre endringer som støtter bestemte krav. Du kan for eksempel justere ER-datamodellen og ER-modelltilordningen for å få tilgang til kundespesifikke programdata, eller du kan endre et ER-format for å endre oppsettet for et generert dokument.

Du kan bruke tilpassede ER-formater til å behandle betalingsfiler som genererer leverandørbetalinger, og til å behandle kontrollrapporter. Versjonskontroll støttes i ER-komponenter. Microsoft kan derfor tilby oppdaterte versjoner av ER-løsninger for behandling av leverandørbetaling, og du kan automatisk slå sammen den oppdaterte versjonen med den tilpassede komponenten ved å rebasere den. Du må imidlertid teste den rebaserte versjonen for å være sikker på at den fungerer som forventet.

ER-datamodeller og ER-modelltilordninger er felles for mange ER-formater som brukes til å behandle betalinger av forskjellige typer og å generere lands-/områdespesifikke betalingsdokumenter. Det er derfor svært ønskelig å automatisere testing av brukergodkjenning og integrering, slik at den utføres automatisk i firmaer, men tar hensyn til lands-/områdekonteksten for hvert målfirma, bruker forskjellige datasett og så videre.

Hvis du vil ha mer informasjon om hvordan du oppretter en egendefinert versjon av et format som er basert på formatet du har mottatt fra en konfigurasjonsleverandør, kan du se [ER Oppgradere formatet ved å ta i bruk en ny, grunnleggende versjon av dette formatet](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Nøkkelbegreper

Avanserte funksjonsbrukere kan redigere testing av brukergodkjenning og integrering uten å måtte skrive kildekode.

- Bruk ER-grunnlinjefunksjonen til å sammenligne genererte dokumenter med hovedkopier. Hvis du vil ha mer informasjon, kan du se [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md).
- Bruk oppgaveopptakeren til å ta opp testtilfeller, og ta med grunnlinjevurdering. Hvis du vil ha mer informasjon, kan du se [Ressurser for Oppgaveregistrering](../user-interface/task-recorder.md).
- Grupper testtilfeller for testscenarier som kreves. Hvis du vil ha mer informasjon, kan du se [Opprette og automatisere brukergodkjenningstester](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Bruk Forretningsprosessmodelerer (BPM) i LCS til å opprette biblioteker for brukergodkjenningstester.
    - Bruk BPM-testbiblioteker til å opprette en testplan og testserier i Microsoft Azure DevOps Services (Azure DevOps).

Avanserte funksjonsbrukere kan kjøre brukergodkjennings- og integreringstester.

- Bruk RSAT (Regression Suite Automation Tool) til å kjøre testtilfeller i ønsket testserie.
- Rapporter resultatene av testingen til Azure DevOps, og bruk denne tjenesten til å undersøke disse resultatene.

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre oppgavene i denne artikkelen, må du ha oppfylt følgende forutsetninger:

- Distribuer en topologi som støtter testautomatisering. Du må ha tilgang til forekomsten i denne topologien for rollen **Systemansvarlig**. Denne topologien må inneholde demonstrasjonsdataene som blir brukt i dette eksemplet. Hvis du vil ha mer informasjon, kan du se [Distribuere og bruke et miljø som støtter sammenhengende automatisering av bygging og testing](../perf-test/continuous-build-test-automation.md).
- Hvis du vil kjøre brukergodkjennings- og integreringstester automatisk, må du installere RSAT i topologien du bruker, og konfigurere den på riktig måte. Hvis du vil ha mer informasjon om hvordan du installerer og konfigurerer RSAT og konfigurerer det slik at det fungerer med Finance and Operations-apper og Azure DevOps, kan du se [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Vær oppmerksom på forutsetningene for å bruke verktøyet. Illustrasjonen nedenfor viser et eksempel på RSAT-innstillingene. Det blå rektanglet vises rundt parameterne som angir tilgang til Azure DevOps. Det grønne rektanglet vises rundt parameterne som angir tilgang til forekomsten.

    ![RSAT-innstillinger.](media/GER-Configure.png "Skjermbilde av dialogboksen RSAT-innstillinger")

- For å kunne organisere testtilfeller i serier og derved bidra til å garantere riktig utførelsessekvens, slik at du kan samle logger med testutførelser for ytterligere rapportering og undersøkelse, må du ha tilgang til Azure DevOps fra den distribuerte topologien.
- For å fullføre eksemplet i denne artikkelen anbefaler vi at du laster ned [ER-bruk for RSAT-tester](https://go.microsoft.com/fwlink/?linkid=874684). Denne ZIP-filen inneholder følgende oppgaveveiledninger:

    | Innhold                                           | Filnavn og -plassering |
    |---------------------------------------------------|------------------------|
    | Eksempel på oppgaveopptak for å klargjøre data for testing | Prepare\\Recording.xml |
    | Eksempel på oppgaveopptak for å behandle leverandørbetaling   | Process\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Klargjøre leverandørmodulen for å behandle leverandørbetalinger

1. Logg på forekomsten.
2. Last ned følgende ER-konfigurasjoner fra LCS. Hvis du vil ha instruksjoner, kan du se [ER Importere en konfigurasjon fra Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).

    - **Betalingsmodell** – ER-modellkonfigurasjon
    - **Betalingsmodelltilordning 1611** – ER-modelltilordningskonfigurasjon
    - **BBS (Storbritannia)** – ER-formatkonfigurasjon

    ![Konfigurasjoner for elektronisk rapportering.](media/GER-Configurations.png "Skjermbilde av Konfigurasjoner-siden i Elektronisk rapportering")

3. Velg demonstrasjonsdatafirmaet **GBSI**, som har en lands-/områdekontekst i Storbritannia.
4. Konfigurer leverandørparametere:

    1. Gå til **Leverandører \> Betalingsoppsett \> Betalingsmåter**.
    2. Velg betalingsmåten **Elektronisk**.
    3. Konfigurer den valgte betalingsmåten slik at den bruker ER-formatet **BBS (Storbritannia)**, som du lastet ned tidligere for behandling av leverandørbetaling:

        1. I hurtigfanen **Filformater** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.
        2. I feltet **Eksportformatkonfigurasjon** velger du **BBS (Storbritannia)**.

    ![Betalingsmåter-siden.](media/GER-APParameters.png "Skjermbilde av Betalingsmåter-siden")

    > [!NOTE]
    > Hvis du har den avledede versjonen av dette ER-formatet som ble opprettet for å støtte tilpasninger, kan du velge denne konfigurasjonen i betalingsmåten **Elektronisk**.

5. Opprette et eksempel på leverandørbetaling:

    1. Gå til **Leverandører \> Betalinger \> Betalingsjournal**.
    2. Kontroller at du ikke har postert betalingsjournalen.

        ![Betalingsjournal-siden.](media/GER-APJournal.png "Skjermbilde av Betalingsjournal-siden")

    3. Velg **Linjer**, og angi en linje som inneholder informasjonen nedenfor.

        | Felt               | Eksempelverdi   |
        |---------------------|-----------------|
        | Navn på leverandør         | GB\_SI\_000001  |
        | Debet               | 1,000.00        |
        | Valuta            | GBP             |
        | Motkontotype | Bank            |
        | Motkonto      | GBSI OPER       |
        | Betalingsmåte   | Elektronisk      |

    ![Leverandørbetalinger-siden.](media/GER-APJournalLines.png "Skjermbilde av Leverandørbetalinger-siden")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Klargjøre ER-rammeverket for å teste behandling av leverandørbetaling

### <a name="configure-er-parameters"></a>Konfigurere ER-parametere

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Parametere for elektronisk rapportering**.
2. I **Grunnlinje**-feltet i **Vedlegg**-fanen velger du **Fil** som dokumenttypen som DM-rammeverket (dokumentstyring) skal bruke til å beholde dokumenter som er knyttet til grunnlinjefunksjonen, som DM-vedlegg.

    ![Siden Parametere for elektronisk rapportering.](media/GER-ERParameters.png "Skjermbilde av siden Parametere for elektronisk rapportering")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Generer grunnlinjekopier av dokumenter som er knyttet til leverandørbetaling

1. Gå til **Leverandører \> Betalinger \> Betalingsjournal**.
2. Velg **Linjer**.
3. Velg **Generer betalinger**.
4. Velg betalingsmåten **Elektronisk**.
5. Velg bankkontoen **GBSI OPER**.
6. Sett alternativet **Skriv ut kontrollrapport** til **Ja**.
7. Last ned de genererte utdataene som en ZIP-fil.
8. Åpne den nedlastede filen.
9. Pakk ut følgende filer fra den nedlastede filen:

    - **Fil** – betalingsfil i tekstformat
    - **ERVendOutPaymControlReport** – kontrollrapportfil i XLSX-format

    ![Utpakkede filer.](media/GER-APJournalProcessed.png "Skjermbilde av navn på utpakkede filer i Windows Utforsker")

### <a name="turn-on-the-er-baseline-feature"></a>Aktivere ER-grunnlinjefunksjonen

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. Velg **Brukerparametere** i **Konfigurasjoner**-fanen i handlingsruten.
3. Sett alternativet **Kjør i feilsøkingsmodus** til **Ja**.

Hvis du aktiverer parameteren **Kjør i feilsøkingsmodus**, tvinger du ER-rammeverket til å utføre følgende handlinger etter utførelsen av ethvert ER-format som genererer utgående dokumenter:

1. Finn ut om en grunnlinje ble konfigurert for noen av komponentene i det utførte ER-formatet.
2. Finn ut om hver konfigurerte grunnlinje gjelder under gjeldende forhold (firmakode for det påloggede firmaet, filnavn og filtype for de genererte utdataene og så videre).
3. Utfør følgende handlinger for hver gjeldende grunnlinje:

    1. Sammenlign utdataene som genereres under utførelse av ER-formatet, med den tilsvarende grunnlinjen.
    2. Lagre resultatene av sammenligningen i feilsøkingsloggen for ER-konfigurasjoner.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Konfigurer ER-grunnlinjer for behandling av leverandørbetaling

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. Velg **Grunnlinjer**.
3. Velg **Ny**.
4. I feltet **Referanse** velger du formatet **BBS (Storbritannia)**.
5. Velg **Vedlegg**.
6. Legg til en ny grunnlinje for leverandørbetalingsfilen:

    1. Velg **Ny**.
    2. I **Type**-feltet velger du DM-dokumenttypen **Fil** som du konfigurerte i ER-parameterne for å lagre grunnlinjeartefakter.
    3. Bla gjennom for å velge den lokalt lagrede **Fil**-betalingsfilen i tekstformat.
    4. I **Beskrivelse**-feltet angir du **TXT-fil for betaling**.

7. Legg til en ny grunnlinje for kontrollrapporten for leverandørbetalingen:

    1. Velg **Ny**.
    2. I **Type**-feltet velger du DM-dokumenttypen **Fil** som du konfigurerte i ER-parameterne for å lagre grunnlinjeartefakter.
    3. Bla gjennom for å velge den lokalt lagrede kontrollrapportfilen **ERVendOutPaymControlReport** i XLSX-format.
    4. I **Beskrivelse**-feltet angir du **XLSX-fil for betalingskontrollrapport**.

    ![Grunnlinjer for leverandørbetalingsfilen og kontrollrapporten.](media/GER-BaselineAttachments.png "Skjermbilde av Konfigurasjoner-siden med XLSX-fil for betalingskontrollrapport valg")

8. Lukk siden.
9. I hurtigfanen **Grunnlinjer** velger du **Ny** for å konfigurere en grunnlinje for betalingsfilen:

    1. Gi linjen navnet **Grunnlinjeinnstilling for betalingsfil**.
    2. I feltet **Navn på filkomponent** velger du **fil** for å bruke denne grunnlinjen på utdataene i ER-format som genererer betalingsfilen i tekstformatet BBS (Storbritannia).
    3. I **Firmaer**-feltet velger du **GBSI** for å bruke denne grunnlinjen når ER-formatet **BBS (Storbritannia)** kjøres i firmaet GBSI.
    4. I feltet **Filnavnmaske** angir du **\*.TXT** for å bruke denne grunnlinjen bare på utdata i **fil**-formatkomponenten som har filtypen **.txt**.
    5. I **Grunnlinje**-feltet velger du **TXT-fil for betaling**, slik at denne grunnlinjen brukes til sammenligning med de genererte utdataene.

10. Velg **Ny** for å konfigurere en grunnlinje for kontrollrapporten:

    1. Gi linjen navnet **Grunnlinjeinnstilling for kontrollrapport**.
    2. I feltet **Navn på filkomponent** velger du **ERVendOutPaymControlReport** for å bruke denne grunnlinjen på utdataene i ER-format som genererer kontrollrapporten.
    3. I **Firmaer**-feltet velger du **GBSI** for å bruke denne grunnlinjen når ER-formatet **BBS (Storbritannia)** kjøres i firmaet GBSI.
    4. I feltet **Filnavnmaske** angir du **\*.XLSX** for å bruke denne grunnlinjen bare på utdata i formatkomponenten **ERVendOutPaymControlReport** som har filtypen **.xslx**.
    5. I **Grunnlinje**-feltet velger du **XLSX-fil for betalingskontrollrapport**, slik at denne grunnlinjen brukes til sammenligning med de genererte utdataene.

    ![Skjermbilde av hurtigfanen Grunnlinjer på Konfigurasjoner-siden.](media/GER-BaselineRules.png "Skjermbilde av hurtigfanen Grunnlinjer på Konfigurasjoner-siden")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Ta opp tester for å validere behandling av leverandørbetaling

Som avansert funksjonsbruker kan du ta opp dine egne trinn for å teste behandling av leverandørbetaling. Vi anbefaler at du spiller av oppgaveopptaket **Prepare\\Recording.xml** du lastet ned tidligere (og redigerer det etter behov). Dette opptaket brukes til å angi riktig tilstand for alle testdataene. Dette trinnet er nødvendig fordi testingen kan gjøres mange ganger, og alle testene må bruke data som er i samme tilstand.

### <a name="reset-user-settings"></a>Tilbakestille brukerinnstillinger

1. Åpne standard instrumentbord.
2. Velg **Innstillinger**-knappen (tannhjulsymbolet).
3. Velg **Brukeralternativer**.
4. Velg **Bruksdata**.
5. Velg **Tilbakestill**.
6. Velg **Ja** for å bekrefte at du vil tilbakestille bruksdataene.
7. Lukk siden.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Ta opp trinnene for å klargjøre data for testing

1. Velg **Innstillinger**-knappen (tannhjulsymbolet).
2. Velg **Oppgaveopptaker**.
3. Velg **Spill av opptak**.
4. Velg **Åpne fra denne PC-en**.
5. Velg **Bla gjennom**, og velg den lokalt lagrede filen **Prepare\\Recording.xml**.
6. Velg **Start**.
7. Fortsett å velge **Spill av neste ventende trinn** til alle trinnene i opptaket er avspilt.

Dette oppgaveopptaket utfører følgende handlinger:

1. Sett statusen for den behandlede betalingslinjen til **Ingen**.

    ![Skjermbilde av oppgaveopptakstrinn 3 til og med 4.](media/GER-Recording1Review1.png "Skjermbilde av oppgaveopptakstrinn 3 til og med 4")

2. Aktiver ER-brukerparameteren **Kjør i feilsøkingsmodus**.

    ![Skjermbilde av oppgaveopptakstrinn 9 til og med 10.](media/GER-Recording1Review2.png "Skjermbilde av oppgaveopptakstrinn 9 til og med 10")

3. Rydd opp i feilsøkingsloggen for ER som inneholder resultatene av sammenligningen av genererte filer og grunnlinjer.

    ![Skjermbilde av oppgaveopptakstrinn 13 til og med 15.](media/GER-Recording1Review3.png "Skjermbilde av oppgaveopptakstrinn 13 til og med 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Ta opp trinnene for å teste behandling av leverandørbetaling

Vi anbefaler at du spiller av oppgaveopptaket **Process\\Recording.xml** du lastet ned tidligere (og redigerer det etter behov). Dette opptaket brukes til å behandle leverandørbetalinger og validere resultatene av sammenligningen av genererte dokumenter og tilsvarende grunnlinjer.

1. Velg **Innstillinger**-knappen (tannhjulsymbolet).
2. Velg **Oppgaveopptaker**.
3. Velg **Spill av opptak**.
4. Velg **Åpne fra denne PC-en**.
5. Velg **Bla gjennom**, og velg den lokalt lagrede filen **Process\\Recording.xml**.
6. Velg **Start**.
7. Fortsett å velge **Spill av neste ventende trinn** til alle trinnene i opptaket er avspilt.

Dette oppgaveopptaket utfører følgende handlinger:

1. Start behandling av leverandørbetaling.
2. Velg de riktige kjøretidsparameterne, og aktiver generering av en kontrollrapport.

    ![Skjermbilde av oppgaveopptakstrinn 3 til og med 8.](media/GER-Recording2Review1.png "Skjermbilde av oppgaveopptakstrinn 3 til og med 8")

3. Åpne feilsøkingsloggen for ER for å ta opp resultatene av sammenligningen av genererte utdata og tilsvarende grunnlinjer.

    Resultatene av sammenligningen vises i feltet **Generert tekst** i feilsøkingsloggen for ER. Feltene **Formatkomponent** og **Formatbane som forårsaket en loggoppføring** refererer til filkomponenten som de genererte utdataene har blitt sammenlignet med grunnlinjen for.

    ![Oppføringer på siden Kjøringslogger for elektronisk rapportering.](media/GER-ERDebugLog.png "Skjermbilde av oppføringer på siden Kjøringslogger for elektronisk rapportering")

4. Sammenligningen av de gjeldende utdataene med grunnlinjen tar du opp ved å bruke alternativet **Valider** i Oppgaveopptaker og velge **Gjeldende verdi**.

    ![Bruke alternativet Valider til sammenligning med den gjeldende verdien.](media/GER-TRRecordValidation.png "Skjermbilde av å bruke alternativet Valider til sammenligning med den gjeldende verdien")

    Illustrasjonen nedenfor viser hvordan valideringstrinnene som er tatt opp, ser ut i oppgaveopptaket.

    ![Skjermbilde av oppgaveopptakstrinn 13 og 15.](media/GER-Recording2Review2.png "Skjermbilde av oppgaveopptakstrinn 13 og 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Legge til testene som er tatt opp, i Azure DevOps

1. Åpne Azure DevOps-miljøet.
2. Velg prosjektet du definerte i RSAT-parameterne da du [konfigurerte verktøyet](#prerequisites).
3. Velg testplanen du definerte i RSAT-parameterne da du [konfigurerte verktøyet](#prerequisites).
4. Opprett et nytt testtilfelle for den valgte testplanen:

    1. Gi testtilfellet navnet **Klargjør data for å teste behandling av leverandørens elektroniske betaling**.
    2. Legg ved filen **Recording.xml** fra **Prepare**-mappen du lastet ned tidligere.

5. Opprett et nytt testtilfelle for den valgte testplanen:

    1. Gi testtilfellet navnet **Test behandling av leverandørbetalinger ved å bruke ER-formatet BBS (Storbritannia)**.
    2. Legg ved filen **Recording.xml** fra **Process**-mappen du lastet ned tidligere.

    ![Nye testtilfeller for den valgte testplanen.](media/GER-RSAT-DevOps-Tests-Passed.png "Skjermbilde av de nye testtilfellene for den valgte testplanen")

> [!NOTE]
> Vær oppmerksom på den riktige utføringsrekkefølgen til testene som legges til.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Klargjøre RSAT for å kjøre testene som er tatt opp

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Laste inn testene fra Azure DevOps til RSAT

1. Åpne det lokale RSAT-programmet i den gjeldende topologien.
2. Velg **Last inn** for å laste inn testene som for øyeblikket ligger i Azure DevOps, i RSAT.

    ![Tester lastet inn i RSAT.](media/GER-RSAT-RSAT-Tests-Loaded.png "Skjermbilde av testene som er lastet inn i RSAT")

### <a name="create-automation-and-parameters-files"></a>Opprette automatiserings- og parameterfiler

1. I RSAT velger du testene du lastet inn fra Azure DevOps.
2. Velg **Ny** for å opprette automatiserings- og parameterfiler for RSAT.

    ![Automatiserings- og parameterfiler for RSAT opprettet i RSAT.](media/GER-RSAT-RSAT-Tests-Initiated.png "Skjermbilde av automatiserings- og parameterfiler for RSAT som er opprettet i RSAT")

### <a name="modify-the-parameters-files"></a>Endre parameterfilene

1. Velg testtilfellet **Klargjør data for å teste behandling av leverandørens elektroniske betaling** i RSAT.
2. Velg **Rediger**.
3. I Microsoft Excel-arbeidsboken som åpnes, endrer du firmakoden til **GBSI** i regnearket **Generelt** siden dette firmaet skal brukes til testutførelse.
4. Velg testtilfellet **Test behandling av leverandørbetalinger ved å bruke ER-formatet BBS (Storbritannia)** i RSAT.
5. Velg **Rediger**.
6. I Excel-arbeidsboken som åpnes, endrer du firmakoden til **GBSI** i regnearket **Generelt**.
7. I regnearket **ERFormatMappingRunLogTable** legger du merke til at cellene A:3 og C:3 inneholder teksten til feltene i feilsøkingsloggtabellen for ER som brukes til å validere resultatene av sammenligningen av utdataene og grunnlinjen. Disse tekstene brukes til å evaluere poster i feilsøkingsloggen for ER som opprettes under testutførelsen.

    ![Skjermbilde av regnearket ERFormatMappingRunLogTable.](media/GER-RSAT-RSAT-ExcelParameters.png "Skjermbilde av regnearket ERFormatMappingRunLogTable")

## <a name="run-the-tests-and-analyze-the-results"></a>Kjøre testene og analysere resultatene

### <a name="run-the-tests-in-rsat"></a>Kjøre testene i RSAT

1. I RSAT velger du de innlastede testene.
2. Velg **Kjør**.

Legg merke til at testtilfeller kjøres automatisk i programmet ved hjelp av en nettleser.

### <a name="analyze-the-results-of-test-execution"></a>Analysere resultatene av testutførelsen

Resultatene av testutførelsen lagres i RSAT. Legg merke til at begge testene har bestått.

![Tester som har bestått i RSAT.](media/GER-RSAT-RSAT-Tests-Passed.png "Skjermbilde av tester som har bestått i RSAT")

Legg merke til at resultatene av testutførelsen også sendes til Azure DevOps, slik at du kan analysere ytterligere.

![Skjermbilde av resultatene av testutførelse i Azure DevOps.](media/GER-RSAT-DevOps-Tests-Added.png "Skjermbilde av resultatene av testutførelse i Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Simulere en situasjon der tester ikke består

Denne testserien kan ikke ha bestått når minst ett av de genererte utdataene ikke samsvarer med den tilsvarende grunnlinjen. For å skape denne situasjonen kan du bruke den avledede versjonen av formatet **BBS (Storbritannia)**, som genererer en betalingsfil som har et annet innhold enn den tilsvarende grunnlinjen. Du kan simulere denne situasjonen ved å bruke det samme formatet **BBS (Storbritannia)**, men endre betalingsbeløpet på den behandlede betalingslinjen.

1. Åpne programmet, og gå til **Leverandører \> Betalinger \> Betalingsjournal**.
2. Velg **Linjer**.
3. Velg betalingslinjen, og velg deretter **Betalingsstatus \> Ingen**.
4. I **Debet**-feltet endrer du verdien fra **1 000,00** til **2 000,00**.
5. Velg **Lagre** for å lagre endringene.

### <a name="run-the-tests-in-rsat"></a>Kjøre testene i RSAT

1. I RSAT velger du de innlastede testene.
2. Velg **Kjør**.

Legg merke til at testtilfeller kjøres automatisk i programmet ved hjelp av en nettleser.

### <a name="analyze-the-results-of-test-execution"></a>Analysere resultatene av testutførelsen

Resultatene av testutførelsen lagres i RSAT. Legg merke til at den andre testen ikke bestod under den andre utførelsen.

![Testresultat Ikke bestått i RSAT.](media/GER-RSAT-RSAT-Tests-Failed.png "Skjermbilde av testresultat Ikke bestått i RSAT")

Legg merke til at resultatene av testutførelsen også sendes til Azure DevOps, slik at du kan analysere ytterligere.

![Testresultat Ikke bestått i Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed.png "Skjermbilde av testresultat Ikke bestått i Azure DevOps")

Du har tilgang til statusen for hver test. Du har også tilgang til utførelsesloggen, slik at du kan analysere årsakene til eventuelle feil. I illustrasjonen nedenfor viser utførelsesloggen at testen ikke har bestått på grunn av forskjellen i innhold mellom den genererte betalingsfilen og grunnlinjen for den.

![Utførelseslogg for analyse av test som ikke har bestått, i Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Skjermbilde av utførelseslogg for analyse av test som ikke har bestått, i Azure DevOps")

Som du har sett, kan derfor virkemåten til alle ER-format evalueres automatisk ved å bruke RSAT som testplattform og å bruke Oppgaveopptaker-baserte testtilfeller som bruker ER-grunnlinjefunksjonen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Ressurser for Oppgaveregistrering](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Opprette og automatisere brukergodkjenningstester](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Distribuere og bruke et miljø som støtter sammenhengende automatisering av bygging og testing](../perf-test/continuous-build-test-automation.md)
- [Spore genererte rapportresultater og sammenligne dem med grunnlinjeverdier](er-trace-reports-compare-baseline.md)
- [ER Oppgradere formatet ved å ta i bruk en ny, grunnleggende versjon av dette formatet](tasks/er-upgrade-format.md)
- [ER Importere en konfigurasjon fra Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]