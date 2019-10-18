---
title: Revaluering av valuta i et konsolideringsfirma
description: Dette emnet beskriver hvordan å revaluere valuta i et konsolideringsselskap.
author: ShylaThompson
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
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179182"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f4af7-103">Revaluering av valuta i et konsolideringsfirma</span><span class="sxs-lookup"><span data-stu-id="f4af7-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4af7-104">Når du konsoliderer data fra én regnskapsvaluta til en annen, du må fortsatt kjøre valutarevaluering hvis det er endringer i valutakurser, slik at kontosaldoene revalueres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="f4af7-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f4af7-105">Når du konsoliderer de opprinnelig dataene, kan du bruke kategorien **Omveksling av valuta** for å velge de opprinnelige valutakursene for omveksling i løpet av konsolideringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f4af7-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f4af7-106">Når en ny valutakurs angis (for eksempel i neste måned), må du revaluere kontosaldoene.</span><span class="sxs-lookup"><span data-stu-id="f4af7-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f4af7-107">Urealisert fortjeneste og tap oppdateres deretter tilsvarende, basert på den nye valutakursen og datoen.</span><span class="sxs-lookup"><span data-stu-id="f4af7-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f4af7-108">Eksemplet nedenfor illustrerer regnskapsoppføringer som opprettes under prosessen.</span><span class="sxs-lookup"><span data-stu-id="f4af7-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f4af7-109">Firmaoppsett</span><span class="sxs-lookup"><span data-stu-id="f4af7-109">Company setup</span></span>
-   <span data-ttu-id="f4af7-110">**Kilde/driftsselskap (USMF)** – Amerikanske dollar (USD) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="f4af7-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f4af7-111">**Konsolidert firma (CON)** – Euro (EUR) brukes som regnskaps- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="f4af7-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f4af7-112">**Realisert fortjeneste** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="f4af7-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="f4af7-113">**Realisert tap** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="f4af7-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f4af7-114">**Urealisert fortjeneste** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="f4af7-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f4af7-115">**Urealisert tap** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="f4af7-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f4af7-116">Opprinnelige transaksjoner</span><span class="sxs-lookup"><span data-stu-id="f4af7-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f4af7-117">Kontantmottakstransaksjoner i USMF</span><span class="sxs-lookup"><span data-stu-id="f4af7-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f4af7-118">Dato</span><span class="sxs-lookup"><span data-stu-id="f4af7-118">Date</span></span>       | <span data-ttu-id="f4af7-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f4af7-119">Ledger account</span></span>               | <span data-ttu-id="f4af7-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4af7-120">Currency</span></span> | <span data-ttu-id="f4af7-121">Beløp</span><span class="sxs-lookup"><span data-stu-id="f4af7-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f4af7-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-122">10/11/2015</span></span> | <span data-ttu-id="f4af7-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="f4af7-123">110110 – Cash</span></span>                | <span data-ttu-id="f4af7-124">USD</span><span class="sxs-lookup"><span data-stu-id="f4af7-124">USD</span></span>      | <span data-ttu-id="f4af7-125">500</span><span class="sxs-lookup"><span data-stu-id="f4af7-125">500</span></span>    |
| <span data-ttu-id="f4af7-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-126">10/11/2015</span></span> | <span data-ttu-id="f4af7-127">130100 – Kunder</span><span class="sxs-lookup"><span data-stu-id="f4af7-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f4af7-128">USD</span><span class="sxs-lookup"><span data-stu-id="f4af7-128">USD</span></span>      | <span data-ttu-id="f4af7-129">-500</span><span class="sxs-lookup"><span data-stu-id="f4af7-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f4af7-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="f4af7-130">Exchange rates</span></span>

