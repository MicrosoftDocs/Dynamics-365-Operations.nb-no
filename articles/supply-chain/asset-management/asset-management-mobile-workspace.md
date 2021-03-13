---
title: Bruke det mobile arbeidsområdet Aktivastyring
description: Dette emnet inneholder informasjon om det mobile arbeidsområdet Aktivastyring
author: josaw1
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: afda807714f14efb1cbab4ecfdd273aac52f4558
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033158"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="4c327-103">Bruke det mobile arbeidsområdet Aktivastyring</span><span class="sxs-lookup"><span data-stu-id="4c327-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c327-104">Dette emnet inneholder informasjon om det mobile arbeidsområdet **Aktivastyring**.</span><span class="sxs-lookup"><span data-stu-id="4c327-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="4c327-105">Dette arbeidsområdet lar brukere vise og opprette vedlikeholdsforespørsler og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="4c327-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="4c327-106">Brukere kan også vise tilordnede arbeidsordrejobber i en kalender- eller listevisning.</span><span class="sxs-lookup"><span data-stu-id="4c327-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="4c327-107">Du kan også vise og søke etter aktiva og arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="4c327-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="4c327-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="4c327-108">Overview</span></span>

<span data-ttu-id="4c327-109">Aktivastyring er en avansert modul for håndtering av aktiva og arbeidsordrejobber i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4c327-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4c327-110">Det mobile arbeidsområdet **Aktivastyring** lar brukere raskt vise tilordnede arbeidsordrejobber på den valgte mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="4c327-111">Brukere kan også opprette og administrere vedlikeholdsforespørsler, oppdatere livssyklustilstand og vise detaljer for arbeidssted ved hjelp av mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="4c327-112">Det mobile arbeidsområdet for **Aktivastyring** lar brukere utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="4c327-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="4c327-113">Opprette, vise og rediger vedlikeholdsforespørsler, ta et bilde eller legger ved et eksisterende bilde i vedlikeholdsforespørselen, endre livssyklustilstanden for vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="4c327-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="4c327-114">Opprette, vise og rediger arbeidsordrer, ta et bilde eller legger ved et eksisterende bilde i arbeidsordren, endre livssyklustilstanden for arbeidsordren, vise arbeidsordrejobber.</span><span class="sxs-lookup"><span data-stu-id="4c327-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="4c327-115">Vise tilordnet arbeidsordrejobber i en kalender visning.</span><span class="sxs-lookup"><span data-stu-id="4c327-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="4c327-116">Opprette, vise og redigere arbeidsordrejobb, oppdater anleggsmiddeltellere, vise sjekkliste for vedlikehold, vise og rediger merknader for arbeidsordrejobb, vise verktøyene som kreves for arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="4c327-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="4c327-117">Vise eller søke etter et bestemt anleggsmiddel eller arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="4c327-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4c327-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="4c327-118">Prerequisites</span></span>

<span data-ttu-id="4c327-119">Før du kan bruke det mobile arbeidsområdet **Aktivastyring**, må administratoren konfigurere den nødvendige brukeren og arbeiderkontoene og publisere arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="4c327-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="4c327-120">Hvis du vil ha mer informasjon, kan du se [Konfigurere det mobile arbeidsområdet Aktivastyring](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="4c327-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="4c327-121">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="4c327-121">Download and install the mobile app</span></span>

<span data-ttu-id="4c327-122">Last ned og installer mobilappen Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="4c327-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="4c327-123">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="4c327-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="4c327-124">For iPhone</span><span class="sxs-lookup"><span data-stu-id="4c327-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="4c327-125">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="4c327-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="4c327-126">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="4c327-127">Skriv inn URL-adressen for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4c327-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="4c327-128">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="4c327-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="4c327-129">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="4c327-129">Enter your credentials.</span></span>

