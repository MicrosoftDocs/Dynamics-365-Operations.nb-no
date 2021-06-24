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
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188003"
---
# <a name="overhead-calculation"></a><span data-ttu-id="4b27b-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="4b27b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b27b-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="4b27b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="4b27b-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-105">Term definition</span></span>

<span data-ttu-id="4b27b-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="4b27b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4b27b-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4b27b-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="4b27b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4b27b-109">Leie</span><span class="sxs-lookup"><span data-stu-id="4b27b-109">Rent</span></span>
-   <span data-ttu-id="4b27b-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-110">Electricity</span></span>
-   <span data-ttu-id="4b27b-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="4b27b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4b27b-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="4b27b-112">Overhead calculation overview</span></span>
<span data-ttu-id="4b27b-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="4b27b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4b27b-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="4b27b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4b27b-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="4b27b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4b27b-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="4b27b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4b27b-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4b27b-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="4b27b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4b27b-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="4b27b-119">Version type</span></span>
-   <span data-ttu-id="4b27b-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="4b27b-120">Date and time</span></span>
-   <span data-ttu-id="4b27b-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="4b27b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4b27b-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="4b27b-122">Fiscal year</span></span>
-   <span data-ttu-id="4b27b-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="4b27b-123">Fiscal period</span></span>

