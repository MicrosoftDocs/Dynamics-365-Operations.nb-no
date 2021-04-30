---
title: Dobbel rapportering
description: Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881162"
---
# <a name="dual-reporting"></a><span data-ttu-id="d6e87-103">Dobbel rapportering</span><span class="sxs-lookup"><span data-stu-id="d6e87-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6e87-104">Dette emnet leder deg gjennom et eksempel som viser hvordan du kan oppfylle kravene for både IFRS-rapportering (International Financial Reporting Standard) og lovbestemt rapportering i Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="d6e87-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="d6e87-105">Det er nødvendig å ha erfaring med posteringslag i Microsoft Dynamics 365 Finance, og dette gjør det enklere å forstå eksemplet.</span><span class="sxs-lookup"><span data-stu-id="d6e87-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="d6e87-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d6e87-106">Example</span></span>

<span data-ttu-id="d6e87-107">Det følgende eksemplet gjør rede for en leieavtale under italiensk lovbestemt rapportering, ved hjelp av både kontantprinsippmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="d6e87-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="d6e87-108">Firmaet må opprette tre tablåer for å følge både de italienske lovbestemte kravene og IFRS 16-kravene.</span><span class="sxs-lookup"><span data-stu-id="d6e87-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="d6e87-109">Det kreves ett tablå for IFRS 16, ett tablå for lovbestemte krav og ett tablå for å tilbakeføre lovbestemte posteringer automatisk.</span><span class="sxs-lookup"><span data-stu-id="d6e87-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="d6e87-110">Tablåene blir opprettet som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="d6e87-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="d6e87-111">**IFRS 16-tablå**</span><span class="sxs-lookup"><span data-stu-id="d6e87-111">**IFRS 16 book**</span></span>

<span data-ttu-id="d6e87-112">IFRS 16-tablået konfigureres slik at det er i samsvar med IFRS 16-regnskapsstandarden.</span><span class="sxs-lookup"><span data-stu-id="d6e87-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="d6e87-113">Alle oppføringer som posteres i dette tablået, posteres på et egendefinert lag.</span><span class="sxs-lookup"><span data-stu-id="d6e87-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="d6e87-114">Navn</span><span class="sxs-lookup"><span data-stu-id="d6e87-114">Name</span></span>                                    | <span data-ttu-id="d6e87-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="d6e87-116">Registertype</span><span class="sxs-lookup"><span data-stu-id="d6e87-116">Book type</span></span>                               | <span data-ttu-id="d6e87-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="d6e87-117">IFRS 16</span></span>        |
| <span data-ttu-id="d6e87-118">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-118">Book description</span></span>                        | <span data-ttu-id="d6e87-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="d6e87-119">IFRS 16</span></span>        |
| <span data-ttu-id="d6e87-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="d6e87-120">Posting Layer</span></span>                           | <span data-ttu-id="d6e87-121">Tilpasset lag 1</span><span class="sxs-lookup"><span data-stu-id="d6e87-121">Custom layer 1</span></span> |
| <span data-ttu-id="d6e87-122">Leietype</span><span class="sxs-lookup"><span data-stu-id="d6e87-122">Lease Type</span></span>                              | <span data-ttu-id="d6e87-123">Finance</span><span class="sxs-lookup"><span data-stu-id="d6e87-123">Finance</span></span>        |
| <span data-ttu-id="d6e87-124">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="d6e87-124">Accounting Framework</span></span>                    | <span data-ttu-id="d6e87-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="d6e87-125">IFRS 16</span></span>        |
| <span data-ttu-id="d6e87-126">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="d6e87-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="d6e87-127">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-127">0.00</span></span>           |
| <span data-ttu-id="d6e87-128">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="d6e87-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="d6e87-129">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-129">0.00</span></span>           |
| <span data-ttu-id="d6e87-130">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="d6e87-130">Short-term threshold</span></span>                    | <span data-ttu-id="d6e87-131">12</span><span class="sxs-lookup"><span data-stu-id="d6e87-131">12</span></span>             |
| <span data-ttu-id="d6e87-132">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="d6e87-132">Low Value Threshold</span></span>                     | <span data-ttu-id="d6e87-133">5 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-133">5,000.00</span></span>       |
| <span data-ttu-id="d6e87-134">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="d6e87-134">Pay to Vendor</span></span>                           | <span data-ttu-id="d6e87-135">Nr.</span><span class="sxs-lookup"><span data-stu-id="d6e87-135">No</span></span>             |

<span data-ttu-id="d6e87-136">**Lovbestemt tablå**</span><span class="sxs-lookup"><span data-stu-id="d6e87-136">**Statutory book**</span></span>

<span data-ttu-id="d6e87-137">Det lovbestemte tablået er et kontantprinsipptablå der firmaet gjør rede for leieutgiftene som kontantbeløpet som betales hver måned i leie.</span><span class="sxs-lookup"><span data-stu-id="d6e87-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="d6e87-138">Dette tablået produserer ikke en bruksrettseiendel eller leieforpliktelse.</span><span class="sxs-lookup"><span data-stu-id="d6e87-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="d6e87-139">Navn</span><span class="sxs-lookup"><span data-stu-id="d6e87-139">Name</span></span>                                    | <span data-ttu-id="d6e87-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="d6e87-141">Registertype</span><span class="sxs-lookup"><span data-stu-id="d6e87-141">Book type</span></span>                               | <span data-ttu-id="d6e87-142">Lovbestemt</span><span class="sxs-lookup"><span data-stu-id="d6e87-142">Statutory</span></span>   |
| <span data-ttu-id="d6e87-143">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-143">Book description</span></span>                        | <span data-ttu-id="d6e87-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="d6e87-144">Local GAAP</span></span>  |
| <span data-ttu-id="d6e87-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="d6e87-145">Posting Layer</span></span>                           | <span data-ttu-id="d6e87-146">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-146">Current</span></span>     |
| <span data-ttu-id="d6e87-147">Leietype</span><span class="sxs-lookup"><span data-stu-id="d6e87-147">Lease Type</span></span>                              | <span data-ttu-id="d6e87-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="d6e87-148">Automatic</span></span>   |
| <span data-ttu-id="d6e87-149">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="d6e87-149">Accounting Framework</span></span>                    | <span data-ttu-id="d6e87-150">Kontantgrunnlag</span><span class="sxs-lookup"><span data-stu-id="d6e87-150">Cash basis</span></span>  |
| <span data-ttu-id="d6e87-151">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="d6e87-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="d6e87-152">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-152">0.00</span></span>        |
| <span data-ttu-id="d6e87-153">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="d6e87-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="d6e87-154">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-154">0.00</span></span>        |
| <span data-ttu-id="d6e87-155">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="d6e87-155">Short-term threshold</span></span>                    | <span data-ttu-id="d6e87-156">0</span><span class="sxs-lookup"><span data-stu-id="d6e87-156">0</span></span>           |
| <span data-ttu-id="d6e87-157">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="d6e87-157">Low Value Threshold</span></span>                     | <span data-ttu-id="d6e87-158">0</span><span class="sxs-lookup"><span data-stu-id="d6e87-158">0</span></span>           |
| <span data-ttu-id="d6e87-159">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="d6e87-159">Pay to Vendor</span></span>                           | <span data-ttu-id="d6e87-160">Nr.</span><span class="sxs-lookup"><span data-stu-id="d6e87-160">No</span></span>          |

