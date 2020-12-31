---
title: Revaluering av valuta i et konsolideringsfirma
description: Dette emnet beskriver hvordan å revaluere valuta i et konsolideringsselskap.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4446564"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="b2432-103">Revaluering av valuta i et konsolideringsfirma</span><span class="sxs-lookup"><span data-stu-id="b2432-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2432-104">Når du konsoliderer data fra én regnskapsvaluta til en annen, du må fortsatt kjøre valutarevaluering hvis det er endringer i valutakurser, slik at kontosaldoene revalueres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="b2432-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="b2432-105">Når du konsoliderer de opprinnelig dataene, kan du bruke kategorien **Omveksling av valuta** for å velge de opprinnelige valutakursene for omveksling i løpet av konsolideringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b2432-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="b2432-106">Når en ny valutakurs angis (for eksempel i neste måned), må du revaluere kontosaldoene.</span><span class="sxs-lookup"><span data-stu-id="b2432-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="b2432-107">Urealisert fortjeneste og tap oppdateres deretter tilsvarende, basert på den nye valutakursen og datoen.</span><span class="sxs-lookup"><span data-stu-id="b2432-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="b2432-108">Eksemplet nedenfor illustrerer regnskapsoppføringer som opprettes under prosessen.</span><span class="sxs-lookup"><span data-stu-id="b2432-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="b2432-109">Firmaoppsett</span><span class="sxs-lookup"><span data-stu-id="b2432-109">Company setup</span></span>
-   <span data-ttu-id="b2432-110">**Kilde/driftsselskap (USMF)** – Amerikanske dollar (USD) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="b2432-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="b2432-111">**Konsolidert firma (CON)** – Euro (EUR) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="b2432-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="b2432-112">**Realisert fortjeneste** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="b2432-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="b2432-113">**Realisert tap** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="b2432-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="b2432-114">**Urealisert fortjeneste** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="b2432-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="b2432-115">**Urealisert tap** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="b2432-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="b2432-116">Opprinnelige transaksjoner</span><span class="sxs-lookup"><span data-stu-id="b2432-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="b2432-117">Kontantmottakstransaksjoner i USMF</span><span class="sxs-lookup"><span data-stu-id="b2432-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="b2432-118">Dato</span><span class="sxs-lookup"><span data-stu-id="b2432-118">Date</span></span>       | <span data-ttu-id="b2432-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="b2432-119">Ledger account</span></span>               | <span data-ttu-id="b2432-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="b2432-120">Currency</span></span> | <span data-ttu-id="b2432-121">Beløp</span><span class="sxs-lookup"><span data-stu-id="b2432-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="b2432-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="b2432-122">10/11/2015</span></span> | <span data-ttu-id="b2432-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="b2432-123">110110 – Cash</span></span>                | <span data-ttu-id="b2432-124">USD</span><span class="sxs-lookup"><span data-stu-id="b2432-124">USD</span></span>      | <span data-ttu-id="b2432-125">500</span><span class="sxs-lookup"><span data-stu-id="b2432-125">500</span></span>    |
| <span data-ttu-id="b2432-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="b2432-126">10/11/2015</span></span> | <span data-ttu-id="b2432-127">130100 – Kunder</span><span class="sxs-lookup"><span data-stu-id="b2432-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="b2432-128">USD</span><span class="sxs-lookup"><span data-stu-id="b2432-128">USD</span></span>      | <span data-ttu-id="b2432-129">-500</span><span class="sxs-lookup"><span data-stu-id="b2432-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="b2432-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="b2432-130">Exchange rates</span></span>

