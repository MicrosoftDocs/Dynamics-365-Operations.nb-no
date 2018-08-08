---
title: "Fraværsregistrering i timeregistrering"
description: "Dette emnet beskriver hvordan du håndterer fraværsregistreringer i Timeregistrering."
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7ef244d5abf762bcaab426cf1cefb232383a8109
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="fd481-103">Fraværsregistrering i timeregistrering</span><span class="sxs-lookup"><span data-stu-id="fd481-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd481-104">Dette emnet beskriver begreper for fravær, og forklarer hvordan du håndterer fravær i Timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="fd481-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="fd481-105">Fravær som er basert på vanlig arbeidtid</span><span class="sxs-lookup"><span data-stu-id="fd481-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="fd481-106">Arbeidere anses som fraværende i timer de ikke arbeider i den vanlige arbeidstiden.</span><span class="sxs-lookup"><span data-stu-id="fd481-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="fd481-107">Vanlig arbeidstid defineres i profilen for standard arbeidstid for en arbeider.</span><span class="sxs-lookup"><span data-stu-id="fd481-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="fd481-108">En arbeider arbeider for eksempel på en dagprofil som har innstempling 07:00 og utstempling 15:00.</span><span class="sxs-lookup"><span data-stu-id="fd481-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="fd481-109">Hvis arbeideren stempler inn 09:00, anses vedkommende som fraværende fra 07:00 til 09:00 denne dagen.</span><span class="sxs-lookup"><span data-stu-id="fd481-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="fd481-110">I slike tilfeller blir arbeidere bedt om å angi en årsak til fraværet.</span><span class="sxs-lookup"><span data-stu-id="fd481-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="fd481-111">De kan angi en årsak ved å velge en fraværskode.</span><span class="sxs-lookup"><span data-stu-id="fd481-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="fd481-112">Fraværskoder</span><span class="sxs-lookup"><span data-stu-id="fd481-112">Absence codes</span></span>

<span data-ttu-id="fd481-113">Fraværskoder definere ulike typer fravær.</span><span class="sxs-lookup"><span data-stu-id="fd481-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="fd481-114">Fraværskoder defineres av firmaet.</span><span class="sxs-lookup"><span data-stu-id="fd481-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="fd481-115">Forskjellige regler kan brukes på fraværskoder.</span><span class="sxs-lookup"><span data-stu-id="fd481-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="fd481-116">En fraværskode kan for eksempel konfigureres til å trekke fra eller gi lønn.</span><span class="sxs-lookup"><span data-stu-id="fd481-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="fd481-117">Et firma definerer for eksempel en **For sent**-fraværskode som arbeidere kan bruke hvis de kommer inn for sent og ikke har en god grunn.</span><span class="sxs-lookup"><span data-stu-id="fd481-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="fd481-118">Firmaet definerer også en **Internt kurs**-fraværskode som arbeidere bruker for tid som brukes for deltakelse på interne kurs.</span><span class="sxs-lookup"><span data-stu-id="fd481-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="fd481-119">Disse fraværskoder kan defineres slik at **For sent** trekker lønn fra en arbeider, men **Internt kurs** ikke trekke lønn fra en arbeider.</span><span class="sxs-lookup"><span data-stu-id="fd481-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="fd481-120">Du kan definere automatiske fraværskoder.</span><span class="sxs-lookup"><span data-stu-id="fd481-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="fd481-121">Disse fraværskodene kan brukes til å beregne en arbeiders klokkeslett når ingen fravær er registrert.</span><span class="sxs-lookup"><span data-stu-id="fd481-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="fd481-122">Arbeiderens tidsprofil bestemmer om fraværskoden for standardtid eller fleksetid brukes.</span><span class="sxs-lookup"><span data-stu-id="fd481-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="fd481-123">Definere standardtid og fleksitid</span><span class="sxs-lookup"><span data-stu-id="fd481-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="fd481-124">Konfigurer parametere for standardtid og fleksitid ved hjelp av alternativene **Sett inn fravær automatisk** og **Sett inn fleksitid automatisk** på siden **Parametere for timeregistrering**.</span><span class="sxs-lookup"><span data-stu-id="fd481-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="fd481-125">Fraværsgrupper</span><span class="sxs-lookup"><span data-stu-id="fd481-125">Absence groups</span></span>

<span data-ttu-id="fd481-126">Fraværskoder grupperes i fraværsgrupper.</span><span class="sxs-lookup"><span data-stu-id="fd481-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="fd481-127">Du kan bruke fraværsgrupper til å gruppere fraværskoder som har felles egenskaper.</span><span class="sxs-lookup"><span data-stu-id="fd481-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="fd481-128">Eksempler omfatter koder for gyldig fravær eller fravær på grunn av en legetime, meddommertjeneste eller sykt barn.</span><span class="sxs-lookup"><span data-stu-id="fd481-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="fd481-129">Planlagt fravær</span><span class="sxs-lookup"><span data-stu-id="fd481-129">Planned absence</span></span>

