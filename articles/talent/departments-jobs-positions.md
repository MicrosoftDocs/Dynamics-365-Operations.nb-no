---
title: Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger
description: Avdelinger, jobber og stillinger er organisasjonselementer som vedlikeholdes i Personale. Dette emnet beskriver konseptuell informasjon om disse elementene.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: af2d61717a5aa02b2a3ef26144a845b81b32ca53
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="organize-your-workforce-using-departments-jobs-and-positions"></a><span data-ttu-id="f0027-104">Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="f0027-104">Organize your workforce using departments, jobs, and positions</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="f0027-105">Avdelinger, jobber og stillinger er organisasjonselementer som vedlikeholdes i Personale.</span><span class="sxs-lookup"><span data-stu-id="f0027-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="f0027-106">Dette emnet beskriver konseptuell informasjon om disse elementene.</span><span class="sxs-lookup"><span data-stu-id="f0027-106">This topic describes conceptual information about these elements.</span></span> 

<span data-ttu-id="f0027-107">Eksemplet nedenfor brukes til å illustrere begreper som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f0027-107">The following example is used to illustrate the concepts described in this topic.</span></span>

|<span data-ttu-id="f0027-108">**Avdeling**</span><span class="sxs-lookup"><span data-stu-id="f0027-108">**Department**</span></span>|<span data-ttu-id="f0027-109">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="f0027-109">**Position**</span></span>|<span data-ttu-id="f0027-110">**Jobb**</span><span class="sxs-lookup"><span data-stu-id="f0027-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="f0027-111">**Salg**</span><span class="sxs-lookup"><span data-stu-id="f0027-111">**Sales**</span></span>|<span data-ttu-id="f0027-112">Salgssjef (øst)</span><span class="sxs-lookup"><span data-stu-id="f0027-112">Sales manager (East)</span></span>|<span data-ttu-id="f0027-113">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="f0027-113">Sales manager</span></span>|
|<span data-ttu-id="f0027-114">**Salg**</span><span class="sxs-lookup"><span data-stu-id="f0027-114">**Sales**</span></span>|<span data-ttu-id="f0027-115">Salgssjef (vest)</span><span class="sxs-lookup"><span data-stu-id="f0027-115">Sales manager (West)</span></span>|<span data-ttu-id="f0027-116">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="f0027-116">Sales manager</span></span>|
|<span data-ttu-id="f0027-117">**Salg**</span><span class="sxs-lookup"><span data-stu-id="f0027-117">**Sales**</span></span>|<span data-ttu-id="f0027-118">Salgssjef (sentralt)</span><span class="sxs-lookup"><span data-stu-id="f0027-118">Sales manager (Central)</span></span>|<span data-ttu-id="f0027-119">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="f0027-119">Sales manager</span></span>|
|<span data-ttu-id="f0027-120">**Regnskap**</span><span class="sxs-lookup"><span data-stu-id="f0027-120">**Accounting**</span></span>|<span data-ttu-id="f0027-121">Regnskapsansvarlig</span><span class="sxs-lookup"><span data-stu-id="f0027-121">Accounting supervisor</span></span>|<span data-ttu-id="f0027-122">Regnskapssjef</span><span class="sxs-lookup"><span data-stu-id="f0027-122">Accounting manager</span></span>|
|<span data-ttu-id="f0027-123">**Regnskap**</span><span class="sxs-lookup"><span data-stu-id="f0027-123">**Accounting**</span></span>|<span data-ttu-id="f0027-124">Regnskap -A</span><span class="sxs-lookup"><span data-stu-id="f0027-124">Accounting-A</span></span>|<span data-ttu-id="f0027-125">Regnskapsfører</span><span class="sxs-lookup"><span data-stu-id="f0027-125">Accountant</span></span>|
|<span data-ttu-id="f0027-126">**Personale**</span><span class="sxs-lookup"><span data-stu-id="f0027-126">**Human resources**</span></span>|<span data-ttu-id="f0027-127">Personale (øst)</span><span class="sxs-lookup"><span data-stu-id="f0027-127">HR manager (East)</span></span>|<span data-ttu-id="f0027-128">Personale</span><span class="sxs-lookup"><span data-stu-id="f0027-128">HR manager</span></span>|
|<span data-ttu-id="f0027-129">**Personale**</span><span class="sxs-lookup"><span data-stu-id="f0027-129">**Human resources**</span></span>|<span data-ttu-id="f0027-130">Personale (vest)</span><span class="sxs-lookup"><span data-stu-id="f0027-130">HR manager (West)</span></span>|<span data-ttu-id="f0027-131">Personale</span><span class="sxs-lookup"><span data-stu-id="f0027-131">HR manager</span></span>|
|<span data-ttu-id="f0027-132">**Personale**</span><span class="sxs-lookup"><span data-stu-id="f0027-132">**Human resources**</span></span>|<span data-ttu-id="f0027-133">Personale (sentralt)</span><span class="sxs-lookup"><span data-stu-id="f0027-133">HR manager (Central)</span></span>|<span data-ttu-id="f0027-134">Personale</span><span class="sxs-lookup"><span data-stu-id="f0027-134">HR manager</span></span>|

 
 <a name="departments"></a><span data-ttu-id="f0027-135">Avdelinger</span><span class="sxs-lookup"><span data-stu-id="f0027-135">Departments</span></span>
