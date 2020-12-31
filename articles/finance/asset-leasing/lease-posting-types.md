---
title: Leieposteringstyper
description: Dette emnet beskriver posteringstypene som brukes ved transaksjoner for leie av anleggsmidler.
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
ms.openlocfilehash: ceb4fbeb4dbf2f535e05a9d46c84169435d2803b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446605"
---
# <a name="lease-posting-types"></a><span data-ttu-id="3d946-103">Leieposteringstyper</span><span class="sxs-lookup"><span data-stu-id="3d946-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d946-104">Dette emnet beskriver posteringstypene som brukes ved transaksjoner for leie av anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="3d946-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="3d946-105">Leieaktivum</span><span class="sxs-lookup"><span data-stu-id="3d946-105">Lease asset</span></span>

<span data-ttu-id="3d946-106">Kontoen er knyttet til bruksrettseiendelen.</span><span class="sxs-lookup"><span data-stu-id="3d946-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="3d946-107">Denne kontoen debiteres når en leieavtale opprinnelig gjenkjennes i henhold til de nye regnskapsstandardene for leieavtaler, Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="3d946-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="3d946-108">For en modifisert leieavtale kan denne kontoen enten debiteres eller krediteres, avhengig av om endringen øker eller reduserer leieforpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="3d946-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="3d946-109">**Eksempeljournaloppføringer:** Opprinnelig føring</span><span class="sxs-lookup"><span data-stu-id="3d946-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="3d946-110">**Debet:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="3d946-111">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="3d946-112">Leiegjeld</span><span class="sxs-lookup"><span data-stu-id="3d946-112">Lease liability</span></span>

<span data-ttu-id="3d946-113">Kontoen er knyttet til leieforpliktelsen som oppstår når betalinger blir diskontert under de nye IFRS 16- og ASC 842-standardene.</span><span class="sxs-lookup"><span data-stu-id="3d946-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="3d946-114">Denne kontoen krediteres når en leieavtale opprinnelig gjenkjennes under de nye standardene.</span><span class="sxs-lookup"><span data-stu-id="3d946-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="3d946-115">Den debiteres for leiebetalinger og krediteres for renteavsetninger.</span><span class="sxs-lookup"><span data-stu-id="3d946-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="3d946-116">**Eksempeljournaloppføringer:** Opprinnelig føring</span><span class="sxs-lookup"><span data-stu-id="3d946-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="3d946-117">**Debet:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="3d946-118">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="3d946-119">**Eksempeljournalposter:** Renteavsetning</span><span class="sxs-lookup"><span data-stu-id="3d946-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="3d946-120">**Debet:** Renteutgift XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="3d946-121">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="3d946-122">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="3d946-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="3d946-123">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="3d946-124">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="3d946-125">Kortsiktig leiegjeld</span><span class="sxs-lookup"><span data-stu-id="3d946-125">Short-term lease liability</span></span>

<span data-ttu-id="3d946-126">Kontoen knyttes til korttidsleieforpliktelsen når journaloppføringen for omklassifisering av korttidsleieforpliktelse posteres.</span><span class="sxs-lookup"><span data-stu-id="3d946-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="3d946-127">Denne kontoen krediteres for kortsiktig gjeld fra nedbetalingplanen på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="3d946-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="3d946-128">Det samme beløpet blir imidlertid debitert den første dagen i neste måned.</span><span class="sxs-lookup"><span data-stu-id="3d946-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="3d946-129">**Eksempeljournaloppføringer:** Omklassifisering av kortsiktig leieforpliktelse</span><span class="sxs-lookup"><span data-stu-id="3d946-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="3d946-130">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="3d946-131">**Kredit:** Kortsiktig leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="3d946-132">**Debet:** Kortsiktig leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="3d946-133">**Kredit:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="3d946-134">Avskrivningskostnad</span><span class="sxs-lookup"><span data-stu-id="3d946-134">Depreciation expense</span></span>

