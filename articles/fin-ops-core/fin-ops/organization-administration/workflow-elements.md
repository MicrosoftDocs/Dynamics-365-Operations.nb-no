---
title: Arbeidsflytelementer
description: Dette emnet beskriver de ulike elementene som utgjør en arbeidsflyt.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce4b0c3ee996dfbf0904f8e7fd3b3bfb53a149c2
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698053"
---
# <a name="workflow-elements"></a><span data-ttu-id="31b7e-103">Arbeidsflytelementer</span><span class="sxs-lookup"><span data-stu-id="31b7e-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31b7e-104">Dette emnet beskriver de ulike elementene som utgjør en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="31b7e-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="31b7e-105">En arbeidsflyt består av elementer.</span><span class="sxs-lookup"><span data-stu-id="31b7e-105">A workflow consists of elements.</span></span> <span data-ttu-id="31b7e-106">Delene nedenfor beskriver hver elementtype.</span><span class="sxs-lookup"><span data-stu-id="31b7e-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="31b7e-107">Oppgaver</span><span class="sxs-lookup"><span data-stu-id="31b7e-107">Tasks</span></span>

<span data-ttu-id="31b7e-108">En *oppgave* er en arbeidsenhet som må utføres.</span><span class="sxs-lookup"><span data-stu-id="31b7e-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="31b7e-109">To typer oppgaver kan legges til en arbeidsflyt: manuelle og automatiserte oppgaver.</span><span class="sxs-lookup"><span data-stu-id="31b7e-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="31b7e-110">Manuell oppgave</span><span class="sxs-lookup"><span data-stu-id="31b7e-110">Manual task</span></span>

<span data-ttu-id="31b7e-111">En *manuell oppgave* er en arbeidsenhet som må utføres av en bruker.</span><span class="sxs-lookup"><span data-stu-id="31b7e-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="31b7e-112">En arbeidsflyt for reiseregningsrapport kan for eksempel ha manuelle oppgaver som krever at den tilordnede brukeren utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="31b7e-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="31b7e-113">Se gjennom kvitteringene som sendes sammen med en reiseregning.</span><span class="sxs-lookup"><span data-stu-id="31b7e-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="31b7e-114">Ring en ansatts leder.</span><span class="sxs-lookup"><span data-stu-id="31b7e-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="31b7e-115">Automatisert oppgave</span><span class="sxs-lookup"><span data-stu-id="31b7e-115">Automated task</span></span>

<span data-ttu-id="31b7e-116">En *automatisert oppgave* er en arbeidsenhet som må utføres av systemet.</span><span class="sxs-lookup"><span data-stu-id="31b7e-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="31b7e-117">Ingen brukerhandling er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="31b7e-117">No human interaction is required.</span></span> <span data-ttu-id="31b7e-118">En arbeidsflyt for reiseregningsrapport kan for eksempel ha automatiserte oppgaver som krever at systemet utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="31b7e-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="31b7e-119">Utfør en kredittsjekk.</span><span class="sxs-lookup"><span data-stu-id="31b7e-119">Perform a credit check.</span></span>
- <span data-ttu-id="31b7e-120">Opprett en kundepost for kunden hvis en post ikke allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="31b7e-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="31b7e-121">Godkjenningsprosesser</span><span class="sxs-lookup"><span data-stu-id="31b7e-121">Approval processes</span></span>

<span data-ttu-id="31b7e-122">En *godkjenningsprosess* er en prosess som består av separate trinn.</span><span class="sxs-lookup"><span data-stu-id="31b7e-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="31b7e-123">I hvert godkjenningstrinn, kan brukeren utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="31b7e-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="31b7e-124">Godkjenne dokumentet</span><span class="sxs-lookup"><span data-stu-id="31b7e-124">Approve the document.</span></span>
- <span data-ttu-id="31b7e-125">Avvise dokumentet</span><span class="sxs-lookup"><span data-stu-id="31b7e-125">Reject the document.</span></span>
- <span data-ttu-id="31b7e-126">Be om en endring i dokumentet</span><span class="sxs-lookup"><span data-stu-id="31b7e-126">Request a change to the document.</span></span>
- <span data-ttu-id="31b7e-127">Tilordne dokumentet til en annen bruker for godkjenning</span><span class="sxs-lookup"><span data-stu-id="31b7e-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="31b7e-128">Elementer for arbeidsflyt for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="31b7e-128">Line-item workflow elements</span></span>

