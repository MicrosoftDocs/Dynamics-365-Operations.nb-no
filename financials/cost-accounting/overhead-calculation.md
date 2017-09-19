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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: a8c867ba49b95af2816fe8294059307e974c0a81
ms.contentlocale: nb-no
ms.lasthandoff: 09/18/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="6394f-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6394f-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6394f-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="6394f-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6394f-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="6394f-105">Term definition</span></span>
---------------

<span data-ttu-id="6394f-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="6394f-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6394f-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="6394f-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6394f-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="6394f-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6394f-109">Leie</span><span class="sxs-lookup"><span data-stu-id="6394f-109">Rent</span></span>
-   <span data-ttu-id="6394f-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-110">Electricity</span></span>
-   <span data-ttu-id="6394f-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="6394f-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6394f-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6394f-112">Overhead calculation overview</span></span>
<span data-ttu-id="6394f-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="6394f-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6394f-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="6394f-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6394f-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="6394f-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6394f-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="6394f-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6394f-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="6394f-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6394f-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="6394f-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6394f-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="6394f-119">Version type</span></span>
-   <span data-ttu-id="6394f-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="6394f-120">Date and time</span></span>
-   <span data-ttu-id="6394f-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="6394f-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6394f-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="6394f-122">Fiscal year</span></span>
-   <span data-ttu-id="6394f-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="6394f-123">Fiscal period</span></span>

<span data-ttu-id="6394f-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="6394f-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6394f-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="6394f-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6394f-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6394f-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6394f-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="6394f-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6394f-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="6394f-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6394f-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="6394f-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6394f-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="6394f-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="6394f-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6394f-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6394f-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="6394f-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6394f-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="6394f-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6394f-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="6394f-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6394f-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="6394f-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6394f-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="6394f-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6394f-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6394f-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="6394f-140">Main account</span></span></th>
<th><span data-ttu-id="6394f-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="6394f-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6394f-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-143">CC099</span></span></td>
<td><span data-ttu-id="6394f-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-144">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-145">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-145">10001</span></span></td>
<td><span data-ttu-id="6394f-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-146">Electricity</span></span></td>
<td><span data-ttu-id="6394f-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6394f-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6394f-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="6394f-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6394f-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="6394f-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6394f-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6394f-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="6394f-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6394f-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="6394f-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6394f-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="6394f-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6394f-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="6394f-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6394f-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6394f-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="6394f-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6394f-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="6394f-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6394f-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-160">Journal</span></span></th>
<th><span data-ttu-id="6394f-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6394f-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6394f-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6394f-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6394f-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="6394f-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-164">00001</span><span class="sxs-lookup"><span data-stu-id="6394f-164">00001</span></span></td>
<td><span data-ttu-id="6394f-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6394f-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6394f-166">Fiscal</span></span></td>
<td><span data-ttu-id="6394f-167">2017</span><span class="sxs-lookup"><span data-stu-id="6394f-167">2017</span></span></td>
<td><span data-ttu-id="6394f-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-168">Period 1</span></span></td>
<td><span data-ttu-id="6394f-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6394f-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="6394f-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-173">Cost element</span></span></th>
<th><span data-ttu-id="6394f-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6394f-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-177">CC099</span></span></td>
<td><span data-ttu-id="6394f-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-178">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-179">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-179">10001</span></span></td>
<td><span data-ttu-id="6394f-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-180">Electricity</span></span></td>
<td><span data-ttu-id="6394f-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6394f-181">Unclassified</span></span></td>
<td><span data-ttu-id="6394f-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6394f-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6394f-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-185">Cost element</span></span></th>
<th><span data-ttu-id="6394f-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-187">Amount</span></span></th>
<th><span data-ttu-id="6394f-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-189">CC099</span></span></td>
<td><span data-ttu-id="6394f-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-190">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-191">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-191">10001</span></span></td>
<td><span data-ttu-id="6394f-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-192">Electricity</span></span></td>
<td><span data-ttu-id="6394f-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6394f-193">Unclassified</span></span></td>
<td><span data-ttu-id="6394f-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-194">10,000.00</span></span></td>
<td><span data-ttu-id="6394f-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-196">CC099</span></span></td>
<td><span data-ttu-id="6394f-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-197">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-198">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-198">10001</span></span></td>
<td><span data-ttu-id="6394f-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-199">Electricity</span></span></td>
<td><span data-ttu-id="6394f-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6394f-200">Unclassified</span></span></td>
<td><span data-ttu-id="6394f-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6394f-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-203">CC099</span></span></td>
<td><span data-ttu-id="6394f-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-204">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-205">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-205">10001</span></span></td>
<td><span data-ttu-id="6394f-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-206">Electricity</span></span></td>
<td><span data-ttu-id="6394f-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-208">1,000.00</span></span></td>
<td><span data-ttu-id="6394f-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-210">CC099</span></span></td>
<td><span data-ttu-id="6394f-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-211">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-212">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-212">10001</span></span></td>
<td><span data-ttu-id="6394f-213">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-213">Electricity</span></span></td>
<td><span data-ttu-id="6394f-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-214">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6394f-215">9,000.00</span></span></td>
<td><span data-ttu-id="6394f-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-217">Hvis du vil ha detaljert informasjon om kostnadsatferd, kan du se Policy for kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="6394f-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="6394f-218">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="6394f-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6394f-219">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="6394f-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6394f-220">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6394f-221">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="6394f-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6394f-222">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="6394f-222">Define the cost distribution rule</span></span>

