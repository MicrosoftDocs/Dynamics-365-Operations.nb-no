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
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009524"
---
# <a name="overhead-calculation"></a><span data-ttu-id="bd2a6-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bd2a6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd2a6-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="bd2a6-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-105">Term definition</span></span>
---------------

<span data-ttu-id="bd2a6-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="bd2a6-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="bd2a6-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="bd2a6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="bd2a6-109">Leie</span><span class="sxs-lookup"><span data-stu-id="bd2a6-109">Rent</span></span>
-   <span data-ttu-id="bd2a6-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-110">Electricity</span></span>
-   <span data-ttu-id="bd2a6-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="bd2a6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="bd2a6-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bd2a6-112">Overhead calculation overview</span></span>
<span data-ttu-id="bd2a6-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="bd2a6-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="bd2a6-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="bd2a6-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="bd2a6-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="bd2a6-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="bd2a6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="bd2a6-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="bd2a6-119">Version type</span></span>
-   <span data-ttu-id="bd2a6-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="bd2a6-120">Date and time</span></span>
-   <span data-ttu-id="bd2a6-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="bd2a6-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="bd2a6-122">Fiscal year</span></span>
-   <span data-ttu-id="bd2a6-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="bd2a6-123">Fiscal period</span></span>

<span data-ttu-id="bd2a6-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="bd2a6-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="bd2a6-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="bd2a6-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="bd2a6-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="bd2a6-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="bd2a6-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="bd2a6-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="bd2a6-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="bd2a6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="bd2a6-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="bd2a6-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="bd2a6-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="bd2a6-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="bd2a6-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="bd2a6-140">Main account</span></span></th>
<th><span data-ttu-id="bd2a6-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-143">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-144">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-145">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-145">10001</span></span></td>
<td><span data-ttu-id="bd2a6-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-146">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="bd2a6-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="bd2a6-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="bd2a6-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="bd2a6-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="bd2a6-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="bd2a6-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="bd2a6-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="bd2a6-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="bd2a6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="bd2a6-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="bd2a6-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="bd2a6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="bd2a6-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="bd2a6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="bd2a6-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-160">Journal</span></span></th>
<th><span data-ttu-id="bd2a6-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bd2a6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd2a6-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd2a6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd2a6-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-164">00001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-164">00001</span></span></td>
<td><span data-ttu-id="bd2a6-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="bd2a6-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bd2a6-166">Fiscal</span></span></td>
<td><span data-ttu-id="bd2a6-167">2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-167">2017</span></span></td>
<td><span data-ttu-id="bd2a6-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-168">Period 1</span></span></td>
<td><span data-ttu-id="bd2a6-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bd2a6-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-173">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-177">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-178">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-179">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-179">10001</span></span></td>
<td><span data-ttu-id="bd2a6-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-180">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bd2a6-181">Unclassified</span></span></td>
<td><span data-ttu-id="bd2a6-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd2a6-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bd2a6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-185">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-187">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-189">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-190">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-191">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-191">10001</span></span></td>
<td><span data-ttu-id="bd2a6-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-192">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bd2a6-193">Unclassified</span></span></td>
<td><span data-ttu-id="bd2a6-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-194">10,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-196">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-197">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-198">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-198">10001</span></span></td>
<td><span data-ttu-id="bd2a6-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-199">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bd2a6-200">Unclassified</span></span></td>
<td><span data-ttu-id="bd2a6-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-203">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-204">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-205">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-205">10001</span></span></td>
<td><span data-ttu-id="bd2a6-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-206">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-208">1,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-210">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-211">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-212">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-212">10001</span></span></td>
<td><span data-ttu-id="bd2a6-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="bd2a6-213">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-214">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-215">9,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="bd2a6-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="bd2a6-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="bd2a6-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="bd2a6-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="bd2a6-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="bd2a6-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="bd2a6-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="bd2a6-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="bd2a6-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="bd2a6-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-228">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-229">kWt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-230">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-231">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-231">HR</span></span></td>
<td><span data-ttu-id="bd2a6-232">1 000</span><span class="sxs-lookup"><span data-stu-id="bd2a6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-233">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-234">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-234">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-235">6,000</span><span class="sxs-lookup"><span data-stu-id="bd2a6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-236">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-237">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-237">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-238">0</span><span class="sxs-lookup"><span data-stu-id="bd2a6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-240">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-241">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-244">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-245">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-245">HR</span></span></td>
<td><span data-ttu-id="bd2a6-246">1 000</span><span class="sxs-lookup"><span data-stu-id="bd2a6-246">1,000</span></span></td>
<td><span data-ttu-id="bd2a6-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-249">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-250">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-250">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-251">6,000</span><span class="sxs-lookup"><span data-stu-id="bd2a6-251">6,000</span></span></td>
<td><span data-ttu-id="bd2a6-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="bd2a6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-254">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-255">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-255">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-256">0</span><span class="sxs-lookup"><span data-stu-id="bd2a6-256">0</span></span></td>
<td><span data-ttu-id="bd2a6-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="bd2a6-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-261">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-262">Formel</span><span class="sxs-lookup"><span data-stu-id="bd2a6-262">Formula</span></span></th>
<th><span data-ttu-id="bd2a6-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-263">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-266">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-267">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-267">HR</span></span></td>
<td><span data-ttu-id="bd2a6-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bd2a6-269">1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-269">1</span></span></td>
<td><span data-ttu-id="bd2a6-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-272">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-273">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-273">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bd2a6-275">1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-275">1</span></span></td>
<td><span data-ttu-id="bd2a6-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-278">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-279">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-279">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bd2a6-281">0</span><span class="sxs-lookup"><span data-stu-id="bd2a6-281">0</span></span></td>
<td><span data-ttu-id="bd2a6-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="bd2a6-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-285">Journal</span></span></th>
<th><span data-ttu-id="bd2a6-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bd2a6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd2a6-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd2a6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd2a6-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-289">00002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-289">00002</span></span></td>
<td><span data-ttu-id="bd2a6-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="bd2a6-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bd2a6-291">Fiscal</span></span></td>
<td><span data-ttu-id="bd2a6-292">2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-292">2017</span></span></td>
<td><span data-ttu-id="bd2a6-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-293">Period 1</span></span></td>
<td><span data-ttu-id="bd2a6-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bd2a6-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-298">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-302">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-303">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-304">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-304">10001</span></span></td>
<td><span data-ttu-id="bd2a6-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-305">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-309">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-310">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-311">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-311">10001</span></span></td>
<td><span data-ttu-id="bd2a6-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-312">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-313">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd2a6-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bd2a6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-317">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-319">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-321">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-322">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-323">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-323">10001</span></span></td>
<td><span data-ttu-id="bd2a6-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-324">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-328">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-329">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-329">HR</span></span></td>
<td><span data-ttu-id="bd2a6-330">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-330">10001</span></span></td>
<td><span data-ttu-id="bd2a6-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-331">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-333">500.00</span></span></td>
<td><span data-ttu-id="bd2a6-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-335">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-336">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-336">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-337">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-337">10001</span></span></td>
<td><span data-ttu-id="bd2a6-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-338">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-340">500.00</span></span></td>
<td><span data-ttu-id="bd2a6-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-342">CC099</span></span></td>
<td><span data-ttu-id="bd2a6-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-343">Default cost center</span></span></td>
<td><span data-ttu-id="bd2a6-344">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-344">10001</span></span></td>
<td><span data-ttu-id="bd2a6-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-345">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-346">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="bd2a6-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-349">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-350">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-350">HR</span></span></td>
<td><span data-ttu-id="bd2a6-351">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-351">10001</span></span></td>
<td><span data-ttu-id="bd2a6-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-352">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-353">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-354">1,285.71</span></span></td>
<td><span data-ttu-id="bd2a6-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-356">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-357">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-357">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-358">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-358">10001</span></span></td>
<td><span data-ttu-id="bd2a6-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="bd2a6-359">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-360">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="bd2a6-361">7,714.29</span></span></td>
<td><span data-ttu-id="bd2a6-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="bd2a6-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bd2a6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="bd2a6-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="bd2a6-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="bd2a6-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bd2a6-367">Define the overhead rate</span></span>

