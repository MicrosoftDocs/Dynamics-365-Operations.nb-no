---
title: Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS
description: Dette emnet beskriver hvordan du synkroniserer oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce-salgsstedet (POS).
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020633"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="ddc48-103">Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="ddc48-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ddc48-104">Dette emnet beskriver hvordan du synkroniserer oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce-salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="ddc48-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="ddc48-105">Et av hovedformålene med Teams-integrering er å aktivere synkronisering av oppgavestyring mellom POS-programmet og Teams.</span><span class="sxs-lookup"><span data-stu-id="ddc48-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="ddc48-106">På denne måten kan butikkansatte bruke enten POS-programmet eller Teams til å administrere oppgaver, uten at de må bytte programmer.</span><span class="sxs-lookup"><span data-stu-id="ddc48-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="ddc48-107">Siden Planner brukes som et oppbevaringssted for oppgaver i Teams, må det være en kobling mellom Teams og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ddc48-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="ddc48-108">Denne koblingen opprettes ved å bruke en bestemt plan-ID for en angitt butikkgruppe.</span><span class="sxs-lookup"><span data-stu-id="ddc48-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="ddc48-109">Fremgangsmåtene nedenfor viser hvordan du konfigurerer oppgavebehandlingssynkronisering mellom POS- og Teams-programmene.</span><span class="sxs-lookup"><span data-stu-id="ddc48-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="ddc48-110">Publiser en testoppgaveliste i Teams</span><span class="sxs-lookup"><span data-stu-id="ddc48-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="ddc48-111">Fremgangsmåten nedenfor forutsetter at butikkgruppene bruker integrering av Microsoft Teams-oppgavebehandling med Commerce for første gang.</span><span class="sxs-lookup"><span data-stu-id="ddc48-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="ddc48-112">Følg denne fremgangsmåten for å publisere en testoppgaveliste i Teams.</span><span class="sxs-lookup"><span data-stu-id="ddc48-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="ddc48-113">Logg deg på Teams som en kommunikasjonsleder.</span><span class="sxs-lookup"><span data-stu-id="ddc48-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="ddc48-114">Kommunikasjonsledere er vanligvis brukere som har rollen **Regional leder** i Commerce.</span><span class="sxs-lookup"><span data-stu-id="ddc48-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="ddc48-115">Velg **Oppgaver etter planlegger** i den venstre navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="ddc48-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="ddc48-116">På fanen **Publiserte lister** velger du **Ny liste** nederst til venstre og gir den nye listen navnet **Testoppgaveliste**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="ddc48-117">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-117">Select **Create**.</span></span> <span data-ttu-id="ddc48-118">Den nye listen vises under **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="ddc48-119">Under **Oppgavetittel** gir du den første oppgaven tittelen **Testing av Teams-integrering**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="ddc48-120">Velg deretter **Enter**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="ddc48-121">Velg oppgavelisten i **Utkast**-listen.</span><span class="sxs-lookup"><span data-stu-id="ddc48-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="ddc48-122">Velg deretter **Publiser** øverst til høyre.</span><span class="sxs-lookup"><span data-stu-id="ddc48-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="ddc48-123">I dialogboksen **Velg hvem det skal publiseres til** velger du teamene som skal motta testoppgavelisten.</span><span class="sxs-lookup"><span data-stu-id="ddc48-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="ddc48-124">Velg **Neste** for å gå gjennom publikasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="ddc48-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="ddc48-125">Hvis du må gjøre endringer, velger du **Tilbake**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="ddc48-126">Velg **Bekreft for å fortsette**, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="ddc48-127">Når publiseringen er fullført, viser en melding øverst på fanen **Publiserte lister** om oppgavelisten ble levert.</span><span class="sxs-lookup"><span data-stu-id="ddc48-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="ddc48-128">Hvis du vil ha mer informasjon, kan du se [Publiser oppgavelister for å opprette og spore arbeid i organisasjonen](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="ddc48-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="ddc48-129">Koble POS og Teams for oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="ddc48-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="ddc48-130">Hvis du vil koble POS- og Microsoft Teams-programmene for oppgavebehandling i Commerce Headquarters, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ddc48-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ddc48-131">Gå til **Retail og Commerce \> Oppgavebehandling \> Oppgaveintegrering med Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="ddc48-132">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ddc48-133">Sett alternativet **Aktiver integrering av oppgavebehandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="ddc48-134">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ddc48-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ddc48-135">Velg **Konfigurer oppgavebehandling** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ddc48-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="ddc48-136">Du skal motta en varsling som angir at en satsvis jobb med navnet **Teams-klargjøring** opprettes.</span><span class="sxs-lookup"><span data-stu-id="ddc48-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="ddc48-137">Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**, og finn den nyeste jobben som har beskrivelsen **Teams-klargjøring**.</span><span class="sxs-lookup"><span data-stu-id="ddc48-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="ddc48-138">Vent til denne jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="ddc48-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="ddc48-139">Kjør **CDX-jobb 1070** for å publisere plan-ID-en og lagre referanser til Retail Server.</span><span class="sxs-lookup"><span data-stu-id="ddc48-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ddc48-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ddc48-140">Additional resources</span></span>

[<span data-ttu-id="ddc48-141">Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="ddc48-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ddc48-142">Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="ddc48-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ddc48-143">Klargjøring av Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ddc48-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ddc48-144">Behandle brukerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ddc48-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ddc48-145">Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ddc48-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="ddc48-146">Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="ddc48-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
