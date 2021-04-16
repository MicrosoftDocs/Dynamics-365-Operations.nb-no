---
title: Konfigurere manuelle oppgaver i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene for en manuell oppgave.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4be7f0ee5e487185033b7ccb9a2b0a91eb4a36c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747861"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="c667e-103">Konfigurere manuelle oppgaver i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="c667e-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c667e-104">Dette emnet forklarer hvordan du konfigurerer egenskapene for en manuell oppgave.</span><span class="sxs-lookup"><span data-stu-id="c667e-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="c667e-105">Når du skal konfigurere en manuell oppgave i redigeringsprogrammet for arbeidsflyt, høyreklikker du oppgaven og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="c667e-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c667e-106">Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for den manuelle oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="c667e-107">Gi navn til oppgaven</span><span class="sxs-lookup"><span data-stu-id="c667e-107">Name the task</span></span>

<span data-ttu-id="c667e-108">Følg denne fremgangsmåten for å sette et navn på den manuelle oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="c667e-109">Klikk på **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="c667e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c667e-110">I feltet **Navn** angir du et unikt navn på oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="c667e-111">Legg inn en emnelinje og instruksjoner</span><span class="sxs-lookup"><span data-stu-id="c667e-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="c667e-112">Du må skrive inn en emnelinje og instruksjoner til brukeren som er knyttet til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="c667e-113">Hvis du for eksempel konfigurerer en oppgave for innkjøpsrekvisisjoner, ser brukeren som er tilordnet til oppgaven, emnelinjen og instruksjonene på **Innkjøpsrekvisisjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="c667e-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="c667e-114">Emnelinjen vises i en meldingslinje øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="c667e-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="c667e-115">Brukeren kan deretter klikke ikonet i meldingslinjen for å vise instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="c667e-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="c667e-116">Følg trinnene nedenfor for å legge inn en emnelinje og instruksjoner.</span><span class="sxs-lookup"><span data-stu-id="c667e-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="c667e-117">Klikk på **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="c667e-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c667e-118">I **Emne for arbeidselement**-feltet angir du emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="c667e-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="c667e-119">Hvis du vil tilpasse emnelinjen, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="c667e-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="c667e-120">Plassholdere erstattes med de riktige dataene når emnelinjen vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="c667e-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="c667e-121">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="c667e-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="c667e-122">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="c667e-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c667e-123">Klikk på **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="c667e-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c667e-124">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="c667e-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c667e-125">Klikk på **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="c667e-125">Click **Insert**.</span></span>

4. <span data-ttu-id="c667e-126">Hvis du vil legge til oversettelser av emnelinjen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c667e-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="c667e-127">Klikk på **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="c667e-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="c667e-128">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c667e-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c667e-129">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="c667e-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="c667e-130">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="c667e-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c667e-131">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="c667e-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="c667e-132">Klikk på **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="c667e-132">Click **Close**.</span></span>

5. <span data-ttu-id="c667e-133">I **Instruksjoner for arbeidselement**-feltet angir du instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="c667e-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="c667e-134">Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="c667e-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="c667e-135">Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="c667e-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="c667e-136">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="c667e-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="c667e-137">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="c667e-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c667e-138">Klikk på **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="c667e-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c667e-139">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="c667e-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c667e-140">Klikk på **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="c667e-140">Click **Insert**.</span></span>

7. <span data-ttu-id="c667e-141">Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c667e-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="c667e-142">Klikk på **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="c667e-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="c667e-143">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c667e-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c667e-144">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="c667e-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="c667e-145">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="c667e-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c667e-146">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 6.</span><span class="sxs-lookup"><span data-stu-id="c667e-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="c667e-147">Klikk på **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="c667e-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="c667e-148">Tildele oppgaven</span><span class="sxs-lookup"><span data-stu-id="c667e-148">Assign the task</span></span>

