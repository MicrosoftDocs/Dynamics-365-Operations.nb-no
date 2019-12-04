---
title: Arbeidsflyter for innkjøp og leverandører
description: Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ceab555bf278ced13d8360956f6db65ba275f8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813460"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="eff2a-104">Arbeidsflyter for innkjøp og leverandører</span><span class="sxs-lookup"><span data-stu-id="eff2a-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eff2a-105">Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="eff2a-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="eff2a-106">Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="eff2a-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="eff2a-107">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="eff2a-107">A workflow represents a business process.</span></span> <span data-ttu-id="eff2a-108">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="eff2a-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="eff2a-109">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="eff2a-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="eff2a-110">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="eff2a-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="eff2a-111">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="eff2a-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="eff2a-112">**Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="eff2a-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="eff2a-113">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="eff2a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="eff2a-114">**Sentralisert arbeidsliste**– Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet på tvers av alle arbeidsflyter de deltar i.</span><span class="sxs-lookup"><span data-stu-id="eff2a-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="eff2a-115">Dette er tilgjengelig på siden Arbeidselementer.</span><span class="sxs-lookup"><span data-stu-id="eff2a-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="eff2a-116"> Arbeidsflyttypene som du kan opprette</span><span class="sxs-lookup"><span data-stu-id="eff2a-116">The types of workflows that you can create</span></span>
<span data-ttu-id="eff2a-117">Arbeidsflyttypene nedenfor er tilgjengelige for Innkjøp og leverandører.</span><span class="sxs-lookup"><span data-stu-id="eff2a-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="eff2a-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="eff2a-118">**Type**</span></span>                         | <span data-ttu-id="eff2a-119">**Bruk denne typen til å gjøre følgende:**</span><span class="sxs-lookup"><span data-stu-id="eff2a-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="eff2a-120">Gjennomgang av innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="eff2a-120">Purchase requisition review</span></span>      | <span data-ttu-id="eff2a-121">Opprett arbeidsflyter for gjennomgang og godkjenning av innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="eff2a-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="eff2a-122">Gjennomgang av innkjøpsrekvisisjonslinje</span><span class="sxs-lookup"><span data-stu-id="eff2a-122">Purchase requisition line review</span></span> | <span data-ttu-id="eff2a-123">Opprett arbeidsflyter for gjennomgang og godkjenning av innkjøpsrekvisisjonslinjer.</span><span class="sxs-lookup"><span data-stu-id="eff2a-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="eff2a-124">Bestillingsarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="eff2a-124">Purchase order workflow</span></span>          | <span data-ttu-id="eff2a-125">Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillinger.</span><span class="sxs-lookup"><span data-stu-id="eff2a-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="eff2a-126">Bestillingslinjearbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="eff2a-126">Purchase order line workflow</span></span>     | <span data-ttu-id="eff2a-127">Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="eff2a-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="eff2a-128">Arbeidsflyt for søknad om tillegging av leverandører</span><span class="sxs-lookup"><span data-stu-id="eff2a-128">Vendor add application workflow</span></span>  | <span data-ttu-id="eff2a-129">Opprett arbeidsflyter for gjennomgang og godkjenning for å legge til nye leverandører via leverandørforespørsler.</span><span class="sxs-lookup"><span data-stu-id="eff2a-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="eff2a-130">Opprette en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="eff2a-130">Creating a workflow</span></span>

<span data-ttu-id="eff2a-131">Hvis du vil opprette en arbeidsflyt, kan du gå til Innkjøp og leverandører &gt; Oppsett &gt; Arbeidsflyter for innkjøp og leverandører, og opprette en ny arbeidsflyt ved å velge typen arbeidsflyt som du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="eff2a-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="eff2a-132">Du kan dra arbeidsflytelementer til utformingen og koble elementene til en flyt på arbeidsflytlerretet.</span><span class="sxs-lookup"><span data-stu-id="eff2a-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="eff2a-133">Arbeidsflytelementene må konfigureres.</span><span class="sxs-lookup"><span data-stu-id="eff2a-133">The workflow elements should be configured.</span></span> <span data-ttu-id="eff2a-134">For arbeidsflytelementer for godkjenning og oppgave kan du konfigurere hvilken deltaker som skal utføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="eff2a-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="eff2a-135">Deltakertyper</span><span class="sxs-lookup"><span data-stu-id="eff2a-135">Types of participants</span></span>

<span data-ttu-id="eff2a-136">Du kan tilordne et godkjenningstrinn til deltakergruppene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="eff2a-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="eff2a-137">Brukergruppe</span><span class="sxs-lookup"><span data-stu-id="eff2a-137">User group</span></span>    | <span data-ttu-id="eff2a-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="eff2a-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="eff2a-139">Deltaker</span><span class="sxs-lookup"><span data-stu-id="eff2a-139">Participant</span></span>   | <span data-ttu-id="eff2a-140">Tilordne godkjenningstrinnet til medlemmer av en gruppe eller rolle.</span><span class="sxs-lookup"><span data-stu-id="eff2a-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="eff2a-141">Hierarki</span><span class="sxs-lookup"><span data-stu-id="eff2a-141">Hierarchy</span></span>     | <span data-ttu-id="eff2a-142">Tilordne godkjenningstrinnet til brukere i et bestemt organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="eff2a-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="eff2a-143">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="eff2a-143">Workflow user</span></span> | <span data-ttu-id="eff2a-144">Tilordne godkjenningstrinnet til brukere av denne arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="eff2a-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="eff2a-145">Kø</span><span class="sxs-lookup"><span data-stu-id="eff2a-145">Queue</span></span>         | <span data-ttu-id="eff2a-146">Tilordne godkjenningstrinnet til en arbeidselementkø.</span><span class="sxs-lookup"><span data-stu-id="eff2a-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="eff2a-147">Bruker</span><span class="sxs-lookup"><span data-stu-id="eff2a-147">User</span></span>          | <span data-ttu-id="eff2a-148">Tilordne godkjenningstrinnet til bestemte brukere.</span><span class="sxs-lookup"><span data-stu-id="eff2a-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="eff2a-149">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="eff2a-149">Additional resources</span></span>

- [<span data-ttu-id="eff2a-150">Definere arbeidsflyter for forretningsprosesser for innkjøpsrekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="eff2a-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="eff2a-151">Arbeidsflyt for innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="eff2a-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="eff2a-152">Ønske leverandører velkommen</span><span class="sxs-lookup"><span data-stu-id="eff2a-152">Onboard vendors</span></span>](vendor-onboarding.md)