<span data-ttu-id="4b27b-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4b27b-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4b27b-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4b27b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4b27b-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="4b27b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4b27b-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="4b27b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4b27b-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="4b27b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4b27b-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="4b27b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4b27b-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4b27b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4b27b-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="4b27b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4b27b-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="4b27b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4b27b-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="4b27b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4b27b-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="4b27b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4b27b-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="4b27b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4b27b-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4b27b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="4b27b-140">Main account</span></span></th>
<th><span data-ttu-id="4b27b-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="4b27b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4b27b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-143">CC099</span></span></td>
<td><span data-ttu-id="4b27b-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-144">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-145">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-145">10001</span></span></td>
<td><span data-ttu-id="4b27b-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-146">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4b27b-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4b27b-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="4b27b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4b27b-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="4b27b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4b27b-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4b27b-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="4b27b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4b27b-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4b27b-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="4b27b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4b27b-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="4b27b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4b27b-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4b27b-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="4b27b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4b27b-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="4b27b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4b27b-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-160">Journal</span></span></th>
<th><span data-ttu-id="4b27b-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="4b27b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b27b-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4b27b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b27b-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-164">00001</span><span class="sxs-lookup"><span data-stu-id="4b27b-164">00001</span></span></td>
<td><span data-ttu-id="4b27b-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4b27b-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="4b27b-166">Fiscal</span></span></td>
<td><span data-ttu-id="4b27b-167">2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-167">2017</span></span></td>
<td><span data-ttu-id="4b27b-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-168">Period 1</span></span></td>
<td><span data-ttu-id="4b27b-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4b27b-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="4b27b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-173">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4b27b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-177">CC099</span></span></td>
<td><span data-ttu-id="4b27b-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-178">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-179">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-179">10001</span></span></td>
<td><span data-ttu-id="4b27b-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-180">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="4b27b-181">Unclassified</span></span></td>
<td><span data-ttu-id="4b27b-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b27b-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="4b27b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-185">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-187">Amount</span></span></th>
<th><span data-ttu-id="4b27b-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-189">CC099</span></span></td>
<td><span data-ttu-id="4b27b-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-190">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-191">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-191">10001</span></span></td>
<td><span data-ttu-id="4b27b-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-192">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="4b27b-193">Unclassified</span></span></td>
<td><span data-ttu-id="4b27b-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-194">10,000.00</span></span></td>
<td><span data-ttu-id="4b27b-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-196">CC099</span></span></td>
<td><span data-ttu-id="4b27b-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-197">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-198">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-198">10001</span></span></td>
<td><span data-ttu-id="4b27b-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-199">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="4b27b-200">Unclassified</span></span></td>
<td><span data-ttu-id="4b27b-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4b27b-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-203">CC099</span></span></td>
<td><span data-ttu-id="4b27b-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-204">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-205">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-205">10001</span></span></td>
<td><span data-ttu-id="4b27b-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-206">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-208">1,000.00</span></span></td>
<td><span data-ttu-id="4b27b-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-210">CC099</span></span></td>
<td><span data-ttu-id="4b27b-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-211">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-212">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-212">10001</span></span></td>
<td><span data-ttu-id="4b27b-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="4b27b-213">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-214">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-215">9,000.00</span></span></td>
<td><span data-ttu-id="4b27b-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="4b27b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4b27b-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4b27b-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="4b27b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4b27b-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="4b27b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4b27b-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4b27b-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="4b27b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4b27b-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="4b27b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4b27b-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="4b27b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4b27b-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="4b27b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4b27b-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="4b27b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4b27b-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="4b27b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-228">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-229">kWt</span><span class="sxs-lookup"><span data-stu-id="4b27b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-230">CC001</span></span></td>
<td><span data-ttu-id="4b27b-231">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-231">HR</span></span></td>
<td><span data-ttu-id="4b27b-232">1 000</span><span class="sxs-lookup"><span data-stu-id="4b27b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-233">CC002</span></span></td>
<td><span data-ttu-id="4b27b-234">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-234">Finance</span></span></td>
<td><span data-ttu-id="4b27b-235">6,000</span><span class="sxs-lookup"><span data-stu-id="4b27b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-236">CC003</span></span></td>
<td><span data-ttu-id="4b27b-237">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-237">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-238">0</span><span class="sxs-lookup"><span data-stu-id="4b27b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="4b27b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-240">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-241">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-244">CC001</span></span></td>
<td><span data-ttu-id="4b27b-245">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-245">HR</span></span></td>
<td><span data-ttu-id="4b27b-246">1 000</span><span class="sxs-lookup"><span data-stu-id="4b27b-246">1,000</span></span></td>
<td><span data-ttu-id="4b27b-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4b27b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4b27b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-249">CC002</span></span></td>
<td><span data-ttu-id="4b27b-250">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-250">Finance</span></span></td>
<td><span data-ttu-id="4b27b-251">6,000</span><span class="sxs-lookup"><span data-stu-id="4b27b-251">6,000</span></span></td>
<td><span data-ttu-id="4b27b-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4b27b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4b27b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-254">CC003</span></span></td>
<td><span data-ttu-id="4b27b-255">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-255">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-256">0</span><span class="sxs-lookup"><span data-stu-id="4b27b-256">0</span></span></td>
<td><span data-ttu-id="4b27b-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4b27b-258">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="4b27b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4b27b-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="4b27b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-261">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-262">Formel</span><span class="sxs-lookup"><span data-stu-id="4b27b-262">Formula</span></span></th>
<th><span data-ttu-id="4b27b-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-263">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-266">CC001</span></span></td>
<td><span data-ttu-id="4b27b-267">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-267">HR</span></span></td>
<td><span data-ttu-id="4b27b-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4b27b-269">1</span><span class="sxs-lookup"><span data-stu-id="4b27b-269">1</span></span></td>
<td><span data-ttu-id="4b27b-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4b27b-271">500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-272">CC002</span></span></td>
<td><span data-ttu-id="4b27b-273">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-273">Finance</span></span></td>
<td><span data-ttu-id="4b27b-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4b27b-275">1</span><span class="sxs-lookup"><span data-stu-id="4b27b-275">1</span></span></td>
<td><span data-ttu-id="4b27b-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4b27b-277">500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-278">CC003</span></span></td>
<td><span data-ttu-id="4b27b-279">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-279">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4b27b-281">0</span><span class="sxs-lookup"><span data-stu-id="4b27b-281">0</span></span></td>
<td><span data-ttu-id="4b27b-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4b27b-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4b27b-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-285">Journal</span></span></th>
<th><span data-ttu-id="4b27b-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="4b27b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b27b-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4b27b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b27b-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-289">00002</span><span class="sxs-lookup"><span data-stu-id="4b27b-289">00002</span></span></td>
<td><span data-ttu-id="4b27b-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4b27b-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="4b27b-291">Fiscal</span></span></td>
<td><span data-ttu-id="4b27b-292">2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-292">2017</span></span></td>
<td><span data-ttu-id="4b27b-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-293">Period 1</span></span></td>
<td><span data-ttu-id="4b27b-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4b27b-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="4b27b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-298">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-302">CC099</span></span></td>
<td><span data-ttu-id="4b27b-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-303">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-304">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-304">10001</span></span></td>
<td><span data-ttu-id="4b27b-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-305">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-309">CC099</span></span></td>
<td><span data-ttu-id="4b27b-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-310">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-311">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-311">10001</span></span></td>
<td><span data-ttu-id="4b27b-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-312">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-313">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b27b-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="4b27b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-317">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-319">Amount</span></span></th>
<th><span data-ttu-id="4b27b-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-321">CC099</span></span></td>
<td><span data-ttu-id="4b27b-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-322">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-323">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-323">10001</span></span></td>
<td><span data-ttu-id="4b27b-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-324">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4b27b-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-328">CC001</span></span></td>
<td><span data-ttu-id="4b27b-329">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-329">HR</span></span></td>
<td><span data-ttu-id="4b27b-330">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-330">10001</span></span></td>
<td><span data-ttu-id="4b27b-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-331">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-333">500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-333">500.00</span></span></td>
<td><span data-ttu-id="4b27b-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-335">CC002</span></span></td>
<td><span data-ttu-id="4b27b-336">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-336">Finance</span></span></td>
<td><span data-ttu-id="4b27b-337">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-337">10001</span></span></td>
<td><span data-ttu-id="4b27b-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-338">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-340">500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-340">500.00</span></span></td>
<td><span data-ttu-id="4b27b-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-342">CC099</span></span></td>
<td><span data-ttu-id="4b27b-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="4b27b-343">Default cost center</span></span></td>
<td><span data-ttu-id="4b27b-344">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-344">10001</span></span></td>
<td><span data-ttu-id="4b27b-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-345">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-346">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4b27b-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-349">CC001</span></span></td>
<td><span data-ttu-id="4b27b-350">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-350">HR</span></span></td>
<td><span data-ttu-id="4b27b-351">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-351">10001</span></span></td>
<td><span data-ttu-id="4b27b-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-352">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-353">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4b27b-354">1,285.71</span></span></td>
<td><span data-ttu-id="4b27b-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-356">CC002</span></span></td>
<td><span data-ttu-id="4b27b-357">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-357">Finance</span></span></td>
<td><span data-ttu-id="4b27b-358">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-358">10001</span></span></td>
<td><span data-ttu-id="4b27b-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="4b27b-359">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-360">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4b27b-361">7,714.29</span></span></td>
<td><span data-ttu-id="4b27b-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="4b27b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4b27b-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="4b27b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4b27b-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4b27b-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="4b27b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4b27b-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="4b27b-367">Define the overhead rate</span></span>

