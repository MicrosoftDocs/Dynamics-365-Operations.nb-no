---
title: Oversikt over arbeidsflytsystem
description: Dette emnet beskriver arbeidsflytsystemet.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbcab469e1dc8c139d180abdb7ed0bd8fba488a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747741"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="af06b-103">Oversikt over arbeidsflytsystem</span><span class="sxs-lookup"><span data-stu-id="af06b-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af06b-104">Dette emnet beskriver arbeidsflytsystemet.</span><span class="sxs-lookup"><span data-stu-id="af06b-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="af06b-105">Hva er arbeidsflyt?</span><span class="sxs-lookup"><span data-stu-id="af06b-105">What is workflow?</span></span>

<span data-ttu-id="af06b-106">Begrepet *arbeidsflyt* kan defineres på to måter: som et system og en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="af06b-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="af06b-107">Workflow er et system</span><span class="sxs-lookup"><span data-stu-id="af06b-107">Workflow is a system</span></span>

<span data-ttu-id="af06b-108">Workflow er et system som kjører på Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="af06b-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="af06b-109">Arbeidsflytsystemet inneholder funksjonalitet du kan bruke til å opprette enkle arbeidsflyter eller forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="af06b-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="af06b-110">Arbeidsflyt er en forretningsprosess</span><span class="sxs-lookup"><span data-stu-id="af06b-110">Workflow is a business process</span></span>

<span data-ttu-id="af06b-111">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="af06b-111">A workflow represents a business process.</span></span> <span data-ttu-id="af06b-112">Det definerer hvordan et dokument går eller flyttes gjennom systemet ved å vise hvem som må utføre en oppgave, ta avgjørelser eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="af06b-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="af06b-113">Illustrasjonen nedenfor viser for eksempel en arbeidsflyt for reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="af06b-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Arbeidsflyt med elementer som er tilordnet til brukere](./media/workflow_user.gif)

<span data-ttu-id="af06b-115">Hvis du vil forstå denne arbeidsflyten bedre, kan vi anta at Erik sender en reiseregningsrapport på NOK 42 000.</span><span class="sxs-lookup"><span data-stu-id="af06b-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="af06b-116">I denne situasjonen må Henrik gå gjennom kvitteringene som Erik sendte til ham.</span><span class="sxs-lookup"><span data-stu-id="af06b-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="af06b-117">Deretter må Dag og Jorunn godkjenne reiseregningsrapporten.</span><span class="sxs-lookup"><span data-stu-id="af06b-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="af06b-118">La oss nå anta at Erik sender en reiseregningsrapport på NOK 11 000.</span><span class="sxs-lookup"><span data-stu-id="af06b-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="af06b-119">I denne situasjonen må Henrik se gjennom kvitteringene, og Dag, Jorunn og Karen må godkjenne reiseregningsrapporten.</span><span class="sxs-lookup"><span data-stu-id="af06b-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="af06b-120"> Fordeler ved bruk av arbeidsflytsystemet</span><span class="sxs-lookup"><span data-stu-id="af06b-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="af06b-121">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="af06b-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="af06b-122">**Konsekvente prosesser** – Du kan definere hvordan bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter, skal behandles.</span><span class="sxs-lookup"><span data-stu-id="af06b-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="af06b-123">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="af06b-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="af06b-124">**Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for arbeidsflytforekomster.</span><span class="sxs-lookup"><span data-stu-id="af06b-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="af06b-125">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="af06b-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="af06b-126">**Sentralisert arbeidsliste** – Brukere kan vise en sentralisert arbeidsliste som viser arbeidsflytoppgavene og -godkjenningene som er tilordnet til dem.</span><span class="sxs-lookup"><span data-stu-id="af06b-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="af06b-127">Arbeidsflytinnhold</span><span class="sxs-lookup"><span data-stu-id="af06b-127">Workflow content</span></span>

+ [<span data-ttu-id="af06b-128">Arkitektur i arbeidsflytsystemet</span><span class="sxs-lookup"><span data-stu-id="af06b-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="af06b-129">Arbeidsflytelementer</span><span class="sxs-lookup"><span data-stu-id="af06b-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="af06b-130">Handlinger i godkjenningsprosesser i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="af06b-131">Oversikt over å opprette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="af06b-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="af06b-132">Konfigurere egenskaper for arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="af06b-133">Konfigurere manuelle oppgaver i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="af06b-134">Konfigurere automatiserte oppgaver i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="af06b-135">Konfigurere godkjenningsprosesser i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="af06b-136">Konfigurere godkjenningstrinn i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="af06b-137">Konfigurere manuelle beslutninger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="af06b-138">Konfigurere en betingede beslutninger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="af06b-139">Konfigurere parallelle aktiviter i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="af06b-140">Konfigurere parallelle avdelinger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="af06b-141">Konfigurere arbeidsflyter for linjeelement</span><span class="sxs-lookup"><span data-stu-id="af06b-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="af06b-142">Vanlige spørsmål om arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="af06b-142">Workflow FAQ</span></span>](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]