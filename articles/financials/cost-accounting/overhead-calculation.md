---
title: Beregning av indirekte kostnader
description: Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544061"
---
# <a name="overhead-calculation"></a><span data-ttu-id="dd724-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="dd724-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd724-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="dd724-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="dd724-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="dd724-105">Term definition</span></span>
---------------

<span data-ttu-id="dd724-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="dd724-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="dd724-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="dd724-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="dd724-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="dd724-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="dd724-109">Leie</span><span class="sxs-lookup"><span data-stu-id="dd724-109">Rent</span></span>
-   <span data-ttu-id="dd724-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-110">Electricity</span></span>
-   <span data-ttu-id="dd724-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="dd724-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="dd724-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="dd724-112">Overhead calculation overview</span></span>
<span data-ttu-id="dd724-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="dd724-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="dd724-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="dd724-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="dd724-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="dd724-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="dd724-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="dd724-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="dd724-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="dd724-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="dd724-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="dd724-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="dd724-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="dd724-119">Version type</span></span>
-   <span data-ttu-id="dd724-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="dd724-120">Date and time</span></span>
-   <span data-ttu-id="dd724-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="dd724-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="dd724-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="dd724-122">Fiscal year</span></span>
-   <span data-ttu-id="dd724-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="dd724-123">Fiscal period</span></span>

<span data-ttu-id="dd724-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="dd724-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="dd724-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="dd724-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="dd724-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="dd724-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="dd724-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="dd724-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="dd724-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="dd724-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="dd724-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="dd724-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="dd724-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="dd724-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="dd724-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="dd724-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="dd724-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="dd724-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="dd724-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="dd724-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="dd724-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="dd724-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="dd724-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="dd724-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="dd724-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="dd724-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="dd724-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="dd724-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="dd724-140">Main account</span></span></th>
<th><span data-ttu-id="dd724-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="dd724-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="dd724-143">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-143">CC099</span></span></td>
<td><span data-ttu-id="dd724-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-144">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-145">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-145">10001</span></span></td>
<td><span data-ttu-id="dd724-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-146">Electricity</span></span></td>
<td><span data-ttu-id="dd724-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="dd724-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="dd724-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="dd724-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="dd724-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="dd724-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="dd724-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-151">Define the cost behavior rule</span></span>

<span data-ttu-id="dd724-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="dd724-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="dd724-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="dd724-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="dd724-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="dd724-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="dd724-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="dd724-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="dd724-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="dd724-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="dd724-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="dd724-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="dd724-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="dd724-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-160">Journal</span></span></th>
<th><span data-ttu-id="dd724-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="dd724-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd724-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="dd724-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd724-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="dd724-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-164">00001</span><span class="sxs-lookup"><span data-stu-id="dd724-164">00001</span></span></td>
<td><span data-ttu-id="dd724-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="dd724-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="dd724-166">Fiscal</span></span></td>
<td><span data-ttu-id="dd724-167">2017</span><span class="sxs-lookup"><span data-stu-id="dd724-167">2017</span></span></td>
<td><span data-ttu-id="dd724-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-168">Period 1</span></span></td>
<td><span data-ttu-id="dd724-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dd724-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="dd724-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-173">Cost element</span></span></th>
<th><span data-ttu-id="dd724-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-174">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="dd724-177">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-177">CC099</span></span></td>
<td><span data-ttu-id="dd724-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-178">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-179">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-179">10001</span></span></td>
<td><span data-ttu-id="dd724-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-180">Electricity</span></span></td>
<td><span data-ttu-id="dd724-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="dd724-181">Unclassified</span></span></td>
<td><span data-ttu-id="dd724-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd724-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="dd724-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-185">Cost element</span></span></th>
<th><span data-ttu-id="dd724-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-186">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-187">Amount</span></span></th>
<th><span data-ttu-id="dd724-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-189">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-189">CC099</span></span></td>
<td><span data-ttu-id="dd724-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-190">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-191">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-191">10001</span></span></td>
<td><span data-ttu-id="dd724-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-192">Electricity</span></span></td>
<td><span data-ttu-id="dd724-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="dd724-193">Unclassified</span></span></td>
<td><span data-ttu-id="dd724-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-194">10,000.00</span></span></td>
<td><span data-ttu-id="dd724-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-196">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-196">CC099</span></span></td>
<td><span data-ttu-id="dd724-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-197">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-198">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-198">10001</span></span></td>
<td><span data-ttu-id="dd724-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-199">Electricity</span></span></td>
<td><span data-ttu-id="dd724-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="dd724-200">Unclassified</span></span></td>
<td><span data-ttu-id="dd724-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-201">-10,000.00</span></span></td>
<td><span data-ttu-id="dd724-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-203">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-203">CC099</span></span></td>
<td><span data-ttu-id="dd724-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-204">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-205">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-205">10001</span></span></td>
<td><span data-ttu-id="dd724-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-206">Electricity</span></span></td>
<td><span data-ttu-id="dd724-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-207">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-208">1,000.00</span></span></td>
<td><span data-ttu-id="dd724-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-210">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-210">CC099</span></span></td>
<td><span data-ttu-id="dd724-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-211">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-212">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-212">10001</span></span></td>
<td><span data-ttu-id="dd724-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="dd724-213">Electricity</span></span></td>
<td><span data-ttu-id="dd724-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-214">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd724-215">9,000.00</span></span></td>
<td><span data-ttu-id="dd724-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="dd724-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="dd724-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="dd724-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="dd724-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="dd724-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="dd724-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="dd724-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="dd724-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="dd724-221">Define the cost distribution rule</span></span>