| <span data-ttu-id="b2432-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="b2432-131">From currency</span></span> | <span data-ttu-id="b2432-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="b2432-132">To currency</span></span> | <span data-ttu-id="b2432-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="b2432-133">Start date</span></span> | <span data-ttu-id="b2432-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="b2432-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="b2432-135">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-135">EUR</span></span>           | <span data-ttu-id="b2432-136">USD</span><span class="sxs-lookup"><span data-stu-id="b2432-136">USD</span></span>         | <span data-ttu-id="b2432-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="b2432-137">10/1/2015</span></span>  | <span data-ttu-id="b2432-138">200</span><span class="sxs-lookup"><span data-stu-id="b2432-138">200</span></span>           |
| <span data-ttu-id="b2432-139">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-139">EUR</span></span>           | <span data-ttu-id="b2432-140">USD</span><span class="sxs-lookup"><span data-stu-id="b2432-140">USD</span></span>         | <span data-ttu-id="b2432-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="b2432-141">11/1/2015</span></span>  | <span data-ttu-id="b2432-142">150</span><span class="sxs-lookup"><span data-stu-id="b2432-142">150</span></span>           |
| <span data-ttu-id="b2432-143">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-143">EUR</span></span>           | <span data-ttu-id="b2432-144">USD</span><span class="sxs-lookup"><span data-stu-id="b2432-144">USD</span></span>         | <span data-ttu-id="b2432-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="b2432-145">12/1/2012</span></span>  | <span data-ttu-id="b2432-146">100</span><span class="sxs-lookup"><span data-stu-id="b2432-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="b2432-147">Utfør konsolideringen for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="b2432-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="b2432-148">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="b2432-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="b2432-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="b2432-149">Ledger account</span></span> | <span data-ttu-id="b2432-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="b2432-150">Currency</span></span> | <span data-ttu-id="b2432-151">Beløp</span><span class="sxs-lookup"><span data-stu-id="b2432-151">Amount</span></span> | <span data-ttu-id="b2432-152">Beregning</span><span class="sxs-lookup"><span data-stu-id="b2432-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="b2432-153">110110</span><span class="sxs-lookup"><span data-stu-id="b2432-153">110110</span></span>         | <span data-ttu-id="b2432-154">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-154">EUR</span></span>      | <span data-ttu-id="b2432-155">250</span><span class="sxs-lookup"><span data-stu-id="b2432-155">250</span></span>    | <span data-ttu-id="b2432-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="b2432-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="b2432-157">130100</span><span class="sxs-lookup"><span data-stu-id="b2432-157">130100</span></span>         | <span data-ttu-id="b2432-158">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-158">EUR</span></span>      | <span data-ttu-id="b2432-159">-250</span><span class="sxs-lookup"><span data-stu-id="b2432-159">-250</span></span>   | <span data-ttu-id="b2432-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="b2432-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="b2432-161">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="b2432-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="b2432-162">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="b2432-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="b2432-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="b2432-163">Ledger account</span></span> | <span data-ttu-id="b2432-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="b2432-164">Currency</span></span> | <span data-ttu-id="b2432-165">Beløp</span><span class="sxs-lookup"><span data-stu-id="b2432-165">Amount</span></span>  | <span data-ttu-id="b2432-166">Beregning</span><span class="sxs-lookup"><span data-stu-id="b2432-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="b2432-167">110110</span><span class="sxs-lookup"><span data-stu-id="b2432-167">110110</span></span>         | <span data-ttu-id="b2432-168">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-168">EUR</span></span>      | <span data-ttu-id="b2432-169">333.33</span><span class="sxs-lookup"><span data-stu-id="b2432-169">333.33</span></span>  | <span data-ttu-id="b2432-170">Opprinnelig beløp 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="b2432-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="b2432-171">130100</span><span class="sxs-lookup"><span data-stu-id="b2432-171">130100</span></span>         | <span data-ttu-id="b2432-172">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-172">EUR</span></span>      | <span data-ttu-id="b2432-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="b2432-173">-333.33</span></span> | <span data-ttu-id="b2432-174">Opprinnelig beløp -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="b2432-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="b2432-175">801400</span><span class="sxs-lookup"><span data-stu-id="b2432-175">801400</span></span>         | <span data-ttu-id="b2432-176">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-176">EUR</span></span>      | <span data-ttu-id="b2432-177">83.33</span><span class="sxs-lookup"><span data-stu-id="b2432-177">83.33</span></span>   | <span data-ttu-id="b2432-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="b2432-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="b2432-179">801600</span><span class="sxs-lookup"><span data-stu-id="b2432-179">801600</span></span>         | <span data-ttu-id="b2432-180">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-180">EUR</span></span>      | <span data-ttu-id="b2432-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="b2432-181">-83.33</span></span>  | <span data-ttu-id="b2432-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="b2432-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="b2432-183">Du vil se tilleggstransaksjoner for rapporteringsvalutabeløpene.</span><span class="sxs-lookup"><span data-stu-id="b2432-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="b2432-184">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 31. desember 2015</span><span class="sxs-lookup"><span data-stu-id="b2432-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="b2432-185">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="b2432-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="b2432-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="b2432-186">Ledger account</span></span> | <span data-ttu-id="b2432-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="b2432-187">Currency</span></span> | <span data-ttu-id="b2432-188">Beløp</span><span class="sxs-lookup"><span data-stu-id="b2432-188">Amount</span></span>  | <span data-ttu-id="b2432-189">Beregning</span><span class="sxs-lookup"><span data-stu-id="b2432-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="b2432-190">110110</span><span class="sxs-lookup"><span data-stu-id="b2432-190">110110</span></span>         | <span data-ttu-id="b2432-191">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-191">EUR</span></span>      | <span data-ttu-id="b2432-192">500,00</span><span class="sxs-lookup"><span data-stu-id="b2432-192">500.00</span></span>  | <span data-ttu-id="b2432-193">Opprinnelig beløp 500 × 1</span><span class="sxs-lookup"><span data-stu-id="b2432-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="b2432-194">130100</span><span class="sxs-lookup"><span data-stu-id="b2432-194">130100</span></span>         | <span data-ttu-id="b2432-195">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-195">EUR</span></span>      | <span data-ttu-id="b2432-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="b2432-196">-500.00</span></span> | <span data-ttu-id="b2432-197">Opprinnelig beløp -500 × 1</span><span class="sxs-lookup"><span data-stu-id="b2432-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="b2432-198">801400</span><span class="sxs-lookup"><span data-stu-id="b2432-198">801400</span></span>         | <span data-ttu-id="b2432-199">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-199">EUR</span></span>      | <span data-ttu-id="b2432-200">250</span><span class="sxs-lookup"><span data-stu-id="b2432-200">250</span></span>     | <span data-ttu-id="b2432-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="b2432-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="b2432-202">801600</span><span class="sxs-lookup"><span data-stu-id="b2432-202">801600</span></span>         | <span data-ttu-id="b2432-203">EUR</span><span class="sxs-lookup"><span data-stu-id="b2432-203">EUR</span></span>      | <span data-ttu-id="b2432-204">-250</span><span class="sxs-lookup"><span data-stu-id="b2432-204">-250</span></span>    | <span data-ttu-id="b2432-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="b2432-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





