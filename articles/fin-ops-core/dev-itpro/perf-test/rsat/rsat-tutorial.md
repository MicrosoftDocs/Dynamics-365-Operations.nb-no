---
title: Opplæring for Regression Suite Automation Tool
description: Denne artikkelen viser hvordan du bruker Regression Suite Automation Tool (RSAT). Det beskriver ulike funksjoner og gir eksempler som omfatter avansert skripting.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277412"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Opplæring for Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format.

Denne opplæringen går gjennom noen av de avanserte funksjonene i Regression Suite Automation Tool (RSAT), inneholder en demonstrasjonsoppgave og beskriver strategier og ting som er viktig å lære.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Funksjoner å merke seg i RSAT og Oppgaveopptaker

### <a name="validate-a-field-value"></a>Valider en feltverdi

RSAT gjør det mulig å ta med valideringstrinn i testsaken for å validere forventede verdier. Hvis du vil ha informasjon om denne funksjonen, kan du se artikkelen [Validere forventede verdier](rsat-validate-expected.md).

Følgende eksempel viser hvordan du kan bruke denne funksjonen til å validere om lagerbeholdningen er større enn 0 (null).

1. I demonstrasjonsdataene i firmaet **USMF** oppretter du et oppgaveopptak som har følgende trinn:

    1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
    2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på verdien **1000** for **Varenummer**-feltet.
    3. Velg **Lagerbeholdning**.
    4. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på verdien **1** for **Område**-feltet.
    5. Merk den valgte raden i listen.
    6. Valider at verdien i feltet **Totalt tilgjengelig** er **411,0000000000000000**.

2. Lagre oppgaveopptaket som et **utvikleropptak**, og knytt det til testsaken i Azure DevOps.
3. Legg til testtilfellet i testplanen, og last inn testtilfellet i RSAT.
4. Åpne Excel-parameterfilen, og gå til fanen **TestCaseSteps**.
5. Du kan validere om lagerbeholdningen alltid kommer til å være større enn **0**, ved å gå til trinnet **Valider totalt tilgjengelig** og endre verdien fra **411** til **0**. Endre verdien i **Operator**-feltet fra et likhetstegn (**=**) til et større enn-tegn (**\>**).
6. Lagre og lukk Excel-parameterfilen.
7. Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen, i Azure DevOps.

Hvis verdien i feltet **Totalt tilgjengelig** for den angitte varen i beholdningen er større enn 0 (null), blir testene bestått, uavhengig av den faktiske verdien for lagerbeholdningen.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Lagrede variabler og kjeding av testsaker