| <span data-ttu-id="f4af7-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="f4af7-131">From currency</span></span> | <span data-ttu-id="f4af7-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="f4af7-132">To currency</span></span> | <span data-ttu-id="f4af7-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="f4af7-133">Start date</span></span> | <span data-ttu-id="f4af7-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="f4af7-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f4af7-135">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-135">EUR</span></span>           | <span data-ttu-id="f4af7-136">USD</span><span class="sxs-lookup"><span data-stu-id="f4af7-136">USD</span></span>         | <span data-ttu-id="f4af7-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-137">10/1/2015</span></span>  | <span data-ttu-id="f4af7-138">200</span><span class="sxs-lookup"><span data-stu-id="f4af7-138">200</span></span>           |
| <span data-ttu-id="f4af7-139">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-139">EUR</span></span>           | <span data-ttu-id="f4af7-140">USD</span><span class="sxs-lookup"><span data-stu-id="f4af7-140">USD</span></span>         | <span data-ttu-id="f4af7-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-141">11/1/2015</span></span>  | <span data-ttu-id="f4af7-142">150</span><span class="sxs-lookup"><span data-stu-id="f4af7-142">150</span></span>           |
| <span data-ttu-id="f4af7-143">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-143">EUR</span></span>           | <span data-ttu-id="f4af7-144">USD</span><span class="sxs-lookup"><span data-stu-id="f4af7-144">USD</span></span>         | <span data-ttu-id="f4af7-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="f4af7-145">12/1/2012</span></span>  | <span data-ttu-id="f4af7-146">100</span><span class="sxs-lookup"><span data-stu-id="f4af7-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f4af7-147">Utfør konsolideringen for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f4af7-148">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="f4af7-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="f4af7-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f4af7-149">Ledger account</span></span> | <span data-ttu-id="f4af7-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4af7-150">Currency</span></span> | <span data-ttu-id="f4af7-151">Beløp</span><span class="sxs-lookup"><span data-stu-id="f4af7-151">Amount</span></span> | <span data-ttu-id="f4af7-152">Beregning</span><span class="sxs-lookup"><span data-stu-id="f4af7-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f4af7-153">110110</span><span class="sxs-lookup"><span data-stu-id="f4af7-153">110110</span></span>         | <span data-ttu-id="f4af7-154">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-154">EUR</span></span>      | <span data-ttu-id="f4af7-155">250</span><span class="sxs-lookup"><span data-stu-id="f4af7-155">250</span></span>    | <span data-ttu-id="f4af7-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f4af7-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="f4af7-157">130100</span><span class="sxs-lookup"><span data-stu-id="f4af7-157">130100</span></span>         | <span data-ttu-id="f4af7-158">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-158">EUR</span></span>      | <span data-ttu-id="f4af7-159">-250</span><span class="sxs-lookup"><span data-stu-id="f4af7-159">-250</span></span>   | <span data-ttu-id="f4af7-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f4af7-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f4af7-161">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f4af7-162">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="f4af7-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="f4af7-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f4af7-163">Ledger account</span></span> | <span data-ttu-id="f4af7-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4af7-164">Currency</span></span> | <span data-ttu-id="f4af7-165">Beløp</span><span class="sxs-lookup"><span data-stu-id="f4af7-165">Amount</span></span>  | <span data-ttu-id="f4af7-166">Beregning</span><span class="sxs-lookup"><span data-stu-id="f4af7-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f4af7-167">110110</span><span class="sxs-lookup"><span data-stu-id="f4af7-167">110110</span></span>         | <span data-ttu-id="f4af7-168">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-168">EUR</span></span>      | <span data-ttu-id="f4af7-169">333.33</span><span class="sxs-lookup"><span data-stu-id="f4af7-169">333.33</span></span>  | <span data-ttu-id="f4af7-170">Opprinnelig beløp 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f4af7-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f4af7-171">130100</span><span class="sxs-lookup"><span data-stu-id="f4af7-171">130100</span></span>         | <span data-ttu-id="f4af7-172">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-172">EUR</span></span>      | <span data-ttu-id="f4af7-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="f4af7-173">-333.33</span></span> | <span data-ttu-id="f4af7-174">Opprinnelig beløp -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f4af7-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f4af7-175">801400</span><span class="sxs-lookup"><span data-stu-id="f4af7-175">801400</span></span>         | <span data-ttu-id="f4af7-176">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-176">EUR</span></span>      | <span data-ttu-id="f4af7-177">83.33</span><span class="sxs-lookup"><span data-stu-id="f4af7-177">83.33</span></span>   | <span data-ttu-id="f4af7-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="f4af7-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="f4af7-179">801600</span><span class="sxs-lookup"><span data-stu-id="f4af7-179">801600</span></span>         | <span data-ttu-id="f4af7-180">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-180">EUR</span></span>      | <span data-ttu-id="f4af7-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="f4af7-181">-83.33</span></span>  | <span data-ttu-id="f4af7-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="f4af7-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f4af7-183">Du vil se tilleggstransaksjoner for rapporteringsvalutabeløpene.</span><span class="sxs-lookup"><span data-stu-id="f4af7-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f4af7-184">Utfør valutarevaluering for kontoene fra 1. oktober 2015 til 31. desember 2015</span><span class="sxs-lookup"><span data-stu-id="f4af7-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f4af7-185">Saldoer i konsolideringsfirmaet</span><span class="sxs-lookup"><span data-stu-id="f4af7-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="f4af7-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f4af7-186">Ledger account</span></span> | <span data-ttu-id="f4af7-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4af7-187">Currency</span></span> | <span data-ttu-id="f4af7-188">Beløp</span><span class="sxs-lookup"><span data-stu-id="f4af7-188">Amount</span></span>  | <span data-ttu-id="f4af7-189">Beregning</span><span class="sxs-lookup"><span data-stu-id="f4af7-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f4af7-190">110110</span><span class="sxs-lookup"><span data-stu-id="f4af7-190">110110</span></span>         | <span data-ttu-id="f4af7-191">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-191">EUR</span></span>      | <span data-ttu-id="f4af7-192">500,00</span><span class="sxs-lookup"><span data-stu-id="f4af7-192">500.00</span></span>  | <span data-ttu-id="f4af7-193">Opprinnelig beløp 500 × 1</span><span class="sxs-lookup"><span data-stu-id="f4af7-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f4af7-194">130100</span><span class="sxs-lookup"><span data-stu-id="f4af7-194">130100</span></span>         | <span data-ttu-id="f4af7-195">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-195">EUR</span></span>      | <span data-ttu-id="f4af7-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="f4af7-196">-500.00</span></span> | <span data-ttu-id="f4af7-197">Opprinnelig beløp -500 × 1</span><span class="sxs-lookup"><span data-stu-id="f4af7-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f4af7-198">801400</span><span class="sxs-lookup"><span data-stu-id="f4af7-198">801400</span></span>         | <span data-ttu-id="f4af7-199">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-199">EUR</span></span>      | <span data-ttu-id="f4af7-200">250</span><span class="sxs-lookup"><span data-stu-id="f4af7-200">250</span></span>     | <span data-ttu-id="f4af7-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="f4af7-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f4af7-202">801600</span><span class="sxs-lookup"><span data-stu-id="f4af7-202">801600</span></span>         | <span data-ttu-id="f4af7-203">EUR</span><span class="sxs-lookup"><span data-stu-id="f4af7-203">EUR</span></span>      | <span data-ttu-id="f4af7-204">-250</span><span class="sxs-lookup"><span data-stu-id="f4af7-204">-250</span></span>    | <span data-ttu-id="f4af7-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="f4af7-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