<span data-ttu-id="dd724-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="dd724-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="dd724-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="dd724-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="dd724-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="dd724-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="dd724-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="dd724-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="dd724-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="dd724-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="dd724-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="dd724-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-228">Cost object</span></span></th>
<th><span data-ttu-id="dd724-229">kWt</span><span class="sxs-lookup"><span data-stu-id="dd724-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-230">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-230">CC001</span></span></td>
<td><span data-ttu-id="dd724-231">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-231">HR</span></span></td>
<td><span data-ttu-id="dd724-232">1 000</span><span class="sxs-lookup"><span data-stu-id="dd724-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-233">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-233">CC002</span></span></td>
<td><span data-ttu-id="dd724-234">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-234">Finance</span></span></td>
<td><span data-ttu-id="dd724-235">6,000</span><span class="sxs-lookup"><span data-stu-id="dd724-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-236">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-236">CC003</span></span></td>
<td><span data-ttu-id="dd724-237">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-237">Assembly</span></span></td>
<td><span data-ttu-id="dd724-238">0</span><span class="sxs-lookup"><span data-stu-id="dd724-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="dd724-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-240">Cost object</span></span></th>
<th><span data-ttu-id="dd724-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-241">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-242">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-244">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-244">CC001</span></span></td>
<td><span data-ttu-id="dd724-245">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-245">HR</span></span></td>
<td><span data-ttu-id="dd724-246">1 000</span><span class="sxs-lookup"><span data-stu-id="dd724-246">1,000</span></span></td>
<td><span data-ttu-id="dd724-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dd724-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="dd724-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-249">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-249">CC002</span></span></td>
<td><span data-ttu-id="dd724-250">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-250">Finance</span></span></td>
<td><span data-ttu-id="dd724-251">6,000</span><span class="sxs-lookup"><span data-stu-id="dd724-251">6,000</span></span></td>
<td><span data-ttu-id="dd724-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dd724-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="dd724-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-254">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-254">CC003</span></span></td>
<td><span data-ttu-id="dd724-255">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-255">Assembly</span></span></td>
<td><span data-ttu-id="dd724-256">0</span><span class="sxs-lookup"><span data-stu-id="dd724-256">0</span></span></td>
<td><span data-ttu-id="dd724-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dd724-258">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="dd724-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="dd724-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="dd724-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-261">Cost object</span></span></th>
<th><span data-ttu-id="dd724-262">Formel</span><span class="sxs-lookup"><span data-stu-id="dd724-262">Formula</span></span></th>
<th><span data-ttu-id="dd724-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-263">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-264">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-266">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-266">CC001</span></span></td>
<td><span data-ttu-id="dd724-267">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-267">HR</span></span></td>
<td><span data-ttu-id="dd724-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dd724-269">1</span><span class="sxs-lookup"><span data-stu-id="dd724-269">1</span></span></td>
<td><span data-ttu-id="dd724-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dd724-271">500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-272">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-272">CC002</span></span></td>
<td><span data-ttu-id="dd724-273">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-273">Finance</span></span></td>
<td><span data-ttu-id="dd724-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dd724-275">1</span><span class="sxs-lookup"><span data-stu-id="dd724-275">1</span></span></td>
<td><span data-ttu-id="dd724-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dd724-277">500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-278">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-278">CC003</span></span></td>
<td><span data-ttu-id="dd724-279">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-279">Assembly</span></span></td>
<td><span data-ttu-id="dd724-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dd724-281">0</span><span class="sxs-lookup"><span data-stu-id="dd724-281">0</span></span></td>
<td><span data-ttu-id="dd724-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dd724-283">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="dd724-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-285">Journal</span></span></th>
<th><span data-ttu-id="dd724-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="dd724-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd724-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="dd724-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd724-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="dd724-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-289">00002</span><span class="sxs-lookup"><span data-stu-id="dd724-289">00002</span></span></td>
<td><span data-ttu-id="dd724-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="dd724-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="dd724-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="dd724-291">Fiscal</span></span></td>
<td><span data-ttu-id="dd724-292">2017</span><span class="sxs-lookup"><span data-stu-id="dd724-292">2017</span></span></td>
<td><span data-ttu-id="dd724-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-293">Period 1</span></span></td>
<td><span data-ttu-id="dd724-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dd724-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="dd724-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-298">Cost element</span></span></th>
<th><span data-ttu-id="dd724-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-299">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-302">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-302">CC099</span></span></td>
<td><span data-ttu-id="dd724-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-303">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-304">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-304">10001</span></span></td>
<td><span data-ttu-id="dd724-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-305">Electricity</span></span></td>
<td><span data-ttu-id="dd724-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-306">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-309">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-309">CC099</span></span></td>
<td><span data-ttu-id="dd724-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-310">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-311">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-311">10001</span></span></td>
<td><span data-ttu-id="dd724-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-312">Electricity</span></span></td>
<td><span data-ttu-id="dd724-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-313">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd724-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd724-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="dd724-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-317">Cost element</span></span></th>
<th><span data-ttu-id="dd724-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-318">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-319">Amount</span></span></th>
<th><span data-ttu-id="dd724-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-321">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-321">CC099</span></span></td>
<td><span data-ttu-id="dd724-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-322">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-323">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-323">10001</span></span></td>
<td><span data-ttu-id="dd724-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-324">Electricity</span></span></td>
<td><span data-ttu-id="dd724-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-325">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-326">-1,000.00</span></span></td>
<td><span data-ttu-id="dd724-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-328">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-328">CC001</span></span></td>
<td><span data-ttu-id="dd724-329">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-329">HR</span></span></td>
<td><span data-ttu-id="dd724-330">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-330">10001</span></span></td>
<td><span data-ttu-id="dd724-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-331">Electricity</span></span></td>
<td><span data-ttu-id="dd724-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-332">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-333">500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-333">500.00</span></span></td>
<td><span data-ttu-id="dd724-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-335">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-335">CC002</span></span></td>
<td><span data-ttu-id="dd724-336">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-336">Finance</span></span></td>
<td><span data-ttu-id="dd724-337">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-337">10001</span></span></td>
<td><span data-ttu-id="dd724-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-338">Electricity</span></span></td>
<td><span data-ttu-id="dd724-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-339">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-340">500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-340">500.00</span></span></td>
<td><span data-ttu-id="dd724-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-342">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-342">CC099</span></span></td>
<td><span data-ttu-id="dd724-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="dd724-343">Default cost center</span></span></td>
<td><span data-ttu-id="dd724-344">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-344">10001</span></span></td>
<td><span data-ttu-id="dd724-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-345">Electricity</span></span></td>
<td><span data-ttu-id="dd724-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-346">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="dd724-347">-9,000.00</span></span></td>
<td><span data-ttu-id="dd724-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-349">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-349">CC001</span></span></td>
<td><span data-ttu-id="dd724-350">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-350">HR</span></span></td>
<td><span data-ttu-id="dd724-351">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-351">10001</span></span></td>
<td><span data-ttu-id="dd724-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-352">Electricity</span></span></td>
<td><span data-ttu-id="dd724-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-353">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="dd724-354">1,285.71</span></span></td>
<td><span data-ttu-id="dd724-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-356">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-356">CC002</span></span></td>
<td><span data-ttu-id="dd724-357">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-357">Finance</span></span></td>
<td><span data-ttu-id="dd724-358">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-358">10001</span></span></td>
<td><span data-ttu-id="dd724-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="dd724-359">Electricity</span></span></td>
<td><span data-ttu-id="dd724-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-360">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="dd724-361">7,714.29</span></span></td>
<td><span data-ttu-id="dd724-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="dd724-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="dd724-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="dd724-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="dd724-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="dd724-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="dd724-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="dd724-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="dd724-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="dd724-367">Define the overhead rate</span></span>

