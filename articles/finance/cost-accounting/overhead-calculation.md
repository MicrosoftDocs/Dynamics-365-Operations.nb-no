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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759478"
---
# <a name="overhead-calculation"></a><span data-ttu-id="8a3f4-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="8a3f4-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a3f4-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8a3f4-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-105">Term definition</span></span>
---------------

<span data-ttu-id="8a3f4-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8a3f4-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8a3f4-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="8a3f4-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8a3f4-109">Leie</span><span class="sxs-lookup"><span data-stu-id="8a3f4-109">Rent</span></span>
-   <span data-ttu-id="8a3f4-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-110">Electricity</span></span>
-   <span data-ttu-id="8a3f4-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="8a3f4-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8a3f4-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="8a3f4-112">Overhead calculation overview</span></span>
<span data-ttu-id="8a3f4-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8a3f4-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8a3f4-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8a3f4-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8a3f4-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8a3f4-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="8a3f4-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8a3f4-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="8a3f4-119">Version type</span></span>
-   <span data-ttu-id="8a3f4-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="8a3f4-120">Date and time</span></span>
-   <span data-ttu-id="8a3f4-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8a3f4-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="8a3f4-122">Fiscal year</span></span>
-   <span data-ttu-id="8a3f4-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="8a3f4-123">Fiscal period</span></span>

<span data-ttu-id="8a3f4-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8a3f4-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8a3f4-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8a3f4-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8a3f4-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8a3f4-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8a3f4-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8a3f4-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8a3f4-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="8a3f4-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8a3f4-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8a3f4-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8a3f4-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8a3f4-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8a3f4-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="8a3f4-140">Main account</span></span></th>
<th><span data-ttu-id="8a3f4-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-143">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-144">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-145">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-145">10001</span></span></td>
<td><span data-ttu-id="8a3f4-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-146">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8a3f4-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8a3f4-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8a3f4-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8a3f4-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8a3f4-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8a3f4-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8a3f4-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8a3f4-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="8a3f4-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8a3f4-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8a3f4-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="8a3f4-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8a3f4-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="8a3f4-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8a3f4-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-160">Journal</span></span></th>
<th><span data-ttu-id="8a3f4-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="8a3f4-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8a3f4-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8a3f4-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8a3f4-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-164">00001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-164">00001</span></span></td>
<td><span data-ttu-id="8a3f4-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8a3f4-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="8a3f4-166">Fiscal</span></span></td>
<td><span data-ttu-id="8a3f4-167">2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-167">2017</span></span></td>
<td><span data-ttu-id="8a3f4-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-168">Period 1</span></span></td>
<td><span data-ttu-id="8a3f4-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8a3f4-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-173">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-177">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-178">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-179">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-179">10001</span></span></td>
<td><span data-ttu-id="8a3f4-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-180">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="8a3f4-181">Unclassified</span></span></td>
<td><span data-ttu-id="8a3f4-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8a3f4-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="8a3f4-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-185">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-187">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-189">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-190">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-191">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-191">10001</span></span></td>
<td><span data-ttu-id="8a3f4-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-192">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="8a3f4-193">Unclassified</span></span></td>
<td><span data-ttu-id="8a3f4-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-194">10,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-196">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-197">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-198">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-198">10001</span></span></td>
<td><span data-ttu-id="8a3f4-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-199">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="8a3f4-200">Unclassified</span></span></td>
<td><span data-ttu-id="8a3f4-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-203">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-204">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-205">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-205">10001</span></span></td>
<td><span data-ttu-id="8a3f4-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-206">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-208">1,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-210">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-211">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-212">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-212">10001</span></span></td>
<td><span data-ttu-id="8a3f4-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="8a3f4-213">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-214">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-215">9,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8a3f4-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8a3f4-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8a3f4-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8a3f4-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-221">Define the cost distribution rule</span></span>

