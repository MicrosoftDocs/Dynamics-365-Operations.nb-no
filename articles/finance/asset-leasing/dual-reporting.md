---
title: Dobbel rapportering
description: Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446582"
---
# <a name="dual-reporting"></a><span data-ttu-id="6c36e-103">Dobbel rapportering</span><span class="sxs-lookup"><span data-stu-id="6c36e-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c36e-104">Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="6c36e-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="6c36e-105">Det er nødvendig å ha erfaring med posteringslag i Microsoft Dynamics 365 Finance, og dette gjør det enklere å forstå eksemplet.</span><span class="sxs-lookup"><span data-stu-id="6c36e-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="6c36e-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6c36e-106">Example</span></span>

<span data-ttu-id="6c36e-107">Det følgende eksemplet gjør rede for en leieavtale under italiensk lovbestemt rapportering, ved hjelp av både kontantprinsippmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="6c36e-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="6c36e-108">Firmaet må opprette tre tablåer for å følge både de italienske lovbestemte kravene og IFRS 16-kravene.</span><span class="sxs-lookup"><span data-stu-id="6c36e-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="6c36e-109">Det kreves ett tablå for IFRS 16, ett tablå for lovbestemte krav og ett tablå for å tilbakeføre lovbestemte posteringer automatisk.</span><span class="sxs-lookup"><span data-stu-id="6c36e-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="6c36e-110">Tablåene blir opprettet som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="6c36e-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="6c36e-111">**IFRS 16-tablå**</span><span class="sxs-lookup"><span data-stu-id="6c36e-111">**IFRS 16 book**</span></span>

<span data-ttu-id="6c36e-112">IFRS 16-tablået konfigureres slik at det er i samsvar med IFRS 16-regnskapsstandarden.</span><span class="sxs-lookup"><span data-stu-id="6c36e-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="6c36e-113">Alle oppføringer som posteres i dette tablået, posteres på et egendefinert lag.</span><span class="sxs-lookup"><span data-stu-id="6c36e-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="6c36e-114">Navn</span><span class="sxs-lookup"><span data-stu-id="6c36e-114">Name</span></span>                                    | <span data-ttu-id="6c36e-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="6c36e-116">Registertype</span><span class="sxs-lookup"><span data-stu-id="6c36e-116">Book type</span></span>                               | <span data-ttu-id="6c36e-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="6c36e-117">IFRS 16</span></span>        |
| <span data-ttu-id="6c36e-118">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-118">Book description</span></span>                        | <span data-ttu-id="6c36e-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="6c36e-119">IFRS 16</span></span>        |
| <span data-ttu-id="6c36e-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="6c36e-120">Posting Layer</span></span>                           | <span data-ttu-id="6c36e-121">Tilpasset lag 1</span><span class="sxs-lookup"><span data-stu-id="6c36e-121">Custom layer 1</span></span> |
| <span data-ttu-id="6c36e-122">Leietype</span><span class="sxs-lookup"><span data-stu-id="6c36e-122">Lease Type</span></span>                              | <span data-ttu-id="6c36e-123">Finance</span><span class="sxs-lookup"><span data-stu-id="6c36e-123">Finance</span></span>        |
| <span data-ttu-id="6c36e-124">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="6c36e-124">Accounting Framework</span></span>                    | <span data-ttu-id="6c36e-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="6c36e-125">IFRS 16</span></span>        |
| <span data-ttu-id="6c36e-126">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="6c36e-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="6c36e-127">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-127">0.00</span></span>           |
| <span data-ttu-id="6c36e-128">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="6c36e-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="6c36e-129">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-129">0.00</span></span>           |
| <span data-ttu-id="6c36e-130">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="6c36e-130">Short-term threshold</span></span>                    | <span data-ttu-id="6c36e-131">12</span><span class="sxs-lookup"><span data-stu-id="6c36e-131">12</span></span>             |
| <span data-ttu-id="6c36e-132">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="6c36e-132">Low Value Threshold</span></span>                     | <span data-ttu-id="6c36e-133">5 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-133">5,000.00</span></span>       |
| <span data-ttu-id="6c36e-134">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="6c36e-134">Pay to Vendor</span></span>                           | <span data-ttu-id="6c36e-135">Nr.</span><span class="sxs-lookup"><span data-stu-id="6c36e-135">No</span></span>             |

<span data-ttu-id="6c36e-136">**Lovbestemt tablå**</span><span class="sxs-lookup"><span data-stu-id="6c36e-136">**Statutory book**</span></span>

<span data-ttu-id="6c36e-137">Det lovbestemte tablået er et kontantprinsipptablå der firmaet gjør rede for leieutgiftene som kontantbeløpet som betales hver måned i leie.</span><span class="sxs-lookup"><span data-stu-id="6c36e-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="6c36e-138">Dette tablået produserer ikke en bruksrettseiendel eller leieforpliktelse.</span><span class="sxs-lookup"><span data-stu-id="6c36e-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="6c36e-139">Navn</span><span class="sxs-lookup"><span data-stu-id="6c36e-139">Name</span></span>                                    | <span data-ttu-id="6c36e-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="6c36e-141">Registertype</span><span class="sxs-lookup"><span data-stu-id="6c36e-141">Book type</span></span>                               | <span data-ttu-id="6c36e-142">Lovbestemt</span><span class="sxs-lookup"><span data-stu-id="6c36e-142">Statutory</span></span>   |
| <span data-ttu-id="6c36e-143">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-143">Book description</span></span>                        | <span data-ttu-id="6c36e-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="6c36e-144">Local GAAP</span></span>  |
| <span data-ttu-id="6c36e-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="6c36e-145">Posting Layer</span></span>                           | <span data-ttu-id="6c36e-146">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-146">Current</span></span>     |
| <span data-ttu-id="6c36e-147">Leietype</span><span class="sxs-lookup"><span data-stu-id="6c36e-147">Lease Type</span></span>                              | <span data-ttu-id="6c36e-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="6c36e-148">Automatic</span></span>   |
| <span data-ttu-id="6c36e-149">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="6c36e-149">Accounting Framework</span></span>                    | <span data-ttu-id="6c36e-150">Kontantgrunnlag</span><span class="sxs-lookup"><span data-stu-id="6c36e-150">Cash basis</span></span>  |
| <span data-ttu-id="6c36e-151">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="6c36e-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="6c36e-152">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-152">0.00</span></span>        |
| <span data-ttu-id="6c36e-153">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="6c36e-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="6c36e-154">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-154">0.00</span></span>        |
| <span data-ttu-id="6c36e-155">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="6c36e-155">Short-term threshold</span></span>                    | <span data-ttu-id="6c36e-156">0</span><span class="sxs-lookup"><span data-stu-id="6c36e-156">0</span></span>           |
| <span data-ttu-id="6c36e-157">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="6c36e-157">Low Value Threshold</span></span>                     | <span data-ttu-id="6c36e-158">0</span><span class="sxs-lookup"><span data-stu-id="6c36e-158">0</span></span>           |
| <span data-ttu-id="6c36e-159">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="6c36e-159">Pay to Vendor</span></span>                           | <span data-ttu-id="6c36e-160">Nr.</span><span class="sxs-lookup"><span data-stu-id="6c36e-160">No</span></span>          |

