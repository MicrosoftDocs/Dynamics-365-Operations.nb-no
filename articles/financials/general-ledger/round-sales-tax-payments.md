---
title: Mva-betalinger og avrundingsregler
description: Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1531863"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="a3c33-103">Mva-betalinger og avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="a3c33-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3c33-104">Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="a3c33-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="a3c33-105">Med jevne mellomrom må mva rapporteres og betales til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="a3c33-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="a3c33-106">Dette kan gjøres ved å kjøre prosessen for utligning og postering av mva på Merverdiavgift-siden.</span><span class="sxs-lookup"><span data-stu-id="a3c33-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="a3c33-107">Merverdiavgift for en periode utlignes mot mva-kontoene, og mva-saldoen posteres til mva-utligningskontoen.</span><span class="sxs-lookup"><span data-stu-id="a3c33-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="a3c33-108">Mva-saldoen, som posteres på mva-oppgjørskontoen, kan avrundes hvis skattemyndighetene krever det, ved å definere en avrundingsregel på Merverdiavgift-siden.</span><span class="sxs-lookup"><span data-stu-id="a3c33-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="a3c33-109">Avrundingsdifferansen posteres til mva-avrundingskontoen som velges i feltet Kontoer for automatiske transaksjoner i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="a3c33-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="a3c33-110">Eksemplet nedenfor viser hvordan avrundingsregelen i Skattemyndighet fungerer.</span><span class="sxs-lookup"><span data-stu-id="a3c33-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="a3c33-111">Eksempler</span><span class="sxs-lookup"><span data-stu-id="a3c33-111">Examples</span></span>

