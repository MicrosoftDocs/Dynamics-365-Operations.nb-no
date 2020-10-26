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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976481"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6e320-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6e320-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e320-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="6e320-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6e320-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="6e320-105">Term definition</span></span>
---------------

<span data-ttu-id="6e320-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="6e320-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6e320-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="6e320-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6e320-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="6e320-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6e320-109">Leie</span><span class="sxs-lookup"><span data-stu-id="6e320-109">Rent</span></span>
-   <span data-ttu-id="6e320-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-110">Electricity</span></span>
-   <span data-ttu-id="6e320-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="6e320-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6e320-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6e320-112">Overhead calculation overview</span></span>
<span data-ttu-id="6e320-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="6e320-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6e320-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="6e320-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6e320-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="6e320-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6e320-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="6e320-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6e320-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="6e320-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6e320-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="6e320-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6e320-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="6e320-119">Version type</span></span>
-   <span data-ttu-id="6e320-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="6e320-120">Date and time</span></span>
-   <span data-ttu-id="6e320-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="6e320-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6e320-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="6e320-122">Fiscal year</span></span>
-   <span data-ttu-id="6e320-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="6e320-123">Fiscal period</span></span>

<span data-ttu-id="6e320-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="6e320-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6e320-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="6e320-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6e320-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6e320-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6e320-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="6e320-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6e320-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="6e320-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6e320-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="6e320-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6e320-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="6e320-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6e320-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6e320-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6e320-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="6e320-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6e320-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="6e320-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6e320-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="6e320-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6e320-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="6e320-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6e320-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="6e320-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6e320-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6e320-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="6e320-140">Main account</span></span></th>
<th><span data-ttu-id="6e320-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="6e320-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6e320-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-143">CC099</span></span></td>
<td><span data-ttu-id="6e320-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-144">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-145">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-145">10001</span></span></td>
<td><span data-ttu-id="6e320-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-146">Electricity</span></span></td>
<td><span data-ttu-id="6e320-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6e320-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6e320-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="6e320-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6e320-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader** .</span><span class="sxs-lookup"><span data-stu-id="6e320-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost** .</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6e320-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6e320-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="6e320-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6e320-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="6e320-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6e320-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="6e320-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6e320-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="6e320-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6e320-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6e320-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="6e320-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6e320-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="6e320-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6e320-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-160">Journal</span></span></th>
<th><span data-ttu-id="6e320-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6e320-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6e320-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6e320-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6e320-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="6e320-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-164">00001</span><span class="sxs-lookup"><span data-stu-id="6e320-164">00001</span></span></td>
<td><span data-ttu-id="6e320-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6e320-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6e320-166">Fiscal</span></span></td>
<td><span data-ttu-id="6e320-167">2017</span><span class="sxs-lookup"><span data-stu-id="6e320-167">2017</span></span></td>
<td><span data-ttu-id="6e320-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-168">Period 1</span></span></td>
<td><span data-ttu-id="6e320-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6e320-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="6e320-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-173">Cost element</span></span></th>
<th><span data-ttu-id="6e320-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6e320-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-177">CC099</span></span></td>
<td><span data-ttu-id="6e320-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-178">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-179">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-179">10001</span></span></td>
<td><span data-ttu-id="6e320-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-180">Electricity</span></span></td>
<td><span data-ttu-id="6e320-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6e320-181">Unclassified</span></span></td>
<td><span data-ttu-id="6e320-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6e320-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6e320-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-185">Cost element</span></span></th>
<th><span data-ttu-id="6e320-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-187">Amount</span></span></th>
<th><span data-ttu-id="6e320-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-189">CC099</span></span></td>
<td><span data-ttu-id="6e320-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-190">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-191">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-191">10001</span></span></td>
<td><span data-ttu-id="6e320-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-192">Electricity</span></span></td>
<td><span data-ttu-id="6e320-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6e320-193">Unclassified</span></span></td>
<td><span data-ttu-id="6e320-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-194">10,000.00</span></span></td>
<td><span data-ttu-id="6e320-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-196">CC099</span></span></td>
<td><span data-ttu-id="6e320-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-197">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-198">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-198">10001</span></span></td>
<td><span data-ttu-id="6e320-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-199">Electricity</span></span></td>
<td><span data-ttu-id="6e320-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6e320-200">Unclassified</span></span></td>
<td><span data-ttu-id="6e320-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6e320-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-203">CC099</span></span></td>
<td><span data-ttu-id="6e320-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-204">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-205">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-205">10001</span></span></td>
<td><span data-ttu-id="6e320-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-206">Electricity</span></span></td>
<td><span data-ttu-id="6e320-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-208">1,000.00</span></span></td>
<td><span data-ttu-id="6e320-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-210">CC099</span></span></td>
<td><span data-ttu-id="6e320-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-211">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-212">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-212">10001</span></span></td>
<td><span data-ttu-id="6e320-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="6e320-213">Electricity</span></span></td>
<td><span data-ttu-id="6e320-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-214">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6e320-215">9,000.00</span></span></td>
<td><span data-ttu-id="6e320-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6e320-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6e320-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="6e320-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6e320-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6e320-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6e320-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="6e320-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6e320-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="6e320-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6e320-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="6e320-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6e320-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="6e320-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6e320-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="6e320-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6e320-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="6e320-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6e320-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="6e320-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6e320-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6e320-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-228">Cost object</span></span></th>
<th><span data-ttu-id="6e320-229">kWt</span><span class="sxs-lookup"><span data-stu-id="6e320-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-230">CC001</span></span></td>
<td><span data-ttu-id="6e320-231">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-231">HR</span></span></td>
<td><span data-ttu-id="6e320-232">1 000</span><span class="sxs-lookup"><span data-stu-id="6e320-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-233">CC002</span></span></td>
<td><span data-ttu-id="6e320-234">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-234">Finance</span></span></td>
<td><span data-ttu-id="6e320-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6e320-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-236">CC003</span></span></td>
<td><span data-ttu-id="6e320-237">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-237">Assembly</span></span></td>
<td><span data-ttu-id="6e320-238">0</span><span class="sxs-lookup"><span data-stu-id="6e320-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="6e320-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-240">Cost object</span></span></th>
<th><span data-ttu-id="6e320-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-241">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-244">CC001</span></span></td>
<td><span data-ttu-id="6e320-245">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-245">HR</span></span></td>
<td><span data-ttu-id="6e320-246">1 000</span><span class="sxs-lookup"><span data-stu-id="6e320-246">1,000</span></span></td>
<td><span data-ttu-id="6e320-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6e320-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6e320-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-249">CC002</span></span></td>
<td><span data-ttu-id="6e320-250">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-250">Finance</span></span></td>
<td><span data-ttu-id="6e320-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6e320-251">6,000</span></span></td>
<td><span data-ttu-id="6e320-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6e320-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6e320-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-254">CC003</span></span></td>
<td><span data-ttu-id="6e320-255">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-255">Assembly</span></span></td>
<td><span data-ttu-id="6e320-256">0</span><span class="sxs-lookup"><span data-stu-id="6e320-256">0</span></span></td>
<td><span data-ttu-id="6e320-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6e320-258">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="6e320-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6e320-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="6e320-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-261">Cost object</span></span></th>
<th><span data-ttu-id="6e320-262">Formel</span><span class="sxs-lookup"><span data-stu-id="6e320-262">Formula</span></span></th>
<th><span data-ttu-id="6e320-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-263">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-266">CC001</span></span></td>
<td><span data-ttu-id="6e320-267">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-267">HR</span></span></td>
<td><span data-ttu-id="6e320-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6e320-269">1</span><span class="sxs-lookup"><span data-stu-id="6e320-269">1</span></span></td>
<td><span data-ttu-id="6e320-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6e320-271">500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-272">CC002</span></span></td>
<td><span data-ttu-id="6e320-273">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-273">Finance</span></span></td>
<td><span data-ttu-id="6e320-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6e320-275">1</span><span class="sxs-lookup"><span data-stu-id="6e320-275">1</span></span></td>
<td><span data-ttu-id="6e320-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6e320-277">500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-278">CC003</span></span></td>
<td><span data-ttu-id="6e320-279">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-279">Assembly</span></span></td>
<td><span data-ttu-id="6e320-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6e320-281">0</span><span class="sxs-lookup"><span data-stu-id="6e320-281">0</span></span></td>
<td><span data-ttu-id="6e320-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6e320-283">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6e320-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-285">Journal</span></span></th>
<th><span data-ttu-id="6e320-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6e320-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6e320-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6e320-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6e320-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="6e320-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-289">00002</span><span class="sxs-lookup"><span data-stu-id="6e320-289">00002</span></span></td>
<td><span data-ttu-id="6e320-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="6e320-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6e320-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6e320-291">Fiscal</span></span></td>
<td><span data-ttu-id="6e320-292">2017</span><span class="sxs-lookup"><span data-stu-id="6e320-292">2017</span></span></td>
<td><span data-ttu-id="6e320-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-293">Period 1</span></span></td>
<td><span data-ttu-id="6e320-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6e320-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="6e320-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-298">Cost element</span></span></th>
<th><span data-ttu-id="6e320-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-302">CC099</span></span></td>
<td><span data-ttu-id="6e320-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-303">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-304">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-304">10001</span></span></td>
<td><span data-ttu-id="6e320-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-305">Electricity</span></span></td>
<td><span data-ttu-id="6e320-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-309">CC099</span></span></td>
<td><span data-ttu-id="6e320-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-310">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-311">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-311">10001</span></span></td>
<td><span data-ttu-id="6e320-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-312">Electricity</span></span></td>
<td><span data-ttu-id="6e320-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-313">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6e320-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6e320-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6e320-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-317">Cost element</span></span></th>
<th><span data-ttu-id="6e320-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-319">Amount</span></span></th>
<th><span data-ttu-id="6e320-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-321">CC099</span></span></td>
<td><span data-ttu-id="6e320-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-322">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-323">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-323">10001</span></span></td>
<td><span data-ttu-id="6e320-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-324">Electricity</span></span></td>
<td><span data-ttu-id="6e320-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6e320-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-328">CC001</span></span></td>
<td><span data-ttu-id="6e320-329">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-329">HR</span></span></td>
<td><span data-ttu-id="6e320-330">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-330">10001</span></span></td>
<td><span data-ttu-id="6e320-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-331">Electricity</span></span></td>
<td><span data-ttu-id="6e320-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-333">500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-333">500.00</span></span></td>
<td><span data-ttu-id="6e320-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-335">CC002</span></span></td>
<td><span data-ttu-id="6e320-336">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-336">Finance</span></span></td>
<td><span data-ttu-id="6e320-337">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-337">10001</span></span></td>
<td><span data-ttu-id="6e320-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-338">Electricity</span></span></td>
<td><span data-ttu-id="6e320-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-340">500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-340">500.00</span></span></td>
<td><span data-ttu-id="6e320-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-342">CC099</span></span></td>
<td><span data-ttu-id="6e320-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="6e320-343">Default cost center</span></span></td>
<td><span data-ttu-id="6e320-344">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-344">10001</span></span></td>
<td><span data-ttu-id="6e320-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-345">Electricity</span></span></td>
<td><span data-ttu-id="6e320-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-346">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="6e320-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6e320-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-349">CC001</span></span></td>
<td><span data-ttu-id="6e320-350">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-350">HR</span></span></td>
<td><span data-ttu-id="6e320-351">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-351">10001</span></span></td>
<td><span data-ttu-id="6e320-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-352">Electricity</span></span></td>
<td><span data-ttu-id="6e320-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-353">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6e320-354">1,285.71</span></span></td>
<td><span data-ttu-id="6e320-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-356">CC002</span></span></td>
<td><span data-ttu-id="6e320-357">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-357">Finance</span></span></td>
<td><span data-ttu-id="6e320-358">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-358">10001</span></span></td>
<td><span data-ttu-id="6e320-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="6e320-359">Electricity</span></span></td>
<td><span data-ttu-id="6e320-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-360">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6e320-361">7,714.29</span></span></td>
<td><span data-ttu-id="6e320-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6e320-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6e320-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6e320-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6e320-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6e320-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6e320-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="6e320-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6e320-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6e320-367">Define the overhead rate</span></span>

