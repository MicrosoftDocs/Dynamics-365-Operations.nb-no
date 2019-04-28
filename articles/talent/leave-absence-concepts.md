---
title: Begreper for permisjon og fravær
description: Dette emnet beskriver begreper for permisjon og fravær og hvordan avspaseringssaldoer fastsettes.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "857299"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="f9472-103">Begreper for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="f9472-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f9472-104">Begreper og termer som er beskrevet i dette emnet, kan hjelpe deg med å finne ut hvordan en ansatt belønnes med avspasering, og hvordan den ansattes tidssaldoer beregnes.</span><span class="sxs-lookup"><span data-stu-id="f9472-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="f9472-105">Hvis du vil ha mer informasjon om permisjons- og fraværsadministrasjon, kan du se [Administrasjon av permisjon og fravær](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="f9472-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="f9472-106">Permisjonsplandetaljer</span><span class="sxs-lookup"><span data-stu-id="f9472-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="f9472-107">Startdato</span><span class="sxs-lookup"><span data-stu-id="f9472-107">Start date</span></span>

<span data-ttu-id="f9472-108">Startdatoen er datoen som avsetningsbehandlingen starter på.</span><span class="sxs-lookup"><span data-stu-id="f9472-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="f9472-109">Startdatoen fungerer også som merkedato for å beregne overføringsbeløp.</span><span class="sxs-lookup"><span data-stu-id="f9472-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="f9472-110">Avsetninger</span><span class="sxs-lookup"><span data-stu-id="f9472-110">Accruals</span></span>

<span data-ttu-id="f9472-111">Avsetninger bestemmer når og hvor ofte en ansatt belønnes med avspasering.</span><span class="sxs-lookup"><span data-stu-id="f9472-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="f9472-112">Retningslinjer om når avsetningene skal tildeles og policyer om fordeling, defineres i **Avsetninger**-delen når du definerer permisjons- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="f9472-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="f9472-113">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-113">Accrual frequency</span></span>

<span data-ttu-id="f9472-114">Avsetningsfrekvensen definerer hvor ofte permisjon avsettes eller tildeles.</span><span class="sxs-lookup"><span data-stu-id="f9472-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="f9472-115">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f9472-115">The following options are available:</span></span>

- <span data-ttu-id="f9472-116">Daglig</span><span class="sxs-lookup"><span data-stu-id="f9472-116">Daily</span></span>
- <span data-ttu-id="f9472-117">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="f9472-117">Weekly</span></span>
- <span data-ttu-id="f9472-118">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="f9472-118">Biweekly</span></span>
- <span data-ttu-id="f9472-119">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-119">Semimonthly</span></span>
- <span data-ttu-id="f9472-120">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-120">Monthly</span></span>
- <span data-ttu-id="f9472-121">Kvartalsvis</span><span class="sxs-lookup"><span data-stu-id="f9472-121">Quarterly</span></span>
- <span data-ttu-id="f9472-122">Hvert halvår</span><span class="sxs-lookup"><span data-stu-id="f9472-122">Semiannually</span></span>
- <span data-ttu-id="f9472-123">Årlig</span><span class="sxs-lookup"><span data-stu-id="f9472-123">Annually</span></span>
- <span data-ttu-id="f9472-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f9472-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="f9472-125">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-125">Accrual period basis</span></span>

<span data-ttu-id="f9472-126">Avsetningsperiodegrunnlaget fastsetter datoen som brukes til å beregne avsetningsperioder.</span><span class="sxs-lookup"><span data-stu-id="f9472-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="f9472-127">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f9472-127">The following options are available:</span></span>

- <span data-ttu-id="f9472-128">**Startdato for plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-128">**Plan start date**</span></span>
- <span data-ttu-id="f9472-129">**Spesifikk dato for ansatt** – Når dette alternativet er valgt, fastsetter verdien kilden til den opprinnelige datoverdien som brukes til å beregne avsetningsperioder.</span><span class="sxs-lookup"><span data-stu-id="f9472-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="f9472-130">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f9472-130">The following options are available:</span></span>

    - <span data-ttu-id="f9472-131">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="f9472-131">Custom</span></span>
    - <span data-ttu-id="f9472-132">Jubileumsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-132">Anniversary date</span></span>
    - <span data-ttu-id="f9472-133">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="f9472-133">Original hire date</span></span>
    - <span data-ttu-id="f9472-134">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-134">Seniority date</span></span>
    - <span data-ttu-id="f9472-135">Arbeiderens justerte startdato</span><span class="sxs-lookup"><span data-stu-id="f9472-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="f9472-136">Arbeiderens startdato</span><span class="sxs-lookup"><span data-stu-id="f9472-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="f9472-137">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-137">Accrual award date</span></span>

