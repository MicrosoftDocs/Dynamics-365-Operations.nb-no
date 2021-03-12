---
title: Konfigurere godkjenningsprosesser i en arbeidsflyt
description: Bruk fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningsprosessen.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7dc365bc2a317b67235f1ad01a4157089e0079d
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798935"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="03dcf-103">Konfigurere godkjenningsprosesser i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="03dcf-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03dcf-104">Bruk fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="03dcf-105">Når du skal konfigurere en godkjenningsprosess i redigeringsprogrammet for arbeidsflyt, høyreklikker du godkjenningstrinnet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="03dcf-106">Gi navn til godkjenningsprosessen</span><span class="sxs-lookup"><span data-stu-id="03dcf-106">Name the approval process</span></span>

<span data-ttu-id="03dcf-107">Bruk fremgangsmåten nedenfor for å sette et navn på godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="03dcf-108">Klikk på **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="03dcf-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="03dcf-109">I feltet **Navn** angir du et unikt navn på godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="03dcf-110">Angi når systemet skal utføre en handling med dokumentet automatisk</span><span class="sxs-lookup"><span data-stu-id="03dcf-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="03dcf-111">Du kan konfigurere systemet slik at det automatisk utfører en handling på dokumenter som oppfyller bestemte betingelser.</span><span class="sxs-lookup"><span data-stu-id="03dcf-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="03dcf-112">Systemet kan for eksempel godkjenne reiseregninger med totalsummer som er mindre enn USD 100.</span><span class="sxs-lookup"><span data-stu-id="03dcf-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="03dcf-113">Følg denne fremgangsmåten for å angi når systemet utfører en handling på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="03dcf-114">I den venstre ruten klikker du **Automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="03dcf-115">Merk av for **Aktiver automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="03dcf-116">Klikk på **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="03dcf-117">Angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="03dcf-117">Enter a condition.</span></span>
5. <span data-ttu-id="03dcf-118">Angi flere betingelser om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="03dcf-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="03dcf-119">Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="03dcf-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="03dcf-120">Klikk på **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="03dcf-121">Velg en post i **Valider betingelse**-området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="03dcf-122">Klikk på **Test**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-122">Click **Test**.</span></span> <span data-ttu-id="03dcf-123">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="03dcf-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="03dcf-124">Klikk på **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="03dcf-125">I listen **Autofullføringshandling** velger du handlingen som systemet skal utføre på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="03dcf-126">Angi når varslinger skal sendes</span><span class="sxs-lookup"><span data-stu-id="03dcf-126">Specify when notifications are sent</span></span>

<span data-ttu-id="03dcf-127">Du kan sende meldinger til personer når et dokument er godkjent, avvist, delegert eller videresendt, eller når det er bedt om en endring.</span><span class="sxs-lookup"><span data-stu-id="03dcf-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="03dcf-128">Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="03dcf-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="03dcf-129">I den venstre ruten klikker du **Varslinger**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="03dcf-130">Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:</span><span class="sxs-lookup"><span data-stu-id="03dcf-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="03dcf-131">**Representant** – Når et dokument er tilordnet til en annen bruker for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="03dcf-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="03dcf-132">**Videresend** – Når den tilordnede brukeren ikke har gjort noe på et dokument i tildelt tidsrom.</span><span class="sxs-lookup"><span data-stu-id="03dcf-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="03dcf-133">**Godkjenn** – Når et dokument er godkjent.</span><span class="sxs-lookup"><span data-stu-id="03dcf-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="03dcf-134">**Avvis** – Når et dokument er avvist.</span><span class="sxs-lookup"><span data-stu-id="03dcf-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="03dcf-135">**Be om endring** – Når den tilordnede brukeren har bedt om en endring i et dokument som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="03dcf-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="03dcf-136">Velg raden for en hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="03dcf-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="03dcf-137">Klikk på fanen **Varslingstekst**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="03dcf-138">I tekstboksen angir du teksten for varslingen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="03dcf-139">Du kan tilpasse teksten ved å sette inn plassholdere som vil bli erstattet med de aktuelle dataene når de vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="03dcf-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="03dcf-140">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="03dcf-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="03dcf-141">Klikk på i tekstboksen der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="03dcf-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="03dcf-142">Klikk på **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="03dcf-143">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="03dcf-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="03dcf-144">Klikk på **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-144">Click **Insert**.</span></span>

