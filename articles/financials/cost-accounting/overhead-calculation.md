---
title: Beregning av indirekte kostnader
description: Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 549e9b4b073a4e93dd3a1dd52dd6f43e7420a31b
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="44456-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="44456-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="44456-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="44456-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="44456-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="44456-105">Term definition</span></span>
---------------

<span data-ttu-id="44456-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="44456-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="44456-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="44456-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="44456-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="44456-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="44456-109">Leie</span><span class="sxs-lookup"><span data-stu-id="44456-109">Rent</span></span>
-   <span data-ttu-id="44456-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-110">Electricity</span></span>
-   <span data-ttu-id="44456-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="44456-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="44456-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="44456-112">Overhead calculation overview</span></span>
<span data-ttu-id="44456-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="44456-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="44456-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="44456-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="44456-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="44456-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="44456-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="44456-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="44456-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="44456-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="44456-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="44456-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="44456-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="44456-119">Version type</span></span>
-   <span data-ttu-id="44456-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="44456-120">Date and time</span></span>
-   <span data-ttu-id="44456-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="44456-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="44456-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="44456-122">Fiscal year</span></span>
-   <span data-ttu-id="44456-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="44456-123">Fiscal period</span></span>

<span data-ttu-id="44456-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="44456-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="44456-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="44456-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="44456-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="44456-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="44456-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="44456-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="44456-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="44456-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="44456-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="44456-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="44456-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="44456-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="44456-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="44456-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="44456-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="44456-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="44456-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="44456-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="44456-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="44456-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="44456-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="44456-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="44456-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="44456-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="44456-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="44456-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="44456-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="44456-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="44456-140">Main account</span></span></th>
<th><span data-ttu-id="44456-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="44456-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="44456-143">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-143">CC099</span></span></td>
<td><span data-ttu-id="44456-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-144">Default cost center</span></span></td>
<td><span data-ttu-id="44456-145">10001</span><span class="sxs-lookup"><span data-stu-id="44456-145">10001</span></span></td>
<td><span data-ttu-id="44456-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-146">Electricity</span></span></td>
<td><span data-ttu-id="44456-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="44456-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="44456-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="44456-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="44456-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="44456-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="44456-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-151">Define the cost behavior rule</span></span>

<span data-ttu-id="44456-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="44456-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="44456-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="44456-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="44456-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="44456-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="44456-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="44456-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="44456-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="44456-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="44456-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="44456-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="44456-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="44456-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-160">Journal</span></span></th>
<th><span data-ttu-id="44456-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="44456-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="44456-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="44456-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="44456-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="44456-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-164">00001</span><span class="sxs-lookup"><span data-stu-id="44456-164">00001</span></span></td>
<td><span data-ttu-id="44456-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="44456-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="44456-166">Fiscal</span></span></td>
<td><span data-ttu-id="44456-167">2017</span><span class="sxs-lookup"><span data-stu-id="44456-167">2017</span></span></td>
<td><span data-ttu-id="44456-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-168">Period 1</span></span></td>
<td><span data-ttu-id="44456-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="44456-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="44456-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="44456-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-173">Cost element</span></span></th>
<th><span data-ttu-id="44456-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-174">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="44456-177">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-177">CC099</span></span></td>
<td><span data-ttu-id="44456-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-178">Default cost center</span></span></td>
<td><span data-ttu-id="44456-179">10001</span><span class="sxs-lookup"><span data-stu-id="44456-179">10001</span></span></td>
<td><span data-ttu-id="44456-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-180">Electricity</span></span></td>
<td><span data-ttu-id="44456-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="44456-181">Unclassified</span></span></td>
<td><span data-ttu-id="44456-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="44456-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="44456-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-185">Cost element</span></span></th>
<th><span data-ttu-id="44456-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-186">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-187">Amount</span></span></th>
<th><span data-ttu-id="44456-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-189">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-189">CC099</span></span></td>
<td><span data-ttu-id="44456-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-190">Default cost center</span></span></td>
<td><span data-ttu-id="44456-191">10001</span><span class="sxs-lookup"><span data-stu-id="44456-191">10001</span></span></td>
<td><span data-ttu-id="44456-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-192">Electricity</span></span></td>
<td><span data-ttu-id="44456-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="44456-193">Unclassified</span></span></td>
<td><span data-ttu-id="44456-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-194">10,000.00</span></span></td>
<td><span data-ttu-id="44456-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-196">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-196">CC099</span></span></td>
<td><span data-ttu-id="44456-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-197">Default cost center</span></span></td>
<td><span data-ttu-id="44456-198">10001</span><span class="sxs-lookup"><span data-stu-id="44456-198">10001</span></span></td>
<td><span data-ttu-id="44456-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-199">Electricity</span></span></td>
<td><span data-ttu-id="44456-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="44456-200">Unclassified</span></span></td>
<td><span data-ttu-id="44456-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-201">-10,000.00</span></span></td>
<td><span data-ttu-id="44456-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-203">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-203">CC099</span></span></td>
<td><span data-ttu-id="44456-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-204">Default cost center</span></span></td>
<td><span data-ttu-id="44456-205">10001</span><span class="sxs-lookup"><span data-stu-id="44456-205">10001</span></span></td>
<td><span data-ttu-id="44456-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-206">Electricity</span></span></td>
<td><span data-ttu-id="44456-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-207">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-208">1,000.00</span></span></td>
<td><span data-ttu-id="44456-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-210">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-210">CC099</span></span></td>
<td><span data-ttu-id="44456-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-211">Default cost center</span></span></td>
<td><span data-ttu-id="44456-212">10001</span><span class="sxs-lookup"><span data-stu-id="44456-212">10001</span></span></td>
<td><span data-ttu-id="44456-213">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-213">Electricity</span></span></td>
<td><span data-ttu-id="44456-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-214">Variable cost</span></span></td>
<td><span data-ttu-id="44456-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="44456-215">9,000.00</span></span></td>
<td><span data-ttu-id="44456-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-217">Hvis du vil ha detaljert informasjon om kostnadsatferd, kan du se Policy for kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="44456-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="44456-218">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="44456-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="44456-219">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="44456-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="44456-220">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="44456-221">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="44456-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="44456-222">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="44456-222">Define the cost distribution rule</span></span>