<span data-ttu-id="f9472-138">Belønningsdatoen for avsetning bestemmer når en ansatt tildeles fri.</span><span class="sxs-lookup"><span data-stu-id="f9472-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="f9472-139">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f9472-139">The following options are available:</span></span>

- <span data-ttu-id="f9472-140">**Sluttdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den siste dagen i belønningsperioden.</span><span class="sxs-lookup"><span data-stu-id="f9472-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="f9472-141">Hvis du vil avsette riktig tid, må avsetningsprosessen inkludere hele perioden.</span><span class="sxs-lookup"><span data-stu-id="f9472-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="f9472-142">Avsetningsperioden er for eksempel fra 1. januar 2018 til og med 31. januar 2018.</span><span class="sxs-lookup"><span data-stu-id="f9472-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="f9472-143">For at januar skal tas med i dette tilfelle, må avsetningen kjøres for 1. februar 2018.</span><span class="sxs-lookup"><span data-stu-id="f9472-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="f9472-144">**Startdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den første dagen i belønningsperioden.</span><span class="sxs-lookup"><span data-stu-id="f9472-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="f9472-145">Avsetningspolicy ved registrering</span><span class="sxs-lookup"><span data-stu-id="f9472-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="f9472-146">Avsetningspolicyen ved registrering angir hvordan avsetning beregnes når ansatte registreres i midten av en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="f9472-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="f9472-147">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f9472-147">The following options are available:</span></span>

- <span data-ttu-id="f9472-148">**Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager.</span><span class="sxs-lookup"><span data-stu-id="f9472-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="f9472-149">Denne differansen brukes når avsetninger behandles.</span><span class="sxs-lookup"><span data-stu-id="f9472-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="f9472-150">**Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="f9472-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="f9472-151">**Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="f9472-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="f9472-152">Avsetningspolicy ved avregistrering</span><span class="sxs-lookup"><span data-stu-id="f9472-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="f9472-153">Avsetningspolicyen ved avregistrering angir hvordan avsetning beregnes når ansatte avregistreres i midten av en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="f9472-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="f9472-154">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f9472-154">The following options are available:</span></span>

- <span data-ttu-id="f9472-155">**Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager.</span><span class="sxs-lookup"><span data-stu-id="f9472-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="f9472-156">Denne differansen brukes når avsetninger behandles.</span><span class="sxs-lookup"><span data-stu-id="f9472-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="f9472-157">**Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="f9472-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="f9472-158">**Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="f9472-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="f9472-159">Avsetningsplan</span><span class="sxs-lookup"><span data-stu-id="f9472-159">Accrual schedule</span></span>

<span data-ttu-id="f9472-160">Avsetningsplanen bestemmer hvordan en ansatt skal avsette avspasering, og hvor mye den ansatte skal avsette og overføre.</span><span class="sxs-lookup"><span data-stu-id="f9472-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="f9472-161">Lag kan opprettes slik at avspasering tildeles basert på forskjellige nivåer.</span><span class="sxs-lookup"><span data-stu-id="f9472-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="f9472-162">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="f9472-162">Months of service</span></span>

<span data-ttu-id="f9472-163">**Måneder med jobberfaring**-verdien definerer det minste antallet måneder som ansatte må arbeide for å være berettiget til avsetninger.</span><span class="sxs-lookup"><span data-stu-id="f9472-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="f9472-164">Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.</span><span class="sxs-lookup"><span data-stu-id="f9472-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="f9472-165">Arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="f9472-165">Hours worked</span></span>

<span data-ttu-id="f9472-166">**Arbeidstimer**-verdien definerer det minste antallet timer som ansatte må arbeide per avsetningsperiode for å være berettiget til avsetninger.</span><span class="sxs-lookup"><span data-stu-id="f9472-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="f9472-167">Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.</span><span class="sxs-lookup"><span data-stu-id="f9472-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="f9472-168">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-168">Accrual amount</span></span>

