---
title: Definere rentesatser for en rentekode
description: "Rentekoder inneholder innstillinger som bestemmer nå renter belastes og hvordan de beregnes på forfalte kontoer."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59acfaa93b1352f2be6d750dea6bdd740bac0312
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="bc255-103">Definere rentesatser for en rentekode</span><span class="sxs-lookup"><span data-stu-id="bc255-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bc255-104">Rentekoder inneholder innstillinger som bestemmer nå renter belastes og hvordan de beregnes på forfalte kontoer.</span><span class="sxs-lookup"><span data-stu-id="bc255-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="bc255-105">Du kan definere en enkelt rentekode og bruke den på flere kundeposteringsprofiler, faktureringskoder eller på bestemte fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="bc255-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="bc255-106">Når rentekodedetaljene er endret vil alle funksjonene som bruker koden implementere endringene for nye transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="bc255-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="bc255-107">For hver rentekode kan du definere to typer satser:</span><span class="sxs-lookup"><span data-stu-id="bc255-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="bc255-108">Satser for renteinntekter − Disse representerer inntekt som er tjent ved å belaste renter på fakturaer eller rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="bc255-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="bc255-109">Satser for rentebetalinger − Disse representerer en kostnad som er betalt for renter på kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="bc255-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="bc255-110">Begge disse satstypene kan eksistere på samme tid og i den samme rentekoden.</span><span class="sxs-lookup"><span data-stu-id="bc255-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="bc255-111">Rentesatser kan baseres på tre beregningstyper:</span><span class="sxs-lookup"><span data-stu-id="bc255-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="bc255-112">Rente i prosent.</span><span class="sxs-lookup"><span data-stu-id="bc255-112">Interest by percentage.</span></span>
-   <span data-ttu-id="bc255-113">Rente i beløp.</span><span class="sxs-lookup"><span data-stu-id="bc255-113">Interest by amount.</span></span>
-   <span data-ttu-id="bc255-114">Rente etter intervall, som resulterer i en enkelt prosent eller et enkelt beløp.</span><span class="sxs-lookup"><span data-stu-id="bc255-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="bc255-115">Når en rente brukes til å beregne rente, opprettes det en egen rentenota for hver rentesats som er aktiv i løpet av det tidsrommet som betalingen overskrider forfallsdatoen for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="bc255-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="bc255-116">Du bruker fanen **Inntekter** på siden **Rentekode** for å definere rentesatser for rente som får du ved å belaste rente.</span><span class="sxs-lookup"><span data-stu-id="bc255-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="bc255-117">Bruk **Betalinger**-fanen til å definere rentesatser for renter du betaler.</span><span class="sxs-lookup"><span data-stu-id="bc255-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="bc255-118">Rentesatser basert på en prosent</span><span class="sxs-lookup"><span data-stu-id="bc255-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="bc255-119">Du kan definere rentesatser som beregner en bestemt prosent.</span><span class="sxs-lookup"><span data-stu-id="bc255-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="bc255-120">Rentebeløp gjelder for alle valutaer.</span><span class="sxs-lookup"><span data-stu-id="bc255-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="bc255-121">Valgfrie rentebeløpsgrenser kan angis.</span><span class="sxs-lookup"><span data-stu-id="bc255-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="bc255-122">**Prosent** velges i **Beregn rente basert på**-feltet på siden **Definer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="bc255-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="bc255-123">For eksempel, for å definere en rentekode som setter 5 prosent rente for annenhver måned som fakturabetalingen overskrider transaksjonens forfallsdato, angir du 2 i feltet **Beregn renter hver** og velger **Måned**.</span><span class="sxs-lookup"><span data-stu-id="bc255-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="bc255-124">Rentesatser basert på beløp</span><span class="sxs-lookup"><span data-stu-id="bc255-124">Interest rates based on amounts</span></span>
<span data-ttu-id="bc255-125">Du kan definere rentesatser som beregner et bestemt beløp per valuta.</span><span class="sxs-lookup"><span data-stu-id="bc255-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="bc255-126">Et rentebeløp angis for hver valuta i rentekoden.</span><span class="sxs-lookup"><span data-stu-id="bc255-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="bc255-127">Valgfrie rentebeløpsgrenser kan angis.</span><span class="sxs-lookup"><span data-stu-id="bc255-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="bc255-128">**Beløp** velges i **Beregn rente basert på**-feltet på **Definer rentekoder**-siden.</span><span class="sxs-lookup"><span data-stu-id="bc255-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="bc255-129">For eksempel, for å definere en rentekode som setter en rente på 25,00 for hver 20. dag som fakturabetalingen overskrider transaksjonens forfallsdato, angir du 20 i feltet **Beregn renter hver** og velger **Dag**.</span><span class="sxs-lookup"><span data-stu-id="bc255-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="bc255-130">Rentesatser basert på intervaller</span><span class="sxs-lookup"><span data-stu-id="bc255-130">Interest rates based on ranges</span></span>
<span data-ttu-id="bc255-131">Du kan definere rentesatser som varierer avhengig av forfalt beløp, antall dager beløpet er forsinket eller antall måneder beløpet er forsinket.</span><span class="sxs-lookup"><span data-stu-id="bc255-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="bc255-132">Du kan bruke **Inntjening etter valuta**-fanene for å definere bestemte renteinnstillinger for hver valuta.</span><span class="sxs-lookup"><span data-stu-id="bc255-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="bc255-133">Dette er også der du definerer området.</span><span class="sxs-lookup"><span data-stu-id="bc255-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="bc255-134">Bruk **Områder**-knappen til å legge til linjer som representerer områdene som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="bc255-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="bc255-135">**Fra**-verdien representerer begynnelsen på området, og **Renteverdi**-tallet representerer en prosent eller et beløp, avhengig av valget i **Beregn rente basert på**-feltet på **Definer rentekoder**-siden.</span><span class="sxs-lookup"><span data-stu-id="bc255-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="bc255-136">Eksempel 1: Rente etter intervall = Beløp</span><span class="sxs-lookup"><span data-stu-id="bc255-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="bc255-137">Du definerer en rentekode som setter rente én gang for hver tredje måned fakturabetalingen overskrider transaksjonens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="bc255-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="bc255-138">Du vil basere beregningen på en renteverdiprosent, ifølge trinnvise beløpsintervaller.</span><span class="sxs-lookup"><span data-stu-id="bc255-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="bc255-139">Renteverdien vil være 1 prosent for fakturabeløp opptil 1 000,00, 2 prosent for beløp fra 1 001,00 til 5 000,00 og 3 prosent for beløp større enn 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="bc255-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="bc255-140">Slik definerer du verdiene i rentekodefeltene.</span><span class="sxs-lookup"><span data-stu-id="bc255-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="bc255-141">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="bc255-141">**Field name**</span></span>                  | <span data-ttu-id="bc255-142">**Feltverdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="bc255-143">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="bc255-143">**Interest code**</span></span>               | <span data-ttu-id="bc255-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="bc255-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="bc255-145">**Beregn renter hver**</span><span class="sxs-lookup"><span data-stu-id="bc255-145">**Calculate interest every**</span></span>    | <span data-ttu-id="bc255-146">3/måned</span><span class="sxs-lookup"><span data-stu-id="bc255-146">3/Month</span></span>         |
| <span data-ttu-id="bc255-147">**Rente etter intervall**</span><span class="sxs-lookup"><span data-stu-id="bc255-147">**Interest by range**</span></span>           | <span data-ttu-id="bc255-148">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc255-148">Amount</span></span>          |
| <span data-ttu-id="bc255-149">**Beregn rente basert på**</span><span class="sxs-lookup"><span data-stu-id="bc255-149">**Calculate interest based on**</span></span> | <span data-ttu-id="bc255-150">Prosent</span><span class="sxs-lookup"><span data-stu-id="bc255-150">Percentage</span></span>      |

