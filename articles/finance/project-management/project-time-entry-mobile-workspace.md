---
title: Mobilt arbeidsområde for registrering av prosjekttid
description: Dette emnet gir informasjon om det mobile arbeidsområdet for registrering av prosjekttid. Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250375"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="28ca7-104">Mobilt arbeidsområde for registrering av prosjekttid</span><span class="sxs-lookup"><span data-stu-id="28ca7-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28ca7-105">Dette emnet gir informasjon om det mobile arbeidsområdet for **registrering av prosjekttid**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="28ca7-106">Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="28ca7-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="28ca7-107">Dette mobile arbeidsområdet er ment å brukes med mobilappen Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="28ca7-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="28ca7-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="28ca7-108">Overview</span></span>
<span data-ttu-id="28ca7-109">Prosjektressurser er ofte på stedet eller reiser som en del av det daglige arbeidet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="28ca7-110">Det mobile arbeidsområdet **Registrering av prosjekttid** lar brukere angi fakturerbar eller ikke-fakturerbar tid mot et prosjekt på mobilenheten etter eget valg.</span><span class="sxs-lookup"><span data-stu-id="28ca7-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="28ca7-111">Derfor kan prosjektressurser registrere oppføringer når som helst og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="28ca7-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="28ca7-112">De kan også vise oppføringer som allerede er registrert.</span><span class="sxs-lookup"><span data-stu-id="28ca7-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="28ca7-113">I det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="28ca7-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="28ca7-114">For en valgt dato kan du angi hvor mange timer du har brukt på en bestemt oppgave.</span><span class="sxs-lookup"><span data-stu-id="28ca7-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="28ca7-115">Søke etter prosjektnavn eller kunde til å finne prosjektet å angi tid for.</span><span class="sxs-lookup"><span data-stu-id="28ca7-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="28ca7-116">Angi kategori og aktivitet for tiden du har brukt.</span><span class="sxs-lookup"><span data-stu-id="28ca7-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="28ca7-117">Registrere tiden som fakturerbar eller ikke-fakturerbar for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="28ca7-118">Du kan også angi eventuelle eksterne eller interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="28ca7-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="28ca7-119">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="28ca7-119">Prerequisites</span></span>
<span data-ttu-id="28ca7-120">Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="28ca7-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="28ca7-121">Forutsetninger hvis du bruker Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="28ca7-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="28ca7-122">Hvis Finance har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Tidsoppføring for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="28ca7-123">Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="28ca7-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="28ca7-124">Forutsetninger hvis du bruker versjon 1611 med Platform update 3 eller nyere</span><span class="sxs-lookup"><span data-stu-id="28ca7-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="28ca7-125">Hvis versjon 1611 med Platform update 3 eller nyere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="28ca7-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="28ca7-126">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="28ca7-126">Prerequisite</span></span></th>
<th><span data-ttu-id="28ca7-127">Rolle</span><span class="sxs-lookup"><span data-stu-id="28ca7-127">Role</span></span></th>
<th><span data-ttu-id="28ca7-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="28ca7-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="28ca7-129">Implementer KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="28ca7-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="28ca7-130">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="28ca7-130">System administrator</span></span></td>
<td><span data-ttu-id="28ca7-131">KB 4018050 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>registrering av prosjekttid</strong>.</span><span class="sxs-lookup"><span data-stu-id="28ca7-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="28ca7-132">Systemadministrator må følge trinnene nedenfor for å implementere KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="28ca7-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="28ca7-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="28ca7-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="28ca7-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="28ca7-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="28ca7-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder modellene <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong>, og laste deretter opp den distribuerbare pakken til LCS.</span><span class="sxs-lookup"><span data-stu-id="28ca7-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="28ca7-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</span><span class="sxs-lookup"><span data-stu-id="28ca7-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28ca7-137">Publiser det mobile arbeidsområdet <strong>Tidsoppføring for prosjekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="28ca7-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="28ca7-138">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="28ca7-138">System administrator</span></span></td>
<td><span data-ttu-id="28ca7-139">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="28ca7-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="28ca7-140">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="28ca7-140">Download and install the mobile app</span></span>

