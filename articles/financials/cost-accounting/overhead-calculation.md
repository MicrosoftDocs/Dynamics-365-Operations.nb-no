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
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f56feac74dfe78b740342688a908d001614cffd0
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="c126d-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="c126d-103">Overhead calculation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c126d-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="c126d-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c126d-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="c126d-105">Term definition</span></span>
---------------

<span data-ttu-id="c126d-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="c126d-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c126d-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c126d-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c126d-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="c126d-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c126d-109">Leie</span><span class="sxs-lookup"><span data-stu-id="c126d-109">Rent</span></span>
-   <span data-ttu-id="c126d-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-110">Electricity</span></span>
-   <span data-ttu-id="c126d-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="c126d-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c126d-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="c126d-112">Overhead calculation overview</span></span>
<span data-ttu-id="c126d-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="c126d-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c126d-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="c126d-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c126d-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="c126d-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c126d-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="c126d-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c126d-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="c126d-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c126d-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="c126d-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c126d-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="c126d-119">Version type</span></span>
-   <span data-ttu-id="c126d-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="c126d-120">Date and time</span></span>
-   <span data-ttu-id="c126d-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="c126d-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c126d-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="c126d-122">Fiscal year</span></span>
-   <span data-ttu-id="c126d-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="c126d-123">Fiscal period</span></span>

<span data-ttu-id="c126d-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="c126d-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c126d-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="c126d-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c126d-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c126d-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c126d-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="c126d-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c126d-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="c126d-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c126d-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="c126d-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c126d-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="c126d-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c126d-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c126d-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c126d-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="c126d-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c126d-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="c126d-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c126d-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="c126d-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c126d-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="c126d-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c126d-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="c126d-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c126d-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c126d-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="c126d-140">Main account</span></span></th>
<th><span data-ttu-id="c126d-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="c126d-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c126d-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-143">CC099</span></span></td>
<td><span data-ttu-id="c126d-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-144">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-145">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-145">10001</span></span></td>
<td><span data-ttu-id="c126d-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-146">Electricity</span></span></td>
<td><span data-ttu-id="c126d-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c126d-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c126d-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="c126d-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c126d-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="c126d-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c126d-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c126d-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="c126d-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c126d-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="c126d-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c126d-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="c126d-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c126d-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="c126d-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c126d-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c126d-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="c126d-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c126d-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="c126d-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c126d-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-160">Journal</span></span></th>
<th><span data-ttu-id="c126d-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="c126d-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c126d-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c126d-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c126d-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="c126d-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-164">00001</span><span class="sxs-lookup"><span data-stu-id="c126d-164">00001</span></span></td>
<td><span data-ttu-id="c126d-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c126d-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="c126d-166">Fiscal</span></span></td>
<td><span data-ttu-id="c126d-167">2017</span><span class="sxs-lookup"><span data-stu-id="c126d-167">2017</span></span></td>
<td><span data-ttu-id="c126d-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-168">Period 1</span></span></td>
<td><span data-ttu-id="c126d-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c126d-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="c126d-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-173">Cost element</span></span></th>
<th><span data-ttu-id="c126d-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c126d-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-177">CC099</span></span></td>
<td><span data-ttu-id="c126d-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-178">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-179">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-179">10001</span></span></td>
<td><span data-ttu-id="c126d-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-180">Electricity</span></span></td>
<td><span data-ttu-id="c126d-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="c126d-181">Unclassified</span></span></td>
<td><span data-ttu-id="c126d-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c126d-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c126d-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-185">Cost element</span></span></th>
<th><span data-ttu-id="c126d-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-187">Amount</span></span></th>
<th><span data-ttu-id="c126d-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-189">CC099</span></span></td>
<td><span data-ttu-id="c126d-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-190">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-191">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-191">10001</span></span></td>
<td><span data-ttu-id="c126d-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-192">Electricity</span></span></td>
<td><span data-ttu-id="c126d-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="c126d-193">Unclassified</span></span></td>
<td><span data-ttu-id="c126d-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-194">10,000.00</span></span></td>
<td><span data-ttu-id="c126d-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-196">CC099</span></span></td>
<td><span data-ttu-id="c126d-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-197">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-198">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-198">10001</span></span></td>
<td><span data-ttu-id="c126d-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-199">Electricity</span></span></td>
<td><span data-ttu-id="c126d-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="c126d-200">Unclassified</span></span></td>
<td><span data-ttu-id="c126d-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c126d-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-203">CC099</span></span></td>
<td><span data-ttu-id="c126d-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-204">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-205">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-205">10001</span></span></td>
<td><span data-ttu-id="c126d-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-206">Electricity</span></span></td>
<td><span data-ttu-id="c126d-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-208">1,000.00</span></span></td>
<td><span data-ttu-id="c126d-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-210">CC099</span></span></td>
<td><span data-ttu-id="c126d-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-211">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-212">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-212">10001</span></span></td>
<td><span data-ttu-id="c126d-213">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-213">Electricity</span></span></td>
<td><span data-ttu-id="c126d-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-214">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c126d-215">9,000.00</span></span></td>
<td><span data-ttu-id="c126d-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-217">Hvis du vil ha detaljert informasjon om kostnadsatferd, kan du se Policy for kostnadsatferd.</span><span class="sxs-lookup"><span data-stu-id="c126d-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="c126d-218">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="c126d-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c126d-219">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="c126d-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c126d-220">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c126d-221">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="c126d-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c126d-222">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="c126d-222">Define the cost distribution rule</span></span>