<span data-ttu-id="3d946-135">Kontoen er knyttet til utgiften som er knyttet til avskrivningen for bruksrettseiendelen under IFRS 16, ASC 842 og finansiell leie under IAS 17 og ASC 840.</span><span class="sxs-lookup"><span data-stu-id="3d946-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="3d946-136">Denne kontoen debiteres når en bruksrettseiendel avskrives hver måned.</span><span class="sxs-lookup"><span data-stu-id="3d946-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="3d946-137">**Eksempeljournaloppføringer:** Avskrivningsavsetning</span><span class="sxs-lookup"><span data-stu-id="3d946-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="3d946-138">**Debet:** Avskrivningskostnad XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="3d946-139">**Kredit:** Akkumulert avskrivning XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="3d946-140">Fortjeneste/tap ved endring av leie</span><span class="sxs-lookup"><span data-stu-id="3d946-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="3d946-141">Kontoen er knyttet til tap eller vinning som oppstår ved leieendringer.</span><span class="sxs-lookup"><span data-stu-id="3d946-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="3d946-142">Det kan oppstå en gevinst under en endring i leien hvis endringen reduserer leieforpliktelsen med et beløp som overskrider den bokførte verdien til bruksrettseiendelen.</span><span class="sxs-lookup"><span data-stu-id="3d946-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="3d946-143">En leie har for eksempel en gjeldende bokført verdi for leieforpliktelsen på $150 000 og en bokført verdi for bruksrettseiendelen på $100 000.</span><span class="sxs-lookup"><span data-stu-id="3d946-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="3d946-144">Leieavtalen endres, og denne endringen gir en ny nåverdi av fremtidige minimums leiebetalinger (PVFMLP) på $40 000.</span><span class="sxs-lookup"><span data-stu-id="3d946-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="3d946-145">Derfor blir leieforpliktelse debitert med $110 000 ($150 000–$40 000).</span><span class="sxs-lookup"><span data-stu-id="3d946-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="3d946-146">Siden bruksrettseiendelen bare er $100 000, vil reduksjonen på $110 000 redusere aktivaet under 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3d946-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="3d946-147">Derfor angir regnskapsveiledningen at resten skal bokføres til en fortjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="3d946-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="3d946-148">I dette tilfellet vil den endelige journaloppføringen være en debitering av leieforpliktelsen på $110 000, en kreditering til leieaktivaet på $100 000, og en kreditering av fortjenestekontoen på $10 000.</span><span class="sxs-lookup"><span data-stu-id="3d946-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="3d946-149">**Eksempeljournaloppføringer:** Leieendring</span><span class="sxs-lookup"><span data-stu-id="3d946-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="3d946-150">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="3d946-151">**Kredit:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="3d946-152">**Kredit:** Fortjeneste XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="3d946-153">Akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="3d946-153">Accumulated depreciation</span></span>

<span data-ttu-id="3d946-154">Kontoen er knyttet til kontoen for bruksrettseiendelen.</span><span class="sxs-lookup"><span data-stu-id="3d946-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="3d946-155">Denne kontoen krediteres når en avskrivningskostnad posteres.</span><span class="sxs-lookup"><span data-stu-id="3d946-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="3d946-156">**Eksempeljournaloppføringer:** Avskrivningsavsetning</span><span class="sxs-lookup"><span data-stu-id="3d946-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="3d946-157">**Debet:** Avskrivningskostnad XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="3d946-158">**Kredit:** Akkumulert avskrivning XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="3d946-159">Tilbakeholdt overskudd</span><span class="sxs-lookup"><span data-stu-id="3d946-159">Retained earnings</span></span>

<span data-ttu-id="3d946-160">Kontoen som er knyttet til tilbakeholdt overskudd.</span><span class="sxs-lookup"><span data-stu-id="3d946-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="3d946-161">Denne kontoen kan enten debiteres eller krediteres i en journaloppføring for overgangsjustering ved å bruke den fullstendige retrospektive metoden eller det kumulative oppdateringsalternativet for metode A.</span><span class="sxs-lookup"><span data-stu-id="3d946-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="3d946-162">Differansen mellom den opprinnelige bruksrettseiendelen og leieforpliktelsen posteres til tilbakeholdt overskudd.</span><span class="sxs-lookup"><span data-stu-id="3d946-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="3d946-163">I sjeldne tilfeller påvirkes også tilbakeholdt overskudd under endring av leieavtaler hvis klassifiseringen av en leieavtale endres fra finansiell til gjeldende for å skrive bruksrettseiendelen opp eller ned, slik at den samsvarer med leieforpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="3d946-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="3d946-164">**Eksempeljournaloppføringer:** Overgangsjustering (fullstendig retrospektiv eller kumulativ oppsamlingsalternativ A-metoden)</span><span class="sxs-lookup"><span data-stu-id="3d946-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="3d946-165">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="3d946-166">**Kredit:** Leieaktiva XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="3d946-167">**Kredit:** Tilbakeholdt overskudd XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="3d946-168">Variabel betaling</span><span class="sxs-lookup"><span data-stu-id="3d946-168">Variable payment</span></span>

