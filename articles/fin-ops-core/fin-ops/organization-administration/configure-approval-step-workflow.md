---
title: Konfigurere godkjenningstrinn i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene for et godkjenningstrinn.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69035be84d489d6ea2342c6974cfa9a31531f1c7
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698077"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="f6731-103">Konfigurere godkjenningstrinn i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="f6731-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6731-104">Dette emnet forklarer hvordan du konfigurerer egenskapene for et godkjenningstrinn.</span><span class="sxs-lookup"><span data-stu-id="f6731-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="f6731-105">Når du skal konfigurere et godkjenningstrinn i redigeringsprogrammet for arbeidsflyt, høyreklikker du godkjenningstrinnet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="f6731-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f6731-106">Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="f6731-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="f6731-107">Gi navn til trinnet</span><span class="sxs-lookup"><span data-stu-id="f6731-107">Name the step</span></span>
<span data-ttu-id="f6731-108">Følg denne fremgangsmåten for å sette et navn på godkjenningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="f6731-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="f6731-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="f6731-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f6731-110">I feltet **Navn** angir du et unikt navn på godkjenningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="f6731-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="f6731-111">Legg inn en emnelinje og instruksjoner</span><span class="sxs-lookup"><span data-stu-id="f6731-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="f6731-112">Du må skrive inn en emnelinje og instruksjoner til brukeren som er knyttet til godkjenningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="f6731-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="f6731-113">Hvis du for eksempel konfigurerer et godkjenningstrinn for innkjøpsrekvisisjoner, ser brukeren som er tilordnet til trinnet, emnelinjen og instruksjonene på **Innkjøpsrekvisisjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="f6731-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="f6731-114">Emnelinjen vises i en meldingslinje øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="f6731-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="f6731-115">Brukeren kan deretter klikke ikonet i meldingslinjen for å vise instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="f6731-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="f6731-116">Følg trinnene nedenfor for å legge inn en emnelinje og instruksjoner.</span><span class="sxs-lookup"><span data-stu-id="f6731-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="f6731-117">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="f6731-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f6731-118">I **Emne for arbeidselement**-feltet angir du emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="f6731-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="f6731-119">Hvis du vil tilpasse emnelinjen, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="f6731-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="f6731-120">Plassholdere erstattes med de riktige dataene når emnelinjen vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="f6731-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="f6731-121">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="f6731-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="f6731-122">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="f6731-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f6731-123">Klikk **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="f6731-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f6731-124">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="f6731-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f6731-125">Klikk **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="f6731-125">Click **Insert**.</span></span>

4. <span data-ttu-id="f6731-126">Hvis du vil legge til oversettelser av emnelinjen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f6731-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="f6731-127">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="f6731-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="f6731-128">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f6731-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f6731-129">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="f6731-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="f6731-130">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="f6731-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f6731-131">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="f6731-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="f6731-132">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="f6731-132">Click **Close**.</span></span>

5. <span data-ttu-id="f6731-133">I **Instruksjoner for arbeidselement**-feltet angir du instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="f6731-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="f6731-134">Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="f6731-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="f6731-135">Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="f6731-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="f6731-136">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="f6731-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="f6731-137">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="f6731-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f6731-138">Klikk **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="f6731-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f6731-139">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="f6731-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f6731-140">Klikk **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="f6731-140">Click **Insert**.</span></span>

7. <span data-ttu-id="f6731-141">Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f6731-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="f6731-142">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="f6731-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="f6731-143">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f6731-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f6731-144">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="f6731-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="f6731-145">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="f6731-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f6731-146">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 6.</span><span class="sxs-lookup"><span data-stu-id="f6731-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="f6731-147">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="f6731-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="f6731-148">Tildele godkjenningstrinnet</span><span class="sxs-lookup"><span data-stu-id="f6731-148">Assign the approval step</span></span>

