---
title: Opplæring for Regression Suite Automation Tool
description: Dette emnet viser hvordan du bruker Regression Suite Automation Tool (RSAT). Det beskriver ulike funksjoner og gir eksempler som omfatter avansert skripting.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 5a9f19168093f24a7f152b2b5b23b3728ca80222
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745171"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="21a68-104">Opplæring for Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="21a68-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="21a68-105">Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="21a68-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="21a68-106">Denne opplæringen går gjennom noen av de avanserte funksjonene i Regression Suite Automation Tool (RSAT), inneholder en demonstrasjonsoppgave og beskriver strategier og ting som er viktig å lære.</span><span class="sxs-lookup"><span data-stu-id="21a68-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="21a68-107">Funksjoner å merke seg i RSAT og Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="21a68-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="21a68-108">Valider en feltverdi</span><span class="sxs-lookup"><span data-stu-id="21a68-108">Validate a field value</span></span>

<span data-ttu-id="21a68-109">RSAT gjør det mulig å ta med valideringstrinn i testsaken for å validere forventede verdier.</span><span class="sxs-lookup"><span data-stu-id="21a68-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="21a68-110">Hvis du vil ha informasjon om denne funksjonen, kan du se artikkelen [Validere forventede verdier](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="21a68-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="21a68-111">Følgende eksempel viser hvordan du kan bruke denne funksjonen til å validere om lagerbeholdningen er større enn 0 (null).</span><span class="sxs-lookup"><span data-stu-id="21a68-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="21a68-112">I demonstrasjonsdataene i firmaet **USMF** oppretter du et oppgaveopptak som har følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="21a68-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="21a68-113">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="21a68-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="21a68-114">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="21a68-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="21a68-115">Du kan for eksempel filtrere på verdien **1000** for **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="21a68-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="21a68-116">Velg **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="21a68-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="21a68-117">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="21a68-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="21a68-118">Du kan for eksempel filtrere på verdien **1** for **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="21a68-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="21a68-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="21a68-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="21a68-120">Valider at verdien i feltet **Totalt tilgjengelig** er **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="21a68-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="21a68-121">Lagre oppgaveopptaket som et **utvikleropptak**, og knytt det til testsaken i Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="21a68-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="21a68-122">Legg til testtilfellet i testplanen, og last inn testtilfellet i RSAT.</span><span class="sxs-lookup"><span data-stu-id="21a68-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="21a68-123">Åpne Excel-parameterfilen, og gå til fanen **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="21a68-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="21a68-124">Du kan validere om lagerbeholdningen alltid kommer til å være større enn **0**, ved å gå til trinnet **Valider totalt tilgjengelig** og endre verdien fra **411** til **0**.</span><span class="sxs-lookup"><span data-stu-id="21a68-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="21a68-125">Endre verdien i **Operator**-feltet fra et likhetstegn (**=**) til et større enn-tegn (**\>**).</span><span class="sxs-lookup"><span data-stu-id="21a68-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="21a68-126">Lagre og lukk Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="21a68-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="21a68-127">Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen, i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="21a68-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="21a68-128">Hvis verdien i feltet **Totalt tilgjengelig** for den angitte varen i beholdningen er større enn 0 (null), blir testene bestått, uavhengig av den faktiske verdien for lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="21a68-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="21a68-129">Lagrede variabler og kjeding av testsaker</span><span class="sxs-lookup"><span data-stu-id="21a68-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="21a68-130">En av nøkkelfunksjonene i RSAT er kjeding av testtilfeller, det vil si muligheten for en test til å sende variabler til andre tester.</span><span class="sxs-lookup"><span data-stu-id="21a68-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="21a68-131">Hvis du vil ha mer informasjon, se artikkelen [Kopiere variabler for å kjede testtilfeller](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="21a68-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="21a68-132">Avledet testtilfelle</span><span class="sxs-lookup"><span data-stu-id="21a68-132">Derived test case</span></span>