<span data-ttu-id="8a3f4-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8a3f4-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8a3f4-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8a3f4-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8a3f4-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8a3f4-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-228">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-229">kWt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-230">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-230">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-231">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-231">HR</span></span></td>
<td><span data-ttu-id="8a3f4-232">1 000</span><span class="sxs-lookup"><span data-stu-id="8a3f4-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-233">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-233">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-234">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-234">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-235">6,000</span><span class="sxs-lookup"><span data-stu-id="8a3f4-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-236">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-236">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-237">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-237">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-238">0</span><span class="sxs-lookup"><span data-stu-id="8a3f4-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-240">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-241">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-242">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-244">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-244">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-245">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-245">HR</span></span></td>
<td><span data-ttu-id="8a3f4-246">1 000</span><span class="sxs-lookup"><span data-stu-id="8a3f4-246">1,000</span></span></td>
<td><span data-ttu-id="8a3f4-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-249">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-249">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-250">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-250">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-251">6,000</span><span class="sxs-lookup"><span data-stu-id="8a3f4-251">6,000</span></span></td>
<td><span data-ttu-id="8a3f4-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8a3f4-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-254">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-254">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-255">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-255">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-256">0</span><span class="sxs-lookup"><span data-stu-id="8a3f4-256">0</span></span></td>
<td><span data-ttu-id="8a3f4-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-258">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8a3f4-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-261">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-262">Formel</span><span class="sxs-lookup"><span data-stu-id="8a3f4-262">Formula</span></span></th>
<th><span data-ttu-id="8a3f4-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-263">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-264">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-266">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-266">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-267">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-267">HR</span></span></td>
<td><span data-ttu-id="8a3f4-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8a3f4-269">1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-269">1</span></span></td>
<td><span data-ttu-id="8a3f4-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-271">500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-272">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-272">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-273">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-273">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8a3f4-275">1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-275">1</span></span></td>
<td><span data-ttu-id="8a3f4-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-277">500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-278">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-278">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-279">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-279">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8a3f4-281">0</span><span class="sxs-lookup"><span data-stu-id="8a3f4-281">0</span></span></td>
<td><span data-ttu-id="8a3f4-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-283">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8a3f4-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-285">Journal</span></span></th>
<th><span data-ttu-id="8a3f4-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="8a3f4-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8a3f4-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8a3f4-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8a3f4-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-289">00002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-289">00002</span></span></td>
<td><span data-ttu-id="8a3f4-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8a3f4-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="8a3f4-291">Fiscal</span></span></td>
<td><span data-ttu-id="8a3f4-292">2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-292">2017</span></span></td>
<td><span data-ttu-id="8a3f4-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-293">Period 1</span></span></td>
<td><span data-ttu-id="8a3f4-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8a3f4-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-298">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-299">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-302">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-302">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-303">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-304">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-304">10001</span></span></td>
<td><span data-ttu-id="8a3f4-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-305">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-306">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-309">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-309">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-310">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-311">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-311">10001</span></span></td>
<td><span data-ttu-id="8a3f4-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-312">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-313">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8a3f4-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="8a3f4-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-317">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-318">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-319">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-321">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-321">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-322">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-323">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-323">10001</span></span></td>
<td><span data-ttu-id="8a3f4-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-324">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-325">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-326">-1,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-328">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-328">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-329">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-329">HR</span></span></td>
<td><span data-ttu-id="8a3f4-330">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-330">10001</span></span></td>
<td><span data-ttu-id="8a3f4-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-331">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-332">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-333">500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-333">500.00</span></span></td>
<td><span data-ttu-id="8a3f4-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-335">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-335">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-336">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-336">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-337">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-337">10001</span></span></td>
<td><span data-ttu-id="8a3f4-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-338">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-339">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-340">500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-340">500.00</span></span></td>
<td><span data-ttu-id="8a3f4-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-342">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-342">CC099</span></span></td>
<td><span data-ttu-id="8a3f4-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-343">Default cost center</span></span></td>
<td><span data-ttu-id="8a3f4-344">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-344">10001</span></span></td>
<td><span data-ttu-id="8a3f4-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-345">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-346">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-347">-9,000.00</span></span></td>
<td><span data-ttu-id="8a3f4-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-349">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-349">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-350">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-350">HR</span></span></td>
<td><span data-ttu-id="8a3f4-351">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-351">10001</span></span></td>
<td><span data-ttu-id="8a3f4-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-352">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-353">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-354">1,285.71</span></span></td>
<td><span data-ttu-id="8a3f4-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-356">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-356">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-357">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-357">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-358">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-358">10001</span></span></td>
<td><span data-ttu-id="8a3f4-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="8a3f4-359">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-360">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8a3f4-361">7,714.29</span></span></td>
<td><span data-ttu-id="8a3f4-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8a3f4-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="8a3f4-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8a3f4-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8a3f4-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8a3f4-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="8a3f4-367">Define the overhead rate</span></span>

