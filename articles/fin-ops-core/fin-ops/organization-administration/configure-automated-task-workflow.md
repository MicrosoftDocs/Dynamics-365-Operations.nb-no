---
title: Konfigurere automatiserte oppgaver i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene for en automatisert oppgave.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f02b128036ebc0bd8789ecafd1e72e26fe31436
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747961"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="8dcd2-103">Konfigurere automatiserte oppgaver i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="8dcd2-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8dcd2-104">Dette emnet forklarer hvordan du konfigurerer egenskapene for en automatisert oppgave.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="8dcd2-105">Når du skal konfigurere en automatisert oppgave i redigeringsprogrammet for arbeidsflyt, høyreklikker du oppgaven og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8dcd2-106">Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for den automatiserte oppgaven.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="8dcd2-107">Gi navn til oppgaven</span><span class="sxs-lookup"><span data-stu-id="8dcd2-107">Name the task</span></span>

<span data-ttu-id="8dcd2-108">Følg denne fremgangsmåten for å sette et navn på den automatiserte oppgaven.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="8dcd2-109">Klikk på **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8dcd2-110">I feltet **Navn** angir du et unikt navn på oppgaven.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="8dcd2-111">Angi når varslinger skal sendes</span><span class="sxs-lookup"><span data-stu-id="8dcd2-111">Specify when notifications are sent</span></span>

<span data-ttu-id="8dcd2-112">Du kan sende meldinger til personer når en automatisert oppgave er kjørt eller avbrutt.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="8dcd2-113">Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="8dcd2-114">I den venstre ruten klikker du **Varslinger**.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="8dcd2-115">Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:</span><span class="sxs-lookup"><span data-stu-id="8dcd2-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="8dcd2-116">**Utførelse** – Meldinger blir sendt når oppgaven er kjørt.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="8dcd2-117">**Avbrutt** – Meldinger blir sendt når oppgaven er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="8dcd2-118">Velg raden for en hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="8dcd2-119">I tekstfeltet i fanen **Varslingstekst** skriver du inn teksten i meldingen.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="8dcd2-120">Hvis du vil tilpasse varslingen, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="8dcd2-121">Plassholdere erstattes med de riktige dataene når varslingen vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="8dcd2-122">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="8dcd2-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8dcd2-123">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8dcd2-124">Klikk på **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8dcd2-125">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8dcd2-126">Klikk på **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-126">Click **Insert**.</span></span>

6. <span data-ttu-id="8dcd2-127">Hvis du vil legge til oversettelser av varslingen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="8dcd2-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="8dcd2-128">Klikk på **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="8dcd2-129">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8dcd2-130">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8dcd2-131">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8dcd2-132">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 5.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="8dcd2-133">Klikk på **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-133">Click **Close**.</span></span>

7. <span data-ttu-id="8dcd2-134">I **Mottaker**-fanen angir du hvem meldingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="8dcd2-135">Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 8.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8dcd2-136">Alternativ</span><span class="sxs-lookup"><span data-stu-id="8dcd2-136">Option</span></span></th>
    <th><span data-ttu-id="8dcd2-137">Varslingsmottakere</span><span class="sxs-lookup"><span data-stu-id="8dcd2-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="8dcd2-138">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="8dcd2-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8dcd2-139">Deltaker</span><span class="sxs-lookup"><span data-stu-id="8dcd2-139">Participant</span></span></td>
    <td><span data-ttu-id="8dcd2-140">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="8dcd2-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8dcd2-141">Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-fanen i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som meldingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="8dcd2-142">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8dcd2-143">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="8dcd2-143">Workflow user</span></span></td>
    <td><span data-ttu-id="8dcd2-144">Brukere som deltar i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="8dcd2-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8dcd2-145">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8dcd2-146">Bruker</span><span class="sxs-lookup"><span data-stu-id="8dcd2-146">User</span></span></td>
    <td><span data-ttu-id="8dcd2-147">Bestemte brukere</span><span class="sxs-lookup"><span data-stu-id="8dcd2-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8dcd2-148">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8dcd2-149"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8dcd2-150">Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="8dcd2-151">Gjenta trinn 3 til 7 for hver hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="8dcd2-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]