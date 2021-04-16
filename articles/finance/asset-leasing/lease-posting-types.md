---
title: Leieposteringstyper
description: Dette emnet beskriver posteringstypene som brukes ved transaksjoner for leie av anleggsmidler.
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
ms.openlocfilehash: ddc229f3ab8e048390f27503e2c6c26bd1a6f24f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841147"
---
# <a name="lease-posting-types"></a><span data-ttu-id="a0410-103">Leieposteringstyper</span><span class="sxs-lookup"><span data-stu-id="a0410-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0410-104">Dette emnet beskriver posteringstypene som brukes ved transaksjoner for leie av anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="a0410-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="a0410-105">Leieaktivum</span><span class="sxs-lookup"><span data-stu-id="a0410-105">Lease asset</span></span>

<span data-ttu-id="a0410-106">Kontoen er knyttet til bruksrettseiendelen.</span><span class="sxs-lookup"><span data-stu-id="a0410-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="a0410-107">Denne kontoen debiteres når en leieavtale opprinnelig gjenkjennes i henhold til de nye regnskapsstandardene for leieavtaler, Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="a0410-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="a0410-108">For en modifisert leieavtale kan denne kontoen enten debiteres eller krediteres, avhengig av om endringen øker eller reduserer leieforpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="a0410-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="a0410-109">**Eksempeljournaloppføringer:** Opprinnelig føring</span><span class="sxs-lookup"><span data-stu-id="a0410-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="a0410-110">**Debet:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a0410-111">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="a0410-112">Leiegjeld</span><span class="sxs-lookup"><span data-stu-id="a0410-112">Lease liability</span></span>

<span data-ttu-id="a0410-113">Kontoen er knyttet til leieforpliktelsen som oppstår når betalinger blir diskontert under de nye IFRS 16- og ASC 842-standardene.</span><span class="sxs-lookup"><span data-stu-id="a0410-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="a0410-114">Denne kontoen krediteres når en leieavtale opprinnelig gjenkjennes under de nye standardene.</span><span class="sxs-lookup"><span data-stu-id="a0410-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="a0410-115">Den debiteres for leiebetalinger og krediteres for renteavsetninger.</span><span class="sxs-lookup"><span data-stu-id="a0410-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="a0410-116">**Eksempeljournaloppføringer:** Opprinnelig føring</span><span class="sxs-lookup"><span data-stu-id="a0410-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="a0410-117">**Debet:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a0410-118">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="a0410-119">**Eksempeljournalposter:** Renteavsetning</span><span class="sxs-lookup"><span data-stu-id="a0410-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="a0410-120">**Debet:** Renteutgift XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="a0410-121">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="a0410-122">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="a0410-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a0410-123">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a0410-124">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="a0410-125">Kortsiktig leiegjeld</span><span class="sxs-lookup"><span data-stu-id="a0410-125">Short-term lease liability</span></span>

<span data-ttu-id="a0410-126">Kontoen knyttes til korttidsleieforpliktelsen når journaloppføringen for omklassifisering av korttidsleieforpliktelse posteres.</span><span class="sxs-lookup"><span data-stu-id="a0410-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="a0410-127">Denne kontoen krediteres for kortsiktig gjeld fra nedbetalingplanen på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="a0410-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="a0410-128">Det samme beløpet blir imidlertid debitert den første dagen i neste måned.</span><span class="sxs-lookup"><span data-stu-id="a0410-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="a0410-129">**Eksempeljournaloppføringer:** Omklassifisering av kortsiktig leieforpliktelse</span><span class="sxs-lookup"><span data-stu-id="a0410-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="a0410-130">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a0410-131">**Kredit:** Kortsiktig leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="a0410-132">**Debet:** Kortsiktig leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="a0410-133">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="a0410-134">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="a0410-134">Depreciation expense</span></span>