7. <span data-ttu-id="03dcf-145">Hvis du vil legge til oversettelser av varslingen, klikker du **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="03dcf-146">I skjemaet som vises, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="03dcf-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="03dcf-147">Klikk på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-147">Click **Add**.</span></span>
    2. <span data-ttu-id="03dcf-148">I listen som vises, velger du språket teksten skal angis på.</span><span class="sxs-lookup"><span data-stu-id="03dcf-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="03dcf-149">I tekstboksen **Oversatt tekst** legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="03dcf-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="03dcf-150">Hvis du vil tilpasse teksten, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="03dcf-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="03dcf-151">Klikk på **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-151">Click **Close**.</span></span>

8. <span data-ttu-id="03dcf-152">Klikk på fanen **Mottaker**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="03dcf-153">Angi hvem varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="03dcf-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="03dcf-154">Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for alternativet før du går til trinn 10.</span><span class="sxs-lookup"><span data-stu-id="03dcf-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="03dcf-155">Alternativ</span><span class="sxs-lookup"><span data-stu-id="03dcf-155">Option</span></span></th>
    <th><span data-ttu-id="03dcf-156">Varslingsmottakere</span><span class="sxs-lookup"><span data-stu-id="03dcf-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="03dcf-157">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="03dcf-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="03dcf-158"><strong>Deltaker</strong></span><span class="sxs-lookup"><span data-stu-id="03dcf-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="03dcf-159">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="03dcf-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dcf-160">Når du har valgt <strong>Deltaker</strong>, klikker du <strong>Rollebasert</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dcf-161">I <strong>Type deltaker</strong>-listen velger du typen gruppe eller rolle som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="03dcf-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="03dcf-162">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="03dcf-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dcf-163"><strong>Arbeidsflytbruker</strong></span><span class="sxs-lookup"><span data-stu-id="03dcf-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="03dcf-164">Brukere som deltar i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="03dcf-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dcf-165">Når du har valgt <strong>Arbeidsflytbruker</strong>, klikker du <strong>Arbeidsflytbruker</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dcf-166">I <strong>Arbeidsflytbruker</strong>-listen velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="03dcf-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dcf-167"><strong>Bruker</strong></span><span class="sxs-lookup"><span data-stu-id="03dcf-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="03dcf-168">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="03dcf-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dcf-169">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dcf-170">Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="03dcf-171">Gjenta trinn 3 til 9 for hver hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="03dcf-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="03dcf-172"> Angi en endelig godkjenner</span><span class="sxs-lookup"><span data-stu-id="03dcf-172">Specify a final approver</span></span>

<span data-ttu-id="03dcf-173">Du kan angi en endelig godkjenner for scenarier der godkjenneren er personen som sendte dokumentet til godkjenning, og Sperr godkjenning av innsender brukes.</span><span class="sxs-lookup"><span data-stu-id="03dcf-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="03dcf-174">Hvis du vil angi en endelig godkjenner, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="03dcf-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="03dcf-175">I redigeringsprogrammet for arbeidsflyt høyreklikker du godkjenningselementet og velger deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="03dcf-176">Klikk på **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="03dcf-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="03dcf-177">Merk av for **Bruk siste godkjenner**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="03dcf-178">Velg en bruker som skal være den endelig godkjenneren, fra listen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="03dcf-179">Angi en tidsfrist</span><span class="sxs-lookup"><span data-stu-id="03dcf-179">Set a time limit</span></span>