1. <span data-ttu-id="4c327-130">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="4c327-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="4c327-131">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="4c327-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="4c327-132">![Velge et arbeidsområde](media/am-mobile-01.png "Velge et arbeidsområde")</span><span class="sxs-lookup"><span data-stu-id="4c327-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="4c327-133">Vise tilordnet arbeidsordrejobber i en kalender visning</span><span class="sxs-lookup"><span data-stu-id="4c327-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="4c327-134">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-135">Velg **Min kalender for arbeidsordrejobber**.</span><span class="sxs-lookup"><span data-stu-id="4c327-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="4c327-136">Velg datoen du vil vise arbeidsordrejobber for.</span><span class="sxs-lookup"><span data-stu-id="4c327-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="4c327-137">I listen vises ID for anleggsmiddel og arbeidssted for hver arbeidsordrejobb.</span><span class="sxs-lookup"><span data-stu-id="4c327-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="4c327-138">Velg en arbeidsordrejobb i listen for å se jobbdetaljer: Detaljer om anleggsmiddel og arbeidssted, samt andre navigasjonskoblinger for å vise **Vedlegg**, **Kontrollister**, **Verktøy**, **Anleggsmiddeltellere**, **Merknader** og **Journaler**.</span><span class="sxs-lookup"><span data-stu-id="4c327-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="4c327-139">![Vise tilordnet arbeidsordrejobber i en kalender visning](media/am-mobile-02.png "Vise tilordnet arbeidsordrejobber i en kalender visning")</span><span class="sxs-lookup"><span data-stu-id="4c327-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="4c327-140">Opprette en arbeidsordrejobb</span><span class="sxs-lookup"><span data-stu-id="4c327-140">Create a work order job</span></span>