------------

<span data-ttu-id="f0027-136">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon som er ansvarlig for et bestemt område i organisasjonen, for eksempel salg eller regnskap.</span><span class="sxs-lookup"><span data-stu-id="f0027-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="f0027-137">En avdeling som brukes til å rapportere om funksjonsområder og kan ha resultatansvar.</span><span class="sxs-lookup"><span data-stu-id="f0027-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="f0027-138">En avdeling kan også inneholde en gruppe med kostsentre.</span><span class="sxs-lookup"><span data-stu-id="f0027-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="f0027-139">Salg, regnskap og personale er noen eksempler på avdelinger i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="f0027-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="f0027-140">Jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="f0027-140">Jobs and positions</span></span>
<span data-ttu-id="f0027-141">En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb.</span><span class="sxs-lookup"><span data-stu-id="f0027-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f0027-142">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="f0027-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="f0027-143">Ansvarsområder, jobboppgaver, jobbfunksjoner, ferdigheter, utdanningsinformasjon og sertifikater som kreves for en jobb, er også nødvendig for stillinger som er tilknyttet en jobb.</span><span class="sxs-lookup"><span data-stu-id="f0027-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="f0027-144">Jobboppgaver</span><span class="sxs-lookup"><span data-stu-id="f0027-144">Job tasks</span></span>

<span data-ttu-id="f0027-145">Du kan opprette jobboppgaver som beskriver de grunnleggende oppgavene som må fullføres av en arbeider i en stilling for jobben.</span><span class="sxs-lookup"><span data-stu-id="f0027-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="f0027-146">Den samme jobboppgaven kan legges til flere jobber, og stillinger for disse jobbene arver disse jobboppgavene.</span><span class="sxs-lookup"><span data-stu-id="f0027-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="f0027-147">Eksempler på jobboppgaver er oppført i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f0027-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f0027-148">Jobb</span><span class="sxs-lookup"><span data-stu-id="f0027-148">Job</span></span></th>
<th><span data-ttu-id="f0027-149">Jobboppgave</span><span class="sxs-lookup"><span data-stu-id="f0027-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0027-150">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="f0027-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="f0027-151"><span class="input">Ytelsesgjennomgang</span> – Vurder jobbytelsen til hver enkelt selger.</span><span class="sxs-lookup"><span data-stu-id="f0027-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="f0027-152"><span class="input">Fraværsgjennomgang</span> – Godkjenn eller avvis fraværsforespørsler eller registreringer for hver selger.</span><span class="sxs-lookup"><span data-stu-id="f0027-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0027-153">Regnskapsfører</span><span class="sxs-lookup"><span data-stu-id="f0027-153">Accountant</span></span></td>
<td><span data-ttu-id="f0027-154"><span class="input">Finansrapport</span> – Vis ukentlige finansrapporter til økonomisjef.</span><span class="sxs-lookup"><span data-stu-id="f0027-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="f0027-155">Jobbfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f0027-155">Job functions</span></span>

