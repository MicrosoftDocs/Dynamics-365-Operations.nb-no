---
title: Dobbel rapportering
description: Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815986"
---
# <a name="dual-reporting"></a><span data-ttu-id="f6abb-103">Dobbel rapportering</span><span class="sxs-lookup"><span data-stu-id="f6abb-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6abb-104">Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="f6abb-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="f6abb-105">Det er nødvendig å ha erfaring med posteringslag i Microsoft Dynamics 365 Finance, og dette gjør det enklere å forstå eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f6abb-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="f6abb-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f6abb-106">Example</span></span>

<span data-ttu-id="f6abb-107">Det følgende eksemplet gjør rede for en leieavtale under italiensk lovbestemt rapportering, ved hjelp av både kontantprinsippmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="f6abb-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="f6abb-108">Firmaet må opprette tre tablåer for å følge både de italienske lovbestemte kravene og IFRS 16-kravene.</span><span class="sxs-lookup"><span data-stu-id="f6abb-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="f6abb-109">Det kreves ett tablå for IFRS 16, ett tablå for lovbestemte krav og ett tablå for å tilbakeføre lovbestemte posteringer automatisk.</span><span class="sxs-lookup"><span data-stu-id="f6abb-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="f6abb-110">Tablåene blir opprettet som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="f6abb-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="f6abb-111">**IFRS 16-tablå**</span><span class="sxs-lookup"><span data-stu-id="f6abb-111">**IFRS 16 book**</span></span>

<span data-ttu-id="f6abb-112">IFRS 16-tablået konfigureres slik at det er i samsvar med IFRS 16-regnskapsstandarden.</span><span class="sxs-lookup"><span data-stu-id="f6abb-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="f6abb-113">Alle oppføringer som posteres i dette tablået, posteres på et egendefinert lag.</span><span class="sxs-lookup"><span data-stu-id="f6abb-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="f6abb-114">Navn</span><span class="sxs-lookup"><span data-stu-id="f6abb-114">Name</span></span>                                    | <span data-ttu-id="f6abb-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="f6abb-116">Registertype</span><span class="sxs-lookup"><span data-stu-id="f6abb-116">Book type</span></span>                               | <span data-ttu-id="f6abb-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="f6abb-117">IFRS 16</span></span>        |
| <span data-ttu-id="f6abb-118">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-118">Book description</span></span>                        | <span data-ttu-id="f6abb-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="f6abb-119">IFRS 16</span></span>        |
| <span data-ttu-id="f6abb-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="f6abb-120">Posting Layer</span></span>                           | <span data-ttu-id="f6abb-121">Tilpasset lag 1</span><span class="sxs-lookup"><span data-stu-id="f6abb-121">Custom layer 1</span></span> |
| <span data-ttu-id="f6abb-122">Leietype</span><span class="sxs-lookup"><span data-stu-id="f6abb-122">Lease Type</span></span>                              | <span data-ttu-id="f6abb-123">Finance</span><span class="sxs-lookup"><span data-stu-id="f6abb-123">Finance</span></span>        |
| <span data-ttu-id="f6abb-124">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="f6abb-124">Accounting Framework</span></span>                    | <span data-ttu-id="f6abb-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="f6abb-125">IFRS 16</span></span>        |
| <span data-ttu-id="f6abb-126">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="f6abb-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="f6abb-127">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-127">0.00</span></span>           |
| <span data-ttu-id="f6abb-128">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="f6abb-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="f6abb-129">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-129">0.00</span></span>           |
| <span data-ttu-id="f6abb-130">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="f6abb-130">Short-term threshold</span></span>                    | <span data-ttu-id="f6abb-131">12</span><span class="sxs-lookup"><span data-stu-id="f6abb-131">12</span></span>             |
| <span data-ttu-id="f6abb-132">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="f6abb-132">Low Value Threshold</span></span>                     | <span data-ttu-id="f6abb-133">5 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-133">5,000.00</span></span>       |
| <span data-ttu-id="f6abb-134">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="f6abb-134">Pay to Vendor</span></span>                           | <span data-ttu-id="f6abb-135">Nr.</span><span class="sxs-lookup"><span data-stu-id="f6abb-135">No</span></span>             |

<span data-ttu-id="f6abb-136">**Lovbestemt tablå**</span><span class="sxs-lookup"><span data-stu-id="f6abb-136">**Statutory book**</span></span>

<span data-ttu-id="f6abb-137">Det lovbestemte tablået er et kontantprinsipptablå der firmaet gjør rede for leieutgiftene som kontantbeløpet som betales hver måned i leie.</span><span class="sxs-lookup"><span data-stu-id="f6abb-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="f6abb-138">Dette tablået produserer ikke en bruksrettseiendel eller leieforpliktelse.</span><span class="sxs-lookup"><span data-stu-id="f6abb-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="f6abb-139">Navn</span><span class="sxs-lookup"><span data-stu-id="f6abb-139">Name</span></span>                                    | <span data-ttu-id="f6abb-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="f6abb-141">Registertype</span><span class="sxs-lookup"><span data-stu-id="f6abb-141">Book type</span></span>                               | <span data-ttu-id="f6abb-142">Lovbestemt</span><span class="sxs-lookup"><span data-stu-id="f6abb-142">Statutory</span></span>   |
| <span data-ttu-id="f6abb-143">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-143">Book description</span></span>                        | <span data-ttu-id="f6abb-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="f6abb-144">Local GAAP</span></span>  |
| <span data-ttu-id="f6abb-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="f6abb-145">Posting Layer</span></span>                           | <span data-ttu-id="f6abb-146">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-146">Current</span></span>     |
| <span data-ttu-id="f6abb-147">Leietype</span><span class="sxs-lookup"><span data-stu-id="f6abb-147">Lease Type</span></span>                              | <span data-ttu-id="f6abb-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="f6abb-148">Automatic</span></span>   |
| <span data-ttu-id="f6abb-149">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="f6abb-149">Accounting Framework</span></span>                    | <span data-ttu-id="f6abb-150">Kontantgrunnlag</span><span class="sxs-lookup"><span data-stu-id="f6abb-150">Cash basis</span></span>  |
| <span data-ttu-id="f6abb-151">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="f6abb-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="f6abb-152">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-152">0.00</span></span>        |
| <span data-ttu-id="f6abb-153">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="f6abb-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="f6abb-154">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-154">0.00</span></span>        |
| <span data-ttu-id="f6abb-155">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="f6abb-155">Short-term threshold</span></span>                    | <span data-ttu-id="f6abb-156">0</span><span class="sxs-lookup"><span data-stu-id="f6abb-156">0</span></span>           |
| <span data-ttu-id="f6abb-157">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="f6abb-157">Low Value Threshold</span></span>                     | <span data-ttu-id="f6abb-158">0</span><span class="sxs-lookup"><span data-stu-id="f6abb-158">0</span></span>           |
| <span data-ttu-id="f6abb-159">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="f6abb-159">Pay to Vendor</span></span>                           | <span data-ttu-id="f6abb-160">Nr.</span><span class="sxs-lookup"><span data-stu-id="f6abb-160">No</span></span>          |