1. <span data-ttu-id="4c327-141">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-142">Velg **Alle arbeidsordrer for vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="4c327-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="4c327-143">Velg arbeidsordren du vil opprette en ny arbeidsordrejobb for.</span><span class="sxs-lookup"><span data-stu-id="4c327-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="4c327-144">Velg **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="4c327-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="4c327-145">Velg **anleggsmiddelet** du vil opprette en arbeidsordrejobb for.</span><span class="sxs-lookup"><span data-stu-id="4c327-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="4c327-146">Velg **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**.</span><span class="sxs-lookup"><span data-stu-id="4c327-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="4c327-147">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-147">Select **Done**.</span></span>

    <span data-ttu-id="4c327-148">![Skjermen Legg til linje](media/am-mobile-03.png "Skjermen Legg til linje")</span><span class="sxs-lookup"><span data-stu-id="4c327-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="4c327-149">Legge til vedlegg i en arbeidsordrejobb</span><span class="sxs-lookup"><span data-stu-id="4c327-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="4c327-150">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-151">Velg **Alle arbeidsordrer for vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="4c327-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="4c327-152">Velg arbeidsordren > arbeidsordrejobben du vil legge til et vedlegg i.</span><span class="sxs-lookup"><span data-stu-id="4c327-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="4c327-153">Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="4c327-154">Velg **Vedlegg** på siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="4c327-155">Du vil se eksisterende vedlegg i arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="4c327-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="4c327-156">Velg **Legg til vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="4c327-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="4c327-157">Angi **Navn** og **Merknader** for vedlegget.</span><span class="sxs-lookup"><span data-stu-id="4c327-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="4c327-158">Velg **Velg bilde** for å velge et bilde fra mobilgalleriet, eller **Ta bilde** for å ta et bilde.</span><span class="sxs-lookup"><span data-stu-id="4c327-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="4c327-159">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-159">Select **Done**.</span></span>

    <span data-ttu-id="4c327-160">![Vise og legge til vedlegg for en arbeidsordrejobb](media/am-mobile-04.png "Vise og legge til vedlegg for en arbeidsordrejobb")</span><span class="sxs-lookup"><span data-stu-id="4c327-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="4c327-161">Vise kontrolliste for vedlikehold på en arbeidsordrejobb</span><span class="sxs-lookup"><span data-stu-id="4c327-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="4c327-162">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-163">Velg **Alle arbeidsordrer for vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="4c327-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="4c327-164">Velg arbeidsordren > arbeidsordrejobben du vil vise kontrollister for.</span><span class="sxs-lookup"><span data-stu-id="4c327-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="4c327-165">Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="4c327-166">Velg **Kontrolliste** på siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="4c327-167">Det vises en liste over kontrollistelinjer som er knyttet til arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="4c327-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="4c327-168">Velg en kontrollistelinje for å vise **Instruksjoner** og legge til **Merknader**.</span><span class="sxs-lookup"><span data-stu-id="4c327-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="4c327-169">Velg Tilbake-knappen (**<**) for å gå tilbake til forrige side.</span><span class="sxs-lookup"><span data-stu-id="4c327-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="4c327-170">![Sjekkliste for vedlikehold og linjedetaljer](media/am-mobile-05.png "Sjekkliste for vedlikehold og linjedetaljer")</span><span class="sxs-lookup"><span data-stu-id="4c327-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="4c327-171">Vise og oppdatere anleggsmiddeltellere i en arbeidsordrejobb</span><span class="sxs-lookup"><span data-stu-id="4c327-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="4c327-172">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-173">Velg **Alle arbeidsordrer for vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="4c327-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="4c327-174">Velg arbeidsordren > arbeidsordrejobben du vil vise anleggsmiddeltellere for.</span><span class="sxs-lookup"><span data-stu-id="4c327-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="4c327-175">Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="4c327-176">Velg **Anleggsmiddeltellere** på siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="4c327-177">Det vises en liste over anleggsmiddeltellere som er knyttet til arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="4c327-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="4c327-178">Velg blyantikonet på en anleggsmiddeltellerlinje for å oppdatere tellerverdien.</span><span class="sxs-lookup"><span data-stu-id="4c327-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="4c327-179">Angi en ny tellerverdi, og velg **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="4c327-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="4c327-180">![Vis og oppdater aktivatellere](media/am-mobile-06.png "Vis og oppdater aktivatellere")</span><span class="sxs-lookup"><span data-stu-id="4c327-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="4c327-181">Registrere forbruk i en arbeidsordrejobb</span><span class="sxs-lookup"><span data-stu-id="4c327-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="4c327-182">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-183">Velg **Alle arbeidsordrer for vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="4c327-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="4c327-184">Velg arbeidsordren > arbeidsordrejobben du vil legge til forbruksregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="4c327-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="4c327-185">Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="4c327-186">Velg **Journaler** på siden **Detaljer for arbeidsordrejobb**.</span><span class="sxs-lookup"><span data-stu-id="4c327-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="4c327-187">Velg **Legg til timer** for å opprette arbeidstimeregistreringer.</span><span class="sxs-lookup"><span data-stu-id="4c327-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="4c327-188">Velg **Kategori** fra oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4c327-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="4c327-189">I **Timer**-feltet angir du antallet arbeidstimer som er brukt på arbeidsordrejobben.</span><span class="sxs-lookup"><span data-stu-id="4c327-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="4c327-190">Velg aktuell **Linjeegenskap**.</span><span class="sxs-lookup"><span data-stu-id="4c327-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="4c327-191">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-191">Select **Done**.</span></span>

1. <span data-ttu-id="4c327-192">Velg **Legg til varer** for å opprette vareregistreringer.</span><span class="sxs-lookup"><span data-stu-id="4c327-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="4c327-193">Velg **Varenummer** fra oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4c327-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="4c327-194">Velg **Område** fra oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4c327-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="4c327-195">Angi **Antall** varer som skal forbrukes.</span><span class="sxs-lookup"><span data-stu-id="4c327-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="4c327-196">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-196">Select **Done**.</span></span>

