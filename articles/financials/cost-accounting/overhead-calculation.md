---
title: Beregning av indirekte kostnader
description: Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="bc92d-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bc92d-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc92d-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="bc92d-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="bc92d-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-105">Term definition</span></span>
---------------

<span data-ttu-id="bc92d-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="bc92d-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="bc92d-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="bc92d-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="bc92d-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="bc92d-109">Leie</span><span class="sxs-lookup"><span data-stu-id="bc92d-109">Rent</span></span>
-   <span data-ttu-id="bc92d-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-110">Electricity</span></span>
-   <span data-ttu-id="bc92d-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="bc92d-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="bc92d-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bc92d-112">Overhead calculation overview</span></span>
<span data-ttu-id="bc92d-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="bc92d-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="bc92d-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="bc92d-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="bc92d-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="bc92d-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="bc92d-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="bc92d-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="bc92d-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="bc92d-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="bc92d-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="bc92d-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="bc92d-119">Version type</span></span>
-   <span data-ttu-id="bc92d-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="bc92d-120">Date and time</span></span>
-   <span data-ttu-id="bc92d-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="bc92d-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="bc92d-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="bc92d-122">Fiscal year</span></span>
-   <span data-ttu-id="bc92d-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="bc92d-123">Fiscal period</span></span>

<span data-ttu-id="bc92d-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="bc92d-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="bc92d-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bc92d-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="bc92d-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="bc92d-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="bc92d-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="bc92d-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="bc92d-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="bc92d-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="bc92d-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="bc92d-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="bc92d-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="bc92d-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="bc92d-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="bc92d-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="bc92d-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="bc92d-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="bc92d-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="bc92d-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="bc92d-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="bc92d-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="bc92d-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="bc92d-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="bc92d-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bc92d-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="bc92d-140">Main account</span></span></th>
<th><span data-ttu-id="bc92d-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="bc92d-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="bc92d-143">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-143">CC099</span></span></td>
<td><span data-ttu-id="bc92d-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-144">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-145">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-145">10001</span></span></td>
<td><span data-ttu-id="bc92d-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-146">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="bc92d-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="bc92d-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="bc92d-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="bc92d-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="bc92d-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="bc92d-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-151">Define the cost behavior rule</span></span>

<span data-ttu-id="bc92d-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="bc92d-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="bc92d-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="bc92d-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="bc92d-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="bc92d-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="bc92d-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="bc92d-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="bc92d-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="bc92d-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="bc92d-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="bc92d-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="bc92d-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-160">Journal</span></span></th>
<th><span data-ttu-id="bc92d-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bc92d-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bc92d-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bc92d-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bc92d-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-164">00001</span><span class="sxs-lookup"><span data-stu-id="bc92d-164">00001</span></span></td>
<td><span data-ttu-id="bc92d-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="bc92d-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bc92d-166">Fiscal</span></span></td>
<td><span data-ttu-id="bc92d-167">2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-167">2017</span></span></td>
<td><span data-ttu-id="bc92d-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-168">Period 1</span></span></td>
<td><span data-ttu-id="bc92d-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bc92d-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="bc92d-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-173">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-174">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="bc92d-177">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-177">CC099</span></span></td>
<td><span data-ttu-id="bc92d-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-178">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-179">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-179">10001</span></span></td>
<td><span data-ttu-id="bc92d-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-180">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bc92d-181">Unclassified</span></span></td>
<td><span data-ttu-id="bc92d-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bc92d-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bc92d-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-185">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-186">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-187">Amount</span></span></th>
<th><span data-ttu-id="bc92d-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-189">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-189">CC099</span></span></td>
<td><span data-ttu-id="bc92d-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-190">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-191">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-191">10001</span></span></td>
<td><span data-ttu-id="bc92d-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-192">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bc92d-193">Unclassified</span></span></td>
<td><span data-ttu-id="bc92d-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-194">10,000.00</span></span></td>
<td><span data-ttu-id="bc92d-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-196">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-196">CC099</span></span></td>
<td><span data-ttu-id="bc92d-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-197">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-198">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-198">10001</span></span></td>
<td><span data-ttu-id="bc92d-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-199">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bc92d-200">Unclassified</span></span></td>
<td><span data-ttu-id="bc92d-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-201">-10,000.00</span></span></td>
<td><span data-ttu-id="bc92d-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-203">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-203">CC099</span></span></td>
<td><span data-ttu-id="bc92d-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-204">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-205">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-205">10001</span></span></td>
<td><span data-ttu-id="bc92d-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-206">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-207">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-208">1,000.00</span></span></td>
<td><span data-ttu-id="bc92d-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-210">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-210">CC099</span></span></td>
<td><span data-ttu-id="bc92d-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-211">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-212">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-212">10001</span></span></td>
<td><span data-ttu-id="bc92d-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="bc92d-213">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-214">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-215">9,000.00</span></span></td>
<td><span data-ttu-id="bc92d-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="bc92d-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="bc92d-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="bc92d-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bc92d-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="bc92d-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="bc92d-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="bc92d-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-221">Define the cost distribution rule</span></span>

