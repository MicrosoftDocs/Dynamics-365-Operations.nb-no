---
title: Bruke opplæringen for Regression Suite Automation Tool
description: Dette emnet viser hvordan du bruker Regression Suite Automation Tool (RSAT). Det beskriver ulike funksjoner og gir eksempler som omfatter avansert skripting.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070826"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Bruke opplæringen for Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format. 

Denne opplæringen går gjennom noen av de avanserte funksjonene i Regression Suite Automation Tool (RSAT), inneholder en demonstrasjonsoppgave og beskriver strategier og ting som er viktig å lære.

## <a name="features-of-rsattask-recorder"></a>Funksjoner i RSAT/Oppgaveopptaker

### <a name="validate-a-field-value"></a>Valider en feltverdi

Hvis du vil ha informasjon om denne funksjonen, kan du se [Opprette et nytt oppgaveopptak som har en valideringsfunksjon](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Lagret variabel

Hvis du vil ha informasjon om denne funksjonen, kan du se [Endre et eksisterende oppgaveopptak for å opprette en lagret variabel](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Avledet testtilfelle

1. Åpne Regression Suite Automation Tool (RSAT), og velg begge testtilfellene du opprettet i [Opplæring i installasjon og konfigurasjon av Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).
2. Velg **Ny \> Opprett avledet testtilfelle**.

    ![Kommandoen Opprett avledet testtilfelle på Ny-menyen](./media/use_rsa_tool_01.png)

3. Du får en melding om at en avledet test opprettes for hvert valgte testtilfelle i gjeldende testserie, og at hvert avledede testtilfelle har ha en egen kopi av Excel-parameterfilen. Velg **OK**.

    > [!NOTE]
    > Når du kjører et avledet testtilfelle, bruker det oppgaveopptaket for det overordnede testtilfellet og sin egen kopi av Excel-parameterfilen. På denne måten kan du kjøre den samme testen med ulike parametere, uten å måtte ta vare på flere enn ett oppgaveopptak. Et avledet testtilfelle kan ikke være en del av den samme testserien som det overordnede testtilfellet.

    ![Meldingsboks](./media/use_rsa_tool_02.png)

    Det opprettes to ytterligere testtilfeller, og det er merket av for **Avledet?** ved siden av dem.

    ![Avledede testtilfeller opprettet](./media/use_rsa_tool_03.png)

    Et avledet testtilfelle opprettes automatisk i Azure DevOps. Det er et underordnet element for testtilfellet **Opprett et nytt produkt** og er merket med et spesielt nøkkelord: **RSAT:DerivedTestSteps**. Disse testtilfellene blir også automatisk lagt til i testplanen i Azure DevOps.

    ![Nøkkelordet RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Hvis de avledede testtilfellene som opprettes, av en eller annen årsak ikke er i riktig rekkefølge, går du til Azure DevOps og endrer rekkefølgen på testtilfellene i testserien, slik at RSAT kan kjøre dem i riktig rekkefølge.

4. Velg de avledede testtilfellene, og velg deretter **Rediger** for å åpne de tilsvarende Excel-parameterfilene.
5. Rediger disse Excel-parameterfilene på samme måte som du redigerte de overordnede filene. Du må med andre ord passe på at produkt-ID-en er satt slik at den genereres automatisk. Kontroller også at den lagrede variabelen kopieres til de relevante feltene.
6. Oppdater verdien i **Firma**-feltet til **USSI** i **Generelt**-fanen for begge Excel-parameterfilene, slik at de avledede testtilfellene kjøres mot en annen juridisk enhet enn det overordnede testtilfellet. Hvis du vil kjøre testtilfellen mot en bestemt bruker (eller rollen som er knyttet til en bestemt bruker), kan du oppdatere verdien i **Testbruker**-feltet.
7. Velg **Kjør**, og valider at produktet er opprettet i begge de juridiske enhetene USMF og USSI.

### <a name="validate-notifications"></a>Validere varslinger

Denne funksjonen kan brukes til å validere om en handling er utført. Når en produksjonsordre for eksempel opprettes, estimeres og deretter startes, viser appen meldingen "Produksjon – start" for å varsle deg om at produksjonsordren er startet.

![Varslingen Produksjon – start](./media/use_rsa_tool_05.png)

Du kan validere denne meldingen via RSAT ved å angi meldingsteksten i fanen **Meldingsvalidering** i Excel-parameterfilen for det aktuelle opptaket.

![Fanen Meldingsvalidering](./media/use_rsa_tool_06.png)

Etter at testtilfellet er kjørt, sammenlignes meldingen i Excel-parameterfilen med meldingen som vises. Hvis meldingene ikke samsvarer, mislykkes testtilfellet.

> [!NOTE]
> Du kan angi flere meldinger i fanen **Meldingsvalidering** i Excel-parameterfilen. Meldingene kan også være feilmeldinger eller advarsler i stedet for informasjonsmeldinger.

### <a name="validate-values-by-using-operators"></a>Validere verdier ved hjelp av operatorer

I tidligere versjoner av RSAT kunne du bare validere verdier hvis en kontrollverdi var lik en forventet verdi. Med den nye funksjonen kan du validere at en variabel ikke er lik, er mindre enn eller er større enn en bestemt verdi.

- Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien i følgende element fra **false** til **true**.

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    I Excel-parameterfilen vises et nytt **Operator**-felt.

    > [!NOTE]
    > Hvis du har brukt en eldre versjon av RSAT, må du generere nye Excel-parameterfiler.

    ![Operator-feltet](./media/use_rsa_tool_07.png)

Følgende eksempel viser hvordan du kan bruke denne funksjonen til å validere om lagerbeholdningen er større enn 0 (null).

1. I demonstrasjonsdataene i firmaet **USMF** oppretter du et oppgaveopptak som har følgende trinn:

    1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
    2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på verdien **1000** for **Varenummer**-feltet.
    3. Velg **Lagerbeholdning**.
    4. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på verdien **1** for **Område**-feltet.
    5. Merk den valgte raden i listen.
    6. Valider at verdien i feltet **Totalt tilgjengelig** er **411,0000000000000000**.

2. Lagre oppgaveopptaket i BPM-biblioteket i LCS, og synkroniser det med Azure DevOps.
3. Legg til testtilfellet i testplanen, og last inn testtilfellet i RSAT.
4. Åpne Excel-parameterfilen. I fanen **InventOnhandItem** vises delen **Valider InventOnhandItem** som omfatter et **Operator**-felt.

    ![Operator-feltet](./media/use_rsa_tool_08.png)

5. Du kan validere om lagerbeholdningen alltid er større enn 0, ved å endre verdien i **Verdi**-feltet fra **411** til **0** og verdien i **Operator**-feltet fra et likhetstegn (**=**) til et større enn-tegn (**\>**).

    ![Verdiene i feltene Verdi og Operator er endret](./media/use_rsa_tool_09.png)

6. Lagre og lukk Excel-parameterfilen.
7. Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen, i Azure DevOps.

Hvis verdien i feltet **Totalt tilgjengelig** for den angitte varen i beholdningen er større enn 0 (null), blir testene bestått, uavhengig av den faktiske verdien for lagerbeholdningen.

### <a name="generator-logs"></a>Generatorlogger

Denne funksjonen oppretter en mappe som inneholder loggene for testtilfellene som er kjørt.

- Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien i følgende element fra **false** til **true**.

    ```xml
    <add key="LogGeneration" value="false" />
    ```

Etter at testtilfellene er kjørt, kan du finne loggfilene under **C:\\Brukere\\\<Brukernavn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Mappen GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Hvis det fantes eksisterende testtilfeller før du endret verdien i .config-filen, blir det ikke generert logger for disse testtilfellene før du har generert nye testutførelsesfiler.
> 
> ![Kommandoen Generer bare testutførelsesfiler på Ny-menyen](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Øyeblikksbilde

Denne funksjonen tar skjermbilder av trinnene som ble utført under oppgaveopptaket.

- Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien for følgende element fra **false** til **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Det opprettes en separat mappe under **C:\\Brukere\\\<Brukernavn\>\\AppData\\Roaming\\regressionTool\\playback** for hvert testtilfelle som kjøres.

![Øyeblikksbildemappe for et testtilfelle](./media/use_rsa_tool_12.png)

I hver av disse mappene kan du finne øyeblikksbilder av trinnene som ble utført mens testtilfellene ble kjørt.

![Øyeblikksbildefiler](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>Oppgave

### <a name="scenario"></a>Scenario

1. Produktdesigneren oppretter et nytt frigitt produkt.
2. Produksjonssjefen starter en produksjonsordre for å bringe lagernivået til to stykker.
3. Produksjonen starter og avslutter produksjonsordren og kontrollerer at beholdningsantallet er to stykker.
4. Salgsteamet mottar en ordre på fire stykker av det nye produktet. Salgsteamet oppdaterer derfor nettobehovet via den dynamiske planen. Siden det ikke finnes mer kapasitet, settes standard ordrepolicy til «kjøp i stedet for å lage». Det opprettes derfor et bestillingsforslag.
5. Innkjøperen legger til en leverandør, autoriserer bestillingsforslaget og bekrefter deretter bestillingen.
6. Når varene som ble kjøpt, ankommer i butikken, søker butikkoperatøren etter den tilknyttede bestillingen og mottar varene. Siden ordren nå er fullført, kan varene plukkes og pakkes mot salgsordren.
7. Finans posterer innkjøpsfakturaen og salgsfakturaen.

Illustrasjonen nedenfor viser flyten for dette scenariet.

![Flyt for demonstrasjonsscenariet](./media/use_rsa_tool_14.png)

Illustrasjonen nedenfor viser forretningsprosessene for dette scenariet i RSAT.

![Forretningsprosesser for demonstrasjonsscenariet](./media/use_rsa_tool_15.png)

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
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>? 
Viser hjelp om alle tilgjengelige kommandoer og deres parametere.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a>Valgfrie parametere

**``command``**


Der ``[command]`` er en av kommandoene angitt nedenfor.


#### <a name="about"></a>about
Viser gjeldende versjon.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls
Tømmer skjermen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a>last ned
Laster ned vedlegg for den angitte testsaken til utdatamappen. Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker. Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``test_case_id``** representerer ID-en til testsaken.  
**``output_dir``** representerer utdatamappen. Katalogen må finnes.

##### <a name="examples"></a>Eksempler

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a>rediger
Lar deg åpne parameterfilen i Excel-programmet og redigere den.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``excel_file``** må inneholde en fullstendig bane til en eksisterende Excel-fil.

##### <a name="examples"></a>Eksempler
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a>generate
Genererer testkjøring og parameterfiler for den angitte testsaken i utdatamappen.
Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker. Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``test_case_id``** representerer ID-en til testsaken.  
**``output_dir``** representerer utdatamappen. Katalogen må finnes.

##### <a name="examples"></a>Eksempler
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a>generatederived
Genererer en ny testsak, avledet fra den angitte testsaken. Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker. Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``parent_test_case_id``** representerer ID-en til den overordnede testsaken.  
**``test_plan_id``** representerer ID-en til testplanen.  
**``test_suite_id``** representerer ID-en til testverktøyet.

##### <a name="examples"></a>Eksempler
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a>generatetestonly
Genererer bare testkjøringsfil for den angitte testsaken i utdatamappen. Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker. Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``test_case_id``** representerer ID-en til testsaken.  
**``output_dir``** representerer utdatamappen. Katalogen må finnes.

##### <a name="examples"></a>Eksempler
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a>generatetestsuite
Genererer alle testsaker for det angitte verktøyet i utdatamappen.
Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy. Bruk en verdi fra kolonnen som en **test_suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``test_suite_name``** representerer navnet til testverktøyet.  
**``output_dir``** representerer utdatamappen. Katalogen må finnes.

##### <a name="examples"></a>Eksempler
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a>help
Identisk med [?](####?)- kommandoen


#### <a name="list"></a>listen
Viser alle tilgjengelige testsaker.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a>listtestplans
Viser alle tilgjengelige testplaner.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a>listtestsuite
Viser testsaker for det angitte testverktøyet. Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy. Bruk en verdi fra den første kolonnen som en **suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``suite_name``** navnet på det ønskede verktøyet.

##### <a name="examples"></a>Eksempler
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a>listtestsuitenames
Viser alle tilgjengelige testverktøy.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a>playback
Spiller av en testsak ved hjelp av en Excel-fil.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``excel_file``** en fullstendig bane til Excel-filen. Filen må finnes. 

##### <a name="examples"></a>Eksempler
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a>playbackbyid
Spiller av flere testsaker samtidig.
Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker. Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``test_case_id1``** ID for eksisterende testsak.  
**``test_case_id2``** ID for eksisterende testsak.  
**``test_case_idN``** ID for eksisterende testsak.  

##### <a name="examples"></a>Eksempler
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a>playbackmany
Spiller av mange testsaker samtidig ved hjelp av Excel-filer.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``excel_file1``** fullstendig bane til Excel-filen. Filen må finnes.  
**``excel_file2``** fullstendig bane til Excel-filen. Filen må finnes.  
**``excel_fileN``** fullstendig bane til Excel-filen. Filen må finnes.  

##### <a name="examples"></a>Eksempler
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a>playbacksuite
Spiller av alle testsaker fra det angitte testverktøyet. Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy. Bruk en verdi fra den første kolonnen som en **suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``suite_name``** navnet på det ønskede verktøyet.

##### <a name="examples"></a>Eksempler
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a>quit
Lukker appen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a>upload
Laster opp alle filer som hører til angitt testverktøy eller testsaker.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a>Obligatoriske parametere
**``suite_name``** alle filer som hører til angitt testverktøy, lastes opp.
**``testcase_id``** alle filer som hører til angitte testsaker, lastes opp.

##### <a name="examples"></a>Eksempler
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a>uploadrecording
Laster opp bare opptaksfilen som hører til angitte testsaker.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a>Obligatoriske parametere
**``testcase_id``** opptaksfilen som hører til angitte testsaker, lastes opp.

##### <a name="examples"></a>Eksempler
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a>usage
Viser to måter å aktivere dette programmet på: én som bruker en standard innstillingsfil, en annen som angir en innstillingsfil.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a>Windows PowerShell-eksempler

#### <a name="run-a-test-case-in-a-loop"></a>Kjøre et testtilfelle i en løkke

Du har et testskript som oppretter en ny kunde. Du kan kjøre dette testtilfellet i en løkke via skripting ved randomisere følgende data før hver gjentakelse kjøres:

- Kunde-ID
- Kundenavn
- Kundeadresse

Kunde-ID-en er i formatet *ATCUS\<nummer\>*, der \<nummer\> er en verdi mellom **000000001** og **999999999**.

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
$excelFilename = "full path to excel file parameter file"
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

```xpp
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
