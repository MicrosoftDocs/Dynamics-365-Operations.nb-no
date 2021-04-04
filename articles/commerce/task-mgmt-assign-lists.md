---
title: Tilordne oppgavelister til butikker eller ansatte
description: Dette emnet beskriver hvordan du tilordner oppgavelister til butikker eller ansatte i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3d249809f15b50c59620d69a901a427dc3ecb2f0
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477590"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="74b55-103">Tilordne oppgavelister til butikker eller ansatte</span><span class="sxs-lookup"><span data-stu-id="74b55-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74b55-104">Dette emnet beskriver hvordan du tilordner oppgavelister til butikker eller ansatte i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74b55-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="74b55-105">Ved hjelp av oppgavebehandling i Dynamics 365 Commerce kan du tilordne en oppgaveliste til flere butikker eller ansatte, eller til en kombinasjon av butikker og ansatte.</span><span class="sxs-lookup"><span data-stu-id="74b55-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="74b55-106">Det kan for eksempel hende at en regional leder for 20 butikker vil tilordne oppgavelisten **Forberedelser for høytiden** til alle de 20 butikkene.</span><span class="sxs-lookup"><span data-stu-id="74b55-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="74b55-107">Starte tilordningsprosessen for oppgaveliste</span><span class="sxs-lookup"><span data-stu-id="74b55-107">Start the task list assignment process</span></span>

<span data-ttu-id="74b55-108">Følg denne fremgangs måten for å starte prosessen med å tilordne en oppgaveliste.</span><span class="sxs-lookup"><span data-stu-id="74b55-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="74b55-109">Gå til **Retail og Commerce \> Oppgavebehandling \> Administrasjon av oppgavebehandling**.</span><span class="sxs-lookup"><span data-stu-id="74b55-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="74b55-110">Velg oppgavelisten du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="74b55-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="74b55-111">Velg **Start prosess**.</span><span class="sxs-lookup"><span data-stu-id="74b55-111">Select **Start process**.</span></span>
1. <span data-ttu-id="74b55-112">I dialogboksen **Start prosess**, i kategorien **Generelt**, i feltet **Prosessnavn** angir du et navn (for eksempel **Butikker i østlige region**).</span><span class="sxs-lookup"><span data-stu-id="74b55-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="74b55-113">I **Måldato**-feltet angir du en dato.</span><span class="sxs-lookup"><span data-stu-id="74b55-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="74b55-114">Hvis du vil tilordne oppgavelisten til butikker, går du til kategorien **Butikker** og bruker filteret **Organisasjonshierarki** til å finne og velge butikkene.</span><span class="sxs-lookup"><span data-stu-id="74b55-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="74b55-115">Hvis du vil tilordne oppgavelisten til ansatte, går du til kategorien **Ansatte** for å finne og velge de ansatte.</span><span class="sxs-lookup"><span data-stu-id="74b55-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="74b55-116">Velg **OK** for å starte prosessen.</span><span class="sxs-lookup"><span data-stu-id="74b55-116">Select **OK** to start the process.</span></span> <span data-ttu-id="74b55-117">Oppgavelisten tilordnes til de valgte butikkene eller ansatte.</span><span class="sxs-lookup"><span data-stu-id="74b55-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="74b55-118">Illustrasjonen nedenfor viser et eksempel på hvordan du finner og velger butikker i dialogboksen **Start prosess**.</span><span class="sxs-lookup"><span data-stu-id="74b55-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Finne og velge butikker i dialogboksen Start prosess](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="74b55-120">Tilordne oppgavelister regelmessig</span><span class="sxs-lookup"><span data-stu-id="74b55-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="74b55-121">Forhandleren har noen ganger gjentakende oppgaver, for eksempel "Sjekkliste for torsdagslukking" eller "Sjekkliste for første dag i måneden".</span><span class="sxs-lookup"><span data-stu-id="74b55-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="74b55-122">Det kan derfor hende at de vil tilordne oppgavelisten regelmessig.</span><span class="sxs-lookup"><span data-stu-id="74b55-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="74b55-123">Gå til **Retail og Commerce \> Oppgavebehandling \> Administrasjon av oppgavebehandling**.</span><span class="sxs-lookup"><span data-stu-id="74b55-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="74b55-124">Velg oppgavelisten du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="74b55-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="74b55-125">Velg **Start prosess**.</span><span class="sxs-lookup"><span data-stu-id="74b55-125">Select **Start process**.</span></span>
1. <span data-ttu-id="74b55-126">I dialogboksen **Start prosess**, i kategorien **Generelt**, i feltet **Prosessnavn** angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="74b55-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="74b55-127">Sett alternativet **Gjentakelse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="74b55-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="74b55-128">Angi et antall dager i feltet **Forskyvning av måldato for gjentakelse i dager**.</span><span class="sxs-lookup"><span data-stu-id="74b55-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="74b55-129">Hvis du for eksempel angir **4**, er måldatoen gjentakelsesdatoen pluss fire dager.</span><span class="sxs-lookup"><span data-stu-id="74b55-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="74b55-130">I kategorien **Kjør i bakgrunnen** velger du **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="74b55-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="74b55-131">Angi frekvenskriteriene i dialogboksen **Definer regelmessighet**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74b55-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="74b55-132">Illustrasjonen nedenfor viser et eksempel på hvordan du kan angi frekvenskriterier i dialogboksen **Definer regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="74b55-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Angi frekvenskriterier i dialogboksen Definer regelmessighet](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="74b55-134">Status for sporing av oppgaveliste</span><span class="sxs-lookup"><span data-stu-id="74b55-134">Track task list status</span></span>

<span data-ttu-id="74b55-135">Hvis du er en regional leder eller butikkleder, vil du kanskje spore statusen for oppgavelister som er tilordnet til flere butikker eller ansatte.</span><span class="sxs-lookup"><span data-stu-id="74b55-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="74b55-136">Deretter kan du følge opp med butikker eller ansatte som ikke utførte de tildelte oppgavene i tide.</span><span class="sxs-lookup"><span data-stu-id="74b55-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="74b55-137">Med Commerce Back Office kan du vise statusen for oppgavelister, tildele oppgaver på nytt eller endre statusen for en oppgave.</span><span class="sxs-lookup"><span data-stu-id="74b55-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="74b55-138">Følg denne fremgangsmåten for å spore statusen for oppgavelisten for alle oppgaver.</span><span class="sxs-lookup"><span data-stu-id="74b55-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="74b55-139">Gå til **Retail og Commerce \> Oppgavebehandling \> Oppgavebehandlingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="74b55-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="74b55-140">Velg kategorien **Alle oppgavelister** for å vise statusen for alle oppgavelistene som er tilordnet forskjellige butikker.</span><span class="sxs-lookup"><span data-stu-id="74b55-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="74b55-141">Følg denne fremgangsmåten for å spore statusen for alle oppgaver som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="74b55-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="74b55-142">Gå til **Retail og Commerce \> Oppgavebehandling \> Oppgavebehandlingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="74b55-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="74b55-143">Velg kategorien **Mine oppgaver** eller **Alle oppgaver** for å vise eller oppdatere statusen for oppgaver som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="74b55-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74b55-144">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="74b55-144">Additional resources</span></span>

[<span data-ttu-id="74b55-145">Oversikt over oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="74b55-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="74b55-146">Konfigurere oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="74b55-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="74b55-147">Opprette oppgavelister og legge til oppgaver</span><span class="sxs-lookup"><span data-stu-id="74b55-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="74b55-148">Oppgavebehandling på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="74b55-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