<span data-ttu-id="bd2a6-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="bd2a6-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-370">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="bd2a6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-372">Proj 1</span></span></td>
<td><span data-ttu-id="bd2a6-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-373">Project 1</span></span></td>
<td><span data-ttu-id="bd2a6-374">3</span><span class="sxs-lookup"><span data-stu-id="bd2a6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-375">Proj 2</span></span></td>
<td><span data-ttu-id="bd2a6-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-376">Project 2</span></span></td>
<td><span data-ttu-id="bd2a6-377">1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-379">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-380">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="bd2a6-382">Units</span></span></th>
<th><span data-ttu-id="bd2a6-383">Sats</span><span class="sxs-lookup"><span data-stu-id="bd2a6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-384">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-385">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-385">HR</span></span></td>
<td><span data-ttu-id="bd2a6-386">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-386">10001</span></span></td>
<td><span data-ttu-id="bd2a6-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-387">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-388">1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-388">1</span></span></td>
<td><span data-ttu-id="bd2a6-389">10</span><span class="sxs-lookup"><span data-stu-id="bd2a6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-391">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-392">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-393">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-396">Proj 1</span></span></td>
<td><span data-ttu-id="bd2a6-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-397">Project 1</span></span></td>
<td><span data-ttu-id="bd2a6-398">3</span><span class="sxs-lookup"><span data-stu-id="bd2a6-398">3</span></span></td>
<td><span data-ttu-id="bd2a6-399">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-399">10001</span></span></td>
<td><span data-ttu-id="bd2a6-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="bd2a6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-402">Proj 2</span></span></td>
<td><span data-ttu-id="bd2a6-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-403">Project 2</span></span></td>
<td><span data-ttu-id="bd2a6-404">1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-404">1</span></span></td>
<td><span data-ttu-id="bd2a6-405">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-405">10001</span></span></td>
<td><span data-ttu-id="bd2a6-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="bd2a6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="bd2a6-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-409">Journal</span></span></th>
<th><span data-ttu-id="bd2a6-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bd2a6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd2a6-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd2a6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd2a6-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-413">00003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-413">00003</span></span></td>
<td><span data-ttu-id="bd2a6-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="bd2a6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="bd2a6-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bd2a6-415">Fiscal</span></span></td>
<td><span data-ttu-id="bd2a6-416">2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-416">2017</span></span></td>
<td><span data-ttu-id="bd2a6-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-417">Period 1</span></span></td>
<td><span data-ttu-id="bd2a6-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="bd2a6-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-421">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-424">Proj 1</span></span></td>
<td><span data-ttu-id="bd2a6-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="bd2a6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-428">Proj 2</span></span></td>
<td><span data-ttu-id="bd2a6-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="bd2a6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd2a6-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bd2a6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-433">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-435">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-437">CC0001</span></span></td>
<td><span data-ttu-id="bd2a6-438">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-438">HR</span></span></td>
<td><span data-ttu-id="bd2a6-439">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-439">10001</span></span></td>
<td><span data-ttu-id="bd2a6-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-440">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-441">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-442">-30.00</span></span></td>
<td><span data-ttu-id="bd2a6-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-444">Proj 1</span></span></td>
<td><span data-ttu-id="bd2a6-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="bd2a6-446">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-446">10001</span></span></td>
<td><span data-ttu-id="bd2a6-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-447">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-448">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-449">30.00</span></span></td>
<td><span data-ttu-id="bd2a6-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-451">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-452">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-452">HR</span></span></td>
<td><span data-ttu-id="bd2a6-453">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-453">10001</span></span></td>
<td><span data-ttu-id="bd2a6-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-454">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-455">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-456">-10.00</span></span></td>
<td><span data-ttu-id="bd2a6-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-458">Proj 2</span></span></td>
<td><span data-ttu-id="bd2a6-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="bd2a6-460">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-460">10001</span></span></td>
<td><span data-ttu-id="bd2a6-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="bd2a6-461">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-462">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-463">10,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-463">10.00</span></span></td>
<td><span data-ttu-id="bd2a6-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="bd2a6-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="bd2a6-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="bd2a6-468">Finance støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="bd2a6-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="bd2a6-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="bd2a6-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="bd2a6-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="bd2a6-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="bd2a6-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="bd2a6-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-475">Define the cost allocation</span></span>

