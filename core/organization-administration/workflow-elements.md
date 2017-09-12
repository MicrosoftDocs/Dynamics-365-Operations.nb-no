---
title: Arbeidsflytelementer
description: "Denne artikkelen beskriver de ulike elementene som utgjør en arbeidsflyt."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5620a91ff9f300bed782170307a295ab79fc5b2e
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="c1c93-103">Arbeidsflytelementer</span><span class="sxs-lookup"><span data-stu-id="c1c93-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c1c93-104">Denne artikkelen beskriver de ulike elementene som utgjør en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="c1c93-104">This article describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="c1c93-105">En arbeidsflyt består av elementer.</span><span class="sxs-lookup"><span data-stu-id="c1c93-105">A workflow consists of elements.</span></span> <span data-ttu-id="c1c93-106">Delene nedenfor beskriver hver elementtype.</span><span class="sxs-lookup"><span data-stu-id="c1c93-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="c1c93-107">Oppgaver</span><span class="sxs-lookup"><span data-stu-id="c1c93-107">Tasks</span></span>
<span data-ttu-id="c1c93-108">En *oppgave* er en arbeidsenhet som må utføres.</span><span class="sxs-lookup"><span data-stu-id="c1c93-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="c1c93-109">To typer oppgaver kan legges til en arbeidsflyt: manuelle og automatiserte oppgaver.</span><span class="sxs-lookup"><span data-stu-id="c1c93-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="c1c93-110">Manuell oppgave</span><span class="sxs-lookup"><span data-stu-id="c1c93-110">Manual task</span></span>

<span data-ttu-id="c1c93-111">En *manuell oppgave* er en arbeidsenhet som må utføres av en bruker.</span><span class="sxs-lookup"><span data-stu-id="c1c93-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="c1c93-112">En arbeidsflyt for reiseregningsrapport kan for eksempel ha manuelle oppgaver som krever at den tilordnede brukeren utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="c1c93-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="c1c93-113">Se gjennom kvitteringene som sendes sammen med en reiseregning.</span><span class="sxs-lookup"><span data-stu-id="c1c93-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="c1c93-114">Ring en ansatts leder.</span><span class="sxs-lookup"><span data-stu-id="c1c93-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="c1c93-115">Automatisert oppgave</span><span class="sxs-lookup"><span data-stu-id="c1c93-115">Automated task</span></span>

<span data-ttu-id="c1c93-116">En *automatisert oppgave* er en arbeidsenhet som må utføres av systemet.</span><span class="sxs-lookup"><span data-stu-id="c1c93-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="c1c93-117">Ingen brukerhandling er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="c1c93-117">No human interaction is required.</span></span> <span data-ttu-id="c1c93-118">En arbeidsflyt for reiseregningsrapport kan for eksempel ha automatiserte oppgaver som krever at systemet utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="c1c93-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="c1c93-119">Utfør en kredittsjekk.</span><span class="sxs-lookup"><span data-stu-id="c1c93-119">Perform a credit check.</span></span>
-   <span data-ttu-id="c1c93-120">Opprett en kundepost for kunden hvis en post ikke allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="c1c93-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="c1c93-121">Godkjenningsprosesser</span><span class="sxs-lookup"><span data-stu-id="c1c93-121">Approval processes</span></span>
<span data-ttu-id="c1c93-122">En *godkjenningsprosess* er en prosess som består av separate trinn.</span><span class="sxs-lookup"><span data-stu-id="c1c93-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="c1c93-123">I hvert godkjenningstrinn, kan brukeren utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="c1c93-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="c1c93-124">Godkjenne dokumentet</span><span class="sxs-lookup"><span data-stu-id="c1c93-124">Approve the document.</span></span>
-   <span data-ttu-id="c1c93-125">Avvise dokumentet</span><span class="sxs-lookup"><span data-stu-id="c1c93-125">Reject the document.</span></span>
-   <span data-ttu-id="c1c93-126">Be om en endring i dokumentet</span><span class="sxs-lookup"><span data-stu-id="c1c93-126">Request a change to the document.</span></span>
-   <span data-ttu-id="c1c93-127">Tilordne dokumentet til en annen bruker for godkjenning</span><span class="sxs-lookup"><span data-stu-id="c1c93-127">Assign the document to another user for approval.</span></span>