<span data-ttu-id="21a68-133">RSAT lar deg bruke samme oppgaveopptak med flere testtilfeller, slik at en oppgave kan kjøres med forskjellige datakonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="21a68-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="21a68-134">Se artikkelen [Avledede testtilfeller](rsat-derived-test-cases.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="21a68-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="21a68-135">Validere varslinger og meldinger</span><span class="sxs-lookup"><span data-stu-id="21a68-135">Validate notifications and messages</span></span>

<span data-ttu-id="21a68-136">Denne funksjonen kan brukes til å validere om en handling er utført.</span><span class="sxs-lookup"><span data-stu-id="21a68-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="21a68-137">Når en produksjonsordre for eksempel opprettes, estimeres og deretter startes, viser appen meldingen "Produksjon – start" for å varsle deg om at produksjonsordren er startet.</span><span class="sxs-lookup"><span data-stu-id="21a68-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Varslingen Produksjon – start](./media/use_rsa_tool_05.png)

<span data-ttu-id="21a68-139">Du kan validere denne meldingen via RSAT ved å angi meldingsteksten i fanen **Meldingsvalidering** i Excel-parameterfilen for det aktuelle opptaket.</span><span class="sxs-lookup"><span data-stu-id="21a68-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Fanen Meldingsvalidering](./media/use_rsa_tool_06.png)

<span data-ttu-id="21a68-141">Etter at testtilfellet er kjørt, sammenlignes meldingen i Excel-parameterfilen med meldingen som vises.</span><span class="sxs-lookup"><span data-stu-id="21a68-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="21a68-142">Hvis meldingene ikke samsvarer, mislykkes testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="21a68-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="21a68-143">Du kan angi flere meldinger i fanen **Meldingsvalidering** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="21a68-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="21a68-144">Meldingene kan også være feilmeldinger eller advarsler i stedet for informasjonsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="21a68-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="21a68-145">Øyeblikksbilde</span><span class="sxs-lookup"><span data-stu-id="21a68-145">Snapshot</span></span>

<span data-ttu-id="21a68-146">Denne funksjonen tar skjermbilder av trinnene som ble utført under oppgaveopptaket.</span><span class="sxs-lookup"><span data-stu-id="21a68-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="21a68-147">Dette er nyttig for revisjon og feilsøking.</span><span class="sxs-lookup"><span data-stu-id="21a68-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="21a68-148">Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien for følgende element fra **false** til **true**.</span><span class="sxs-lookup"><span data-stu-id="21a68-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="21a68-149">Når du kjører test tilfellet, vil RSAT generere øyeblikksbilder av trinnene i avspillingsmappen for testtilfellene i det gjeldende katalogen.</span><span class="sxs-lookup"><span data-stu-id="21a68-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="21a68-150">Hvis du bruker en eldre versjon av RSAT, lagres bildene på **C:\\Brukere\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, og en separat mappe opprettes for hvert testtilfelle som kjøres.</span><span class="sxs-lookup"><span data-stu-id="21a68-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="21a68-151">Tildeling</span><span class="sxs-lookup"><span data-stu-id="21a68-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="21a68-152">Scenario</span><span class="sxs-lookup"><span data-stu-id="21a68-152">Scenario</span></span>

