---
title: Konfigurere komponenter for en jobb
description: "Dette emnet beskriver de grunnleggende elementene som en jobb kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: b3fec97811c5096e81d7adb3d1a304b11a6fd788
ms.contentlocale: nb-no
ms.lasthandoff: 01/19/2018

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="3c0c0-103">Konfigurere komponenter for en jobb</span><span class="sxs-lookup"><span data-stu-id="3c0c0-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="3c0c0-104">Dette emnet beskriver de grunnleggende elementene som en jobb kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="3c0c0-105">Før du kan opprette jobber, må du definere litt referanseinformasjon.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="3c0c0-106">Du kan opprette en jobb med bare ett navn.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-106">You can create a job that has only a name.</span></span> <span data-ttu-id="3c0c0-107">Ved å inkludere tilleggsinformasjon, for eksempel en jobbtittel, angir du imidlertid standardverdier for stillinger som er knyttet til jobben.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="3c0c0-108">Noe av informasjonen du angir kan dessuten brukes til å filtrere kompensasjonsplaner på bestemte jobber.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="3c0c0-109">Hvis du vil definere berettigelse som du kan bruke til å filtrere kompensasjonsplaner på en bestemt jobb, bør du sette opp jobbfunksjoner og jobbtyper før du setter opp jobber.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="3c0c0-110">Ved å ha disse standardverdiene tilgjengelige, sparer du tid når du legger til stillinger for jobben.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="3c0c0-111">Noen jobbdetaljer, for eksempel tittel, type og funksjon, er datoeffektive.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="3c0c0-112">Hvis du oppretter en jobb i dag, men ikke legger til disse detaljene før senere, og du deretter ser på jobben på opprettelsesdatoen, vises ikke disse detaljene.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="3c0c0-113">Derfor bør du opprette noe av denne referanseinformasjon før du trenger den.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="3c0c0-114">På denne måten kan du legge til informasjonen for nye jobber når du oppretter dem.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="3c0c0-115">Jobbtitler</span><span class="sxs-lookup"><span data-stu-id="3c0c0-115">Job titles</span></span>
<span data-ttu-id="3c0c0-116">Før du oppretter jobber, må du definere titler for disse jobbene.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="3c0c0-117">Stillinger arver jobbtitler fra jobbene som stillingene er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="3c0c0-118">Vedlikehold jobbtitler ved hjelp av **Titler**-siden, som du kan åpne ved hjelp av funksjonen Søk.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="3c0c0-119">På **Titler **-siden skriver du inn titlene du har tenkt å bruke for jobbene.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="3c0c0-120">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="3c0c0-120">Job types</span></span>
<span data-ttu-id="3c0c0-121">Du bruker jobbtyper til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="3c0c0-122">Jobbtyper er ikke nødvendige.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-122">Job types aren't required.</span></span> <span data-ttu-id="3c0c0-123">Men hvis du har tenkt å bruke jobbtyper når du definerer rettighetsregler for kompensasjonsstyring, bør du definere jobbtyper før du definerer jobber.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="3c0c0-124">Noen eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="3c0c0-125">Du vedlikeholder jobbtyper ved hjelp av **Jobbtyper**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="3c0c0-126">Angi et navn for jobbtypen og en kort beskrivelse av den på **Jobbtyper**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="3c0c0-127">I feltet **Status, fritatt fra avgift** velger du ett av følgende alternativer for å angi fritaksstatusen fra avgifter Fair Labor Standards Act (FLSA) for jobber som har denne jobbtypen:</span><span class="sxs-lookup"><span data-stu-id="3c0c0-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="3c0c0-128">**Avgiftsfri** – Jobber er fritatt fra overtid under FLSA.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="3c0c0-129">**Ikke fritatt fra avgift** – Jobber er ikke fritatt fra overtid under FLSA.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="3c0c0-130">**Gjelder ikke** – FLSA-dekning er ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="3c0c0-131">Jobbfunksjoner</span><span class="sxs-lookup"><span data-stu-id="3c0c0-131">Job functions</span></span>
<span data-ttu-id="3c0c0-132">Jobbfunksjoner beskriver funksjonskategori på høynivåplan og relaterer avgifter på høyt nivå.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="3c0c0-133">Jobbfunksjoner er ikke nødvendige.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-133">Job functions aren't required.</span></span> <span data-ttu-id="3c0c0-134">Du kan bruke jobbfunksjoner sammen med jobbtyper for å filtrere kompensasjonsplaner for bestemte jobber.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="3c0c0-135">Du tilordninger jobbfunksjoner og jobbtyper med kompensasjonsplaner ved å definere rettighetsregler på siden **Rettighetsregler**.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="3c0c0-136">Du kan deretter knytte et sett med nivåer til kompensasjonsplanen som gjelder en kombinasjon av jobbtype og jobbfunksjon som du har definert gjennom en rettighetsregel.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="3c0c0-137">(Disse funksjonene gjelder både faste og variable kompensasjonsplaner.) Jobbfunksjoner er ikke nødvendige, men hvis du har tenkt å bruke jobbfunksjoner når du definerer rettighetsregler for kompensasjonsstyring, bør du definere jobbfunksjoner før du definerer jobber.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="3c0c0-138">Tabellen nedenfor viser noen eksempler på jobbfunksjoner.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="3c0c0-139">Jobb</span><span class="sxs-lookup"><span data-stu-id="3c0c0-139">Job</span></span>           | <span data-ttu-id="3c0c0-140">Jobbfunksjon</span><span class="sxs-lookup"><span data-stu-id="3c0c0-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="3c0c0-141">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="3c0c0-141">Sales manager</span></span> | <span data-ttu-id="3c0c0-142">Mellomleder</span><span class="sxs-lookup"><span data-stu-id="3c0c0-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="3c0c0-143">Regnskapsfører</span><span class="sxs-lookup"><span data-stu-id="3c0c0-143">Accountant</span></span>    | <span data-ttu-id="3c0c0-144">Eksperter</span><span class="sxs-lookup"><span data-stu-id="3c0c0-144">Professionals</span></span>        |

