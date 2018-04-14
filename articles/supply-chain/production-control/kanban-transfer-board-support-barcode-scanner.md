---
title: "Støtte for Kanban-overføringskort for strekkodelesere"
description: "Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0696580dcf50139639dace641169d041021cf1b8
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="352e1-103">Støtte for Kanban-overføringskort for strekkodelesere</span><span class="sxs-lookup"><span data-stu-id="352e1-103">Kanban transfer board support for barcode scanners</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="352e1-104">Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.</span><span class="sxs-lookup"><span data-stu-id="352e1-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="352e1-105">Registreringsmoduser</span><span class="sxs-lookup"><span data-stu-id="352e1-105">Registration modes</span></span>
------------------

<span data-ttu-id="352e1-106">I hurtigkategorien **Skanner - registrering** kan du velge registreringsmodus, som styrer handlingen når du skanner et Kanban-kortnummer eller skriver inn nummeret manuelt i feltet Kanban-kortnummer.</span><span class="sxs-lookup"><span data-stu-id="352e1-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="352e1-107">Angi registreringsmodus</span><span class="sxs-lookup"><span data-stu-id="352e1-107">Set registration mode</span></span> | <span data-ttu-id="352e1-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="352e1-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="352e1-109">Starte</span><span class="sxs-lookup"><span data-stu-id="352e1-109">Start</span></span>                 | <span data-ttu-id="352e1-110">Registrerer en Kanban-overføringsjobb som pågående.</span><span class="sxs-lookup"><span data-stu-id="352e1-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="352e1-111">Fullført</span><span class="sxs-lookup"><span data-stu-id="352e1-111">Complete</span></span>              | <span data-ttu-id="352e1-112">Registrerer en Kanban-overføringsjobb som fullført.</span><span class="sxs-lookup"><span data-stu-id="352e1-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="352e1-113">Tom</span><span class="sxs-lookup"><span data-stu-id="352e1-113">Empty</span></span>                 | <span data-ttu-id="352e1-114">Registrerer materialhåndteringsenheten som et Kanban-kort refererer til, som tomt.</span><span class="sxs-lookup"><span data-stu-id="352e1-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="352e1-115">Velg</span><span class="sxs-lookup"><span data-stu-id="352e1-115">Select</span></span>                | <span data-ttu-id="352e1-116">Registrerer et Kanban-kortnummer og velger den refererte jobben automatisk i Kanban-listen.</span><span class="sxs-lookup"><span data-stu-id="352e1-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="352e1-117">Registreringsmodusen Velg</span><span class="sxs-lookup"><span data-stu-id="352e1-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="352e1-118">Når du bruker en strekkodeleser til å velge en jobb, endres visningsmodusen for Kanban-kortet.</span><span class="sxs-lookup"><span data-stu-id="352e1-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="352e1-119">I denne modusen gjelder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="352e1-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="352e1-120">Bare den skannede Kanban-jobben vises.</span><span class="sxs-lookup"><span data-stu-id="352e1-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="352e1-121">Detaljene om den valgte jobben vises i hurtigkategorien **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="352e1-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="352e1-122">**Meldinger**-hurtigkategorien viser meldinger bare for den valgte jobben.</span><span class="sxs-lookup"><span data-stu-id="352e1-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="352e1-123">Du kan endre statusen på jobben ved hjelp av funksjonene som er tilgjengelige i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="352e1-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="352e1-124">Kanban-overføringskortet fortsetter å vise bare én jobb i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="352e1-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="352e1-125">Du kan oppdatere informasjonen i listen over jobber manuelt ved å klikke **Oppdater** (SKIFT+F5) i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="352e1-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="352e1-126">Når du oppdaterer informasjonen, vises alle resultatene for jobbfilteret på nytt.</span><span class="sxs-lookup"><span data-stu-id="352e1-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="352e1-127">Jobbstatus og mulige handlinger</span><span class="sxs-lookup"><span data-stu-id="352e1-127">Job status and possible actions</span></span>
<span data-ttu-id="352e1-128">Statusen for den valgte jobben og statusen for tilknyttede jobber for hendelses-Kanbaner, bestemmer om du kan behandle jobben ytterligere.</span><span class="sxs-lookup"><span data-stu-id="352e1-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="352e1-129">Tabellen nedenfor viser informasjon om disse statusene og oppgavene:</span><span class="sxs-lookup"><span data-stu-id="352e1-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="352e1-130">Statusene som er tilgjengelige for jobber eller for håndteringsenhetene som jobbene refererer til.</span><span class="sxs-lookup"><span data-stu-id="352e1-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="352e1-131">Hver oppgave du kan utføre for jobben.</span><span class="sxs-lookup"><span data-stu-id="352e1-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="352e1-132">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="352e1-132">Job type</span></span></th>
<th><span data-ttu-id="352e1-133">Jobbstatusen eller statusen for håndteringsenheten</span><span class="sxs-lookup"><span data-stu-id="352e1-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="352e1-134">Oppdater plukkliste</span><span class="sxs-lookup"><span data-stu-id="352e1-134">Update picking list</span></span></th>
<th><span data-ttu-id="352e1-135">Starte</span><span class="sxs-lookup"><span data-stu-id="352e1-135">Start</span></span></th>
<th><span data-ttu-id="352e1-136">Oppdater registrering</span><span class="sxs-lookup"><span data-stu-id="352e1-136">Update registration</span></span></th>
<th><span data-ttu-id="352e1-137">Fullført</span><span class="sxs-lookup"><span data-stu-id="352e1-137">Complete</span></span></th>
<th><span data-ttu-id="352e1-138">Tom</span><span class="sxs-lookup"><span data-stu-id="352e1-138">Empty</span></span></th>
<th><span data-ttu-id="352e1-139">Opprett hendelses-Kanbaner</span><span class="sxs-lookup"><span data-stu-id="352e1-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="352e1-140">Overføring</span><span class="sxs-lookup"><span data-stu-id="352e1-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="352e1-141">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="352e1-141">Not planned</span></span></li>
<li><span data-ttu-id="352e1-142">Ingen tilknyttede jobber, eller tilknyttede jobber er fullført</span><span class="sxs-lookup"><span data-stu-id="352e1-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="352e1-143">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-143">Yes</span></span></td>
<td><span data-ttu-id="352e1-144">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-144">Yes</span></span></td>
<td><span data-ttu-id="352e1-145">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-145">Yes</span></span></td>
<td><span data-ttu-id="352e1-146">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-146">Yes</span></span></td>
<td><span data-ttu-id="352e1-147">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-147">No</span></span></td>
<td><span data-ttu-id="352e1-148">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="352e1-149">Overføring</span><span class="sxs-lookup"><span data-stu-id="352e1-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="352e1-150">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="352e1-150">Not planned</span></span></li>
<li><span data-ttu-id="352e1-151">Den tilknyttede jobben er ikke fullført</span><span class="sxs-lookup"><span data-stu-id="352e1-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="352e1-152">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-152">Yes</span></span></td>
<td><span data-ttu-id="352e1-153">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-153">No</span></span></td>
<td><span data-ttu-id="352e1-154">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-154">Yes</span></span></td>
<td><span data-ttu-id="352e1-155">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-155">No</span></span></td>
<td><span data-ttu-id="352e1-156">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-156">No</span></span></td>
<td><span data-ttu-id="352e1-157">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="352e1-158">Overføring</span><span class="sxs-lookup"><span data-stu-id="352e1-158">Transfer</span></span></td>
<td><span data-ttu-id="352e1-159">Pågår</span><span class="sxs-lookup"><span data-stu-id="352e1-159">In progress</span></span></td>
<td><span data-ttu-id="352e1-160">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-160">Yes</span></span></td>
<td><span data-ttu-id="352e1-161">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-161">No</span></span></td>
<td><span data-ttu-id="352e1-162">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-162">Yes</span></span></td>
<td><span data-ttu-id="352e1-163">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-163">Yes</span></span></td>
<td><span data-ttu-id="352e1-164">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-164">No</span></span></td>
<td><span data-ttu-id="352e1-165">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="352e1-166">Overføring</span><span class="sxs-lookup"><span data-stu-id="352e1-166">Transfer</span></span></td>
<td><span data-ttu-id="352e1-167">Fullført</span><span class="sxs-lookup"><span data-stu-id="352e1-167">Completed</span></span></td>
<td><span data-ttu-id="352e1-168">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-168">No</span></span></td>
<td><span data-ttu-id="352e1-169">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-169">No</span></span></td>
<td><span data-ttu-id="352e1-170">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-170">No</span></span></td>
<td><span data-ttu-id="352e1-171">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-171">No</span></span></td>
<td><span data-ttu-id="352e1-172">Ja</span><span class="sxs-lookup"><span data-stu-id="352e1-172">Yes</span></span></td>
<td><span data-ttu-id="352e1-173">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="352e1-174">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="352e1-174">Transfer or process</span></span></td>
<td><span data-ttu-id="352e1-175">Tom</span><span class="sxs-lookup"><span data-stu-id="352e1-175">Empty</span></span></td>
<td><span data-ttu-id="352e1-176">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-176">No</span></span></td>
<td><span data-ttu-id="352e1-177">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-177">No</span></span></td>
<td><span data-ttu-id="352e1-178">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-178">No</span></span></td>
<td><span data-ttu-id="352e1-179">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-179">No</span></span></td>
<td><span data-ttu-id="352e1-180">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-180">No</span></span></td>
<td><span data-ttu-id="352e1-181">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="352e1-182">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="352e1-182">Transfer or process</span></span></td>
<td><span data-ttu-id="352e1-183">Finner ikke et Kanban-kort</span><span class="sxs-lookup"><span data-stu-id="352e1-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="352e1-184">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-184">No</span></span></td>
<td><span data-ttu-id="352e1-185">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-185">No</span></span></td>
<td><span data-ttu-id="352e1-186">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-186">No</span></span></td>
<td><span data-ttu-id="352e1-187">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-187">No</span></span></td>
<td><span data-ttu-id="352e1-188">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-188">No</span></span></td>
<td><span data-ttu-id="352e1-189">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="352e1-190">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="352e1-190">Transfer or process</span></span></td>
<td><span data-ttu-id="352e1-191">Det er funnet et Kanban-kort, men det er ikke tilordnet til en Kanban</span><span class="sxs-lookup"><span data-stu-id="352e1-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="352e1-192">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-192">No</span></span></td>
<td><span data-ttu-id="352e1-193">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-193">No</span></span></td>
<td><span data-ttu-id="352e1-194">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-194">No</span></span></td>
<td><span data-ttu-id="352e1-195">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-195">No</span></span></td>
<td><span data-ttu-id="352e1-196">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-196">No</span></span></td>
<td><span data-ttu-id="352e1-197">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="352e1-198">Behandle</span><span class="sxs-lookup"><span data-stu-id="352e1-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="352e1-199">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="352e1-199">Not planned</span></span></li>
<li><span data-ttu-id="352e1-200">Klargjort</span><span class="sxs-lookup"><span data-stu-id="352e1-200">Prepared</span></span></li>
<li><span data-ttu-id="352e1-201">Pågår</span><span class="sxs-lookup"><span data-stu-id="352e1-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="352e1-202">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-202">No</span></span></td>
<td><span data-ttu-id="352e1-203">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-203">No</span></span></td>
<td><span data-ttu-id="352e1-204">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-204">No</span></span></td>
<td><span data-ttu-id="352e1-205">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-205">No</span></span></td>
<td><span data-ttu-id="352e1-206">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-206">No</span></span></td>
<td><span data-ttu-id="352e1-207">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="352e1-208">Behandle</span><span class="sxs-lookup"><span data-stu-id="352e1-208">Process</span></span></td>
<td><span data-ttu-id="352e1-209">Fullført</span><span class="sxs-lookup"><span data-stu-id="352e1-209">Completed</span></span></td>
<td><span data-ttu-id="352e1-210">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-210">No</span></span></td>
<td><span data-ttu-id="352e1-211">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-211">No</span></span></td>
<td><span data-ttu-id="352e1-212">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-212">No</span></span></td>
<td><span data-ttu-id="352e1-213">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-213">No</span></span></td>
<td><span data-ttu-id="352e1-214">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-214">No</span></span></td>
<td><span data-ttu-id="352e1-215">Antall</span><span class="sxs-lookup"><span data-stu-id="352e1-215">No</span></span></td>
</tr>
</tbody>
</table>