<span data-ttu-id="a3c33-112">Den totale merverdiavgiften for en periode viser en kreditsaldo på -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="a3c33-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="a3c33-113">Den juridiske enheten krevde inn mer merverdiavgift enn den betalte.</span><span class="sxs-lookup"><span data-stu-id="a3c33-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="a3c33-114">Derfor skylder den juridiske enheten penger til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="a3c33-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="a3c33-115">Den juridiske enheten ønsker å bruke en avrundingsmetode som runder av saldoen til nærmeste 1,00.</span><span class="sxs-lookup"><span data-stu-id="a3c33-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="a3c33-116">Brukeren som er ansvarlig for merverdiavgiftsregnskapet, gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="a3c33-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="a3c33-117">Klikk Avgift &gt; Indirekte avgifter &gt; Merverdiavgift &gt; Skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="a3c33-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="a3c33-118">Velg Normal i Avrundingsform-feltet på hurtigfanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="a3c33-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="a3c33-119">Angi 1,00i Avrund-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3c33-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="a3c33-120">Når tiden er inne for å betale merverdiavgift til skattemyndighetene, åpner du siden Utlign og poster merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="a3c33-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="a3c33-121">(Klikk Avgift &gt; Deklareringer &gt; Merverdiavgift &gt; Utlign og poster merverdiavgift.)</span><span class="sxs-lookup"><span data-stu-id="a3c33-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="a3c33-122">I mva-oppgjørskontoen rundes avgiftsgjeldbeløpet på 98 765,43 av til 98 765.</span><span class="sxs-lookup"><span data-stu-id="a3c33-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="a3c33-123">Tabellen nedenfor viser hvordan et beløp på 98 765,43 avrundes ved hjelp av hver avrundingsmetode som er tilgjengelig i Avrundingsform-feltet på siden Skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="a3c33-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="a3c33-124">Avrundingsform</span><span class="sxs-lookup"><span data-stu-id="a3c33-124">Rounding form option</span></span>                | <span data-ttu-id="a3c33-125">Avrundingsverdi = 0,01</span><span class="sxs-lookup"><span data-stu-id="a3c33-125">Round-off value = 0.01</span></span> | <span data-ttu-id="a3c33-126">Avrundingsverdi = 0,10</span><span class="sxs-lookup"><span data-stu-id="a3c33-126">Round-off value = 0.10</span></span> | <span data-ttu-id="a3c33-127">Avrundingsverdi = 1,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-127">Round-off value = 1.00</span></span> | <span data-ttu-id="a3c33-128">Avrundingsverdi = 100,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="a3c33-129">Normal</span><span class="sxs-lookup"><span data-stu-id="a3c33-129">Normal</span></span>                              | <span data-ttu-id="a3c33-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a3c33-130">98,765.43</span></span>              | <span data-ttu-id="a3c33-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="a3c33-131">98,765.40</span></span>              | <span data-ttu-id="a3c33-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-132">98,765.00</span></span>              | <span data-ttu-id="a3c33-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-133">98,800.00</span></span>                |
| <span data-ttu-id="a3c33-134">Nedover</span><span class="sxs-lookup"><span data-stu-id="a3c33-134">Downward</span></span>                            | <span data-ttu-id="a3c33-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a3c33-135">98,765.43</span></span>              | <span data-ttu-id="a3c33-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="a3c33-136">98,765.40</span></span>              | <span data-ttu-id="a3c33-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-137">98,765.00</span></span>              | <span data-ttu-id="a3c33-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-138">98,700.00</span></span>                |
| <span data-ttu-id="a3c33-139">Avrundes opp</span><span class="sxs-lookup"><span data-stu-id="a3c33-139">Rounding-up</span></span>                         | <span data-ttu-id="a3c33-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a3c33-140">98,765.43</span></span>              | <span data-ttu-id="a3c33-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="a3c33-141">98,765.50</span></span>              | <span data-ttu-id="a3c33-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-142">98,766.00</span></span>              | <span data-ttu-id="a3c33-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-143">98,800.00</span></span>                |
| <span data-ttu-id="a3c33-144">Egen fordel, for en kreditsaldo</span><span class="sxs-lookup"><span data-stu-id="a3c33-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="a3c33-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a3c33-145">98,765.43</span></span>              | <span data-ttu-id="a3c33-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="a3c33-146">98,765.40</span></span>              | <span data-ttu-id="a3c33-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-147">98,765.00</span></span>              | <span data-ttu-id="a3c33-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-148">98,700.00</span></span>                |
| <span data-ttu-id="a3c33-149">Egen fordel, for en debetsaldo</span><span class="sxs-lookup"><span data-stu-id="a3c33-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="a3c33-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a3c33-150">98,765.43</span></span>              | <span data-ttu-id="a3c33-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="a3c33-151">98,765.50</span></span>              | <span data-ttu-id="a3c33-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a3c33-152">98,766.00</span></span>              | <span data-ttu-id="a3c33-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a3c33-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="a3c33-154">Ingen avrunding i det hele tatt, siden avrundingen er 0,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="a3c33-155">avrunding (1,0151, 0,00) = 1,0151 avrunding (1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="a3c33-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="a3c33-156">Vanlig avrunding, og avrundingspresisjon er 0,01</span><span class="sxs-lookup"><span data-stu-id="a3c33-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="a3c33-157">Avrunding</span><span class="sxs-lookup"><span data-stu-id="a3c33-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="a3c33-158">Beregningsprosessen</span><span class="sxs-lookup"><span data-stu-id="a3c33-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a3c33-159">avrunding (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="a3c33-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="a3c33-160">avrunding (1,015 / 0,01, 0) = avrunding (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="a3c33-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="a3c33-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="a3c33-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a3c33-162">avrunding (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="a3c33-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a3c33-163">avrunding (1,014 / 0,01, 0) = avrunding (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="a3c33-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="a3c33-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="a3c33-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a3c33-165">avrunding (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="a3c33-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a3c33-166">avrunding (1,011 / 0,02, 0) = avrunding (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="a3c33-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="a3c33-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="a3c33-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a3c33-168">avrunding (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a3c33-169">avrunding (1,009 / 0,02, 0) = avrunding (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="a3c33-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="a3c33-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="a3c33-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="a3c33-171">Hvis du velger Egen fordel, skjer avrundingen alltid til fordel for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="a3c33-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="a3c33-172">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a3c33-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="a3c33-173">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="a3c33-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="a3c33-174">Opprette en mva-betaling</span><span class="sxs-lookup"><span data-stu-id="a3c33-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="a3c33-175">Opprette salgstransaksjoner på dokumenter</span><span class="sxs-lookup"><span data-stu-id="a3c33-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="a3c33-176">Vise posterte mva-transaksjoner</span><span class="sxs-lookup"><span data-stu-id="a3c33-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="a3c33-177">avrundingsfunksjon</span><span class="sxs-lookup"><span data-stu-id="a3c33-177">round Function</span></span>](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


