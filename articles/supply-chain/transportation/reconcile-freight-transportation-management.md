---
title: Avstemme frakt i transportstyring
description: Dette emnet beskriver fraktavstemmingsprosessen.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014514"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="ced5d-103">Avstemme frakt i transportstyring</span><span class="sxs-lookup"><span data-stu-id="ced5d-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ced5d-104">Dette emnet beskriver fraktavstemmingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ced5d-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="ced5d-105">Fraktavstemming kan gjøres manuelt, eller det kan settes opp til å skje automatisk.</span><span class="sxs-lookup"><span data-stu-id="ced5d-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="ced5d-106">Hvis du vil bruke automatisk fraktavstemming, må du opprette en revisjonsstandard der du kan definere kriteriene som bestemmer hvilke fraktbrev som sammenlignes automatisk.</span><span class="sxs-lookup"><span data-stu-id="ced5d-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="ced5d-107">Fraktavstemmingsprosessen</span><span class="sxs-lookup"><span data-stu-id="ced5d-107">The freight reconciliation process</span></span>

<span data-ttu-id="ced5d-108">Fraktsatser beregnes av satsmotoren som er tilknyttet med den aktuelle transportøren.</span><span class="sxs-lookup"><span data-stu-id="ced5d-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="ced5d-109">Når en last er bekreftet, genereres et fraktbrev og fraktsatser overføres til den.</span><span class="sxs-lookup"><span data-stu-id="ced5d-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="ced5d-110">Fraktsatsene fordeles som tillegg til det aktuelle kildedokumentet (bestilling, salgsordre, og/eller overføringsordre), avhengig av oppsettet som brukes for den vanlige faktureringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ced5d-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="ced5d-111">Fraktavstemmingsprosessen (som også kalles kontrollprosessen) kan starte så snart fraktfakturaen mottas fra transportøren.</span><span class="sxs-lookup"><span data-stu-id="ced5d-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="ced5d-112">Fakturaen kan mottas elektronisk eller på papir.</span><span class="sxs-lookup"><span data-stu-id="ced5d-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="ced5d-113">Hvis fakturaen mottas på papir, kan du generere en elektronisk faktura ved hjelp av fraktbrevet som mal.</span><span class="sxs-lookup"><span data-stu-id="ced5d-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="ced5d-114">[![Fraktavstemmingsprosessen](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="ced5d-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="ced5d-115">Manuell avstemming</span><span class="sxs-lookup"><span data-stu-id="ced5d-115">Manual reconciliation</span></span>

<span data-ttu-id="ced5d-116">Hvis du er avstemmer frakt manuelt, må du sammenligne hver fakturalinje med fraktbrevlinjen eller -linjene for lasten som skal faktureres.</span><span class="sxs-lookup"><span data-stu-id="ced5d-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="ced5d-117">Du gjør dette på siden **Samsvare fraktbrev og faktura**.</span><span class="sxs-lookup"><span data-stu-id="ced5d-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="ced5d-118">Hvis beløpet på fakturalinjen ikke samsvarer med hvor fraktbrevbeløpet, må du velge en avstemmingsårsak for forskjellen.</span><span class="sxs-lookup"><span data-stu-id="ced5d-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="ced5d-119">Hvis det er flere årsaker til avstemming, kan du dele de ikke-samsvarte beløpene på tvers av dem.</span><span class="sxs-lookup"><span data-stu-id="ced5d-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="ced5d-120">Årsaken til avstemming bestemmer hvordan differansebeløpene posteres i Finans.</span><span class="sxs-lookup"><span data-stu-id="ced5d-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="ced5d-121">Når avstemmingen av hele fakturabeløpet er gjort rede for, sendes sendt til godkjenning, og deretter posteres journalen.</span><span class="sxs-lookup"><span data-stu-id="ced5d-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="ced5d-122">Illustrasjonen nedenfor viser hvordan du genererer en fraktfaktura og utfører fraktavstemming.</span><span class="sxs-lookup"><span data-stu-id="ced5d-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="ced5d-123">[![Fraktavstemmingsoppgaver](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="ced5d-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="ced5d-124">Automatisk avstemming</span><span class="sxs-lookup"><span data-stu-id="ced5d-124">Automatic reconciliation</span></span>