<span data-ttu-id="f6abb-161">**Lovbestemt tilbakeføringstablå**</span><span class="sxs-lookup"><span data-stu-id="f6abb-161">**Statutory reversal book**</span></span>

<span data-ttu-id="f6abb-162">Det lovbestemte tilbakeføringstablået konfigureres på samme måte som det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="f6abb-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="f6abb-163">Navn</span><span class="sxs-lookup"><span data-stu-id="f6abb-163">Name</span></span>                                    | <span data-ttu-id="f6abb-164">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="f6abb-165">Registertype</span><span class="sxs-lookup"><span data-stu-id="f6abb-165">Book type</span></span>                               | <span data-ttu-id="f6abb-166">Lovbestemt – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="f6abb-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="f6abb-167">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-167">Book description</span></span>                        | <span data-ttu-id="f6abb-168">Tablå for å tilbakeføre lovbestemt tablå</span><span class="sxs-lookup"><span data-stu-id="f6abb-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="f6abb-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="f6abb-169">Posting Layer</span></span>                           | <span data-ttu-id="f6abb-170">Tilpasset lag 1</span><span class="sxs-lookup"><span data-stu-id="f6abb-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="f6abb-171">Leietype</span><span class="sxs-lookup"><span data-stu-id="f6abb-171">Lease Type</span></span>                              | <span data-ttu-id="f6abb-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="f6abb-172">Automatic</span></span>                      |
| <span data-ttu-id="f6abb-173">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="f6abb-173">Accounting Framework</span></span>                    | <span data-ttu-id="f6abb-174">Kontantgrunnlag</span><span class="sxs-lookup"><span data-stu-id="f6abb-174">Cash basis</span></span>                     |
| <span data-ttu-id="f6abb-175">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="f6abb-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="f6abb-176">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-176">0.00</span></span>                           |
| <span data-ttu-id="f6abb-177">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="f6abb-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="f6abb-178">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-178">0.00</span></span>                           |
| <span data-ttu-id="f6abb-179">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="f6abb-179">Short-term threshold</span></span>                    | <span data-ttu-id="f6abb-180">0</span><span class="sxs-lookup"><span data-stu-id="f6abb-180">0</span></span>                              |
| <span data-ttu-id="f6abb-181">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="f6abb-181">Low Value Threshold</span></span>                     | <span data-ttu-id="f6abb-182">0</span><span class="sxs-lookup"><span data-stu-id="f6abb-182">0</span></span>                              |
| <span data-ttu-id="f6abb-183">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="f6abb-183">Pay to Vendor</span></span>                           | <span data-ttu-id="f6abb-184">Nr.</span><span class="sxs-lookup"><span data-stu-id="f6abb-184">No</span></span>                             |

<span data-ttu-id="f6abb-185">I dette eksemplet er det opprettet en leieavtale som har følgende innstillinger i fanene **Generelt** og **Linjer i betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="f6abb-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="f6abb-186">**Fanen Generelt**</span><span class="sxs-lookup"><span data-stu-id="f6abb-186">**General tab**</span></span>

| <span data-ttu-id="f6abb-187">Felt</span><span class="sxs-lookup"><span data-stu-id="f6abb-187">Field</span></span>                      | <span data-ttu-id="f6abb-188">Verdi</span><span class="sxs-lookup"><span data-stu-id="f6abb-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="f6abb-189">Trinnvis lånerente</span><span class="sxs-lookup"><span data-stu-id="f6abb-189">Incremental borrowing rate</span></span> | <span data-ttu-id="f6abb-190">5 %</span><span class="sxs-lookup"><span data-stu-id="f6abb-190">5%</span></span>               |
| <span data-ttu-id="f6abb-191">Startdato</span><span class="sxs-lookup"><span data-stu-id="f6abb-191">Commencement date</span></span>          | <span data-ttu-id="f6abb-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="f6abb-192">1/1/2020</span></span>         |
| <span data-ttu-id="f6abb-193">Leiegruppe</span><span class="sxs-lookup"><span data-stu-id="f6abb-193">Lease group</span></span>                | <span data-ttu-id="f6abb-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="f6abb-194">Buildings</span></span>        |
| <span data-ttu-id="f6abb-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="f6abb-195">Vendor</span></span>                     | <span data-ttu-id="f6abb-196">1001</span><span class="sxs-lookup"><span data-stu-id="f6abb-196">1001</span></span>             |
| <span data-ttu-id="f6abb-197">Aktivaets gjennomsnittsverdi</span><span class="sxs-lookup"><span data-stu-id="f6abb-197">Fair value of the asset</span></span>    | <span data-ttu-id="f6abb-198">245 000</span><span class="sxs-lookup"><span data-stu-id="f6abb-198">245,000</span></span>          |
| <span data-ttu-id="f6abb-199">Aktivalevetid</span><span class="sxs-lookup"><span data-stu-id="f6abb-199">Asset useful life</span></span>          | <span data-ttu-id="f6abb-200">120</span><span class="sxs-lookup"><span data-stu-id="f6abb-200">120</span></span>              |
| <span data-ttu-id="f6abb-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="f6abb-201">Annuity type</span></span>               | <span data-ttu-id="f6abb-202">Vanlig annuitet</span><span class="sxs-lookup"><span data-stu-id="f6abb-202">Ordinary annuity</span></span> |
| <span data-ttu-id="f6abb-203">Sammensetningsintervall</span><span class="sxs-lookup"><span data-stu-id="f6abb-203">Compounding interval</span></span>       | <span data-ttu-id="f6abb-204">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f6abb-204">Monthly</span></span>          |