<span data-ttu-id="bc92d-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="bc92d-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="bc92d-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="bc92d-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="bc92d-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="bc92d-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="bc92d-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="bc92d-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="bc92d-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="bc92d-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="bc92d-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bc92d-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-228">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-229">kWt</span><span class="sxs-lookup"><span data-stu-id="bc92d-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-230">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-230">CC001</span></span></td>
<td><span data-ttu-id="bc92d-231">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-231">HR</span></span></td>
<td><span data-ttu-id="bc92d-232">1 000</span><span class="sxs-lookup"><span data-stu-id="bc92d-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-233">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-233">CC002</span></span></td>
<td><span data-ttu-id="bc92d-234">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-234">Finance</span></span></td>
<td><span data-ttu-id="bc92d-235">6,000</span><span class="sxs-lookup"><span data-stu-id="bc92d-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-236">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-236">CC003</span></span></td>
<td><span data-ttu-id="bc92d-237">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-237">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-238">0</span><span class="sxs-lookup"><span data-stu-id="bc92d-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="bc92d-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-240">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-241">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-242">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-244">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-244">CC001</span></span></td>
<td><span data-ttu-id="bc92d-245">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-245">HR</span></span></td>
<td><span data-ttu-id="bc92d-246">1 000</span><span class="sxs-lookup"><span data-stu-id="bc92d-246">1,000</span></span></td>
<td><span data-ttu-id="bc92d-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bc92d-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="bc92d-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-249">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-249">CC002</span></span></td>
<td><span data-ttu-id="bc92d-250">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-250">Finance</span></span></td>
<td><span data-ttu-id="bc92d-251">6,000</span><span class="sxs-lookup"><span data-stu-id="bc92d-251">6,000</span></span></td>
<td><span data-ttu-id="bc92d-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bc92d-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="bc92d-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-254">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-254">CC003</span></span></td>
<td><span data-ttu-id="bc92d-255">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-255">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-256">0</span><span class="sxs-lookup"><span data-stu-id="bc92d-256">0</span></span></td>
<td><span data-ttu-id="bc92d-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bc92d-258">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="bc92d-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="bc92d-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="bc92d-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-261">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-262">Formel</span><span class="sxs-lookup"><span data-stu-id="bc92d-262">Formula</span></span></th>
<th><span data-ttu-id="bc92d-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-263">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-264">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-266">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-266">CC001</span></span></td>
<td><span data-ttu-id="bc92d-267">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-267">HR</span></span></td>
<td><span data-ttu-id="bc92d-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bc92d-269">1</span><span class="sxs-lookup"><span data-stu-id="bc92d-269">1</span></span></td>
<td><span data-ttu-id="bc92d-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bc92d-271">500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-272">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-272">CC002</span></span></td>
<td><span data-ttu-id="bc92d-273">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-273">Finance</span></span></td>
<td><span data-ttu-id="bc92d-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bc92d-275">1</span><span class="sxs-lookup"><span data-stu-id="bc92d-275">1</span></span></td>
<td><span data-ttu-id="bc92d-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bc92d-277">500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-278">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-278">CC003</span></span></td>
<td><span data-ttu-id="bc92d-279">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-279">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bc92d-281">0</span><span class="sxs-lookup"><span data-stu-id="bc92d-281">0</span></span></td>
<td><span data-ttu-id="bc92d-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bc92d-283">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="bc92d-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-285">Journal</span></span></th>
<th><span data-ttu-id="bc92d-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bc92d-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bc92d-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bc92d-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bc92d-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-289">00002</span><span class="sxs-lookup"><span data-stu-id="bc92d-289">00002</span></span></td>
<td><span data-ttu-id="bc92d-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="bc92d-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bc92d-291">Fiscal</span></span></td>
<td><span data-ttu-id="bc92d-292">2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-292">2017</span></span></td>
<td><span data-ttu-id="bc92d-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-293">Period 1</span></span></td>
<td><span data-ttu-id="bc92d-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bc92d-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="bc92d-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-298">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-299">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-302">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-302">CC099</span></span></td>
<td><span data-ttu-id="bc92d-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-303">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-304">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-304">10001</span></span></td>
<td><span data-ttu-id="bc92d-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-305">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-306">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-309">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-309">CC099</span></span></td>
<td><span data-ttu-id="bc92d-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-310">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-311">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-311">10001</span></span></td>
<td><span data-ttu-id="bc92d-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-312">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-313">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bc92d-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bc92d-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-317">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-318">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-319">Amount</span></span></th>
<th><span data-ttu-id="bc92d-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-321">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-321">CC099</span></span></td>
<td><span data-ttu-id="bc92d-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-322">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-323">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-323">10001</span></span></td>
<td><span data-ttu-id="bc92d-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-324">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-325">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-326">-1,000.00</span></span></td>
<td><span data-ttu-id="bc92d-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-328">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-328">CC001</span></span></td>
<td><span data-ttu-id="bc92d-329">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-329">HR</span></span></td>
<td><span data-ttu-id="bc92d-330">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-330">10001</span></span></td>
<td><span data-ttu-id="bc92d-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-331">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-332">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-333">500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-333">500.00</span></span></td>
<td><span data-ttu-id="bc92d-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-335">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-335">CC002</span></span></td>
<td><span data-ttu-id="bc92d-336">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-336">Finance</span></span></td>
<td><span data-ttu-id="bc92d-337">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-337">10001</span></span></td>
<td><span data-ttu-id="bc92d-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-338">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-339">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-340">500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-340">500.00</span></span></td>
<td><span data-ttu-id="bc92d-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-342">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-342">CC099</span></span></td>
<td><span data-ttu-id="bc92d-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bc92d-343">Default cost center</span></span></td>
<td><span data-ttu-id="bc92d-344">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-344">10001</span></span></td>
<td><span data-ttu-id="bc92d-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-345">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-346">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-347">-9,000.00</span></span></td>
<td><span data-ttu-id="bc92d-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-349">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-349">CC001</span></span></td>
<td><span data-ttu-id="bc92d-350">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-350">HR</span></span></td>
<td><span data-ttu-id="bc92d-351">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-351">10001</span></span></td>
<td><span data-ttu-id="bc92d-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-352">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-353">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="bc92d-354">1,285.71</span></span></td>
<td><span data-ttu-id="bc92d-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-356">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-356">CC002</span></span></td>
<td><span data-ttu-id="bc92d-357">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-357">Finance</span></span></td>
<td><span data-ttu-id="bc92d-358">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-358">10001</span></span></td>
<td><span data-ttu-id="bc92d-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="bc92d-359">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-360">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="bc92d-361">7,714.29</span></span></td>
<td><span data-ttu-id="bc92d-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="bc92d-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="bc92d-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bc92d-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="bc92d-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="bc92d-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="bc92d-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="bc92d-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bc92d-367">Define the overhead rate</span></span>