<span data-ttu-id="6c36e-161">**Lovbestemt tilbakeføringstablå**</span><span class="sxs-lookup"><span data-stu-id="6c36e-161">**Statutory reversal book**</span></span>

<span data-ttu-id="6c36e-162">Det lovbestemte tilbakeføringstablået konfigureres på samme måte som det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="6c36e-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="6c36e-163">Navn</span><span class="sxs-lookup"><span data-stu-id="6c36e-163">Name</span></span>                                    | <span data-ttu-id="6c36e-164">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="6c36e-165">Registertype</span><span class="sxs-lookup"><span data-stu-id="6c36e-165">Book type</span></span>                               | <span data-ttu-id="6c36e-166">Lovbestemt – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="6c36e-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="6c36e-167">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-167">Book description</span></span>                        | <span data-ttu-id="6c36e-168">Tablå for å tilbakeføre lovbestemt tablå</span><span class="sxs-lookup"><span data-stu-id="6c36e-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="6c36e-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="6c36e-169">Posting Layer</span></span>                           | <span data-ttu-id="6c36e-170">Tilpasset lag 1</span><span class="sxs-lookup"><span data-stu-id="6c36e-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="6c36e-171">Leietype</span><span class="sxs-lookup"><span data-stu-id="6c36e-171">Lease Type</span></span>                              | <span data-ttu-id="6c36e-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="6c36e-172">Automatic</span></span>                      |
| <span data-ttu-id="6c36e-173">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="6c36e-173">Accounting Framework</span></span>                    | <span data-ttu-id="6c36e-174">Kontantgrunnlag</span><span class="sxs-lookup"><span data-stu-id="6c36e-174">Cash basis</span></span>                     |
| <span data-ttu-id="6c36e-175">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="6c36e-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="6c36e-176">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-176">0.00</span></span>                           |
| <span data-ttu-id="6c36e-177">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="6c36e-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="6c36e-178">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-178">0.00</span></span>                           |
| <span data-ttu-id="6c36e-179">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="6c36e-179">Short-term threshold</span></span>                    | <span data-ttu-id="6c36e-180">0</span><span class="sxs-lookup"><span data-stu-id="6c36e-180">0</span></span>                              |
| <span data-ttu-id="6c36e-181">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="6c36e-181">Low Value Threshold</span></span>                     | <span data-ttu-id="6c36e-182">0</span><span class="sxs-lookup"><span data-stu-id="6c36e-182">0</span></span>                              |
| <span data-ttu-id="6c36e-183">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="6c36e-183">Pay to Vendor</span></span>                           | <span data-ttu-id="6c36e-184">Nr.</span><span class="sxs-lookup"><span data-stu-id="6c36e-184">No</span></span>                             |

<span data-ttu-id="6c36e-185">I dette eksemplet er det opprettet en leieavtale som har følgende innstillinger i fanene **Generelt** og **Linjer i betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="6c36e-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="6c36e-186">**Fanen Generelt**</span><span class="sxs-lookup"><span data-stu-id="6c36e-186">**General tab**</span></span>

| <span data-ttu-id="6c36e-187">Felt</span><span class="sxs-lookup"><span data-stu-id="6c36e-187">Field</span></span>                      | <span data-ttu-id="6c36e-188">Verdi</span><span class="sxs-lookup"><span data-stu-id="6c36e-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="6c36e-189">Trinnvis lånerente</span><span class="sxs-lookup"><span data-stu-id="6c36e-189">Incremental borrowing rate</span></span> | <span data-ttu-id="6c36e-190">5 %</span><span class="sxs-lookup"><span data-stu-id="6c36e-190">5%</span></span>               |
| <span data-ttu-id="6c36e-191">Startdato</span><span class="sxs-lookup"><span data-stu-id="6c36e-191">Commencement date</span></span>          | <span data-ttu-id="6c36e-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="6c36e-192">1/1/2020</span></span>         |
| <span data-ttu-id="6c36e-193">Leiegruppe</span><span class="sxs-lookup"><span data-stu-id="6c36e-193">Lease group</span></span>                | <span data-ttu-id="6c36e-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="6c36e-194">Buildings</span></span>        |
| <span data-ttu-id="6c36e-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="6c36e-195">Vendor</span></span>                     | <span data-ttu-id="6c36e-196">1001</span><span class="sxs-lookup"><span data-stu-id="6c36e-196">1001</span></span>             |
| <span data-ttu-id="6c36e-197">Aktivaets gjennomsnittsverdi</span><span class="sxs-lookup"><span data-stu-id="6c36e-197">Fair value of the asset</span></span>    | <span data-ttu-id="6c36e-198">245 000</span><span class="sxs-lookup"><span data-stu-id="6c36e-198">245,000</span></span>          |
| <span data-ttu-id="6c36e-199">Aktivalevetid</span><span class="sxs-lookup"><span data-stu-id="6c36e-199">Asset useful life</span></span>          | <span data-ttu-id="6c36e-200">120</span><span class="sxs-lookup"><span data-stu-id="6c36e-200">120</span></span>              |
| <span data-ttu-id="6c36e-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="6c36e-201">Annuity type</span></span>               | <span data-ttu-id="6c36e-202">Vanlig annuitet</span><span class="sxs-lookup"><span data-stu-id="6c36e-202">Ordinary annuity</span></span> |
| <span data-ttu-id="6c36e-203">Sammensetningsintervall</span><span class="sxs-lookup"><span data-stu-id="6c36e-203">Compounding interval</span></span>       | <span data-ttu-id="6c36e-204">Månedlig</span><span class="sxs-lookup"><span data-stu-id="6c36e-204">Monthly</span></span>          |

