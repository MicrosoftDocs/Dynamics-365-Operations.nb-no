---
title: "Beregningsmåter av merverdiavgift i grunnlagsfeltet"
description: "Denne artikkelen beskriver alternativene i Opprinnelse-feltet på siden for mva-koder, og hvordan mva beregnes basert på det valgte alternativet for en mva-kode."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4c1e1a588e07b9f60880dcf1c34139c5c1ceba35
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="e08d0-103">Beregningsmåter av merverdiavgift i grunnlagsfeltet</span><span class="sxs-lookup"><span data-stu-id="e08d0-103">Sales tax calculation methods in the Origin field</span></span>

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

<span data-ttu-id="e08d0-104">Denne artikkelen beskriver alternativene i Opprinnelse-feltet på siden for mva-koder, og hvordan mva beregnes basert på det valgte alternativet for en mva-kode.</span><span class="sxs-lookup"><span data-stu-id="e08d0-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="e08d0-105">For hver mva-kode du oppretter på siden Mva-koder, må du velge beregningsmåten som skal brukes for grunnlagsbeløpet for merverdiavgift i grunnlagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="e08d0-106">Prosent av nettobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-106">Percentage of net amount</span></span>
<span data-ttu-id="e08d0-107">Beregningsmåten Prosent av nettobeløp er standardverdien i grunnlagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="e08d0-108">Merverdiavgiften beregnes som en prosent av innkjøps- eller salgsbeløpet, minus eventuell merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="e08d0-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="e08d0-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e08d0-109">Example</span></span>

<span data-ttu-id="e08d0-110">Avgiftssatsen er 25 %.</span><span class="sxs-lookup"><span data-stu-id="e08d0-110">The tax rate is 25%.</span></span> <span data-ttu-id="e08d0-111">Fakturalinjen viser et antall på 10 varer til 1,00 krone hver, og kunden får 10 % linjerabatt.</span><span class="sxs-lookup"><span data-stu-id="e08d0-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="e08d0-112">Nettobeløp: (10 x 1,00)-10% = 9,00 merverdiavgift: 9,00 x 25% = 2,25 totalbeløp: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="e08d0-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="e08d0-113">Prosent av bruttobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-113">Percentage of gross amount</span></span>
<span data-ttu-id="e08d0-114">Hvis du velger metoden Prosent av bruttobeløp, beregnes merverdiavgift som en prosent av bruttosalgsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="e08d0-115">Bruttobeløpet er nettolinjebeløpet pluss alle skatter og avgifter for linjen unntatt én avgift med opprinnelse = prosent av bruttobeløp.</span><span class="sxs-lookup"><span data-stu-id="e08d0-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="e08d0-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e08d0-116">Example</span></span>

<span data-ttu-id="e08d0-117">Skattemyndighetene har innført spesielle avgifter på en vare.</span><span class="sxs-lookup"><span data-stu-id="e08d0-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="e08d0-118">Avgiftsbeløpene legges til nettobeløpet før merverdiavgift beregnes.</span><span class="sxs-lookup"><span data-stu-id="e08d0-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="e08d0-119">Gitt følgende mva-koder:</span><span class="sxs-lookup"><span data-stu-id="e08d0-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="e08d0-120">AVGIFT 1 = 10%, ved bruk av beregningsmåten prosent av nettobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="e08d0-121">AVGIFT 2 = 20%, ved bruk av beregningsmåten prosent av nettobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="e08d0-122">MERVERDIAVGIFT = 25%, ved bruk av beregningsmåten prosent av bruttobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="e08d0-123">Hvis nettobeløpet er 10,00, er AVGIFT 1 1,00 (10,00 x 10%) og AVGIFT 2 = 2,00 (10,00 x 20%).</span><span class="sxs-lookup"><span data-stu-id="e08d0-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="e08d0-124">Beløpene er som følger: bruttobeløp: nettobeløp + AVGIFT 1 beløp AVGIFT 2 beløp (10,00 + 1,00 + 2,00) = 13,00 MERVERDIAVGIFT = 13,00 x 25% = 3,25 Total AVGIFT og MERVERDIAVGIFT: 1,00 + 2,00 + 3,25 = 6,25 totalbeløp: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="e08d0-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="e08d0-125">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="e08d0-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08d0-126">Bare én avgiftskode med opprinnelse = prosenten av bruttobeløpet kan brukes for en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="e08d0-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="e08d0-127">Hvis mer enn én eller slik avgiftskode bestemmes for en transaksjon, vises en feil om at merverdiavgift ikke kan beregnes.</span><span class="sxs-lookup"><span data-stu-id="e08d0-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="e08d0-128">Prosent av merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="e08d0-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="e08d0-129">Når du velger prosent av merverdiavgift i grunnlagsfeltet, beregnes merverdiavgift som en prosent av merverdiavgiften som er valgt i feltet Merverdiavgift på merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="e08d0-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="e08d0-130">Merverdiavgiften som er valgt i feltet Merverdiavgift på merverdiavgift, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="e08d0-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="e08d0-131">Den andre merverdiavgiften beregnes deretter basert på det første mva-beløpet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="e08d0-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e08d0-132">Example</span></span>

