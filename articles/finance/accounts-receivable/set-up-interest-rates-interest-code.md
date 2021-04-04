---
title: Definere rentesatser for en rentekode
description: Rentekoder inneholder innstillinger som bestemmer nå renter belastes og hvordan de beregnes på forfalte kontoer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d9ff856e34eb894c5d0ab5fe17c8e95f62fff57
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555371"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="4f7b5-103">Definere rentesatser for en rentekode</span><span class="sxs-lookup"><span data-stu-id="4f7b5-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f7b5-104">Rentekoder inneholder innstillinger som bestemmer nå renter belastes og hvordan de beregnes på forfalte kontoer.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="4f7b5-105">Du kan definere en enkelt rentekode og bruke den på flere kundeposteringsprofiler, faktureringskoder eller på bestemte fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="4f7b5-106">Når rentekodedetaljene er endret vil alle funksjonene som bruker koden implementere endringene for nye transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="4f7b5-107">For hver rentekode kan du definere to typer satser:</span><span class="sxs-lookup"><span data-stu-id="4f7b5-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="4f7b5-108">Satser for renteinntekter − Disse representerer inntekt som er tjent ved å belaste renter på fakturaer eller rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="4f7b5-109">Satser for rentebetalinger − Disse representerer en kostnad som er betalt for renter på kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="4f7b5-110">Begge disse satstypene kan eksistere på samme tid og i den samme rentekoden.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="4f7b5-111">Rentesatser kan baseres på tre beregningstyper:</span><span class="sxs-lookup"><span data-stu-id="4f7b5-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="4f7b5-112">Rente i prosent.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-112">Interest by percentage.</span></span>
-   <span data-ttu-id="4f7b5-113">Rente i beløp.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-113">Interest by amount.</span></span>
-   <span data-ttu-id="4f7b5-114">Rente etter intervall, som resulterer i en enkelt prosent eller et enkelt beløp.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="4f7b5-115">Når en rente brukes til å beregne rente, opprettes det en egen rentenota for hver rentesats som er aktiv i løpet av det tidsrommet som betalingen overskrider forfallsdatoen for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="4f7b5-116">Du bruker fanen **Inntekter** på siden **Rentekode** for å definere rentesatser for rente som får du ved å belaste rente.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="4f7b5-117">Bruk **Betalinger**-fanen til å definere rentesatser for renter du betaler.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="4f7b5-118">Rentesatser basert på en prosent</span><span class="sxs-lookup"><span data-stu-id="4f7b5-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="4f7b5-119">Du kan definere rentesatser som beregner en bestemt prosent.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="4f7b5-120">Rentebeløp gjelder for alle valutaer.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="4f7b5-121">Valgfrie rentebeløpsgrenser kan angis.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="4f7b5-122">**Prosent** velges i feltet **Beregn rente basert på** på siden **Definer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="4f7b5-123">For eksempel, for å definere en rentekode som setter 5 prosent rente for annenhver måned som fakturabetalingen overskrider transaksjonens forfallsdato, angir du 2 i feltet **Beregn renter hver** og velger **Måned**.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="4f7b5-124">Den nye algoritmen for rentenotaberegning legges til ved hjelp av Funksjonsstyring.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="4f7b5-125">For å bruke denne algoritmen, aktiverer du funksjonen **(GBL) Tillat å beregne rente per dag som årlig prosent delt på 365**.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="4f7b5-126">Hvis du vil ha informasjon om hvordan du aktiverer funksjonen, kan du se [Oversikt over funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f7b5-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="4f7b5-127">Formelen for beregningen for rentenotabeløpet er:</span><span class="sxs-lookup"><span data-stu-id="4f7b5-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="4f7b5-128">Rentenotabeløp = Beløp skyldig \* Årlig rente % / 365 \* Antall dager forsinket</span><span class="sxs-lookup"><span data-stu-id="4f7b5-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="4f7b5-129">Denne funksjonen er tilgjengelig i versjon 10.0.18 eller senere.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="4f7b5-130">Rentesatser basert på beløp</span><span class="sxs-lookup"><span data-stu-id="4f7b5-130">Interest rates based on amounts</span></span>
<span data-ttu-id="4f7b5-131">Du kan definere rentesatser som beregner et bestemt beløp per valuta.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="4f7b5-132">Et rentebeløp angis for hver valuta i rentekoden.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="4f7b5-133">Valgfrie rentebeløpsgrenser kan angis.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="4f7b5-134">**Beløp** velges i **Beregn rente basert på**-feltet på **Definer rentekoder**-siden.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="4f7b5-135">For eksempel, for å definere en rentekode som setter en rente på 25,00 for hver 20. dag som fakturabetalingen overskrider transaksjonens forfallsdato, angir du 20 i feltet **Beregn renter hver** og velger **Dag**.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="4f7b5-136">Rentesatser basert på intervaller</span><span class="sxs-lookup"><span data-stu-id="4f7b5-136">Interest rates based on ranges</span></span>
<span data-ttu-id="4f7b5-137">Du kan definere rentesatser som varierer avhengig av forfalt beløp, antall dager beløpet er forsinket eller antall måneder beløpet er forsinket.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="4f7b5-138">Du kan bruke **Inntjening etter valuta**-fanene for å definere bestemte renteinnstillinger for hver valuta.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="4f7b5-139">Dette er også der du definerer området.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="4f7b5-140">Bruk **Områder**-knappen til å legge til linjer som representerer områdene som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="4f7b5-141">**Fra**-verdien representerer begynnelsen på området, og **Renteverdi**-tallet representerer en prosent eller et beløp, avhengig av valget i **Beregn rente basert på**-feltet på **Definer rentekoder**-siden.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="4f7b5-142">Eksempel 1: Rente etter intervall = Beløp</span><span class="sxs-lookup"><span data-stu-id="4f7b5-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="4f7b5-143">Du definerer en rentekode som setter rente én gang for hver tredje måned fakturabetalingen overskrider transaksjonens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="4f7b5-144">Du vil basere beregningen på en renteverdiprosent, ifølge trinnvise beløpsintervaller.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="4f7b5-145">Renteverdien vil være 1 prosent for fakturabeløp opptil 1 000,00, 2 prosent for beløp fra 1 001,00 til 5 000,00 og 3 prosent for beløp større enn 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="4f7b5-146">Slik definerer du verdiene i rentekodefeltene.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="4f7b5-147">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-147">**Field name**</span></span>                  | <span data-ttu-id="4f7b5-148">**Feltverdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="4f7b5-149">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-149">**Interest code**</span></span>               | <span data-ttu-id="4f7b5-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="4f7b5-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="4f7b5-151">**Beregn renter hver**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-151">**Calculate interest every**</span></span>    | <span data-ttu-id="4f7b5-152">3/måned</span><span class="sxs-lookup"><span data-stu-id="4f7b5-152">3/Month</span></span>         |
| <span data-ttu-id="4f7b5-153">**Rente etter intervall**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-153">**Interest by range**</span></span>           | <span data-ttu-id="4f7b5-154">Beløp</span><span class="sxs-lookup"><span data-stu-id="4f7b5-154">Amount</span></span>          |
| <span data-ttu-id="4f7b5-155">**Beregn rente basert på**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-155">**Calculate interest based on**</span></span> | <span data-ttu-id="4f7b5-156">Prosent</span><span class="sxs-lookup"><span data-stu-id="4f7b5-156">Percentage</span></span>      |

