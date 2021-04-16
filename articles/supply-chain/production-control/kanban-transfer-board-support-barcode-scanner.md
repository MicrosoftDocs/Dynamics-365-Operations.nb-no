---
title: Støtte for Kanban-overføringskort for strekkodelesere
description: Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a7073fb5d77e2d11569e86b92433864371f0e1d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825873"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="d03ce-103">Støtte for Kanban-overføringskort for strekkodelesere</span><span class="sxs-lookup"><span data-stu-id="d03ce-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d03ce-104">Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.</span><span class="sxs-lookup"><span data-stu-id="d03ce-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="d03ce-105">Registreringsmoduser</span><span class="sxs-lookup"><span data-stu-id="d03ce-105">Registration modes</span></span>
------------------

<span data-ttu-id="d03ce-106">I hurtigfanen **Skanner - registrering** kan du velge registreringsmodus, som styrer handlingen når du skanner et Kanban-kortnummer eller skriver inn nummeret manuelt i feltet Kanban-kortnummer.</span><span class="sxs-lookup"><span data-stu-id="d03ce-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="d03ce-107">Angi registreringsmodus</span><span class="sxs-lookup"><span data-stu-id="d03ce-107">Set registration mode</span></span> | <span data-ttu-id="d03ce-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d03ce-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d03ce-109">Starte</span><span class="sxs-lookup"><span data-stu-id="d03ce-109">Start</span></span>                 | <span data-ttu-id="d03ce-110">Registrerer en Kanban-overføringsjobb som pågående.</span><span class="sxs-lookup"><span data-stu-id="d03ce-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="d03ce-111">Fullført</span><span class="sxs-lookup"><span data-stu-id="d03ce-111">Complete</span></span>              | <span data-ttu-id="d03ce-112">Registrerer en Kanban-overføringsjobb som fullført.</span><span class="sxs-lookup"><span data-stu-id="d03ce-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="d03ce-113">Tom</span><span class="sxs-lookup"><span data-stu-id="d03ce-113">Empty</span></span>                 | <span data-ttu-id="d03ce-114">Registrerer materialhåndteringsenheten som et Kanban-kort refererer til, som tomt.</span><span class="sxs-lookup"><span data-stu-id="d03ce-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="d03ce-115">Velg</span><span class="sxs-lookup"><span data-stu-id="d03ce-115">Select</span></span>                | <span data-ttu-id="d03ce-116">Registrerer et Kanban-kortnummer og velger den refererte jobben automatisk i Kanban-listen.</span><span class="sxs-lookup"><span data-stu-id="d03ce-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="d03ce-117">Registreringsmodusen Velg</span><span class="sxs-lookup"><span data-stu-id="d03ce-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="d03ce-118">Når du bruker en strekkodeleser til å velge en jobb, endres visningsmodusen for Kanban-kortet.</span><span class="sxs-lookup"><span data-stu-id="d03ce-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="d03ce-119">I denne modusen gjelder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="d03ce-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="d03ce-120">Bare den skannede Kanban-jobben vises.</span><span class="sxs-lookup"><span data-stu-id="d03ce-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="d03ce-121">Detaljene om den valgte jobben vises i hurtigfanen **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="d03ce-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="d03ce-122">**Meldinger**-hurtigfanen viser meldinger bare for den valgte jobben.</span><span class="sxs-lookup"><span data-stu-id="d03ce-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="d03ce-123">Du kan endre statusen på jobben ved hjelp av funksjonene som er tilgjengelige i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d03ce-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="d03ce-124">Kanban-overføringskortet fortsetter å vise bare én jobb i denne perioden.</span><span class="sxs-lookup"><span data-stu-id="d03ce-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="d03ce-125">Du kan oppdatere informasjonen i listen over jobber manuelt ved å klikke **Oppdater** (SKIFT+F5) i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d03ce-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="d03ce-126">Når du oppdaterer informasjonen, vises alle resultatene for jobbfilteret på nytt.</span><span class="sxs-lookup"><span data-stu-id="d03ce-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="d03ce-127">Jobbstatus og mulige handlinger</span><span class="sxs-lookup"><span data-stu-id="d03ce-127">Job status and possible actions</span></span>
<span data-ttu-id="d03ce-128">Statusen for den valgte jobben og statusen for tilknyttede jobber for hendelses-Kanbaner, bestemmer om du kan behandle jobben ytterligere.</span><span class="sxs-lookup"><span data-stu-id="d03ce-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="d03ce-129">Tabellen nedenfor viser informasjon om disse statusene og oppgavene:</span><span class="sxs-lookup"><span data-stu-id="d03ce-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="d03ce-130">Statusene som er tilgjengelige for jobber eller for håndteringsenhetene som jobbene refererer til.</span><span class="sxs-lookup"><span data-stu-id="d03ce-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="d03ce-131">Hver oppgave du kan utføre for jobben.</span><span class="sxs-lookup"><span data-stu-id="d03ce-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="d03ce-132">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="d03ce-132">Job type</span></span></th>
<th><span data-ttu-id="d03ce-133">Jobbstatusen eller statusen for håndteringsenheten</span><span class="sxs-lookup"><span data-stu-id="d03ce-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="d03ce-134">Oppdater plukkliste</span><span class="sxs-lookup"><span data-stu-id="d03ce-134">Update picking list</span></span></th>
<th><span data-ttu-id="d03ce-135">Starte</span><span class="sxs-lookup"><span data-stu-id="d03ce-135">Start</span></span></th>
<th><span data-ttu-id="d03ce-136">Oppdater registrering</span><span class="sxs-lookup"><span data-stu-id="d03ce-136">Update registration</span></span></th>
<th><span data-ttu-id="d03ce-137">Fullført</span><span class="sxs-lookup"><span data-stu-id="d03ce-137">Complete</span></span></th>
<th><span data-ttu-id="d03ce-138">Tom</span><span class="sxs-lookup"><span data-stu-id="d03ce-138">Empty</span></span></th>
<th><span data-ttu-id="d03ce-139">Opprett hendelses-Kanbaner</span><span class="sxs-lookup"><span data-stu-id="d03ce-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d03ce-140">Overføring</span><span class="sxs-lookup"><span data-stu-id="d03ce-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="d03ce-141">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="d03ce-141">Not planned</span></span></li>
<li><span data-ttu-id="d03ce-142">Ingen tilknyttede jobber, eller tilknyttede jobber er fullført</span><span class="sxs-lookup"><span data-stu-id="d03ce-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="d03ce-143">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-143">Yes</span></span></td>
<td><span data-ttu-id="d03ce-144">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-144">Yes</span></span></td>
<td><span data-ttu-id="d03ce-145">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-145">Yes</span></span></td>
<td><span data-ttu-id="d03ce-146">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-146">Yes</span></span></td>
<td><span data-ttu-id="d03ce-147">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-147">No</span></span></td>
<td><span data-ttu-id="d03ce-148">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03ce-149">Overføring</span><span class="sxs-lookup"><span data-stu-id="d03ce-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="d03ce-150">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="d03ce-150">Not planned</span></span></li>
<li><span data-ttu-id="d03ce-151">Den tilknyttede jobben er ikke fullført</span><span class="sxs-lookup"><span data-stu-id="d03ce-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="d03ce-152">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-152">Yes</span></span></td>
<td><span data-ttu-id="d03ce-153">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-153">No</span></span></td>
<td><span data-ttu-id="d03ce-154">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-154">Yes</span></span></td>
<td><span data-ttu-id="d03ce-155">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-155">No</span></span></td>
<td><span data-ttu-id="d03ce-156">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-156">No</span></span></td>
<td><span data-ttu-id="d03ce-157">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03ce-158">Overføring</span><span class="sxs-lookup"><span data-stu-id="d03ce-158">Transfer</span></span></td>
<td><span data-ttu-id="d03ce-159">Pågår</span><span class="sxs-lookup"><span data-stu-id="d03ce-159">In progress</span></span></td>
<td><span data-ttu-id="d03ce-160">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-160">Yes</span></span></td>
<td><span data-ttu-id="d03ce-161">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-161">No</span></span></td>
<td><span data-ttu-id="d03ce-162">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-162">Yes</span></span></td>
<td><span data-ttu-id="d03ce-163">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-163">Yes</span></span></td>
<td><span data-ttu-id="d03ce-164">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-164">No</span></span></td>
<td><span data-ttu-id="d03ce-165">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03ce-166">Overføring</span><span class="sxs-lookup"><span data-stu-id="d03ce-166">Transfer</span></span></td>
<td><span data-ttu-id="d03ce-167">Fullført</span><span class="sxs-lookup"><span data-stu-id="d03ce-167">Completed</span></span></td>
<td><span data-ttu-id="d03ce-168">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-168">No</span></span></td>
<td><span data-ttu-id="d03ce-169">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-169">No</span></span></td>
<td><span data-ttu-id="d03ce-170">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-170">No</span></span></td>
<td><span data-ttu-id="d03ce-171">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-171">No</span></span></td>
<td><span data-ttu-id="d03ce-172">Ja</span><span class="sxs-lookup"><span data-stu-id="d03ce-172">Yes</span></span></td>
<td><span data-ttu-id="d03ce-173">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03ce-174">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="d03ce-174">Transfer or process</span></span></td>
<td><span data-ttu-id="d03ce-175">Tom</span><span class="sxs-lookup"><span data-stu-id="d03ce-175">Empty</span></span></td>
<td><span data-ttu-id="d03ce-176">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-176">No</span></span></td>
<td><span data-ttu-id="d03ce-177">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-177">No</span></span></td>
<td><span data-ttu-id="d03ce-178">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-178">No</span></span></td>
<td><span data-ttu-id="d03ce-179">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-179">No</span></span></td>
<td><span data-ttu-id="d03ce-180">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-180">No</span></span></td>
<td><span data-ttu-id="d03ce-181">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03ce-182">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="d03ce-182">Transfer or process</span></span></td>
<td><span data-ttu-id="d03ce-183">Finner ikke et Kanban-kort</span><span class="sxs-lookup"><span data-stu-id="d03ce-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="d03ce-184">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-184">No</span></span></td>
<td><span data-ttu-id="d03ce-185">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-185">No</span></span></td>
<td><span data-ttu-id="d03ce-186">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-186">No</span></span></td>
<td><span data-ttu-id="d03ce-187">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-187">No</span></span></td>
<td><span data-ttu-id="d03ce-188">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-188">No</span></span></td>
<td><span data-ttu-id="d03ce-189">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03ce-190">Overføring eller behandling</span><span class="sxs-lookup"><span data-stu-id="d03ce-190">Transfer or process</span></span></td>
<td><span data-ttu-id="d03ce-191">Det er funnet et Kanban-kort, men det er ikke tilordnet til en Kanban</span><span class="sxs-lookup"><span data-stu-id="d03ce-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="d03ce-192">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-192">No</span></span></td>
<td><span data-ttu-id="d03ce-193">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-193">No</span></span></td>
<td><span data-ttu-id="d03ce-194">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-194">No</span></span></td>
<td><span data-ttu-id="d03ce-195">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-195">No</span></span></td>
<td><span data-ttu-id="d03ce-196">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-196">No</span></span></td>
<td><span data-ttu-id="d03ce-197">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03ce-198">Behandle</span><span class="sxs-lookup"><span data-stu-id="d03ce-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="d03ce-199">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="d03ce-199">Not planned</span></span></li>
<li><span data-ttu-id="d03ce-200">Klargjort</span><span class="sxs-lookup"><span data-stu-id="d03ce-200">Prepared</span></span></li>
<li><span data-ttu-id="d03ce-201">Pågår</span><span class="sxs-lookup"><span data-stu-id="d03ce-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="d03ce-202">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-202">No</span></span></td>
<td><span data-ttu-id="d03ce-203">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-203">No</span></span></td>
<td><span data-ttu-id="d03ce-204">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-204">No</span></span></td>
<td><span data-ttu-id="d03ce-205">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-205">No</span></span></td>
<td><span data-ttu-id="d03ce-206">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-206">No</span></span></td>
<td><span data-ttu-id="d03ce-207">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03ce-208">Behandle</span><span class="sxs-lookup"><span data-stu-id="d03ce-208">Process</span></span></td>
<td><span data-ttu-id="d03ce-209">Fullført</span><span class="sxs-lookup"><span data-stu-id="d03ce-209">Completed</span></span></td>
<td><span data-ttu-id="d03ce-210">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-210">No</span></span></td>
<td><span data-ttu-id="d03ce-211">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-211">No</span></span></td>
<td><span data-ttu-id="d03ce-212">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-212">No</span></span></td>
<td><span data-ttu-id="d03ce-213">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-213">No</span></span></td>
<td><span data-ttu-id="d03ce-214">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-214">No</span></span></td>
<td><span data-ttu-id="d03ce-215">Antall</span><span class="sxs-lookup"><span data-stu-id="d03ce-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]