<span data-ttu-id="f6abb-205">**Fanen Linjer i betalingsplan**</span><span class="sxs-lookup"><span data-stu-id="f6abb-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="f6abb-206">Felt</span><span class="sxs-lookup"><span data-stu-id="f6abb-206">Field</span></span>             | <span data-ttu-id="f6abb-207">Verdi</span><span class="sxs-lookup"><span data-stu-id="f6abb-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="f6abb-208">Startdato</span><span class="sxs-lookup"><span data-stu-id="f6abb-208">Start date</span></span>        | <span data-ttu-id="f6abb-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="f6abb-209">1/1/2020</span></span>   |
| <span data-ttu-id="f6abb-210">Periodeintervall</span><span class="sxs-lookup"><span data-stu-id="f6abb-210">Period interval</span></span>   | <span data-ttu-id="f6abb-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="f6abb-211">Months</span></span>     |
| <span data-ttu-id="f6abb-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="f6abb-212">Periods</span></span>           | <span data-ttu-id="f6abb-213">24</span><span class="sxs-lookup"><span data-stu-id="f6abb-213">24</span></span>         |
| <span data-ttu-id="f6abb-214">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="f6abb-214">End date</span></span>          | <span data-ttu-id="f6abb-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="f6abb-215">12/31/2020</span></span> |
| <span data-ttu-id="f6abb-216">Betalingsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f6abb-216">Payment frequency</span></span> | <span data-ttu-id="f6abb-217">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f6abb-217">Monthly</span></span>    |
| <span data-ttu-id="f6abb-218">Betalingsbeløp</span><span class="sxs-lookup"><span data-stu-id="f6abb-218">Payment amount</span></span>    | <span data-ttu-id="f6abb-219">1 000</span><span class="sxs-lookup"><span data-stu-id="f6abb-219">1,000</span></span>      |