<span data-ttu-id="44456-223">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="44456-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="44456-224">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="44456-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="44456-225">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="44456-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="44456-226">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="44456-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="44456-227">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="44456-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="44456-228">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-229">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-229">Cost object</span></span></th>
<th><span data-ttu-id="44456-230">kWt</span><span class="sxs-lookup"><span data-stu-id="44456-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-231">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-231">CC001</span></span></td>
<td><span data-ttu-id="44456-232">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-232">HR</span></span></td>
<td><span data-ttu-id="44456-233">1 000</span><span class="sxs-lookup"><span data-stu-id="44456-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-234">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-234">CC002</span></span></td>
<td><span data-ttu-id="44456-235">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-235">Finance</span></span></td>
<td><span data-ttu-id="44456-236">6,000</span><span class="sxs-lookup"><span data-stu-id="44456-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-237">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-237">CC003</span></span></td>
<td><span data-ttu-id="44456-238">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-238">Assembly</span></span></td>
<td><span data-ttu-id="44456-239">0</span><span class="sxs-lookup"><span data-stu-id="44456-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-240">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="44456-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-241">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-241">Cost object</span></span></th>
<th><span data-ttu-id="44456-242">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-242">Magnitude</span></span></th>
<th><span data-ttu-id="44456-243">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-243">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-244">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-245">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-245">CC001</span></span></td>
<td><span data-ttu-id="44456-246">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-246">HR</span></span></td>
<td><span data-ttu-id="44456-247">1 000</span><span class="sxs-lookup"><span data-stu-id="44456-247">1,000</span></span></td>
<td><span data-ttu-id="44456-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="44456-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="44456-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-250">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-250">CC002</span></span></td>
<td><span data-ttu-id="44456-251">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-251">Finance</span></span></td>
<td><span data-ttu-id="44456-252">6,000</span><span class="sxs-lookup"><span data-stu-id="44456-252">6,000</span></span></td>
<td><span data-ttu-id="44456-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="44456-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="44456-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-255">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-255">CC003</span></span></td>
<td><span data-ttu-id="44456-256">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-256">Assembly</span></span></td>
<td><span data-ttu-id="44456-257">0</span><span class="sxs-lookup"><span data-stu-id="44456-257">0</span></span></td>
<td><span data-ttu-id="44456-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="44456-259">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-260">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="44456-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="44456-261">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="44456-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-262">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-262">Cost object</span></span></th>
<th><span data-ttu-id="44456-263">Formel</span><span class="sxs-lookup"><span data-stu-id="44456-263">Formula</span></span></th>
<th><span data-ttu-id="44456-264">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-264">Magnitude</span></span></th>
<th><span data-ttu-id="44456-265">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-265">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-266">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-267">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-267">CC001</span></span></td>
<td><span data-ttu-id="44456-268">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-268">HR</span></span></td>
<td><span data-ttu-id="44456-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="44456-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="44456-270">1</span><span class="sxs-lookup"><span data-stu-id="44456-270">1</span></span></td>
<td><span data-ttu-id="44456-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="44456-272">500,00</span><span class="sxs-lookup"><span data-stu-id="44456-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-273">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-273">CC002</span></span></td>
<td><span data-ttu-id="44456-274">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-274">Finance</span></span></td>
<td><span data-ttu-id="44456-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="44456-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="44456-276">1</span><span class="sxs-lookup"><span data-stu-id="44456-276">1</span></span></td>
<td><span data-ttu-id="44456-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="44456-278">500,00</span><span class="sxs-lookup"><span data-stu-id="44456-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-279">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-279">CC003</span></span></td>
<td><span data-ttu-id="44456-280">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-280">Assembly</span></span></td>
<td><span data-ttu-id="44456-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="44456-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="44456-282">0</span><span class="sxs-lookup"><span data-stu-id="44456-282">0</span></span></td>
<td><span data-ttu-id="44456-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="44456-284">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="44456-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-286">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-286">Journal</span></span></th>
<th><span data-ttu-id="44456-287">Journaltype</span><span class="sxs-lookup"><span data-stu-id="44456-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="44456-288">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="44456-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="44456-289">Versjon</span><span class="sxs-lookup"><span data-stu-id="44456-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-290">00002</span><span class="sxs-lookup"><span data-stu-id="44456-290">00002</span></span></td>
<td><span data-ttu-id="44456-291">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="44456-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="44456-292">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="44456-292">Fiscal</span></span></td>
<td><span data-ttu-id="44456-293">2017</span><span class="sxs-lookup"><span data-stu-id="44456-293">2017</span></span></td>
<td><span data-ttu-id="44456-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-294">Period 1</span></span></td>
<td><span data-ttu-id="44456-295">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="44456-296">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="44456-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-297">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="44456-298">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-299">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-299">Cost element</span></span></th>
<th><span data-ttu-id="44456-300">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-300">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-301">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-302">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-303">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-303">CC099</span></span></td>
<td><span data-ttu-id="44456-304">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-304">Default cost center</span></span></td>
<td><span data-ttu-id="44456-305">10001</span><span class="sxs-lookup"><span data-stu-id="44456-305">10001</span></span></td>
<td><span data-ttu-id="44456-306">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-306">Electricity</span></span></td>
<td><span data-ttu-id="44456-307">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-307">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-309">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-310">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-310">CC099</span></span></td>
<td><span data-ttu-id="44456-311">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-311">Default cost center</span></span></td>
<td><span data-ttu-id="44456-312">10001</span><span class="sxs-lookup"><span data-stu-id="44456-312">10001</span></span></td>
<td><span data-ttu-id="44456-313">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-313">Electricity</span></span></td>
<td><span data-ttu-id="44456-314">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-314">Variable cost</span></span></td>
<td><span data-ttu-id="44456-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="44456-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="44456-316">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="44456-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-317">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-318">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-318">Cost element</span></span></th>
<th><span data-ttu-id="44456-319">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-319">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-320">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-320">Amount</span></span></th>
<th><span data-ttu-id="44456-321">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-322">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-322">CC099</span></span></td>
<td><span data-ttu-id="44456-323">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-323">Default cost center</span></span></td>
<td><span data-ttu-id="44456-324">10001</span><span class="sxs-lookup"><span data-stu-id="44456-324">10001</span></span></td>
<td><span data-ttu-id="44456-325">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-325">Electricity</span></span></td>
<td><span data-ttu-id="44456-326">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-326">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-327">-1,000.00</span></span></td>
<td><span data-ttu-id="44456-328">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-329">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-329">CC001</span></span></td>
<td><span data-ttu-id="44456-330">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-330">HR</span></span></td>
<td><span data-ttu-id="44456-331">10001</span><span class="sxs-lookup"><span data-stu-id="44456-331">10001</span></span></td>
<td><span data-ttu-id="44456-332">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-332">Electricity</span></span></td>
<td><span data-ttu-id="44456-333">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-333">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-334">500,00</span><span class="sxs-lookup"><span data-stu-id="44456-334">500.00</span></span></td>
<td><span data-ttu-id="44456-335">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-336">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-336">CC002</span></span></td>
<td><span data-ttu-id="44456-337">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-337">Finance</span></span></td>
<td><span data-ttu-id="44456-338">10001</span><span class="sxs-lookup"><span data-stu-id="44456-338">10001</span></span></td>
<td><span data-ttu-id="44456-339">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-339">Electricity</span></span></td>
<td><span data-ttu-id="44456-340">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-340">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-341">500,00</span><span class="sxs-lookup"><span data-stu-id="44456-341">500.00</span></span></td>
<td><span data-ttu-id="44456-342">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-343">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-343">CC099</span></span></td>
<td><span data-ttu-id="44456-344">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="44456-344">Default cost center</span></span></td>
<td><span data-ttu-id="44456-345">10001</span><span class="sxs-lookup"><span data-stu-id="44456-345">10001</span></span></td>
<td><span data-ttu-id="44456-346">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-346">Electricity</span></span></td>
<td><span data-ttu-id="44456-347">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-347">Variable cost</span></span></td>
<td><span data-ttu-id="44456-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="44456-348">-9,000.00</span></span></td>
<td><span data-ttu-id="44456-349">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-350">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-350">CC001</span></span></td>
<td><span data-ttu-id="44456-351">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-351">HR</span></span></td>
<td><span data-ttu-id="44456-352">10001</span><span class="sxs-lookup"><span data-stu-id="44456-352">10001</span></span></td>
<td><span data-ttu-id="44456-353">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-353">Electricity</span></span></td>
<td><span data-ttu-id="44456-354">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-354">Variable cost</span></span></td>
<td><span data-ttu-id="44456-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="44456-355">1,285.71</span></span></td>
<td><span data-ttu-id="44456-356">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-357">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-357">CC002</span></span></td>
<td><span data-ttu-id="44456-358">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-358">Finance</span></span></td>
<td><span data-ttu-id="44456-359">10001</span><span class="sxs-lookup"><span data-stu-id="44456-359">10001</span></span></td>
<td><span data-ttu-id="44456-360">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-360">Electricity</span></span></td>
<td><span data-ttu-id="44456-361">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-361">Variable cost</span></span></td>
<td><span data-ttu-id="44456-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="44456-362">7,714.29</span></span></td>
<td><span data-ttu-id="44456-363">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-364">Hvis du vil ha detaljert informasjon om kostnadsdistribusjon og tildelingsgrunnlag, kan du se Kostnadsdistribusjonspolicy og Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="44456-365">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="44456-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="44456-366">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="44456-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="44456-367">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="44456-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="44456-368">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="44456-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="44456-369">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="44456-369">Define the overhead rate</span></span>