<span data-ttu-id="31b7e-129">Du kan opprette en arbeidsflyt for å behandle dokumenter eller linjeelementene på et dokument.</span><span class="sxs-lookup"><span data-stu-id="31b7e-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="31b7e-130">Du har for eksempel opprettet en godkjenningsarbeidsflyt for timeregistreringer.</span><span class="sxs-lookup"><span data-stu-id="31b7e-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="31b7e-131">(Vi refererer til denne arbeidsflyten som *dokumentarbeidsflyten*.) Du kan legge til et *arbeidsflyt for linjeelementer*-elementet som arbeidsflyten for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="31b7e-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="31b7e-132">Når linjeelementet kjøres, sendes hvert linjeelement for dokumentet til behandling.</span><span class="sxs-lookup"><span data-stu-id="31b7e-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="31b7e-133">Du vil kanskje at alle linjeelementene skal behandles av den samme arbeidsflyten for linjeelement, eller du vil kanskje at hvert linjeelement skal behandles av en annen arbeidsflyt for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="31b7e-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="31b7e-134">La oss si at en ansatt har sendt en timeregistrering som ligner den følgende illustrasjonen.</span><span class="sxs-lookup"><span data-stu-id="31b7e-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Arbeidsflyt med linjeelementer](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="31b7e-136">I dette scenariet vil du kanskje opprette følgende arbeidsflyter for linjeelementer:</span><span class="sxs-lookup"><span data-stu-id="31b7e-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="31b7e-137">**Arbeidsflyt for linjeelement 1** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 1111.</span><span class="sxs-lookup"><span data-stu-id="31b7e-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="31b7e-138">**Arbeidsflyt for linjeelement 2** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 2222.</span><span class="sxs-lookup"><span data-stu-id="31b7e-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="31b7e-139">**Arbeidsflyt for linjeelement 3** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 3333.</span><span class="sxs-lookup"><span data-stu-id="31b7e-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="31b7e-140">Flytkontrollelementer</span><span class="sxs-lookup"><span data-stu-id="31b7e-140">Flow-control elements</span></span>

<span data-ttu-id="31b7e-141">Følgende elementer lar deg utforme arbeidsflyter som har alternative grener eller grener som kjøres samtidig.</span><span class="sxs-lookup"><span data-stu-id="31b7e-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="31b7e-142">Manuell beslutning</span><span class="sxs-lookup"><span data-stu-id="31b7e-142">Manual decision</span></span>

<span data-ttu-id="31b7e-143">En *manuell beslutning* er et punkt der en arbeidsflyt deles opp i to grener.</span><span class="sxs-lookup"><span data-stu-id="31b7e-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="31b7e-144">En bruker må ta en beslutning, og denne beslutningen bestemmer hvilken gren som skal brukes til å behandle dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="31b7e-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="31b7e-145">Betinget beslutning</span><span class="sxs-lookup"><span data-stu-id="31b7e-145">Conditional decision</span></span>

<span data-ttu-id="31b7e-146">En *betinget beslutning* er også et punkt der en arbeidsflyt deles opp i to grener.</span><span class="sxs-lookup"><span data-stu-id="31b7e-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="31b7e-147">Imidlertid bestemmer systemet hvilken gren som skal brukes til å behandle dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="31b7e-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="31b7e-148">For å ta denne beslutningen evaluerer systemet dokumentet for å fastslå om det oppfyller angitte vilkår.</span><span class="sxs-lookup"><span data-stu-id="31b7e-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="31b7e-149">Parallell aktivitet</span><span class="sxs-lookup"><span data-stu-id="31b7e-149">Parallel activity</span></span>

<span data-ttu-id="31b7e-150">En *parallellaktivitet* er et arbeidsflytelement som omfatter to eller flere arbeidsflytgrener som kjøres samtidig.</span><span class="sxs-lookup"><span data-stu-id="31b7e-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="31b7e-151">Underarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="31b7e-151">Subworkflow</span></span>

<span data-ttu-id="31b7e-152">En *underarbeidsflyt* er en arbeidsflyt som kjøres i en annen arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="31b7e-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
