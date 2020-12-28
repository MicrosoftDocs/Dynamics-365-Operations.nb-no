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
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462142"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="dbd78-103">Begreper for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="dbd78-103">Leave and absence concepts</span></span>

<span data-ttu-id="dbd78-104">Begreper og termer som er beskrevet i dette emnet, kan hjelpe deg med å finne ut hvordan en ansatt belønnes med avspasering, og hvordan den ansattes tidssaldoer beregnes.</span><span class="sxs-lookup"><span data-stu-id="dbd78-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="dbd78-105">Hvis du vil ha mer informasjon om permisjons- og fraværsadministrasjon, kan du se [Administrasjon av permisjon og fravær](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="dbd78-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="dbd78-106">Permisjonsplandetaljer</span><span class="sxs-lookup"><span data-stu-id="dbd78-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="dbd78-107">Startdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-107">Start date</span></span>

<span data-ttu-id="dbd78-108">Startdatoen er datoen som avsetningsbehandlingen starter på.</span><span class="sxs-lookup"><span data-stu-id="dbd78-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="dbd78-109">Startdatoen fungerer også som merkedato for å beregne overføringsbeløp.</span><span class="sxs-lookup"><span data-stu-id="dbd78-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="dbd78-110">Avsetninger</span><span class="sxs-lookup"><span data-stu-id="dbd78-110">Accruals</span></span>

<span data-ttu-id="dbd78-111">Avsetninger bestemmer når og hvor ofte en ansatt belønnes med avspasering.</span><span class="sxs-lookup"><span data-stu-id="dbd78-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="dbd78-112">Retningslinjer om når avsetningene skal tildeles og policyer om fordeling, defineres i **Avsetninger**-delen når du definerer permisjons- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="dbd78-113">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-113">Accrual frequency</span></span>

<span data-ttu-id="dbd78-114">Avsetningsfrekvensen definerer hvor ofte permisjon avsettes eller tildeles.</span><span class="sxs-lookup"><span data-stu-id="dbd78-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="dbd78-115">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dbd78-115">The following options are available:</span></span>

- <span data-ttu-id="dbd78-116">Daglig</span><span class="sxs-lookup"><span data-stu-id="dbd78-116">Daily</span></span>
- <span data-ttu-id="dbd78-117">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-117">Weekly</span></span>
- <span data-ttu-id="dbd78-118">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="dbd78-118">Biweekly</span></span>
- <span data-ttu-id="dbd78-119">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-119">Semimonthly</span></span>
- <span data-ttu-id="dbd78-120">Månedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-120">Monthly</span></span>
- <span data-ttu-id="dbd78-121">Kvartalsvis</span><span class="sxs-lookup"><span data-stu-id="dbd78-121">Quarterly</span></span>
- <span data-ttu-id="dbd78-122">Hvert halvår</span><span class="sxs-lookup"><span data-stu-id="dbd78-122">Semiannually</span></span>
- <span data-ttu-id="dbd78-123">Årlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-123">Annually</span></span>
- <span data-ttu-id="dbd78-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="dbd78-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="dbd78-125">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-125">Accrual period basis</span></span>

<span data-ttu-id="dbd78-126">Avsetningsperiodegrunnlaget fastsetter datoen som brukes til å beregne avsetningsperioder.</span><span class="sxs-lookup"><span data-stu-id="dbd78-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="dbd78-127">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dbd78-127">The following options are available:</span></span>

- <span data-ttu-id="dbd78-128">**Startdato for plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-128">**Plan start date**</span></span>
- <span data-ttu-id="dbd78-129">**Spesifikk dato for ansatt** – Når dette alternativet er valgt, fastsetter verdien kilden til den opprinnelige datoverdien som brukes til å beregne avsetningsperioder.</span><span class="sxs-lookup"><span data-stu-id="dbd78-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="dbd78-130">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dbd78-130">The following options are available:</span></span>

    - <span data-ttu-id="dbd78-131">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="dbd78-131">Custom</span></span>
    - <span data-ttu-id="dbd78-132">Jubileumsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-132">Anniversary date</span></span>
    - <span data-ttu-id="dbd78-133">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-133">Original hire date</span></span>
    - <span data-ttu-id="dbd78-134">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-134">Seniority date</span></span>
    - <span data-ttu-id="dbd78-135">Arbeiderens justerte startdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="dbd78-136">Arbeiderens startdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="dbd78-137">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-137">Accrual award date</span></span>