<span data-ttu-id="3d946-169">Kontoen er knyttet til variable leiebetalinger som produseres ved hjelp av en indeksverdiregulering under ASC 842, ASC 840 og IAS 17-leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="3d946-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="3d946-170">I leiebetalingsplanen er variable betalinger inkludert i **Variabel betaling**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="3d946-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="3d946-171">Denne kontoen debiteres når det opprettes en faktura mot en betalingsplanlinje som inneholder en variabel betaling.</span><span class="sxs-lookup"><span data-stu-id="3d946-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="3d946-172">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="3d946-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="3d946-173">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="3d946-174">**Debet:** Variabel betaling XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="3d946-175">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="3d946-176">Aktiva med utsatt leie (gjeld)</span><span class="sxs-lookup"><span data-stu-id="3d946-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="3d946-177">Kontoen er knyttet til aktiva med utsatt leie eller gjeld som fremstilles av en leieavtale med utsatt leie.</span><span class="sxs-lookup"><span data-stu-id="3d946-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="3d946-178">Denne kontoen debiteres når en faktura posteres mot en leieavtale med utsatt leie, hvis leiebetalingsbeløpet er mer enn periodens lineær renteutgift.</span><span class="sxs-lookup"><span data-stu-id="3d946-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="3d946-179">Den krediteres hvis leiebetalingen er mindre enn periodens lineær renteutgift.</span><span class="sxs-lookup"><span data-stu-id="3d946-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="3d946-180">**Eksempel på journaloppføringer:** Leiebetaling (leieavtale med utsatt leie)</span><span class="sxs-lookup"><span data-stu-id="3d946-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="3d946-181">**Debet:** Leieutgift XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="3d946-182">**Kredit:** Utsatt leieavgift (gjeld) XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="3d946-183">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="3d946-184">Leieutgift</span><span class="sxs-lookup"><span data-stu-id="3d946-184">Lease expense</span></span>

<span data-ttu-id="3d946-185">Kontoen er knyttet til leieutgiften hvis leieavtalen klassifiseres som en leieavtale med utsatt leie.</span><span class="sxs-lookup"><span data-stu-id="3d946-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="3d946-186">Denne kontoen debiteres når en faktura posteres mot en leieavtale med utsatt leie.</span><span class="sxs-lookup"><span data-stu-id="3d946-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="3d946-187">**Eksempel på journaloppføringer:** Leiebetaling (leieavtale med utsatt leie)</span><span class="sxs-lookup"><span data-stu-id="3d946-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="3d946-188">**Debet:** Leieutgift XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="3d946-189">**Kredit:** Utsatt leieavgift (gjeld) XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="3d946-190">**Kredit:** Leverandør-/leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="3d946-191">Verdiforringelsesutgift</span><span class="sxs-lookup"><span data-stu-id="3d946-191">Impairment expense</span></span>

<span data-ttu-id="3d946-192">Kontoen posteres mot når en leieavtale svekkes.</span><span class="sxs-lookup"><span data-stu-id="3d946-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="3d946-193">Denne kontoen debiteres, mens bruksrettseiendelskontoen krediteres direkte.</span><span class="sxs-lookup"><span data-stu-id="3d946-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="3d946-194">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="3d946-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="3d946-195">**Debet:** Verdiforringelsesutgift XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="3d946-196">**Kredit:** Bruksrettseiendel XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="3d946-197">Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="3d946-197">Lease payment</span></span>

<span data-ttu-id="3d946-198">Kontoen posteres mot hvis parameteren **Betal til leverandør** er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="3d946-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="3d946-199">Denne kontoen krediteres i stedet for leverandøren hvis parameteren er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="3d946-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="3d946-200">**Eksempeljournaloppføringer:** Leiebetaling</span><span class="sxs-lookup"><span data-stu-id="3d946-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="3d946-201">**Debet:** Leieforpliktelse XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="3d946-202">**Kredit:** Leiebetaling XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="3d946-203">Utgiftstypeposteringer</span><span class="sxs-lookup"><span data-stu-id="3d946-203">Expense type postings</span></span>

<span data-ttu-id="3d946-204">Kontoen som velges for hver utgiftstype, debiteres når det genereres en betaling for denne utgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="3d946-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="3d946-205">Kontoen som er angitt for utgiftstypen **Forsikring**, debiteres eksempelvis når en journaloppføring for faktura eller betaling opprettes ut fra fullbyrdelseskostnadsplanen for forsikringsutgifter.</span><span class="sxs-lookup"><span data-stu-id="3d946-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="3d946-206">**Eksempeljournaloppføringer:** Forsikringsbetaling</span><span class="sxs-lookup"><span data-stu-id="3d946-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="3d946-207">**Debet:** Forsikringsutgiftstypekonto XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="3d946-208">**Kredit:** Motkonto XXX</span><span class="sxs-lookup"><span data-stu-id="3d946-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="3d946-209">Motkontoen velges på leienivå på linjene for betalingsplanen for fullbyrdelseskostnad.</span><span class="sxs-lookup"><span data-stu-id="3d946-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="3d946-210">Denne motkontoen kan knyttes til leverandøren eller til en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="3d946-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
