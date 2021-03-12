---
title: Mva-beregning på generelle journallinjer
description: Dette emnet beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: e420632c248b5b43d4983c5eb483cac580e67f20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975564"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="19008-103">Mva-beregning på generelle journallinjer</span><span class="sxs-lookup"><span data-stu-id="19008-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="19008-104">Dette emnet beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.</span><span class="sxs-lookup"><span data-stu-id="19008-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="19008-105">Prosessen kan deles inn i tre trinn:</span><span class="sxs-lookup"><span data-stu-id="19008-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="19008-106">Fastslå mva-retningen.</span><span class="sxs-lookup"><span data-stu-id="19008-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="19008-107">Fastslår du mva-beløpet som skal lagres en midlertidig mva-tabell.</span><span class="sxs-lookup"><span data-stu-id="19008-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="19008-108">Fastslå mva-beløpet og kontoen på bilaget.</span><span class="sxs-lookup"><span data-stu-id="19008-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="19008-109">Fastslå mva-retningen</span><span class="sxs-lookup"><span data-stu-id="19008-109">Determine the sales tax direction</span></span>

<span data-ttu-id="19008-110">Hvordan mva-retningen bestemmes avhenger av kontotypen i bilaget.</span><span class="sxs-lookup"><span data-stu-id="19008-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="19008-111">Mva-retningen bestemmes av kombinasjonen av kontotypen og mva-koden.</span><span class="sxs-lookup"><span data-stu-id="19008-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="19008-112">Avsnittene nedenfor beskriver mulighetene mer detaljert.</span><span class="sxs-lookup"><span data-stu-id="19008-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="19008-113">Kontotype er Prosjekt</span><span class="sxs-lookup"><span data-stu-id="19008-113">Account type is Project</span></span>