1. <span data-ttu-id="21a68-153">Produktdesigneren oppretter et nytt frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="21a68-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="21a68-154">Produksjonssjefen starter en produksjonsordre for å bringe lagernivået til to stykker.</span><span class="sxs-lookup"><span data-stu-id="21a68-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="21a68-155">Produksjonen starter og avslutter produksjonsordren og kontrollerer at beholdningsantallet er to stykker.</span><span class="sxs-lookup"><span data-stu-id="21a68-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="21a68-156">Salgsteamet mottar en ordre på fire stykker av det nye produktet.</span><span class="sxs-lookup"><span data-stu-id="21a68-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="21a68-157">Salgsteamet oppdaterer derfor nettobehovet via den dynamiske planen.</span><span class="sxs-lookup"><span data-stu-id="21a68-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="21a68-158">Siden det ikke finnes mer kapasitet, settes standard ordrepolicy til «kjøp i stedet for å lage».</span><span class="sxs-lookup"><span data-stu-id="21a68-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="21a68-159">Det opprettes derfor et bestillingsforslag.</span><span class="sxs-lookup"><span data-stu-id="21a68-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="21a68-160">Innkjøperen legger til en leverandør, autoriserer bestillingsforslaget og bekrefter deretter bestillingen.</span><span class="sxs-lookup"><span data-stu-id="21a68-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="21a68-161">Når varene som ble kjøpt, ankommer i butikken, søker butikkoperatøren etter den tilknyttede bestillingen og mottar varene.</span><span class="sxs-lookup"><span data-stu-id="21a68-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="21a68-162">Siden ordren nå er fullført, kan varene plukkes og pakkes mot salgsordren.</span><span class="sxs-lookup"><span data-stu-id="21a68-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="21a68-163">Finans posterer innkjøpsfakturaen og salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="21a68-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="21a68-164">Illustrasjonen nedenfor viser flyten for dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="21a68-164">The following illustration shows the flow for this scenario.</span></span>

![Flyt for demonstrasjonsscenariet](./media/use_rsa_tool_14.png)

<span data-ttu-id="21a68-166">Følgende illustrasjon viser hierarkiet for forretningsprosesser for dette scenarioet i LCS Forretningsprosessmodelerer.</span><span class="sxs-lookup"><span data-stu-id="21a68-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Forretningsprosesser for demonstrasjonsscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="21a68-168">Strategi – viktige punkt</span><span class="sxs-lookup"><span data-stu-id="21a68-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="21a68-169">Data</span><span class="sxs-lookup"><span data-stu-id="21a68-169">Data</span></span>

- <span data-ttu-id="21a68-170">Sørg for at du har representative datavolumer (en kopi av konfigurasjonsdata for produksjon / gylne konfigurasjonsdata pluss overførte data).</span><span class="sxs-lookup"><span data-stu-id="21a68-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="21a68-171">Når du genererer nye data via Oppgaveopptaker, oppretter du testnavn som ikke kommer i konflikt med eksisterende navn (for eksempel ved å bruke et prefiks som **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="21a68-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="21a68-172">Bruk tidsgjenoppretting av database for Azure til å kjøre tester på nytt i andre miljøer enn Lag 1-miljøer.</span><span class="sxs-lookup"><span data-stu-id="21a68-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="21a68-173">Selv om du kan bruke Excel-funksjonene **TILFELDIG** og **NÅ** til å generere en unik kombinasjon, er det langt fra lettvint.</span><span class="sxs-lookup"><span data-stu-id="21a68-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="21a68-174">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="21a68-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="21a68-175">Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="21a68-175">Task recorder</span></span>

- <span data-ttu-id="21a68-176">Definer scenarier før du starter opptaket.</span><span class="sxs-lookup"><span data-stu-id="21a68-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="21a68-177">Et velstyrt prosjekt har forhåndsdefinerte testscenarier.</span><span class="sxs-lookup"><span data-stu-id="21a68-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="21a68-178">Når du skal bygge et testtilfelle, vurderer du hvor forutsigbart resultatet av testscenariene er.</span><span class="sxs-lookup"><span data-stu-id="21a68-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="21a68-179">Del opp opptak hvis de skal utføres av ulike roller, eller hvis det er ventetid eller en ekstern hendelse før neste trinn.</span><span class="sxs-lookup"><span data-stu-id="21a68-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="21a68-180">Unngå å velge verdier i lister.</span><span class="sxs-lookup"><span data-stu-id="21a68-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="21a68-181">Bruk i stedet tekstformater, for eksempel **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="21a68-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="21a68-182">Når du velger i en liste, blir posisjonen til verdien i listen tatt opp, ikke selve verdien.</span><span class="sxs-lookup"><span data-stu-id="21a68-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="21a68-183">Hvis elementer blir lagt til i denne listen, kan posisjonen til verdien bli endret.</span><span class="sxs-lookup"><span data-stu-id="21a68-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="21a68-184">Derfor bruker opptaket en annen parameter, og resten av scenariet kan bli påvirket.</span><span class="sxs-lookup"><span data-stu-id="21a68-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="21a68-185">Tenk på flerbrukerfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="21a68-185">Think about multi-user behavior.</span></span> <span data-ttu-id="21a68-186">Du kan for eksempel ikke ta for gitt at den nyopprettede salgsordren alltid velges automatisk.</span><span class="sxs-lookup"><span data-stu-id="21a68-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="21a68-187">Bruk i stedet alltid filteret til å finne riktig ordre.</span><span class="sxs-lookup"><span data-stu-id="21a68-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="21a68-188">Bruk Kopier-funksjonen i Oppgaveopptaker til å lagre navnet på et nyopprettet produkt, slik at det kan brukes i kjedede testtilfeller.</span><span class="sxs-lookup"><span data-stu-id="21a68-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="21a68-189">Bruk Valider-funksjonen i Oppgaveopptaker til å angi kontrollpunkt som kontrollerer at trinn er kjørt på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="21a68-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="21a68-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="21a68-190">RSAT</span></span>