<span data-ttu-id="bc255-151">Slik definerer du intervallinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="bc255-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="bc255-152">**Fra verdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-152">**From value**</span></span> | <span data-ttu-id="bc255-153">**Renteverdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="bc255-154">0</span><span class="sxs-lookup"><span data-stu-id="bc255-154">0</span></span>              | <span data-ttu-id="bc255-155">1</span><span class="sxs-lookup"><span data-stu-id="bc255-155">1</span></span>                  |
| <span data-ttu-id="bc255-156">1,001</span><span class="sxs-lookup"><span data-stu-id="bc255-156">1,001</span></span>          | <span data-ttu-id="bc255-157">2</span><span class="sxs-lookup"><span data-stu-id="bc255-157">2</span></span>                  |
| <span data-ttu-id="bc255-158">5,001</span><span class="sxs-lookup"><span data-stu-id="bc255-158">5,001</span></span>          | <span data-ttu-id="bc255-159">3</span><span class="sxs-lookup"><span data-stu-id="bc255-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="bc255-160">Eksempel 2: Rente etter intervall = Dager</span><span class="sxs-lookup"><span data-stu-id="bc255-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="bc255-161">Du definerer en rentekode som setter rente én gang for hver 15. dag fakturabetalingen overskrider transaksjonens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="bc255-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="bc255-162">Du vil basere beregningen på et renteverdibeløp, ifølge trinnvise dagsintervaller.</span><span class="sxs-lookup"><span data-stu-id="bc255-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="bc255-163">Renteverdien vil være 10,00 per 15 dager for de 60 første dagene, 15,00 per 15 dager fra dag 61 til 90 og 20,00 per 15 dager fra dag 91 og senere.</span><span class="sxs-lookup"><span data-stu-id="bc255-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="bc255-164">Slik definerer du verdiene i rentekodefeltene.</span><span class="sxs-lookup"><span data-stu-id="bc255-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="bc255-165">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="bc255-165">**Field name**</span></span>                  | <span data-ttu-id="bc255-166">**Feltverdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="bc255-167">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="bc255-167">**Interest code**</span></span>               | <span data-ttu-id="bc255-168">15DBelXDag</span><span class="sxs-lookup"><span data-stu-id="bc255-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="bc255-169">**Beregn renter hver**</span><span class="sxs-lookup"><span data-stu-id="bc255-169">**Calculate interest every**</span></span>    | <span data-ttu-id="bc255-170">15/dag</span><span class="sxs-lookup"><span data-stu-id="bc255-170">15/Day</span></span>          |
| <span data-ttu-id="bc255-171">**Rente etter intervall**</span><span class="sxs-lookup"><span data-stu-id="bc255-171">**Interest by range**</span></span>           | <span data-ttu-id="bc255-172">Dager</span><span class="sxs-lookup"><span data-stu-id="bc255-172">Days</span></span>            |
| <span data-ttu-id="bc255-173">**Beregn rente basert på**</span><span class="sxs-lookup"><span data-stu-id="bc255-173">**Calculate interest based on**</span></span> | <span data-ttu-id="bc255-174">Beløp</span><span class="sxs-lookup"><span data-stu-id="bc255-174">Amount</span></span>          |

