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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "335123"
---
# <a name="overhead-calculation"></a><span data-ttu-id="94ad2-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="94ad2-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94ad2-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="94ad2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="94ad2-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-105">Term definition</span></span>
---------------

<span data-ttu-id="94ad2-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="94ad2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="94ad2-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="94ad2-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="94ad2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="94ad2-109">Leie</span><span class="sxs-lookup"><span data-stu-id="94ad2-109">Rent</span></span>
-   <span data-ttu-id="94ad2-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-110">Electricity</span></span>
-   <span data-ttu-id="94ad2-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="94ad2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="94ad2-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="94ad2-112">Overhead calculation overview</span></span>
<span data-ttu-id="94ad2-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="94ad2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="94ad2-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="94ad2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="94ad2-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="94ad2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="94ad2-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="94ad2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="94ad2-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="94ad2-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="94ad2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="94ad2-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="94ad2-119">Version type</span></span>
-   <span data-ttu-id="94ad2-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="94ad2-120">Date and time</span></span>
-   <span data-ttu-id="94ad2-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="94ad2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="94ad2-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="94ad2-122">Fiscal year</span></span>
-   <span data-ttu-id="94ad2-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="94ad2-123">Fiscal period</span></span>

<span data-ttu-id="94ad2-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="94ad2-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="94ad2-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="94ad2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="94ad2-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="94ad2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="94ad2-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="94ad2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="94ad2-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="94ad2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="94ad2-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="94ad2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="94ad2-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="94ad2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="94ad2-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="94ad2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="94ad2-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="94ad2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="94ad2-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="94ad2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="94ad2-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="94ad2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="94ad2-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="94ad2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="94ad2-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="94ad2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="94ad2-140">Main account</span></span></th>
<th><span data-ttu-id="94ad2-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="94ad2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="94ad2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-143">CC099</span></span></td>
<td><span data-ttu-id="94ad2-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-144">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-145">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-145">10001</span></span></td>
<td><span data-ttu-id="94ad2-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-146">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="94ad2-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="94ad2-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="94ad2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="94ad2-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="94ad2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="94ad2-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="94ad2-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="94ad2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="94ad2-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="94ad2-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="94ad2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="94ad2-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="94ad2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="94ad2-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="94ad2-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="94ad2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="94ad2-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="94ad2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="94ad2-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-160">Journal</span></span></th>
<th><span data-ttu-id="94ad2-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="94ad2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="94ad2-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="94ad2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="94ad2-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-164">00001</span><span class="sxs-lookup"><span data-stu-id="94ad2-164">00001</span></span></td>
<td><span data-ttu-id="94ad2-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="94ad2-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="94ad2-166">Fiscal</span></span></td>
<td><span data-ttu-id="94ad2-167">2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-167">2017</span></span></td>
<td><span data-ttu-id="94ad2-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-168">Period 1</span></span></td>
<td><span data-ttu-id="94ad2-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="94ad2-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="94ad2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-173">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="94ad2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-177">CC099</span></span></td>
<td><span data-ttu-id="94ad2-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-178">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-179">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-179">10001</span></span></td>
<td><span data-ttu-id="94ad2-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-180">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="94ad2-181">Unclassified</span></span></td>
<td><span data-ttu-id="94ad2-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="94ad2-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="94ad2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-185">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-187">Amount</span></span></th>
<th><span data-ttu-id="94ad2-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-189">CC099</span></span></td>
<td><span data-ttu-id="94ad2-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-190">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-191">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-191">10001</span></span></td>
<td><span data-ttu-id="94ad2-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-192">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="94ad2-193">Unclassified</span></span></td>
<td><span data-ttu-id="94ad2-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-194">10,000.00</span></span></td>
<td><span data-ttu-id="94ad2-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-196">CC099</span></span></td>
<td><span data-ttu-id="94ad2-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-197">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-198">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-198">10001</span></span></td>
<td><span data-ttu-id="94ad2-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-199">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="94ad2-200">Unclassified</span></span></td>
<td><span data-ttu-id="94ad2-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="94ad2-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-203">CC099</span></span></td>
<td><span data-ttu-id="94ad2-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-204">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-205">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-205">10001</span></span></td>
<td><span data-ttu-id="94ad2-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-206">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-208">1,000.00</span></span></td>
<td><span data-ttu-id="94ad2-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-210">CC099</span></span></td>
<td><span data-ttu-id="94ad2-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-211">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-212">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-212">10001</span></span></td>
<td><span data-ttu-id="94ad2-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="94ad2-213">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-214">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-215">9,000.00</span></span></td>
<td><span data-ttu-id="94ad2-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="94ad2-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="94ad2-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="94ad2-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="94ad2-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="94ad2-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="94ad2-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="94ad2-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-221">Define the cost distribution rule</span></span>

