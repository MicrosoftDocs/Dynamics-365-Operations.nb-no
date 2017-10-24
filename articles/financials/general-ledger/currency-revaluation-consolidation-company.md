---
title: Revaluering av valuta i et konsolideringsfirma
description: "Dette emnet beskriver hvordan å revaluere valuta i et konsolideringsselskap."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c91399e96c54f7cf9968a15e3fff90c3a71ca6
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="0cf79-103">Revaluering av valuta i et konsolideringsfirma</span><span class="sxs-lookup"><span data-stu-id="0cf79-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="0cf79-104">Når du konsoliderer data fra én regnskapsvaluta til en annen, du må fortsatt kjøre valutarevaluering hvis det er endringer i valutakurser, slik at kontosaldoene revalueres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="0cf79-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="0cf79-105">Når du konsoliderer de opprinnelig dataene, kan du bruke kategorien **Omveksling av valuta** for å velge de opprinnelige valutakursene for omveksling i løpet av konsolideringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="0cf79-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="0cf79-106">Når en ny valutakurs angis (for eksempel i neste måned), må du revaluere kontosaldoene.</span><span class="sxs-lookup"><span data-stu-id="0cf79-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="0cf79-107">Urealisert fortjeneste og tap oppdateres deretter tilsvarende, basert på den nye valutakursen og datoen.</span><span class="sxs-lookup"><span data-stu-id="0cf79-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="0cf79-108">Eksemplet nedenfor illustrerer regnskapsoppføringer som opprettes under prosessen.</span><span class="sxs-lookup"><span data-stu-id="0cf79-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="0cf79-109">Firmaoppsett</span><span class="sxs-lookup"><span data-stu-id="0cf79-109">Company setup</span></span>
-   <span data-ttu-id="0cf79-110">**Kilde/driftsselskap (USMF)** – Amerikanske dollar (USD) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="0cf79-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="0cf79-111">**Konsolidert firma (CON)** – Euro (EUR) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="0cf79-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="0cf79-112">**Realisert fortjeneste ** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="0cf79-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="0cf79-113">**Realisert tap** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="0cf79-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="0cf79-114">**Urealisert fortjeneste** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="0cf79-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="0cf79-115">**Urealisert tap** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="0cf79-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="0cf79-116">Opprinnelige transaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cf79-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="0cf79-117">Kontantmottakstransaksjoner i USMF</span><span class="sxs-lookup"><span data-stu-id="0cf79-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="0cf79-118">Dato</span><span class="sxs-lookup"><span data-stu-id="0cf79-118">Date</span></span>       | <span data-ttu-id="0cf79-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="0cf79-119">Ledger account</span></span>               | <span data-ttu-id="0cf79-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="0cf79-120">Currency</span></span> | <span data-ttu-id="0cf79-121">Beløp</span><span class="sxs-lookup"><span data-stu-id="0cf79-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="0cf79-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-122">10/11/2015</span></span> | <span data-ttu-id="0cf79-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="0cf79-123">110110 – Cash</span></span>                | <span data-ttu-id="0cf79-124">USD</span><span class="sxs-lookup"><span data-stu-id="0cf79-124">USD</span></span>      | <span data-ttu-id="0cf79-125">500</span><span class="sxs-lookup"><span data-stu-id="0cf79-125">500</span></span>    |
| <span data-ttu-id="0cf79-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-126">10/11/2015</span></span> | <span data-ttu-id="0cf79-127">130100 – Kunder</span><span class="sxs-lookup"><span data-stu-id="0cf79-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="0cf79-128">USD</span><span class="sxs-lookup"><span data-stu-id="0cf79-128">USD</span></span>      | <span data-ttu-id="0cf79-129">-500</span><span class="sxs-lookup"><span data-stu-id="0cf79-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="0cf79-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="0cf79-130">Exchange rates</span></span>
| <span data-ttu-id="0cf79-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="0cf79-131">From currency</span></span> | <span data-ttu-id="0cf79-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="0cf79-132">To currency</span></span> | <span data-ttu-id="0cf79-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="0cf79-133">Start date</span></span> | <span data-ttu-id="0cf79-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="0cf79-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="0cf79-135">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-135">EUR</span></span>           | <span data-ttu-id="0cf79-136">USD</span><span class="sxs-lookup"><span data-stu-id="0cf79-136">USD</span></span>         | <span data-ttu-id="0cf79-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-137">10/1/2015</span></span>  | <span data-ttu-id="0cf79-138">200</span><span class="sxs-lookup"><span data-stu-id="0cf79-138">200</span></span>           |
| <span data-ttu-id="0cf79-139">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-139">EUR</span></span>           | <span data-ttu-id="0cf79-140">USD</span><span class="sxs-lookup"><span data-stu-id="0cf79-140">USD</span></span>         | <span data-ttu-id="0cf79-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-141">11/1/2015</span></span>  | <span data-ttu-id="0cf79-142">150</span><span class="sxs-lookup"><span data-stu-id="0cf79-142">150</span></span>           |
| <span data-ttu-id="0cf79-143">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-143">EUR</span></span>           | <span data-ttu-id="0cf79-144">USD</span><span class="sxs-lookup"><span data-stu-id="0cf79-144">USD</span></span>         | <span data-ttu-id="0cf79-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="0cf79-145">12/1/2012</span></span>  | <span data-ttu-id="0cf79-146">100</span><span class="sxs-lookup"><span data-stu-id="0cf79-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="0cf79-147">Utfør konsolideringen for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0cf79-148">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="0cf79-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="0cf79-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="0cf79-149">Ledger account</span></span> | <span data-ttu-id="0cf79-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="0cf79-150">Currency</span></span> | <span data-ttu-id="0cf79-151">Beløp</span><span class="sxs-lookup"><span data-stu-id="0cf79-151">Amount</span></span> | <span data-ttu-id="0cf79-152">Beregning</span><span class="sxs-lookup"><span data-stu-id="0cf79-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="0cf79-153">110110</span><span class="sxs-lookup"><span data-stu-id="0cf79-153">110110</span></span>         | <span data-ttu-id="0cf79-154">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-154">EUR</span></span>      | <span data-ttu-id="0cf79-155">250</span><span class="sxs-lookup"><span data-stu-id="0cf79-155">250</span></span>    | <span data-ttu-id="0cf79-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="0cf79-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="0cf79-157">130100</span><span class="sxs-lookup"><span data-stu-id="0cf79-157">130100</span></span>         | <span data-ttu-id="0cf79-158">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-158">EUR</span></span>      | <span data-ttu-id="0cf79-159">-250</span><span class="sxs-lookup"><span data-stu-id="0cf79-159">-250</span></span>   | <span data-ttu-id="0cf79-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="0cf79-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="0cf79-161">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0cf79-162">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="0cf79-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="0cf79-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="0cf79-163">Ledger account</span></span> | <span data-ttu-id="0cf79-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="0cf79-164">Currency</span></span> | <span data-ttu-id="0cf79-165">Beløp</span><span class="sxs-lookup"><span data-stu-id="0cf79-165">Amount</span></span>  | <span data-ttu-id="0cf79-166">Beregning</span><span class="sxs-lookup"><span data-stu-id="0cf79-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="0cf79-167">110110</span><span class="sxs-lookup"><span data-stu-id="0cf79-167">110110</span></span>         | <span data-ttu-id="0cf79-168">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-168">EUR</span></span>      | <span data-ttu-id="0cf79-169">333.33</span><span class="sxs-lookup"><span data-stu-id="0cf79-169">333.33</span></span>  | <span data-ttu-id="0cf79-170">Opprinnelig beløp 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="0cf79-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="0cf79-171">130100</span><span class="sxs-lookup"><span data-stu-id="0cf79-171">130100</span></span>         | <span data-ttu-id="0cf79-172">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-172">EUR</span></span>      | <span data-ttu-id="0cf79-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="0cf79-173">-333.33</span></span> | <span data-ttu-id="0cf79-174">Opprinnelig beløp -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="0cf79-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="0cf79-175">801400</span><span class="sxs-lookup"><span data-stu-id="0cf79-175">801400</span></span>         | <span data-ttu-id="0cf79-176">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-176">EUR</span></span>      | <span data-ttu-id="0cf79-177">83.33</span><span class="sxs-lookup"><span data-stu-id="0cf79-177">83.33</span></span>   | <span data-ttu-id="0cf79-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="0cf79-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="0cf79-179">801600</span><span class="sxs-lookup"><span data-stu-id="0cf79-179">801600</span></span>         | <span data-ttu-id="0cf79-180">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-180">EUR</span></span>      | <span data-ttu-id="0cf79-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="0cf79-181">-83.33</span></span>  | <span data-ttu-id="0cf79-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="0cf79-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="0cf79-183">Du vil se tilleggstransaksjoner for rapporteringsvalutabeløpene.</span><span class="sxs-lookup"><span data-stu-id="0cf79-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="0cf79-184">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 31. desember 2015</span><span class="sxs-lookup"><span data-stu-id="0cf79-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0cf79-185">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="0cf79-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="0cf79-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="0cf79-186">Ledger account</span></span> | <span data-ttu-id="0cf79-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="0cf79-187">Currency</span></span> | <span data-ttu-id="0cf79-188">Beløp</span><span class="sxs-lookup"><span data-stu-id="0cf79-188">Amount</span></span>  | <span data-ttu-id="0cf79-189">Beregning</span><span class="sxs-lookup"><span data-stu-id="0cf79-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="0cf79-190">110110</span><span class="sxs-lookup"><span data-stu-id="0cf79-190">110110</span></span>         | <span data-ttu-id="0cf79-191">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-191">EUR</span></span>      | <span data-ttu-id="0cf79-192">500,00</span><span class="sxs-lookup"><span data-stu-id="0cf79-192">500.00</span></span>  | <span data-ttu-id="0cf79-193">Opprinnelig beløp 500 × 1</span><span class="sxs-lookup"><span data-stu-id="0cf79-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="0cf79-194">130100</span><span class="sxs-lookup"><span data-stu-id="0cf79-194">130100</span></span>         | <span data-ttu-id="0cf79-195">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-195">EUR</span></span>      | <span data-ttu-id="0cf79-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="0cf79-196">-500.00</span></span> | <span data-ttu-id="0cf79-197">Opprinnelig beløp -500 × 1</span><span class="sxs-lookup"><span data-stu-id="0cf79-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="0cf79-198">801400</span><span class="sxs-lookup"><span data-stu-id="0cf79-198">801400</span></span>         | <span data-ttu-id="0cf79-199">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-199">EUR</span></span>      | <span data-ttu-id="0cf79-200">250</span><span class="sxs-lookup"><span data-stu-id="0cf79-200">250</span></span>     | <span data-ttu-id="0cf79-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="0cf79-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="0cf79-202">801600</span><span class="sxs-lookup"><span data-stu-id="0cf79-202">801600</span></span>         | <span data-ttu-id="0cf79-203">EUR</span><span class="sxs-lookup"><span data-stu-id="0cf79-203">EUR</span></span>      | <span data-ttu-id="0cf79-204">-250</span><span class="sxs-lookup"><span data-stu-id="0cf79-204">-250</span></span>    | <span data-ttu-id="0cf79-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="0cf79-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