- <span data-ttu-id="21a68-191">Hvis du vil kjøre testen i et annet firma, kan du endre firmaet i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="21a68-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="21a68-192">Sørg for at innstillingene og dataene er tilgjengelige i det nylig valgte firmaet.</span><span class="sxs-lookup"><span data-stu-id="21a68-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="21a68-193">Du kan endre testbrukeren i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="21a68-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="21a68-194">Angi e-post-ID-en til brukeren som skal kjøre testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="21a68-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="21a68-195">På denne måten kan testtilfellet kjøres ved hjelp av sikkerhetstillatelsene til den angitte brukeren.</span><span class="sxs-lookup"><span data-stu-id="21a68-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="21a68-196">Hvis du vil vente før testen startes, kan du definere en pause i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="21a68-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="21a68-197">Pausen kan brukes i en satsvis jobb (for eksempel hvis en arbeidsflyt må kjøres før neste trinn kan utføres).</span><span class="sxs-lookup"><span data-stu-id="21a68-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="21a68-198">Avansert skripting</span><span class="sxs-lookup"><span data-stu-id="21a68-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="21a68-199">CLI</span><span class="sxs-lookup"><span data-stu-id="21a68-199">CLI</span></span>

<span data-ttu-id="21a68-200">RSAT kan kalles fra et **ledetekstvindu** eller et **PowerShell**-vindu.</span><span class="sxs-lookup"><span data-stu-id="21a68-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="21a68-201">Kontroller at miljøvariabelen **TestRoot** er satt til RSAT-installasjonsbanen.</span><span class="sxs-lookup"><span data-stu-id="21a68-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="21a68-202">(I Microsoft Windows åpner du **Kontrollpanel**, velger **System og sikkerhet \> System \> Avanserte systeminnstillinger** og deretter **Miljøvariabler**.)</span><span class="sxs-lookup"><span data-stu-id="21a68-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="21a68-203">Åpne et **ledetekstvindu** eller et **PowerShell**-vindu som administrator.</span><span class="sxs-lookup"><span data-stu-id="21a68-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="21a68-204">Gå til installasjonskatalogen for RSAT.</span><span class="sxs-lookup"><span data-stu-id="21a68-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="21a68-205">Vis alle kommandoer.</span><span class="sxs-lookup"><span data-stu-id="21a68-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="21a68-206">?</span><span class="sxs-lookup"><span data-stu-id="21a68-206">?</span></span>

<span data-ttu-id="21a68-207">Viser hjelp om alle tilgjengelige kommandoer og deres parametere.</span><span class="sxs-lookup"><span data-stu-id="21a68-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="21a68-208">?: Valgfrie parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-208">?: Optional parameters</span></span>