<span data-ttu-id="d6e87-161">**Lovbestemt tilbakeføringstablå**</span><span class="sxs-lookup"><span data-stu-id="d6e87-161">**Statutory reversal book**</span></span>

<span data-ttu-id="d6e87-162">Det lovbestemte tilbakeføringstablået konfigureres på samme måte som det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="d6e87-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="d6e87-163">Navn</span><span class="sxs-lookup"><span data-stu-id="d6e87-163">Name</span></span>                                    | <span data-ttu-id="d6e87-164">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="d6e87-165">Registertype</span><span class="sxs-lookup"><span data-stu-id="d6e87-165">Book type</span></span>                               | <span data-ttu-id="d6e87-166">Lovbestemt – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="d6e87-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="d6e87-167">Tablåbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-167">Book description</span></span>                        | <span data-ttu-id="d6e87-168">Tablå for å tilbakeføre lovbestemt tablå</span><span class="sxs-lookup"><span data-stu-id="d6e87-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="d6e87-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="d6e87-169">Posting Layer</span></span>                           | <span data-ttu-id="d6e87-170">Tilpasset lag 1</span><span class="sxs-lookup"><span data-stu-id="d6e87-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="d6e87-171">Leietype</span><span class="sxs-lookup"><span data-stu-id="d6e87-171">Lease Type</span></span>                              | <span data-ttu-id="d6e87-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="d6e87-172">Automatic</span></span>                      |
| <span data-ttu-id="d6e87-173">Regnskapsrammeverk</span><span class="sxs-lookup"><span data-stu-id="d6e87-173">Accounting Framework</span></span>                    | <span data-ttu-id="d6e87-174">Kontantgrunnlag</span><span class="sxs-lookup"><span data-stu-id="d6e87-174">Cash basis</span></span>                     |
| <span data-ttu-id="d6e87-175">Konfigurasjon av leieperiode / levetid</span><span class="sxs-lookup"><span data-stu-id="d6e87-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="d6e87-176">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-176">0.00</span></span>                           |
| <span data-ttu-id="d6e87-177">Konfigurasjon av nåværende verdi / virkelig verdi på aktivum</span><span class="sxs-lookup"><span data-stu-id="d6e87-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="d6e87-178">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-178">0.00</span></span>                           |
| <span data-ttu-id="d6e87-179">Korttidsterskel</span><span class="sxs-lookup"><span data-stu-id="d6e87-179">Short-term threshold</span></span>                    | <span data-ttu-id="d6e87-180">0</span><span class="sxs-lookup"><span data-stu-id="d6e87-180">0</span></span>                              |
| <span data-ttu-id="d6e87-181">Lavverditerskel</span><span class="sxs-lookup"><span data-stu-id="d6e87-181">Low Value Threshold</span></span>                     | <span data-ttu-id="d6e87-182">0</span><span class="sxs-lookup"><span data-stu-id="d6e87-182">0</span></span>                              |
| <span data-ttu-id="d6e87-183">Betal til leverandør</span><span class="sxs-lookup"><span data-stu-id="d6e87-183">Pay to Vendor</span></span>                           | <span data-ttu-id="d6e87-184">Nr.</span><span class="sxs-lookup"><span data-stu-id="d6e87-184">No</span></span>                             |

<span data-ttu-id="d6e87-185">I dette eksemplet er det opprettet en leieavtale som har følgende innstillinger i fanene **Generelt** og **Linjer i betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="d6e87-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="d6e87-186">**Fanen Generelt**</span><span class="sxs-lookup"><span data-stu-id="d6e87-186">**General tab**</span></span>

| <span data-ttu-id="d6e87-187">Felt</span><span class="sxs-lookup"><span data-stu-id="d6e87-187">Field</span></span>                      | <span data-ttu-id="d6e87-188">Verdi</span><span class="sxs-lookup"><span data-stu-id="d6e87-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="d6e87-189">Trinnvis lånerente</span><span class="sxs-lookup"><span data-stu-id="d6e87-189">Incremental borrowing rate</span></span> | <span data-ttu-id="d6e87-190">5 %</span><span class="sxs-lookup"><span data-stu-id="d6e87-190">5%</span></span>               |
| <span data-ttu-id="d6e87-191">Startdato</span><span class="sxs-lookup"><span data-stu-id="d6e87-191">Commencement date</span></span>          | <span data-ttu-id="d6e87-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="d6e87-192">1/1/2020</span></span>         |
| <span data-ttu-id="d6e87-193">Leiegruppe</span><span class="sxs-lookup"><span data-stu-id="d6e87-193">Lease group</span></span>                | <span data-ttu-id="d6e87-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="d6e87-194">Buildings</span></span>        |
| <span data-ttu-id="d6e87-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="d6e87-195">Vendor</span></span>                     | <span data-ttu-id="d6e87-196">1001</span><span class="sxs-lookup"><span data-stu-id="d6e87-196">1001</span></span>             |
| <span data-ttu-id="d6e87-197">Aktivaets gjennomsnittsverdi</span><span class="sxs-lookup"><span data-stu-id="d6e87-197">Fair value of the asset</span></span>    | <span data-ttu-id="d6e87-198">245 000</span><span class="sxs-lookup"><span data-stu-id="d6e87-198">245,000</span></span>          |
| <span data-ttu-id="d6e87-199">Aktivalevetid</span><span class="sxs-lookup"><span data-stu-id="d6e87-199">Asset useful life</span></span>          | <span data-ttu-id="d6e87-200">120</span><span class="sxs-lookup"><span data-stu-id="d6e87-200">120</span></span>              |
| <span data-ttu-id="d6e87-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="d6e87-201">Annuity type</span></span>               | <span data-ttu-id="d6e87-202">Vanlig annuitet</span><span class="sxs-lookup"><span data-stu-id="d6e87-202">Ordinary annuity</span></span> |
| <span data-ttu-id="d6e87-203">Sammensetningsintervall</span><span class="sxs-lookup"><span data-stu-id="d6e87-203">Compounding interval</span></span>       | <span data-ttu-id="d6e87-204">Månedlig</span><span class="sxs-lookup"><span data-stu-id="d6e87-204">Monthly</span></span>          |

