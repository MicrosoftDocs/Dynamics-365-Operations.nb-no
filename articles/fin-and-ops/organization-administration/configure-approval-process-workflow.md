---
title: Konfigurere godkjenningsprosesser i en arbeidsflyt
description: "Bruk fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningsprosessen."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 08641eaac31813a8bee3231118f8e2bf802ea3e1
ms.contentlocale: nb-no
ms.lasthandoff: 12/18/2018

---

# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="34833-103">Konfigurere godkjenningsprosesser i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="34833-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34833-104">Bruk fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="34833-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="34833-105">Når du skal konfigurere en godkjenningsprosess i redigeringsprogrammet for arbeidsflyt, høyreklikker du godkjenningstrinnet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="34833-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="34833-106">Gi navn til godkjenningsprosessen</span><span class="sxs-lookup"><span data-stu-id="34833-106">Name the approval process</span></span>

<span data-ttu-id="34833-107">Bruk fremgangsmåten nedenfor for å sette et navn på godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="34833-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="34833-108">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="34833-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="34833-109">I feltet **Navn** angir du et unikt navn på godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="34833-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="34833-110">Angi når systemet skal utføre en handling med dokumentet automatisk</span><span class="sxs-lookup"><span data-stu-id="34833-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="34833-111">Du kan konfigurere systemet slik at det automatisk utfører en handling på dokumenter som oppfyller bestemte betingelser.</span><span class="sxs-lookup"><span data-stu-id="34833-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="34833-112">Systemet kan for eksempel godkjenne reiseregninger med totalsummer som er mindre enn USD 100.</span><span class="sxs-lookup"><span data-stu-id="34833-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="34833-113">Følg denne fremgangsmåten for å angi når systemet utfører en handling på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="34833-114">I den venstre ruten klikker du **Automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="34833-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="34833-115">Merk av for **Aktiver automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="34833-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="34833-116">Klikk **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="34833-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="34833-117">Angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="34833-117">Enter a condition.</span></span>
5. <span data-ttu-id="34833-118">Angi flere betingelser om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="34833-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="34833-119">Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="34833-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="34833-120">Klikk **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.</span><span class="sxs-lookup"><span data-stu-id="34833-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="34833-121">Velg en post i **Valider betingelse**-området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="34833-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="34833-122">Klikk **Test**.</span><span class="sxs-lookup"><span data-stu-id="34833-122">Click **Test**.</span></span> <span data-ttu-id="34833-123">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="34833-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="34833-124">Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="34833-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="34833-125">I listen **Autofullføringshandling** velger du handlingen som systemet skal utføre på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="34833-126">Angi når varslinger skal sendes</span><span class="sxs-lookup"><span data-stu-id="34833-126">Specify when notifications are sent</span></span>

<span data-ttu-id="34833-127">Du kan sende meldinger til personer når et dokument er godkjent, avvist, delegert eller videresendt, eller når det er bedt om en endring.</span><span class="sxs-lookup"><span data-stu-id="34833-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="34833-128">Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="34833-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="34833-129">I den venstre ruten klikker du **Varslinger**.</span><span class="sxs-lookup"><span data-stu-id="34833-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="34833-130">Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:</span><span class="sxs-lookup"><span data-stu-id="34833-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="34833-131">**Representant** – Når et dokument er tilordnet til en annen bruker for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="34833-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="34833-132">**Videresend** – Når den tilordnede brukeren ikke har gjort noe på et dokument i tildelt tidsrom.</span><span class="sxs-lookup"><span data-stu-id="34833-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="34833-133">**Godkjenn** – Når et dokument er godkjent.</span><span class="sxs-lookup"><span data-stu-id="34833-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="34833-134">**Avvis** – Når et dokument er avvist.</span><span class="sxs-lookup"><span data-stu-id="34833-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="34833-135">**Be om endring** – Når den tilordnede brukeren har bedt om en endring i et dokument som ble sendt.</span><span class="sxs-lookup"><span data-stu-id="34833-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="34833-136">Velg raden for en hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="34833-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="34833-137">Klikk kategorien **Varslingstekst**.</span><span class="sxs-lookup"><span data-stu-id="34833-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="34833-138">I tekstboksen angir du teksten for varslingen.</span><span class="sxs-lookup"><span data-stu-id="34833-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="34833-139">Du kan tilpasse teksten ved å sette inn plassholdere som vil bli erstattet med de aktuelle dataene når de vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="34833-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="34833-140">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="34833-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="34833-141">Klikk i tekstboksen der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="34833-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="34833-142">Klikk **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="34833-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="34833-143">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="34833-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="34833-144">Klikk **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="34833-144">Click **Insert**.</span></span>

