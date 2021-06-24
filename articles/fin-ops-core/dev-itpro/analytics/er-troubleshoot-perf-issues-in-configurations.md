---
title: Feilsøke ytelsesproblemer i ER-konfigurasjoner
description: Dette emnet beskriver hvordan du finner og retter ytelsesproblemer i ER-konfigurasjoner (elektronisk rapportering).
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216871"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="fef04-103">Feilsøke ytelsesproblemer i ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fef04-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="fef04-104">Dette emnet forklarer hvordan du løser ytelsesproblemer i ER-[konfigurasjoner](general-electronic-reporting.md#Configuration) ([elektronisk rapportering](general-electronic-reporting.md)).</span><span class="sxs-lookup"><span data-stu-id="fef04-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="fef04-105">Ytelsesundersøkelser består vanligvis av flere trinn.</span><span class="sxs-lookup"><span data-stu-id="fef04-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="fef04-106">[Samle inn](#collecting-data) data.</span><span class="sxs-lookup"><span data-stu-id="fef04-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="fef04-107">Analyser de innsamlede dataene.</span><span class="sxs-lookup"><span data-stu-id="fef04-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="fef04-108">Bruk ER-konfigurasjoner til å [gjøre endringer](#making-changes) basert på resultatene av analysen, eller bestem deg for å samle inn flere data.</span><span class="sxs-lookup"><span data-stu-id="fef04-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="fef04-109">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="fef04-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="fef04-110">Analysere kjøretid</span><span class="sxs-lookup"><span data-stu-id="fef04-110">Analyze execution time</span></span>