<span data-ttu-id="e08d0-133">Gitt følgende mva-koder:</span><span class="sxs-lookup"><span data-stu-id="e08d0-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="e08d0-134">AVGIFT 1 = 10%, ved bruk av beregningsmåten prosent av nettobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="e08d0-135">AVGIFT 2 = 20%, ved bruk av metoden Prosent av merverdiavgift, med Avgift 1 i feltet Merverdiavgift på merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="e08d0-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="e08d0-136">MERVERDIAVGIFT 1 = 25%, ved bruk av metoden prosent av bruttobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="e08d0-137">Nettobeløp: 10,00 AVGIFT 1: 10,00 x 10% = 1,00 AVGIFT 2: 1,00 x 20% = 0,20 bruttobeløp: 10,00 + 1,00 + 0,20 = 11,20 MERVERDIAVGIFT: 11,20 x 25% = 2,80 total AVGIFT og MERVERDIAVGIFT: 1,00 + 0,20 + 2,80 = 4,00 totalbeløp: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="e08d0-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="e08d0-138">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="e08d0-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08d0-139">Mva-beregninger med flere nivåer er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="e08d0-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="e08d0-140">En avgift kan ikke beregnes basert på en avgift som allerede er beregnet basert på en annen avgift.</span><span class="sxs-lookup"><span data-stu-id="e08d0-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="e08d0-141">Flere mva på mva-koder på enkeltnivå kan beregnes på en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="e08d0-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="e08d0-142">Beløp per enhet</span><span class="sxs-lookup"><span data-stu-id="e08d0-142">Amount per unit</span></span>
<span data-ttu-id="e08d0-143">Når du velger Beløp per enhet i grunnlagsfeltet, beregnes merverdiavgift som et fast beløp per enhet ganget med antallet på dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="e08d0-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="e08d0-144">En enhet må velges i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="e08d0-145">Beløpet per enhet angis på siden Verdier for merverdiavgiftskode.</span><span class="sxs-lookup"><span data-stu-id="e08d0-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="e08d0-146">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e08d0-146">Example</span></span>

<span data-ttu-id="e08d0-147">Mva-koden er definert som: USD 1,20 per enhet = boks på en salgsfakturalinje 25 bokser for en vare selges Mva-sats beregnes som 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="e08d0-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="e08d0-148">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="e08d0-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08d0-149">Hvis transaksjonen angis i en annen enhet enn enheten som er angitt i mva-koden, omregnes den automatisk basert på enhetsomregningene som er angitt på Enhetsomregninger-siden.</span><span class="sxs-lookup"><span data-stu-id="e08d0-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="e08d0-150">Beløp per enhet, tilleggsalternativ</span><span class="sxs-lookup"><span data-stu-id="e08d0-150">Amount per unit, additional option</span></span>

<span data-ttu-id="e08d0-151">I kategorien Beregning kan du velge om et beløp per enhet beregnet mva beregnes før andre mva-koder og legges til nettobeløpet før andre mva-koder med opprinnelse = prosent av nettobeløp beregnes.</span><span class="sxs-lookup"><span data-stu-id="e08d0-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="e08d0-152">Eksempler</span><span class="sxs-lookup"><span data-stu-id="e08d0-152">Examples</span></span>

<span data-ttu-id="e08d0-153">Anta at vi beregner 2 avgiftskoder i en transaksjon:</span><span class="sxs-lookup"><span data-stu-id="e08d0-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="e08d0-154">AVGIFT: Opprinnelse = beløp per enhet og en merverdiavgift, verdien er satt til 5,00 per enhet = stk.</span><span class="sxs-lookup"><span data-stu-id="e08d0-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="e08d0-155">MERVERVIDAVGIFT: Opprinnelse = som vist i eksemplene nedenfor, settes verdien til 25%</span><span class="sxs-lookup"><span data-stu-id="e08d0-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="e08d0-156">Vi selger 1 stykk av en vare til en enhetspris på 10,00</span><span class="sxs-lookup"><span data-stu-id="e08d0-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="e08d0-157">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="e08d0-157">Example 1</span></span>

<span data-ttu-id="e08d0-158">MERVERVIDAVGIFT: Opprinnelse = metoden prosent av bruttobeløp, alternativet Beregn før merverdiavgift har ingen innvirkning fordi MERVERVIDAVGIFT beregnes som en prosent av bruttobeløpet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="e08d0-159">AVGIFT: 1 x 5,00 = 5,00 bruttobeløp: 10,00 + 5,00 = 15,00 MERVERVIDAVGIFT: 15,00 x 25% = 3.75 total merverdiavgift: 5,00 + 3,75 = 8,75 totalbeløp: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="e08d0-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="e08d0-160">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="e08d0-160">Example 2</span></span>

