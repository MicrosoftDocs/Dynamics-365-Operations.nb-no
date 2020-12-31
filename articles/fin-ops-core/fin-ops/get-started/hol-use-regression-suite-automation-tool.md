---
title: Bruke opplæringen for Regression Suite Automation Tool
description: Dette emnet viser hvordan du bruker Regression Suite Automation Tool (RSAT). Det beskriver ulike funksjoner og gir eksempler som omfatter avansert skripting.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 798717b276e68949a9425350720bf683a37d6fb5
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692996"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="58a53-104">Opplæring for Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="58a53-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="58a53-105">Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="58a53-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="58a53-106">Denne opplæringen går gjennom noen av de avanserte funksjonene i Regression Suite Automation Tool (RSAT), inneholder en demonstrasjonsoppgave og beskriver strategier og ting som er viktig å lære.</span><span class="sxs-lookup"><span data-stu-id="58a53-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="58a53-107">Funksjoner å merke seg i RSAT og Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="58a53-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="58a53-108">Valider en feltverdi</span><span class="sxs-lookup"><span data-stu-id="58a53-108">Validate a field value</span></span>

<span data-ttu-id="58a53-109">RSAT gjør det mulig å ta med valideringstrinn i testsaken for å validere forventede verdier.</span><span class="sxs-lookup"><span data-stu-id="58a53-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="58a53-110">Hvis du vil ha informasjon om denne funksjonen, kan du se artikkelen [Validere forventede verdier](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="58a53-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="58a53-111">Følgende eksempel viser hvordan du kan bruke denne funksjonen til å validere om lagerbeholdningen er større enn 0 (null).</span><span class="sxs-lookup"><span data-stu-id="58a53-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="58a53-112">I demonstrasjonsdataene i firmaet **USMF** oppretter du et oppgaveopptak som har følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="58a53-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="58a53-113">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="58a53-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="58a53-114">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="58a53-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="58a53-115">Du kan for eksempel filtrere på verdien **1000** for **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="58a53-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="58a53-116">Velg **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="58a53-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="58a53-117">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="58a53-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="58a53-118">Du kan for eksempel filtrere på verdien **1** for **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="58a53-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="58a53-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="58a53-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="58a53-120">Valider at verdien i feltet **Totalt tilgjengelig** er **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="58a53-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="58a53-121">Lagre oppgaveopptaket, og knytt det til testsaken i Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="58a53-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="58a53-122">Legg til testtilfellet i testplanen, og last inn testtilfellet i RSAT.</span><span class="sxs-lookup"><span data-stu-id="58a53-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="58a53-123">Åpne Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="58a53-123">Open the Excel parameter file.</span></span> <span data-ttu-id="58a53-124">I fanen **InventOnhandItem** vises delen **Valider InventOnhandItem** som omfatter et **Operator**-felt.</span><span class="sxs-lookup"><span data-stu-id="58a53-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operator-feltet](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="58a53-126">Du kan validere om lagerbeholdningen alltid er større enn 0, ved å endre verdien i **Verdi**-feltet fra **411** til **0** og verdien i **Operator**-feltet fra et likhetstegn (**=**) til et større enn-tegn (**\>**).</span><span class="sxs-lookup"><span data-stu-id="58a53-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Verdiene i feltene Verdi og Operator er endret](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="58a53-128">Lagre og lukk Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="58a53-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="58a53-129">Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen, i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="58a53-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="58a53-130">Hvis verdien i feltet **Totalt tilgjengelig** for den angitte varen i beholdningen er større enn 0 (null), blir testene bestått, uavhengig av den faktiske verdien for lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="58a53-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="58a53-131">Lagrede variabler og kjeding av testsaker</span><span class="sxs-lookup"><span data-stu-id="58a53-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="58a53-132">En av nøkkelfunksjonene i RSAT er kjeding av testtilfeller, det vil si muligheten for en test til å sende variabler til andre tester.</span><span class="sxs-lookup"><span data-stu-id="58a53-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="58a53-133">Hvis du vil ha mer informasjon, se artikkelen [Kopiere variabler for å kjede testtilfeller](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="58a53-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="58a53-134">Avledet testtilfelle</span><span class="sxs-lookup"><span data-stu-id="58a53-134">Derived test case</span></span>

<span data-ttu-id="58a53-135">RSAT lar deg bruke samme oppgaveopptak med flere testtilfeller, slik at en oppgave kan kjøres med forskjellige datakonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="58a53-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="58a53-136">Se artikkelen [Avledede testtilfeller](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="58a53-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="58a53-137">Validere varslinger og meldinger</span><span class="sxs-lookup"><span data-stu-id="58a53-137">Validate notifications and messages</span></span>

<span data-ttu-id="58a53-138">Denne funksjonen kan brukes til å validere om en handling er utført.</span><span class="sxs-lookup"><span data-stu-id="58a53-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="58a53-139">Når en produksjonsordre for eksempel opprettes, estimeres og deretter startes, viser appen meldingen "Produksjon – start" for å varsle deg om at produksjonsordren er startet.</span><span class="sxs-lookup"><span data-stu-id="58a53-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Varslingen Produksjon – start](./media/use_rsa_tool_05.png)

<span data-ttu-id="58a53-141">Du kan validere denne meldingen via RSAT ved å angi meldingsteksten i fanen **Meldingsvalidering** i Excel-parameterfilen for det aktuelle opptaket.</span><span class="sxs-lookup"><span data-stu-id="58a53-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Fanen Meldingsvalidering](./media/use_rsa_tool_06.png)

<span data-ttu-id="58a53-143">Etter at testtilfellet er kjørt, sammenlignes meldingen i Excel-parameterfilen med meldingen som vises.</span><span class="sxs-lookup"><span data-stu-id="58a53-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="58a53-144">Hvis meldingene ikke samsvarer, mislykkes testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="58a53-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="58a53-145">Du kan angi flere meldinger i fanen **Meldingsvalidering** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="58a53-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="58a53-146">Meldingene kan også være feilmeldinger eller advarsler i stedet for informasjonsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="58a53-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="58a53-147">Øyeblikksbilde</span><span class="sxs-lookup"><span data-stu-id="58a53-147">Snapshot</span></span>

<span data-ttu-id="58a53-148">Denne funksjonen tar skjermbilder av trinnene som ble utført under oppgaveopptaket.</span><span class="sxs-lookup"><span data-stu-id="58a53-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="58a53-149">Dette er nyttig for revisjon og feilsøking.</span><span class="sxs-lookup"><span data-stu-id="58a53-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="58a53-150">Hvis du vil bruke denne funksjonen, åpner du filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installasjonsmappen (for eksempel **C:\\Programfiler (x86)\\Regression Suite Automation Tool**) og endrer verdien for følgende element fra **false** til **true**.</span><span class="sxs-lookup"><span data-stu-id="58a53-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="58a53-151">Når du kjører test tilfellet, vil RSAT generere øyeblikksbilder av trinnene i avspillingsmappen for testtilfellene i det gjeldende katalogen.</span><span class="sxs-lookup"><span data-stu-id="58a53-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="58a53-152">Hvis du bruker en eldre versjon av RSAT, lagres bildene på **C:\\Brukere\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, og en separat mappe opprettes for hvert testtilfelle som kjøres.</span><span class="sxs-lookup"><span data-stu-id="58a53-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="58a53-153">Tildeling</span><span class="sxs-lookup"><span data-stu-id="58a53-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="58a53-154">Scenario</span><span class="sxs-lookup"><span data-stu-id="58a53-154">Scenario</span></span>

1. <span data-ttu-id="58a53-155">Produktdesigneren oppretter et nytt frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="58a53-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="58a53-156">Produksjonssjefen starter en produksjonsordre for å bringe lagernivået til to stykker.</span><span class="sxs-lookup"><span data-stu-id="58a53-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="58a53-157">Produksjonen starter og avslutter produksjonsordren og kontrollerer at beholdningsantallet er to stykker.</span><span class="sxs-lookup"><span data-stu-id="58a53-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="58a53-158">Salgsteamet mottar en ordre på fire stykker av det nye produktet.</span><span class="sxs-lookup"><span data-stu-id="58a53-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="58a53-159">Salgsteamet oppdaterer derfor nettobehovet via den dynamiske planen.</span><span class="sxs-lookup"><span data-stu-id="58a53-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="58a53-160">Siden det ikke finnes mer kapasitet, settes standard ordrepolicy til «kjøp i stedet for å lage».</span><span class="sxs-lookup"><span data-stu-id="58a53-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="58a53-161">Det opprettes derfor et bestillingsforslag.</span><span class="sxs-lookup"><span data-stu-id="58a53-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="58a53-162">Innkjøperen legger til en leverandør, autoriserer bestillingsforslaget og bekrefter deretter bestillingen.</span><span class="sxs-lookup"><span data-stu-id="58a53-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="58a53-163">Når varene som ble kjøpt, ankommer i butikken, søker butikkoperatøren etter den tilknyttede bestillingen og mottar varene.</span><span class="sxs-lookup"><span data-stu-id="58a53-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="58a53-164">Siden ordren nå er fullført, kan varene plukkes og pakkes mot salgsordren.</span><span class="sxs-lookup"><span data-stu-id="58a53-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="58a53-165">Finans posterer innkjøpsfakturaen og salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="58a53-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="58a53-166">Illustrasjonen nedenfor viser flyten for dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="58a53-166">The following illustration shows the flow for this scenario.</span></span>

![Flyt for demonstrasjonsscenariet](./media/use_rsa_tool_14.png)

<span data-ttu-id="58a53-168">Følgende illustrasjon viser hierarkiet for forretningsprosesser for dette scenarioet i LCS Forretningsprosessmodelerer.</span><span class="sxs-lookup"><span data-stu-id="58a53-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Forretningsprosesser for demonstrasjonsscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="58a53-170">Strategi – viktige punkt</span><span class="sxs-lookup"><span data-stu-id="58a53-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="58a53-171">Data</span><span class="sxs-lookup"><span data-stu-id="58a53-171">Data</span></span>

- <span data-ttu-id="58a53-172">Sørg for at du har representative datavolumer (en kopi av konfigurasjonsdata for produksjon / gylne konfigurasjonsdata pluss overførte data).</span><span class="sxs-lookup"><span data-stu-id="58a53-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="58a53-173">Når du genererer nye data via Oppgaveopptaker, oppretter du testnavn som ikke kommer i konflikt med eksisterende navn (for eksempel ved å bruke et prefiks som **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="58a53-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="58a53-174">Bruk tidsgjenoppretting av database for Azure til å kjøre tester på nytt i andre miljøer enn Lag 1-miljøer.</span><span class="sxs-lookup"><span data-stu-id="58a53-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="58a53-175">Selv om du kan bruke Excel-funksjonene **TILFELDIG** og **NÅ** til å generere en unik kombinasjon, er det langt fra lettvint.</span><span class="sxs-lookup"><span data-stu-id="58a53-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="58a53-176">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="58a53-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="58a53-177">Oppgaveopptaker</span><span class="sxs-lookup"><span data-stu-id="58a53-177">Task recorder</span></span>

- <span data-ttu-id="58a53-178">Definer scenarier før du starter opptaket.</span><span class="sxs-lookup"><span data-stu-id="58a53-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="58a53-179">Et velstyrt prosjekt har forhåndsdefinerte testscenarier.</span><span class="sxs-lookup"><span data-stu-id="58a53-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="58a53-180">Når du skal bygge et testtilfelle, vurderer du hvor forutsigbart resultatet av testscenariene er.</span><span class="sxs-lookup"><span data-stu-id="58a53-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="58a53-181">Del opp opptak hvis de skal utføres av ulike roller, eller hvis det er ventetid eller en ekstern hendelse før neste trinn.</span><span class="sxs-lookup"><span data-stu-id="58a53-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="58a53-182">Unngå å velge verdier i lister.</span><span class="sxs-lookup"><span data-stu-id="58a53-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="58a53-183">Bruk i stedet tekstformater, for eksempel **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="58a53-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="58a53-184">Når du velger i en liste, blir posisjonen til verdien i listen tatt opp, ikke selve verdien.</span><span class="sxs-lookup"><span data-stu-id="58a53-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="58a53-185">Hvis elementer blir lagt til i denne listen, kan posisjonen til verdien bli endret.</span><span class="sxs-lookup"><span data-stu-id="58a53-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="58a53-186">Derfor bruker opptaket en annen parameter, og resten av scenariet kan bli påvirket.</span><span class="sxs-lookup"><span data-stu-id="58a53-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="58a53-187">Tenk på flerbrukerfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="58a53-187">Think about multi-user behavior.</span></span> <span data-ttu-id="58a53-188">Du kan for eksempel ikke ta for gitt at den nyopprettede salgsordren alltid velges automatisk.</span><span class="sxs-lookup"><span data-stu-id="58a53-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="58a53-189">Bruk i stedet alltid filteret til å finne riktig ordre.</span><span class="sxs-lookup"><span data-stu-id="58a53-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="58a53-190">Bruk Kopier-funksjonen i Oppgaveopptaker til å lagre navnet på et nyopprettet produkt, slik at det kan brukes i kjedede testtilfeller.</span><span class="sxs-lookup"><span data-stu-id="58a53-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="58a53-191">Bruk Valider-funksjonen i Oppgaveopptaker til å angi kontrollpunkt som kontrollerer at trinn er kjørt på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="58a53-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="58a53-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="58a53-192">RSAT</span></span>

- <span data-ttu-id="58a53-193">Hvis du vil kjøre testen i et annet firma, kan du endre firmaet i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="58a53-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="58a53-194">Sørg for at innstillingene og dataene er tilgjengelige i det nylig valgte firmaet.</span><span class="sxs-lookup"><span data-stu-id="58a53-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="58a53-195">Du kan endre testbrukeren i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="58a53-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="58a53-196">Angi e-post-ID-en til brukeren som skal kjøre testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="58a53-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="58a53-197">På denne måten kan testtilfellet kjøres ved hjelp av sikkerhetstillatelsene til den angitte brukeren.</span><span class="sxs-lookup"><span data-stu-id="58a53-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="58a53-198">Hvis du vil vente før testen startes, kan du definere en pause i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="58a53-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="58a53-199">Pausen kan brukes i en satsvis jobb (for eksempel hvis en arbeidsflyt må kjøres før neste trinn kan utføres).</span><span class="sxs-lookup"><span data-stu-id="58a53-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="58a53-200">Avansert skripting</span><span class="sxs-lookup"><span data-stu-id="58a53-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="58a53-201">CLI</span><span class="sxs-lookup"><span data-stu-id="58a53-201">CLI</span></span>

<span data-ttu-id="58a53-202">RSAT kan kalles fra et **ledetekstvindu** eller et **PowerShell**-vindu.</span><span class="sxs-lookup"><span data-stu-id="58a53-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="58a53-203">Kontroller at miljøvariabelen **TestRoot** er satt til RSAT-installasjonsbanen.</span><span class="sxs-lookup"><span data-stu-id="58a53-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="58a53-204">(I Microsoft Windows åpner du **Kontrollpanel**, velger **System og sikkerhet \> System \> Avanserte systeminnstillinger** og deretter **Miljøvariabler**.)</span><span class="sxs-lookup"><span data-stu-id="58a53-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="58a53-205">Åpne et **ledetekstvindu** eller et **PowerShell**-vindu som administrator.</span><span class="sxs-lookup"><span data-stu-id="58a53-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="58a53-206">Gå til installasjonskatalogen for RSAT.</span><span class="sxs-lookup"><span data-stu-id="58a53-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="58a53-207">Vis alle kommandoer.</span><span class="sxs-lookup"><span data-stu-id="58a53-207">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="58a53-208">?</span><span class="sxs-lookup"><span data-stu-id="58a53-208">?</span></span> 
<span data-ttu-id="58a53-209">Viser hjelp om alle tilgjengelige kommandoer og deres parametere.</span><span class="sxs-lookup"><span data-stu-id="58a53-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="58a53-210">Valgfrie parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="58a53-211">Der ``[command]`` er en av kommandoene angitt nedenfor.</span><span class="sxs-lookup"><span data-stu-id="58a53-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="58a53-212">about</span><span class="sxs-lookup"><span data-stu-id="58a53-212">about</span></span>
<span data-ttu-id="58a53-213">Viser gjeldende versjon.</span><span class="sxs-lookup"><span data-stu-id="58a53-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="58a53-214">cls</span><span class="sxs-lookup"><span data-stu-id="58a53-214">cls</span></span>
<span data-ttu-id="58a53-215">Tømmer skjermen.</span><span class="sxs-lookup"><span data-stu-id="58a53-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="58a53-216">last ned</span><span class="sxs-lookup"><span data-stu-id="58a53-216">download</span></span>
<span data-ttu-id="58a53-217">Laster ned vedlegg for den angitte testsaken til utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="58a53-218">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="58a53-219">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-220">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-220">Required parameters</span></span>
<span data-ttu-id="58a53-221">**``test_case_id``** representerer ID-en til testsaken.</span><span class="sxs-lookup"><span data-stu-id="58a53-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="58a53-222">**``output_dir``** representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="58a53-223">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-224">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="58a53-225">rediger</span><span class="sxs-lookup"><span data-stu-id="58a53-225">edit</span></span>
<span data-ttu-id="58a53-226">Lar deg åpne parameterfilen i Excel-programmet og redigere den.</span><span class="sxs-lookup"><span data-stu-id="58a53-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-227">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-227">Required parameters</span></span>
<span data-ttu-id="58a53-228">**``excel_file``** må inneholde en fullstendig bane til en eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="58a53-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-229">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="58a53-230">generate</span><span class="sxs-lookup"><span data-stu-id="58a53-230">generate</span></span>
<span data-ttu-id="58a53-231">Genererer testkjøring og parameterfiler for den angitte testsaken i utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="58a53-232">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="58a53-233">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-234">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-234">Required parameters</span></span>
<span data-ttu-id="58a53-235">**``test_case_id``** representerer ID-en til testsaken.</span><span class="sxs-lookup"><span data-stu-id="58a53-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="58a53-236">**``output_dir``** representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="58a53-237">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-238">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="58a53-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="58a53-239">generatederived</span></span>
<span data-ttu-id="58a53-240">Genererer en ny testsak, avledet fra den angitte testsaken.</span><span class="sxs-lookup"><span data-stu-id="58a53-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="58a53-241">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="58a53-242">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-243">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-243">Required parameters</span></span>
<span data-ttu-id="58a53-244">**``parent_test_case_id``** representerer ID-en til den overordnede testsaken.</span><span class="sxs-lookup"><span data-stu-id="58a53-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="58a53-245">**``test_plan_id``** representerer ID-en til testplanen.</span><span class="sxs-lookup"><span data-stu-id="58a53-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="58a53-246">**``test_suite_id``** representerer ID-en til testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="58a53-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-247">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="58a53-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="58a53-248">generatetestonly</span></span>
<span data-ttu-id="58a53-249">Genererer bare testkjøringsfil for den angitte testsaken i utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="58a53-250">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="58a53-251">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-252">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-252">Required parameters</span></span>
<span data-ttu-id="58a53-253">**``test_case_id``** representerer ID-en til testsaken.</span><span class="sxs-lookup"><span data-stu-id="58a53-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="58a53-254">**``output_dir``** representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="58a53-255">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-256">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="58a53-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="58a53-257">generatetestsuite</span></span>
<span data-ttu-id="58a53-258">Genererer alle testsaker for det angitte verktøyet i utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="58a53-259">Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="58a53-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="58a53-260">Bruk en verdi fra kolonnen som en **test_suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-261">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-261">Required parameters</span></span>
<span data-ttu-id="58a53-262">**``test_suite_name``** representerer navnet til testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="58a53-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="58a53-263">**``output_dir``** representerer utdatamappen.</span><span class="sxs-lookup"><span data-stu-id="58a53-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="58a53-264">Katalogen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-265">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="58a53-266">help</span><span class="sxs-lookup"><span data-stu-id="58a53-266">help</span></span>
<span data-ttu-id="58a53-267">Identisk med [?](#section)-</span><span class="sxs-lookup"><span data-stu-id="58a53-267">Identical to the [?](#section)</span></span> <span data-ttu-id="58a53-268">kommandoen</span><span class="sxs-lookup"><span data-stu-id="58a53-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="58a53-269">listen</span><span class="sxs-lookup"><span data-stu-id="58a53-269">list</span></span>
<span data-ttu-id="58a53-270">Viser alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="58a53-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="58a53-271">listtestplans</span></span>
<span data-ttu-id="58a53-272">Viser alle tilgjengelige testplaner.</span><span class="sxs-lookup"><span data-stu-id="58a53-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="58a53-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="58a53-273">listtestsuite</span></span>
<span data-ttu-id="58a53-274">Viser testsaker for det angitte testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="58a53-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="58a53-275">Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="58a53-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="58a53-276">Bruk en verdi fra den første kolonnen som en **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-277">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-277">Required parameters</span></span>
<span data-ttu-id="58a53-278">**``suite_name``** navnet på det ønskede verktøyet.</span><span class="sxs-lookup"><span data-stu-id="58a53-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-279">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="58a53-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="58a53-280">listtestsuitenames</span></span>
<span data-ttu-id="58a53-281">Viser alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="58a53-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="58a53-282">playback</span><span class="sxs-lookup"><span data-stu-id="58a53-282">playback</span></span>
<span data-ttu-id="58a53-283">Spiller av en testsak ved hjelp av en Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="58a53-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-284">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-284">Required parameters</span></span>
<span data-ttu-id="58a53-285">**``excel_file``** en fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="58a53-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="58a53-286">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="58a53-287">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="58a53-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="58a53-288">playbackbyid</span></span>
<span data-ttu-id="58a53-289">Spiller av flere testsaker samtidig.</span><span class="sxs-lookup"><span data-stu-id="58a53-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="58a53-290">Du kan bruke ``list``-kommandoen til å hente alle tilgjengelige testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="58a53-291">Bruk en verdi fra den første kolonnen som en **test_case_id**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-292">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-292">Required parameters</span></span>
<span data-ttu-id="58a53-293">**``test_case_id1``** ID for eksisterende testsak.</span><span class="sxs-lookup"><span data-stu-id="58a53-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="58a53-294">**``test_case_id2``** ID for eksisterende testsak.</span><span class="sxs-lookup"><span data-stu-id="58a53-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="58a53-295">**``test_case_idN``** ID for eksisterende testsak.</span><span class="sxs-lookup"><span data-stu-id="58a53-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="58a53-296">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="58a53-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="58a53-297">playbackmany</span></span>
<span data-ttu-id="58a53-298">Spiller av mange testsaker samtidig ved hjelp av Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="58a53-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-299">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-299">Required parameters</span></span>
<span data-ttu-id="58a53-300">**``excel_file1``** fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="58a53-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="58a53-301">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-301">File must exist.</span></span>  
<span data-ttu-id="58a53-302">**``excel_file2``** fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="58a53-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="58a53-303">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-303">File must exist.</span></span>  
<span data-ttu-id="58a53-304">**``excel_fileN``** fullstendig bane til Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="58a53-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="58a53-305">Filen må finnes.</span><span class="sxs-lookup"><span data-stu-id="58a53-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="58a53-306">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="58a53-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="58a53-307">playbacksuite</span></span>
<span data-ttu-id="58a53-308">Spiller av alle testsaker fra det angitte testverktøyet.</span><span class="sxs-lookup"><span data-stu-id="58a53-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="58a53-309">Du kan bruke ``listtestsuitenames``-kommandoen til å hente alle tilgjengelige testverktøy.</span><span class="sxs-lookup"><span data-stu-id="58a53-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="58a53-310">Bruk en verdi fra den første kolonnen som en **suite_name**-parameter.</span><span class="sxs-lookup"><span data-stu-id="58a53-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-311">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-311">Required parameters</span></span>
<span data-ttu-id="58a53-312">**``suite_name``** navnet på det ønskede verktøyet.</span><span class="sxs-lookup"><span data-stu-id="58a53-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-313">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="58a53-314">quit</span><span class="sxs-lookup"><span data-stu-id="58a53-314">quit</span></span>
<span data-ttu-id="58a53-315">Lukker appen.</span><span class="sxs-lookup"><span data-stu-id="58a53-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="58a53-316">upload</span><span class="sxs-lookup"><span data-stu-id="58a53-316">upload</span></span>
<span data-ttu-id="58a53-317">Laster opp alle filer som hører til angitt testverktøy eller testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="58a53-318">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-318">Required parameters</span></span>
<span data-ttu-id="58a53-319">**``suite_name``** alle filer som hører til angitt testverktøy, lastes opp.</span><span class="sxs-lookup"><span data-stu-id="58a53-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="58a53-320">**``testcase_id``** alle filer som hører til angitte testsaker, lastes opp.</span><span class="sxs-lookup"><span data-stu-id="58a53-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-321">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="58a53-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="58a53-322">uploadrecording</span></span>
<span data-ttu-id="58a53-323">Laster opp bare opptaksfilen som hører til angitte testsaker.</span><span class="sxs-lookup"><span data-stu-id="58a53-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="58a53-324">Obligatoriske parametere</span><span class="sxs-lookup"><span data-stu-id="58a53-324">Required parameters</span></span>
<span data-ttu-id="58a53-325">**``testcase_id``** opptaksfilen som hører til angitte testsaker, lastes opp.</span><span class="sxs-lookup"><span data-stu-id="58a53-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="58a53-326">Eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="58a53-327">usage</span><span class="sxs-lookup"><span data-stu-id="58a53-327">usage</span></span>
<span data-ttu-id="58a53-328">Viser to måter å aktivere dette programmet på: én som bruker en standard innstillingsfil, en annen som angir en innstillingsfil.</span><span class="sxs-lookup"><span data-stu-id="58a53-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="58a53-329">Windows PowerShell-eksempler</span><span class="sxs-lookup"><span data-stu-id="58a53-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="58a53-330">Eksempelskriptene nedenfor leveres som de er for illustrasjonsformål og støttes ikke av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="58a53-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="58a53-331">Kjøre et testtilfelle i en løkke</span><span class="sxs-lookup"><span data-stu-id="58a53-331">Run a test case in a loop</span></span>

<span data-ttu-id="58a53-332">Du har et testskript som oppretter en ny kunde.</span><span class="sxs-lookup"><span data-stu-id="58a53-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="58a53-333">Du kan kjøre dette testtilfellet i en løkke via skripting ved randomisere følgende data før hver gjentakelse kjøres:</span><span class="sxs-lookup"><span data-stu-id="58a53-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="58a53-334">Kunde-ID</span><span class="sxs-lookup"><span data-stu-id="58a53-334">Customer ID</span></span>
- <span data-ttu-id="58a53-335">Kundenavn</span><span class="sxs-lookup"><span data-stu-id="58a53-335">Customer name</span></span>
- <span data-ttu-id="58a53-336">Kundeadresse</span><span class="sxs-lookup"><span data-stu-id="58a53-336">Customer address</span></span>

<span data-ttu-id="58a53-337">Kunde-ID-en er i formatet *ATCUS\<number\>*, der \<number\> er en verdi mellom **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="58a53-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="58a53-338">I det følgende eksemplet brukes én parameter, **start**, til å definere det første nummeret som brukes.</span><span class="sxs-lookup"><span data-stu-id="58a53-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="58a53-339">Det bruker en andre parameter, **nr**, til å definere antallet kunder som må opprettes.</span><span class="sxs-lookup"><span data-stu-id="58a53-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="58a53-340">For hver gjentakelse endres parameterne i Excel-parameterfilen ved hjelp av en UpdateCustomer-funksjon.</span><span class="sxs-lookup"><span data-stu-id="58a53-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="58a53-341">Deretter kalles RSAT-kommandolinjen i en RunTestCase-funksjon.</span><span class="sxs-lookup"><span data-stu-id="58a53-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="58a53-342">Åpne Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i administratormodus, og lim inn følgende kode i vinduet kalt **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="58a53-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="58a53-343">Kjør et skript som er avhengig av data i Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="58a53-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="58a53-344">Det følgende eksemplet bruker et OData-kall (Open Data Protocol) til å finne ordrestatusen for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="58a53-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="58a53-345">Hvis statusen ikke er **fakturert**, kan du for eksempel kalle et RSAT-testtilfelle som posterer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="58a53-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