<span data-ttu-id="f0027-156">Jobbfunksjoner er som jobboppgaver.</span><span class="sxs-lookup"><span data-stu-id="f0027-156">Job functions are like job tasks.</span></span> <span data-ttu-id="f0027-157">En jobbfunksjon beskriver en eller flere oppgaver, plikter eller ansvarsområder som er tilordnet til en jobb.</span><span class="sxs-lookup"><span data-stu-id="f0027-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="f0027-158">Jobbtyper kan være knyttet til jobber og brukes til å definere og implementere rettighetsregler for kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="f0027-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="f0027-159">Eksempler på jobbfunksjoner er oppført i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f0027-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="f0027-160">Jobb</span><span class="sxs-lookup"><span data-stu-id="f0027-160">Job</span></span>           | <span data-ttu-id="f0027-161">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="f0027-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="f0027-162">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="f0027-162">Sales manager</span></span> | <span data-ttu-id="f0027-163">Adm. personer – Administrer personer som rapporterer til deg.</span><span class="sxs-lookup"><span data-stu-id="f0027-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="f0027-164">Regnskapsfører</span><span class="sxs-lookup"><span data-stu-id="f0027-164">Accountant</span></span>    | <span data-ttu-id="f0027-165">Finansgjennomgang – Vedlikehold økonomiske data for et sett med kontoer.</span><span class="sxs-lookup"><span data-stu-id="f0027-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="f0027-166">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="f0027-166">Job types</span></span>

<span data-ttu-id="f0027-167">Bruk jobbtyper til å klassifisere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="f0027-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="f0027-168">Jobbtyper, på samme måte som jobbfunksjoner, kan være knyttet til jobber og brukes til å definere og implementere rettighetsregler for kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="f0027-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="f0027-169">Noen eksempler på jobbtyper er inkludert i følgende liste:</span><span class="sxs-lookup"><span data-stu-id="f0027-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="f0027-170">Heltid</span><span class="sxs-lookup"><span data-stu-id="f0027-170">Full-time</span></span>
-   <span data-ttu-id="f0027-171">Deltid</span><span class="sxs-lookup"><span data-stu-id="f0027-171">Part-time</span></span>
-   <span data-ttu-id="f0027-172">Lønn</span><span class="sxs-lookup"><span data-stu-id="f0027-172">Salary</span></span>
-   <span data-ttu-id="f0027-173">Timelønn</span><span class="sxs-lookup"><span data-stu-id="f0027-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="f0027-174">Ansvarsområder</span><span class="sxs-lookup"><span data-stu-id="f0027-174">Areas of responsibility</span></span>

<span data-ttu-id="f0027-175">Bruk ansvarsområder for å angi arbeidsrollene, prosessene og produktene som en arbeider som er i en stilling for jobben, har ansvaret for.</span><span class="sxs-lookup"><span data-stu-id="f0027-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="f0027-176">Et eksempel på et ansvarsområde for en jobb med navnet "Regnskap" kan være "Økonomisk rapportering for produkt A".</span><span class="sxs-lookup"><span data-stu-id="f0027-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="f0027-177">Stillinger</span><span class="sxs-lookup"><span data-stu-id="f0027-177">Positions</span></span>
----------

<span data-ttu-id="f0027-178">Stillinger er et viktig element i det nederste nivået i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f0027-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="f0027-179">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="f0027-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="f0027-180">Stillingen "Salgssjef (øst)" er for eksempel bare én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="f0027-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="f0027-181">Stillinger finnes i en avdeling, og tilordnes til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="f0027-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="f0027-182">Opprettelse og vedlikehold av stilling</span><span class="sxs-lookup"><span data-stu-id="f0027-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="f0027-183">Du kan vise en logg over stillingsrelaterte systemendringer på en lett tilgjengelig listeside.</span><span class="sxs-lookup"><span data-stu-id="f0027-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="f0027-184">Du kan opprette årsakskoder som brukerne kan velge når de oppretter eller endrer stillinger.</span><span class="sxs-lookup"><span data-stu-id="f0027-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="f0027-185">Du kan opprette personalhandlingstyper og tilordne en nummerserie til personalhandlinger.</span><span class="sxs-lookup"><span data-stu-id="f0027-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="f0027-186">Du kan angi en arbeidsflyt slik stillingstillegg og -endringer kan kreve godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f0027-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="f0027-187">Stillingsvarighet</span><span class="sxs-lookup"><span data-stu-id="f0027-187">Position duration</span></span>