<span data-ttu-id="f6abb-220">Hvis du vil gjøre rede for denne leien under to rammeverk, bruker du et gjeldende posteringslag og et egendefinert posteringslag.</span><span class="sxs-lookup"><span data-stu-id="f6abb-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="f6abb-221">Følgende tabell viser et eksempel på hver journaloppføring som kreves for å representere økonomien riktig under hver rapporteringsstandard.</span><span class="sxs-lookup"><span data-stu-id="f6abb-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="f6abb-222">En detaljert beskrivelse av hver journaloppføring for den første måneden av leieavtalen gis etterpå.</span><span class="sxs-lookup"><span data-stu-id="f6abb-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="f6abb-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="f6abb-224">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="f6abb-225">Lovbestemt tablå (gjeldende lag)</span><span class="sxs-lookup"><span data-stu-id="f6abb-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="f6abb-226">Gjeldende lag totalt</span><span class="sxs-lookup"><span data-stu-id="f6abb-226">Current layer total</span></span></th>
<th><span data-ttu-id="f6abb-227">Tilbakeføringstablå (egendefinert lag)</span><span class="sxs-lookup"><span data-stu-id="f6abb-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="f6abb-228">IFRS 16-tablå (egendefinert lag)</span><span class="sxs-lookup"><span data-stu-id="f6abb-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="f6abb-229">Gjeldende lag + egendefinert lag totalt</span><span class="sxs-lookup"><span data-stu-id="f6abb-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6abb-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="f6abb-230">JE-100</span></span></th>
<th><span data-ttu-id="f6abb-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="f6abb-231">JE-110</span></span></th>
<th><span data-ttu-id="f6abb-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="f6abb-232">JE-120</span></span></th>
<th><span data-ttu-id="f6abb-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="f6abb-233">JE-130</span></span></th>
<th><span data-ttu-id="f6abb-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="f6abb-234">JE-140</span></span></th>
<th><span data-ttu-id="f6abb-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="f6abb-235">JE-150</span></span></th>
<th><span data-ttu-id="f6abb-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="f6abb-236">JE-160</span></span></th>
<th><span data-ttu-id="f6abb-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="f6abb-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6abb-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6abb-246">1</span><span class="sxs-lookup"><span data-stu-id="f6abb-246">1</span></span></td>
<td><span data-ttu-id="f6abb-247">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-247">Lease expense</span></span></td>
<td><span data-ttu-id="f6abb-248">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-249">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-249">1,000.00</span></span></td>
<td><span data-ttu-id="f6abb-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-251">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-252">2</span><span class="sxs-lookup"><span data-stu-id="f6abb-252">2</span></span></td>
<td><span data-ttu-id="f6abb-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="f6abb-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-254">3,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-255">3,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-256">3,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-257">3</span><span class="sxs-lookup"><span data-stu-id="f6abb-257">3</span></span></td>
<td><span data-ttu-id="f6abb-258">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-259">5,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-260">5,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-261">5,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-262">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-262">4</span></span></td>
<td><span data-ttu-id="f6abb-263">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-263">Clearing account</span></span></td>
<td><span data-ttu-id="f6abb-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-264">-1,000.00</span></span></td>
<td><span data-ttu-id="f6abb-265">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-266">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-266">0.00</span></span></td>
<td><span data-ttu-id="f6abb-267">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-269">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-270">5</span><span class="sxs-lookup"><span data-stu-id="f6abb-270">5</span></span></td>
<td><span data-ttu-id="f6abb-271">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="f6abb-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-272">-1,008.00</span></span></td>
<td><span data-ttu-id="f6abb-273">1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-273">1,008.00</span></span></td>
<td><span data-ttu-id="f6abb-274">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-275">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-276">6</span><span class="sxs-lookup"><span data-stu-id="f6abb-276">6</span></span></td>
<td><span data-ttu-id="f6abb-277">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="f6abb-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-278">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-279">22 794,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-280">22 793,90</span><span class="sxs-lookup"><span data-stu-id="f6abb-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-281">7</span><span class="sxs-lookup"><span data-stu-id="f6abb-281">7</span></span></td>
<td><span data-ttu-id="f6abb-282">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="f6abb-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-283">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-284">-22,794.00</span></span></td>
<td><span data-ttu-id="f6abb-285">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-285">1,000.00</span></span></td>
<td><span data-ttu-id="f6abb-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="f6abb-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="f6abb-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-288">8</span><span class="sxs-lookup"><span data-stu-id="f6abb-288">8</span></span></td>
<td><span data-ttu-id="f6abb-289">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-290">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-291">94.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-292">94.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-293">9</span><span class="sxs-lookup"><span data-stu-id="f6abb-293">9</span></span></td>
<td><span data-ttu-id="f6abb-294">Kontanter</span><span class="sxs-lookup"><span data-stu-id="f6abb-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-295">-1,008.00</span></span></td>
<td><span data-ttu-id="f6abb-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-298">10</span><span class="sxs-lookup"><span data-stu-id="f6abb-298">10</span></span></td>
<td><span data-ttu-id="f6abb-299">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="f6abb-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-300">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-301">949.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-301">949.75</span></span></td>
<td><span data-ttu-id="f6abb-302">949.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-303">11</span><span class="sxs-lookup"><span data-stu-id="f6abb-303">11</span></span></td>
<td><span data-ttu-id="f6abb-304">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="f6abb-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-305">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="f6abb-306">-949.75</span></span></td>
<td><span data-ttu-id="f6abb-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="f6abb-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6abb-308">Som den foregående tabellen viser kreves det tre tablåer for å rapportere både under lovbestemt rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="f6abb-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="f6abb-309">Det lovbestemte tablået registrerer leiebetalingen i henhold til reglene for kontantprinsippregnskap under det gjeldende laget.</span><span class="sxs-lookup"><span data-stu-id="f6abb-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="f6abb-310">Det lovbestemte tilbakeføringstablået tilbakestiller lovbestemte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="f6abb-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="f6abb-311">IFRS 16-tablået oppretter journaloppføringene som kreves under IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="f6abb-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="f6abb-312">Du trenger bare å angi en leieavtale én gang.</span><span class="sxs-lookup"><span data-stu-id="f6abb-312">You must enter a lease only one time.</span></span> <span data-ttu-id="f6abb-313">Du kan deretter åpne **Tablåer**-siden for å se alle tablåene som er knyttet til leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="f6abb-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="f6abb-314">Når du oppretter tablåene, må alle tre knyttes til samme leiepost.</span><span class="sxs-lookup"><span data-stu-id="f6abb-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="f6abb-315">Den første journaloppføringen registrerer leieutgiften under det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="f6abb-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="f6abb-316">Du kan opprette betalingene i en bunke eller ved å velge betalingsplanen i det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="f6abb-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="f6abb-317">I dette eksemplet produseres følgende journaloppføring for det lovbestemte tablået fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="f6abb-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="f6abb-318">Leiebetaling – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="f6abb-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="f6abb-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-319">Account type</span></span> | <span data-ttu-id="f6abb-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-320">Account number</span></span> | <span data-ttu-id="f6abb-321">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-321">Layer</span></span>   | <span data-ttu-id="f6abb-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-322">Account description</span></span> | <span data-ttu-id="f6abb-323">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-323">Debit</span></span>    | <span data-ttu-id="f6abb-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="f6abb-325">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-325">Ledger</span></span>       | <span data-ttu-id="f6abb-326">1</span><span class="sxs-lookup"><span data-stu-id="f6abb-326">1</span></span>              | <span data-ttu-id="f6abb-327">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-327">Current</span></span> | <span data-ttu-id="f6abb-328">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-328">Lease expense</span></span>       | <span data-ttu-id="f6abb-329">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-329">1,000.00</span></span> |          |
| <span data-ttu-id="f6abb-330">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-330">Ledger</span></span>       | <span data-ttu-id="f6abb-331">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-331">4</span></span>              | <span data-ttu-id="f6abb-332">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-332">Current</span></span> | <span data-ttu-id="f6abb-333">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-333">Clearing account</span></span>    |          | <span data-ttu-id="f6abb-334">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-334">1,000.00</span></span> |