<span data-ttu-id="21a68-209">`command`: Der ``[command]`` er en av kommandoene angitt nedenfor.</span><span class="sxs-lookup"><span data-stu-id="21a68-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="21a68-210">about</span><span class="sxs-lookup"><span data-stu-id="21a68-210">about</span></span>

<span data-ttu-id="21a68-211">Viser gjeldende versjon.</span><span class="sxs-lookup"><span data-stu-id="21a68-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="21a68-212">cls</span><span class="sxs-lookup"><span data-stu-id="21a68-212">cls</span></span>

<span data-ttu-id="21a68-213">Tømmer skjermen.</span><span class="sxs-lookup"><span data-stu-id="21a68-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="21a68-214">download</span><span class="sxs-lookup"><span data-stu-id="21a68-214">download</span></span>

<span data-ttu-id="21a68-215">Laster ned vedlegg for den angitte testsaken til utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="21a68-216">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="21a68-217">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="21a68-218">download: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-218">download: required parameters</span></span>

+ <span data-ttu-id="21a68-219">`test_case_id`: representerer ID-en til testsaken.</span><span class="sxs-lookup"><span data-stu-id="21a68-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="21a68-220">`output_dir`: representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="21a68-221">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="21a68-222">download: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="21a68-223">edit</span><span class="sxs-lookup"><span data-stu-id="21a68-223">edit</span></span>

<span data-ttu-id="21a68-224">Lar deg åpne parameterfilen i Excel-programmet og redigere den.</span><span class="sxs-lookup"><span data-stu-id="21a68-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="21a68-225">edit: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-225">edit: required parameters</span></span>

+ <span data-ttu-id="21a68-226">`excel_file`: må inneholde en fullstendig bane til en eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="21a68-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="21a68-227">edit: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="21a68-228">generate</span><span class="sxs-lookup"><span data-stu-id="21a68-228">generate</span></span>

<span data-ttu-id="21a68-229">Genererer testkjøring og parameterfiler for den angitte testsaken i utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="21a68-230">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="21a68-231">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="21a68-232">generere: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-232">generate: required parameters</span></span>

+ <span data-ttu-id="21a68-233">`test_case_id`: representerer ID-en til testsaken.</span><span class="sxs-lookup"><span data-stu-id="21a68-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="21a68-234">`output_dir`: representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="21a68-235">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="21a68-236">generere: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="21a68-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="21a68-237">generatederived</span></span>

<span data-ttu-id="21a68-238">Genererer en ny testsak, avledet fra den angitte testsaken.</span><span class="sxs-lookup"><span data-stu-id="21a68-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="21a68-239">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="21a68-240">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="21a68-241">generatederived: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="21a68-242">`parent_test_case_id`: representerer ID-en til den overordnede testsaken.</span><span class="sxs-lookup"><span data-stu-id="21a68-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="21a68-243">`test_plan_id`: representerer ID-en til testplanen.</span><span class="sxs-lookup"><span data-stu-id="21a68-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="21a68-244">`test_suite_id`: representerer ID-en til testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="21a68-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="21a68-245">generatederived: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="21a68-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="21a68-246">generatetestonly</span></span>

<span data-ttu-id="21a68-247">Genererer bare testkjøringsfil for den angitte testsaken i utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="21a68-248">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="21a68-249">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="21a68-250">generatetestonly: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="21a68-251">`test_case_id`: representerer ID-en til testsaken.</span><span class="sxs-lookup"><span data-stu-id="21a68-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="21a68-252">`output_dir`: representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="21a68-253">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="21a68-254">generatetestonly: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="21a68-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="21a68-255">generatetestsuite</span></span>

<span data-ttu-id="21a68-256">Genererer alle testsaker for det angitte verktøyet i utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="21a68-257">Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="21a68-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="21a68-258">Bruk en verdi fra kolonnen som en **test_suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="21a68-259">generatetestsuite: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="21a68-260">`test_suite_name`: representerer navnet på testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="21a68-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="21a68-261">`output_dir`: representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="21a68-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="21a68-262">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="21a68-263">generatetestsuite: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="21a68-264">help</span><span class="sxs-lookup"><span data-stu-id="21a68-264">help</span></span>

