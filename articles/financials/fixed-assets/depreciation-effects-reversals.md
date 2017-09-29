---
title: "Avskrivningseffekter av tilbakeføringer"
description: "Denne artikkelen beskriver potensielle konsekvenser av å tilbakeføre en anleggsmiddeltransaksjon."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7309cb3175f65bc6b806edb875ac9406a8faaf66
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="ac8cc-103">Avskrivningseffekter av tilbakeføringer</span><span class="sxs-lookup"><span data-stu-id="ac8cc-103">Depreciation effects with reversals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ac8cc-104">Denne artikkelen beskriver potensielle konsekvenser av å tilbakeføre en anleggsmiddeltransaksjon.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="ac8cc-105">Du kan tilbakeføre anleggsmiddeltransaksjoner, og transaksjoner som er tilknyttet et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="ac8cc-106">Du kan også oppheve en tilbakeført transaksjon.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="ac8cc-107">Du kan tilbakeføre eller oppheve en transaksjon som ikke har den nyeste transaksjonen postert til tablået for anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="ac8cc-108">Først må du bestemme om det er postert avskrivningstransaksjoner etter transaksjonen du tilbakefører.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="ac8cc-109">Dette er fordi avskrivning ikke omberegnes når du tilbakefører en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="ac8cc-110">Derfor er avskrivning ofte overvurdert eller undervurdert etter tilbakeføringen, som vist i eksemplene.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="ac8cc-111">For å sikre at avskrivningen er riktig når du tilbakefører en transaksjon, må du ikke gå videre med tilbakeføringen hvis du får en melding som sier at avskrivningen ikke blir omberegnet.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="ac8cc-112">Da må du i stedet tilbakeføre den avskrivningstransaksjonen som ble postert etter den transaksjonen du forsøkte å tilbakeføre, og deretter gå videre med tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="ac8cc-113">Du vil ikke få noen advarsel om avskrivningsomberegning, og du kan gå videre med tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="ac8cc-114">Eksemplene nedenfor viser beregningene som skjer hvis du fortsetter etter meldingen uten å tilbakeføre avskrivningstransaksjonene først.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="ac8cc-115"> Eksempel 1: Avskrivning overvurdert</span><span class="sxs-lookup"><span data-stu-id="ac8cc-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="ac8cc-116">Et anleggsmiddelet er definert med 5 års levetid og lineær avskrivning (60 avskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="ac8cc-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="ac8cc-117">I dette eksemplet er avskrivningen overvurdert.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="ac8cc-118">Transaksjonshistorikk for anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="ac8cc-118">Asset transaction history</span></span>

| <span data-ttu-id="ac8cc-119">Dato</span><span class="sxs-lookup"><span data-stu-id="ac8cc-119">Date</span></span>       | <span data-ttu-id="ac8cc-120">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ac8cc-120">Transaction type</span></span>                                                          | <span data-ttu-id="ac8cc-121">Beløp</span><span class="sxs-lookup"><span data-stu-id="ac8cc-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ac8cc-122">1. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-122">January 1</span></span>  | <span data-ttu-id="ac8cc-123">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="ac8cc-123">Acquisition</span></span>                                                               | <span data-ttu-id="ac8cc-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="ac8cc-124">59,000.00</span></span>                                 |
| <span data-ttu-id="ac8cc-125">1. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-125">January 1</span></span>  | <span data-ttu-id="ac8cc-126">Anskaffelsesjustering</span><span class="sxs-lookup"><span data-stu-id="ac8cc-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="ac8cc-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="ac8cc-127">1,000.00</span></span>                                  |
| <span data-ttu-id="ac8cc-128">31. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-128">January 31</span></span> | <span data-ttu-id="ac8cc-129">Avskrivning (opprettet ved bruk av forslag for én avskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="ac8cc-130">1 000,00Beregning: Bokført verdi (59 000 + 1 000) / Antall gjenværende avskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="ac8cc-131">Tilbakeføringshandling</span><span class="sxs-lookup"><span data-stu-id="ac8cc-131">Reversal action</span></span>

| <span data-ttu-id="ac8cc-132">Dato</span><span class="sxs-lookup"><span data-stu-id="ac8cc-132">Date</span></span>      | <span data-ttu-id="ac8cc-133">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ac8cc-133">Transaction type</span></span>                | <span data-ttu-id="ac8cc-134">Beløp</span><span class="sxs-lookup"><span data-stu-id="ac8cc-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="ac8cc-135">1. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-135">January 1</span></span> | <span data-ttu-id="ac8cc-136">Tilbakeføring av anskaffelsesjustering</span><span class="sxs-lookup"><span data-stu-id="ac8cc-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="ac8cc-137">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="ac8cc-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="ac8cc-138">Avskrivningseffekt</span><span class="sxs-lookup"><span data-stu-id="ac8cc-138">Depreciation effect</span></span>

| <span data-ttu-id="ac8cc-139">Dato</span><span class="sxs-lookup"><span data-stu-id="ac8cc-139">Date</span></span>        | <span data-ttu-id="ac8cc-140">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ac8cc-140">Transaction type</span></span>        | <span data-ttu-id="ac8cc-141">Beløp</span><span class="sxs-lookup"><span data-stu-id="ac8cc-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8cc-142">28. februar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-142">February 28</span></span> | <span data-ttu-id="ac8cc-143">Avskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-143">Depreciation (proposal)</span></span> | <span data-ttu-id="ac8cc-144">983,05Beregning: Bokført verdi (59 000 - 1 000 avskrivning) / Antall gjenværende avskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="ac8cc-145">Avskrivningen er overvurdert med 16,95 (1 000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="ac8cc-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="ac8cc-146"> Eksempel 2: Avskrivning undervurdert</span><span class="sxs-lookup"><span data-stu-id="ac8cc-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="ac8cc-147">Et anleggsmiddelet er definert med 5 års levetid og lineær avskrivning (60 avskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="ac8cc-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="ac8cc-148">I dette eksemplet er avskrivningen undervurdert.</span><span class="sxs-lookup"><span data-stu-id="ac8cc-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="ac8cc-149">Transaksjonshistorikk for anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="ac8cc-149">Asset transaction history</span></span>

| <span data-ttu-id="ac8cc-150">Dato</span><span class="sxs-lookup"><span data-stu-id="ac8cc-150">Date</span></span>       | <span data-ttu-id="ac8cc-151">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ac8cc-151">Transaction type</span></span>                                                          | <span data-ttu-id="ac8cc-152">Beløp</span><span class="sxs-lookup"><span data-stu-id="ac8cc-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="ac8cc-153">1. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-153">January 1</span></span>  | <span data-ttu-id="ac8cc-154">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="ac8cc-154">Acquisition</span></span>                                                               | <span data-ttu-id="ac8cc-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="ac8cc-155">59,000.00</span></span>                                   |
| <span data-ttu-id="ac8cc-156">1. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-156">January 1</span></span>  | <span data-ttu-id="ac8cc-157">Skriv ned justering</span><span class="sxs-lookup"><span data-stu-id="ac8cc-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="ac8cc-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="ac8cc-158">1,000.00</span></span>                                    |
| <span data-ttu-id="ac8cc-159">31. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-159">January 31</span></span> | <span data-ttu-id="ac8cc-160">Avskrivning (opprettet ved bruk av forslag for én avskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="ac8cc-161">966,67Beregning: Bokført verdi (59 000 - 1 000) / Antall gjenværende avskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="ac8cc-162">Tilbakeføringshandling</span><span class="sxs-lookup"><span data-stu-id="ac8cc-162">Reversal action</span></span>

| <span data-ttu-id="ac8cc-163">Dato</span><span class="sxs-lookup"><span data-stu-id="ac8cc-163">Date</span></span>      | <span data-ttu-id="ac8cc-164">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ac8cc-164">Transaction type</span></span>               | <span data-ttu-id="ac8cc-165">Beløp</span><span class="sxs-lookup"><span data-stu-id="ac8cc-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="ac8cc-166">1. januar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-166">January 1</span></span> | <span data-ttu-id="ac8cc-167">Tilbakeføring av nedskrivingsjustering</span><span class="sxs-lookup"><span data-stu-id="ac8cc-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="ac8cc-168">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="ac8cc-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="ac8cc-169">Avskrivningseffekt</span><span class="sxs-lookup"><span data-stu-id="ac8cc-169">Depreciation effect</span></span>

| <span data-ttu-id="ac8cc-170">Dato</span><span class="sxs-lookup"><span data-stu-id="ac8cc-170">Date</span></span>        | <span data-ttu-id="ac8cc-171">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ac8cc-171">Transaction type</span></span>        | <span data-ttu-id="ac8cc-172">Beløp</span><span class="sxs-lookup"><span data-stu-id="ac8cc-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8cc-173">28. februar</span><span class="sxs-lookup"><span data-stu-id="ac8cc-173">February 28</span></span> | <span data-ttu-id="ac8cc-174">Avskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-174">Depreciation (proposal)</span></span> | <span data-ttu-id="ac8cc-175">983,62Beregning: Bokført verdi (59 000 - 966,67 avskrivning) / Antall gjenværende avskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="ac8cc-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="ac8cc-176">Avskrivningen er undervurdert med 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="ac8cc-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="see-also"></a><span data-ttu-id="ac8cc-177">Se også</span><span class="sxs-lookup"><span data-stu-id="ac8cc-177">See also</span></span>
--------

[<span data-ttu-id="ac8cc-178">Avskrivning av anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="ac8cc-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