7. <span data-ttu-id="34833-145">Hvis du vil legge til oversettelser av varslingen, klikker du **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="34833-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="34833-146">I skjemaet som vises, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="34833-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="34833-147">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="34833-147">Click **Add**.</span></span>
    2. <span data-ttu-id="34833-148">I listen som vises, velger du språket teksten skal angis på.</span><span class="sxs-lookup"><span data-stu-id="34833-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="34833-149">I tekstboksen **Oversatt tekst** legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="34833-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="34833-150">Hvis du vil tilpasse teksten, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="34833-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="34833-151">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="34833-151">Click **Close**.</span></span>

8. <span data-ttu-id="34833-152">Klikk kategorien **Mottaker**.</span><span class="sxs-lookup"><span data-stu-id="34833-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="34833-153">Angi hvem varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="34833-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="34833-154">Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for alternativet før du går til trinn 10.</span><span class="sxs-lookup"><span data-stu-id="34833-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="34833-155">Alternativ</span><span class="sxs-lookup"><span data-stu-id="34833-155">Option</span></span></th>
    <th><span data-ttu-id="34833-156">Varslingsmottakere</span><span class="sxs-lookup"><span data-stu-id="34833-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="34833-157">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="34833-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="34833-158"><strong>Deltaker</strong></span><span class="sxs-lookup"><span data-stu-id="34833-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="34833-159">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="34833-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="34833-160">Når du har valgt <strong>Deltaker</strong>, klikker du <strong>Rollebasert</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="34833-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="34833-161">I <strong>Type deltaker</strong>-listen velger du typen gruppe eller rolle som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="34833-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="34833-162">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="34833-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="34833-163"><strong>Arbeidsflytbruker</strong></span><span class="sxs-lookup"><span data-stu-id="34833-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="34833-164">Brukere som deltar i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="34833-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="34833-165">Når du har valgt <strong>Arbeidsflytbruker</strong>, klikker du <strong>Arbeidsflytbruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="34833-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="34833-166">I <strong>Arbeidsflytbruker</strong>-listen velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="34833-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="34833-167"><strong>Bruker</strong></span><span class="sxs-lookup"><span data-stu-id="34833-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="34833-168">Bestemte Microsoft Dynamics 365 for Finance and Operations-brukere</span><span class="sxs-lookup"><span data-stu-id="34833-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="34833-169">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="34833-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="34833-170"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle Microsoft Dynamics 365 for Finance and Operations-brukere.</span><span class="sxs-lookup"><span data-stu-id="34833-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="34833-171">Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="34833-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="34833-172">Gjenta trinn 3 til 9 for hver hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="34833-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="34833-173"> Angi en endelig godkjenner</span><span class="sxs-lookup"><span data-stu-id="34833-173">Specify a final approver</span></span>

<span data-ttu-id="34833-174">Du bør tilordne en endelig godkjenner for scenarier der godkjenneren er personen som sendte dokumentet til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="34833-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="34833-175">Hvis du vil angi en endelig godkjenner, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="34833-175">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="34833-176">Klikk **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="34833-176">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="34833-177">Merk av for **Bruk siste godkjenner**.</span><span class="sxs-lookup"><span data-stu-id="34833-177">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="34833-178">Velg den brukeren som skal være den endelig godkjenneren, fra listen.</span><span class="sxs-lookup"><span data-stu-id="34833-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="34833-179">Angi en tidsfrist</span><span class="sxs-lookup"><span data-stu-id="34833-179">Set a time limit</span></span>