<span data-ttu-id="f6abb-335">En regnskapsassistent bruker standard Dynamics 365-funksjonalitet til å opprette en faktura for å betale leien utenfor Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="f6abb-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="f6abb-336">I stedet for å velge **Leieutgift** som debetkonto velger regnskapsassistenten en avregningskonto for å generere følgende oppføring.</span><span class="sxs-lookup"><span data-stu-id="f6abb-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="f6abb-337">AP-prosess – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="f6abb-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="f6abb-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-338">Account type</span></span> | <span data-ttu-id="f6abb-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-339">Account number</span></span> | <span data-ttu-id="f6abb-340">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-340">Layer</span></span>   | <span data-ttu-id="f6abb-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-341">Account description</span></span> | <span data-ttu-id="f6abb-342">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-342">Debit</span></span>    | <span data-ttu-id="f6abb-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="f6abb-344">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-344">Ledger</span></span>       | <span data-ttu-id="f6abb-345">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-345">4</span></span>              | <span data-ttu-id="f6abb-346">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-346">Current</span></span> | <span data-ttu-id="f6abb-347">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-347">Clearing account</span></span>    | <span data-ttu-id="f6abb-348">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-348">1,000.00</span></span> |          |
| <span data-ttu-id="f6abb-349">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-349">Ledger</span></span>       | <span data-ttu-id="f6abb-350">2</span><span class="sxs-lookup"><span data-stu-id="f6abb-350">2</span></span>              | <span data-ttu-id="f6abb-351">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-351">Current</span></span> | <span data-ttu-id="f6abb-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="f6abb-352">Bank fee</span></span>            | <span data-ttu-id="f6abb-353">3,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-353">3.00</span></span>     |          |
| <span data-ttu-id="f6abb-354">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-354">Ledger</span></span>       | <span data-ttu-id="f6abb-355">3</span><span class="sxs-lookup"><span data-stu-id="f6abb-355">3</span></span>              | <span data-ttu-id="f6abb-356">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-356">Current</span></span> | <span data-ttu-id="f6abb-357">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-357">VAT expense</span></span>         | <span data-ttu-id="f6abb-358">5,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-358">5.00</span></span>     |          |
| <span data-ttu-id="f6abb-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="f6abb-359">Vendor</span></span>       | <span data-ttu-id="f6abb-360">5</span><span class="sxs-lookup"><span data-stu-id="f6abb-360">5</span></span>              | <span data-ttu-id="f6abb-361">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-361">Current</span></span> | <span data-ttu-id="f6abb-362">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="f6abb-362">Accounts payable</span></span>    |          | <span data-ttu-id="f6abb-363">1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-363">1,008.00</span></span> |

<span data-ttu-id="f6abb-364">Når utdraget er utstedt til leverandøren, følger du den vanlige betalingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f6abb-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="f6abb-365">Følgende journaloppføring genereres i løpet av denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="f6abb-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="f6abb-366">Kontantbetaling – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="f6abb-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="f6abb-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-367">Account type</span></span> | <span data-ttu-id="f6abb-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-368">Account number</span></span> | <span data-ttu-id="f6abb-369">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-369">Layer</span></span>   | <span data-ttu-id="f6abb-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-370">Account description</span></span> | <span data-ttu-id="f6abb-371">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-371">Debit</span></span>    | <span data-ttu-id="f6abb-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="f6abb-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="f6abb-373">Vendor</span></span>       | <span data-ttu-id="f6abb-374">5</span><span class="sxs-lookup"><span data-stu-id="f6abb-374">5</span></span>              | <span data-ttu-id="f6abb-375">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-375">Current</span></span> | <span data-ttu-id="f6abb-376">Leverandører</span><span class="sxs-lookup"><span data-stu-id="f6abb-376">Accounts Payable</span></span>    | <span data-ttu-id="f6abb-377">1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-377">1,008.00</span></span> |          |
| <span data-ttu-id="f6abb-378">Bank</span><span class="sxs-lookup"><span data-stu-id="f6abb-378">Bank</span></span>         | <span data-ttu-id="f6abb-379">9</span><span class="sxs-lookup"><span data-stu-id="f6abb-379">9</span></span>              | <span data-ttu-id="f6abb-380">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="f6abb-380">Current</span></span> | <span data-ttu-id="f6abb-381">Kontanter</span><span class="sxs-lookup"><span data-stu-id="f6abb-381">Cash</span></span>                |          | <span data-ttu-id="f6abb-382">1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-382">1,008.00</span></span> |