<span data-ttu-id="6c36e-205">**Fanen Linjer i betalingsplan**</span><span class="sxs-lookup"><span data-stu-id="6c36e-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="6c36e-206">Felt</span><span class="sxs-lookup"><span data-stu-id="6c36e-206">Field</span></span>             | <span data-ttu-id="6c36e-207">Verdi</span><span class="sxs-lookup"><span data-stu-id="6c36e-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="6c36e-208">Startdato</span><span class="sxs-lookup"><span data-stu-id="6c36e-208">Start date</span></span>        | <span data-ttu-id="6c36e-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="6c36e-209">1/1/2020</span></span>   |
| <span data-ttu-id="6c36e-210">Periodeintervall</span><span class="sxs-lookup"><span data-stu-id="6c36e-210">Period interval</span></span>   | <span data-ttu-id="6c36e-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="6c36e-211">Months</span></span>     |
| <span data-ttu-id="6c36e-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="6c36e-212">Periods</span></span>           | <span data-ttu-id="6c36e-213">24</span><span class="sxs-lookup"><span data-stu-id="6c36e-213">24</span></span>         |
| <span data-ttu-id="6c36e-214">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="6c36e-214">End date</span></span>          | <span data-ttu-id="6c36e-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="6c36e-215">12/31/2020</span></span> |
| <span data-ttu-id="6c36e-216">Betalingsfrekvens</span><span class="sxs-lookup"><span data-stu-id="6c36e-216">Payment frequency</span></span> | <span data-ttu-id="6c36e-217">Månedlig</span><span class="sxs-lookup"><span data-stu-id="6c36e-217">Monthly</span></span>    |
| <span data-ttu-id="6c36e-218">Betalingsbeløp</span><span class="sxs-lookup"><span data-stu-id="6c36e-218">Payment amount</span></span>    | <span data-ttu-id="6c36e-219">1 000</span><span class="sxs-lookup"><span data-stu-id="6c36e-219">1,000</span></span>      |