<span data-ttu-id="d6e87-205">**Fanen Linjer i betalingsplan**</span><span class="sxs-lookup"><span data-stu-id="d6e87-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="d6e87-206">Felt</span><span class="sxs-lookup"><span data-stu-id="d6e87-206">Field</span></span>             | <span data-ttu-id="d6e87-207">Verdi</span><span class="sxs-lookup"><span data-stu-id="d6e87-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="d6e87-208">Startdato</span><span class="sxs-lookup"><span data-stu-id="d6e87-208">Start date</span></span>        | <span data-ttu-id="d6e87-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="d6e87-209">1/1/2020</span></span>   |
| <span data-ttu-id="d6e87-210">Periodeintervall</span><span class="sxs-lookup"><span data-stu-id="d6e87-210">Period interval</span></span>   | <span data-ttu-id="d6e87-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="d6e87-211">Months</span></span>     |
| <span data-ttu-id="d6e87-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="d6e87-212">Periods</span></span>           | <span data-ttu-id="d6e87-213">24</span><span class="sxs-lookup"><span data-stu-id="d6e87-213">24</span></span>         |
| <span data-ttu-id="d6e87-214">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="d6e87-214">End date</span></span>          | <span data-ttu-id="d6e87-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="d6e87-215">12/31/2020</span></span> |
| <span data-ttu-id="d6e87-216">Betalingsfrekvens</span><span class="sxs-lookup"><span data-stu-id="d6e87-216">Payment frequency</span></span> | <span data-ttu-id="d6e87-217">Månedlig</span><span class="sxs-lookup"><span data-stu-id="d6e87-217">Monthly</span></span>    |
| <span data-ttu-id="d6e87-218">Betalingsbeløp</span><span class="sxs-lookup"><span data-stu-id="d6e87-218">Payment amount</span></span>    | <span data-ttu-id="d6e87-219">1 000</span><span class="sxs-lookup"><span data-stu-id="d6e87-219">1,000</span></span>      |