<span data-ttu-id="bc255-175">Slik definerer du intervallinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="bc255-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="bc255-176">**Fra verdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-176">**From value**</span></span> | <span data-ttu-id="bc255-177">**Renteverdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="bc255-178">0</span><span class="sxs-lookup"><span data-stu-id="bc255-178">0</span></span>              | <span data-ttu-id="bc255-179">10</span><span class="sxs-lookup"><span data-stu-id="bc255-179">10</span></span>                 |
| <span data-ttu-id="bc255-180">61</span><span class="sxs-lookup"><span data-stu-id="bc255-180">61</span></span>             | <span data-ttu-id="bc255-181">15</span><span class="sxs-lookup"><span data-stu-id="bc255-181">15</span></span>                 |
| <span data-ttu-id="bc255-182">91</span><span class="sxs-lookup"><span data-stu-id="bc255-182">91</span></span>             | <span data-ttu-id="bc255-183">20</span><span class="sxs-lookup"><span data-stu-id="bc255-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="bc255-184">Eksempel 3: Rente etter intervall = Måneder</span><span class="sxs-lookup"><span data-stu-id="bc255-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="bc255-185">Du definerer en rentekode som setter rente én gang for hver måned fakturabetalingen overskrider transaksjonens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="bc255-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="bc255-186">Du vil basere beregningen på en renteverdiprosent, ifølge trinnvise månedsintervaller.</span><span class="sxs-lookup"><span data-stu-id="bc255-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="bc255-187">Renteverdien vil være 1,5 prosent per måned de første tre månedene etter forfall, 2,0 prosent per måned for de neste tre månedene og 2,5 prosent per måned for hver måned etter de første seks månedene.</span><span class="sxs-lookup"><span data-stu-id="bc255-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="bc255-188">Slik definerer du verdiene i rentekodefeltene.</span><span class="sxs-lookup"><span data-stu-id="bc255-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="bc255-189">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="bc255-189">**Field name**</span></span>                  | <span data-ttu-id="bc255-190">**Feltverdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="bc255-191">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="bc255-191">**Interest code**</span></span>               | <span data-ttu-id="bc255-192">1M%EtMnd</span><span class="sxs-lookup"><span data-stu-id="bc255-192">1M%ByMth</span></span>        |
| <span data-ttu-id="bc255-193">**Beregn renter hver**</span><span class="sxs-lookup"><span data-stu-id="bc255-193">**Calculate interest every**</span></span>    | <span data-ttu-id="bc255-194">1/måned</span><span class="sxs-lookup"><span data-stu-id="bc255-194">1/Month</span></span>         |
| <span data-ttu-id="bc255-195">**Rente etter intervall**</span><span class="sxs-lookup"><span data-stu-id="bc255-195">**Interest by range**</span></span>           | <span data-ttu-id="bc255-196">Måneder</span><span class="sxs-lookup"><span data-stu-id="bc255-196">Months</span></span>          |
| <span data-ttu-id="bc255-197">**Beregn rente basert på**</span><span class="sxs-lookup"><span data-stu-id="bc255-197">**Calculate interest based on**</span></span> | <span data-ttu-id="bc255-198">Prosent</span><span class="sxs-lookup"><span data-stu-id="bc255-198">Percentage</span></span>      |