<span data-ttu-id="a0410-135">Kontoen er knyttet til utgiften som er knyttet til avskrivningen for bruksrettseiendelen under IFRS 16, ASC 842 og finansiell leie under IAS 17 og ASC 840.</span><span class="sxs-lookup"><span data-stu-id="a0410-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="a0410-136">Denne kontoen debiteres når en bruksrettseiendel avskrives hver måned.</span><span class="sxs-lookup"><span data-stu-id="a0410-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="a0410-137">**Eksempeljournaloppføringer:** Avskrivningsavsetning</span><span class="sxs-lookup"><span data-stu-id="a0410-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="a0410-138">**Debet:** Avskrivningskostnad XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="a0410-139">**Kredit:** Akkumulert avskrivning XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="a0410-140">Fortjeneste/tap ved endring av leie</span><span class="sxs-lookup"><span data-stu-id="a0410-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="a0410-141">Kontoen er knyttet til tap eller vinning som oppstår ved leieendringer.</span><span class="sxs-lookup"><span data-stu-id="a0410-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="a0410-142">Det kan oppstå en gevinst under en endring i leien hvis endringen reduserer leieforpliktelsen med et beløp som overskrider den bokførte verdien til bruksrettseiendelen.</span><span class="sxs-lookup"><span data-stu-id="a0410-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="a0410-143">En leie har for eksempel en gjeldende bokført verdi for leieforpliktelsen på $150 000 og en bokført verdi for bruksrettseiendelen på $100 000.</span><span class="sxs-lookup"><span data-stu-id="a0410-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="a0410-144">Leieavtalen endres, og denne endringen gir en ny nåverdi av fremtidige minimums leiebetalinger (PVFMLP) på $40 000.</span><span class="sxs-lookup"><span data-stu-id="a0410-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="a0410-145">Derfor blir leieforpliktelse debitert med $110 000 ($150 000–$40 000).</span><span class="sxs-lookup"><span data-stu-id="a0410-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="a0410-146">Siden bruksrettseiendelen bare er $100 000, vil reduksjonen på $110 000 redusere aktivaet under 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a0410-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="a0410-147">Derfor angir regnskapsveiledningen at resten skal bokføres til en fortjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="a0410-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="a0410-148">I dette tilfellet vil den endelige journaloppføringen være en debitering av leieforpliktelsen på $110 000, en kreditering til leieaktivaet på $100 000, og en kreditering av fortjenestekontoen på $10 000.</span><span class="sxs-lookup"><span data-stu-id="a0410-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="a0410-149">**Eksempeljournaloppføringer:** Leieendring</span><span class="sxs-lookup"><span data-stu-id="a0410-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="a0410-150">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a0410-151">**Kredit:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="a0410-152">**Kredit:** Fortjeneste XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="a0410-153">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="a0410-153">Accumulated depreciation</span></span>

<span data-ttu-id="a0410-154">Kontoen er knyttet til kontoen for bruksrettseiendelen.</span><span class="sxs-lookup"><span data-stu-id="a0410-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="a0410-155">Denne kontoen krediteres når en avskrivningskostnad posteres.</span><span class="sxs-lookup"><span data-stu-id="a0410-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="a0410-156">**Eksempeljournaloppføringer:** Avskrivningsavsetning</span><span class="sxs-lookup"><span data-stu-id="a0410-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="a0410-157">**Debet:** Avskrivningskostnad XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="a0410-158">**Kredit:** Akkumulert avskrivning XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="a0410-159">Variabel betaling</span><span class="sxs-lookup"><span data-stu-id="a0410-159">Variable payment</span></span>