<span data-ttu-id="d6e87-220">Hvis du vil gjøre rede for denne leien under to rammeverk, bruker du et gjeldende posteringslag og et egendefinert posteringslag.</span><span class="sxs-lookup"><span data-stu-id="d6e87-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="d6e87-221">Følgende tabell viser et eksempel på hver journaloppføring som kreves for å representere økonomien riktig under hver rapporteringsstandard.</span><span class="sxs-lookup"><span data-stu-id="d6e87-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="d6e87-222">En detaljert beskrivelse av hver journaloppføring for den første måneden av leieavtalen gis etterpå.</span><span class="sxs-lookup"><span data-stu-id="d6e87-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="d6e87-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="d6e87-224">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="d6e87-225">Lovbestemt tablå (gjeldende lag)</span><span class="sxs-lookup"><span data-stu-id="d6e87-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="d6e87-226">Gjeldende lag totalt</span><span class="sxs-lookup"><span data-stu-id="d6e87-226">Current layer total</span></span></th>
<th><span data-ttu-id="d6e87-227">Tilbakeføringstablå (egendefinert lag)</span><span class="sxs-lookup"><span data-stu-id="d6e87-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="d6e87-228">IFRS 16-tablå (egendefinert lag)</span><span class="sxs-lookup"><span data-stu-id="d6e87-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="d6e87-229">Gjeldende lag + egendefinert lag totalt</span><span class="sxs-lookup"><span data-stu-id="d6e87-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d6e87-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="d6e87-230">JE-100</span></span></th>
<th><span data-ttu-id="d6e87-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="d6e87-231">JE-110</span></span></th>
<th><span data-ttu-id="d6e87-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="d6e87-232">JE-120</span></span></th>
<th><span data-ttu-id="d6e87-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="d6e87-233">JE-130</span></span></th>
<th><span data-ttu-id="d6e87-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="d6e87-234">JE-140</span></span></th>
<th><span data-ttu-id="d6e87-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="d6e87-235">JE-150</span></span></th>
<th><span data-ttu-id="d6e87-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="d6e87-236">JE-160</span></span></th>
<th><span data-ttu-id="d6e87-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="d6e87-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d6e87-238">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-239">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-240">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-241">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-242">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-243">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-244">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-245">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d6e87-246">1</span><span class="sxs-lookup"><span data-stu-id="d6e87-246">1</span></span></td>
<td><span data-ttu-id="d6e87-247">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-247">Lease expense</span></span></td>
<td><span data-ttu-id="d6e87-248">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-249">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-249">1,000.00</span></span></td>
<td><span data-ttu-id="d6e87-250">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-251">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-252">2</span><span class="sxs-lookup"><span data-stu-id="d6e87-252">2</span></span></td>
<td><span data-ttu-id="d6e87-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="d6e87-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-254">3,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-255">3,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-256">3,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-257">3</span><span class="sxs-lookup"><span data-stu-id="d6e87-257">3</span></span></td>
<td><span data-ttu-id="d6e87-258">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-259">5,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-260">5,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-261">5,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-262">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-262">4</span></span></td>
<td><span data-ttu-id="d6e87-263">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-263">Clearing account</span></span></td>
<td><span data-ttu-id="d6e87-264">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-264">-1,000.00</span></span></td>
<td><span data-ttu-id="d6e87-265">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-266">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-266">0.00</span></span></td>
<td><span data-ttu-id="d6e87-267">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-268">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-269">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-270">5</span><span class="sxs-lookup"><span data-stu-id="d6e87-270">5</span></span></td>
<td><span data-ttu-id="d6e87-271">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="d6e87-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-272">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-272">-1,008.00</span></span></td>
<td><span data-ttu-id="d6e87-273">1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-273">1,008.00</span></span></td>
<td><span data-ttu-id="d6e87-274">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-275">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-276">6</span><span class="sxs-lookup"><span data-stu-id="d6e87-276">6</span></span></td>
<td><span data-ttu-id="d6e87-277">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="d6e87-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-278">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-279">22 794,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-280">22 793,90</span><span class="sxs-lookup"><span data-stu-id="d6e87-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-281">7</span><span class="sxs-lookup"><span data-stu-id="d6e87-281">7</span></span></td>
<td><span data-ttu-id="d6e87-282">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="d6e87-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-283">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-284">-22,794.00</span></span></td>
<td><span data-ttu-id="d6e87-285">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-285">1,000.00</span></span></td>
<td><span data-ttu-id="d6e87-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="d6e87-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="d6e87-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-288">8</span><span class="sxs-lookup"><span data-stu-id="d6e87-288">8</span></span></td>
<td><span data-ttu-id="d6e87-289">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-290">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-291">94.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-292">94.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-293">9</span><span class="sxs-lookup"><span data-stu-id="d6e87-293">9</span></span></td>
<td><span data-ttu-id="d6e87-294">Kontanter</span><span class="sxs-lookup"><span data-stu-id="d6e87-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-295">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-295">-1,008.00</span></span></td>
<td><span data-ttu-id="d6e87-296">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-297">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-298">10</span><span class="sxs-lookup"><span data-stu-id="d6e87-298">10</span></span></td>
<td><span data-ttu-id="d6e87-299">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="d6e87-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-300">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-301">949.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-301">949.75</span></span></td>
<td><span data-ttu-id="d6e87-302">949.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-303">11</span><span class="sxs-lookup"><span data-stu-id="d6e87-303">11</span></span></td>
<td><span data-ttu-id="d6e87-304">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="d6e87-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-305">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="d6e87-306">-949.75</span></span></td>
<td><span data-ttu-id="d6e87-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="d6e87-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d6e87-308">Som den foregående tabellen viser kreves det tre tablåer for å rapportere både under lovbestemt rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="d6e87-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="d6e87-309">Det lovbestemte tablået registrerer leiebetalingen i henhold til reglene for kontantprinsippregnskap under det gjeldende laget.</span><span class="sxs-lookup"><span data-stu-id="d6e87-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="d6e87-310">Det lovbestemte tilbakeføringstablået tilbakestiller lovbestemte journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="d6e87-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="d6e87-311">IFRS 16-tablået oppretter journaloppføringene som kreves under IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="d6e87-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="d6e87-312">Du trenger bare å angi en leieavtale én gang.</span><span class="sxs-lookup"><span data-stu-id="d6e87-312">You must enter a lease only one time.</span></span> <span data-ttu-id="d6e87-313">Du kan deretter åpne **Tablåer**-siden for å se alle tablåene som er knyttet til leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="d6e87-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="d6e87-314">Når du oppretter tablåene, må alle tre knyttes til samme leiepost.</span><span class="sxs-lookup"><span data-stu-id="d6e87-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="d6e87-315">Den første journaloppføringen registrerer leieutgiften under det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="d6e87-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="d6e87-316">Du kan opprette betalingene i en bunke eller ved å velge betalingsplanen i det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="d6e87-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="d6e87-317">I dette eksemplet produseres følgende journaloppføring for det lovbestemte tablået fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="d6e87-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="d6e87-318">Leiebetaling – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="d6e87-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="d6e87-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-319">Account type</span></span> | <span data-ttu-id="d6e87-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-320">Account number</span></span> | <span data-ttu-id="d6e87-321">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-321">Layer</span></span>   | <span data-ttu-id="d6e87-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-322">Account description</span></span> | <span data-ttu-id="d6e87-323">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-323">Debit</span></span>    | <span data-ttu-id="d6e87-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="d6e87-325">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-325">Ledger</span></span>       | <span data-ttu-id="d6e87-326">1</span><span class="sxs-lookup"><span data-stu-id="d6e87-326">1</span></span>              | <span data-ttu-id="d6e87-327">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-327">Current</span></span> | <span data-ttu-id="d6e87-328">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-328">Lease expense</span></span>       | <span data-ttu-id="d6e87-329">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-329">1,000.00</span></span> |          |
| <span data-ttu-id="d6e87-330">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-330">Ledger</span></span>       | <span data-ttu-id="d6e87-331">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-331">4</span></span>              | <span data-ttu-id="d6e87-332">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-332">Current</span></span> | <span data-ttu-id="d6e87-333">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-333">Clearing account</span></span>    |          | <span data-ttu-id="d6e87-334">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-334">1,000.00</span></span> |