<span data-ttu-id="fd481-130">Hvis du vet at en arbeider vil være fraværende en periode, for eksempel en kommende ferie, kan du bruke planlagt fravær.</span><span class="sxs-lookup"><span data-stu-id="fd481-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="fd481-131">Du kan definere planlagt fravær ved å konfigurere fraværskoden slik at det anses som planlagt fravær.</span><span class="sxs-lookup"><span data-stu-id="fd481-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="fd481-132">Når du definerer et planlagt fravær, blir du ikke bedt om en fraværskode i løpet av fraværsperioden når tidsregistrering for brukeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="fd481-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="fd481-133">Planlagt fravær kan defineres for én enkelt arbeider, eller du kan definere en satsvis jobb for å masseoppdatere planlagt fravær for arbeidere.</span><span class="sxs-lookup"><span data-stu-id="fd481-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="fd481-134">Definere planlagt fravær</span><span class="sxs-lookup"><span data-stu-id="fd481-134">Set up planned absence</span></span>

1. <span data-ttu-id="fd481-135">Velg **Personale** &gt; **Arbeidere** &gt; **Ansatte**, og velg en ansatt.</span><span class="sxs-lookup"><span data-stu-id="fd481-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="fd481-136">Velg **Tid** &gt; **Tidstildelinger** &gt; **Fraværsregistrering**, og angi det planlagte fraværet.</span><span class="sxs-lookup"><span data-stu-id="fd481-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="fd481-137">Avbrutt planlagt fravær</span><span class="sxs-lookup"><span data-stu-id="fd481-137">Interrupted planned absence</span></span>

<span data-ttu-id="fd481-138">Hvis du bruker alternativet **Avbryt** når du definerer et planlagt fravær, blir det planlagte fraværet avbrutt hvis arbeideren stempler inn i løpet av perioden for planlagt fravær.</span><span class="sxs-lookup"><span data-stu-id="fd481-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="fd481-139">Det planlagte fraværet vil bli merket som **Avbrutt** og vil ikke ha noen innvirkning på fremtidige beregninger.</span><span class="sxs-lookup"><span data-stu-id="fd481-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="fd481-140">Definere planlagt fravær for avbrudd</span><span class="sxs-lookup"><span data-stu-id="fd481-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="fd481-141">Åpne siden **Fraværsregistrering** som beskrevet i fremgangsmåten for å definere planlagt fravær.</span><span class="sxs-lookup"><span data-stu-id="fd481-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="fd481-142">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="fd481-142">Select **Interrupt**.</span></span>

<span data-ttu-id="fd481-143">Alternativet **Avbryt** brukes når tiden registreres gjennom shop floor-terminalen eller -enheten.</span><span class="sxs-lookup"><span data-stu-id="fd481-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="fd481-144">Alternativet gjelder ikke hvis registreringer er angitt på sidene for beregning og godkjenningsstatus eller på siden **Elektronisk tidskort**.</span><span class="sxs-lookup"><span data-stu-id="fd481-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="fd481-145">Eksempler på bruk av fravær i en fleksiprofil</span><span class="sxs-lookup"><span data-stu-id="fd481-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="fd481-146">De tre eksemplene nedenfor viser hvordan fravær beregnes i en profil som har fleksiperioder.</span><span class="sxs-lookup"><span data-stu-id="fd481-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="fd481-147">Eksemplene bruker profilen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fd481-147">The examples use the following profile.</span></span>

