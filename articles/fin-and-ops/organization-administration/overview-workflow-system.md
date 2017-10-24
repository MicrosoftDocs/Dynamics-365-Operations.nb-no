---
title: Arbeidsflytoversikt
description: Dette emnet beskriver arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6622f0e5ed6c38bb8131d13aa02061968862678b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-overview"></a><span data-ttu-id="6d0b8-103">Arbeidsflytoversikt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-103">Workflow overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6d0b8-104">Dette emnet beskriver arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="6d0b8-105">Hva er arbeidsflyt?</span><span class="sxs-lookup"><span data-stu-id="6d0b8-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="6d0b8-106">Begrepet *arbeidsflyt* kan defineres på to måter: som et system og en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="6d0b8-107">Workflow er et system</span><span class="sxs-lookup"><span data-stu-id="6d0b8-107">Workflow is a system</span></span>

<span data-ttu-id="6d0b8-108">Arbeidsflyt er et system som installeres med Finance and Operations, og som kjøres på Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="6d0b8-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="6d0b8-109">Arbeidsflytsystemet inneholder funksjonalitet du kan bruke til å opprette enkle arbeidsflyter eller forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="6d0b8-110">Arbeidsflyt er en forretningsprosess</span><span class="sxs-lookup"><span data-stu-id="6d0b8-110">Workflow is a business process</span></span>

<span data-ttu-id="6d0b8-111">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-111">A workflow represents a business process.</span></span> <span data-ttu-id="6d0b8-112">Det definerer hvordan et dokument går eller flyttes gjennom systemet ved å vise hvem som må utføre en oppgave, ta avgjørelser eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="6d0b8-113">Illustrasjonen nedenfor viser for eksempel en arbeidsflyt for reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![Arbeidsflyt med elementer som er tilordnet til brukere](./media/workflow_user.gif) 

<span data-ttu-id="6d0b8-115">Hvis du vil forstå denne arbeidsflyten bedre, kan vi anta at Erik sender en reiseregningsrapport på NOK 42 000.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="6d0b8-116">I denne situasjonen må Henrik gå gjennom kvitteringene som Erik sendte til ham.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="6d0b8-117">Deretter må Dag og Jorunn godkjenne reiseregningsrapporten.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="6d0b8-118">La oss nå anta at Erik sender en reiseregningsrapport på NOK 11 000.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="6d0b8-119">I denne situasjonen må Henrik se gjennom kvitteringene, og Dag, Jorunn og Karen må godkjenne reiseregningsrapporten.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="6d0b8-120"> Fordeler ved bruk av arbeidsflytsystemet</span><span class="sxs-lookup"><span data-stu-id="6d0b8-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="6d0b8-121">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="6d0b8-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="6d0b8-122">**Konsekvente prosesser** – Du kan definere hvordan bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter, skal behandles.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="6d0b8-123">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="6d0b8-124">**Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for arbeidsflytforekomster.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="6d0b8-125">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="6d0b8-126">**Sentralisert arbeidsliste** – Brukere kan vise en sentralisert arbeidsliste som viser arbeidsflytoppgavene og -godkjenningene som er tilordnet til dem.</span><span class="sxs-lookup"><span data-stu-id="6d0b8-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="6d0b8-127">Arbeidsflytinnhold</span><span class="sxs-lookup"><span data-stu-id="6d0b8-127">Workflow content</span></span>

+ [<span data-ttu-id="6d0b8-128">Arbeidsflytarkitektur</span><span class="sxs-lookup"><span data-stu-id="6d0b8-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="6d0b8-129">Arbeidsflytelementer</span><span class="sxs-lookup"><span data-stu-id="6d0b8-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="6d0b8-130">Arbeidsflythandlinger</span><span class="sxs-lookup"><span data-stu-id="6d0b8-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="6d0b8-131">Opprette en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="6d0b8-132">Konfigurere egenskaper for arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="6d0b8-133">Konfigurere en manuell oppgave i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="6d0b8-134">Konfigurere en automatisert oppgave i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="6d0b8-135">Konfigurere en godkjenningsprosess i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="6d0b8-136">Konfigurere et godkjenningstrinn i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="6d0b8-137">Konfigurere en manuell beslutning i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="6d0b8-138">Konfigurere en betinget beslutning i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="6d0b8-139">Konfigurere en parallell aktivitet i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="6d0b8-140">Konfigurere en parallell avdeling i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="6d0b8-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="6d0b8-141">Konfigurere en arbeidsflyt for linjeelement</span><span class="sxs-lookup"><span data-stu-id="6d0b8-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