<span data-ttu-id="d6e87-335">En regnskapsassistent bruker standard Dynamics 365-funksjonalitet til å opprette en faktura for å betale leien utenfor Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="d6e87-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="d6e87-336">I stedet for å velge **Leieutgift** som debetkonto velger regnskapsassistenten en avregningskonto for å generere følgende oppføring.</span><span class="sxs-lookup"><span data-stu-id="d6e87-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="d6e87-337">AP-prosess – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="d6e87-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="d6e87-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-338">Account type</span></span> | <span data-ttu-id="d6e87-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-339">Account number</span></span> | <span data-ttu-id="d6e87-340">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-340">Layer</span></span>   | <span data-ttu-id="d6e87-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-341">Account description</span></span> | <span data-ttu-id="d6e87-342">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-342">Debit</span></span>    | <span data-ttu-id="d6e87-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="d6e87-344">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-344">Ledger</span></span>       | <span data-ttu-id="d6e87-345">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-345">4</span></span>              | <span data-ttu-id="d6e87-346">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-346">Current</span></span> | <span data-ttu-id="d6e87-347">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-347">Clearing account</span></span>    | <span data-ttu-id="d6e87-348">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-348">1,000.00</span></span> |          |
| <span data-ttu-id="d6e87-349">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-349">Ledger</span></span>       | <span data-ttu-id="d6e87-350">2</span><span class="sxs-lookup"><span data-stu-id="d6e87-350">2</span></span>              | <span data-ttu-id="d6e87-351">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-351">Current</span></span> | <span data-ttu-id="d6e87-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="d6e87-352">Bank fee</span></span>            | <span data-ttu-id="d6e87-353">3,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-353">3.00</span></span>     |          |
| <span data-ttu-id="d6e87-354">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-354">Ledger</span></span>       | <span data-ttu-id="d6e87-355">3</span><span class="sxs-lookup"><span data-stu-id="d6e87-355">3</span></span>              | <span data-ttu-id="d6e87-356">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-356">Current</span></span> | <span data-ttu-id="d6e87-357">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-357">VAT expense</span></span>         | <span data-ttu-id="d6e87-358">5,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-358">5.00</span></span>     |          |
| <span data-ttu-id="d6e87-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="d6e87-359">Vendor</span></span>       | <span data-ttu-id="d6e87-360">5</span><span class="sxs-lookup"><span data-stu-id="d6e87-360">5</span></span>              | <span data-ttu-id="d6e87-361">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-361">Current</span></span> | <span data-ttu-id="d6e87-362">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="d6e87-362">Accounts payable</span></span>    |          | <span data-ttu-id="d6e87-363">1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-363">1,008.00</span></span> |

<span data-ttu-id="d6e87-364">Når utdraget er utstedt til leverandøren, følger du den vanlige betalingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="d6e87-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="d6e87-365">Følgende journaloppføring genereres i løpet av denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="d6e87-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="d6e87-366">Kontantbetaling – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="d6e87-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="d6e87-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-367">Account type</span></span> | <span data-ttu-id="d6e87-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-368">Account number</span></span> | <span data-ttu-id="d6e87-369">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-369">Layer</span></span>   | <span data-ttu-id="d6e87-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-370">Account description</span></span> | <span data-ttu-id="d6e87-371">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-371">Debit</span></span>    | <span data-ttu-id="d6e87-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="d6e87-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="d6e87-373">Vendor</span></span>       | <span data-ttu-id="d6e87-374">5</span><span class="sxs-lookup"><span data-stu-id="d6e87-374">5</span></span>              | <span data-ttu-id="d6e87-375">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-375">Current</span></span> | <span data-ttu-id="d6e87-376">Leverandører</span><span class="sxs-lookup"><span data-stu-id="d6e87-376">Accounts Payable</span></span>    | <span data-ttu-id="d6e87-377">1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-377">1,008.00</span></span> |          |
| <span data-ttu-id="d6e87-378">Bank</span><span class="sxs-lookup"><span data-stu-id="d6e87-378">Bank</span></span>         | <span data-ttu-id="d6e87-379">9</span><span class="sxs-lookup"><span data-stu-id="d6e87-379">9</span></span>              | <span data-ttu-id="d6e87-380">Gjeldende</span><span class="sxs-lookup"><span data-stu-id="d6e87-380">Current</span></span> | <span data-ttu-id="d6e87-381">Kontanter</span><span class="sxs-lookup"><span data-stu-id="d6e87-381">Cash</span></span>                |          | <span data-ttu-id="d6e87-382">1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-382">1,008.00</span></span> |