<span data-ttu-id="dd724-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="dd724-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="dd724-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="dd724-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-370">Cost object</span></span></th>
<th><span data-ttu-id="dd724-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="dd724-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-372">Proj 1</span></span></td>
<td><span data-ttu-id="dd724-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-373">Project 1</span></span></td>
<td><span data-ttu-id="dd724-374">3</span><span class="sxs-lookup"><span data-stu-id="dd724-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-375">Proj 2</span></span></td>
<td><span data-ttu-id="dd724-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-376">Project 2</span></span></td>
<td><span data-ttu-id="dd724-377">1</span><span class="sxs-lookup"><span data-stu-id="dd724-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="dd724-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-379">Cost object</span></span></th>
<th><span data-ttu-id="dd724-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-380">Cost element</span></span></th>
<th><span data-ttu-id="dd724-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-381">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="dd724-382">Units</span></span></th>
<th><span data-ttu-id="dd724-383">Sats</span><span class="sxs-lookup"><span data-stu-id="dd724-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-384">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-384">CC001</span></span></td>
<td><span data-ttu-id="dd724-385">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-385">HR</span></span></td>
<td><span data-ttu-id="dd724-386">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-386">10001</span></span></td>
<td><span data-ttu-id="dd724-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-387">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-388">1</span><span class="sxs-lookup"><span data-stu-id="dd724-388">1</span></span></td>
<td><span data-ttu-id="dd724-389">10</span><span class="sxs-lookup"><span data-stu-id="dd724-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="dd724-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-391">Cost object</span></span></th>
<th><span data-ttu-id="dd724-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-392">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-393">Cost element</span></span></th>
<th><span data-ttu-id="dd724-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-394">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-396">Proj 1</span></span></td>
<td><span data-ttu-id="dd724-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-397">Project 1</span></span></td>
<td><span data-ttu-id="dd724-398">3</span><span class="sxs-lookup"><span data-stu-id="dd724-398">3</span></span></td>
<td><span data-ttu-id="dd724-399">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-399">10001</span></span></td>
<td><span data-ttu-id="dd724-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="dd724-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="dd724-401">30,00</span><span class="sxs-lookup"><span data-stu-id="dd724-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-402">Proj 2</span></span></td>
<td><span data-ttu-id="dd724-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-403">Project 2</span></span></td>
<td><span data-ttu-id="dd724-404">1</span><span class="sxs-lookup"><span data-stu-id="dd724-404">1</span></span></td>
<td><span data-ttu-id="dd724-405">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-405">10001</span></span></td>
<td><span data-ttu-id="dd724-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="dd724-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="dd724-407">10,00</span><span class="sxs-lookup"><span data-stu-id="dd724-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="dd724-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-409">Journal</span></span></th>
<th><span data-ttu-id="dd724-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="dd724-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd724-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="dd724-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd724-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="dd724-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-413">00003</span><span class="sxs-lookup"><span data-stu-id="dd724-413">00003</span></span></td>
<td><span data-ttu-id="dd724-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="dd724-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="dd724-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="dd724-415">Fiscal</span></span></td>
<td><span data-ttu-id="dd724-416">2017</span><span class="sxs-lookup"><span data-stu-id="dd724-416">2017</span></span></td>
<td><span data-ttu-id="dd724-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-417">Period 1</span></span></td>
<td><span data-ttu-id="dd724-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="dd724-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="dd724-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-421">Cost object</span></span></th>
<th><span data-ttu-id="dd724-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-424">Proj 1</span></span></td>
<td><span data-ttu-id="dd724-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="dd724-426">3,00</span><span class="sxs-lookup"><span data-stu-id="dd724-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-428">Proj 2</span></span></td>
<td><span data-ttu-id="dd724-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="dd724-430">1,00</span><span class="sxs-lookup"><span data-stu-id="dd724-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd724-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="dd724-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-433">Cost element</span></span></th>
<th><span data-ttu-id="dd724-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-434">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-435">Amount</span></span></th>
<th><span data-ttu-id="dd724-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="dd724-437">CC0001</span></span></td>
<td><span data-ttu-id="dd724-438">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-438">HR</span></span></td>
<td><span data-ttu-id="dd724-439">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-439">10001</span></span></td>
<td><span data-ttu-id="dd724-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-440">Electricity</span></span></td>
<td><span data-ttu-id="dd724-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-441">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="dd724-442">-30.00</span></span></td>
<td><span data-ttu-id="dd724-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-444">Proj 1</span></span></td>
<td><span data-ttu-id="dd724-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="dd724-446">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-446">10001</span></span></td>
<td><span data-ttu-id="dd724-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-447">Electricity</span></span></td>
<td><span data-ttu-id="dd724-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-448">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-449">30,00</span><span class="sxs-lookup"><span data-stu-id="dd724-449">30.00</span></span></td>
<td><span data-ttu-id="dd724-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-451">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-451">CC001</span></span></td>
<td><span data-ttu-id="dd724-452">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-452">HR</span></span></td>
<td><span data-ttu-id="dd724-453">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-453">10001</span></span></td>
<td><span data-ttu-id="dd724-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-454">Electricity</span></span></td>
<td><span data-ttu-id="dd724-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-455">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="dd724-456">-10.00</span></span></td>
<td><span data-ttu-id="dd724-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-458">Proj 2</span></span></td>
<td><span data-ttu-id="dd724-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="dd724-460">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-460">10001</span></span></td>
<td><span data-ttu-id="dd724-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="dd724-461">Electricity</span></span></td>
<td><span data-ttu-id="dd724-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-462">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-463">10,00</span><span class="sxs-lookup"><span data-stu-id="dd724-463">10.00</span></span></td>
<td><span data-ttu-id="dd724-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="dd724-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="dd724-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="dd724-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="dd724-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="dd724-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="dd724-468">Finance and Operations støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="dd724-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="dd724-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="dd724-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="dd724-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="dd724-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="dd724-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="dd724-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="dd724-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="dd724-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="dd724-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="dd724-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="dd724-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="dd724-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="dd724-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="dd724-475">Define the cost allocation</span></span>