<span data-ttu-id="f6731-149">Følg denne fremgangsmåten for å angi hvem godkjenningstrinnet skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="f6731-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="f6731-150">I den venstre ruten klikker du **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="f6731-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="f6731-151">I **Tilordningstype**-kategorien velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 3.</span><span class="sxs-lookup"><span data-stu-id="f6731-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f6731-152">Alternativ</span><span class="sxs-lookup"><span data-stu-id="f6731-152">Option</span></span></th>
    <th><span data-ttu-id="f6731-153">Brukere som godkjenningstrinnet er tilordnet til</span><span class="sxs-lookup"><span data-stu-id="f6731-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="f6731-154">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="f6731-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f6731-155">Deltaker</span><span class="sxs-lookup"><span data-stu-id="f6731-155">Participant</span></span></td>
    <td><span data-ttu-id="f6731-156">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="f6731-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f6731-157">Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-kategorien i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som trinnet skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="f6731-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="f6731-158">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som trinnet skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="f6731-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f6731-159">Hierarki</span><span class="sxs-lookup"><span data-stu-id="f6731-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="f6731-160">Brukere i et bestemt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f6731-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f6731-161">Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som trinnet skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="f6731-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="f6731-162">Systemet må hente et område med brukernavn fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f6731-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="f6731-163">Disse navnene representerer brukere som trinnet kan tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="f6731-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="f6731-164">Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="f6731-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="f6731-165">Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</span><span class="sxs-lookup"><span data-stu-id="f6731-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="f6731-166">Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="f6731-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="f6731-167">Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</span><span class="sxs-lookup"><span data-stu-id="f6731-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="f6731-168">I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som trinnet skal tilordnes til:</span><span class="sxs-lookup"><span data-stu-id="f6731-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="f6731-169"><strong>Tilordne til alle hentede brukere</strong> – Trinnet tilordnes til alle brukere i området.</span><span class="sxs-lookup"><span data-stu-id="f6731-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="f6731-170"><strong>Bare tilordne til den siste hentede brukeren</strong> – Trinnet tilordnes bare til den siste brukeren i området.</span><span class="sxs-lookup"><span data-stu-id="f6731-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="f6731-171"><strong>Utelat brukere med følgende vilkår</strong> – Trinnet tilordnes ikke til noen brukere i området som oppfyller et bestemt vilkår.</span><span class="sxs-lookup"><span data-stu-id="f6731-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="f6731-172">Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</span><span class="sxs-lookup"><span data-stu-id="f6731-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f6731-173">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="f6731-173">Workflow user</span></span></td>
    <td><span data-ttu-id="f6731-174">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="f6731-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="f6731-175">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="f6731-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f6731-176">Bruker</span><span class="sxs-lookup"><span data-stu-id="f6731-176">User</span></span></td>
    <td><span data-ttu-id="f6731-177">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="f6731-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f6731-178">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="f6731-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f6731-179"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle systembrukere.</span><span class="sxs-lookup"><span data-stu-id="f6731-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="f6731-180">Velg brukerne du vil tilordne trinnet til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="f6731-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="f6731-181">I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å utføre handlinger på eller svare på dokumenter som kommer til godkjenningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="f6731-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="f6731-182">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="f6731-182">Select one of the following options:</span></span>

    - <span data-ttu-id="f6731-183">**Timer** – Angi antallet timer som brukeren har til å svare.</span><span class="sxs-lookup"><span data-stu-id="f6731-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="f6731-184">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="f6731-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f6731-185">**Dager** – Angi antallet dager som brukeren har til å svare.</span><span class="sxs-lookup"><span data-stu-id="f6731-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="f6731-186">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="f6731-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f6731-187">**Uker** – Angi antallet uker som brukeren har til å svare.</span><span class="sxs-lookup"><span data-stu-id="f6731-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="f6731-188">**Måneder** – Velg dagen og uken som brukeren må svare innen.</span><span class="sxs-lookup"><span data-stu-id="f6731-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="f6731-189">Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="f6731-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="f6731-190">**År** – Velg dagen, uken og måneden som brukeren må svare innen.</span><span class="sxs-lookup"><span data-stu-id="f6731-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="f6731-191">Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="f6731-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="f6731-192">Hvis brukeren ikke gjør noe med dokumentet innenfor den tillatte tiden, er dokumentet forfalt.</span><span class="sxs-lookup"><span data-stu-id="f6731-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="f6731-193">Et dokument som er forfalt, videresendes, basert på alternativene du velger i **Eskalering**-området på siden.</span><span class="sxs-lookup"><span data-stu-id="f6731-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="f6731-194">Hvis du har tilordnet godkjenningstrinnet til flere brukere eller en gruppe brukere i **Fullføringspolicy**-kategorien, velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="f6731-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="f6731-195">**Én enkelt godkjenner** – Handlingen som utføres på dokumentet, bestemmes av den første personen som svarer.</span><span class="sxs-lookup"><span data-stu-id="f6731-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="f6731-196">Erik har for eksempel sendt en reiseregning på NOK 15 000.</span><span class="sxs-lookup"><span data-stu-id="f6731-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="f6731-197">Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn.</span><span class="sxs-lookup"><span data-stu-id="f6731-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="f6731-198">Hvis Jorunn er den første personen som svarer på dokumentet, brukes handlingen hun bestemmer seg for, på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6731-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="f6731-199">Hvis Jorunn avviser dokumentet, avvises det og sendes tilbake til Erik.</span><span class="sxs-lookup"><span data-stu-id="f6731-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="f6731-200">Hvis Jorunn godkjenner dokumentet, sendes det til Karen for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f6731-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Arbeidsflyt som har en godkjenningsprosess](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="f6731-202">**Flertallet av godkjennere** – Handlingen som skal brukes på dokumentet, fastsettes når de fleste av godkjennerne svarer.</span><span class="sxs-lookup"><span data-stu-id="f6731-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="f6731-203">Erik har for eksempel sendt en reiseregning på NOK 15 000.</span><span class="sxs-lookup"><span data-stu-id="f6731-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="f6731-204">Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn.</span><span class="sxs-lookup"><span data-stu-id="f6731-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="f6731-205">Hvis Jorunn og Johanne er de første to godkjennerne som svarer, utføres handlingen de gjør, på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6731-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="f6731-206">Hvis Jorunn godkjenner dokumentet, men Johanne avviser det, avvises dokumentet og det sendes tilbake til Erik.</span><span class="sxs-lookup"><span data-stu-id="f6731-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="f6731-207">Hvis både Jorunn og Johanne godkjenner dokumentet, sendes det til Karen til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f6731-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="f6731-208">**Prosent av godkjennere** – Handlingen som brukes på dokumentet, bestemmes når en bestemt prosent av godkjennerne svarer.</span><span class="sxs-lookup"><span data-stu-id="f6731-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="f6731-209">Erik har for eksempel sendt en reiseregning på NOK 15 000.</span><span class="sxs-lookup"><span data-stu-id="f6731-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="f6731-210">Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn, og du har angitt **50** som prosent.</span><span class="sxs-lookup"><span data-stu-id="f6731-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="f6731-211">Hvis Jorunn og Johanne er de første to godkjennerne som svarer, brukes handlingen som de gjør, på dokumentet fordi de oppfyller kravene til 50 prosent av godkjennere.</span><span class="sxs-lookup"><span data-stu-id="f6731-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="f6731-212">Hvis Jorunn godkjenner dokumentet, men Johanne avviser det, avvises dokumentet og det sendes tilbake til Erik.</span><span class="sxs-lookup"><span data-stu-id="f6731-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="f6731-213">Hvis både Jorunn og Johanne godkjenner dokumentet, sendes det til Karen til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f6731-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="f6731-214">**Alle godkjennere** – Alle godkjennerne må godkjenne dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6731-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="f6731-215">Ellers kan ikke arbeidsflyten fortsette.</span><span class="sxs-lookup"><span data-stu-id="f6731-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="f6731-216">Erik har for eksempel sendt en reiseregning på NOK 15 000.</span><span class="sxs-lookup"><span data-stu-id="f6731-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="f6731-217">Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn.</span><span class="sxs-lookup"><span data-stu-id="f6731-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="f6731-218">Hvis Jorunn og Johanne godkjenner dokumentet, men Bjørn avviser det, avvises dokumentet og det sendes tilbake til Erik.</span><span class="sxs-lookup"><span data-stu-id="f6731-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="f6731-219">Hvis Jorunn, Johanne og Bjørn godkjenner dokumentet, sendes det til Karen til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f6731-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="f6731-220">Angi når godkjenningstrinnet er nødvendig</span><span class="sxs-lookup"><span data-stu-id="f6731-220">Specify when the approval step is required</span></span>

<span data-ttu-id="f6731-221">Du kan angi når godkjenningstrinnet er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f6731-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="f6731-222">Godkjenningstrinnet kan alltid være nødvendig, eller det kan bare være nødvendig hvis bestemte betingelser er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="f6731-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="f6731-223">Godkjenningstrinnet er alltid nødvendig</span><span class="sxs-lookup"><span data-stu-id="f6731-223">The approval step is always required</span></span>

<span data-ttu-id="f6731-224">Følg disse trinnene hvis godkjenningstrinnet alltid er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f6731-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="f6731-225">I den venstre ruten klikker du **Betingelse**.</span><span class="sxs-lookup"><span data-stu-id="f6731-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="f6731-226">Velg alternativet **Kjør alltid dette trinnet**.</span><span class="sxs-lookup"><span data-stu-id="f6731-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="f6731-227">Godkjenningstrinnet er nødvendig ved bestemte betingelser</span><span class="sxs-lookup"><span data-stu-id="f6731-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="f6731-228">Godkjenningstrinnet du konfigurerer, kan være nødvendig bare hvis bestemte betingelser er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="f6731-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="f6731-229">Hvis du for eksempel konfigurerer et godkjenningstrinn for en arbeidsflyt for innkjøpsrekvisisjon, vil du at godkjenningstrinnet bare skal forekomme hvis beløpet i innkjøpsrekvisisjonen er mer enn NOK 10 000.</span><span class="sxs-lookup"><span data-stu-id="f6731-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="f6731-230">Følg disse trinnene for å angi når godkjenningstrinnet er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f6731-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="f6731-231">I den venstre ruten klikker du **Betingelse**.</span><span class="sxs-lookup"><span data-stu-id="f6731-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="f6731-232">Velg alternativet **Kjør bare dette trinnet når følgende betingelse er oppfylt**.</span><span class="sxs-lookup"><span data-stu-id="f6731-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="f6731-233">Angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="f6731-233">Enter a condition.</span></span>
4. <span data-ttu-id="f6731-234">Angi eventuelle ekstra betingelser som kreves.</span><span class="sxs-lookup"><span data-stu-id="f6731-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="f6731-235">Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="f6731-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="f6731-236">Klikk **Test**.</span><span class="sxs-lookup"><span data-stu-id="f6731-236">Click **Test**.</span></span>
    2. <span data-ttu-id="f6731-237">På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post.</span><span class="sxs-lookup"><span data-stu-id="f6731-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="f6731-238">Klikk **Test**.</span><span class="sxs-lookup"><span data-stu-id="f6731-238">Click **Test**.</span></span> <span data-ttu-id="f6731-239">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="f6731-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="f6731-240">Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="f6731-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="f6731-241">Angi hva som skjer når dokumentet er forfalt</span><span class="sxs-lookup"><span data-stu-id="f6731-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="f6731-242">Hvis en bruker ikke gjør noe med et dokument innenfor den tillatte tiden, er dokumentet forfalt.</span><span class="sxs-lookup"><span data-stu-id="f6731-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="f6731-243">Et dokument som er forfalt, kan videresendes eller tilordnes automatisk til en annen bruker for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f6731-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="f6731-244">Følg denne fremgangsmåten for å videresende dokumentet hvis det er forfalt.</span><span class="sxs-lookup"><span data-stu-id="f6731-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="f6731-245">I den venstre ruten klikker du **Eskalering**.</span><span class="sxs-lookup"><span data-stu-id="f6731-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="f6731-246">Merk av for **Bruk videresendingsbane** hvis du vil opprette en videresendingsbane.</span><span class="sxs-lookup"><span data-stu-id="f6731-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="f6731-247">Systemet tilordner automatisk dokumentet til brukerne som er oppført i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="f6731-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="f6731-248">Tabellen nedenfor er et eksempel på en videresendingsbane.</span><span class="sxs-lookup"><span data-stu-id="f6731-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="f6731-249">Sekvens</span><span class="sxs-lookup"><span data-stu-id="f6731-249">Sequence</span></span> | <span data-ttu-id="f6731-250">Videresendingsbane</span><span class="sxs-lookup"><span data-stu-id="f6731-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="f6731-251">1</span><span class="sxs-lookup"><span data-stu-id="f6731-251">1</span></span>        | <span data-ttu-id="f6731-252">Tilordne til: Doris</span><span class="sxs-lookup"><span data-stu-id="f6731-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="f6731-253">2</span><span class="sxs-lookup"><span data-stu-id="f6731-253">2</span></span>        | <span data-ttu-id="f6731-254">Tilordne til: Elin</span><span class="sxs-lookup"><span data-stu-id="f6731-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="f6731-255">3</span><span class="sxs-lookup"><span data-stu-id="f6731-255">3</span></span>        | <span data-ttu-id="f6731-256">Endelig handling: Avvis</span><span class="sxs-lookup"><span data-stu-id="f6731-256">Final action: Reject</span></span> |

    <span data-ttu-id="f6731-257">I dette eksempelet tilordnes det forfalte dokumentet til Doris.</span><span class="sxs-lookup"><span data-stu-id="f6731-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="f6731-258">Hvis Doris ikke svarer innenfor det tillatte tidsrommet, tilordnes dokumentet til Elin.</span><span class="sxs-lookup"><span data-stu-id="f6731-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="f6731-259">Hvis Elin ikke svarer innenfor det tillatte tidsrommet, avvises dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6731-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="f6731-260">Klikk **Legg til videresending** for å legge til en bruker i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="f6731-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="f6731-261">I **Tilordningstype**-kategorien velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 4.</span><span class="sxs-lookup"><span data-stu-id="f6731-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f6731-262">Alternativ</span><span class="sxs-lookup"><span data-stu-id="f6731-262">Option</span></span></th>
    <th><span data-ttu-id="f6731-263">Brukere som dokumentet videresendes til</span><span class="sxs-lookup"><span data-stu-id="f6731-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="f6731-264">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="f6731-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f6731-265">Hierarki</span><span class="sxs-lookup"><span data-stu-id="f6731-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="f6731-266">Brukere i et bestemt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f6731-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f6731-267">Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som dokumentet videresendes til.</span><span class="sxs-lookup"><span data-stu-id="f6731-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="f6731-268">Systemet må hente et område med brukernavn fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f6731-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="f6731-269">Disse navnene representerer brukere som dokumentet kan videresendes til.</span><span class="sxs-lookup"><span data-stu-id="f6731-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="f6731-270">Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="f6731-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="f6731-271">Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</span><span class="sxs-lookup"><span data-stu-id="f6731-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="f6731-272">Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="f6731-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="f6731-273">Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</span><span class="sxs-lookup"><span data-stu-id="f6731-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="f6731-274">I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som dokumentet skal videresendes til:</span><span class="sxs-lookup"><span data-stu-id="f6731-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="f6731-275"><strong>Tilordne til alle hentede brukere</strong> – Dokumentet videresendes til alle brukere i området.</span><span class="sxs-lookup"><span data-stu-id="f6731-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="f6731-276"><strong>Bare tilordne til den siste hentede brukeren</strong> – Dokumentet videresendes bare til den siste brukeren i området.</span><span class="sxs-lookup"><span data-stu-id="f6731-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="f6731-277"><strong>Utelat brukere med følgende vilkår</strong> – Dokumentet videresendes ikke til noen brukere i området som oppfyller et bestemt vilkår.</span><span class="sxs-lookup"><span data-stu-id="f6731-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="f6731-278">Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</span><span class="sxs-lookup"><span data-stu-id="f6731-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f6731-279">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="f6731-279">Workflow user</span></span></td>
    <td><span data-ttu-id="f6731-280">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="f6731-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="f6731-281">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="f6731-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f6731-282">Bruker</span><span class="sxs-lookup"><span data-stu-id="f6731-282">User</span></span></td>
    <td><span data-ttu-id="f6731-283">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="f6731-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f6731-284">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="f6731-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f6731-285"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere.</span><span class="sxs-lookup"><span data-stu-id="f6731-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f6731-286">Velg brukerne du vil videresende dokumentet til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="f6731-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="f6731-287">I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å utføre handlinger på eller svare på dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f6731-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="f6731-288">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="f6731-288">Select one of the following options:</span></span>

    - <span data-ttu-id="f6731-289">**Timer** – Angi antallet timer som brukeren har til å svare.</span><span class="sxs-lookup"><span data-stu-id="f6731-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="f6731-290">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="f6731-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f6731-291">**Dager** – Angi antallet dager som brukeren har til å svare.</span><span class="sxs-lookup"><span data-stu-id="f6731-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="f6731-292">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="f6731-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f6731-293">**Uker** – Angi antallet uker som brukeren har til å svare.</span><span class="sxs-lookup"><span data-stu-id="f6731-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="f6731-294">**Måneder** – Velg dagen og uken som brukeren må svare innen.</span><span class="sxs-lookup"><span data-stu-id="f6731-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="f6731-295">Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="f6731-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="f6731-296">**År** – Velg dagen, uken og måneden som brukeren må svare innen.</span><span class="sxs-lookup"><span data-stu-id="f6731-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="f6731-297">Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="f6731-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="f6731-298">Gjenta trinn 3 og 4 for hver bruker som skal legges til i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="f6731-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="f6731-299">Du kan endre rekkefølgen på brukerne.</span><span class="sxs-lookup"><span data-stu-id="f6731-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="f6731-300">Hvis brukerne i videresendingsbanen ikke svarer innen tidsfristen, vil systemet automatisk utføre en handling med dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6731-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="f6731-301">Hvis du vil angi handlingen systemet skal utføre, merker du **Handling**-raden, og velger deretter en handling i kategorien **Avslutt handling**.</span><span class="sxs-lookup"><span data-stu-id="f6731-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
