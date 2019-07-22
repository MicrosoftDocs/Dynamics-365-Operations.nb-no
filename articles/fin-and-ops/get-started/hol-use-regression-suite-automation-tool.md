---
title: Bruke opplæring for Regression Suite Automation Tool
description: Dette emnet viser hvordan du bruker Regression Suite Automation Tool (RSAT). Det beskriver ulike funksjoner og gir eksempler som omfatter avansert skripting.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 8f3cd6a27ba0e09e48c0562aff46791228bb46b5
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703858"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="77d86-104">Bruke opplæringen for Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="77d86-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="77d86-105">Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="77d86-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="77d86-106">Denne opplæringen går gjennom noen av de avanserte funksjonene i Regression Suite Automation Tool (RSAT), inneholder en demonstrasjonsoppgave og beskriver strategier og ting som er viktig å lære.</span><span class="sxs-lookup"><span data-stu-id="77d86-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="77d86-107">Funksjoner i RSAT/Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="77d86-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="77d86-108">Valider en feltverdi</span><span class="sxs-lookup"><span data-stu-id="77d86-108">Validate a field value</span></span>

<span data-ttu-id="77d86-109">Hvis du vil ha informasjon om denne funksjonen, kan du se [Opprette et nytt oppgaveopptak som har en valideringsfunksjon](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="77d86-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="77d86-110">Lagret variabel</span><span class="sxs-lookup"><span data-stu-id="77d86-110">Saved variable</span></span>

<span data-ttu-id="77d86-111">Hvis du vil ha informasjon om denne funksjonen, kan du se [Endre et eksisterende oppgaveopptak for å opprette en lagret variabel](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="77d86-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="77d86-112">Avledet testtilfelle</span><span class="sxs-lookup"><span data-stu-id="77d86-112">Derived test case</span></span>

1. <span data-ttu-id="77d86-113">Åpne Regression Suite Automation Tool (RSAT), og velg begge testtilfellene du opprettet i [Installasjon og konfigurasjon av Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="77d86-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="77d86-114">Velg **Ny \> Opprett avledet testtilfelle**.</span><span class="sxs-lookup"><span data-stu-id="77d86-114">Select **New \> Create derived test case**.</span></span>

    ![Kommandoen Opprett avledet testtilfelle på Ny-menyen](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="77d86-116">Du får en melding om at en avledet test opprettes for hvert valgte testtilfelle i gjeldende testserie, og at hvert avledede testtilfelle har ha en egen kopi av Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="77d86-117">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="77d86-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="77d86-118">Når du kjører et avledet testtilfelle, bruker det oppgaveopptaket for det overordnede testtilfellet og sin egen kopi av Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="77d86-119">På denne måten kan du kjøre den samme testen med ulike parametere, uten å måtte ta vare på flere enn ett oppgaveopptak.</span><span class="sxs-lookup"><span data-stu-id="77d86-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="77d86-120">Et avledet testtilfelle kan ikke være en del av den samme testserien som det overordnede testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="77d86-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Meldingsboks](./media/use_rsa_tool_02.png)

    <span data-ttu-id="77d86-122">Det opprettes to ytterligere testtilfeller, og det er merket av for **Avledet?** ved siden av dem.</span><span class="sxs-lookup"><span data-stu-id="77d86-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Avledede testtilfeller opprettet](./media/use_rsa_tool_03.png)

    <span data-ttu-id="77d86-124">Et avledet testtilfelle opprettes automatisk i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="77d86-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="77d86-125">Det er et underordnet element for testtilfellet **Opprett et nytt produkt** og er merket med et spesielt nøkkelord: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="77d86-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="77d86-126">Disse testtilfellene blir også automatisk lagt til i testplanen i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="77d86-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Nøkkelordet RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="77d86-128">Hvis de avledede testtilfellene som opprettes, av en eller annen årsak ikke er i riktig rekkefølge, går du til Azure DevOps og endrer rekkefølgen på testtilfellene i testserien, slik at RSAT kan kjøre dem i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="77d86-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="77d86-129">Velg de avledede testtilfellene, og velg deretter **Rediger** for å åpne de tilsvarende Excel-parameterfilene.</span><span class="sxs-lookup"><span data-stu-id="77d86-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="77d86-130">Rediger disse Excel-parameterfilene på samme måte som du redigerte de overordnede filene.</span><span class="sxs-lookup"><span data-stu-id="77d86-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="77d86-131">Du må med andre ord passe på at produkt-ID-en er satt slik at den genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="77d86-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="77d86-132">Kontroller også at den lagrede variabelen kopieres til de relevante feltene.</span><span class="sxs-lookup"><span data-stu-id="77d86-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="77d86-133">Oppdater verdien i **Firma**-feltet til **USSI** i **Generelt**-fanen for begge Excel-parameterfilene, slik at de avledede testtilfellene kjøres mot en annen juridisk enhet enn det overordnede testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="77d86-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="77d86-134">Hvis du vil kjøre testtilfellen mot en bestemt bruker (eller rollen som er knyttet til en bestemt bruker), kan du oppdatere verdien i **Testbruker**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77d86-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="77d86-135">Velg **Kjør**, og valider at produktet er opprettet i begge de juridiske enhetene USMF og USSI.</span><span class="sxs-lookup"><span data-stu-id="77d86-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="77d86-136">Validere varslinger</span><span class="sxs-lookup"><span data-stu-id="77d86-136">Validate notifications</span></span>

<span data-ttu-id="77d86-137">Denne funksjonen kan brukes til å validere om en handling er utført.</span><span class="sxs-lookup"><span data-stu-id="77d86-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="77d86-138">Når en produksjonsordre for eksempel opprettes, estimeres og deretter startes, viser Microsoft Dynamics 365 for Finance and Operations meldingen "Produksjon – start" for å varsle deg om at produksjonsordren er startet.</span><span class="sxs-lookup"><span data-stu-id="77d86-138">For example, when a production order is created, estimated, and then started, Microsoft Dynamics 365 for Finance and Operations shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Varslingen Produksjon – start](./media/use_rsa_tool_05.png)

<span data-ttu-id="77d86-140">Du kan validere denne meldingen via RSAT ved å angi meldingsteksten i fanen **Meldingsvalidering** i Excel-parameterfilen for det aktuelle opptaket.</span><span class="sxs-lookup"><span data-stu-id="77d86-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Fanen Meldingsvalidering](./media/use_rsa_tool_06.png)

<span data-ttu-id="77d86-142">Etter at testtilfellet er kjørt, sammenlignes meldingen i Excel-parameterfilen med meldingen som vises i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="77d86-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown in Finance and Operations.</span></span> <span data-ttu-id="77d86-143">Hvis meldingene ikke samsvarer, mislykkes testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="77d86-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="77d86-144">Du kan angi flere meldinger i fanen **Meldingsvalidering** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="77d86-145">Meldingene kan også være feilmeldinger eller advarsler i stedet for informasjonsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="77d86-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="77d86-146">Validere verdier ved hjelp av operatorer</span><span class="sxs-lookup"><span data-stu-id="77d86-146">Validate values by using operators</span></span>

<span data-ttu-id="77d86-147">I tidligere versjoner av RSAT kunne du bare validere verdier hvis en kontrollverdi var lik en forventet verdi.</span><span class="sxs-lookup"><span data-stu-id="77d86-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="77d86-148">Med den nye funksjonen kan du validere at en variabel ikke er lik, er mindre enn eller er større enn en bestemt verdi.</span><span class="sxs-lookup"><span data-stu-id="77d86-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="77d86-149">Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien i følgende element fra **false** til **true**.</span><span class="sxs-lookup"><span data-stu-id="77d86-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="77d86-150">I Excel-parameterfilen vises et nytt **Operator**-felt.</span><span class="sxs-lookup"><span data-stu-id="77d86-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="77d86-151">Hvis du har brukt en eldre versjon av RSAT, må du generere nye Excel-parameterfiler.</span><span class="sxs-lookup"><span data-stu-id="77d86-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Operator-feltet](./media/use_rsa_tool_07.png)

<span data-ttu-id="77d86-153">Følgende eksempel viser hvordan du kan bruke denne funksjonen til å validere om lagerbeholdningen er større enn 0 (null).</span><span class="sxs-lookup"><span data-stu-id="77d86-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="77d86-154">I demonstrasjonsdataene i firmaet **USMF** oppretter du et oppgaveopptak som har følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="77d86-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="77d86-155">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="77d86-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="77d86-156">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="77d86-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="77d86-157">Du kan for eksempel filtrere på verdien **1000** for **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77d86-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="77d86-158">Velg **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="77d86-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="77d86-159">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="77d86-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="77d86-160">Du kan for eksempel filtrere på verdien **1** for **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77d86-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="77d86-161">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="77d86-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="77d86-162">Valider at verdien i feltet **Totalt tilgjengelig** er **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="77d86-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="77d86-163">Lagre oppgaveopptaket i BPM-biblioteket i LCS, og synkroniser det med Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="77d86-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="77d86-164">Legg til testtilfellet i testplanen, og last inn testtilfellet i RSAT.</span><span class="sxs-lookup"><span data-stu-id="77d86-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="77d86-165">Åpne Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-165">Open the Excel parameter file.</span></span> <span data-ttu-id="77d86-166">I fanen **InventOnhandItem** vises delen **Valider InventOnhandItem** som omfatter et **Operator**-felt.</span><span class="sxs-lookup"><span data-stu-id="77d86-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operator-feltet](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="77d86-168">Du kan validere om lagerbeholdningen alltid er større enn 0, ved å endre verdien i **Verdi**-feltet fra **411** til **0** og verdien i **Operator**-feltet fra et likhetstegn (**=**) til et større enn-tegn (**\>**).</span><span class="sxs-lookup"><span data-stu-id="77d86-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Verdiene i feltene Verdi og Operator er endret](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="77d86-170">Lagre og lukk Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="77d86-171">Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen, i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="77d86-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="77d86-172">Hvis verdien i feltet **Totalt tilgjengelig** for den angitte varen i beholdningen er større enn 0 (null), blir testene bestått, uavhengig av den faktiske verdien for lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="77d86-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="77d86-173">Generatorlogger</span><span class="sxs-lookup"><span data-stu-id="77d86-173">Generator logs</span></span>

<span data-ttu-id="77d86-174">Denne funksjonen oppretter en mappe som inneholder loggene for testtilfellene som er kjørt.</span><span class="sxs-lookup"><span data-stu-id="77d86-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="77d86-175">Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien i følgende element fra **false** til **true**.</span><span class="sxs-lookup"><span data-stu-id="77d86-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="77d86-176">Etter at testtilfellene er kjørt, kan du finne loggfilene under **C:\\Brukere\\\<Brukernavn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="77d86-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Mappen GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="77d86-178">Hvis det fantes eksisterende testtilfeller før du endret verdien i .config-filen, blir det ikke generert logger for disse testtilfellene før du har generert nye testutførelsesfiler.</span><span class="sxs-lookup"><span data-stu-id="77d86-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Kommandoen Generer bare testutførelsesfiler på Ny-menyen](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="77d86-180">Øyeblikksbilde</span><span class="sxs-lookup"><span data-stu-id="77d86-180">Snapshot</span></span>

<span data-ttu-id="77d86-181">Denne funksjonen tar skjermbilder av trinnene som ble utført under oppgaveopptaket.</span><span class="sxs-lookup"><span data-stu-id="77d86-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="77d86-182">Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien for følgende element fra **false** til **true**.</span><span class="sxs-lookup"><span data-stu-id="77d86-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="77d86-183">Det opprettes en separat mappe under **C:\\Brukere\\\<Brukernavn\>\\AppData\\Roaming\\regressionTool\\playback** for hvert testtilfelle som kjøres.</span><span class="sxs-lookup"><span data-stu-id="77d86-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Øyeblikksbildemappe for et testtilfelle](./media/use_rsa_tool_12.png)

<span data-ttu-id="77d86-185">I hver av disse mappene kan du finne øyeblikksbilder av trinnene som ble utført mens testtilfellene ble kjørt.</span><span class="sxs-lookup"><span data-stu-id="77d86-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Øyeblikksbildefiler](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="77d86-187">Oppgave</span><span class="sxs-lookup"><span data-stu-id="77d86-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="77d86-188">Scenario</span><span class="sxs-lookup"><span data-stu-id="77d86-188">Scenario</span></span>

1. <span data-ttu-id="77d86-189">Produktdesigneren oppretter et nytt frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="77d86-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="77d86-190">Produksjonssjefen starter en produksjonsordre for å bringe lagernivået til to stykker.</span><span class="sxs-lookup"><span data-stu-id="77d86-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="77d86-191">Produksjonen starter og avslutter produksjonsordren og kontrollerer at beholdningsantallet er to stykker.</span><span class="sxs-lookup"><span data-stu-id="77d86-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="77d86-192">Salgsteamet mottar en ordre på fire stykker av det nye produktet.</span><span class="sxs-lookup"><span data-stu-id="77d86-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="77d86-193">Salgsteamet oppdaterer derfor nettobehovet via den dynamiske planen.</span><span class="sxs-lookup"><span data-stu-id="77d86-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="77d86-194">Siden det ikke finnes mer kapasitet, settes standard ordrepolicy til «kjøp i stedet for å lage».</span><span class="sxs-lookup"><span data-stu-id="77d86-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="77d86-195">Det opprettes derfor et bestillingsforslag.</span><span class="sxs-lookup"><span data-stu-id="77d86-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="77d86-196">Innkjøperen legger til en leverandør, autoriserer bestillingsforslaget og bekrefter deretter bestillingen.</span><span class="sxs-lookup"><span data-stu-id="77d86-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="77d86-197">Når varene som ble kjøpt, ankommer i butikken, søker butikkoperatøren etter den tilknyttede bestillingen og mottar varene.</span><span class="sxs-lookup"><span data-stu-id="77d86-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="77d86-198">Siden ordren nå er fullført, kan varene plukkes og pakkes mot salgsordren.</span><span class="sxs-lookup"><span data-stu-id="77d86-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="77d86-199">Finans posterer innkjøpsfakturaen og salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="77d86-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="77d86-200">Illustrasjonen nedenfor viser flyten for dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="77d86-200">The following illustration shows the flow for this scenario.</span></span>

![Flyt for demonstrasjonsscenariet](./media/use_rsa_tool_14.png)

<span data-ttu-id="77d86-202">Illustrasjonen nedenfor viser forretningsprosessene for dette scenariet i RSAT.</span><span class="sxs-lookup"><span data-stu-id="77d86-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Forretningsprosesser for demonstrasjonsscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="77d86-204">Strategi – viktige punkt</span><span class="sxs-lookup"><span data-stu-id="77d86-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="77d86-205">Data</span><span class="sxs-lookup"><span data-stu-id="77d86-205">Data</span></span>

- <span data-ttu-id="77d86-206">Sørg for at du har representative datavolumer (en kopi av konfigurasjonsdata for produksjon / gylne konfigurasjonsdata pluss overførte data).</span><span class="sxs-lookup"><span data-stu-id="77d86-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="77d86-207">Når du genererer nye data via Oppgaveopptaker, oppretter du testnavn som ikke kommer i konflikt med eksisterende navn (for eksempel ved å bruke et prefiks som **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="77d86-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="77d86-208">Bruk tidsgjenoppretting av database for Azure til å kjøre tester på nytt i andre miljøer enn Lag 1-miljøer.</span><span class="sxs-lookup"><span data-stu-id="77d86-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="77d86-209">Selv om du kan bruke Excel-funksjonene **TILFELDIG** og **NÅ** til å generere en unik kombinasjon, er det langt fra lettvint.</span><span class="sxs-lookup"><span data-stu-id="77d86-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="77d86-210">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="77d86-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="77d86-211">Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="77d86-211">Task recorder</span></span>

- <span data-ttu-id="77d86-212">Definer scenarier før du starter opptaket.</span><span class="sxs-lookup"><span data-stu-id="77d86-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="77d86-213">Et velstyrt prosjekt har forhåndsdefinerte testscenarier.</span><span class="sxs-lookup"><span data-stu-id="77d86-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="77d86-214">Når du skal bygge et testtilfelle, vurderer du hvor forutsigbart resultatet av testscenariene er.</span><span class="sxs-lookup"><span data-stu-id="77d86-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="77d86-215">Del opp opptak hvis de skal utføres av ulike roller, eller hvis det er ventetid eller en ekstern hendelse før neste trinn.</span><span class="sxs-lookup"><span data-stu-id="77d86-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="77d86-216">Unngå å velge verdier i lister.</span><span class="sxs-lookup"><span data-stu-id="77d86-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="77d86-217">Bruk i stedet tekstformater, for eksempel **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="77d86-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="77d86-218">Når du velger i en liste, blir posisjonen til verdien i listen tatt opp, ikke selve verdien.</span><span class="sxs-lookup"><span data-stu-id="77d86-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="77d86-219">Hvis elementer blir lagt til i denne listen, kan posisjonen til verdien bli endret.</span><span class="sxs-lookup"><span data-stu-id="77d86-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="77d86-220">Derfor bruker opptaket en annen parameter, og resten av scenariet kan bli påvirket.</span><span class="sxs-lookup"><span data-stu-id="77d86-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="77d86-221">Tenk på flerbrukerfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="77d86-221">Think about multi-user behavior.</span></span> <span data-ttu-id="77d86-222">Du kan for eksempel ikke ta for gitt at den nyopprettede salgsordren alltid velges automatisk.</span><span class="sxs-lookup"><span data-stu-id="77d86-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="77d86-223">Bruk i stedet alltid filteret til å finne riktig ordre.</span><span class="sxs-lookup"><span data-stu-id="77d86-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="77d86-224">Bruk Kopier-funksjonen i Oppgaveopptaker til å lagre navnet på et nyopprettet produkt, slik at det kan brukes i kjedede testtilfeller.</span><span class="sxs-lookup"><span data-stu-id="77d86-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="77d86-225">Bruk Valider-funksjonen i Oppgaveopptaker til å angi kontrollpunkt som kontrollerer at trinn er kjørt på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="77d86-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="77d86-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="77d86-226">RSAT</span></span>

- <span data-ttu-id="77d86-227">Hvis du vil kjøre testen i et annet firma, kan du endre firmaet i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="77d86-228">Sørg for at innstillingene og dataene er tilgjengelige i det nylig valgte firmaet.</span><span class="sxs-lookup"><span data-stu-id="77d86-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="77d86-229">Du kan endre testbrukeren i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="77d86-230">Angi e-post-ID-en til brukeren som skal kjøre testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="77d86-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="77d86-231">På denne måten kan testtilfellet kjøres ved hjelp av sikkerhetstillatelsene til den angitte brukeren.</span><span class="sxs-lookup"><span data-stu-id="77d86-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="77d86-232">Hvis du vil vente før testen startes, kan du definere en pause i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="77d86-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="77d86-233">Pausen kan brukes i en satsvis jobb (for eksempel hvis en arbeidsflyt må kjøres før neste trinn kan utføres).</span><span class="sxs-lookup"><span data-stu-id="77d86-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="77d86-234">Avansert skripting</span><span class="sxs-lookup"><span data-stu-id="77d86-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="77d86-235">Kommandolinje</span><span class="sxs-lookup"><span data-stu-id="77d86-235">Command line</span></span>

<span data-ttu-id="77d86-236">RSAT kan kalles fra et **ledetekstvindu**.</span><span class="sxs-lookup"><span data-stu-id="77d86-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="77d86-237">Kontroller at miljøvariabelen **TestRoot** er satt til RSAT-installasjonsbanen.</span><span class="sxs-lookup"><span data-stu-id="77d86-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="77d86-238">(I Microsoft Windows åpner du **Kontrollpanel**, velger **System og sikkerhet \> System \> Avanserte systeminnstillinger** og deretter **Miljøvariabler**.)</span><span class="sxs-lookup"><span data-stu-id="77d86-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="77d86-239">Åpne et **ledetekstvindu** som administrator.</span><span class="sxs-lookup"><span data-stu-id="77d86-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="77d86-240">Kjør verktøyet fra installasjonskatalogen.</span><span class="sxs-lookup"><span data-stu-id="77d86-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="77d86-241">Vis alle kommandoer.</span><span class="sxs-lookup"><span data-stu-id="77d86-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="77d86-242">Windows PowerShell-eksempler</span><span class="sxs-lookup"><span data-stu-id="77d86-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="77d86-243">Kjøre et testtilfelle i en løkke</span><span class="sxs-lookup"><span data-stu-id="77d86-243">Run a test case in a loop</span></span>

<span data-ttu-id="77d86-244">Du har et testskript som oppretter en ny kunde.</span><span class="sxs-lookup"><span data-stu-id="77d86-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="77d86-245">Du kan kjøre dette testtilfellet i en løkke via skripting ved randomisere følgende data før hver gjentakelse kjøres:</span><span class="sxs-lookup"><span data-stu-id="77d86-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="77d86-246">Kunde-ID</span><span class="sxs-lookup"><span data-stu-id="77d86-246">Customer ID</span></span>
- <span data-ttu-id="77d86-247">Kundenavn</span><span class="sxs-lookup"><span data-stu-id="77d86-247">Customer name</span></span>
- <span data-ttu-id="77d86-248">Kundeadresse</span><span class="sxs-lookup"><span data-stu-id="77d86-248">Customer address</span></span>

<span data-ttu-id="77d86-249">Kunde-ID-en er i formatet *ATCUS\<nummer\>*, der \<nummer\> er en verdi mellom **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="77d86-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="77d86-250">I det følgende eksemplet brukes én parameter, **start**, til å definere det første nummeret som brukes.</span><span class="sxs-lookup"><span data-stu-id="77d86-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="77d86-251">Det bruker en andre parameter, **nr**, til å definere antallet kunder som må opprettes.</span><span class="sxs-lookup"><span data-stu-id="77d86-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="77d86-252">For hver gjentakelse endres parameterne i Excel-parameterfilen ved hjelp av en UpdateCustomer-funksjon.</span><span class="sxs-lookup"><span data-stu-id="77d86-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="77d86-253">Deretter kalles RSAT-kommandolinjen i en RunTestCase-funksjon.</span><span class="sxs-lookup"><span data-stu-id="77d86-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="77d86-254">Åpne Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i administratormodus, og lim inn følgende kode i vinduet kalt **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="77d86-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="77d86-255">Kjør et skript som er avhengig av data i Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="77d86-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="77d86-256">Det følgende eksemplet bruker et OData-kall (Open Data Protocol) til å finne ordrestatusen for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="77d86-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="77d86-257">Hvis statusen ikke er **fakturert**, kan du for eksempel kalle et RSAT-testtilfelle som posterer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="77d86-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