## <a name="lineitem-workflow-elements"></a><span data-ttu-id="c1c93-128">Elementer for arbeidsflyt for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="c1c93-128">Lineitem workflow elements</span></span>
<span data-ttu-id="c1c93-129">Du kan opprette en arbeidsflyt for å behandle dokumenter eller linjeelementene på et dokument.</span><span class="sxs-lookup"><span data-stu-id="c1c93-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="c1c93-130">Du har for eksempel opprettet en godkjenningsarbeidsflyt for timeregistreringer.</span><span class="sxs-lookup"><span data-stu-id="c1c93-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="c1c93-131">(Vi refererer til denne arbeidsflyten som *dokumentarbeidsflyten*.) Du kan legge til et *arbeidsflyt for linjeelementer*-elementet som arbeidsflyten for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="c1c93-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="c1c93-132">Når linjeelementet kjøres, sendes hvert linjeelement for dokumentet til behandling.</span><span class="sxs-lookup"><span data-stu-id="c1c93-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="c1c93-133">Du vil kanskje at alle linjeelementene skal behandles av den samme arbeidsflyten for linjeelement, eller du vil kanskje at hvert linjeelement skal behandles av en annen arbeidsflyt for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="c1c93-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="c1c93-134">La oss si at en ansatt har sendt en timeregistrering som ligner den følgende illustrasjonen.</span><span class="sxs-lookup"><span data-stu-id="c1c93-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span> <span data-ttu-id="c1c93-135">![Arbeidsflyt med linjeelementer](./media/workflow_lineitemworkflow.gif) I dette scenariet kan det hende at du vil opprette følgende arbeidsflyter for linjeelement:</span><span class="sxs-lookup"><span data-stu-id="c1c93-135">![Workflow with line items](./media/workflow_lineitemworkflow.gif) In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="c1c93-136">**Arbeidsflyt for linjeelement 1** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 1111.</span><span class="sxs-lookup"><span data-stu-id="c1c93-136">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="c1c93-137">**Arbeidsflyt for linjeelement 2** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 2222.</span><span class="sxs-lookup"><span data-stu-id="c1c93-137">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="c1c93-138">**Arbeidsflyt for linjeelement 3** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 3333.</span><span class="sxs-lookup"><span data-stu-id="c1c93-138">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flowcontrol-elements"></a><span data-ttu-id="c1c93-139">Flytkontrollelementer</span><span class="sxs-lookup"><span data-stu-id="c1c93-139">Flowcontrol elements</span></span>
<span data-ttu-id="c1c93-140">Følgende elementer lar deg utforme arbeidsflyter som har alternative grener eller grener som kjøres samtidig.</span><span class="sxs-lookup"><span data-stu-id="c1c93-140">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="c1c93-141">Manuell beslutning</span><span class="sxs-lookup"><span data-stu-id="c1c93-141">Manual decision</span></span>

<span data-ttu-id="c1c93-142">En *manuell beslutning* er et punkt der en arbeidsflyt deles opp i to grener.</span><span class="sxs-lookup"><span data-stu-id="c1c93-142">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="c1c93-143">En bruker må ta en beslutning, og denne beslutningen bestemmer hvilken gren som skal brukes til å behandle dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="c1c93-143">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="c1c93-144">Betinget beslutning</span><span class="sxs-lookup"><span data-stu-id="c1c93-144">Conditional decision</span></span>

<span data-ttu-id="c1c93-145">En *betinget beslutning* er også et punkt der en arbeidsflyt deles opp i to grener.</span><span class="sxs-lookup"><span data-stu-id="c1c93-145">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="c1c93-146">Imidlertid bestemmer systemet hvilken gren som skal brukes til å behandle dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="c1c93-146">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="c1c93-147">For å ta denne beslutningen evaluerer systemet dokumentet for å fastslå om det oppfyller angitte vilkår.</span><span class="sxs-lookup"><span data-stu-id="c1c93-147">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="c1c93-148">Parallell aktivitet</span><span class="sxs-lookup"><span data-stu-id="c1c93-148">Parallel activity</span></span>

<span data-ttu-id="c1c93-149">En *parallellaktivitet* er et arbeidsflytelement som omfatter to eller flere arbeidsflytgrener som kjøres samtidig.</span><span class="sxs-lookup"><span data-stu-id="c1c93-149">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="c1c93-150">Underarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="c1c93-150">Subworkflow</span></span>

<span data-ttu-id="c1c93-151">En *underarbeidsflyt* er en arbeidsflyt som kjøres i en annen arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="c1c93-151">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