<span data-ttu-id="8a3f4-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8a3f4-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-370">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="8a3f4-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-372">Proj 1</span></span></td>
<td><span data-ttu-id="8a3f4-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-373">Project 1</span></span></td>
<td><span data-ttu-id="8a3f4-374">3</span><span class="sxs-lookup"><span data-stu-id="8a3f4-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-375">Proj 2</span></span></td>
<td><span data-ttu-id="8a3f4-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-376">Project 2</span></span></td>
<td><span data-ttu-id="8a3f4-377">1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-379">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-380">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-381">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-382">Units</span></span></th>
<th><span data-ttu-id="8a3f4-383">Sats</span><span class="sxs-lookup"><span data-stu-id="8a3f4-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-384">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-384">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-385">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-385">HR</span></span></td>
<td><span data-ttu-id="8a3f4-386">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-386">10001</span></span></td>
<td><span data-ttu-id="8a3f4-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-387">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-388">1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-388">1</span></span></td>
<td><span data-ttu-id="8a3f4-389">10</span><span class="sxs-lookup"><span data-stu-id="8a3f4-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-391">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-392">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-393">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-394">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-396">Proj 1</span></span></td>
<td><span data-ttu-id="8a3f4-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-397">Project 1</span></span></td>
<td><span data-ttu-id="8a3f4-398">3</span><span class="sxs-lookup"><span data-stu-id="8a3f4-398">3</span></span></td>
<td><span data-ttu-id="8a3f4-399">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-399">10001</span></span></td>
<td><span data-ttu-id="8a3f4-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8a3f4-401">30,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-402">Proj 2</span></span></td>
<td><span data-ttu-id="8a3f4-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-403">Project 2</span></span></td>
<td><span data-ttu-id="8a3f4-404">1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-404">1</span></span></td>
<td><span data-ttu-id="8a3f4-405">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-405">10001</span></span></td>
<td><span data-ttu-id="8a3f4-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8a3f4-407">10,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8a3f4-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-409">Journal</span></span></th>
<th><span data-ttu-id="8a3f4-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="8a3f4-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8a3f4-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8a3f4-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8a3f4-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-413">00003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-413">00003</span></span></td>
<td><span data-ttu-id="8a3f4-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="8a3f4-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8a3f4-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="8a3f4-415">Fiscal</span></span></td>
<td><span data-ttu-id="8a3f4-416">2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-416">2017</span></span></td>
<td><span data-ttu-id="8a3f4-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-417">Period 1</span></span></td>
<td><span data-ttu-id="8a3f4-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8a3f4-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-421">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-424">Proj 1</span></span></td>
<td><span data-ttu-id="8a3f4-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8a3f4-426">3,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-428">Proj 2</span></span></td>
<td><span data-ttu-id="8a3f4-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8a3f4-430">1,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8a3f4-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="8a3f4-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-433">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-434">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-435">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-437">CC0001</span></span></td>
<td><span data-ttu-id="8a3f4-438">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-438">HR</span></span></td>
<td><span data-ttu-id="8a3f4-439">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-439">10001</span></span></td>
<td><span data-ttu-id="8a3f4-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-440">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-441">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-442">-30.00</span></span></td>
<td><span data-ttu-id="8a3f4-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-444">Proj 1</span></span></td>
<td><span data-ttu-id="8a3f4-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8a3f4-446">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-446">10001</span></span></td>
<td><span data-ttu-id="8a3f4-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-447">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-448">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-449">30,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-449">30.00</span></span></td>
<td><span data-ttu-id="8a3f4-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-451">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-451">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-452">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-452">HR</span></span></td>
<td><span data-ttu-id="8a3f4-453">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-453">10001</span></span></td>
<td><span data-ttu-id="8a3f4-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-454">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-455">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-456">-10.00</span></span></td>
<td><span data-ttu-id="8a3f4-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-458">Proj 2</span></span></td>
<td><span data-ttu-id="8a3f4-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8a3f4-460">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-460">10001</span></span></td>
<td><span data-ttu-id="8a3f4-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="8a3f4-461">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-462">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-463">10,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-463">10.00</span></span></td>
<td><span data-ttu-id="8a3f4-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8a3f4-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8a3f4-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8a3f4-468">Finance støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="8a3f4-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8a3f4-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8a3f4-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8a3f4-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8a3f4-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8a3f4-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8a3f4-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-475">Define the cost allocation</span></span>

