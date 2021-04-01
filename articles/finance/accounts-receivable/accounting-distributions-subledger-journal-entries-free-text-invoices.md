---
title: Regnskapsdistribusjoner og journaloppføringer for fritekstfakturaer
description: Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura. Alle beløp som må redegjøres for når fritekstfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5b35347d63bffbf5b9261cbd93f49120ded19a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248069"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a><span data-ttu-id="91a63-104">Regnskapsdistribusjoner og underfinansoppføringer for fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="91a63-104">Accounting distributions and subledger entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91a63-105">Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="91a63-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="91a63-106">Alle beløp som må redegjøres for når fritekstfakturaen er journalføres, har én eller flere regnskapsdistribusjoner.</span><span class="sxs-lookup"><span data-stu-id="91a63-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="91a63-107">Regnskapsdistribusjoner</span><span class="sxs-lookup"><span data-stu-id="91a63-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="91a63-108">Du kan bruke følgende knapper på Fritekstfaktura-siden for å vise, og eventuelt endre, regnskapsdistribusjonene for hvert beløp i fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="91a63-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="91a63-109">**Fordel beløp** – Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer, for eksempel avgifter eller gebyrer.</span><span class="sxs-lookup"><span data-stu-id="91a63-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="91a63-110">Du kan også vise og endre regnskapsdistribusjonene for den underordnede linjen direkte fra Mva-transaksjoner- eller Tilleggstransaksjoner-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="91a63-111">Endre fritekstfakturahodebeløp, for eksempel tillegg eller avrundingsbeløp for valuta.</span><span class="sxs-lookup"><span data-stu-id="91a63-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="91a63-112">Endre fritekstfakturalinjebeløp.</span><span class="sxs-lookup"><span data-stu-id="91a63-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="91a63-113">**Vis distribusjoner** – Vis regnskapsdistribusjonene for alle linjer i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="91a63-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="91a63-114">Du kan ikke endre regnskapsdistribusjonene fra denne visningen.</span><span class="sxs-lookup"><span data-stu-id="91a63-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="91a63-115">Vis overskrift og linjebeløp.</span><span class="sxs-lookup"><span data-stu-id="91a63-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="91a63-116">Distribuere beløp</span><span class="sxs-lookup"><span data-stu-id="91a63-116">Distributing amounts</span></span>
<span data-ttu-id="91a63-117">Når du registrerer en fritekstfaktura, fordeles hvert beløp på følgende måte.</span><span class="sxs-lookup"><span data-stu-id="91a63-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91a63-118">Angi et pengebeløp</span><span class="sxs-lookup"><span data-stu-id="91a63-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="91a63-119">Der hovedkontoen vises fra</span><span class="sxs-lookup"><span data-stu-id="91a63-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="91a63-120">Rekkefølge som bestemmer hvilken standard finansdimensjon som vises</span><span class="sxs-lookup"><span data-stu-id="91a63-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91a63-121">Fritekstfakturalinje</span><span class="sxs-lookup"><span data-stu-id="91a63-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="91a63-122">Finanskontoen på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="91a63-123">Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="91a63-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="91a63-124">Hvis hovedkontoen ikke er en tildelingskonto, bruk standardmalen for finansdimensjon på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-125">Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-126">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a63-127">Fritekstfakturalinje for en anleggsmiddelnummer- og verdimodellkombinasjon</span><span class="sxs-lookup"><span data-stu-id="91a63-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="91a63-128"><strong>Obs! </strong></span><span class="sxs-lookup"><span data-stu-id="91a63-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91a63-129">Hovedkontoen på fritekstfakturalinjen blir avhendingskonto for anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="91a63-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="91a63-130">Finanskontoen på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="91a63-131">Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-132">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a63-133">Rabattbeløp for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="91a63-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="91a63-134">Hovedkontoen for kunderabattfelt på Kontantrabatt-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="91a63-135">Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="91a63-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="91a63-136">Hvis hovedkontoen ikke er en tildelingskonto, bruk standardmalen for finansdimensjon på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-137">Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-138">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91a63-139">Mva-beløp for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="91a63-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="91a63-140">Feltet Konto, utgående mva på siden Finansposteringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="91a63-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="91a63-141">Bruk finansdimensjonene som er definert for linjebeløpet for fritekstfakturaen eller distribusjonene for gebyrlinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="91a63-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="91a63-142">Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-143">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91a63-144">Gebyrlinjebeløp for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="91a63-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="91a63-145">Kreditkonto-feltet på siden Tilleggskode.</span><span class="sxs-lookup"><span data-stu-id="91a63-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="91a63-146">Hvis hovedkontoen er en tildelingskonto, bruker du standardverdien fra tildelingskontodefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="91a63-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="91a63-147">Hvis hovedkontoen ikke er en tildelingskonto, bruk standardmalen for finansdimensjon på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-148">Bruk standard finansdimensjonsverdier på fritekstfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="91a63-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="91a63-149">Bruk standard finansdimensjonsverdier fra hovedkontoen på Kontoplan-siden.</span><span class="sxs-lookup"><span data-stu-id="91a63-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="91a63-150">Distribusjonsavgifter</span><span class="sxs-lookup"><span data-stu-id="91a63-150">Distributing taxes</span></span>
<span data-ttu-id="91a63-151">Kan ikke opprette regnskapsdistribusjoner for avgifter før avgifter er beregnet.</span><span class="sxs-lookup"><span data-stu-id="91a63-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="91a63-152">Hvis du vil beregne merverdiavgift, må du fullføre en av de følgende oppgavene i Fritekstfaktura-skjemaet:</span><span class="sxs-lookup"><span data-stu-id="91a63-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="91a63-153">Vis merverdiavgiften.</span><span class="sxs-lookup"><span data-stu-id="91a63-153">View the sales tax.</span></span>
-   <span data-ttu-id="91a63-154">Vis fakturatotalen.</span><span class="sxs-lookup"><span data-stu-id="91a63-154">View the invoice total.</span></span>
-   <span data-ttu-id="91a63-155">Vis kontantstrømmen.</span><span class="sxs-lookup"><span data-stu-id="91a63-155">View the cash flow.</span></span>
-   <span data-ttu-id="91a63-156">Vis regnskapsdistribusjoner for hele fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="91a63-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="91a63-157">Vis underfinansjournalen.</span><span class="sxs-lookup"><span data-stu-id="91a63-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="91a63-158"> Underfinansjournaler for fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="91a63-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="91a63-159">Før du posterer en fritekstfaktura, kan du vise den fullstendige regnskapsoppføringen for fakturaen, som inkluderer debet og kredit, for å bekrefte at fakturaen posteres på de riktige kontoene.</span><span class="sxs-lookup"><span data-stu-id="91a63-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="91a63-160">Denne visningen av den fullstendige regnskapsoppføringen kalles en underfinansjournal.</span><span class="sxs-lookup"><span data-stu-id="91a63-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="91a63-161">Hvis underfinansjournaloppføringen er feil når du forhåndsviser den før du journalfører fritekstfakturaen, kan du ikke endre underfinansjournaloppføringen.</span><span class="sxs-lookup"><span data-stu-id="91a63-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="91a63-162">I stedet må du endre regnskapsdistribusjonene eller posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="91a63-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="91a63-163">Regnskapsdistribusjonene brukes til å definere én side av regnskapsoppføringen, debet eller kredit.</span><span class="sxs-lookup"><span data-stu-id="91a63-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="91a63-164">Motkontooppføringen i underfinansjournalen opprettes fra posteringsprofilene, for eksempel fra kundekontoen eller avgiften.</span><span class="sxs-lookup"><span data-stu-id="91a63-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]