<span data-ttu-id="dbd78-138">Belønningsdatoen for avsetning bestemmer når en ansatt tildeles fri.</span><span class="sxs-lookup"><span data-stu-id="dbd78-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="dbd78-139">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dbd78-139">The following options are available:</span></span>

- <span data-ttu-id="dbd78-140">**Sluttdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den siste dagen i belønningsperioden.</span><span class="sxs-lookup"><span data-stu-id="dbd78-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="dbd78-141">Hvis du vil avsette riktig tid, må avsetningsprosessen inkludere hele perioden.</span><span class="sxs-lookup"><span data-stu-id="dbd78-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="dbd78-142">Avsetningsperioden er for eksempel fra 1. januar 2018 til og med 31. januar 2018.</span><span class="sxs-lookup"><span data-stu-id="dbd78-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="dbd78-143">For at januar skal tas med i dette tilfelle, må avsetningen kjøres for 1. februar 2018.</span><span class="sxs-lookup"><span data-stu-id="dbd78-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="dbd78-144">**Startdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den første dagen i belønningsperioden.</span><span class="sxs-lookup"><span data-stu-id="dbd78-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="dbd78-145">Avsetningspolicy ved registrering</span><span class="sxs-lookup"><span data-stu-id="dbd78-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="dbd78-146">Avsetningspolicyen ved registrering angir hvordan avsetning beregnes når ansatte registreres i midten av en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="dbd78-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="dbd78-147">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dbd78-147">The following options are available:</span></span>

- <span data-ttu-id="dbd78-148">**Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager.</span><span class="sxs-lookup"><span data-stu-id="dbd78-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="dbd78-149">Denne differansen brukes når avsetninger behandles.</span><span class="sxs-lookup"><span data-stu-id="dbd78-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="dbd78-150">**Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="dbd78-151">**Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="dbd78-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="dbd78-152">Avsetningspolicy ved avregistrering</span><span class="sxs-lookup"><span data-stu-id="dbd78-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="dbd78-153">Avsetningspolicyen ved avregistrering angir hvordan avsetning beregnes når ansatte avregistreres i midten av en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="dbd78-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="dbd78-154">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dbd78-154">The following options are available:</span></span>

- <span data-ttu-id="dbd78-155">**Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager.</span><span class="sxs-lookup"><span data-stu-id="dbd78-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="dbd78-156">Denne differansen brukes når avsetninger behandles.</span><span class="sxs-lookup"><span data-stu-id="dbd78-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="dbd78-157">**Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="dbd78-158">**Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="dbd78-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="dbd78-159">Avsetningsplan</span><span class="sxs-lookup"><span data-stu-id="dbd78-159">Accrual schedule</span></span>

<span data-ttu-id="dbd78-160">Avsetningsplanen bestemmer hvordan en ansatt skal avsette avspasering, og hvor mye den ansatte skal avsette og overføre.</span><span class="sxs-lookup"><span data-stu-id="dbd78-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="dbd78-161">Lag kan opprettes slik at avspasering tildeles basert på forskjellige nivåer.</span><span class="sxs-lookup"><span data-stu-id="dbd78-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="dbd78-162">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="dbd78-162">Months of service</span></span>

<span data-ttu-id="dbd78-163">**Måneder med jobberfaring**-verdien definerer det minste antallet måneder som ansatte må arbeide for å være berettiget til avsetninger.</span><span class="sxs-lookup"><span data-stu-id="dbd78-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="dbd78-164">Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.</span><span class="sxs-lookup"><span data-stu-id="dbd78-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="dbd78-165">Arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="dbd78-165">Hours worked</span></span>

<span data-ttu-id="dbd78-166">**Arbeidstimer**-verdien definerer det minste antallet timer som ansatte må arbeide per avsetningsperiode for å være berettiget til avsetninger.</span><span class="sxs-lookup"><span data-stu-id="dbd78-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="dbd78-167">Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.</span><span class="sxs-lookup"><span data-stu-id="dbd78-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="dbd78-168">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-168">Accrual amount</span></span>