<span data-ttu-id="21a68-265">Identisk med [?](#section)-</span><span class="sxs-lookup"><span data-stu-id="21a68-265">Identical to the [?](#section)</span></span> <span data-ttu-id="21a68-266">kommandoen.</span><span class="sxs-lookup"><span data-stu-id="21a68-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="21a68-267">listen</span><span class="sxs-lookup"><span data-stu-id="21a68-267">list</span></span>

<span data-ttu-id="21a68-268">Viser alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="21a68-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="21a68-269">listtestplans</span></span>

<span data-ttu-id="21a68-270">Viser alle tilgjengelige testplaner.</span><span class="sxs-lookup"><span data-stu-id="21a68-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="21a68-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="21a68-271">listtestsuite</span></span>

<span data-ttu-id="21a68-272">Viser testsaker for det angitte testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="21a68-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="21a68-273">Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="21a68-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="21a68-274">Bruk en verdi fra den første kolonnen som en **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="21a68-275">listtestsuite: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="21a68-276">`suite_name`: navnet på det ønskede verktøyet.</span><span class="sxs-lookup"><span data-stu-id="21a68-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="21a68-277">listtestsuite: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="21a68-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="21a68-278">listtestsuitenames</span></span>

<span data-ttu-id="21a68-279">Viser alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="21a68-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="21a68-280">playback</span><span class="sxs-lookup"><span data-stu-id="21a68-280">playback</span></span>

<span data-ttu-id="21a68-281">Spiller av en testsak ved hjelp av en Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="21a68-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="21a68-282">playback: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-282">playback: required parameters</span></span>

+ <span data-ttu-id="21a68-283">`excel_file`: en fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="21a68-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="21a68-284">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="21a68-285">playback: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="21a68-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="21a68-286">playbackbyid</span></span>

<span data-ttu-id="21a68-287">Spiller av flere testsaker samtidig.</span><span class="sxs-lookup"><span data-stu-id="21a68-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="21a68-288">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="21a68-289">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="21a68-290">playbackbyid: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="21a68-291">`test_case_id1`: ID for eksisterende testsak.</span><span class="sxs-lookup"><span data-stu-id="21a68-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="21a68-292">`test_case_id2`: ID for eksisterende testsak.</span><span class="sxs-lookup"><span data-stu-id="21a68-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="21a68-293">`test_case_idN`: ID for eksisterende testsak.</span><span class="sxs-lookup"><span data-stu-id="21a68-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="21a68-294">playbackbyid: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="21a68-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="21a68-295">playbackmany</span></span>

<span data-ttu-id="21a68-296">Spiller av mange testsaker samtidig ved hjelp av Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="21a68-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="21a68-297">playbackmany: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="21a68-298">`excel_file1`: fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="21a68-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="21a68-299">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-299">File must exist.</span></span>
+ <span data-ttu-id="21a68-300">`excel_file2`: fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="21a68-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="21a68-301">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-301">File must exist.</span></span>
+ <span data-ttu-id="21a68-302">`excel_fileN`: fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="21a68-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="21a68-303">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="21a68-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="21a68-304">playbackmany: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="21a68-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="21a68-305">playbacksuite</span></span>

<span data-ttu-id="21a68-306">Spiller av alle testsaker fra det angitte testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="21a68-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="21a68-307">Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="21a68-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="21a68-308">Bruk en verdi fra den første kolonnen som en **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="21a68-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="21a68-309">playbacksuite: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="21a68-310">`suite_name`: navnet på det ønskede verktøyet.</span><span class="sxs-lookup"><span data-stu-id="21a68-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="21a68-311">playbacksuite: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="21a68-312">quit</span><span class="sxs-lookup"><span data-stu-id="21a68-312">quit</span></span>

<span data-ttu-id="21a68-313">Lukker appen.</span><span class="sxs-lookup"><span data-stu-id="21a68-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="21a68-314">upload</span><span class="sxs-lookup"><span data-stu-id="21a68-314">upload</span></span>

<span data-ttu-id="21a68-315">Laster opp alle filer som hører til angitt testverktøy eller testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="21a68-316">upload: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-316">upload: required parameters</span></span>

+ <span data-ttu-id="21a68-317">`suite_name`: alle filer som hører til angitt testverktøy, lastes opp.</span><span class="sxs-lookup"><span data-stu-id="21a68-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="21a68-318">`testcase_id`: alle filer som hører til angitte testsaker, lastes opp.</span><span class="sxs-lookup"><span data-stu-id="21a68-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="21a68-319">upload: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="21a68-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="21a68-320">uploadrecording</span></span>

<span data-ttu-id="21a68-321">Laster opp bare opptaksfilen som hører til angitte testsaker.</span><span class="sxs-lookup"><span data-stu-id="21a68-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="21a68-322">uploadrecording: nødvendige parametere</span><span class="sxs-lookup"><span data-stu-id="21a68-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="21a68-323">`testcase_id`: opptaksfilen som hører til angitte testsaker, lastes opp.</span><span class="sxs-lookup"><span data-stu-id="21a68-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="21a68-324">uploadrecording: eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="21a68-325">usage</span><span class="sxs-lookup"><span data-stu-id="21a68-325">usage</span></span>

<span data-ttu-id="21a68-326">Viser to måter å aktivere dette programmet på: én som bruker en standard innstillingsfil, en annen som angir en innstillingsfil.</span><span class="sxs-lookup"><span data-stu-id="21a68-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="21a68-327">Windows PowerShell-eksempler</span><span class="sxs-lookup"><span data-stu-id="21a68-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="21a68-328">Kjøre et testtilfelle i en løkke</span><span class="sxs-lookup"><span data-stu-id="21a68-328">Run a test case in a loop</span></span>

<span data-ttu-id="21a68-329">Du har et testskript som oppretter en ny kunde.</span><span class="sxs-lookup"><span data-stu-id="21a68-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="21a68-330">Du kan kjøre dette testtilfellet i en løkke via skripting ved randomisere følgende data før hver gjentakelse kjøres:</span><span class="sxs-lookup"><span data-stu-id="21a68-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="21a68-331">Kunde-ID</span><span class="sxs-lookup"><span data-stu-id="21a68-331">Customer ID</span></span>
- <span data-ttu-id="21a68-332">Kundenavn</span><span class="sxs-lookup"><span data-stu-id="21a68-332">Customer name</span></span>
- <span data-ttu-id="21a68-333">Kundeadresse</span><span class="sxs-lookup"><span data-stu-id="21a68-333">Customer address</span></span>

<span data-ttu-id="21a68-334">Kunde-ID-en er i formatet *ATCUS\<number\>*, der \<number\> er en verdi mellom **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="21a68-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="21a68-335">I det følgende eksemplet brukes én parameter, **start**, til å definere det første nummeret som brukes.</span><span class="sxs-lookup"><span data-stu-id="21a68-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="21a68-336">Det bruker en andre parameter, **nr**, til å definere antallet kunder som må opprettes.</span><span class="sxs-lookup"><span data-stu-id="21a68-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="21a68-337">For hver gjentakelse endres parameterne i Excel-parameterfilen ved hjelp av en UpdateCustomer-funksjon.</span><span class="sxs-lookup"><span data-stu-id="21a68-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="21a68-338">Deretter kalles RSAT-kommandolinjen i en RunTestCase-funksjon.</span><span class="sxs-lookup"><span data-stu-id="21a68-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="21a68-339">Åpne Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i administratormodus, og lim inn følgende kode i vinduet kalt **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="21a68-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="21a68-340">Kjør et skript som er avhengig av data i Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="21a68-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="21a68-341">Det følgende eksemplet bruker et OData-kall (Open Data Protocol) til å finne ordrestatusen for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="21a68-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="21a68-342">Hvis statusen ikke er **fakturert**, kan du for eksempel kalle et RSAT-testtilfelle som posterer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="21a68-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]