<span data-ttu-id="fef04-111">Kjøretiden kan avhenge av uforutsigbare faktorer, for eksempel andre oppgaver som kjører i samme miljø, og hurtigbufring som bruker data når den kalles opp for første gang.</span><span class="sxs-lookup"><span data-stu-id="fef04-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="fef04-112">Du må derfor gjenta kjøringen og målingen flere ganger.</span><span class="sxs-lookup"><span data-stu-id="fef04-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="fef04-113">Noen ganger skyldes ikke ytelsesproblemer en ER-formatkonfigurasjon som brukes til rapportering.</span><span class="sxs-lookup"><span data-stu-id="fef04-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="fef04-114">De skyldes i stedet X++-koden som brukes til å åpne denne ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fef04-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="fef04-115">Se på kjøretiden for rapporten i [handlingssenteret](#infolog-time) eller [hendelsesloggen](#event-log-time).</span><span class="sxs-lookup"><span data-stu-id="fef04-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="fef04-116">Sammenlign kjøretiden for rapporten med den totale kjøretiden i scenarioet.</span><span class="sxs-lookup"><span data-stu-id="fef04-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="fef04-117">Hvis kjøretiden for rapporten er mye kortere enn den totale kjøretiden, må du ta hensyn til mengden data som rapporten behandler:</span><span class="sxs-lookup"><span data-stu-id="fef04-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="fef04-118">Hvis rapporten behandler en liten mengde data, kan problemet ha å gjøre med innlastingstiden til konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fef04-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="fef04-119">Hvis rapporten behandler en stor mengde data, kan problemet ha å gjøre med forhåndsbehandling av X++.</span><span class="sxs-lookup"><span data-stu-id="fef04-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="fef04-120">Bruk [Trace Parser](#analyze-trace-parser-trace) til å analysere dette tilfellet.</span><span class="sxs-lookup"><span data-stu-id="fef04-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="fef04-121">Når det gjelder andre tilfeller, kan du se de neste delene.</span><span class="sxs-lookup"><span data-stu-id="fef04-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="fef04-122">Kjør flere tester som omfatter ulike datamengder, slik at du kan finne ut hvordan kjøretiden avhenger av datamengden.</span><span class="sxs-lookup"><span data-stu-id="fef04-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="fef04-123">Analysere Trace Parser-sporinger</span><span class="sxs-lookup"><span data-stu-id="fef04-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="fef04-124">Klargjør et lite eksempel, eller samle inn flere sporinger under tilfeldige deler av rapportgenereringen.</span><span class="sxs-lookup"><span data-stu-id="fef04-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="fef04-125">I [Trace Parser](#trace-parser) kan du deretter foreta en standard bunn-til-topp-analyse og svare på følgende spørsmål:</span><span class="sxs-lookup"><span data-stu-id="fef04-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="fef04-126">Hva er de beste metodene når det gjelder tidsforbruk?</span><span class="sxs-lookup"><span data-stu-id="fef04-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="fef04-127">Hvilken del av totaltiden bruker disse metodene?</span><span class="sxs-lookup"><span data-stu-id="fef04-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="fef04-128">Svar på de samme spørsmålene for spørringer.</span><span class="sxs-lookup"><span data-stu-id="fef04-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="fef04-129">Hvis du ser at metoder har prefikset «ER», kan du gå videre til neste del.</span><span class="sxs-lookup"><span data-stu-id="fef04-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="fef04-130">Hvis du ser at metoder eller spørringer stammer fra programserien, vurderer du generiske optimaliseringer (for eksempel ved å opprette indekser).</span><span class="sxs-lookup"><span data-stu-id="fef04-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="fef04-131">Analyser antall oppkall.</span><span class="sxs-lookup"><span data-stu-id="fef04-131">Analyze the number of calls.</span></span> <span data-ttu-id="fef04-132">Hvis antallet er betydelig høyere enn forventet, vurderer du å hurtigbufre de tilsvarende nodene for konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fef04-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="fef04-133">Analysere databaseoppkall</span><span class="sxs-lookup"><span data-stu-id="fef04-133">Analyze database calls</span></span>

<span data-ttu-id="fef04-134">Gjør klart et eksempel som har en liten mengde data, slik at du kan samle inn en [ER-sporing](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="fef04-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="fef04-135">Åpne deretter sporingen i ER-utforming av modelltilordning, og se nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="fef04-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="fef04-136">Svar på følgende spørsmål:</span><span class="sxs-lookup"><span data-stu-id="fef04-136">Answer the following questions:</span></span>

- <span data-ttu-id="fef04-137">Skjer det noen spørringsduplisering?</span><span class="sxs-lookup"><span data-stu-id="fef04-137">Is there any query duplication?</span></span> <span data-ttu-id="fef04-138">Hvis det gjør det, vurderer du en av følgende rettelser:</span><span class="sxs-lookup"><span data-stu-id="fef04-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="fef04-139">[Bruk hurtigbufring](#use-caching) hvis du tror at det er flere oppkall i én overordnet post.</span><span class="sxs-lookup"><span data-stu-id="fef04-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="fef04-140">[Bruk et hurtigbufret, parameterisert beregnet felt](#cached-parameterized) hvis du tror at det er oppkall til samme post i ulike poster.</span><span class="sxs-lookup"><span data-stu-id="fef04-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="fef04-141">[Bruk en **JOIN**-datakilde](#use-join-datasource) hvis du må lese til et stort antall ulike poster fra en database.</span><span class="sxs-lookup"><span data-stu-id="fef04-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="fef04-142">Svarer antall spørringer og hentede poster til den totale datamengden?</span><span class="sxs-lookup"><span data-stu-id="fef04-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="fef04-143">Hvis et dokument for eksempel har 10 linjer, viser statistikken at rapporten henter 10 linjer eller 1 000 linjer?</span><span class="sxs-lookup"><span data-stu-id="fef04-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="fef04-144">Hvis du har et betydelig antall hentede poster, vurderer du en av følgende rettelser:</span><span class="sxs-lookup"><span data-stu-id="fef04-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="fef04-145">[Bruk **FILTER**-funksjonen i stedet for **WHERE**-funksjonen](#filter) til å behandle data på SQL Server-siden.</span><span class="sxs-lookup"><span data-stu-id="fef04-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="fef04-146">Bruk hurtigbufring til å unngå at de samme dataene hentes.</span><span class="sxs-lookup"><span data-stu-id="fef04-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="fef04-147">[Bruk funksjoner for innsamlede data](#collected-data) til å unngå å hente de samme dataene til summering.</span><span class="sxs-lookup"><span data-stu-id="fef04-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="fef04-148">Analysere PerfView-sporinger</span><span class="sxs-lookup"><span data-stu-id="fef04-148">Analyze PerfView traces</span></span>

<span data-ttu-id="fef04-149">[PerfView](#perfview) er et verktøy for erfarne utviklere.</span><span class="sxs-lookup"><span data-stu-id="fef04-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="fef04-150">Hvis du vil ha mer detaljert informasjon om følgende trinn, kan du se [Grunnleggende om undersøkelse i veggklokketid](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="fef04-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="fef04-151">Samle inn en sporing ved hjelp av trådtid.</span><span class="sxs-lookup"><span data-stu-id="fef04-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="fef04-152">Ta bare med stakker som bruker **runUnattended**, for å filtrere tråden som har konfigurasjonskjøring.</span><span class="sxs-lookup"><span data-stu-id="fef04-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="fef04-153">(Legg til **runUnattended** i inndataboksen **IncPats**.)</span><span class="sxs-lookup"><span data-stu-id="fef04-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="fef04-154">Fold all CPU-tid, nettverkstid og blokkert tid.</span><span class="sxs-lookup"><span data-stu-id="fef04-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="fef04-155">Last inn [ER-forhåndsinnstillinger for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="fef04-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="fef04-156">Velg **ER** \> **Annen forhåndsinnstilling**.</span><span class="sxs-lookup"><span data-stu-id="fef04-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="fef04-157">Se på navnene:</span><span class="sxs-lookup"><span data-stu-id="fef04-157">Look at the names:</span></span>

    - <span data-ttu-id="fef04-158">Du kommer sannsynligvis til å se plattformkoden som bruker mest tid.</span><span class="sxs-lookup"><span data-stu-id="fef04-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="fef04-159">Du kan dobbelttrykke (eller dobbeltklikke) og gå opp gjennom **oppkallere**.</span><span class="sxs-lookup"><span data-stu-id="fef04-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="fef04-160">Hvis du finner klasser som har prefikset «ERExpression», og hvis de er funksjoner som er knyttet til formler, kan du gjette funksjonsnavnet basert på klassenavnet, og du kan se på ER-repositoriet for å vise attributtene.</span><span class="sxs-lookup"><span data-stu-id="fef04-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="fef04-161">Rettelser</span><span class="sxs-lookup"><span data-stu-id="fef04-161">Fixes</span></span>

- <span data-ttu-id="fef04-162">Hvis du ser at mesteparten av CPU-tiden brukes på spørringer, prøver du å redusere antall spørringer:</span><span class="sxs-lookup"><span data-stu-id="fef04-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="fef04-163">[Se gjennom ER-sporingen](#analyze-database-calls) etter dupliserte spørringer.</span><span class="sxs-lookup"><span data-stu-id="fef04-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="fef04-164">Se hvor mange poster som er hentet, og vurder hvor mye data som teoretisk skulle vært hentet.</span><span class="sxs-lookup"><span data-stu-id="fef04-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="fef04-165">Hvis du ser at mesteparten av CPU-tiden brukes av funksjonene som brukes, prøver du å finne ut hvor i konfigurasjonen mesteparten av ressursene brukes.</span><span class="sxs-lookup"><span data-stu-id="fef04-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="fef04-166">Hvis du ser at mesteparten av CPU-tiden brukes av funksjonene for datainnsamling, vurderer du å erstatte dem med *SQL-setningsdelen GROUP BY* på modelltilordningssiden.</span><span class="sxs-lookup"><span data-stu-id="fef04-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="fef04-167">Samle inn data</span><span class="sxs-lookup"><span data-stu-id="fef04-167">Collecting data</span></span>

<span data-ttu-id="fef04-168">Du kan samle inn tilgjengelige data på flere ulike måter, avhengig av miljøet ditt:</span><span class="sxs-lookup"><span data-stu-id="fef04-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="fef04-169">Få den totale kjøretiden:</span><span class="sxs-lookup"><span data-stu-id="fef04-169">Get the total running time:</span></span>

    - <span data-ttu-id="fef04-170">fra handlingssenteret</span><span class="sxs-lookup"><span data-stu-id="fef04-170">From the Action center</span></span>
    - <span data-ttu-id="fef04-171">fra hendelsesloggen</span><span class="sxs-lookup"><span data-stu-id="fef04-171">From the event log</span></span>

- <span data-ttu-id="fef04-172">Profiler kjøringen:</span><span class="sxs-lookup"><span data-stu-id="fef04-172">Profile the execution:</span></span>

    - <span data-ttu-id="fef04-173">ved å bruke ER-verktøy</span><span class="sxs-lookup"><span data-stu-id="fef04-173">By using ER tools</span></span>
    - <span data-ttu-id="fef04-174">ved å bruke Trace Parser</span><span class="sxs-lookup"><span data-stu-id="fef04-174">By using Trace parser</span></span>
    - <span data-ttu-id="fef04-175">ved å bruke PerfView</span><span class="sxs-lookup"><span data-stu-id="fef04-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="fef04-176">Samle inn data i et produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="fef04-176">Collecting data in a production environment</span></span>

<span data-ttu-id="fef04-177">Noen ganger kan problemer bare reproduseres i et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="fef04-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="fef04-178">Du kan samle inn data på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="fef04-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="fef04-179">ved å bruke [Trace Parser](../perf-test/trace-trace-tutorial.md)-sporinger</span><span class="sxs-lookup"><span data-stu-id="fef04-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="fef04-180">ved å bruke [ER-kjørings](trace-execution-er-troubleshoot-perf.md)sporinger</span><span class="sxs-lookup"><span data-stu-id="fef04-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="fef04-181">ved å bruke den totale kjøringstiden</span><span class="sxs-lookup"><span data-stu-id="fef04-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="fef04-182">Samle inn data i et utviklingsmiljø</span><span class="sxs-lookup"><span data-stu-id="fef04-182">Collecting data in a development environment</span></span>

<span data-ttu-id="fef04-183">I tillegg til verktøyene som kan brukes i et produksjonsmiljø, finnes det flere verktøy du kan bruke i et utviklingsmiljø:</span><span class="sxs-lookup"><span data-stu-id="fef04-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="fef04-184">Hendelseslogg (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="fef04-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="fef04-185">Denne loggen kan gi deg den totale kjøretiden.</span><span class="sxs-lookup"><span data-stu-id="fef04-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="fef04-186">Vanlige .NET-verktøy, for eksempel PerfView.</span><span class="sxs-lookup"><span data-stu-id="fef04-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="fef04-187">Et utviklingsmiljø gir deg i tillegg større fleksibilitet til å eksperimentere.</span><span class="sxs-lookup"><span data-stu-id="fef04-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="fef04-188">Du kan for eksempel deaktivere deler av rapporter for å se hvordan kjøringstiden påvirkes.</span><span class="sxs-lookup"><span data-stu-id="fef04-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="fef04-189">Verktøy</span><span class="sxs-lookup"><span data-stu-id="fef04-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="fef04-190">Kjøringstiden i handlingssenteret</span><span class="sxs-lookup"><span data-stu-id="fef04-190">Execution time in the Action center</span></span>

<span data-ttu-id="fef04-191">ER kan vise kjøringstiden for konfigurasjonen i handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="fef04-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="fef04-192">Dette alternativet fungerer bare for en bestemt bruker og et bestemt firma, og bare for interaktive økter.</span><span class="sxs-lookup"><span data-stu-id="fef04-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="fef04-193">Følg denne fremgangsmåten for å gjøre denne funksjonen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="fef04-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="fef04-194">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fef04-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="fef04-195">På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="fef04-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="fef04-196">Sett alternativet **Vis filgenereringstid** til **Ja** i dialogboksen **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="fef04-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="fef04-197">Kjøringstiden i hendelsesloggen</span><span class="sxs-lookup"><span data-stu-id="fef04-197">Execution time in the event log</span></span>

1. <span data-ttu-id="fef04-198">Åpne Windows Hendelsesliste.</span><span class="sxs-lookup"><span data-stu-id="fef04-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="fef04-199">Åpne **Microsoft-Dynamics-ElectronicReporting/Operational** under **Program- og tjenestelogger**.</span><span class="sxs-lookup"><span data-stu-id="fef04-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="fef04-200">Se etter **FormatMapingRun**-hendelser der **EventID=2** siden disse hendelsene inneholder informasjon om tidsforbruk.</span><span class="sxs-lookup"><span data-stu-id="fef04-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="fef04-201">Trace Parser-sporinger</span><span class="sxs-lookup"><span data-stu-id="fef04-201">Trace parser traces</span></span> 

<span data-ttu-id="fef04-202">Siden ER implementeres i X++, kan du bruke vanlige X++-verktøy til å analysere ytelsen.</span><span class="sxs-lookup"><span data-stu-id="fef04-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="fef04-203">Hvis du vil ha mer informasjon, kan du se [Registrere sporinger ved hjelp av Trace Parser](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="fef04-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="fef04-204">Det er noen få begrensninger ved denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fef04-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="fef04-205">Siden en del av ER implementeres i C#, blir ikke alle detaljene tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="fef04-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="fef04-206">Du kan imidlertid vise informasjon om databruk.</span><span class="sxs-lookup"><span data-stu-id="fef04-206">However, you can view the data usage details.</span></span> <span data-ttu-id="fef04-207">Lange rapportkjøringer kan i tillegg overskride begrensninger ved sporingslagring.</span><span class="sxs-lookup"><span data-stu-id="fef04-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="fef04-208">ER-sporinger</span><span class="sxs-lookup"><span data-stu-id="fef04-208">ER traces</span></span>

<span data-ttu-id="fef04-209">ER kan samle inn sine egne sporinger, og det har visualiserings- og analyseverktøy for disse sporingene.</span><span class="sxs-lookup"><span data-stu-id="fef04-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="fef04-210">Hvis du vil ha mer informasjon, kan du se [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="fef04-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="fef04-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="fef04-211">PerfView</span></span>

<span data-ttu-id="fef04-212">Siden både X++ og ER implementeres over .NET-plattformen, kan du bruke vanlige .NET-verktøy.</span><span class="sxs-lookup"><span data-stu-id="fef04-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="fef04-213">Du kan for eksempel bruke det gratis [PerfView](https://github.com/Microsoft/perfview)-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="fef04-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="fef04-214">Du kan også samle inn data fra kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="fef04-214">You can also collect data from the command line.</span></span> <span data-ttu-id="fef04-215">Windows PowerShell-skriptet nedenfor samler for eksempel inn kjøringstiden til en formatkjøring stoppes på maskinen.</span><span class="sxs-lookup"><span data-stu-id="fef04-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="fef04-216">Det er noen få begrensninger ved denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fef04-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="fef04-217">Du må ha administrativ tilgang til maskinen.</span><span class="sxs-lookup"><span data-stu-id="fef04-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="fef04-218">Du må i tillegg være en erfaren utvikler, fordi det er en bratt læringskurve forbundet med dette.</span><span class="sxs-lookup"><span data-stu-id="fef04-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="fef04-219">Gjøre endringer</span><span class="sxs-lookup"><span data-stu-id="fef04-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="fef04-220">Bruke hurtigbufring</span><span class="sxs-lookup"><span data-stu-id="fef04-220">Use caching</span></span>

<span data-ttu-id="fef04-221">Selv om hurtigbufring reduserer tiden det tar å hente inn data igjen, koster det minne.</span><span class="sxs-lookup"><span data-stu-id="fef04-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="fef04-222">Bruk hurtigbufring i tilfeller der mengden hentede data ikke er særlig stor.</span><span class="sxs-lookup"><span data-stu-id="fef04-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="fef04-223">Hvis du vil ha mer informasjon og et eksempel som viser hvordan du bruker hurtigbufring, kan du se [Forbedre modelltilordningen basert på informasjon fra kjøringssporingen](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="fef04-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="fef04-224">Bruke et hurtigbufret, parameterisert beregnet felt</span><span class="sxs-lookup"><span data-stu-id="fef04-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="fef04-225">Noen ganger må verdier slås opp gjentatte ganger.</span><span class="sxs-lookup"><span data-stu-id="fef04-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="fef04-226">Eksempler omfatter kontonavn og kontonumre.</span><span class="sxs-lookup"><span data-stu-id="fef04-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="fef04-227">Du kan spare tid ved å opprette et beregnet felt som har parametere på det øverste nivået, og deretter legge til feltet i hurtigbufferen.</span><span class="sxs-lookup"><span data-stu-id="fef04-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="fef04-228">Vi anbefaler at du bare bruker denne fremgangsmåten når størrelsen på de hurtigbufrede dataene er liten.</span><span class="sxs-lookup"><span data-stu-id="fef04-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="fef04-229">Hvis du vil ha mer informasjon, kan du se [Forbedre ytelsen for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="fef04-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="fef04-230">Bruke en JOIN-datakilde</span><span class="sxs-lookup"><span data-stu-id="fef04-230">Use a JOIN data source</span></span>

<span data-ttu-id="fef04-231">En **JOIN**-datakilde gjør at flere tilkoblede poster kan hentes av én spørring.</span><span class="sxs-lookup"><span data-stu-id="fef04-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="fef04-232">Du trenger ikke å bruke en egen spørring til å hente hver tilkoblede post.</span><span class="sxs-lookup"><span data-stu-id="fef04-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="fef04-233">Hvis du for eksempel har 1000 linjer og henter varedata for hver linje etter relasjon, har du 1001 spørringer (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="fef04-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="fef04-234">Hvis du bruker en **JOIN**-datakilde, bruker du bare én spørring til å hente de samme dataene.</span><span class="sxs-lookup"><span data-stu-id="fef04-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="fef04-235">Hvis du vil ha mer informasjon, kan du se [Bruke JOIN-datakilder i ER-modelltilordninger til å hente data fra flere programtabeller](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="fef04-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="fef04-236">Bruke FILTER-funksjonen i stedet for WHERE-funksjonen</span><span class="sxs-lookup"><span data-stu-id="fef04-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="fef04-237">**[FILTER](er-functions-list-filter.md)**-funksjonen kjører betingelser på SQL Server, mens **WHERE**-funksjonen henter alle data fra listen, én post om gangen, og bruker betingelsen for hver post.</span><span class="sxs-lookup"><span data-stu-id="fef04-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="fef04-238">La oss si at du ønsker å velge én post blant 1000 poster.</span><span class="sxs-lookup"><span data-stu-id="fef04-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="fef04-239">Hvis du bruker **WHERE**, blir alle 1000 poster hentet.</span><span class="sxs-lookup"><span data-stu-id="fef04-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="fef04-240">Hvis du imidlertid bruker **FILTER**, blir nøyaktig én post hentet.</span><span class="sxs-lookup"><span data-stu-id="fef04-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="fef04-241">**FILTER** kan også bruke indekser på databasesiden.</span><span class="sxs-lookup"><span data-stu-id="fef04-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="fef04-242">Bruke funksjoner for innsamlede data eller en datakilde for akkumulerte data</span><span class="sxs-lookup"><span data-stu-id="fef04-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="fef04-243">Hvis konfigurasjonen har en *GROUP BY*-komponent som viser en oversikt over tidligere hentede data etter rapport, henter komponenten alle dataene på nytt.</span><span class="sxs-lookup"><span data-stu-id="fef04-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="fef04-244">Når du bruker funksjoner for innsamlede data, gjør du at ER kan akkumulere data under første henting.</span><span class="sxs-lookup"><span data-stu-id="fef04-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="fef04-245">Hvis du vil ha mer informasjon, kan du se [ER Konfigurere format for å utføre telling og summering](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="fef04-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="fef04-246">Skrive om deler av konfigurasjonen i X++</span><span class="sxs-lookup"><span data-stu-id="fef04-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="fef04-247">ER støtter oppkallemetoder for tabeller og klasser, inkludert utvidelser.</span><span class="sxs-lookup"><span data-stu-id="fef04-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="fef04-248">Vurder å skrive om deler av modelltilordningen i X++ for å forbedre ytelsen.</span><span class="sxs-lookup"><span data-stu-id="fef04-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="fef04-249">ER kan bruke data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="fef04-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="fef04-250">Klasser (datakilder for **objekt** og **klasse**)</span><span class="sxs-lookup"><span data-stu-id="fef04-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="fef04-251">Tabeller (datakilder for **tabell** og **tabellposter**)</span><span class="sxs-lookup"><span data-stu-id="fef04-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="fef04-252">[ER API-en](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) gir også en måte å sende forhåndsberegnede data fra oppkallekoden på.</span><span class="sxs-lookup"><span data-stu-id="fef04-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="fef04-253">Programserien inneholder en rekke eksempler på denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fef04-253">The application suite contains numerous examples of this approach.</span></span>