<span data-ttu-id="c126d-223">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="c126d-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c126d-224">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="c126d-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c126d-225">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="c126d-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c126d-226">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="c126d-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c126d-227">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="c126d-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c126d-228">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-229">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-229">Cost object</span></span></th>
<th><span data-ttu-id="c126d-230">kWt</span><span class="sxs-lookup"><span data-stu-id="c126d-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-231">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-231">CC001</span></span></td>
<td><span data-ttu-id="c126d-232">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-232">HR</span></span></td>
<td><span data-ttu-id="c126d-233">1 000</span><span class="sxs-lookup"><span data-stu-id="c126d-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-234">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-234">CC002</span></span></td>
<td><span data-ttu-id="c126d-235">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-235">Finance</span></span></td>
<td><span data-ttu-id="c126d-236">6,000</span><span class="sxs-lookup"><span data-stu-id="c126d-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-237">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-237">CC003</span></span></td>
<td><span data-ttu-id="c126d-238">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-238">Assembly</span></span></td>
<td><span data-ttu-id="c126d-239">0</span><span class="sxs-lookup"><span data-stu-id="c126d-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-240">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="c126d-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-241">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-241">Cost object</span></span></th>
<th><span data-ttu-id="c126d-242">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-242">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-243">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-243">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-244">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-245">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-245">CC001</span></span></td>
<td><span data-ttu-id="c126d-246">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-246">HR</span></span></td>
<td><span data-ttu-id="c126d-247">1 000</span><span class="sxs-lookup"><span data-stu-id="c126d-247">1,000</span></span></td>
<td><span data-ttu-id="c126d-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c126d-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c126d-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-250">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-250">CC002</span></span></td>
<td><span data-ttu-id="c126d-251">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-251">Finance</span></span></td>
<td><span data-ttu-id="c126d-252">6,000</span><span class="sxs-lookup"><span data-stu-id="c126d-252">6,000</span></span></td>
<td><span data-ttu-id="c126d-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c126d-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c126d-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-255">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-255">CC003</span></span></td>
<td><span data-ttu-id="c126d-256">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-256">Assembly</span></span></td>
<td><span data-ttu-id="c126d-257">0</span><span class="sxs-lookup"><span data-stu-id="c126d-257">0</span></span></td>
<td><span data-ttu-id="c126d-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c126d-259">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-260">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="c126d-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c126d-261">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="c126d-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-262">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-262">Cost object</span></span></th>
<th><span data-ttu-id="c126d-263">Formel</span><span class="sxs-lookup"><span data-stu-id="c126d-263">Formula</span></span></th>
<th><span data-ttu-id="c126d-264">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-264">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-265">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-265">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-266">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-267">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-267">CC001</span></span></td>
<td><span data-ttu-id="c126d-268">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-268">HR</span></span></td>
<td><span data-ttu-id="c126d-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c126d-270">1</span><span class="sxs-lookup"><span data-stu-id="c126d-270">1</span></span></td>
<td><span data-ttu-id="c126d-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c126d-272">500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-273">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-273">CC002</span></span></td>
<td><span data-ttu-id="c126d-274">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-274">Finance</span></span></td>
<td><span data-ttu-id="c126d-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c126d-276">1</span><span class="sxs-lookup"><span data-stu-id="c126d-276">1</span></span></td>
<td><span data-ttu-id="c126d-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c126d-278">500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-279">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-279">CC003</span></span></td>
<td><span data-ttu-id="c126d-280">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-280">Assembly</span></span></td>
<td><span data-ttu-id="c126d-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c126d-282">0</span><span class="sxs-lookup"><span data-stu-id="c126d-282">0</span></span></td>
<td><span data-ttu-id="c126d-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c126d-284">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c126d-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-286">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-286">Journal</span></span></th>
<th><span data-ttu-id="c126d-287">Journaltype</span><span class="sxs-lookup"><span data-stu-id="c126d-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c126d-288">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c126d-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c126d-289">Versjon</span><span class="sxs-lookup"><span data-stu-id="c126d-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-290">00002</span><span class="sxs-lookup"><span data-stu-id="c126d-290">00002</span></span></td>
<td><span data-ttu-id="c126d-291">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="c126d-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c126d-292">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="c126d-292">Fiscal</span></span></td>
<td><span data-ttu-id="c126d-293">2017</span><span class="sxs-lookup"><span data-stu-id="c126d-293">2017</span></span></td>
<td><span data-ttu-id="c126d-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-294">Period 1</span></span></td>
<td><span data-ttu-id="c126d-295">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c126d-296">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="c126d-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-297">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-298">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-299">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-299">Cost element</span></span></th>
<th><span data-ttu-id="c126d-300">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-300">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-301">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-302">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-303">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-303">CC099</span></span></td>
<td><span data-ttu-id="c126d-304">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-304">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-305">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-305">10001</span></span></td>
<td><span data-ttu-id="c126d-306">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-306">Electricity</span></span></td>
<td><span data-ttu-id="c126d-307">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-307">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-309">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-310">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-310">CC099</span></span></td>
<td><span data-ttu-id="c126d-311">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-311">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-312">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-312">10001</span></span></td>
<td><span data-ttu-id="c126d-313">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-313">Electricity</span></span></td>
<td><span data-ttu-id="c126d-314">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-314">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c126d-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c126d-316">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c126d-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-317">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-318">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-318">Cost element</span></span></th>
<th><span data-ttu-id="c126d-319">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-319">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-320">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-320">Amount</span></span></th>
<th><span data-ttu-id="c126d-321">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-322">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-322">CC099</span></span></td>
<td><span data-ttu-id="c126d-323">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-323">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-324">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-324">10001</span></span></td>
<td><span data-ttu-id="c126d-325">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-325">Electricity</span></span></td>
<td><span data-ttu-id="c126d-326">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-326">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-327">-1,000.00</span></span></td>
<td><span data-ttu-id="c126d-328">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-329">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-329">CC001</span></span></td>
<td><span data-ttu-id="c126d-330">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-330">HR</span></span></td>
<td><span data-ttu-id="c126d-331">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-331">10001</span></span></td>
<td><span data-ttu-id="c126d-332">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-332">Electricity</span></span></td>
<td><span data-ttu-id="c126d-333">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-333">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-334">500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-334">500.00</span></span></td>
<td><span data-ttu-id="c126d-335">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-336">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-336">CC002</span></span></td>
<td><span data-ttu-id="c126d-337">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-337">Finance</span></span></td>
<td><span data-ttu-id="c126d-338">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-338">10001</span></span></td>
<td><span data-ttu-id="c126d-339">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-339">Electricity</span></span></td>
<td><span data-ttu-id="c126d-340">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-340">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-341">500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-341">500.00</span></span></td>
<td><span data-ttu-id="c126d-342">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-343">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-343">CC099</span></span></td>
<td><span data-ttu-id="c126d-344">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="c126d-344">Default cost center</span></span></td>
<td><span data-ttu-id="c126d-345">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-345">10001</span></span></td>
<td><span data-ttu-id="c126d-346">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-346">Electricity</span></span></td>
<td><span data-ttu-id="c126d-347">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-347">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="c126d-348">-9,000.00</span></span></td>
<td><span data-ttu-id="c126d-349">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-350">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-350">CC001</span></span></td>
<td><span data-ttu-id="c126d-351">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-351">HR</span></span></td>
<td><span data-ttu-id="c126d-352">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-352">10001</span></span></td>
<td><span data-ttu-id="c126d-353">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-353">Electricity</span></span></td>
<td><span data-ttu-id="c126d-354">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-354">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c126d-355">1,285.71</span></span></td>
<td><span data-ttu-id="c126d-356">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-357">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-357">CC002</span></span></td>
<td><span data-ttu-id="c126d-358">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-358">Finance</span></span></td>
<td><span data-ttu-id="c126d-359">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-359">10001</span></span></td>
<td><span data-ttu-id="c126d-360">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-360">Electricity</span></span></td>
<td><span data-ttu-id="c126d-361">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-361">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c126d-362">7,714.29</span></span></td>
<td><span data-ttu-id="c126d-363">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-364">Hvis du vil ha detaljert informasjon om kostnadsdistribusjon og tildelingsgrunnlag, kan du se Kostnadsdistribusjonspolicy og Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="c126d-365">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="c126d-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c126d-366">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="c126d-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c126d-367">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="c126d-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c126d-368">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="c126d-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c126d-369">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="c126d-369">Define the overhead rate</span></span>