1. <span data-ttu-id="4c327-197">Velg **Legg til utgift** for å opprette utgiftsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="4c327-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="4c327-198">Velg **Kategori** fra oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4c327-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="4c327-199">Angi antallet for utgiftsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="4c327-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="4c327-200">Velg **Salgsvaluta** fra oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4c327-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="4c327-201">Angi **Kostpris** for utgiftsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="4c327-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="4c327-202">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-202">Select **Done**.</span></span>

    <span data-ttu-id="4c327-203">![Oppdatere en arbeidsordrejournal](media/am-mobile-07.png "Oppdatere en arbeidsordrejournal")</span><span class="sxs-lookup"><span data-stu-id="4c327-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="4c327-204">Oppdatere livssyklustilstand på en arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="4c327-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="4c327-205">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-206">Velg **Alle arbeidsordrer for vedlikehold**.</span><span class="sxs-lookup"><span data-stu-id="4c327-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="4c327-207">Velg arbeidsordren du vil oppdatere livssyklustilstand for.</span><span class="sxs-lookup"><span data-stu-id="4c327-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="4c327-208">Velg **Oppdater tilstand**-knappen nederst på skjermen.</span><span class="sxs-lookup"><span data-stu-id="4c327-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="4c327-209">Velg en ny livssyklustilstand fra listen.</span><span class="sxs-lookup"><span data-stu-id="4c327-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="4c327-210">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-210">Select **Done**.</span></span>

    <span data-ttu-id="4c327-211">![Oppdatere livssyklustilstand på en arbeidsordre](media/am-mobile-08.png "Oppdatere livssyklustilstand på en arbeidsordre")</span><span class="sxs-lookup"><span data-stu-id="4c327-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="4c327-212">Opprette en melding</span><span class="sxs-lookup"><span data-stu-id="4c327-212">Create a maintenance request</span></span>

1. <span data-ttu-id="4c327-213">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-214">Velg **Alle vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="4c327-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="4c327-215">Velg **Handlinger** nederst på skjermen, og velg deretter **Opprett vedlikeholdsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="4c327-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="4c327-216">Hvis nummerserie er aktivert for vedlikeholdsforespørsler i **Aktivastyring**, skjules feltet **Vedlikeholdsforespørsel** fordi det fylles ut automatisk. Hvis feltet **Vedlikeholdsforespørsel** vises, angir du en ID for vedlikeholdsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="4c327-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="4c327-217">Velg **Type vedlikeholdsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="4c327-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="4c327-218">Angi en **Beskrivelse** vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="4c327-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="4c327-219">Velg **Anleggsmiddel** du vil opprette forespørselen for.</span><span class="sxs-lookup"><span data-stu-id="4c327-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="4c327-220">Velg **Servicenivå** for vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="4c327-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="4c327-221">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-221">Select **Done**.</span></span>

    <span data-ttu-id="4c327-222">![Opprette en melding](media/am-mobile-09.png "Opprette en melding")</span><span class="sxs-lookup"><span data-stu-id="4c327-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="4c327-223">Legge til vedlegg i en vedlikeholdsforespørsel</span><span class="sxs-lookup"><span data-stu-id="4c327-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="4c327-224">Åpne arbeidsområdet **Aktivastyring** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="4c327-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="4c327-225">Velg **Alle vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="4c327-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="4c327-226">Velg vedlikeholdsforespørselen du vil legge til et vedlegg i.</span><span class="sxs-lookup"><span data-stu-id="4c327-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="4c327-227">Velg **Vedlegg** nederst på skjermen.</span><span class="sxs-lookup"><span data-stu-id="4c327-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="4c327-228">Velg **Legg til vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="4c327-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="4c327-229">Angi **Navn** og **Merknader** for vedlegget.</span><span class="sxs-lookup"><span data-stu-id="4c327-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="4c327-230">Velg **Velg bilde** for å velge et bilde fra mobilgalleriet, eller **Ta bilde** for å ta et bilde.</span><span class="sxs-lookup"><span data-stu-id="4c327-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="4c327-231">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="4c327-231">Select **Done**.</span></span>

    <span data-ttu-id="4c327-232">![Legge til et vedlegg i en vedlikeholdsforespørsel](media/am-mobile-10.png "Legge til et vedlegg i en vedlikeholdsforespørsel")</span><span class="sxs-lookup"><span data-stu-id="4c327-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>