<span data-ttu-id="bd2a6-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="bd2a6-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="bd2a6-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-479">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="bd2a6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-481">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-482">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-482">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-483">35</span><span class="sxs-lookup"><span data-stu-id="bd2a6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-484">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-485">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-485">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-486">55</span><span class="sxs-lookup"><span data-stu-id="bd2a6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-487">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-488">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-489">10</span><span class="sxs-lookup"><span data-stu-id="bd2a6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="bd2a6-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-492">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="bd2a6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-494">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-495">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-495">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-496">65</span><span class="sxs-lookup"><span data-stu-id="bd2a6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-497">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-498">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-499">35</span><span class="sxs-lookup"><span data-stu-id="bd2a6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="bd2a6-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-502">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-504">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-505">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-506">60</span><span class="sxs-lookup"><span data-stu-id="bd2a6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-507">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-508">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-509">20</span><span class="sxs-lookup"><span data-stu-id="bd2a6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="bd2a6-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-512">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-514">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-515">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-516">80</span><span class="sxs-lookup"><span data-stu-id="bd2a6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-517">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-518">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-519">15</span><span class="sxs-lookup"><span data-stu-id="bd2a6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd2a6-520">Statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="bd2a6-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="bd2a6-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-523">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-524">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-526">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-528">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-529">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-529">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-530">35</span><span class="sxs-lookup"><span data-stu-id="bd2a6-530">35</span></span></td>
<td><span data-ttu-id="bd2a6-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bd2a6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-532">175.00</span></span></td>
<td><span data-ttu-id="bd2a6-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-534">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-535">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-535">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-536">55</span><span class="sxs-lookup"><span data-stu-id="bd2a6-536">55</span></span></td>
<td><span data-ttu-id="bd2a6-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bd2a6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-538">275.00</span></span></td>
<td><span data-ttu-id="bd2a6-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-540">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-541">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-542">10</span><span class="sxs-lookup"><span data-stu-id="bd2a6-542">10</span></span></td>
<td><span data-ttu-id="bd2a6-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bd2a6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-544">50.00</span></span></td>
<td><span data-ttu-id="bd2a6-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-546">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-547">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-547">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-548">35</span><span class="sxs-lookup"><span data-stu-id="bd2a6-548">35</span></span></td>
<td><span data-ttu-id="bd2a6-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bd2a6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-550">436.00</span></span></td>
<td><span data-ttu-id="bd2a6-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-552">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-553">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-553">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-554">55</span><span class="sxs-lookup"><span data-stu-id="bd2a6-554">55</span></span></td>
<td><span data-ttu-id="bd2a6-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bd2a6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="bd2a6-556">685.14</span></span></td>
<td><span data-ttu-id="bd2a6-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-558">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-559">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-560">10</span><span class="sxs-lookup"><span data-stu-id="bd2a6-560">10</span></span></td>
<td><span data-ttu-id="bd2a6-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bd2a6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="bd2a6-562">124.57</span></span></td>
<td><span data-ttu-id="bd2a6-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-565">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-566">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-568">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-570">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-571">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-571">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-572">65</span><span class="sxs-lookup"><span data-stu-id="bd2a6-572">65</span></span></td>
<td><span data-ttu-id="bd2a6-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="bd2a6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="bd2a6-574">438.75</span></span></td>
<td><span data-ttu-id="bd2a6-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-576">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-577">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-578">35</span><span class="sxs-lookup"><span data-stu-id="bd2a6-578">35</span></span></td>
<td><span data-ttu-id="bd2a6-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="bd2a6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="bd2a6-580">236.25</span></span></td>
<td><span data-ttu-id="bd2a6-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-582">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-583">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-583">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-584">65</span><span class="sxs-lookup"><span data-stu-id="bd2a6-584">65</span></span></td>
<td><span data-ttu-id="bd2a6-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="bd2a6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="bd2a6-586">5,297.69</span></span></td>
<td><span data-ttu-id="bd2a6-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-588">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-589">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-590">35</span><span class="sxs-lookup"><span data-stu-id="bd2a6-590">35</span></span></td>
<td><span data-ttu-id="bd2a6-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="bd2a6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="bd2a6-592">2,852.60</span></span></td>
<td><span data-ttu-id="bd2a6-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-595">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-596">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-598">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-600">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-601">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-602">60</span><span class="sxs-lookup"><span data-stu-id="bd2a6-602">60</span></span></td>
<td><span data-ttu-id="bd2a6-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="bd2a6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="bd2a6-604">535.31</span></span></td>
<td><span data-ttu-id="bd2a6-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-606">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-607">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-608">20</span><span class="sxs-lookup"><span data-stu-id="bd2a6-608">20</span></span></td>
<td><span data-ttu-id="bd2a6-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="bd2a6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="bd2a6-610">178.44</span></span></td>
<td><span data-ttu-id="bd2a6-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-612">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-613">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-614">60</span><span class="sxs-lookup"><span data-stu-id="bd2a6-614">60</span></span></td>
<td><span data-ttu-id="bd2a6-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="bd2a6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="bd2a6-616">4,487.12</span></span></td>
<td><span data-ttu-id="bd2a6-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-618">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-619">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-620">20</span><span class="sxs-lookup"><span data-stu-id="bd2a6-620">20</span></span></td>
<td><span data-ttu-id="bd2a6-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="bd2a6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-622">1,495.71</span></span></td>
<td><span data-ttu-id="bd2a6-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd2a6-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="bd2a6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-625">Cost object</span></span></th>
<th><span data-ttu-id="bd2a6-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="bd2a6-626">Magnitude</span></span></th>
<th><span data-ttu-id="bd2a6-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="bd2a6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="bd2a6-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-628">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-630">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-631">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-632">80</span><span class="sxs-lookup"><span data-stu-id="bd2a6-632">80</span></span></td>
<td><span data-ttu-id="bd2a6-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="bd2a6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="bd2a6-634">241.05</span></span></td>
<td><span data-ttu-id="bd2a6-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-636">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-637">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-638">15</span><span class="sxs-lookup"><span data-stu-id="bd2a6-638">15</span></span></td>
<td><span data-ttu-id="bd2a6-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="bd2a6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="bd2a6-640">45.20</span></span></td>
<td><span data-ttu-id="bd2a6-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-642">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-643">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-644">80</span><span class="sxs-lookup"><span data-stu-id="bd2a6-644">80</span></span></td>
<td><span data-ttu-id="bd2a6-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="bd2a6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="bd2a6-646">2,507.09</span></span></td>
<td><span data-ttu-id="bd2a6-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-648">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-649">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-650">15</span><span class="sxs-lookup"><span data-stu-id="bd2a6-650">15</span></span></td>
<td><span data-ttu-id="bd2a6-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="bd2a6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="bd2a6-652">470.08</span></span></td>
<td><span data-ttu-id="bd2a6-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bd2a6-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="bd2a6-655">Journal</span></span></th>
<th><span data-ttu-id="bd2a6-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="bd2a6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd2a6-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd2a6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd2a6-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-659">00004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-659">00004</span></span></td>
<td><span data-ttu-id="bd2a6-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="bd2a6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="bd2a6-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="bd2a6-661">Fiscal</span></span></td>
<td><span data-ttu-id="bd2a6-662">2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-662">2017</span></span></td>
<td><span data-ttu-id="bd2a6-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-663">Period 1</span></span></td>
<td><span data-ttu-id="bd2a6-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="bd2a6-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="bd2a6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd2a6-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-668">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-672">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-673">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-673">HR</span></span></td>
<td><span data-ttu-id="bd2a6-674">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-674">10001</span></span></td>
<td><span data-ttu-id="bd2a6-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-675">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-679">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-680">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-680">HR</span></span></td>
<td><span data-ttu-id="bd2a6-681">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-681">10001</span></span></td>
<td><span data-ttu-id="bd2a6-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-682">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-683">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-686">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-687">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-687">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-688">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-688">10001</span></span></td>
<td><span data-ttu-id="bd2a6-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-689">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-693">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-694">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-694">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-695">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-695">10001</span></span></td>
<td><span data-ttu-id="bd2a6-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-696">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-697">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="bd2a6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-700">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-701">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-701">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-702">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-702">10001</span></span></td>
<td><span data-ttu-id="bd2a6-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-703">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="bd2a6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-707">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-708">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-708">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-709">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-709">10001</span></span></td>
<td><span data-ttu-id="bd2a6-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-710">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-711">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="bd2a6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-714">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-715">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-716">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-716">10001</span></span></td>
<td><span data-ttu-id="bd2a6-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-717">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="bd2a6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-721">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-722">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-723">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-723">10001</span></span></td>
<td><span data-ttu-id="bd2a6-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-724">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-725">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="bd2a6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-728">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-729">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-730">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-730">10001</span></span></td>
<td><span data-ttu-id="bd2a6-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-731">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="bd2a6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-735">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-736">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-737">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-737">10001</span></span></td>
<td><span data-ttu-id="bd2a6-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-738">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-739">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="bd2a6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-742">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-743">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-744">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-744">10001</span></span></td>
<td><span data-ttu-id="bd2a6-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-745">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="bd2a6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd2a6-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-749">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-750">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-751">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-751">10001</span></span></td>
<td><span data-ttu-id="bd2a6-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-752">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-753">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="bd2a6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd2a6-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="bd2a6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd2a6-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd2a6-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-757">Cost element</span></span></th>
<th><span data-ttu-id="bd2a6-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="bd2a6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="bd2a6-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="bd2a6-759">Amount</span></span></th>
<th><span data-ttu-id="bd2a6-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="bd2a6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd2a6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-761">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-762">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-762">HR</span></span></td>
<td><span data-ttu-id="bd2a6-763">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-763">10001</span></span></td>
<td><span data-ttu-id="bd2a6-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-764">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-766">-500.00</span></span></td>
<td><span data-ttu-id="bd2a6-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-768">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-769">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-769">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-770">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-770">10001</span></span></td>
<td><span data-ttu-id="bd2a6-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-771">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-773">175.00</span></span></td>
<td><span data-ttu-id="bd2a6-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-775">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-776">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-776">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-777">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-777">10001</span></span></td>
<td><span data-ttu-id="bd2a6-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-778">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-780">275.00</span></span></td>
<td><span data-ttu-id="bd2a6-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-782">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-783">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-784">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-784">10001</span></span></td>
<td><span data-ttu-id="bd2a6-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-785">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-787">50,00</span></span></td>
<td><span data-ttu-id="bd2a6-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-789">CC001</span></span></td>
<td><span data-ttu-id="bd2a6-790">Personale</span><span class="sxs-lookup"><span data-stu-id="bd2a6-790">HR</span></span></td>
<td><span data-ttu-id="bd2a6-791">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-791">10001</span></span></td>
<td><span data-ttu-id="bd2a6-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-792">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-793">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="bd2a6-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-796">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-797">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-797">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-798">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-798">10001</span></span></td>
<td><span data-ttu-id="bd2a6-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-799">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-800">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-801">436.00</span></span></td>
<td><span data-ttu-id="bd2a6-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-803">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-804">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-804">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-805">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-805">10001</span></span></td>
<td><span data-ttu-id="bd2a6-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-806">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-807">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="bd2a6-808">685.14</span></span></td>
<td><span data-ttu-id="bd2a6-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-810">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-811">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-812">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-812">10001</span></span></td>
<td><span data-ttu-id="bd2a6-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-813">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-814">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="bd2a6-815">124.57</span></span></td>
<td><span data-ttu-id="bd2a6-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-817">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-818">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-818">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-819">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-819">10001</span></span></td>
<td><span data-ttu-id="bd2a6-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-820">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-822">-675.00</span></span></td>
<td><span data-ttu-id="bd2a6-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-824">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-825">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-825">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-826">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-826">10001</span></span></td>
<td><span data-ttu-id="bd2a6-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-827">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="bd2a6-829">438.75</span></span></td>
<td><span data-ttu-id="bd2a6-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-831">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-832">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-833">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-833">10001</span></span></td>
<td><span data-ttu-id="bd2a6-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-834">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="bd2a6-836">236.25</span></span></td>
<td><span data-ttu-id="bd2a6-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-838">CC002</span></span></td>
<td><span data-ttu-id="bd2a6-839">Finans</span><span class="sxs-lookup"><span data-stu-id="bd2a6-839">Finance</span></span></td>
<td><span data-ttu-id="bd2a6-840">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-840">10001</span></span></td>
<td><span data-ttu-id="bd2a6-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-841">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-842">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="bd2a6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="bd2a6-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-845">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-846">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-846">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-847">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-847">10001</span></span></td>
<td><span data-ttu-id="bd2a6-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-848">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-849">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="bd2a6-850">5,297.69</span></span></td>
<td><span data-ttu-id="bd2a6-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-852">CC004</span></span></td>
<td><span data-ttu-id="bd2a6-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="bd2a6-853">Packaging</span></span></td>
<td><span data-ttu-id="bd2a6-854">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-854">10001</span></span></td>
<td><span data-ttu-id="bd2a6-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-855">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-856">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="bd2a6-857">2,852.60</span></span></td>
<td><span data-ttu-id="bd2a6-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-859">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-860">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-860">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-861">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-861">10001</span></span></td>
<td><span data-ttu-id="bd2a6-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-862">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="bd2a6-864">-713.75</span></span></td>
<td><span data-ttu-id="bd2a6-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-866">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-867">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-868">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-868">10001</span></span></td>
<td><span data-ttu-id="bd2a6-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-869">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="bd2a6-871">535.31</span></span></td>
<td><span data-ttu-id="bd2a6-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-873">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-874">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-875">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-875">10001</span></span></td>
<td><span data-ttu-id="bd2a6-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-876">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="bd2a6-878">178.44</span></span></td>
<td><span data-ttu-id="bd2a6-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-880">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-881">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-881">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-882">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-882">10001</span></span></td>
<td><span data-ttu-id="bd2a6-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-883">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-884">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="bd2a6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="bd2a6-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-887">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-888">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-889">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-889">10001</span></span></td>
<td><span data-ttu-id="bd2a6-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-890">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-891">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="bd2a6-892">4,487.12</span></span></td>
<td><span data-ttu-id="bd2a6-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-894">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-895">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-896">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-896">10001</span></span></td>
<td><span data-ttu-id="bd2a6-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-897">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-898">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="bd2a6-899">1,495.71</span></span></td>
<td><span data-ttu-id="bd2a6-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-901">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-902">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-902">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-903">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-903">10001</span></span></td>
<td><span data-ttu-id="bd2a6-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-904">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="bd2a6-906">-286.25</span></span></td>
<td><span data-ttu-id="bd2a6-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-908">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-909">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-910">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-910">10001</span></span></td>
<td><span data-ttu-id="bd2a6-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-911">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="bd2a6-913">241.05</span></span></td>
<td><span data-ttu-id="bd2a6-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-915">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-916">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-917">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-917">10001</span></span></td>
<td><span data-ttu-id="bd2a6-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-918">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="bd2a6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="bd2a6-920">45.20</span></span></td>
<td><span data-ttu-id="bd2a6-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-922">CC003</span></span></td>
<td><span data-ttu-id="bd2a6-923">Samling</span><span class="sxs-lookup"><span data-stu-id="bd2a6-923">Assembly</span></span></td>
<td><span data-ttu-id="bd2a6-924">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-924">10001</span></span></td>
<td><span data-ttu-id="bd2a6-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-925">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-926">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="bd2a6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="bd2a6-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-929">Prod 1</span></span></td>
<td><span data-ttu-id="bd2a6-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-930">Product 1</span></span></td>
<td><span data-ttu-id="bd2a6-931">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-931">10001</span></span></td>
<td><span data-ttu-id="bd2a6-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-932">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-933">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="bd2a6-934">2,507.09</span></span></td>
<td><span data-ttu-id="bd2a6-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd2a6-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-936">Prod 2</span></span></td>
<td><span data-ttu-id="bd2a6-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-937">Product 2</span></span></td>
<td><span data-ttu-id="bd2a6-938">10001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-938">10001</span></span></td>
<td><span data-ttu-id="bd2a6-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="bd2a6-939">Electricity</span></span></td>
<td><span data-ttu-id="bd2a6-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-940">Variable cost</span></span></td>
<td><span data-ttu-id="bd2a6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="bd2a6-941">470.08</span></span></td>
<td><span data-ttu-id="bd2a6-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="bd2a6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="bd2a6-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="bd2a6-943">Conclusion</span></span>
<span data-ttu-id="bd2a6-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="bd2a6-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="bd2a6-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="bd2a6-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="bd2a6-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="bd2a6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="bd2a6-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="bd2a6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="bd2a6-950">Sum</span><span class="sxs-lookup"><span data-stu-id="bd2a6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bd2a6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="bd2a6-951">CC099</span></span></th>
<th><span data-ttu-id="bd2a6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="bd2a6-952">CC001</span></span></th>
<th><span data-ttu-id="bd2a6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="bd2a6-953">CC002</span></span></th>
<th><span data-ttu-id="bd2a6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="bd2a6-954">CC003</span></span></th>
<th><span data-ttu-id="bd2a6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="bd2a6-955">CC004</span></span></th>
<th><span data-ttu-id="bd2a6-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-956">Proj 1</span></span></th>
<th><span data-ttu-id="bd2a6-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-957">Proj 2</span></span></th>
<th><span data-ttu-id="bd2a6-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd2a6-958">Prod 1</span></span></th>
<th><span data-ttu-id="bd2a6-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd2a6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="bd2a6-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="bd2a6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="bd2a6-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="bd2a6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="bd2a6-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="bd2a6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="bd2a6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="bd2a6-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="bd2a6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-982">000</span><span class="sxs-lookup"><span data-stu-id="bd2a6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="bd2a6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="bd2a6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="bd2a6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd2a6-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="bd2a6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd2a6-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="bd2a6-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="bd2a6-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="bd2a6-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="bd2a6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="bd2a6-996">Hvis du vil ha mer informasjon, se [Policy for opprullet kost og beregning av administrasjonskostnader](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="bd2a6-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