<span data-ttu-id="c667e-149">Følg denne fremgangsmåten for å angi hvem den manuelle oppgaven skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="c667e-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="c667e-150">I den venstre ruten klikker du **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="c667e-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="c667e-151">I **Tilordningstype**-fanen velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 3.</span><span class="sxs-lookup"><span data-stu-id="c667e-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c667e-152">Alternativ</span><span class="sxs-lookup"><span data-stu-id="c667e-152">Option</span></span></th>
    <th><span data-ttu-id="c667e-153">Brukere som oppgaven er tilordnet til</span><span class="sxs-lookup"><span data-stu-id="c667e-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="c667e-154">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="c667e-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c667e-155">Deltaker</span><span class="sxs-lookup"><span data-stu-id="c667e-155">Participant</span></span></td>
    <td><span data-ttu-id="c667e-156">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="c667e-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-157">Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-fanen i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som oppgaven skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="c667e-158">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som oppgaven skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-159">Hierarki</span><span class="sxs-lookup"><span data-stu-id="c667e-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="c667e-160">Brukere i et bestemt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="c667e-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-161">Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-fanen i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som oppgaven skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="c667e-162">Systemet må hente et område med brukernavn fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c667e-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="c667e-163">Disse navnene representerer brukere som oppgaven kan tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="c667e-164">Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="c667e-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="c667e-165">Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</span><span class="sxs-lookup"><span data-stu-id="c667e-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="c667e-166">Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="c667e-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="c667e-167">Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</span><span class="sxs-lookup"><span data-stu-id="c667e-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="c667e-168">I fanen <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som oppgaven skal tilordnes til:</span><span class="sxs-lookup"><span data-stu-id="c667e-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="c667e-169"><strong>Tilordne til alle hentede brukere</strong> – Oppgaven tilordnes til alle brukere i området.</span><span class="sxs-lookup"><span data-stu-id="c667e-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="c667e-170"><strong>Bare tilordne til den siste hentede brukeren</strong> – Oppgaven tilordnes bare til den siste brukeren i området.</span><span class="sxs-lookup"><span data-stu-id="c667e-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="c667e-171"><strong>Utelat brukere med følgende vilkår</strong> – Oppgaven tilordnes ikke til noen brukere i området som oppfyller et bestemt vilkår.</span><span class="sxs-lookup"><span data-stu-id="c667e-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="c667e-172">Klikk på <strong>Legg til betingelse</strong> for å angi vilkåret.</span><span class="sxs-lookup"><span data-stu-id="c667e-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-173">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="c667e-173">Workflow user</span></span></td>
    <td><span data-ttu-id="c667e-174">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="c667e-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="c667e-175">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="c667e-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-176">Bruker</span><span class="sxs-lookup"><span data-stu-id="c667e-176">User</span></span></td>
    <td><span data-ttu-id="c667e-177">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="c667e-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-178">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c667e-179"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere.</span><span class="sxs-lookup"><span data-stu-id="c667e-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c667e-180">Velg brukerne du vil tilordne oppgaven til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="c667e-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-181">Kø</span><span class="sxs-lookup"><span data-stu-id="c667e-181">Queue</span></span></td>
    <td><span data-ttu-id="c667e-182">En arbeidselementkø</span><span class="sxs-lookup"><span data-stu-id="c667e-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-183">Når du har valgt <strong>Kø</strong>, klikker du <strong>Købasert</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="c667e-184">Gjør følgende for å tilordne oppgaven til en bestemt kø:</span><span class="sxs-lookup"><span data-stu-id="c667e-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="c667e-185">I <strong>Køtype</strong>-listen velger du <strong>Arbeidselementkøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="c667e-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="c667e-186">Velg køen i <strong>Kønavn</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="c667e-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="c667e-187">Hvis en bestemt betingelse skal bestemme hvilken kø oppgaven skal tilordnes til, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="c667e-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="c667e-188">I <strong>Køtype</strong>-listen velger du <strong>Betingede arbeidselementkøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="c667e-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="c667e-189">I <strong>Kønavn</strong>-listen velger du <strong>Betinget kø</strong>.</span><span class="sxs-lookup"><span data-stu-id="c667e-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="c667e-190">Dette alternativet brukes bare i noen få arbeidsflyter, for eksempel saksbehandling.</span><span class="sxs-lookup"><span data-stu-id="c667e-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="c667e-191">I **Tidsbegrensning**-fanen i **Varighet**-feltet angir du hvor lang tid brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="c667e-192">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="c667e-192">Select one of the following options:</span></span>

    - <span data-ttu-id="c667e-193">**Timer** – Angi antallet timer som brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="c667e-194">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="c667e-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c667e-195">**Dager** – Angi antallet dager som brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="c667e-196">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="c667e-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c667e-197">**Uker** – Angi antallet uker som brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="c667e-198">**Måneder** – Velg dagen og uken som brukeren senest må fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="c667e-199">Du vil kanskje at brukeren fullfører oppgaven innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="c667e-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="c667e-200">**År** – Velg dagen, uken og måneden som brukeren senest må fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="c667e-201">Du vil kanskje at brukeren svarer innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="c667e-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="c667e-202">Hvis brukeren ikke fullfører oppgaven innenfor den tillatte tiden, er oppgaven forfalt.</span><span class="sxs-lookup"><span data-stu-id="c667e-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="c667e-203">En oppgave som er forfalt, kan videresendes, basert på alternativene du velger i **Eskalering**-området på siden.</span><span class="sxs-lookup"><span data-stu-id="c667e-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="c667e-204">Angi hva som skal skje når en oppgave er forfalt</span><span class="sxs-lookup"><span data-stu-id="c667e-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="c667e-205">Hvis en bruker ikke fullfører den manuelle oppgaven innenfor den tillatte tiden, er oppgaven forfalt.</span><span class="sxs-lookup"><span data-stu-id="c667e-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="c667e-206">En oppgave som er forfalt, kan videresendes eller tilordnes automatisk til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="c667e-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="c667e-207">Følg denne fremgangsmåten for å videresende oppgaven hvis den er forfalt.</span><span class="sxs-lookup"><span data-stu-id="c667e-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="c667e-208">I den venstre ruten klikker du **Eskalering**.</span><span class="sxs-lookup"><span data-stu-id="c667e-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="c667e-209">Merk av for **Bruk videresendingsbane** hvis du vil opprette en videresendingsbane.</span><span class="sxs-lookup"><span data-stu-id="c667e-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="c667e-210">Systemet tilordner automatisk oppgaven til brukerne som er oppført i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="c667e-211">Tabellen nedenfor er et eksempel på en videresendingsbane.</span><span class="sxs-lookup"><span data-stu-id="c667e-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="c667e-212">Sekvens</span><span class="sxs-lookup"><span data-stu-id="c667e-212">Sequence</span></span> | <span data-ttu-id="c667e-213">Videresendingsbane</span><span class="sxs-lookup"><span data-stu-id="c667e-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="c667e-214">1</span><span class="sxs-lookup"><span data-stu-id="c667e-214">1</span></span>        | <span data-ttu-id="c667e-215">Tilordne til: Doris</span><span class="sxs-lookup"><span data-stu-id="c667e-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="c667e-216">2</span><span class="sxs-lookup"><span data-stu-id="c667e-216">2</span></span>        | <span data-ttu-id="c667e-217">Tilordne til: Elin</span><span class="sxs-lookup"><span data-stu-id="c667e-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="c667e-218">3</span><span class="sxs-lookup"><span data-stu-id="c667e-218">3</span></span>        | <span data-ttu-id="c667e-219">Endelig handling: Avvis</span><span class="sxs-lookup"><span data-stu-id="c667e-219">Final action: Reject</span></span> |

    <span data-ttu-id="c667e-220">I dette eksempelet tilordnes den forfalte oppgaven til Doris.</span><span class="sxs-lookup"><span data-stu-id="c667e-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="c667e-221">Hvis Doris ikke fullfører oppgaven innen tidsfristen, tilordnes oppgaven til Elin.</span><span class="sxs-lookup"><span data-stu-id="c667e-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="c667e-222">Hvis Elin ikke fullfører oppgaven innen tidsfristen, vil systemet avvise dokumentet som ble sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="c667e-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="c667e-223">Klikk på **Legg til videresending** for å legge til en bruker i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="c667e-224">I **Tilordningstype**-fanen velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 4.</span><span class="sxs-lookup"><span data-stu-id="c667e-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c667e-225">Alternativ</span><span class="sxs-lookup"><span data-stu-id="c667e-225">Option</span></span></th>
    <th><span data-ttu-id="c667e-226">Brukere som oppgaven videresendes til</span><span class="sxs-lookup"><span data-stu-id="c667e-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="c667e-227">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="c667e-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c667e-228">Hierarki</span><span class="sxs-lookup"><span data-stu-id="c667e-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="c667e-229">Brukere i et bestemt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="c667e-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-230">Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-fanen i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som oppgaven skal videresendes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="c667e-231">Systemet må hente et område med brukernavn fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c667e-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="c667e-232">Disse navnene representerer brukere som oppgaven kan videresendes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="c667e-233">Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="c667e-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="c667e-234">Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</span><span class="sxs-lookup"><span data-stu-id="c667e-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="c667e-235">Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="c667e-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="c667e-236">Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</span><span class="sxs-lookup"><span data-stu-id="c667e-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="c667e-237">I fanen <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som oppgaven skal videresendes til:</span><span class="sxs-lookup"><span data-stu-id="c667e-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="c667e-238"><strong>Tilordne til alle hentede brukere</strong> – Oppgaven videresendes til alle brukere i området.</span><span class="sxs-lookup"><span data-stu-id="c667e-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="c667e-239"><strong>Bare tilordne til den siste hentede brukeren</strong> – Oppgaven videresendes bare til den siste brukeren i området.</span><span class="sxs-lookup"><span data-stu-id="c667e-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="c667e-240"><strong>Utelat brukere med følgende vilkår</strong> – Oppgaven videresendes ikke til noen brukere i området som oppfyller et bestemt vilkår.</span><span class="sxs-lookup"><span data-stu-id="c667e-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="c667e-241">Klikk på <strong>Legg til betingelse</strong> for å angi vilkåret.</span><span class="sxs-lookup"><span data-stu-id="c667e-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-242">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="c667e-242">Workflow user</span></span></td>
    <td><span data-ttu-id="c667e-243">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="c667e-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="c667e-244">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="c667e-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-245">Bruker</span><span class="sxs-lookup"><span data-stu-id="c667e-245">User</span></span></td>
    <td><span data-ttu-id="c667e-246">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="c667e-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-247">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c667e-248"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere.</span><span class="sxs-lookup"><span data-stu-id="c667e-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c667e-249">Velg brukerne du vil videresende oppgaven til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="c667e-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="c667e-250">I **Tidsbegrensning**-fanen i **Varighet**-feltet angir du hvor lang tid brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="c667e-251">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="c667e-251">Select one of the following options:</span></span>

    - <span data-ttu-id="c667e-252">**Timer** – Angi antallet timer som brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="c667e-253">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="c667e-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c667e-254">**Dager** – Angi antallet dager som brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="c667e-255">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="c667e-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c667e-256">**Uker** – Angi antallet uker som brukeren har til å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="c667e-257">**Måneder** – Velg dagen og uken som brukeren senest må fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="c667e-258">Du vil kanskje at brukeren fullfører oppgaven innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="c667e-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="c667e-259">**År** – Velg dagen, uken og måneden som brukeren senest må fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="c667e-260">Du vil kanskje at brukeren svarer innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="c667e-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="c667e-261">Gjenta trinn 3 og 4 for hver bruker som skal legges til i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="c667e-262">Du kan endre rekkefølgen på brukerne.</span><span class="sxs-lookup"><span data-stu-id="c667e-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="c667e-263">Hvis brukerne i videresendingsbanen ikke fullfører oppgaven innen tidsfristen, vil systemet utføre en handling med oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="c667e-264">Hvis du vil angi handlingen systemet skal utføre, merker du **Handling**-raden, og velger deretter en handling i fanen **Avslutt handling**.</span><span class="sxs-lookup"><span data-stu-id="c667e-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="c667e-265">Angi når systemet skal utføre en handling med oppgaven automatisk</span><span class="sxs-lookup"><span data-stu-id="c667e-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="c667e-266">Du kan konfigurere systemet slik at det utfører en handling med den manuelle oppgaven når bestemte betingelser er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="c667e-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="c667e-267">En oppgave krever for eksempel at noen i reiseregningsavdelingen går gjennom kvitteringene som følger med reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="c667e-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="c667e-268">I henhold til firmapolicyen må denne oppgaven utføres hvis det totale beløpet for utgiftsrapporten er større enn USD 100.</span><span class="sxs-lookup"><span data-stu-id="c667e-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="c667e-269">I dette scenariet kan du konfigurere systemet til automatisk å merke oppgaven som **Fullført** når samlet beløp er mindre enn 100.</span><span class="sxs-lookup"><span data-stu-id="c667e-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="c667e-270">Følg denne fremgangsmåten for å angi når systemet utfører en handling med den manuelle oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="c667e-271">I den venstre ruten klikker du **Automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="c667e-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="c667e-272">Merk av for **Aktiver automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="c667e-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="c667e-273">Klikk på **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="c667e-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="c667e-274">Angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="c667e-274">Enter a condition.</span></span>
