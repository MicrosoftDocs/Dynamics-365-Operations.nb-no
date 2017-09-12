---
title: Revaluering av valuta i et konsolideringsfirma
description: 
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="48fd0-102">Revaluering av valuta i et konsolideringsfirma</span><span class="sxs-lookup"><span data-stu-id="48fd0-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="48fd0-103">Når du konsoliderer data fra én regnskapsvaluta til en annen, du må fortsatt kjøre valutarevaluering hvis det er endringer i valutakurser, slik at kontosaldoene revalueres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="48fd0-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="48fd0-104">Når du konsoliderer de opprinnelig dataene, kan du bruke kategorien **Omveksling av valuta** for å velge de opprinnelige valutakursene for omveksling i løpet av konsolideringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="48fd0-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="48fd0-105">Når en ny valutakurs angis (for eksempel i neste måned), må du revaluere kontosaldoene.</span><span class="sxs-lookup"><span data-stu-id="48fd0-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="48fd0-106">Urealisert fortjeneste og tap oppdateres deretter tilsvarende, basert på den nye valutakursen og datoen.</span><span class="sxs-lookup"><span data-stu-id="48fd0-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="48fd0-107">Eksemplet nedenfor illustrerer regnskapsoppføringer som opprettes under prosessen.</span><span class="sxs-lookup"><span data-stu-id="48fd0-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="48fd0-108">Firmaoppsett</span><span class="sxs-lookup"><span data-stu-id="48fd0-108">Company setup</span></span>
-   <span data-ttu-id="48fd0-109">**Kilde/driftsselskap (USMF)** – Amerikanske dollar (USD) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="48fd0-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="48fd0-110">**Konsolidert firma (CON)** – Euro (EUR) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="48fd0-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="48fd0-111">**Realisert fortjeneste ** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="48fd0-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="48fd0-112">**Realisert tap** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="48fd0-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="48fd0-113">**Urealisert fortjeneste** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="48fd0-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="48fd0-114">**Urealisert tap** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="48fd0-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="48fd0-115">Opprinnelige transaksjoner</span><span class="sxs-lookup"><span data-stu-id="48fd0-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="48fd0-116">Kontantmottakstransaksjoner i USMF</span><span class="sxs-lookup"><span data-stu-id="48fd0-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="48fd0-117">Dato</span><span class="sxs-lookup"><span data-stu-id="48fd0-117">Date</span></span>       | <span data-ttu-id="48fd0-118">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="48fd0-118">Ledger account</span></span>               | <span data-ttu-id="48fd0-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="48fd0-119">Currency</span></span> | <span data-ttu-id="48fd0-120">Beløp</span><span class="sxs-lookup"><span data-stu-id="48fd0-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="48fd0-121">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-121">10/11/2015</span></span> | <span data-ttu-id="48fd0-122">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="48fd0-122">110110 – Cash</span></span>                | <span data-ttu-id="48fd0-123">USD</span><span class="sxs-lookup"><span data-stu-id="48fd0-123">USD</span></span>      | <span data-ttu-id="48fd0-124">500</span><span class="sxs-lookup"><span data-stu-id="48fd0-124">500</span></span>    |
| <span data-ttu-id="48fd0-125">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-125">10/11/2015</span></span> | <span data-ttu-id="48fd0-126">130100 – Kunder</span><span class="sxs-lookup"><span data-stu-id="48fd0-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="48fd0-127">USD</span><span class="sxs-lookup"><span data-stu-id="48fd0-127">USD</span></span>      | <span data-ttu-id="48fd0-128">-500</span><span class="sxs-lookup"><span data-stu-id="48fd0-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="48fd0-129">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="48fd0-129">Exchange rates</span></span>
| <span data-ttu-id="48fd0-130">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="48fd0-130">From currency</span></span> | <span data-ttu-id="48fd0-131">Til valuta</span><span class="sxs-lookup"><span data-stu-id="48fd0-131">To currency</span></span> | <span data-ttu-id="48fd0-132">Startdato</span><span class="sxs-lookup"><span data-stu-id="48fd0-132">Start date</span></span> | <span data-ttu-id="48fd0-133">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="48fd0-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="48fd0-134">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-134">EUR</span></span>           | <span data-ttu-id="48fd0-135">USD</span><span class="sxs-lookup"><span data-stu-id="48fd0-135">USD</span></span>         | <span data-ttu-id="48fd0-136">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-136">10/1/2015</span></span>  | <span data-ttu-id="48fd0-137">200</span><span class="sxs-lookup"><span data-stu-id="48fd0-137">200</span></span>           |
| <span data-ttu-id="48fd0-138">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-138">EUR</span></span>           | <span data-ttu-id="48fd0-139">USD</span><span class="sxs-lookup"><span data-stu-id="48fd0-139">USD</span></span>         | <span data-ttu-id="48fd0-140">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-140">11/1/2015</span></span>  | <span data-ttu-id="48fd0-141">150</span><span class="sxs-lookup"><span data-stu-id="48fd0-141">150</span></span>           |
| <span data-ttu-id="48fd0-142">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-142">EUR</span></span>           | <span data-ttu-id="48fd0-143">USD</span><span class="sxs-lookup"><span data-stu-id="48fd0-143">USD</span></span>         | <span data-ttu-id="48fd0-144">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="48fd0-144">12/1/2012</span></span>  | <span data-ttu-id="48fd0-145">100</span><span class="sxs-lookup"><span data-stu-id="48fd0-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="48fd0-146">Utfør konsolideringen for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="48fd0-147">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="48fd0-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="48fd0-148">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="48fd0-148">Ledger account</span></span> | <span data-ttu-id="48fd0-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="48fd0-149">Currency</span></span> | <span data-ttu-id="48fd0-150">Beløp</span><span class="sxs-lookup"><span data-stu-id="48fd0-150">Amount</span></span> | <span data-ttu-id="48fd0-151">Beregning</span><span class="sxs-lookup"><span data-stu-id="48fd0-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="48fd0-152">110110</span><span class="sxs-lookup"><span data-stu-id="48fd0-152">110110</span></span>         | <span data-ttu-id="48fd0-153">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-153">EUR</span></span>      | <span data-ttu-id="48fd0-154">250</span><span class="sxs-lookup"><span data-stu-id="48fd0-154">250</span></span>    | <span data-ttu-id="48fd0-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="48fd0-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="48fd0-156">130100</span><span class="sxs-lookup"><span data-stu-id="48fd0-156">130100</span></span>         | <span data-ttu-id="48fd0-157">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-157">EUR</span></span>      | <span data-ttu-id="48fd0-158">-250</span><span class="sxs-lookup"><span data-stu-id="48fd0-158">-250</span></span>   | <span data-ttu-id="48fd0-159">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="48fd0-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="48fd0-160">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="48fd0-161">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="48fd0-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="48fd0-162">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="48fd0-162">Ledger account</span></span> | <span data-ttu-id="48fd0-163">Valuta</span><span class="sxs-lookup"><span data-stu-id="48fd0-163">Currency</span></span> | <span data-ttu-id="48fd0-164">Beløp</span><span class="sxs-lookup"><span data-stu-id="48fd0-164">Amount</span></span>  | <span data-ttu-id="48fd0-165">Beregning</span><span class="sxs-lookup"><span data-stu-id="48fd0-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="48fd0-166">110110</span><span class="sxs-lookup"><span data-stu-id="48fd0-166">110110</span></span>         | <span data-ttu-id="48fd0-167">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-167">EUR</span></span>      | <span data-ttu-id="48fd0-168">333.33</span><span class="sxs-lookup"><span data-stu-id="48fd0-168">333.33</span></span>  | <span data-ttu-id="48fd0-169">Opprinnelig beløp 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="48fd0-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="48fd0-170">130100</span><span class="sxs-lookup"><span data-stu-id="48fd0-170">130100</span></span>         | <span data-ttu-id="48fd0-171">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-171">EUR</span></span>      | <span data-ttu-id="48fd0-172">-333,33</span><span class="sxs-lookup"><span data-stu-id="48fd0-172">-333.33</span></span> | <span data-ttu-id="48fd0-173">Opprinnelig beløp -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="48fd0-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="48fd0-174">801400</span><span class="sxs-lookup"><span data-stu-id="48fd0-174">801400</span></span>         | <span data-ttu-id="48fd0-175">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-175">EUR</span></span>      | <span data-ttu-id="48fd0-176">83.33</span><span class="sxs-lookup"><span data-stu-id="48fd0-176">83.33</span></span>   | <span data-ttu-id="48fd0-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="48fd0-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="48fd0-178">801600</span><span class="sxs-lookup"><span data-stu-id="48fd0-178">801600</span></span>         | <span data-ttu-id="48fd0-179">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-179">EUR</span></span>      | <span data-ttu-id="48fd0-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="48fd0-180">-83.33</span></span>  | <span data-ttu-id="48fd0-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="48fd0-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="48fd0-182">Du vil se tilleggstransaksjoner for rapporteringsvalutabeløpene.</span><span class="sxs-lookup"><span data-stu-id="48fd0-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="48fd0-183">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 31. desember 2015</span><span class="sxs-lookup"><span data-stu-id="48fd0-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="48fd0-184">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="48fd0-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="48fd0-185">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="48fd0-185">Ledger account</span></span> | <span data-ttu-id="48fd0-186">Valuta</span><span class="sxs-lookup"><span data-stu-id="48fd0-186">Currency</span></span> | <span data-ttu-id="48fd0-187">Beløp</span><span class="sxs-lookup"><span data-stu-id="48fd0-187">Amount</span></span>  | <span data-ttu-id="48fd0-188">Beregning</span><span class="sxs-lookup"><span data-stu-id="48fd0-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="48fd0-189">110110</span><span class="sxs-lookup"><span data-stu-id="48fd0-189">110110</span></span>         | <span data-ttu-id="48fd0-190">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-190">EUR</span></span>      | <span data-ttu-id="48fd0-191">500,00</span><span class="sxs-lookup"><span data-stu-id="48fd0-191">500.00</span></span>  | <span data-ttu-id="48fd0-192">Opprinnelig beløp 500 × 1</span><span class="sxs-lookup"><span data-stu-id="48fd0-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="48fd0-193">130100</span><span class="sxs-lookup"><span data-stu-id="48fd0-193">130100</span></span>         | <span data-ttu-id="48fd0-194">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-194">EUR</span></span>      | <span data-ttu-id="48fd0-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="48fd0-195">-500.00</span></span> | <span data-ttu-id="48fd0-196">Opprinnelig beløp -500 × 1</span><span class="sxs-lookup"><span data-stu-id="48fd0-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="48fd0-197">801400</span><span class="sxs-lookup"><span data-stu-id="48fd0-197">801400</span></span>         | <span data-ttu-id="48fd0-198">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-198">EUR</span></span>      | <span data-ttu-id="48fd0-199">250</span><span class="sxs-lookup"><span data-stu-id="48fd0-199">250</span></span>     | <span data-ttu-id="48fd0-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="48fd0-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="48fd0-201">801600</span><span class="sxs-lookup"><span data-stu-id="48fd0-201">801600</span></span>         | <span data-ttu-id="48fd0-202">EUR</span><span class="sxs-lookup"><span data-stu-id="48fd0-202">EUR</span></span>      | <span data-ttu-id="48fd0-203">-250</span><span class="sxs-lookup"><span data-stu-id="48fd0-203">-250</span></span>    | <span data-ttu-id="48fd0-204">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="48fd0-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