<span data-ttu-id="4f7b5-157">Slik definerer du intervallinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="4f7b5-158">**Fra verdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-158">**From value**</span></span> | <span data-ttu-id="4f7b5-159">**Renteverdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="4f7b5-160">0</span><span class="sxs-lookup"><span data-stu-id="4f7b5-160">0</span></span>              | <span data-ttu-id="4f7b5-161">1</span><span class="sxs-lookup"><span data-stu-id="4f7b5-161">1</span></span>                  |
| <span data-ttu-id="4f7b5-162">1,001</span><span class="sxs-lookup"><span data-stu-id="4f7b5-162">1,001</span></span>          | <span data-ttu-id="4f7b5-163">2</span><span class="sxs-lookup"><span data-stu-id="4f7b5-163">2</span></span>                  |
| <span data-ttu-id="4f7b5-164">5,001</span><span class="sxs-lookup"><span data-stu-id="4f7b5-164">5,001</span></span>          | <span data-ttu-id="4f7b5-165">3</span><span class="sxs-lookup"><span data-stu-id="4f7b5-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="4f7b5-166">Eksempel 2: Rente etter intervall = Dager</span><span class="sxs-lookup"><span data-stu-id="4f7b5-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="4f7b5-167">Du definerer en rentekode som setter rente én gang for hver 15. dag fakturabetalingen overskrider transaksjonens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="4f7b5-168">Du vil basere beregningen på et renteverdibeløp, ifølge trinnvise dagsintervaller.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="4f7b5-169">Renteverdien vil være 10,00 per 15 dager for de 60 første dagene, 15,00 per 15 dager fra dag 61 til 90 og 20,00 per 15 dager fra dag 91 og senere.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="4f7b5-170">Slik definerer du verdiene i rentekodefeltene.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="4f7b5-171">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-171">**Field name**</span></span>                  | <span data-ttu-id="4f7b5-172">**Feltverdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="4f7b5-173">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-173">**Interest code**</span></span>               | <span data-ttu-id="4f7b5-174">15DBelXDag</span><span class="sxs-lookup"><span data-stu-id="4f7b5-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="4f7b5-175">**Beregn renter hver**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-175">**Calculate interest every**</span></span>    | <span data-ttu-id="4f7b5-176">15/dag</span><span class="sxs-lookup"><span data-stu-id="4f7b5-176">15/Day</span></span>          |
| <span data-ttu-id="4f7b5-177">**Rente etter intervall**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-177">**Interest by range**</span></span>           | <span data-ttu-id="4f7b5-178">Dager</span><span class="sxs-lookup"><span data-stu-id="4f7b5-178">Days</span></span>            |
| <span data-ttu-id="4f7b5-179">**Beregn rente basert på**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-179">**Calculate interest based on**</span></span> | <span data-ttu-id="4f7b5-180">Beløp</span><span class="sxs-lookup"><span data-stu-id="4f7b5-180">Amount</span></span>          |