5. <span data-ttu-id="c667e-275">Angi eventuelle ekstra betingelser som kreves.</span><span class="sxs-lookup"><span data-stu-id="c667e-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="c667e-276">Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="c667e-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="c667e-277">Klikk på **Test**.</span><span class="sxs-lookup"><span data-stu-id="c667e-277">Click **Test**.</span></span>
    2. <span data-ttu-id="c667e-278">På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post.</span><span class="sxs-lookup"><span data-stu-id="c667e-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="c667e-279">Klikk på **Test**.</span><span class="sxs-lookup"><span data-stu-id="c667e-279">Click **Test**.</span></span> <span data-ttu-id="c667e-280">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="c667e-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="c667e-281">Klikk på **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="c667e-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="c667e-282">I listen **Autofullføringshandling** velger du den handlingen som systemet skal utføre med oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c667e-283">Angi når varslinger skal sendes</span><span class="sxs-lookup"><span data-stu-id="c667e-283">Specify when notifications are sent</span></span>

<span data-ttu-id="c667e-284">Du kan sende meldinger til personer når en manuell oppgave er delegert, videresendt, fullført eller avvist, eller når det er bedt om en endring.</span><span class="sxs-lookup"><span data-stu-id="c667e-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="c667e-285">Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="c667e-286">I den venstre ruten klikker du **Varslinger**.</span><span class="sxs-lookup"><span data-stu-id="c667e-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="c667e-287">Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:</span><span class="sxs-lookup"><span data-stu-id="c667e-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="c667e-288">**Deleger** – Oppgaven er tilordnet til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="c667e-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="c667e-289">**Eskaler** – Den tilordnede brukeren har ikke fullført oppgaven innen fristen.</span><span class="sxs-lookup"><span data-stu-id="c667e-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="c667e-290">**Fullført** – Den tilordnede brukeren har fullført oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="c667e-291">**Avvis** – Den tilordnede brukeren har avvist dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="c667e-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="c667e-292">**Be om endring** – Den tilordnede brukeren har bedt om en endring i dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="c667e-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="c667e-293">Velg raden for en hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="c667e-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="c667e-294">I tekstfeltet i fanen **Varslingstekst** skriver du inn teksten i meldingen.</span><span class="sxs-lookup"><span data-stu-id="c667e-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="c667e-295">Hvis du vil tilpasse varslingen, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="c667e-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="c667e-296">Plassholdere erstattes med den riktige informasjonen når varslingen vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="c667e-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="c667e-297">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="c667e-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="c667e-298">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="c667e-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c667e-299">Klikk på **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="c667e-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c667e-300">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="c667e-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c667e-301">Klikk på **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="c667e-301">Click **Insert**.</span></span>

