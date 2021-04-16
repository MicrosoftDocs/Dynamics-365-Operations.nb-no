---
title: Beregning av indirekte kostnader
description: Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822909"
---
# <a name="overhead-calculation"></a><span data-ttu-id="92704-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="92704-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92704-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="92704-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="92704-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="92704-105">Term definition</span></span>
---------------

<span data-ttu-id="92704-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="92704-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="92704-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="92704-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="92704-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="92704-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="92704-109">Leie</span><span class="sxs-lookup"><span data-stu-id="92704-109">Rent</span></span>
-   <span data-ttu-id="92704-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-110">Electricity</span></span>
-   <span data-ttu-id="92704-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="92704-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="92704-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="92704-112">Overhead calculation overview</span></span>
<span data-ttu-id="92704-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="92704-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="92704-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="92704-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="92704-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="92704-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="92704-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="92704-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="92704-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="92704-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="92704-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="92704-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="92704-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="92704-119">Version type</span></span>
-   <span data-ttu-id="92704-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="92704-120">Date and time</span></span>
-   <span data-ttu-id="92704-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="92704-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="92704-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="92704-122">Fiscal year</span></span>
-   <span data-ttu-id="92704-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="92704-123">Fiscal period</span></span>

<span data-ttu-id="92704-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="92704-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="92704-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="92704-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="92704-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="92704-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="92704-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="92704-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="92704-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="92704-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="92704-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="92704-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="92704-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="92704-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="92704-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="92704-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="92704-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="92704-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="92704-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="92704-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="92704-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="92704-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="92704-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="92704-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="92704-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="92704-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="92704-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="92704-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="92704-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="92704-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="92704-140">Main account</span></span></th>
<th><span data-ttu-id="92704-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="92704-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="92704-143">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-143">CC099</span></span></td>
<td><span data-ttu-id="92704-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-144">Default cost center</span></span></td>
<td><span data-ttu-id="92704-145">10001</span><span class="sxs-lookup"><span data-stu-id="92704-145">10001</span></span></td>
<td><span data-ttu-id="92704-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-146">Electricity</span></span></td>
<td><span data-ttu-id="92704-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="92704-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="92704-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="92704-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="92704-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="92704-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="92704-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-151">Define the cost behavior rule</span></span>

<span data-ttu-id="92704-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="92704-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="92704-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="92704-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="92704-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="92704-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="92704-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="92704-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="92704-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="92704-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="92704-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="92704-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="92704-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="92704-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-160">Journal</span></span></th>
<th><span data-ttu-id="92704-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="92704-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="92704-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="92704-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="92704-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="92704-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-164">00001</span><span class="sxs-lookup"><span data-stu-id="92704-164">00001</span></span></td>
<td><span data-ttu-id="92704-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="92704-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="92704-166">Fiscal</span></span></td>
<td><span data-ttu-id="92704-167">2017</span><span class="sxs-lookup"><span data-stu-id="92704-167">2017</span></span></td>
<td><span data-ttu-id="92704-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-168">Period 1</span></span></td>
<td><span data-ttu-id="92704-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="92704-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="92704-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="92704-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-173">Cost element</span></span></th>
<th><span data-ttu-id="92704-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-174">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="92704-177">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-177">CC099</span></span></td>
<td><span data-ttu-id="92704-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-178">Default cost center</span></span></td>
<td><span data-ttu-id="92704-179">10001</span><span class="sxs-lookup"><span data-stu-id="92704-179">10001</span></span></td>
<td><span data-ttu-id="92704-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-180">Electricity</span></span></td>
<td><span data-ttu-id="92704-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="92704-181">Unclassified</span></span></td>
<td><span data-ttu-id="92704-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="92704-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="92704-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-185">Cost element</span></span></th>
<th><span data-ttu-id="92704-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-186">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-187">Amount</span></span></th>
<th><span data-ttu-id="92704-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-189">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-189">CC099</span></span></td>
<td><span data-ttu-id="92704-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-190">Default cost center</span></span></td>
<td><span data-ttu-id="92704-191">10001</span><span class="sxs-lookup"><span data-stu-id="92704-191">10001</span></span></td>
<td><span data-ttu-id="92704-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-192">Electricity</span></span></td>
<td><span data-ttu-id="92704-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="92704-193">Unclassified</span></span></td>
<td><span data-ttu-id="92704-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-194">10,000.00</span></span></td>
<td><span data-ttu-id="92704-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-196">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-196">CC099</span></span></td>
<td><span data-ttu-id="92704-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-197">Default cost center</span></span></td>
<td><span data-ttu-id="92704-198">10001</span><span class="sxs-lookup"><span data-stu-id="92704-198">10001</span></span></td>
<td><span data-ttu-id="92704-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-199">Electricity</span></span></td>
<td><span data-ttu-id="92704-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="92704-200">Unclassified</span></span></td>
<td><span data-ttu-id="92704-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-201">-10,000.00</span></span></td>
<td><span data-ttu-id="92704-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-203">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-203">CC099</span></span></td>
<td><span data-ttu-id="92704-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-204">Default cost center</span></span></td>
<td><span data-ttu-id="92704-205">10001</span><span class="sxs-lookup"><span data-stu-id="92704-205">10001</span></span></td>
<td><span data-ttu-id="92704-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-206">Electricity</span></span></td>
<td><span data-ttu-id="92704-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-207">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-208">1,000.00</span></span></td>
<td><span data-ttu-id="92704-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-210">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-210">CC099</span></span></td>
<td><span data-ttu-id="92704-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-211">Default cost center</span></span></td>
<td><span data-ttu-id="92704-212">10001</span><span class="sxs-lookup"><span data-stu-id="92704-212">10001</span></span></td>
<td><span data-ttu-id="92704-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="92704-213">Electricity</span></span></td>
<td><span data-ttu-id="92704-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-214">Variable cost</span></span></td>
<td><span data-ttu-id="92704-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="92704-215">9,000.00</span></span></td>
<td><span data-ttu-id="92704-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="92704-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="92704-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="92704-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="92704-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="92704-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="92704-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="92704-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="92704-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="92704-221">Define the cost distribution rule</span></span>