<span data-ttu-id="f6abb-383">Nå har du gjort fullstendig rede for denne leien under lovbestemte rapporteringskrav og kan generere en råbalanse ved hjelp av det gjeldende laget.</span><span class="sxs-lookup"><span data-stu-id="f6abb-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="f6abb-384">Systemet returnerer en råbalanse med følgende tall.</span><span class="sxs-lookup"><span data-stu-id="f6abb-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="f6abb-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="f6abb-386">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="f6abb-387">Lovbestemt tablå (gjeldende lag)</span><span class="sxs-lookup"><span data-stu-id="f6abb-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="f6abb-388">Gjeldende lag totalt</span><span class="sxs-lookup"><span data-stu-id="f6abb-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6abb-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="f6abb-389">JE-100</span></span></th>
<th><span data-ttu-id="f6abb-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="f6abb-390">JE-110</span></span></th>
<th><span data-ttu-id="f6abb-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="f6abb-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6abb-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f6abb-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="f6abb-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6abb-395">1</span><span class="sxs-lookup"><span data-stu-id="f6abb-395">1</span></span></td>
<td><span data-ttu-id="f6abb-396">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-396">Lease expense</span></span></td>
<td><span data-ttu-id="f6abb-397">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-398">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-399">2</span><span class="sxs-lookup"><span data-stu-id="f6abb-399">2</span></span></td>
<td><span data-ttu-id="f6abb-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="f6abb-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-401">3,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-402">3,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-403">3</span><span class="sxs-lookup"><span data-stu-id="f6abb-403">3</span></span></td>
<td><span data-ttu-id="f6abb-404">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-405">5,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-406">5,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-407">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-407">4</span></span></td>
<td><span data-ttu-id="f6abb-408">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-408">Clearing account</span></span></td>
<td><span data-ttu-id="f6abb-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-409">-1,000.00</span></span></td>
<td><span data-ttu-id="f6abb-410">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-411">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-412">5</span><span class="sxs-lookup"><span data-stu-id="f6abb-412">5</span></span></td>
<td><span data-ttu-id="f6abb-413">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="f6abb-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="f6abb-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-414">-1,008.00</span></span></td>
<td><span data-ttu-id="f6abb-415">1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-415">1,008.00</span></span></td>
<td><span data-ttu-id="f6abb-416">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-417">6</span><span class="sxs-lookup"><span data-stu-id="f6abb-417">6</span></span></td>
<td><span data-ttu-id="f6abb-418">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="f6abb-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-419">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-420">7</span><span class="sxs-lookup"><span data-stu-id="f6abb-420">7</span></span></td>
<td><span data-ttu-id="f6abb-421">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="f6abb-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-422">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-423">8</span><span class="sxs-lookup"><span data-stu-id="f6abb-423">8</span></span></td>
<td><span data-ttu-id="f6abb-424">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-425">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-426">9</span><span class="sxs-lookup"><span data-stu-id="f6abb-426">9</span></span></td>
<td><span data-ttu-id="f6abb-427">Kontanter</span><span class="sxs-lookup"><span data-stu-id="f6abb-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-428">-1,008.00</span></span></td>
<td><span data-ttu-id="f6abb-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-430">10</span><span class="sxs-lookup"><span data-stu-id="f6abb-430">10</span></span></td>
<td><span data-ttu-id="f6abb-431">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="f6abb-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-432">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6abb-433">11</span><span class="sxs-lookup"><span data-stu-id="f6abb-433">11</span></span></td>
<td><span data-ttu-id="f6abb-434">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="f6abb-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f6abb-435">0,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6abb-436">Hvis du vil bruke IFRS 16-tallene til å kjøre den samme råbalansen, må lovbestemte regnskapsjournaloppføringer tilbakeføres, og IFRS 16-journaloppføringer må posteres.</span><span class="sxs-lookup"><span data-stu-id="f6abb-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="f6abb-437">For å tilbakeføre lovbestemte journaloppføringer omfatter dette eksemplet et lovbestemt tilbakeføringstablå som har samme konfigurasjon som det lovbestemte tablået, men en motsatt posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="f6abb-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="f6abb-438">Det lovbestemte tablået *debiterte* for eksempel en leieutgiftskonto, men tilbakeføringstablået *krediterer* denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="f6abb-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="f6abb-439">Disse relasjonene kan enkelt defineres i posteringskontoene for Aktivaleie på siden **Parametere for aktivaleie** (**Aktivaleie \> Oppsett \> Parametere for aktivaleie**).</span><span class="sxs-lookup"><span data-stu-id="f6abb-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="f6abb-440">Når den samme prosessen som ble brukt for det lovbestemte tablået, brukes for tilbakeføringstablået, produseres følgende journaloppføring.</span><span class="sxs-lookup"><span data-stu-id="f6abb-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="f6abb-441">Forskjellen er at tilbakeføringstablået posterer tilbakeføringsoppføringene fra det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="f6abb-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="f6abb-442">Tilbakeføringsoppføringene gjøres også på det egendefinerte laget.</span><span class="sxs-lookup"><span data-stu-id="f6abb-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="f6abb-443">Når en råbalanse kjøres på det gjeldende laget, blir ikke tilbakeføringsjournaloppføringene tatt med.</span><span class="sxs-lookup"><span data-stu-id="f6abb-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="f6abb-444">Leiebetaling – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="f6abb-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="f6abb-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-445">Account type</span></span> | <span data-ttu-id="f6abb-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-446">Account number</span></span> | <span data-ttu-id="f6abb-447">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-447">Layer</span></span>  | <span data-ttu-id="f6abb-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-448">Account description</span></span> | <span data-ttu-id="f6abb-449">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-449">Debit</span></span>    | <span data-ttu-id="f6abb-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="f6abb-451">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-451">Ledger</span></span>       | <span data-ttu-id="f6abb-452">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-452">4</span></span>              | <span data-ttu-id="f6abb-453">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-453">Custom</span></span> | <span data-ttu-id="f6abb-454">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-454">Clearing account</span></span>    | <span data-ttu-id="f6abb-455">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-455">1,000.00</span></span> |          |
| <span data-ttu-id="f6abb-456">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-456">Ledger</span></span>       | <span data-ttu-id="f6abb-457">1</span><span class="sxs-lookup"><span data-stu-id="f6abb-457">1</span></span>              | <span data-ttu-id="f6abb-458">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-458">Custom</span></span> | <span data-ttu-id="f6abb-459">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-459">Lease expense</span></span>       |          | <span data-ttu-id="f6abb-460">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-460">1,000.00</span></span> |

<span data-ttu-id="f6abb-461">Nå som du har fjernet de lovbestemte journaloppføringene, skal du postere alle journaloppføringer som kreves av IFRS 16, i IFRS 16-tablået.</span><span class="sxs-lookup"><span data-stu-id="f6abb-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="f6abb-462">Disse oppføringene omfatter den opprinnelige føringen av bruksrettseiendelen og gjelden, og posten for rente og avskrivning.</span><span class="sxs-lookup"><span data-stu-id="f6abb-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="f6abb-463">Opprinnelig føring – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="f6abb-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="f6abb-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-464">Account type</span></span> | <span data-ttu-id="f6abb-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-465">Account number</span></span> | <span data-ttu-id="f6abb-466">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-466">Layer</span></span>  | <span data-ttu-id="f6abb-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-467">Account description</span></span>      | <span data-ttu-id="f6abb-468">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-468">Debit</span></span>     | <span data-ttu-id="f6abb-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="f6abb-470">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-470">Ledger</span></span>       | <span data-ttu-id="f6abb-471">6</span><span class="sxs-lookup"><span data-stu-id="f6abb-471">6</span></span>              | <span data-ttu-id="f6abb-472">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-472">Custom</span></span> | <span data-ttu-id="f6abb-473">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="f6abb-473">ROU Asset</span></span>                | <span data-ttu-id="f6abb-474">22 793,90</span><span class="sxs-lookup"><span data-stu-id="f6abb-474">22,793.90</span></span> |           |
| <span data-ttu-id="f6abb-475">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-475">Ledger</span></span>       | <span data-ttu-id="f6abb-476">7</span><span class="sxs-lookup"><span data-stu-id="f6abb-476">7</span></span>              | <span data-ttu-id="f6abb-477">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-477">Custom</span></span> | <span data-ttu-id="f6abb-478">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="f6abb-478">Finance lease obligation</span></span> |           | <span data-ttu-id="f6abb-479">22 793,90</span><span class="sxs-lookup"><span data-stu-id="f6abb-479">22,793.90</span></span> |