<span data-ttu-id="f9472-169">Avsetningsbeløpet er antallet timer eller dager som ansatte skal avsette per periode.</span><span class="sxs-lookup"><span data-stu-id="f9472-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="f9472-170">Perioden er basert på avsetningsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="f9472-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="f9472-171">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-171">Minimum balance</span></span>

<span data-ttu-id="f9472-172">En negativ verdi kan brukes for minimumssaldoen hvis ansatte kan be om mer permisjon enn de har tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f9472-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="f9472-173">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-173">Maximum carry-forward</span></span>

<span data-ttu-id="f9472-174">Avsetningsprosessen justerer permisjonssaldoer som overskrider maksimal overføringssaldo på merkedagen til startdatoen.</span><span class="sxs-lookup"><span data-stu-id="f9472-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="f9472-175">Tildelingsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-175">Grant amount</span></span>

<span data-ttu-id="f9472-176">Tildelingsbeløpet er det opprinnelige antallet timer eller dager som ansatte gis når de registrerer seg for permisjonsplanen første gang.</span><span class="sxs-lookup"><span data-stu-id="f9472-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="f9472-177">Beløpet avsettes ikke for hver avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="f9472-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="f9472-178">Registreringer og saldoer</span><span class="sxs-lookup"><span data-stu-id="f9472-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="f9472-179">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-179">Enrollment date</span></span>

<span data-ttu-id="f9472-180">Registreringsdatoen bestemmer når en ansatt kan begynne å avsette avspasering.</span><span class="sxs-lookup"><span data-stu-id="f9472-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="f9472-181">Hvis for eksempel en ansatt registreres i en ferieplan 15. juni 2018, kan vedkommende ikke avsette avspasering før 15. juni 2018.</span><span class="sxs-lookup"><span data-stu-id="f9472-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="f9472-182">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-182">Current balance</span></span>

<span data-ttu-id="f9472-183">Gjeldende saldo er hvor mye permisjon som er tilgjengelig for avspaseringsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="f9472-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="f9472-184">Dette beløpet inkluderer avsetninger godkjente forespørsler og justeringer til og med den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="f9472-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="f9472-185">Eksempler på gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="f9472-186">Årsplan</span><span class="sxs-lookup"><span data-stu-id="f9472-186">Annual plan</span></span>

<span data-ttu-id="f9472-187">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-187">**Plan setup**</span></span>

| <span data-ttu-id="f9472-188">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-188">Plan start date</span></span> | <span data-ttu-id="f9472-189">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-189">Enrollment date</span></span> | <span data-ttu-id="f9472-190">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-190">Accrual frequency</span></span> | <span data-ttu-id="f9472-191">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-191">Accrual period basis</span></span> | <span data-ttu-id="f9472-192">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f9472-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-193">1/1/2018</span></span>        | <span data-ttu-id="f9472-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-194">1/1/2018</span></span>        | <span data-ttu-id="f9472-195">Årlig</span><span class="sxs-lookup"><span data-stu-id="f9472-195">Annual</span></span>            | <span data-ttu-id="f9472-196">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-196">Plan start date</span></span>      | <span data-ttu-id="f9472-197">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="f9472-197">End of accrual period</span></span> |