<span data-ttu-id="a0410-160">Kontoen er knyttet til variable leiebetalinger som produseres ved hjelp av en indeksverdiregulering under ASC 842, ASC 840 og IAS 17-leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="a0410-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="a0410-161">I leiebetalingsplanen er variable betalinger inkludert i **Variabel betaling**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="a0410-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="a0410-162">Denne kontoen debiteres når det opprettes en faktura mot en betalingsplanlinje som inneholder en variabel betaling.</span><span class="sxs-lookup"><span data-stu-id="a0410-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="a0410-163">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="a0410-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a0410-164">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a0410-165">**Debet:** Variabel betaling XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="a0410-166">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="a0410-167">Aktiva med utsatt leie (gjeld)</span><span class="sxs-lookup"><span data-stu-id="a0410-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="a0410-168">Kontoen er knyttet til aktiva med utsatt leie eller gjeld som fremstilles av en leieavtale med utsatt leie.</span><span class="sxs-lookup"><span data-stu-id="a0410-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="a0410-169">Denne kontoen debiteres når en faktura posteres mot en leieavtale med utsatt leie, hvis leiebetalingsbeløpet er mer enn periodens lineær renteutgift.</span><span class="sxs-lookup"><span data-stu-id="a0410-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="a0410-170">Den krediteres hvis leiebetalingen er mindre enn periodens lineær renteutgift.</span><span class="sxs-lookup"><span data-stu-id="a0410-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="a0410-171">**Eksempel på journaloppføringer:** Leiebetaling (leieavtale med utsatt leie)</span><span class="sxs-lookup"><span data-stu-id="a0410-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="a0410-172">**Debet:** Leieutgift XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="a0410-173">**Kredit:** Utsatt leieavgift (gjeld) XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="a0410-174">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="a0410-175">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="a0410-175">Lease expense</span></span>

<span data-ttu-id="a0410-176">Kontoen er knyttet til leieutgiften hvis leieavtalen klassifiseres som en leieavtale med utsatt leie.</span><span class="sxs-lookup"><span data-stu-id="a0410-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="a0410-177">Denne kontoen debiteres når en faktura posteres mot en leieavtale med utsatt leie.</span><span class="sxs-lookup"><span data-stu-id="a0410-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="a0410-178">**Eksempel på journaloppføringer:** Leiebetaling (leieavtale med utsatt leie)</span><span class="sxs-lookup"><span data-stu-id="a0410-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="a0410-179">**Debet:** Leieutgift XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="a0410-180">**Kredit:** Utsatt leieavgift (gjeld) XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="a0410-181">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="a0410-182">Verdiforringelsesutgift</span><span class="sxs-lookup"><span data-stu-id="a0410-182">Impairment expense</span></span>

<span data-ttu-id="a0410-183">Kontoen posteres mot når en leieavtale svekkes.</span><span class="sxs-lookup"><span data-stu-id="a0410-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="a0410-184">Denne kontoen debiteres, mens bruksrettseiendelskontoen krediteres direkte.</span><span class="sxs-lookup"><span data-stu-id="a0410-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="a0410-185">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="a0410-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a0410-186">**Debet:** Verdiforringelsesutgift XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="a0410-187">**Kredit:** Bruksrettseiendel XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="a0410-188">Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="a0410-188">Lease payment</span></span>

<span data-ttu-id="a0410-189">Kontoen posteres mot hvis parameteren **Betal til leverandør** er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="a0410-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="a0410-190">Denne kontoen krediteres i stedet for leverandøren hvis parameteren er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="a0410-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="a0410-191">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="a0410-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a0410-192">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a0410-193">**Kredit:** Leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="a0410-194">Utgiftstypeposteringer</span><span class="sxs-lookup"><span data-stu-id="a0410-194">Expense type postings</span></span>

<span data-ttu-id="a0410-195">Kontoen som velges for hver utgiftstype, debiteres når det genereres en betaling for denne utgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="a0410-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="a0410-196">Kontoen som er angitt for utgiftstypen **Forsikring**, debiteres eksempelvis når en journaloppføring for faktura eller betaling opprettes ut fra fullbyrdelseskostnadsplanen for forsikringsutgifter.</span><span class="sxs-lookup"><span data-stu-id="a0410-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="a0410-197">**Eksempeljournaloppføringer:** Forsikringsbetaling</span><span class="sxs-lookup"><span data-stu-id="a0410-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="a0410-198">**Debet:** Forsikringsutgiftstypekonto XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="a0410-199">**Kredit:** Motkonto XXX</span><span class="sxs-lookup"><span data-stu-id="a0410-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="a0410-200">Motkontoen velges på leienivå på linjene for betalingsplanen for fullbyrdelseskostnad.</span><span class="sxs-lookup"><span data-stu-id="a0410-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="a0410-201">Denne motkontoen kan knyttes til leverandøren eller til en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="a0410-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