| <span data-ttu-id="fd481-148">Innstempling</span><span class="sxs-lookup"><span data-stu-id="fd481-148">Clock-in</span></span> | <span data-ttu-id="fd481-149">Normaltid</span><span class="sxs-lookup"><span data-stu-id="fd481-149">Standard time</span></span>    | <span data-ttu-id="fd481-150">Bryt</span><span class="sxs-lookup"><span data-stu-id="fd481-150">Break</span></span>             | <span data-ttu-id="fd481-151">Normaltid</span><span class="sxs-lookup"><span data-stu-id="fd481-151">Standard time</span></span> | <span data-ttu-id="fd481-152">Fleksi-</span><span class="sxs-lookup"><span data-stu-id="fd481-152">Flex-</span></span>        | <span data-ttu-id="fd481-153">Utstempling</span><span class="sxs-lookup"><span data-stu-id="fd481-153">Clock-out</span></span> | <span data-ttu-id="fd481-154">Fleksi+</span><span class="sxs-lookup"><span data-stu-id="fd481-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="fd481-155">08:00</span><span class="sxs-lookup"><span data-stu-id="fd481-155">8 AM</span></span>     | <span data-ttu-id="fd481-156">09:00 til 11:30</span><span class="sxs-lookup"><span data-stu-id="fd481-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="fd481-157">11:30 til 12:00</span><span class="sxs-lookup"><span data-stu-id="fd481-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="fd481-158">12:00 til 15:00</span><span class="sxs-lookup"><span data-stu-id="fd481-158">12 PM to 3 PM</span></span> | <span data-ttu-id="fd481-159">12:00 til 15:00</span><span class="sxs-lookup"><span data-stu-id="fd481-159">3 PM to 4 PM</span></span> | <span data-ttu-id="fd481-160">16:00</span><span class="sxs-lookup"><span data-stu-id="fd481-160">4 PM</span></span>      | <span data-ttu-id="fd481-161">16:00 til 18:00</span><span class="sxs-lookup"><span data-stu-id="fd481-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="fd481-162">Eksempel 1: Utstempling i perioden Fleksi-</span><span class="sxs-lookup"><span data-stu-id="fd481-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="fd481-163">Arbeideren stempler inn 8:00 og stempler ut 15:30.</span><span class="sxs-lookup"><span data-stu-id="fd481-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="fd481-164">Siden arbeideren i dette tilfellet stempler ut i perioden Fleksi-, beregnes ikke fravær, og en halv time trekkes fra fleksisaldoen for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="fd481-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="fd481-165">Eksempel 2: Utstempling i løpet av perioden for standardtid</span><span class="sxs-lookup"><span data-stu-id="fd481-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="fd481-166">Arbeideren stempler inn i 8:00 og stempler ut 14:30.</span><span class="sxs-lookup"><span data-stu-id="fd481-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="fd481-167">Siden arbeideren i dette tilfellet stempler ut i perioden for standardtid, beregnes fravær fra 14:30 til 16: 00, og det registreres en fraværsperioden på 1,5 timer.</span><span class="sxs-lookup"><span data-stu-id="fd481-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="fd481-168">Det kreves en fraværskode i dette tidsrommet.</span><span class="sxs-lookup"><span data-stu-id="fd481-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="fd481-169">Eksempel 3: Utstempling i perioden Fleksi+</span><span class="sxs-lookup"><span data-stu-id="fd481-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="fd481-170">Arbeideren stempler inn 8:00 og stempler ut 15:30.</span><span class="sxs-lookup"><span data-stu-id="fd481-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="fd481-171">Siden arbeideren i dette tilfellet stempler ut i perioden Fleksi+, beregnes ikke fravær, og en halv time legges til fleksisaldoen for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="fd481-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="fd481-172">Fravær i beregnings- og godkjenningsåprosessen</span><span class="sxs-lookup"><span data-stu-id="fd481-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="fd481-173">Tidsregistreringer for arbeider må beregnes og godkjennes før de kan overføres til lønningssystemet som lønnsposter.</span><span class="sxs-lookup"><span data-stu-id="fd481-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="fd481-174">En godkjenner kan endre tidsregistreringer for en arbeider.</span><span class="sxs-lookup"><span data-stu-id="fd481-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="fd481-175">Godkjenneren kan også endre alle fravær som arbeideren har registrert.</span><span class="sxs-lookup"><span data-stu-id="fd481-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="fd481-176">Hvis godkjenneren manuelt angir en tidsperiode som har en fraværskode, overstyres ikke fraværskoden for denne perioden av standard fraværskode fra Parametere for timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="fd481-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="fd481-177">En arbeider stempler for eksempel inn 10:00 og velger en fraværskode som angir at hun kommer for sent.</span><span class="sxs-lookup"><span data-stu-id="fd481-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="fd481-178">Senere informerer arbeideren sin overordnede om at hun hadde en legeavtale fra 08:00 til 10:00.</span><span class="sxs-lookup"><span data-stu-id="fd481-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="fd481-179">Legeavtalen skal ikke føre til trekk i lønn for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="fd481-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="fd481-180">I dette tilfellet kan derfor overordnede justere de to timene med fravær fra 08:00 til 10:00 ved å manuelt angi en fraværskode som angir sykdom for disse to timene.</span><span class="sxs-lookup"><span data-stu-id="fd481-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="fd481-181">Beregne og godkjenne fravær</span><span class="sxs-lookup"><span data-stu-id="fd481-181">Calculate and approve absence</span></span>

- <span data-ttu-id="fd481-182">Velg **Timeregistrering** &gt; **Gjennomgå og godkjenn** &gt; **Godkjenn eller beregn**.</span><span class="sxs-lookup"><span data-stu-id="fd481-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>