<span data-ttu-id="4b27b-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4b27b-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-370">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="4b27b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-372">Proj 1</span></span></td>
<td><span data-ttu-id="4b27b-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-373">Project 1</span></span></td>
<td><span data-ttu-id="4b27b-374">3</span><span class="sxs-lookup"><span data-stu-id="4b27b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-375">Proj 2</span></span></td>
<td><span data-ttu-id="4b27b-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-376">Project 2</span></span></td>
<td><span data-ttu-id="4b27b-377">1</span><span class="sxs-lookup"><span data-stu-id="4b27b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="4b27b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-379">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-380">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="4b27b-382">Units</span></span></th>
<th><span data-ttu-id="4b27b-383">Sats</span><span class="sxs-lookup"><span data-stu-id="4b27b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-384">CC001</span></span></td>
<td><span data-ttu-id="4b27b-385">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-385">HR</span></span></td>
<td><span data-ttu-id="4b27b-386">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-386">10001</span></span></td>
<td><span data-ttu-id="4b27b-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-387">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-388">1</span><span class="sxs-lookup"><span data-stu-id="4b27b-388">1</span></span></td>
<td><span data-ttu-id="4b27b-389">10</span><span class="sxs-lookup"><span data-stu-id="4b27b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="4b27b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-391">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-392">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-393">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-396">Proj 1</span></span></td>
<td><span data-ttu-id="4b27b-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-397">Project 1</span></span></td>
<td><span data-ttu-id="4b27b-398">3</span><span class="sxs-lookup"><span data-stu-id="4b27b-398">3</span></span></td>
<td><span data-ttu-id="4b27b-399">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-399">10001</span></span></td>
<td><span data-ttu-id="4b27b-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4b27b-401">30,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-402">Proj 2</span></span></td>
<td><span data-ttu-id="4b27b-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-403">Project 2</span></span></td>
<td><span data-ttu-id="4b27b-404">1</span><span class="sxs-lookup"><span data-stu-id="4b27b-404">1</span></span></td>
<td><span data-ttu-id="4b27b-405">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-405">10001</span></span></td>
<td><span data-ttu-id="4b27b-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4b27b-407">10,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4b27b-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-409">Journal</span></span></th>
<th><span data-ttu-id="4b27b-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="4b27b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b27b-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4b27b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b27b-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-413">00003</span><span class="sxs-lookup"><span data-stu-id="4b27b-413">00003</span></span></td>
<td><span data-ttu-id="4b27b-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="4b27b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4b27b-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="4b27b-415">Fiscal</span></span></td>
<td><span data-ttu-id="4b27b-416">2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-416">2017</span></span></td>
<td><span data-ttu-id="4b27b-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-417">Period 1</span></span></td>
<td><span data-ttu-id="4b27b-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4b27b-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="4b27b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-421">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-424">Proj 1</span></span></td>
<td><span data-ttu-id="4b27b-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4b27b-426">3,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-428">Proj 2</span></span></td>
<td><span data-ttu-id="4b27b-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4b27b-430">1,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b27b-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="4b27b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-433">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-435">Amount</span></span></th>
<th><span data-ttu-id="4b27b-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4b27b-437">CC0001</span></span></td>
<td><span data-ttu-id="4b27b-438">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-438">HR</span></span></td>
<td><span data-ttu-id="4b27b-439">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-439">10001</span></span></td>
<td><span data-ttu-id="4b27b-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-440">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-441">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-442">-30.00</span></span></td>
<td><span data-ttu-id="4b27b-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-444">Proj 1</span></span></td>
<td><span data-ttu-id="4b27b-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4b27b-446">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-446">10001</span></span></td>
<td><span data-ttu-id="4b27b-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-447">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-448">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-449">30,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-449">30.00</span></span></td>
<td><span data-ttu-id="4b27b-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-451">CC001</span></span></td>
<td><span data-ttu-id="4b27b-452">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-452">HR</span></span></td>
<td><span data-ttu-id="4b27b-453">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-453">10001</span></span></td>
<td><span data-ttu-id="4b27b-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-454">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-455">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-456">-10.00</span></span></td>
<td><span data-ttu-id="4b27b-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-458">Proj 2</span></span></td>
<td><span data-ttu-id="4b27b-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4b27b-460">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-460">10001</span></span></td>
<td><span data-ttu-id="4b27b-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="4b27b-461">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-462">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-463">10,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-463">10.00</span></span></td>
<td><span data-ttu-id="4b27b-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="4b27b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4b27b-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="4b27b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4b27b-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="4b27b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4b27b-468">Finance støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="4b27b-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="4b27b-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="4b27b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4b27b-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="4b27b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4b27b-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="4b27b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4b27b-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="4b27b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4b27b-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="4b27b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4b27b-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4b27b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4b27b-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="4b27b-475">Define the cost allocation</span></span>