<span data-ttu-id="94ad2-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="94ad2-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="94ad2-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="94ad2-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="94ad2-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="94ad2-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="94ad2-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="94ad2-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="94ad2-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="94ad2-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="94ad2-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="94ad2-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-228">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-229">kWt</span><span class="sxs-lookup"><span data-stu-id="94ad2-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-230">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-230">CC001</span></span></td>
<td><span data-ttu-id="94ad2-231">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-231">HR</span></span></td>
<td><span data-ttu-id="94ad2-232">1 000</span><span class="sxs-lookup"><span data-stu-id="94ad2-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-233">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-233">CC002</span></span></td>
<td><span data-ttu-id="94ad2-234">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-234">Finance</span></span></td>
<td><span data-ttu-id="94ad2-235">6,000</span><span class="sxs-lookup"><span data-stu-id="94ad2-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-236">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-236">CC003</span></span></td>
<td><span data-ttu-id="94ad2-237">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-237">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-238">0</span><span class="sxs-lookup"><span data-stu-id="94ad2-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="94ad2-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-240">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-241">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-242">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-244">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-244">CC001</span></span></td>
<td><span data-ttu-id="94ad2-245">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-245">HR</span></span></td>
<td><span data-ttu-id="94ad2-246">1 000</span><span class="sxs-lookup"><span data-stu-id="94ad2-246">1,000</span></span></td>
<td><span data-ttu-id="94ad2-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="94ad2-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="94ad2-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-249">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-249">CC002</span></span></td>
<td><span data-ttu-id="94ad2-250">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-250">Finance</span></span></td>
<td><span data-ttu-id="94ad2-251">6,000</span><span class="sxs-lookup"><span data-stu-id="94ad2-251">6,000</span></span></td>
<td><span data-ttu-id="94ad2-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="94ad2-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="94ad2-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-254">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-254">CC003</span></span></td>
<td><span data-ttu-id="94ad2-255">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-255">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-256">0</span><span class="sxs-lookup"><span data-stu-id="94ad2-256">0</span></span></td>
<td><span data-ttu-id="94ad2-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="94ad2-258">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="94ad2-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="94ad2-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="94ad2-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-261">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-262">Formel</span><span class="sxs-lookup"><span data-stu-id="94ad2-262">Formula</span></span></th>
<th><span data-ttu-id="94ad2-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-263">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-264">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-266">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-266">CC001</span></span></td>
<td><span data-ttu-id="94ad2-267">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-267">HR</span></span></td>
<td><span data-ttu-id="94ad2-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="94ad2-269">1</span><span class="sxs-lookup"><span data-stu-id="94ad2-269">1</span></span></td>
<td><span data-ttu-id="94ad2-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="94ad2-271">500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-272">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-272">CC002</span></span></td>
<td><span data-ttu-id="94ad2-273">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-273">Finance</span></span></td>
<td><span data-ttu-id="94ad2-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="94ad2-275">1</span><span class="sxs-lookup"><span data-stu-id="94ad2-275">1</span></span></td>
<td><span data-ttu-id="94ad2-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="94ad2-277">500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-278">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-278">CC003</span></span></td>
<td><span data-ttu-id="94ad2-279">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-279">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="94ad2-281">0</span><span class="sxs-lookup"><span data-stu-id="94ad2-281">0</span></span></td>
<td><span data-ttu-id="94ad2-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="94ad2-283">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="94ad2-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-285">Journal</span></span></th>
<th><span data-ttu-id="94ad2-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="94ad2-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="94ad2-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="94ad2-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="94ad2-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-289">00002</span><span class="sxs-lookup"><span data-stu-id="94ad2-289">00002</span></span></td>
<td><span data-ttu-id="94ad2-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="94ad2-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="94ad2-291">Fiscal</span></span></td>
<td><span data-ttu-id="94ad2-292">2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-292">2017</span></span></td>
<td><span data-ttu-id="94ad2-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-293">Period 1</span></span></td>
<td><span data-ttu-id="94ad2-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="94ad2-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="94ad2-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-298">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-299">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-302">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-302">CC099</span></span></td>
<td><span data-ttu-id="94ad2-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-303">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-304">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-304">10001</span></span></td>
<td><span data-ttu-id="94ad2-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-305">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-306">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-309">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-309">CC099</span></span></td>
<td><span data-ttu-id="94ad2-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-310">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-311">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-311">10001</span></span></td>
<td><span data-ttu-id="94ad2-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-312">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-313">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="94ad2-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="94ad2-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-317">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-318">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-319">Amount</span></span></th>
<th><span data-ttu-id="94ad2-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-321">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-321">CC099</span></span></td>
<td><span data-ttu-id="94ad2-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-322">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-323">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-323">10001</span></span></td>
<td><span data-ttu-id="94ad2-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-324">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-325">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-326">-1,000.00</span></span></td>
<td><span data-ttu-id="94ad2-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-328">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-328">CC001</span></span></td>
<td><span data-ttu-id="94ad2-329">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-329">HR</span></span></td>
<td><span data-ttu-id="94ad2-330">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-330">10001</span></span></td>
<td><span data-ttu-id="94ad2-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-331">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-332">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-333">500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-333">500.00</span></span></td>
<td><span data-ttu-id="94ad2-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-335">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-335">CC002</span></span></td>
<td><span data-ttu-id="94ad2-336">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-336">Finance</span></span></td>
<td><span data-ttu-id="94ad2-337">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-337">10001</span></span></td>
<td><span data-ttu-id="94ad2-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-338">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-339">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-340">500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-340">500.00</span></span></td>
<td><span data-ttu-id="94ad2-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-342">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-342">CC099</span></span></td>
<td><span data-ttu-id="94ad2-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="94ad2-343">Default cost center</span></span></td>
<td><span data-ttu-id="94ad2-344">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-344">10001</span></span></td>
<td><span data-ttu-id="94ad2-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-345">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-346">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-347">-9,000.00</span></span></td>
<td><span data-ttu-id="94ad2-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-349">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-349">CC001</span></span></td>
<td><span data-ttu-id="94ad2-350">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-350">HR</span></span></td>
<td><span data-ttu-id="94ad2-351">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-351">10001</span></span></td>
<td><span data-ttu-id="94ad2-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-352">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-353">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="94ad2-354">1,285.71</span></span></td>
<td><span data-ttu-id="94ad2-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-356">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-356">CC002</span></span></td>
<td><span data-ttu-id="94ad2-357">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-357">Finance</span></span></td>
<td><span data-ttu-id="94ad2-358">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-358">10001</span></span></td>
<td><span data-ttu-id="94ad2-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="94ad2-359">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-360">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="94ad2-361">7,714.29</span></span></td>
<td><span data-ttu-id="94ad2-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="94ad2-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="94ad2-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="94ad2-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="94ad2-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="94ad2-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="94ad2-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="94ad2-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="94ad2-367">Define the overhead rate</span></span>

