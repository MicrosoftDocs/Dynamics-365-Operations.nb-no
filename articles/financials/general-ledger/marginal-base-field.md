---
title: Mva-satser basert på feltene grensegrunnlag og beregningsmetoder
description: Dette emnet beskriver hvordan verdiene i feltene Grensegrunnlag og Beregningsmetode fastslår avgiftssats(er) i salgs- og kjøpstransaksjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0128743e608ec56bea2301ac576551065a1ff290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "366426"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="4d619-103">Mva-satser basert på feltene grensegrunnlag og beregningsmetoder</span><span class="sxs-lookup"><span data-stu-id="4d619-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d619-104">Dette emnet beskriver hvordan verdiene i feltene Grensegrunnlag og Beregningsmetode fastslår avgiftssats(er) i salgs- og kjøpstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4d619-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="4d619-105">Grensegrunnlag på hurtigfanen Beregning på siden Mva-koder bestemmer hvilket beløp som skal brukes til å velge riktig(e) avgiftssats(er) fra satsene på siden Verdier for merverdiavgiftskode.</span><span class="sxs-lookup"><span data-stu-id="4d619-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="4d619-106">Beløpstypen i Grensegrunnlag-feltet sammen med metoden i feltet Beregningsmåte fastsetter logikken for å finne riktig(e) avgiftssats(er) for en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="4d619-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="4d619-107">Forskjellige kombinasjoner av verdier i disse feltene gir meget forskjellige mva-beregninger, slik eksemplene nedenfor viser.</span><span class="sxs-lookup"><span data-stu-id="4d619-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="4d619-108">I eksemplene brukes de samme verdiene for avgiftsintervall, som defineres for hver kode på siden Verdier for merverdiavgiftskode.</span><span class="sxs-lookup"><span data-stu-id="4d619-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="4d619-109">Åpne denne siden ved å klikke Mva-kode &gt; siden Verdier for merverdiavgiftskode.</span><span class="sxs-lookup"><span data-stu-id="4d619-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="4d619-110">Hvis grensegrunnlaget for én eller flere av merverdiavgiftskodene er basert på linjebeløp eller enheter, må verdien i feltet Beregningsmåte på siden Parameter for økonomimodul settes til Linje.</span><span class="sxs-lookup"><span data-stu-id="4d619-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="4d619-111"> Nettobeløp per linje</span><span class="sxs-lookup"><span data-stu-id="4d619-111">Net amount per line</span></span>
<span data-ttu-id="4d619-112">Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av fakturalinjenes nettobeløp, ekskludert andre avgifter.</span><span class="sxs-lookup"><span data-stu-id="4d619-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="4d619-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d619-113">Example</span></span>

<span data-ttu-id="4d619-114">Mva-kodene er angitt i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="4d619-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="4d619-115">Beløpsintervall</span><span class="sxs-lookup"><span data-stu-id="4d619-115">Amount interval</span></span>    | <span data-ttu-id="4d619-116">Avgiftssats</span><span class="sxs-lookup"><span data-stu-id="4d619-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="4d619-117">0 -  50</span><span class="sxs-lookup"><span data-stu-id="4d619-117">0 - 50</span></span>             | <span data-ttu-id="4d619-118">30 %</span><span class="sxs-lookup"><span data-stu-id="4d619-118">30%</span></span>      |
| <span data-ttu-id="4d619-119">50 -100</span><span class="sxs-lookup"><span data-stu-id="4d619-119">50 - 100</span></span>           | <span data-ttu-id="4d619-120">20 %</span><span class="sxs-lookup"><span data-stu-id="4d619-120">20%</span></span>      |
| <span data-ttu-id="4d619-121">100–0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="4d619-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="4d619-122">10 %</span><span class="sxs-lookup"><span data-stu-id="4d619-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="4d619-123">Den øvre grensen på null (0) i det siste intervallet betyr at alle beløp som er større enn 100, inkluderes i intervallet.</span><span class="sxs-lookup"><span data-stu-id="4d619-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="4d619-124">Grensegrunnlag: **Nettobeløp per linje**</span><span class="sxs-lookup"><span data-stu-id="4d619-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="4d619-125">Beregningsmetode: **Intervall**</span><span class="sxs-lookup"><span data-stu-id="4d619-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="4d619-126">Du kjøper åtte lamper som koster 25,00 per stykk.</span><span class="sxs-lookup"><span data-stu-id="4d619-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="4d619-127">Nettobeløpet for fakturalinjen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="4d619-128">Avgiften blir beregnet slik:</span><span class="sxs-lookup"><span data-stu-id="4d619-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="4d619-129">Total merverdiavgift = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00</span><span class="sxs-lookup"><span data-stu-id="4d619-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="4d619-130">Totalt fakturabeløp = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="4d619-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="4d619-131">**Variasjon**</span><span class="sxs-lookup"><span data-stu-id="4d619-131">**Variation**</span></span> 