<span data-ttu-id="6c36e-220">Hvis du vil gjøre rede for denne leien under to rammeverk, bruker du et gjeldende posteringslag og et egendefinert posteringslag.</span><span class="sxs-lookup"><span data-stu-id="6c36e-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="6c36e-221">Følgende tabell viser et eksempel på hver journaloppføring som kreves for å representere økonomien riktig under hver rapporteringsstandard.</span><span class="sxs-lookup"><span data-stu-id="6c36e-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="6c36e-222">En detaljert beskrivelse av hver journaloppføring for den første måneden av leieavtalen gis etterpå.</span><span class="sxs-lookup"><span data-stu-id="6c36e-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="6c36e-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="6c36e-224">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="6c36e-225">Lovbestemt tablå (gjeldende lag)</span><span class="sxs-lookup"><span data-stu-id="6c36e-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="6c36e-226">Gjeldende lag totalt</span><span class="sxs-lookup"><span data-stu-id="6c36e-226">Current layer total</span></span></th>
<th><span data-ttu-id="6c36e-227">Tilbakeføringstablå (egendefinert lag)</span><span class="sxs-lookup"><span data-stu-id="6c36e-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="6c36e-228">IFRS 16-tablå (egendefinert lag)</span><span class="sxs-lookup"><span data-stu-id="6c36e-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="6c36e-229">Gjeldende lag + egendefinert lag totalt</span><span class="sxs-lookup"><span data-stu-id="6c36e-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c36e-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="6c36e-230">JE-100</span></span></th>
<th><span data-ttu-id="6c36e-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="6c36e-231">JE-110</span></span></th>
<th><span data-ttu-id="6c36e-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="6c36e-232">JE-120</span></span></th>
<th><span data-ttu-id="6c36e-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="6c36e-233">JE-130</span></span></th>
<th><span data-ttu-id="6c36e-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="6c36e-234">JE-140</span></span></th>
<th><span data-ttu-id="6c36e-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="6c36e-235">JE-150</span></span></th>
<th><span data-ttu-id="6c36e-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="6c36e-236">JE-160</span></span></th>
<th><span data-ttu-id="6c36e-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="6c36e-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c36e-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c36e-246">1</span><span class="sxs-lookup"><span data-stu-id="6c36e-246">1</span></span></td>
<td><span data-ttu-id="6c36e-247">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-247">Lease expense</span></span></td>
<td><span data-ttu-id="6c36e-248">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-249">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-249">1,000.00</span></span></td>
<td><span data-ttu-id="6c36e-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-251">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-252">2</span><span class="sxs-lookup"><span data-stu-id="6c36e-252">2</span></span></td>
<td><span data-ttu-id="6c36e-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="6c36e-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-254">3,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-255">3,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-256">3,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-257">3</span><span class="sxs-lookup"><span data-stu-id="6c36e-257">3</span></span></td>
<td><span data-ttu-id="6c36e-258">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-259">5,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-260">5,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-261">5,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-262">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-262">4</span></span></td>
<td><span data-ttu-id="6c36e-263">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-263">Clearing account</span></span></td>
<td><span data-ttu-id="6c36e-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-264">-1,000.00</span></span></td>
<td><span data-ttu-id="6c36e-265">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-266">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-266">0.00</span></span></td>
<td><span data-ttu-id="6c36e-267">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-269">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-270">5</span><span class="sxs-lookup"><span data-stu-id="6c36e-270">5</span></span></td>
<td><span data-ttu-id="6c36e-271">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="6c36e-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-272">-1,008.00</span></span></td>
<td><span data-ttu-id="6c36e-273">1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-273">1,008.00</span></span></td>
<td><span data-ttu-id="6c36e-274">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-275">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-276">6</span><span class="sxs-lookup"><span data-stu-id="6c36e-276">6</span></span></td>
<td><span data-ttu-id="6c36e-277">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="6c36e-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-278">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-279">22 794,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-280">22 793,90</span><span class="sxs-lookup"><span data-stu-id="6c36e-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-281">7</span><span class="sxs-lookup"><span data-stu-id="6c36e-281">7</span></span></td>
<td><span data-ttu-id="6c36e-282">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="6c36e-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-283">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-284">-22,794.00</span></span></td>
<td><span data-ttu-id="6c36e-285">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-285">1,000.00</span></span></td>
<td><span data-ttu-id="6c36e-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="6c36e-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="6c36e-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-288">8</span><span class="sxs-lookup"><span data-stu-id="6c36e-288">8</span></span></td>
<td><span data-ttu-id="6c36e-289">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-290">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-291">94.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-292">94.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-293">9</span><span class="sxs-lookup"><span data-stu-id="6c36e-293">9</span></span></td>
<td><span data-ttu-id="6c36e-294">Kontanter</span><span class="sxs-lookup"><span data-stu-id="6c36e-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-295">-1,008.00</span></span></td>
<td><span data-ttu-id="6c36e-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-298">10</span><span class="sxs-lookup"><span data-stu-id="6c36e-298">10</span></span></td>
<td><span data-ttu-id="6c36e-299">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="6c36e-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-300">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-301">949.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-301">949.75</span></span></td>
<td><span data-ttu-id="6c36e-302">949.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-303">11</span><span class="sxs-lookup"><span data-stu-id="6c36e-303">11</span></span></td>
<td><span data-ttu-id="6c36e-304">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="6c36e-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-305">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="6c36e-306">-949.75</span></span></td>
<td><span data-ttu-id="6c36e-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="6c36e-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c36e-308">Som den foregående tabellen viser kreves det tre tablåer for å rapportere både under lovbestemt rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="6c36e-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="6c36e-309">Det lovbestemte tablået registrerer leiebetalingen i henhold til reglene for kontantprinsippregnskap under det gjeldende laget.</span><span class="sxs-lookup"><span data-stu-id="6c36e-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="6c36e-310">Det lovbestemte tilbakeføringstablået tilbakestiller lovbestemte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="6c36e-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="6c36e-311">IFRS 16-tablået oppretter journaloppføringene som kreves under IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="6c36e-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="6c36e-312">Du trenger bare å angi en leieavtale én gang.</span><span class="sxs-lookup"><span data-stu-id="6c36e-312">You must enter a lease only one time.</span></span> <span data-ttu-id="6c36e-313">Du kan deretter åpne **Tablåer**-siden for å se alle tablåene som er knyttet til leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="6c36e-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="6c36e-314">Når du oppretter tablåene, må alle tre knyttes til samme leiepost.</span><span class="sxs-lookup"><span data-stu-id="6c36e-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="6c36e-315">Den første journaloppføringen registrerer leieutgiften under det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="6c36e-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="6c36e-316">Du kan opprette betalingene i en bunke eller ved å velge betalingsplanen i det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="6c36e-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="6c36e-317">I dette eksemplet produseres følgende journaloppføring for det lovbestemte tablået fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="6c36e-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="6c36e-318">Leiebetaling – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="6c36e-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="6c36e-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-319">Account type</span></span> | <span data-ttu-id="6c36e-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-320">Account number</span></span> | <span data-ttu-id="6c36e-321">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-321">Layer</span></span>   | <span data-ttu-id="6c36e-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-322">Account description</span></span> | <span data-ttu-id="6c36e-323">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-323">Debit</span></span>    | <span data-ttu-id="6c36e-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="6c36e-325">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-325">Ledger</span></span>       | <span data-ttu-id="6c36e-326">1</span><span class="sxs-lookup"><span data-stu-id="6c36e-326">1</span></span>              | <span data-ttu-id="6c36e-327">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-327">Current</span></span> | <span data-ttu-id="6c36e-328">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-328">Lease expense</span></span>       | <span data-ttu-id="6c36e-329">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-329">1,000.00</span></span> |          |
| <span data-ttu-id="6c36e-330">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-330">Ledger</span></span>       | <span data-ttu-id="6c36e-331">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-331">4</span></span>              | <span data-ttu-id="6c36e-332">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-332">Current</span></span> | <span data-ttu-id="6c36e-333">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-333">Clearing account</span></span>    |          | <span data-ttu-id="6c36e-334">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-334">1,000.00</span></span> |

