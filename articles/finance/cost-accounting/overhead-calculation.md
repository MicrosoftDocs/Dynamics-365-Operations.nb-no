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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770810"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e7b5c-103">Beregning av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="e7b5c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7b5c-104">Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e7b5c-105">Termdefinisjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-105">Term definition</span></span>
---------------

<span data-ttu-id="e7b5c-106">Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e7b5c-107">Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e7b5c-108">Her er noen eksempler på indirekte kostnader:</span><span class="sxs-lookup"><span data-stu-id="e7b5c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e7b5c-109">Leie</span><span class="sxs-lookup"><span data-stu-id="e7b5c-109">Rent</span></span>
-   <span data-ttu-id="e7b5c-110">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-110">Electricity</span></span>
-   <span data-ttu-id="e7b5c-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="e7b5c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e7b5c-112">Oversikt over indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="e7b5c-112">Overhead calculation overview</span></span>
<span data-ttu-id="e7b5c-113">Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e7b5c-114">Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e7b5c-115">Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e7b5c-116">Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e7b5c-117">Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e7b5c-118">Den unike versjons-ID-en består av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="e7b5c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e7b5c-119">Versjonstype</span><span class="sxs-lookup"><span data-stu-id="e7b5c-119">Version type</span></span>
-   <span data-ttu-id="e7b5c-120">Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="e7b5c-120">Date and time</span></span>
-   <span data-ttu-id="e7b5c-121">Kostnadsregnskapsfinans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e7b5c-122">Regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e7b5c-122">Fiscal year</span></span>
-   <span data-ttu-id="e7b5c-123">Regnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="e7b5c-123">Fiscal period</span></span>

