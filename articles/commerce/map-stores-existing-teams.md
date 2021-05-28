---
title: Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams
description: Dette emnet beskriver hvordan du tilordner butikker og tilsvarende grupper i Dynamics 365 Commerce-hovedkontoret hvis organisasjonen allerede har opprettet grupper i Microsoft Teams før Commerce-integrering.
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
ms.openlocfilehash: ccc2cbf11e405facf310d93e5458cfe12a43146d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020225"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="0b7a8-103">Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0b7a8-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b7a8-104">Dette emnet beskriver hvordan du tilordner butikker og tilsvarende grupper i Dynamics 365 Commerce-hovedkontoret hvis organisasjonen allerede har opprettet grupper i Microsoft Teams før Commerce-integrering.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="0b7a8-105">Organisasjonen kan ha grupper som er opprettet for noen av eller alle butikkene, før integrering av Dynamics 365 Commerce og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="0b7a8-106">Hvis dette er tilfelle, og hvis du skal opprette oppgavesynkronisering mellom Commerce POS og Microsoft Teams, må du angi tilordningen av butikker og tilsvarende team i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="0b7a8-107">Tilordne butikker og tilsvarende grupper i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="0b7a8-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="0b7a8-108">Følg denne fremgangsmåten for å tilordne butikker og tilsvarende grupper i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0b7a8-109">Gå til **Systemadministrasjon \> Arbeidsområde \> Dataadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="0b7a8-110">Velg **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-110">Select **Export**.</span></span> 
1. <span data-ttu-id="0b7a8-111">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0b7a8-112">Under **Gruppenavn** angir du "Eksporter Teams-tilordning".</span><span class="sxs-lookup"><span data-stu-id="0b7a8-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="0b7a8-113">På **Valgte enheter**-hurtigfanen velger du **Legg til enhet**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="0b7a8-114">Dialogboksen **Legg til enhet** vises.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="0b7a8-115">I rullegardinlisten **Enhetsnavn** velger du **Teams-tilordning mellom kilde og team**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="0b7a8-116">I rullegardinlisten **Måldataformat** velger du **CSV**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="0b7a8-117">Velg **Legg til**, og velg deretter **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="0b7a8-118">Velg **Eksporter nå** øverst til venstre under handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="0b7a8-119">Under **Behandlingsstatus for enhet** velger du **Last ned fil**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="0b7a8-120">I den eksporterte CSV-filen angir du verdier for **SOURCETYPE**, **SOURCEID** og **TEAMID** som følger:</span><span class="sxs-lookup"><span data-stu-id="0b7a8-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="0b7a8-121">For **SOURCETYPE** angir du "RetailStore".</span><span class="sxs-lookup"><span data-stu-id="0b7a8-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="0b7a8-122">For **SOURCEID** angir du butikknummeret (for eksempel "000135" for butikken i San Francisco).</span><span class="sxs-lookup"><span data-stu-id="0b7a8-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="0b7a8-123">Du finner butikknumre under **Retail og Commerce \> Kanaler \> Butikker**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="0b7a8-124">For **TEAMID** angir du tilsvarende team-ID fra Microsoft Teams (for eksempel "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="0b7a8-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="0b7a8-125">Du finner informasjon om team-ID-er på [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0b7a8-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="0b7a8-126">Lagre CSV-filen på den lokale maskinen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="0b7a8-127">Gå til **Systemadministrasjon \> Arbeidsområde \> Dataadministrasjon**, og velg deretter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="0b7a8-128">På **Valgte enheter**-hurtigfanen velger du **Legg til fil**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="0b7a8-129">Dialogboksen **Legg til fil** vises.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="0b7a8-130">I rullegardinlisten **Enhetsnavn** velger du **Teams-tilordning mellom kilde og team**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="0b7a8-131">I rullegardinlisten **Kildedataformat** velger du **CSV**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="0b7a8-132">Velg **Last opp og legg til**, velg CSV-filen du lagret tidligere, og velg deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="0b7a8-133">I dialogboksen **Legg til fil** velger du **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="0b7a8-134">Velg **Lagre** i handlingsruten , og velg deretter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="0b7a8-135">Følgende eksempelbilde viser gruppen **Eksporter Teams-tilordning** i Commerce med **Legg til enhet**-elementer og de eksporterte CSV-filhodene uthevet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Eksporter Teams-tilordning i Commerce med Legg til enhet-elementer og de eksporterte CSV-filhodene uthevet](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="0b7a8-137">Når du har fullført trinnene ovenfor, følger du trinnene i [Synkroniser oppgavebehandling mellom Microsoft Teams og POS](synchronize-tasks-teams-pos.md) for å synkronisere oppgavebehandling.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0b7a8-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0b7a8-138">Additional resources</span></span>

[<span data-ttu-id="0b7a8-139">Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="0b7a8-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="0b7a8-140">Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="0b7a8-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="0b7a8-141">Klargjøring av Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b7a8-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="0b7a8-142">Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="0b7a8-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="0b7a8-143">Behandle brukerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0b7a8-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="0b7a8-144">Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="0b7a8-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