<span data-ttu-id="34833-180">Følg denne fremgangsmåten hvis godkjenningsprosessen må fullføres innen et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="34833-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="34833-181">Alternativene du velger her, overstyrer alternativene du valgte i områdene **Tildeling** og **Eskalering** i hvert godkjenningstrinn.</span><span class="sxs-lookup"><span data-stu-id="34833-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="34833-182">Klikk **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="34833-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="34833-183">Merk av for **Angi en tidsgrense for arbeidsflyt** **-element**.</span><span class="sxs-lookup"><span data-stu-id="34833-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="34833-184">I **Varighet**-feltet angir du når godkjenningsprosessen må være fullført.</span><span class="sxs-lookup"><span data-stu-id="34833-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="34833-185">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="34833-185">Select one of the following options:</span></span>

    - <span data-ttu-id="34833-186">**Timer** – Angi antall timer godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="34833-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="34833-187">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="34833-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="34833-188">**Dager** – Angi antall dager godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="34833-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="34833-189">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="34833-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="34833-190">**Uker** – Angi antall uker godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="34833-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="34833-191">**Måneder** – Velg dagen og uken godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="34833-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="34833-192">Det kan for eksempel hende du vil at godkjenningsprosessen skal være fullført fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="34833-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="34833-193">**År** – Velg dagen, uken og måneden godkjenningsprosessen må være fullført innen.</span><span class="sxs-lookup"><span data-stu-id="34833-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="34833-194">Det kan for eksempel hende du vil at godkjenningsprosessen skal være fullført fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="34833-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="34833-195">Hvis tidsgrensen overskrides, vil systemet gjøre noe med dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="34833-196">I listen **Handling** velger du den handlingen som systemet skal utføre.</span><span class="sxs-lookup"><span data-stu-id="34833-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="34833-197">Angi hvilke handlinger som er tilgjengelige for brukeren</span><span class="sxs-lookup"><span data-stu-id="34833-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="34833-198">Når et dokument tilordnes en bruker for godkjenning, må brukeren utføre en handling med dokument.</span><span class="sxs-lookup"><span data-stu-id="34833-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="34833-199">Følg denne fremgangsmåten for å angi hvilke handlinger brukeren kan utføre med det sendte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="34833-200">Klikk **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="34833-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="34833-201">Merk av for **Godkjenn** hvis brukeren kan godkjenne dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="34833-202">Merk av for **Avvis** hvis brukeren kan avvise dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="34833-203">Merk av for **Be om endring** hvis du brukeren kan be om endringer av dokumentet.</span><span class="sxs-lookup"><span data-stu-id="34833-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="34833-204">Merk av for **Representant** hvis brukeren kan tilordne dokumentet til en annen bruker for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="34833-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="34833-205">Avmerkingsboksen **Aktiver handlinger fra arbeidslisten i Enterprise Portal** er utgått.</span><span class="sxs-lookup"><span data-stu-id="34833-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="34833-206"> Konfigurere godkjenningstrinnene</span><span class="sxs-lookup"><span data-stu-id="34833-206">Configure the approval steps</span></span>

<span data-ttu-id="34833-207">En godkjenningsprosess består av godkjenningstrinn.</span><span class="sxs-lookup"><span data-stu-id="34833-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="34833-208">Fullfør fremgangsmåten nedenfor for å legge til trinn i godkjenningsprosessen og konfigurere trinnene.</span><span class="sxs-lookup"><span data-stu-id="34833-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="34833-209">Dobbeltklikk godkjenningsprosessen i redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="34833-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="34833-210">Redigeringsprogrammet for arbeidsflyt viser trinnene i godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="34833-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="34833-211">Hvis du vil legge til et godkjenningstrinn, kan du dra trinnet fra **Arbeidsflytelementer** området til lerretet.</span><span class="sxs-lookup"><span data-stu-id="34833-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="34833-212">Hvis du vil konfigurere et godkjenningstrinn, kan du se [Konfigurere et godkjenningstrinn](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="34833-212">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>

