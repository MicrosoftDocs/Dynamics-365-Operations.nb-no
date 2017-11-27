---
title: Arbeidsflythandlinger
description: "Denne artikkelen forklarer handlingene som hver deltaker i en godkjenningsprosess for arbeidsflyt kan utføre."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a4717accfa7e5879ee757820c39f000fa7d3e95
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-actions"></a><span data-ttu-id="615a8-103">Arbeidsflythandlinger</span><span class="sxs-lookup"><span data-stu-id="615a8-103">Workflow actions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="615a8-104">Denne artikkelen forklarer handlingene som hver deltaker i en godkjenningsprosess for arbeidsflyt kan utføre.</span><span class="sxs-lookup"><span data-stu-id="615a8-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="615a8-105">En arbeidsflyt kan omfatte flere grupper av personer: avsenderen, personer tilordnet oppgaver, beslutningstakere og godkjennere.</span><span class="sxs-lookup"><span data-stu-id="615a8-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="615a8-106">I følgende arbeidsflyt for reiseregning nedenfor er Erik avsenderen, medlemmer av køen er personer som er tilordnet oppgaven, Jon er beslutningstaker, og Dag, Jorunn og Karen er godkjennerne.</span><span class="sxs-lookup"><span data-stu-id="615a8-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>   

<span data-ttu-id="615a8-107">[![Arbeidsflyt\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="615a8-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span> 

<span data-ttu-id="615a8-108">De følgende avsnittene forklarer arbeidsflythandlingene hver gruppe kan utføre.</span><span class="sxs-lookup"><span data-stu-id="615a8-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="615a8-109">Handlinger en avsender kan utføre</span><span class="sxs-lookup"><span data-stu-id="615a8-109">Actions that an originator can perform</span></span>
<span data-ttu-id="615a8-110">Avsenderen starter en arbeidsflyt ved å sende et dokument til behandling.</span><span class="sxs-lookup"><span data-stu-id="615a8-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="615a8-111">For eksempel må Erik klikke **Send** -knappen på siden **Reiseregning** for å sende reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="615a8-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="615a8-112">Handlinger som en person tilordnet en oppgave, kan utføre</span><span class="sxs-lookup"><span data-stu-id="615a8-112">Actions that a task assignee can perform</span></span>
<span data-ttu-id="615a8-113">En oppgave kan tilordnes til flere personer eller til en arbeidselementkø som overvåkes av flere personer.</span><span class="sxs-lookup"><span data-stu-id="615a8-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="615a8-114">Men bare én person kan fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="615a8-114">However, only one person can complete a task.</span></span> <span data-ttu-id="615a8-115">For eksempel har Erik sendt en reiseregning, og har sendt sine kvitteringer til organisasjonens reiseregningsavdeling for gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="615a8-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span> 

<span data-ttu-id="615a8-116">Medlemmene av avdelingen Adventure Works-reiseregninger overvåker køen.</span><span class="sxs-lookup"><span data-stu-id="615a8-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="615a8-117">Julie, et medlem fra avdelingen, har godtatt oppgaven med å gå gjennom Eriks reiseregningen og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="615a8-118">Hun kan nå utføre én av følgende handlinger: fullføre, avvise, delegere, be om endring, tilordne eller frigi.</span><span class="sxs-lookup"><span data-stu-id="615a8-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span> 

<span data-ttu-id="615a8-119">**Obs!** Handlingene som er tilgjengelige, vil variere avhengig av hvordan programvareutvikleren utformet oppgaven.</span><span class="sxs-lookup"><span data-stu-id="615a8-119">**Note:** The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="615a8-120">Fullføre</span><span class="sxs-lookup"><span data-stu-id="615a8-120">Complete</span></span>

<span data-ttu-id="615a8-121">Når en bruker fullfører en oppgave, tilordnes dokumentet som ble sendt til behandling, til den neste brukeren i arbeidsflyten hvis det finnes en neste bruker.</span><span class="sxs-lookup"><span data-stu-id="615a8-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="615a8-122">Hvis det ikke kreves mer behandling, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-122">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="615a8-123">Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="615a8-124">Når Julie har fullført sin gjennomgang, tilordnes dokumentet Jon.</span><span class="sxs-lookup"><span data-stu-id="615a8-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="615a8-125">Avslå</span><span class="sxs-lookup"><span data-stu-id="615a8-125">Reject</span></span>

<span data-ttu-id="615a8-126">Når en bruker avviser et dokument, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-126">When a user rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="615a8-127">Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="615a8-128">Hvis Julie avviser reiseregningen, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-128">If Julie rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="615a8-129">Erik kan deretter sende reiseregningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="615a8-130">Han kan foreta endringer først, eller han kan sende originalversjonen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="615a8-131">Hvis Erik sender reiseregningen på nytt, starter arbeidsflytprosessen fra den manuelle gjennomgangsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="615a8-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="615a8-132">Representant</span><span class="sxs-lookup"><span data-stu-id="615a8-132">Delegate</span></span>

<span data-ttu-id="615a8-133">Når en bruker delegerer en oppgave, tilordnes den til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="615a8-133">When a user delegates a task, the task is assigned to another user.</span></span> 

<span data-ttu-id="615a8-134">Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="615a8-135">Julie delegerer oppgaven til Tim, som er hennes assistent.</span><span class="sxs-lookup"><span data-stu-id="615a8-135">Julie delegates this task to Tim, who is her assistant.</span></span> 

<span data-ttu-id="615a8-136">Tim opptrer deretter på vegne av Julie.</span><span class="sxs-lookup"><span data-stu-id="615a8-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="615a8-137">Derfor, når Tim fullfører sin gjennomgang, tilordnes reiseregningen til Jon, akkurat som om Julie hadde fullført oppgaven.</span><span class="sxs-lookup"><span data-stu-id="615a8-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="615a8-138">Be om endring</span><span class="sxs-lookup"><span data-stu-id="615a8-138">Request change</span></span>

<span data-ttu-id="615a8-139">Når en bruker ber om en endring i et dokument som ble sendt, sendes det tilbake til avsenderen.</span><span class="sxs-lookup"><span data-stu-id="615a8-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span> 

<span data-ttu-id="615a8-140">Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="615a8-141">Julie legger merke til noen feil i reiseregningen og ber om endringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="615a8-142">Reiseregningen sendes tilbake til Erik.</span><span class="sxs-lookup"><span data-stu-id="615a8-142">The expense report is sent back to Sam.</span></span> 

<span data-ttu-id="615a8-143">Erik kan deretter sende reiseregningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="615a8-144">Han kan foreta de forespurte endringene først, eller han kan sende originalversjonen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="615a8-145">Hvis Erik sender reiseregningen på nytt, må et medlem av arbeidselementkøen kontrollere reiseregningen og kvitteringene på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="615a8-146">Tilordne på nytt</span><span class="sxs-lookup"><span data-stu-id="615a8-146">Reassign</span></span>

<span data-ttu-id="615a8-147">Medlemmene av en arbeidselementkø kan tilordne dokumenter som er i køen, på nytt til en annen kø.</span><span class="sxs-lookup"><span data-stu-id="615a8-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span> 

<span data-ttu-id="615a8-148">For eksempel overvåker Julie, som er medlem av avdelingen Adventure Works-reiseregninger, køen.</span><span class="sxs-lookup"><span data-stu-id="615a8-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="615a8-149">For å balansere arbeidsmengden hun kan tilordne reiseregningen på nytt, og kvitteringene som er inkludert i den, til en annen kø.</span><span class="sxs-lookup"><span data-stu-id="615a8-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="615a8-150">Frigi</span><span class="sxs-lookup"><span data-stu-id="615a8-150">Release</span></span>

<span data-ttu-id="615a8-151">Et medlem av en arbeidselementkø kan noen ganger godta en aktivitet, men deretter bestemmer deg for at han eller hun ikke kan fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="615a8-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="615a8-152">I så fall kan personen som godtok oppgaven, frigi dokumentet tilbake til arbeidselementkøen.</span><span class="sxs-lookup"><span data-stu-id="615a8-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span> 

<span data-ttu-id="615a8-153">Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="615a8-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="615a8-154">Hvis Julie bestemmer seg for at hun ikke kan fullføre oppgaven, kan hun frigi dokumentet.</span><span class="sxs-lookup"><span data-stu-id="615a8-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="615a8-155">Reiseregningen returneres til køen slik at andre medlemmer av avdelingen Adventure Works-reiseregninger kan fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="615a8-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="615a8-156">Handlinger som en beslutningstaker kan utføre</span><span class="sxs-lookup"><span data-stu-id="615a8-156">Actions that a decision maker can perform</span></span>
<span data-ttu-id="615a8-157">Vanligvis tilordnes et dokument til en beslutningstaker fordi det er et spørsmål som må besvares av beslutningstaker.</span><span class="sxs-lookup"><span data-stu-id="615a8-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="615a8-158">Svaret på spørsmålet er vanligvis **Ja** eller **Nei** eller **Sann** eller **Usann**.</span><span class="sxs-lookup"><span data-stu-id="615a8-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="615a8-159">Hvis beslutningstakeren ikke velger et av disse valgene, kan han eller hun delegere beslutningen.</span><span class="sxs-lookup"><span data-stu-id="615a8-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="615a8-160">\[Valg 1\] eller \[Valg 2\]</span><span class="sxs-lookup"><span data-stu-id="615a8-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="615a8-161">En beslutningstaker må svare på spørsmål som er knyttet til dokumentet.</span><span class="sxs-lookup"><span data-stu-id="615a8-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="615a8-162">Svaret på spørsmålet er vanligvis **Ja** eller **Nei** eller **Sann** eller **Usann**.</span><span class="sxs-lookup"><span data-stu-id="615a8-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="615a8-163">Svaret som en beslutningstaker velger, bestemmer arbeidsflytgrenen som brukes til å behandle dokumentet.</span><span class="sxs-lookup"><span data-stu-id="615a8-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span> 

<span data-ttu-id="615a8-164">Eksempelvis tilordnes Eriks reiseregningen til Jon.</span><span class="sxs-lookup"><span data-stu-id="615a8-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="615a8-165">Jon må bestemme om informasjonen i dokumentet krever et kall til Eriks sjef.</span><span class="sxs-lookup"><span data-stu-id="615a8-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="615a8-166">Hvis Jon bestemmer seg for at det kreves en samtale, tilordnes reiseregningen til Anita, som deretter må ringe Eriks sjef.</span><span class="sxs-lookup"><span data-stu-id="615a8-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="615a8-167">Hvis Jon bestemmer seg for at en samtale ikke er nødvendig, tilordnes reiseregningen til Dag for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="615a8-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="615a8-168">Representant</span><span class="sxs-lookup"><span data-stu-id="615a8-168">Delegate</span></span>

<span data-ttu-id="615a8-169">Når en beslutningstaker delegerer en avgjørelse, tilordnes dokumentet til en annen bruker som må ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="615a8-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span> 

<span data-ttu-id="615a8-170">Eksempelvis tilordnes Eriks reiseregningen til Jon.</span><span class="sxs-lookup"><span data-stu-id="615a8-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="615a8-171">Jon delegerer beslutningen til Maria, som er hans assistent.</span><span class="sxs-lookup"><span data-stu-id="615a8-171">John delegates the decision to Maria, who is his assistant.</span></span> 

<span data-ttu-id="615a8-172">Maria opptrer deretter på vegne av Jon.</span><span class="sxs-lookup"><span data-stu-id="615a8-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="615a8-173">Hvis Maria bestemmer seg for å ringe Sams sjef, tilordnes reiseregningen til Anita, som deretter må ringe Eriks sjef.</span><span class="sxs-lookup"><span data-stu-id="615a8-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="615a8-174">Hvis Maria bestemmer seg for at en samtale ikke er nødvendig, tilordnes reiseregningen til Dag for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="615a8-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="615a8-175">Handlinger en godkjenner kan utføre</span><span class="sxs-lookup"><span data-stu-id="615a8-175">Actions that an approver can perform</span></span>
<span data-ttu-id="615a8-176">Når et dokument tilordnes en godkjenner, kan han eller hun utføre én av følgende handlinger: godkjenne, avvise, delegere eller be om endring.</span><span class="sxs-lookup"><span data-stu-id="615a8-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="615a8-177">Godkjenne</span><span class="sxs-lookup"><span data-stu-id="615a8-177">Approve</span></span>

<span data-ttu-id="615a8-178">Når en godkjenner godkjenner et dokument, tilordnes dokumentert den neste brukeren i arbeidsflyten, hvis det er en neste bruker.</span><span class="sxs-lookup"><span data-stu-id="615a8-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="615a8-179">Hvis det ikke kreves mer behandling, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-179">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="615a8-180">For eksempel har Erik sendt en reiseregning på NOK 6 000, og dette dokumentet er tilordnet Dag.</span><span class="sxs-lookup"><span data-stu-id="615a8-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="615a8-181">Når Dag godkjenner dokumentet, tilordnes det til Jorunn for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="615a8-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="615a8-182">Når Jorunn har godkjent reiseregningen, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="615a8-183">Avslå</span><span class="sxs-lookup"><span data-stu-id="615a8-183">Reject</span></span>

<span data-ttu-id="615a8-184">Når en godkjenner avviser et dokument, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-184">When an approver rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="615a8-185">For eksempel har Erik sendt en reiseregning på NOK 12 000, og dette dokumentet er tilordnet Jorunn.</span><span class="sxs-lookup"><span data-stu-id="615a8-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="615a8-186">Hvis Jorunn avviser reiseregningsrapporten, avsluttes arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-186">If Sue rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="615a8-187">Erik kan deretter sende reiseregningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="615a8-188">Han kan foreta endringer først, eller han kan sende originalversjonen av reiseregningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="615a8-189">Hvis Erik sender reiseregningen på nytt, starter arbeidsflytprosessen fra godkjenningprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="615a8-190">Representant</span><span class="sxs-lookup"><span data-stu-id="615a8-190">Delegate</span></span>

<span data-ttu-id="615a8-191">Når en godkjenner delegerer et dokument, tilordnes det til en annen bruker for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="615a8-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span> 

<span data-ttu-id="615a8-192">For eksempel har Erik sendt en reiseregning på NOK 12 000, og dette dokumentet er tilordnet Dag.</span><span class="sxs-lookup"><span data-stu-id="615a8-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="615a8-193">Dag delegerer reiseregningsrapporten til Karen.</span><span class="sxs-lookup"><span data-stu-id="615a8-193">Frank delegates the expense report to Ann.</span></span> 

<span data-ttu-id="615a8-194">Karen fungerer deretter på vegne av Dag.</span><span class="sxs-lookup"><span data-stu-id="615a8-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="615a8-195">Dette betyr at når Karen godkjenner dokumentet, tilordnes det til Jorunn for godkjenning, som om Dag hadde godkjent det.</span><span class="sxs-lookup"><span data-stu-id="615a8-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="615a8-196">Når Jorunn har godkjent dokumentet, sendes det til Karen for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="615a8-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="615a8-197">Be om endring</span><span class="sxs-lookup"><span data-stu-id="615a8-197">Request change</span></span>

<span data-ttu-id="615a8-198">Når en godkjenner ber om en endring i et dokument, sendes det tilbake til avsenderen.</span><span class="sxs-lookup"><span data-stu-id="615a8-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span> 

<span data-ttu-id="615a8-199">For eksempel har Erik sendt en reiseregning på NOK 12 000, og dette dokumentet er tilordnet Jorunn.</span><span class="sxs-lookup"><span data-stu-id="615a8-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="615a8-200">Hvis Jorunn ber om en endring, sendes reiseregningsrapporten tilbake til Erik.</span><span class="sxs-lookup"><span data-stu-id="615a8-200">If Sue requests a change, the expense report is sent back to Sam.</span></span> 

<span data-ttu-id="615a8-201">Erik kan deretter sende reiseregningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="615a8-202">Han kan foreta de forespurte endringer først, eller han kan sende originalversjonen av reiseregningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="615a8-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="615a8-203">Hvis Erik sender reiseregningsrapporten på nytt, sendes den til Dag for godkjenning, fordi han er den første godkjenneren i godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="615a8-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>