<span data-ttu-id="d6e87-383">Nå har du gjort fullstendig rede for denne leien under lovbestemte rapporteringskrav og kan generere en råbalanse ved hjelp av det gjeldende laget.</span><span class="sxs-lookup"><span data-stu-id="d6e87-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="d6e87-384">Systemet returnerer en råbalanse med følgende tall.</span><span class="sxs-lookup"><span data-stu-id="d6e87-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="d6e87-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="d6e87-386">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="d6e87-387">Lovbestemt tablå (gjeldende lag)</span><span class="sxs-lookup"><span data-stu-id="d6e87-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="d6e87-388">Gjeldende lag totalt</span><span class="sxs-lookup"><span data-stu-id="d6e87-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d6e87-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="d6e87-389">JE-100</span></span></th>
<th><span data-ttu-id="d6e87-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="d6e87-390">JE-110</span></span></th>
<th><span data-ttu-id="d6e87-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="d6e87-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d6e87-392">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-393">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d6e87-394">Debet (kredit)</span><span class="sxs-lookup"><span data-stu-id="d6e87-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d6e87-395">1</span><span class="sxs-lookup"><span data-stu-id="d6e87-395">1</span></span></td>
<td><span data-ttu-id="d6e87-396">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-396">Lease expense</span></span></td>
<td><span data-ttu-id="d6e87-397">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-398">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-399">2</span><span class="sxs-lookup"><span data-stu-id="d6e87-399">2</span></span></td>
<td><span data-ttu-id="d6e87-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="d6e87-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-401">3,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-402">3,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-403">3</span><span class="sxs-lookup"><span data-stu-id="d6e87-403">3</span></span></td>
<td><span data-ttu-id="d6e87-404">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-405">5,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-406">5,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-407">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-407">4</span></span></td>
<td><span data-ttu-id="d6e87-408">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-408">Clearing account</span></span></td>
<td><span data-ttu-id="d6e87-409">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-409">-1,000.00</span></span></td>
<td><span data-ttu-id="d6e87-410">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-411">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-412">5</span><span class="sxs-lookup"><span data-stu-id="d6e87-412">5</span></span></td>
<td><span data-ttu-id="d6e87-413">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="d6e87-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="d6e87-414">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-414">-1,008.00</span></span></td>
<td><span data-ttu-id="d6e87-415">1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-415">1,008.00</span></span></td>
<td><span data-ttu-id="d6e87-416">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-417">6</span><span class="sxs-lookup"><span data-stu-id="d6e87-417">6</span></span></td>
<td><span data-ttu-id="d6e87-418">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="d6e87-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-419">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-420">7</span><span class="sxs-lookup"><span data-stu-id="d6e87-420">7</span></span></td>
<td><span data-ttu-id="d6e87-421">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="d6e87-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-422">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-423">8</span><span class="sxs-lookup"><span data-stu-id="d6e87-423">8</span></span></td>
<td><span data-ttu-id="d6e87-424">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-425">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-426">9</span><span class="sxs-lookup"><span data-stu-id="d6e87-426">9</span></span></td>
<td><span data-ttu-id="d6e87-427">Kontanter</span><span class="sxs-lookup"><span data-stu-id="d6e87-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-428">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-428">-1,008.00</span></span></td>
<td><span data-ttu-id="d6e87-429">-1 008,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-430">10</span><span class="sxs-lookup"><span data-stu-id="d6e87-430">10</span></span></td>
<td><span data-ttu-id="d6e87-431">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="d6e87-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-432">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d6e87-433">11</span><span class="sxs-lookup"><span data-stu-id="d6e87-433">11</span></span></td>
<td><span data-ttu-id="d6e87-434">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="d6e87-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d6e87-435">0,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d6e87-436">Hvis du vil bruke IFRS 16-tallene til å kjøre den samme råbalansen, må lovbestemte regnskapsjournaloppføringer tilbakeføres, og IFRS 16-journaloppføringer må posteres.</span><span class="sxs-lookup"><span data-stu-id="d6e87-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="d6e87-437">For å tilbakeføre lovbestemte journaloppføringer omfatter dette eksemplet et lovbestemt tilbakeføringstablå som har samme konfigurasjon som det lovbestemte tablået, men en motsatt posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="d6e87-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="d6e87-438">Det lovbestemte tablået *debiterte* for eksempel en leieutgiftskonto, men tilbakeføringstablået *krediterer* denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="d6e87-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="d6e87-439">Disse relasjonene kan enkelt defineres i posteringskontoene for Aktivaleie på siden **Parametere for aktivaleie** (**Aktivaleie \> Oppsett \> Parametere for aktivaleie**).</span><span class="sxs-lookup"><span data-stu-id="d6e87-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="d6e87-440">Når den samme prosessen som ble brukt for det lovbestemte tablået, brukes for tilbakeføringstablået, produseres følgende journaloppføring.</span><span class="sxs-lookup"><span data-stu-id="d6e87-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="d6e87-441">Forskjellen er at tilbakeføringstablået posterer tilbakeføringsoppføringene fra det lovbestemte tablået.</span><span class="sxs-lookup"><span data-stu-id="d6e87-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="d6e87-442">Tilbakeføringsoppføringene gjøres også på det egendefinerte laget.</span><span class="sxs-lookup"><span data-stu-id="d6e87-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="d6e87-443">Når en råbalanse kjøres på det gjeldende laget, blir ikke tilbakeføringsjournaloppføringene tatt med.</span><span class="sxs-lookup"><span data-stu-id="d6e87-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="d6e87-444">Leiebetaling – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="d6e87-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="d6e87-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-445">Account type</span></span> | <span data-ttu-id="d6e87-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-446">Account number</span></span> | <span data-ttu-id="d6e87-447">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-447">Layer</span></span>  | <span data-ttu-id="d6e87-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-448">Account description</span></span> | <span data-ttu-id="d6e87-449">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-449">Debit</span></span>    | <span data-ttu-id="d6e87-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="d6e87-451">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-451">Ledger</span></span>       | <span data-ttu-id="d6e87-452">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-452">4</span></span>              | <span data-ttu-id="d6e87-453">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-453">Custom</span></span> | <span data-ttu-id="d6e87-454">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-454">Clearing account</span></span>    | <span data-ttu-id="d6e87-455">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-455">1,000.00</span></span> |          |
| <span data-ttu-id="d6e87-456">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-456">Ledger</span></span>       | <span data-ttu-id="d6e87-457">1</span><span class="sxs-lookup"><span data-stu-id="d6e87-457">1</span></span>              | <span data-ttu-id="d6e87-458">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-458">Custom</span></span> | <span data-ttu-id="d6e87-459">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-459">Lease expense</span></span>       |          | <span data-ttu-id="d6e87-460">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-460">1,000.00</span></span> |

<span data-ttu-id="d6e87-461">Nå som du har fjernet de lovbestemte journaloppføringene, skal du postere alle journaloppføringer som kreves av IFRS 16, i IFRS 16-tablået.</span><span class="sxs-lookup"><span data-stu-id="d6e87-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="d6e87-462">Disse oppføringene omfatter den opprinnelige føringen av bruksrettseiendelen og gjelden, og posten for rente og avskrivning.</span><span class="sxs-lookup"><span data-stu-id="d6e87-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="d6e87-463">Opprinnelig føring – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="d6e87-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="d6e87-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-464">Account type</span></span> | <span data-ttu-id="d6e87-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-465">Account number</span></span> | <span data-ttu-id="d6e87-466">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-466">Layer</span></span>  | <span data-ttu-id="d6e87-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-467">Account description</span></span>      | <span data-ttu-id="d6e87-468">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-468">Debit</span></span>     | <span data-ttu-id="d6e87-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="d6e87-470">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-470">Ledger</span></span>       | <span data-ttu-id="d6e87-471">6</span><span class="sxs-lookup"><span data-stu-id="d6e87-471">6</span></span>              | <span data-ttu-id="d6e87-472">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-472">Custom</span></span> | <span data-ttu-id="d6e87-473">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="d6e87-473">ROU Asset</span></span>                | <span data-ttu-id="d6e87-474">22 793,90</span><span class="sxs-lookup"><span data-stu-id="d6e87-474">22,793.90</span></span> |           |
| <span data-ttu-id="d6e87-475">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-475">Ledger</span></span>       | <span data-ttu-id="d6e87-476">7</span><span class="sxs-lookup"><span data-stu-id="d6e87-476">7</span></span>              | <span data-ttu-id="d6e87-477">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-477">Custom</span></span> | <span data-ttu-id="d6e87-478">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="d6e87-478">Finance lease obligation</span></span> |           | <span data-ttu-id="d6e87-479">22 793,90</span><span class="sxs-lookup"><span data-stu-id="d6e87-479">22,793.90</span></span> |

