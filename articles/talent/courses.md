---
title: "Definer opplæringskurs"
description: "Personaladministratorer og ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om opplæringen som tilbys ansatte."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0b28c62fe586102a3fb98d77edbea2c06bcf852
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-training-courses"></a><span data-ttu-id="19fb1-103">Definer opplæringskurs</span><span class="sxs-lookup"><span data-stu-id="19fb1-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="19fb1-104">Personaladministratorer og ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om opplæringen som tilbys ansatte.</span><span class="sxs-lookup"><span data-stu-id="19fb1-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="19fb1-105"> Definer forutsetninger</span><span class="sxs-lookup"><span data-stu-id="19fb1-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="19fb1-106">Følgende informasjon er obligatorisk og må defineres før du oppretter kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="19fb1-107">**Kurstyper**</span><span class="sxs-lookup"><span data-stu-id="19fb1-107">**Course types**</span></span>

<span data-ttu-id="19fb1-108">Følgende informasjon er valgfri informasjon som du kan angi for kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="19fb1-109">Hvis du vet at du skal skrive inn denne informasjonen for kursene, bør du få denne informasjonen på plass før du oppretter kursposter.</span><span class="sxs-lookup"><span data-stu-id="19fb1-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="19fb1-110">**Kurslokalegrupper**</span><span class="sxs-lookup"><span data-stu-id="19fb1-110">**Classroom groups**</span></span>
-   <span data-ttu-id="19fb1-111">**Kursgrupper**</span><span class="sxs-lookup"><span data-stu-id="19fb1-111">**Course groups**</span></span>
-   <span data-ttu-id="19fb1-112">**Kurslokasjoner**</span><span class="sxs-lookup"><span data-stu-id="19fb1-112">**Course locations**</span></span>
-   <span data-ttu-id="19fb1-113">**Kurslokaler**</span><span class="sxs-lookup"><span data-stu-id="19fb1-113">**Classrooms**</span></span>
-   <span data-ttu-id="19fb1-114">**Instruktører**</span><span class="sxs-lookup"><span data-stu-id="19fb1-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="19fb1-115">Kurstyper</span><span class="sxs-lookup"><span data-stu-id="19fb1-115">Course types</span></span>
<span data-ttu-id="19fb1-116">Du kan bruke kurstyper til å kategorisere kurs i henhold til strukturen eller innholdet i kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="19fb1-117">Du kan opprette kurstyper på siden **Kurstyper**.</span><span class="sxs-lookup"><span data-stu-id="19fb1-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="19fb1-118">Du må velge en kurstype når du oppretter en kurspost.</span><span class="sxs-lookup"><span data-stu-id="19fb1-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="19fb1-119">Oppsettype for kurs</span><span class="sxs-lookup"><span data-stu-id="19fb1-119">Course setup type</span></span>
<span data-ttu-id="19fb1-120">Tabellen nedenfor viser de tre typene oppsett for kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="19fb1-121">Oppsettyper bestemme strukturen for kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19fb1-122">Oppsettype</span><span class="sxs-lookup"><span data-stu-id="19fb1-122">Setup type</span></span></th>
<th><span data-ttu-id="19fb1-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="19fb1-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19fb1-124"><strong>Standard</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="19fb1-125">Velg denne typen for kurs som ikke har en daglig agenda.</span><span class="sxs-lookup"><span data-stu-id="19fb1-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="19fb1-126">Dette er standard oppsettypen når du oppretter et nytt kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19fb1-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="19fb1-128">Velg denne typen for å planlegge detaljene for hver dag i et kurs som foregår over flere dager.</span><span class="sxs-lookup"><span data-stu-id="19fb1-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19fb1-129"><strong>Agenda + økt</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="19fb1-130">Velg denne typen for mer komplekse kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="19fb1-131">Du kan for eksempel dele agendaen for kurset i spor og økter.</span><span class="sxs-lookup"><span data-stu-id="19fb1-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="19fb1-132"><strong>Spor</strong> – Spor er spesifikke emneområder for et kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="19fb1-133"><strong>Økter</strong> – Økter deler opp spor og hjelper med å identifisere bestemte prosesser eller teknikker som er relevante for sporet.</span><span class="sxs-lookup"><span data-stu-id="19fb1-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="19fb1-134">Kursoppgaver</span><span class="sxs-lookup"><span data-stu-id="19fb1-134">Course tasks</span></span>
<span data-ttu-id="19fb1-135">For hvert kurs kan du for eksempel utføre følgende oppgaver.</span><span class="sxs-lookup"><span data-stu-id="19fb1-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="19fb1-136">Registrere deltakere</span><span class="sxs-lookup"><span data-stu-id="19fb1-136">Register participants</span></span>
-   <span data-ttu-id="19fb1-137">Spesifisere en registreringsfrist</span><span class="sxs-lookup"><span data-stu-id="19fb1-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="19fb1-138">Definere minste og største antall deltakere</span><span class="sxs-lookup"><span data-stu-id="19fb1-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="19fb1-139">Tilordne en kurslokasjon og et klasserom</span><span class="sxs-lookup"><span data-stu-id="19fb1-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="19fb1-140">Anbefale hoteller for kursdeltakere</span><span class="sxs-lookup"><span data-stu-id="19fb1-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="19fb1-141">Opprette en kursbeskrivelse som du deretter annonserer i Ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="19fb1-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="19fb1-142">**Obs!** Du kan slette et kurs bare hvis ingen er registrert for kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="19fb1-143">Kursstatuser</span><span class="sxs-lookup"><span data-stu-id="19fb1-143">Course statuses</span></span>
<span data-ttu-id="19fb1-144">Tabellen nedenfor viser de mulige kursstatusene og handlingene du kan fullføre når kurset er en bestemt status.</span><span class="sxs-lookup"><span data-stu-id="19fb1-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19fb1-145">Status</span><span class="sxs-lookup"><span data-stu-id="19fb1-145">Status</span></span></th>
<th><span data-ttu-id="19fb1-146">Handlinger</span><span class="sxs-lookup"><span data-stu-id="19fb1-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19fb1-147"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="19fb1-148">Skriv inn og endre kursinformasjon.</span><span class="sxs-lookup"><span data-stu-id="19fb1-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="19fb1-149">Endre kursstatusen til <strong>Åpen</strong> slik at arbeidere kan melde seg på kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19fb1-150"><strong>Åpne</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="19fb1-151">Registrer deltakere på kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="19fb1-152">Fjern deltakere fra kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="19fb1-153">Bekreft deltakere for kurset.</span><span class="sxs-lookup"><span data-stu-id="19fb1-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="19fb1-154">Endre kursstatus til<strong> Lukket</strong> eller <strong>Avbrutt</strong>.</span><span class="sxs-lookup"><span data-stu-id="19fb1-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="19fb1-155">Planlegg spørreskjemaer for deltakere med statusen <strong>Bekreftet</strong>.</span><span class="sxs-lookup"><span data-stu-id="19fb1-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19fb1-156"><strong>Lukket</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="19fb1-157">Du kan åpne kurset på nytt.</span><span class="sxs-lookup"><span data-stu-id="19fb1-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19fb1-158"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="19fb1-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="19fb1-159">Du kan åpne kurset på nytt.</span><span class="sxs-lookup"><span data-stu-id="19fb1-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="19fb1-160">Kursdeltakere</span><span class="sxs-lookup"><span data-stu-id="19fb1-160">Course participants</span></span>
<span data-ttu-id="19fb1-161">Kursdeltakere er arbeidere, søkere eller kontakter som deltar på et opplæringskurs eller et arrangement.</span><span class="sxs-lookup"><span data-stu-id="19fb1-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="19fb1-162">Du kan bare registrere deltakere for åpne kurs.</span><span class="sxs-lookup"><span data-stu-id="19fb1-162">You can only register participants for open courses.</span></span> <span data-ttu-id="19fb1-163">Det største og minste antallet deltakere som kan meldes på et kurs, er definert på hurtigfanen **Generelt** på siden **Kurs**.</span><span class="sxs-lookup"><span data-stu-id="19fb1-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="19fb1-164">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="19fb1-164">Workflow</span></span>
--------

<span data-ttu-id="19fb1-165">Ansatte som registrerer seg for et kurs via siden **Ansattselvbetjening**, kan rute registreringen gjennom arbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="19fb1-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="19fb1-166">En arbeidsflyt kan tilordnes til et kurs i hurtigfanen **Generelt** på siden **Kurs**.</span><span class="sxs-lookup"><span data-stu-id="19fb1-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