<span data-ttu-id="ced5d-125">Hvis du vil bruke automatisk avstemming, må du angi tidsplanen for avstemming og fakturaene og transportørene som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="ced5d-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="ced5d-126">Treff for fakturalinjer og fraktbrev gjøres i henhold til oppsettet av typen revisjonsstandard og fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="ced5d-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="ced5d-127">Når du har kjørt automatisk avstemming, må du håndtere alle fakturaer som systemet ikke kan samsvare.</span><span class="sxs-lookup"><span data-stu-id="ced5d-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="ced5d-128">Du må behandle disse fakturaene manuelt før du kan bokføre alle fakturaene for betaling.</span><span class="sxs-lookup"><span data-stu-id="ced5d-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="ced5d-129">Samsvare fraktbrev med fraktfakturaer ved hjelp av automatisk eller manuell avstemming</span><span class="sxs-lookup"><span data-stu-id="ced5d-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="ced5d-130">*Samsvaring* er prosessen med å finne fraktsedlene som samsvarer med hver fraktfaktura.</span><span class="sxs-lookup"><span data-stu-id="ced5d-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="ced5d-131">Du kan gjøre dette ved å samsvare én fakturalinje om gangen (manuelt samsvar), eller ved å samsvare alle tilgjengelige fakturaer samtidig (automatisk samsvar).</span><span class="sxs-lookup"><span data-stu-id="ced5d-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="ced5d-132">Automatisk samsvar</span><span class="sxs-lookup"><span data-stu-id="ced5d-132">Auto matching</span></span>

<span data-ttu-id="ced5d-133">Når flere fraktfakturaer samsvares med samme fraktbrev, fungerer prosessen for automatisk samsvar på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="ced5d-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="ced5d-134">Alle fraktfakturaer som ikke samsvarer, sorteres etter beløp, med det største beløpet først.</span><span class="sxs-lookup"><span data-stu-id="ced5d-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="ced5d-135">Fraktfakturaene samsvares én om gangen til fraktbrevet ikke har noe gjenstående positivt beløp.</span><span class="sxs-lookup"><span data-stu-id="ced5d-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="ced5d-136">Det gjenstående beløpet angis, avhengig av oppsettet for revisjonsstandarden og det gjenstående beløpet på fraktfakturaene.</span><span class="sxs-lookup"><span data-stu-id="ced5d-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="ced5d-137">Manuelt samsvar</span><span class="sxs-lookup"><span data-stu-id="ced5d-137">Manual matching</span></span>

<span data-ttu-id="ced5d-138">Alle fraktsedler med positive beløp blir tilgjengelige for samsvar.</span><span class="sxs-lookup"><span data-stu-id="ced5d-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="ced5d-139">I likhet med automatisk samsvar kan brukeren bare samsvare fraktfakturaer med negative beløp med fraktsedler som ikke samsvarer helt.</span><span class="sxs-lookup"><span data-stu-id="ced5d-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="ced5d-140">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ced5d-140">Example</span></span>

<span data-ttu-id="ced5d-141">La oss si at du har en fraktseddel for et beløp på 1500 og har opprettet tre fraktfakturaer for fraktseddelen med én fakturalinje for hver faktura med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="ced5d-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="ced5d-142">Opprinnelig fraktseddel: beløp på 1500</span><span class="sxs-lookup"><span data-stu-id="ced5d-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="ced5d-143">Faktura 1 (Fakt1): beløp på 1000</span><span class="sxs-lookup"><span data-stu-id="ced5d-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="ced5d-144">Faktura 2 (Fakt2): beløp på 600</span><span class="sxs-lookup"><span data-stu-id="ced5d-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="ced5d-145">Faktura 3 (Fakt3): beløp på -100</span><span class="sxs-lookup"><span data-stu-id="ced5d-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="ced5d-146">Resultat for automatisk samsvar</span><span class="sxs-lookup"><span data-stu-id="ced5d-146">Automatic matching result</span></span>

