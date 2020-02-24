---
title: Bruke arbeidsflyter til å administrere informasjon om ansatte
description: Denne artikkelen forklarer hvordan du kan bruke arbeidsflytfunksjonen for personal til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a159f5fd811ee80c0ac45ca1b582f2f46fcb2c61
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010032"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="5914a-104">Bruke arbeidsflyter til å administrere informasjon om ansatte</span><span class="sxs-lookup"><span data-stu-id="5914a-104">Use workflows to manage employee information</span></span>

<span data-ttu-id="5914a-105">Denne artikkelen forklarer hvordan du kan bruke arbeidsflytfunksjonen for personal til å administrere informasjon om ansatte.</span><span class="sxs-lookup"><span data-stu-id="5914a-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="5914a-106">Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post.</span><span class="sxs-lookup"><span data-stu-id="5914a-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="5914a-107">Arbeidsflytfunksjonen for personale inneholder flere arbeidsflyter for administrasjon av personalaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="5914a-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="5914a-108">I tillegg finnes mange tilgjengelige alternativer, slik at du kan endre bestemte arbeidsflyter og knytte dem til et rapporteringshierarki.</span><span class="sxs-lookup"><span data-stu-id="5914a-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="5914a-109">Arbeidsflyter er tilgjengelige for å bidra til å administrere endringer i standard informasjonstyper om ansatte.</span><span class="sxs-lookup"><span data-stu-id="5914a-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="5914a-110">Du kan knytte en arbeidsflyt til en stilling.</span><span class="sxs-lookup"><span data-stu-id="5914a-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="5914a-111">Hvis ansatte endrer sine ansattpost, startes en arbeidsflyt som krever godkjenning før den nye informasjonen lagres.</span><span class="sxs-lookup"><span data-stu-id="5914a-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="5914a-112">Arbeidsflyter er forhåndsdefinerte for følgende typer informasjon for å bidra til effektivt å administrere endringer og holde de ansattes data nøyaktige:</span><span class="sxs-lookup"><span data-stu-id="5914a-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="5914a-113">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="5914a-113">Identification numbers</span></span>
-   <span data-ttu-id="5914a-114">Kurs</span><span class="sxs-lookup"><span data-stu-id="5914a-114">Courses</span></span>
-   <span data-ttu-id="5914a-115">Utdanning</span><span class="sxs-lookup"><span data-stu-id="5914a-115">Education</span></span>
-   <span data-ttu-id="5914a-116">Bilde</span><span class="sxs-lookup"><span data-stu-id="5914a-116">Image</span></span>
-   <span data-ttu-id="5914a-117">Utlånte varer</span><span class="sxs-lookup"><span data-stu-id="5914a-117">Loaned items</span></span>
-   <span data-ttu-id="5914a-118">Yrkeserfaring</span><span class="sxs-lookup"><span data-stu-id="5914a-118">Professional experience</span></span>
-   <span data-ttu-id="5914a-119">Prosjekterfaring</span><span class="sxs-lookup"><span data-stu-id="5914a-119">Project experience</span></span>
-   <span data-ttu-id="5914a-120">Kompetanse</span><span class="sxs-lookup"><span data-stu-id="5914a-120">Skills</span></span>
-   <span data-ttu-id="5914a-121">Tillitsverv</span><span class="sxs-lookup"><span data-stu-id="5914a-121">Positions of trust</span></span>
-   <span data-ttu-id="5914a-122">Personalhandlinger</span><span class="sxs-lookup"><span data-stu-id="5914a-122">Human resources actions</span></span>
-   <span data-ttu-id="5914a-123">Kursregistrering</span><span class="sxs-lookup"><span data-stu-id="5914a-123">Course registration</span></span>