<span data-ttu-id="6c36e-335">En regnskapsassistent bruker standard Dynamics 365-funksjonalitet til å opprette en faktura for å betale leien utenfor Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="6c36e-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="6c36e-336">I stedet for å velge **Leieutgift** som debetkonto velger regnskapsassistenten en avregningskonto for å generere følgende oppføring.</span><span class="sxs-lookup"><span data-stu-id="6c36e-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="6c36e-337">AP-prosess – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="6c36e-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="6c36e-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-338">Account type</span></span> | <span data-ttu-id="6c36e-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-339">Account number</span></span> | <span data-ttu-id="6c36e-340">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-340">Layer</span></span>   | <span data-ttu-id="6c36e-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-341">Account description</span></span> | <span data-ttu-id="6c36e-342">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-342">Debit</span></span>    | <span data-ttu-id="6c36e-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="6c36e-344">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-344">Ledger</span></span>       | <span data-ttu-id="6c36e-345">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-345">4</span></span>              | <span data-ttu-id="6c36e-346">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-346">Current</span></span> | <span data-ttu-id="6c36e-347">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-347">Clearing account</span></span>    | <span data-ttu-id="6c36e-348">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-348">1,000.00</span></span> |          |
| <span data-ttu-id="6c36e-349">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-349">Ledger</span></span>       | <span data-ttu-id="6c36e-350">2</span><span class="sxs-lookup"><span data-stu-id="6c36e-350">2</span></span>              | <span data-ttu-id="6c36e-351">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-351">Current</span></span> | <span data-ttu-id="6c36e-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="6c36e-352">Bank fee</span></span>            | <span data-ttu-id="6c36e-353">3,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-353">3.00</span></span>     |          |
| <span data-ttu-id="6c36e-354">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-354">Ledger</span></span>       | <span data-ttu-id="6c36e-355">3</span><span class="sxs-lookup"><span data-stu-id="6c36e-355">3</span></span>              | <span data-ttu-id="6c36e-356">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-356">Current</span></span> | <span data-ttu-id="6c36e-357">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-357">VAT expense</span></span>         | <span data-ttu-id="6c36e-358">5,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-358">5.00</span></span>     |          |
| <span data-ttu-id="6c36e-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="6c36e-359">Vendor</span></span>       | <span data-ttu-id="6c36e-360">5</span><span class="sxs-lookup"><span data-stu-id="6c36e-360">5</span></span>              | <span data-ttu-id="6c36e-361">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-361">Current</span></span> | <span data-ttu-id="6c36e-362">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="6c36e-362">Accounts payable</span></span>    |          | <span data-ttu-id="6c36e-363">1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-363">1,008.00</span></span> |

<span data-ttu-id="6c36e-364">Når utdraget er utstedt til leverandøren, følger du den vanlige betalingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="6c36e-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="6c36e-365">Følgende journaloppføring genereres i løpet av denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="6c36e-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="6c36e-366">Kontantbetaling – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="6c36e-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="6c36e-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-367">Account type</span></span> | <span data-ttu-id="6c36e-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-368">Account number</span></span> | <span data-ttu-id="6c36e-369">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-369">Layer</span></span>   | <span data-ttu-id="6c36e-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-370">Account description</span></span> | <span data-ttu-id="6c36e-371">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-371">Debit</span></span>    | <span data-ttu-id="6c36e-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="6c36e-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="6c36e-373">Vendor</span></span>       | <span data-ttu-id="6c36e-374">5</span><span class="sxs-lookup"><span data-stu-id="6c36e-374">5</span></span>              | <span data-ttu-id="6c36e-375">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-375">Current</span></span> | <span data-ttu-id="6c36e-376">Leverandører</span><span class="sxs-lookup"><span data-stu-id="6c36e-376">Accounts Payable</span></span>    | <span data-ttu-id="6c36e-377">1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-377">1,008.00</span></span> |          |
| <span data-ttu-id="6c36e-378">Bank</span><span class="sxs-lookup"><span data-stu-id="6c36e-378">Bank</span></span>         | <span data-ttu-id="6c36e-379">9</span><span class="sxs-lookup"><span data-stu-id="6c36e-379">9</span></span>              | <span data-ttu-id="6c36e-380">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="6c36e-380">Current</span></span> | <span data-ttu-id="6c36e-381">Kontanter</span><span class="sxs-lookup"><span data-stu-id="6c36e-381">Cash</span></span>                |          | <span data-ttu-id="6c36e-382">1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-382">1,008.00</span></span> |