<span data-ttu-id="8a3f4-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8a3f4-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8a3f4-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-479">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="8a3f4-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-481">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-481">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-482">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-482">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-483">35</span><span class="sxs-lookup"><span data-stu-id="8a3f4-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-484">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-484">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-485">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-485">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-486">55</span><span class="sxs-lookup"><span data-stu-id="8a3f4-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-487">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-487">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-488">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-489">10</span><span class="sxs-lookup"><span data-stu-id="8a3f4-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8a3f4-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-492">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="8a3f4-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-494">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-494">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-495">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-495">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-496">65</span><span class="sxs-lookup"><span data-stu-id="8a3f4-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-497">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-497">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-498">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-499">35</span><span class="sxs-lookup"><span data-stu-id="8a3f4-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8a3f4-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-502">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-504">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-505">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-506">60</span><span class="sxs-lookup"><span data-stu-id="8a3f4-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-507">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-508">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-509">20</span><span class="sxs-lookup"><span data-stu-id="8a3f4-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8a3f4-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-512">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-514">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-515">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-516">80</span><span class="sxs-lookup"><span data-stu-id="8a3f4-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-517">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-518">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-519">15</span><span class="sxs-lookup"><span data-stu-id="8a3f4-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8a3f4-520">Statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8a3f4-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="8a3f4-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-523">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-524">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-525">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-526">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-528">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-528">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-529">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-529">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-530">35</span><span class="sxs-lookup"><span data-stu-id="8a3f4-530">35</span></span></td>
<td><span data-ttu-id="8a3f4-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8a3f4-532">175.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-532">175.00</span></span></td>
<td><span data-ttu-id="8a3f4-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-534">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-534">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-535">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-535">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-536">55</span><span class="sxs-lookup"><span data-stu-id="8a3f4-536">55</span></span></td>
<td><span data-ttu-id="8a3f4-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8a3f4-538">275.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-538">275.00</span></span></td>
<td><span data-ttu-id="8a3f4-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-540">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-540">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-541">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-542">10</span><span class="sxs-lookup"><span data-stu-id="8a3f4-542">10</span></span></td>
<td><span data-ttu-id="8a3f4-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8a3f4-544">50,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-544">50.00</span></span></td>
<td><span data-ttu-id="8a3f4-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-546">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-546">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-547">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-547">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-548">35</span><span class="sxs-lookup"><span data-stu-id="8a3f4-548">35</span></span></td>
<td><span data-ttu-id="8a3f4-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8a3f4-550">436.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-550">436.00</span></span></td>
<td><span data-ttu-id="8a3f4-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-552">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-552">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-553">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-553">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-554">55</span><span class="sxs-lookup"><span data-stu-id="8a3f4-554">55</span></span></td>
<td><span data-ttu-id="8a3f4-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8a3f4-556">685.14</span><span class="sxs-lookup"><span data-stu-id="8a3f4-556">685.14</span></span></td>
<td><span data-ttu-id="8a3f4-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-558">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-558">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-559">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-560">10</span><span class="sxs-lookup"><span data-stu-id="8a3f4-560">10</span></span></td>
<td><span data-ttu-id="8a3f4-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8a3f4-562">124.57</span><span class="sxs-lookup"><span data-stu-id="8a3f4-562">124.57</span></span></td>
<td><span data-ttu-id="8a3f4-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-565">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-566">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-567">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-568">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-570">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-570">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-571">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-571">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-572">65</span><span class="sxs-lookup"><span data-stu-id="8a3f4-572">65</span></span></td>
<td><span data-ttu-id="8a3f4-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8a3f4-574">438.75</span><span class="sxs-lookup"><span data-stu-id="8a3f4-574">438.75</span></span></td>
<td><span data-ttu-id="8a3f4-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-576">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-576">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-577">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-578">35</span><span class="sxs-lookup"><span data-stu-id="8a3f4-578">35</span></span></td>
<td><span data-ttu-id="8a3f4-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8a3f4-580">236.25</span><span class="sxs-lookup"><span data-stu-id="8a3f4-580">236.25</span></span></td>
<td><span data-ttu-id="8a3f4-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-582">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-582">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-583">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-583">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-584">65</span><span class="sxs-lookup"><span data-stu-id="8a3f4-584">65</span></span></td>
<td><span data-ttu-id="8a3f4-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8a3f4-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8a3f4-586">5,297.69</span></span></td>
<td><span data-ttu-id="8a3f4-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-588">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-588">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-589">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-590">35</span><span class="sxs-lookup"><span data-stu-id="8a3f4-590">35</span></span></td>
<td><span data-ttu-id="8a3f4-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8a3f4-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8a3f4-592">2,852.60</span></span></td>
<td><span data-ttu-id="8a3f4-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-595">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-596">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-597">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-598">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-600">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-601">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-602">60</span><span class="sxs-lookup"><span data-stu-id="8a3f4-602">60</span></span></td>
<td><span data-ttu-id="8a3f4-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8a3f4-604">535.31</span><span class="sxs-lookup"><span data-stu-id="8a3f4-604">535.31</span></span></td>
<td><span data-ttu-id="8a3f4-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-606">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-607">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-608">20</span><span class="sxs-lookup"><span data-stu-id="8a3f4-608">20</span></span></td>
<td><span data-ttu-id="8a3f4-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8a3f4-610">178.44</span><span class="sxs-lookup"><span data-stu-id="8a3f4-610">178.44</span></span></td>
<td><span data-ttu-id="8a3f4-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-612">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-613">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-614">60</span><span class="sxs-lookup"><span data-stu-id="8a3f4-614">60</span></span></td>
<td><span data-ttu-id="8a3f4-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8a3f4-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8a3f4-616">4,487.12</span></span></td>
<td><span data-ttu-id="8a3f4-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-618">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-619">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-620">20</span><span class="sxs-lookup"><span data-stu-id="8a3f4-620">20</span></span></td>
<td><span data-ttu-id="8a3f4-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8a3f4-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-622">1,495.71</span></span></td>
<td><span data-ttu-id="8a3f4-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8a3f4-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-625">Cost object</span></span></th>
<th><span data-ttu-id="8a3f4-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="8a3f4-626">Magnitude</span></span></th>
<th><span data-ttu-id="8a3f4-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="8a3f4-627">Allocation factor</span></span></th>
<th><span data-ttu-id="8a3f4-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-628">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-630">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-631">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-632">80</span><span class="sxs-lookup"><span data-stu-id="8a3f4-632">80</span></span></td>
<td><span data-ttu-id="8a3f4-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8a3f4-634">241.05</span><span class="sxs-lookup"><span data-stu-id="8a3f4-634">241.05</span></span></td>
<td><span data-ttu-id="8a3f4-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-636">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-637">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-638">15</span><span class="sxs-lookup"><span data-stu-id="8a3f4-638">15</span></span></td>
<td><span data-ttu-id="8a3f4-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8a3f4-640">45.20</span><span class="sxs-lookup"><span data-stu-id="8a3f4-640">45.20</span></span></td>
<td><span data-ttu-id="8a3f4-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-642">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-643">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-644">80</span><span class="sxs-lookup"><span data-stu-id="8a3f4-644">80</span></span></td>
<td><span data-ttu-id="8a3f4-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8a3f4-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8a3f4-646">2,507.09</span></span></td>
<td><span data-ttu-id="8a3f4-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-648">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-649">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-650">15</span><span class="sxs-lookup"><span data-stu-id="8a3f4-650">15</span></span></td>
<td><span data-ttu-id="8a3f4-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8a3f4-652">470.08</span><span class="sxs-lookup"><span data-stu-id="8a3f4-652">470.08</span></span></td>
<td><span data-ttu-id="8a3f4-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8a3f4-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-655">Journal</span></span></th>
<th><span data-ttu-id="8a3f4-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="8a3f4-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8a3f4-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="8a3f4-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8a3f4-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-659">00004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-659">00004</span></span></td>
<td><span data-ttu-id="8a3f4-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="8a3f4-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8a3f4-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="8a3f4-661">Fiscal</span></span></td>
<td><span data-ttu-id="8a3f4-662">2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-662">2017</span></span></td>
<td><span data-ttu-id="8a3f4-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-663">Period 1</span></span></td>
<td><span data-ttu-id="8a3f4-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8a3f4-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="8a3f4-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8a3f4-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-668">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-669">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-672">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-672">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-673">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-673">HR</span></span></td>
<td><span data-ttu-id="8a3f4-674">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-674">10001</span></span></td>
<td><span data-ttu-id="8a3f4-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-675">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-676">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-677">500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-679">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-679">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-680">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-680">HR</span></span></td>
<td><span data-ttu-id="8a3f4-681">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-681">10001</span></span></td>
<td><span data-ttu-id="8a3f4-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-682">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-683">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-686">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-686">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-687">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-687">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-688">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-688">10001</span></span></td>
<td><span data-ttu-id="8a3f4-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-689">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-690">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-691">675.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-693">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-693">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-694">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-694">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-695">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-695">10001</span></span></td>
<td><span data-ttu-id="8a3f4-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-696">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-697">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8a3f4-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-700">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-700">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-701">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-701">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-702">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-702">10001</span></span></td>
<td><span data-ttu-id="8a3f4-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-703">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-704">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-705">713.75</span><span class="sxs-lookup"><span data-stu-id="8a3f4-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-707">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-707">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-708">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-708">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-709">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-709">10001</span></span></td>
<td><span data-ttu-id="8a3f4-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-710">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-711">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8a3f4-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-714">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-714">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-715">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-716">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-716">10001</span></span></td>
<td><span data-ttu-id="8a3f4-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-717">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-718">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-719">286.25</span><span class="sxs-lookup"><span data-stu-id="8a3f4-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-721">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-721">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-722">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-723">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-723">10001</span></span></td>
<td><span data-ttu-id="8a3f4-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-724">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-725">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8a3f4-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-728">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-729">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-730">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-730">10001</span></span></td>
<td><span data-ttu-id="8a3f4-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-731">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-732">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-733">776.36</span><span class="sxs-lookup"><span data-stu-id="8a3f4-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-735">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-736">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-737">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-737">10001</span></span></td>
<td><span data-ttu-id="8a3f4-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-738">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-739">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8a3f4-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-742">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-743">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-744">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-744">10001</span></span></td>
<td><span data-ttu-id="8a3f4-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-745">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-746">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-747">223.64</span><span class="sxs-lookup"><span data-stu-id="8a3f4-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="8a3f4-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-749">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-750">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-751">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-751">10001</span></span></td>
<td><span data-ttu-id="8a3f4-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-752">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-753">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8a3f4-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8a3f4-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="8a3f4-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8a3f4-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8a3f4-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-757">Cost element</span></span></th>
<th><span data-ttu-id="8a3f4-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="8a3f4-758">Cost behavior</span></span></th>
<th><span data-ttu-id="8a3f4-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="8a3f4-759">Amount</span></span></th>
<th><span data-ttu-id="8a3f4-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="8a3f4-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a3f4-761">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-761">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-762">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-762">HR</span></span></td>
<td><span data-ttu-id="8a3f4-763">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-763">10001</span></span></td>
<td><span data-ttu-id="8a3f4-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-764">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-765">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-766">-500.00</span></span></td>
<td><span data-ttu-id="8a3f4-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-768">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-768">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-769">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-769">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-770">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-770">10001</span></span></td>
<td><span data-ttu-id="8a3f4-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-771">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-772">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-773">175.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-773">175.00</span></span></td>
<td><span data-ttu-id="8a3f4-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-775">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-775">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-776">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-776">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-777">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-777">10001</span></span></td>
<td><span data-ttu-id="8a3f4-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-778">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-779">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-780">275.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-780">275.00</span></span></td>
<td><span data-ttu-id="8a3f4-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-782">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-782">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-783">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-784">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-784">10001</span></span></td>
<td><span data-ttu-id="8a3f4-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-785">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-786">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-787">50,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-787">50,00</span></span></td>
<td><span data-ttu-id="8a3f4-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-789">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-789">CC001</span></span></td>
<td><span data-ttu-id="8a3f4-790">Personale</span><span class="sxs-lookup"><span data-stu-id="8a3f4-790">HR</span></span></td>
<td><span data-ttu-id="8a3f4-791">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-791">10001</span></span></td>
<td><span data-ttu-id="8a3f4-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-792">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-793">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-794">-1,245.71</span></span></td>
<td><span data-ttu-id="8a3f4-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-796">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-796">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-797">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-797">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-798">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-798">10001</span></span></td>
<td><span data-ttu-id="8a3f4-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-799">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-800">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-801">436.00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-801">436.00</span></span></td>
<td><span data-ttu-id="8a3f4-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-803">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-803">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-804">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-804">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-805">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-805">10001</span></span></td>
<td><span data-ttu-id="8a3f4-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-806">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-807">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-808">685.14</span><span class="sxs-lookup"><span data-stu-id="8a3f4-808">685.14</span></span></td>
<td><span data-ttu-id="8a3f4-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-810">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-810">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-811">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-812">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-812">10001</span></span></td>
<td><span data-ttu-id="8a3f4-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-813">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-814">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-815">124.57</span><span class="sxs-lookup"><span data-stu-id="8a3f4-815">124.57</span></span></td>
<td><span data-ttu-id="8a3f4-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-817">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-817">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-818">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-818">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-819">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-819">10001</span></span></td>
<td><span data-ttu-id="8a3f4-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-820">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-821">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-822">-675.00</span></span></td>
<td><span data-ttu-id="8a3f4-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-824">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-824">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-825">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-825">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-826">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-826">10001</span></span></td>
<td><span data-ttu-id="8a3f4-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-827">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-828">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-829">438.75</span><span class="sxs-lookup"><span data-stu-id="8a3f4-829">438.75</span></span></td>
<td><span data-ttu-id="8a3f4-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-831">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-831">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-832">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-833">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-833">10001</span></span></td>
<td><span data-ttu-id="8a3f4-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-834">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-835">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-836">236.25</span><span class="sxs-lookup"><span data-stu-id="8a3f4-836">236.25</span></span></td>
<td><span data-ttu-id="8a3f4-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-838">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-838">CC002</span></span></td>
<td><span data-ttu-id="8a3f4-839">Finans</span><span class="sxs-lookup"><span data-stu-id="8a3f4-839">Finance</span></span></td>
<td><span data-ttu-id="8a3f4-840">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-840">10001</span></span></td>
<td><span data-ttu-id="8a3f4-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-841">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-842">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="8a3f4-843">-8,150.29</span></span></td>
<td><span data-ttu-id="8a3f4-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-845">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-845">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-846">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-846">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-847">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-847">10001</span></span></td>
<td><span data-ttu-id="8a3f4-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-848">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-849">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8a3f4-850">5,297.69</span></span></td>
<td><span data-ttu-id="8a3f4-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-852">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-852">CC004</span></span></td>
<td><span data-ttu-id="8a3f4-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="8a3f4-853">Packaging</span></span></td>
<td><span data-ttu-id="8a3f4-854">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-854">10001</span></span></td>
<td><span data-ttu-id="8a3f4-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-855">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-856">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8a3f4-857">2,852.60</span></span></td>
<td><span data-ttu-id="8a3f4-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-859">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-859">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-860">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-860">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-861">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-861">10001</span></span></td>
<td><span data-ttu-id="8a3f4-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-862">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-863">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="8a3f4-864">-713.75</span></span></td>
<td><span data-ttu-id="8a3f4-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-866">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-867">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-868">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-868">10001</span></span></td>
<td><span data-ttu-id="8a3f4-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-869">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-870">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-871">535.31</span><span class="sxs-lookup"><span data-stu-id="8a3f4-871">535.31</span></span></td>
<td><span data-ttu-id="8a3f4-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-873">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-874">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-875">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-875">10001</span></span></td>
<td><span data-ttu-id="8a3f4-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-876">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-877">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-878">178.44</span><span class="sxs-lookup"><span data-stu-id="8a3f4-878">178.44</span></span></td>
<td><span data-ttu-id="8a3f4-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-880">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-880">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-881">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-881">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-882">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-882">10001</span></span></td>
<td><span data-ttu-id="8a3f4-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-883">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-884">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="8a3f4-885">-5,982.83</span></span></td>
<td><span data-ttu-id="8a3f4-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-887">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-888">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-889">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-889">10001</span></span></td>
<td><span data-ttu-id="8a3f4-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-890">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-891">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8a3f4-892">4,487.12</span></span></td>
<td><span data-ttu-id="8a3f4-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-894">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-895">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-896">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-896">10001</span></span></td>
<td><span data-ttu-id="8a3f4-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-897">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-898">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8a3f4-899">1,495.71</span></span></td>
<td><span data-ttu-id="8a3f4-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-901">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-901">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-902">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-902">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-903">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-903">10001</span></span></td>
<td><span data-ttu-id="8a3f4-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-904">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-905">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="8a3f4-906">-286.25</span></span></td>
<td><span data-ttu-id="8a3f4-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-908">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-909">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-910">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-910">10001</span></span></td>
<td><span data-ttu-id="8a3f4-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-911">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-912">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-913">241.05</span><span class="sxs-lookup"><span data-stu-id="8a3f4-913">241.05</span></span></td>
<td><span data-ttu-id="8a3f4-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-915">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-916">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-917">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-917">10001</span></span></td>
<td><span data-ttu-id="8a3f4-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-918">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-919">Fixed cost</span></span></td>
<td><span data-ttu-id="8a3f4-920">45.20</span><span class="sxs-lookup"><span data-stu-id="8a3f4-920">45.20</span></span></td>
<td><span data-ttu-id="8a3f4-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-922">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-922">CC003</span></span></td>
<td><span data-ttu-id="8a3f4-923">Samling</span><span class="sxs-lookup"><span data-stu-id="8a3f4-923">Assembly</span></span></td>
<td><span data-ttu-id="8a3f4-924">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-924">10001</span></span></td>
<td><span data-ttu-id="8a3f4-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-925">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-926">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="8a3f4-927">-2,977.17</span></span></td>
<td><span data-ttu-id="8a3f4-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-929">Prod 1</span></span></td>
<td><span data-ttu-id="8a3f4-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-930">Product 1</span></span></td>
<td><span data-ttu-id="8a3f4-931">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-931">10001</span></span></td>
<td><span data-ttu-id="8a3f4-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-932">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-933">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8a3f4-934">2,507.09</span></span></td>
<td><span data-ttu-id="8a3f4-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8a3f4-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-936">Prod 2</span></span></td>
<td><span data-ttu-id="8a3f4-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-937">Product 2</span></span></td>
<td><span data-ttu-id="8a3f4-938">10001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-938">10001</span></span></td>
<td><span data-ttu-id="8a3f4-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="8a3f4-939">Electricity</span></span></td>
<td><span data-ttu-id="8a3f4-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-940">Variable cost</span></span></td>
<td><span data-ttu-id="8a3f4-941">470.08</span><span class="sxs-lookup"><span data-stu-id="8a3f4-941">470.08</span></span></td>
<td><span data-ttu-id="8a3f4-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="8a3f4-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8a3f4-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="8a3f4-943">Conclusion</span></span>
<span data-ttu-id="8a3f4-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8a3f4-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8a3f4-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8a3f4-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8a3f4-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="8a3f4-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8a3f4-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="8a3f4-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8a3f4-950">Sum</span><span class="sxs-lookup"><span data-stu-id="8a3f4-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8a3f4-951">CC099</span><span class="sxs-lookup"><span data-stu-id="8a3f4-951">CC099</span></span></th>
<th><span data-ttu-id="8a3f4-952">CC001</span><span class="sxs-lookup"><span data-stu-id="8a3f4-952">CC001</span></span></th>
<th><span data-ttu-id="8a3f4-953">CC002</span><span class="sxs-lookup"><span data-stu-id="8a3f4-953">CC002</span></span></th>
<th><span data-ttu-id="8a3f4-954">CC003</span><span class="sxs-lookup"><span data-stu-id="8a3f4-954">CC003</span></span></th>
<th><span data-ttu-id="8a3f4-955">CC004</span><span class="sxs-lookup"><span data-stu-id="8a3f4-955">CC004</span></span></th>
<th><span data-ttu-id="8a3f4-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-956">Proj 1</span></span></th>
<th><span data-ttu-id="8a3f4-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-957">Proj 2</span></span></th>
<th><span data-ttu-id="8a3f4-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-958">Prod 1</span></span></th>
<th><span data-ttu-id="8a3f4-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8a3f4-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="8a3f4-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8a3f4-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="8a3f4-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-971">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8a3f4-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-973">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-975">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-978">776.36</span><span class="sxs-lookup"><span data-stu-id="8a3f4-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-979">223.64</span><span class="sxs-lookup"><span data-stu-id="8a3f4-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8a3f4-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="8a3f4-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-982">000</span><span class="sxs-lookup"><span data-stu-id="8a3f4-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-983">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-984">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-985">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-987">30,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-988">10,00</span><span class="sxs-lookup"><span data-stu-id="8a3f4-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8a3f4-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8a3f4-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8a3f4-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8a3f4-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8a3f4-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8a3f4-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8a3f4-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8a3f4-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8a3f4-996">Hvis du vil ha mer informasjon, se [Policy for opprullet kost og beregning av administrasjonskostnader](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



