---
title: Mva-betalinger og avrundingsregler
description: Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edbe92d009c77702a21d32afb5aebe93bc5e2ee0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815386"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="acf52-103">Mva-betalinger og avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="acf52-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acf52-104">Denne artikkelen forklarer hvordan oppsettet av avrundingsregler for mva-myndighetene fungerer, og avrunding av merverdiavgiftsbalansen under utligning og bokføring av merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="acf52-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="acf52-105">Med jevne mellomrom må mva rapporteres og betales til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="acf52-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="acf52-106">Dette kan gjøres ved å kjøre prosessen for utligning og postering av mva på Merverdiavgift-siden.</span><span class="sxs-lookup"><span data-stu-id="acf52-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="acf52-107">Merverdiavgift for en periode utlignes mot mva-kontoene, og mva-saldoen posteres til mva-utligningskontoen.</span><span class="sxs-lookup"><span data-stu-id="acf52-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="acf52-108">Mva-saldoen, som posteres på mva-oppgjørskontoen, kan avrundes hvis skattemyndighetene krever det, ved å definere en avrundingsregel på Merverdiavgift-siden.</span><span class="sxs-lookup"><span data-stu-id="acf52-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="acf52-109">Avrundingsdifferansen posteres til mva-avrundingskontoen som velges i feltet Kontoer for automatiske transaksjoner i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="acf52-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="acf52-110">Eksemplet nedenfor viser hvordan avrundingsregelen i Skattemyndighet fungerer.</span><span class="sxs-lookup"><span data-stu-id="acf52-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="acf52-111">Eksempler</span><span class="sxs-lookup"><span data-stu-id="acf52-111">Examples</span></span>