<span data-ttu-id="92704-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="92704-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="92704-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="92704-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="92704-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="92704-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="92704-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="92704-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="92704-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="92704-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="92704-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="92704-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-228">Cost object</span></span></th>
<th><span data-ttu-id="92704-229">kWt</span><span class="sxs-lookup"><span data-stu-id="92704-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-230">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-230">CC001</span></span></td>
<td><span data-ttu-id="92704-231">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-231">HR</span></span></td>
<td><span data-ttu-id="92704-232">1 000</span><span class="sxs-lookup"><span data-stu-id="92704-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-233">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-233">CC002</span></span></td>
<td><span data-ttu-id="92704-234">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-234">Finance</span></span></td>
<td><span data-ttu-id="92704-235">6,000</span><span class="sxs-lookup"><span data-stu-id="92704-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-236">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-236">CC003</span></span></td>
<td><span data-ttu-id="92704-237">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-237">Assembly</span></span></td>
<td><span data-ttu-id="92704-238">0</span><span class="sxs-lookup"><span data-stu-id="92704-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="92704-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-240">Cost object</span></span></th>
<th><span data-ttu-id="92704-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-241">Magnitude</span></span></th>
<th><span data-ttu-id="92704-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-242">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-244">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-244">CC001</span></span></td>
<td><span data-ttu-id="92704-245">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-245">HR</span></span></td>
<td><span data-ttu-id="92704-246">1 000</span><span class="sxs-lookup"><span data-stu-id="92704-246">1,000</span></span></td>
<td><span data-ttu-id="92704-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="92704-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="92704-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-249">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-249">CC002</span></span></td>
<td><span data-ttu-id="92704-250">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-250">Finance</span></span></td>
<td><span data-ttu-id="92704-251">6,000</span><span class="sxs-lookup"><span data-stu-id="92704-251">6,000</span></span></td>
<td><span data-ttu-id="92704-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="92704-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="92704-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-254">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-254">CC003</span></span></td>
<td><span data-ttu-id="92704-255">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-255">Assembly</span></span></td>
<td><span data-ttu-id="92704-256">0</span><span class="sxs-lookup"><span data-stu-id="92704-256">0</span></span></td>
<td><span data-ttu-id="92704-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="92704-258">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="92704-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="92704-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="92704-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-261">Cost object</span></span></th>
<th><span data-ttu-id="92704-262">Formel</span><span class="sxs-lookup"><span data-stu-id="92704-262">Formula</span></span></th>
<th><span data-ttu-id="92704-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-263">Magnitude</span></span></th>
<th><span data-ttu-id="92704-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-264">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-266">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-266">CC001</span></span></td>
<td><span data-ttu-id="92704-267">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-267">HR</span></span></td>
<td><span data-ttu-id="92704-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="92704-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="92704-269">1</span><span class="sxs-lookup"><span data-stu-id="92704-269">1</span></span></td>
<td><span data-ttu-id="92704-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="92704-271">500,00</span><span class="sxs-lookup"><span data-stu-id="92704-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-272">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-272">CC002</span></span></td>
<td><span data-ttu-id="92704-273">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-273">Finance</span></span></td>
<td><span data-ttu-id="92704-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="92704-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="92704-275">1</span><span class="sxs-lookup"><span data-stu-id="92704-275">1</span></span></td>
<td><span data-ttu-id="92704-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="92704-277">500,00</span><span class="sxs-lookup"><span data-stu-id="92704-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-278">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-278">CC003</span></span></td>
<td><span data-ttu-id="92704-279">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-279">Assembly</span></span></td>
<td><span data-ttu-id="92704-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="92704-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="92704-281">0</span><span class="sxs-lookup"><span data-stu-id="92704-281">0</span></span></td>
<td><span data-ttu-id="92704-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="92704-283">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="92704-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-285">Journal</span></span></th>
<th><span data-ttu-id="92704-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="92704-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="92704-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="92704-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="92704-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="92704-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-289">00002</span><span class="sxs-lookup"><span data-stu-id="92704-289">00002</span></span></td>
<td><span data-ttu-id="92704-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="92704-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="92704-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="92704-291">Fiscal</span></span></td>
<td><span data-ttu-id="92704-292">2017</span><span class="sxs-lookup"><span data-stu-id="92704-292">2017</span></span></td>
<td><span data-ttu-id="92704-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-293">Period 1</span></span></td>
<td><span data-ttu-id="92704-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="92704-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="92704-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="92704-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-298">Cost element</span></span></th>
<th><span data-ttu-id="92704-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-299">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-302">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-302">CC099</span></span></td>
<td><span data-ttu-id="92704-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-303">Default cost center</span></span></td>
<td><span data-ttu-id="92704-304">10001</span><span class="sxs-lookup"><span data-stu-id="92704-304">10001</span></span></td>
<td><span data-ttu-id="92704-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-305">Electricity</span></span></td>
<td><span data-ttu-id="92704-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-306">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-309">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-309">CC099</span></span></td>
<td><span data-ttu-id="92704-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-310">Default cost center</span></span></td>
<td><span data-ttu-id="92704-311">10001</span><span class="sxs-lookup"><span data-stu-id="92704-311">10001</span></span></td>
<td><span data-ttu-id="92704-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-312">Electricity</span></span></td>
<td><span data-ttu-id="92704-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-313">Variable cost</span></span></td>
<td><span data-ttu-id="92704-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="92704-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="92704-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="92704-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-317">Cost element</span></span></th>
<th><span data-ttu-id="92704-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-318">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-319">Amount</span></span></th>
<th><span data-ttu-id="92704-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-321">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-321">CC099</span></span></td>
<td><span data-ttu-id="92704-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-322">Default cost center</span></span></td>
<td><span data-ttu-id="92704-323">10001</span><span class="sxs-lookup"><span data-stu-id="92704-323">10001</span></span></td>
<td><span data-ttu-id="92704-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-324">Electricity</span></span></td>
<td><span data-ttu-id="92704-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-325">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-326">-1,000.00</span></span></td>
<td><span data-ttu-id="92704-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-328">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-328">CC001</span></span></td>
<td><span data-ttu-id="92704-329">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-329">HR</span></span></td>
<td><span data-ttu-id="92704-330">10001</span><span class="sxs-lookup"><span data-stu-id="92704-330">10001</span></span></td>
<td><span data-ttu-id="92704-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-331">Electricity</span></span></td>
<td><span data-ttu-id="92704-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-332">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-333">500,00</span><span class="sxs-lookup"><span data-stu-id="92704-333">500.00</span></span></td>
<td><span data-ttu-id="92704-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-335">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-335">CC002</span></span></td>
<td><span data-ttu-id="92704-336">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-336">Finance</span></span></td>
<td><span data-ttu-id="92704-337">10001</span><span class="sxs-lookup"><span data-stu-id="92704-337">10001</span></span></td>
<td><span data-ttu-id="92704-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-338">Electricity</span></span></td>
<td><span data-ttu-id="92704-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-339">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-340">500,00</span><span class="sxs-lookup"><span data-stu-id="92704-340">500.00</span></span></td>
<td><span data-ttu-id="92704-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-342">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-342">CC099</span></span></td>
<td><span data-ttu-id="92704-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="92704-343">Default cost center</span></span></td>
<td><span data-ttu-id="92704-344">10001</span><span class="sxs-lookup"><span data-stu-id="92704-344">10001</span></span></td>
<td><span data-ttu-id="92704-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-345">Electricity</span></span></td>
<td><span data-ttu-id="92704-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-346">Variable cost</span></span></td>
<td><span data-ttu-id="92704-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="92704-347">-9,000.00</span></span></td>
<td><span data-ttu-id="92704-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-349">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-349">CC001</span></span></td>
<td><span data-ttu-id="92704-350">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-350">HR</span></span></td>
<td><span data-ttu-id="92704-351">10001</span><span class="sxs-lookup"><span data-stu-id="92704-351">10001</span></span></td>
<td><span data-ttu-id="92704-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-352">Electricity</span></span></td>
<td><span data-ttu-id="92704-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-353">Variable cost</span></span></td>
<td><span data-ttu-id="92704-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="92704-354">1,285.71</span></span></td>
<td><span data-ttu-id="92704-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-356">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-356">CC002</span></span></td>
<td><span data-ttu-id="92704-357">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-357">Finance</span></span></td>
<td><span data-ttu-id="92704-358">10001</span><span class="sxs-lookup"><span data-stu-id="92704-358">10001</span></span></td>
<td><span data-ttu-id="92704-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="92704-359">Electricity</span></span></td>
<td><span data-ttu-id="92704-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-360">Variable cost</span></span></td>
<td><span data-ttu-id="92704-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="92704-361">7,714.29</span></span></td>
<td><span data-ttu-id="92704-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="92704-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="92704-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="92704-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="92704-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="92704-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="92704-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="92704-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="92704-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="92704-367">Define the overhead rate</span></span>

