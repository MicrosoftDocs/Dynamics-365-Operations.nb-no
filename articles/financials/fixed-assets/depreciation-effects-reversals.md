---
title: Avskrivningseffekter av tilbakeføringer
description: Denne artikkelen beskriver potensielle konsekvenser av å tilbakeføre en anleggsmiddeltransaksjon.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d624fa998329680d9fa471fa325f6fcfd3920c6a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "320150"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="0a79f-103">Avskrivningseffekter av tilbakeføringer</span><span class="sxs-lookup"><span data-stu-id="0a79f-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a79f-104">Denne artikkelen beskriver potensielle konsekvenser av å tilbakeføre en anleggsmiddeltransaksjon.</span><span class="sxs-lookup"><span data-stu-id="0a79f-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="0a79f-105">Du kan tilbakeføre anleggsmiddeltransaksjoner, og transaksjoner som er tilknyttet et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="0a79f-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="0a79f-106">Du kan også oppheve en tilbakeført transaksjon.</span><span class="sxs-lookup"><span data-stu-id="0a79f-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="0a79f-107">Du kan tilbakeføre eller oppheve en transaksjon som ikke har den nyeste transaksjonen postert til tablået for anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="0a79f-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="0a79f-108">Først må du bestemme om det er postert avskrivningstransaksjoner etter transaksjonen du tilbakefører.</span><span class="sxs-lookup"><span data-stu-id="0a79f-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="0a79f-109">Dette er fordi avskrivning ikke omberegnes når du tilbakefører en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="0a79f-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="0a79f-110">Derfor er avskrivning ofte overvurdert eller undervurdert etter tilbakeføringen, som vist i eksemplene.</span><span class="sxs-lookup"><span data-stu-id="0a79f-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="0a79f-111">For å sikre at avskrivningen er riktig når du tilbakefører en transaksjon, må du ikke gå videre med tilbakeføringen hvis du får en melding som sier at avskrivningen ikke blir omberegnet.</span><span class="sxs-lookup"><span data-stu-id="0a79f-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="0a79f-112">Da må du i stedet tilbakeføre den avskrivningstransaksjonen som ble postert etter den transaksjonen du forsøkte å tilbakeføre, og deretter gå videre med tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="0a79f-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="0a79f-113">Du vil ikke få noen advarsel om avskrivningsomberegning, og du kan gå videre med tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="0a79f-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="0a79f-114">Eksemplene nedenfor viser beregningene som skjer hvis du fortsetter etter meldingen uten å tilbakeføre avskrivningstransaksjonene først.</span><span class="sxs-lookup"><span data-stu-id="0a79f-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="0a79f-115"> Eksempel 1: Avskrivning overvurdert</span><span class="sxs-lookup"><span data-stu-id="0a79f-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="0a79f-116">Et anleggsmiddelet er definert med 5 års levetid og lineær avskrivning (60 avskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="0a79f-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="0a79f-117">I dette eksemplet er avskrivningen overvurdert.</span><span class="sxs-lookup"><span data-stu-id="0a79f-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="0a79f-118">Transaksjonshistorikk for anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="0a79f-118">Asset transaction history</span></span>

| <span data-ttu-id="0a79f-119">Dato</span><span class="sxs-lookup"><span data-stu-id="0a79f-119">Date</span></span>       | <span data-ttu-id="0a79f-120">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="0a79f-120">Transaction type</span></span>                                                          | <span data-ttu-id="0a79f-121">Beløp</span><span class="sxs-lookup"><span data-stu-id="0a79f-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0a79f-122">1. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-122">January 1</span></span>  | <span data-ttu-id="0a79f-123">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="0a79f-123">Acquisition</span></span>                                                               | <span data-ttu-id="0a79f-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="0a79f-124">59,000.00</span></span>                                 |
| <span data-ttu-id="0a79f-125">1. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-125">January 1</span></span>  | <span data-ttu-id="0a79f-126">Anskaffelsesjustering</span><span class="sxs-lookup"><span data-stu-id="0a79f-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="0a79f-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="0a79f-127">1,000.00</span></span>                                  |
| <span data-ttu-id="0a79f-128">31. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-128">January 31</span></span> | <span data-ttu-id="0a79f-129">Avskrivning (opprettet ved bruk av forslag for én avskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="0a79f-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="0a79f-130">1 000,00Beregning: Bokført verdi (59 000 + 1 000) / Antall gjenværende avskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="0a79f-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="0a79f-131">Tilbakeføringshandling</span><span class="sxs-lookup"><span data-stu-id="0a79f-131">Reversal action</span></span>

| <span data-ttu-id="0a79f-132">Dato</span><span class="sxs-lookup"><span data-stu-id="0a79f-132">Date</span></span>      | <span data-ttu-id="0a79f-133">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="0a79f-133">Transaction type</span></span>                | <span data-ttu-id="0a79f-134">Beløp</span><span class="sxs-lookup"><span data-stu-id="0a79f-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="0a79f-135">1. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-135">January 1</span></span> | <span data-ttu-id="0a79f-136">Tilbakeføring av anskaffelsesjustering</span><span class="sxs-lookup"><span data-stu-id="0a79f-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="0a79f-137">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="0a79f-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="0a79f-138">Avskrivningseffekt</span><span class="sxs-lookup"><span data-stu-id="0a79f-138">Depreciation effect</span></span>

| <span data-ttu-id="0a79f-139">Dato</span><span class="sxs-lookup"><span data-stu-id="0a79f-139">Date</span></span>        | <span data-ttu-id="0a79f-140">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="0a79f-140">Transaction type</span></span>        | <span data-ttu-id="0a79f-141">Beløp</span><span class="sxs-lookup"><span data-stu-id="0a79f-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a79f-142">28. februar</span><span class="sxs-lookup"><span data-stu-id="0a79f-142">February 28</span></span> | <span data-ttu-id="0a79f-143">Avskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="0a79f-143">Depreciation (proposal)</span></span> | <span data-ttu-id="0a79f-144">983,05Beregning: Bokført verdi (59 000 - 1 000 avskrivning) / Antall gjenværende avskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="0a79f-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="0a79f-145">Avskrivningen er overvurdert med 16,95 (1 000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="0a79f-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="0a79f-146"> Eksempel 2: Avskrivning undervurdert</span><span class="sxs-lookup"><span data-stu-id="0a79f-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="0a79f-147">Et anleggsmiddelet er definert med 5 års levetid og lineær avskrivning (60 avskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="0a79f-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="0a79f-148">I dette eksemplet er avskrivningen undervurdert.</span><span class="sxs-lookup"><span data-stu-id="0a79f-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="0a79f-149">Transaksjonshistorikk for anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="0a79f-149">Asset transaction history</span></span>

| <span data-ttu-id="0a79f-150">Dato</span><span class="sxs-lookup"><span data-stu-id="0a79f-150">Date</span></span>       | <span data-ttu-id="0a79f-151">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="0a79f-151">Transaction type</span></span>                                                          | <span data-ttu-id="0a79f-152">Beløp</span><span class="sxs-lookup"><span data-stu-id="0a79f-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="0a79f-153">1. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-153">January 1</span></span>  | <span data-ttu-id="0a79f-154">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="0a79f-154">Acquisition</span></span>                                                               | <span data-ttu-id="0a79f-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="0a79f-155">59,000.00</span></span>                                   |
| <span data-ttu-id="0a79f-156">1. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-156">January 1</span></span>  | <span data-ttu-id="0a79f-157">Skriv ned justering</span><span class="sxs-lookup"><span data-stu-id="0a79f-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="0a79f-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="0a79f-158">1,000.00</span></span>                                    |
| <span data-ttu-id="0a79f-159">31. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-159">January 31</span></span> | <span data-ttu-id="0a79f-160">Avskrivning (opprettet ved bruk av forslag for én avskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="0a79f-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="0a79f-161">966,67Beregning: Bokført verdi (59 000 - 1 000) / Antall gjenværende avskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="0a79f-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="0a79f-162">Tilbakeføringshandling</span><span class="sxs-lookup"><span data-stu-id="0a79f-162">Reversal action</span></span>

| <span data-ttu-id="0a79f-163">Dato</span><span class="sxs-lookup"><span data-stu-id="0a79f-163">Date</span></span>      | <span data-ttu-id="0a79f-164">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="0a79f-164">Transaction type</span></span>               | <span data-ttu-id="0a79f-165">Beløp</span><span class="sxs-lookup"><span data-stu-id="0a79f-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="0a79f-166">1. januar</span><span class="sxs-lookup"><span data-stu-id="0a79f-166">January 1</span></span> | <span data-ttu-id="0a79f-167">Tilbakeføring av nedskrivingsjustering</span><span class="sxs-lookup"><span data-stu-id="0a79f-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="0a79f-168">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="0a79f-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="0a79f-169">Avskrivningseffekt</span><span class="sxs-lookup"><span data-stu-id="0a79f-169">Depreciation effect</span></span>

| <span data-ttu-id="0a79f-170">Dato</span><span class="sxs-lookup"><span data-stu-id="0a79f-170">Date</span></span>        | <span data-ttu-id="0a79f-171">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="0a79f-171">Transaction type</span></span>        | <span data-ttu-id="0a79f-172">Beløp</span><span class="sxs-lookup"><span data-stu-id="0a79f-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a79f-173">28. februar</span><span class="sxs-lookup"><span data-stu-id="0a79f-173">February 28</span></span> | <span data-ttu-id="0a79f-174">Avskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="0a79f-174">Depreciation (proposal)</span></span> | <span data-ttu-id="0a79f-175">983,62Beregning: Bokført verdi (59 000 - 966,67 avskrivning) / Antall gjenværende avskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="0a79f-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="0a79f-176">Avskrivningen er undervurdert med 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="0a79f-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="0a79f-177">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0a79f-177">Additional resources</span></span>
--------

[<span data-ttu-id="0a79f-178">Avskrivning av anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="0a79f-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



