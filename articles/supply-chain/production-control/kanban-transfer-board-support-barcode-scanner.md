---
title: Støtte for Kanban-overføringskort for strekkodelesere
description: Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "319460"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="fdfc6-103">Støtte for Kanban-overføringskort for strekkodelesere</span><span class="sxs-lookup"><span data-stu-id="fdfc6-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdfc6-104">Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="fdfc6-105">Registreringsmoduser</span><span class="sxs-lookup"><span data-stu-id="fdfc6-105">Registration modes</span></span>
------------------

<span data-ttu-id="fdfc6-106">I hurtigkategorien **Skanner - registrering** kan du velge registreringsmodus, som styrer handlingen når du skanner et Kanban-kortnummer eller skriver inn nummeret manuelt i feltet Kanban-kortnummer.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="fdfc6-107">Angi registreringsmodus</span><span class="sxs-lookup"><span data-stu-id="fdfc6-107">Set registration mode</span></span> | <span data-ttu-id="fdfc6-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fdfc6-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfc6-109">Starte</span><span class="sxs-lookup"><span data-stu-id="fdfc6-109">Start</span></span>                 | <span data-ttu-id="fdfc6-110">Registrerer en Kanban-overføringsjobb som pågående.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="fdfc6-111">Fullført</span><span class="sxs-lookup"><span data-stu-id="fdfc6-111">Complete</span></span>              | <span data-ttu-id="fdfc6-112">Registrerer en Kanban-overføringsjobb som fullført.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="fdfc6-113">Tom</span><span class="sxs-lookup"><span data-stu-id="fdfc6-113">Empty</span></span>                 | <span data-ttu-id="fdfc6-114">Registrerer materialhåndteringsenheten som et Kanban-kort refererer til, som tomt.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="fdfc6-115">Velg</span><span class="sxs-lookup"><span data-stu-id="fdfc6-115">Select</span></span>                | <span data-ttu-id="fdfc6-116">Registrerer et Kanban-kortnummer og velger den refererte jobben automatisk i Kanban-listen.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="fdfc6-117">Registreringsmodusen Velg</span><span class="sxs-lookup"><span data-stu-id="fdfc6-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="fdfc6-118">Når du bruker en strekkodeleser til å velge en jobb, endres visningsmodusen for Kanban-kortet.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="fdfc6-119"> I denne modusen gjelder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="fdfc6-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="fdfc6-120">Bare den skannede Kanban-jobben vises.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="fdfc6-121">Detaljene om den valgte jobben vises i hurtigkategorien **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="fdfc6-122">**Meldinger**-hurtigkategorien viser meldinger bare for den valgte jobben.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="fdfc6-123">Du kan endre statusen på jobben ved hjelp av funksjonene som er tilgjengelige i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="fdfc6-124">Kanban-overføringskortet fortsetter å vise bare én jobb i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="fdfc6-125">Du kan oppdatere informasjonen i listen over jobber manuelt ved å klikke **Oppdater** (SKIFT+F5) i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="fdfc6-126">Når du oppdaterer informasjonen, vises alle resultatene for jobbfilteret på nytt.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="fdfc6-127">Jobbstatus og mulige handlinger</span><span class="sxs-lookup"><span data-stu-id="fdfc6-127">Job status and possible actions</span></span>
<span data-ttu-id="fdfc6-128">Statusen for den valgte jobben og statusen for tilknyttede jobber for hendelses-Kanbaner, bestemmer om du kan behandle jobben ytterligere.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="fdfc6-129">Tabellen nedenfor viser informasjon om disse statusene og oppgavene:</span><span class="sxs-lookup"><span data-stu-id="fdfc6-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="fdfc6-130">Statusene som er tilgjengelige for jobber eller for håndteringsenhetene som jobbene refererer til.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="fdfc6-131">Hver oppgave du kan utføre for jobben.</span><span class="sxs-lookup"><span data-stu-id="fdfc6-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="fdfc6-132">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="fdfc6-132">Job type</span></span></th>
<th><span data-ttu-id="fdfc6-133">Jobbstatusen eller statusen for håndteringsenheten</span><span class="sxs-lookup"><span data-stu-id="fdfc6-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="fdfc6-134">Oppdater plukkliste</span><span class="sxs-lookup"><span data-stu-id="fdfc6-134">Update picking list</span></span></th>
<th><span data-ttu-id="fdfc6-135">Starte</span><span class="sxs-lookup"><span data-stu-id="fdfc6-135">Start</span></span></th>
<th><span data-ttu-id="fdfc6-136">Oppdater registrering</span><span class="sxs-lookup"><span data-stu-id="fdfc6-136">Update registration</span></span></th>
<th><span data-ttu-id="fdfc6-137">Fullført</span><span class="sxs-lookup"><span data-stu-id="fdfc6-137">Complete</span></span></th>
<th><span data-ttu-id="fdfc6-138">Tom</span><span class="sxs-lookup"><span data-stu-id="fdfc6-138">Empty</span></span></th>
<th><span data-ttu-id="fdfc6-139">Opprett hendelses-Kanbaner</span><span class="sxs-lookup"><span data-stu-id="fdfc6-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fdfc6-140">Overføring</span><span class="sxs-lookup"><span data-stu-id="fdfc6-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="fdfc6-141">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="fdfc6-141">Not planned</span></span></li>
<li><span data-ttu-id="fdfc6-142">Ingen tilknyttede jobber, eller tilknyttede jobber er fullført</span><span class="sxs-lookup"><span data-stu-id="fdfc6-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="fdfc6-143">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-143">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-144">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-144">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-145">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-145">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-146">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-146">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-147">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-147">No</span></span></td>
<td><span data-ttu-id="fdfc6-148">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdfc6-149">Overføring</span><span class="sxs-lookup"><span data-stu-id="fdfc6-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="fdfc6-150">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="fdfc6-150">Not planned</span></span></li>
<li><span data-ttu-id="fdfc6-151">Den tilknyttede jobben er ikke fullført</span><span class="sxs-lookup"><span data-stu-id="fdfc6-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="fdfc6-152">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-152">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-153">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-153">No</span></span></td>
<td><span data-ttu-id="fdfc6-154">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-154">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-155">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-155">No</span></span></td>
<td><span data-ttu-id="fdfc6-156">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-156">No</span></span></td>
<td><span data-ttu-id="fdfc6-157">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdfc6-158">Overføring</span><span class="sxs-lookup"><span data-stu-id="fdfc6-158">Transfer</span></span></td>
<td><span data-ttu-id="fdfc6-159">Pågår</span><span class="sxs-lookup"><span data-stu-id="fdfc6-159">In progress</span></span></td>
<td><span data-ttu-id="fdfc6-160">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-160">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-161">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-161">No</span></span></td>
<td><span data-ttu-id="fdfc6-162">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-162">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-163">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-163">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-164">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-164">No</span></span></td>
<td><span data-ttu-id="fdfc6-165">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdfc6-166">Overføring</span><span class="sxs-lookup"><span data-stu-id="fdfc6-166">Transfer</span></span></td>
<td><span data-ttu-id="fdfc6-167">Fullført</span><span class="sxs-lookup"><span data-stu-id="fdfc6-167">Completed</span></span></td>
<td><span data-ttu-id="fdfc6-168">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-168">No</span></span></td>
<td><span data-ttu-id="fdfc6-169">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-169">No</span></span></td>
<td><span data-ttu-id="fdfc6-170">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-170">No</span></span></td>
<td><span data-ttu-id="fdfc6-171">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-171">No</span></span></td>
<td><span data-ttu-id="fdfc6-172">Ja</span><span class="sxs-lookup"><span data-stu-id="fdfc6-172">Yes</span></span></td>
<td><span data-ttu-id="fdfc6-173">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdfc6-174">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="fdfc6-174">Transfer or process</span></span></td>
<td><span data-ttu-id="fdfc6-175">Tom</span><span class="sxs-lookup"><span data-stu-id="fdfc6-175">Empty</span></span></td>
<td><span data-ttu-id="fdfc6-176">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-176">No</span></span></td>
<td><span data-ttu-id="fdfc6-177">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-177">No</span></span></td>
<td><span data-ttu-id="fdfc6-178">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-178">No</span></span></td>
<td><span data-ttu-id="fdfc6-179">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-179">No</span></span></td>
<td><span data-ttu-id="fdfc6-180">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-180">No</span></span></td>
<td><span data-ttu-id="fdfc6-181">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdfc6-182">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="fdfc6-182">Transfer or process</span></span></td>
<td><span data-ttu-id="fdfc6-183">Finner ikke et Kanban-kort</span><span class="sxs-lookup"><span data-stu-id="fdfc6-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="fdfc6-184">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-184">No</span></span></td>
<td><span data-ttu-id="fdfc6-185">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-185">No</span></span></td>
<td><span data-ttu-id="fdfc6-186">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-186">No</span></span></td>
<td><span data-ttu-id="fdfc6-187">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-187">No</span></span></td>
<td><span data-ttu-id="fdfc6-188">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-188">No</span></span></td>
<td><span data-ttu-id="fdfc6-189">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdfc6-190">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="fdfc6-190">Transfer or process</span></span></td>
<td><span data-ttu-id="fdfc6-191">Det er funnet et Kanban-kort, men det er ikke tilordnet til en Kanban</span><span class="sxs-lookup"><span data-stu-id="fdfc6-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="fdfc6-192">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-192">No</span></span></td>
<td><span data-ttu-id="fdfc6-193">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-193">No</span></span></td>
<td><span data-ttu-id="fdfc6-194">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-194">No</span></span></td>
<td><span data-ttu-id="fdfc6-195">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-195">No</span></span></td>
<td><span data-ttu-id="fdfc6-196">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-196">No</span></span></td>
<td><span data-ttu-id="fdfc6-197">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdfc6-198">Behandle</span><span class="sxs-lookup"><span data-stu-id="fdfc6-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="fdfc6-199">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="fdfc6-199">Not planned</span></span></li>
<li><span data-ttu-id="fdfc6-200">Klargjort</span><span class="sxs-lookup"><span data-stu-id="fdfc6-200">Prepared</span></span></li>
<li><span data-ttu-id="fdfc6-201">Pågår</span><span class="sxs-lookup"><span data-stu-id="fdfc6-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="fdfc6-202">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-202">No</span></span></td>
<td><span data-ttu-id="fdfc6-203">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-203">No</span></span></td>
<td><span data-ttu-id="fdfc6-204">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-204">No</span></span></td>
<td><span data-ttu-id="fdfc6-205">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-205">No</span></span></td>
<td><span data-ttu-id="fdfc6-206">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-206">No</span></span></td>
<td><span data-ttu-id="fdfc6-207">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdfc6-208">Behandle</span><span class="sxs-lookup"><span data-stu-id="fdfc6-208">Process</span></span></td>
<td><span data-ttu-id="fdfc6-209">Fullført</span><span class="sxs-lookup"><span data-stu-id="fdfc6-209">Completed</span></span></td>
<td><span data-ttu-id="fdfc6-210">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-210">No</span></span></td>
<td><span data-ttu-id="fdfc6-211">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-211">No</span></span></td>
<td><span data-ttu-id="fdfc6-212">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-212">No</span></span></td>
<td><span data-ttu-id="fdfc6-213">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-213">No</span></span></td>
<td><span data-ttu-id="fdfc6-214">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-214">No</span></span></td>
<td><span data-ttu-id="fdfc6-215">Antall</span><span class="sxs-lookup"><span data-stu-id="fdfc6-215">No</span></span></td>
</tr>
</tbody>
</table>





