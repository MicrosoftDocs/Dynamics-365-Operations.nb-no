---
title: Mva-beregning på generelle journallinjer
description: Dette emnet beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.
author: EricWang
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e4d367fe6cb729c9c5658a9bbbac04e53fdf9644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815338"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="23637-103">Mva-beregning på generelle journallinjer</span><span class="sxs-lookup"><span data-stu-id="23637-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="23637-104">Dette emnet beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.</span><span class="sxs-lookup"><span data-stu-id="23637-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="23637-105">Prosessen kan deles inn i tre trinn:</span><span class="sxs-lookup"><span data-stu-id="23637-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="23637-106">Fastslå mva-retningen.</span><span class="sxs-lookup"><span data-stu-id="23637-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="23637-107">Fastslår du mva-beløpet som skal lagres en midlertidig mva-tabell.</span><span class="sxs-lookup"><span data-stu-id="23637-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="23637-108">Fastslå mva-beløpet og kontoen på bilaget.</span><span class="sxs-lookup"><span data-stu-id="23637-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="23637-109">Fastslå mva-retningen</span><span class="sxs-lookup"><span data-stu-id="23637-109">Determine the sales tax direction</span></span>

<span data-ttu-id="23637-110">Hvordan mva-retningen bestemmes avhenger av kontotypen i bilaget.</span><span class="sxs-lookup"><span data-stu-id="23637-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="23637-111">Mva-retningen bestemmes av kombinasjonen av kontotypen og mva-koden.</span><span class="sxs-lookup"><span data-stu-id="23637-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="23637-112">Avsnittene nedenfor beskriver mulighetene mer detaljert.</span><span class="sxs-lookup"><span data-stu-id="23637-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="23637-113">Kontotype er Prosjekt</span><span class="sxs-lookup"><span data-stu-id="23637-113">Account type is Project</span></span>