<span data-ttu-id="acf52-112">Den totale merverdiavgiften for en periode viser en kreditsaldo på -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="acf52-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="acf52-113">Den juridiske enheten krevde inn mer merverdiavgift enn den betalte.</span><span class="sxs-lookup"><span data-stu-id="acf52-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="acf52-114">Derfor skylder den juridiske enheten penger til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="acf52-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="acf52-115">Den juridiske enheten ønsker å bruke en avrundingsmetode som runder av saldoen til nærmeste 1,00.</span><span class="sxs-lookup"><span data-stu-id="acf52-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="acf52-116">Brukeren som er ansvarlig for merverdiavgiftsregnskapet, gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="acf52-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="acf52-117">Klikk **Avgift** > **Indirekte avgifter** > **Merverdiavgift** > **Skattemyndigheter**.</span><span class="sxs-lookup"><span data-stu-id="acf52-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="acf52-118">Velg **Normal** i **Avrundingsform**-feltet på hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="acf52-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="acf52-119">Angi 1,00 i **Avrund**-feltet.</span><span class="sxs-lookup"><span data-stu-id="acf52-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="acf52-120">Når tiden er inne for å betale merverdiavgift til skattemyndighetene, går du til **Avgift** > **Deklareringer** > **Merverdiavgift** > **Utlign og poster merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="acf52-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="acf52-121">I mva-oppgjørskontoen kan du se at avgiftsgjeldbeløpet på **98 765,43** avrundes til **98 765**.</span><span class="sxs-lookup"><span data-stu-id="acf52-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="acf52-122">Tabellen nedenfor viser hvordan et beløp på 98 765,43 avrundes ved hjelp av hver avrundingsmetode som er tilgjengelig i **Avrundingsform**-feltet på siden **Skattemyndigheter**.</span><span class="sxs-lookup"><span data-stu-id="acf52-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="acf52-123">Hvis avrundingsverdien er angitt som 0,00:</span><span class="sxs-lookup"><span data-stu-id="acf52-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="acf52-124">For vanlig avrunding er avrundingsfunksjonen den samme som for **Avrunding = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="acf52-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="acf52-125">For **Avrundingsform**, **Nedover**, **Avrundes opp** og **Egen fordel** er virkemåten den samme som for **Avrunding = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="acf52-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="acf52-126">Avrundingsform</span><span class="sxs-lookup"><span data-stu-id="acf52-126">Rounding form option</span></span>                | <span data-ttu-id="acf52-127">Avrundingsverdi = 0,01</span><span class="sxs-lookup"><span data-stu-id="acf52-127">Round-off value = 0.01</span></span> | <span data-ttu-id="acf52-128">Avrundingsverdi = 0,10</span><span class="sxs-lookup"><span data-stu-id="acf52-128">Round-off value = 0.10</span></span> | <span data-ttu-id="acf52-129">Avrundingsverdi = 1,00</span><span class="sxs-lookup"><span data-stu-id="acf52-129">Round-off value = 1.00</span></span> | <span data-ttu-id="acf52-130">Avrundingsverdi = 100,00</span><span class="sxs-lookup"><span data-stu-id="acf52-130">Round-off value = 100.00</span></span> | <span data-ttu-id="acf52-131">Avrundingsverdi = 0,00</span><span class="sxs-lookup"><span data-stu-id="acf52-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="acf52-132">Normal</span><span class="sxs-lookup"><span data-stu-id="acf52-132">Normal</span></span>                              | <span data-ttu-id="acf52-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="acf52-133">98,765.43</span></span>              | <span data-ttu-id="acf52-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="acf52-134">98,765.40</span></span>              | <span data-ttu-id="acf52-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="acf52-135">98,765.00</span></span>              | <span data-ttu-id="acf52-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="acf52-136">98,800.00</span></span>                | <span data-ttu-id="acf52-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="acf52-137">98,765.43</span></span>                |
| <span data-ttu-id="acf52-138">Nedover</span><span class="sxs-lookup"><span data-stu-id="acf52-138">Downward</span></span>                            | <span data-ttu-id="acf52-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="acf52-139">98,765.43</span></span>              | <span data-ttu-id="acf52-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="acf52-140">98,765.40</span></span>              | <span data-ttu-id="acf52-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="acf52-141">98,765.00</span></span>              | <span data-ttu-id="acf52-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="acf52-142">98,700.00</span></span>                | <span data-ttu-id="acf52-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="acf52-143">98,765.00</span></span>                |
| <span data-ttu-id="acf52-144">Avrundes opp</span><span class="sxs-lookup"><span data-stu-id="acf52-144">Rounding-up</span></span>                         | <span data-ttu-id="acf52-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="acf52-145">98,765.43</span></span>              | <span data-ttu-id="acf52-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="acf52-146">98,765.50</span></span>              | <span data-ttu-id="acf52-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="acf52-147">98,766.00</span></span>              | <span data-ttu-id="acf52-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="acf52-148">98,800.00</span></span>                | <span data-ttu-id="acf52-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="acf52-149">98,766.00</span></span>                |
| <span data-ttu-id="acf52-150">Egen fordel, for en kreditsaldo</span><span class="sxs-lookup"><span data-stu-id="acf52-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="acf52-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="acf52-151">98,765.43</span></span>              | <span data-ttu-id="acf52-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="acf52-152">98,765.40</span></span>              | <span data-ttu-id="acf52-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="acf52-153">98,765.00</span></span>              | <span data-ttu-id="acf52-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="acf52-154">98,700.00</span></span>                | <span data-ttu-id="acf52-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="acf52-155">98,765.00</span></span>                |
| <span data-ttu-id="acf52-156">Egen fordel, for en debetsaldo</span><span class="sxs-lookup"><span data-stu-id="acf52-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="acf52-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="acf52-157">98,765.43</span></span>              | <span data-ttu-id="acf52-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="acf52-158">98,765.50</span></span>              | <span data-ttu-id="acf52-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="acf52-159">98,766.00</span></span>              | <span data-ttu-id="acf52-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="acf52-160">98,800.00</span></span>                | <span data-ttu-id="acf52-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="acf52-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="acf52-162">Vanlig avrunding, og avrundingspresisjon er 0,01</span><span class="sxs-lookup"><span data-stu-id="acf52-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="acf52-163">Avrunding</span><span class="sxs-lookup"><span data-stu-id="acf52-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="acf52-164">Beregningsprosessen</span><span class="sxs-lookup"><span data-stu-id="acf52-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="acf52-165">avrunding (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="acf52-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="acf52-166">avrunding (1,015 / 0,01, 0) = avrunding (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="acf52-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="acf52-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="acf52-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="acf52-168">avrunding (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="acf52-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="acf52-169">avrunding (1,014 / 0,01, 0) = avrunding (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="acf52-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="acf52-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="acf52-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="acf52-171">avrunding (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="acf52-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="acf52-172">avrunding (1,011 / 0,02, 0) = avrunding (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="acf52-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="acf52-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="acf52-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="acf52-174">avrunding (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="acf52-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="acf52-175">avrunding (1,009 / 0,02, 0) = avrunding (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="acf52-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="acf52-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="acf52-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="acf52-177">Hvis du velger Egen fordel, skjer avrundingen alltid til fordel for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="acf52-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="acf52-178">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="acf52-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="acf52-179">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="acf52-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="acf52-180">Opprette en mva-betaling</span><span class="sxs-lookup"><span data-stu-id="acf52-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="acf52-181">Opprette mva-transaksjoner på dokumenter</span><span class="sxs-lookup"><span data-stu-id="acf52-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="acf52-182">Vise posterte mva-transaksjoner</span><span class="sxs-lookup"><span data-stu-id="acf52-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="acf52-183">avrundingsfunksjon</span><span class="sxs-lookup"><span data-stu-id="acf52-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]