<span data-ttu-id="f6abb-480">Leiebetalingen posteres som de andre leiebetalingene.</span><span class="sxs-lookup"><span data-stu-id="f6abb-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="f6abb-481">Grunnen til å bruke avregningskontoen er å sikre at kontanter bare krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="f6abb-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="f6abb-482">Leiebetaling – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="f6abb-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="f6abb-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-483">Account type</span></span> | <span data-ttu-id="f6abb-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-484">Account number</span></span> | <span data-ttu-id="f6abb-485">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-485">Layer</span></span>  | <span data-ttu-id="f6abb-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-486">Account description</span></span>      | <span data-ttu-id="f6abb-487">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-487">Debit</span></span>    | <span data-ttu-id="f6abb-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="f6abb-489">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-489">Ledger</span></span>       | <span data-ttu-id="f6abb-490">7</span><span class="sxs-lookup"><span data-stu-id="f6abb-490">7</span></span>              | <span data-ttu-id="f6abb-491">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-491">Custom</span></span> | <span data-ttu-id="f6abb-492">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="f6abb-492">Finance lease obligation</span></span> | <span data-ttu-id="f6abb-493">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-493">1,000.00</span></span> |          |
| <span data-ttu-id="f6abb-494">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-494">Ledger</span></span>       | <span data-ttu-id="f6abb-495">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-495">4</span></span>              | <span data-ttu-id="f6abb-496">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-496">Custom</span></span> | <span data-ttu-id="f6abb-497">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-497">Clearing account</span></span>         |          | <span data-ttu-id="f6abb-498">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f6abb-498">1,000.00</span></span> |

<span data-ttu-id="f6abb-499">Journaloppføringen for renteutgift genereres fra nedbetalingsplanen for gjeld.</span><span class="sxs-lookup"><span data-stu-id="f6abb-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="f6abb-500">Renteutgift – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="f6abb-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="f6abb-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-501">Account type</span></span> | <span data-ttu-id="f6abb-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-502">Account number</span></span> | <span data-ttu-id="f6abb-503">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-503">Layer</span></span>  | <span data-ttu-id="f6abb-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-504">Account description</span></span>      | <span data-ttu-id="f6abb-505">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-505">Debit</span></span> | <span data-ttu-id="f6abb-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="f6abb-507">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-507">Ledger</span></span>       | <span data-ttu-id="f6abb-508">8</span><span class="sxs-lookup"><span data-stu-id="f6abb-508">8</span></span>              | <span data-ttu-id="f6abb-509">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-509">Custom</span></span> | <span data-ttu-id="f6abb-510">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-510">Interest expense</span></span>         | <span data-ttu-id="f6abb-511">94.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-511">94.97</span></span> |        |
| <span data-ttu-id="f6abb-512">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-512">Ledger</span></span>       | <span data-ttu-id="f6abb-513">7</span><span class="sxs-lookup"><span data-stu-id="f6abb-513">7</span></span>              | <span data-ttu-id="f6abb-514">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-514">Custom</span></span> | <span data-ttu-id="f6abb-515">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="f6abb-515">Finance lease obligation</span></span> |       | <span data-ttu-id="f6abb-516">94.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-516">94.97</span></span>  |

<span data-ttu-id="f6abb-517">Journaloppføringen for avskrivningskostnad genereres fra avskrivningsplanen for aktiva.</span><span class="sxs-lookup"><span data-stu-id="f6abb-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="f6abb-518">Avskrivningskostnad – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="f6abb-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="f6abb-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="f6abb-519">Account type</span></span> | <span data-ttu-id="f6abb-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="f6abb-520">Account number</span></span> | <span data-ttu-id="f6abb-521">Lag</span><span class="sxs-lookup"><span data-stu-id="f6abb-521">Layer</span></span>  | <span data-ttu-id="f6abb-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-522">Account description</span></span>      | <span data-ttu-id="f6abb-523">Debet</span><span class="sxs-lookup"><span data-stu-id="f6abb-523">Debit</span></span>  | <span data-ttu-id="f6abb-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="f6abb-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="f6abb-525">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-525">Ledger</span></span>       | <span data-ttu-id="f6abb-526">10</span><span class="sxs-lookup"><span data-stu-id="f6abb-526">10</span></span>             | <span data-ttu-id="f6abb-527">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-527">Custom</span></span> | <span data-ttu-id="f6abb-528">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="f6abb-528">Depreciation expense</span></span>     | <span data-ttu-id="f6abb-529">949.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-529">949.75</span></span> |        |
| <span data-ttu-id="f6abb-530">Finans</span><span class="sxs-lookup"><span data-stu-id="f6abb-530">Ledger</span></span>       | <span data-ttu-id="f6abb-531">11</span><span class="sxs-lookup"><span data-stu-id="f6abb-531">11</span></span>             | <span data-ttu-id="f6abb-532">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f6abb-532">Custom</span></span> | <span data-ttu-id="f6abb-533">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="f6abb-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="f6abb-534">949.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-534">949.75</span></span> |