<span data-ttu-id="c126d-370">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c126d-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c126d-371">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="c126d-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-372">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-372">Cost object</span></span></th>
<th><span data-ttu-id="c126d-373">Timeantall</span><span class="sxs-lookup"><span data-stu-id="c126d-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-374">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-374">Proj 1</span></span></td>
<td><span data-ttu-id="c126d-375">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-375">Project 1</span></span></td>
<td><span data-ttu-id="c126d-376">3</span><span class="sxs-lookup"><span data-stu-id="c126d-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-377">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-377">Proj 2</span></span></td>
<td><span data-ttu-id="c126d-378">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-378">Project 2</span></span></td>
<td><span data-ttu-id="c126d-379">1</span><span class="sxs-lookup"><span data-stu-id="c126d-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-380">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="c126d-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-381">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-381">Cost object</span></span></th>
<th><span data-ttu-id="c126d-382">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-382">Cost element</span></span></th>
<th><span data-ttu-id="c126d-383">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-383">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-384">Enheter</span><span class="sxs-lookup"><span data-stu-id="c126d-384">Units</span></span></th>
<th><span data-ttu-id="c126d-385">Sats</span><span class="sxs-lookup"><span data-stu-id="c126d-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-386">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-386">CC001</span></span></td>
<td><span data-ttu-id="c126d-387">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-387">HR</span></span></td>
<td><span data-ttu-id="c126d-388">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-388">10001</span></span></td>
<td><span data-ttu-id="c126d-389">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-389">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-390">1</span><span class="sxs-lookup"><span data-stu-id="c126d-390">1</span></span></td>
<td><span data-ttu-id="c126d-391">10</span><span class="sxs-lookup"><span data-stu-id="c126d-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-392">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-393">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-393">Cost object</span></span></th>
<th><span data-ttu-id="c126d-394">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-394">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-395">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-395">Cost element</span></span></th>
<th><span data-ttu-id="c126d-396">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-396">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-397">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-398">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-398">Proj 1</span></span></td>
<td><span data-ttu-id="c126d-399">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-399">Project 1</span></span></td>
<td><span data-ttu-id="c126d-400">3</span><span class="sxs-lookup"><span data-stu-id="c126d-400">3</span></span></td>
<td><span data-ttu-id="c126d-401">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-401">10001</span></span></td>
<td><span data-ttu-id="c126d-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c126d-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c126d-403">30,00</span><span class="sxs-lookup"><span data-stu-id="c126d-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-404">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-404">Proj 2</span></span></td>
<td><span data-ttu-id="c126d-405">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-405">Project 2</span></span></td>
<td><span data-ttu-id="c126d-406">1</span><span class="sxs-lookup"><span data-stu-id="c126d-406">1</span></span></td>
<td><span data-ttu-id="c126d-407">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-407">10001</span></span></td>
<td><span data-ttu-id="c126d-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c126d-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c126d-409">10,00</span><span class="sxs-lookup"><span data-stu-id="c126d-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c126d-410">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-411">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-411">Journal</span></span></th>
<th><span data-ttu-id="c126d-412">Journaltype</span><span class="sxs-lookup"><span data-stu-id="c126d-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c126d-413">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c126d-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c126d-414">Versjon</span><span class="sxs-lookup"><span data-stu-id="c126d-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-415">00003</span><span class="sxs-lookup"><span data-stu-id="c126d-415">00003</span></span></td>
<td><span data-ttu-id="c126d-416">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="c126d-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c126d-417">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="c126d-417">Fiscal</span></span></td>
<td><span data-ttu-id="c126d-418">2017</span><span class="sxs-lookup"><span data-stu-id="c126d-418">2017</span></span></td>
<td><span data-ttu-id="c126d-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-419">Period 1</span></span></td>
<td><span data-ttu-id="c126d-420">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c126d-421">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="c126d-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-422">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-423">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-423">Cost object</span></span></th>
<th><span data-ttu-id="c126d-424">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-425">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-426">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-426">Proj 1</span></span></td>
<td><span data-ttu-id="c126d-427">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c126d-428">3,00</span><span class="sxs-lookup"><span data-stu-id="c126d-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-429">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-430">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-430">Proj 2</span></span></td>
<td><span data-ttu-id="c126d-431">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c126d-432">1,00</span><span class="sxs-lookup"><span data-stu-id="c126d-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c126d-433">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c126d-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-434">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-435">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-435">Cost element</span></span></th>
<th><span data-ttu-id="c126d-436">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-436">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-437">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-437">Amount</span></span></th>
<th><span data-ttu-id="c126d-438">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="c126d-439">CC0001</span></span></td>
<td><span data-ttu-id="c126d-440">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-440">HR</span></span></td>
<td><span data-ttu-id="c126d-441">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-441">10001</span></span></td>
<td><span data-ttu-id="c126d-442">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-442">Electricity</span></span></td>
<td><span data-ttu-id="c126d-443">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-443">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="c126d-444">-30.00</span></span></td>
<td><span data-ttu-id="c126d-445">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-446">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-446">Proj 1</span></span></td>
<td><span data-ttu-id="c126d-447">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c126d-448">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-448">10001</span></span></td>
<td><span data-ttu-id="c126d-449">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-449">Electricity</span></span></td>
<td><span data-ttu-id="c126d-450">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-450">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-451">30,00</span><span class="sxs-lookup"><span data-stu-id="c126d-451">30.00</span></span></td>
<td><span data-ttu-id="c126d-452">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-453">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-453">CC001</span></span></td>
<td><span data-ttu-id="c126d-454">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-454">HR</span></span></td>
<td><span data-ttu-id="c126d-455">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-455">10001</span></span></td>
<td><span data-ttu-id="c126d-456">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-456">Electricity</span></span></td>
<td><span data-ttu-id="c126d-457">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-457">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="c126d-458">-10.00</span></span></td>
<td><span data-ttu-id="c126d-459">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-460">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-460">Proj 2</span></span></td>
<td><span data-ttu-id="c126d-461">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c126d-462">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-462">10001</span></span></td>
<td><span data-ttu-id="c126d-463">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-463">Electricity</span></span></td>
<td><span data-ttu-id="c126d-464">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-464">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-465">10,00</span><span class="sxs-lookup"><span data-stu-id="c126d-465">10.00</span></span></td>
<td><span data-ttu-id="c126d-466">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-467">Hvis du vil ha mer informasjon om policyen for sats for indirekte kostnader, kan du se Policy for sats for indirekte kostnader og Tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="c126d-468">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="c126d-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c126d-469">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="c126d-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c126d-470">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c126d-471">Finance and Operations støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="c126d-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c126d-472">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="c126d-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c126d-473">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="c126d-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c126d-474">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c126d-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c126d-475">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="c126d-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c126d-476">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="c126d-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c126d-477">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c126d-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c126d-478">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="c126d-478">Define the cost allocation</span></span>