<span data-ttu-id="6e320-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="6e320-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6e320-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6e320-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-370">Cost object</span></span></th>
<th><span data-ttu-id="6e320-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="6e320-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-372">Proj 1</span></span></td>
<td><span data-ttu-id="6e320-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-373">Project 1</span></span></td>
<td><span data-ttu-id="6e320-374">3</span><span class="sxs-lookup"><span data-stu-id="6e320-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-375">Proj 2</span></span></td>
<td><span data-ttu-id="6e320-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-376">Project 2</span></span></td>
<td><span data-ttu-id="6e320-377">1</span><span class="sxs-lookup"><span data-stu-id="6e320-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="6e320-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-379">Cost object</span></span></th>
<th><span data-ttu-id="6e320-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-380">Cost element</span></span></th>
<th><span data-ttu-id="6e320-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="6e320-382">Units</span></span></th>
<th><span data-ttu-id="6e320-383">Sats</span><span class="sxs-lookup"><span data-stu-id="6e320-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-384">CC001</span></span></td>
<td><span data-ttu-id="6e320-385">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-385">HR</span></span></td>
<td><span data-ttu-id="6e320-386">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-386">10001</span></span></td>
<td><span data-ttu-id="6e320-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-387">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-388">1</span><span class="sxs-lookup"><span data-stu-id="6e320-388">1</span></span></td>
<td><span data-ttu-id="6e320-389">10</span><span class="sxs-lookup"><span data-stu-id="6e320-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6e320-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-391">Cost object</span></span></th>
<th><span data-ttu-id="6e320-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-392">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-393">Cost element</span></span></th>
<th><span data-ttu-id="6e320-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-396">Proj 1</span></span></td>
<td><span data-ttu-id="6e320-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-397">Project 1</span></span></td>
<td><span data-ttu-id="6e320-398">3</span><span class="sxs-lookup"><span data-stu-id="6e320-398">3</span></span></td>
<td><span data-ttu-id="6e320-399">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-399">10001</span></span></td>
<td><span data-ttu-id="6e320-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6e320-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6e320-401">30,00</span><span class="sxs-lookup"><span data-stu-id="6e320-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-402">Proj 2</span></span></td>
<td><span data-ttu-id="6e320-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-403">Project 2</span></span></td>
<td><span data-ttu-id="6e320-404">1</span><span class="sxs-lookup"><span data-stu-id="6e320-404">1</span></span></td>
<td><span data-ttu-id="6e320-405">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-405">10001</span></span></td>
<td><span data-ttu-id="6e320-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6e320-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6e320-407">10,00</span><span class="sxs-lookup"><span data-stu-id="6e320-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6e320-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-409">Journal</span></span></th>
<th><span data-ttu-id="6e320-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6e320-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6e320-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6e320-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6e320-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="6e320-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-413">00003</span><span class="sxs-lookup"><span data-stu-id="6e320-413">00003</span></span></td>
<td><span data-ttu-id="6e320-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="6e320-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6e320-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6e320-415">Fiscal</span></span></td>
<td><span data-ttu-id="6e320-416">2017</span><span class="sxs-lookup"><span data-stu-id="6e320-416">2017</span></span></td>
<td><span data-ttu-id="6e320-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-417">Period 1</span></span></td>
<td><span data-ttu-id="6e320-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6e320-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="6e320-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-421">Cost object</span></span></th>
<th><span data-ttu-id="6e320-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-424">Proj 1</span></span></td>
<td><span data-ttu-id="6e320-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6e320-426">3,00</span><span class="sxs-lookup"><span data-stu-id="6e320-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-428">Proj 2</span></span></td>
<td><span data-ttu-id="6e320-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6e320-430">1,00</span><span class="sxs-lookup"><span data-stu-id="6e320-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6e320-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6e320-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-433">Cost element</span></span></th>
<th><span data-ttu-id="6e320-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-435">Amount</span></span></th>
<th><span data-ttu-id="6e320-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6e320-437">CC0001</span></span></td>
<td><span data-ttu-id="6e320-438">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-438">HR</span></span></td>
<td><span data-ttu-id="6e320-439">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-439">10001</span></span></td>
<td><span data-ttu-id="6e320-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-440">Electricity</span></span></td>
<td><span data-ttu-id="6e320-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-441">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="6e320-442">-30.00</span></span></td>
<td><span data-ttu-id="6e320-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-444">Proj 1</span></span></td>
<td><span data-ttu-id="6e320-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6e320-446">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-446">10001</span></span></td>
<td><span data-ttu-id="6e320-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-447">Electricity</span></span></td>
<td><span data-ttu-id="6e320-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-448">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-449">30,00</span><span class="sxs-lookup"><span data-stu-id="6e320-449">30.00</span></span></td>
<td><span data-ttu-id="6e320-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-451">CC001</span></span></td>
<td><span data-ttu-id="6e320-452">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-452">HR</span></span></td>
<td><span data-ttu-id="6e320-453">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-453">10001</span></span></td>
<td><span data-ttu-id="6e320-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-454">Electricity</span></span></td>
<td><span data-ttu-id="6e320-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-455">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="6e320-456">-10.00</span></span></td>
<td><span data-ttu-id="6e320-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-458">Proj 2</span></span></td>
<td><span data-ttu-id="6e320-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6e320-460">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-460">10001</span></span></td>
<td><span data-ttu-id="6e320-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="6e320-461">Electricity</span></span></td>
<td><span data-ttu-id="6e320-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-462">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-463">10,00</span><span class="sxs-lookup"><span data-stu-id="6e320-463">10.00</span></span></td>
<td><span data-ttu-id="6e320-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="6e320-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6e320-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="6e320-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6e320-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6e320-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6e320-468">Finance støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="6e320-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="6e320-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="6e320-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6e320-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="6e320-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6e320-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="6e320-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6e320-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="6e320-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6e320-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="6e320-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6e320-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6e320-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6e320-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="6e320-475">Define the cost allocation</span></span>