<span data-ttu-id="dbd78-169">Avsetningsbeløpet er antallet timer eller dager som ansatte skal avsette per periode.</span><span class="sxs-lookup"><span data-stu-id="dbd78-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="dbd78-170">Perioden er basert på avsetningsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="dbd78-171">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-171">Minimum balance</span></span>

<span data-ttu-id="dbd78-172">En negativ verdi kan brukes for minimumssaldoen hvis ansatte kan be om mer permisjon enn de har tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dbd78-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="dbd78-173">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-173">Maximum carry-forward</span></span>

<span data-ttu-id="dbd78-174">Avsetningsprosessen justerer permisjonssaldoer som overskrider maksimal overføringssaldo på merkedagen til startdatoen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="dbd78-175">Tildelingsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-175">Grant amount</span></span>

<span data-ttu-id="dbd78-176">Tildelingsbeløpet er det opprinnelige antallet timer eller dager som ansatte gis når de registrerer seg for permisjonsplanen første gang.</span><span class="sxs-lookup"><span data-stu-id="dbd78-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="dbd78-177">Beløpet avsettes ikke for hver avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="dbd78-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="dbd78-178">Registreringer og saldoer</span><span class="sxs-lookup"><span data-stu-id="dbd78-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="dbd78-179">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-179">Enrollment date</span></span>

<span data-ttu-id="dbd78-180">Registreringsdatoen bestemmer når en ansatt kan begynne å avsette avspasering.</span><span class="sxs-lookup"><span data-stu-id="dbd78-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="dbd78-181">Hvis for eksempel en ansatt registreres i en ferieplan 15. juni 2018, kan vedkommende ikke avsette avspasering før 15. juni 2018.</span><span class="sxs-lookup"><span data-stu-id="dbd78-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="dbd78-182">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-182">Current balance</span></span>

<span data-ttu-id="dbd78-183">Gjeldende saldo er hvor mye permisjon som er tilgjengelig for avspaseringsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="dbd78-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="dbd78-184">Dette beløpet inkluderer avsetninger godkjente forespørsler og justeringer til og med den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="dbd78-185">Eksempler på gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="dbd78-186">Årsplan</span><span class="sxs-lookup"><span data-stu-id="dbd78-186">Annual plan</span></span>

<span data-ttu-id="dbd78-187">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-187">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-188">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-188">Plan start date</span></span> | <span data-ttu-id="dbd78-189">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-189">Enrollment date</span></span> | <span data-ttu-id="dbd78-190">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-190">Accrual frequency</span></span> | <span data-ttu-id="dbd78-191">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-191">Accrual period basis</span></span> | <span data-ttu-id="dbd78-192">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="dbd78-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-193">1/1/2018</span></span>        | <span data-ttu-id="dbd78-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-194">1/1/2018</span></span>        | <span data-ttu-id="dbd78-195">Årlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-195">Annual</span></span>            | <span data-ttu-id="dbd78-196">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-196">Plan start date</span></span>      | <span data-ttu-id="dbd78-197">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="dbd78-197">End of accrual period</span></span> |