<span data-ttu-id="4b27b-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="4b27b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4b27b-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4b27b-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-479">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="4b27b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-481">CC002</span></span></td>
<td><span data-ttu-id="4b27b-482">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-482">Finance</span></span></td>
<td><span data-ttu-id="4b27b-483">35</span><span class="sxs-lookup"><span data-stu-id="4b27b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-484">CC003</span></span></td>
<td><span data-ttu-id="4b27b-485">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-485">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-486">55</span><span class="sxs-lookup"><span data-stu-id="4b27b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-487">CC004</span></span></td>
<td><span data-ttu-id="4b27b-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-488">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-489">10</span><span class="sxs-lookup"><span data-stu-id="4b27b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4b27b-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-492">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="4b27b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-494">CC003</span></span></td>
<td><span data-ttu-id="4b27b-495">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-495">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-496">65</span><span class="sxs-lookup"><span data-stu-id="4b27b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-497">CC004</span></span></td>
<td><span data-ttu-id="4b27b-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-498">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-499">35</span><span class="sxs-lookup"><span data-stu-id="4b27b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4b27b-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-502">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="4b27b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-504">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-505">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-506">60</span><span class="sxs-lookup"><span data-stu-id="4b27b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-507">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-508">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-509">20</span><span class="sxs-lookup"><span data-stu-id="4b27b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="4b27b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4b27b-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-512">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="4b27b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-514">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-515">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-516">80</span><span class="sxs-lookup"><span data-stu-id="4b27b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-517">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-518">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-519">15</span><span class="sxs-lookup"><span data-stu-id="4b27b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4b27b-520">Statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="4b27b-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4b27b-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="4b27b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4b27b-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="4b27b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-523">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-524">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-526">Amount</span></span></th>
<th><span data-ttu-id="4b27b-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-528">CC002</span></span></td>
<td><span data-ttu-id="4b27b-529">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-529">Finance</span></span></td>
<td><span data-ttu-id="4b27b-530">35</span><span class="sxs-lookup"><span data-stu-id="4b27b-530">35</span></span></td>
<td><span data-ttu-id="4b27b-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4b27b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-532">175.00</span></span></td>
<td><span data-ttu-id="4b27b-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-534">CC003</span></span></td>
<td><span data-ttu-id="4b27b-535">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-535">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-536">55</span><span class="sxs-lookup"><span data-stu-id="4b27b-536">55</span></span></td>
<td><span data-ttu-id="4b27b-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4b27b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-538">275.00</span></span></td>
<td><span data-ttu-id="4b27b-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-540">CC004</span></span></td>
<td><span data-ttu-id="4b27b-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-541">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-542">10</span><span class="sxs-lookup"><span data-stu-id="4b27b-542">10</span></span></td>
<td><span data-ttu-id="4b27b-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4b27b-544">50,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-544">50.00</span></span></td>
<td><span data-ttu-id="4b27b-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-546">CC002</span></span></td>
<td><span data-ttu-id="4b27b-547">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-547">Finance</span></span></td>
<td><span data-ttu-id="4b27b-548">35</span><span class="sxs-lookup"><span data-stu-id="4b27b-548">35</span></span></td>
<td><span data-ttu-id="4b27b-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4b27b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4b27b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-550">436.00</span></span></td>
<td><span data-ttu-id="4b27b-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-552">CC003</span></span></td>
<td><span data-ttu-id="4b27b-553">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-553">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-554">55</span><span class="sxs-lookup"><span data-stu-id="4b27b-554">55</span></span></td>
<td><span data-ttu-id="4b27b-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4b27b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4b27b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4b27b-556">685.14</span></span></td>
<td><span data-ttu-id="4b27b-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-558">CC004</span></span></td>
<td><span data-ttu-id="4b27b-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-559">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-560">10</span><span class="sxs-lookup"><span data-stu-id="4b27b-560">10</span></span></td>
<td><span data-ttu-id="4b27b-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4b27b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4b27b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4b27b-562">124.57</span></span></td>
<td><span data-ttu-id="4b27b-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="4b27b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-565">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-566">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-568">Amount</span></span></th>
<th><span data-ttu-id="4b27b-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-570">CC003</span></span></td>
<td><span data-ttu-id="4b27b-571">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-571">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-572">65</span><span class="sxs-lookup"><span data-stu-id="4b27b-572">65</span></span></td>
<td><span data-ttu-id="4b27b-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4b27b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4b27b-574">438.75</span></span></td>
<td><span data-ttu-id="4b27b-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-576">CC004</span></span></td>
<td><span data-ttu-id="4b27b-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-577">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-578">35</span><span class="sxs-lookup"><span data-stu-id="4b27b-578">35</span></span></td>
<td><span data-ttu-id="4b27b-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4b27b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4b27b-580">236.25</span></span></td>
<td><span data-ttu-id="4b27b-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-582">CC003</span></span></td>
<td><span data-ttu-id="4b27b-583">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-583">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-584">65</span><span class="sxs-lookup"><span data-stu-id="4b27b-584">65</span></span></td>
<td><span data-ttu-id="4b27b-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4b27b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4b27b-586">5,297.69</span></span></td>
<td><span data-ttu-id="4b27b-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-588">CC004</span></span></td>
<td><span data-ttu-id="4b27b-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-589">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-590">35</span><span class="sxs-lookup"><span data-stu-id="4b27b-590">35</span></span></td>
<td><span data-ttu-id="4b27b-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4b27b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4b27b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4b27b-592">2,852.60</span></span></td>
<td><span data-ttu-id="4b27b-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="4b27b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-595">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-596">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-598">Amount</span></span></th>
<th><span data-ttu-id="4b27b-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-600">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-601">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-602">60</span><span class="sxs-lookup"><span data-stu-id="4b27b-602">60</span></span></td>
<td><span data-ttu-id="4b27b-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4b27b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4b27b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4b27b-604">535.31</span></span></td>
<td><span data-ttu-id="4b27b-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-606">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-607">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-608">20</span><span class="sxs-lookup"><span data-stu-id="4b27b-608">20</span></span></td>
<td><span data-ttu-id="4b27b-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4b27b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4b27b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4b27b-610">178.44</span></span></td>
<td><span data-ttu-id="4b27b-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-612">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-613">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-614">60</span><span class="sxs-lookup"><span data-stu-id="4b27b-614">60</span></span></td>
<td><span data-ttu-id="4b27b-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4b27b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4b27b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4b27b-616">4,487.12</span></span></td>
<td><span data-ttu-id="4b27b-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-618">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-619">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-620">20</span><span class="sxs-lookup"><span data-stu-id="4b27b-620">20</span></span></td>
<td><span data-ttu-id="4b27b-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4b27b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4b27b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4b27b-622">1,495.71</span></span></td>
<td><span data-ttu-id="4b27b-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b27b-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="4b27b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-625">Cost object</span></span></th>
<th><span data-ttu-id="4b27b-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="4b27b-626">Magnitude</span></span></th>
<th><span data-ttu-id="4b27b-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="4b27b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4b27b-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-628">Amount</span></span></th>
<th><span data-ttu-id="4b27b-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-630">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-631">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-632">80</span><span class="sxs-lookup"><span data-stu-id="4b27b-632">80</span></span></td>
<td><span data-ttu-id="4b27b-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4b27b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4b27b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4b27b-634">241.05</span></span></td>
<td><span data-ttu-id="4b27b-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-636">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-637">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-638">15</span><span class="sxs-lookup"><span data-stu-id="4b27b-638">15</span></span></td>
<td><span data-ttu-id="4b27b-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4b27b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4b27b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4b27b-640">45.20</span></span></td>
<td><span data-ttu-id="4b27b-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-642">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-643">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-644">80</span><span class="sxs-lookup"><span data-stu-id="4b27b-644">80</span></span></td>
<td><span data-ttu-id="4b27b-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4b27b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4b27b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4b27b-646">2,507.09</span></span></td>
<td><span data-ttu-id="4b27b-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-648">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-649">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-650">15</span><span class="sxs-lookup"><span data-stu-id="4b27b-650">15</span></span></td>
<td><span data-ttu-id="4b27b-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4b27b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4b27b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4b27b-652">470.08</span></span></td>
<td><span data-ttu-id="4b27b-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4b27b-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="4b27b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="4b27b-655">Journal</span></span></th>
<th><span data-ttu-id="4b27b-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="4b27b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b27b-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4b27b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b27b-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-659">00004</span><span class="sxs-lookup"><span data-stu-id="4b27b-659">00004</span></span></td>
<td><span data-ttu-id="4b27b-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="4b27b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4b27b-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="4b27b-661">Fiscal</span></span></td>
<td><span data-ttu-id="4b27b-662">2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-662">2017</span></span></td>
<td><span data-ttu-id="4b27b-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-663">Period 1</span></span></td>
<td><span data-ttu-id="4b27b-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4b27b-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="4b27b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b27b-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-668">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-672">CC001</span></span></td>
<td><span data-ttu-id="4b27b-673">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-673">HR</span></span></td>
<td><span data-ttu-id="4b27b-674">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-674">10001</span></span></td>
<td><span data-ttu-id="4b27b-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-675">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-677">500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-679">CC001</span></span></td>
<td><span data-ttu-id="4b27b-680">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-680">HR</span></span></td>
<td><span data-ttu-id="4b27b-681">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-681">10001</span></span></td>
<td><span data-ttu-id="4b27b-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-682">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-683">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4b27b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-686">CC002</span></span></td>
<td><span data-ttu-id="4b27b-687">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-687">Finance</span></span></td>
<td><span data-ttu-id="4b27b-688">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-688">10001</span></span></td>
<td><span data-ttu-id="4b27b-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-689">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-693">CC002</span></span></td>
<td><span data-ttu-id="4b27b-694">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-694">Finance</span></span></td>
<td><span data-ttu-id="4b27b-695">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-695">10001</span></span></td>
<td><span data-ttu-id="4b27b-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-696">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-697">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4b27b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-700">CC003</span></span></td>
<td><span data-ttu-id="4b27b-701">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-701">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-702">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-702">10001</span></span></td>
<td><span data-ttu-id="4b27b-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-703">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4b27b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-707">CC003</span></span></td>
<td><span data-ttu-id="4b27b-708">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-708">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-709">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-709">10001</span></span></td>
<td><span data-ttu-id="4b27b-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-710">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-711">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4b27b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-714">CC003</span></span></td>
<td><span data-ttu-id="4b27b-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-715">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-716">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-716">10001</span></span></td>
<td><span data-ttu-id="4b27b-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-717">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4b27b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-721">CC003</span></span></td>
<td><span data-ttu-id="4b27b-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-722">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-723">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-723">10001</span></span></td>
<td><span data-ttu-id="4b27b-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-724">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-725">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4b27b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-728">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-729">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-730">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-730">10001</span></span></td>
<td><span data-ttu-id="4b27b-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-731">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4b27b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-735">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-736">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-737">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-737">10001</span></span></td>
<td><span data-ttu-id="4b27b-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-738">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-739">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4b27b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-742">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-743">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-744">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-744">10001</span></span></td>
<td><span data-ttu-id="4b27b-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-745">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4b27b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b27b-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-749">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-750">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-751">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-751">10001</span></span></td>
<td><span data-ttu-id="4b27b-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-752">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-753">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4b27b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b27b-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="4b27b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b27b-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b27b-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-757">Cost element</span></span></th>
<th><span data-ttu-id="4b27b-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="4b27b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4b27b-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="4b27b-759">Amount</span></span></th>
<th><span data-ttu-id="4b27b-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="4b27b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b27b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-761">CC001</span></span></td>
<td><span data-ttu-id="4b27b-762">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-762">HR</span></span></td>
<td><span data-ttu-id="4b27b-763">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-763">10001</span></span></td>
<td><span data-ttu-id="4b27b-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-764">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-766">-500.00</span></span></td>
<td><span data-ttu-id="4b27b-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-768">CC002</span></span></td>
<td><span data-ttu-id="4b27b-769">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-769">Finance</span></span></td>
<td><span data-ttu-id="4b27b-770">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-770">10001</span></span></td>
<td><span data-ttu-id="4b27b-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-771">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-773">175.00</span></span></td>
<td><span data-ttu-id="4b27b-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-775">CC003</span></span></td>
<td><span data-ttu-id="4b27b-776">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-776">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-777">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-777">10001</span></span></td>
<td><span data-ttu-id="4b27b-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-778">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-780">275.00</span></span></td>
<td><span data-ttu-id="4b27b-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-782">CC004</span></span></td>
<td><span data-ttu-id="4b27b-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-783">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-784">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-784">10001</span></span></td>
<td><span data-ttu-id="4b27b-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-785">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-787">50,00</span></span></td>
<td><span data-ttu-id="4b27b-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-789">CC001</span></span></td>
<td><span data-ttu-id="4b27b-790">Personale</span><span class="sxs-lookup"><span data-stu-id="4b27b-790">HR</span></span></td>
<td><span data-ttu-id="4b27b-791">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-791">10001</span></span></td>
<td><span data-ttu-id="4b27b-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-792">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-793">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="4b27b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4b27b-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-796">CC002</span></span></td>
<td><span data-ttu-id="4b27b-797">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-797">Finance</span></span></td>
<td><span data-ttu-id="4b27b-798">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-798">10001</span></span></td>
<td><span data-ttu-id="4b27b-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-799">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-800">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4b27b-801">436.00</span></span></td>
<td><span data-ttu-id="4b27b-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-803">CC003</span></span></td>
<td><span data-ttu-id="4b27b-804">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-804">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-805">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-805">10001</span></span></td>
<td><span data-ttu-id="4b27b-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-806">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-807">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4b27b-808">685.14</span></span></td>
<td><span data-ttu-id="4b27b-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-810">CC004</span></span></td>
<td><span data-ttu-id="4b27b-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-811">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-812">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-812">10001</span></span></td>
<td><span data-ttu-id="4b27b-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-813">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-814">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4b27b-815">124.57</span></span></td>
<td><span data-ttu-id="4b27b-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-817">CC002</span></span></td>
<td><span data-ttu-id="4b27b-818">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-818">Finance</span></span></td>
<td><span data-ttu-id="4b27b-819">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-819">10001</span></span></td>
<td><span data-ttu-id="4b27b-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-820">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-822">-675.00</span></span></td>
<td><span data-ttu-id="4b27b-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-824">CC003</span></span></td>
<td><span data-ttu-id="4b27b-825">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-825">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-826">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-826">10001</span></span></td>
<td><span data-ttu-id="4b27b-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-827">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4b27b-829">438.75</span></span></td>
<td><span data-ttu-id="4b27b-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-831">CC004</span></span></td>
<td><span data-ttu-id="4b27b-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-832">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-833">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-833">10001</span></span></td>
<td><span data-ttu-id="4b27b-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-834">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4b27b-836">236.25</span></span></td>
<td><span data-ttu-id="4b27b-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-838">CC002</span></span></td>
<td><span data-ttu-id="4b27b-839">Finans</span><span class="sxs-lookup"><span data-stu-id="4b27b-839">Finance</span></span></td>
<td><span data-ttu-id="4b27b-840">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-840">10001</span></span></td>
<td><span data-ttu-id="4b27b-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-841">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-842">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="4b27b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4b27b-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-845">CC003</span></span></td>
<td><span data-ttu-id="4b27b-846">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-846">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-847">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-847">10001</span></span></td>
<td><span data-ttu-id="4b27b-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-848">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-849">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4b27b-850">5,297.69</span></span></td>
<td><span data-ttu-id="4b27b-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-852">CC004</span></span></td>
<td><span data-ttu-id="4b27b-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="4b27b-853">Packaging</span></span></td>
<td><span data-ttu-id="4b27b-854">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-854">10001</span></span></td>
<td><span data-ttu-id="4b27b-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-855">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-856">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4b27b-857">2,852.60</span></span></td>
<td><span data-ttu-id="4b27b-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-859">CC003</span></span></td>
<td><span data-ttu-id="4b27b-860">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-860">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-861">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-861">10001</span></span></td>
<td><span data-ttu-id="4b27b-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-862">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="4b27b-864">-713.75</span></span></td>
<td><span data-ttu-id="4b27b-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-866">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-867">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-868">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-868">10001</span></span></td>
<td><span data-ttu-id="4b27b-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-869">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4b27b-871">535.31</span></span></td>
<td><span data-ttu-id="4b27b-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-873">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-874">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-875">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-875">10001</span></span></td>
<td><span data-ttu-id="4b27b-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-876">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4b27b-878">178.44</span></span></td>
<td><span data-ttu-id="4b27b-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-880">CC003</span></span></td>
<td><span data-ttu-id="4b27b-881">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-881">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-882">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-882">10001</span></span></td>
<td><span data-ttu-id="4b27b-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-883">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-884">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="4b27b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4b27b-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-887">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-888">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-889">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-889">10001</span></span></td>
<td><span data-ttu-id="4b27b-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-890">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-891">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4b27b-892">4,487.12</span></span></td>
<td><span data-ttu-id="4b27b-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-894">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-895">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-896">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-896">10001</span></span></td>
<td><span data-ttu-id="4b27b-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-897">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-898">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4b27b-899">1,495.71</span></span></td>
<td><span data-ttu-id="4b27b-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-901">CC003</span></span></td>
<td><span data-ttu-id="4b27b-902">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-902">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-903">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-903">10001</span></span></td>
<td><span data-ttu-id="4b27b-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-904">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="4b27b-906">-286.25</span></span></td>
<td><span data-ttu-id="4b27b-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-908">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-909">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-910">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-910">10001</span></span></td>
<td><span data-ttu-id="4b27b-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-911">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4b27b-913">241.05</span></span></td>
<td><span data-ttu-id="4b27b-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-915">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-916">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-917">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-917">10001</span></span></td>
<td><span data-ttu-id="4b27b-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-918">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4b27b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4b27b-920">45.20</span></span></td>
<td><span data-ttu-id="4b27b-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-922">CC003</span></span></td>
<td><span data-ttu-id="4b27b-923">Samling</span><span class="sxs-lookup"><span data-stu-id="4b27b-923">Assembly</span></span></td>
<td><span data-ttu-id="4b27b-924">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-924">10001</span></span></td>
<td><span data-ttu-id="4b27b-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-925">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-926">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="4b27b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4b27b-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-929">Prod 1</span></span></td>
<td><span data-ttu-id="4b27b-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-930">Product 1</span></span></td>
<td><span data-ttu-id="4b27b-931">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-931">10001</span></span></td>
<td><span data-ttu-id="4b27b-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-932">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-933">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4b27b-934">2,507.09</span></span></td>
<td><span data-ttu-id="4b27b-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b27b-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-936">Prod 2</span></span></td>
<td><span data-ttu-id="4b27b-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-937">Product 2</span></span></td>
<td><span data-ttu-id="4b27b-938">10001</span><span class="sxs-lookup"><span data-stu-id="4b27b-938">10001</span></span></td>
<td><span data-ttu-id="4b27b-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="4b27b-939">Electricity</span></span></td>
<td><span data-ttu-id="4b27b-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-940">Variable cost</span></span></td>
<td><span data-ttu-id="4b27b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4b27b-941">470.08</span></span></td>
<td><span data-ttu-id="4b27b-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="4b27b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4b27b-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="4b27b-943">Conclusion</span></span>
<span data-ttu-id="4b27b-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="4b27b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4b27b-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="4b27b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4b27b-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="4b27b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4b27b-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4b27b-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="4b27b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4b27b-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="4b27b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4b27b-950">Sum</span><span class="sxs-lookup"><span data-stu-id="4b27b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4b27b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4b27b-951">CC099</span></span></th>
<th><span data-ttu-id="4b27b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4b27b-952">CC001</span></span></th>
<th><span data-ttu-id="4b27b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4b27b-953">CC002</span></span></th>
<th><span data-ttu-id="4b27b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4b27b-954">CC003</span></span></th>
<th><span data-ttu-id="4b27b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4b27b-955">CC004</span></span></th>
<th><span data-ttu-id="4b27b-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-956">Proj 1</span></span></th>
<th><span data-ttu-id="4b27b-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-957">Proj 2</span></span></th>
<th><span data-ttu-id="4b27b-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b27b-958">Prod 1</span></span></th>
<th><span data-ttu-id="4b27b-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b27b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4b27b-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="4b27b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4b27b-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="4b27b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-971">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4b27b-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-973">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-975">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4b27b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4b27b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4b27b-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="4b27b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-982">000</span><span class="sxs-lookup"><span data-stu-id="4b27b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-983">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-984">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-985">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-987">30,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-988">10,00</span><span class="sxs-lookup"><span data-stu-id="4b27b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4b27b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4b27b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b27b-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4b27b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4b27b-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="4b27b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4b27b-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="4b27b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4b27b-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="4b27b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4b27b-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="4b27b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4b27b-996">Hvis du vil ha mer informasjon, se [Policy for opprullet kost og beregning av administrasjonskostnader](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="4b27b-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]