<span data-ttu-id="4d619-132">Hvis fakturaen har to linjer med fire varer på hver linje, blir nettobeløpet på hver linje 100,00, og merverdiavgiften beregnes slik:</span><span class="sxs-lookup"><span data-stu-id="4d619-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="4d619-133">Mva-linje 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="4d619-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="4d619-134">Mva-linje 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="4d619-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="4d619-135">Total merverdiavgift = 25,00 +25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="4d619-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="4d619-136">Totalt fakturabeløp = 200,00 +50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="4d619-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="4d619-137"> Nettobeløp per enhet</span><span class="sxs-lookup"><span data-stu-id="4d619-137">Net amount per unit</span></span>
<span data-ttu-id="4d619-138">Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av verdien av hver enhet, ekskludert andre avgifter.</span><span class="sxs-lookup"><span data-stu-id="4d619-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="4d619-139">Når et enhetsbasert Grensegrunnlag er valgt, må en Enhet også angis for Mva-koden.</span><span class="sxs-lookup"><span data-stu-id="4d619-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="4d619-140">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d619-140">Example</span></span>

<span data-ttu-id="4d619-141">Mva-kodene er angitt i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="4d619-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="4d619-142">Beløp</span><span class="sxs-lookup"><span data-stu-id="4d619-142">Amount</span></span>             | <span data-ttu-id="4d619-143">Avgiftssats</span><span class="sxs-lookup"><span data-stu-id="4d619-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="4d619-144">0 -  50</span><span class="sxs-lookup"><span data-stu-id="4d619-144">0 - 50</span></span>             | <span data-ttu-id="4d619-145">30 %</span><span class="sxs-lookup"><span data-stu-id="4d619-145">30%</span></span>      |
| <span data-ttu-id="4d619-146">50 -100</span><span class="sxs-lookup"><span data-stu-id="4d619-146">50 - 100</span></span>           | <span data-ttu-id="4d619-147">20 %</span><span class="sxs-lookup"><span data-stu-id="4d619-147">20%</span></span>      |
| <span data-ttu-id="4d619-148">100–0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="4d619-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="4d619-149">10 %</span><span class="sxs-lookup"><span data-stu-id="4d619-149">10%</span></span>      |

<span data-ttu-id="4d619-150">Grensegrunnlag: **Nettobeløp per enhet**</span><span class="sxs-lookup"><span data-stu-id="4d619-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="4d619-151">Beregningsmetode: **Hele beløp**</span><span class="sxs-lookup"><span data-stu-id="4d619-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="4d619-152">Du kjøper åtte lamper som koster 25,00 per stykk.</span><span class="sxs-lookup"><span data-stu-id="4d619-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="4d619-153">Nettobeløpet for fakturalinjen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="4d619-154">Mva beregnes på følgende måte: Merverdiavgift per enhet = 25,00 x 30 % = 7,50 Total merverdiavgift = 7,50 x 8 enheter = 60,00 Totalt fakturabeløp = 200,00 + 60,00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="4d619-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="4d619-155"> Nettobeløp på fakturasaldo</span><span class="sxs-lookup"><span data-stu-id="4d619-155">Net amount of invoice balance</span></span>

<span data-ttu-id="4d619-156">Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av fakturaens totalverdi, ekskludert andre avgifter.</span><span class="sxs-lookup"><span data-stu-id="4d619-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="4d619-157">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d619-157">Example</span></span>

<span data-ttu-id="4d619-158">Mva-kodene er angitt i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="4d619-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="4d619-159">Beløp</span><span class="sxs-lookup"><span data-stu-id="4d619-159">Amount</span></span>            | <span data-ttu-id="4d619-160">Avgiftssats</span><span class="sxs-lookup"><span data-stu-id="4d619-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="4d619-161">0 -  50</span><span class="sxs-lookup"><span data-stu-id="4d619-161">0 - 50</span></span>            | <span data-ttu-id="4d619-162">30 %</span><span class="sxs-lookup"><span data-stu-id="4d619-162">30%</span></span>      |
| <span data-ttu-id="4d619-163">50 -100</span><span class="sxs-lookup"><span data-stu-id="4d619-163">50 - 100</span></span>          | <span data-ttu-id="4d619-164">20 %</span><span class="sxs-lookup"><span data-stu-id="4d619-164">20%</span></span>      |
| <span data-ttu-id="4d619-165">100–0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="4d619-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="4d619-166">10 %</span><span class="sxs-lookup"><span data-stu-id="4d619-166">10%</span></span>      |