<span data-ttu-id="e7b5c-124">Beregning av indirekte kostnader kjøres uavhengig av versjonen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e7b5c-125">Derfor kan du beregne budsjettversjonen før den faktiske versjonen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e7b5c-126">Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e7b5c-127">I hvert trinn opprettes et journalhode med journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e7b5c-128">Dette journalhodet inneholder inndataene for hvert beregningstrinn.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e7b5c-129">Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e7b5c-130">Derfor må du alltid full sporbarhet.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e7b5c-131">[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e7b5c-132">Beregne og tildele den indirekte kostnaden for strøm</span><span class="sxs-lookup"><span data-stu-id="e7b5c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e7b5c-133">I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e7b5c-134">Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e7b5c-135">For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e7b5c-136">Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e7b5c-137">I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-138">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-139">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="e7b5c-140">Main account</span></span></th>
<th><span data-ttu-id="e7b5c-141">Beløp i regnskapsvalutaen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-143">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-144">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-144">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-145">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-145">10001</span></span></td>
<td><span data-ttu-id="e7b5c-146">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-146">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e7b5c-148">Trinn 1: Behandle beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e7b5c-149">Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e7b5c-150">Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e7b5c-151">Definere regelen for kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e7b5c-152">I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e7b5c-153">Strømregninger samsvarer ofte med denne definisjonen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e7b5c-154">Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e7b5c-155">Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:</span><span class="sxs-lookup"><span data-stu-id="e7b5c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e7b5c-156">Fast beløp 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e7b5c-157">0 &lt;= 1 000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="e7b5c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e7b5c-158">1000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="e7b5c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e7b5c-159">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-160">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-160">Journal</span></span></th>
<th><span data-ttu-id="e7b5c-161">Journaltype</span><span class="sxs-lookup"><span data-stu-id="e7b5c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7b5c-162">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7b5c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7b5c-163">Versjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-164">00001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-164">00001</span></span></td>
<td><span data-ttu-id="e7b5c-165">Journal for beregning av kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e7b5c-166">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="e7b5c-166">Fiscal</span></span></td>
<td><span data-ttu-id="e7b5c-167">2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-167">2017</span></span></td>
<td><span data-ttu-id="e7b5c-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-168">Period 1</span></span></td>
<td><span data-ttu-id="e7b5c-169">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e7b5c-170">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-171">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-172">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-173">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-173">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-174">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-175">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-177">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-178">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-178">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-179">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-179">10001</span></span></td>
<td><span data-ttu-id="e7b5c-180">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-180">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-181">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="e7b5c-181">Unclassified</span></span></td>
<td><span data-ttu-id="e7b5c-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7b5c-183">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="e7b5c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-184">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-185">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-185">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-186">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-187">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-188">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-189">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-190">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-190">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-191">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-191">10001</span></span></td>
<td><span data-ttu-id="e7b5c-192">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-192">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-193">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="e7b5c-193">Unclassified</span></span></td>
<td><span data-ttu-id="e7b5c-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-194">10,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-196">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-197">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-197">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-198">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-198">10001</span></span></td>
<td><span data-ttu-id="e7b5c-199">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-199">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-200">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="e7b5c-200">Unclassified</span></span></td>
<td><span data-ttu-id="e7b5c-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-203">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-204">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-204">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-205">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-205">10001</span></span></td>
<td><span data-ttu-id="e7b5c-206">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-206">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-207">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-208">1,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-210">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-211">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-211">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-212">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-212">10001</span></span></td>
<td><span data-ttu-id="e7b5c-213">Strøm</span><span class="sxs-lookup"><span data-stu-id="e7b5c-213">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-214">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-214">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-215">9,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-217">For mer informasjon, se [Opprette og tilordne en kostnadsadferdspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e7b5c-218">Trinn 2: Behandle beregning av kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e7b5c-219">Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e7b5c-220">Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e7b5c-221">Definere regelen for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e7b5c-222">I finansbokføring registreres ofte strømkostnader som et engangsbeløp.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e7b5c-223">I kostnadsregnskap er ikke denne tilnærmingen detaljert nok.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e7b5c-224">Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e7b5c-225">Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e7b5c-226">Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e7b5c-227">Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-228">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-228">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-229">kWt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-230">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-231">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-231">HR</span></span></td>
<td><span data-ttu-id="e7b5c-232">1 000</span><span class="sxs-lookup"><span data-stu-id="e7b5c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-233">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-234">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-234">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-235">6,000</span><span class="sxs-lookup"><span data-stu-id="e7b5c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-236">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-237">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-237">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-238">0</span><span class="sxs-lookup"><span data-stu-id="e7b5c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-239">Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-240">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-240">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-241">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-241">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-242">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-243">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-244">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-245">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-245">HR</span></span></td>
<td><span data-ttu-id="e7b5c-246">1 000</span><span class="sxs-lookup"><span data-stu-id="e7b5c-246">1,000</span></span></td>
<td><span data-ttu-id="e7b5c-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-249">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-250">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-250">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-251">6,000</span><span class="sxs-lookup"><span data-stu-id="e7b5c-251">6,000</span></span></td>
<td><span data-ttu-id="e7b5c-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e7b5c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-254">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-255">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-255">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-256">0</span><span class="sxs-lookup"><span data-stu-id="e7b5c-256">0</span></span></td>
<td><span data-ttu-id="e7b5c-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-259">De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e7b5c-260">Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-261">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-261">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-262">Formel</span><span class="sxs-lookup"><span data-stu-id="e7b5c-262">Formula</span></span></th>
<th><span data-ttu-id="e7b5c-263">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-263">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-264">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-265">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-266">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-267">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-267">HR</span></span></td>
<td><span data-ttu-id="e7b5c-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e7b5c-269">1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-269">1</span></span></td>
<td><span data-ttu-id="e7b5c-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-271">500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-272">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-273">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-273">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e7b5c-275">1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-275">1</span></span></td>
<td><span data-ttu-id="e7b5c-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-277">500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-278">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-279">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-279">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e7b5c-281">0</span><span class="sxs-lookup"><span data-stu-id="e7b5c-281">0</span></span></td>
<td><span data-ttu-id="e7b5c-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e7b5c-284">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-285">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-285">Journal</span></span></th>
<th><span data-ttu-id="e7b5c-286">Journaltype</span><span class="sxs-lookup"><span data-stu-id="e7b5c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7b5c-287">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7b5c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7b5c-288">Versjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-289">00002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-289">00002</span></span></td>
<td><span data-ttu-id="e7b5c-290">Beregningsjournal for kostnadsdistribusjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e7b5c-291">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="e7b5c-291">Fiscal</span></span></td>
<td><span data-ttu-id="e7b5c-292">2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-292">2017</span></span></td>
<td><span data-ttu-id="e7b5c-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-293">Period 1</span></span></td>
<td><span data-ttu-id="e7b5c-294">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e7b5c-295">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-296">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-297">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-298">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-298">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-299">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-300">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-302">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-303">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-303">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-304">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-304">10001</span></span></td>
<td><span data-ttu-id="e7b5c-305">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-305">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-306">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-309">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-310">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-310">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-311">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-311">10001</span></span></td>
<td><span data-ttu-id="e7b5c-312">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-312">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-313">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-313">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7b5c-315">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="e7b5c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-316">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-317">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-317">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-318">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-319">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-319">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-320">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-321">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-322">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-322">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-323">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-323">10001</span></span></td>
<td><span data-ttu-id="e7b5c-324">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-324">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-325">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-328">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-329">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-329">HR</span></span></td>
<td><span data-ttu-id="e7b5c-330">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-330">10001</span></span></td>
<td><span data-ttu-id="e7b5c-331">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-331">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-332">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-333">500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-333">500.00</span></span></td>
<td><span data-ttu-id="e7b5c-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-335">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-336">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-336">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-337">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-337">10001</span></span></td>
<td><span data-ttu-id="e7b5c-338">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-338">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-339">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-340">500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-340">500.00</span></span></td>
<td><span data-ttu-id="e7b5c-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-342">CC099</span></span></td>
<td><span data-ttu-id="e7b5c-343">Standard kostsenter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-343">Default cost center</span></span></td>
<td><span data-ttu-id="e7b5c-344">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-344">10001</span></span></td>
<td><span data-ttu-id="e7b5c-345">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-345">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-346">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-346">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e7b5c-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-349">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-350">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-350">HR</span></span></td>
<td><span data-ttu-id="e7b5c-351">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-351">10001</span></span></td>
<td><span data-ttu-id="e7b5c-352">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-352">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-353">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-353">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-354">1,285.71</span></span></td>
<td><span data-ttu-id="e7b5c-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-356">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-357">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-357">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-358">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-358">10001</span></span></td>
<td><span data-ttu-id="e7b5c-359">Strøm</span><span class="sxs-lookup"><span data-stu-id="e7b5c-359">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-360">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-360">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e7b5c-361">7,714.29</span></span></td>
<td><span data-ttu-id="e7b5c-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-363">For mer informasjon, se [Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e7b5c-364">Trinn 3: Behandle beregningen av indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="e7b5c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e7b5c-365">Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e7b5c-366">Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e7b5c-367">Definer satsen for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="e7b5c-367">Define the overhead rate</span></span>

<span data-ttu-id="e7b5c-368">Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e7b5c-369">Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-370">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-370">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-371">Timeantall</span><span class="sxs-lookup"><span data-stu-id="e7b5c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-372">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-372">Proj 1</span></span></td>
<td><span data-ttu-id="e7b5c-373">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-373">Project 1</span></span></td>
<td><span data-ttu-id="e7b5c-374">3</span><span class="sxs-lookup"><span data-stu-id="e7b5c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-375">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-375">Proj 2</span></span></td>
<td><span data-ttu-id="e7b5c-376">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-376">Project 2</span></span></td>
<td><span data-ttu-id="e7b5c-377">1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-378">En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-379">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-379">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-380">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-380">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-381">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-382">Enheter</span><span class="sxs-lookup"><span data-stu-id="e7b5c-382">Units</span></span></th>
<th><span data-ttu-id="e7b5c-383">Sats</span><span class="sxs-lookup"><span data-stu-id="e7b5c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-384">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-385">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-385">HR</span></span></td>
<td><span data-ttu-id="e7b5c-386">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-386">10001</span></span></td>
<td><span data-ttu-id="e7b5c-387">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-387">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-388">1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-388">1</span></span></td>
<td><span data-ttu-id="e7b5c-389">10</span><span class="sxs-lookup"><span data-stu-id="e7b5c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-390">Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-391">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-391">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-392">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-392">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-393">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-393">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-394">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-395">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-396">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-396">Proj 1</span></span></td>
<td><span data-ttu-id="e7b5c-397">Prosjekt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-397">Project 1</span></span></td>
<td><span data-ttu-id="e7b5c-398">3</span><span class="sxs-lookup"><span data-stu-id="e7b5c-398">3</span></span></td>
<td><span data-ttu-id="e7b5c-399">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-399">10001</span></span></td>
<td><span data-ttu-id="e7b5c-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e7b5c-401">30,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-402">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-402">Proj 2</span></span></td>
<td><span data-ttu-id="e7b5c-403">Prosjekt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-403">Project 2</span></span></td>
<td><span data-ttu-id="e7b5c-404">1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-404">1</span></span></td>
<td><span data-ttu-id="e7b5c-405">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-405">10001</span></span></td>
<td><span data-ttu-id="e7b5c-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e7b5c-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e7b5c-408">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-409">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-409">Journal</span></span></th>
<th><span data-ttu-id="e7b5c-410">Journaltype</span><span class="sxs-lookup"><span data-stu-id="e7b5c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7b5c-411">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7b5c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7b5c-412">Versjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-413">00003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-413">00003</span></span></td>
<td><span data-ttu-id="e7b5c-414">Journal for beregning av sats for indirekte kostnader</span><span class="sxs-lookup"><span data-stu-id="e7b5c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e7b5c-415">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="e7b5c-415">Fiscal</span></span></td>
<td><span data-ttu-id="e7b5c-416">2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-416">2017</span></span></td>
<td><span data-ttu-id="e7b5c-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-417">Period 1</span></span></td>
<td><span data-ttu-id="e7b5c-418">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e7b5c-419">Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-420">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-421">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-421">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-422">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-424">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-424">Proj 1</span></span></td>
<td><span data-ttu-id="e7b5c-425">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e7b5c-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-428">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-428">Proj 2</span></span></td>
<td><span data-ttu-id="e7b5c-429">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e7b5c-430">1,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7b5c-431">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="e7b5c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-432">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-433">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-433">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-434">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-435">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-435">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-436">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-437">CC0001</span></span></td>
<td><span data-ttu-id="e7b5c-438">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-438">HR</span></span></td>
<td><span data-ttu-id="e7b5c-439">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-439">10001</span></span></td>
<td><span data-ttu-id="e7b5c-440">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-440">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-441">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-441">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-442">-30.00</span></span></td>
<td><span data-ttu-id="e7b5c-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-444">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-444">Proj 1</span></span></td>
<td><span data-ttu-id="e7b5c-445">internt prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e7b5c-446">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-446">10001</span></span></td>
<td><span data-ttu-id="e7b5c-447">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-447">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-448">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-448">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-449">30,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-449">30.00</span></span></td>
<td><span data-ttu-id="e7b5c-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-451">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-452">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-452">HR</span></span></td>
<td><span data-ttu-id="e7b5c-453">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-453">10001</span></span></td>
<td><span data-ttu-id="e7b5c-454">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-454">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-455">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-455">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-456">-10.00</span></span></td>
<td><span data-ttu-id="e7b5c-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-458">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-458">Proj 2</span></span></td>
<td><span data-ttu-id="e7b5c-459">internt prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e7b5c-460">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-460">10001</span></span></td>
<td><span data-ttu-id="e7b5c-461">Strøm</span><span class="sxs-lookup"><span data-stu-id="e7b5c-461">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-462">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-462">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-463">10,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-463">10.00</span></span></td>
<td><span data-ttu-id="e7b5c-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-465">For mer informasjon, se [Beregn indirekte kostnader](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e7b5c-466">Trinn 4: Behandle beregning av kostnadstildeling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e7b5c-467">Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e7b5c-468">Finance støtter gjensidig tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="e7b5c-469">I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e7b5c-470">Systemet fastslår automatisk riktig rekkefølge for tildelingene.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e7b5c-471">Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e7b5c-472">Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e7b5c-473">Tildelingsrekkefølgen styres av kostnadskontrollenheten.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e7b5c-474">[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e7b5c-475">Definere kostnadstildelingen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-475">Define the cost allocation</span></span>

<span data-ttu-id="e7b5c-476">Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e7b5c-477">Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e7b5c-478">Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-479">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-479">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-480">Personaletjenester</span><span class="sxs-lookup"><span data-stu-id="e7b5c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-481">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-482">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-482">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-483">35</span><span class="sxs-lookup"><span data-stu-id="e7b5c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-484">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-485">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-485">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-486">55</span><span class="sxs-lookup"><span data-stu-id="e7b5c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-487">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-488">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-488">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-489">10</span><span class="sxs-lookup"><span data-stu-id="e7b5c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-490">Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e7b5c-491">Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-492">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-492">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-493">Finanstjenester</span><span class="sxs-lookup"><span data-stu-id="e7b5c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-494">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-495">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-495">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-496">65</span><span class="sxs-lookup"><span data-stu-id="e7b5c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-497">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-498">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-498">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-499">35</span><span class="sxs-lookup"><span data-stu-id="e7b5c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-500">Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e7b5c-501">Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-502">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-502">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-503">Monteringstjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-504">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-505">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-506">60</span><span class="sxs-lookup"><span data-stu-id="e7b5c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-507">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-508">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-509">20</span><span class="sxs-lookup"><span data-stu-id="e7b5c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-510">Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e7b5c-511">Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-512">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-512">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-513">Emballasjetjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-514">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-515">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-516">80</span><span class="sxs-lookup"><span data-stu-id="e7b5c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-517">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-518">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-519">15</span><span class="sxs-lookup"><span data-stu-id="e7b5c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e7b5c-520">Statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e7b5c-521">Hvis du vil ha mer informasjon, kan du se [Mal for leverandør av statistisk måling](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e7b5c-522">Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-523">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-523">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-524">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-524">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-525">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-526">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-526">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-527">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-528">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-529">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-529">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-530">35</span><span class="sxs-lookup"><span data-stu-id="e7b5c-530">35</span></span></td>
<td><span data-ttu-id="e7b5c-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e7b5c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-532">175.00</span></span></td>
<td><span data-ttu-id="e7b5c-533">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-534">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-535">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-535">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-536">55</span><span class="sxs-lookup"><span data-stu-id="e7b5c-536">55</span></span></td>
<td><span data-ttu-id="e7b5c-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e7b5c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-538">275.00</span></span></td>
<td><span data-ttu-id="e7b5c-539">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-540">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-541">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-541">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-542">10</span><span class="sxs-lookup"><span data-stu-id="e7b5c-542">10</span></span></td>
<td><span data-ttu-id="e7b5c-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e7b5c-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-544">50.00</span></span></td>
<td><span data-ttu-id="e7b5c-545">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-546">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-547">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-547">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-548">35</span><span class="sxs-lookup"><span data-stu-id="e7b5c-548">35</span></span></td>
<td><span data-ttu-id="e7b5c-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e7b5c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-550">436.00</span></span></td>
<td><span data-ttu-id="e7b5c-551">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-552">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-553">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-553">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-554">55</span><span class="sxs-lookup"><span data-stu-id="e7b5c-554">55</span></span></td>
<td><span data-ttu-id="e7b5c-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e7b5c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e7b5c-556">685.14</span></span></td>
<td><span data-ttu-id="e7b5c-557">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-558">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-559">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-559">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-560">10</span><span class="sxs-lookup"><span data-stu-id="e7b5c-560">10</span></span></td>
<td><span data-ttu-id="e7b5c-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e7b5c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e7b5c-562">124.57</span></span></td>
<td><span data-ttu-id="e7b5c-563">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-564">Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-565">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-565">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-566">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-566">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-567">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-568">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-568">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-569">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-570">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-571">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-571">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-572">65</span><span class="sxs-lookup"><span data-stu-id="e7b5c-572">65</span></span></td>
<td><span data-ttu-id="e7b5c-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e7b5c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e7b5c-574">438.75</span></span></td>
<td><span data-ttu-id="e7b5c-575">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-576">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-577">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-577">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-578">35</span><span class="sxs-lookup"><span data-stu-id="e7b5c-578">35</span></span></td>
<td><span data-ttu-id="e7b5c-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e7b5c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e7b5c-580">236.25</span></span></td>
<td><span data-ttu-id="e7b5c-581">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-582">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-583">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-583">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-584">65</span><span class="sxs-lookup"><span data-stu-id="e7b5c-584">65</span></span></td>
<td><span data-ttu-id="e7b5c-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e7b5c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e7b5c-586">5,297.69</span></span></td>
<td><span data-ttu-id="e7b5c-587">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-588">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-589">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-589">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-590">35</span><span class="sxs-lookup"><span data-stu-id="e7b5c-590">35</span></span></td>
<td><span data-ttu-id="e7b5c-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e7b5c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e7b5c-592">2,852.60</span></span></td>
<td><span data-ttu-id="e7b5c-593">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-594">Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-595">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-595">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-596">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-596">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-597">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-598">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-598">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-599">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-600">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-601">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-602">60</span><span class="sxs-lookup"><span data-stu-id="e7b5c-602">60</span></span></td>
<td><span data-ttu-id="e7b5c-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e7b5c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e7b5c-604">535.31</span></span></td>
<td><span data-ttu-id="e7b5c-605">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-606">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-607">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-608">20</span><span class="sxs-lookup"><span data-stu-id="e7b5c-608">20</span></span></td>
<td><span data-ttu-id="e7b5c-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e7b5c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e7b5c-610">178.44</span></span></td>
<td><span data-ttu-id="e7b5c-611">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-612">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-613">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-614">60</span><span class="sxs-lookup"><span data-stu-id="e7b5c-614">60</span></span></td>
<td><span data-ttu-id="e7b5c-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e7b5c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e7b5c-616">4,487.12</span></span></td>
<td><span data-ttu-id="e7b5c-617">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-618">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-619">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-620">20</span><span class="sxs-lookup"><span data-stu-id="e7b5c-620">20</span></span></td>
<td><span data-ttu-id="e7b5c-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e7b5c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-622">1,495.71</span></span></td>
<td><span data-ttu-id="e7b5c-623">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7b5c-624">Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).</span><span class="sxs-lookup"><span data-stu-id="e7b5c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-625">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-625">Cost object</span></span></th>
<th><span data-ttu-id="e7b5c-626">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e7b5c-626">Magnitude</span></span></th>
<th><span data-ttu-id="e7b5c-627">Tildelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7b5c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e7b5c-628">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-628">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-629">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-630">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-631">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-632">80</span><span class="sxs-lookup"><span data-stu-id="e7b5c-632">80</span></span></td>
<td><span data-ttu-id="e7b5c-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e7b5c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e7b5c-634">241.05</span></span></td>
<td><span data-ttu-id="e7b5c-635">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-636">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-637">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-638">15</span><span class="sxs-lookup"><span data-stu-id="e7b5c-638">15</span></span></td>
<td><span data-ttu-id="e7b5c-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e7b5c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e7b5c-640">45.20</span></span></td>
<td><span data-ttu-id="e7b5c-641">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-642">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-643">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-644">80</span><span class="sxs-lookup"><span data-stu-id="e7b5c-644">80</span></span></td>
<td><span data-ttu-id="e7b5c-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e7b5c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e7b5c-646">2,507.09</span></span></td>
<td><span data-ttu-id="e7b5c-647">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-648">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-649">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-650">15</span><span class="sxs-lookup"><span data-stu-id="e7b5c-650">15</span></span></td>
<td><span data-ttu-id="e7b5c-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e7b5c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e7b5c-652">470.08</span></span></td>
<td><span data-ttu-id="e7b5c-653">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e7b5c-654">Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-655">Journalen</span><span class="sxs-lookup"><span data-stu-id="e7b5c-655">Journal</span></span></th>
<th><span data-ttu-id="e7b5c-656">Journaltype</span><span class="sxs-lookup"><span data-stu-id="e7b5c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7b5c-657">Økonomisk kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7b5c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7b5c-658">Versjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-659">00004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-659">00004</span></span></td>
<td><span data-ttu-id="e7b5c-660">Kostfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="e7b5c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e7b5c-661">Skattemessig</span><span class="sxs-lookup"><span data-stu-id="e7b5c-661">Fiscal</span></span></td>
<td><span data-ttu-id="e7b5c-662">2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-662">2017</span></span></td>
<td><span data-ttu-id="e7b5c-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-663">Period 1</span></span></td>
<td><span data-ttu-id="e7b5c-664">Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e7b5c-665">Journallinjer</span><span class="sxs-lookup"><span data-stu-id="e7b5c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7b5c-666">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-667">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-668">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-668">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-669">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-670">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-672">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-673">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-673">HR</span></span></td>
<td><span data-ttu-id="e7b5c-674">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-674">10001</span></span></td>
<td><span data-ttu-id="e7b5c-675">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-675">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-676">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-677">500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-679">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-680">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-680">HR</span></span></td>
<td><span data-ttu-id="e7b5c-681">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-681">10001</span></span></td>
<td><span data-ttu-id="e7b5c-682">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-682">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-683">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-683">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-686">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-687">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-687">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-688">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-688">10001</span></span></td>
<td><span data-ttu-id="e7b5c-689">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-689">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-690">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-693">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-694">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-694">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-695">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-695">10001</span></span></td>
<td><span data-ttu-id="e7b5c-696">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-696">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-697">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-697">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e7b5c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-700">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-701">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-701">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-702">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-702">10001</span></span></td>
<td><span data-ttu-id="e7b5c-703">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-703">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-704">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e7b5c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-707">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-708">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-708">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-709">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-709">10001</span></span></td>
<td><span data-ttu-id="e7b5c-710">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-710">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-711">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-711">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e7b5c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-714">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-715">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-715">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-716">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-716">10001</span></span></td>
<td><span data-ttu-id="e7b5c-717">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-717">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-718">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e7b5c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-721">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-722">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-722">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-723">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-723">10001</span></span></td>
<td><span data-ttu-id="e7b5c-724">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-724">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-725">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-725">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e7b5c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-728">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-729">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-730">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-730">10001</span></span></td>
<td><span data-ttu-id="e7b5c-731">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-731">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-732">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e7b5c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-735">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-736">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-737">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-737">10001</span></span></td>
<td><span data-ttu-id="e7b5c-738">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-738">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-739">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-739">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e7b5c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-742">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-743">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-744">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-744">10001</span></span></td>
<td><span data-ttu-id="e7b5c-745">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-745">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-746">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e7b5c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7b5c-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-749">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-750">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-751">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-751">10001</span></span></td>
<td><span data-ttu-id="e7b5c-752">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-752">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-753">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-753">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e7b5c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7b5c-755">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="e7b5c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7b5c-756">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7b5c-757">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-757">Cost element</span></span></th>
<th><span data-ttu-id="e7b5c-758">Kostnadsatferd</span><span class="sxs-lookup"><span data-stu-id="e7b5c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e7b5c-759">Beløp</span><span class="sxs-lookup"><span data-stu-id="e7b5c-759">Amount</span></span></th>
<th><span data-ttu-id="e7b5c-760">Regnskapsdato</span><span class="sxs-lookup"><span data-stu-id="e7b5c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7b5c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-761">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-762">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-762">HR</span></span></td>
<td><span data-ttu-id="e7b5c-763">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-763">10001</span></span></td>
<td><span data-ttu-id="e7b5c-764">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-764">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-765">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-766">-500.00</span></span></td>
<td><span data-ttu-id="e7b5c-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-768">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-769">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-769">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-770">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-770">10001</span></span></td>
<td><span data-ttu-id="e7b5c-771">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-771">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-772">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-773">175.00</span></span></td>
<td><span data-ttu-id="e7b5c-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-775">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-776">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-776">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-777">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-777">10001</span></span></td>
<td><span data-ttu-id="e7b5c-778">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-778">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-779">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-780">275.00</span></span></td>
<td><span data-ttu-id="e7b5c-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-782">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-783">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-783">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-784">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-784">10001</span></span></td>
<td><span data-ttu-id="e7b5c-785">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-785">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-786">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-787">50,00</span></span></td>
<td><span data-ttu-id="e7b5c-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-789">CC001</span></span></td>
<td><span data-ttu-id="e7b5c-790">Personale</span><span class="sxs-lookup"><span data-stu-id="e7b5c-790">HR</span></span></td>
<td><span data-ttu-id="e7b5c-791">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-791">10001</span></span></td>
<td><span data-ttu-id="e7b5c-792">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-792">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-793">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-793">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e7b5c-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-796">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-797">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-797">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-798">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-798">10001</span></span></td>
<td><span data-ttu-id="e7b5c-799">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-799">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-800">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-800">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-801">436.00</span></span></td>
<td><span data-ttu-id="e7b5c-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-803">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-804">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-804">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-805">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-805">10001</span></span></td>
<td><span data-ttu-id="e7b5c-806">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-806">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-807">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-807">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e7b5c-808">685.14</span></span></td>
<td><span data-ttu-id="e7b5c-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-810">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-811">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-811">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-812">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-812">10001</span></span></td>
<td><span data-ttu-id="e7b5c-813">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-813">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-814">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-814">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e7b5c-815">124.57</span></span></td>
<td><span data-ttu-id="e7b5c-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-817">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-818">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-818">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-819">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-819">10001</span></span></td>
<td><span data-ttu-id="e7b5c-820">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-820">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-821">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-822">-675.00</span></span></td>
<td><span data-ttu-id="e7b5c-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-824">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-825">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-825">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-826">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-826">10001</span></span></td>
<td><span data-ttu-id="e7b5c-827">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-827">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-828">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e7b5c-829">438.75</span></span></td>
<td><span data-ttu-id="e7b5c-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-831">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-832">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-832">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-833">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-833">10001</span></span></td>
<td><span data-ttu-id="e7b5c-834">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-834">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-835">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e7b5c-836">236.25</span></span></td>
<td><span data-ttu-id="e7b5c-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-838">CC002</span></span></td>
<td><span data-ttu-id="e7b5c-839">Finans</span><span class="sxs-lookup"><span data-stu-id="e7b5c-839">Finance</span></span></td>
<td><span data-ttu-id="e7b5c-840">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-840">10001</span></span></td>
<td><span data-ttu-id="e7b5c-841">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-841">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-842">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-842">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="e7b5c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e7b5c-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-845">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-846">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-846">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-847">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-847">10001</span></span></td>
<td><span data-ttu-id="e7b5c-848">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-848">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-849">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-849">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e7b5c-850">5,297.69</span></span></td>
<td><span data-ttu-id="e7b5c-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-852">CC004</span></span></td>
<td><span data-ttu-id="e7b5c-853">Innpakning</span><span class="sxs-lookup"><span data-stu-id="e7b5c-853">Packaging</span></span></td>
<td><span data-ttu-id="e7b5c-854">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-854">10001</span></span></td>
<td><span data-ttu-id="e7b5c-855">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-855">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-856">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-856">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e7b5c-857">2,852.60</span></span></td>
<td><span data-ttu-id="e7b5c-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-859">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-860">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-860">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-861">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-861">10001</span></span></td>
<td><span data-ttu-id="e7b5c-862">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-862">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-863">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="e7b5c-864">-713.75</span></span></td>
<td><span data-ttu-id="e7b5c-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-866">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-867">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-868">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-868">10001</span></span></td>
<td><span data-ttu-id="e7b5c-869">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-869">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-870">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e7b5c-871">535.31</span></span></td>
<td><span data-ttu-id="e7b5c-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-873">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-874">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-875">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-875">10001</span></span></td>
<td><span data-ttu-id="e7b5c-876">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-876">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-877">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e7b5c-878">178.44</span></span></td>
<td><span data-ttu-id="e7b5c-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-880">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-881">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-881">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-882">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-882">10001</span></span></td>
<td><span data-ttu-id="e7b5c-883">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-883">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-884">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-884">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="e7b5c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e7b5c-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-887">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-888">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-889">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-889">10001</span></span></td>
<td><span data-ttu-id="e7b5c-890">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-890">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-891">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-891">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e7b5c-892">4,487.12</span></span></td>
<td><span data-ttu-id="e7b5c-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-894">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-895">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-896">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-896">10001</span></span></td>
<td><span data-ttu-id="e7b5c-897">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-897">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-898">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-898">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e7b5c-899">1,495.71</span></span></td>
<td><span data-ttu-id="e7b5c-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-901">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-902">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-902">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-903">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-903">10001</span></span></td>
<td><span data-ttu-id="e7b5c-904">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-904">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-905">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="e7b5c-906">-286.25</span></span></td>
<td><span data-ttu-id="e7b5c-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-908">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-909">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-910">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-910">10001</span></span></td>
<td><span data-ttu-id="e7b5c-911">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-911">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-912">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e7b5c-913">241.05</span></span></td>
<td><span data-ttu-id="e7b5c-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-915">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-916">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-917">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-917">10001</span></span></td>
<td><span data-ttu-id="e7b5c-918">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-918">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-919">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e7b5c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e7b5c-920">45.20</span></span></td>
<td><span data-ttu-id="e7b5c-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-922">CC003</span></span></td>
<td><span data-ttu-id="e7b5c-923">Samling</span><span class="sxs-lookup"><span data-stu-id="e7b5c-923">Assembly</span></span></td>
<td><span data-ttu-id="e7b5c-924">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-924">10001</span></span></td>
<td><span data-ttu-id="e7b5c-925">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-925">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-926">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-926">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-927">-2 977,17</span><span class="sxs-lookup"><span data-stu-id="e7b5c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e7b5c-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-929">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-929">Prod 1</span></span></td>
<td><span data-ttu-id="e7b5c-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-930">Product 1</span></span></td>
<td><span data-ttu-id="e7b5c-931">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-931">10001</span></span></td>
<td><span data-ttu-id="e7b5c-932">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-932">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-933">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-933">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e7b5c-934">2,507.09</span></span></td>
<td><span data-ttu-id="e7b5c-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7b5c-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-936">Prod 2</span></span></td>
<td><span data-ttu-id="e7b5c-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-937">Product 2</span></span></td>
<td><span data-ttu-id="e7b5c-938">10001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-938">10001</span></span></td>
<td><span data-ttu-id="e7b5c-939">Elektrisitet</span><span class="sxs-lookup"><span data-stu-id="e7b5c-939">Electricity</span></span></td>
<td><span data-ttu-id="e7b5c-940">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-940">Variable cost</span></span></td>
<td><span data-ttu-id="e7b5c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e7b5c-941">470.08</span></span></td>
<td><span data-ttu-id="e7b5c-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7b5c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e7b5c-943">Konklusjon</span><span class="sxs-lookup"><span data-stu-id="e7b5c-943">Conclusion</span></span>
<span data-ttu-id="e7b5c-944">I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e7b5c-945">Derfor vet regnskapsførere at denne kostnaden må tildeles.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e7b5c-946">I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e7b5c-947">Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e7b5c-948">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="e7b5c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e7b5c-949">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7b5c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e7b5c-950">Sum</span><span class="sxs-lookup"><span data-stu-id="e7b5c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e7b5c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e7b5c-951">CC099</span></span></th>
<th><span data-ttu-id="e7b5c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e7b5c-952">CC001</span></span></th>
<th><span data-ttu-id="e7b5c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e7b5c-953">CC002</span></span></th>
<th><span data-ttu-id="e7b5c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e7b5c-954">CC003</span></span></th>
<th><span data-ttu-id="e7b5c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e7b5c-955">CC004</span></span></th>
<th><span data-ttu-id="e7b5c-956">Prosj 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-956">Proj 1</span></span></th>
<th><span data-ttu-id="e7b5c-957">Prosj 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-957">Proj 2</span></span></th>
<th><span data-ttu-id="e7b5c-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7b5c-958">Prod 1</span></span></th>
<th><span data-ttu-id="e7b5c-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7b5c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e7b5c-960">10001 Strøm</span><span class="sxs-lookup"><span data-stu-id="e7b5c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e7b5c-970">Uklassifisert</span><span class="sxs-lookup"><span data-stu-id="e7b5c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e7b5c-972">Fast kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e7b5c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e7b5c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e7b5c-981">Variabel kostnad</span><span class="sxs-lookup"><span data-stu-id="e7b5c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-982">000</span><span class="sxs-lookup"><span data-stu-id="e7b5c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-987">30,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e7b5c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e7b5c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e7b5c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7b5c-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e7b5c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e7b5c-992">Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e7b5c-993">Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e7b5c-994">Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e7b5c-995">Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten.</span><span class="sxs-lookup"><span data-stu-id="e7b5c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e7b5c-996">Hvis du vil ha mer informasjon, se [Policy for opprullet kost og beregning av administrasjonskostnader](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="e7b5c-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