<span data-ttu-id="bc92d-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="bc92d-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-370">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="bc92d-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-372">Proj 1</span></span></td>
<td><span data-ttu-id="bc92d-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-373">Project 1</span></span></td>
<td><span data-ttu-id="bc92d-374">3</span><span class="sxs-lookup"><span data-stu-id="bc92d-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-375">Proj 2</span></span></td>
<td><span data-ttu-id="bc92d-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-376">Project 2</span></span></td>
<td><span data-ttu-id="bc92d-377">1</span><span class="sxs-lookup"><span data-stu-id="bc92d-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="bc92d-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-379">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-380">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-381">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="bc92d-382">Units</span></span></th>
<th><span data-ttu-id="bc92d-383">Sats</span><span class="sxs-lookup"><span data-stu-id="bc92d-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-384">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-384">CC001</span></span></td>
<td><span data-ttu-id="bc92d-385">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-385">HR</span></span></td>
<td><span data-ttu-id="bc92d-386">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-386">10001</span></span></td>
<td><span data-ttu-id="bc92d-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-387">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-388">1</span><span class="sxs-lookup"><span data-stu-id="bc92d-388">1</span></span></td>
<td><span data-ttu-id="bc92d-389">10</span><span class="sxs-lookup"><span data-stu-id="bc92d-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bc92d-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-391">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-392">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-393">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-394">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-396">Proj 1</span></span></td>
<td><span data-ttu-id="bc92d-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-397">Project 1</span></span></td>
<td><span data-ttu-id="bc92d-398">3</span><span class="sxs-lookup"><span data-stu-id="bc92d-398">3</span></span></td>
<td><span data-ttu-id="bc92d-399">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-399">10001</span></span></td>
<td><span data-ttu-id="bc92d-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="bc92d-401">30,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-402">Proj 2</span></span></td>
<td><span data-ttu-id="bc92d-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-403">Project 2</span></span></td>
<td><span data-ttu-id="bc92d-404">1</span><span class="sxs-lookup"><span data-stu-id="bc92d-404">1</span></span></td>
<td><span data-ttu-id="bc92d-405">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-405">10001</span></span></td>
<td><span data-ttu-id="bc92d-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="bc92d-407">10,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="bc92d-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-409">Journal</span></span></th>
<th><span data-ttu-id="bc92d-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bc92d-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bc92d-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bc92d-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bc92d-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-413">00003</span><span class="sxs-lookup"><span data-stu-id="bc92d-413">00003</span></span></td>
<td><span data-ttu-id="bc92d-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bc92d-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="bc92d-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bc92d-415">Fiscal</span></span></td>
<td><span data-ttu-id="bc92d-416">2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-416">2017</span></span></td>
<td><span data-ttu-id="bc92d-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-417">Period 1</span></span></td>
<td><span data-ttu-id="bc92d-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="bc92d-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="bc92d-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-421">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-424">Proj 1</span></span></td>
<td><span data-ttu-id="bc92d-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="bc92d-426">3,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-428">Proj 2</span></span></td>
<td><span data-ttu-id="bc92d-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="bc92d-430">1,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bc92d-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bc92d-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-433">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-434">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-435">Amount</span></span></th>
<th><span data-ttu-id="bc92d-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="bc92d-437">CC0001</span></span></td>
<td><span data-ttu-id="bc92d-438">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-438">HR</span></span></td>
<td><span data-ttu-id="bc92d-439">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-439">10001</span></span></td>
<td><span data-ttu-id="bc92d-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-440">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-441">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-442">-30.00</span></span></td>
<td><span data-ttu-id="bc92d-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-444">Proj 1</span></span></td>
<td><span data-ttu-id="bc92d-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="bc92d-446">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-446">10001</span></span></td>
<td><span data-ttu-id="bc92d-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-447">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-448">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-449">30,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-449">30.00</span></span></td>
<td><span data-ttu-id="bc92d-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-451">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-451">CC001</span></span></td>
<td><span data-ttu-id="bc92d-452">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-452">HR</span></span></td>
<td><span data-ttu-id="bc92d-453">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-453">10001</span></span></td>
<td><span data-ttu-id="bc92d-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-454">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-455">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-456">-10.00</span></span></td>
<td><span data-ttu-id="bc92d-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-458">Proj 2</span></span></td>
<td><span data-ttu-id="bc92d-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="bc92d-460">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-460">10001</span></span></td>
<td><span data-ttu-id="bc92d-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="bc92d-461">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-462">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-463">10,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-463">10.00</span></span></td>
<td><span data-ttu-id="bc92d-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="bc92d-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="bc92d-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="bc92d-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="bc92d-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bc92d-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="bc92d-468">Finance and Operations støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="bc92d-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="bc92d-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="bc92d-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="bc92d-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="bc92d-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="bc92d-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bc92d-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="bc92d-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="bc92d-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="bc92d-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="bc92d-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="bc92d-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="bc92d-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="bc92d-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="bc92d-475">Define the cost allocation</span></span>