<span data-ttu-id="d6e87-480">Leiebetalingen posteres som de andre leiebetalingene.</span><span class="sxs-lookup"><span data-stu-id="d6e87-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="d6e87-481">Grunnen til å bruke avregningskontoen er å sikre at kontanter bare krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="d6e87-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="d6e87-482">Leiebetaling – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="d6e87-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="d6e87-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-483">Account type</span></span> | <span data-ttu-id="d6e87-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-484">Account number</span></span> | <span data-ttu-id="d6e87-485">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-485">Layer</span></span>  | <span data-ttu-id="d6e87-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-486">Account description</span></span>      | <span data-ttu-id="d6e87-487">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-487">Debit</span></span>    | <span data-ttu-id="d6e87-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="d6e87-489">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-489">Ledger</span></span>       | <span data-ttu-id="d6e87-490">7</span><span class="sxs-lookup"><span data-stu-id="d6e87-490">7</span></span>              | <span data-ttu-id="d6e87-491">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-491">Custom</span></span> | <span data-ttu-id="d6e87-492">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="d6e87-492">Finance lease obligation</span></span> | <span data-ttu-id="d6e87-493">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-493">1,000.00</span></span> |          |
| <span data-ttu-id="d6e87-494">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-494">Ledger</span></span>       | <span data-ttu-id="d6e87-495">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-495">4</span></span>              | <span data-ttu-id="d6e87-496">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-496">Custom</span></span> | <span data-ttu-id="d6e87-497">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-497">Clearing account</span></span>         |          | <span data-ttu-id="d6e87-498">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d6e87-498">1,000.00</span></span> |

<span data-ttu-id="d6e87-499">Journaloppføringen for renteutgift genereres fra nedbetalingsplanen for gjeld.</span><span class="sxs-lookup"><span data-stu-id="d6e87-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="d6e87-500">Renteutgift – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="d6e87-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="d6e87-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-501">Account type</span></span> | <span data-ttu-id="d6e87-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-502">Account number</span></span> | <span data-ttu-id="d6e87-503">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-503">Layer</span></span>  | <span data-ttu-id="d6e87-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-504">Account description</span></span>      | <span data-ttu-id="d6e87-505">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-505">Debit</span></span> | <span data-ttu-id="d6e87-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="d6e87-507">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-507">Ledger</span></span>       | <span data-ttu-id="d6e87-508">8</span><span class="sxs-lookup"><span data-stu-id="d6e87-508">8</span></span>              | <span data-ttu-id="d6e87-509">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-509">Custom</span></span> | <span data-ttu-id="d6e87-510">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-510">Interest expense</span></span>         | <span data-ttu-id="d6e87-511">94.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-511">94.97</span></span> |        |
| <span data-ttu-id="d6e87-512">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-512">Ledger</span></span>       | <span data-ttu-id="d6e87-513">7</span><span class="sxs-lookup"><span data-stu-id="d6e87-513">7</span></span>              | <span data-ttu-id="d6e87-514">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-514">Custom</span></span> | <span data-ttu-id="d6e87-515">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="d6e87-515">Finance lease obligation</span></span> |       | <span data-ttu-id="d6e87-516">94.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-516">94.97</span></span>  |

<span data-ttu-id="d6e87-517">Journaloppføringen for avskrivningskostnad genereres fra avskrivningsplanen for aktiva.</span><span class="sxs-lookup"><span data-stu-id="d6e87-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="d6e87-518">Avskrivningskostnad – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="d6e87-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="d6e87-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="d6e87-519">Account type</span></span> | <span data-ttu-id="d6e87-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="d6e87-520">Account number</span></span> | <span data-ttu-id="d6e87-521">Lag</span><span class="sxs-lookup"><span data-stu-id="d6e87-521">Layer</span></span>  | <span data-ttu-id="d6e87-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-522">Account description</span></span>      | <span data-ttu-id="d6e87-523">Debet</span><span class="sxs-lookup"><span data-stu-id="d6e87-523">Debit</span></span>  | <span data-ttu-id="d6e87-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="d6e87-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="d6e87-525">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-525">Ledger</span></span>       | <span data-ttu-id="d6e87-526">10</span><span class="sxs-lookup"><span data-stu-id="d6e87-526">10</span></span>             | <span data-ttu-id="d6e87-527">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-527">Custom</span></span> | <span data-ttu-id="d6e87-528">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="d6e87-528">Depreciation expense</span></span>     | <span data-ttu-id="d6e87-529">949.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-529">949.75</span></span> |        |
| <span data-ttu-id="d6e87-530">Finans</span><span class="sxs-lookup"><span data-stu-id="d6e87-530">Ledger</span></span>       | <span data-ttu-id="d6e87-531">11</span><span class="sxs-lookup"><span data-stu-id="d6e87-531">11</span></span>             | <span data-ttu-id="d6e87-532">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="d6e87-532">Custom</span></span> | <span data-ttu-id="d6e87-533">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="d6e87-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="d6e87-534">949.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-534">949.75</span></span> |