<span data-ttu-id="3c0c0-145">Du vedlikeholder jobbfunksjoner ved hjelp av **Jobbfunksjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="3c0c0-146">Angi en ID-kode og en kort beskrivelse av jobbfunksjonen på siden **Jobbfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="3c0c0-147">Jobboppgaver</span><span class="sxs-lookup"><span data-stu-id="3c0c0-147">Job tasks</span></span>
<span data-ttu-id="3c0c0-148">Jobboppgaver beskriver de grunnleggende oppgavene som må fullføres av en arbeider i en stilling for jobben.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="3c0c0-149">Den samme jobboppgaven kan legges til flere jobber, og til stillinger for jobbene som bruker disse jobboppgavene.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="3c0c0-150">Tabellen nedenfor viser noen eksempler på jobboppgaver.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3c0c0-151">Jobb</span><span class="sxs-lookup"><span data-stu-id="3c0c0-151">Job</span></span></th>
<th><span data-ttu-id="3c0c0-152">Jobboppgave</span><span class="sxs-lookup"><span data-stu-id="3c0c0-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c0c0-153">Salgssjef</span><span class="sxs-lookup"><span data-stu-id="3c0c0-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="3c0c0-154"><strong>Ytelsesgjennomgang</strong> – Vurder jobbytelsen til hver enkelt selger.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="3c0c0-155"><strong>Fraværsgjennomgang</strong> – Godkjenn eller avvis fraværsforespørsler eller registreringer for hver selger.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c0c0-156">Regnskapsfører</span><span class="sxs-lookup"><span data-stu-id="3c0c0-156">Accountant</span></span></td>
<td><span data-ttu-id="3c0c0-157"><strong>Finansrapport</strong> – Vis ukentlige finansrapporter til økonomisjef.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c0c0-158">Du vedlikeholder jobboppgaver ved hjelp av **Jobboppgaver**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="3c0c0-159">Angi et navn for jobboppgaven og en kort beskrivelse av den på **Jobboppgaver**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="3c0c0-160">Du kan legge inn tilleggsinformasjon i **Merknad**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="3c0c0-161">Notatene kan oppdateres for en bestemt jobb uten å endre notatene du har angitt her.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="3c0c0-162">Ansvarsområder</span><span class="sxs-lookup"><span data-stu-id="3c0c0-162">Areas of responsibility</span></span>
<span data-ttu-id="3c0c0-163">Du bruker ansvarsområder for å angi arbeidsrollene, prosessene og produktene som en arbeider som er i en stilling for jobben, har ansvaret for.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="3c0c0-164">Et eksempel på et ansvarsområde for en jobb med navnet "Regnskap" kan være "Økonomisk rapportering for produkt A".</span><span class="sxs-lookup"><span data-stu-id="3c0c0-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="3c0c0-165">Du vedlikeholder ansvarsområder ved hjelp av **Ansvarsområder**-siden, som du finner ved hjelp av funksjonen Søk.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="3c0c0-166">Angi et navn for ansvaret og en kort beskrivelse av det på **Ansvarsområder**-siden.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="3c0c0-167">Du kan legge inn tilleggsinformasjon i **Merknad**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="3c0c0-168">Notatene kan oppdateres for en bestemt jobb uten å endre notatene du har angitt her.</span><span class="sxs-lookup"><span data-stu-id="3c0c0-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>