<span data-ttu-id="03dcf-180">Følg denne fremgangsmåten hvis godkjenningsprosessen må fullføres innen et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="03dcf-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="03dcf-181">Alternativene du velger her, overstyrer alternativene du valgte i områdene **Tildeling** og **Eskalering** i hvert godkjenningstrinn.</span><span class="sxs-lookup"><span data-stu-id="03dcf-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="03dcf-182">Klikk på **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="03dcf-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="03dcf-183">Merk av for **Angi en tidsgrense for arbeidsflyt** **-element**.</span><span class="sxs-lookup"><span data-stu-id="03dcf-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="03dcf-184">I **Varighet**-feltet angir du når godkjenningsprosessen må være fullført.</span><span class="sxs-lookup"><span data-stu-id="03dcf-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="03dcf-185">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="03dcf-185">Select one of the following options:</span></span>

    - <span data-ttu-id="03dcf-186">**Timer** – Angi antall timer godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="03dcf-187">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="03dcf-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dcf-188">**Dager** – Angi antall dager godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="03dcf-189">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="03dcf-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dcf-190">**Uker** – Angi antall uker godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="03dcf-191">**Måneder** – Velg dagen og uken godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="03dcf-192">Det kan for eksempel hende du vil at godkjenningsprosessen skal være fullført fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="03dcf-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="03dcf-193">**År** – Velg dagen, uken og måneden godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="03dcf-194">Det kan for eksempel hende du vil at godkjenningsprosessen skal være fullført fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="03dcf-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="03dcf-195">Hvis tidsgrensen overskrides, vil systemet gjøre noe med dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="03dcf-196">I listen **Handling** velger du den handlingen som systemet skal utføre.</span><span class="sxs-lookup"><span data-stu-id="03dcf-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="03dcf-197">Angi hvilke handlinger som er tilgjengelige for brukeren</span><span class="sxs-lookup"><span data-stu-id="03dcf-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="03dcf-198">Når et dokument tilordnes en bruker for godkjenning, må brukeren utføre en handling med dokument.</span><span class="sxs-lookup"><span data-stu-id="03dcf-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="03dcf-199">Følg denne fremgangsmåten for å angi hvilke handlinger brukeren kan utføre med det sendte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="03dcf-200">Klikk på **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="03dcf-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="03dcf-201">Merk av for **Godkjenn** hvis brukeren kan godkjenne dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="03dcf-202">Merk av for **Avvis** hvis brukeren kan avvise dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="03dcf-203">Merk av for **Be om endring** hvis du brukeren kan be om endringer av dokumentet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="03dcf-204">Merk av for **Representant** hvis brukeren kan tilordne dokumentet til en annen bruker for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="03dcf-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="03dcf-205">Avmerkingsboksen **Aktiver handlinger fra arbeidslisten i Enterprise Portal** er utgått.</span><span class="sxs-lookup"><span data-stu-id="03dcf-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="03dcf-206"> Konfigurere godkjenningstrinnene</span><span class="sxs-lookup"><span data-stu-id="03dcf-206">Configure the approval steps</span></span>

<span data-ttu-id="03dcf-207">En godkjenningsprosess består av godkjenningstrinn.</span><span class="sxs-lookup"><span data-stu-id="03dcf-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="03dcf-208">Fullfør fremgangsmåten nedenfor for å legge til trinn i godkjenningsprosessen og konfigurere trinnene.</span><span class="sxs-lookup"><span data-stu-id="03dcf-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="03dcf-209">Dobbeltklikk godkjenningsprosessen i redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="03dcf-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="03dcf-210">Redigeringsprogrammet for arbeidsflyt viser trinnene i godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="03dcf-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="03dcf-211">Hvis du vil legge til et godkjenningstrinn, kan du dra trinnet fra **Arbeidsflytelementer** området til lerretet.</span><span class="sxs-lookup"><span data-stu-id="03dcf-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="03dcf-212">Hvis du vil konfigurere et godkjenningstrinn, kan du se [Konfigurere godkjenningstrinn i en arbeidsflyt](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="03dcf-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>