<span data-ttu-id="28ca7-141">Laste ned og installere Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="28ca7-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="28ca7-142">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="28ca7-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="28ca7-143">For iPhone</span><span class="sxs-lookup"><span data-stu-id="28ca7-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="28ca7-144">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="28ca7-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="28ca7-145">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="28ca7-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="28ca7-146">Skriv inn URL-adressen for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="28ca7-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="28ca7-147">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="28ca7-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="28ca7-148">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="28ca7-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="28ca7-149">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="28ca7-150">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="28ca7-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="28ca7-151">[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="28ca7-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="28ca7-152">Angi tid ved hjelp av det mobile arbeidsområdet Registrering av prosjekttid</span><span class="sxs-lookup"><span data-stu-id="28ca7-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="28ca7-153">Velg arbeidsområdet **Registrering av prosjekttid** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="28ca7-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="28ca7-154">Velg **Tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-154">Select **Time entry**.</span></span> <span data-ttu-id="28ca7-155">Du kan se kalenderdatoene for gjeldende uke.</span><span class="sxs-lookup"><span data-stu-id="28ca7-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="28ca7-156">Velg **Handlinger** &gt; **Ny oppføring** for en valgt dato.</span><span class="sxs-lookup"><span data-stu-id="28ca7-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="28ca7-157">Angi antallet timer som skal registreres.</span><span class="sxs-lookup"><span data-stu-id="28ca7-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="28ca7-158">Velg prosjektet for timeregistreringen.</span><span class="sxs-lookup"><span data-stu-id="28ca7-158">Select the project for the time entry.</span></span> <span data-ttu-id="28ca7-159">Du kan se en liste over prosjekter som er lastet inn i ditt program for frakoblet bruk.</span><span class="sxs-lookup"><span data-stu-id="28ca7-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="28ca7-160">50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="28ca7-161">Hvis du vil ha mer informasjon, kan du se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="28ca7-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="28ca7-162">Hvis prosjektet ikke finnes i listen, velger du **Søk etter**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="28ca7-163">Søk etter navn, eller bytt til å søke etter prosjektnavn eller kunde.</span><span class="sxs-lookup"><span data-stu-id="28ca7-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="28ca7-164">Velg en kategori.</span><span class="sxs-lookup"><span data-stu-id="28ca7-164">Select a category.</span></span> <span data-ttu-id="28ca7-165">Du kan se en liste over kategorier som er lastet inn i ditt program for frakoblet bruk.</span><span class="sxs-lookup"><span data-stu-id="28ca7-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="28ca7-166">50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="28ca7-167">Hvis du vil ha mer informasjon, kan du se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="28ca7-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="28ca7-168">Hvis kategorien ikke finnes i listen, velger du **Søk etter**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="28ca7-169">Søk etter kategori, eller bytt til å søke etter kategorinavn.</span><span class="sxs-lookup"><span data-stu-id="28ca7-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="28ca7-170">Velg en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-170">Select an activity.</span></span> <span data-ttu-id="28ca7-171">Du kan se en liste over aktiviteter som er lastet inn i ditt program for frakoblet bruk.</span><span class="sxs-lookup"><span data-stu-id="28ca7-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="28ca7-172">50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="28ca7-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="28ca7-173">Hvis du vil ha mer informasjon, kan du se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="28ca7-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="28ca7-174">Hvis aktiviteten ikke finnes i listen, velger du **Søk etter**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="28ca7-175">Søke etter aktivitetsnummeret, eller bytt til å søke etter formål.</span><span class="sxs-lookup"><span data-stu-id="28ca7-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="28ca7-176">Velg linjeegenskapen.</span><span class="sxs-lookup"><span data-stu-id="28ca7-176">Select the line property.</span></span>
12. <span data-ttu-id="28ca7-177">Valgfritt: Angi eventuelle eksterne og interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="28ca7-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="28ca7-178">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="28ca7-178">Select **Done**.</span></span>
