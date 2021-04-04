---
title: Definer opplæringskurs
description: Personaladministratorer og ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om opplæringen som tilbys ansatte.
author: andreabichsel
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e642146701edad6b2275156e89048bc5a418c8a0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467921"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="eeaae-103">Definer opplæringskurs</span><span class="sxs-lookup"><span data-stu-id="eeaae-103">Set up training courses</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eeaae-104">Personaladministratorer og ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om opplæringen som tilbys ansatte.</span><span class="sxs-lookup"><span data-stu-id="eeaae-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="eeaae-105"> Definer forutsetninger</span><span class="sxs-lookup"><span data-stu-id="eeaae-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="eeaae-106">Følgende informasjon er obligatorisk og må defineres før du oppretter kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="eeaae-107">**Kurstyper**</span><span class="sxs-lookup"><span data-stu-id="eeaae-107">**Course types**</span></span>

<span data-ttu-id="eeaae-108">Følgende informasjon er valgfri informasjon som du kan angi for kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="eeaae-109">Hvis du vet at du skal skrive inn denne informasjonen for kursene, bør du få denne informasjonen på plass før du oppretter kursposter.</span><span class="sxs-lookup"><span data-stu-id="eeaae-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="eeaae-110">**Kurslokalegrupper**</span><span class="sxs-lookup"><span data-stu-id="eeaae-110">**Classroom groups**</span></span>
-   <span data-ttu-id="eeaae-111">**Kursgrupper**</span><span class="sxs-lookup"><span data-stu-id="eeaae-111">**Course groups**</span></span>
-   <span data-ttu-id="eeaae-112">**Kurslokasjoner**</span><span class="sxs-lookup"><span data-stu-id="eeaae-112">**Course locations**</span></span>
-   <span data-ttu-id="eeaae-113">**Kurslokaler**</span><span class="sxs-lookup"><span data-stu-id="eeaae-113">**Classrooms**</span></span>
-   <span data-ttu-id="eeaae-114">**Instruktører**</span><span class="sxs-lookup"><span data-stu-id="eeaae-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="eeaae-115">Kurstyper</span><span class="sxs-lookup"><span data-stu-id="eeaae-115">Course types</span></span>
<span data-ttu-id="eeaae-116">Du kan bruke kurstyper til å kategorisere kurs i henhold til strukturen eller innholdet i kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="eeaae-117">Du kan opprette kurstyper på siden **Kurstyper**.</span><span class="sxs-lookup"><span data-stu-id="eeaae-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="eeaae-118">Du må velge en kurstype når du oppretter en kurspost.</span><span class="sxs-lookup"><span data-stu-id="eeaae-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="eeaae-119">Oppsettype for kurs</span><span class="sxs-lookup"><span data-stu-id="eeaae-119">Course setup type</span></span>
<span data-ttu-id="eeaae-120">Tabellen nedenfor viser de tre typene oppsett for kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="eeaae-121">Oppsettyper bestemme strukturen for kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="eeaae-122">Oppsettype</span><span class="sxs-lookup"><span data-stu-id="eeaae-122">Setup type</span></span></th>
<th><span data-ttu-id="eeaae-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="eeaae-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeaae-124"><strong>Standard</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="eeaae-125">Velg denne typen for kurs som ikke har en daglig agenda.</span><span class="sxs-lookup"><span data-stu-id="eeaae-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="eeaae-126">Dette er standard oppsettypen når du oppretter et nytt kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeaae-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="eeaae-128">Velg denne typen for å planlegge detaljene for hver dag i et kurs som foregår over flere dager.</span><span class="sxs-lookup"><span data-stu-id="eeaae-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeaae-129"><strong>Agenda + økt</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="eeaae-130">Velg denne typen for mer komplekse kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="eeaae-131">Du kan for eksempel dele agendaen for kurset i spor og økter.</span><span class="sxs-lookup"><span data-stu-id="eeaae-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="eeaae-132"><strong>Spor</strong> – Spor er spesifikke emneområder for et kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="eeaae-133"><strong>Økter</strong> – Økter deler opp spor og hjelper med å identifisere bestemte prosesser eller teknikker som er relevante for sporet.</span><span class="sxs-lookup"><span data-stu-id="eeaae-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="eeaae-134">Kursoppgaver</span><span class="sxs-lookup"><span data-stu-id="eeaae-134">Course tasks</span></span>
<span data-ttu-id="eeaae-135">For hvert kurs kan du for eksempel utføre følgende oppgaver.</span><span class="sxs-lookup"><span data-stu-id="eeaae-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="eeaae-136">Registrere deltakere</span><span class="sxs-lookup"><span data-stu-id="eeaae-136">Register participants</span></span>
- <span data-ttu-id="eeaae-137">Spesifisere en registreringsfrist</span><span class="sxs-lookup"><span data-stu-id="eeaae-137">Specify a registration deadline</span></span>
- <span data-ttu-id="eeaae-138">Definere minste og største antall deltakere</span><span class="sxs-lookup"><span data-stu-id="eeaae-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="eeaae-139">Tilordne en kurslokasjon og et klasserom</span><span class="sxs-lookup"><span data-stu-id="eeaae-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="eeaae-140">Anbefale hoteller for kursdeltakere</span><span class="sxs-lookup"><span data-stu-id="eeaae-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="eeaae-141">Opprette en kursbeskrivelse som du deretter annonserer i Ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="eeaae-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="eeaae-142">**Obs!** Du kan slette et kurs bare hvis ingen er registrert for kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="eeaae-143">Kursstatuser</span><span class="sxs-lookup"><span data-stu-id="eeaae-143">Course statuses</span></span>
<span data-ttu-id="eeaae-144">Tabellen nedenfor viser de mulige kursstatusene og handlingene du kan fullføre når kurset er en bestemt status.</span><span class="sxs-lookup"><span data-stu-id="eeaae-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="eeaae-145">Status</span><span class="sxs-lookup"><span data-stu-id="eeaae-145">Status</span></span></th>
<th><span data-ttu-id="eeaae-146">Handlinger</span><span class="sxs-lookup"><span data-stu-id="eeaae-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeaae-147"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="eeaae-148">Skriv inn og endre kursinformasjon.</span><span class="sxs-lookup"><span data-stu-id="eeaae-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="eeaae-149">Endre kursstatusen til <strong>Åpen</strong> slik at arbeidere kan melde seg på kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeaae-150"><strong>Åpne</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="eeaae-151">Registrer deltakere på kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="eeaae-152">Fjern deltakere fra kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="eeaae-153">Bekreft deltakere for kurset.</span><span class="sxs-lookup"><span data-stu-id="eeaae-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="eeaae-154">Endre kursstatus til<strong> Lukket</strong> eller <strong>Avbrutt</strong>.</span><span class="sxs-lookup"><span data-stu-id="eeaae-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="eeaae-155">Planlegg spørreskjemaer for deltakere med statusen <strong>Bekreftet</strong>.</span><span class="sxs-lookup"><span data-stu-id="eeaae-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeaae-156"><strong>Lukket</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="eeaae-157">Du kan åpne kurset på nytt.</span><span class="sxs-lookup"><span data-stu-id="eeaae-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeaae-158"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="eeaae-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="eeaae-159">Du kan åpne kurset på nytt.</span><span class="sxs-lookup"><span data-stu-id="eeaae-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="eeaae-160">Kursdeltakere</span><span class="sxs-lookup"><span data-stu-id="eeaae-160">Course participants</span></span>
<span data-ttu-id="eeaae-161">Kursdeltakere er arbeidere som deltar på et opplæringskurs eller et arrangement.</span><span class="sxs-lookup"><span data-stu-id="eeaae-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="eeaae-162">Du kan bare registrere deltakere for åpne kurs.</span><span class="sxs-lookup"><span data-stu-id="eeaae-162">You can only register participants for open courses.</span></span> <span data-ttu-id="eeaae-163">Det største og minste antallet deltakere som kan meldes på et kurs, er definert på hurtigfanen **Generelt** på siden **Kurs**.</span><span class="sxs-lookup"><span data-stu-id="eeaae-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="eeaae-164">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="eeaae-164">Workflow</span></span>
--------

<span data-ttu-id="eeaae-165">Ansatte som registrerer seg for et kurs via siden **Ansattselvbetjening**, kan rute registreringen gjennom arbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="eeaae-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="eeaae-166">Du kan tilordne en arbeidsflyt til et kurs i hurtigfanen **Generelt** på **Kurs**-siden.</span><span class="sxs-lookup"><span data-stu-id="eeaae-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>







[!INCLUDE[footer-include](../includes/footer-banner.md)]