En av nøkkelfunksjonene i RSAT er kjeding av testtilfeller, det vil si muligheten for en test til å sende variabler til andre tester. Hvis du vil ha mer informasjon, se artikkelen [Kopiere variabler for å kjede testtilfeller](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Avledet testtilfelle

RSAT lar deg bruke samme oppgaveopptak med flere testtilfeller, slik at en oppgave kan kjøres med forskjellige datakonfigurasjoner. Se artikkelen [Avledede testtilfeller](rsat-derived-test-cases.md) for mer informasjon.

### <a name="validate-notifications-and-messages"></a>Validere varslinger og meldinger

Denne funksjonen kan brukes til å validere om en handling er utført. Når en produksjonsordre for eksempel opprettes, estimeres og deretter startes, viser appen meldingen "Produksjon – start" for å varsle deg om at produksjonsordren er startet.

![Varslingen Produksjon – start.](./media/use_rsa_tool_05.png)

Du kan validere denne meldingen via RSAT ved å angi meldingsteksten i fanen **Meldingsvalidering** i Excel-parameterfilen for det aktuelle opptaket.

![Fanen Meldingsvalidering.](./media/use_rsa_tool_06.png)

Etter at testtilfellet er kjørt, sammenlignes meldingen i Excel-parameterfilen med meldingen som vises. Hvis meldingene ikke samsvarer, mislykkes testtilfellet.

> [!NOTE]
> Du kan angi flere meldinger i fanen **Meldingsvalidering** i Excel-parameterfilen. Meldingene kan også være feilmeldinger eller advarsler i stedet for informasjonsmeldinger.

### <a name="snapshot"></a>Øyeblikksbilde

Denne funksjonen tar skjermbilder av trinnene som ble utført under oppgaveopptaket. Dette er nyttig for revisjon og feilsøking.

- Hvis du vil bruke denne funksjonen mens du kjører RSAT med brukergrensesnittet, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien i følgende element fra **false** til **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Hvis du vil bruke denne funksjonen mens du kjører RSAT fra CLI (for eksempel Azure DevOps), åpner du filen **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien i følgende element fra **false** til **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Når du kjører testtilfeller, vil RSAT generere øyeblikksbilder av trinnene og lagre dem i avspillingsmappen for testtilfellene i den gjeldende katalogen. I avspillingsmappen opprettes det en egen undermappe med navnet **StepSnapshots**. Denne mappen inneholder øyeblikksbilder av testtilfeller som kjøres.

## <a name="assignment"></a>Tildeling

### <a name="scenario"></a>Scenario

1. Produktdesigneren oppretter et nytt frigitt produkt.
2. Produksjonssjefen starter en produksjonsordre for å bringe lagernivået til to stykker.
3. Produksjonen starter og avslutter produksjonsordren og kontrollerer at beholdningsantallet er to stykker.
4. Salgsteamet mottar en ordre på fire stykker av det nye produktet. Salgsteamet oppdaterer derfor nettobehovet via den dynamiske planen. Siden det ikke finnes mer kapasitet, settes standard ordrepolicy til «kjøp i stedet for å lage». Det opprettes derfor et bestillingsforslag.
5. Innkjøperen legger til en leverandør, autoriserer bestillingsforslaget og bekrefter deretter bestillingen.
6. Når varene som ble kjøpt, ankommer i butikken, søker butikkoperatøren etter den tilknyttede bestillingen og mottar varene. Siden ordren nå er fullført, kan varene plukkes og pakkes mot salgsordren.
7. Finans posterer innkjøpsfakturaen og salgsfakturaen.

Illustrasjonen nedenfor viser flyten for dette scenariet.

![Flyt for demonstrasjonsscenariet.](./media/use_rsa_tool_14.png)

Følgende illustrasjon viser hierarkiet for forretningsprosesser for dette scenarioet i LCS Forretningsprosessmodelerer.

![Forretningsprosesser for demonstrasjonsscenariet.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategi – viktige punkt

### <a name="data"></a>Data

- Sørg for at du har representative datavolumer (en kopi av konfigurasjonsdata for produksjon / gylne konfigurasjonsdata pluss overførte data).
- Når du genererer nye data via Oppgaveopptaker, oppretter du testnavn som ikke kommer i konflikt med eksisterende navn (for eksempel ved å bruke et prefiks som **RSATxxx**).
- Bruk tidsgjenoppretting av database for Azure til å kjøre tester på nytt i andre miljøer enn Lag 1-miljøer.
- Selv om du kan bruke Excel-funksjonene **TILFELDIG** og **NÅ** til å generere en unik kombinasjon, er det langt fra lettvint. Her er et eksempel:

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Oppgaveopptaker

- Definer scenarier før du starter opptaket. Et velstyrt prosjekt har forhåndsdefinerte testscenarier. Når du skal bygge et testtilfelle, vurderer du hvor forutsigbart resultatet av testscenariene er.
- Del opp opptak hvis de skal utføres av ulike roller, eller hvis det er ventetid eller en ekstern hendelse før neste trinn.
- Unngå å velge verdier i lister. Bruk i stedet tekstformater, for eksempel **FIFO**, **AudioRM** og **SiteWH**. Når du velger i en liste, blir posisjonen til verdien i listen tatt opp, ikke selve verdien. Hvis elementer blir lagt til i denne listen, kan posisjonen til verdien bli endret. Derfor bruker opptaket en annen parameter, og resten av scenariet kan bli påvirket.
- Tenk på flerbrukerfunksjonalitet. Du kan for eksempel ikke ta for gitt at den nyopprettede salgsordren alltid velges automatisk. Bruk i stedet alltid filteret til å finne riktig ordre.
- Bruk Kopier-funksjonen i Oppgaveopptaker til å lagre navnet på et nyopprettet produkt, slik at det kan brukes i kjedede testtilfeller.
- Bruk Valider-funksjonen i Oppgaveopptaker til å angi kontrollpunkt som kontrollerer at trinn er kjørt på riktig måte.

### <a name="rsat"></a>RSAT

- Hvis du vil kjøre testen i et annet firma, kan du endre firmaet i **Generelt**-fanen i Excel-parameterfilen. Sørg for at innstillingene og dataene er tilgjengelige i det nylig valgte firmaet.
- Du kan endre testbrukeren i **Generelt**-fanen i Excel-parameterfilen. Angi e-post-ID-en til brukeren som skal kjøre testtilfellet. På denne måten kan testtilfellet kjøres ved hjelp av sikkerhetstillatelsene til den angitte brukeren.
- Hvis du vil vente før testen startes, kan du definere en pause i **Generelt**-fanen i Excel-parameterfilen. Pausen kan brukes i en satsvis jobb (for eksempel hvis en arbeidsflyt må kjøres før neste trinn kan utføres).

## <a name="advanced-scripting"></a>Avansert skripting

### <a name="cli"></a>CLI

RSAT kan kalles fra et **ledetekstvindu** eller et **PowerShell**-vindu.

> [!NOTE]
> Kontroller at miljøvariabelen **TestRoot** er satt til RSAT-installasjonsbanen. (I Microsoft Windows åpner du **Kontrollpanel**, velger **System og sikkerhet \> System \> Avanserte systeminnstillinger** og deretter **Miljøvariabler**.)

1. Åpne et **ledetekstvindu** eller et **PowerShell**-vindu som administrator.
2. Gå til installasjonskatalogen for RSAT.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Vis alle kommandoer.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Viser alle kommandoer eller viser hjelp for en bestemt kommando sammen med de tilgjengelige parameterne.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valgfrie parametere

`command`: Der ``[command]`` er en av kommandoene i den forrige listen.

#### <a name="about"></a>om

Viser versjonen av det installerte RSAT-systemet.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Tømmer skjermen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>download

Laster ned vedlegg (registrering, kjøring og parameterfiler) for det angitte testtilfellet fra Azure DevOps til utdatakatalogen. Du kan bruke kommandoen ``list`` til å hente alle tilgjengelige testtilfeller, og bruke en hvilken som helst verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil nedlastingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.

##### <a name="download-required-parameters"></a>download: nødvendige parametere

+ `test_case_id`: representerer ID-en til testsaken.

##### <a name="download-optional-parameters"></a>download: valgfrie parametere

+ `output_dir`: Representerer arbeidskatalogen for utdata. Katalogen må finnes. Arbeidskatalogen fra innstillingene vil bli brukt hvis denne parameteren ikke er spesifisert.

##### <a name="download-examples"></a>download: eksempler

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Laster ned vedlegg (registrering, kjøring og parameterfiler) for alle testtilfeller i den angitte testserien fra Azure DevOps til utdatakatalogen. Du kan bruke kommandoen ``listtestsuitenames`` til å hente alle tilgjengelige testserier, og bruke en hvilken som helst verdi som en **test_suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil nedlastingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/byid`: Denne bryteren angir at den ønskede testserien identifiseres av dens Azure DevOps-ID i stedet for navnet på testserien.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: nødvendige parametere

+ `test_suite_name`: representerer navnet på testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **ikke** er angitt. Dette navnet er navnet på Azure DevOps-testserien.
+ `test_suite_id`: representerer ID-en til testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **er** angitt. Denne ID-en er Azure DevOps-ID-en for testserien.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: valgfrie parametere

+ `output_dir`: Representerer arbeidskatalogen for utdata. Katalogen må finnes. Arbeidskatalogen fra innstillingene vil bli brukt hvis denne parameteren ikke er spesifisert.

##### <a name="downloadsuite-examples"></a>downloadsuite: eksempler

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>rediger

Lar deg åpne parameterfilen i Excel-programmet og redigere den.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: nødvendige parametere

+ `excel_file`: må inneholde en fullstendig bane til en eksisterende Excel-fil.

##### <a name="edit-examples"></a>edit: eksempler

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Genererer testkjøring og parameterfiler for den angitte testsaken i utdatamappen. Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker. Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil genereringsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/dllonly`: Generer bare filer for testkjøring. Ikke generer Excel-parameterfilen på nytt.
+ `/keepcustomexcel`: Oppgrader den eksisterende parameterfilen. Generer også kjøringsfilene på nytt.

##### <a name="generate-required-parameters"></a>generere: nødvendige parametere

+ `test_case_id`: representerer ID-en til testsaken.

##### <a name="generate-optional-parameters"></a>generate: valgfrie parametere

+ `output_dir`: Representerer arbeidskatalogen for utdata. Katalogen må finnes. Arbeidskatalogen fra innstillingene vil bli brukt hvis denne parameteren ikke er spesifisert.

##### <a name="generate-examples"></a>generere: eksempler

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Genererer en ny avledet testsak (underordnet testsak) fra den angitte testsaken. Den nye testsaken legges også til i angitte testserien. Du kan bruke kommandoen ``list`` til å hente alle tilgjengelige testtilfeller, og bruke en hvilken som helst verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil genereringsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.

##### <a name="generatederived-required-parameters"></a>generatederived: nødvendige parametere

+ `parent_test_case_id`: representerer ID-en til den overordnede testsaken.
+ `test_plan_id`: representerer ID-en til testplanen.
+ `test_suite_id`: representerer ID-en til testverktøyet.

##### <a name="generatederived-examples"></a>generatederived: eksempler

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Genererer bare testkjøringsfiler for den angitte testsaken. Den generer ikke Excel-parameterfilen på nytt. Filene genereres i den angitte utdatakatalogen. Du kan bruke kommandoen ``list`` til å hente alle tilgjengelige testtilfeller, og bruke en hvilken som helst verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil genereringsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: nødvendige parametere

+ `test_case_id`: representerer ID-en til testsaken.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: valgfrie parametere

+ `output_dir`: Representerer arbeidskatalogen for utdata. Katalogen må finnes. Arbeidskatalogen fra innstillingene vil bli brukt hvis denne parameteren ikke er spesifisert.

##### <a name="generatetestonly-examples"></a>generatetestonly: eksempler

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Genererer testautomatiseringsfiler for alle testsaker i den angitte testserien. Du kan bruke kommandoen ``listtestsuitenames`` til å hente alle tilgjengelige testserier, og bruke en hvilken som helst verdi som en **test_suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil genereringsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/dllonly`: Generer bare filer for testkjøring. Ikke generer Excel-parameterfilen på nytt.
+ `/keepcustomexcel`: Oppgrader eksisterende parameterfil. Generer også kjøringsfilene på nytt.
+ `/byid`: Denne bryteren angir at den ønskede testserien identifiseres av dens Azure DevOps-ID i stedet for navnet på testserien.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: nødvendige parametere

+ `test_suite_name`: representerer navnet på testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **ikke** er angitt. Dette navnet er navnet på Azure DevOps-testserien.
+ `test_suite_id`: representerer ID-en til testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **er** angitt. Denne ID-en er Azure DevOps-ID-en for testserien.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: valgfrie parametere

+ `output_dir`: Representerer arbeidskatalogen for utdata. Katalogen må finnes. Arbeidskatalogen fra innstillingene vil bli brukt hvis denne parameteren ikke er spesifisert.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: eksempler

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>help

Identisk med [?](#section)- kommandoen.

#### <a name="list"></a>liste

Viser alle tilgjengelige testtilfeller i den gjeldende testplanen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Viser alle tilgjengelige testplaner.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Viser testsaker for det angitte testverktøyet. Du kan bruke kommandoen ``listtestsuitenames`` til å hente alle tilgjengelige testserier, og bruke en hvilken som helst verdi fra listen som en **suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: nødvendige parametere

+ `test_suite_name`: Navnet på den ønskede serien.

##### <a name="listtestsuite-examples"></a>listtestsuite: eksempler

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Viser testsaker for det angitte testverktøyet.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: nødvendige parametere

+ `test_suite_id`: ID-en til den ønskede serien.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: eksempler

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Viser alle tilgjengelige testserier i den gjeldende testplanen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Spiller av testtilfellet som er knyttet til den angitte Excel-parameterfilen. Denne kommandoen bruker eksisterende lokale automasjonsfiler og laster ikke ned filer fra Azure DevOps. Denne kommandoen støttes ikke for testtilfeller for POS-handel.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil avspillingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/comments[="comment"]`: Angi en egendefinert informasjonsstreng som skal tas med i **Kommentarer**-feltet på sammendrags- og testresultatsidene for Azure DevOps-testtilfelleskjøringer.

##### <a name="playback-required-parameters"></a>playback: nødvendige parametere

+ `excel_parameter_file`: Den fullstendige banen til en Excel-parameterfil. Filen må finnes.

##### <a name="playback-examples"></a>playback: eksempler

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Spiller av flere testsaker samtidig. Testtilfellene identifiseres av ID-en. Denne kommandoen vil laste ned filer fra Azure DevOps. Du kan bruke kommandoen ``list`` til å hente alle tilgjengelige testtilfeller, og bruke en hvilken som helst verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil avspillingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/comments[="comment"]`: Angi en egendefinert informasjonsstreng som skal tas med i **Kommentarer**-feltet på sammendrags- og testresultatsidene for Azure DevOps-testtilfelleskjøringer.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: nødvendige parametere

+ `test_case_id1`: ID-en for en eksisterende testsak.
+ `test_case_id2`: ID-en for en eksisterende testsak.
+ `test_case_idN`: ID-en for en eksisterende testsak.

##### <a name="playbackbyid-examples"></a>playbackbyid: eksempler

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Spiller av mange testsaker samtidig. Testtsakene identifiseres av Excel-parameterfiler. Denne kommandoen bruker eksisterende lokale automasjonsfiler og laster ikke ned filer fra Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil avspillingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/comments[="comment"]`: Angi en egendefinert informasjonsstreng som skal tas med i **Kommentarer**-feltet på sammendrags- og testresultatsidene for Azure DevOps-testtilfelleskjøringer.

##### <a name="playbackmany-required-parameters"></a>playbackmany: nødvendige parametere

+ `excel_parameter_file1`: Den fullstendige banen til Excel-parameterfilen. Filen må finnes.
+ `excel_parameter_file2`: Den fullstendige banen til Excel-parameterfilen. Filen må finnes.
+ `excel_parameter_fileN`: Den fullstendige banen til Excel-parameterfilen. Filen må finnes.

##### <a name="playbackmany-examples"></a>playbackmany: eksempler

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Spiller av alle testsaker fra en eller flere angitte testserier. Hvis bryteren /local er angitt, brukes lokale vedlegg for avspilling. Hvis ikke, lastes vedleggene ned fra Azure DevOps. Du kan bruke kommandoen ``listtestsuitenames`` til å hente alle tilgjengelige testserier, og bruke en hvilken som helst verdi fra den første kolonnen som en **suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: valgfrie brytere

+ `/updatedriver`: Hvis denne bryteren er angitt, vil webdriveren i nettleseren oppdateres etter behov før avspillingsprosessen kjøres.
+ `/local`: Denne bryteren angir at lokale vedlegg skal brukes for avspilling i stedet for å laste ned filer fra Azure DevOps.
+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil avspillingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/comments[="comment"]`: Angi en egendefinert informasjonsstreng som skal tas med i **Kommentarer**-feltet på sammendrags- og testresultatsidene for Azure DevOps-testtilfelleskjøringer.
+ `/byid`: Denne bryteren angir at den ønskede testserien identifiseres av dens Azure DevOps-ID i stedet for navnet på testserien.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: nødvendige parametere

+ `test_suite_name1`: representerer navnet på testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **ikke** er angitt. Dette navnet er navnet på Azure DevOps-testserien.
+ `test_suite_nameN`: representerer navnet på testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **ikke** er angitt. Dette navnet er navnet på Azure DevOps-testserien.
+ `test_suite_id1`: representerer ID-en til testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **er** angitt. Denne ID-en er Azure DevOps-ID-en for testserien.
+ `test_suite_idN`: representerer ID-en til testverktøyet. Denne parameteren er nødvendig hvis /byid-bryteren **er** angitt. Denne ID-en er Azure DevOps-ID-en for testserien.

##### <a name="playbacksuite-examples"></a>playbacksuite: eksempler

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Kjører alle testsaker i den angitte Azure DevOps-testserien.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: valgfrie brytere

+ `/retry[=seconds]`: Hvis denne bryteren er angitt, og testtilfeller er blokkert av andre RSAT-forekomster, vil avspillingsprosessen vente det angitte antallet sekunder og deretter prøve en gang til. Standardverdien for \[seconds\] er 120 sekunder. Uten denne bryteren avbrytes prosessen umiddelbart hvis testtilfeller er blokkert.
+ `/comments[="comment"]`: Angi en egendefinert informasjonsstreng som skal tas med i **Kommentarer**-feltet på sammendrags- og testresultatsidene for Azure DevOps-testtilfelleskjøringer.
+ `/byid`: Denne bryteren angir at den ønskede testserien identifiseres av dens Azure DevOps-ID i stedet for navnet på testserien.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: nødvendige parametere

+ `test_suite_id`: Representerer ID-en til testserien slik den eksisterer i Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: eksempler

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Lukker appen. Denne kommandoen er bare nyttig når appene kjører i interaktiv modus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: eksempler

`quit`

#### <a name="upload"></a>upload

Laster opp vedleggsfiler (registrering, kjøring og parameterfiler) som tilhører en angitt testserie eller testtilfeller, til Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: nødvendige parametere

+ `test_suite_name`: Alle filer som tilhører den angitte testserien, lastes opp.
+ `test_case_id1`: Representerer ID-en til den første testsaken som skal lastes opp. Bruk denne parameteren bare når det ikke er angitt noe navn på testserien.
+ `test_case_idN`: Representerer ID-en til den siste testsaken som skal lastes opp. Bruk denne parameteren bare når det ikke er angitt noe navn på testserien.

##### <a name="upload-examples"></a>upload: eksempler

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Laster opp bare opptaksfilen som tilhører en eller flere angitte testsaker, til Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: nødvendige parametere

+ `test_case_id1`: Representerer ID-en til den første testsaken for opptaket som skal lastes opp til Azure DevOps.
+ `test_case_idN`: Representerer ID-en til den siste testsaken for opptaket som skal lastes opp til Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: eksempler

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Viser de tre bruksmodusene for denne appen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Interaktiv kjøring av appen:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Kjøring av appen ved å angi en kommando:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Kjøring av appen ved å angi en innstillingsfil:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Windows PowerShell-eksempler

#### <a name="run-a-test-case-in-a-loop"></a>Kjøre et testtilfelle i en løkke

Du har et testskript som oppretter en ny kunde. Du kan kjøre dette testtilfellet i en løkke via skripting ved randomisere følgende data før hver gjentakelse kjøres:

- Kunde-ID
- Kundenavn
- Kundeadresse

Kunde-ID-en er i formatet *ATCUS\<number\>*, der \<number\> er en verdi mellom **000000001** og **999999999**.

I det følgende eksemplet brukes én parameter, **start**, til å definere det første nummeret som brukes. Det bruker en andre parameter, **nr**, til å definere antallet kunder som må opprettes. For hver gjentakelse endres parameterne i Excel-parameterfilen ved hjelp av en UpdateCustomer-funksjon. Deretter kalles RSAT-kommandolinjen i en RunTestCase-funksjon.

Åpne Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i administratormodus, og lim inn følgende kode i vinduet kalt **Untitled1.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Kjør et skript som er avhengig av data i Microsoft Dynamics 365

Det følgende eksemplet bruker et OData-kall (Open Data Protocol) til å finne ordrestatusen for en bestilling. Hvis statusen ikke er **fakturert**, kan du for eksempel kalle et RSAT-testtilfelle som posterer fakturaen.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
