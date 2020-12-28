---
title: Støtte for Kanban-overføringskort for strekkodelesere
description: Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bd6f1bdd847f74cee7d3594d19b72454063c0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434635"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="6b7f9-103">Støtte for Kanban-overføringskort for strekkodelesere</span><span class="sxs-lookup"><span data-stu-id="6b7f9-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b7f9-104">Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="6b7f9-105">Registreringsmoduser</span><span class="sxs-lookup"><span data-stu-id="6b7f9-105">Registration modes</span></span>
------------------

<span data-ttu-id="6b7f9-106">I hurtigkategorien **Skanner - registrering** kan du velge registreringsmodus, som styrer handlingen når du skanner et Kanban-kortnummer eller skriver inn nummeret manuelt i feltet Kanban-kortnummer.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="6b7f9-107">Angi registreringsmodus</span><span class="sxs-lookup"><span data-stu-id="6b7f9-107">Set registration mode</span></span> | <span data-ttu-id="6b7f9-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6b7f9-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7f9-109">Starte</span><span class="sxs-lookup"><span data-stu-id="6b7f9-109">Start</span></span>                 | <span data-ttu-id="6b7f9-110">Registrerer en Kanban-overføringsjobb som pågående.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="6b7f9-111">Fullført</span><span class="sxs-lookup"><span data-stu-id="6b7f9-111">Complete</span></span>              | <span data-ttu-id="6b7f9-112">Registrerer en Kanban-overføringsjobb som fullført.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="6b7f9-113">Tom</span><span class="sxs-lookup"><span data-stu-id="6b7f9-113">Empty</span></span>                 | <span data-ttu-id="6b7f9-114">Registrerer materialhåndteringsenheten som et Kanban-kort refererer til, som tomt.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="6b7f9-115">Velg</span><span class="sxs-lookup"><span data-stu-id="6b7f9-115">Select</span></span>                | <span data-ttu-id="6b7f9-116">Registrerer et Kanban-kortnummer og velger den refererte jobben automatisk i Kanban-listen.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="6b7f9-117">Registreringsmodusen Velg</span><span class="sxs-lookup"><span data-stu-id="6b7f9-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="6b7f9-118">Når du bruker en strekkodeleser til å velge en jobb, endres visningsmodusen for Kanban-kortet.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="6b7f9-119"> I denne modusen gjelder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="6b7f9-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="6b7f9-120">Bare den skannede Kanban-jobben vises.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="6b7f9-121">Detaljene om den valgte jobben vises i hurtigkategorien **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="6b7f9-122">**Meldinger**-hurtigkategorien viser meldinger bare for den valgte jobben.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="6b7f9-123">Du kan endre statusen på jobben ved hjelp av funksjonene som er tilgjengelige i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="6b7f9-124">Kanban-overføringskortet fortsetter å vise bare én jobb i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="6b7f9-125">Du kan oppdatere informasjonen i listen over jobber manuelt ved å klikke **Oppdater** (SKIFT+F5) i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="6b7f9-126">Når du oppdaterer informasjonen, vises alle resultatene for jobbfilteret på nytt.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="6b7f9-127">Jobbstatus og mulige handlinger</span><span class="sxs-lookup"><span data-stu-id="6b7f9-127">Job status and possible actions</span></span>
<span data-ttu-id="6b7f9-128">Statusen for den valgte jobben og statusen for tilknyttede jobber for hendelses-Kanbaner, bestemmer om du kan behandle jobben ytterligere.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="6b7f9-129">Tabellen nedenfor viser informasjon om disse statusene og oppgavene:</span><span class="sxs-lookup"><span data-stu-id="6b7f9-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="6b7f9-130">Statusene som er tilgjengelige for jobber eller for håndteringsenhetene som jobbene refererer til.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="6b7f9-131">Hver oppgave du kan utføre for jobben.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="6b7f9-132">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="6b7f9-132">Job type</span></span></th>
<th><span data-ttu-id="6b7f9-133">Jobbstatusen eller statusen for håndteringsenheten</span><span class="sxs-lookup"><span data-stu-id="6b7f9-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="6b7f9-134">Oppdater plukkliste</span><span class="sxs-lookup"><span data-stu-id="6b7f9-134">Update picking list</span></span></th>
<th><span data-ttu-id="6b7f9-135">Starte</span><span class="sxs-lookup"><span data-stu-id="6b7f9-135">Start</span></span></th>
<th><span data-ttu-id="6b7f9-136">Oppdater registrering</span><span class="sxs-lookup"><span data-stu-id="6b7f9-136">Update registration</span></span></th>
<th><span data-ttu-id="6b7f9-137">Fullført</span><span class="sxs-lookup"><span data-stu-id="6b7f9-137">Complete</span></span></th>
<th><span data-ttu-id="6b7f9-138">Tom</span><span class="sxs-lookup"><span data-stu-id="6b7f9-138">Empty</span></span></th>
<th><span data-ttu-id="6b7f9-139">Opprett hendelses-Kanbaner</span><span class="sxs-lookup"><span data-stu-id="6b7f9-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b7f9-140">Overføring</span><span class="sxs-lookup"><span data-stu-id="6b7f9-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="6b7f9-141">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="6b7f9-141">Not planned</span></span></li>
<li><span data-ttu-id="6b7f9-142">Ingen tilknyttede jobber, eller tilknyttede jobber er fullført</span><span class="sxs-lookup"><span data-stu-id="6b7f9-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="6b7f9-143">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-143">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-144">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-144">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-145">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-145">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-146">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-146">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-147">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-147">No</span></span></td>
<td><span data-ttu-id="6b7f9-148">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b7f9-149">Overføring</span><span class="sxs-lookup"><span data-stu-id="6b7f9-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="6b7f9-150">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="6b7f9-150">Not planned</span></span></li>
<li><span data-ttu-id="6b7f9-151">Den tilknyttede jobben er ikke fullført</span><span class="sxs-lookup"><span data-stu-id="6b7f9-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="6b7f9-152">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-152">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-153">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-153">No</span></span></td>
<td><span data-ttu-id="6b7f9-154">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-154">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-155">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-155">No</span></span></td>
<td><span data-ttu-id="6b7f9-156">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-156">No</span></span></td>
<td><span data-ttu-id="6b7f9-157">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b7f9-158">Overføring</span><span class="sxs-lookup"><span data-stu-id="6b7f9-158">Transfer</span></span></td>
<td><span data-ttu-id="6b7f9-159">Pågår</span><span class="sxs-lookup"><span data-stu-id="6b7f9-159">In progress</span></span></td>
<td><span data-ttu-id="6b7f9-160">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-160">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-161">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-161">No</span></span></td>
<td><span data-ttu-id="6b7f9-162">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-162">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-163">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-163">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-164">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-164">No</span></span></td>
<td><span data-ttu-id="6b7f9-165">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b7f9-166">Overføring</span><span class="sxs-lookup"><span data-stu-id="6b7f9-166">Transfer</span></span></td>
<td><span data-ttu-id="6b7f9-167">Fullført</span><span class="sxs-lookup"><span data-stu-id="6b7f9-167">Completed</span></span></td>
<td><span data-ttu-id="6b7f9-168">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-168">No</span></span></td>
<td><span data-ttu-id="6b7f9-169">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-169">No</span></span></td>
<td><span data-ttu-id="6b7f9-170">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-170">No</span></span></td>
<td><span data-ttu-id="6b7f9-171">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-171">No</span></span></td>
<td><span data-ttu-id="6b7f9-172">Ja</span><span class="sxs-lookup"><span data-stu-id="6b7f9-172">Yes</span></span></td>
<td><span data-ttu-id="6b7f9-173">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b7f9-174">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="6b7f9-174">Transfer or process</span></span></td>
<td><span data-ttu-id="6b7f9-175">Tom</span><span class="sxs-lookup"><span data-stu-id="6b7f9-175">Empty</span></span></td>
<td><span data-ttu-id="6b7f9-176">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-176">No</span></span></td>
<td><span data-ttu-id="6b7f9-177">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-177">No</span></span></td>
<td><span data-ttu-id="6b7f9-178">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-178">No</span></span></td>
<td><span data-ttu-id="6b7f9-179">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-179">No</span></span></td>
<td><span data-ttu-id="6b7f9-180">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-180">No</span></span></td>
<td><span data-ttu-id="6b7f9-181">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b7f9-182">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="6b7f9-182">Transfer or process</span></span></td>
<td><span data-ttu-id="6b7f9-183">Finner ikke et Kanban-kort</span><span class="sxs-lookup"><span data-stu-id="6b7f9-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="6b7f9-184">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-184">No</span></span></td>
<td><span data-ttu-id="6b7f9-185">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-185">No</span></span></td>
<td><span data-ttu-id="6b7f9-186">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-186">No</span></span></td>
<td><span data-ttu-id="6b7f9-187">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-187">No</span></span></td>
<td><span data-ttu-id="6b7f9-188">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-188">No</span></span></td>
<td><span data-ttu-id="6b7f9-189">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b7f9-190">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="6b7f9-190">Transfer or process</span></span></td>
<td><span data-ttu-id="6b7f9-191">Det er funnet et Kanban-kort, men det er ikke tilordnet til en Kanban</span><span class="sxs-lookup"><span data-stu-id="6b7f9-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="6b7f9-192">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-192">No</span></span></td>
<td><span data-ttu-id="6b7f9-193">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-193">No</span></span></td>
<td><span data-ttu-id="6b7f9-194">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-194">No</span></span></td>
<td><span data-ttu-id="6b7f9-195">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-195">No</span></span></td>
<td><span data-ttu-id="6b7f9-196">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-196">No</span></span></td>
<td><span data-ttu-id="6b7f9-197">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b7f9-198">Behandle</span><span class="sxs-lookup"><span data-stu-id="6b7f9-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="6b7f9-199">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="6b7f9-199">Not planned</span></span></li>
<li><span data-ttu-id="6b7f9-200">Klargjort</span><span class="sxs-lookup"><span data-stu-id="6b7f9-200">Prepared</span></span></li>
<li><span data-ttu-id="6b7f9-201">Pågår</span><span class="sxs-lookup"><span data-stu-id="6b7f9-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="6b7f9-202">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-202">No</span></span></td>
<td><span data-ttu-id="6b7f9-203">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-203">No</span></span></td>
<td><span data-ttu-id="6b7f9-204">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-204">No</span></span></td>
<td><span data-ttu-id="6b7f9-205">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-205">No</span></span></td>
<td><span data-ttu-id="6b7f9-206">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-206">No</span></span></td>
<td><span data-ttu-id="6b7f9-207">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b7f9-208">Behandle</span><span class="sxs-lookup"><span data-stu-id="6b7f9-208">Process</span></span></td>
<td><span data-ttu-id="6b7f9-209">Fullført</span><span class="sxs-lookup"><span data-stu-id="6b7f9-209">Completed</span></span></td>
<td><span data-ttu-id="6b7f9-210">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-210">No</span></span></td>
<td><span data-ttu-id="6b7f9-211">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-211">No</span></span></td>
<td><span data-ttu-id="6b7f9-212">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-212">No</span></span></td>
<td><span data-ttu-id="6b7f9-213">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-213">No</span></span></td>
<td><span data-ttu-id="6b7f9-214">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-214">No</span></span></td>
<td><span data-ttu-id="6b7f9-215">Antall</span><span class="sxs-lookup"><span data-stu-id="6b7f9-215">No</span></span></td>
</tr>
</tbody>
</table>