<span data-ttu-id="e08d0-161">MERVERVIDAVGIFT: Opprinnelse = prosent av nettobeløp, alternativet Beregn før merverdiavgift er ikke valgt for avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="e08d0-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="e08d0-162">Nettobeløp: 10,00 AVGIFT: 1 x 5,00 = 5,00 MERVERVIDAVGIFT: 10,00 x 25% = 2,50 Total merverdiavgift: 5,00 + 2,50 = 7,50 Totalbeløp: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="e08d0-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="e08d0-163">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="e08d0-163">Example 3</span></span>

<span data-ttu-id="e08d0-164">MERVERVIDAVGIFT = Opprinnelse = prosent av nettobeløp, alternativet Beregn før merverdiavgift er valgt for avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="e08d0-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="e08d0-165">Nettobeløp: 10,00 AVGIFT: 1 x 5,00 = 5,00 MERVERVIDAVGIFT: (10,00 + 5,00) x 25% = 3,75 Total merverdiavgift: 5,00 + 3,75 = 8,75 Totalbeløp: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="e08d0-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="e08d0-166">Eksempel 4</span><span class="sxs-lookup"><span data-stu-id="e08d0-166">Example 4</span></span>

<span data-ttu-id="e08d0-167">Resultatet i eksempel 3 og 1 er det samme fordi det bare er én avgift.</span><span class="sxs-lookup"><span data-stu-id="e08d0-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="e08d0-168">Anta at du har to avgifter, og bare én av dem er inkludert i nettobeløpet for mva-beregningen: AVGIFT 1: 5,00, med samme beløp per enhet-metode og alternativet Beregn før merverdiavgift er valgt AVGIFT 2: 2,50, med beløp per enhet-metoden og alternativet Beregn før merverdiavgift ikke er valgt Merverdiavgift : 25%, med metoden Prosent av nettobeløp Nettobeløp: 10,00 AVGIFT 1: 1 x 5,00 = 5,00 AVGIFT 2: 1 x 2,50 = 2,50 Nettobeløpet er mva-pliktig: 10,00 + 5,00 = 15,00 MERVERDIAVGIFT: 15,00 x 25% = 3.75 Total merverdiavgift, inkludert avgifter: 5,00 + 2,50 + 3,75 = 11,25 Totalbeløp: 10,00 + 11,25 = 21,25 MERVERDIAVGIFT på 25% beregnes for summen av nettobeløpet (10,00) + AVGIFT 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="e08d0-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="e08d0-169">AVGIFT 2 legges til avgiftsbeløpet etter at merverdiavgiften er beregnet.</span><span class="sxs-lookup"><span data-stu-id="e08d0-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="e08d0-170">Beregnet prosent av nettobeløp</span><span class="sxs-lookup"><span data-stu-id="e08d0-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="e08d0-171">Beregnet prosent av nettobeløp håndterer avgiftsberegning forskjellig, avhengig av innstillingen for parameteren Beløp inkludert merverdiavgift for bilaget eller journalen.</span><span class="sxs-lookup"><span data-stu-id="e08d0-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="e08d0-172">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="e08d0-172">Example 1</span></span>

<span data-ttu-id="e08d0-173">Dokumentet / journalen er satt til Beløp inkludert merverdiavgift = Ja Transaksjonslinjebeløp: 10,00 Avgiftssats: 25% Merverdiavgift: Transaksjonslinjebeløp x avgiftssats (10,00 x 25%) = 2,50 Avgiftsgrunnlagsbeløp (opprinnelig beløp): Transaksjonslinjebeløp - Merverdiavgift (10,00 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="e08d0-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="e08d0-174">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="e08d0-174">Example 2</span></span>

<span data-ttu-id="e08d0-175">Dokumentet / journalen er satt til Beløp inkludert merverdiavgift = Nei Transaksjonslinjebeløp: 10,00 Avgiftssats: 25% Merverdiavgift: (Transaksjonslinjebeløp x avgiftssats) / (100 - avgiftssats) (10,00 x 25%) / (100% - 25%) = 3,33 Avgiftsgrunnlagsbeløp (opprinnelig beløp): Transaksjonslinjebeløp = 10,00</span><span class="sxs-lookup"><span data-stu-id="e08d0-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="see-also"></a><span data-ttu-id="e08d0-176">Se også</span><span class="sxs-lookup"><span data-stu-id="e08d0-176">See also</span></span>
--------

[<span data-ttu-id="e08d0-177">Bestemme mva-satser basert på feltene Grensegrunnlag og Beregningsmåte</span><span class="sxs-lookup"><span data-stu-id="e08d0-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="e08d0-178">Hele beløp og alternativer for intervallberegning for mva-koder</span><span class="sxs-lookup"><span data-stu-id="e08d0-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