6. <span data-ttu-id="c667e-302">Hvis du vil legge til oversettelser av varslingen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c667e-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="c667e-303">Klikk på **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="c667e-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="c667e-304">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c667e-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c667e-305">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="c667e-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="c667e-306">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="c667e-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c667e-307">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 5.</span><span class="sxs-lookup"><span data-stu-id="c667e-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="c667e-308">Klikk på **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="c667e-308">Click **Close**.</span></span>

7. <span data-ttu-id="c667e-309">I **Mottaker**-fanen angir du hvem meldingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="c667e-310">Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 8.</span><span class="sxs-lookup"><span data-stu-id="c667e-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c667e-311">Alternativ</span><span class="sxs-lookup"><span data-stu-id="c667e-311">Option</span></span></th>
    <th><span data-ttu-id="c667e-312">Varslingsmottakere</span><span class="sxs-lookup"><span data-stu-id="c667e-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="c667e-313">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="c667e-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c667e-314">Deltaker</span><span class="sxs-lookup"><span data-stu-id="c667e-314">Participant</span></span></td>
    <td><span data-ttu-id="c667e-315">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="c667e-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-316">Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-fanen i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som meldingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c667e-317">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="c667e-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-318">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="c667e-318">Workflow user</span></span></td>
    <td><span data-ttu-id="c667e-319">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="c667e-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="c667e-320">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="c667e-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c667e-321">Bruker</span><span class="sxs-lookup"><span data-stu-id="c667e-321">User</span></span></td>
    <td><span data-ttu-id="c667e-322">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="c667e-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c667e-323">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="c667e-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c667e-324"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere.</span><span class="sxs-lookup"><span data-stu-id="c667e-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c667e-325">Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="c667e-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="c667e-326">Gjenta trinn 3 til 7 for hver hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="c667e-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="c667e-327">Angi en tidsfrist</span><span class="sxs-lookup"><span data-stu-id="c667e-327">Set a time limit</span></span>