<span data-ttu-id="4f7b5-181">Slik definerer du intervallinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="4f7b5-182">**Fra verdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-182">**From value**</span></span> | <span data-ttu-id="4f7b5-183">**Renteverdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="4f7b5-184">0</span><span class="sxs-lookup"><span data-stu-id="4f7b5-184">0</span></span>              | <span data-ttu-id="4f7b5-185">10</span><span class="sxs-lookup"><span data-stu-id="4f7b5-185">10</span></span>                 |
| <span data-ttu-id="4f7b5-186">61</span><span class="sxs-lookup"><span data-stu-id="4f7b5-186">61</span></span>             | <span data-ttu-id="4f7b5-187">15</span><span class="sxs-lookup"><span data-stu-id="4f7b5-187">15</span></span>                 |
| <span data-ttu-id="4f7b5-188">91</span><span class="sxs-lookup"><span data-stu-id="4f7b5-188">91</span></span>             | <span data-ttu-id="4f7b5-189">20</span><span class="sxs-lookup"><span data-stu-id="4f7b5-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="4f7b5-190">Eksempel 3: Rente etter intervall = Måneder</span><span class="sxs-lookup"><span data-stu-id="4f7b5-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="4f7b5-191">Du definerer en rentekode som setter rente én gang for hver måned fakturabetalingen overskrider transaksjonens forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="4f7b5-192">Du vil basere beregningen på en renteverdiprosent, ifølge trinnvise månedsintervaller.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="4f7b5-193">Renteverdien vil være 1,5 prosent per måned de første tre månedene etter forfall, 2,0 prosent per måned for de neste tre månedene og 2,5 prosent per måned for hver måned etter de første seks månedene.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="4f7b5-194">Slik definerer du verdiene i rentekodefeltene.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="4f7b5-195">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-195">**Field name**</span></span>                  | <span data-ttu-id="4f7b5-196">**Feltverdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="4f7b5-197">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-197">**Interest code**</span></span>               | <span data-ttu-id="4f7b5-198">1M%EtMnd</span><span class="sxs-lookup"><span data-stu-id="4f7b5-198">1M%ByMth</span></span>        |
| <span data-ttu-id="4f7b5-199">**Beregn renter hver**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-199">**Calculate interest every**</span></span>    | <span data-ttu-id="4f7b5-200">1/måned</span><span class="sxs-lookup"><span data-stu-id="4f7b5-200">1/Month</span></span>         |
| <span data-ttu-id="4f7b5-201">**Rente etter intervall**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-201">**Interest by range**</span></span>           | <span data-ttu-id="4f7b5-202">Måneder</span><span class="sxs-lookup"><span data-stu-id="4f7b5-202">Months</span></span>          |
| <span data-ttu-id="4f7b5-203">**Beregn rente basert på**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-203">**Calculate interest based on**</span></span> | <span data-ttu-id="4f7b5-204">Prosent</span><span class="sxs-lookup"><span data-stu-id="4f7b5-204">Percentage</span></span>      |

<span data-ttu-id="4f7b5-205">Slik definerer du intervallinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="4f7b5-206">**Fra verdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-206">**From value**</span></span> | <span data-ttu-id="4f7b5-207">**Renteverdi**</span><span class="sxs-lookup"><span data-stu-id="4f7b5-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="4f7b5-208">0</span><span class="sxs-lookup"><span data-stu-id="4f7b5-208">0</span></span>              | <span data-ttu-id="4f7b5-209">1.5</span><span class="sxs-lookup"><span data-stu-id="4f7b5-209">1.5</span></span>                |
| <span data-ttu-id="4f7b5-210">4</span><span class="sxs-lookup"><span data-stu-id="4f7b5-210">4</span></span>              | <span data-ttu-id="4f7b5-211">2</span><span class="sxs-lookup"><span data-stu-id="4f7b5-211">2</span></span>                  |
| <span data-ttu-id="4f7b5-212">7</span><span class="sxs-lookup"><span data-stu-id="4f7b5-212">7</span></span>              | <span data-ttu-id="4f7b5-213">2,5</span><span class="sxs-lookup"><span data-stu-id="4f7b5-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="4f7b5-214">Nye versjoner</span><span class="sxs-lookup"><span data-stu-id="4f7b5-214">New versions</span></span>
<span data-ttu-id="4f7b5-215">Rentekoder har gyldighet fra en dato.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-215">Interest codes are date effective.</span></span> <span data-ttu-id="4f7b5-216">Hvis du vil endre rentesatsen, kan du opprette en **ny versjon** som gjelder fra og med en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="4f7b5-217">For å vise forskjellige versjoner, kan du bruke **Per dato**-menyvalget for å velge fristen.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="4f7b5-218">Du kan også velge **Vis alle poster** for å vise alle rentekoder på siden.</span><span class="sxs-lookup"><span data-stu-id="4f7b5-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