<span data-ttu-id="ced5d-147">Automatisk samsvar utføres i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="ced5d-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="ced5d-148">Sorter alle fraktfakturaer i synkende rekkefølge etter beløp: Fakt1 -> Fakt2 -> Fakt3.</span><span class="sxs-lookup"><span data-stu-id="ced5d-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="ced5d-149">Samsvar Fakt1 med fraktseddel.</span><span class="sxs-lookup"><span data-stu-id="ced5d-149">Match Inv1 with FB.</span></span> <span data-ttu-id="ced5d-150">Fakt1 har 1000 samsvart, og fraktseddel har beløp på 500 gjenstående, slik at statusen settes til *Delvis samsvar*.</span><span class="sxs-lookup"><span data-stu-id="ced5d-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="ced5d-151">Samsvar Fakt2 med fraktseddel.</span><span class="sxs-lookup"><span data-stu-id="ced5d-151">Match Inv2 with FB.</span></span> <span data-ttu-id="ced5d-152">Fakt2 har 500 samsvart, og fraktseddel har beløp på 0 gjenstående, slik at statusen settes til *Fullstendig samsvar*.</span><span class="sxs-lookup"><span data-stu-id="ced5d-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="ced5d-153">Siden fraktseddel nå har fullstendig samsvar, behandles ikke Fakt3.</span><span class="sxs-lookup"><span data-stu-id="ced5d-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="ced5d-154">Resultat for manuelt samsvar</span><span class="sxs-lookup"><span data-stu-id="ced5d-154">Manual matching result</span></span>

<span data-ttu-id="ced5d-155">Når det gjelder manuelt samsvar, varierer resultatene avhengig av samsvarsrekkefølgen, som vist i eksemplene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ced5d-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="ced5d-156">Manuelt samsvar – eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ced5d-156">Manual matching case 1</span></span>

<span data-ttu-id="ced5d-157">Det er flere måter å foreta manuelt samsvar på. I dette eksemplet kan du gå frem på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="ced5d-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="ced5d-158">Samsvar fraktseddel med Fakt1.</span><span class="sxs-lookup"><span data-stu-id="ced5d-158">Match FB with Inv1.</span></span> <span data-ttu-id="ced5d-159">Fraktseddel har beløp på 500 gjenstående, slik at statusen settes til *Delvis samsvar*.</span><span class="sxs-lookup"><span data-stu-id="ced5d-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="ced5d-160">Samsvar Fakt2 med fraktseddel.</span><span class="sxs-lookup"><span data-stu-id="ced5d-160">Match Inv2 with FB.</span></span> <span data-ttu-id="ced5d-161">Fakt2 har 500 samsvart, og fraktseddel har beløp på 0 gjenstående, slik at statusen settes til *Fullstendig samsvar*.</span><span class="sxs-lookup"><span data-stu-id="ced5d-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="ced5d-162">Når Fakt3 samsvares manuelt, finner du ingen fraktsedler uten samsvar.</span><span class="sxs-lookup"><span data-stu-id="ced5d-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="ced5d-163">Dette eksemplet er egentlig det samme som automatisk samsvar</span><span class="sxs-lookup"><span data-stu-id="ced5d-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="ced5d-164">Manuelt samsvar – eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ced5d-164">Manual matching case 2</span></span>

<span data-ttu-id="ced5d-165">I dette eksemplet skal du gå frem på en annen måte for å foreta manuelt samsvar:</span><span class="sxs-lookup"><span data-stu-id="ced5d-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="ced5d-166">Samsvar Fakt3 med fraktseddel.</span><span class="sxs-lookup"><span data-stu-id="ced5d-166">Match Inv3 with FB.</span></span> <span data-ttu-id="ced5d-167">Nå har fraktseddel et gjenstående beløp på 1600, som er det samme som å trekke minus 100 fra 1500.</span><span class="sxs-lookup"><span data-stu-id="ced5d-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="ced5d-168">Både fraktseddel og Fakt3 har et samsvarende antall på -100.</span><span class="sxs-lookup"><span data-stu-id="ced5d-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="ced5d-169">Samsvar Fakt1 og Fakt2 med fraktseddel én om gangen.</span><span class="sxs-lookup"><span data-stu-id="ced5d-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="ced5d-170">Fraktseddel samsvarer fullstendig.</span><span class="sxs-lookup"><span data-stu-id="ced5d-170">FB is fully matched.</span></span>

<span data-ttu-id="ced5d-171">Som dette eksemplet viser bør samsvarende fraktfakturaer med negative beløp bare utføres manuelt.</span><span class="sxs-lookup"><span data-stu-id="ced5d-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="ced5d-172">Dette sikrer at det alltid går an å samsvare fraktfakturaene med negative beløp med en fraktseddel som ikke samsvarer fullstendig, fordi det gjør at du kan kontrollere samsvarsrekkefølgen.</span><span class="sxs-lookup"><span data-stu-id="ced5d-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>