<span data-ttu-id="dbd78-198">Avsetninger behandles 1. januar 2019 (1.1.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="dbd78-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="dbd78-199">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-199">**Results**</span></span>

| <span data-ttu-id="dbd78-200">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-200">Accrual amount</span></span> | <span data-ttu-id="dbd78-201">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-201">Minimum balance</span></span> | <span data-ttu-id="dbd78-202">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-202">Maximum carry-forward</span></span> | <span data-ttu-id="dbd78-203">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-203">Request amount</span></span> | <span data-ttu-id="dbd78-204">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="dbd78-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="dbd78-205">200</span><span class="sxs-lookup"><span data-stu-id="dbd78-205">200</span></span>            | <span data-ttu-id="dbd78-206">0</span><span class="sxs-lookup"><span data-stu-id="dbd78-206">0</span></span>               | <span data-ttu-id="dbd78-207">120</span><span class="sxs-lookup"><span data-stu-id="dbd78-207">120</span></span>                   | <span data-ttu-id="dbd78-208">40</span><span class="sxs-lookup"><span data-stu-id="dbd78-208">40</span></span>             | <span data-ttu-id="dbd78-209">160</span><span class="sxs-lookup"><span data-stu-id="dbd78-209">160</span></span>                              |

<span data-ttu-id="dbd78-210">Gjeldende saldo (160) = avsetningsbeløp (200) – forespurt beløp (40)</span><span class="sxs-lookup"><span data-stu-id="dbd78-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="dbd78-211">Halvmånedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-211">Semimonthly plan</span></span>

<span data-ttu-id="dbd78-212">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-212">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-213">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-213">Plan start date</span></span> | <span data-ttu-id="dbd78-214">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-214">Enrollment date</span></span> | <span data-ttu-id="dbd78-215">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-215">Accrual frequency</span></span> | <span data-ttu-id="dbd78-216">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-216">Accrual period basis</span></span> | <span data-ttu-id="dbd78-217">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="dbd78-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-218">1/1/2018</span></span>        | <span data-ttu-id="dbd78-219">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-219">2/1/2018</span></span>        | <span data-ttu-id="dbd78-220">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-220">Semimonthly</span></span>       | <span data-ttu-id="dbd78-221">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-221">Plan start date</span></span>      | <span data-ttu-id="dbd78-222">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="dbd78-222">End of accrual period</span></span> |

<span data-ttu-id="dbd78-223">Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="dbd78-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="dbd78-224">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-224">**Results**</span></span>

| <span data-ttu-id="dbd78-225">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-225">Accrual amount</span></span> | <span data-ttu-id="dbd78-226">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-226">Minimum balance</span></span> | <span data-ttu-id="dbd78-227">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-227">Maximum carry-forward</span></span> | <span data-ttu-id="dbd78-228">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-228">Request amount</span></span> | <span data-ttu-id="dbd78-229">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="dbd78-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="dbd78-230">5</span><span class="sxs-lookup"><span data-stu-id="dbd78-230">5</span></span>              | <span data-ttu-id="dbd78-231">0</span><span class="sxs-lookup"><span data-stu-id="dbd78-231">0</span></span>               | <span data-ttu-id="dbd78-232">120</span><span class="sxs-lookup"><span data-stu-id="dbd78-232">120</span></span>                   | <span data-ttu-id="dbd78-233">8</span><span class="sxs-lookup"><span data-stu-id="dbd78-233">8</span></span>              | <span data-ttu-id="dbd78-234">22</span><span class="sxs-lookup"><span data-stu-id="dbd78-234">22</span></span>                               |

<span data-ttu-id="dbd78-235">Gjeldende saldo (22) = avsetningsbeløp (5 x 6) – forespurt beløp (8)</span><span class="sxs-lookup"><span data-stu-id="dbd78-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="dbd78-236">Månedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-236">Monthly plan</span></span>

<span data-ttu-id="dbd78-237">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-237">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-238">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-238">Plan start date</span></span> | <span data-ttu-id="dbd78-239">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-239">Enrollment date</span></span> | <span data-ttu-id="dbd78-240">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-240">Accrual frequency</span></span> | <span data-ttu-id="dbd78-241">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-241">Accrual period basis</span></span> | <span data-ttu-id="dbd78-242">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="dbd78-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-243">1/1/2018</span></span>        | <span data-ttu-id="dbd78-244">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-244">2/1/2018</span></span>        | <span data-ttu-id="dbd78-245">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-245">Semimonthly</span></span>       | <span data-ttu-id="dbd78-246">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-246">Plan start date</span></span>      | <span data-ttu-id="dbd78-247">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="dbd78-247">End of accrual period</span></span> |

<span data-ttu-id="dbd78-248">Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="dbd78-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="dbd78-249">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-249">**Results**</span></span>

| <span data-ttu-id="dbd78-250">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-250">Accrual amount</span></span> | <span data-ttu-id="dbd78-251">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-251">Minimum balance</span></span> | <span data-ttu-id="dbd78-252">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-252">Maximum carry-forward</span></span> | <span data-ttu-id="dbd78-253">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-253">Request amount</span></span> | <span data-ttu-id="dbd78-254">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="dbd78-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="dbd78-255">5</span><span class="sxs-lookup"><span data-stu-id="dbd78-255">5</span></span>              | <span data-ttu-id="dbd78-256">0</span><span class="sxs-lookup"><span data-stu-id="dbd78-256">0</span></span>               | <span data-ttu-id="dbd78-257">120</span><span class="sxs-lookup"><span data-stu-id="dbd78-257">120</span></span>                   | <span data-ttu-id="dbd78-258">8</span><span class="sxs-lookup"><span data-stu-id="dbd78-258">8</span></span>              | <span data-ttu-id="dbd78-259">7</span><span class="sxs-lookup"><span data-stu-id="dbd78-259">7</span></span>                                |

<span data-ttu-id="dbd78-260">Gjeldende saldo (7) = avsetningsbeløp (5 x 3) – forespurt beløp (8)</span><span class="sxs-lookup"><span data-stu-id="dbd78-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="dbd78-261">Prognosesaldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-261">Forecasted balance</span></span>

<span data-ttu-id="dbd78-262">*Prognosesaldo* er hvor mye permisjon som er tilgjengelig på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="dbd78-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="dbd78-263">Avsetninger og overføringsjusteringer er anslått frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="dbd78-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="dbd78-264">Følgende formel brukes:</span><span class="sxs-lookup"><span data-stu-id="dbd78-264">The following formula is used:</span></span>

<span data-ttu-id="dbd78-265">Mandag prognosesaldo = gjeldende saldo – forespørsler + avsetninger – overføringsjustering</span><span class="sxs-lookup"><span data-stu-id="dbd78-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="dbd78-266">Eksempler på prognosesaldoer</span><span class="sxs-lookup"><span data-stu-id="dbd78-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="dbd78-267">Årsplan</span><span class="sxs-lookup"><span data-stu-id="dbd78-267">Annual plan</span></span>

<span data-ttu-id="dbd78-268">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-268">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-269">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-269">Plan start date</span></span> | <span data-ttu-id="dbd78-270">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-270">Enrollment date</span></span> | <span data-ttu-id="dbd78-271">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-271">Accrual frequency</span></span> | <span data-ttu-id="dbd78-272">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-272">Accrual period basis</span></span> | <span data-ttu-id="dbd78-273">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="dbd78-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-274">1/1/2018</span></span>        | <span data-ttu-id="dbd78-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-275">1/1/2018</span></span>        | <span data-ttu-id="dbd78-276">Årlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-276">Annual</span></span>            | <span data-ttu-id="dbd78-277">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-277">Plan start date</span></span>      | <span data-ttu-id="dbd78-278">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="dbd78-278">End of accrual period</span></span> |

<span data-ttu-id="dbd78-279">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="dbd78-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="dbd78-280">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-280">**Results**</span></span>

| <span data-ttu-id="dbd78-281">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-281">Accrual amount</span></span> | <span data-ttu-id="dbd78-282">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-282">Minimum balance</span></span> | <span data-ttu-id="dbd78-283">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-283">Maximum carry-forward</span></span> | <span data-ttu-id="dbd78-284">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-284">Current balance</span></span> | <span data-ttu-id="dbd78-285">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="dbd78-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="dbd78-286">20</span><span class="sxs-lookup"><span data-stu-id="dbd78-286">20</span></span>             | <span data-ttu-id="dbd78-287">0</span><span class="sxs-lookup"><span data-stu-id="dbd78-287">0</span></span>               | <span data-ttu-id="dbd78-288">20</span><span class="sxs-lookup"><span data-stu-id="dbd78-288">20</span></span>                    | <span data-ttu-id="dbd78-289">40</span><span class="sxs-lookup"><span data-stu-id="dbd78-289">40</span></span>              | <span data-ttu-id="dbd78-290">40</span><span class="sxs-lookup"><span data-stu-id="dbd78-290">40</span></span>                                   |

<span data-ttu-id="dbd78-291">Prognosesaldo (40) = avsetningsbeløp (20) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="dbd78-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="dbd78-292">Halvmånedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-292">Semimonthly plan</span></span>

<span data-ttu-id="dbd78-293">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-293">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-294">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-294">Plan start date</span></span> | <span data-ttu-id="dbd78-295">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-295">Enrollment date</span></span> | <span data-ttu-id="dbd78-296">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-296">Accrual frequency</span></span> | <span data-ttu-id="dbd78-297">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-297">Accrual period basis</span></span> | <span data-ttu-id="dbd78-298">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="dbd78-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-299">1/1/2018</span></span>        | <span data-ttu-id="dbd78-300">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-300">2/1/2018</span></span>        | <span data-ttu-id="dbd78-301">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-301">Semimonthly</span></span>       | <span data-ttu-id="dbd78-302">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-302">Plan start date</span></span>      | <span data-ttu-id="dbd78-303">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="dbd78-303">End of accrual period</span></span> |

<span data-ttu-id="dbd78-304">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="dbd78-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="dbd78-305">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-305">**Results**</span></span>

| <span data-ttu-id="dbd78-306">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-306">Accrual amount</span></span> | <span data-ttu-id="dbd78-307">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-307">Minimum balance</span></span> | <span data-ttu-id="dbd78-308">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-308">Maximum carry-forward</span></span> | <span data-ttu-id="dbd78-309">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-309">Current balance</span></span> | <span data-ttu-id="dbd78-310">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="dbd78-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="dbd78-311">5</span><span class="sxs-lookup"><span data-stu-id="dbd78-311">5</span></span>              | <span data-ttu-id="dbd78-312">0</span><span class="sxs-lookup"><span data-stu-id="dbd78-312">0</span></span>               | <span data-ttu-id="dbd78-313">20</span><span class="sxs-lookup"><span data-stu-id="dbd78-313">20</span></span>                    | <span data-ttu-id="dbd78-314">40</span><span class="sxs-lookup"><span data-stu-id="dbd78-314">40</span></span>              | <span data-ttu-id="dbd78-315">35</span><span class="sxs-lookup"><span data-stu-id="dbd78-315">35</span></span>                                   |

<span data-ttu-id="dbd78-316">Prognosesaldo (35) = avsetningsbeløp (5 x 3) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="dbd78-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="dbd78-317">Månedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-317">Monthly plan</span></span>

<span data-ttu-id="dbd78-318">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-318">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-319">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-319">Plan start date</span></span> | <span data-ttu-id="dbd78-320">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-320">Enrollment date</span></span> | <span data-ttu-id="dbd78-321">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-321">Accrual frequency</span></span> | <span data-ttu-id="dbd78-322">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-322">Accrual period basis</span></span> | <span data-ttu-id="dbd78-323">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="dbd78-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-324">1/1/2018</span></span>        | <span data-ttu-id="dbd78-325">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-325">2/1/2018</span></span>        | <span data-ttu-id="dbd78-326">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-326">Semimonthly</span></span>       | <span data-ttu-id="dbd78-327">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-327">Plan start date</span></span>      | <span data-ttu-id="dbd78-328">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="dbd78-328">End of accrual period</span></span> |

<span data-ttu-id="dbd78-329">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="dbd78-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="dbd78-330">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-330">**Results**</span></span>

| <span data-ttu-id="dbd78-331">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-331">Accrual amount</span></span> | <span data-ttu-id="dbd78-332">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-332">Minimum balance</span></span> | <span data-ttu-id="dbd78-333">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="dbd78-333">Maximum carry-forward</span></span> | <span data-ttu-id="dbd78-334">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-334">Current balance</span></span> | <span data-ttu-id="dbd78-335">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="dbd78-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="dbd78-336">10</span><span class="sxs-lookup"><span data-stu-id="dbd78-336">10</span></span>             | <span data-ttu-id="dbd78-337">0</span><span class="sxs-lookup"><span data-stu-id="dbd78-337">0</span></span>               | <span data-ttu-id="dbd78-338">20</span><span class="sxs-lookup"><span data-stu-id="dbd78-338">20</span></span>                    | <span data-ttu-id="dbd78-339">40</span><span class="sxs-lookup"><span data-stu-id="dbd78-339">40</span></span>              | <span data-ttu-id="dbd78-340">30</span><span class="sxs-lookup"><span data-stu-id="dbd78-340">30</span></span>                                   |

<span data-ttu-id="dbd78-341">Prognosesaldo (30) = avsetningsbeløp (10 x 1) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="dbd78-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="dbd78-342">Eksempler på fordelingssaldo</span><span class="sxs-lookup"><span data-stu-id="dbd78-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="dbd78-343">Fordelt månedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-343">Prorated monthly plan</span></span>

<span data-ttu-id="dbd78-344">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-344">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-345">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-345">Plan start date</span></span> | <span data-ttu-id="dbd78-346">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-346">Accrual frequency</span></span> | <span data-ttu-id="dbd78-347">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="dbd78-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-348">1/1/2018</span></span>        | <span data-ttu-id="dbd78-349">Månedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-349">Monthly</span></span>           | <span data-ttu-id="dbd78-350">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-350">Plan start date</span></span>      |

<span data-ttu-id="dbd78-351">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-351">**Results**</span></span>

| <span data-ttu-id="dbd78-352">Ansatt</span><span class="sxs-lookup"><span data-stu-id="dbd78-352">Employee</span></span>            | <span data-ttu-id="dbd78-353">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="dbd78-353">Months of service</span></span> | <span data-ttu-id="dbd78-354">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-354">Enrollment date</span></span> | <span data-ttu-id="dbd78-355">Startdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-355">Start date</span></span> | <span data-ttu-id="dbd78-356">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-356">Accrual amount</span></span> | <span data-ttu-id="dbd78-357">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-357">Process accrual</span></span> | <span data-ttu-id="dbd78-358">Beholdning</span><span class="sxs-lookup"><span data-stu-id="dbd78-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="dbd78-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="dbd78-359">Jeannette Nicholson</span></span> | <span data-ttu-id="dbd78-360">0,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-360">0.00</span></span>              | <span data-ttu-id="dbd78-361">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-361">6/1/2018</span></span>        | <span data-ttu-id="dbd78-362">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-362">6/1/2018</span></span>   | <span data-ttu-id="dbd78-363">1,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-363">1.00</span></span>           | <span data-ttu-id="dbd78-364">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-364">9/1/2018</span></span>        | <span data-ttu-id="dbd78-365">3,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-365">3.00</span></span>    |
| <span data-ttu-id="dbd78-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="dbd78-366">Jay Norman</span></span>          | <span data-ttu-id="dbd78-367">0,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-367">0.00</span></span>              | <span data-ttu-id="dbd78-368">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-368">6/15/2018</span></span>       | <span data-ttu-id="dbd78-369">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-369">6/15/2018</span></span>  | <span data-ttu-id="dbd78-370">1,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-370">1.00</span></span>           | <span data-ttu-id="dbd78-371">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-371">9/1/2018</span></span>        | <span data-ttu-id="dbd78-372">2.53</span><span class="sxs-lookup"><span data-stu-id="dbd78-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="dbd78-373">Full avsetning, månedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-373">Full accrual monthly plan</span></span>

<span data-ttu-id="dbd78-374">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-374">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-375">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-375">Plan start date</span></span> | <span data-ttu-id="dbd78-376">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-376">Accrual frequency</span></span> | <span data-ttu-id="dbd78-377">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="dbd78-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-378">1/1/2018</span></span>        | <span data-ttu-id="dbd78-379">Månedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-379">Monthly</span></span>           | <span data-ttu-id="dbd78-380">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-380">Plan start date</span></span>      |

<span data-ttu-id="dbd78-381">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-381">**Results**</span></span>

| <span data-ttu-id="dbd78-382">Ansatt</span><span class="sxs-lookup"><span data-stu-id="dbd78-382">Employee</span></span>            | <span data-ttu-id="dbd78-383">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="dbd78-383">Months of service</span></span> | <span data-ttu-id="dbd78-384">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-384">Enrollment date</span></span> | <span data-ttu-id="dbd78-385">Startdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-385">Start date</span></span> | <span data-ttu-id="dbd78-386">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-386">Accrual amount</span></span> | <span data-ttu-id="dbd78-387">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-387">Process accrual</span></span> | <span data-ttu-id="dbd78-388">Beholdning</span><span class="sxs-lookup"><span data-stu-id="dbd78-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="dbd78-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="dbd78-389">Jeannette Nicholson</span></span> | <span data-ttu-id="dbd78-390">0,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-390">0.00</span></span>              | <span data-ttu-id="dbd78-391">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-391">6/1/2018</span></span>        | <span data-ttu-id="dbd78-392">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-392">6/1/2018</span></span>   | <span data-ttu-id="dbd78-393">1,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-393">1.00</span></span>           | <span data-ttu-id="dbd78-394">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-394">9/1/2018</span></span>        | <span data-ttu-id="dbd78-395">3,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-395">3.00</span></span>    |
| <span data-ttu-id="dbd78-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="dbd78-396">Jay Norman</span></span>          | <span data-ttu-id="dbd78-397">0,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-397">0.00</span></span>              | <span data-ttu-id="dbd78-398">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-398">6/15/2018</span></span>       | <span data-ttu-id="dbd78-399">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-399">6/15/2018</span></span>  | <span data-ttu-id="dbd78-400">1,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-400">1.00</span></span>           | <span data-ttu-id="dbd78-401">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-401">9/1/2018</span></span>        | <span data-ttu-id="dbd78-402">3,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="dbd78-403">Ingen avsetning, månedlig plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-403">No accrual monthly plan</span></span>

<span data-ttu-id="dbd78-404">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="dbd78-404">**Plan setup**</span></span>

| <span data-ttu-id="dbd78-405">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-405">Plan start date</span></span> | <span data-ttu-id="dbd78-406">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="dbd78-406">Accrual frequency</span></span> | <span data-ttu-id="dbd78-407">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="dbd78-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="dbd78-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-408">1/1/2018</span></span>        | <span data-ttu-id="dbd78-409">Månedlig</span><span class="sxs-lookup"><span data-stu-id="dbd78-409">Monthly</span></span>           | <span data-ttu-id="dbd78-410">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="dbd78-410">Plan start date</span></span>      |

<span data-ttu-id="dbd78-411">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="dbd78-411">**Results**</span></span>

| <span data-ttu-id="dbd78-412">Ansatt</span><span class="sxs-lookup"><span data-stu-id="dbd78-412">Employee</span></span>            | <span data-ttu-id="dbd78-413">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="dbd78-413">Months of service</span></span> | <span data-ttu-id="dbd78-414">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-414">Enrollment date</span></span> | <span data-ttu-id="dbd78-415">Startdato</span><span class="sxs-lookup"><span data-stu-id="dbd78-415">Start date</span></span> | <span data-ttu-id="dbd78-416">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dbd78-416">Accrual amount</span></span> | <span data-ttu-id="dbd78-417">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="dbd78-417">Process accrual</span></span> | <span data-ttu-id="dbd78-418">Beholdning</span><span class="sxs-lookup"><span data-stu-id="dbd78-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="dbd78-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="dbd78-419">Jeannette Nicholson</span></span> | <span data-ttu-id="dbd78-420">0,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-420">0.00</span></span>              | <span data-ttu-id="dbd78-421">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-421">6/1/2018</span></span>        | <span data-ttu-id="dbd78-422">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-422">6/1/2018</span></span>   | <span data-ttu-id="dbd78-423">1,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-423">1.00</span></span>           | <span data-ttu-id="dbd78-424">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-424">9/1/2018</span></span>        | <span data-ttu-id="dbd78-425">3,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-425">3.00</span></span>    |
| <span data-ttu-id="dbd78-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="dbd78-426">Jay Norman</span></span>          | <span data-ttu-id="dbd78-427">0,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-427">0.00</span></span>              | <span data-ttu-id="dbd78-428">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-428">6/15/2018</span></span>       | <span data-ttu-id="dbd78-429">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-429">6/15/2018</span></span>  | <span data-ttu-id="dbd78-430">1,00</span><span class="sxs-lookup"><span data-stu-id="dbd78-430">1.00</span></span>           | <span data-ttu-id="dbd78-431">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="dbd78-431">9/1/2018</span></span>        | <span data-ttu-id="dbd78-432">2.00</span><span class="sxs-lookup"><span data-stu-id="dbd78-432">2.00</span></span>    |