<span data-ttu-id="bc92d-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="bc92d-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="bc92d-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="bc92d-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-479">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="bc92d-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-481">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-481">CC002</span></span></td>
<td><span data-ttu-id="bc92d-482">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-482">Finance</span></span></td>
<td><span data-ttu-id="bc92d-483">35</span><span class="sxs-lookup"><span data-stu-id="bc92d-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-484">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-484">CC003</span></span></td>
<td><span data-ttu-id="bc92d-485">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-485">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-486">55</span><span class="sxs-lookup"><span data-stu-id="bc92d-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-487">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-487">CC004</span></span></td>
<td><span data-ttu-id="bc92d-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-488">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-489">10</span><span class="sxs-lookup"><span data-stu-id="bc92d-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="bc92d-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-492">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="bc92d-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-494">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-494">CC003</span></span></td>
<td><span data-ttu-id="bc92d-495">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-495">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-496">65</span><span class="sxs-lookup"><span data-stu-id="bc92d-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-497">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-497">CC004</span></span></td>
<td><span data-ttu-id="bc92d-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-498">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-499">35</span><span class="sxs-lookup"><span data-stu-id="bc92d-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="bc92d-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-502">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="bc92d-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-504">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-505">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-506">60</span><span class="sxs-lookup"><span data-stu-id="bc92d-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-507">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-508">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-509">20</span><span class="sxs-lookup"><span data-stu-id="bc92d-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bc92d-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="bc92d-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-512">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="bc92d-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-514">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-514">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-515">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-516">80</span><span class="sxs-lookup"><span data-stu-id="bc92d-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-517">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-518">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-519">sept.</span><span class="sxs-lookup"><span data-stu-id="bc92d-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bc92d-520">I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="bc92d-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="bc92d-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="bc92d-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="bc92d-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bc92d-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-523">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-524">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-525">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-526">Amount</span></span></th>
<th><span data-ttu-id="bc92d-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-528">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-528">CC002</span></span></td>
<td><span data-ttu-id="bc92d-529">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-529">Finance</span></span></td>
<td><span data-ttu-id="bc92d-530">35</span><span class="sxs-lookup"><span data-stu-id="bc92d-530">35</span></span></td>
<td><span data-ttu-id="bc92d-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bc92d-532">175.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-532">175.00</span></span></td>
<td><span data-ttu-id="bc92d-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-534">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-534">CC003</span></span></td>
<td><span data-ttu-id="bc92d-535">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-535">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-536">55</span><span class="sxs-lookup"><span data-stu-id="bc92d-536">55</span></span></td>
<td><span data-ttu-id="bc92d-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bc92d-538">275.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-538">275.00</span></span></td>
<td><span data-ttu-id="bc92d-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-540">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-540">CC004</span></span></td>
<td><span data-ttu-id="bc92d-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-541">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-542">10</span><span class="sxs-lookup"><span data-stu-id="bc92d-542">10</span></span></td>
<td><span data-ttu-id="bc92d-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bc92d-544">50,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-544">50.00</span></span></td>
<td><span data-ttu-id="bc92d-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-546">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-546">CC002</span></span></td>
<td><span data-ttu-id="bc92d-547">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-547">Finance</span></span></td>
<td><span data-ttu-id="bc92d-548">35</span><span class="sxs-lookup"><span data-stu-id="bc92d-548">35</span></span></td>
<td><span data-ttu-id="bc92d-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="bc92d-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bc92d-550">436.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-550">436.00</span></span></td>
<td><span data-ttu-id="bc92d-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-552">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-552">CC003</span></span></td>
<td><span data-ttu-id="bc92d-553">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-553">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-554">55</span><span class="sxs-lookup"><span data-stu-id="bc92d-554">55</span></span></td>
<td><span data-ttu-id="bc92d-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="bc92d-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bc92d-556">685.14</span><span class="sxs-lookup"><span data-stu-id="bc92d-556">685.14</span></span></td>
<td><span data-ttu-id="bc92d-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-558">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-558">CC004</span></span></td>
<td><span data-ttu-id="bc92d-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-559">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-560">10</span><span class="sxs-lookup"><span data-stu-id="bc92d-560">10</span></span></td>
<td><span data-ttu-id="bc92d-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="bc92d-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bc92d-562">124.57</span><span class="sxs-lookup"><span data-stu-id="bc92d-562">124.57</span></span></td>
<td><span data-ttu-id="bc92d-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bc92d-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-565">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-566">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-567">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-568">Amount</span></span></th>
<th><span data-ttu-id="bc92d-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-570">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-570">CC003</span></span></td>
<td><span data-ttu-id="bc92d-571">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-571">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-572">65</span><span class="sxs-lookup"><span data-stu-id="bc92d-572">65</span></span></td>
<td><span data-ttu-id="bc92d-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="bc92d-574">438.75</span><span class="sxs-lookup"><span data-stu-id="bc92d-574">438.75</span></span></td>
<td><span data-ttu-id="bc92d-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-576">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-576">CC004</span></span></td>
<td><span data-ttu-id="bc92d-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-577">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-578">35</span><span class="sxs-lookup"><span data-stu-id="bc92d-578">35</span></span></td>
<td><span data-ttu-id="bc92d-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="bc92d-580">236.25</span><span class="sxs-lookup"><span data-stu-id="bc92d-580">236.25</span></span></td>
<td><span data-ttu-id="bc92d-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-582">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-582">CC003</span></span></td>
<td><span data-ttu-id="bc92d-583">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-583">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-584">65</span><span class="sxs-lookup"><span data-stu-id="bc92d-584">65</span></span></td>
<td><span data-ttu-id="bc92d-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="bc92d-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="bc92d-586">5,297.69</span></span></td>
<td><span data-ttu-id="bc92d-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-588">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-588">CC004</span></span></td>
<td><span data-ttu-id="bc92d-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-589">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-590">35</span><span class="sxs-lookup"><span data-stu-id="bc92d-590">35</span></span></td>
<td><span data-ttu-id="bc92d-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="bc92d-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="bc92d-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="bc92d-592">2,852.60</span></span></td>
<td><span data-ttu-id="bc92d-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bc92d-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-595">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-596">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-597">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-598">Amount</span></span></th>
<th><span data-ttu-id="bc92d-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-600">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-601">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-602">60</span><span class="sxs-lookup"><span data-stu-id="bc92d-602">60</span></span></td>
<td><span data-ttu-id="bc92d-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="bc92d-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="bc92d-604">535.31</span><span class="sxs-lookup"><span data-stu-id="bc92d-604">535.31</span></span></td>
<td><span data-ttu-id="bc92d-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-606">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-607">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-608">20</span><span class="sxs-lookup"><span data-stu-id="bc92d-608">20</span></span></td>
<td><span data-ttu-id="bc92d-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="bc92d-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="bc92d-610">178.44</span><span class="sxs-lookup"><span data-stu-id="bc92d-610">178.44</span></span></td>
<td><span data-ttu-id="bc92d-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-612">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-613">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-614">60</span><span class="sxs-lookup"><span data-stu-id="bc92d-614">60</span></span></td>
<td><span data-ttu-id="bc92d-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="bc92d-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="bc92d-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="bc92d-616">4,487.12</span></span></td>
<td><span data-ttu-id="bc92d-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-618">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-619">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-620">20</span><span class="sxs-lookup"><span data-stu-id="bc92d-620">20</span></span></td>
<td><span data-ttu-id="bc92d-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="bc92d-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="bc92d-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="bc92d-622">1,495.71</span></span></td>
<td><span data-ttu-id="bc92d-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc92d-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bc92d-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-625">Cost object</span></span></th>
<th><span data-ttu-id="bc92d-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bc92d-626">Magnitude</span></span></th>
<th><span data-ttu-id="bc92d-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bc92d-627">Allocation factor</span></span></th>
<th><span data-ttu-id="bc92d-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-628">Amount</span></span></th>
<th><span data-ttu-id="bc92d-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-630">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-631">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-632">80</span><span class="sxs-lookup"><span data-stu-id="bc92d-632">80</span></span></td>
<td><span data-ttu-id="bc92d-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="bc92d-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="bc92d-634">241.05</span><span class="sxs-lookup"><span data-stu-id="bc92d-634">241.05</span></span></td>
<td><span data-ttu-id="bc92d-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-636">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-637">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-638">15</span><span class="sxs-lookup"><span data-stu-id="bc92d-638">15</span></span></td>
<td><span data-ttu-id="bc92d-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="bc92d-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="bc92d-640">45.20</span><span class="sxs-lookup"><span data-stu-id="bc92d-640">45.20</span></span></td>
<td><span data-ttu-id="bc92d-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-642">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-643">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-644">80</span><span class="sxs-lookup"><span data-stu-id="bc92d-644">80</span></span></td>
<td><span data-ttu-id="bc92d-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="bc92d-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="bc92d-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="bc92d-646">2,507.09</span></span></td>
<td><span data-ttu-id="bc92d-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-648">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-649">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-650">15</span><span class="sxs-lookup"><span data-stu-id="bc92d-650">15</span></span></td>
<td><span data-ttu-id="bc92d-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="bc92d-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="bc92d-652">470.08</span><span class="sxs-lookup"><span data-stu-id="bc92d-652">470.08</span></span></td>
<td><span data-ttu-id="bc92d-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bc92d-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="bc92d-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="bc92d-655">Journal</span></span></th>
<th><span data-ttu-id="bc92d-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bc92d-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bc92d-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bc92d-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bc92d-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-659">00004</span><span class="sxs-lookup"><span data-stu-id="bc92d-659">00004</span></span></td>
<td><span data-ttu-id="bc92d-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="bc92d-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="bc92d-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bc92d-661">Fiscal</span></span></td>
<td><span data-ttu-id="bc92d-662">2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-662">2017</span></span></td>
<td><span data-ttu-id="bc92d-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-663">Period 1</span></span></td>
<td><span data-ttu-id="bc92d-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="bc92d-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="bc92d-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc92d-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-668">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-669">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-672">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-672">CC001</span></span></td>
<td><span data-ttu-id="bc92d-673">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-673">HR</span></span></td>
<td><span data-ttu-id="bc92d-674">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-674">10001</span></span></td>
<td><span data-ttu-id="bc92d-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-675">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-676">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-677">500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-679">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-679">CC001</span></span></td>
<td><span data-ttu-id="bc92d-680">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-680">HR</span></span></td>
<td><span data-ttu-id="bc92d-681">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-681">10001</span></span></td>
<td><span data-ttu-id="bc92d-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-682">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-683">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="bc92d-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-686">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-686">CC002</span></span></td>
<td><span data-ttu-id="bc92d-687">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-687">Finance</span></span></td>
<td><span data-ttu-id="bc92d-688">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-688">10001</span></span></td>
<td><span data-ttu-id="bc92d-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-689">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-690">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-691">675.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-693">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-693">CC002</span></span></td>
<td><span data-ttu-id="bc92d-694">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-694">Finance</span></span></td>
<td><span data-ttu-id="bc92d-695">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-695">10001</span></span></td>
<td><span data-ttu-id="bc92d-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-696">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-697">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="bc92d-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-700">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-700">CC003</span></span></td>
<td><span data-ttu-id="bc92d-701">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-701">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-702">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-702">10001</span></span></td>
<td><span data-ttu-id="bc92d-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-703">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-704">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-705">713.75</span><span class="sxs-lookup"><span data-stu-id="bc92d-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-707">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-707">CC003</span></span></td>
<td><span data-ttu-id="bc92d-708">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-708">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-709">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-709">10001</span></span></td>
<td><span data-ttu-id="bc92d-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-710">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-711">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="bc92d-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-714">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-714">CC003</span></span></td>
<td><span data-ttu-id="bc92d-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-715">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-716">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-716">10001</span></span></td>
<td><span data-ttu-id="bc92d-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-717">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-718">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-719">286.25</span><span class="sxs-lookup"><span data-stu-id="bc92d-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-721">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-721">CC003</span></span></td>
<td><span data-ttu-id="bc92d-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-722">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-723">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-723">10001</span></span></td>
<td><span data-ttu-id="bc92d-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-724">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-725">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="bc92d-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-728">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-729">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-730">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-730">10001</span></span></td>
<td><span data-ttu-id="bc92d-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-731">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-732">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-733">776.36</span><span class="sxs-lookup"><span data-stu-id="bc92d-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-735">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-736">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-737">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-737">10001</span></span></td>
<td><span data-ttu-id="bc92d-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-738">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-739">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="bc92d-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-742">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-743">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-744">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-744">10001</span></span></td>
<td><span data-ttu-id="bc92d-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-745">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-746">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-747">223.64</span><span class="sxs-lookup"><span data-stu-id="bc92d-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="bc92d-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-749">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-750">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-751">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-751">10001</span></span></td>
<td><span data-ttu-id="bc92d-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-752">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-753">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="bc92d-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bc92d-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bc92d-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bc92d-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bc92d-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-757">Cost element</span></span></th>
<th><span data-ttu-id="bc92d-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bc92d-758">Cost behavior</span></span></th>
<th><span data-ttu-id="bc92d-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc92d-759">Amount</span></span></th>
<th><span data-ttu-id="bc92d-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bc92d-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc92d-761">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-761">CC001</span></span></td>
<td><span data-ttu-id="bc92d-762">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-762">HR</span></span></td>
<td><span data-ttu-id="bc92d-763">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-763">10001</span></span></td>
<td><span data-ttu-id="bc92d-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-764">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-765">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-766">-500.00</span></span></td>
<td><span data-ttu-id="bc92d-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-768">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-768">CC002</span></span></td>
<td><span data-ttu-id="bc92d-769">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-769">Finance</span></span></td>
<td><span data-ttu-id="bc92d-770">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-770">10001</span></span></td>
<td><span data-ttu-id="bc92d-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-771">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-772">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-773">175.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-773">175.00</span></span></td>
<td><span data-ttu-id="bc92d-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-775">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-775">CC003</span></span></td>
<td><span data-ttu-id="bc92d-776">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-776">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-777">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-777">10001</span></span></td>
<td><span data-ttu-id="bc92d-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-778">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-779">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-780">275.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-780">275.00</span></span></td>
<td><span data-ttu-id="bc92d-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-782">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-782">CC004</span></span></td>
<td><span data-ttu-id="bc92d-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-783">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-784">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-784">10001</span></span></td>
<td><span data-ttu-id="bc92d-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-785">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-786">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-787">50,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-787">50,00</span></span></td>
<td><span data-ttu-id="bc92d-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-789">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-789">CC001</span></span></td>
<td><span data-ttu-id="bc92d-790">Personale</span><span class="sxs-lookup"><span data-stu-id="bc92d-790">HR</span></span></td>
<td><span data-ttu-id="bc92d-791">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-791">10001</span></span></td>
<td><span data-ttu-id="bc92d-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-792">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-793">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="bc92d-794">-1,245.71</span></span></td>
<td><span data-ttu-id="bc92d-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-796">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-796">CC002</span></span></td>
<td><span data-ttu-id="bc92d-797">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-797">Finance</span></span></td>
<td><span data-ttu-id="bc92d-798">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-798">10001</span></span></td>
<td><span data-ttu-id="bc92d-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-799">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-800">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-801">436.00</span><span class="sxs-lookup"><span data-stu-id="bc92d-801">436.00</span></span></td>
<td><span data-ttu-id="bc92d-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-803">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-803">CC003</span></span></td>
<td><span data-ttu-id="bc92d-804">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-804">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-805">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-805">10001</span></span></td>
<td><span data-ttu-id="bc92d-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-806">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-807">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-808">685.14</span><span class="sxs-lookup"><span data-stu-id="bc92d-808">685.14</span></span></td>
<td><span data-ttu-id="bc92d-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-810">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-810">CC004</span></span></td>
<td><span data-ttu-id="bc92d-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-811">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-812">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-812">10001</span></span></td>
<td><span data-ttu-id="bc92d-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-813">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-814">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-815">124.57</span><span class="sxs-lookup"><span data-stu-id="bc92d-815">124.57</span></span></td>
<td><span data-ttu-id="bc92d-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-817">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-817">CC002</span></span></td>
<td><span data-ttu-id="bc92d-818">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-818">Finance</span></span></td>
<td><span data-ttu-id="bc92d-819">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-819">10001</span></span></td>
<td><span data-ttu-id="bc92d-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-820">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-821">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-822">-675.00</span></span></td>
<td><span data-ttu-id="bc92d-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-824">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-824">CC003</span></span></td>
<td><span data-ttu-id="bc92d-825">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-825">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-826">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-826">10001</span></span></td>
<td><span data-ttu-id="bc92d-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-827">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-828">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-829">438.75</span><span class="sxs-lookup"><span data-stu-id="bc92d-829">438.75</span></span></td>
<td><span data-ttu-id="bc92d-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-831">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-831">CC004</span></span></td>
<td><span data-ttu-id="bc92d-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-832">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-833">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-833">10001</span></span></td>
<td><span data-ttu-id="bc92d-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-834">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-835">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-836">236.25</span><span class="sxs-lookup"><span data-stu-id="bc92d-836">236.25</span></span></td>
<td><span data-ttu-id="bc92d-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-838">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-838">CC002</span></span></td>
<td><span data-ttu-id="bc92d-839">Finans</span><span class="sxs-lookup"><span data-stu-id="bc92d-839">Finance</span></span></td>
<td><span data-ttu-id="bc92d-840">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-840">10001</span></span></td>
<td><span data-ttu-id="bc92d-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-841">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-842">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="bc92d-843">-8,150.29</span></span></td>
<td><span data-ttu-id="bc92d-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-845">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-845">CC003</span></span></td>
<td><span data-ttu-id="bc92d-846">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-846">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-847">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-847">10001</span></span></td>
<td><span data-ttu-id="bc92d-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-848">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-849">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="bc92d-850">5,297.69</span></span></td>
<td><span data-ttu-id="bc92d-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-852">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-852">CC004</span></span></td>
<td><span data-ttu-id="bc92d-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bc92d-853">Packaging</span></span></td>
<td><span data-ttu-id="bc92d-854">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-854">10001</span></span></td>
<td><span data-ttu-id="bc92d-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-855">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-856">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="bc92d-857">2,852.60</span></span></td>
<td><span data-ttu-id="bc92d-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-859">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-859">CC003</span></span></td>
<td><span data-ttu-id="bc92d-860">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-860">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-861">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-861">10001</span></span></td>
<td><span data-ttu-id="bc92d-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-862">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-863">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="bc92d-864">-713.75</span></span></td>
<td><span data-ttu-id="bc92d-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-866">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-867">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-868">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-868">10001</span></span></td>
<td><span data-ttu-id="bc92d-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-869">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-870">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-871">535.31</span><span class="sxs-lookup"><span data-stu-id="bc92d-871">535.31</span></span></td>
<td><span data-ttu-id="bc92d-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-873">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-874">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-875">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-875">10001</span></span></td>
<td><span data-ttu-id="bc92d-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-876">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-877">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-878">178.44</span><span class="sxs-lookup"><span data-stu-id="bc92d-878">178.44</span></span></td>
<td><span data-ttu-id="bc92d-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-880">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-880">CC003</span></span></td>
<td><span data-ttu-id="bc92d-881">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-881">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-882">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-882">10001</span></span></td>
<td><span data-ttu-id="bc92d-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-883">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-884">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="bc92d-885">-5,982.83</span></span></td>
<td><span data-ttu-id="bc92d-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-887">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-888">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-889">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-889">10001</span></span></td>
<td><span data-ttu-id="bc92d-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-890">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-891">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="bc92d-892">4,487.12</span></span></td>
<td><span data-ttu-id="bc92d-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-894">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-895">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-896">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-896">10001</span></span></td>
<td><span data-ttu-id="bc92d-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-897">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-898">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="bc92d-899">1,495.71</span></span></td>
<td><span data-ttu-id="bc92d-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-901">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-901">CC003</span></span></td>
<td><span data-ttu-id="bc92d-902">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-902">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-903">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-903">10001</span></span></td>
<td><span data-ttu-id="bc92d-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-904">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-905">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="bc92d-906">-286.25</span></span></td>
<td><span data-ttu-id="bc92d-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-908">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-909">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-910">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-910">10001</span></span></td>
<td><span data-ttu-id="bc92d-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-911">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-912">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-913">241.05</span><span class="sxs-lookup"><span data-stu-id="bc92d-913">241.05</span></span></td>
<td><span data-ttu-id="bc92d-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-915">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-916">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-917">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-917">10001</span></span></td>
<td><span data-ttu-id="bc92d-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-918">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-919">Fixed cost</span></span></td>
<td><span data-ttu-id="bc92d-920">45.20</span><span class="sxs-lookup"><span data-stu-id="bc92d-920">45.20</span></span></td>
<td><span data-ttu-id="bc92d-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-922">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-922">CC003</span></span></td>
<td><span data-ttu-id="bc92d-923">Samling</span><span class="sxs-lookup"><span data-stu-id="bc92d-923">Assembly</span></span></td>
<td><span data-ttu-id="bc92d-924">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-924">10001</span></span></td>
<td><span data-ttu-id="bc92d-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-925">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-926">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="bc92d-927">-2,977.17</span></span></td>
<td><span data-ttu-id="bc92d-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-929">Prod 1</span></span></td>
<td><span data-ttu-id="bc92d-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-930">Product 1</span></span></td>
<td><span data-ttu-id="bc92d-931">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-931">10001</span></span></td>
<td><span data-ttu-id="bc92d-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-932">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-933">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="bc92d-934">2,507.09</span></span></td>
<td><span data-ttu-id="bc92d-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc92d-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-936">Prod 2</span></span></td>
<td><span data-ttu-id="bc92d-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-937">Product 2</span></span></td>
<td><span data-ttu-id="bc92d-938">10001</span><span class="sxs-lookup"><span data-stu-id="bc92d-938">10001</span></span></td>
<td><span data-ttu-id="bc92d-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bc92d-939">Electricity</span></span></td>
<td><span data-ttu-id="bc92d-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-940">Variable cost</span></span></td>
<td><span data-ttu-id="bc92d-941">470.08</span><span class="sxs-lookup"><span data-stu-id="bc92d-941">470.08</span></span></td>
<td><span data-ttu-id="bc92d-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bc92d-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="bc92d-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="bc92d-943">Conclusion</span></span>
<span data-ttu-id="bc92d-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="bc92d-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="bc92d-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="bc92d-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="bc92d-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="bc92d-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="bc92d-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="bc92d-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bc92d-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="bc92d-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bc92d-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="bc92d-950">Sum</span><span class="sxs-lookup"><span data-stu-id="bc92d-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bc92d-951">CC099</span><span class="sxs-lookup"><span data-stu-id="bc92d-951">CC099</span></span></th>
<th><span data-ttu-id="bc92d-952">CC001</span><span class="sxs-lookup"><span data-stu-id="bc92d-952">CC001</span></span></th>
<th><span data-ttu-id="bc92d-953">CC002</span><span class="sxs-lookup"><span data-stu-id="bc92d-953">CC002</span></span></th>
<th><span data-ttu-id="bc92d-954">CC003</span><span class="sxs-lookup"><span data-stu-id="bc92d-954">CC003</span></span></th>
<th><span data-ttu-id="bc92d-955">CC004</span><span class="sxs-lookup"><span data-stu-id="bc92d-955">CC004</span></span></th>
<th><span data-ttu-id="bc92d-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-956">Proj 1</span></span></th>
<th><span data-ttu-id="bc92d-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-957">Proj 2</span></span></th>
<th><span data-ttu-id="bc92d-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bc92d-958">Prod 1</span></span></th>
<th><span data-ttu-id="bc92d-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bc92d-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="bc92d-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="bc92d-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="bc92d-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bc92d-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-971">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="bc92d-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-973">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-974">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-975">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-976">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-977">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-978">776.36</span><span class="sxs-lookup"><span data-stu-id="bc92d-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-979">223.64</span><span class="sxs-lookup"><span data-stu-id="bc92d-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="bc92d-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bc92d-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-982">000</span><span class="sxs-lookup"><span data-stu-id="bc92d-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-983">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-984">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-985">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-986">0,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-987">30,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-988">10,00</span><span class="sxs-lookup"><span data-stu-id="bc92d-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="bc92d-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="bc92d-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bc92d-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="bc92d-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bc92d-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="bc92d-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="bc92d-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="bc92d-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="bc92d-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="bc92d-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="bc92d-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="bc92d-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="bc92d-996">Hvis du vil ha mer informasjon, kan du se [Kostnadsopprulling](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="bc92d-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