<span data-ttu-id="6394f-223">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="6394f-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6394f-224">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="6394f-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6394f-225">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="6394f-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6394f-226">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="6394f-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6394f-227">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="6394f-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6394f-228">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-229">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-229">Cost object</span></span></th>
<th><span data-ttu-id="6394f-230">kWt</span><span class="sxs-lookup"><span data-stu-id="6394f-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-231">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-231">CC001</span></span></td>
<td><span data-ttu-id="6394f-232">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-232">HR</span></span></td>
<td><span data-ttu-id="6394f-233">1 000</span><span class="sxs-lookup"><span data-stu-id="6394f-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-234">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-234">CC002</span></span></td>
<td><span data-ttu-id="6394f-235">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-235">Finance</span></span></td>
<td><span data-ttu-id="6394f-236">6,000</span><span class="sxs-lookup"><span data-stu-id="6394f-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-237">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-237">CC003</span></span></td>
<td><span data-ttu-id="6394f-238">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-238">Assembly</span></span></td>
<td><span data-ttu-id="6394f-239">0</span><span class="sxs-lookup"><span data-stu-id="6394f-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-240">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="6394f-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-241">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-241">Cost object</span></span></th>
<th><span data-ttu-id="6394f-242">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-242">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-243">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-243">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-244">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-245">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-245">CC001</span></span></td>
<td><span data-ttu-id="6394f-246">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-246">HR</span></span></td>
<td><span data-ttu-id="6394f-247">1 000</span><span class="sxs-lookup"><span data-stu-id="6394f-247">1,000</span></span></td>
<td><span data-ttu-id="6394f-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6394f-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6394f-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-250">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-250">CC002</span></span></td>
<td><span data-ttu-id="6394f-251">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-251">Finance</span></span></td>
<td><span data-ttu-id="6394f-252">6,000</span><span class="sxs-lookup"><span data-stu-id="6394f-252">6,000</span></span></td>
<td><span data-ttu-id="6394f-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6394f-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6394f-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-255">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-255">CC003</span></span></td>
<td><span data-ttu-id="6394f-256">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-256">Assembly</span></span></td>
<td><span data-ttu-id="6394f-257">0</span><span class="sxs-lookup"><span data-stu-id="6394f-257">0</span></span></td>
<td><span data-ttu-id="6394f-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6394f-259">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-260">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="6394f-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6394f-261">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="6394f-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-262">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-262">Cost object</span></span></th>
<th><span data-ttu-id="6394f-263">Formel</span><span class="sxs-lookup"><span data-stu-id="6394f-263">Formula</span></span></th>
<th><span data-ttu-id="6394f-264">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-264">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-265">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-265">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-266">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-267">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-267">CC001</span></span></td>
<td><span data-ttu-id="6394f-268">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-268">HR</span></span></td>
<td><span data-ttu-id="6394f-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6394f-270">1</span><span class="sxs-lookup"><span data-stu-id="6394f-270">1</span></span></td>
<td><span data-ttu-id="6394f-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6394f-272">500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-273">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-273">CC002</span></span></td>
<td><span data-ttu-id="6394f-274">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-274">Finance</span></span></td>
<td><span data-ttu-id="6394f-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6394f-276">1</span><span class="sxs-lookup"><span data-stu-id="6394f-276">1</span></span></td>
<td><span data-ttu-id="6394f-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6394f-278">500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-279">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-279">CC003</span></span></td>
<td><span data-ttu-id="6394f-280">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-280">Assembly</span></span></td>
<td><span data-ttu-id="6394f-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6394f-282">0</span><span class="sxs-lookup"><span data-stu-id="6394f-282">0</span></span></td>
<td><span data-ttu-id="6394f-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6394f-284">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6394f-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-286">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-286">Journal</span></span></th>
<th><span data-ttu-id="6394f-287">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6394f-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6394f-288">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6394f-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6394f-289">Versjon</span><span class="sxs-lookup"><span data-stu-id="6394f-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-290">00002</span><span class="sxs-lookup"><span data-stu-id="6394f-290">00002</span></span></td>
<td><span data-ttu-id="6394f-291">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="6394f-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6394f-292">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6394f-292">Fiscal</span></span></td>
<td><span data-ttu-id="6394f-293">2017</span><span class="sxs-lookup"><span data-stu-id="6394f-293">2017</span></span></td>
<td><span data-ttu-id="6394f-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-294">Period 1</span></span></td>
<td><span data-ttu-id="6394f-295">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6394f-296">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="6394f-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-297">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-298">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-299">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-299">Cost element</span></span></th>
<th><span data-ttu-id="6394f-300">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-300">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-301">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-302">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-303">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-303">CC099</span></span></td>
<td><span data-ttu-id="6394f-304">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-304">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-305">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-305">10001</span></span></td>
<td><span data-ttu-id="6394f-306">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-306">Electricity</span></span></td>
<td><span data-ttu-id="6394f-307">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-307">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-309">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-310">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-310">CC099</span></span></td>
<td><span data-ttu-id="6394f-311">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-311">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-312">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-312">10001</span></span></td>
<td><span data-ttu-id="6394f-313">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-313">Electricity</span></span></td>
<td><span data-ttu-id="6394f-314">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-314">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6394f-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6394f-316">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6394f-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-317">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-318">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-318">Cost element</span></span></th>
<th><span data-ttu-id="6394f-319">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-319">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-320">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-320">Amount</span></span></th>
<th><span data-ttu-id="6394f-321">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-322">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-322">CC099</span></span></td>
<td><span data-ttu-id="6394f-323">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-323">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-324">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-324">10001</span></span></td>
<td><span data-ttu-id="6394f-325">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-325">Electricity</span></span></td>
<td><span data-ttu-id="6394f-326">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-326">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-327">-1,000.00</span></span></td>
<td><span data-ttu-id="6394f-328">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-329">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-329">CC001</span></span></td>
<td><span data-ttu-id="6394f-330">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-330">HR</span></span></td>
<td><span data-ttu-id="6394f-331">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-331">10001</span></span></td>
<td><span data-ttu-id="6394f-332">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-332">Electricity</span></span></td>
<td><span data-ttu-id="6394f-333">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-333">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-334">500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-334">500.00</span></span></td>
<td><span data-ttu-id="6394f-335">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-336">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-336">CC002</span></span></td>
<td><span data-ttu-id="6394f-337">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-337">Finance</span></span></td>
<td><span data-ttu-id="6394f-338">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-338">10001</span></span></td>
<td><span data-ttu-id="6394f-339">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-339">Electricity</span></span></td>
<td><span data-ttu-id="6394f-340">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-340">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-341">500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-341">500.00</span></span></td>
<td><span data-ttu-id="6394f-342">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-343">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-343">CC099</span></span></td>
<td><span data-ttu-id="6394f-344">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6394f-344">Default cost center</span></span></td>
<td><span data-ttu-id="6394f-345">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-345">10001</span></span></td>
<td><span data-ttu-id="6394f-346">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-346">Electricity</span></span></td>
<td><span data-ttu-id="6394f-347">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-347">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="6394f-348">-9,000.00</span></span></td>
<td><span data-ttu-id="6394f-349">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-350">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-350">CC001</span></span></td>
<td><span data-ttu-id="6394f-351">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-351">HR</span></span></td>
<td><span data-ttu-id="6394f-352">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-352">10001</span></span></td>
<td><span data-ttu-id="6394f-353">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-353">Electricity</span></span></td>
<td><span data-ttu-id="6394f-354">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-354">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6394f-355">1,285.71</span></span></td>
<td><span data-ttu-id="6394f-356">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-357">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-357">CC002</span></span></td>
<td><span data-ttu-id="6394f-358">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-358">Finance</span></span></td>
<td><span data-ttu-id="6394f-359">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-359">10001</span></span></td>
<td><span data-ttu-id="6394f-360">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-360">Electricity</span></span></td>
<td><span data-ttu-id="6394f-361">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-361">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6394f-362">7,714.29</span></span></td>
<td><span data-ttu-id="6394f-363">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-364">Hvis du vil ha detaljert informasjon om kostnadsdistribusjon og tildelingsgrunnlag, kan du se Kostnadsdistribusjonspolicy og Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="6394f-365">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="6394f-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6394f-366">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6394f-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6394f-367">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6394f-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6394f-368">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="6394f-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6394f-369">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6394f-369">Define the overhead rate</span></span>