<span data-ttu-id="19008-114">Hvis et bilag har journallinje der kontotypen er **Prosjekt**, vil alle journallinjene i bilaget bruke samme mva-retning.</span><span class="sxs-lookup"><span data-stu-id="19008-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="19008-115">Illustrasjonen nedenfor viser regelen.</span><span class="sxs-lookup"><span data-stu-id="19008-115">The following illustration shows the rule.</span></span> <span data-ttu-id="19008-116">Punktene nedenfor viser de mulige avgiftsretningene for prosjektkontoer.</span><span class="sxs-lookup"><span data-stu-id="19008-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="19008-117">•   Hvis mva-koden er use tax, er mva-retningen use tax.</span><span class="sxs-lookup"><span data-stu-id="19008-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="19008-118">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="19008-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="19008-119">•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="19008-120">•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="19008-121">I andre tilfeller er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="19008-122">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="19008-122">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for prosjektkontoer](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="19008-124">Kontotype er Leverandør</span><span class="sxs-lookup"><span data-stu-id="19008-124">Account type is Vendor</span></span>

<span data-ttu-id="19008-125">Hvis et bilag har journallinje der kontotypen er **Leverandør**, vil alle journallinjene i bilaget bruke samme mva-retning.</span><span class="sxs-lookup"><span data-stu-id="19008-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="19008-126">Punktene nedenfor viser de mulige avgiftsretningene for leverandørkontoer.</span><span class="sxs-lookup"><span data-stu-id="19008-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="19008-127">•   Hvis mva-koden er use tax, er mva-retningen use tax.</span><span class="sxs-lookup"><span data-stu-id="19008-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="19008-128">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="19008-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="19008-129">•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="19008-130">•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="19008-131">I andre tilfeller er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="19008-132">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="19008-132">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for leverandørkontoer](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="19008-134">Kontotype er Kunde</span><span class="sxs-lookup"><span data-stu-id="19008-134">Account type is Customer</span></span>

<span data-ttu-id="19008-135">Hvis et bilag har journallinje der kontotypen er **Kunde**, vil alle journallinjene i bilaget bruke samme mva-retning.</span><span class="sxs-lookup"><span data-stu-id="19008-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="19008-136">Punktene nedenfor viser de mulige avgiftsretningene for kundekontoer.</span><span class="sxs-lookup"><span data-stu-id="19008-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="19008-137">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="19008-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="19008-138">•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="19008-139">•   Hvis mva-koden er snudd avregning, er mva-retningen innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="19008-140">I andre tilfeller er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="19008-141">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="19008-141">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for kundekontoer](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="19008-143">Kontotype er Finans</span><span class="sxs-lookup"><span data-stu-id="19008-143">Account type is Ledger</span></span>

<span data-ttu-id="19008-144">Illustrasjonen nedenfor viser regelen som gjelder når et bilag bare har journallinjer der kontotypen er **Finans**.</span><span class="sxs-lookup"><span data-stu-id="19008-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="19008-145">Punktene nedenfor viser de mulige avgiftsretningene for finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="19008-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="19008-146">•   Hvis mva-koden er use tax, er mva-retningen use tax.</span><span class="sxs-lookup"><span data-stu-id="19008-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="19008-147">•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.</span><span class="sxs-lookup"><span data-stu-id="19008-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="19008-148">Hvis journalbeløpet imidlertid er debet (positivt), er mva-retningen Innkommende merverdiavgift. Hvis journalbeløpet er kredit (negativt), er mva-retningen Utgående merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="19008-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="19008-149">Diagrammet nedenfor illustrerer regelen grafisk.</span><span class="sxs-lookup"><span data-stu-id="19008-149">The following diagram illustrates the rule graphically.</span></span>

![Muligheter for avgiftsretning for finanskontoer](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="19008-151">Overstyre mva-retningen</span><span class="sxs-lookup"><span data-stu-id="19008-151">Override the sales tax direction</span></span>

<span data-ttu-id="19008-152">Du kan overstyre mva-retningen når bilaget bare inneholder linjer der kontotypen er **Finans.**</span><span class="sxs-lookup"><span data-stu-id="19008-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="19008-153">Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**, og velg hurtigfanen **Overstyringer for juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="19008-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="19008-154">Fastslå mva-beløp</span><span class="sxs-lookup"><span data-stu-id="19008-154">Determine the sales tax amount</span></span>

<span data-ttu-id="19008-155">Denne delen beskriver hvordan fortegnet for mva-beløpet beregnes.</span><span class="sxs-lookup"><span data-stu-id="19008-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Siden Mva-transaksjoner](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="19008-157">Tabellen nedenfor viser den generelle regelen for å fastslå fortegnet for mva-beløp i den midlertidige mva-tabellen.</span><span class="sxs-lookup"><span data-stu-id="19008-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="19008-158">Journallinjebeløp</span><span class="sxs-lookup"><span data-stu-id="19008-158">Journal line amount</span></span> | <span data-ttu-id="19008-159">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="19008-159">Sales tax direction</span></span>  | <span data-ttu-id="19008-160">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="19008-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="19008-161">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-161">Positive</span></span>            | <span data-ttu-id="19008-162">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-162">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-163">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-163">Positive</span></span>              |
| <span data-ttu-id="19008-164">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-164">Positive</span></span>            | <span data-ttu-id="19008-165">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-165">Sales Tax Payable</span></span>    | <span data-ttu-id="19008-166">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-166">Negative</span></span>              |
| <span data-ttu-id="19008-167">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-167">Negative</span></span>            | <span data-ttu-id="19008-168">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-168">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-169">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-169">Negative</span></span>              |
| <span data-ttu-id="19008-170">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-170">Negative</span></span>            | <span data-ttu-id="19008-171">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-171">Sales Tax Payable</span></span>    | <span data-ttu-id="19008-172">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-172">Positive</span></span>              |

<span data-ttu-id="19008-173">Det finnes en spesialregel for bilag som bare har **Prosjekt**- eller **Finans**-linjer når det velges en mva-gruppe eller en mva-gruppe for vare på **Finans**-linjen.</span><span class="sxs-lookup"><span data-stu-id="19008-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="19008-174">Denne regelen styres ved hjelp av funksjonen Aktiver uavhengig beregning av merverdiavgift for generelle journaler.</span><span class="sxs-lookup"><span data-stu-id="19008-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="19008-175">Når denne funksjonen er deaktivert, bruker avgiftsbeløpet **Finans**-linjen debet-/kreditretningen for **Prosjekt**-linjen.</span><span class="sxs-lookup"><span data-stu-id="19008-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="19008-176">Når denne funksjonen er aktivert, bruker avgiftsbeløpet **Finans**-linjen sin egen debet-/kreditretning.</span><span class="sxs-lookup"><span data-stu-id="19008-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="19008-177">Tabellene nedenfor viser regelen for hvert scenario.</span><span class="sxs-lookup"><span data-stu-id="19008-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="19008-178">**Regel når funksjonen er aktivert**</span><span class="sxs-lookup"><span data-stu-id="19008-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="19008-179">Journallinjebeløp for prosjekt</span><span class="sxs-lookup"><span data-stu-id="19008-179">Journal line amount of project</span></span> | <span data-ttu-id="19008-180">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="19008-180">Sales tax direction</span></span>  | <span data-ttu-id="19008-181">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="19008-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="19008-182">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-182">Positive</span></span>                       | <span data-ttu-id="19008-183">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-183">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-184">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-184">Positive</span></span>              |
| <span data-ttu-id="19008-185">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-185">Negative</span></span>                       | <span data-ttu-id="19008-186">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-186">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-187">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-187">Negative</span></span>              |

<span data-ttu-id="19008-188">**Regel når funksjonen er deaktivert**</span><span class="sxs-lookup"><span data-stu-id="19008-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="19008-189">Journallinjebeløp for finans</span><span class="sxs-lookup"><span data-stu-id="19008-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="19008-190">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="19008-190">Sales tax direction</span></span>  | <span data-ttu-id="19008-191">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="19008-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="19008-192">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-192">Positive</span></span>                       | <span data-ttu-id="19008-193">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-193">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-194">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-194">Positive</span></span>              |
| <span data-ttu-id="19008-195">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-195">Negative</span></span>                       | <span data-ttu-id="19008-196">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-196">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-197">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="19008-198">Fastslå mva-beløpet og kontoen på bilaget</span><span class="sxs-lookup"><span data-stu-id="19008-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="19008-199">Når du posterer merverdiavgift, hentes hovedkontoen fra profilen for finansposteringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="19008-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="19008-200">Når merverdiavgift er til innkommende, bruker systemet kontoen Innkommende merverdiavgift som er angitt i profilen.</span><span class="sxs-lookup"><span data-stu-id="19008-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="19008-201">For merverdiavgift som er utgående bruker systemet kontoen Utgående merverdiavgift som er angitt i profilen.</span><span class="sxs-lookup"><span data-stu-id="19008-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="19008-202">Tabellen nedenfor viser den generelle regelen.</span><span class="sxs-lookup"><span data-stu-id="19008-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="19008-203">Mva-retning</span><span class="sxs-lookup"><span data-stu-id="19008-203">Sales tax direction</span></span>  | <span data-ttu-id="19008-204">Fortegn for mva-beløp</span><span class="sxs-lookup"><span data-stu-id="19008-204">Sales tax amount sign</span></span> | <span data-ttu-id="19008-205">Mva-konto</span><span class="sxs-lookup"><span data-stu-id="19008-205">Sales tax account</span></span>      | <span data-ttu-id="19008-206">Beløp på bilag</span><span class="sxs-lookup"><span data-stu-id="19008-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="19008-207">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-207">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-208">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-208">Positive</span></span>              | <span data-ttu-id="19008-209">Konto for innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-209">Tax Receivable Account</span></span> | <span data-ttu-id="19008-210">Positive (debet)</span><span class="sxs-lookup"><span data-stu-id="19008-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="19008-211">Innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-211">Sales Tax Receivable</span></span> | <span data-ttu-id="19008-212">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-212">Negative</span></span>              | <span data-ttu-id="19008-213">Konto for innkommende merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-213">Tax Receivable Account</span></span> | <span data-ttu-id="19008-214">Negativ (kredit)</span><span class="sxs-lookup"><span data-stu-id="19008-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="19008-215">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-215">Sales Tax Payable</span></span>    | <span data-ttu-id="19008-216">Positiv</span><span class="sxs-lookup"><span data-stu-id="19008-216">Positive</span></span>              | <span data-ttu-id="19008-217">Konto for utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-217">Tax Payable Account</span></span>    | <span data-ttu-id="19008-218">Negativ (kredit)</span><span class="sxs-lookup"><span data-stu-id="19008-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="19008-219">Utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-219">Sales Tax Payable</span></span>    | <span data-ttu-id="19008-220">Negativ</span><span class="sxs-lookup"><span data-stu-id="19008-220">Negative</span></span>              | <span data-ttu-id="19008-221">Konto for utgående merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="19008-221">Tax Payable Account</span></span>    | <span data-ttu-id="19008-222">Positive (debet)</span><span class="sxs-lookup"><span data-stu-id="19008-222">Positive (Debit)</span></span>  |
