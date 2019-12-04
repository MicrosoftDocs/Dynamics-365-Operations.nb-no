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
ms.openlocfilehash: 3dbf5807a213e425b24d5a4809df694393faeb9b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832774"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="3e0a4-103">Begreper for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="3e0a4-103">Leave and absence concepts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e0a4-104">Begreper og termer som er beskrevet i dette emnet, kan hjelpe deg med å finne ut hvordan en ansatt belønnes med avspasering, og hvordan den ansattes tidssaldoer beregnes.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="3e0a4-105">Hvis du vil ha mer informasjon om permisjons- og fraværsadministrasjon, kan du se [Administrasjon av permisjon og fravær](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="3e0a4-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="3e0a4-106">Permisjonsplandetaljer</span><span class="sxs-lookup"><span data-stu-id="3e0a4-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="3e0a4-107">Startdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-107">Start date</span></span>

<span data-ttu-id="3e0a4-108">Startdatoen er datoen som avsetningsbehandlingen starter på.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="3e0a4-109">Startdatoen fungerer også som merkedato for å beregne overføringsbeløp.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="3e0a4-110">Avsetninger</span><span class="sxs-lookup"><span data-stu-id="3e0a4-110">Accruals</span></span>

<span data-ttu-id="3e0a4-111">Avsetninger bestemmer når og hvor ofte en ansatt belønnes med avspasering.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="3e0a4-112">Retningslinjer om når avsetningene skal tildeles og policyer om fordeling, defineres i **Avsetninger**-delen når du definerer permisjons- og fraværsplanen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="3e0a4-113">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-113">Accrual frequency</span></span>

<span data-ttu-id="3e0a4-114">Avsetningsfrekvensen definerer hvor ofte permisjon avsettes eller tildeles.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="3e0a4-115">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-115">The following options are available:</span></span>

- <span data-ttu-id="3e0a4-116">Daglig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-116">Daily</span></span>
- <span data-ttu-id="3e0a4-117">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-117">Weekly</span></span>
- <span data-ttu-id="3e0a4-118">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="3e0a4-118">Biweekly</span></span>
- <span data-ttu-id="3e0a4-119">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-119">Semimonthly</span></span>
- <span data-ttu-id="3e0a4-120">Månedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-120">Monthly</span></span>
- <span data-ttu-id="3e0a4-121">Kvartalsvis</span><span class="sxs-lookup"><span data-stu-id="3e0a4-121">Quarterly</span></span>
- <span data-ttu-id="3e0a4-122">Hvert halvår</span><span class="sxs-lookup"><span data-stu-id="3e0a4-122">Semiannually</span></span>
- <span data-ttu-id="3e0a4-123">Årlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-123">Annually</span></span>
- <span data-ttu-id="3e0a4-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e0a4-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="3e0a4-125">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-125">Accrual period basis</span></span>

<span data-ttu-id="3e0a4-126">Avsetningsperiodegrunnlaget fastsetter datoen som brukes til å beregne avsetningsperioder.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="3e0a4-127">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-127">The following options are available:</span></span>

- <span data-ttu-id="3e0a4-128">**Startdato for plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-128">**Plan start date**</span></span>
- <span data-ttu-id="3e0a4-129">**Spesifikk dato for ansatt** – Når dette alternativet er valgt, fastsetter verdien kilden til den opprinnelige datoverdien som brukes til å beregne avsetningsperioder.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="3e0a4-130">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-130">The following options are available:</span></span>

    - <span data-ttu-id="3e0a4-131">Egendefinert</span><span class="sxs-lookup"><span data-stu-id="3e0a4-131">Custom</span></span>
    - <span data-ttu-id="3e0a4-132">Jubileumsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-132">Anniversary date</span></span>
    - <span data-ttu-id="3e0a4-133">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-133">Original hire date</span></span>
    - <span data-ttu-id="3e0a4-134">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-134">Seniority date</span></span>
    - <span data-ttu-id="3e0a4-135">Arbeiderens justerte startdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="3e0a4-136">Arbeiderens startdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="3e0a4-137">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-137">Accrual award date</span></span>

<span data-ttu-id="3e0a4-138">Belønningsdatoen for avsetning bestemmer når en ansatt tildeles fri.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="3e0a4-139">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-139">The following options are available:</span></span>

- <span data-ttu-id="3e0a4-140">**Sluttdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den siste dagen i belønningsperioden.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="3e0a4-141">Hvis du vil avsette riktig tid, må avsetningsprosessen inkludere hele perioden.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="3e0a4-142">Avsetningsperioden er for eksempel fra 1. januar 2018 til og med 31. januar 2018.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="3e0a4-143">For at januar skal tas med i dette tilfelle, må avsetningen kjøres for 1. februar 2018.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="3e0a4-144">**Startdato for avsetningsperiode** – Den ansatte blir tildelt avspasering på den første dagen i belønningsperioden.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="3e0a4-145">Avsetningspolicy ved registrering</span><span class="sxs-lookup"><span data-stu-id="3e0a4-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="3e0a4-146">Avsetningspolicyen ved registrering angir hvordan avsetning beregnes når ansatte registreres i midten av en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="3e0a4-147">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-147">The following options are available:</span></span>

- <span data-ttu-id="3e0a4-148">**Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="3e0a4-149">Denne differansen brukes når avsetninger behandles.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="3e0a4-150">**Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="3e0a4-151">**Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="3e0a4-152">Avsetningspolicy ved avregistrering</span><span class="sxs-lookup"><span data-stu-id="3e0a4-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="3e0a4-153">Avsetningspolicyen ved avregistrering angir hvordan avsetning beregnes når ansatte avregistreres i midten av en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="3e0a4-154">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-154">The following options are available:</span></span>

- <span data-ttu-id="3e0a4-155">**Fordelt** – Datointervallet mellom registreringsdatoen og startdatoen brukes til å fastsette forskjellen i dager.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="3e0a4-156">Denne differansen brukes når avsetninger behandles.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="3e0a4-157">**Full avsetning** – Full avsetning, basert på nivået, gis i den første avsetningsbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="3e0a4-158">**Ingen avsetning** – Ingen avsetning gis før neste avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="3e0a4-159">Avsetningsplan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-159">Accrual schedule</span></span>

<span data-ttu-id="3e0a4-160">Avsetningsplanen bestemmer hvordan en ansatt skal avsette avspasering, og hvor mye den ansatte skal avsette og overføre.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="3e0a4-161">Lag kan opprettes slik at avspasering tildeles basert på forskjellige nivåer.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="3e0a4-162">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-162">Months of service</span></span>

<span data-ttu-id="3e0a4-163">**Måneder med jobberfaring**-verdien definerer det minste antallet måneder som ansatte må arbeide for å være berettiget til avsetninger.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="3e0a4-164">Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="3e0a4-165">Arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="3e0a4-165">Hours worked</span></span>

<span data-ttu-id="3e0a4-166">**Arbeidstimer**-verdien definerer det minste antallet timer som ansatte må arbeide per avsetningsperiode for å være berettiget til avsetninger.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="3e0a4-167">Hvis ikke det kreves et minimum for ansatte, setter du verdien til **0**.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="3e0a4-168">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-168">Accrual amount</span></span>

<span data-ttu-id="3e0a4-169">Avsetningsbeløpet er antallet timer eller dager som ansatte skal avsette per periode.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="3e0a4-170">Perioden er basert på avsetningsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="3e0a4-171">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-171">Minimum balance</span></span>

<span data-ttu-id="3e0a4-172">En negativ verdi kan brukes for minimumssaldoen hvis ansatte kan be om mer permisjon enn de har tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="3e0a4-173">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-173">Maximum carry-forward</span></span>

<span data-ttu-id="3e0a4-174">Avsetningsprosessen justerer permisjonssaldoer som overskrider maksimal overføringssaldo på merkedagen til startdatoen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="3e0a4-175">Tildelingsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-175">Grant amount</span></span>

<span data-ttu-id="3e0a4-176">Tildelingsbeløpet er det opprinnelige antallet timer eller dager som ansatte gis når de registrerer seg for permisjonsplanen første gang.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="3e0a4-177">Beløpet avsettes ikke for hver avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="3e0a4-178">Registreringer og saldoer</span><span class="sxs-lookup"><span data-stu-id="3e0a4-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="3e0a4-179">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-179">Enrollment date</span></span>

<span data-ttu-id="3e0a4-180">Registreringsdatoen bestemmer når en ansatt kan begynne å avsette avspasering.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="3e0a4-181">Hvis for eksempel en ansatt registreres i en ferieplan 15. juni 2018, kan vedkommende ikke avsette avspasering før 15. juni 2018.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="3e0a4-182">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-182">Current balance</span></span>

<span data-ttu-id="3e0a4-183">Gjeldende saldo er hvor mye permisjon som er tilgjengelig for avspaseringsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="3e0a4-184">Dette beløpet inkluderer avsetninger godkjente forespørsler og justeringer til og med den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="3e0a4-185">Eksempler på gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="3e0a4-186">Årsplan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-186">Annual plan</span></span>

<span data-ttu-id="3e0a4-187">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-187">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-188">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-188">Plan start date</span></span> | <span data-ttu-id="3e0a4-189">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-189">Enrollment date</span></span> | <span data-ttu-id="3e0a4-190">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-190">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-191">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-191">Accrual period basis</span></span> | <span data-ttu-id="3e0a4-192">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="3e0a4-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-193">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-194">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-195">Årlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-195">Annual</span></span>            | <span data-ttu-id="3e0a4-196">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-196">Plan start date</span></span>      | <span data-ttu-id="3e0a4-197">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="3e0a4-197">End of accrual period</span></span> |

<span data-ttu-id="3e0a4-198">Avsetninger behandles 1. januar 2019 (1.1.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="3e0a4-199">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-199">**Results**</span></span>

| <span data-ttu-id="3e0a4-200">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-200">Accrual amount</span></span> | <span data-ttu-id="3e0a4-201">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-201">Minimum balance</span></span> | <span data-ttu-id="3e0a4-202">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-202">Maximum carry-forward</span></span> | <span data-ttu-id="3e0a4-203">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-203">Request amount</span></span> | <span data-ttu-id="3e0a4-204">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="3e0a4-205">200</span><span class="sxs-lookup"><span data-stu-id="3e0a4-205">200</span></span>            | <span data-ttu-id="3e0a4-206">0</span><span class="sxs-lookup"><span data-stu-id="3e0a4-206">0</span></span>               | <span data-ttu-id="3e0a4-207">120</span><span class="sxs-lookup"><span data-stu-id="3e0a4-207">120</span></span>                   | <span data-ttu-id="3e0a4-208">40</span><span class="sxs-lookup"><span data-stu-id="3e0a4-208">40</span></span>             | <span data-ttu-id="3e0a4-209">160</span><span class="sxs-lookup"><span data-stu-id="3e0a4-209">160</span></span>                              |

<span data-ttu-id="3e0a4-210">Gjeldende saldo (160) = avsetningsbeløp (200) – forespurt beløp (40)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="3e0a4-211">Halvmånedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-211">Semimonthly plan</span></span>

<span data-ttu-id="3e0a4-212">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-212">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-213">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-213">Plan start date</span></span> | <span data-ttu-id="3e0a4-214">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-214">Enrollment date</span></span> | <span data-ttu-id="3e0a4-215">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-215">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-216">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-216">Accrual period basis</span></span> | <span data-ttu-id="3e0a4-217">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="3e0a4-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-218">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-219">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-219">2/1/2018</span></span>        | <span data-ttu-id="3e0a4-220">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-220">Semimonthly</span></span>       | <span data-ttu-id="3e0a4-221">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-221">Plan start date</span></span>      | <span data-ttu-id="3e0a4-222">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="3e0a4-222">End of accrual period</span></span> |

<span data-ttu-id="3e0a4-223">Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="3e0a4-224">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-224">**Results**</span></span>

| <span data-ttu-id="3e0a4-225">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-225">Accrual amount</span></span> | <span data-ttu-id="3e0a4-226">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-226">Minimum balance</span></span> | <span data-ttu-id="3e0a4-227">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-227">Maximum carry-forward</span></span> | <span data-ttu-id="3e0a4-228">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-228">Request amount</span></span> | <span data-ttu-id="3e0a4-229">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="3e0a4-230">5</span><span class="sxs-lookup"><span data-stu-id="3e0a4-230">5</span></span>              | <span data-ttu-id="3e0a4-231">0</span><span class="sxs-lookup"><span data-stu-id="3e0a4-231">0</span></span>               | <span data-ttu-id="3e0a4-232">120</span><span class="sxs-lookup"><span data-stu-id="3e0a4-232">120</span></span>                   | <span data-ttu-id="3e0a4-233">8</span><span class="sxs-lookup"><span data-stu-id="3e0a4-233">8</span></span>              | <span data-ttu-id="3e0a4-234">22</span><span class="sxs-lookup"><span data-stu-id="3e0a4-234">22</span></span>                               |

<span data-ttu-id="3e0a4-235">Gjeldende saldo (22) = avsetningsbeløp (5 x 6) – forespurt beløp (8)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="3e0a4-236">Månedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-236">Monthly plan</span></span>

<span data-ttu-id="3e0a4-237">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-237">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-238">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-238">Plan start date</span></span> | <span data-ttu-id="3e0a4-239">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-239">Enrollment date</span></span> | <span data-ttu-id="3e0a4-240">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-240">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-241">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-241">Accrual period basis</span></span> | <span data-ttu-id="3e0a4-242">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="3e0a4-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-243">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-244">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-244">2/1/2018</span></span>        | <span data-ttu-id="3e0a4-245">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-245">Semimonthly</span></span>       | <span data-ttu-id="3e0a4-246">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-246">Plan start date</span></span>      | <span data-ttu-id="3e0a4-247">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="3e0a4-247">End of accrual period</span></span> |

<span data-ttu-id="3e0a4-248">Avsetninger behandles 1. mai 2018 (1.5.2018), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="3e0a4-249">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-249">**Results**</span></span>

| <span data-ttu-id="3e0a4-250">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-250">Accrual amount</span></span> | <span data-ttu-id="3e0a4-251">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-251">Minimum balance</span></span> | <span data-ttu-id="3e0a4-252">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-252">Maximum carry-forward</span></span> | <span data-ttu-id="3e0a4-253">Forespørselsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-253">Request amount</span></span> | <span data-ttu-id="3e0a4-254">Gjeldende saldo (per 1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="3e0a4-255">5</span><span class="sxs-lookup"><span data-stu-id="3e0a4-255">5</span></span>              | <span data-ttu-id="3e0a4-256">0</span><span class="sxs-lookup"><span data-stu-id="3e0a4-256">0</span></span>               | <span data-ttu-id="3e0a4-257">120</span><span class="sxs-lookup"><span data-stu-id="3e0a4-257">120</span></span>                   | <span data-ttu-id="3e0a4-258">8</span><span class="sxs-lookup"><span data-stu-id="3e0a4-258">8</span></span>              | <span data-ttu-id="3e0a4-259">7</span><span class="sxs-lookup"><span data-stu-id="3e0a4-259">7</span></span>                                |

<span data-ttu-id="3e0a4-260">Gjeldende saldo (7) = avsetningsbeløp (5 x 3) – forespurt beløp (8)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="3e0a4-261">Prognosesaldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-261">Forecasted balance</span></span>

<span data-ttu-id="3e0a4-262">*Prognosesaldo* er hvor mye permisjon som er tilgjengelig på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="3e0a4-263">Avsetninger og overføringsjusteringer er anslått frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="3e0a4-264">Følgende formel brukes:</span><span class="sxs-lookup"><span data-stu-id="3e0a4-264">The following formula is used:</span></span>

<span data-ttu-id="3e0a4-265">Mandag prognosesaldo = gjeldende saldo – forespørsler + avsetninger – overføringsjustering</span><span class="sxs-lookup"><span data-stu-id="3e0a4-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="3e0a4-266">Eksempler på prognosesaldoer</span><span class="sxs-lookup"><span data-stu-id="3e0a4-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="3e0a4-267">Årsplan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-267">Annual plan</span></span>

<span data-ttu-id="3e0a4-268">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-268">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-269">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-269">Plan start date</span></span> | <span data-ttu-id="3e0a4-270">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-270">Enrollment date</span></span> | <span data-ttu-id="3e0a4-271">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-271">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-272">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-272">Accrual period basis</span></span> | <span data-ttu-id="3e0a4-273">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="3e0a4-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-274">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-275">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-276">Årlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-276">Annual</span></span>            | <span data-ttu-id="3e0a4-277">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-277">Plan start date</span></span>      | <span data-ttu-id="3e0a4-278">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="3e0a4-278">End of accrual period</span></span> |

<span data-ttu-id="3e0a4-279">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="3e0a4-280">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-280">**Results**</span></span>

| <span data-ttu-id="3e0a4-281">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-281">Accrual amount</span></span> | <span data-ttu-id="3e0a4-282">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-282">Minimum balance</span></span> | <span data-ttu-id="3e0a4-283">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-283">Maximum carry-forward</span></span> | <span data-ttu-id="3e0a4-284">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-284">Current balance</span></span> | <span data-ttu-id="3e0a4-285">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="3e0a4-286">20</span><span class="sxs-lookup"><span data-stu-id="3e0a4-286">20</span></span>             | <span data-ttu-id="3e0a4-287">0</span><span class="sxs-lookup"><span data-stu-id="3e0a4-287">0</span></span>               | <span data-ttu-id="3e0a4-288">20</span><span class="sxs-lookup"><span data-stu-id="3e0a4-288">20</span></span>                    | <span data-ttu-id="3e0a4-289">40</span><span class="sxs-lookup"><span data-stu-id="3e0a4-289">40</span></span>              | <span data-ttu-id="3e0a4-290">40</span><span class="sxs-lookup"><span data-stu-id="3e0a4-290">40</span></span>                                   |

<span data-ttu-id="3e0a4-291">Prognosesaldo (40) = avsetningsbeløp (20) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="3e0a4-292">Halvmånedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-292">Semimonthly plan</span></span>

<span data-ttu-id="3e0a4-293">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-293">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-294">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-294">Plan start date</span></span> | <span data-ttu-id="3e0a4-295">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-295">Enrollment date</span></span> | <span data-ttu-id="3e0a4-296">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-296">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-297">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-297">Accrual period basis</span></span> | <span data-ttu-id="3e0a4-298">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="3e0a4-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-299">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-300">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-300">2/1/2018</span></span>        | <span data-ttu-id="3e0a4-301">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-301">Semimonthly</span></span>       | <span data-ttu-id="3e0a4-302">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-302">Plan start date</span></span>      | <span data-ttu-id="3e0a4-303">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="3e0a4-303">End of accrual period</span></span> |

<span data-ttu-id="3e0a4-304">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="3e0a4-305">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-305">**Results**</span></span>

| <span data-ttu-id="3e0a4-306">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-306">Accrual amount</span></span> | <span data-ttu-id="3e0a4-307">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-307">Minimum balance</span></span> | <span data-ttu-id="3e0a4-308">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-308">Maximum carry-forward</span></span> | <span data-ttu-id="3e0a4-309">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-309">Current balance</span></span> | <span data-ttu-id="3e0a4-310">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="3e0a4-311">5</span><span class="sxs-lookup"><span data-stu-id="3e0a4-311">5</span></span>              | <span data-ttu-id="3e0a4-312">0</span><span class="sxs-lookup"><span data-stu-id="3e0a4-312">0</span></span>               | <span data-ttu-id="3e0a4-313">20</span><span class="sxs-lookup"><span data-stu-id="3e0a4-313">20</span></span>                    | <span data-ttu-id="3e0a4-314">40</span><span class="sxs-lookup"><span data-stu-id="3e0a4-314">40</span></span>              | <span data-ttu-id="3e0a4-315">35</span><span class="sxs-lookup"><span data-stu-id="3e0a4-315">35</span></span>                                   |

<span data-ttu-id="3e0a4-316">Prognosesaldo (35) = avsetningsbeløp (5 x 3) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="3e0a4-317">Månedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-317">Monthly plan</span></span>

<span data-ttu-id="3e0a4-318">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-318">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-319">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-319">Plan start date</span></span> | <span data-ttu-id="3e0a4-320">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-320">Enrollment date</span></span> | <span data-ttu-id="3e0a4-321">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-321">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-322">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-322">Accrual period basis</span></span> | <span data-ttu-id="3e0a4-323">Belønningsdato for avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="3e0a4-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-324">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-325">1/2/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-325">2/1/2018</span></span>        | <span data-ttu-id="3e0a4-326">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-326">Semimonthly</span></span>       | <span data-ttu-id="3e0a4-327">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-327">Plan start date</span></span>      | <span data-ttu-id="3e0a4-328">Slutt på avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="3e0a4-328">End of accrual period</span></span> |

<span data-ttu-id="3e0a4-329">Avsetninger behandles 15. februar 2019 (15.2.2019), slik at hele perioden er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3e0a4-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="3e0a4-330">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-330">**Results**</span></span>

| <span data-ttu-id="3e0a4-331">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-331">Accrual amount</span></span> | <span data-ttu-id="3e0a4-332">Minste saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-332">Minimum balance</span></span> | <span data-ttu-id="3e0a4-333">Maksimal overføring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-333">Maximum carry-forward</span></span> | <span data-ttu-id="3e0a4-334">Gjeldende saldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-334">Current balance</span></span> | <span data-ttu-id="3e0a4-335">Prognosesaldo (per 15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="3e0a4-336">10</span><span class="sxs-lookup"><span data-stu-id="3e0a4-336">10</span></span>             | <span data-ttu-id="3e0a4-337">0</span><span class="sxs-lookup"><span data-stu-id="3e0a4-337">0</span></span>               | <span data-ttu-id="3e0a4-338">20</span><span class="sxs-lookup"><span data-stu-id="3e0a4-338">20</span></span>                    | <span data-ttu-id="3e0a4-339">40</span><span class="sxs-lookup"><span data-stu-id="3e0a4-339">40</span></span>              | <span data-ttu-id="3e0a4-340">30</span><span class="sxs-lookup"><span data-stu-id="3e0a4-340">30</span></span>                                   |

<span data-ttu-id="3e0a4-341">Prognosesaldo (30) = avsetningsbeløp (10 x 1) + gjeldende saldo (40) – overføringsjustering (20)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="3e0a4-342">Eksempler på fordelingssaldo</span><span class="sxs-lookup"><span data-stu-id="3e0a4-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="3e0a4-343">Fordelt månedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-343">Prorated monthly plan</span></span>

<span data-ttu-id="3e0a4-344">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-344">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-345">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-345">Plan start date</span></span> | <span data-ttu-id="3e0a4-346">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-346">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-347">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="3e0a4-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-348">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-349">Månedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-349">Monthly</span></span>           | <span data-ttu-id="3e0a4-350">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-350">Plan start date</span></span>      |

<span data-ttu-id="3e0a4-351">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-351">**Results**</span></span>

| <span data-ttu-id="3e0a4-352">Ansatt</span><span class="sxs-lookup"><span data-stu-id="3e0a4-352">Employee</span></span>            | <span data-ttu-id="3e0a4-353">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-353">Months of service</span></span> | <span data-ttu-id="3e0a4-354">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-354">Enrollment date</span></span> | <span data-ttu-id="3e0a4-355">Startdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-355">Start date</span></span> | <span data-ttu-id="3e0a4-356">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-356">Accrual amount</span></span> | <span data-ttu-id="3e0a4-357">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-357">Process accrual</span></span> | <span data-ttu-id="3e0a4-358">Beholdning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="3e0a4-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="3e0a4-359">Jeannette Nicholson</span></span> | <span data-ttu-id="3e0a4-360">0,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-360">0.00</span></span>              | <span data-ttu-id="3e0a4-361">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-361">6/1/2018</span></span>        | <span data-ttu-id="3e0a4-362">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-362">6/1/2018</span></span>   | <span data-ttu-id="3e0a4-363">1,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-363">1.00</span></span>           | <span data-ttu-id="3e0a4-364">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-364">9/1/2018</span></span>        | <span data-ttu-id="3e0a4-365">3,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-365">3.00</span></span>    |
| <span data-ttu-id="3e0a4-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="3e0a4-366">Jay Norman</span></span>          | <span data-ttu-id="3e0a4-367">0,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-367">0.00</span></span>              | <span data-ttu-id="3e0a4-368">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-368">6/15/2018</span></span>       | <span data-ttu-id="3e0a4-369">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-369">6/15/2018</span></span>  | <span data-ttu-id="3e0a4-370">1,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-370">1.00</span></span>           | <span data-ttu-id="3e0a4-371">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-371">9/1/2018</span></span>        | <span data-ttu-id="3e0a4-372">2.53</span><span class="sxs-lookup"><span data-stu-id="3e0a4-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="3e0a4-373">Full avsetning, månedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-373">Full accrual monthly plan</span></span>

<span data-ttu-id="3e0a4-374">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-374">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-375">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-375">Plan start date</span></span> | <span data-ttu-id="3e0a4-376">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-376">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-377">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="3e0a4-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-378">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-379">Månedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-379">Monthly</span></span>           | <span data-ttu-id="3e0a4-380">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-380">Plan start date</span></span>      |

<span data-ttu-id="3e0a4-381">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-381">**Results**</span></span>

| <span data-ttu-id="3e0a4-382">Ansatt</span><span class="sxs-lookup"><span data-stu-id="3e0a4-382">Employee</span></span>            | <span data-ttu-id="3e0a4-383">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-383">Months of service</span></span> | <span data-ttu-id="3e0a4-384">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-384">Enrollment date</span></span> | <span data-ttu-id="3e0a4-385">Startdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-385">Start date</span></span> | <span data-ttu-id="3e0a4-386">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-386">Accrual amount</span></span> | <span data-ttu-id="3e0a4-387">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-387">Process accrual</span></span> | <span data-ttu-id="3e0a4-388">Beholdning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="3e0a4-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="3e0a4-389">Jeannette Nicholson</span></span> | <span data-ttu-id="3e0a4-390">0,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-390">0.00</span></span>              | <span data-ttu-id="3e0a4-391">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-391">6/1/2018</span></span>        | <span data-ttu-id="3e0a4-392">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-392">6/1/2018</span></span>   | <span data-ttu-id="3e0a4-393">1,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-393">1.00</span></span>           | <span data-ttu-id="3e0a4-394">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-394">9/1/2018</span></span>        | <span data-ttu-id="3e0a4-395">3,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-395">3.00</span></span>    |
| <span data-ttu-id="3e0a4-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="3e0a4-396">Jay Norman</span></span>          | <span data-ttu-id="3e0a4-397">0,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-397">0.00</span></span>              | <span data-ttu-id="3e0a4-398">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-398">6/15/2018</span></span>       | <span data-ttu-id="3e0a4-399">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-399">6/15/2018</span></span>  | <span data-ttu-id="3e0a4-400">1,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-400">1.00</span></span>           | <span data-ttu-id="3e0a4-401">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-401">9/1/2018</span></span>        | <span data-ttu-id="3e0a4-402">3,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="3e0a4-403">Ingen avsetning, månedlig plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-403">No accrual monthly plan</span></span>

<span data-ttu-id="3e0a4-404">**Oppsett av plan**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-404">**Plan setup**</span></span>

| <span data-ttu-id="3e0a4-405">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-405">Plan start date</span></span> | <span data-ttu-id="3e0a4-406">Avsetningsfrekvens</span><span class="sxs-lookup"><span data-stu-id="3e0a4-406">Accrual frequency</span></span> | <span data-ttu-id="3e0a4-407">Avsetningsperiodegrunnlag</span><span class="sxs-lookup"><span data-stu-id="3e0a4-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="3e0a4-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-408">1/1/2018</span></span>        | <span data-ttu-id="3e0a4-409">Månedlig</span><span class="sxs-lookup"><span data-stu-id="3e0a4-409">Monthly</span></span>           | <span data-ttu-id="3e0a4-410">Startdato for plan</span><span class="sxs-lookup"><span data-stu-id="3e0a4-410">Plan start date</span></span>      |

<span data-ttu-id="3e0a4-411">**Resultater**</span><span class="sxs-lookup"><span data-stu-id="3e0a4-411">**Results**</span></span>

| <span data-ttu-id="3e0a4-412">Ansatt</span><span class="sxs-lookup"><span data-stu-id="3e0a4-412">Employee</span></span>            | <span data-ttu-id="3e0a4-413">Måneder med jobberfaring</span><span class="sxs-lookup"><span data-stu-id="3e0a4-413">Months of service</span></span> | <span data-ttu-id="3e0a4-414">Registreringsdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-414">Enrollment date</span></span> | <span data-ttu-id="3e0a4-415">Startdato</span><span class="sxs-lookup"><span data-stu-id="3e0a4-415">Start date</span></span> | <span data-ttu-id="3e0a4-416">Avsetningsbeløp</span><span class="sxs-lookup"><span data-stu-id="3e0a4-416">Accrual amount</span></span> | <span data-ttu-id="3e0a4-417">Behandle avsetning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-417">Process accrual</span></span> | <span data-ttu-id="3e0a4-418">Beholdning</span><span class="sxs-lookup"><span data-stu-id="3e0a4-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="3e0a4-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="3e0a4-419">Jeannette Nicholson</span></span> | <span data-ttu-id="3e0a4-420">0,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-420">0.00</span></span>              | <span data-ttu-id="3e0a4-421">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-421">6/1/2018</span></span>        | <span data-ttu-id="3e0a4-422">1/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-422">6/1/2018</span></span>   | <span data-ttu-id="3e0a4-423">1,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-423">1.00</span></span>           | <span data-ttu-id="3e0a4-424">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-424">9/1/2018</span></span>        | <span data-ttu-id="3e0a4-425">3,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-425">3.00</span></span>    |
| <span data-ttu-id="3e0a4-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="3e0a4-426">Jay Norman</span></span>          | <span data-ttu-id="3e0a4-427">0,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-427">0.00</span></span>              | <span data-ttu-id="3e0a4-428">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-428">6/15/2018</span></span>       | <span data-ttu-id="3e0a4-429">15/6/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-429">6/15/2018</span></span>  | <span data-ttu-id="3e0a4-430">1,00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-430">1.00</span></span>           | <span data-ttu-id="3e0a4-431">1/9/2018</span><span class="sxs-lookup"><span data-stu-id="3e0a4-431">9/1/2018</span></span>        | <span data-ttu-id="3e0a4-432">2.00</span><span class="sxs-lookup"><span data-stu-id="3e0a4-432">2.00</span></span>    |