<span data-ttu-id="94ad2-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="94ad2-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-370">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="94ad2-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-372">Proj 1</span></span></td>
<td><span data-ttu-id="94ad2-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-373">Project 1</span></span></td>
<td><span data-ttu-id="94ad2-374">3</span><span class="sxs-lookup"><span data-stu-id="94ad2-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-375">Proj 2</span></span></td>
<td><span data-ttu-id="94ad2-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-376">Project 2</span></span></td>
<td><span data-ttu-id="94ad2-377">1</span><span class="sxs-lookup"><span data-stu-id="94ad2-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="94ad2-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-379">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-380">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-381">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="94ad2-382">Units</span></span></th>
<th><span data-ttu-id="94ad2-383">Sats</span><span class="sxs-lookup"><span data-stu-id="94ad2-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-384">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-384">CC001</span></span></td>
<td><span data-ttu-id="94ad2-385">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-385">HR</span></span></td>
<td><span data-ttu-id="94ad2-386">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-386">10001</span></span></td>
<td><span data-ttu-id="94ad2-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-387">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-388">1</span><span class="sxs-lookup"><span data-stu-id="94ad2-388">1</span></span></td>
<td><span data-ttu-id="94ad2-389">10</span><span class="sxs-lookup"><span data-stu-id="94ad2-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="94ad2-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-391">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-392">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-393">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-394">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-396">Proj 1</span></span></td>
<td><span data-ttu-id="94ad2-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-397">Project 1</span></span></td>
<td><span data-ttu-id="94ad2-398">3</span><span class="sxs-lookup"><span data-stu-id="94ad2-398">3</span></span></td>
<td><span data-ttu-id="94ad2-399">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-399">10001</span></span></td>
<td><span data-ttu-id="94ad2-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="94ad2-401">30,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-402">Proj 2</span></span></td>
<td><span data-ttu-id="94ad2-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-403">Project 2</span></span></td>
<td><span data-ttu-id="94ad2-404">1</span><span class="sxs-lookup"><span data-stu-id="94ad2-404">1</span></span></td>
<td><span data-ttu-id="94ad2-405">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-405">10001</span></span></td>
<td><span data-ttu-id="94ad2-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="94ad2-407">10,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="94ad2-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-409">Journal</span></span></th>
<th><span data-ttu-id="94ad2-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="94ad2-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="94ad2-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="94ad2-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="94ad2-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-413">00003</span><span class="sxs-lookup"><span data-stu-id="94ad2-413">00003</span></span></td>
<td><span data-ttu-id="94ad2-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="94ad2-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="94ad2-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="94ad2-415">Fiscal</span></span></td>
<td><span data-ttu-id="94ad2-416">2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-416">2017</span></span></td>
<td><span data-ttu-id="94ad2-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-417">Period 1</span></span></td>
<td><span data-ttu-id="94ad2-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="94ad2-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="94ad2-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-421">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-424">Proj 1</span></span></td>
<td><span data-ttu-id="94ad2-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="94ad2-426">3,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-428">Proj 2</span></span></td>
<td><span data-ttu-id="94ad2-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="94ad2-430">1,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="94ad2-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="94ad2-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-433">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-434">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-435">Amount</span></span></th>
<th><span data-ttu-id="94ad2-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="94ad2-437">CC0001</span></span></td>
<td><span data-ttu-id="94ad2-438">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-438">HR</span></span></td>
<td><span data-ttu-id="94ad2-439">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-439">10001</span></span></td>
<td><span data-ttu-id="94ad2-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-440">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-441">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-442">-30.00</span></span></td>
<td><span data-ttu-id="94ad2-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-444">Proj 1</span></span></td>
<td><span data-ttu-id="94ad2-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="94ad2-446">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-446">10001</span></span></td>
<td><span data-ttu-id="94ad2-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-447">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-448">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-449">30,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-449">30.00</span></span></td>
<td><span data-ttu-id="94ad2-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-451">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-451">CC001</span></span></td>
<td><span data-ttu-id="94ad2-452">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-452">HR</span></span></td>
<td><span data-ttu-id="94ad2-453">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-453">10001</span></span></td>
<td><span data-ttu-id="94ad2-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-454">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-455">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-456">-10.00</span></span></td>
<td><span data-ttu-id="94ad2-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-458">Proj 2</span></span></td>
<td><span data-ttu-id="94ad2-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="94ad2-460">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-460">10001</span></span></td>
<td><span data-ttu-id="94ad2-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="94ad2-461">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-462">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-463">10,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-463">10.00</span></span></td>
<td><span data-ttu-id="94ad2-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="94ad2-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="94ad2-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="94ad2-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="94ad2-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="94ad2-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="94ad2-468">Finance and Operations støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="94ad2-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="94ad2-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="94ad2-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="94ad2-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="94ad2-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="94ad2-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="94ad2-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="94ad2-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="94ad2-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="94ad2-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="94ad2-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="94ad2-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="94ad2-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="94ad2-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="94ad2-475">Define the cost allocation</span></span>