<span data-ttu-id="6c36e-383">Nå har du gjort fullstendig rede for denne leien under lovbestemte rapporteringskrav og kan generere en råbalanse ved hjelp av det gjeldende laget.</span><span class="sxs-lookup"><span data-stu-id="6c36e-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="6c36e-384">Systemet returnerer en råbalanse med følgende tall.</span><span class="sxs-lookup"><span data-stu-id="6c36e-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="6c36e-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="6c36e-386">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="6c36e-387">Lovbestemt tablå (gjeldende lag)</span><span class="sxs-lookup"><span data-stu-id="6c36e-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="6c36e-388">Gjeldende lag totalt</span><span class="sxs-lookup"><span data-stu-id="6c36e-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c36e-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="6c36e-389">JE-100</span></span></th>
<th><span data-ttu-id="6c36e-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="6c36e-390">JE-110</span></span></th>
<th><span data-ttu-id="6c36e-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="6c36e-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c36e-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="6c36e-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="6c36e-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c36e-395">1</span><span class="sxs-lookup"><span data-stu-id="6c36e-395">1</span></span></td>
<td><span data-ttu-id="6c36e-396">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-396">Lease expense</span></span></td>
<td><span data-ttu-id="6c36e-397">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-398">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-399">2</span><span class="sxs-lookup"><span data-stu-id="6c36e-399">2</span></span></td>
<td><span data-ttu-id="6c36e-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="6c36e-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-401">3,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-402">3,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-403">3</span><span class="sxs-lookup"><span data-stu-id="6c36e-403">3</span></span></td>
<td><span data-ttu-id="6c36e-404">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-405">5,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-406">5,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-407">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-407">4</span></span></td>
<td><span data-ttu-id="6c36e-408">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-408">Clearing account</span></span></td>
<td><span data-ttu-id="6c36e-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-409">-1,000.00</span></span></td>
<td><span data-ttu-id="6c36e-410">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-411">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-412">5</span><span class="sxs-lookup"><span data-stu-id="6c36e-412">5</span></span></td>
<td><span data-ttu-id="6c36e-413">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="6c36e-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="6c36e-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-414">-1,008.00</span></span></td>
<td><span data-ttu-id="6c36e-415">1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-415">1,008.00</span></span></td>
<td><span data-ttu-id="6c36e-416">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-417">6</span><span class="sxs-lookup"><span data-stu-id="6c36e-417">6</span></span></td>
<td><span data-ttu-id="6c36e-418">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="6c36e-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-419">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-420">7</span><span class="sxs-lookup"><span data-stu-id="6c36e-420">7</span></span></td>
<td><span data-ttu-id="6c36e-421">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="6c36e-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-422">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-423">8</span><span class="sxs-lookup"><span data-stu-id="6c36e-423">8</span></span></td>
<td><span data-ttu-id="6c36e-424">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-425">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-426">9</span><span class="sxs-lookup"><span data-stu-id="6c36e-426">9</span></span></td>
<td><span data-ttu-id="6c36e-427">Kontanter</span><span class="sxs-lookup"><span data-stu-id="6c36e-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-428">-1,008.00</span></span></td>
<td><span data-ttu-id="6c36e-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-430">10</span><span class="sxs-lookup"><span data-stu-id="6c36e-430">10</span></span></td>
<td><span data-ttu-id="6c36e-431">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="6c36e-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-432">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c36e-433">11</span><span class="sxs-lookup"><span data-stu-id="6c36e-433">11</span></span></td>
<td><span data-ttu-id="6c36e-434">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="6c36e-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="6c36e-435">0,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c36e-436">Hvis du vil bruke IFRS 16-tallene til å kjøre den samme råbalansen, må lovbestemte regnskapsjournaloppføringer tilbakeføres, og IFRS 16-journaloppføringer må posteres.</span><span class="sxs-lookup"><span data-stu-id="6c36e-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="6c36e-437">For å tilbakeføre lovbestemte journaloppføringer omfatter dette eksemplet et lovbestemt tilbakeføringstablå som har samme konfigurasjon som det lovbestemte tablået, men en motsatt posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="6c36e-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="6c36e-438">Det lovbestemte tablået *debiterte* for eksempel en leieutgiftskonto, men tilbakeføringstablået *krediterer* denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="6c36e-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="6c36e-439">Disse relasjonene kan enkelt defineres i posteringskontoene for Aktivaleie på siden **Parametere for aktivaleie** (**Aktivaleie \> Oppsett \> Parametere for aktivaleie**).</span><span class="sxs-lookup"><span data-stu-id="6c36e-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="6c36e-440">Når den samme prosessen som ble brukt for det lovbestemte tablået, brukes for tilbakeføringstablået, produseres følgende journaloppføring.</span><span class="sxs-lookup"><span data-stu-id="6c36e-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="6c36e-441">Forskjellen er at tilbakeføringstablået posterer tilbakeføringsoppføringene fra det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="6c36e-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="6c36e-442">Tilbakeføringsoppføringene gjøres også på det egendefinerte laget.</span><span class="sxs-lookup"><span data-stu-id="6c36e-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="6c36e-443">Når en råbalanse kjøres på det gjeldende laget, blir ikke tilbakeføringsjournaloppføringene tatt med.</span><span class="sxs-lookup"><span data-stu-id="6c36e-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="6c36e-444">Leiebetaling – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="6c36e-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="6c36e-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-445">Account type</span></span> | <span data-ttu-id="6c36e-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-446">Account number</span></span> | <span data-ttu-id="6c36e-447">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-447">Layer</span></span>  | <span data-ttu-id="6c36e-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-448">Account description</span></span> | <span data-ttu-id="6c36e-449">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-449">Debit</span></span>    | <span data-ttu-id="6c36e-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="6c36e-451">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-451">Ledger</span></span>       | <span data-ttu-id="6c36e-452">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-452">4</span></span>              | <span data-ttu-id="6c36e-453">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-453">Custom</span></span> | <span data-ttu-id="6c36e-454">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-454">Clearing account</span></span>    | <span data-ttu-id="6c36e-455">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-455">1,000.00</span></span> |          |
| <span data-ttu-id="6c36e-456">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-456">Ledger</span></span>       | <span data-ttu-id="6c36e-457">1</span><span class="sxs-lookup"><span data-stu-id="6c36e-457">1</span></span>              | <span data-ttu-id="6c36e-458">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-458">Custom</span></span> | <span data-ttu-id="6c36e-459">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-459">Lease expense</span></span>       |          | <span data-ttu-id="6c36e-460">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-460">1,000.00</span></span> |

<span data-ttu-id="6c36e-461">Nå som du har fjernet de lovbestemte journaloppføringene, skal du postere alle journaloppføringer som kreves av IFRS 16, i IFRS 16-tablået.</span><span class="sxs-lookup"><span data-stu-id="6c36e-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="6c36e-462">Disse oppføringene omfatter den opprinnelige føringen av bruksrettseiendelen og gjelden, og posten for rente og avskrivning.</span><span class="sxs-lookup"><span data-stu-id="6c36e-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="6c36e-463">Opprinnelig føring – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="6c36e-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="6c36e-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-464">Account type</span></span> | <span data-ttu-id="6c36e-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-465">Account number</span></span> | <span data-ttu-id="6c36e-466">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-466">Layer</span></span>  | <span data-ttu-id="6c36e-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-467">Account description</span></span>      | <span data-ttu-id="6c36e-468">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-468">Debit</span></span>     | <span data-ttu-id="6c36e-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="6c36e-470">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-470">Ledger</span></span>       | <span data-ttu-id="6c36e-471">6</span><span class="sxs-lookup"><span data-stu-id="6c36e-471">6</span></span>              | <span data-ttu-id="6c36e-472">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-472">Custom</span></span> | <span data-ttu-id="6c36e-473">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="6c36e-473">ROU Asset</span></span>                | <span data-ttu-id="6c36e-474">22 793,90</span><span class="sxs-lookup"><span data-stu-id="6c36e-474">22,793.90</span></span> |           |
| <span data-ttu-id="6c36e-475">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-475">Ledger</span></span>       | <span data-ttu-id="6c36e-476">7</span><span class="sxs-lookup"><span data-stu-id="6c36e-476">7</span></span>              | <span data-ttu-id="6c36e-477">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-477">Custom</span></span> | <span data-ttu-id="6c36e-478">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="6c36e-478">Finance lease obligation</span></span> |           | <span data-ttu-id="6c36e-479">22 793,90</span><span class="sxs-lookup"><span data-stu-id="6c36e-479">22,793.90</span></span> |