<span data-ttu-id="d6e87-535">Når alle disse journaloppføringene er opprettet og postert, vises følgende verdier for egendefinert lag 1.</span><span class="sxs-lookup"><span data-stu-id="d6e87-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="d6e87-536">Vær oppmerksom på at den siste kolonnen omfatter bankgebyret, merverdiavgift (mva) og reduksjonen i kontanter fra forrige lag, men den omfatter ikke journaloppføringene for lovbestemt rapportering.</span><span class="sxs-lookup"><span data-stu-id="d6e87-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="d6e87-537">Derfor oppnår du ekte funksjonalitet for dobbel rapportering.</span><span class="sxs-lookup"><span data-stu-id="d6e87-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="d6e87-538">Nå trenger firmaet bare å kjøre råbalansen og kombinere det gjeldende laget og det egendefinerte laget for å opprette en IFRS-råbalanse.</span><span class="sxs-lookup"><span data-stu-id="d6e87-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="d6e87-539">Kontonr.</span><span class="sxs-lookup"><span data-stu-id="d6e87-539">Account No</span></span> | <span data-ttu-id="d6e87-540">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d6e87-540">Description</span></span>              | <span data-ttu-id="d6e87-541">Lovbestemt tablå\-gjeldende lag\-JE\-100\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-542">Lovbestemt tablå\-gjeldende lag\-JE\-110\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-543">Lovbestemt tablå\-gjeldende lag\-JE\-120\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-544">Gjeldende lag \- totaler</span><span class="sxs-lookup"><span data-stu-id="d6e87-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="d6e87-545">Tilbakeføringstablå\-egendefinert lag\-JE\-130\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-546">IFRS 16-tablå\-egendefinert lag\-JE\-140\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-547">IFRS 16-tablå\-egendefinert lag\-JE\-150\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-548">IFRS 16-tablå\-egendefinert lag\-JE\-160\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-549">IFRS 16-tablå\-egendefinert lag\-JE\-170\-debet \(kredit\)</span><span class="sxs-lookup"><span data-stu-id="d6e87-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="d6e87-550">Egendefinert lag \+ gjeldende lag \- totaler</span><span class="sxs-lookup"><span data-stu-id="d6e87-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="d6e87-551">1</span><span class="sxs-lookup"><span data-stu-id="d6e87-551">1</span></span>          | <span data-ttu-id="d6e87-552">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-552">Lease expense</span></span>            | <span data-ttu-id="d6e87-553">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="d6e87-554">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-554">1,000\.00</span></span>               |   | <span data-ttu-id="d6e87-555">\-1 000</span><span class="sxs-lookup"><span data-stu-id="d6e87-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="d6e87-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-556">0\.00</span></span>                                   |
| <span data-ttu-id="d6e87-557">2</span><span class="sxs-lookup"><span data-stu-id="d6e87-557">2</span></span>          | <span data-ttu-id="d6e87-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="d6e87-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="d6e87-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="d6e87-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d6e87-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-561">3\.00</span></span>                                   |
| <span data-ttu-id="d6e87-562">3</span><span class="sxs-lookup"><span data-stu-id="d6e87-562">3</span></span>          | <span data-ttu-id="d6e87-563">Mva-utgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="d6e87-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="d6e87-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d6e87-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-566">5\.00</span></span>                                   |
| <span data-ttu-id="d6e87-567">4</span><span class="sxs-lookup"><span data-stu-id="d6e87-567">4</span></span>          | <span data-ttu-id="d6e87-568">Avregningskonto</span><span class="sxs-lookup"><span data-stu-id="d6e87-568">Clearing account</span></span>         | <span data-ttu-id="d6e87-569">\-1 000\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="d6e87-570">1 000\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="d6e87-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-571">0\.00</span></span>                   |   | <span data-ttu-id="d6e87-572">1 000</span><span class="sxs-lookup"><span data-stu-id="d6e87-572">1,000</span></span>                                           |                                                | <span data-ttu-id="d6e87-573">\-1 000</span><span class="sxs-lookup"><span data-stu-id="d6e87-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="d6e87-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-574">0\.00</span></span>                                   |
| <span data-ttu-id="d6e87-575">5</span><span class="sxs-lookup"><span data-stu-id="d6e87-575">5</span></span>          | <span data-ttu-id="d6e87-576">Leverandørreskontro</span><span class="sxs-lookup"><span data-stu-id="d6e87-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="d6e87-577">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="d6e87-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-578">1,008\.00</span></span>                                         | <span data-ttu-id="d6e87-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d6e87-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-580">0\.00</span></span>                                   |
| <span data-ttu-id="d6e87-581">6</span><span class="sxs-lookup"><span data-stu-id="d6e87-581">6</span></span>          | <span data-ttu-id="d6e87-582">Bruksrettseiendel</span><span class="sxs-lookup"><span data-stu-id="d6e87-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="d6e87-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="d6e87-584">22,794</span><span class="sxs-lookup"><span data-stu-id="d6e87-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="d6e87-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="d6e87-585">22,793\.90</span></span>                              |
| <span data-ttu-id="d6e87-586">7</span><span class="sxs-lookup"><span data-stu-id="d6e87-586">7</span></span>          | <span data-ttu-id="d6e87-587">Forpliktelse for finansiell leie</span><span class="sxs-lookup"><span data-stu-id="d6e87-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="d6e87-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="d6e87-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="d6e87-589">\-22,794</span></span>                                       | <span data-ttu-id="d6e87-590">1 000</span><span class="sxs-lookup"><span data-stu-id="d6e87-590">1,000</span></span>                                          | <span data-ttu-id="d6e87-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="d6e87-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="d6e87-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="d6e87-593">8</span><span class="sxs-lookup"><span data-stu-id="d6e87-593">8</span></span>          | <span data-ttu-id="d6e87-594">Renteutgift</span><span class="sxs-lookup"><span data-stu-id="d6e87-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="d6e87-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="d6e87-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="d6e87-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="d6e87-597">94\.97</span></span>                                  |
| <span data-ttu-id="d6e87-598">9</span><span class="sxs-lookup"><span data-stu-id="d6e87-598">9</span></span>          | <span data-ttu-id="d6e87-599">Kontanter</span><span class="sxs-lookup"><span data-stu-id="d6e87-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="d6e87-600">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="d6e87-601">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d6e87-602">\-1 008\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="d6e87-603">10</span><span class="sxs-lookup"><span data-stu-id="d6e87-603">10</span></span>         | <span data-ttu-id="d6e87-604">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="d6e87-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="d6e87-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="d6e87-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-606">949\.75</span></span>                                        | <span data-ttu-id="d6e87-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-607">949\.75</span></span>                                 |
| <span data-ttu-id="d6e87-608">11</span><span class="sxs-lookup"><span data-stu-id="d6e87-608">11</span></span>         | <span data-ttu-id="d6e87-609">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="d6e87-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="d6e87-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="d6e87-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="d6e87-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-611">\-949\.75</span></span>                                      | <span data-ttu-id="d6e87-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="d6e87-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
