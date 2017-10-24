---
title: Mva-betalinger og avrundingsregler
description: "Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8de01b77fcbeb65321e60614b6a11d264460208f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="19a5c-103">Mva-betalinger og avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="19a5c-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19a5c-104">Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19a5c-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="19a5c-105">Med jevne mellomrom må mva rapporteres og betales til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="19a5c-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="19a5c-106">Dette kan gjøres ved å kjøre prosessen for utligning og postering av mva på Merverdiavgift-siden.</span><span class="sxs-lookup"><span data-stu-id="19a5c-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="19a5c-107">Merverdiavgift for en periode utlignes mot mva-kontoene, og mva-saldoen posteres til mva-utligningskontoen.</span><span class="sxs-lookup"><span data-stu-id="19a5c-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="19a5c-108">Mva-saldoen, som posteres på mva-oppgjørskontoen, kan avrundes hvis skattemyndighetene krever det, ved å definere en avrundingsregel på Merverdiavgift-siden.</span><span class="sxs-lookup"><span data-stu-id="19a5c-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="19a5c-109">Avrundingsdifferansen posteres til mva-avrundingskontoen som velges i feltet Kontoer for automatiske transaksjoner i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="19a5c-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="19a5c-110">Eksemplet nedenfor viser hvordan avrundingsregelen i Skattemyndighet fungerer.</span><span class="sxs-lookup"><span data-stu-id="19a5c-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="19a5c-111">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="19a5c-111">Example:</span></span>

<span data-ttu-id="19a5c-112">Den totale merverdiavgiften for en periode viser en kreditsaldo på -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="19a5c-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="19a5c-113">Den juridiske enheten krevde inn mer merverdiavgift enn den betalte.</span><span class="sxs-lookup"><span data-stu-id="19a5c-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="19a5c-114">Derfor skylder den juridiske enheten penger til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="19a5c-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="19a5c-115">Den juridiske enheten ønsker å bruke en avrundingsmetode som runder av saldoen til nærmeste 1,00.</span><span class="sxs-lookup"><span data-stu-id="19a5c-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="19a5c-116">Brukeren som er ansvarlig for merverdiavgiftsregnskapet, gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="19a5c-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="19a5c-117">Klikk Avgift &gt; Indirekte avgifter &gt; Merverdiavgift &gt; Skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="19a5c-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="19a5c-118">Velg Normal i Avrundingsform-feltet på hurtigfanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="19a5c-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="19a5c-119">Angi 1,00i Avrund-feltet.</span><span class="sxs-lookup"><span data-stu-id="19a5c-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="19a5c-120">Når tiden er inne for å betale merverdiavgift til skattemyndighetene, åpner du siden Utlign og poster merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19a5c-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="19a5c-121">(Klikk Avgift &gt; Deklareringer &gt; Merverdiavgift &gt; Utlign og poster merverdiavgift.)</span><span class="sxs-lookup"><span data-stu-id="19a5c-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="19a5c-122">I mva-oppgjørskontoen rundes avgiftsgjeldbeløpet på 98 765,43 av til 98 765.</span><span class="sxs-lookup"><span data-stu-id="19a5c-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="19a5c-123">Tabellen nedenfor viser hvordan et beløp på 98 765,43 avrundes ved hjelp av hver avrundingsmetode som er tilgjengelig i Avrundingsform-feltet på siden Skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="19a5c-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="19a5c-124">Avrundingsform</span><span class="sxs-lookup"><span data-stu-id="19a5c-124">Rounding form option</span></span>                | <span data-ttu-id="19a5c-125">Avrundingsverdi = 0,01</span><span class="sxs-lookup"><span data-stu-id="19a5c-125">Round-off value = 0.01</span></span> | <span data-ttu-id="19a5c-126">Avrundingsverdi = 0,10</span><span class="sxs-lookup"><span data-stu-id="19a5c-126">Round-off value = 0.10</span></span> | <span data-ttu-id="19a5c-127">Avrundingsverdi = 1,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-127">Round-off value = 1.00</span></span> | <span data-ttu-id="19a5c-128">Avrundingsverdi = 100,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="19a5c-129">Normal</span><span class="sxs-lookup"><span data-stu-id="19a5c-129">Normal</span></span>                              | <span data-ttu-id="19a5c-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19a5c-130">98,765.43</span></span>              | <span data-ttu-id="19a5c-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="19a5c-131">98,765.40</span></span>              | <span data-ttu-id="19a5c-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-132">98,765.00</span></span>              | <span data-ttu-id="19a5c-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-133">98,800.00</span></span>                |
| <span data-ttu-id="19a5c-134">Nedover</span><span class="sxs-lookup"><span data-stu-id="19a5c-134">Downward</span></span>                            | <span data-ttu-id="19a5c-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19a5c-135">98,765.43</span></span>              | <span data-ttu-id="19a5c-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="19a5c-136">98,765.40</span></span>              | <span data-ttu-id="19a5c-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-137">98,765.00</span></span>              | <span data-ttu-id="19a5c-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-138">98,700.00</span></span>                |
| <span data-ttu-id="19a5c-139">Avrundes opp</span><span class="sxs-lookup"><span data-stu-id="19a5c-139">Rounding-up</span></span>                         | <span data-ttu-id="19a5c-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19a5c-140">98,765.43</span></span>              | <span data-ttu-id="19a5c-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="19a5c-141">98,765.50</span></span>              | <span data-ttu-id="19a5c-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-142">98,766.00</span></span>              | <span data-ttu-id="19a5c-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-143">98,800.00</span></span>                |
| <span data-ttu-id="19a5c-144">Egen fordel, for en kreditsaldo</span><span class="sxs-lookup"><span data-stu-id="19a5c-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="19a5c-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19a5c-145">98,765.43</span></span>              | <span data-ttu-id="19a5c-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="19a5c-146">98,765.40</span></span>              | <span data-ttu-id="19a5c-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-147">98,765.00</span></span>              | <span data-ttu-id="19a5c-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-148">98,700.00</span></span>                |
| <span data-ttu-id="19a5c-149">Egen fordel, for en debetsaldo</span><span class="sxs-lookup"><span data-stu-id="19a5c-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="19a5c-150">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19a5c-150">98,765.43</span></span>              | <span data-ttu-id="19a5c-151">98 765,50</span><span class="sxs-lookup"><span data-stu-id="19a5c-151">98,765.50</span></span>              | <span data-ttu-id="19a5c-152">98 766,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-152">98,766.00</span></span>              | <span data-ttu-id="19a5c-153">98 800,00</span><span class="sxs-lookup"><span data-stu-id="19a5c-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="19a5c-154">Hvis du velger Egen fordel, skjer avrundingen alltid til fordel for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="19a5c-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="19a5c-155">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="19a5c-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="19a5c-156">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19a5c-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="19a5c-157">Opprette en mva-betaling</span><span class="sxs-lookup"><span data-stu-id="19a5c-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="19a5c-158">Opprette salgstransaksjoner på dokumenter</span><span class="sxs-lookup"><span data-stu-id="19a5c-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="19a5c-159">Vise posterte mva-transaksjoner</span><span class="sxs-lookup"><span data-stu-id="19a5c-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