<span data-ttu-id="6c36e-480">Leiebetalingen posteres som de andre leiebetalingene.</span><span class="sxs-lookup"><span data-stu-id="6c36e-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="6c36e-481">Grunnen til å bruke avregningskontoen er å sikre at kontanter bare krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="6c36e-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="6c36e-482">Leiebetaling – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="6c36e-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="6c36e-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-483">Account type</span></span> | <span data-ttu-id="6c36e-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-484">Account number</span></span> | <span data-ttu-id="6c36e-485">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-485">Layer</span></span>  | <span data-ttu-id="6c36e-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-486">Account description</span></span>      | <span data-ttu-id="6c36e-487">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-487">Debit</span></span>    | <span data-ttu-id="6c36e-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="6c36e-489">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-489">Ledger</span></span>       | <span data-ttu-id="6c36e-490">7</span><span class="sxs-lookup"><span data-stu-id="6c36e-490">7</span></span>              | <span data-ttu-id="6c36e-491">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-491">Custom</span></span> | <span data-ttu-id="6c36e-492">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="6c36e-492">Finance lease obligation</span></span> | <span data-ttu-id="6c36e-493">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-493">1,000.00</span></span> |          |
| <span data-ttu-id="6c36e-494">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-494">Ledger</span></span>       | <span data-ttu-id="6c36e-495">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-495">4</span></span>              | <span data-ttu-id="6c36e-496">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-496">Custom</span></span> | <span data-ttu-id="6c36e-497">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-497">Clearing account</span></span>         |          | <span data-ttu-id="6c36e-498">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6c36e-498">1,000.00</span></span> |

<span data-ttu-id="6c36e-499">Journaloppføringen for renteutgift genereres fra nedbetalingsplanen for gjeld.</span><span class="sxs-lookup"><span data-stu-id="6c36e-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="6c36e-500">Renteutgift – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="6c36e-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="6c36e-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-501">Account type</span></span> | <span data-ttu-id="6c36e-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-502">Account number</span></span> | <span data-ttu-id="6c36e-503">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-503">Layer</span></span>  | <span data-ttu-id="6c36e-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-504">Account description</span></span>      | <span data-ttu-id="6c36e-505">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-505">Debit</span></span> | <span data-ttu-id="6c36e-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="6c36e-507">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-507">Ledger</span></span>       | <span data-ttu-id="6c36e-508">8</span><span class="sxs-lookup"><span data-stu-id="6c36e-508">8</span></span>              | <span data-ttu-id="6c36e-509">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-509">Custom</span></span> | <span data-ttu-id="6c36e-510">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-510">Interest expense</span></span>         | <span data-ttu-id="6c36e-511">94.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-511">94.97</span></span> |        |
| <span data-ttu-id="6c36e-512">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-512">Ledger</span></span>       | <span data-ttu-id="6c36e-513">7</span><span class="sxs-lookup"><span data-stu-id="6c36e-513">7</span></span>              | <span data-ttu-id="6c36e-514">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-514">Custom</span></span> | <span data-ttu-id="6c36e-515">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="6c36e-515">Finance lease obligation</span></span> |       | <span data-ttu-id="6c36e-516">94.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-516">94.97</span></span>  |

<span data-ttu-id="6c36e-517">Journaloppføringen for avskrivningskostnad genereres fra avskrivningsplanen for aktiva.</span><span class="sxs-lookup"><span data-stu-id="6c36e-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="6c36e-518">Avskrivningskostnad – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="6c36e-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="6c36e-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="6c36e-519">Account type</span></span> | <span data-ttu-id="6c36e-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6c36e-520">Account number</span></span> | <span data-ttu-id="6c36e-521">Lag</span><span class="sxs-lookup"><span data-stu-id="6c36e-521">Layer</span></span>  | <span data-ttu-id="6c36e-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-522">Account description</span></span>      | <span data-ttu-id="6c36e-523">Debet</span><span class="sxs-lookup"><span data-stu-id="6c36e-523">Debit</span></span>  | <span data-ttu-id="6c36e-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="6c36e-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="6c36e-525">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-525">Ledger</span></span>       | <span data-ttu-id="6c36e-526">10</span><span class="sxs-lookup"><span data-stu-id="6c36e-526">10</span></span>             | <span data-ttu-id="6c36e-527">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-527">Custom</span></span> | <span data-ttu-id="6c36e-528">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="6c36e-528">Depreciation expense</span></span>     | <span data-ttu-id="6c36e-529">949.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-529">949.75</span></span> |        |
| <span data-ttu-id="6c36e-530">Finans</span><span class="sxs-lookup"><span data-stu-id="6c36e-530">Ledger</span></span>       | <span data-ttu-id="6c36e-531">11</span><span class="sxs-lookup"><span data-stu-id="6c36e-531">11</span></span>             | <span data-ttu-id="6c36e-532">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="6c36e-532">Custom</span></span> | <span data-ttu-id="6c36e-533">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="6c36e-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="6c36e-534">949.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-534">949.75</span></span> |