<span data-ttu-id="f9472-198">Avsetninger behandles 1. januar 2019 (1.1.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f9472-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f9472-199">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-199">**Results**</span></span>

| <span data-ttu-id="f9472-200">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-200">Accrual amount</span></span> | <span data-ttu-id="f9472-201">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-201">Minimum balance</span></span> | <span data-ttu-id="f9472-202">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-202">Maximum carry-forward</span></span> | <span data-ttu-id="f9472-203">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-203">Request amount</span></span> | <span data-ttu-id="f9472-204">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="f9472-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="f9472-205">200</span><span class="sxs-lookup"><span data-stu-id="f9472-205">200</span></span>            | <span data-ttu-id="f9472-206">0</span><span class="sxs-lookup"><span data-stu-id="f9472-206">0</span></span>               | <span data-ttu-id="f9472-207">120</span><span class="sxs-lookup"><span data-stu-id="f9472-207">120</span></span>                   | <span data-ttu-id="f9472-208">40</span><span class="sxs-lookup"><span data-stu-id="f9472-208">40</span></span>             | <span data-ttu-id="f9472-209">160</span><span class="sxs-lookup"><span data-stu-id="f9472-209">160</span></span>                              |

<span data-ttu-id="f9472-210">Gjeldende saldo (160) = avsetningsbeløp (200) – forespurt beløp (40)</span><span class="sxs-lookup"><span data-stu-id="f9472-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="f9472-211">Halvmånedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-211">Semimonthly plan</span></span>

<span data-ttu-id="f9472-212">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-212">**Plan setup**</span></span>

| <span data-ttu-id="f9472-213">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-213">Plan start date</span></span> | <span data-ttu-id="f9472-214">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-214">Enrollment date</span></span> | <span data-ttu-id="f9472-215">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-215">Accrual frequency</span></span> | <span data-ttu-id="f9472-216">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-216">Accrual period basis</span></span> | <span data-ttu-id="f9472-217">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f9472-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-218">1/1/2018</span></span>        | <span data-ttu-id="f9472-219">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-219">2/1/2018</span></span>        | <span data-ttu-id="f9472-220">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-220">Semimonthly</span></span>       | <span data-ttu-id="f9472-221">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-221">Plan start date</span></span>      | <span data-ttu-id="f9472-222">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="f9472-222">End of accrual period</span></span> |

<span data-ttu-id="f9472-223">Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f9472-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="f9472-224">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-224">**Results**</span></span>

| <span data-ttu-id="f9472-225">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-225">Accrual amount</span></span> | <span data-ttu-id="f9472-226">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-226">Minimum balance</span></span> | <span data-ttu-id="f9472-227">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-227">Maximum carry-forward</span></span> | <span data-ttu-id="f9472-228">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-228">Request amount</span></span> | <span data-ttu-id="f9472-229">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="f9472-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="f9472-230">5</span><span class="sxs-lookup"><span data-stu-id="f9472-230">5</span></span>              | <span data-ttu-id="f9472-231">0</span><span class="sxs-lookup"><span data-stu-id="f9472-231">0</span></span>               | <span data-ttu-id="f9472-232">120</span><span class="sxs-lookup"><span data-stu-id="f9472-232">120</span></span>                   | <span data-ttu-id="f9472-233">8</span><span class="sxs-lookup"><span data-stu-id="f9472-233">8</span></span>              | <span data-ttu-id="f9472-234">22</span><span class="sxs-lookup"><span data-stu-id="f9472-234">22</span></span>                               |

<span data-ttu-id="f9472-235">Gjeldende saldo (22) = avsetningsbeløp (5 x 6) – forespurt beløp (8)</span><span class="sxs-lookup"><span data-stu-id="f9472-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="f9472-236">Månedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-236">Monthly plan</span></span>

<span data-ttu-id="f9472-237">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-237">**Plan setup**</span></span>

| <span data-ttu-id="f9472-238">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-238">Plan start date</span></span> | <span data-ttu-id="f9472-239">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-239">Enrollment date</span></span> | <span data-ttu-id="f9472-240">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-240">Accrual frequency</span></span> | <span data-ttu-id="f9472-241">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-241">Accrual period basis</span></span> | <span data-ttu-id="f9472-242">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f9472-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-243">1/1/2018</span></span>        | <span data-ttu-id="f9472-244">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-244">2/1/2018</span></span>        | <span data-ttu-id="f9472-245">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-245">Semimonthly</span></span>       | <span data-ttu-id="f9472-246">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-246">Plan start date</span></span>      | <span data-ttu-id="f9472-247">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="f9472-247">End of accrual period</span></span> |

<span data-ttu-id="f9472-248">Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f9472-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="f9472-249">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-249">**Results**</span></span>

| <span data-ttu-id="f9472-250">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-250">Accrual amount</span></span> | <span data-ttu-id="f9472-251">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-251">Minimum balance</span></span> | <span data-ttu-id="f9472-252">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-252">Maximum carry-forward</span></span> | <span data-ttu-id="f9472-253">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-253">Request amount</span></span> | <span data-ttu-id="f9472-254">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="f9472-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="f9472-255">5</span><span class="sxs-lookup"><span data-stu-id="f9472-255">5</span></span>              | <span data-ttu-id="f9472-256">0</span><span class="sxs-lookup"><span data-stu-id="f9472-256">0</span></span>               | <span data-ttu-id="f9472-257">120</span><span class="sxs-lookup"><span data-stu-id="f9472-257">120</span></span>                   | <span data-ttu-id="f9472-258">8</span><span class="sxs-lookup"><span data-stu-id="f9472-258">8</span></span>              | <span data-ttu-id="f9472-259">7</span><span class="sxs-lookup"><span data-stu-id="f9472-259">7</span></span>                                |

<span data-ttu-id="f9472-260">Gjeldende saldo (7) = avsetningsbeløp (5 x 3) – forespurt beløp (8)</span><span class="sxs-lookup"><span data-stu-id="f9472-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="f9472-261">Prognosesaldo</span><span class="sxs-lookup"><span data-stu-id="f9472-261">Forecasted balance</span></span>

<span data-ttu-id="f9472-262">*Prognosesaldo* er hvor mye permisjon som er tilgjengelig på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="f9472-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="f9472-263">Avsetninger og overføringsjusteringer er anslått frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="f9472-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="f9472-264">Følgende formel brukes:</span><span class="sxs-lookup"><span data-stu-id="f9472-264">The following formula is used:</span></span>

<span data-ttu-id="f9472-265">Mandag prognosesaldo = gjeldende saldo – forespørsler + avsetninger – overføringsjustering</span><span class="sxs-lookup"><span data-stu-id="f9472-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="f9472-266">Eksempler på prognosesaldoer</span><span class="sxs-lookup"><span data-stu-id="f9472-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="f9472-267">Årsplan</span><span class="sxs-lookup"><span data-stu-id="f9472-267">Annual plan</span></span>

<span data-ttu-id="f9472-268">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-268">**Plan setup**</span></span>

| <span data-ttu-id="f9472-269">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-269">Plan start date</span></span> | <span data-ttu-id="f9472-270">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-270">Enrollment date</span></span> | <span data-ttu-id="f9472-271">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-271">Accrual frequency</span></span> | <span data-ttu-id="f9472-272">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-272">Accrual period basis</span></span> | <span data-ttu-id="f9472-273">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f9472-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-274">1/1/2018</span></span>        | <span data-ttu-id="f9472-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-275">1/1/2018</span></span>        | <span data-ttu-id="f9472-276">Årlig</span><span class="sxs-lookup"><span data-stu-id="f9472-276">Annual</span></span>            | <span data-ttu-id="f9472-277">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-277">Plan start date</span></span>      | <span data-ttu-id="f9472-278">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="f9472-278">End of accrual period</span></span> |

<span data-ttu-id="f9472-279">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f9472-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f9472-280">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-280">**Results**</span></span>

| <span data-ttu-id="f9472-281">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-281">Accrual amount</span></span> | <span data-ttu-id="f9472-282">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-282">Minimum balance</span></span> | <span data-ttu-id="f9472-283">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-283">Maximum carry-forward</span></span> | <span data-ttu-id="f9472-284">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-284">Current balance</span></span> | <span data-ttu-id="f9472-285">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="f9472-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="f9472-286">20</span><span class="sxs-lookup"><span data-stu-id="f9472-286">20</span></span>             | <span data-ttu-id="f9472-287">0</span><span class="sxs-lookup"><span data-stu-id="f9472-287">0</span></span>               | <span data-ttu-id="f9472-288">20</span><span class="sxs-lookup"><span data-stu-id="f9472-288">20</span></span>                    | <span data-ttu-id="f9472-289">40</span><span class="sxs-lookup"><span data-stu-id="f9472-289">40</span></span>              | <span data-ttu-id="f9472-290">40</span><span class="sxs-lookup"><span data-stu-id="f9472-290">40</span></span>                                   |

<span data-ttu-id="f9472-291">Prognosesaldo (40) = avsetningsbeløp (20) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="f9472-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="f9472-292">Halvmånedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-292">Semimonthly plan</span></span>

<span data-ttu-id="f9472-293">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-293">**Plan setup**</span></span>

| <span data-ttu-id="f9472-294">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-294">Plan start date</span></span> | <span data-ttu-id="f9472-295">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-295">Enrollment date</span></span> | <span data-ttu-id="f9472-296">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-296">Accrual frequency</span></span> | <span data-ttu-id="f9472-297">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-297">Accrual period basis</span></span> | <span data-ttu-id="f9472-298">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f9472-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-299">1/1/2018</span></span>        | <span data-ttu-id="f9472-300">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-300">2/1/2018</span></span>        | <span data-ttu-id="f9472-301">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-301">Semimonthly</span></span>       | <span data-ttu-id="f9472-302">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-302">Plan start date</span></span>      | <span data-ttu-id="f9472-303">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="f9472-303">End of accrual period</span></span> |

<span data-ttu-id="f9472-304">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f9472-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f9472-305">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-305">**Results**</span></span>

| <span data-ttu-id="f9472-306">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-306">Accrual amount</span></span> | <span data-ttu-id="f9472-307">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-307">Minimum balance</span></span> | <span data-ttu-id="f9472-308">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-308">Maximum carry-forward</span></span> | <span data-ttu-id="f9472-309">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-309">Current balance</span></span> | <span data-ttu-id="f9472-310">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="f9472-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="f9472-311">5</span><span class="sxs-lookup"><span data-stu-id="f9472-311">5</span></span>              | <span data-ttu-id="f9472-312">0</span><span class="sxs-lookup"><span data-stu-id="f9472-312">0</span></span>               | <span data-ttu-id="f9472-313">20</span><span class="sxs-lookup"><span data-stu-id="f9472-313">20</span></span>                    | <span data-ttu-id="f9472-314">40</span><span class="sxs-lookup"><span data-stu-id="f9472-314">40</span></span>              | <span data-ttu-id="f9472-315">35</span><span class="sxs-lookup"><span data-stu-id="f9472-315">35</span></span>                                   |

<span data-ttu-id="f9472-316">Prognosesaldo (35) = avsetningsbeløp (5 x 3) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="f9472-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="f9472-317">Månedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-317">Monthly plan</span></span>

<span data-ttu-id="f9472-318">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-318">**Plan setup**</span></span>

| <span data-ttu-id="f9472-319">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-319">Plan start date</span></span> | <span data-ttu-id="f9472-320">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-320">Enrollment date</span></span> | <span data-ttu-id="f9472-321">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-321">Accrual frequency</span></span> | <span data-ttu-id="f9472-322">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-322">Accrual period basis</span></span> | <span data-ttu-id="f9472-323">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f9472-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-324">1/1/2018</span></span>        | <span data-ttu-id="f9472-325">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-325">2/1/2018</span></span>        | <span data-ttu-id="f9472-326">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-326">Semimonthly</span></span>       | <span data-ttu-id="f9472-327">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-327">Plan start date</span></span>      | <span data-ttu-id="f9472-328">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="f9472-328">End of accrual period</span></span> |

<span data-ttu-id="f9472-329">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f9472-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f9472-330">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-330">**Results**</span></span>

| <span data-ttu-id="f9472-331">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-331">Accrual amount</span></span> | <span data-ttu-id="f9472-332">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-332">Minimum balance</span></span> | <span data-ttu-id="f9472-333">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="f9472-333">Maximum carry-forward</span></span> | <span data-ttu-id="f9472-334">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="f9472-334">Current balance</span></span> | <span data-ttu-id="f9472-335">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="f9472-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="f9472-336">10</span><span class="sxs-lookup"><span data-stu-id="f9472-336">10</span></span>             | <span data-ttu-id="f9472-337">0</span><span class="sxs-lookup"><span data-stu-id="f9472-337">0</span></span>               | <span data-ttu-id="f9472-338">20</span><span class="sxs-lookup"><span data-stu-id="f9472-338">20</span></span>                    | <span data-ttu-id="f9472-339">40</span><span class="sxs-lookup"><span data-stu-id="f9472-339">40</span></span>              | <span data-ttu-id="f9472-340">30</span><span class="sxs-lookup"><span data-stu-id="f9472-340">30</span></span>                                   |

<span data-ttu-id="f9472-341">Prognosesaldo (30) = avsetningsbeløp (10 x 1) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="f9472-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="f9472-342">Eksempler på fordelingssaldo</span><span class="sxs-lookup"><span data-stu-id="f9472-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="f9472-343">Fordelt månedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-343">Prorated monthly plan</span></span>

<span data-ttu-id="f9472-344">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-344">**Plan setup**</span></span>

| <span data-ttu-id="f9472-345">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-345">Plan start date</span></span> | <span data-ttu-id="f9472-346">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-346">Accrual frequency</span></span> | <span data-ttu-id="f9472-347">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="f9472-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-348">1/1/2018</span></span>        | <span data-ttu-id="f9472-349">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-349">Monthly</span></span>           | <span data-ttu-id="f9472-350">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-350">Plan start date</span></span>      |

<span data-ttu-id="f9472-351">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-351">**Results**</span></span>

| <span data-ttu-id="f9472-352">Ansatt</span><span class="sxs-lookup"><span data-stu-id="f9472-352">Employee</span></span>            | <span data-ttu-id="f9472-353">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="f9472-353">Months of service</span></span> | <span data-ttu-id="f9472-354">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-354">Enrollment date</span></span> | <span data-ttu-id="f9472-355">Startdato</span><span class="sxs-lookup"><span data-stu-id="f9472-355">Start date</span></span> | <span data-ttu-id="f9472-356">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-356">Accrual amount</span></span> | <span data-ttu-id="f9472-357">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-357">Process accrual</span></span> | <span data-ttu-id="f9472-358">Beholdning</span><span class="sxs-lookup"><span data-stu-id="f9472-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="f9472-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="f9472-359">Jeannette Nicholson</span></span> | <span data-ttu-id="f9472-360">0,00</span><span class="sxs-lookup"><span data-stu-id="f9472-360">0.00</span></span>              | <span data-ttu-id="f9472-361">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-361">6/1/2018</span></span>        | <span data-ttu-id="f9472-362">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-362">6/1/2018</span></span>   | <span data-ttu-id="f9472-363">1,00</span><span class="sxs-lookup"><span data-stu-id="f9472-363">1.00</span></span>           | <span data-ttu-id="f9472-364">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-364">9/1/2018</span></span>        | <span data-ttu-id="f9472-365">3,00</span><span class="sxs-lookup"><span data-stu-id="f9472-365">3.00</span></span>    |
| <span data-ttu-id="f9472-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="f9472-366">Jay Norman</span></span>          | <span data-ttu-id="f9472-367">0,00</span><span class="sxs-lookup"><span data-stu-id="f9472-367">0.00</span></span>              | <span data-ttu-id="f9472-368">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-368">6/15/2018</span></span>       | <span data-ttu-id="f9472-369">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-369">6/15/2018</span></span>  | <span data-ttu-id="f9472-370">1,00</span><span class="sxs-lookup"><span data-stu-id="f9472-370">1.00</span></span>           | <span data-ttu-id="f9472-371">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-371">9/1/2018</span></span>        | <span data-ttu-id="f9472-372">2.53</span><span class="sxs-lookup"><span data-stu-id="f9472-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="f9472-373">Full avsetning, månedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-373">Full accrual monthly plan</span></span>

<span data-ttu-id="f9472-374">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-374">**Plan setup**</span></span>

| <span data-ttu-id="f9472-375">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-375">Plan start date</span></span> | <span data-ttu-id="f9472-376">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-376">Accrual frequency</span></span> | <span data-ttu-id="f9472-377">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="f9472-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-378">1/1/2018</span></span>        | <span data-ttu-id="f9472-379">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-379">Monthly</span></span>           | <span data-ttu-id="f9472-380">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-380">Plan start date</span></span>      |

<span data-ttu-id="f9472-381">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-381">**Results**</span></span>

| <span data-ttu-id="f9472-382">Ansatt</span><span class="sxs-lookup"><span data-stu-id="f9472-382">Employee</span></span>            | <span data-ttu-id="f9472-383">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="f9472-383">Months of service</span></span> | <span data-ttu-id="f9472-384">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-384">Enrollment date</span></span> | <span data-ttu-id="f9472-385">Startdato</span><span class="sxs-lookup"><span data-stu-id="f9472-385">Start date</span></span> | <span data-ttu-id="f9472-386">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-386">Accrual amount</span></span> | <span data-ttu-id="f9472-387">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-387">Process accrual</span></span> | <span data-ttu-id="f9472-388">Beholdning</span><span class="sxs-lookup"><span data-stu-id="f9472-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="f9472-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="f9472-389">Jeannette Nicholson</span></span> | <span data-ttu-id="f9472-390">0,00</span><span class="sxs-lookup"><span data-stu-id="f9472-390">0.00</span></span>              | <span data-ttu-id="f9472-391">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-391">6/1/2018</span></span>        | <span data-ttu-id="f9472-392">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-392">6/1/2018</span></span>   | <span data-ttu-id="f9472-393">1,00</span><span class="sxs-lookup"><span data-stu-id="f9472-393">1.00</span></span>           | <span data-ttu-id="f9472-394">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-394">9/1/2018</span></span>        | <span data-ttu-id="f9472-395">3,00</span><span class="sxs-lookup"><span data-stu-id="f9472-395">3.00</span></span>    |
| <span data-ttu-id="f9472-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="f9472-396">Jay Norman</span></span>          | <span data-ttu-id="f9472-397">0,00</span><span class="sxs-lookup"><span data-stu-id="f9472-397">0.00</span></span>              | <span data-ttu-id="f9472-398">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-398">6/15/2018</span></span>       | <span data-ttu-id="f9472-399">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-399">6/15/2018</span></span>  | <span data-ttu-id="f9472-400">1,00</span><span class="sxs-lookup"><span data-stu-id="f9472-400">1.00</span></span>           | <span data-ttu-id="f9472-401">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-401">9/1/2018</span></span>        | <span data-ttu-id="f9472-402">3,00</span><span class="sxs-lookup"><span data-stu-id="f9472-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="f9472-403">Ingen avsetning, månedlig plan</span><span class="sxs-lookup"><span data-stu-id="f9472-403">No accrual monthly plan</span></span>

<span data-ttu-id="f9472-404">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="f9472-404">**Plan setup**</span></span>

| <span data-ttu-id="f9472-405">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-405">Plan start date</span></span> | <span data-ttu-id="f9472-406">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="f9472-406">Accrual frequency</span></span> | <span data-ttu-id="f9472-407">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="f9472-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="f9472-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-408">1/1/2018</span></span>        | <span data-ttu-id="f9472-409">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f9472-409">Monthly</span></span>           | <span data-ttu-id="f9472-410">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="f9472-410">Plan start date</span></span>      |

<span data-ttu-id="f9472-411">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="f9472-411">**Results**</span></span>

| <span data-ttu-id="f9472-412">Ansatt</span><span class="sxs-lookup"><span data-stu-id="f9472-412">Employee</span></span>            | <span data-ttu-id="f9472-413">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="f9472-413">Months of service</span></span> | <span data-ttu-id="f9472-414">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="f9472-414">Enrollment date</span></span> | <span data-ttu-id="f9472-415">Startdato</span><span class="sxs-lookup"><span data-stu-id="f9472-415">Start date</span></span> | <span data-ttu-id="f9472-416">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="f9472-416">Accrual amount</span></span> | <span data-ttu-id="f9472-417">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="f9472-417">Process accrual</span></span> | <span data-ttu-id="f9472-418">Beholdning</span><span class="sxs-lookup"><span data-stu-id="f9472-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="f9472-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="f9472-419">Jeannette Nicholson</span></span> | <span data-ttu-id="f9472-420">0,00</span><span class="sxs-lookup"><span data-stu-id="f9472-420">0.00</span></span>              | <span data-ttu-id="f9472-421">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-421">6/1/2018</span></span>        | <span data-ttu-id="f9472-422">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-422">6/1/2018</span></span>   | <span data-ttu-id="f9472-423">1,00</span><span class="sxs-lookup"><span data-stu-id="f9472-423">1.00</span></span>           | <span data-ttu-id="f9472-424">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-424">9/1/2018</span></span>        | <span data-ttu-id="f9472-425">3,00</span><span class="sxs-lookup"><span data-stu-id="f9472-425">3.00</span></span>    |
| <span data-ttu-id="f9472-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="f9472-426">Jay Norman</span></span>          | <span data-ttu-id="f9472-427">0,00</span><span class="sxs-lookup"><span data-stu-id="f9472-427">0.00</span></span>              | <span data-ttu-id="f9472-428">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-428">6/15/2018</span></span>       | <span data-ttu-id="f9472-429">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-429">6/15/2018</span></span>  | <span data-ttu-id="f9472-430">1,00</span><span class="sxs-lookup"><span data-stu-id="f9472-430">1.00</span></span>           | <span data-ttu-id="f9472-431">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="f9472-431">9/1/2018</span></span>        | <span data-ttu-id="f9472-432">2.00</span><span class="sxs-lookup"><span data-stu-id="f9472-432">2.00</span></span>    |