<span data-ttu-id="92704-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="92704-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="92704-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="92704-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-370">Cost object</span></span></th>
<th><span data-ttu-id="92704-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="92704-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-372">Proj 1</span></span></td>
<td><span data-ttu-id="92704-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="92704-373">Project 1</span></span></td>
<td><span data-ttu-id="92704-374">3</span><span class="sxs-lookup"><span data-stu-id="92704-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-375">Proj 2</span></span></td>
<td><span data-ttu-id="92704-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="92704-376">Project 2</span></span></td>
<td><span data-ttu-id="92704-377">1</span><span class="sxs-lookup"><span data-stu-id="92704-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="92704-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-379">Cost object</span></span></th>
<th><span data-ttu-id="92704-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-380">Cost element</span></span></th>
<th><span data-ttu-id="92704-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-381">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="92704-382">Units</span></span></th>
<th><span data-ttu-id="92704-383">Sats</span><span class="sxs-lookup"><span data-stu-id="92704-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-384">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-384">CC001</span></span></td>
<td><span data-ttu-id="92704-385">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-385">HR</span></span></td>
<td><span data-ttu-id="92704-386">10001</span><span class="sxs-lookup"><span data-stu-id="92704-386">10001</span></span></td>
<td><span data-ttu-id="92704-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-387">Variable cost</span></span></td>
<td><span data-ttu-id="92704-388">1</span><span class="sxs-lookup"><span data-stu-id="92704-388">1</span></span></td>
<td><span data-ttu-id="92704-389">10</span><span class="sxs-lookup"><span data-stu-id="92704-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="92704-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-391">Cost object</span></span></th>
<th><span data-ttu-id="92704-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-392">Magnitude</span></span></th>
<th><span data-ttu-id="92704-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-393">Cost element</span></span></th>
<th><span data-ttu-id="92704-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-394">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-396">Proj 1</span></span></td>
<td><span data-ttu-id="92704-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="92704-397">Project 1</span></span></td>
<td><span data-ttu-id="92704-398">3</span><span class="sxs-lookup"><span data-stu-id="92704-398">3</span></span></td>
<td><span data-ttu-id="92704-399">10001</span><span class="sxs-lookup"><span data-stu-id="92704-399">10001</span></span></td>
<td><span data-ttu-id="92704-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="92704-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="92704-401">30,00</span><span class="sxs-lookup"><span data-stu-id="92704-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-402">Proj 2</span></span></td>
<td><span data-ttu-id="92704-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="92704-403">Project 2</span></span></td>
<td><span data-ttu-id="92704-404">1</span><span class="sxs-lookup"><span data-stu-id="92704-404">1</span></span></td>
<td><span data-ttu-id="92704-405">10001</span><span class="sxs-lookup"><span data-stu-id="92704-405">10001</span></span></td>
<td><span data-ttu-id="92704-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="92704-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="92704-407">10,00</span><span class="sxs-lookup"><span data-stu-id="92704-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="92704-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-409">Journal</span></span></th>
<th><span data-ttu-id="92704-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="92704-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="92704-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="92704-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="92704-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="92704-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-413">00003</span><span class="sxs-lookup"><span data-stu-id="92704-413">00003</span></span></td>
<td><span data-ttu-id="92704-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="92704-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="92704-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="92704-415">Fiscal</span></span></td>
<td><span data-ttu-id="92704-416">2017</span><span class="sxs-lookup"><span data-stu-id="92704-416">2017</span></span></td>
<td><span data-ttu-id="92704-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-417">Period 1</span></span></td>
<td><span data-ttu-id="92704-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="92704-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="92704-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="92704-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-421">Cost object</span></span></th>
<th><span data-ttu-id="92704-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-424">Proj 1</span></span></td>
<td><span data-ttu-id="92704-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="92704-426">3,00</span><span class="sxs-lookup"><span data-stu-id="92704-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-428">Proj 2</span></span></td>
<td><span data-ttu-id="92704-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="92704-430">1,00</span><span class="sxs-lookup"><span data-stu-id="92704-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="92704-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="92704-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-433">Cost element</span></span></th>
<th><span data-ttu-id="92704-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-434">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-435">Amount</span></span></th>
<th><span data-ttu-id="92704-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="92704-437">CC0001</span></span></td>
<td><span data-ttu-id="92704-438">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-438">HR</span></span></td>
<td><span data-ttu-id="92704-439">10001</span><span class="sxs-lookup"><span data-stu-id="92704-439">10001</span></span></td>
<td><span data-ttu-id="92704-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-440">Electricity</span></span></td>
<td><span data-ttu-id="92704-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-441">Variable cost</span></span></td>
<td><span data-ttu-id="92704-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="92704-442">-30.00</span></span></td>
<td><span data-ttu-id="92704-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-444">Proj 1</span></span></td>
<td><span data-ttu-id="92704-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="92704-446">10001</span><span class="sxs-lookup"><span data-stu-id="92704-446">10001</span></span></td>
<td><span data-ttu-id="92704-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-447">Electricity</span></span></td>
<td><span data-ttu-id="92704-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-448">Variable cost</span></span></td>
<td><span data-ttu-id="92704-449">30,00</span><span class="sxs-lookup"><span data-stu-id="92704-449">30.00</span></span></td>
<td><span data-ttu-id="92704-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-451">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-451">CC001</span></span></td>
<td><span data-ttu-id="92704-452">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-452">HR</span></span></td>
<td><span data-ttu-id="92704-453">10001</span><span class="sxs-lookup"><span data-stu-id="92704-453">10001</span></span></td>
<td><span data-ttu-id="92704-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-454">Electricity</span></span></td>
<td><span data-ttu-id="92704-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-455">Variable cost</span></span></td>
<td><span data-ttu-id="92704-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="92704-456">-10.00</span></span></td>
<td><span data-ttu-id="92704-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-458">Proj 2</span></span></td>
<td><span data-ttu-id="92704-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="92704-460">10001</span><span class="sxs-lookup"><span data-stu-id="92704-460">10001</span></span></td>
<td><span data-ttu-id="92704-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="92704-461">Electricity</span></span></td>
<td><span data-ttu-id="92704-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-462">Variable cost</span></span></td>
<td><span data-ttu-id="92704-463">10,00</span><span class="sxs-lookup"><span data-stu-id="92704-463">10.00</span></span></td>
<td><span data-ttu-id="92704-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="92704-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="92704-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="92704-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="92704-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="92704-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="92704-468">Finance støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="92704-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="92704-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="92704-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="92704-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="92704-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="92704-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="92704-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="92704-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="92704-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="92704-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="92704-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="92704-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="92704-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="92704-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="92704-475">Define the cost allocation</span></span>