<span data-ttu-id="c667e-328">Følg denne fremgangsmåten hvis den manuelle oppgaven må fullføres innen et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="c667e-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="c667e-329">Alternativene du velger i prosedyren, overstyrer alternativene du velger i **Tilordning**- og **Eskalering**-området på siden.</span><span class="sxs-lookup"><span data-stu-id="c667e-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="c667e-330">Klikk på **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="c667e-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="c667e-331">Merk av for **Angi en tidsgrense for arbeidsflytelementet**.</span><span class="sxs-lookup"><span data-stu-id="c667e-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="c667e-332">I **Varighet**-feltet angir du når oppgaven må være fullført.</span><span class="sxs-lookup"><span data-stu-id="c667e-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="c667e-333">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="c667e-333">Select one of the following options:</span></span>

    - <span data-ttu-id="c667e-334">**Timer** – Angi hvor mange timer det kan gå før oppgaven må være fullført.</span><span class="sxs-lookup"><span data-stu-id="c667e-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="c667e-335">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="c667e-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c667e-336">**Dager** – Angi hvor mange dager det kan gå før oppgaven må være fullført.</span><span class="sxs-lookup"><span data-stu-id="c667e-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="c667e-337">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="c667e-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c667e-338">**Uker** – Angi hvor mange uker det kan gå før oppgaven må være fullført.</span><span class="sxs-lookup"><span data-stu-id="c667e-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="c667e-339">**Måneder** – Velg dagen og uken da oppgaven må være fullført.</span><span class="sxs-lookup"><span data-stu-id="c667e-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="c667e-340">Du vil for eksempel at oppgaven skal fullføres innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="c667e-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="c667e-341">**År** – Velg dagen, uken og måneden da oppgaven må være fullført.</span><span class="sxs-lookup"><span data-stu-id="c667e-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="c667e-342">Du vil for eksempel at oppgaven skal fullføres innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="c667e-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="c667e-343">Hvis tidsgrensen overskrides, vil systemet gjøre noe med oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="c667e-344">I listen **Handling** velger du den handlingen som systemet skal utføre.</span><span class="sxs-lookup"><span data-stu-id="c667e-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="c667e-345">Angi hvilke handlinger som er tilgjengelige for brukeren</span><span class="sxs-lookup"><span data-stu-id="c667e-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="c667e-346">Når den manuelle oppgaven tilordnes en bruker, må brukeren utføre en handling med oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="c667e-347">Følg denne fremgangsmåten for å angi hvilke handlinger brukeren kan utføre med oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="c667e-348">Handlingene som er tilgjengelige, vil variere avhengig av utformingen av oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="c667e-349">Klikk på **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="c667e-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="c667e-350">Merk av for **Fullført** hvis brukeren skal kunne merke oppgaven som **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="c667e-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="c667e-351">Merk av for **Avvis** hvis brukeren skal kunne avvise dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="c667e-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="c667e-352">Merk av for **Be om endring** hvis brukeren skal kunne be om endringer av dokumentet som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="c667e-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="c667e-353">Merk av for **Deleger** hvis brukeren skal kunne tilordne oppgaven til andre brukere.</span><span class="sxs-lookup"><span data-stu-id="c667e-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="c667e-354">Merk av for **Tilordne på nytt** hvis brukeren skal kunne tilordne oppgaven på nytt til andre brukere i arbeidselementkøen.</span><span class="sxs-lookup"><span data-stu-id="c667e-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="c667e-355">Merk av for **Frigi** hvis brukeren skal kunne tilordne oppgaven på nytt til arbeidselementkøen.</span><span class="sxs-lookup"><span data-stu-id="c667e-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="c667e-356">En annen bruker kan deretter fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="c667e-356">Another user can then complete the task.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]