<span data-ttu-id="23637-114">Hvis et bilag har journallinje der kontotypen er **Prosjekt**, vil alle journallinjene i bilaget bruke samme mva-retning.</span><span class="sxs-lookup"><span data-stu-id="23637-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="23637-115">Illustrasjonen nedenfor viser regelen.</span><span class="sxs-lookup"><span data-stu-id="23637-115">The following illustration shows the rule.</span></span> <span data-ttu-id="23637-116">Punktene nedenfor viser de mulige avgiftsretningene for prosjektkontoer.</span><span class="sxs-lookup"><span data-stu-id="23637-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="23637-117">•   Hvis mva-koden er use tax, er mva-retningen use tax.</span><span class="sxs-lookup"><span data-stu-id="23637-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="23637-118">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="23637-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="23637-119">•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="23637-120">•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="23637-121">I andre tilfeller er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="23637-122">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="23637-122">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for prosjektkontoer](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="23637-124">Kontotype er Leverandør</span><span class="sxs-lookup"><span data-stu-id="23637-124">Account type is Vendor</span></span>

<span data-ttu-id="23637-125">Hvis et bilag har journallinje der kontotypen er **Leverandør**, vil alle journallinjene i bilaget bruke samme mva-retning.</span><span class="sxs-lookup"><span data-stu-id="23637-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="23637-126">Punktene nedenfor viser de mulige avgiftsretningene for leverandørkontoer.</span><span class="sxs-lookup"><span data-stu-id="23637-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="23637-127">•   Hvis mva-koden er use tax, er mva-retningen use tax.</span><span class="sxs-lookup"><span data-stu-id="23637-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="23637-128">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="23637-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="23637-129">•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="23637-130">•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="23637-131">I andre tilfeller er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="23637-132">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="23637-132">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for leverandørkontoer](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="23637-134">Kontotype er Kunde</span><span class="sxs-lookup"><span data-stu-id="23637-134">Account type is Customer</span></span>

<span data-ttu-id="23637-135">Hvis et bilag har journallinje der kontotypen er **Kunde**, vil alle journallinjene i bilaget bruke samme mva-retning.</span><span class="sxs-lookup"><span data-stu-id="23637-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="23637-136">Punktene nedenfor viser de mulige avgiftsretningene for kundekontoer.</span><span class="sxs-lookup"><span data-stu-id="23637-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="23637-137">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="23637-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="23637-138">•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="23637-139">•   Hvis mva-koden er snudd avregning, er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="23637-140">I andre tilfeller er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="23637-141">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="23637-141">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for kundekontoer](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="23637-143">Kontotype er Finans</span><span class="sxs-lookup"><span data-stu-id="23637-143">Account type is Ledger</span></span>

<span data-ttu-id="23637-144">Illustrasjonen nedenfor viser regelen som gjelder når et bilag bare har journallinjer der kontotypen er **Finans**.</span><span class="sxs-lookup"><span data-stu-id="23637-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="23637-145">Punktene nedenfor viser de mulige avgiftsretningene for finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="23637-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="23637-146">•   Hvis mva-koden er use tax, er mva-retningen use tax.</span><span class="sxs-lookup"><span data-stu-id="23637-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="23637-147">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="23637-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="23637-148">Hvis journalbeløpet imidlertid er debet (positivt), er mva-retningen Innkommende merverdiavgift. Hvis journalbeløpet er kredit (negativt), er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="23637-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="23637-149">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="23637-149">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for finanskontoer](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="23637-151">Overstyre mva-retningen</span><span class="sxs-lookup"><span data-stu-id="23637-151">Override the sales tax direction</span></span>

<span data-ttu-id="23637-152">Du kan overstyre mva-retningen når bilaget bare inneholder linjer der kontotypen er **Finans.**</span><span class="sxs-lookup"><span data-stu-id="23637-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="23637-153">Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**, og velg hurtigfanen **Overstyringer for juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="23637-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="23637-154">Fastslå mva-beløp</span><span class="sxs-lookup"><span data-stu-id="23637-154">Determine the sales tax amount</span></span>

<span data-ttu-id="23637-155">Denne delen beskriver hvordan fortegnet for mva-beløpet beregnes.</span><span class="sxs-lookup"><span data-stu-id="23637-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Siden Mva-transaksjoner](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="23637-157">Tabellen nedenfor viser den generelle regelen for å fastslå fortegnet for mva-beløp i den midlertidige mva-tabellen.</span><span class="sxs-lookup"><span data-stu-id="23637-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="23637-158">Journallinjebeløp</span><span class="sxs-lookup"><span data-stu-id="23637-158">Journal line amount</span></span> | <span data-ttu-id="23637-159">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="23637-159">Sales tax direction</span></span>  | <span data-ttu-id="23637-160">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="23637-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="23637-161">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-161">Positive</span></span>            | <span data-ttu-id="23637-162">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-162">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-163">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-163">Positive</span></span>              |
| <span data-ttu-id="23637-164">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-164">Positive</span></span>            | <span data-ttu-id="23637-165">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-165">Sales Tax Payable</span></span>    | <span data-ttu-id="23637-166">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-166">Negative</span></span>              |
| <span data-ttu-id="23637-167">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-167">Negative</span></span>            | <span data-ttu-id="23637-168">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-168">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-169">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-169">Negative</span></span>              |
| <span data-ttu-id="23637-170">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-170">Negative</span></span>            | <span data-ttu-id="23637-171">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-171">Sales Tax Payable</span></span>    | <span data-ttu-id="23637-172">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-172">Positive</span></span>              |

<span data-ttu-id="23637-173">Det finnes en spesialregel for bilag som bare har **Prosjekt**- eller **Finans**-linjer når det velges en mva-gruppe eller en mva-gruppe for vare på **Finans**-linjen.</span><span class="sxs-lookup"><span data-stu-id="23637-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="23637-174">Denne regelen styres ved hjelp av funksjonen Aktiver uavhengig beregning av merverdiavgift for generelle journaler.</span><span class="sxs-lookup"><span data-stu-id="23637-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="23637-175">Når denne funksjonen er deaktivert, bruker avgiftsbeløpet **Finans**-linjen debet-/kreditretningen for **Prosjekt**-linjen.</span><span class="sxs-lookup"><span data-stu-id="23637-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="23637-176">Når denne funksjonen er aktivert, bruker avgiftsbeløpet **Finans**-linjen sin egen debet-/kreditretning.</span><span class="sxs-lookup"><span data-stu-id="23637-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="23637-177">Tabellene nedenfor viser regelen for hvert scenario.</span><span class="sxs-lookup"><span data-stu-id="23637-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="23637-178">**Regel når funksjonen er aktivert**</span><span class="sxs-lookup"><span data-stu-id="23637-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="23637-179">Journallinjebeløp for prosjekt</span><span class="sxs-lookup"><span data-stu-id="23637-179">Journal line amount of project</span></span> | <span data-ttu-id="23637-180">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="23637-180">Sales tax direction</span></span>  | <span data-ttu-id="23637-181">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="23637-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="23637-182">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-182">Positive</span></span>                       | <span data-ttu-id="23637-183">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-183">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-184">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-184">Positive</span></span>              |
| <span data-ttu-id="23637-185">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-185">Negative</span></span>                       | <span data-ttu-id="23637-186">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-186">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-187">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-187">Negative</span></span>              |

<span data-ttu-id="23637-188">**Regel når funksjonen er deaktivert**</span><span class="sxs-lookup"><span data-stu-id="23637-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="23637-189">Journallinjebeløp for finans</span><span class="sxs-lookup"><span data-stu-id="23637-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="23637-190">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="23637-190">Sales tax direction</span></span>  | <span data-ttu-id="23637-191">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="23637-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="23637-192">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-192">Positive</span></span>                       | <span data-ttu-id="23637-193">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-193">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-194">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-194">Positive</span></span>              |
| <span data-ttu-id="23637-195">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-195">Negative</span></span>                       | <span data-ttu-id="23637-196">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-196">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-197">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="23637-198">Fastslå mva-beløpet og kontoen på bilaget</span><span class="sxs-lookup"><span data-stu-id="23637-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="23637-199">Når du posterer merverdiavgift, hentes hovedkontoen fra profilen for finansposteringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="23637-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="23637-200">Når merverdiavgift er til innkommende, bruker systemet kontoen Innkommende merverdiavgift som er angitt i profilen.</span><span class="sxs-lookup"><span data-stu-id="23637-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="23637-201">For merverdiavgift som er utgående bruker systemet kontoen Utgående merverdiavgift som er angitt i profilen.</span><span class="sxs-lookup"><span data-stu-id="23637-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="23637-202">Tabellen nedenfor viser den generelle regelen.</span><span class="sxs-lookup"><span data-stu-id="23637-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="23637-203">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="23637-203">Sales tax direction</span></span>  | <span data-ttu-id="23637-204">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="23637-204">Sales tax amount sign</span></span> | <span data-ttu-id="23637-205">Mva-konto</span><span class="sxs-lookup"><span data-stu-id="23637-205">Sales tax account</span></span>      | <span data-ttu-id="23637-206">Beløp på bilag</span><span class="sxs-lookup"><span data-stu-id="23637-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="23637-207">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-207">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-208">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-208">Positive</span></span>              | <span data-ttu-id="23637-209">Konto for innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-209">Tax Receivable Account</span></span> | <span data-ttu-id="23637-210">Positive (debet)</span><span class="sxs-lookup"><span data-stu-id="23637-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="23637-211">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-211">Sales Tax Receivable</span></span> | <span data-ttu-id="23637-212">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-212">Negative</span></span>              | <span data-ttu-id="23637-213">Konto for innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-213">Tax Receivable Account</span></span> | <span data-ttu-id="23637-214">Negativ (kredit)</span><span class="sxs-lookup"><span data-stu-id="23637-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="23637-215">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-215">Sales Tax Payable</span></span>    | <span data-ttu-id="23637-216">Positiv</span><span class="sxs-lookup"><span data-stu-id="23637-216">Positive</span></span>              | <span data-ttu-id="23637-217">Konto for utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-217">Tax Payable Account</span></span>    | <span data-ttu-id="23637-218">Negativ (kredit)</span><span class="sxs-lookup"><span data-stu-id="23637-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="23637-219">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-219">Sales Tax Payable</span></span>    | <span data-ttu-id="23637-220">Negativ</span><span class="sxs-lookup"><span data-stu-id="23637-220">Negative</span></span>              | <span data-ttu-id="23637-221">Konto for utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="23637-221">Tax Payable Account</span></span>    | <span data-ttu-id="23637-222">Positive (debet)</span><span class="sxs-lookup"><span data-stu-id="23637-222">Positive (Debit)</span></span>  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]