<span data-ttu-id="94ad2-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="94ad2-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="94ad2-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="94ad2-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-479">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="94ad2-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-481">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-481">CC002</span></span></td>
<td><span data-ttu-id="94ad2-482">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-482">Finance</span></span></td>
<td><span data-ttu-id="94ad2-483">35</span><span class="sxs-lookup"><span data-stu-id="94ad2-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-484">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-484">CC003</span></span></td>
<td><span data-ttu-id="94ad2-485">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-485">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-486">55</span><span class="sxs-lookup"><span data-stu-id="94ad2-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-487">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-487">CC004</span></span></td>
<td><span data-ttu-id="94ad2-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-488">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-489">10</span><span class="sxs-lookup"><span data-stu-id="94ad2-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="94ad2-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-492">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="94ad2-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-494">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-494">CC003</span></span></td>
<td><span data-ttu-id="94ad2-495">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-495">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-496">65</span><span class="sxs-lookup"><span data-stu-id="94ad2-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-497">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-497">CC004</span></span></td>
<td><span data-ttu-id="94ad2-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-498">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-499">35</span><span class="sxs-lookup"><span data-stu-id="94ad2-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="94ad2-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-502">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="94ad2-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-504">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-505">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-506">60</span><span class="sxs-lookup"><span data-stu-id="94ad2-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-507">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-508">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-509">20</span><span class="sxs-lookup"><span data-stu-id="94ad2-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="94ad2-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="94ad2-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-512">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="94ad2-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-514">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-514">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-515">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-516">80</span><span class="sxs-lookup"><span data-stu-id="94ad2-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-517">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-518">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-519">sept.</span><span class="sxs-lookup"><span data-stu-id="94ad2-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="94ad2-520">I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="94ad2-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="94ad2-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="94ad2-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="94ad2-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="94ad2-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-523">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-524">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-525">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-526">Amount</span></span></th>
<th><span data-ttu-id="94ad2-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-528">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-528">CC002</span></span></td>
<td><span data-ttu-id="94ad2-529">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-529">Finance</span></span></td>
<td><span data-ttu-id="94ad2-530">35</span><span class="sxs-lookup"><span data-stu-id="94ad2-530">35</span></span></td>
<td><span data-ttu-id="94ad2-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="94ad2-532">175.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-532">175.00</span></span></td>
<td><span data-ttu-id="94ad2-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-534">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-534">CC003</span></span></td>
<td><span data-ttu-id="94ad2-535">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-535">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-536">55</span><span class="sxs-lookup"><span data-stu-id="94ad2-536">55</span></span></td>
<td><span data-ttu-id="94ad2-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="94ad2-538">275.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-538">275.00</span></span></td>
<td><span data-ttu-id="94ad2-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-540">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-540">CC004</span></span></td>
<td><span data-ttu-id="94ad2-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-541">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-542">10</span><span class="sxs-lookup"><span data-stu-id="94ad2-542">10</span></span></td>
<td><span data-ttu-id="94ad2-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="94ad2-544">50,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-544">50.00</span></span></td>
<td><span data-ttu-id="94ad2-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-546">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-546">CC002</span></span></td>
<td><span data-ttu-id="94ad2-547">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-547">Finance</span></span></td>
<td><span data-ttu-id="94ad2-548">35</span><span class="sxs-lookup"><span data-stu-id="94ad2-548">35</span></span></td>
<td><span data-ttu-id="94ad2-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="94ad2-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="94ad2-550">436.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-550">436.00</span></span></td>
<td><span data-ttu-id="94ad2-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-552">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-552">CC003</span></span></td>
<td><span data-ttu-id="94ad2-553">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-553">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-554">55</span><span class="sxs-lookup"><span data-stu-id="94ad2-554">55</span></span></td>
<td><span data-ttu-id="94ad2-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="94ad2-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="94ad2-556">685.14</span><span class="sxs-lookup"><span data-stu-id="94ad2-556">685.14</span></span></td>
<td><span data-ttu-id="94ad2-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-558">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-558">CC004</span></span></td>
<td><span data-ttu-id="94ad2-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-559">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-560">10</span><span class="sxs-lookup"><span data-stu-id="94ad2-560">10</span></span></td>
<td><span data-ttu-id="94ad2-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="94ad2-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="94ad2-562">124.57</span><span class="sxs-lookup"><span data-stu-id="94ad2-562">124.57</span></span></td>
<td><span data-ttu-id="94ad2-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="94ad2-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-565">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-566">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-567">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-568">Amount</span></span></th>
<th><span data-ttu-id="94ad2-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-570">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-570">CC003</span></span></td>
<td><span data-ttu-id="94ad2-571">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-571">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-572">65</span><span class="sxs-lookup"><span data-stu-id="94ad2-572">65</span></span></td>
<td><span data-ttu-id="94ad2-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="94ad2-574">438.75</span><span class="sxs-lookup"><span data-stu-id="94ad2-574">438.75</span></span></td>
<td><span data-ttu-id="94ad2-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-576">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-576">CC004</span></span></td>
<td><span data-ttu-id="94ad2-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-577">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-578">35</span><span class="sxs-lookup"><span data-stu-id="94ad2-578">35</span></span></td>
<td><span data-ttu-id="94ad2-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="94ad2-580">236.25</span><span class="sxs-lookup"><span data-stu-id="94ad2-580">236.25</span></span></td>
<td><span data-ttu-id="94ad2-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-582">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-582">CC003</span></span></td>
<td><span data-ttu-id="94ad2-583">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-583">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-584">65</span><span class="sxs-lookup"><span data-stu-id="94ad2-584">65</span></span></td>
<td><span data-ttu-id="94ad2-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="94ad2-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="94ad2-586">5,297.69</span></span></td>
<td><span data-ttu-id="94ad2-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-588">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-588">CC004</span></span></td>
<td><span data-ttu-id="94ad2-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-589">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-590">35</span><span class="sxs-lookup"><span data-stu-id="94ad2-590">35</span></span></td>
<td><span data-ttu-id="94ad2-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="94ad2-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="94ad2-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="94ad2-592">2,852.60</span></span></td>
<td><span data-ttu-id="94ad2-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="94ad2-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-595">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-596">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-597">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-598">Amount</span></span></th>
<th><span data-ttu-id="94ad2-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-600">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-601">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-602">60</span><span class="sxs-lookup"><span data-stu-id="94ad2-602">60</span></span></td>
<td><span data-ttu-id="94ad2-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="94ad2-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="94ad2-604">535.31</span><span class="sxs-lookup"><span data-stu-id="94ad2-604">535.31</span></span></td>
<td><span data-ttu-id="94ad2-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-606">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-607">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-608">20</span><span class="sxs-lookup"><span data-stu-id="94ad2-608">20</span></span></td>
<td><span data-ttu-id="94ad2-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="94ad2-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="94ad2-610">178.44</span><span class="sxs-lookup"><span data-stu-id="94ad2-610">178.44</span></span></td>
<td><span data-ttu-id="94ad2-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-612">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-613">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-614">60</span><span class="sxs-lookup"><span data-stu-id="94ad2-614">60</span></span></td>
<td><span data-ttu-id="94ad2-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="94ad2-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="94ad2-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="94ad2-616">4,487.12</span></span></td>
<td><span data-ttu-id="94ad2-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-618">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-619">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-620">20</span><span class="sxs-lookup"><span data-stu-id="94ad2-620">20</span></span></td>
<td><span data-ttu-id="94ad2-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="94ad2-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="94ad2-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="94ad2-622">1,495.71</span></span></td>
<td><span data-ttu-id="94ad2-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="94ad2-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="94ad2-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-625">Cost object</span></span></th>
<th><span data-ttu-id="94ad2-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="94ad2-626">Magnitude</span></span></th>
<th><span data-ttu-id="94ad2-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="94ad2-627">Allocation factor</span></span></th>
<th><span data-ttu-id="94ad2-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-628">Amount</span></span></th>
<th><span data-ttu-id="94ad2-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-630">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-631">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-632">80</span><span class="sxs-lookup"><span data-stu-id="94ad2-632">80</span></span></td>
<td><span data-ttu-id="94ad2-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="94ad2-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="94ad2-634">241.05</span><span class="sxs-lookup"><span data-stu-id="94ad2-634">241.05</span></span></td>
<td><span data-ttu-id="94ad2-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-636">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-637">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-638">15</span><span class="sxs-lookup"><span data-stu-id="94ad2-638">15</span></span></td>
<td><span data-ttu-id="94ad2-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="94ad2-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="94ad2-640">45.20</span><span class="sxs-lookup"><span data-stu-id="94ad2-640">45.20</span></span></td>
<td><span data-ttu-id="94ad2-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-642">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-643">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-644">80</span><span class="sxs-lookup"><span data-stu-id="94ad2-644">80</span></span></td>
<td><span data-ttu-id="94ad2-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="94ad2-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="94ad2-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="94ad2-646">2,507.09</span></span></td>
<td><span data-ttu-id="94ad2-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-648">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-649">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-650">15</span><span class="sxs-lookup"><span data-stu-id="94ad2-650">15</span></span></td>
<td><span data-ttu-id="94ad2-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="94ad2-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="94ad2-652">470.08</span><span class="sxs-lookup"><span data-stu-id="94ad2-652">470.08</span></span></td>
<td><span data-ttu-id="94ad2-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="94ad2-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="94ad2-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="94ad2-655">Journal</span></span></th>
<th><span data-ttu-id="94ad2-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="94ad2-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="94ad2-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="94ad2-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="94ad2-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-659">00004</span><span class="sxs-lookup"><span data-stu-id="94ad2-659">00004</span></span></td>
<td><span data-ttu-id="94ad2-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="94ad2-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="94ad2-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="94ad2-661">Fiscal</span></span></td>
<td><span data-ttu-id="94ad2-662">2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-662">2017</span></span></td>
<td><span data-ttu-id="94ad2-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-663">Period 1</span></span></td>
<td><span data-ttu-id="94ad2-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="94ad2-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="94ad2-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94ad2-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-668">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-669">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-672">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-672">CC001</span></span></td>
<td><span data-ttu-id="94ad2-673">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-673">HR</span></span></td>
<td><span data-ttu-id="94ad2-674">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-674">10001</span></span></td>
<td><span data-ttu-id="94ad2-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-675">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-676">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-677">500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-679">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-679">CC001</span></span></td>
<td><span data-ttu-id="94ad2-680">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-680">HR</span></span></td>
<td><span data-ttu-id="94ad2-681">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-681">10001</span></span></td>
<td><span data-ttu-id="94ad2-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-682">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-683">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="94ad2-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-686">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-686">CC002</span></span></td>
<td><span data-ttu-id="94ad2-687">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-687">Finance</span></span></td>
<td><span data-ttu-id="94ad2-688">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-688">10001</span></span></td>
<td><span data-ttu-id="94ad2-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-689">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-690">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-691">675.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-693">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-693">CC002</span></span></td>
<td><span data-ttu-id="94ad2-694">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-694">Finance</span></span></td>
<td><span data-ttu-id="94ad2-695">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-695">10001</span></span></td>
<td><span data-ttu-id="94ad2-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-696">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-697">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="94ad2-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-700">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-700">CC003</span></span></td>
<td><span data-ttu-id="94ad2-701">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-701">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-702">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-702">10001</span></span></td>
<td><span data-ttu-id="94ad2-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-703">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-704">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-705">713.75</span><span class="sxs-lookup"><span data-stu-id="94ad2-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-707">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-707">CC003</span></span></td>
<td><span data-ttu-id="94ad2-708">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-708">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-709">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-709">10001</span></span></td>
<td><span data-ttu-id="94ad2-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-710">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-711">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="94ad2-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-714">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-714">CC003</span></span></td>
<td><span data-ttu-id="94ad2-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-715">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-716">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-716">10001</span></span></td>
<td><span data-ttu-id="94ad2-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-717">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-718">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-719">286.25</span><span class="sxs-lookup"><span data-stu-id="94ad2-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-721">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-721">CC003</span></span></td>
<td><span data-ttu-id="94ad2-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-722">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-723">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-723">10001</span></span></td>
<td><span data-ttu-id="94ad2-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-724">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-725">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="94ad2-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-728">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-729">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-730">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-730">10001</span></span></td>
<td><span data-ttu-id="94ad2-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-731">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-732">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-733">776.36</span><span class="sxs-lookup"><span data-stu-id="94ad2-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-735">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-736">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-737">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-737">10001</span></span></td>
<td><span data-ttu-id="94ad2-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-738">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-739">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="94ad2-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-742">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-743">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-744">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-744">10001</span></span></td>
<td><span data-ttu-id="94ad2-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-745">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-746">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-747">223.64</span><span class="sxs-lookup"><span data-stu-id="94ad2-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="94ad2-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-749">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-750">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-751">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-751">10001</span></span></td>
<td><span data-ttu-id="94ad2-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-752">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-753">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="94ad2-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="94ad2-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="94ad2-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="94ad2-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="94ad2-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-757">Cost element</span></span></th>
<th><span data-ttu-id="94ad2-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="94ad2-758">Cost behavior</span></span></th>
<th><span data-ttu-id="94ad2-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="94ad2-759">Amount</span></span></th>
<th><span data-ttu-id="94ad2-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="94ad2-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94ad2-761">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-761">CC001</span></span></td>
<td><span data-ttu-id="94ad2-762">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-762">HR</span></span></td>
<td><span data-ttu-id="94ad2-763">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-763">10001</span></span></td>
<td><span data-ttu-id="94ad2-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-764">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-765">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-766">-500.00</span></span></td>
<td><span data-ttu-id="94ad2-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-768">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-768">CC002</span></span></td>
<td><span data-ttu-id="94ad2-769">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-769">Finance</span></span></td>
<td><span data-ttu-id="94ad2-770">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-770">10001</span></span></td>
<td><span data-ttu-id="94ad2-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-771">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-772">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-773">175.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-773">175.00</span></span></td>
<td><span data-ttu-id="94ad2-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-775">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-775">CC003</span></span></td>
<td><span data-ttu-id="94ad2-776">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-776">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-777">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-777">10001</span></span></td>
<td><span data-ttu-id="94ad2-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-778">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-779">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-780">275.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-780">275.00</span></span></td>
<td><span data-ttu-id="94ad2-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-782">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-782">CC004</span></span></td>
<td><span data-ttu-id="94ad2-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-783">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-784">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-784">10001</span></span></td>
<td><span data-ttu-id="94ad2-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-785">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-786">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-787">50,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-787">50,00</span></span></td>
<td><span data-ttu-id="94ad2-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-789">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-789">CC001</span></span></td>
<td><span data-ttu-id="94ad2-790">Personale</span><span class="sxs-lookup"><span data-stu-id="94ad2-790">HR</span></span></td>
<td><span data-ttu-id="94ad2-791">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-791">10001</span></span></td>
<td><span data-ttu-id="94ad2-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-792">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-793">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="94ad2-794">-1,245.71</span></span></td>
<td><span data-ttu-id="94ad2-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-796">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-796">CC002</span></span></td>
<td><span data-ttu-id="94ad2-797">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-797">Finance</span></span></td>
<td><span data-ttu-id="94ad2-798">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-798">10001</span></span></td>
<td><span data-ttu-id="94ad2-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-799">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-800">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-801">436.00</span><span class="sxs-lookup"><span data-stu-id="94ad2-801">436.00</span></span></td>
<td><span data-ttu-id="94ad2-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-803">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-803">CC003</span></span></td>
<td><span data-ttu-id="94ad2-804">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-804">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-805">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-805">10001</span></span></td>
<td><span data-ttu-id="94ad2-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-806">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-807">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-808">685.14</span><span class="sxs-lookup"><span data-stu-id="94ad2-808">685.14</span></span></td>
<td><span data-ttu-id="94ad2-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-810">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-810">CC004</span></span></td>
<td><span data-ttu-id="94ad2-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-811">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-812">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-812">10001</span></span></td>
<td><span data-ttu-id="94ad2-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-813">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-814">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-815">124.57</span><span class="sxs-lookup"><span data-stu-id="94ad2-815">124.57</span></span></td>
<td><span data-ttu-id="94ad2-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-817">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-817">CC002</span></span></td>
<td><span data-ttu-id="94ad2-818">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-818">Finance</span></span></td>
<td><span data-ttu-id="94ad2-819">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-819">10001</span></span></td>
<td><span data-ttu-id="94ad2-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-820">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-821">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-822">-675.00</span></span></td>
<td><span data-ttu-id="94ad2-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-824">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-824">CC003</span></span></td>
<td><span data-ttu-id="94ad2-825">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-825">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-826">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-826">10001</span></span></td>
<td><span data-ttu-id="94ad2-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-827">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-828">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-829">438.75</span><span class="sxs-lookup"><span data-stu-id="94ad2-829">438.75</span></span></td>
<td><span data-ttu-id="94ad2-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-831">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-831">CC004</span></span></td>
<td><span data-ttu-id="94ad2-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-832">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-833">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-833">10001</span></span></td>
<td><span data-ttu-id="94ad2-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-834">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-835">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-836">236.25</span><span class="sxs-lookup"><span data-stu-id="94ad2-836">236.25</span></span></td>
<td><span data-ttu-id="94ad2-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-838">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-838">CC002</span></span></td>
<td><span data-ttu-id="94ad2-839">Finans</span><span class="sxs-lookup"><span data-stu-id="94ad2-839">Finance</span></span></td>
<td><span data-ttu-id="94ad2-840">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-840">10001</span></span></td>
<td><span data-ttu-id="94ad2-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-841">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-842">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="94ad2-843">-8,150.29</span></span></td>
<td><span data-ttu-id="94ad2-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-845">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-845">CC003</span></span></td>
<td><span data-ttu-id="94ad2-846">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-846">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-847">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-847">10001</span></span></td>
<td><span data-ttu-id="94ad2-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-848">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-849">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="94ad2-850">5,297.69</span></span></td>
<td><span data-ttu-id="94ad2-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-852">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-852">CC004</span></span></td>
<td><span data-ttu-id="94ad2-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="94ad2-853">Packaging</span></span></td>
<td><span data-ttu-id="94ad2-854">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-854">10001</span></span></td>
<td><span data-ttu-id="94ad2-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-855">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-856">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="94ad2-857">2,852.60</span></span></td>
<td><span data-ttu-id="94ad2-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-859">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-859">CC003</span></span></td>
<td><span data-ttu-id="94ad2-860">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-860">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-861">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-861">10001</span></span></td>
<td><span data-ttu-id="94ad2-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-862">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-863">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="94ad2-864">-713.75</span></span></td>
<td><span data-ttu-id="94ad2-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-866">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-867">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-868">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-868">10001</span></span></td>
<td><span data-ttu-id="94ad2-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-869">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-870">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-871">535.31</span><span class="sxs-lookup"><span data-stu-id="94ad2-871">535.31</span></span></td>
<td><span data-ttu-id="94ad2-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-873">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-874">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-875">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-875">10001</span></span></td>
<td><span data-ttu-id="94ad2-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-876">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-877">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-878">178.44</span><span class="sxs-lookup"><span data-stu-id="94ad2-878">178.44</span></span></td>
<td><span data-ttu-id="94ad2-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-880">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-880">CC003</span></span></td>
<td><span data-ttu-id="94ad2-881">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-881">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-882">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-882">10001</span></span></td>
<td><span data-ttu-id="94ad2-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-883">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-884">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="94ad2-885">-5,982.83</span></span></td>
<td><span data-ttu-id="94ad2-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-887">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-888">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-889">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-889">10001</span></span></td>
<td><span data-ttu-id="94ad2-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-890">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-891">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="94ad2-892">4,487.12</span></span></td>
<td><span data-ttu-id="94ad2-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-894">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-895">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-896">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-896">10001</span></span></td>
<td><span data-ttu-id="94ad2-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-897">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-898">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="94ad2-899">1,495.71</span></span></td>
<td><span data-ttu-id="94ad2-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-901">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-901">CC003</span></span></td>
<td><span data-ttu-id="94ad2-902">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-902">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-903">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-903">10001</span></span></td>
<td><span data-ttu-id="94ad2-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-904">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-905">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="94ad2-906">-286.25</span></span></td>
<td><span data-ttu-id="94ad2-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-908">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-909">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-910">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-910">10001</span></span></td>
<td><span data-ttu-id="94ad2-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-911">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-912">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-913">241.05</span><span class="sxs-lookup"><span data-stu-id="94ad2-913">241.05</span></span></td>
<td><span data-ttu-id="94ad2-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-915">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-916">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-917">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-917">10001</span></span></td>
<td><span data-ttu-id="94ad2-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-918">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-919">Fixed cost</span></span></td>
<td><span data-ttu-id="94ad2-920">45.20</span><span class="sxs-lookup"><span data-stu-id="94ad2-920">45.20</span></span></td>
<td><span data-ttu-id="94ad2-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-922">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-922">CC003</span></span></td>
<td><span data-ttu-id="94ad2-923">Samling</span><span class="sxs-lookup"><span data-stu-id="94ad2-923">Assembly</span></span></td>
<td><span data-ttu-id="94ad2-924">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-924">10001</span></span></td>
<td><span data-ttu-id="94ad2-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-925">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-926">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="94ad2-927">-2,977.17</span></span></td>
<td><span data-ttu-id="94ad2-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-929">Prod 1</span></span></td>
<td><span data-ttu-id="94ad2-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-930">Product 1</span></span></td>
<td><span data-ttu-id="94ad2-931">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-931">10001</span></span></td>
<td><span data-ttu-id="94ad2-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-932">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-933">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="94ad2-934">2,507.09</span></span></td>
<td><span data-ttu-id="94ad2-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ad2-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-936">Prod 2</span></span></td>
<td><span data-ttu-id="94ad2-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-937">Product 2</span></span></td>
<td><span data-ttu-id="94ad2-938">10001</span><span class="sxs-lookup"><span data-stu-id="94ad2-938">10001</span></span></td>
<td><span data-ttu-id="94ad2-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="94ad2-939">Electricity</span></span></td>
<td><span data-ttu-id="94ad2-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-940">Variable cost</span></span></td>
<td><span data-ttu-id="94ad2-941">470.08</span><span class="sxs-lookup"><span data-stu-id="94ad2-941">470.08</span></span></td>
<td><span data-ttu-id="94ad2-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="94ad2-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="94ad2-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="94ad2-943">Conclusion</span></span>
<span data-ttu-id="94ad2-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="94ad2-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="94ad2-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="94ad2-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="94ad2-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="94ad2-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="94ad2-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="94ad2-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="94ad2-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="94ad2-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="94ad2-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="94ad2-950">Sum</span><span class="sxs-lookup"><span data-stu-id="94ad2-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="94ad2-951">CC099</span><span class="sxs-lookup"><span data-stu-id="94ad2-951">CC099</span></span></th>
<th><span data-ttu-id="94ad2-952">CC001</span><span class="sxs-lookup"><span data-stu-id="94ad2-952">CC001</span></span></th>
<th><span data-ttu-id="94ad2-953">CC002</span><span class="sxs-lookup"><span data-stu-id="94ad2-953">CC002</span></span></th>
<th><span data-ttu-id="94ad2-954">CC003</span><span class="sxs-lookup"><span data-stu-id="94ad2-954">CC003</span></span></th>
<th><span data-ttu-id="94ad2-955">CC004</span><span class="sxs-lookup"><span data-stu-id="94ad2-955">CC004</span></span></th>
<th><span data-ttu-id="94ad2-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-956">Proj 1</span></span></th>
<th><span data-ttu-id="94ad2-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-957">Proj 2</span></span></th>
<th><span data-ttu-id="94ad2-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="94ad2-958">Prod 1</span></span></th>
<th><span data-ttu-id="94ad2-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="94ad2-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="94ad2-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="94ad2-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="94ad2-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="94ad2-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-971">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="94ad2-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-973">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-974">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-975">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-976">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-977">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-978">776.36</span><span class="sxs-lookup"><span data-stu-id="94ad2-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-979">223.64</span><span class="sxs-lookup"><span data-stu-id="94ad2-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="94ad2-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="94ad2-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-982">000</span><span class="sxs-lookup"><span data-stu-id="94ad2-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-983">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-984">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-985">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-986">0,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-987">30,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-988">10,00</span><span class="sxs-lookup"><span data-stu-id="94ad2-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="94ad2-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="94ad2-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="94ad2-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="94ad2-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="94ad2-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="94ad2-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="94ad2-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="94ad2-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="94ad2-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="94ad2-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="94ad2-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="94ad2-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="94ad2-996">Hvis du vil ha mer informasjon, kan du se [Kostnadsopprulling](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="94ad2-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