<span data-ttu-id="c126d-479">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="c126d-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c126d-480">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="c126d-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c126d-481">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="c126d-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-482">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-482">Cost object</span></span></th>
<th><span data-ttu-id="c126d-483">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="c126d-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-484">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-484">CC002</span></span></td>
<td><span data-ttu-id="c126d-485">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-485">Finance</span></span></td>
<td><span data-ttu-id="c126d-486">35</span><span class="sxs-lookup"><span data-stu-id="c126d-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-487">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-487">CC003</span></span></td>
<td><span data-ttu-id="c126d-488">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-488">Assembly</span></span></td>
<td><span data-ttu-id="c126d-489">55</span><span class="sxs-lookup"><span data-stu-id="c126d-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-490">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-490">CC004</span></span></td>
<td><span data-ttu-id="c126d-491">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-491">Packaging</span></span></td>
<td><span data-ttu-id="c126d-492">10</span><span class="sxs-lookup"><span data-stu-id="c126d-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-493">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="c126d-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c126d-494">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="c126d-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-495">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-495">Cost object</span></span></th>
<th><span data-ttu-id="c126d-496">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="c126d-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-497">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-497">CC003</span></span></td>
<td><span data-ttu-id="c126d-498">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-498">Assembly</span></span></td>
<td><span data-ttu-id="c126d-499">65</span><span class="sxs-lookup"><span data-stu-id="c126d-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-500">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-500">CC004</span></span></td>
<td><span data-ttu-id="c126d-501">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-501">Packaging</span></span></td>
<td><span data-ttu-id="c126d-502">35</span><span class="sxs-lookup"><span data-stu-id="c126d-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-503">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="c126d-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c126d-504">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="c126d-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-505">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-505">Cost object</span></span></th>
<th><span data-ttu-id="c126d-506">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="c126d-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-507">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-508">Product 1</span></span></td>
<td><span data-ttu-id="c126d-509">60</span><span class="sxs-lookup"><span data-stu-id="c126d-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-510">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-511">Product 2</span></span></td>
<td><span data-ttu-id="c126d-512">20</span><span class="sxs-lookup"><span data-stu-id="c126d-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-513">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="c126d-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c126d-514">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="c126d-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-515">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-515">Cost object</span></span></th>
<th><span data-ttu-id="c126d-516">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="c126d-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-517">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-517">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-518">Product 1</span></span></td>
<td><span data-ttu-id="c126d-519">80</span><span class="sxs-lookup"><span data-stu-id="c126d-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-520">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-521">Product 2</span></span></td>
<td><span data-ttu-id="c126d-522">15</span><span class="sxs-lookup"><span data-stu-id="c126d-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-523">**Obs!** I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="c126d-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c126d-524">Hvis du vil ha mer informasjon om statistiske målleverandører, kan du se Maler for leverandør av statistisk måling.</span><span class="sxs-lookup"><span data-stu-id="c126d-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="c126d-525">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.) Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="c126d-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-526">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-526">Cost object</span></span></th>
<th><span data-ttu-id="c126d-527">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-527">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-528">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-528">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-529">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-529">Amount</span></span></th>
<th><span data-ttu-id="c126d-530">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-531">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-531">CC002</span></span></td>
<td><span data-ttu-id="c126d-532">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-532">Finance</span></span></td>
<td><span data-ttu-id="c126d-533">35</span><span class="sxs-lookup"><span data-stu-id="c126d-533">35</span></span></td>
<td><span data-ttu-id="c126d-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c126d-535">175.00</span><span class="sxs-lookup"><span data-stu-id="c126d-535">175.00</span></span></td>
<td><span data-ttu-id="c126d-536">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-537">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-537">CC003</span></span></td>
<td><span data-ttu-id="c126d-538">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-538">Assembly</span></span></td>
<td><span data-ttu-id="c126d-539">55</span><span class="sxs-lookup"><span data-stu-id="c126d-539">55</span></span></td>
<td><span data-ttu-id="c126d-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c126d-541">275.00</span><span class="sxs-lookup"><span data-stu-id="c126d-541">275.00</span></span></td>
<td><span data-ttu-id="c126d-542">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-543">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-543">CC004</span></span></td>
<td><span data-ttu-id="c126d-544">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-544">Packaging</span></span></td>
<td><span data-ttu-id="c126d-545">10</span><span class="sxs-lookup"><span data-stu-id="c126d-545">10</span></span></td>
<td><span data-ttu-id="c126d-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c126d-547">50,00</span><span class="sxs-lookup"><span data-stu-id="c126d-547">50.00</span></span></td>
<td><span data-ttu-id="c126d-548">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-549">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-549">CC002</span></span></td>
<td><span data-ttu-id="c126d-550">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-550">Finance</span></span></td>
<td><span data-ttu-id="c126d-551">35</span><span class="sxs-lookup"><span data-stu-id="c126d-551">35</span></span></td>
<td><span data-ttu-id="c126d-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="c126d-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c126d-553">436.00</span><span class="sxs-lookup"><span data-stu-id="c126d-553">436.00</span></span></td>
<td><span data-ttu-id="c126d-554">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-555">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-555">CC003</span></span></td>
<td><span data-ttu-id="c126d-556">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-556">Assembly</span></span></td>
<td><span data-ttu-id="c126d-557">55</span><span class="sxs-lookup"><span data-stu-id="c126d-557">55</span></span></td>
<td><span data-ttu-id="c126d-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="c126d-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c126d-559">685.14</span><span class="sxs-lookup"><span data-stu-id="c126d-559">685.14</span></span></td>
<td><span data-ttu-id="c126d-560">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-561">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-561">CC004</span></span></td>
<td><span data-ttu-id="c126d-562">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-562">Packaging</span></span></td>
<td><span data-ttu-id="c126d-563">10</span><span class="sxs-lookup"><span data-stu-id="c126d-563">10</span></span></td>
<td><span data-ttu-id="c126d-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="c126d-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c126d-565">124.57</span><span class="sxs-lookup"><span data-stu-id="c126d-565">124.57</span></span></td>
<td><span data-ttu-id="c126d-566">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-567">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="c126d-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-568">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-568">Cost object</span></span></th>
<th><span data-ttu-id="c126d-569">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-569">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-570">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-570">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-571">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-571">Amount</span></span></th>
<th><span data-ttu-id="c126d-572">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-573">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-573">CC003</span></span></td>
<td><span data-ttu-id="c126d-574">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-574">Assembly</span></span></td>
<td><span data-ttu-id="c126d-575">65</span><span class="sxs-lookup"><span data-stu-id="c126d-575">65</span></span></td>
<td><span data-ttu-id="c126d-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c126d-577">438.75</span><span class="sxs-lookup"><span data-stu-id="c126d-577">438.75</span></span></td>
<td><span data-ttu-id="c126d-578">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-579">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-579">CC004</span></span></td>
<td><span data-ttu-id="c126d-580">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-580">Packaging</span></span></td>
<td><span data-ttu-id="c126d-581">35</span><span class="sxs-lookup"><span data-stu-id="c126d-581">35</span></span></td>
<td><span data-ttu-id="c126d-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c126d-583">236.25</span><span class="sxs-lookup"><span data-stu-id="c126d-583">236.25</span></span></td>
<td><span data-ttu-id="c126d-584">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-585">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-585">CC003</span></span></td>
<td><span data-ttu-id="c126d-586">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-586">Assembly</span></span></td>
<td><span data-ttu-id="c126d-587">65</span><span class="sxs-lookup"><span data-stu-id="c126d-587">65</span></span></td>
<td><span data-ttu-id="c126d-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c126d-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c126d-589">5,297.69</span></span></td>
<td><span data-ttu-id="c126d-590">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-591">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-591">CC004</span></span></td>
<td><span data-ttu-id="c126d-592">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-592">Packaging</span></span></td>
<td><span data-ttu-id="c126d-593">35</span><span class="sxs-lookup"><span data-stu-id="c126d-593">35</span></span></td>
<td><span data-ttu-id="c126d-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c126d-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c126d-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c126d-595">2,852.60</span></span></td>
<td><span data-ttu-id="c126d-596">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-597">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="c126d-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-598">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-598">Cost object</span></span></th>
<th><span data-ttu-id="c126d-599">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-599">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-600">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-600">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-601">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-601">Amount</span></span></th>
<th><span data-ttu-id="c126d-602">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-603">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-604">Product 1</span></span></td>
<td><span data-ttu-id="c126d-605">60</span><span class="sxs-lookup"><span data-stu-id="c126d-605">60</span></span></td>
<td><span data-ttu-id="c126d-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c126d-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c126d-607">535.31</span><span class="sxs-lookup"><span data-stu-id="c126d-607">535.31</span></span></td>
<td><span data-ttu-id="c126d-608">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-609">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-610">Product 2</span></span></td>
<td><span data-ttu-id="c126d-611">20</span><span class="sxs-lookup"><span data-stu-id="c126d-611">20</span></span></td>
<td><span data-ttu-id="c126d-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c126d-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c126d-613">178.44</span><span class="sxs-lookup"><span data-stu-id="c126d-613">178.44</span></span></td>
<td><span data-ttu-id="c126d-614">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-615">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-616">Product 1</span></span></td>
<td><span data-ttu-id="c126d-617">60</span><span class="sxs-lookup"><span data-stu-id="c126d-617">60</span></span></td>
<td><span data-ttu-id="c126d-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c126d-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c126d-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c126d-619">4,487.12</span></span></td>
<td><span data-ttu-id="c126d-620">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-621">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-622">Product 2</span></span></td>
<td><span data-ttu-id="c126d-623">20</span><span class="sxs-lookup"><span data-stu-id="c126d-623">20</span></span></td>
<td><span data-ttu-id="c126d-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c126d-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c126d-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c126d-625">1,495.71</span></span></td>
<td><span data-ttu-id="c126d-626">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c126d-627">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="c126d-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-628">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-628">Cost object</span></span></th>
<th><span data-ttu-id="c126d-629">Størrelse</span><span class="sxs-lookup"><span data-stu-id="c126d-629">Magnitude</span></span></th>
<th><span data-ttu-id="c126d-630">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="c126d-630">Allocation factor</span></span></th>
<th><span data-ttu-id="c126d-631">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-631">Amount</span></span></th>
<th><span data-ttu-id="c126d-632">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-633">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-634">Product 1</span></span></td>
<td><span data-ttu-id="c126d-635">80</span><span class="sxs-lookup"><span data-stu-id="c126d-635">80</span></span></td>
<td><span data-ttu-id="c126d-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c126d-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c126d-637">241.05</span><span class="sxs-lookup"><span data-stu-id="c126d-637">241.05</span></span></td>
<td><span data-ttu-id="c126d-638">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-639">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-640">Product 2</span></span></td>
<td><span data-ttu-id="c126d-641">15</span><span class="sxs-lookup"><span data-stu-id="c126d-641">15</span></span></td>
<td><span data-ttu-id="c126d-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c126d-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c126d-643">45.20</span><span class="sxs-lookup"><span data-stu-id="c126d-643">45.20</span></span></td>
<td><span data-ttu-id="c126d-644">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-645">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-646">Product 1</span></span></td>
<td><span data-ttu-id="c126d-647">80</span><span class="sxs-lookup"><span data-stu-id="c126d-647">80</span></span></td>
<td><span data-ttu-id="c126d-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c126d-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c126d-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c126d-649">2,507.09</span></span></td>
<td><span data-ttu-id="c126d-650">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-651">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-652">Product 2</span></span></td>
<td><span data-ttu-id="c126d-653">15</span><span class="sxs-lookup"><span data-stu-id="c126d-653">15</span></span></td>
<td><span data-ttu-id="c126d-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c126d-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c126d-655">470.08</span><span class="sxs-lookup"><span data-stu-id="c126d-655">470.08</span></span></td>
<td><span data-ttu-id="c126d-656">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c126d-657">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="c126d-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-658">Journalen</span><span class="sxs-lookup"><span data-stu-id="c126d-658">Journal</span></span></th>
<th><span data-ttu-id="c126d-659">Journaltype</span><span class="sxs-lookup"><span data-stu-id="c126d-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c126d-660">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="c126d-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c126d-661">Versjon</span><span class="sxs-lookup"><span data-stu-id="c126d-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-662">00004</span><span class="sxs-lookup"><span data-stu-id="c126d-662">00004</span></span></td>
<td><span data-ttu-id="c126d-663">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="c126d-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c126d-664">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="c126d-664">Fiscal</span></span></td>
<td><span data-ttu-id="c126d-665">2017</span><span class="sxs-lookup"><span data-stu-id="c126d-665">2017</span></span></td>
<td><span data-ttu-id="c126d-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-666">Period 1</span></span></td>
<td><span data-ttu-id="c126d-667">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="c126d-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c126d-668">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="c126d-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c126d-669">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-670">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-671">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-671">Cost element</span></span></th>
<th><span data-ttu-id="c126d-672">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-672">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-673">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-674">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-675">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-675">CC001</span></span></td>
<td><span data-ttu-id="c126d-676">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-676">HR</span></span></td>
<td><span data-ttu-id="c126d-677">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-677">10001</span></span></td>
<td><span data-ttu-id="c126d-678">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-678">Electricity</span></span></td>
<td><span data-ttu-id="c126d-679">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-679">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-680">500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-681">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-682">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-682">CC001</span></span></td>
<td><span data-ttu-id="c126d-683">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-683">HR</span></span></td>
<td><span data-ttu-id="c126d-684">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-684">10001</span></span></td>
<td><span data-ttu-id="c126d-685">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-685">Electricity</span></span></td>
<td><span data-ttu-id="c126d-686">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-686">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c126d-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-688">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-689">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-689">CC002</span></span></td>
<td><span data-ttu-id="c126d-690">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-690">Finance</span></span></td>
<td><span data-ttu-id="c126d-691">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-691">10001</span></span></td>
<td><span data-ttu-id="c126d-692">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-692">Electricity</span></span></td>
<td><span data-ttu-id="c126d-693">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-693">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-694">675.00</span><span class="sxs-lookup"><span data-stu-id="c126d-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-695">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-696">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-696">CC002</span></span></td>
<td><span data-ttu-id="c126d-697">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-697">Finance</span></span></td>
<td><span data-ttu-id="c126d-698">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-698">10001</span></span></td>
<td><span data-ttu-id="c126d-699">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-699">Electricity</span></span></td>
<td><span data-ttu-id="c126d-700">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-700">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c126d-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-702">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-703">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-703">CC003</span></span></td>
<td><span data-ttu-id="c126d-704">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-704">Assembly</span></span></td>
<td><span data-ttu-id="c126d-705">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-705">10001</span></span></td>
<td><span data-ttu-id="c126d-706">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-706">Electricity</span></span></td>
<td><span data-ttu-id="c126d-707">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-707">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-708">713.75</span><span class="sxs-lookup"><span data-stu-id="c126d-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-709">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-710">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-710">CC003</span></span></td>
<td><span data-ttu-id="c126d-711">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-711">Assembly</span></span></td>
<td><span data-ttu-id="c126d-712">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-712">10001</span></span></td>
<td><span data-ttu-id="c126d-713">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-713">Electricity</span></span></td>
<td><span data-ttu-id="c126d-714">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-714">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c126d-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-716">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-717">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-717">CC003</span></span></td>
<td><span data-ttu-id="c126d-718">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-718">Packaging</span></span></td>
<td><span data-ttu-id="c126d-719">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-719">10001</span></span></td>
<td><span data-ttu-id="c126d-720">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-720">Electricity</span></span></td>
<td><span data-ttu-id="c126d-721">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-721">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-722">286.25</span><span class="sxs-lookup"><span data-stu-id="c126d-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-723">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-724">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-724">CC003</span></span></td>
<td><span data-ttu-id="c126d-725">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-725">Packaging</span></span></td>
<td><span data-ttu-id="c126d-726">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-726">10001</span></span></td>
<td><span data-ttu-id="c126d-727">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-727">Electricity</span></span></td>
<td><span data-ttu-id="c126d-728">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-728">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c126d-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-730">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-731">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-732">Product 1</span></span></td>
<td><span data-ttu-id="c126d-733">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-733">10001</span></span></td>
<td><span data-ttu-id="c126d-734">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-734">Electricity</span></span></td>
<td><span data-ttu-id="c126d-735">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-735">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-736">776.36</span><span class="sxs-lookup"><span data-stu-id="c126d-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-737">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-738">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-739">Product 1</span></span></td>
<td><span data-ttu-id="c126d-740">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-740">10001</span></span></td>
<td><span data-ttu-id="c126d-741">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-741">Electricity</span></span></td>
<td><span data-ttu-id="c126d-742">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-742">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c126d-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-744">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-745">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-746">Product 1</span></span></td>
<td><span data-ttu-id="c126d-747">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-747">10001</span></span></td>
<td><span data-ttu-id="c126d-748">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-748">Electricity</span></span></td>
<td><span data-ttu-id="c126d-749">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-749">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-750">223.64</span><span class="sxs-lookup"><span data-stu-id="c126d-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-751">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="c126d-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-752">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-753">Product 1</span></span></td>
<td><span data-ttu-id="c126d-754">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-754">10001</span></span></td>
<td><span data-ttu-id="c126d-755">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-755">Electricity</span></span></td>
<td><span data-ttu-id="c126d-756">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-756">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c126d-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c126d-758">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c126d-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c126d-759">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c126d-760">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-760">Cost element</span></span></th>
<th><span data-ttu-id="c126d-761">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="c126d-761">Cost behavior</span></span></th>
<th><span data-ttu-id="c126d-762">Beløp</span><span class="sxs-lookup"><span data-stu-id="c126d-762">Amount</span></span></th>
<th><span data-ttu-id="c126d-763">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="c126d-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c126d-764">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-764">CC001</span></span></td>
<td><span data-ttu-id="c126d-765">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-765">HR</span></span></td>
<td><span data-ttu-id="c126d-766">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-766">10001</span></span></td>
<td><span data-ttu-id="c126d-767">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-767">Electricity</span></span></td>
<td><span data-ttu-id="c126d-768">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-768">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="c126d-769">-500.00</span></span></td>
<td><span data-ttu-id="c126d-770">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-771">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-771">CC002</span></span></td>
<td><span data-ttu-id="c126d-772">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-772">Finance</span></span></td>
<td><span data-ttu-id="c126d-773">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-773">10001</span></span></td>
<td><span data-ttu-id="c126d-774">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-774">Electricity</span></span></td>
<td><span data-ttu-id="c126d-775">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-775">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-776">175.00</span><span class="sxs-lookup"><span data-stu-id="c126d-776">175.00</span></span></td>
<td><span data-ttu-id="c126d-777">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-778">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-778">CC003</span></span></td>
<td><span data-ttu-id="c126d-779">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-779">Assembly</span></span></td>
<td><span data-ttu-id="c126d-780">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-780">10001</span></span></td>
<td><span data-ttu-id="c126d-781">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-781">Electricity</span></span></td>
<td><span data-ttu-id="c126d-782">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-782">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-783">275.00</span><span class="sxs-lookup"><span data-stu-id="c126d-783">275.00</span></span></td>
<td><span data-ttu-id="c126d-784">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-785">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-785">CC004</span></span></td>
<td><span data-ttu-id="c126d-786">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-786">Packaging</span></span></td>
<td><span data-ttu-id="c126d-787">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-787">10001</span></span></td>
<td><span data-ttu-id="c126d-788">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-788">Electricity</span></span></td>
<td><span data-ttu-id="c126d-789">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-789">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-790">50,00</span><span class="sxs-lookup"><span data-stu-id="c126d-790">50,00</span></span></td>
<td><span data-ttu-id="c126d-791">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-792">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-792">CC001</span></span></td>
<td><span data-ttu-id="c126d-793">Personale</span><span class="sxs-lookup"><span data-stu-id="c126d-793">HR</span></span></td>
<td><span data-ttu-id="c126d-794">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-794">10001</span></span></td>
<td><span data-ttu-id="c126d-795">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-795">Electricity</span></span></td>
<td><span data-ttu-id="c126d-796">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-796">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="c126d-797">-1,245.71</span></span></td>
<td><span data-ttu-id="c126d-798">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-799">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-799">CC002</span></span></td>
<td><span data-ttu-id="c126d-800">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-800">Finance</span></span></td>
<td><span data-ttu-id="c126d-801">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-801">10001</span></span></td>
<td><span data-ttu-id="c126d-802">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-802">Electricity</span></span></td>
<td><span data-ttu-id="c126d-803">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-803">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-804">436.00</span><span class="sxs-lookup"><span data-stu-id="c126d-804">436.00</span></span></td>
<td><span data-ttu-id="c126d-805">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-806">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-806">CC003</span></span></td>
<td><span data-ttu-id="c126d-807">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-807">Assembly</span></span></td>
<td><span data-ttu-id="c126d-808">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-808">10001</span></span></td>
<td><span data-ttu-id="c126d-809">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-809">Electricity</span></span></td>
<td><span data-ttu-id="c126d-810">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-810">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-811">685.14</span><span class="sxs-lookup"><span data-stu-id="c126d-811">685.14</span></span></td>
<td><span data-ttu-id="c126d-812">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-813">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-813">CC004</span></span></td>
<td><span data-ttu-id="c126d-814">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-814">Packaging</span></span></td>
<td><span data-ttu-id="c126d-815">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-815">10001</span></span></td>
<td><span data-ttu-id="c126d-816">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-816">Electricity</span></span></td>
<td><span data-ttu-id="c126d-817">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-817">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-818">124.57</span><span class="sxs-lookup"><span data-stu-id="c126d-818">124.57</span></span></td>
<td><span data-ttu-id="c126d-819">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-820">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-820">CC002</span></span></td>
<td><span data-ttu-id="c126d-821">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-821">Finance</span></span></td>
<td><span data-ttu-id="c126d-822">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-822">10001</span></span></td>
<td><span data-ttu-id="c126d-823">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-823">Electricity</span></span></td>
<td><span data-ttu-id="c126d-824">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-824">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="c126d-825">-675.00</span></span></td>
<td><span data-ttu-id="c126d-826">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-827">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-827">CC003</span></span></td>
<td><span data-ttu-id="c126d-828">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-828">Assembly</span></span></td>
<td><span data-ttu-id="c126d-829">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-829">10001</span></span></td>
<td><span data-ttu-id="c126d-830">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-830">Electricity</span></span></td>
<td><span data-ttu-id="c126d-831">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-831">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-832">438.75</span><span class="sxs-lookup"><span data-stu-id="c126d-832">438.75</span></span></td>
<td><span data-ttu-id="c126d-833">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-834">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-834">CC004</span></span></td>
<td><span data-ttu-id="c126d-835">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-835">Packaging</span></span></td>
<td><span data-ttu-id="c126d-836">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-836">10001</span></span></td>
<td><span data-ttu-id="c126d-837">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-837">Electricity</span></span></td>
<td><span data-ttu-id="c126d-838">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-838">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-839">236.25</span><span class="sxs-lookup"><span data-stu-id="c126d-839">236.25</span></span></td>
<td><span data-ttu-id="c126d-840">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-841">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-841">CC002</span></span></td>
<td><span data-ttu-id="c126d-842">Finans</span><span class="sxs-lookup"><span data-stu-id="c126d-842">Finance</span></span></td>
<td><span data-ttu-id="c126d-843">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-843">10001</span></span></td>
<td><span data-ttu-id="c126d-844">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-844">Electricity</span></span></td>
<td><span data-ttu-id="c126d-845">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-845">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="c126d-846">-8,150.29</span></span></td>
<td><span data-ttu-id="c126d-847">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-848">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-848">CC003</span></span></td>
<td><span data-ttu-id="c126d-849">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-849">Assembly</span></span></td>
<td><span data-ttu-id="c126d-850">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-850">10001</span></span></td>
<td><span data-ttu-id="c126d-851">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-851">Electricity</span></span></td>
<td><span data-ttu-id="c126d-852">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-852">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c126d-853">5,297.69</span></span></td>
<td><span data-ttu-id="c126d-854">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-855">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-855">CC004</span></span></td>
<td><span data-ttu-id="c126d-856">Innpakning</span><span class="sxs-lookup"><span data-stu-id="c126d-856">Packaging</span></span></td>
<td><span data-ttu-id="c126d-857">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-857">10001</span></span></td>
<td><span data-ttu-id="c126d-858">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-858">Electricity</span></span></td>
<td><span data-ttu-id="c126d-859">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-859">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c126d-860">2,852.60</span></span></td>
<td><span data-ttu-id="c126d-861">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-862">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-862">CC003</span></span></td>
<td><span data-ttu-id="c126d-863">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-863">Assembly</span></span></td>
<td><span data-ttu-id="c126d-864">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-864">10001</span></span></td>
<td><span data-ttu-id="c126d-865">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-865">Electricity</span></span></td>
<td><span data-ttu-id="c126d-866">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-866">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="c126d-867">-713.75</span></span></td>
<td><span data-ttu-id="c126d-868">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-869">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-870">Product 1</span></span></td>
<td><span data-ttu-id="c126d-871">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-871">10001</span></span></td>
<td><span data-ttu-id="c126d-872">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-872">Electricity</span></span></td>
<td><span data-ttu-id="c126d-873">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-873">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-874">535.31</span><span class="sxs-lookup"><span data-stu-id="c126d-874">535.31</span></span></td>
<td><span data-ttu-id="c126d-875">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-876">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-877">Product 2</span></span></td>
<td><span data-ttu-id="c126d-878">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-878">10001</span></span></td>
<td><span data-ttu-id="c126d-879">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-879">Electricity</span></span></td>
<td><span data-ttu-id="c126d-880">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-880">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-881">178.44</span><span class="sxs-lookup"><span data-stu-id="c126d-881">178.44</span></span></td>
<td><span data-ttu-id="c126d-882">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-883">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-883">CC003</span></span></td>
<td><span data-ttu-id="c126d-884">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-884">Assembly</span></span></td>
<td><span data-ttu-id="c126d-885">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-885">10001</span></span></td>
<td><span data-ttu-id="c126d-886">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-886">Electricity</span></span></td>
<td><span data-ttu-id="c126d-887">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-887">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="c126d-888">-5,982.83</span></span></td>
<td><span data-ttu-id="c126d-889">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-890">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-891">Product 1</span></span></td>
<td><span data-ttu-id="c126d-892">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-892">10001</span></span></td>
<td><span data-ttu-id="c126d-893">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-893">Electricity</span></span></td>
<td><span data-ttu-id="c126d-894">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-894">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c126d-895">4,487.12</span></span></td>
<td><span data-ttu-id="c126d-896">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-897">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-898">Product 2</span></span></td>
<td><span data-ttu-id="c126d-899">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-899">10001</span></span></td>
<td><span data-ttu-id="c126d-900">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-900">Electricity</span></span></td>
<td><span data-ttu-id="c126d-901">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-901">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c126d-902">1,495.71</span></span></td>
<td><span data-ttu-id="c126d-903">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-904">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-904">CC003</span></span></td>
<td><span data-ttu-id="c126d-905">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-905">Assembly</span></span></td>
<td><span data-ttu-id="c126d-906">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-906">10001</span></span></td>
<td><span data-ttu-id="c126d-907">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-907">Electricity</span></span></td>
<td><span data-ttu-id="c126d-908">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-908">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="c126d-909">-286.25</span></span></td>
<td><span data-ttu-id="c126d-910">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-911">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-912">Product 1</span></span></td>
<td><span data-ttu-id="c126d-913">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-913">10001</span></span></td>
<td><span data-ttu-id="c126d-914">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-914">Electricity</span></span></td>
<td><span data-ttu-id="c126d-915">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-915">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-916">241.05</span><span class="sxs-lookup"><span data-stu-id="c126d-916">241.05</span></span></td>
<td><span data-ttu-id="c126d-917">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-918">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-919">Product 2</span></span></td>
<td><span data-ttu-id="c126d-920">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-920">10001</span></span></td>
<td><span data-ttu-id="c126d-921">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-921">Electricity</span></span></td>
<td><span data-ttu-id="c126d-922">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-922">Fixed cost</span></span></td>
<td><span data-ttu-id="c126d-923">45.20</span><span class="sxs-lookup"><span data-stu-id="c126d-923">45.20</span></span></td>
<td><span data-ttu-id="c126d-924">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-925">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-925">CC003</span></span></td>
<td><span data-ttu-id="c126d-926">Samling</span><span class="sxs-lookup"><span data-stu-id="c126d-926">Assembly</span></span></td>
<td><span data-ttu-id="c126d-927">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-927">10001</span></span></td>
<td><span data-ttu-id="c126d-928">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-928">Electricity</span></span></td>
<td><span data-ttu-id="c126d-929">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-929">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-930">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="c126d-930">-2,977.17</span></span></td>
<td><span data-ttu-id="c126d-931">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-932">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-932">Prod 1</span></span></td>
<td><span data-ttu-id="c126d-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="c126d-933">Product 1</span></span></td>
<td><span data-ttu-id="c126d-934">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-934">10001</span></span></td>
<td><span data-ttu-id="c126d-935">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-935">Electricity</span></span></td>
<td><span data-ttu-id="c126d-936">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-936">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c126d-937">2,507.09</span></span></td>
<td><span data-ttu-id="c126d-938">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c126d-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-939">Prod 2</span></span></td>
<td><span data-ttu-id="c126d-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="c126d-940">Product 2</span></span></td>
<td><span data-ttu-id="c126d-941">10001</span><span class="sxs-lookup"><span data-stu-id="c126d-941">10001</span></span></td>
<td><span data-ttu-id="c126d-942">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="c126d-942">Electricity</span></span></td>
<td><span data-ttu-id="c126d-943">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-943">Variable cost</span></span></td>
<td><span data-ttu-id="c126d-944">470.08</span><span class="sxs-lookup"><span data-stu-id="c126d-944">470.08</span></span></td>
<td><span data-ttu-id="c126d-945">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="c126d-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c126d-946">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="c126d-946">Conclusion</span></span>
<span data-ttu-id="c126d-947">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="c126d-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c126d-948">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="c126d-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c126d-949">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="c126d-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c126d-950">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="c126d-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c126d-951">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="c126d-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c126d-952">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="c126d-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c126d-953">Sum</span><span class="sxs-lookup"><span data-stu-id="c126d-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c126d-954">CC099</span><span class="sxs-lookup"><span data-stu-id="c126d-954">CC099</span></span></th>
<th><span data-ttu-id="c126d-955">CC001</span><span class="sxs-lookup"><span data-stu-id="c126d-955">CC001</span></span></th>
<th><span data-ttu-id="c126d-956">CC002</span><span class="sxs-lookup"><span data-stu-id="c126d-956">CC002</span></span></th>
<th><span data-ttu-id="c126d-957">CC003</span><span class="sxs-lookup"><span data-stu-id="c126d-957">CC003</span></span></th>
<th><span data-ttu-id="c126d-958">CC004</span><span class="sxs-lookup"><span data-stu-id="c126d-958">CC004</span></span></th>
<th><span data-ttu-id="c126d-959">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="c126d-959">Proj 1</span></span></th>
<th><span data-ttu-id="c126d-960">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="c126d-960">Proj 2</span></span></th>
<th><span data-ttu-id="c126d-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c126d-961">Prod 1</span></span></th>
<th><span data-ttu-id="c126d-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c126d-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c126d-963">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="c126d-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c126d-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c126d-973">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="c126d-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c126d-975">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-978">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-979">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-980">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c126d-981">776.36</span><span class="sxs-lookup"><span data-stu-id="c126d-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-982">223.64</span><span class="sxs-lookup"><span data-stu-id="c126d-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c126d-984">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="c126d-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-985">000</span><span class="sxs-lookup"><span data-stu-id="c126d-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-987">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-988">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-989">0,00</span><span class="sxs-lookup"><span data-stu-id="c126d-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-990">30,00</span><span class="sxs-lookup"><span data-stu-id="c126d-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-991">10,00</span><span class="sxs-lookup"><span data-stu-id="c126d-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c126d-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c126d-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c126d-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="c126d-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c126d-995">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="c126d-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c126d-996">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="c126d-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c126d-997">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="c126d-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c126d-998">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="c126d-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c126d-999">Hvis du vil ha mer informasjon, kan du se policyen for kostnadsakkumulering.</span><span class="sxs-lookup"><span data-stu-id="c126d-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="c126d-1000">(Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)</span><span class="sxs-lookup"><span data-stu-id="c126d-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