<span data-ttu-id="bc255-199">Slik definerer du intervallinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="bc255-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="bc255-200">**Fra verdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-200">**From value**</span></span> | <span data-ttu-id="bc255-201">**Renteverdi**</span><span class="sxs-lookup"><span data-stu-id="bc255-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="bc255-202">0</span><span class="sxs-lookup"><span data-stu-id="bc255-202">0</span></span>              | <span data-ttu-id="bc255-203">1.5</span><span class="sxs-lookup"><span data-stu-id="bc255-203">1.5</span></span>                |
| <span data-ttu-id="bc255-204">4</span><span class="sxs-lookup"><span data-stu-id="bc255-204">4</span></span>              | <span data-ttu-id="bc255-205">2</span><span class="sxs-lookup"><span data-stu-id="bc255-205">2</span></span>                  |
| <span data-ttu-id="bc255-206">7</span><span class="sxs-lookup"><span data-stu-id="bc255-206">7</span></span>              | <span data-ttu-id="bc255-207">2,5</span><span class="sxs-lookup"><span data-stu-id="bc255-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="bc255-208">Nye versjoner</span><span class="sxs-lookup"><span data-stu-id="bc255-208">New versions</span></span>
<span data-ttu-id="bc255-209">Rentekoder har gyldighet fra en dato.</span><span class="sxs-lookup"><span data-stu-id="bc255-209">Interest codes are date effective.</span></span> <span data-ttu-id="bc255-210">Hvis du vil endre rentesatsen, kan du opprette en **ny versjon** som gjelder fra og med en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="bc255-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="bc255-211">For å vise forskjellige versjoner, kan du bruke **Per dato**-menyvalget for å velge fristen.</span><span class="sxs-lookup"><span data-stu-id="bc255-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="bc255-212">Du kan også velge **Vis alle poster** for å vise alle rentekoder på siden.</span><span class="sxs-lookup"><span data-stu-id="bc255-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