<span data-ttu-id="4d619-167">Grensegrunnlag: **Nettobeløp på fakturasaldo**</span><span class="sxs-lookup"><span data-stu-id="4d619-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="4d619-168">Beregningsmetode: **Intervall** En salgsfaktura har to linjer med fire lamper på hver linje for 25,00 per stykk.</span><span class="sxs-lookup"><span data-stu-id="4d619-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="4d619-169">Nettobeløpet på fakturasaldo er 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="4d619-170">Mva beregnes på følgende måte: Total merverdiavgift = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Totalt fakturabeløp = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="4d619-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="4d619-171"> Bruttobeløp per linje</span><span class="sxs-lookup"><span data-stu-id="4d619-171">Gross amount per line</span></span>

<span data-ttu-id="4d619-172">Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av verdien på linjen inkludert alle andre avgifter for linjen.</span><span class="sxs-lookup"><span data-stu-id="4d619-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="4d619-173">I en mva-gruppe kan du bare ha én mva-kode med dette valget i Grensegrunnlag-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d619-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="4d619-174">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d619-174">Example</span></span>

<span data-ttu-id="4d619-175">Mva-kodene er angitt i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="4d619-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="4d619-176">Beløp</span><span class="sxs-lookup"><span data-stu-id="4d619-176">Amount</span></span>             | <span data-ttu-id="4d619-177">Avgiftssats</span><span class="sxs-lookup"><span data-stu-id="4d619-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="4d619-178">0 -  50</span><span class="sxs-lookup"><span data-stu-id="4d619-178">0 - 50</span></span>             | <span data-ttu-id="4d619-179">30 %</span><span class="sxs-lookup"><span data-stu-id="4d619-179">30%</span></span>      |
| <span data-ttu-id="4d619-180">50 -100</span><span class="sxs-lookup"><span data-stu-id="4d619-180">50 - 100</span></span>           | <span data-ttu-id="4d619-181">20 %</span><span class="sxs-lookup"><span data-stu-id="4d619-181">20%</span></span>      |
| <span data-ttu-id="4d619-182">100–0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="4d619-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="4d619-183">10 %</span><span class="sxs-lookup"><span data-stu-id="4d619-183">10%</span></span>      |

<span data-ttu-id="4d619-184">Grensegrunnlag: **Bruttobeløp per linje** Beregningsmetode: **Intervall** I tillegg er en annen kode beregnet for en spesialavgift på 5,00 for hver lampe.</span><span class="sxs-lookup"><span data-stu-id="4d619-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="4d619-185">Avgiften blir lagt til nettobeløpet før beregningen av merverdiavgiften.</span><span class="sxs-lookup"><span data-stu-id="4d619-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="4d619-186">Du kjøper åtte lamper som koster 25,00 per stykk.</span><span class="sxs-lookup"><span data-stu-id="4d619-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="4d619-187">Nettobeløpet for fakturalinjen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="4d619-188">Bruttobeløpet på fakturalinjen er 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="4d619-189">Mva beregnes på følgende måte: Total merverdiavgift = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="4d619-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="4d619-190">**Variasjon**</span><span class="sxs-lookup"><span data-stu-id="4d619-190">**Variation**</span></span> 

<span data-ttu-id="4d619-191">Hvis fakturaen er opprettet med to fakturalinjer med fire varer på hver linje, blir nettobeløpet per fakturalinje 100,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="4d619-192">Bruttobeløpet (inkludert avgiften på 4 x 5,00) per fakturalinje blir 120,00, og merverdiavgiften er opprettet på følgende måte: Mva-fakturalinje 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Mva-fakturalinje 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Total merverdiavgift = 27,00 + 27,00 = 54,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="4d619-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="4d619-193"> Bruttobeløp per enhet</span><span class="sxs-lookup"><span data-stu-id="4d619-193">Gross amount per unit</span></span>

<span data-ttu-id="4d619-194">Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av verdien av enheten inkludert andre avgifter.</span><span class="sxs-lookup"><span data-stu-id="4d619-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="4d619-195">I en mva-gruppe kan du bare ha én mva-kode med dette valget i Grensegrunnlag-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d619-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="4d619-196">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d619-196">Example</span></span>