<span data-ttu-id="dd724-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="dd724-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="dd724-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="dd724-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="dd724-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="dd724-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-479">Cost object</span></span></th>
<th><span data-ttu-id="dd724-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="dd724-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-481">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-481">CC002</span></span></td>
<td><span data-ttu-id="dd724-482">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-482">Finance</span></span></td>
<td><span data-ttu-id="dd724-483">35</span><span class="sxs-lookup"><span data-stu-id="dd724-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-484">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-484">CC003</span></span></td>
<td><span data-ttu-id="dd724-485">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-485">Assembly</span></span></td>
<td><span data-ttu-id="dd724-486">55</span><span class="sxs-lookup"><span data-stu-id="dd724-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-487">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-487">CC004</span></span></td>
<td><span data-ttu-id="dd724-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-488">Packaging</span></span></td>
<td><span data-ttu-id="dd724-489">10</span><span class="sxs-lookup"><span data-stu-id="dd724-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="dd724-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="dd724-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="dd724-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-492">Cost object</span></span></th>
<th><span data-ttu-id="dd724-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="dd724-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-494">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-494">CC003</span></span></td>
<td><span data-ttu-id="dd724-495">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-495">Assembly</span></span></td>
<td><span data-ttu-id="dd724-496">65</span><span class="sxs-lookup"><span data-stu-id="dd724-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-497">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-497">CC004</span></span></td>
<td><span data-ttu-id="dd724-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-498">Packaging</span></span></td>
<td><span data-ttu-id="dd724-499">35</span><span class="sxs-lookup"><span data-stu-id="dd724-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="dd724-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="dd724-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="dd724-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-502">Cost object</span></span></th>
<th><span data-ttu-id="dd724-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="dd724-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-504">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-505">Product 1</span></span></td>
<td><span data-ttu-id="dd724-506">60</span><span class="sxs-lookup"><span data-stu-id="dd724-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-507">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-508">Product 2</span></span></td>
<td><span data-ttu-id="dd724-509">20</span><span class="sxs-lookup"><span data-stu-id="dd724-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="dd724-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="dd724-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="dd724-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-512">Cost object</span></span></th>
<th><span data-ttu-id="dd724-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="dd724-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-514">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-514">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-515">Product 1</span></span></td>
<td><span data-ttu-id="dd724-516">80</span><span class="sxs-lookup"><span data-stu-id="dd724-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-517">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-518">Product 2</span></span></td>
<td><span data-ttu-id="dd724-519">sept.</span><span class="sxs-lookup"><span data-stu-id="dd724-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dd724-520">I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="dd724-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="dd724-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="dd724-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="dd724-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="dd724-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-523">Cost object</span></span></th>
<th><span data-ttu-id="dd724-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-524">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-525">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-526">Amount</span></span></th>
<th><span data-ttu-id="dd724-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-528">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-528">CC002</span></span></td>
<td><span data-ttu-id="dd724-529">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-529">Finance</span></span></td>
<td><span data-ttu-id="dd724-530">35</span><span class="sxs-lookup"><span data-stu-id="dd724-530">35</span></span></td>
<td><span data-ttu-id="dd724-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dd724-532">175.00</span><span class="sxs-lookup"><span data-stu-id="dd724-532">175.00</span></span></td>
<td><span data-ttu-id="dd724-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-534">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-534">CC003</span></span></td>
<td><span data-ttu-id="dd724-535">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-535">Assembly</span></span></td>
<td><span data-ttu-id="dd724-536">55</span><span class="sxs-lookup"><span data-stu-id="dd724-536">55</span></span></td>
<td><span data-ttu-id="dd724-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dd724-538">275.00</span><span class="sxs-lookup"><span data-stu-id="dd724-538">275.00</span></span></td>
<td><span data-ttu-id="dd724-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-540">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-540">CC004</span></span></td>
<td><span data-ttu-id="dd724-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-541">Packaging</span></span></td>
<td><span data-ttu-id="dd724-542">10</span><span class="sxs-lookup"><span data-stu-id="dd724-542">10</span></span></td>
<td><span data-ttu-id="dd724-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dd724-544">50,00</span><span class="sxs-lookup"><span data-stu-id="dd724-544">50.00</span></span></td>
<td><span data-ttu-id="dd724-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-546">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-546">CC002</span></span></td>
<td><span data-ttu-id="dd724-547">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-547">Finance</span></span></td>
<td><span data-ttu-id="dd724-548">35</span><span class="sxs-lookup"><span data-stu-id="dd724-548">35</span></span></td>
<td><span data-ttu-id="dd724-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="dd724-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dd724-550">436.00</span><span class="sxs-lookup"><span data-stu-id="dd724-550">436.00</span></span></td>
<td><span data-ttu-id="dd724-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-552">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-552">CC003</span></span></td>
<td><span data-ttu-id="dd724-553">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-553">Assembly</span></span></td>
<td><span data-ttu-id="dd724-554">55</span><span class="sxs-lookup"><span data-stu-id="dd724-554">55</span></span></td>
<td><span data-ttu-id="dd724-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="dd724-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dd724-556">685.14</span><span class="sxs-lookup"><span data-stu-id="dd724-556">685.14</span></span></td>
<td><span data-ttu-id="dd724-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-558">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-558">CC004</span></span></td>
<td><span data-ttu-id="dd724-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-559">Packaging</span></span></td>
<td><span data-ttu-id="dd724-560">10</span><span class="sxs-lookup"><span data-stu-id="dd724-560">10</span></span></td>
<td><span data-ttu-id="dd724-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="dd724-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dd724-562">124.57</span><span class="sxs-lookup"><span data-stu-id="dd724-562">124.57</span></span></td>
<td><span data-ttu-id="dd724-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="dd724-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-565">Cost object</span></span></th>
<th><span data-ttu-id="dd724-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-566">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-567">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-568">Amount</span></span></th>
<th><span data-ttu-id="dd724-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-570">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-570">CC003</span></span></td>
<td><span data-ttu-id="dd724-571">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-571">Assembly</span></span></td>
<td><span data-ttu-id="dd724-572">65</span><span class="sxs-lookup"><span data-stu-id="dd724-572">65</span></span></td>
<td><span data-ttu-id="dd724-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="dd724-574">438.75</span><span class="sxs-lookup"><span data-stu-id="dd724-574">438.75</span></span></td>
<td><span data-ttu-id="dd724-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-576">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-576">CC004</span></span></td>
<td><span data-ttu-id="dd724-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-577">Packaging</span></span></td>
<td><span data-ttu-id="dd724-578">35</span><span class="sxs-lookup"><span data-stu-id="dd724-578">35</span></span></td>
<td><span data-ttu-id="dd724-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="dd724-580">236.25</span><span class="sxs-lookup"><span data-stu-id="dd724-580">236.25</span></span></td>
<td><span data-ttu-id="dd724-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-582">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-582">CC003</span></span></td>
<td><span data-ttu-id="dd724-583">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-583">Assembly</span></span></td>
<td><span data-ttu-id="dd724-584">65</span><span class="sxs-lookup"><span data-stu-id="dd724-584">65</span></span></td>
<td><span data-ttu-id="dd724-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="dd724-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="dd724-586">5,297.69</span></span></td>
<td><span data-ttu-id="dd724-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-588">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-588">CC004</span></span></td>
<td><span data-ttu-id="dd724-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-589">Packaging</span></span></td>
<td><span data-ttu-id="dd724-590">35</span><span class="sxs-lookup"><span data-stu-id="dd724-590">35</span></span></td>
<td><span data-ttu-id="dd724-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="dd724-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="dd724-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="dd724-592">2,852.60</span></span></td>
<td><span data-ttu-id="dd724-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="dd724-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-595">Cost object</span></span></th>
<th><span data-ttu-id="dd724-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-596">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-597">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-598">Amount</span></span></th>
<th><span data-ttu-id="dd724-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-600">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-601">Product 1</span></span></td>
<td><span data-ttu-id="dd724-602">60</span><span class="sxs-lookup"><span data-stu-id="dd724-602">60</span></span></td>
<td><span data-ttu-id="dd724-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="dd724-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="dd724-604">535.31</span><span class="sxs-lookup"><span data-stu-id="dd724-604">535.31</span></span></td>
<td><span data-ttu-id="dd724-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-606">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-607">Product 2</span></span></td>
<td><span data-ttu-id="dd724-608">20</span><span class="sxs-lookup"><span data-stu-id="dd724-608">20</span></span></td>
<td><span data-ttu-id="dd724-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="dd724-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="dd724-610">178.44</span><span class="sxs-lookup"><span data-stu-id="dd724-610">178.44</span></span></td>
<td><span data-ttu-id="dd724-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-612">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-613">Product 1</span></span></td>
<td><span data-ttu-id="dd724-614">60</span><span class="sxs-lookup"><span data-stu-id="dd724-614">60</span></span></td>
<td><span data-ttu-id="dd724-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="dd724-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="dd724-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="dd724-616">4,487.12</span></span></td>
<td><span data-ttu-id="dd724-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-618">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-619">Product 2</span></span></td>
<td><span data-ttu-id="dd724-620">20</span><span class="sxs-lookup"><span data-stu-id="dd724-620">20</span></span></td>
<td><span data-ttu-id="dd724-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="dd724-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="dd724-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="dd724-622">1,495.71</span></span></td>
<td><span data-ttu-id="dd724-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd724-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="dd724-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-625">Cost object</span></span></th>
<th><span data-ttu-id="dd724-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="dd724-626">Magnitude</span></span></th>
<th><span data-ttu-id="dd724-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="dd724-627">Allocation factor</span></span></th>
<th><span data-ttu-id="dd724-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-628">Amount</span></span></th>
<th><span data-ttu-id="dd724-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-630">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-631">Product 1</span></span></td>
<td><span data-ttu-id="dd724-632">80</span><span class="sxs-lookup"><span data-stu-id="dd724-632">80</span></span></td>
<td><span data-ttu-id="dd724-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="dd724-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="dd724-634">241.05</span><span class="sxs-lookup"><span data-stu-id="dd724-634">241.05</span></span></td>
<td><span data-ttu-id="dd724-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-636">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-637">Product 2</span></span></td>
<td><span data-ttu-id="dd724-638">15</span><span class="sxs-lookup"><span data-stu-id="dd724-638">15</span></span></td>
<td><span data-ttu-id="dd724-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="dd724-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="dd724-640">45.20</span><span class="sxs-lookup"><span data-stu-id="dd724-640">45.20</span></span></td>
<td><span data-ttu-id="dd724-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-642">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-643">Product 1</span></span></td>
<td><span data-ttu-id="dd724-644">80</span><span class="sxs-lookup"><span data-stu-id="dd724-644">80</span></span></td>
<td><span data-ttu-id="dd724-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="dd724-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="dd724-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="dd724-646">2,507.09</span></span></td>
<td><span data-ttu-id="dd724-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-648">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-649">Product 2</span></span></td>
<td><span data-ttu-id="dd724-650">15</span><span class="sxs-lookup"><span data-stu-id="dd724-650">15</span></span></td>
<td><span data-ttu-id="dd724-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="dd724-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="dd724-652">470.08</span><span class="sxs-lookup"><span data-stu-id="dd724-652">470.08</span></span></td>
<td><span data-ttu-id="dd724-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dd724-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="dd724-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="dd724-655">Journal</span></span></th>
<th><span data-ttu-id="dd724-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="dd724-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd724-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="dd724-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd724-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="dd724-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-659">00004</span><span class="sxs-lookup"><span data-stu-id="dd724-659">00004</span></span></td>
<td><span data-ttu-id="dd724-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="dd724-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="dd724-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="dd724-661">Fiscal</span></span></td>
<td><span data-ttu-id="dd724-662">2017</span><span class="sxs-lookup"><span data-stu-id="dd724-662">2017</span></span></td>
<td><span data-ttu-id="dd724-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-663">Period 1</span></span></td>
<td><span data-ttu-id="dd724-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="dd724-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="dd724-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="dd724-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd724-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-668">Cost element</span></span></th>
<th><span data-ttu-id="dd724-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-669">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-672">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-672">CC001</span></span></td>
<td><span data-ttu-id="dd724-673">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-673">HR</span></span></td>
<td><span data-ttu-id="dd724-674">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-674">10001</span></span></td>
<td><span data-ttu-id="dd724-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-675">Electricity</span></span></td>
<td><span data-ttu-id="dd724-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-676">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-677">500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-679">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-679">CC001</span></span></td>
<td><span data-ttu-id="dd724-680">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-680">HR</span></span></td>
<td><span data-ttu-id="dd724-681">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-681">10001</span></span></td>
<td><span data-ttu-id="dd724-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-682">Electricity</span></span></td>
<td><span data-ttu-id="dd724-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-683">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="dd724-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-686">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-686">CC002</span></span></td>
<td><span data-ttu-id="dd724-687">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-687">Finance</span></span></td>
<td><span data-ttu-id="dd724-688">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-688">10001</span></span></td>
<td><span data-ttu-id="dd724-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-689">Electricity</span></span></td>
<td><span data-ttu-id="dd724-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-690">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-691">675.00</span><span class="sxs-lookup"><span data-stu-id="dd724-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-693">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-693">CC002</span></span></td>
<td><span data-ttu-id="dd724-694">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-694">Finance</span></span></td>
<td><span data-ttu-id="dd724-695">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-695">10001</span></span></td>
<td><span data-ttu-id="dd724-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-696">Electricity</span></span></td>
<td><span data-ttu-id="dd724-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-697">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="dd724-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-700">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-700">CC003</span></span></td>
<td><span data-ttu-id="dd724-701">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-701">Assembly</span></span></td>
<td><span data-ttu-id="dd724-702">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-702">10001</span></span></td>
<td><span data-ttu-id="dd724-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-703">Electricity</span></span></td>
<td><span data-ttu-id="dd724-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-704">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-705">713.75</span><span class="sxs-lookup"><span data-stu-id="dd724-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-707">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-707">CC003</span></span></td>
<td><span data-ttu-id="dd724-708">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-708">Assembly</span></span></td>
<td><span data-ttu-id="dd724-709">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-709">10001</span></span></td>
<td><span data-ttu-id="dd724-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-710">Electricity</span></span></td>
<td><span data-ttu-id="dd724-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-711">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="dd724-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-714">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-714">CC003</span></span></td>
<td><span data-ttu-id="dd724-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-715">Packaging</span></span></td>
<td><span data-ttu-id="dd724-716">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-716">10001</span></span></td>
<td><span data-ttu-id="dd724-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-717">Electricity</span></span></td>
<td><span data-ttu-id="dd724-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-718">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-719">286.25</span><span class="sxs-lookup"><span data-stu-id="dd724-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-721">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-721">CC003</span></span></td>
<td><span data-ttu-id="dd724-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-722">Packaging</span></span></td>
<td><span data-ttu-id="dd724-723">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-723">10001</span></span></td>
<td><span data-ttu-id="dd724-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-724">Electricity</span></span></td>
<td><span data-ttu-id="dd724-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-725">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="dd724-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-728">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-729">Product 1</span></span></td>
<td><span data-ttu-id="dd724-730">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-730">10001</span></span></td>
<td><span data-ttu-id="dd724-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-731">Electricity</span></span></td>
<td><span data-ttu-id="dd724-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-732">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-733">776.36</span><span class="sxs-lookup"><span data-stu-id="dd724-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-735">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-736">Product 1</span></span></td>
<td><span data-ttu-id="dd724-737">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-737">10001</span></span></td>
<td><span data-ttu-id="dd724-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-738">Electricity</span></span></td>
<td><span data-ttu-id="dd724-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-739">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="dd724-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-742">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-743">Product 1</span></span></td>
<td><span data-ttu-id="dd724-744">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-744">10001</span></span></td>
<td><span data-ttu-id="dd724-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-745">Electricity</span></span></td>
<td><span data-ttu-id="dd724-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-746">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-747">223.64</span><span class="sxs-lookup"><span data-stu-id="dd724-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd724-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-749">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-750">Product 1</span></span></td>
<td><span data-ttu-id="dd724-751">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-751">10001</span></span></td>
<td><span data-ttu-id="dd724-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-752">Electricity</span></span></td>
<td><span data-ttu-id="dd724-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-753">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="dd724-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd724-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="dd724-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd724-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd724-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-757">Cost element</span></span></th>
<th><span data-ttu-id="dd724-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="dd724-758">Cost behavior</span></span></th>
<th><span data-ttu-id="dd724-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="dd724-759">Amount</span></span></th>
<th><span data-ttu-id="dd724-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="dd724-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd724-761">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-761">CC001</span></span></td>
<td><span data-ttu-id="dd724-762">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-762">HR</span></span></td>
<td><span data-ttu-id="dd724-763">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-763">10001</span></span></td>
<td><span data-ttu-id="dd724-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-764">Electricity</span></span></td>
<td><span data-ttu-id="dd724-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-765">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="dd724-766">-500.00</span></span></td>
<td><span data-ttu-id="dd724-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-768">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-768">CC002</span></span></td>
<td><span data-ttu-id="dd724-769">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-769">Finance</span></span></td>
<td><span data-ttu-id="dd724-770">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-770">10001</span></span></td>
<td><span data-ttu-id="dd724-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-771">Electricity</span></span></td>
<td><span data-ttu-id="dd724-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-772">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-773">175.00</span><span class="sxs-lookup"><span data-stu-id="dd724-773">175.00</span></span></td>
<td><span data-ttu-id="dd724-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-775">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-775">CC003</span></span></td>
<td><span data-ttu-id="dd724-776">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-776">Assembly</span></span></td>
<td><span data-ttu-id="dd724-777">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-777">10001</span></span></td>
<td><span data-ttu-id="dd724-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-778">Electricity</span></span></td>
<td><span data-ttu-id="dd724-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-779">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-780">275.00</span><span class="sxs-lookup"><span data-stu-id="dd724-780">275.00</span></span></td>
<td><span data-ttu-id="dd724-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-782">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-782">CC004</span></span></td>
<td><span data-ttu-id="dd724-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-783">Packaging</span></span></td>
<td><span data-ttu-id="dd724-784">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-784">10001</span></span></td>
<td><span data-ttu-id="dd724-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-785">Electricity</span></span></td>
<td><span data-ttu-id="dd724-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-786">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-787">50,00</span><span class="sxs-lookup"><span data-stu-id="dd724-787">50,00</span></span></td>
<td><span data-ttu-id="dd724-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-789">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-789">CC001</span></span></td>
<td><span data-ttu-id="dd724-790">Personale</span><span class="sxs-lookup"><span data-stu-id="dd724-790">HR</span></span></td>
<td><span data-ttu-id="dd724-791">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-791">10001</span></span></td>
<td><span data-ttu-id="dd724-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-792">Electricity</span></span></td>
<td><span data-ttu-id="dd724-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-793">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="dd724-794">-1,245.71</span></span></td>
<td><span data-ttu-id="dd724-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-796">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-796">CC002</span></span></td>
<td><span data-ttu-id="dd724-797">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-797">Finance</span></span></td>
<td><span data-ttu-id="dd724-798">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-798">10001</span></span></td>
<td><span data-ttu-id="dd724-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-799">Electricity</span></span></td>
<td><span data-ttu-id="dd724-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-800">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-801">436.00</span><span class="sxs-lookup"><span data-stu-id="dd724-801">436.00</span></span></td>
<td><span data-ttu-id="dd724-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-803">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-803">CC003</span></span></td>
<td><span data-ttu-id="dd724-804">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-804">Assembly</span></span></td>
<td><span data-ttu-id="dd724-805">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-805">10001</span></span></td>
<td><span data-ttu-id="dd724-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-806">Electricity</span></span></td>
<td><span data-ttu-id="dd724-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-807">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-808">685.14</span><span class="sxs-lookup"><span data-stu-id="dd724-808">685.14</span></span></td>
<td><span data-ttu-id="dd724-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-810">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-810">CC004</span></span></td>
<td><span data-ttu-id="dd724-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-811">Packaging</span></span></td>
<td><span data-ttu-id="dd724-812">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-812">10001</span></span></td>
<td><span data-ttu-id="dd724-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-813">Electricity</span></span></td>
<td><span data-ttu-id="dd724-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-814">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-815">124.57</span><span class="sxs-lookup"><span data-stu-id="dd724-815">124.57</span></span></td>
<td><span data-ttu-id="dd724-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-817">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-817">CC002</span></span></td>
<td><span data-ttu-id="dd724-818">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-818">Finance</span></span></td>
<td><span data-ttu-id="dd724-819">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-819">10001</span></span></td>
<td><span data-ttu-id="dd724-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-820">Electricity</span></span></td>
<td><span data-ttu-id="dd724-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-821">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="dd724-822">-675.00</span></span></td>
<td><span data-ttu-id="dd724-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-824">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-824">CC003</span></span></td>
<td><span data-ttu-id="dd724-825">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-825">Assembly</span></span></td>
<td><span data-ttu-id="dd724-826">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-826">10001</span></span></td>
<td><span data-ttu-id="dd724-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-827">Electricity</span></span></td>
<td><span data-ttu-id="dd724-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-828">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-829">438.75</span><span class="sxs-lookup"><span data-stu-id="dd724-829">438.75</span></span></td>
<td><span data-ttu-id="dd724-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-831">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-831">CC004</span></span></td>
<td><span data-ttu-id="dd724-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-832">Packaging</span></span></td>
<td><span data-ttu-id="dd724-833">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-833">10001</span></span></td>
<td><span data-ttu-id="dd724-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-834">Electricity</span></span></td>
<td><span data-ttu-id="dd724-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-835">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-836">236.25</span><span class="sxs-lookup"><span data-stu-id="dd724-836">236.25</span></span></td>
<td><span data-ttu-id="dd724-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-838">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-838">CC002</span></span></td>
<td><span data-ttu-id="dd724-839">Finans</span><span class="sxs-lookup"><span data-stu-id="dd724-839">Finance</span></span></td>
<td><span data-ttu-id="dd724-840">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-840">10001</span></span></td>
<td><span data-ttu-id="dd724-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-841">Electricity</span></span></td>
<td><span data-ttu-id="dd724-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-842">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="dd724-843">-8,150.29</span></span></td>
<td><span data-ttu-id="dd724-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-845">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-845">CC003</span></span></td>
<td><span data-ttu-id="dd724-846">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-846">Assembly</span></span></td>
<td><span data-ttu-id="dd724-847">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-847">10001</span></span></td>
<td><span data-ttu-id="dd724-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-848">Electricity</span></span></td>
<td><span data-ttu-id="dd724-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-849">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="dd724-850">5,297.69</span></span></td>
<td><span data-ttu-id="dd724-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-852">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-852">CC004</span></span></td>
<td><span data-ttu-id="dd724-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="dd724-853">Packaging</span></span></td>
<td><span data-ttu-id="dd724-854">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-854">10001</span></span></td>
<td><span data-ttu-id="dd724-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-855">Electricity</span></span></td>
<td><span data-ttu-id="dd724-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-856">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="dd724-857">2,852.60</span></span></td>
<td><span data-ttu-id="dd724-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-859">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-859">CC003</span></span></td>
<td><span data-ttu-id="dd724-860">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-860">Assembly</span></span></td>
<td><span data-ttu-id="dd724-861">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-861">10001</span></span></td>
<td><span data-ttu-id="dd724-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-862">Electricity</span></span></td>
<td><span data-ttu-id="dd724-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-863">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="dd724-864">-713.75</span></span></td>
<td><span data-ttu-id="dd724-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-866">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-867">Product 1</span></span></td>
<td><span data-ttu-id="dd724-868">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-868">10001</span></span></td>
<td><span data-ttu-id="dd724-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-869">Electricity</span></span></td>
<td><span data-ttu-id="dd724-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-870">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-871">535.31</span><span class="sxs-lookup"><span data-stu-id="dd724-871">535.31</span></span></td>
<td><span data-ttu-id="dd724-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-873">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-874">Product 2</span></span></td>
<td><span data-ttu-id="dd724-875">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-875">10001</span></span></td>
<td><span data-ttu-id="dd724-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-876">Electricity</span></span></td>
<td><span data-ttu-id="dd724-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-877">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-878">178.44</span><span class="sxs-lookup"><span data-stu-id="dd724-878">178.44</span></span></td>
<td><span data-ttu-id="dd724-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-880">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-880">CC003</span></span></td>
<td><span data-ttu-id="dd724-881">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-881">Assembly</span></span></td>
<td><span data-ttu-id="dd724-882">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-882">10001</span></span></td>
<td><span data-ttu-id="dd724-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-883">Electricity</span></span></td>
<td><span data-ttu-id="dd724-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-884">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="dd724-885">-5,982.83</span></span></td>
<td><span data-ttu-id="dd724-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-887">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-888">Product 1</span></span></td>
<td><span data-ttu-id="dd724-889">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-889">10001</span></span></td>
<td><span data-ttu-id="dd724-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-890">Electricity</span></span></td>
<td><span data-ttu-id="dd724-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-891">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="dd724-892">4,487.12</span></span></td>
<td><span data-ttu-id="dd724-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-894">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-895">Product 2</span></span></td>
<td><span data-ttu-id="dd724-896">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-896">10001</span></span></td>
<td><span data-ttu-id="dd724-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-897">Electricity</span></span></td>
<td><span data-ttu-id="dd724-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-898">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="dd724-899">1,495.71</span></span></td>
<td><span data-ttu-id="dd724-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-901">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-901">CC003</span></span></td>
<td><span data-ttu-id="dd724-902">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-902">Assembly</span></span></td>
<td><span data-ttu-id="dd724-903">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-903">10001</span></span></td>
<td><span data-ttu-id="dd724-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-904">Electricity</span></span></td>
<td><span data-ttu-id="dd724-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-905">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="dd724-906">-286.25</span></span></td>
<td><span data-ttu-id="dd724-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-908">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-909">Product 1</span></span></td>
<td><span data-ttu-id="dd724-910">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-910">10001</span></span></td>
<td><span data-ttu-id="dd724-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-911">Electricity</span></span></td>
<td><span data-ttu-id="dd724-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-912">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-913">241.05</span><span class="sxs-lookup"><span data-stu-id="dd724-913">241.05</span></span></td>
<td><span data-ttu-id="dd724-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-915">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-916">Product 2</span></span></td>
<td><span data-ttu-id="dd724-917">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-917">10001</span></span></td>
<td><span data-ttu-id="dd724-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-918">Electricity</span></span></td>
<td><span data-ttu-id="dd724-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-919">Fixed cost</span></span></td>
<td><span data-ttu-id="dd724-920">45.20</span><span class="sxs-lookup"><span data-stu-id="dd724-920">45.20</span></span></td>
<td><span data-ttu-id="dd724-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-922">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-922">CC003</span></span></td>
<td><span data-ttu-id="dd724-923">Samling</span><span class="sxs-lookup"><span data-stu-id="dd724-923">Assembly</span></span></td>
<td><span data-ttu-id="dd724-924">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-924">10001</span></span></td>
<td><span data-ttu-id="dd724-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-925">Electricity</span></span></td>
<td><span data-ttu-id="dd724-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-926">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="dd724-927">-2,977.17</span></span></td>
<td><span data-ttu-id="dd724-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-929">Prod 1</span></span></td>
<td><span data-ttu-id="dd724-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="dd724-930">Product 1</span></span></td>
<td><span data-ttu-id="dd724-931">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-931">10001</span></span></td>
<td><span data-ttu-id="dd724-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-932">Electricity</span></span></td>
<td><span data-ttu-id="dd724-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-933">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="dd724-934">2,507.09</span></span></td>
<td><span data-ttu-id="dd724-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd724-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-936">Prod 2</span></span></td>
<td><span data-ttu-id="dd724-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="dd724-937">Product 2</span></span></td>
<td><span data-ttu-id="dd724-938">10001</span><span class="sxs-lookup"><span data-stu-id="dd724-938">10001</span></span></td>
<td><span data-ttu-id="dd724-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="dd724-939">Electricity</span></span></td>
<td><span data-ttu-id="dd724-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-940">Variable cost</span></span></td>
<td><span data-ttu-id="dd724-941">470.08</span><span class="sxs-lookup"><span data-stu-id="dd724-941">470.08</span></span></td>
<td><span data-ttu-id="dd724-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="dd724-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="dd724-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="dd724-943">Conclusion</span></span>
<span data-ttu-id="dd724-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="dd724-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="dd724-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="dd724-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="dd724-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="dd724-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="dd724-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="dd724-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="dd724-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="dd724-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="dd724-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="dd724-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="dd724-950">Sum</span><span class="sxs-lookup"><span data-stu-id="dd724-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dd724-951">CC099</span><span class="sxs-lookup"><span data-stu-id="dd724-951">CC099</span></span></th>
<th><span data-ttu-id="dd724-952">CC001</span><span class="sxs-lookup"><span data-stu-id="dd724-952">CC001</span></span></th>
<th><span data-ttu-id="dd724-953">CC002</span><span class="sxs-lookup"><span data-stu-id="dd724-953">CC002</span></span></th>
<th><span data-ttu-id="dd724-954">CC003</span><span class="sxs-lookup"><span data-stu-id="dd724-954">CC003</span></span></th>
<th><span data-ttu-id="dd724-955">CC004</span><span class="sxs-lookup"><span data-stu-id="dd724-955">CC004</span></span></th>
<th><span data-ttu-id="dd724-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="dd724-956">Proj 1</span></span></th>
<th><span data-ttu-id="dd724-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="dd724-957">Proj 2</span></span></th>
<th><span data-ttu-id="dd724-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="dd724-958">Prod 1</span></span></th>
<th><span data-ttu-id="dd724-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="dd724-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="dd724-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="dd724-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="dd724-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="dd724-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="dd724-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-971">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="dd724-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-973">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-974">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-975">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-976">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-977">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="dd724-978">776.36</span><span class="sxs-lookup"><span data-stu-id="dd724-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-979">223.64</span><span class="sxs-lookup"><span data-stu-id="dd724-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="dd724-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="dd724-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-982">000</span><span class="sxs-lookup"><span data-stu-id="dd724-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-983">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-984">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-985">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-986">0,00</span><span class="sxs-lookup"><span data-stu-id="dd724-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-987">30,00</span><span class="sxs-lookup"><span data-stu-id="dd724-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-988">10,00</span><span class="sxs-lookup"><span data-stu-id="dd724-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="dd724-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="dd724-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd724-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="dd724-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dd724-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="dd724-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="dd724-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd724-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="dd724-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="dd724-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="dd724-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="dd724-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="dd724-996">Hvis du vil ha mer informasjon, kan du se [Kostnadsopprulling](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="dd724-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