<span data-ttu-id="44456-370">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="44456-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="44456-371">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="44456-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-372">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-372">Cost object</span></span></th>
<th><span data-ttu-id="44456-373">Timeantall</span><span class="sxs-lookup"><span data-stu-id="44456-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-374">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-374">Proj 1</span></span></td>
<td><span data-ttu-id="44456-375">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="44456-375">Project 1</span></span></td>
<td><span data-ttu-id="44456-376">3</span><span class="sxs-lookup"><span data-stu-id="44456-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-377">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-377">Proj 2</span></span></td>
<td><span data-ttu-id="44456-378">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="44456-378">Project 2</span></span></td>
<td><span data-ttu-id="44456-379">1</span><span class="sxs-lookup"><span data-stu-id="44456-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-380">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="44456-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-381">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-381">Cost object</span></span></th>
<th><span data-ttu-id="44456-382">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-382">Cost element</span></span></th>
<th><span data-ttu-id="44456-383">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-383">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-384">Enheter</span><span class="sxs-lookup"><span data-stu-id="44456-384">Units</span></span></th>
<th><span data-ttu-id="44456-385">Sats</span><span class="sxs-lookup"><span data-stu-id="44456-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-386">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-386">CC001</span></span></td>
<td><span data-ttu-id="44456-387">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-387">HR</span></span></td>
<td><span data-ttu-id="44456-388">10001</span><span class="sxs-lookup"><span data-stu-id="44456-388">10001</span></span></td>
<td><span data-ttu-id="44456-389">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-389">Variable cost</span></span></td>
<td><span data-ttu-id="44456-390">1</span><span class="sxs-lookup"><span data-stu-id="44456-390">1</span></span></td>
<td><span data-ttu-id="44456-391">10</span><span class="sxs-lookup"><span data-stu-id="44456-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-392">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-393">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-393">Cost object</span></span></th>
<th><span data-ttu-id="44456-394">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-394">Magnitude</span></span></th>
<th><span data-ttu-id="44456-395">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-395">Cost element</span></span></th>
<th><span data-ttu-id="44456-396">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-396">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-397">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-398">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-398">Proj 1</span></span></td>
<td><span data-ttu-id="44456-399">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="44456-399">Project 1</span></span></td>
<td><span data-ttu-id="44456-400">3</span><span class="sxs-lookup"><span data-stu-id="44456-400">3</span></span></td>
<td><span data-ttu-id="44456-401">10001</span><span class="sxs-lookup"><span data-stu-id="44456-401">10001</span></span></td>
<td><span data-ttu-id="44456-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="44456-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="44456-403">30,00</span><span class="sxs-lookup"><span data-stu-id="44456-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-404">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-404">Proj 2</span></span></td>
<td><span data-ttu-id="44456-405">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="44456-405">Project 2</span></span></td>
<td><span data-ttu-id="44456-406">1</span><span class="sxs-lookup"><span data-stu-id="44456-406">1</span></span></td>
<td><span data-ttu-id="44456-407">10001</span><span class="sxs-lookup"><span data-stu-id="44456-407">10001</span></span></td>
<td><span data-ttu-id="44456-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="44456-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="44456-409">10,00</span><span class="sxs-lookup"><span data-stu-id="44456-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="44456-410">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-411">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-411">Journal</span></span></th>
<th><span data-ttu-id="44456-412">Journaltype</span><span class="sxs-lookup"><span data-stu-id="44456-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="44456-413">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="44456-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="44456-414">Versjon</span><span class="sxs-lookup"><span data-stu-id="44456-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-415">00003</span><span class="sxs-lookup"><span data-stu-id="44456-415">00003</span></span></td>
<td><span data-ttu-id="44456-416">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="44456-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="44456-417">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="44456-417">Fiscal</span></span></td>
<td><span data-ttu-id="44456-418">2017</span><span class="sxs-lookup"><span data-stu-id="44456-418">2017</span></span></td>
<td><span data-ttu-id="44456-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-419">Period 1</span></span></td>
<td><span data-ttu-id="44456-420">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="44456-421">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="44456-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-422">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="44456-423">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-423">Cost object</span></span></th>
<th><span data-ttu-id="44456-424">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-425">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-426">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-426">Proj 1</span></span></td>
<td><span data-ttu-id="44456-427">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="44456-428">3,00</span><span class="sxs-lookup"><span data-stu-id="44456-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-429">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-430">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-430">Proj 2</span></span></td>
<td><span data-ttu-id="44456-431">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="44456-432">1,00</span><span class="sxs-lookup"><span data-stu-id="44456-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="44456-433">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="44456-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-434">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-435">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-435">Cost element</span></span></th>
<th><span data-ttu-id="44456-436">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-436">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-437">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-437">Amount</span></span></th>
<th><span data-ttu-id="44456-438">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="44456-439">CC0001</span></span></td>
<td><span data-ttu-id="44456-440">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-440">HR</span></span></td>
<td><span data-ttu-id="44456-441">10001</span><span class="sxs-lookup"><span data-stu-id="44456-441">10001</span></span></td>
<td><span data-ttu-id="44456-442">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-442">Electricity</span></span></td>
<td><span data-ttu-id="44456-443">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-443">Variable cost</span></span></td>
<td><span data-ttu-id="44456-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="44456-444">-30.00</span></span></td>
<td><span data-ttu-id="44456-445">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-446">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-446">Proj 1</span></span></td>
<td><span data-ttu-id="44456-447">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="44456-448">10001</span><span class="sxs-lookup"><span data-stu-id="44456-448">10001</span></span></td>
<td><span data-ttu-id="44456-449">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-449">Electricity</span></span></td>
<td><span data-ttu-id="44456-450">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-450">Variable cost</span></span></td>
<td><span data-ttu-id="44456-451">30,00</span><span class="sxs-lookup"><span data-stu-id="44456-451">30.00</span></span></td>
<td><span data-ttu-id="44456-452">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-453">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-453">CC001</span></span></td>
<td><span data-ttu-id="44456-454">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-454">HR</span></span></td>
<td><span data-ttu-id="44456-455">10001</span><span class="sxs-lookup"><span data-stu-id="44456-455">10001</span></span></td>
<td><span data-ttu-id="44456-456">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-456">Electricity</span></span></td>
<td><span data-ttu-id="44456-457">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-457">Variable cost</span></span></td>
<td><span data-ttu-id="44456-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="44456-458">-10.00</span></span></td>
<td><span data-ttu-id="44456-459">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-460">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-460">Proj 2</span></span></td>
<td><span data-ttu-id="44456-461">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="44456-462">10001</span><span class="sxs-lookup"><span data-stu-id="44456-462">10001</span></span></td>
<td><span data-ttu-id="44456-463">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-463">Electricity</span></span></td>
<td><span data-ttu-id="44456-464">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-464">Variable cost</span></span></td>
<td><span data-ttu-id="44456-465">10,00</span><span class="sxs-lookup"><span data-stu-id="44456-465">10.00</span></span></td>
<td><span data-ttu-id="44456-466">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-467">Hvis du vil ha mer informasjon om policyen for sats for indirekte kostnader, kan du se Policy for sats for indirekte kostnader og Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="44456-468">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="44456-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="44456-469">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="44456-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="44456-470">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="44456-471">Finance and Operations støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="44456-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="44456-472">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="44456-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="44456-473">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="44456-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="44456-474">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="44456-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="44456-475">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="44456-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="44456-476">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="44456-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="44456-477">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="44456-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="44456-478">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="44456-478">Define the cost allocation</span></span>