<span data-ttu-id="6c36e-535">Når alle disse journaloppføringene er opprettet og postert, vises følgende verdier for egendefinert lag 1.</span><span class="sxs-lookup"><span data-stu-id="6c36e-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="6c36e-536">Vær oppmerksom på at den siste kolonnen omfatter bankgebyret, merverdiavgift (mva) og reduksjonen i kontanter fra forrige lag, men den omfatter ikke journaloppføringene for lovbestemt rapportering.</span><span class="sxs-lookup"><span data-stu-id="6c36e-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="6c36e-537">Derfor oppnår du ekte funksjonalitet for dobbel rapportering.</span><span class="sxs-lookup"><span data-stu-id="6c36e-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="6c36e-538">Nå trenger firmaet bare å kjøre råbalansen og kombinere det gjeldende laget og det egendefinerte laget for å opprette en IFRS-råbalanse.</span><span class="sxs-lookup"><span data-stu-id="6c36e-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="6c36e-539">Kontonr.</span><span class="sxs-lookup"><span data-stu-id="6c36e-539">Account No</span></span> | <span data-ttu-id="6c36e-540">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c36e-540">Description</span></span>              | <span data-ttu-id="6c36e-541">Lovbestemt tablå\-gjeldende lag\-JE\-100\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-542">Lovbestemt tablå\-gjeldende lag\-JE\-110\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-543">Lovbestemt tablå\-gjeldende lag\-JE\-120\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-544">Gjeldende lag \- totaler</span><span class="sxs-lookup"><span data-stu-id="6c36e-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="6c36e-545">Tilbakeføringstablå\-egendefinert lag\-JE\-130\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-546">IFRS 16-tablå\-egendefinert lag\-JE\-140\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-547">IFRS 16-tablå\-egendefinert lag\-JE\-150\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-548">IFRS 16-tablå\-egendefinert lag\-JE\-160\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-549">IFRS 16-tablå\-egendefinert lag\-JE\-170\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="6c36e-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="6c36e-550">Egendefinert lag \+ gjeldende lag \- totaler</span><span class="sxs-lookup"><span data-stu-id="6c36e-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="6c36e-551">1</span><span class="sxs-lookup"><span data-stu-id="6c36e-551">1</span></span>          | <span data-ttu-id="6c36e-552">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-552">Lease expense</span></span>            | <span data-ttu-id="6c36e-553">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="6c36e-554">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-554">1,000\.00</span></span>               |   | <span data-ttu-id="6c36e-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="6c36e-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="6c36e-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-556">0\.00</span></span>                                   |
| <span data-ttu-id="6c36e-557">2</span><span class="sxs-lookup"><span data-stu-id="6c36e-557">2</span></span>          | <span data-ttu-id="6c36e-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="6c36e-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="6c36e-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="6c36e-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="6c36e-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-561">3\.00</span></span>                                   |
| <span data-ttu-id="6c36e-562">3</span><span class="sxs-lookup"><span data-stu-id="6c36e-562">3</span></span>          | <span data-ttu-id="6c36e-563">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="6c36e-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="6c36e-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="6c36e-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-566">5\.00</span></span>                                   |
| <span data-ttu-id="6c36e-567">4</span><span class="sxs-lookup"><span data-stu-id="6c36e-567">4</span></span>          | <span data-ttu-id="6c36e-568">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="6c36e-568">Clearing account</span></span>         | <span data-ttu-id="6c36e-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="6c36e-570">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="6c36e-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-571">0\.00</span></span>                   |   | <span data-ttu-id="6c36e-572">1 000</span><span class="sxs-lookup"><span data-stu-id="6c36e-572">1,000</span></span>                                           |                                                | <span data-ttu-id="6c36e-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="6c36e-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="6c36e-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-574">0\.00</span></span>                                   |
| <span data-ttu-id="6c36e-575">5</span><span class="sxs-lookup"><span data-stu-id="6c36e-575">5</span></span>          | <span data-ttu-id="6c36e-576">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="6c36e-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="6c36e-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="6c36e-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-578">1,008\.00</span></span>                                         | <span data-ttu-id="6c36e-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="6c36e-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-580">0\.00</span></span>                                   |
| <span data-ttu-id="6c36e-581">6</span><span class="sxs-lookup"><span data-stu-id="6c36e-581">6</span></span>          | <span data-ttu-id="6c36e-582">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="6c36e-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="6c36e-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="6c36e-584">22,794</span><span class="sxs-lookup"><span data-stu-id="6c36e-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="6c36e-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="6c36e-585">22,793\.90</span></span>                              |
| <span data-ttu-id="6c36e-586">7</span><span class="sxs-lookup"><span data-stu-id="6c36e-586">7</span></span>          | <span data-ttu-id="6c36e-587">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="6c36e-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="6c36e-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="6c36e-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="6c36e-589">\-22,794</span></span>                                       | <span data-ttu-id="6c36e-590">1 000</span><span class="sxs-lookup"><span data-stu-id="6c36e-590">1,000</span></span>                                          | <span data-ttu-id="6c36e-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="6c36e-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="6c36e-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="6c36e-593">8</span><span class="sxs-lookup"><span data-stu-id="6c36e-593">8</span></span>          | <span data-ttu-id="6c36e-594">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="6c36e-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="6c36e-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="6c36e-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="6c36e-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="6c36e-597">94\.97</span></span>                                  |
| <span data-ttu-id="6c36e-598">9</span><span class="sxs-lookup"><span data-stu-id="6c36e-598">9</span></span>          | <span data-ttu-id="6c36e-599">Kontanter</span><span class="sxs-lookup"><span data-stu-id="6c36e-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="6c36e-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="6c36e-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="6c36e-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="6c36e-603">10</span><span class="sxs-lookup"><span data-stu-id="6c36e-603">10</span></span>         | <span data-ttu-id="6c36e-604">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="6c36e-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="6c36e-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="6c36e-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-606">949\.75</span></span>                                        | <span data-ttu-id="6c36e-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-607">949\.75</span></span>                                 |
| <span data-ttu-id="6c36e-608">11</span><span class="sxs-lookup"><span data-stu-id="6c36e-608">11</span></span>         | <span data-ttu-id="6c36e-609">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="6c36e-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="6c36e-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="6c36e-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="6c36e-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-611">\-949\.75</span></span>                                      | <span data-ttu-id="6c36e-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="6c36e-612">\-949\.75</span></span>                               |