<span data-ttu-id="6e320-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="6e320-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6e320-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6e320-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6e320-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6e320-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-479">Cost object</span></span></th>
<th><span data-ttu-id="6e320-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="6e320-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-481">CC002</span></span></td>
<td><span data-ttu-id="6e320-482">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-482">Finance</span></span></td>
<td><span data-ttu-id="6e320-483">35</span><span class="sxs-lookup"><span data-stu-id="6e320-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-484">CC003</span></span></td>
<td><span data-ttu-id="6e320-485">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-485">Assembly</span></span></td>
<td><span data-ttu-id="6e320-486">55</span><span class="sxs-lookup"><span data-stu-id="6e320-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-487">CC004</span></span></td>
<td><span data-ttu-id="6e320-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-488">Packaging</span></span></td>
<td><span data-ttu-id="6e320-489">10</span><span class="sxs-lookup"><span data-stu-id="6e320-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6e320-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6e320-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6e320-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-492">Cost object</span></span></th>
<th><span data-ttu-id="6e320-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="6e320-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-494">CC003</span></span></td>
<td><span data-ttu-id="6e320-495">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-495">Assembly</span></span></td>
<td><span data-ttu-id="6e320-496">65</span><span class="sxs-lookup"><span data-stu-id="6e320-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-497">CC004</span></span></td>
<td><span data-ttu-id="6e320-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-498">Packaging</span></span></td>
<td><span data-ttu-id="6e320-499">35</span><span class="sxs-lookup"><span data-stu-id="6e320-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6e320-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6e320-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6e320-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-502">Cost object</span></span></th>
<th><span data-ttu-id="6e320-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="6e320-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-504">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-505">Product 1</span></span></td>
<td><span data-ttu-id="6e320-506">60</span><span class="sxs-lookup"><span data-stu-id="6e320-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-507">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-508">Product 2</span></span></td>
<td><span data-ttu-id="6e320-509">20</span><span class="sxs-lookup"><span data-stu-id="6e320-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6e320-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6e320-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="6e320-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-512">Cost object</span></span></th>
<th><span data-ttu-id="6e320-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="6e320-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-514">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-515">Product 1</span></span></td>
<td><span data-ttu-id="6e320-516">80</span><span class="sxs-lookup"><span data-stu-id="6e320-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-517">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-518">Product 2</span></span></td>
<td><span data-ttu-id="6e320-519">15</span><span class="sxs-lookup"><span data-stu-id="6e320-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6e320-520">Statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="6e320-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6e320-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="6e320-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6e320-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6e320-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-523">Cost object</span></span></th>
<th><span data-ttu-id="6e320-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-524">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-526">Amount</span></span></th>
<th><span data-ttu-id="6e320-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-528">CC002</span></span></td>
<td><span data-ttu-id="6e320-529">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-529">Finance</span></span></td>
<td><span data-ttu-id="6e320-530">35</span><span class="sxs-lookup"><span data-stu-id="6e320-530">35</span></span></td>
<td><span data-ttu-id="6e320-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6e320-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6e320-532">175.00</span></span></td>
<td><span data-ttu-id="6e320-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-534">CC003</span></span></td>
<td><span data-ttu-id="6e320-535">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-535">Assembly</span></span></td>
<td><span data-ttu-id="6e320-536">55</span><span class="sxs-lookup"><span data-stu-id="6e320-536">55</span></span></td>
<td><span data-ttu-id="6e320-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6e320-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6e320-538">275.00</span></span></td>
<td><span data-ttu-id="6e320-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-540">CC004</span></span></td>
<td><span data-ttu-id="6e320-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-541">Packaging</span></span></td>
<td><span data-ttu-id="6e320-542">10</span><span class="sxs-lookup"><span data-stu-id="6e320-542">10</span></span></td>
<td><span data-ttu-id="6e320-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6e320-544">50,00</span><span class="sxs-lookup"><span data-stu-id="6e320-544">50.00</span></span></td>
<td><span data-ttu-id="6e320-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-546">CC002</span></span></td>
<td><span data-ttu-id="6e320-547">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-547">Finance</span></span></td>
<td><span data-ttu-id="6e320-548">35</span><span class="sxs-lookup"><span data-stu-id="6e320-548">35</span></span></td>
<td><span data-ttu-id="6e320-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6e320-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6e320-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6e320-550">436.00</span></span></td>
<td><span data-ttu-id="6e320-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-552">CC003</span></span></td>
<td><span data-ttu-id="6e320-553">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-553">Assembly</span></span></td>
<td><span data-ttu-id="6e320-554">55</span><span class="sxs-lookup"><span data-stu-id="6e320-554">55</span></span></td>
<td><span data-ttu-id="6e320-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6e320-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6e320-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6e320-556">685.14</span></span></td>
<td><span data-ttu-id="6e320-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-558">CC004</span></span></td>
<td><span data-ttu-id="6e320-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-559">Packaging</span></span></td>
<td><span data-ttu-id="6e320-560">10</span><span class="sxs-lookup"><span data-stu-id="6e320-560">10</span></span></td>
<td><span data-ttu-id="6e320-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6e320-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6e320-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6e320-562">124.57</span></span></td>
<td><span data-ttu-id="6e320-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6e320-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-565">Cost object</span></span></th>
<th><span data-ttu-id="6e320-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-566">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-568">Amount</span></span></th>
<th><span data-ttu-id="6e320-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-570">CC003</span></span></td>
<td><span data-ttu-id="6e320-571">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-571">Assembly</span></span></td>
<td><span data-ttu-id="6e320-572">65</span><span class="sxs-lookup"><span data-stu-id="6e320-572">65</span></span></td>
<td><span data-ttu-id="6e320-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6e320-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6e320-574">438.75</span></span></td>
<td><span data-ttu-id="6e320-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-576">CC004</span></span></td>
<td><span data-ttu-id="6e320-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-577">Packaging</span></span></td>
<td><span data-ttu-id="6e320-578">35</span><span class="sxs-lookup"><span data-stu-id="6e320-578">35</span></span></td>
<td><span data-ttu-id="6e320-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6e320-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6e320-580">236.25</span></span></td>
<td><span data-ttu-id="6e320-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-582">CC003</span></span></td>
<td><span data-ttu-id="6e320-583">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-583">Assembly</span></span></td>
<td><span data-ttu-id="6e320-584">65</span><span class="sxs-lookup"><span data-stu-id="6e320-584">65</span></span></td>
<td><span data-ttu-id="6e320-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6e320-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6e320-586">5,297.69</span></span></td>
<td><span data-ttu-id="6e320-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-588">CC004</span></span></td>
<td><span data-ttu-id="6e320-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-589">Packaging</span></span></td>
<td><span data-ttu-id="6e320-590">35</span><span class="sxs-lookup"><span data-stu-id="6e320-590">35</span></span></td>
<td><span data-ttu-id="6e320-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6e320-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6e320-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6e320-592">2,852.60</span></span></td>
<td><span data-ttu-id="6e320-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6e320-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-595">Cost object</span></span></th>
<th><span data-ttu-id="6e320-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-596">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-598">Amount</span></span></th>
<th><span data-ttu-id="6e320-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-600">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-601">Product 1</span></span></td>
<td><span data-ttu-id="6e320-602">60</span><span class="sxs-lookup"><span data-stu-id="6e320-602">60</span></span></td>
<td><span data-ttu-id="6e320-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6e320-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6e320-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6e320-604">535.31</span></span></td>
<td><span data-ttu-id="6e320-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-606">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-607">Product 2</span></span></td>
<td><span data-ttu-id="6e320-608">20</span><span class="sxs-lookup"><span data-stu-id="6e320-608">20</span></span></td>
<td><span data-ttu-id="6e320-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6e320-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6e320-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6e320-610">178.44</span></span></td>
<td><span data-ttu-id="6e320-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-612">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-613">Product 1</span></span></td>
<td><span data-ttu-id="6e320-614">60</span><span class="sxs-lookup"><span data-stu-id="6e320-614">60</span></span></td>
<td><span data-ttu-id="6e320-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6e320-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6e320-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6e320-616">4,487.12</span></span></td>
<td><span data-ttu-id="6e320-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-618">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-619">Product 2</span></span></td>
<td><span data-ttu-id="6e320-620">20</span><span class="sxs-lookup"><span data-stu-id="6e320-620">20</span></span></td>
<td><span data-ttu-id="6e320-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6e320-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6e320-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6e320-622">1,495.71</span></span></td>
<td><span data-ttu-id="6e320-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e320-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="6e320-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-625">Cost object</span></span></th>
<th><span data-ttu-id="6e320-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="6e320-626">Magnitude</span></span></th>
<th><span data-ttu-id="6e320-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6e320-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6e320-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-628">Amount</span></span></th>
<th><span data-ttu-id="6e320-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-630">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-631">Product 1</span></span></td>
<td><span data-ttu-id="6e320-632">80</span><span class="sxs-lookup"><span data-stu-id="6e320-632">80</span></span></td>
<td><span data-ttu-id="6e320-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6e320-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6e320-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6e320-634">241.05</span></span></td>
<td><span data-ttu-id="6e320-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-636">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-637">Product 2</span></span></td>
<td><span data-ttu-id="6e320-638">15</span><span class="sxs-lookup"><span data-stu-id="6e320-638">15</span></span></td>
<td><span data-ttu-id="6e320-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6e320-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6e320-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6e320-640">45.20</span></span></td>
<td><span data-ttu-id="6e320-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-642">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-643">Product 1</span></span></td>
<td><span data-ttu-id="6e320-644">80</span><span class="sxs-lookup"><span data-stu-id="6e320-644">80</span></span></td>
<td><span data-ttu-id="6e320-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6e320-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6e320-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6e320-646">2,507.09</span></span></td>
<td><span data-ttu-id="6e320-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-648">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-649">Product 2</span></span></td>
<td><span data-ttu-id="6e320-650">15</span><span class="sxs-lookup"><span data-stu-id="6e320-650">15</span></span></td>
<td><span data-ttu-id="6e320-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6e320-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6e320-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6e320-652">470.08</span></span></td>
<td><span data-ttu-id="6e320-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6e320-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="6e320-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="6e320-655">Journal</span></span></th>
<th><span data-ttu-id="6e320-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="6e320-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6e320-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6e320-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6e320-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="6e320-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-659">00004</span><span class="sxs-lookup"><span data-stu-id="6e320-659">00004</span></span></td>
<td><span data-ttu-id="6e320-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="6e320-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6e320-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="6e320-661">Fiscal</span></span></td>
<td><span data-ttu-id="6e320-662">2017</span><span class="sxs-lookup"><span data-stu-id="6e320-662">2017</span></span></td>
<td><span data-ttu-id="6e320-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-663">Period 1</span></span></td>
<td><span data-ttu-id="6e320-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="6e320-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6e320-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="6e320-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6e320-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-668">Cost element</span></span></th>
<th><span data-ttu-id="6e320-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-672">CC001</span></span></td>
<td><span data-ttu-id="6e320-673">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-673">HR</span></span></td>
<td><span data-ttu-id="6e320-674">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-674">10001</span></span></td>
<td><span data-ttu-id="6e320-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-675">Electricity</span></span></td>
<td><span data-ttu-id="6e320-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-677">500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-679">CC001</span></span></td>
<td><span data-ttu-id="6e320-680">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-680">HR</span></span></td>
<td><span data-ttu-id="6e320-681">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-681">10001</span></span></td>
<td><span data-ttu-id="6e320-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-682">Electricity</span></span></td>
<td><span data-ttu-id="6e320-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-683">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6e320-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-686">CC002</span></span></td>
<td><span data-ttu-id="6e320-687">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-687">Finance</span></span></td>
<td><span data-ttu-id="6e320-688">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-688">10001</span></span></td>
<td><span data-ttu-id="6e320-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-689">Electricity</span></span></td>
<td><span data-ttu-id="6e320-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6e320-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-693">CC002</span></span></td>
<td><span data-ttu-id="6e320-694">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-694">Finance</span></span></td>
<td><span data-ttu-id="6e320-695">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-695">10001</span></span></td>
<td><span data-ttu-id="6e320-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-696">Electricity</span></span></td>
<td><span data-ttu-id="6e320-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-697">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6e320-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-700">CC003</span></span></td>
<td><span data-ttu-id="6e320-701">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-701">Assembly</span></span></td>
<td><span data-ttu-id="6e320-702">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-702">10001</span></span></td>
<td><span data-ttu-id="6e320-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-703">Electricity</span></span></td>
<td><span data-ttu-id="6e320-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6e320-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-707">CC003</span></span></td>
<td><span data-ttu-id="6e320-708">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-708">Assembly</span></span></td>
<td><span data-ttu-id="6e320-709">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-709">10001</span></span></td>
<td><span data-ttu-id="6e320-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-710">Electricity</span></span></td>
<td><span data-ttu-id="6e320-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-711">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6e320-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-714">CC003</span></span></td>
<td><span data-ttu-id="6e320-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-715">Packaging</span></span></td>
<td><span data-ttu-id="6e320-716">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-716">10001</span></span></td>
<td><span data-ttu-id="6e320-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-717">Electricity</span></span></td>
<td><span data-ttu-id="6e320-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6e320-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-721">CC003</span></span></td>
<td><span data-ttu-id="6e320-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-722">Packaging</span></span></td>
<td><span data-ttu-id="6e320-723">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-723">10001</span></span></td>
<td><span data-ttu-id="6e320-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-724">Electricity</span></span></td>
<td><span data-ttu-id="6e320-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-725">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6e320-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-728">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-729">Product 1</span></span></td>
<td><span data-ttu-id="6e320-730">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-730">10001</span></span></td>
<td><span data-ttu-id="6e320-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-731">Electricity</span></span></td>
<td><span data-ttu-id="6e320-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6e320-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-735">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-736">Product 1</span></span></td>
<td><span data-ttu-id="6e320-737">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-737">10001</span></span></td>
<td><span data-ttu-id="6e320-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-738">Electricity</span></span></td>
<td><span data-ttu-id="6e320-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-739">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6e320-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-742">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-743">Product 1</span></span></td>
<td><span data-ttu-id="6e320-744">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-744">10001</span></span></td>
<td><span data-ttu-id="6e320-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-745">Electricity</span></span></td>
<td><span data-ttu-id="6e320-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6e320-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6e320-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-749">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-750">Product 1</span></span></td>
<td><span data-ttu-id="6e320-751">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-751">10001</span></span></td>
<td><span data-ttu-id="6e320-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-752">Electricity</span></span></td>
<td><span data-ttu-id="6e320-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-753">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6e320-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6e320-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="6e320-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6e320-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6e320-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-757">Cost element</span></span></th>
<th><span data-ttu-id="6e320-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="6e320-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6e320-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="6e320-759">Amount</span></span></th>
<th><span data-ttu-id="6e320-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="6e320-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e320-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-761">CC001</span></span></td>
<td><span data-ttu-id="6e320-762">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-762">HR</span></span></td>
<td><span data-ttu-id="6e320-763">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-763">10001</span></span></td>
<td><span data-ttu-id="6e320-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-764">Electricity</span></span></td>
<td><span data-ttu-id="6e320-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="6e320-766">-500.00</span></span></td>
<td><span data-ttu-id="6e320-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-768">CC002</span></span></td>
<td><span data-ttu-id="6e320-769">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-769">Finance</span></span></td>
<td><span data-ttu-id="6e320-770">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-770">10001</span></span></td>
<td><span data-ttu-id="6e320-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-771">Electricity</span></span></td>
<td><span data-ttu-id="6e320-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6e320-773">175.00</span></span></td>
<td><span data-ttu-id="6e320-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-775">CC003</span></span></td>
<td><span data-ttu-id="6e320-776">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-776">Assembly</span></span></td>
<td><span data-ttu-id="6e320-777">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-777">10001</span></span></td>
<td><span data-ttu-id="6e320-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-778">Electricity</span></span></td>
<td><span data-ttu-id="6e320-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6e320-780">275.00</span></span></td>
<td><span data-ttu-id="6e320-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-782">CC004</span></span></td>
<td><span data-ttu-id="6e320-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-783">Packaging</span></span></td>
<td><span data-ttu-id="6e320-784">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-784">10001</span></span></td>
<td><span data-ttu-id="6e320-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-785">Electricity</span></span></td>
<td><span data-ttu-id="6e320-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6e320-787">50,00</span></span></td>
<td><span data-ttu-id="6e320-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-789">CC001</span></span></td>
<td><span data-ttu-id="6e320-790">Personale</span><span class="sxs-lookup"><span data-stu-id="6e320-790">HR</span></span></td>
<td><span data-ttu-id="6e320-791">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-791">10001</span></span></td>
<td><span data-ttu-id="6e320-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-792">Electricity</span></span></td>
<td><span data-ttu-id="6e320-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-793">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="6e320-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6e320-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-796">CC002</span></span></td>
<td><span data-ttu-id="6e320-797">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-797">Finance</span></span></td>
<td><span data-ttu-id="6e320-798">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-798">10001</span></span></td>
<td><span data-ttu-id="6e320-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-799">Electricity</span></span></td>
<td><span data-ttu-id="6e320-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-800">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6e320-801">436.00</span></span></td>
<td><span data-ttu-id="6e320-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-803">CC003</span></span></td>
<td><span data-ttu-id="6e320-804">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-804">Assembly</span></span></td>
<td><span data-ttu-id="6e320-805">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-805">10001</span></span></td>
<td><span data-ttu-id="6e320-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-806">Electricity</span></span></td>
<td><span data-ttu-id="6e320-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-807">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6e320-808">685.14</span></span></td>
<td><span data-ttu-id="6e320-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-810">CC004</span></span></td>
<td><span data-ttu-id="6e320-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-811">Packaging</span></span></td>
<td><span data-ttu-id="6e320-812">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-812">10001</span></span></td>
<td><span data-ttu-id="6e320-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-813">Electricity</span></span></td>
<td><span data-ttu-id="6e320-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-814">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6e320-815">124.57</span></span></td>
<td><span data-ttu-id="6e320-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-817">CC002</span></span></td>
<td><span data-ttu-id="6e320-818">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-818">Finance</span></span></td>
<td><span data-ttu-id="6e320-819">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-819">10001</span></span></td>
<td><span data-ttu-id="6e320-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-820">Electricity</span></span></td>
<td><span data-ttu-id="6e320-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="6e320-822">-675.00</span></span></td>
<td><span data-ttu-id="6e320-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-824">CC003</span></span></td>
<td><span data-ttu-id="6e320-825">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-825">Assembly</span></span></td>
<td><span data-ttu-id="6e320-826">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-826">10001</span></span></td>
<td><span data-ttu-id="6e320-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-827">Electricity</span></span></td>
<td><span data-ttu-id="6e320-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6e320-829">438.75</span></span></td>
<td><span data-ttu-id="6e320-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-831">CC004</span></span></td>
<td><span data-ttu-id="6e320-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-832">Packaging</span></span></td>
<td><span data-ttu-id="6e320-833">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-833">10001</span></span></td>
<td><span data-ttu-id="6e320-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-834">Electricity</span></span></td>
<td><span data-ttu-id="6e320-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6e320-836">236.25</span></span></td>
<td><span data-ttu-id="6e320-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-838">CC002</span></span></td>
<td><span data-ttu-id="6e320-839">Finans</span><span class="sxs-lookup"><span data-stu-id="6e320-839">Finance</span></span></td>
<td><span data-ttu-id="6e320-840">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-840">10001</span></span></td>
<td><span data-ttu-id="6e320-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-841">Electricity</span></span></td>
<td><span data-ttu-id="6e320-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-842">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="6e320-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6e320-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-845">CC003</span></span></td>
<td><span data-ttu-id="6e320-846">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-846">Assembly</span></span></td>
<td><span data-ttu-id="6e320-847">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-847">10001</span></span></td>
<td><span data-ttu-id="6e320-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-848">Electricity</span></span></td>
<td><span data-ttu-id="6e320-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-849">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6e320-850">5,297.69</span></span></td>
<td><span data-ttu-id="6e320-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-852">CC004</span></span></td>
<td><span data-ttu-id="6e320-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="6e320-853">Packaging</span></span></td>
<td><span data-ttu-id="6e320-854">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-854">10001</span></span></td>
<td><span data-ttu-id="6e320-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-855">Electricity</span></span></td>
<td><span data-ttu-id="6e320-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-856">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6e320-857">2,852.60</span></span></td>
<td><span data-ttu-id="6e320-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-859">CC003</span></span></td>
<td><span data-ttu-id="6e320-860">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-860">Assembly</span></span></td>
<td><span data-ttu-id="6e320-861">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-861">10001</span></span></td>
<td><span data-ttu-id="6e320-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-862">Electricity</span></span></td>
<td><span data-ttu-id="6e320-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="6e320-864">-713.75</span></span></td>
<td><span data-ttu-id="6e320-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-866">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-867">Product 1</span></span></td>
<td><span data-ttu-id="6e320-868">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-868">10001</span></span></td>
<td><span data-ttu-id="6e320-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-869">Electricity</span></span></td>
<td><span data-ttu-id="6e320-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6e320-871">535.31</span></span></td>
<td><span data-ttu-id="6e320-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-873">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-874">Product 2</span></span></td>
<td><span data-ttu-id="6e320-875">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-875">10001</span></span></td>
<td><span data-ttu-id="6e320-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-876">Electricity</span></span></td>
<td><span data-ttu-id="6e320-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6e320-878">178.44</span></span></td>
<td><span data-ttu-id="6e320-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-880">CC003</span></span></td>
<td><span data-ttu-id="6e320-881">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-881">Assembly</span></span></td>
<td><span data-ttu-id="6e320-882">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-882">10001</span></span></td>
<td><span data-ttu-id="6e320-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-883">Electricity</span></span></td>
<td><span data-ttu-id="6e320-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-884">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="6e320-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6e320-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-887">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-888">Product 1</span></span></td>
<td><span data-ttu-id="6e320-889">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-889">10001</span></span></td>
<td><span data-ttu-id="6e320-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-890">Electricity</span></span></td>
<td><span data-ttu-id="6e320-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-891">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6e320-892">4,487.12</span></span></td>
<td><span data-ttu-id="6e320-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-894">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-895">Product 2</span></span></td>
<td><span data-ttu-id="6e320-896">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-896">10001</span></span></td>
<td><span data-ttu-id="6e320-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-897">Electricity</span></span></td>
<td><span data-ttu-id="6e320-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-898">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6e320-899">1,495.71</span></span></td>
<td><span data-ttu-id="6e320-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-901">CC003</span></span></td>
<td><span data-ttu-id="6e320-902">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-902">Assembly</span></span></td>
<td><span data-ttu-id="6e320-903">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-903">10001</span></span></td>
<td><span data-ttu-id="6e320-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-904">Electricity</span></span></td>
<td><span data-ttu-id="6e320-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="6e320-906">-286.25</span></span></td>
<td><span data-ttu-id="6e320-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-908">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-909">Product 1</span></span></td>
<td><span data-ttu-id="6e320-910">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-910">10001</span></span></td>
<td><span data-ttu-id="6e320-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-911">Electricity</span></span></td>
<td><span data-ttu-id="6e320-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6e320-913">241.05</span></span></td>
<td><span data-ttu-id="6e320-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-915">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-916">Product 2</span></span></td>
<td><span data-ttu-id="6e320-917">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-917">10001</span></span></td>
<td><span data-ttu-id="6e320-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-918">Electricity</span></span></td>
<td><span data-ttu-id="6e320-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6e320-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6e320-920">45.20</span></span></td>
<td><span data-ttu-id="6e320-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-922">CC003</span></span></td>
<td><span data-ttu-id="6e320-923">Samling</span><span class="sxs-lookup"><span data-stu-id="6e320-923">Assembly</span></span></td>
<td><span data-ttu-id="6e320-924">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-924">10001</span></span></td>
<td><span data-ttu-id="6e320-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-925">Electricity</span></span></td>
<td><span data-ttu-id="6e320-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-926">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="6e320-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6e320-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-929">Prod 1</span></span></td>
<td><span data-ttu-id="6e320-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6e320-930">Product 1</span></span></td>
<td><span data-ttu-id="6e320-931">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-931">10001</span></span></td>
<td><span data-ttu-id="6e320-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-932">Electricity</span></span></td>
<td><span data-ttu-id="6e320-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-933">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6e320-934">2,507.09</span></span></td>
<td><span data-ttu-id="6e320-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e320-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-936">Prod 2</span></span></td>
<td><span data-ttu-id="6e320-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6e320-937">Product 2</span></span></td>
<td><span data-ttu-id="6e320-938">10001</span><span class="sxs-lookup"><span data-stu-id="6e320-938">10001</span></span></td>
<td><span data-ttu-id="6e320-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="6e320-939">Electricity</span></span></td>
<td><span data-ttu-id="6e320-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-940">Variable cost</span></span></td>
<td><span data-ttu-id="6e320-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6e320-941">470.08</span></span></td>
<td><span data-ttu-id="6e320-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6e320-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6e320-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="6e320-943">Conclusion</span></span>
<span data-ttu-id="6e320-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="6e320-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6e320-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="6e320-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6e320-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="6e320-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6e320-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="6e320-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6e320-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="6e320-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6e320-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="6e320-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6e320-950">Sum</span><span class="sxs-lookup"><span data-stu-id="6e320-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6e320-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6e320-951">CC099</span></span></th>
<th><span data-ttu-id="6e320-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6e320-952">CC001</span></span></th>
<th><span data-ttu-id="6e320-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6e320-953">CC002</span></span></th>
<th><span data-ttu-id="6e320-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6e320-954">CC003</span></span></th>
<th><span data-ttu-id="6e320-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6e320-955">CC004</span></span></th>
<th><span data-ttu-id="6e320-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="6e320-956">Proj 1</span></span></th>
<th><span data-ttu-id="6e320-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="6e320-957">Proj 2</span></span></th>
<th><span data-ttu-id="6e320-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6e320-958">Prod 1</span></span></th>
<th><span data-ttu-id="6e320-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6e320-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6e320-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="6e320-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6e320-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6e320-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="6e320-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-971">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6e320-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-973">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-974">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-975">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-976">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-977">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6e320-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6e320-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6e320-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6e320-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="6e320-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-982">000</span><span class="sxs-lookup"><span data-stu-id="6e320-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-983">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-984">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-985">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-986">0,00</span><span class="sxs-lookup"><span data-stu-id="6e320-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-987">30,00</span><span class="sxs-lookup"><span data-stu-id="6e320-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-988">10,00</span><span class="sxs-lookup"><span data-stu-id="6e320-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6e320-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6e320-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6e320-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6e320-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6e320-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="6e320-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6e320-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="6e320-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6e320-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="6e320-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6e320-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="6e320-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6e320-996">Hvis du vil ha mer informasjon, se [Policy for opprullet kost og beregning av administrasjonskostnader](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="6e320-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