<span data-ttu-id="92704-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="92704-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="92704-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="92704-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="92704-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="92704-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-479">Cost object</span></span></th>
<th><span data-ttu-id="92704-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="92704-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-481">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-481">CC002</span></span></td>
<td><span data-ttu-id="92704-482">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-482">Finance</span></span></td>
<td><span data-ttu-id="92704-483">35</span><span class="sxs-lookup"><span data-stu-id="92704-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-484">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-484">CC003</span></span></td>
<td><span data-ttu-id="92704-485">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-485">Assembly</span></span></td>
<td><span data-ttu-id="92704-486">55</span><span class="sxs-lookup"><span data-stu-id="92704-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-487">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-487">CC004</span></span></td>
<td><span data-ttu-id="92704-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-488">Packaging</span></span></td>
<td><span data-ttu-id="92704-489">10</span><span class="sxs-lookup"><span data-stu-id="92704-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="92704-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="92704-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="92704-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-492">Cost object</span></span></th>
<th><span data-ttu-id="92704-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="92704-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-494">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-494">CC003</span></span></td>
<td><span data-ttu-id="92704-495">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-495">Assembly</span></span></td>
<td><span data-ttu-id="92704-496">65</span><span class="sxs-lookup"><span data-stu-id="92704-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-497">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-497">CC004</span></span></td>
<td><span data-ttu-id="92704-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-498">Packaging</span></span></td>
<td><span data-ttu-id="92704-499">35</span><span class="sxs-lookup"><span data-stu-id="92704-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="92704-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="92704-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="92704-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-502">Cost object</span></span></th>
<th><span data-ttu-id="92704-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="92704-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-504">Prod 1</span></span></td>
<td><span data-ttu-id="92704-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-505">Product 1</span></span></td>
<td><span data-ttu-id="92704-506">60</span><span class="sxs-lookup"><span data-stu-id="92704-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-507">Prod 2</span></span></td>
<td><span data-ttu-id="92704-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-508">Product 2</span></span></td>
<td><span data-ttu-id="92704-509">20</span><span class="sxs-lookup"><span data-stu-id="92704-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="92704-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="92704-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="92704-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-512">Cost object</span></span></th>
<th><span data-ttu-id="92704-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="92704-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-514">Prod 1</span></span></td>
<td><span data-ttu-id="92704-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-515">Product 1</span></span></td>
<td><span data-ttu-id="92704-516">80</span><span class="sxs-lookup"><span data-stu-id="92704-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-517">Prod 2</span></span></td>
<td><span data-ttu-id="92704-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-518">Product 2</span></span></td>
<td><span data-ttu-id="92704-519">15</span><span class="sxs-lookup"><span data-stu-id="92704-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="92704-520">Statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="92704-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="92704-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="92704-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="92704-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="92704-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-523">Cost object</span></span></th>
<th><span data-ttu-id="92704-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-524">Magnitude</span></span></th>
<th><span data-ttu-id="92704-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-525">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-526">Amount</span></span></th>
<th><span data-ttu-id="92704-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-528">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-528">CC002</span></span></td>
<td><span data-ttu-id="92704-529">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-529">Finance</span></span></td>
<td><span data-ttu-id="92704-530">35</span><span class="sxs-lookup"><span data-stu-id="92704-530">35</span></span></td>
<td><span data-ttu-id="92704-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="92704-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="92704-532">175.00</span><span class="sxs-lookup"><span data-stu-id="92704-532">175.00</span></span></td>
<td><span data-ttu-id="92704-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-534">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-534">CC003</span></span></td>
<td><span data-ttu-id="92704-535">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-535">Assembly</span></span></td>
<td><span data-ttu-id="92704-536">55</span><span class="sxs-lookup"><span data-stu-id="92704-536">55</span></span></td>
<td><span data-ttu-id="92704-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="92704-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="92704-538">275.00</span><span class="sxs-lookup"><span data-stu-id="92704-538">275.00</span></span></td>
<td><span data-ttu-id="92704-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-540">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-540">CC004</span></span></td>
<td><span data-ttu-id="92704-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-541">Packaging</span></span></td>
<td><span data-ttu-id="92704-542">10</span><span class="sxs-lookup"><span data-stu-id="92704-542">10</span></span></td>
<td><span data-ttu-id="92704-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="92704-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="92704-544">50,00</span><span class="sxs-lookup"><span data-stu-id="92704-544">50.00</span></span></td>
<td><span data-ttu-id="92704-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-546">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-546">CC002</span></span></td>
<td><span data-ttu-id="92704-547">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-547">Finance</span></span></td>
<td><span data-ttu-id="92704-548">35</span><span class="sxs-lookup"><span data-stu-id="92704-548">35</span></span></td>
<td><span data-ttu-id="92704-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="92704-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="92704-550">436.00</span><span class="sxs-lookup"><span data-stu-id="92704-550">436.00</span></span></td>
<td><span data-ttu-id="92704-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-552">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-552">CC003</span></span></td>
<td><span data-ttu-id="92704-553">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-553">Assembly</span></span></td>
<td><span data-ttu-id="92704-554">55</span><span class="sxs-lookup"><span data-stu-id="92704-554">55</span></span></td>
<td><span data-ttu-id="92704-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="92704-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="92704-556">685.14</span><span class="sxs-lookup"><span data-stu-id="92704-556">685.14</span></span></td>
<td><span data-ttu-id="92704-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-558">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-558">CC004</span></span></td>
<td><span data-ttu-id="92704-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-559">Packaging</span></span></td>
<td><span data-ttu-id="92704-560">10</span><span class="sxs-lookup"><span data-stu-id="92704-560">10</span></span></td>
<td><span data-ttu-id="92704-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="92704-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="92704-562">124.57</span><span class="sxs-lookup"><span data-stu-id="92704-562">124.57</span></span></td>
<td><span data-ttu-id="92704-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="92704-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-565">Cost object</span></span></th>
<th><span data-ttu-id="92704-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-566">Magnitude</span></span></th>
<th><span data-ttu-id="92704-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-567">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-568">Amount</span></span></th>
<th><span data-ttu-id="92704-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-570">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-570">CC003</span></span></td>
<td><span data-ttu-id="92704-571">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-571">Assembly</span></span></td>
<td><span data-ttu-id="92704-572">65</span><span class="sxs-lookup"><span data-stu-id="92704-572">65</span></span></td>
<td><span data-ttu-id="92704-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="92704-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="92704-574">438.75</span><span class="sxs-lookup"><span data-stu-id="92704-574">438.75</span></span></td>
<td><span data-ttu-id="92704-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-576">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-576">CC004</span></span></td>
<td><span data-ttu-id="92704-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-577">Packaging</span></span></td>
<td><span data-ttu-id="92704-578">35</span><span class="sxs-lookup"><span data-stu-id="92704-578">35</span></span></td>
<td><span data-ttu-id="92704-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="92704-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="92704-580">236.25</span><span class="sxs-lookup"><span data-stu-id="92704-580">236.25</span></span></td>
<td><span data-ttu-id="92704-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-582">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-582">CC003</span></span></td>
<td><span data-ttu-id="92704-583">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-583">Assembly</span></span></td>
<td><span data-ttu-id="92704-584">65</span><span class="sxs-lookup"><span data-stu-id="92704-584">65</span></span></td>
<td><span data-ttu-id="92704-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="92704-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="92704-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="92704-586">5,297.69</span></span></td>
<td><span data-ttu-id="92704-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-588">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-588">CC004</span></span></td>
<td><span data-ttu-id="92704-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-589">Packaging</span></span></td>
<td><span data-ttu-id="92704-590">35</span><span class="sxs-lookup"><span data-stu-id="92704-590">35</span></span></td>
<td><span data-ttu-id="92704-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="92704-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="92704-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="92704-592">2,852.60</span></span></td>
<td><span data-ttu-id="92704-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="92704-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-595">Cost object</span></span></th>
<th><span data-ttu-id="92704-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-596">Magnitude</span></span></th>
<th><span data-ttu-id="92704-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-597">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-598">Amount</span></span></th>
<th><span data-ttu-id="92704-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-600">Prod 1</span></span></td>
<td><span data-ttu-id="92704-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-601">Product 1</span></span></td>
<td><span data-ttu-id="92704-602">60</span><span class="sxs-lookup"><span data-stu-id="92704-602">60</span></span></td>
<td><span data-ttu-id="92704-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="92704-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="92704-604">535.31</span><span class="sxs-lookup"><span data-stu-id="92704-604">535.31</span></span></td>
<td><span data-ttu-id="92704-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-606">Prod 2</span></span></td>
<td><span data-ttu-id="92704-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-607">Product 2</span></span></td>
<td><span data-ttu-id="92704-608">20</span><span class="sxs-lookup"><span data-stu-id="92704-608">20</span></span></td>
<td><span data-ttu-id="92704-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="92704-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="92704-610">178.44</span><span class="sxs-lookup"><span data-stu-id="92704-610">178.44</span></span></td>
<td><span data-ttu-id="92704-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-612">Prod 1</span></span></td>
<td><span data-ttu-id="92704-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-613">Product 1</span></span></td>
<td><span data-ttu-id="92704-614">60</span><span class="sxs-lookup"><span data-stu-id="92704-614">60</span></span></td>
<td><span data-ttu-id="92704-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="92704-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="92704-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="92704-616">4,487.12</span></span></td>
<td><span data-ttu-id="92704-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-618">Prod 2</span></span></td>
<td><span data-ttu-id="92704-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-619">Product 2</span></span></td>
<td><span data-ttu-id="92704-620">20</span><span class="sxs-lookup"><span data-stu-id="92704-620">20</span></span></td>
<td><span data-ttu-id="92704-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="92704-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="92704-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="92704-622">1,495.71</span></span></td>
<td><span data-ttu-id="92704-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92704-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="92704-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-625">Cost object</span></span></th>
<th><span data-ttu-id="92704-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="92704-626">Magnitude</span></span></th>
<th><span data-ttu-id="92704-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="92704-627">Allocation factor</span></span></th>
<th><span data-ttu-id="92704-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-628">Amount</span></span></th>
<th><span data-ttu-id="92704-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-630">Prod 1</span></span></td>
<td><span data-ttu-id="92704-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-631">Product 1</span></span></td>
<td><span data-ttu-id="92704-632">80</span><span class="sxs-lookup"><span data-stu-id="92704-632">80</span></span></td>
<td><span data-ttu-id="92704-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="92704-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="92704-634">241.05</span><span class="sxs-lookup"><span data-stu-id="92704-634">241.05</span></span></td>
<td><span data-ttu-id="92704-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-636">Prod 2</span></span></td>
<td><span data-ttu-id="92704-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-637">Product 2</span></span></td>
<td><span data-ttu-id="92704-638">15</span><span class="sxs-lookup"><span data-stu-id="92704-638">15</span></span></td>
<td><span data-ttu-id="92704-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="92704-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="92704-640">45.20</span><span class="sxs-lookup"><span data-stu-id="92704-640">45.20</span></span></td>
<td><span data-ttu-id="92704-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-642">Prod 1</span></span></td>
<td><span data-ttu-id="92704-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-643">Product 1</span></span></td>
<td><span data-ttu-id="92704-644">80</span><span class="sxs-lookup"><span data-stu-id="92704-644">80</span></span></td>
<td><span data-ttu-id="92704-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="92704-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="92704-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="92704-646">2,507.09</span></span></td>
<td><span data-ttu-id="92704-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-648">Prod 2</span></span></td>
<td><span data-ttu-id="92704-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-649">Product 2</span></span></td>
<td><span data-ttu-id="92704-650">15</span><span class="sxs-lookup"><span data-stu-id="92704-650">15</span></span></td>
<td><span data-ttu-id="92704-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="92704-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="92704-652">470.08</span><span class="sxs-lookup"><span data-stu-id="92704-652">470.08</span></span></td>
<td><span data-ttu-id="92704-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="92704-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="92704-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="92704-655">Journal</span></span></th>
<th><span data-ttu-id="92704-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="92704-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="92704-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="92704-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="92704-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="92704-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-659">00004</span><span class="sxs-lookup"><span data-stu-id="92704-659">00004</span></span></td>
<td><span data-ttu-id="92704-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="92704-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="92704-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="92704-661">Fiscal</span></span></td>
<td><span data-ttu-id="92704-662">2017</span><span class="sxs-lookup"><span data-stu-id="92704-662">2017</span></span></td>
<td><span data-ttu-id="92704-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-663">Period 1</span></span></td>
<td><span data-ttu-id="92704-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="92704-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="92704-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="92704-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92704-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="92704-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-668">Cost element</span></span></th>
<th><span data-ttu-id="92704-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-669">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-672">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-672">CC001</span></span></td>
<td><span data-ttu-id="92704-673">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-673">HR</span></span></td>
<td><span data-ttu-id="92704-674">10001</span><span class="sxs-lookup"><span data-stu-id="92704-674">10001</span></span></td>
<td><span data-ttu-id="92704-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-675">Electricity</span></span></td>
<td><span data-ttu-id="92704-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-676">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-677">500,00</span><span class="sxs-lookup"><span data-stu-id="92704-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-679">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-679">CC001</span></span></td>
<td><span data-ttu-id="92704-680">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-680">HR</span></span></td>
<td><span data-ttu-id="92704-681">10001</span><span class="sxs-lookup"><span data-stu-id="92704-681">10001</span></span></td>
<td><span data-ttu-id="92704-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-682">Electricity</span></span></td>
<td><span data-ttu-id="92704-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-683">Variable cost</span></span></td>
<td><span data-ttu-id="92704-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="92704-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-686">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-686">CC002</span></span></td>
<td><span data-ttu-id="92704-687">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-687">Finance</span></span></td>
<td><span data-ttu-id="92704-688">10001</span><span class="sxs-lookup"><span data-stu-id="92704-688">10001</span></span></td>
<td><span data-ttu-id="92704-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-689">Electricity</span></span></td>
<td><span data-ttu-id="92704-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-690">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-691">675.00</span><span class="sxs-lookup"><span data-stu-id="92704-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-693">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-693">CC002</span></span></td>
<td><span data-ttu-id="92704-694">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-694">Finance</span></span></td>
<td><span data-ttu-id="92704-695">10001</span><span class="sxs-lookup"><span data-stu-id="92704-695">10001</span></span></td>
<td><span data-ttu-id="92704-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-696">Electricity</span></span></td>
<td><span data-ttu-id="92704-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-697">Variable cost</span></span></td>
<td><span data-ttu-id="92704-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="92704-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-700">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-700">CC003</span></span></td>
<td><span data-ttu-id="92704-701">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-701">Assembly</span></span></td>
<td><span data-ttu-id="92704-702">10001</span><span class="sxs-lookup"><span data-stu-id="92704-702">10001</span></span></td>
<td><span data-ttu-id="92704-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-703">Electricity</span></span></td>
<td><span data-ttu-id="92704-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-704">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-705">713.75</span><span class="sxs-lookup"><span data-stu-id="92704-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-707">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-707">CC003</span></span></td>
<td><span data-ttu-id="92704-708">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-708">Assembly</span></span></td>
<td><span data-ttu-id="92704-709">10001</span><span class="sxs-lookup"><span data-stu-id="92704-709">10001</span></span></td>
<td><span data-ttu-id="92704-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-710">Electricity</span></span></td>
<td><span data-ttu-id="92704-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-711">Variable cost</span></span></td>
<td><span data-ttu-id="92704-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="92704-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-714">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-714">CC003</span></span></td>
<td><span data-ttu-id="92704-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-715">Packaging</span></span></td>
<td><span data-ttu-id="92704-716">10001</span><span class="sxs-lookup"><span data-stu-id="92704-716">10001</span></span></td>
<td><span data-ttu-id="92704-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-717">Electricity</span></span></td>
<td><span data-ttu-id="92704-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-718">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-719">286.25</span><span class="sxs-lookup"><span data-stu-id="92704-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-721">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-721">CC003</span></span></td>
<td><span data-ttu-id="92704-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-722">Packaging</span></span></td>
<td><span data-ttu-id="92704-723">10001</span><span class="sxs-lookup"><span data-stu-id="92704-723">10001</span></span></td>
<td><span data-ttu-id="92704-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-724">Electricity</span></span></td>
<td><span data-ttu-id="92704-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-725">Variable cost</span></span></td>
<td><span data-ttu-id="92704-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="92704-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-728">Prod 1</span></span></td>
<td><span data-ttu-id="92704-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-729">Product 1</span></span></td>
<td><span data-ttu-id="92704-730">10001</span><span class="sxs-lookup"><span data-stu-id="92704-730">10001</span></span></td>
<td><span data-ttu-id="92704-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-731">Electricity</span></span></td>
<td><span data-ttu-id="92704-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-732">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-733">776.36</span><span class="sxs-lookup"><span data-stu-id="92704-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-735">Prod 1</span></span></td>
<td><span data-ttu-id="92704-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-736">Product 1</span></span></td>
<td><span data-ttu-id="92704-737">10001</span><span class="sxs-lookup"><span data-stu-id="92704-737">10001</span></span></td>
<td><span data-ttu-id="92704-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-738">Electricity</span></span></td>
<td><span data-ttu-id="92704-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-739">Variable cost</span></span></td>
<td><span data-ttu-id="92704-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="92704-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-742">Prod 2</span></span></td>
<td><span data-ttu-id="92704-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-743">Product 1</span></span></td>
<td><span data-ttu-id="92704-744">10001</span><span class="sxs-lookup"><span data-stu-id="92704-744">10001</span></span></td>
<td><span data-ttu-id="92704-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-745">Electricity</span></span></td>
<td><span data-ttu-id="92704-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-746">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-747">223.64</span><span class="sxs-lookup"><span data-stu-id="92704-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="92704-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-749">Prod 2</span></span></td>
<td><span data-ttu-id="92704-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-750">Product 1</span></span></td>
<td><span data-ttu-id="92704-751">10001</span><span class="sxs-lookup"><span data-stu-id="92704-751">10001</span></span></td>
<td><span data-ttu-id="92704-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-752">Electricity</span></span></td>
<td><span data-ttu-id="92704-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-753">Variable cost</span></span></td>
<td><span data-ttu-id="92704-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="92704-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="92704-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="92704-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="92704-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="92704-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-757">Cost element</span></span></th>
<th><span data-ttu-id="92704-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="92704-758">Cost behavior</span></span></th>
<th><span data-ttu-id="92704-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="92704-759">Amount</span></span></th>
<th><span data-ttu-id="92704-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="92704-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92704-761">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-761">CC001</span></span></td>
<td><span data-ttu-id="92704-762">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-762">HR</span></span></td>
<td><span data-ttu-id="92704-763">10001</span><span class="sxs-lookup"><span data-stu-id="92704-763">10001</span></span></td>
<td><span data-ttu-id="92704-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-764">Electricity</span></span></td>
<td><span data-ttu-id="92704-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-765">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="92704-766">-500.00</span></span></td>
<td><span data-ttu-id="92704-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-768">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-768">CC002</span></span></td>
<td><span data-ttu-id="92704-769">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-769">Finance</span></span></td>
<td><span data-ttu-id="92704-770">10001</span><span class="sxs-lookup"><span data-stu-id="92704-770">10001</span></span></td>
<td><span data-ttu-id="92704-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-771">Electricity</span></span></td>
<td><span data-ttu-id="92704-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-772">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-773">175.00</span><span class="sxs-lookup"><span data-stu-id="92704-773">175.00</span></span></td>
<td><span data-ttu-id="92704-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-775">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-775">CC003</span></span></td>
<td><span data-ttu-id="92704-776">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-776">Assembly</span></span></td>
<td><span data-ttu-id="92704-777">10001</span><span class="sxs-lookup"><span data-stu-id="92704-777">10001</span></span></td>
<td><span data-ttu-id="92704-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-778">Electricity</span></span></td>
<td><span data-ttu-id="92704-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-779">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-780">275.00</span><span class="sxs-lookup"><span data-stu-id="92704-780">275.00</span></span></td>
<td><span data-ttu-id="92704-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-782">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-782">CC004</span></span></td>
<td><span data-ttu-id="92704-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-783">Packaging</span></span></td>
<td><span data-ttu-id="92704-784">10001</span><span class="sxs-lookup"><span data-stu-id="92704-784">10001</span></span></td>
<td><span data-ttu-id="92704-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-785">Electricity</span></span></td>
<td><span data-ttu-id="92704-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-786">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-787">50,00</span><span class="sxs-lookup"><span data-stu-id="92704-787">50,00</span></span></td>
<td><span data-ttu-id="92704-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-789">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-789">CC001</span></span></td>
<td><span data-ttu-id="92704-790">Personale</span><span class="sxs-lookup"><span data-stu-id="92704-790">HR</span></span></td>
<td><span data-ttu-id="92704-791">10001</span><span class="sxs-lookup"><span data-stu-id="92704-791">10001</span></span></td>
<td><span data-ttu-id="92704-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-792">Electricity</span></span></td>
<td><span data-ttu-id="92704-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-793">Variable cost</span></span></td>
<td><span data-ttu-id="92704-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="92704-794">-1,245.71</span></span></td>
<td><span data-ttu-id="92704-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-796">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-796">CC002</span></span></td>
<td><span data-ttu-id="92704-797">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-797">Finance</span></span></td>
<td><span data-ttu-id="92704-798">10001</span><span class="sxs-lookup"><span data-stu-id="92704-798">10001</span></span></td>
<td><span data-ttu-id="92704-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-799">Electricity</span></span></td>
<td><span data-ttu-id="92704-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-800">Variable cost</span></span></td>
<td><span data-ttu-id="92704-801">436.00</span><span class="sxs-lookup"><span data-stu-id="92704-801">436.00</span></span></td>
<td><span data-ttu-id="92704-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-803">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-803">CC003</span></span></td>
<td><span data-ttu-id="92704-804">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-804">Assembly</span></span></td>
<td><span data-ttu-id="92704-805">10001</span><span class="sxs-lookup"><span data-stu-id="92704-805">10001</span></span></td>
<td><span data-ttu-id="92704-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-806">Electricity</span></span></td>
<td><span data-ttu-id="92704-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-807">Variable cost</span></span></td>
<td><span data-ttu-id="92704-808">685.14</span><span class="sxs-lookup"><span data-stu-id="92704-808">685.14</span></span></td>
<td><span data-ttu-id="92704-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-810">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-810">CC004</span></span></td>
<td><span data-ttu-id="92704-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-811">Packaging</span></span></td>
<td><span data-ttu-id="92704-812">10001</span><span class="sxs-lookup"><span data-stu-id="92704-812">10001</span></span></td>
<td><span data-ttu-id="92704-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-813">Electricity</span></span></td>
<td><span data-ttu-id="92704-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-814">Variable cost</span></span></td>
<td><span data-ttu-id="92704-815">124.57</span><span class="sxs-lookup"><span data-stu-id="92704-815">124.57</span></span></td>
<td><span data-ttu-id="92704-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-817">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-817">CC002</span></span></td>
<td><span data-ttu-id="92704-818">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-818">Finance</span></span></td>
<td><span data-ttu-id="92704-819">10001</span><span class="sxs-lookup"><span data-stu-id="92704-819">10001</span></span></td>
<td><span data-ttu-id="92704-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-820">Electricity</span></span></td>
<td><span data-ttu-id="92704-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-821">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="92704-822">-675.00</span></span></td>
<td><span data-ttu-id="92704-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-824">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-824">CC003</span></span></td>
<td><span data-ttu-id="92704-825">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-825">Assembly</span></span></td>
<td><span data-ttu-id="92704-826">10001</span><span class="sxs-lookup"><span data-stu-id="92704-826">10001</span></span></td>
<td><span data-ttu-id="92704-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-827">Electricity</span></span></td>
<td><span data-ttu-id="92704-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-828">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-829">438.75</span><span class="sxs-lookup"><span data-stu-id="92704-829">438.75</span></span></td>
<td><span data-ttu-id="92704-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-831">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-831">CC004</span></span></td>
<td><span data-ttu-id="92704-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-832">Packaging</span></span></td>
<td><span data-ttu-id="92704-833">10001</span><span class="sxs-lookup"><span data-stu-id="92704-833">10001</span></span></td>
<td><span data-ttu-id="92704-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-834">Electricity</span></span></td>
<td><span data-ttu-id="92704-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-835">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-836">236.25</span><span class="sxs-lookup"><span data-stu-id="92704-836">236.25</span></span></td>
<td><span data-ttu-id="92704-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-838">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-838">CC002</span></span></td>
<td><span data-ttu-id="92704-839">Finans</span><span class="sxs-lookup"><span data-stu-id="92704-839">Finance</span></span></td>
<td><span data-ttu-id="92704-840">10001</span><span class="sxs-lookup"><span data-stu-id="92704-840">10001</span></span></td>
<td><span data-ttu-id="92704-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-841">Electricity</span></span></td>
<td><span data-ttu-id="92704-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-842">Variable cost</span></span></td>
<td><span data-ttu-id="92704-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="92704-843">-8,150.29</span></span></td>
<td><span data-ttu-id="92704-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-845">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-845">CC003</span></span></td>
<td><span data-ttu-id="92704-846">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-846">Assembly</span></span></td>
<td><span data-ttu-id="92704-847">10001</span><span class="sxs-lookup"><span data-stu-id="92704-847">10001</span></span></td>
<td><span data-ttu-id="92704-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-848">Electricity</span></span></td>
<td><span data-ttu-id="92704-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-849">Variable cost</span></span></td>
<td><span data-ttu-id="92704-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="92704-850">5,297.69</span></span></td>
<td><span data-ttu-id="92704-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-852">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-852">CC004</span></span></td>
<td><span data-ttu-id="92704-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="92704-853">Packaging</span></span></td>
<td><span data-ttu-id="92704-854">10001</span><span class="sxs-lookup"><span data-stu-id="92704-854">10001</span></span></td>
<td><span data-ttu-id="92704-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-855">Electricity</span></span></td>
<td><span data-ttu-id="92704-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-856">Variable cost</span></span></td>
<td><span data-ttu-id="92704-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="92704-857">2,852.60</span></span></td>
<td><span data-ttu-id="92704-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-859">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-859">CC003</span></span></td>
<td><span data-ttu-id="92704-860">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-860">Assembly</span></span></td>
<td><span data-ttu-id="92704-861">10001</span><span class="sxs-lookup"><span data-stu-id="92704-861">10001</span></span></td>
<td><span data-ttu-id="92704-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-862">Electricity</span></span></td>
<td><span data-ttu-id="92704-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-863">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="92704-864">-713.75</span></span></td>
<td><span data-ttu-id="92704-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-866">Prod 1</span></span></td>
<td><span data-ttu-id="92704-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-867">Product 1</span></span></td>
<td><span data-ttu-id="92704-868">10001</span><span class="sxs-lookup"><span data-stu-id="92704-868">10001</span></span></td>
<td><span data-ttu-id="92704-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-869">Electricity</span></span></td>
<td><span data-ttu-id="92704-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-870">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-871">535.31</span><span class="sxs-lookup"><span data-stu-id="92704-871">535.31</span></span></td>
<td><span data-ttu-id="92704-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-873">Prod 2</span></span></td>
<td><span data-ttu-id="92704-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-874">Product 2</span></span></td>
<td><span data-ttu-id="92704-875">10001</span><span class="sxs-lookup"><span data-stu-id="92704-875">10001</span></span></td>
<td><span data-ttu-id="92704-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-876">Electricity</span></span></td>
<td><span data-ttu-id="92704-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-877">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-878">178.44</span><span class="sxs-lookup"><span data-stu-id="92704-878">178.44</span></span></td>
<td><span data-ttu-id="92704-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-880">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-880">CC003</span></span></td>
<td><span data-ttu-id="92704-881">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-881">Assembly</span></span></td>
<td><span data-ttu-id="92704-882">10001</span><span class="sxs-lookup"><span data-stu-id="92704-882">10001</span></span></td>
<td><span data-ttu-id="92704-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-883">Electricity</span></span></td>
<td><span data-ttu-id="92704-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-884">Variable cost</span></span></td>
<td><span data-ttu-id="92704-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="92704-885">-5,982.83</span></span></td>
<td><span data-ttu-id="92704-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-887">Prod 1</span></span></td>
<td><span data-ttu-id="92704-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-888">Product 1</span></span></td>
<td><span data-ttu-id="92704-889">10001</span><span class="sxs-lookup"><span data-stu-id="92704-889">10001</span></span></td>
<td><span data-ttu-id="92704-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-890">Electricity</span></span></td>
<td><span data-ttu-id="92704-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-891">Variable cost</span></span></td>
<td><span data-ttu-id="92704-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="92704-892">4,487.12</span></span></td>
<td><span data-ttu-id="92704-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-894">Prod 2</span></span></td>
<td><span data-ttu-id="92704-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-895">Product 2</span></span></td>
<td><span data-ttu-id="92704-896">10001</span><span class="sxs-lookup"><span data-stu-id="92704-896">10001</span></span></td>
<td><span data-ttu-id="92704-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-897">Electricity</span></span></td>
<td><span data-ttu-id="92704-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-898">Variable cost</span></span></td>
<td><span data-ttu-id="92704-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="92704-899">1,495.71</span></span></td>
<td><span data-ttu-id="92704-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-901">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-901">CC003</span></span></td>
<td><span data-ttu-id="92704-902">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-902">Assembly</span></span></td>
<td><span data-ttu-id="92704-903">10001</span><span class="sxs-lookup"><span data-stu-id="92704-903">10001</span></span></td>
<td><span data-ttu-id="92704-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-904">Electricity</span></span></td>
<td><span data-ttu-id="92704-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-905">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="92704-906">-286.25</span></span></td>
<td><span data-ttu-id="92704-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-908">Prod 1</span></span></td>
<td><span data-ttu-id="92704-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-909">Product 1</span></span></td>
<td><span data-ttu-id="92704-910">10001</span><span class="sxs-lookup"><span data-stu-id="92704-910">10001</span></span></td>
<td><span data-ttu-id="92704-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-911">Electricity</span></span></td>
<td><span data-ttu-id="92704-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-912">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-913">241.05</span><span class="sxs-lookup"><span data-stu-id="92704-913">241.05</span></span></td>
<td><span data-ttu-id="92704-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-915">Prod 2</span></span></td>
<td><span data-ttu-id="92704-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-916">Product 2</span></span></td>
<td><span data-ttu-id="92704-917">10001</span><span class="sxs-lookup"><span data-stu-id="92704-917">10001</span></span></td>
<td><span data-ttu-id="92704-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-918">Electricity</span></span></td>
<td><span data-ttu-id="92704-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-919">Fixed cost</span></span></td>
<td><span data-ttu-id="92704-920">45.20</span><span class="sxs-lookup"><span data-stu-id="92704-920">45.20</span></span></td>
<td><span data-ttu-id="92704-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-922">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-922">CC003</span></span></td>
<td><span data-ttu-id="92704-923">Samling</span><span class="sxs-lookup"><span data-stu-id="92704-923">Assembly</span></span></td>
<td><span data-ttu-id="92704-924">10001</span><span class="sxs-lookup"><span data-stu-id="92704-924">10001</span></span></td>
<td><span data-ttu-id="92704-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-925">Electricity</span></span></td>
<td><span data-ttu-id="92704-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-926">Variable cost</span></span></td>
<td><span data-ttu-id="92704-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="92704-927">-2,977.17</span></span></td>
<td><span data-ttu-id="92704-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-929">Prod 1</span></span></td>
<td><span data-ttu-id="92704-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="92704-930">Product 1</span></span></td>
<td><span data-ttu-id="92704-931">10001</span><span class="sxs-lookup"><span data-stu-id="92704-931">10001</span></span></td>
<td><span data-ttu-id="92704-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-932">Electricity</span></span></td>
<td><span data-ttu-id="92704-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-933">Variable cost</span></span></td>
<td><span data-ttu-id="92704-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="92704-934">2,507.09</span></span></td>
<td><span data-ttu-id="92704-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92704-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-936">Prod 2</span></span></td>
<td><span data-ttu-id="92704-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="92704-937">Product 2</span></span></td>
<td><span data-ttu-id="92704-938">10001</span><span class="sxs-lookup"><span data-stu-id="92704-938">10001</span></span></td>
<td><span data-ttu-id="92704-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="92704-939">Electricity</span></span></td>
<td><span data-ttu-id="92704-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-940">Variable cost</span></span></td>
<td><span data-ttu-id="92704-941">470.08</span><span class="sxs-lookup"><span data-stu-id="92704-941">470.08</span></span></td>
<td><span data-ttu-id="92704-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="92704-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="92704-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="92704-943">Conclusion</span></span>
<span data-ttu-id="92704-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="92704-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="92704-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="92704-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="92704-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="92704-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="92704-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="92704-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="92704-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="92704-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="92704-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="92704-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="92704-950">Sum</span><span class="sxs-lookup"><span data-stu-id="92704-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="92704-951">CC099</span><span class="sxs-lookup"><span data-stu-id="92704-951">CC099</span></span></th>
<th><span data-ttu-id="92704-952">CC001</span><span class="sxs-lookup"><span data-stu-id="92704-952">CC001</span></span></th>
<th><span data-ttu-id="92704-953">CC002</span><span class="sxs-lookup"><span data-stu-id="92704-953">CC002</span></span></th>
<th><span data-ttu-id="92704-954">CC003</span><span class="sxs-lookup"><span data-stu-id="92704-954">CC003</span></span></th>
<th><span data-ttu-id="92704-955">CC004</span><span class="sxs-lookup"><span data-stu-id="92704-955">CC004</span></span></th>
<th><span data-ttu-id="92704-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="92704-956">Proj 1</span></span></th>
<th><span data-ttu-id="92704-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="92704-957">Proj 2</span></span></th>
<th><span data-ttu-id="92704-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="92704-958">Prod 1</span></span></th>
<th><span data-ttu-id="92704-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="92704-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="92704-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="92704-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="92704-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="92704-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="92704-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="92704-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="92704-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-971">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="92704-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-973">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-974">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-975">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-976">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-977">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="92704-978">776.36</span><span class="sxs-lookup"><span data-stu-id="92704-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-979">223.64</span><span class="sxs-lookup"><span data-stu-id="92704-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="92704-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="92704-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-982">000</span><span class="sxs-lookup"><span data-stu-id="92704-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-983">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-984">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-985">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-986">0,00</span><span class="sxs-lookup"><span data-stu-id="92704-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-987">30,00</span><span class="sxs-lookup"><span data-stu-id="92704-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-988">10,00</span><span class="sxs-lookup"><span data-stu-id="92704-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="92704-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="92704-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="92704-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="92704-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="92704-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="92704-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="92704-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="92704-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="92704-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="92704-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="92704-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="92704-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="92704-996">Hvis du vil ha mer informasjon, se [Policy for opprullet kost og beregning av administrasjonskostnader](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="92704-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]