<span data-ttu-id="5914a-124">Når ansatte ansettes, overføres eller slutter, kan arbeidsflyten inneholde en gjennomgangsprosess.</span><span class="sxs-lookup"><span data-stu-id="5914a-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="5914a-125">På denne måten kan et dokument revideres eller vilkårene i en handling kan defineres som en del av arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="5914a-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="5914a-126">Når gjennomgangsprosessen er fullført, fullføres dokumentet eller handlingen, og arbeidsflyten går til et trinn for endelig godkjenning.</span><span class="sxs-lookup"><span data-stu-id="5914a-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="5914a-127">Knytte en arbeidsflyt til et stillingshierarki</span><span class="sxs-lookup"><span data-stu-id="5914a-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="5914a-128">Du kan knytte en arbeidsflyt til hvilket som helst hierarki som du konfigurerer.</span><span class="sxs-lookup"><span data-stu-id="5914a-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="5914a-129">Hvis en stilling for eksempel er tilknyttet et matriserapporteringshierarki, kan du konfigurere en arbeidsflyt som ruter utgifter for et bestemt prosjekt til prosjektleder i stedet for lederen for ansatt som er knyttet til denne stillingen.</span><span class="sxs-lookup"><span data-stu-id="5914a-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="5914a-130">Hvis du vil opprette en ny arbeidsflyt eller endre en eksisterende arbeidsflyt, går du til siden **Personalarbeidsflyter** og klikker på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5914a-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="5914a-131">Velg en arbeidsflyt i listen for å starte arbeidsflytutformingen.</span><span class="sxs-lookup"><span data-stu-id="5914a-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="5914a-132">Du kan bruke utformingen til å opprette en ny arbeidsflyt eller endre trinnene i en eksisterende arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="5914a-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="5914a-133">Når du endrer en eksisterende arbeidsflyt, lagres endringene som en ny versjon.</span><span class="sxs-lookup"><span data-stu-id="5914a-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="5914a-134">Derfor kan du alltid gå tilbake til en tidligere versjon hvis du må.</span><span class="sxs-lookup"><span data-stu-id="5914a-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="5914a-135">Konfigurere en personalarbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="5914a-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="5914a-136">Følg fremgangsmåten nedenfor hvis du vil konfigurere en grunnleggende arbeidsflyt som startes når ansatte be om endringer av sin personlige ID.</span><span class="sxs-lookup"><span data-stu-id="5914a-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="5914a-137">På siden **Personalarbeidsflyter** klikker du på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5914a-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="5914a-138">I listen over tilgjengelige arbeidsflyter velger du **Identifikasjonsnumre**.</span><span class="sxs-lookup"><span data-stu-id="5914a-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="5914a-139">Klikk på **Kjør** for å starte arbeidsflytutformingen, og angi deretter brukernavn og passord når du blir bedt om det.</span><span class="sxs-lookup"><span data-stu-id="5914a-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="5914a-140">Dra elementet **Godkjenn identifikasjonsnummer** fra listen over arbeidsflytelementer til utformingslerretet.</span><span class="sxs-lookup"><span data-stu-id="5914a-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="5914a-141">Koble godkjenningselement til **Start** og **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="5914a-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="5914a-142">Dobbeltklikk på **Godkjenn element**, og deretter høyreklikker du på og velger **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="5914a-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="5914a-143">Følg denne fremgangsmåten for å legge til instruksjoner for arbeidselement:</span><span class="sxs-lookup"><span data-stu-id="5914a-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="5914a-144">Velg **Tilordning**, og velg deretter **Hierarki** under tilordningstypen.</span><span class="sxs-lookup"><span data-stu-id="5914a-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="5914a-145">Under **Hierarki**-delen velger du **Konfigurerbart hierarki**.</span><span class="sxs-lookup"><span data-stu-id="5914a-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="5914a-146">Legge til et stoppvilkår, og lukke siden.</span><span class="sxs-lookup"><span data-stu-id="5914a-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="5914a-147">Fyll ut eventuelle instruksjoner (ingen ekstra advarsler skal finnes).</span><span class="sxs-lookup"><span data-stu-id="5914a-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="5914a-148">Klikk **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="5914a-148">Click **Save and close**.</span></span> <span data-ttu-id="5914a-149">Aktivere den nye arbeidsflyten når dialogboksen åpnes, og velger **Gjør aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5914a-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="5914a-150">Gå til **Personale** &gt; **Stillinger** &gt; **Stillingshierarkityper**.</span><span class="sxs-lookup"><span data-stu-id="5914a-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="5914a-151">Velg **Matrise**.</span><span class="sxs-lookup"><span data-stu-id="5914a-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="5914a-152">Legg til arbeidsflyten **Arbeideridentifikasjonsnummer** i listen.</span><span class="sxs-lookup"><span data-stu-id="5914a-152">Add the **Worker identification number** workflow to the list.</span></span>




