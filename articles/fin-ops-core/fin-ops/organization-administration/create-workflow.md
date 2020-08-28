---
title: Oversikt over å opprette arbeidsflyter
description: Dette emnet forklarer hvordan du oppretter en arbeidsflyt.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: bcd548bf8e03e0e6df4d413afe8c9ae01c570899
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698024"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="40760-103">Oversikt over å opprette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="40760-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40760-104">Dette emnet forklarer hvordan du oppretter en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="40760-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="40760-105">Åpne redigeringsprogrammet for arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-105">Open the workflow editor</span></span>

<span data-ttu-id="40760-106">Modulen du arbeider i bestemmer hvilke typer arbeidsflyt du kan opprette.</span><span class="sxs-lookup"><span data-stu-id="40760-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="40760-107">Følg denne fremgangsmåten for å velge typen arbeidsflyt for å opprette og åpne redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="40760-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="40760-108">Åpne modulen du vil opprette en ny arbeidsflyt for.</span><span class="sxs-lookup"><span data-stu-id="40760-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="40760-109">Hvis du for eksempel vil opprette en arbeidsflyt for innkjøpsrekvisisjoner, klikker du **Innkjøp og leverandører**.</span><span class="sxs-lookup"><span data-stu-id="40760-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="40760-110">Klikk **Oppsett** &gt; **\[Arbeidsflyter for\] modulnavn**.</span><span class="sxs-lookup"><span data-stu-id="40760-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="40760-111">På listesiden som vises klikker du **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="40760-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="40760-112">På siden **Opprett arbeidsflyt** velger du typen arbeidsflyt å opprette, og deretter klikker du **Opprett arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="40760-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="40760-113">Redigeringsprogrammet for arbeidsflyt åpnes.</span><span class="sxs-lookup"><span data-stu-id="40760-113">The workflow editor appears.</span></span> <span data-ttu-id="40760-114">Du kan nå bruke fremgangsmåtene nedenfor for utforme arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="40760-115">Dra arbeidsflytelementer til lerretet</span><span class="sxs-lookup"><span data-stu-id="40760-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="40760-116">**Arbeidsflytelementer**-området i redigeringsprogrammet for arbeidsflyt inneholder elementer som du kan legge til i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="40760-117">Hvis du vil legge til elementer i arbeidsflyten, drar du dem til arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="40760-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="40760-118">Koble elementene</span><span class="sxs-lookup"><span data-stu-id="40760-118">Connect the elements</span></span>

<span data-ttu-id="40760-119">Hvis du vil koble ett arbeidsflytelement til et annet, holder du markøren over et element til du ser koblingspunkt.</span><span class="sxs-lookup"><span data-stu-id="40760-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="40760-120">Klikk et koblingspunkt, og dra det til et annet element.</span><span class="sxs-lookup"><span data-stu-id="40760-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="40760-121">Pass på at du kobler alle elementene.</span><span class="sxs-lookup"><span data-stu-id="40760-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="40760-122">Konfigurere egenskapene for arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="40760-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="40760-123">Følg disse fremgangsmåtene for å konfigurere egenskapene for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="40760-124">Klikk lerretet for å være sikker på at ingen arbeidsflytelementer er valgt.</span><span class="sxs-lookup"><span data-stu-id="40760-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="40760-125">Klikk **Egenskaper** for å åpne **Egenskaper**-siden for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="40760-126">Følg fremgangsmåten i emnet [Konfigurere egenskaper arbeidsflyt](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="40760-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="40760-127">Konfigurere elementene for arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="40760-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="40760-128">Konfigurer hvert element du dro til lerretet.</span><span class="sxs-lookup"><span data-stu-id="40760-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="40760-129">Hvis du vil ha informasjon om hvordan du konfigurerer hvert arbeidsflytelement, kan du se emnet nedenfor .</span><span class="sxs-lookup"><span data-stu-id="40760-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="40760-130">Konfigurere manuelle oppgaver i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="40760-131">Konfigurere automatiserte oppgaver i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="40760-132">Konfigurere godkjenningsprosesser i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="40760-133">Konfigurere godkjenningstrinn i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="40760-134">Konfigurere manuelle beslutninger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="40760-135">Konfigurere en betingede beslutninger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="40760-136">Konfigurere parallelle avdelinger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="40760-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="40760-137">Konfigurere en parallell avdeling</span><span class="sxs-lookup"><span data-stu-id="40760-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="40760-138">Konfigurere arbeidsflyter for linjeelement</span><span class="sxs-lookup"><span data-stu-id="40760-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="40760-139">Løse eventuelle feil eller advarsler</span><span class="sxs-lookup"><span data-stu-id="40760-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="40760-140">**Feil og advarsler**-ruten, nederst i redigeringsprogrammet for arbeidsflyt, viser meldinger som er generert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="40760-141">Hvis du vil finne elementet der en feil eller advarsel oppstod, dobbeltklikker du feilen eller advarselen.</span><span class="sxs-lookup"><span data-stu-id="40760-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="40760-142">Du må løse alle feil og advarsler må løses før du kan aktivere arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="40760-143">Lagre og aktiver arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="40760-143">Save and activate the workflow</span></span>

<span data-ttu-id="40760-144">Når du er klar til å lagre og aktivere arbeidsflyten, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="40760-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="40760-145">Klikk **Lagre og Lukk** for å lukke redigeringsprogrammet for arbeidsflyt og åpne siden **Lagre arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="40760-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="40760-146">Angi kommentarer om endringene du har gjort i arbeidsflyten, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="40760-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="40760-147">Hvis alle problemer med feil og advarsler er løst, vises **Aktiver arbeidsflyt**-siden.</span><span class="sxs-lookup"><span data-stu-id="40760-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="40760-148">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="40760-148">Select one of the following options:</span></span>

    - <span data-ttu-id="40760-149">Hvis du vil aktivere denne versjonen av arbeidsflyten, klikker du **Aktiver den nye versjonen**.</span><span class="sxs-lookup"><span data-stu-id="40760-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="40760-150">Når en arbeidsflyt er aktiv, kan brukere sende dokumenter til den for behandling.</span><span class="sxs-lookup"><span data-stu-id="40760-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="40760-151">Hvis du ikke vil aktivere denne versjonen, klikker du **Ikke aktiver den nye versjonen**.</span><span class="sxs-lookup"><span data-stu-id="40760-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="40760-152">Du kan aktivere arbeidsflyten senere.</span><span class="sxs-lookup"><span data-stu-id="40760-152">You can activate the workflow later.</span></span>
