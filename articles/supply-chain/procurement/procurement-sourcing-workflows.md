---
title: "Arbeidsflyter for innkjøp og leverandører"
description: "Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="21d19-104">Arbeidsflyter for innkjøp og leverandører</span><span class="sxs-lookup"><span data-stu-id="21d19-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21d19-105">Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="21d19-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="21d19-106">Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="21d19-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="21d19-107">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="21d19-107">A workflow represents a business process.</span></span> <span data-ttu-id="21d19-108">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="21d19-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="21d19-109">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="21d19-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="21d19-110">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="21d19-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="21d19-111">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="21d19-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="21d19-112">**Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="21d19-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="21d19-113">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="21d19-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="21d19-114">**Sentralisert arbeidsliste**– Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet på tvers av alle arbeidsflyter de deltar i.</span><span class="sxs-lookup"><span data-stu-id="21d19-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="21d19-115">Dette er tilgjengelig på siden Arbeidselementer.</span><span class="sxs-lookup"><span data-stu-id="21d19-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="21d19-116"> Arbeidsflyttypene som du kan opprette</span><span class="sxs-lookup"><span data-stu-id="21d19-116">The types of workflows that you can create</span></span>
<span data-ttu-id="21d19-117">Arbeidsflyttypene nedenfor er tilgjengelige for Innkjøp og leverandører.</span><span class="sxs-lookup"><span data-stu-id="21d19-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="21d19-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="21d19-118">**Type**</span></span>                         | <span data-ttu-id="21d19-119">**Bruk denne typen til å gjøre følgende:**</span><span class="sxs-lookup"><span data-stu-id="21d19-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="21d19-120">Gjennomgang av innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="21d19-120">Purchase requisition review</span></span>      | <span data-ttu-id="21d19-121">Opprett gjennomgangsarbeidsflyter for innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="21d19-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="21d19-122">Gjennomgang av innkjøpsrekvisisjonslinje</span><span class="sxs-lookup"><span data-stu-id="21d19-122">Purchase requisition line review</span></span> | <span data-ttu-id="21d19-123">Opprett gjennomgangsarbeidsflyter for innkjøpsrekvisisjonslinjer.</span><span class="sxs-lookup"><span data-stu-id="21d19-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="21d19-124">Bestillingsarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="21d19-124">Purchase order workflow</span></span>          | <span data-ttu-id="21d19-125">Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillinger.</span><span class="sxs-lookup"><span data-stu-id="21d19-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="21d19-126">Bestillingslinjearbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="21d19-126">Purchase order line workflow</span></span>     | <span data-ttu-id="21d19-127">Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="21d19-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="21d19-128">Opprette en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="21d19-128">Creating a workflow</span></span>
<span data-ttu-id="21d19-129">Hvis du vil opprette en arbeidsflyt, kan du gå til Innkjøp og leverandører &gt; Oppsett &gt; Arbeidsflyter for innkjøp og leverandører, og opprette en ny arbeidsflyt ved å velge typen arbeidsflyt som du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="21d19-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="21d19-130">Du kan dra arbeidsflytelementer til utformingen og koble elementene til en flyt på arbeidsflytlerretet.</span><span class="sxs-lookup"><span data-stu-id="21d19-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="21d19-131">Arbeidsflytelementene må konfigureres.</span><span class="sxs-lookup"><span data-stu-id="21d19-131">The workflow elements should be configured.</span></span> <span data-ttu-id="21d19-132">For arbeidsflytelementer for godkjenning og oppgave kan du konfigurere hvilken deltaker som skal utføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="21d19-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="21d19-133">Deltakertyper</span><span class="sxs-lookup"><span data-stu-id="21d19-133">Types of participants</span></span>
----------------------

<span data-ttu-id="21d19-134">Du kan tilordne et godkjenningstrinn til deltakergruppene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="21d19-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="21d19-135">Brukergruppe</span><span class="sxs-lookup"><span data-stu-id="21d19-135">User group</span></span>    | <span data-ttu-id="21d19-136">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="21d19-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="21d19-137">Deltaker</span><span class="sxs-lookup"><span data-stu-id="21d19-137">Participant</span></span>   | <span data-ttu-id="21d19-138">Tilordne godkjenningstrinnet til medlemmer av en gruppe eller rolle.</span><span class="sxs-lookup"><span data-stu-id="21d19-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="21d19-139">Hierarki</span><span class="sxs-lookup"><span data-stu-id="21d19-139">Hierarchy</span></span>     | <span data-ttu-id="21d19-140">Tilordne godkjenningstrinnet til brukere i et bestemt organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="21d19-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="21d19-141">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="21d19-141">Workflow user</span></span> | <span data-ttu-id="21d19-142">Tilordne godkjenningstrinnet til brukere av denne arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="21d19-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="21d19-143">Kø</span><span class="sxs-lookup"><span data-stu-id="21d19-143">Queue</span></span>         | <span data-ttu-id="21d19-144">Tilordne godkjenningstrinnet til en arbeidselementkø.</span><span class="sxs-lookup"><span data-stu-id="21d19-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="21d19-145">Bruker</span><span class="sxs-lookup"><span data-stu-id="21d19-145">User</span></span>          | <span data-ttu-id="21d19-146">Tilordne godkjenningstrinnet til bestemte brukere.</span><span class="sxs-lookup"><span data-stu-id="21d19-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="21d19-147">Se også</span><span class="sxs-lookup"><span data-stu-id="21d19-147">See also</span></span>
--------

[<span data-ttu-id="21d19-148">Definere arbeidsflyter for forretningsprosesser for innkjøpsrekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="21d19-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="21d19-149">Arbeidsflyt for innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="21d19-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




