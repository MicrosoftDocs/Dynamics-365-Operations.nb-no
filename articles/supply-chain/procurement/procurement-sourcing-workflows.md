---
title: Arbeidsflyter for innkjøp og leverandører
description: Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af614b7f29144d02a853ef15b008f2a21d3d3aa5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019760"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="05deb-104">Arbeidsflyter for innkjøp og leverandører</span><span class="sxs-lookup"><span data-stu-id="05deb-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05deb-105">Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="05deb-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="05deb-106">Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="05deb-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="05deb-107">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="05deb-107">A workflow represents a business process.</span></span> <span data-ttu-id="05deb-108">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="05deb-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="05deb-109">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="05deb-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="05deb-110">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="05deb-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="05deb-111">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="05deb-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="05deb-112">**Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="05deb-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="05deb-113">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="05deb-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="05deb-114">**Sentralisert arbeidsliste**– Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet på tvers av alle arbeidsflyter de deltar i.</span><span class="sxs-lookup"><span data-stu-id="05deb-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="05deb-115">Dette er tilgjengelig på siden Arbeidselementer.</span><span class="sxs-lookup"><span data-stu-id="05deb-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="05deb-116"> Arbeidsflyttypene som du kan opprette</span><span class="sxs-lookup"><span data-stu-id="05deb-116">The types of workflows that you can create</span></span>

<span data-ttu-id="05deb-117">Arbeidsflyttypene nedenfor er tilgjengelige for Innkjøp og leverandører.</span><span class="sxs-lookup"><span data-stu-id="05deb-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="05deb-118">Type</span><span class="sxs-lookup"><span data-stu-id="05deb-118">Type</span></span> | <span data-ttu-id="05deb-119">Bruk denne typen til å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="05deb-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="05deb-120">Gjennomgang av innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="05deb-120">Purchase requisition review</span></span> | <span data-ttu-id="05deb-121">Opprett arbeidsflyter for gjennomgang og godkjenning av innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="05deb-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="05deb-122">Gjennomgang av innkjøpsrekvisisjonslinje</span><span class="sxs-lookup"><span data-stu-id="05deb-122">Purchase requisition line review</span></span> | <span data-ttu-id="05deb-123">Opprett arbeidsflyter for gjennomgang og godkjenning av innkjøpsrekvisisjonslinjer.</span><span class="sxs-lookup"><span data-stu-id="05deb-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="05deb-124">Bestillingsarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="05deb-124">Purchase order workflow</span></span> | <span data-ttu-id="05deb-125">Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillinger.</span><span class="sxs-lookup"><span data-stu-id="05deb-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="05deb-126">Bestillingslinjearbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="05deb-126">Purchase order line workflow</span></span> | <span data-ttu-id="05deb-127">Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="05deb-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="05deb-128">Arbeidsflyt for søknad om tillegging av leverandører</span><span class="sxs-lookup"><span data-stu-id="05deb-128">Vendor add application workflow</span></span> | <span data-ttu-id="05deb-129">Opprett arbeidsflyter for gjennomgang og godkjenning for å legge til nye leverandører via leverandørforespørsler.</span><span class="sxs-lookup"><span data-stu-id="05deb-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="05deb-130">Når du legger til en ny arbeidsflyt, kan det hende at du også ser følgende foreldede arbeidsflyter som vises i dialogboksen **Opprett arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="05deb-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="05deb-131">Disse er knyttet til funksjonaliteten *bekreftelse på mottak* som var tilgjengelig i [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), men som nå er avskrevet.</span><span class="sxs-lookup"><span data-stu-id="05deb-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="05deb-132">Disse arbeidsflytene støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="05deb-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="05deb-133">Varslingsarbeidsflyt for forfallsdato for levering</span><span class="sxs-lookup"><span data-stu-id="05deb-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="05deb-134">Varslingsarbeidsflyt for fakturamottak</span><span class="sxs-lookup"><span data-stu-id="05deb-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="05deb-135">Varslingsarbeidsflyt for mislykket mottaksseddel</span><span class="sxs-lookup"><span data-stu-id="05deb-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="05deb-136">Varslingsarbeidsflyt for ubekreftet mottaksseddelavvisning</span><span class="sxs-lookup"><span data-stu-id="05deb-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="05deb-137">Opprette en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="05deb-137">Creating a workflow</span></span>

<span data-ttu-id="05deb-138">Hvis du vil opprette en arbeidsflyt, kan du gå til Innkjøp og leverandører &gt; Oppsett &gt; Arbeidsflyter for innkjøp og leverandører, og opprette en ny arbeidsflyt ved å velge typen arbeidsflyt som du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="05deb-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="05deb-139">Du kan dra arbeidsflytelementer til utformingen og koble elementene til en flyt på arbeidsflytlerretet.</span><span class="sxs-lookup"><span data-stu-id="05deb-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="05deb-140">Arbeidsflytelementene må konfigureres.</span><span class="sxs-lookup"><span data-stu-id="05deb-140">The workflow elements should be configured.</span></span> <span data-ttu-id="05deb-141">For arbeidsflytelementer for godkjenning og oppgave kan du konfigurere hvilken deltaker som skal utføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="05deb-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="05deb-142">Deltakertyper</span><span class="sxs-lookup"><span data-stu-id="05deb-142">Types of participants</span></span>

<span data-ttu-id="05deb-143">Du kan tilordne et godkjenningstrinn til deltakergruppene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="05deb-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="05deb-144">Brukergruppe</span><span class="sxs-lookup"><span data-stu-id="05deb-144">User group</span></span> | <span data-ttu-id="05deb-145">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="05deb-145">Description</span></span> |
|---|---|
| <span data-ttu-id="05deb-146">Deltaker</span><span class="sxs-lookup"><span data-stu-id="05deb-146">Participant</span></span> | <span data-ttu-id="05deb-147">Tilordne godkjenningstrinnet til medlemmer av en gruppe eller rolle.</span><span class="sxs-lookup"><span data-stu-id="05deb-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="05deb-148">Hierarki</span><span class="sxs-lookup"><span data-stu-id="05deb-148">Hierarchy</span></span> | <span data-ttu-id="05deb-149">Tilordne godkjenningstrinnet til brukere i et bestemt organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="05deb-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="05deb-150">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="05deb-150">Workflow user</span></span> | <span data-ttu-id="05deb-151">Tilordne godkjenningstrinnet til brukere av denne arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="05deb-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="05deb-152">Kø</span><span class="sxs-lookup"><span data-stu-id="05deb-152">Queue</span></span> | <span data-ttu-id="05deb-153">Tilordne godkjenningstrinnet til en arbeidselementkø.</span><span class="sxs-lookup"><span data-stu-id="05deb-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="05deb-154">Bruker</span><span class="sxs-lookup"><span data-stu-id="05deb-154">User</span></span> | <span data-ttu-id="05deb-155">Tilordne godkjenningstrinnet til bestemte brukere.</span><span class="sxs-lookup"><span data-stu-id="05deb-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="05deb-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="05deb-156">Additional resources</span></span>

- [<span data-ttu-id="05deb-157">Definere arbeidsflyter for forretningsprosesser for innkjøpsrekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="05deb-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="05deb-158">Arbeidsflyt for innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="05deb-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="05deb-159">Ønske leverandører velkommen</span><span class="sxs-lookup"><span data-stu-id="05deb-159">Onboard vendors</span></span>](vendor-onboarding.md)