<span data-ttu-id="f0027-188">Hver stilling har et tidsrom som stillingen er gyldig i.</span><span class="sxs-lookup"><span data-stu-id="f0027-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="f0027-189">Dette tidsrommet kalles varighet.</span><span class="sxs-lookup"><span data-stu-id="f0027-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="f0027-190">Sommerstillinger kan for eksempel ha varighet fra 1. mai 2015 til 31. august 2015.</span><span class="sxs-lookup"><span data-stu-id="f0027-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="f0027-191">Arbeidertilordninger</span><span class="sxs-lookup"><span data-stu-id="f0027-191">Worker assignments</span></span>

<span data-ttu-id="f0027-192">Når du tilordner en arbeider til en stilling, fyller du denne stillingen.</span><span class="sxs-lookup"><span data-stu-id="f0027-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="f0027-193">Du kan tilordne arbeidere til flere stillinger, men bare én arbeider kan tilordnes til en stilling på samme tid.</span><span class="sxs-lookup"><span data-stu-id="f0027-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="f0027-194">Rapporteringsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="f0027-194">Reporting relationships</span></span>

<span data-ttu-id="f0027-195">Stillinger er viktige elementer i det nederste nivået i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f0027-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="f0027-196">Du kan angi stillingen en stilling rapporterer til, i stillingsskjemaet.</span><span class="sxs-lookup"><span data-stu-id="f0027-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="f0027-197">Når du tilordner en arbeider til en stilling som rapporterer til en annen stilling, oppretter du en rapporteringsrelasjon mellom arbeidere som er tilordnet de to stillingene.</span><span class="sxs-lookup"><span data-stu-id="f0027-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="f0027-198">Stillingen "Regnskapsfører-A" rapporterer for eksempel til stillingen "Regnskapsansvarlig".</span><span class="sxs-lookup"><span data-stu-id="f0027-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="f0027-199">Kim Akers tilordnes stillingen "Regnskapsansvarlig", og Sanjay Patel tilordnes stillingen "Regnskapsfører-A".</span><span class="sxs-lookup"><span data-stu-id="f0027-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="f0027-200">Dette betyr at Sanjay Patel rapporterer til Kim Akers.</span><span class="sxs-lookup"><span data-stu-id="f0027-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="f0027-201">Hvis organisasjonen bruker et matrisehierarki eller et annet egendefinert hierarki, kan du konfigurere stillingshierarkityper og deretter legge til rapporteringsrelasjoner i stillinger for hver hierarkitype som du definerer.</span><span class="sxs-lookup"><span data-stu-id="f0027-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="f0027-202">Lori Penor er for eksempel en daglig leder hos Adventure Works, og tilordnes stillingen "Leder".</span><span class="sxs-lookup"><span data-stu-id="f0027-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="f0027-203">Lori administrerer utviklingen av et produkt som brukes til å rengjøre noe.</span><span class="sxs-lookup"><span data-stu-id="f0027-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="f0027-204">Lori trenger en regnskapsfører for å hjelpe til med økonomien for utvikling av produktet.</span><span class="sxs-lookup"><span data-stu-id="f0027-204">Lori requires an accountant to help her with the finances for developing the product.</span></span> <span data-ttu-id="f0027-205">Hun har derfor rekruttert Sanjay Patel som hennes regnskapsfører.</span><span class="sxs-lookup"><span data-stu-id="f0027-205">Therefore, she has recruited Sanjay Patel to be her accountant.</span></span> <span data-ttu-id="f0027-206">Sanjay rapporterer direkte til Kim Akers, men arbeider også sammen med Lori Penor på arbeidet sitt knyttet til Økonomi for å utvikle ryddeverktøyet.</span><span class="sxs-lookup"><span data-stu-id="f0027-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="f0027-207">For det forrige eksemplet ville du fullført følgende oppgaver for å definere relasjonen mellom Sanjay Patel og Lori Penor:</span><span class="sxs-lookup"><span data-stu-id="f0027-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="f0027-208">Opprett en egendefinert stillingshierarkitype kalt "Gjenstand" for å opprette et hierarki som inkluderer stillinger som er ansvarlig for å arbeide med oppryddingsproduktet.</span><span class="sxs-lookup"><span data-stu-id="f0027-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="f0027-209">Tilordne lederstillingen til stillingen som regnskapsfører-A-stillingen rapporterer til i gjenstand-hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f0027-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="f0027-210">Bruk stillingshierarkiet til å vise rapporteringsstrukturen til stillinger.</span><span class="sxs-lookup"><span data-stu-id="f0027-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="f0027-211">Hvis du har flere stillingshierarkier, kan du vise hierarkiet for hver hierarkitype i stillingshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f0027-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="f0027-212">Du kan også søke etter en stilling etter stillings-ID eller etter navnet på arbeideren som er tilordnet til stillingen.</span><span class="sxs-lookup"><span data-stu-id="f0027-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="f0027-213">Stillingshierarkiet er et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f0027-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="f0027-214">Poster med gyldighet fra dato</span><span class="sxs-lookup"><span data-stu-id="f0027-214">Date effective records</span></span>
<span data-ttu-id="f0027-215">For noen poster kan du angi fremtidige endringer i posten.</span><span class="sxs-lookup"><span data-stu-id="f0027-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="f0027-216">Følgende informasjon er gyldig dato.</span><span class="sxs-lookup"><span data-stu-id="f0027-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f0027-217">Poster</span><span class="sxs-lookup"><span data-stu-id="f0027-217">Records</span></span></th>
<th><span data-ttu-id="f0027-218">Gyldig datoinformasjon</span><span class="sxs-lookup"><span data-stu-id="f0027-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0027-219">Jobber</span><span class="sxs-lookup"><span data-stu-id="f0027-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="f0027-220">Noe detaljert jobbinformasjon</span><span class="sxs-lookup"><span data-stu-id="f0027-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="f0027-221">Jobbklassifiseringsinformasjon</span><span class="sxs-lookup"><span data-stu-id="f0027-221">Job classification information</span></span></li>
<li><span data-ttu-id="f0027-222">Kompensasjonsinformasjon</span><span class="sxs-lookup"><span data-stu-id="f0027-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0027-223">Posisjoner</span><span class="sxs-lookup"><span data-stu-id="f0027-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="f0027-224">Noe detaljert stillingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="f0027-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="f0027-225">Arbeidertilordninger</span><span class="sxs-lookup"><span data-stu-id="f0027-225">Worker assignments</span></span></li>
<li><span data-ttu-id="f0027-226">Stillingsvarigheter</span><span class="sxs-lookup"><span data-stu-id="f0027-226">Position durations</span></span></li>
<li><span data-ttu-id="f0027-227">Stillingshierarkier</span><span class="sxs-lookup"><span data-stu-id="f0027-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f0027-228">Du kan endre informasjonen som er nevnt i den forrige tabellen for en stilling eller en jobb og angi en dato når endringene i stillingen eller jobben skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="f0027-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="f0027-229">En stilling kan for eksempel bare tilordnes én arbeider, men Sanjay Patel, som er tilordnet til stillingen regnskapsfører-A, skal slutte om to uker.</span><span class="sxs-lookup"><span data-stu-id="f0027-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="f0027-230">Joe Healy erstatter Sanjay Patel når han slutter.</span><span class="sxs-lookup"><span data-stu-id="f0027-230">Joe Healy will replace Sanjay Patel when he leaves.</span></span> <span data-ttu-id="f0027-231">Selv om Sanjay fremdeles er tilordnet stillingen sin, kan du tilordne Joe Healy til samme stilling slik at tilordningen bare gjelder etter Sanjays siste dag.</span><span class="sxs-lookup"><span data-stu-id="f0027-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>