<span data-ttu-id="6394f-370">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="6394f-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6394f-371">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6394f-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-372">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-372">Cost object</span></span></th>
<th><span data-ttu-id="6394f-373">Timeantall</span><span class="sxs-lookup"><span data-stu-id="6394f-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-374">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-374">Proj 1</span></span></td>
<td><span data-ttu-id="6394f-375">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-375">Project 1</span></span></td>
<td><span data-ttu-id="6394f-376">3</span><span class="sxs-lookup"><span data-stu-id="6394f-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-377">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-377">Proj 2</span></span></td>
<td><span data-ttu-id="6394f-378">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-378">Project 2</span></span></td>
<td><span data-ttu-id="6394f-379">1</span><span class="sxs-lookup"><span data-stu-id="6394f-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-380">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="6394f-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-381">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-381">Cost object</span></span></th>
<th><span data-ttu-id="6394f-382">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-382">Cost element</span></span></th>
<th><span data-ttu-id="6394f-383">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-383">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-384">Enheter</span><span class="sxs-lookup"><span data-stu-id="6394f-384">Units</span></span></th>
<th><span data-ttu-id="6394f-385">Sats</span><span class="sxs-lookup"><span data-stu-id="6394f-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-386">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-386">CC001</span></span></td>
<td><span data-ttu-id="6394f-387">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-387">HR</span></span></td>
<td><span data-ttu-id="6394f-388">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-388">10001</span></span></td>
<td><span data-ttu-id="6394f-389">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-389">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-390">1</span><span class="sxs-lookup"><span data-stu-id="6394f-390">1</span></span></td>
<td><span data-ttu-id="6394f-391">10</span><span class="sxs-lookup"><span data-stu-id="6394f-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-392">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-393">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-393">Cost object</span></span></th>
<th><span data-ttu-id="6394f-394">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-394">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-395">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-395">Cost element</span></span></th>
<th><span data-ttu-id="6394f-396">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-396">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-397">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-398">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-398">Proj 1</span></span></td>
<td><span data-ttu-id="6394f-399">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-399">Project 1</span></span></td>
<td><span data-ttu-id="6394f-400">3</span><span class="sxs-lookup"><span data-stu-id="6394f-400">3</span></span></td>
<td><span data-ttu-id="6394f-401">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-401">10001</span></span></td>
<td><span data-ttu-id="6394f-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6394f-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6394f-403">30,00</span><span class="sxs-lookup"><span data-stu-id="6394f-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-404">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-404">Proj 2</span></span></td>
<td><span data-ttu-id="6394f-405">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-405">Project 2</span></span></td>
<td><span data-ttu-id="6394f-406">1</span><span class="sxs-lookup"><span data-stu-id="6394f-406">1</span></span></td>
<td><span data-ttu-id="6394f-407">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-407">10001</span></span></td>
<td><span data-ttu-id="6394f-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6394f-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6394f-409">10,00</span><span class="sxs-lookup"><span data-stu-id="6394f-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6394f-410">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-411">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-411">Journal</span></span></th>
<th><span data-ttu-id="6394f-412">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6394f-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6394f-413">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6394f-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6394f-414">Versjon</span><span class="sxs-lookup"><span data-stu-id="6394f-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-415">00003</span><span class="sxs-lookup"><span data-stu-id="6394f-415">00003</span></span></td>
<td><span data-ttu-id="6394f-416">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6394f-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6394f-417">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6394f-417">Fiscal</span></span></td>
<td><span data-ttu-id="6394f-418">2017</span><span class="sxs-lookup"><span data-stu-id="6394f-418">2017</span></span></td>
<td><span data-ttu-id="6394f-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-419">Period 1</span></span></td>
<td><span data-ttu-id="6394f-420">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6394f-421">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="6394f-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-422">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-423">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-423">Cost object</span></span></th>
<th><span data-ttu-id="6394f-424">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-425">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-426">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-426">Proj 1</span></span></td>
<td><span data-ttu-id="6394f-427">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6394f-428">3,00</span><span class="sxs-lookup"><span data-stu-id="6394f-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-429">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-430">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-430">Proj 2</span></span></td>
<td><span data-ttu-id="6394f-431">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6394f-432">1,00</span><span class="sxs-lookup"><span data-stu-id="6394f-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6394f-433">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6394f-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-434">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-435">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-435">Cost element</span></span></th>
<th><span data-ttu-id="6394f-436">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-436">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-437">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-437">Amount</span></span></th>
<th><span data-ttu-id="6394f-438">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="6394f-439">CC0001</span></span></td>
<td><span data-ttu-id="6394f-440">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-440">HR</span></span></td>
<td><span data-ttu-id="6394f-441">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-441">10001</span></span></td>
<td><span data-ttu-id="6394f-442">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-442">Electricity</span></span></td>
<td><span data-ttu-id="6394f-443">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-443">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="6394f-444">-30.00</span></span></td>
<td><span data-ttu-id="6394f-445">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-446">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-446">Proj 1</span></span></td>
<td><span data-ttu-id="6394f-447">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6394f-448">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-448">10001</span></span></td>
<td><span data-ttu-id="6394f-449">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-449">Electricity</span></span></td>
<td><span data-ttu-id="6394f-450">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-450">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-451">30,00</span><span class="sxs-lookup"><span data-stu-id="6394f-451">30.00</span></span></td>
<td><span data-ttu-id="6394f-452">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-453">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-453">CC001</span></span></td>
<td><span data-ttu-id="6394f-454">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-454">HR</span></span></td>
<td><span data-ttu-id="6394f-455">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-455">10001</span></span></td>
<td><span data-ttu-id="6394f-456">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-456">Electricity</span></span></td>
<td><span data-ttu-id="6394f-457">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-457">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="6394f-458">-10.00</span></span></td>
<td><span data-ttu-id="6394f-459">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-460">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-460">Proj 2</span></span></td>
<td><span data-ttu-id="6394f-461">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6394f-462">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-462">10001</span></span></td>
<td><span data-ttu-id="6394f-463">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-463">Electricity</span></span></td>
<td><span data-ttu-id="6394f-464">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-464">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-465">10,00</span><span class="sxs-lookup"><span data-stu-id="6394f-465">10.00</span></span></td>
<td><span data-ttu-id="6394f-466">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-467">Hvis du vil ha mer informasjon om policyen for sats for indirekte kostnader, kan du se Policy for sats for indirekte kostnader og Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="6394f-468">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="6394f-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6394f-469">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="6394f-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6394f-470">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6394f-471">Finance and Operations støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="6394f-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="6394f-472">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="6394f-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6394f-473">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="6394f-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6394f-474">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6394f-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6394f-475">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="6394f-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6394f-476">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="6394f-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="6394f-477">[![Gjensidige metode](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="6394f-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6394f-478">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="6394f-478">Define the cost allocation</span></span>