<span data-ttu-id="f6abb-535">Når alle disse journaloppføringene er opprettet og postert, vises følgende verdier for egendefinert lag 1.</span><span class="sxs-lookup"><span data-stu-id="f6abb-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="f6abb-536">Vær oppmerksom på at den siste kolonnen omfatter bankgebyret, merverdiavgift (mva) og reduksjonen i kontanter fra forrige lag, men den omfatter ikke journaloppføringene for lovbestemt rapportering.</span><span class="sxs-lookup"><span data-stu-id="f6abb-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="f6abb-537">Derfor oppnår du ekte funksjonalitet for dobbel rapportering.</span><span class="sxs-lookup"><span data-stu-id="f6abb-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="f6abb-538">Nå trenger firmaet bare å kjøre råbalansen og kombinere det gjeldende laget og det egendefinerte laget for å opprette en IFRS-råbalanse.</span><span class="sxs-lookup"><span data-stu-id="f6abb-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="f6abb-539">Kontonr.</span><span class="sxs-lookup"><span data-stu-id="f6abb-539">Account No</span></span> | <span data-ttu-id="f6abb-540">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f6abb-540">Description</span></span>              | <span data-ttu-id="f6abb-541">Lovbestemt tablå\-gjeldende lag\-JE\-100\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-542">Lovbestemt tablå\-gjeldende lag\-JE\-110\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-543">Lovbestemt tablå\-gjeldende lag\-JE\-120\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-544">Gjeldende lag \- totaler</span><span class="sxs-lookup"><span data-stu-id="f6abb-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="f6abb-545">Tilbakeføringstablå\-egendefinert lag\-JE\-130\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-546">IFRS 16-tablå\-egendefinert lag\-JE\-140\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-547">IFRS 16-tablå\-egendefinert lag\-JE\-150\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-548">IFRS 16-tablå\-egendefinert lag\-JE\-160\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-549">IFRS 16-tablå\-egendefinert lag\-JE\-170\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="f6abb-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="f6abb-550">Egendefinert lag \+ gjeldende lag \- totaler</span><span class="sxs-lookup"><span data-stu-id="f6abb-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="f6abb-551">1</span><span class="sxs-lookup"><span data-stu-id="f6abb-551">1</span></span>          | <span data-ttu-id="f6abb-552">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-552">Lease expense</span></span>            | <span data-ttu-id="f6abb-553">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="f6abb-554">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-554">1,000\.00</span></span>               |   | <span data-ttu-id="f6abb-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="f6abb-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="f6abb-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-556">0\.00</span></span>                                   |
| <span data-ttu-id="f6abb-557">2</span><span class="sxs-lookup"><span data-stu-id="f6abb-557">2</span></span>          | <span data-ttu-id="f6abb-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="f6abb-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="f6abb-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="f6abb-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f6abb-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-561">3\.00</span></span>                                   |
| <span data-ttu-id="f6abb-562">3</span><span class="sxs-lookup"><span data-stu-id="f6abb-562">3</span></span>          | <span data-ttu-id="f6abb-563">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="f6abb-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="f6abb-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f6abb-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-566">5\.00</span></span>                                   |
| <span data-ttu-id="f6abb-567">4</span><span class="sxs-lookup"><span data-stu-id="f6abb-567">4</span></span>          | <span data-ttu-id="f6abb-568">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="f6abb-568">Clearing account</span></span>         | <span data-ttu-id="f6abb-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="f6abb-570">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="f6abb-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-571">0\.00</span></span>                   |   | <span data-ttu-id="f6abb-572">1 000</span><span class="sxs-lookup"><span data-stu-id="f6abb-572">1,000</span></span>                                           |                                                | <span data-ttu-id="f6abb-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="f6abb-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="f6abb-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-574">0\.00</span></span>                                   |
| <span data-ttu-id="f6abb-575">5</span><span class="sxs-lookup"><span data-stu-id="f6abb-575">5</span></span>          | <span data-ttu-id="f6abb-576">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="f6abb-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="f6abb-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="f6abb-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-578">1,008\.00</span></span>                                         | <span data-ttu-id="f6abb-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f6abb-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-580">0\.00</span></span>                                   |
| <span data-ttu-id="f6abb-581">6</span><span class="sxs-lookup"><span data-stu-id="f6abb-581">6</span></span>          | <span data-ttu-id="f6abb-582">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="f6abb-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="f6abb-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="f6abb-584">22,794</span><span class="sxs-lookup"><span data-stu-id="f6abb-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="f6abb-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="f6abb-585">22,793\.90</span></span>                              |
| <span data-ttu-id="f6abb-586">7</span><span class="sxs-lookup"><span data-stu-id="f6abb-586">7</span></span>          | <span data-ttu-id="f6abb-587">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="f6abb-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="f6abb-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="f6abb-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="f6abb-589">\-22,794</span></span>                                       | <span data-ttu-id="f6abb-590">1 000</span><span class="sxs-lookup"><span data-stu-id="f6abb-590">1,000</span></span>                                          | <span data-ttu-id="f6abb-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="f6abb-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="f6abb-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="f6abb-593">8</span><span class="sxs-lookup"><span data-stu-id="f6abb-593">8</span></span>          | <span data-ttu-id="f6abb-594">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="f6abb-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="f6abb-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="f6abb-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="f6abb-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="f6abb-597">94\.97</span></span>                                  |
| <span data-ttu-id="f6abb-598">9</span><span class="sxs-lookup"><span data-stu-id="f6abb-598">9</span></span>          | <span data-ttu-id="f6abb-599">Kontanter</span><span class="sxs-lookup"><span data-stu-id="f6abb-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="f6abb-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="f6abb-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f6abb-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="f6abb-603">10</span><span class="sxs-lookup"><span data-stu-id="f6abb-603">10</span></span>         | <span data-ttu-id="f6abb-604">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="f6abb-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="f6abb-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="f6abb-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-606">949\.75</span></span>                                        | <span data-ttu-id="f6abb-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-607">949\.75</span></span>                                 |
| <span data-ttu-id="f6abb-608">11</span><span class="sxs-lookup"><span data-stu-id="f6abb-608">11</span></span>         | <span data-ttu-id="f6abb-609">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="f6abb-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="f6abb-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="f6abb-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="f6abb-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-611">\-949\.75</span></span>                                      | <span data-ttu-id="f6abb-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="f6abb-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]