<span data-ttu-id="4d619-197">Mva-kodene er angitt i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="4d619-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="4d619-198">Beløp</span><span class="sxs-lookup"><span data-stu-id="4d619-198">Amount</span></span>             | <span data-ttu-id="4d619-199">Avgiftssats</span><span class="sxs-lookup"><span data-stu-id="4d619-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="4d619-200">0 -  50</span><span class="sxs-lookup"><span data-stu-id="4d619-200">0 - 50</span></span>             | <span data-ttu-id="4d619-201">30 %</span><span class="sxs-lookup"><span data-stu-id="4d619-201">30%</span></span>      |
| <span data-ttu-id="4d619-202">50 -100</span><span class="sxs-lookup"><span data-stu-id="4d619-202">50 - 100</span></span>           | <span data-ttu-id="4d619-203">20 %</span><span class="sxs-lookup"><span data-stu-id="4d619-203">20%</span></span>      |
| <span data-ttu-id="4d619-204">100–0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="4d619-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="4d619-205">10 %</span><span class="sxs-lookup"><span data-stu-id="4d619-205">10%</span></span>      |

<span data-ttu-id="4d619-206">Grensegrunnlag: **Bruttobeløpet per enhet** Det er en spesialavgift på 5,00 for hver lampe.</span><span class="sxs-lookup"><span data-stu-id="4d619-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="4d619-207">Avgiften blir lagt til nettobeløpet før beregningen av merverdiavgiften.</span><span class="sxs-lookup"><span data-stu-id="4d619-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="4d619-208">Du kjøper åtte lamper som koster 25,00 per stykk.</span><span class="sxs-lookup"><span data-stu-id="4d619-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="4d619-209">Bruttobeløpet per enhet er 30,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="4d619-210">Mva beregnes på følgende måte: Merverdiavgift per enhet = 30 x 30 % = 9,00 Total salgsavgift = 9,00 x 8 = 72,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="4d619-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="4d619-211"> Fakturatotal inkl. andre mva-beløp</span><span class="sxs-lookup"><span data-stu-id="4d619-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="4d619-212">Velg dette alternativet for å fastsette merverdiavgiftssatser på grunnlag av fakturaens totalverdi, inkludert andre avgifter.</span><span class="sxs-lookup"><span data-stu-id="4d619-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="4d619-213">I en mva-gruppe kan du bare ha én mva-kode med dette valget i Grensegrunnlag-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d619-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="4d619-214">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4d619-214">Example</span></span>

<span data-ttu-id="4d619-215">Mva-kodene er angitt i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="4d619-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="4d619-216">Beløp</span><span class="sxs-lookup"><span data-stu-id="4d619-216">Amount</span></span>             | <span data-ttu-id="4d619-217">Avgiftssats</span><span class="sxs-lookup"><span data-stu-id="4d619-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="4d619-218">0 -  50</span><span class="sxs-lookup"><span data-stu-id="4d619-218">0 - 50</span></span>             | <span data-ttu-id="4d619-219">30 %</span><span class="sxs-lookup"><span data-stu-id="4d619-219">30%</span></span>      |
| <span data-ttu-id="4d619-220">50 -100</span><span class="sxs-lookup"><span data-stu-id="4d619-220">50 - 100</span></span>           | <span data-ttu-id="4d619-221">20 %</span><span class="sxs-lookup"><span data-stu-id="4d619-221">20%</span></span>      |
| <span data-ttu-id="4d619-222">100–0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="4d619-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="4d619-223">10 %</span><span class="sxs-lookup"><span data-stu-id="4d619-223">10%</span></span>      |

<span data-ttu-id="4d619-224">Grensegrunnlag: **Fakturatotal inkl. andre mva-beløp** Beregningsmetode: **Intervall** </span><span class="sxs-lookup"><span data-stu-id="4d619-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="4d619-225">Det er en spesialavgift på 5,00 for hver lampe.</span><span class="sxs-lookup"><span data-stu-id="4d619-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="4d619-226">Avgiften blir lagt til nettobeløpet før beregningen av merverdiavgiften.</span><span class="sxs-lookup"><span data-stu-id="4d619-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="4d619-227">Du kjøper åtte lamper som koster 25,00 per stykk.</span><span class="sxs-lookup"><span data-stu-id="4d619-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="4d619-228">Nettobeløpet for fakturaen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="4d619-229">Bruttobeløpet på fakturaen er 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="4d619-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="4d619-230">Mva beregnes på følgende måte: Total merverdiavgift = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Total avgift = 5,00 x 8 = 40,00 Totalt fakturabeløp = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="4d619-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="4d619-231">For mer informasjon, se [Alternativer for beregning av hele beløp og intervall for mva-koder](whole-amount-interval-options-sales-tax-codes.md) og [Beregningsmetoder for merverdiavgift i Opprinnelse-feltet](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="4d619-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