<span data-ttu-id="44456-479">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="44456-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="44456-480">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="44456-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="44456-481">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="44456-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-482">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-482">Cost object</span></span></th>
<th><span data-ttu-id="44456-483">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="44456-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-484">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-484">CC002</span></span></td>
<td><span data-ttu-id="44456-485">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-485">Finance</span></span></td>
<td><span data-ttu-id="44456-486">35</span><span class="sxs-lookup"><span data-stu-id="44456-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-487">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-487">CC003</span></span></td>
<td><span data-ttu-id="44456-488">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-488">Assembly</span></span></td>
<td><span data-ttu-id="44456-489">55</span><span class="sxs-lookup"><span data-stu-id="44456-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-490">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-490">CC004</span></span></td>
<td><span data-ttu-id="44456-491">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-491">Packaging</span></span></td>
<td><span data-ttu-id="44456-492">10</span><span class="sxs-lookup"><span data-stu-id="44456-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-493">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="44456-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="44456-494">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="44456-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-495">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-495">Cost object</span></span></th>
<th><span data-ttu-id="44456-496">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="44456-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-497">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-497">CC003</span></span></td>
<td><span data-ttu-id="44456-498">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-498">Assembly</span></span></td>
<td><span data-ttu-id="44456-499">65</span><span class="sxs-lookup"><span data-stu-id="44456-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-500">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-500">CC004</span></span></td>
<td><span data-ttu-id="44456-501">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-501">Packaging</span></span></td>
<td><span data-ttu-id="44456-502">35</span><span class="sxs-lookup"><span data-stu-id="44456-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-503">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="44456-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="44456-504">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="44456-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-505">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-505">Cost object</span></span></th>
<th><span data-ttu-id="44456-506">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="44456-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-507">Prod 1</span></span></td>
<td><span data-ttu-id="44456-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-508">Product 1</span></span></td>
<td><span data-ttu-id="44456-509">60</span><span class="sxs-lookup"><span data-stu-id="44456-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-510">Prod 2</span></span></td>
<td><span data-ttu-id="44456-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-511">Product 2</span></span></td>
<td><span data-ttu-id="44456-512">20</span><span class="sxs-lookup"><span data-stu-id="44456-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-513">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="44456-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="44456-514">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="44456-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-515">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-515">Cost object</span></span></th>
<th><span data-ttu-id="44456-516">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="44456-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-517">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-517">Prod 1</span></span></td>
<td><span data-ttu-id="44456-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-518">Product 1</span></span></td>
<td><span data-ttu-id="44456-519">80</span><span class="sxs-lookup"><span data-stu-id="44456-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-520">Prod 2</span></span></td>
<td><span data-ttu-id="44456-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-521">Product 2</span></span></td>
<td><span data-ttu-id="44456-522">15</span><span class="sxs-lookup"><span data-stu-id="44456-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-523">**Obs!** I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="44456-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="44456-524">Hvis du vil ha mer informasjon om statistiske målleverandører, kan du se Maler for leverandør av statistisk måling.</span><span class="sxs-lookup"><span data-stu-id="44456-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="44456-525">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.) Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="44456-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-526">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-526">Cost object</span></span></th>
<th><span data-ttu-id="44456-527">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-527">Magnitude</span></span></th>
<th><span data-ttu-id="44456-528">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-528">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-529">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-529">Amount</span></span></th>
<th><span data-ttu-id="44456-530">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-531">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-531">CC002</span></span></td>
<td><span data-ttu-id="44456-532">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-532">Finance</span></span></td>
<td><span data-ttu-id="44456-533">35</span><span class="sxs-lookup"><span data-stu-id="44456-533">35</span></span></td>
<td><span data-ttu-id="44456-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="44456-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="44456-535">175.00</span><span class="sxs-lookup"><span data-stu-id="44456-535">175.00</span></span></td>
<td><span data-ttu-id="44456-536">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-537">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-537">CC003</span></span></td>
<td><span data-ttu-id="44456-538">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-538">Assembly</span></span></td>
<td><span data-ttu-id="44456-539">55</span><span class="sxs-lookup"><span data-stu-id="44456-539">55</span></span></td>
<td><span data-ttu-id="44456-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="44456-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="44456-541">275.00</span><span class="sxs-lookup"><span data-stu-id="44456-541">275.00</span></span></td>
<td><span data-ttu-id="44456-542">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-543">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-543">CC004</span></span></td>
<td><span data-ttu-id="44456-544">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-544">Packaging</span></span></td>
<td><span data-ttu-id="44456-545">10</span><span class="sxs-lookup"><span data-stu-id="44456-545">10</span></span></td>
<td><span data-ttu-id="44456-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="44456-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="44456-547">50,00</span><span class="sxs-lookup"><span data-stu-id="44456-547">50.00</span></span></td>
<td><span data-ttu-id="44456-548">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-549">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-549">CC002</span></span></td>
<td><span data-ttu-id="44456-550">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-550">Finance</span></span></td>
<td><span data-ttu-id="44456-551">35</span><span class="sxs-lookup"><span data-stu-id="44456-551">35</span></span></td>
<td><span data-ttu-id="44456-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="44456-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="44456-553">436.00</span><span class="sxs-lookup"><span data-stu-id="44456-553">436.00</span></span></td>
<td><span data-ttu-id="44456-554">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-555">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-555">CC003</span></span></td>
<td><span data-ttu-id="44456-556">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-556">Assembly</span></span></td>
<td><span data-ttu-id="44456-557">55</span><span class="sxs-lookup"><span data-stu-id="44456-557">55</span></span></td>
<td><span data-ttu-id="44456-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="44456-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="44456-559">685.14</span><span class="sxs-lookup"><span data-stu-id="44456-559">685.14</span></span></td>
<td><span data-ttu-id="44456-560">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-561">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-561">CC004</span></span></td>
<td><span data-ttu-id="44456-562">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-562">Packaging</span></span></td>
<td><span data-ttu-id="44456-563">10</span><span class="sxs-lookup"><span data-stu-id="44456-563">10</span></span></td>
<td><span data-ttu-id="44456-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="44456-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="44456-565">124.57</span><span class="sxs-lookup"><span data-stu-id="44456-565">124.57</span></span></td>
<td><span data-ttu-id="44456-566">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-567">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="44456-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-568">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-568">Cost object</span></span></th>
<th><span data-ttu-id="44456-569">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-569">Magnitude</span></span></th>
<th><span data-ttu-id="44456-570">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-570">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-571">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-571">Amount</span></span></th>
<th><span data-ttu-id="44456-572">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-573">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-573">CC003</span></span></td>
<td><span data-ttu-id="44456-574">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-574">Assembly</span></span></td>
<td><span data-ttu-id="44456-575">65</span><span class="sxs-lookup"><span data-stu-id="44456-575">65</span></span></td>
<td><span data-ttu-id="44456-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="44456-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="44456-577">438.75</span><span class="sxs-lookup"><span data-stu-id="44456-577">438.75</span></span></td>
<td><span data-ttu-id="44456-578">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-579">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-579">CC004</span></span></td>
<td><span data-ttu-id="44456-580">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-580">Packaging</span></span></td>
<td><span data-ttu-id="44456-581">35</span><span class="sxs-lookup"><span data-stu-id="44456-581">35</span></span></td>
<td><span data-ttu-id="44456-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="44456-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="44456-583">236.25</span><span class="sxs-lookup"><span data-stu-id="44456-583">236.25</span></span></td>
<td><span data-ttu-id="44456-584">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-585">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-585">CC003</span></span></td>
<td><span data-ttu-id="44456-586">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-586">Assembly</span></span></td>
<td><span data-ttu-id="44456-587">65</span><span class="sxs-lookup"><span data-stu-id="44456-587">65</span></span></td>
<td><span data-ttu-id="44456-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="44456-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="44456-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="44456-589">5,297.69</span></span></td>
<td><span data-ttu-id="44456-590">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-591">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-591">CC004</span></span></td>
<td><span data-ttu-id="44456-592">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-592">Packaging</span></span></td>
<td><span data-ttu-id="44456-593">35</span><span class="sxs-lookup"><span data-stu-id="44456-593">35</span></span></td>
<td><span data-ttu-id="44456-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="44456-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="44456-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="44456-595">2,852.60</span></span></td>
<td><span data-ttu-id="44456-596">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-597">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="44456-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-598">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-598">Cost object</span></span></th>
<th><span data-ttu-id="44456-599">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-599">Magnitude</span></span></th>
<th><span data-ttu-id="44456-600">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-600">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-601">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-601">Amount</span></span></th>
<th><span data-ttu-id="44456-602">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-603">Prod 1</span></span></td>
<td><span data-ttu-id="44456-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-604">Product 1</span></span></td>
<td><span data-ttu-id="44456-605">60</span><span class="sxs-lookup"><span data-stu-id="44456-605">60</span></span></td>
<td><span data-ttu-id="44456-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="44456-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="44456-607">535.31</span><span class="sxs-lookup"><span data-stu-id="44456-607">535.31</span></span></td>
<td><span data-ttu-id="44456-608">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-609">Prod 2</span></span></td>
<td><span data-ttu-id="44456-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-610">Product 2</span></span></td>
<td><span data-ttu-id="44456-611">20</span><span class="sxs-lookup"><span data-stu-id="44456-611">20</span></span></td>
<td><span data-ttu-id="44456-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="44456-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="44456-613">178.44</span><span class="sxs-lookup"><span data-stu-id="44456-613">178.44</span></span></td>
<td><span data-ttu-id="44456-614">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-615">Prod 1</span></span></td>
<td><span data-ttu-id="44456-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-616">Product 1</span></span></td>
<td><span data-ttu-id="44456-617">60</span><span class="sxs-lookup"><span data-stu-id="44456-617">60</span></span></td>
<td><span data-ttu-id="44456-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="44456-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="44456-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="44456-619">4,487.12</span></span></td>
<td><span data-ttu-id="44456-620">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-621">Prod 2</span></span></td>
<td><span data-ttu-id="44456-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-622">Product 2</span></span></td>
<td><span data-ttu-id="44456-623">20</span><span class="sxs-lookup"><span data-stu-id="44456-623">20</span></span></td>
<td><span data-ttu-id="44456-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="44456-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="44456-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="44456-625">1,495.71</span></span></td>
<td><span data-ttu-id="44456-626">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="44456-627">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="44456-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-628">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-628">Cost object</span></span></th>
<th><span data-ttu-id="44456-629">Størrelse</span><span class="sxs-lookup"><span data-stu-id="44456-629">Magnitude</span></span></th>
<th><span data-ttu-id="44456-630">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="44456-630">Allocation factor</span></span></th>
<th><span data-ttu-id="44456-631">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-631">Amount</span></span></th>
<th><span data-ttu-id="44456-632">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-633">Prod 1</span></span></td>
<td><span data-ttu-id="44456-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-634">Product 1</span></span></td>
<td><span data-ttu-id="44456-635">80</span><span class="sxs-lookup"><span data-stu-id="44456-635">80</span></span></td>
<td><span data-ttu-id="44456-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="44456-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="44456-637">241.05</span><span class="sxs-lookup"><span data-stu-id="44456-637">241.05</span></span></td>
<td><span data-ttu-id="44456-638">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-639">Prod 2</span></span></td>
<td><span data-ttu-id="44456-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-640">Product 2</span></span></td>
<td><span data-ttu-id="44456-641">15</span><span class="sxs-lookup"><span data-stu-id="44456-641">15</span></span></td>
<td><span data-ttu-id="44456-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="44456-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="44456-643">45.20</span><span class="sxs-lookup"><span data-stu-id="44456-643">45.20</span></span></td>
<td><span data-ttu-id="44456-644">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-645">Prod 1</span></span></td>
<td><span data-ttu-id="44456-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-646">Product 1</span></span></td>
<td><span data-ttu-id="44456-647">80</span><span class="sxs-lookup"><span data-stu-id="44456-647">80</span></span></td>
<td><span data-ttu-id="44456-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="44456-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="44456-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="44456-649">2,507.09</span></span></td>
<td><span data-ttu-id="44456-650">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-651">Prod 2</span></span></td>
<td><span data-ttu-id="44456-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-652">Product 2</span></span></td>
<td><span data-ttu-id="44456-653">15</span><span class="sxs-lookup"><span data-stu-id="44456-653">15</span></span></td>
<td><span data-ttu-id="44456-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="44456-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="44456-655">470.08</span><span class="sxs-lookup"><span data-stu-id="44456-655">470.08</span></span></td>
<td><span data-ttu-id="44456-656">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="44456-657">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="44456-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-658">Journalen</span><span class="sxs-lookup"><span data-stu-id="44456-658">Journal</span></span></th>
<th><span data-ttu-id="44456-659">Journaltype</span><span class="sxs-lookup"><span data-stu-id="44456-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="44456-660">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="44456-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="44456-661">Versjon</span><span class="sxs-lookup"><span data-stu-id="44456-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-662">00004</span><span class="sxs-lookup"><span data-stu-id="44456-662">00004</span></span></td>
<td><span data-ttu-id="44456-663">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="44456-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="44456-664">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="44456-664">Fiscal</span></span></td>
<td><span data-ttu-id="44456-665">2017</span><span class="sxs-lookup"><span data-stu-id="44456-665">2017</span></span></td>
<td><span data-ttu-id="44456-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-666">Period 1</span></span></td>
<td><span data-ttu-id="44456-667">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="44456-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="44456-668">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="44456-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="44456-669">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="44456-670">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-671">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-671">Cost element</span></span></th>
<th><span data-ttu-id="44456-672">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-672">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-673">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-674">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-675">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-675">CC001</span></span></td>
<td><span data-ttu-id="44456-676">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-676">HR</span></span></td>
<td><span data-ttu-id="44456-677">10001</span><span class="sxs-lookup"><span data-stu-id="44456-677">10001</span></span></td>
<td><span data-ttu-id="44456-678">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-678">Electricity</span></span></td>
<td><span data-ttu-id="44456-679">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-679">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-680">500,00</span><span class="sxs-lookup"><span data-stu-id="44456-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-681">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-682">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-682">CC001</span></span></td>
<td><span data-ttu-id="44456-683">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-683">HR</span></span></td>
<td><span data-ttu-id="44456-684">10001</span><span class="sxs-lookup"><span data-stu-id="44456-684">10001</span></span></td>
<td><span data-ttu-id="44456-685">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-685">Electricity</span></span></td>
<td><span data-ttu-id="44456-686">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-686">Variable cost</span></span></td>
<td><span data-ttu-id="44456-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="44456-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-688">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-689">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-689">CC002</span></span></td>
<td><span data-ttu-id="44456-690">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-690">Finance</span></span></td>
<td><span data-ttu-id="44456-691">10001</span><span class="sxs-lookup"><span data-stu-id="44456-691">10001</span></span></td>
<td><span data-ttu-id="44456-692">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-692">Electricity</span></span></td>
<td><span data-ttu-id="44456-693">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-693">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-694">675.00</span><span class="sxs-lookup"><span data-stu-id="44456-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-695">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-696">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-696">CC002</span></span></td>
<td><span data-ttu-id="44456-697">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-697">Finance</span></span></td>
<td><span data-ttu-id="44456-698">10001</span><span class="sxs-lookup"><span data-stu-id="44456-698">10001</span></span></td>
<td><span data-ttu-id="44456-699">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-699">Electricity</span></span></td>
<td><span data-ttu-id="44456-700">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-700">Variable cost</span></span></td>
<td><span data-ttu-id="44456-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="44456-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-702">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-703">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-703">CC003</span></span></td>
<td><span data-ttu-id="44456-704">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-704">Assembly</span></span></td>
<td><span data-ttu-id="44456-705">10001</span><span class="sxs-lookup"><span data-stu-id="44456-705">10001</span></span></td>
<td><span data-ttu-id="44456-706">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-706">Electricity</span></span></td>
<td><span data-ttu-id="44456-707">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-707">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-708">713.75</span><span class="sxs-lookup"><span data-stu-id="44456-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-709">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-710">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-710">CC003</span></span></td>
<td><span data-ttu-id="44456-711">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-711">Assembly</span></span></td>
<td><span data-ttu-id="44456-712">10001</span><span class="sxs-lookup"><span data-stu-id="44456-712">10001</span></span></td>
<td><span data-ttu-id="44456-713">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-713">Electricity</span></span></td>
<td><span data-ttu-id="44456-714">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-714">Variable cost</span></span></td>
<td><span data-ttu-id="44456-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="44456-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-716">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-717">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-717">CC003</span></span></td>
<td><span data-ttu-id="44456-718">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-718">Packaging</span></span></td>
<td><span data-ttu-id="44456-719">10001</span><span class="sxs-lookup"><span data-stu-id="44456-719">10001</span></span></td>
<td><span data-ttu-id="44456-720">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-720">Electricity</span></span></td>
<td><span data-ttu-id="44456-721">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-721">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-722">286.25</span><span class="sxs-lookup"><span data-stu-id="44456-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-723">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-724">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-724">CC003</span></span></td>
<td><span data-ttu-id="44456-725">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-725">Packaging</span></span></td>
<td><span data-ttu-id="44456-726">10001</span><span class="sxs-lookup"><span data-stu-id="44456-726">10001</span></span></td>
<td><span data-ttu-id="44456-727">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-727">Electricity</span></span></td>
<td><span data-ttu-id="44456-728">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-728">Variable cost</span></span></td>
<td><span data-ttu-id="44456-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="44456-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-730">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-731">Prod 1</span></span></td>
<td><span data-ttu-id="44456-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-732">Product 1</span></span></td>
<td><span data-ttu-id="44456-733">10001</span><span class="sxs-lookup"><span data-stu-id="44456-733">10001</span></span></td>
<td><span data-ttu-id="44456-734">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-734">Electricity</span></span></td>
<td><span data-ttu-id="44456-735">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-735">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-736">776.36</span><span class="sxs-lookup"><span data-stu-id="44456-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-737">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-738">Prod 1</span></span></td>
<td><span data-ttu-id="44456-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-739">Product 1</span></span></td>
<td><span data-ttu-id="44456-740">10001</span><span class="sxs-lookup"><span data-stu-id="44456-740">10001</span></span></td>
<td><span data-ttu-id="44456-741">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-741">Electricity</span></span></td>
<td><span data-ttu-id="44456-742">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-742">Variable cost</span></span></td>
<td><span data-ttu-id="44456-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="44456-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-744">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-745">Prod 2</span></span></td>
<td><span data-ttu-id="44456-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-746">Product 1</span></span></td>
<td><span data-ttu-id="44456-747">10001</span><span class="sxs-lookup"><span data-stu-id="44456-747">10001</span></span></td>
<td><span data-ttu-id="44456-748">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-748">Electricity</span></span></td>
<td><span data-ttu-id="44456-749">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-749">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-750">223.64</span><span class="sxs-lookup"><span data-stu-id="44456-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-751">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="44456-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-752">Prod 2</span></span></td>
<td><span data-ttu-id="44456-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-753">Product 1</span></span></td>
<td><span data-ttu-id="44456-754">10001</span><span class="sxs-lookup"><span data-stu-id="44456-754">10001</span></span></td>
<td><span data-ttu-id="44456-755">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-755">Electricity</span></span></td>
<td><span data-ttu-id="44456-756">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-756">Variable cost</span></span></td>
<td><span data-ttu-id="44456-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="44456-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="44456-758">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="44456-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="44456-759">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="44456-760">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-760">Cost element</span></span></th>
<th><span data-ttu-id="44456-761">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="44456-761">Cost behavior</span></span></th>
<th><span data-ttu-id="44456-762">Beløp</span><span class="sxs-lookup"><span data-stu-id="44456-762">Amount</span></span></th>
<th><span data-ttu-id="44456-763">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="44456-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="44456-764">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-764">CC001</span></span></td>
<td><span data-ttu-id="44456-765">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-765">HR</span></span></td>
<td><span data-ttu-id="44456-766">10001</span><span class="sxs-lookup"><span data-stu-id="44456-766">10001</span></span></td>
<td><span data-ttu-id="44456-767">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-767">Electricity</span></span></td>
<td><span data-ttu-id="44456-768">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-768">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="44456-769">-500.00</span></span></td>
<td><span data-ttu-id="44456-770">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-771">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-771">CC002</span></span></td>
<td><span data-ttu-id="44456-772">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-772">Finance</span></span></td>
<td><span data-ttu-id="44456-773">10001</span><span class="sxs-lookup"><span data-stu-id="44456-773">10001</span></span></td>
<td><span data-ttu-id="44456-774">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-774">Electricity</span></span></td>
<td><span data-ttu-id="44456-775">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-775">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-776">175.00</span><span class="sxs-lookup"><span data-stu-id="44456-776">175.00</span></span></td>
<td><span data-ttu-id="44456-777">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-778">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-778">CC003</span></span></td>
<td><span data-ttu-id="44456-779">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-779">Assembly</span></span></td>
<td><span data-ttu-id="44456-780">10001</span><span class="sxs-lookup"><span data-stu-id="44456-780">10001</span></span></td>
<td><span data-ttu-id="44456-781">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-781">Electricity</span></span></td>
<td><span data-ttu-id="44456-782">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-782">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-783">275.00</span><span class="sxs-lookup"><span data-stu-id="44456-783">275.00</span></span></td>
<td><span data-ttu-id="44456-784">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-785">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-785">CC004</span></span></td>
<td><span data-ttu-id="44456-786">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-786">Packaging</span></span></td>
<td><span data-ttu-id="44456-787">10001</span><span class="sxs-lookup"><span data-stu-id="44456-787">10001</span></span></td>
<td><span data-ttu-id="44456-788">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-788">Electricity</span></span></td>
<td><span data-ttu-id="44456-789">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-789">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-790">50,00</span><span class="sxs-lookup"><span data-stu-id="44456-790">50,00</span></span></td>
<td><span data-ttu-id="44456-791">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-792">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-792">CC001</span></span></td>
<td><span data-ttu-id="44456-793">Personale</span><span class="sxs-lookup"><span data-stu-id="44456-793">HR</span></span></td>
<td><span data-ttu-id="44456-794">10001</span><span class="sxs-lookup"><span data-stu-id="44456-794">10001</span></span></td>
<td><span data-ttu-id="44456-795">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-795">Electricity</span></span></td>
<td><span data-ttu-id="44456-796">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-796">Variable cost</span></span></td>
<td><span data-ttu-id="44456-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="44456-797">-1,245.71</span></span></td>
<td><span data-ttu-id="44456-798">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-799">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-799">CC002</span></span></td>
<td><span data-ttu-id="44456-800">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-800">Finance</span></span></td>
<td><span data-ttu-id="44456-801">10001</span><span class="sxs-lookup"><span data-stu-id="44456-801">10001</span></span></td>
<td><span data-ttu-id="44456-802">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-802">Electricity</span></span></td>
<td><span data-ttu-id="44456-803">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-803">Variable cost</span></span></td>
<td><span data-ttu-id="44456-804">436.00</span><span class="sxs-lookup"><span data-stu-id="44456-804">436.00</span></span></td>
<td><span data-ttu-id="44456-805">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-806">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-806">CC003</span></span></td>
<td><span data-ttu-id="44456-807">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-807">Assembly</span></span></td>
<td><span data-ttu-id="44456-808">10001</span><span class="sxs-lookup"><span data-stu-id="44456-808">10001</span></span></td>
<td><span data-ttu-id="44456-809">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-809">Electricity</span></span></td>
<td><span data-ttu-id="44456-810">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-810">Variable cost</span></span></td>
<td><span data-ttu-id="44456-811">685.14</span><span class="sxs-lookup"><span data-stu-id="44456-811">685.14</span></span></td>
<td><span data-ttu-id="44456-812">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-813">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-813">CC004</span></span></td>
<td><span data-ttu-id="44456-814">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-814">Packaging</span></span></td>
<td><span data-ttu-id="44456-815">10001</span><span class="sxs-lookup"><span data-stu-id="44456-815">10001</span></span></td>
<td><span data-ttu-id="44456-816">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-816">Electricity</span></span></td>
<td><span data-ttu-id="44456-817">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-817">Variable cost</span></span></td>
<td><span data-ttu-id="44456-818">124.57</span><span class="sxs-lookup"><span data-stu-id="44456-818">124.57</span></span></td>
<td><span data-ttu-id="44456-819">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-820">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-820">CC002</span></span></td>
<td><span data-ttu-id="44456-821">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-821">Finance</span></span></td>
<td><span data-ttu-id="44456-822">10001</span><span class="sxs-lookup"><span data-stu-id="44456-822">10001</span></span></td>
<td><span data-ttu-id="44456-823">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-823">Electricity</span></span></td>
<td><span data-ttu-id="44456-824">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-824">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="44456-825">-675.00</span></span></td>
<td><span data-ttu-id="44456-826">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-827">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-827">CC003</span></span></td>
<td><span data-ttu-id="44456-828">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-828">Assembly</span></span></td>
<td><span data-ttu-id="44456-829">10001</span><span class="sxs-lookup"><span data-stu-id="44456-829">10001</span></span></td>
<td><span data-ttu-id="44456-830">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-830">Electricity</span></span></td>
<td><span data-ttu-id="44456-831">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-831">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-832">438.75</span><span class="sxs-lookup"><span data-stu-id="44456-832">438.75</span></span></td>
<td><span data-ttu-id="44456-833">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-834">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-834">CC004</span></span></td>
<td><span data-ttu-id="44456-835">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-835">Packaging</span></span></td>
<td><span data-ttu-id="44456-836">10001</span><span class="sxs-lookup"><span data-stu-id="44456-836">10001</span></span></td>
<td><span data-ttu-id="44456-837">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-837">Electricity</span></span></td>
<td><span data-ttu-id="44456-838">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-838">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-839">236.25</span><span class="sxs-lookup"><span data-stu-id="44456-839">236.25</span></span></td>
<td><span data-ttu-id="44456-840">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-841">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-841">CC002</span></span></td>
<td><span data-ttu-id="44456-842">Finans</span><span class="sxs-lookup"><span data-stu-id="44456-842">Finance</span></span></td>
<td><span data-ttu-id="44456-843">10001</span><span class="sxs-lookup"><span data-stu-id="44456-843">10001</span></span></td>
<td><span data-ttu-id="44456-844">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-844">Electricity</span></span></td>
<td><span data-ttu-id="44456-845">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-845">Variable cost</span></span></td>
<td><span data-ttu-id="44456-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="44456-846">-8,150.29</span></span></td>
<td><span data-ttu-id="44456-847">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-848">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-848">CC003</span></span></td>
<td><span data-ttu-id="44456-849">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-849">Assembly</span></span></td>
<td><span data-ttu-id="44456-850">10001</span><span class="sxs-lookup"><span data-stu-id="44456-850">10001</span></span></td>
<td><span data-ttu-id="44456-851">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-851">Electricity</span></span></td>
<td><span data-ttu-id="44456-852">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-852">Variable cost</span></span></td>
<td><span data-ttu-id="44456-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="44456-853">5,297.69</span></span></td>
<td><span data-ttu-id="44456-854">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-855">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-855">CC004</span></span></td>
<td><span data-ttu-id="44456-856">Innpakning</span><span class="sxs-lookup"><span data-stu-id="44456-856">Packaging</span></span></td>
<td><span data-ttu-id="44456-857">10001</span><span class="sxs-lookup"><span data-stu-id="44456-857">10001</span></span></td>
<td><span data-ttu-id="44456-858">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-858">Electricity</span></span></td>
<td><span data-ttu-id="44456-859">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-859">Variable cost</span></span></td>
<td><span data-ttu-id="44456-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="44456-860">2,852.60</span></span></td>
<td><span data-ttu-id="44456-861">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-862">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-862">CC003</span></span></td>
<td><span data-ttu-id="44456-863">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-863">Assembly</span></span></td>
<td><span data-ttu-id="44456-864">10001</span><span class="sxs-lookup"><span data-stu-id="44456-864">10001</span></span></td>
<td><span data-ttu-id="44456-865">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-865">Electricity</span></span></td>
<td><span data-ttu-id="44456-866">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-866">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="44456-867">-713.75</span></span></td>
<td><span data-ttu-id="44456-868">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-869">Prod 1</span></span></td>
<td><span data-ttu-id="44456-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-870">Product 1</span></span></td>
<td><span data-ttu-id="44456-871">10001</span><span class="sxs-lookup"><span data-stu-id="44456-871">10001</span></span></td>
<td><span data-ttu-id="44456-872">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-872">Electricity</span></span></td>
<td><span data-ttu-id="44456-873">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-873">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-874">535.31</span><span class="sxs-lookup"><span data-stu-id="44456-874">535.31</span></span></td>
<td><span data-ttu-id="44456-875">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-876">Prod 2</span></span></td>
<td><span data-ttu-id="44456-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-877">Product 2</span></span></td>
<td><span data-ttu-id="44456-878">10001</span><span class="sxs-lookup"><span data-stu-id="44456-878">10001</span></span></td>
<td><span data-ttu-id="44456-879">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-879">Electricity</span></span></td>
<td><span data-ttu-id="44456-880">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-880">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-881">178.44</span><span class="sxs-lookup"><span data-stu-id="44456-881">178.44</span></span></td>
<td><span data-ttu-id="44456-882">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-883">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-883">CC003</span></span></td>
<td><span data-ttu-id="44456-884">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-884">Assembly</span></span></td>
<td><span data-ttu-id="44456-885">10001</span><span class="sxs-lookup"><span data-stu-id="44456-885">10001</span></span></td>
<td><span data-ttu-id="44456-886">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-886">Electricity</span></span></td>
<td><span data-ttu-id="44456-887">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-887">Variable cost</span></span></td>
<td><span data-ttu-id="44456-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="44456-888">-5,982.83</span></span></td>
<td><span data-ttu-id="44456-889">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-890">Prod 1</span></span></td>
<td><span data-ttu-id="44456-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-891">Product 1</span></span></td>
<td><span data-ttu-id="44456-892">10001</span><span class="sxs-lookup"><span data-stu-id="44456-892">10001</span></span></td>
<td><span data-ttu-id="44456-893">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-893">Electricity</span></span></td>
<td><span data-ttu-id="44456-894">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-894">Variable cost</span></span></td>
<td><span data-ttu-id="44456-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="44456-895">4,487.12</span></span></td>
<td><span data-ttu-id="44456-896">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-897">Prod 2</span></span></td>
<td><span data-ttu-id="44456-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-898">Product 2</span></span></td>
<td><span data-ttu-id="44456-899">10001</span><span class="sxs-lookup"><span data-stu-id="44456-899">10001</span></span></td>
<td><span data-ttu-id="44456-900">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-900">Electricity</span></span></td>
<td><span data-ttu-id="44456-901">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-901">Variable cost</span></span></td>
<td><span data-ttu-id="44456-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="44456-902">1,495.71</span></span></td>
<td><span data-ttu-id="44456-903">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-904">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-904">CC003</span></span></td>
<td><span data-ttu-id="44456-905">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-905">Assembly</span></span></td>
<td><span data-ttu-id="44456-906">10001</span><span class="sxs-lookup"><span data-stu-id="44456-906">10001</span></span></td>
<td><span data-ttu-id="44456-907">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-907">Electricity</span></span></td>
<td><span data-ttu-id="44456-908">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-908">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="44456-909">-286.25</span></span></td>
<td><span data-ttu-id="44456-910">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-911">Prod 1</span></span></td>
<td><span data-ttu-id="44456-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-912">Product 1</span></span></td>
<td><span data-ttu-id="44456-913">10001</span><span class="sxs-lookup"><span data-stu-id="44456-913">10001</span></span></td>
<td><span data-ttu-id="44456-914">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-914">Electricity</span></span></td>
<td><span data-ttu-id="44456-915">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-915">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-916">241.05</span><span class="sxs-lookup"><span data-stu-id="44456-916">241.05</span></span></td>
<td><span data-ttu-id="44456-917">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-918">Prod 2</span></span></td>
<td><span data-ttu-id="44456-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-919">Product 2</span></span></td>
<td><span data-ttu-id="44456-920">10001</span><span class="sxs-lookup"><span data-stu-id="44456-920">10001</span></span></td>
<td><span data-ttu-id="44456-921">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-921">Electricity</span></span></td>
<td><span data-ttu-id="44456-922">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-922">Fixed cost</span></span></td>
<td><span data-ttu-id="44456-923">45.20</span><span class="sxs-lookup"><span data-stu-id="44456-923">45.20</span></span></td>
<td><span data-ttu-id="44456-924">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-925">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-925">CC003</span></span></td>
<td><span data-ttu-id="44456-926">Samling</span><span class="sxs-lookup"><span data-stu-id="44456-926">Assembly</span></span></td>
<td><span data-ttu-id="44456-927">10001</span><span class="sxs-lookup"><span data-stu-id="44456-927">10001</span></span></td>
<td><span data-ttu-id="44456-928">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-928">Electricity</span></span></td>
<td><span data-ttu-id="44456-929">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-929">Variable cost</span></span></td>
<td><span data-ttu-id="44456-930">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="44456-930">-2,977.17</span></span></td>
<td><span data-ttu-id="44456-931">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-932">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-932">Prod 1</span></span></td>
<td><span data-ttu-id="44456-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="44456-933">Product 1</span></span></td>
<td><span data-ttu-id="44456-934">10001</span><span class="sxs-lookup"><span data-stu-id="44456-934">10001</span></span></td>
<td><span data-ttu-id="44456-935">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-935">Electricity</span></span></td>
<td><span data-ttu-id="44456-936">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-936">Variable cost</span></span></td>
<td><span data-ttu-id="44456-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="44456-937">2,507.09</span></span></td>
<td><span data-ttu-id="44456-938">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44456-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-939">Prod 2</span></span></td>
<td><span data-ttu-id="44456-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="44456-940">Product 2</span></span></td>
<td><span data-ttu-id="44456-941">10001</span><span class="sxs-lookup"><span data-stu-id="44456-941">10001</span></span></td>
<td><span data-ttu-id="44456-942">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="44456-942">Electricity</span></span></td>
<td><span data-ttu-id="44456-943">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-943">Variable cost</span></span></td>
<td><span data-ttu-id="44456-944">470.08</span><span class="sxs-lookup"><span data-stu-id="44456-944">470.08</span></span></td>
<td><span data-ttu-id="44456-945">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="44456-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="44456-946">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="44456-946">Conclusion</span></span>
<span data-ttu-id="44456-947">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="44456-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="44456-948">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="44456-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="44456-949">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="44456-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="44456-950">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="44456-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="44456-951">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="44456-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="44456-952">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="44456-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="44456-953">Sum</span><span class="sxs-lookup"><span data-stu-id="44456-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="44456-954">CC099</span><span class="sxs-lookup"><span data-stu-id="44456-954">CC099</span></span></th>
<th><span data-ttu-id="44456-955">CC001</span><span class="sxs-lookup"><span data-stu-id="44456-955">CC001</span></span></th>
<th><span data-ttu-id="44456-956">CC002</span><span class="sxs-lookup"><span data-stu-id="44456-956">CC002</span></span></th>
<th><span data-ttu-id="44456-957">CC003</span><span class="sxs-lookup"><span data-stu-id="44456-957">CC003</span></span></th>
<th><span data-ttu-id="44456-958">CC004</span><span class="sxs-lookup"><span data-stu-id="44456-958">CC004</span></span></th>
<th><span data-ttu-id="44456-959">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="44456-959">Proj 1</span></span></th>
<th><span data-ttu-id="44456-960">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="44456-960">Proj 2</span></span></th>
<th><span data-ttu-id="44456-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="44456-961">Prod 1</span></span></th>
<th><span data-ttu-id="44456-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="44456-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="44456-963">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="44456-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="44456-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="44456-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="44456-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="44456-973">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="44456-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-974">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="44456-975">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-976">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-977">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-978">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-979">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-980">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="44456-981">776.36</span><span class="sxs-lookup"><span data-stu-id="44456-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-982">223.64</span><span class="sxs-lookup"><span data-stu-id="44456-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="44456-984">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="44456-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-985">000</span><span class="sxs-lookup"><span data-stu-id="44456-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-986">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-987">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-988">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-989">0,00</span><span class="sxs-lookup"><span data-stu-id="44456-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-990">30,00</span><span class="sxs-lookup"><span data-stu-id="44456-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-991">10,00</span><span class="sxs-lookup"><span data-stu-id="44456-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="44456-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="44456-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="44456-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="44456-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="44456-995">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="44456-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="44456-996">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="44456-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="44456-997">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="44456-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="44456-998">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="44456-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="44456-999">Hvis du vil ha mer informasjon, kan du se policyen for kostnadsakkumulering.</span><span class="sxs-lookup"><span data-stu-id="44456-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="44456-1000">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="44456-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