<span data-ttu-id="6394f-479">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="6394f-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6394f-480">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6394f-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6394f-481">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6394f-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-482">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-482">Cost object</span></span></th>
<th><span data-ttu-id="6394f-483">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="6394f-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-484">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-484">CC002</span></span></td>
<td><span data-ttu-id="6394f-485">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-485">Finance</span></span></td>
<td><span data-ttu-id="6394f-486">35</span><span class="sxs-lookup"><span data-stu-id="6394f-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-487">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-487">CC003</span></span></td>
<td><span data-ttu-id="6394f-488">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-488">Assembly</span></span></td>
<td><span data-ttu-id="6394f-489">55</span><span class="sxs-lookup"><span data-stu-id="6394f-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-490">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-490">CC004</span></span></td>
<td><span data-ttu-id="6394f-491">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-491">Packaging</span></span></td>
<td><span data-ttu-id="6394f-492">10</span><span class="sxs-lookup"><span data-stu-id="6394f-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-493">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6394f-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6394f-494">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6394f-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-495">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-495">Cost object</span></span></th>
<th><span data-ttu-id="6394f-496">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="6394f-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-497">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-497">CC003</span></span></td>
<td><span data-ttu-id="6394f-498">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-498">Assembly</span></span></td>
<td><span data-ttu-id="6394f-499">65</span><span class="sxs-lookup"><span data-stu-id="6394f-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-500">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-500">CC004</span></span></td>
<td><span data-ttu-id="6394f-501">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-501">Packaging</span></span></td>
<td><span data-ttu-id="6394f-502">35</span><span class="sxs-lookup"><span data-stu-id="6394f-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-503">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6394f-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6394f-504">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6394f-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-505">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-505">Cost object</span></span></th>
<th><span data-ttu-id="6394f-506">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="6394f-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-507">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-508">Product 1</span></span></td>
<td><span data-ttu-id="6394f-509">60</span><span class="sxs-lookup"><span data-stu-id="6394f-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-510">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-511">Product 2</span></span></td>
<td><span data-ttu-id="6394f-512">20</span><span class="sxs-lookup"><span data-stu-id="6394f-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-513">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6394f-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6394f-514">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6394f-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-515">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-515">Cost object</span></span></th>
<th><span data-ttu-id="6394f-516">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="6394f-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-517">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-517">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-518">Product 1</span></span></td>
<td><span data-ttu-id="6394f-519">80</span><span class="sxs-lookup"><span data-stu-id="6394f-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-520">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-521">Product 2</span></span></td>
<td><span data-ttu-id="6394f-522">15</span><span class="sxs-lookup"><span data-stu-id="6394f-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-523">**Obs!** I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="6394f-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6394f-524">Hvis du vil ha mer informasjon om statistiske målleverandører, kan du se Maler for leverandør av statistisk måling.</span><span class="sxs-lookup"><span data-stu-id="6394f-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="6394f-525">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.) Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6394f-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-526">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-526">Cost object</span></span></th>
<th><span data-ttu-id="6394f-527">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-527">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-528">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-528">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-529">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-529">Amount</span></span></th>
<th><span data-ttu-id="6394f-530">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-531">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-531">CC002</span></span></td>
<td><span data-ttu-id="6394f-532">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-532">Finance</span></span></td>
<td><span data-ttu-id="6394f-533">35</span><span class="sxs-lookup"><span data-stu-id="6394f-533">35</span></span></td>
<td><span data-ttu-id="6394f-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6394f-535">175.00</span><span class="sxs-lookup"><span data-stu-id="6394f-535">175.00</span></span></td>
<td><span data-ttu-id="6394f-536">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-537">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-537">CC003</span></span></td>
<td><span data-ttu-id="6394f-538">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-538">Assembly</span></span></td>
<td><span data-ttu-id="6394f-539">55</span><span class="sxs-lookup"><span data-stu-id="6394f-539">55</span></span></td>
<td><span data-ttu-id="6394f-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6394f-541">275.00</span><span class="sxs-lookup"><span data-stu-id="6394f-541">275.00</span></span></td>
<td><span data-ttu-id="6394f-542">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-543">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-543">CC004</span></span></td>
<td><span data-ttu-id="6394f-544">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-544">Packaging</span></span></td>
<td><span data-ttu-id="6394f-545">10</span><span class="sxs-lookup"><span data-stu-id="6394f-545">10</span></span></td>
<td><span data-ttu-id="6394f-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6394f-547">50,00</span><span class="sxs-lookup"><span data-stu-id="6394f-547">50.00</span></span></td>
<td><span data-ttu-id="6394f-548">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-549">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-549">CC002</span></span></td>
<td><span data-ttu-id="6394f-550">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-550">Finance</span></span></td>
<td><span data-ttu-id="6394f-551">35</span><span class="sxs-lookup"><span data-stu-id="6394f-551">35</span></span></td>
<td><span data-ttu-id="6394f-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6394f-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6394f-553">436.00</span><span class="sxs-lookup"><span data-stu-id="6394f-553">436.00</span></span></td>
<td><span data-ttu-id="6394f-554">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-555">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-555">CC003</span></span></td>
<td><span data-ttu-id="6394f-556">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-556">Assembly</span></span></td>
<td><span data-ttu-id="6394f-557">55</span><span class="sxs-lookup"><span data-stu-id="6394f-557">55</span></span></td>
<td><span data-ttu-id="6394f-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6394f-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6394f-559">685.14</span><span class="sxs-lookup"><span data-stu-id="6394f-559">685.14</span></span></td>
<td><span data-ttu-id="6394f-560">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-561">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-561">CC004</span></span></td>
<td><span data-ttu-id="6394f-562">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-562">Packaging</span></span></td>
<td><span data-ttu-id="6394f-563">10</span><span class="sxs-lookup"><span data-stu-id="6394f-563">10</span></span></td>
<td><span data-ttu-id="6394f-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6394f-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6394f-565">124.57</span><span class="sxs-lookup"><span data-stu-id="6394f-565">124.57</span></span></td>
<td><span data-ttu-id="6394f-566">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-567">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6394f-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-568">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-568">Cost object</span></span></th>
<th><span data-ttu-id="6394f-569">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-569">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-570">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-570">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-571">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-571">Amount</span></span></th>
<th><span data-ttu-id="6394f-572">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-573">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-573">CC003</span></span></td>
<td><span data-ttu-id="6394f-574">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-574">Assembly</span></span></td>
<td><span data-ttu-id="6394f-575">65</span><span class="sxs-lookup"><span data-stu-id="6394f-575">65</span></span></td>
<td><span data-ttu-id="6394f-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6394f-577">438.75</span><span class="sxs-lookup"><span data-stu-id="6394f-577">438.75</span></span></td>
<td><span data-ttu-id="6394f-578">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-579">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-579">CC004</span></span></td>
<td><span data-ttu-id="6394f-580">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-580">Packaging</span></span></td>
<td><span data-ttu-id="6394f-581">35</span><span class="sxs-lookup"><span data-stu-id="6394f-581">35</span></span></td>
<td><span data-ttu-id="6394f-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6394f-583">236.25</span><span class="sxs-lookup"><span data-stu-id="6394f-583">236.25</span></span></td>
<td><span data-ttu-id="6394f-584">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-585">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-585">CC003</span></span></td>
<td><span data-ttu-id="6394f-586">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-586">Assembly</span></span></td>
<td><span data-ttu-id="6394f-587">65</span><span class="sxs-lookup"><span data-stu-id="6394f-587">65</span></span></td>
<td><span data-ttu-id="6394f-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6394f-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6394f-589">5,297.69</span></span></td>
<td><span data-ttu-id="6394f-590">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-591">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-591">CC004</span></span></td>
<td><span data-ttu-id="6394f-592">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-592">Packaging</span></span></td>
<td><span data-ttu-id="6394f-593">35</span><span class="sxs-lookup"><span data-stu-id="6394f-593">35</span></span></td>
<td><span data-ttu-id="6394f-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6394f-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6394f-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6394f-595">2,852.60</span></span></td>
<td><span data-ttu-id="6394f-596">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-597">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6394f-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-598">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-598">Cost object</span></span></th>
<th><span data-ttu-id="6394f-599">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-599">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-600">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-600">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-601">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-601">Amount</span></span></th>
<th><span data-ttu-id="6394f-602">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-603">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-604">Product 1</span></span></td>
<td><span data-ttu-id="6394f-605">60</span><span class="sxs-lookup"><span data-stu-id="6394f-605">60</span></span></td>
<td><span data-ttu-id="6394f-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6394f-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6394f-607">535.31</span><span class="sxs-lookup"><span data-stu-id="6394f-607">535.31</span></span></td>
<td><span data-ttu-id="6394f-608">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-609">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-610">Product 2</span></span></td>
<td><span data-ttu-id="6394f-611">20</span><span class="sxs-lookup"><span data-stu-id="6394f-611">20</span></span></td>
<td><span data-ttu-id="6394f-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6394f-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6394f-613">178.44</span><span class="sxs-lookup"><span data-stu-id="6394f-613">178.44</span></span></td>
<td><span data-ttu-id="6394f-614">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-615">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-616">Product 1</span></span></td>
<td><span data-ttu-id="6394f-617">60</span><span class="sxs-lookup"><span data-stu-id="6394f-617">60</span></span></td>
<td><span data-ttu-id="6394f-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6394f-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6394f-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6394f-619">4,487.12</span></span></td>
<td><span data-ttu-id="6394f-620">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-621">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-622">Product 2</span></span></td>
<td><span data-ttu-id="6394f-623">20</span><span class="sxs-lookup"><span data-stu-id="6394f-623">20</span></span></td>
<td><span data-ttu-id="6394f-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6394f-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6394f-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6394f-625">1,495.71</span></span></td>
<td><span data-ttu-id="6394f-626">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6394f-627">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6394f-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-628">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-628">Cost object</span></span></th>
<th><span data-ttu-id="6394f-629">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6394f-629">Magnitude</span></span></th>
<th><span data-ttu-id="6394f-630">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6394f-630">Allocation factor</span></span></th>
<th><span data-ttu-id="6394f-631">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-631">Amount</span></span></th>
<th><span data-ttu-id="6394f-632">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-633">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-634">Product 1</span></span></td>
<td><span data-ttu-id="6394f-635">80</span><span class="sxs-lookup"><span data-stu-id="6394f-635">80</span></span></td>
<td><span data-ttu-id="6394f-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6394f-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6394f-637">241.05</span><span class="sxs-lookup"><span data-stu-id="6394f-637">241.05</span></span></td>
<td><span data-ttu-id="6394f-638">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-639">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-640">Product 2</span></span></td>
<td><span data-ttu-id="6394f-641">15</span><span class="sxs-lookup"><span data-stu-id="6394f-641">15</span></span></td>
<td><span data-ttu-id="6394f-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6394f-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6394f-643">45.20</span><span class="sxs-lookup"><span data-stu-id="6394f-643">45.20</span></span></td>
<td><span data-ttu-id="6394f-644">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-645">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-646">Product 1</span></span></td>
<td><span data-ttu-id="6394f-647">80</span><span class="sxs-lookup"><span data-stu-id="6394f-647">80</span></span></td>
<td><span data-ttu-id="6394f-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6394f-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6394f-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6394f-649">2,507.09</span></span></td>
<td><span data-ttu-id="6394f-650">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-651">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-652">Product 2</span></span></td>
<td><span data-ttu-id="6394f-653">15</span><span class="sxs-lookup"><span data-stu-id="6394f-653">15</span></span></td>
<td><span data-ttu-id="6394f-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6394f-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6394f-655">470.08</span><span class="sxs-lookup"><span data-stu-id="6394f-655">470.08</span></span></td>
<td><span data-ttu-id="6394f-656">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6394f-657">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="6394f-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-658">Journalen</span><span class="sxs-lookup"><span data-stu-id="6394f-658">Journal</span></span></th>
<th><span data-ttu-id="6394f-659">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6394f-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6394f-660">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6394f-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6394f-661">Versjon</span><span class="sxs-lookup"><span data-stu-id="6394f-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-662">00004</span><span class="sxs-lookup"><span data-stu-id="6394f-662">00004</span></span></td>
<td><span data-ttu-id="6394f-663">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="6394f-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6394f-664">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6394f-664">Fiscal</span></span></td>
<td><span data-ttu-id="6394f-665">2017</span><span class="sxs-lookup"><span data-stu-id="6394f-665">2017</span></span></td>
<td><span data-ttu-id="6394f-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-666">Period 1</span></span></td>
<td><span data-ttu-id="6394f-667">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6394f-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6394f-668">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="6394f-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6394f-669">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-670">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-671">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-671">Cost element</span></span></th>
<th><span data-ttu-id="6394f-672">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-672">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-673">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-674">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-675">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-675">CC001</span></span></td>
<td><span data-ttu-id="6394f-676">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-676">HR</span></span></td>
<td><span data-ttu-id="6394f-677">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-677">10001</span></span></td>
<td><span data-ttu-id="6394f-678">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-678">Electricity</span></span></td>
<td><span data-ttu-id="6394f-679">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-679">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-680">500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-681">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-682">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-682">CC001</span></span></td>
<td><span data-ttu-id="6394f-683">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-683">HR</span></span></td>
<td><span data-ttu-id="6394f-684">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-684">10001</span></span></td>
<td><span data-ttu-id="6394f-685">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-685">Electricity</span></span></td>
<td><span data-ttu-id="6394f-686">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-686">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6394f-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-688">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-689">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-689">CC002</span></span></td>
<td><span data-ttu-id="6394f-690">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-690">Finance</span></span></td>
<td><span data-ttu-id="6394f-691">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-691">10001</span></span></td>
<td><span data-ttu-id="6394f-692">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-692">Electricity</span></span></td>
<td><span data-ttu-id="6394f-693">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-693">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-694">675.00</span><span class="sxs-lookup"><span data-stu-id="6394f-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-695">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-696">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-696">CC002</span></span></td>
<td><span data-ttu-id="6394f-697">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-697">Finance</span></span></td>
<td><span data-ttu-id="6394f-698">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-698">10001</span></span></td>
<td><span data-ttu-id="6394f-699">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-699">Electricity</span></span></td>
<td><span data-ttu-id="6394f-700">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-700">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6394f-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-702">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-703">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-703">CC003</span></span></td>
<td><span data-ttu-id="6394f-704">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-704">Assembly</span></span></td>
<td><span data-ttu-id="6394f-705">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-705">10001</span></span></td>
<td><span data-ttu-id="6394f-706">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-706">Electricity</span></span></td>
<td><span data-ttu-id="6394f-707">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-707">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-708">713.75</span><span class="sxs-lookup"><span data-stu-id="6394f-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-709">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-710">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-710">CC003</span></span></td>
<td><span data-ttu-id="6394f-711">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-711">Assembly</span></span></td>
<td><span data-ttu-id="6394f-712">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-712">10001</span></span></td>
<td><span data-ttu-id="6394f-713">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-713">Electricity</span></span></td>
<td><span data-ttu-id="6394f-714">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-714">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6394f-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-716">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-717">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-717">CC003</span></span></td>
<td><span data-ttu-id="6394f-718">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-718">Packaging</span></span></td>
<td><span data-ttu-id="6394f-719">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-719">10001</span></span></td>
<td><span data-ttu-id="6394f-720">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-720">Electricity</span></span></td>
<td><span data-ttu-id="6394f-721">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-721">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-722">286.25</span><span class="sxs-lookup"><span data-stu-id="6394f-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-723">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-724">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-724">CC003</span></span></td>
<td><span data-ttu-id="6394f-725">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-725">Packaging</span></span></td>
<td><span data-ttu-id="6394f-726">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-726">10001</span></span></td>
<td><span data-ttu-id="6394f-727">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-727">Electricity</span></span></td>
<td><span data-ttu-id="6394f-728">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-728">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6394f-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-730">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-731">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-732">Product 1</span></span></td>
<td><span data-ttu-id="6394f-733">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-733">10001</span></span></td>
<td><span data-ttu-id="6394f-734">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-734">Electricity</span></span></td>
<td><span data-ttu-id="6394f-735">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-735">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-736">776.36</span><span class="sxs-lookup"><span data-stu-id="6394f-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-737">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-738">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-739">Product 1</span></span></td>
<td><span data-ttu-id="6394f-740">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-740">10001</span></span></td>
<td><span data-ttu-id="6394f-741">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-741">Electricity</span></span></td>
<td><span data-ttu-id="6394f-742">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-742">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6394f-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-744">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-745">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-746">Product 1</span></span></td>
<td><span data-ttu-id="6394f-747">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-747">10001</span></span></td>
<td><span data-ttu-id="6394f-748">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-748">Electricity</span></span></td>
<td><span data-ttu-id="6394f-749">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-749">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-750">223.64</span><span class="sxs-lookup"><span data-stu-id="6394f-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-751">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="6394f-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-752">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-753">Product 1</span></span></td>
<td><span data-ttu-id="6394f-754">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-754">10001</span></span></td>
<td><span data-ttu-id="6394f-755">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-755">Electricity</span></span></td>
<td><span data-ttu-id="6394f-756">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-756">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6394f-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6394f-758">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6394f-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6394f-759">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6394f-760">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-760">Cost element</span></span></th>
<th><span data-ttu-id="6394f-761">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6394f-761">Cost behavior</span></span></th>
<th><span data-ttu-id="6394f-762">Beløp</span><span class="sxs-lookup"><span data-stu-id="6394f-762">Amount</span></span></th>
<th><span data-ttu-id="6394f-763">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6394f-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6394f-764">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-764">CC001</span></span></td>
<td><span data-ttu-id="6394f-765">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-765">HR</span></span></td>
<td><span data-ttu-id="6394f-766">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-766">10001</span></span></td>
<td><span data-ttu-id="6394f-767">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-767">Electricity</span></span></td>
<td><span data-ttu-id="6394f-768">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-768">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="6394f-769">-500.00</span></span></td>
<td><span data-ttu-id="6394f-770">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-771">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-771">CC002</span></span></td>
<td><span data-ttu-id="6394f-772">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-772">Finance</span></span></td>
<td><span data-ttu-id="6394f-773">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-773">10001</span></span></td>
<td><span data-ttu-id="6394f-774">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-774">Electricity</span></span></td>
<td><span data-ttu-id="6394f-775">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-775">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-776">175.00</span><span class="sxs-lookup"><span data-stu-id="6394f-776">175.00</span></span></td>
<td><span data-ttu-id="6394f-777">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-778">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-778">CC003</span></span></td>
<td><span data-ttu-id="6394f-779">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-779">Assembly</span></span></td>
<td><span data-ttu-id="6394f-780">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-780">10001</span></span></td>
<td><span data-ttu-id="6394f-781">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-781">Electricity</span></span></td>
<td><span data-ttu-id="6394f-782">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-782">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-783">275.00</span><span class="sxs-lookup"><span data-stu-id="6394f-783">275.00</span></span></td>
<td><span data-ttu-id="6394f-784">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-785">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-785">CC004</span></span></td>
<td><span data-ttu-id="6394f-786">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-786">Packaging</span></span></td>
<td><span data-ttu-id="6394f-787">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-787">10001</span></span></td>
<td><span data-ttu-id="6394f-788">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-788">Electricity</span></span></td>
<td><span data-ttu-id="6394f-789">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-789">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-790">50,00</span><span class="sxs-lookup"><span data-stu-id="6394f-790">50,00</span></span></td>
<td><span data-ttu-id="6394f-791">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-792">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-792">CC001</span></span></td>
<td><span data-ttu-id="6394f-793">Personale</span><span class="sxs-lookup"><span data-stu-id="6394f-793">HR</span></span></td>
<td><span data-ttu-id="6394f-794">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-794">10001</span></span></td>
<td><span data-ttu-id="6394f-795">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-795">Electricity</span></span></td>
<td><span data-ttu-id="6394f-796">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-796">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="6394f-797">-1,245.71</span></span></td>
<td><span data-ttu-id="6394f-798">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-799">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-799">CC002</span></span></td>
<td><span data-ttu-id="6394f-800">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-800">Finance</span></span></td>
<td><span data-ttu-id="6394f-801">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-801">10001</span></span></td>
<td><span data-ttu-id="6394f-802">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-802">Electricity</span></span></td>
<td><span data-ttu-id="6394f-803">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-803">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-804">436.00</span><span class="sxs-lookup"><span data-stu-id="6394f-804">436.00</span></span></td>
<td><span data-ttu-id="6394f-805">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-806">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-806">CC003</span></span></td>
<td><span data-ttu-id="6394f-807">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-807">Assembly</span></span></td>
<td><span data-ttu-id="6394f-808">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-808">10001</span></span></td>
<td><span data-ttu-id="6394f-809">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-809">Electricity</span></span></td>
<td><span data-ttu-id="6394f-810">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-810">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-811">685.14</span><span class="sxs-lookup"><span data-stu-id="6394f-811">685.14</span></span></td>
<td><span data-ttu-id="6394f-812">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-813">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-813">CC004</span></span></td>
<td><span data-ttu-id="6394f-814">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-814">Packaging</span></span></td>
<td><span data-ttu-id="6394f-815">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-815">10001</span></span></td>
<td><span data-ttu-id="6394f-816">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-816">Electricity</span></span></td>
<td><span data-ttu-id="6394f-817">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-817">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-818">124.57</span><span class="sxs-lookup"><span data-stu-id="6394f-818">124.57</span></span></td>
<td><span data-ttu-id="6394f-819">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-820">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-820">CC002</span></span></td>
<td><span data-ttu-id="6394f-821">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-821">Finance</span></span></td>
<td><span data-ttu-id="6394f-822">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-822">10001</span></span></td>
<td><span data-ttu-id="6394f-823">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-823">Electricity</span></span></td>
<td><span data-ttu-id="6394f-824">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-824">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="6394f-825">-675.00</span></span></td>
<td><span data-ttu-id="6394f-826">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-827">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-827">CC003</span></span></td>
<td><span data-ttu-id="6394f-828">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-828">Assembly</span></span></td>
<td><span data-ttu-id="6394f-829">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-829">10001</span></span></td>
<td><span data-ttu-id="6394f-830">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-830">Electricity</span></span></td>
<td><span data-ttu-id="6394f-831">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-831">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-832">438.75</span><span class="sxs-lookup"><span data-stu-id="6394f-832">438.75</span></span></td>
<td><span data-ttu-id="6394f-833">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-834">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-834">CC004</span></span></td>
<td><span data-ttu-id="6394f-835">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-835">Packaging</span></span></td>
<td><span data-ttu-id="6394f-836">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-836">10001</span></span></td>
<td><span data-ttu-id="6394f-837">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-837">Electricity</span></span></td>
<td><span data-ttu-id="6394f-838">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-838">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-839">236.25</span><span class="sxs-lookup"><span data-stu-id="6394f-839">236.25</span></span></td>
<td><span data-ttu-id="6394f-840">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-841">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-841">CC002</span></span></td>
<td><span data-ttu-id="6394f-842">Finans</span><span class="sxs-lookup"><span data-stu-id="6394f-842">Finance</span></span></td>
<td><span data-ttu-id="6394f-843">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-843">10001</span></span></td>
<td><span data-ttu-id="6394f-844">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-844">Electricity</span></span></td>
<td><span data-ttu-id="6394f-845">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-845">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="6394f-846">-8,150.29</span></span></td>
<td><span data-ttu-id="6394f-847">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-848">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-848">CC003</span></span></td>
<td><span data-ttu-id="6394f-849">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-849">Assembly</span></span></td>
<td><span data-ttu-id="6394f-850">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-850">10001</span></span></td>
<td><span data-ttu-id="6394f-851">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-851">Electricity</span></span></td>
<td><span data-ttu-id="6394f-852">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-852">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6394f-853">5,297.69</span></span></td>
<td><span data-ttu-id="6394f-854">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-855">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-855">CC004</span></span></td>
<td><span data-ttu-id="6394f-856">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6394f-856">Packaging</span></span></td>
<td><span data-ttu-id="6394f-857">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-857">10001</span></span></td>
<td><span data-ttu-id="6394f-858">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-858">Electricity</span></span></td>
<td><span data-ttu-id="6394f-859">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-859">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6394f-860">2,852.60</span></span></td>
<td><span data-ttu-id="6394f-861">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-862">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-862">CC003</span></span></td>
<td><span data-ttu-id="6394f-863">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-863">Assembly</span></span></td>
<td><span data-ttu-id="6394f-864">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-864">10001</span></span></td>
<td><span data-ttu-id="6394f-865">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-865">Electricity</span></span></td>
<td><span data-ttu-id="6394f-866">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-866">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="6394f-867">-713.75</span></span></td>
<td><span data-ttu-id="6394f-868">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-869">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-870">Product 1</span></span></td>
<td><span data-ttu-id="6394f-871">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-871">10001</span></span></td>
<td><span data-ttu-id="6394f-872">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-872">Electricity</span></span></td>
<td><span data-ttu-id="6394f-873">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-873">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-874">535.31</span><span class="sxs-lookup"><span data-stu-id="6394f-874">535.31</span></span></td>
<td><span data-ttu-id="6394f-875">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-876">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-877">Product 2</span></span></td>
<td><span data-ttu-id="6394f-878">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-878">10001</span></span></td>
<td><span data-ttu-id="6394f-879">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-879">Electricity</span></span></td>
<td><span data-ttu-id="6394f-880">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-880">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-881">178.44</span><span class="sxs-lookup"><span data-stu-id="6394f-881">178.44</span></span></td>
<td><span data-ttu-id="6394f-882">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-883">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-883">CC003</span></span></td>
<td><span data-ttu-id="6394f-884">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-884">Assembly</span></span></td>
<td><span data-ttu-id="6394f-885">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-885">10001</span></span></td>
<td><span data-ttu-id="6394f-886">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-886">Electricity</span></span></td>
<td><span data-ttu-id="6394f-887">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-887">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="6394f-888">-5,982.83</span></span></td>
<td><span data-ttu-id="6394f-889">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-890">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-891">Product 1</span></span></td>
<td><span data-ttu-id="6394f-892">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-892">10001</span></span></td>
<td><span data-ttu-id="6394f-893">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-893">Electricity</span></span></td>
<td><span data-ttu-id="6394f-894">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-894">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6394f-895">4,487.12</span></span></td>
<td><span data-ttu-id="6394f-896">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-897">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-898">Product 2</span></span></td>
<td><span data-ttu-id="6394f-899">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-899">10001</span></span></td>
<td><span data-ttu-id="6394f-900">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-900">Electricity</span></span></td>
<td><span data-ttu-id="6394f-901">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-901">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6394f-902">1,495.71</span></span></td>
<td><span data-ttu-id="6394f-903">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-904">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-904">CC003</span></span></td>
<td><span data-ttu-id="6394f-905">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-905">Assembly</span></span></td>
<td><span data-ttu-id="6394f-906">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-906">10001</span></span></td>
<td><span data-ttu-id="6394f-907">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-907">Electricity</span></span></td>
<td><span data-ttu-id="6394f-908">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-908">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="6394f-909">-286.25</span></span></td>
<td><span data-ttu-id="6394f-910">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-911">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-912">Product 1</span></span></td>
<td><span data-ttu-id="6394f-913">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-913">10001</span></span></td>
<td><span data-ttu-id="6394f-914">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-914">Electricity</span></span></td>
<td><span data-ttu-id="6394f-915">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-915">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-916">241.05</span><span class="sxs-lookup"><span data-stu-id="6394f-916">241.05</span></span></td>
<td><span data-ttu-id="6394f-917">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-918">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-919">Product 2</span></span></td>
<td><span data-ttu-id="6394f-920">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-920">10001</span></span></td>
<td><span data-ttu-id="6394f-921">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-921">Electricity</span></span></td>
<td><span data-ttu-id="6394f-922">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-922">Fixed cost</span></span></td>
<td><span data-ttu-id="6394f-923">45.20</span><span class="sxs-lookup"><span data-stu-id="6394f-923">45.20</span></span></td>
<td><span data-ttu-id="6394f-924">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-925">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-925">CC003</span></span></td>
<td><span data-ttu-id="6394f-926">Samling</span><span class="sxs-lookup"><span data-stu-id="6394f-926">Assembly</span></span></td>
<td><span data-ttu-id="6394f-927">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-927">10001</span></span></td>
<td><span data-ttu-id="6394f-928">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-928">Electricity</span></span></td>
<td><span data-ttu-id="6394f-929">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-929">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-930">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="6394f-930">-2,977.17</span></span></td>
<td><span data-ttu-id="6394f-931">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-932">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-932">Prod 1</span></span></td>
<td><span data-ttu-id="6394f-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6394f-933">Product 1</span></span></td>
<td><span data-ttu-id="6394f-934">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-934">10001</span></span></td>
<td><span data-ttu-id="6394f-935">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-935">Electricity</span></span></td>
<td><span data-ttu-id="6394f-936">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-936">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6394f-937">2,507.09</span></span></td>
<td><span data-ttu-id="6394f-938">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6394f-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-939">Prod 2</span></span></td>
<td><span data-ttu-id="6394f-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6394f-940">Product 2</span></span></td>
<td><span data-ttu-id="6394f-941">10001</span><span class="sxs-lookup"><span data-stu-id="6394f-941">10001</span></span></td>
<td><span data-ttu-id="6394f-942">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6394f-942">Electricity</span></span></td>
<td><span data-ttu-id="6394f-943">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-943">Variable cost</span></span></td>
<td><span data-ttu-id="6394f-944">470.08</span><span class="sxs-lookup"><span data-stu-id="6394f-944">470.08</span></span></td>
<td><span data-ttu-id="6394f-945">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6394f-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6394f-946">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="6394f-946">Conclusion</span></span>
<span data-ttu-id="6394f-947">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="6394f-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6394f-948">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="6394f-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6394f-949">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="6394f-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6394f-950">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="6394f-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6394f-951">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6394f-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6394f-952">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6394f-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6394f-953">Sum</span><span class="sxs-lookup"><span data-stu-id="6394f-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6394f-954">CC099</span><span class="sxs-lookup"><span data-stu-id="6394f-954">CC099</span></span></th>
<th><span data-ttu-id="6394f-955">CC001</span><span class="sxs-lookup"><span data-stu-id="6394f-955">CC001</span></span></th>
<th><span data-ttu-id="6394f-956">CC002</span><span class="sxs-lookup"><span data-stu-id="6394f-956">CC002</span></span></th>
<th><span data-ttu-id="6394f-957">CC003</span><span class="sxs-lookup"><span data-stu-id="6394f-957">CC003</span></span></th>
<th><span data-ttu-id="6394f-958">CC004</span><span class="sxs-lookup"><span data-stu-id="6394f-958">CC004</span></span></th>
<th><span data-ttu-id="6394f-959">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6394f-959">Proj 1</span></span></th>
<th><span data-ttu-id="6394f-960">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6394f-960">Proj 2</span></span></th>
<th><span data-ttu-id="6394f-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6394f-961">Prod 1</span></span></th>
<th><span data-ttu-id="6394f-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6394f-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6394f-963">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="6394f-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6394f-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6394f-973">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6394f-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-974">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6394f-975">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-976">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-977">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-978">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-979">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-980">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6394f-981">776.36</span><span class="sxs-lookup"><span data-stu-id="6394f-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-982">223.64</span><span class="sxs-lookup"><span data-stu-id="6394f-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6394f-984">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6394f-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-985">000</span><span class="sxs-lookup"><span data-stu-id="6394f-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-986">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-987">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-988">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-989">0,00</span><span class="sxs-lookup"><span data-stu-id="6394f-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-990">30,00</span><span class="sxs-lookup"><span data-stu-id="6394f-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-991">10,00</span><span class="sxs-lookup"><span data-stu-id="6394f-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6394f-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6394f-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6394f-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6394f-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6394f-995">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="6394f-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6394f-996">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="6394f-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6394f-997">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="6394f-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6394f-998">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="6394f-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6394f-999">Hvis du vil ha mer informasjon, kan du se policyen for kostnadsakkumulering.</span><span class="sxs-lookup"><span data-stu-id="6394f-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="6394f-1000">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="6394f-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




