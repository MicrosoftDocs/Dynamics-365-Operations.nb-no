---
title: "Mobilt arbeidsområde for registrering av prosjekttid"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for registrering av prosjekttid. Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: db41b3873755f93895aea7a32b65f2a8ed6a57fd
ms.openlocfilehash: 83899969255a9b771fc5e62e66e3c5ffdca0296e
ms.contentlocale: nb-no
ms.lasthandoff: 08/10/2017

---

# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="86235-104">Mobilt arbeidsområde for registrering av prosjekttid</span><span class="sxs-lookup"><span data-stu-id="86235-104">Project time entry mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="86235-105">Dette emnet gir informasjon om det mobile arbeidsområdet for **registrering av prosjekttid**.</span><span class="sxs-lookup"><span data-stu-id="86235-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="86235-106">Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="86235-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="86235-107">Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="86235-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="86235-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="86235-108">Overview</span></span>
<span data-ttu-id="86235-109">Prosjektressurser er ofte på stedet eller reiser som en del av det daglige arbeidet.</span><span class="sxs-lookup"><span data-stu-id="86235-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="86235-110">Det mobile arbeidsområdet **Registrering av prosjekttid** lar brukere angi fakturerbar eller ikke-fakturerbar tid mot et prosjekt på mobilenheten etter eget valg.</span><span class="sxs-lookup"><span data-stu-id="86235-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="86235-111">Derfor kan prosjektressurser registrere oppføringer når som helst og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="86235-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="86235-112">De kan også vise oppføringer som allerede er registrert.</span><span class="sxs-lookup"><span data-stu-id="86235-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="86235-113">I det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="86235-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="86235-114">For en valgt dato kan du angi hvor mange timer du har brukt på en bestemt oppgave.</span><span class="sxs-lookup"><span data-stu-id="86235-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="86235-115">Søke etter prosjektnavn eller kunde til å finne prosjektet å angi tid for.</span><span class="sxs-lookup"><span data-stu-id="86235-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="86235-116">Angi kategori og aktivitet for tiden du har brukt.</span><span class="sxs-lookup"><span data-stu-id="86235-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="86235-117">Registrere tiden som fakturerbar eller ikke-fakturerbar for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="86235-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="86235-118">Du kan også angi eventuelle eksterne eller interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="86235-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86235-119">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="86235-119">Prerequisites</span></span>
<span data-ttu-id="86235-120">Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="86235-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="86235-121">Forutsetninger hvis du bruker oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="86235-121">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span> 
<span data-ttu-id="86235-122">Hvis oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition er distribuert i organisasjonen, må systemansvarlig publisere det mobile arbeidsområdet **Tidsoppføring for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="86235-122">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="86235-123">Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="86235-123">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="86235-124">Forutsetninger hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere</span><span class="sxs-lookup"><span data-stu-id="86235-124">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="86235-125">Hvis Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="86235-125">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="86235-126">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="86235-126">Prerequisite</span></span></th>
<th><span data-ttu-id="86235-127">Rolle</span><span class="sxs-lookup"><span data-stu-id="86235-127">Role</span></span></th>
<th><span data-ttu-id="86235-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="86235-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="86235-129">Implementer KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="86235-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="86235-130">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="86235-130">System administrator</span></span></td>
<td><span data-ttu-id="86235-131">KB 4018050 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>registrering av prosjekttid</strong>.</span><span class="sxs-lookup"><span data-stu-id="86235-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="86235-132">Systemadministrator må følge trinnene nedenfor for å implementere KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="86235-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="86235-133"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="86235-133"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="86235-134"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjonen for metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="86235-134"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="86235-135"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder modellene <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong>, og laste deretter opp den distribuerbare pakken til LCS.</span><span class="sxs-lookup"><span data-stu-id="86235-135"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="86235-136"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Bruk den distribuerbare pakken</a>.</span><span class="sxs-lookup"><span data-stu-id="86235-136"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86235-137">Publiser det mobile arbeidsområdet <strong>Tidsoppføring for prosjekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="86235-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="86235-138">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="86235-138">System administrator</span></span></td>
<td><span data-ttu-id="86235-139">Se <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="86235-139">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="86235-140">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="86235-140">Download and install the mobile app</span></span>

<span data-ttu-id="86235-141">Last ned og installer mobilappen Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="86235-141">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="86235-142">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="86235-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="86235-143">For iPhone</span><span class="sxs-lookup"><span data-stu-id="86235-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="86235-144">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="86235-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="86235-145">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="86235-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="86235-146">Skriv inn URL-adressen for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="86235-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="86235-147">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="86235-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="86235-148">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="86235-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="86235-149">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="86235-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="86235-150">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="86235-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="86235-151">[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="86235-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="86235-152">Angi tid ved hjelp av det mobile arbeidsområdet Registrering av prosjekttid</span><span class="sxs-lookup"><span data-stu-id="86235-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="86235-153">Velg arbeidsområdet **Registrering av prosjekttid** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="86235-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="86235-154">Velg **Tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="86235-154">Select **Time entry**.</span></span> <span data-ttu-id="86235-155">Du kan se kalenderdatoene for gjeldende uke.</span><span class="sxs-lookup"><span data-stu-id="86235-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="86235-156">Velg **Handlinger** &gt; **Ny oppføring** for en valgt dato.</span><span class="sxs-lookup"><span data-stu-id="86235-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="86235-157">Angi antallet timer som skal registreres.</span><span class="sxs-lookup"><span data-stu-id="86235-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="86235-158">Velg prosjektet for timeregistreringen.</span><span class="sxs-lookup"><span data-stu-id="86235-158">Select the project for the time entry.</span></span> <span data-ttu-id="86235-159">Du kan se en liste over prosjekter som er lastet inn i ditt program for frakoblet bruk.</span><span class="sxs-lookup"><span data-stu-id="86235-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="86235-160">50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="86235-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="86235-161">Hvis du vil ha mer informasjon, kan du se [Mobil plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span><span class="sxs-lookup"><span data-stu-id="86235-161">For more information, see [Mobile platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span></span>
6.  <span data-ttu-id="86235-162">Hvis prosjektet ikke finnes i listen, velger du **Søk etter**.</span><span class="sxs-lookup"><span data-stu-id="86235-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="86235-163">Søk etter navn, eller bytt til å søke etter prosjektnavn eller kunde.</span><span class="sxs-lookup"><span data-stu-id="86235-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="86235-164">Velg en kategori.</span><span class="sxs-lookup"><span data-stu-id="86235-164">Select a category.</span></span> <span data-ttu-id="86235-165">Du kan se en liste over kategorier som er lastet inn i ditt program for frakoblet bruk.</span><span class="sxs-lookup"><span data-stu-id="86235-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="86235-166">50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="86235-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="86235-167">Hvis du vil ha mer informasjon, kan du se [Mobil plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span><span class="sxs-lookup"><span data-stu-id="86235-167">For more information, see [Mobile platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span></span>
8.  <span data-ttu-id="86235-168">Hvis kategorien ikke finnes i listen, velger du **Søk etter**.</span><span class="sxs-lookup"><span data-stu-id="86235-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="86235-169">Søk etter kategori, eller bytt til å søke etter kategorinavn.</span><span class="sxs-lookup"><span data-stu-id="86235-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="86235-170">Velg en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="86235-170">Select an activity.</span></span> <span data-ttu-id="86235-171">Du kan se en liste over aktiviteter som er lastet inn i ditt program for frakoblet bruk.</span><span class="sxs-lookup"><span data-stu-id="86235-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="86235-172">50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet.</span><span class="sxs-lookup"><span data-stu-id="86235-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="86235-173">Hvis du vil ha mer informasjon, kan du se [Mobil plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span><span class="sxs-lookup"><span data-stu-id="86235-173">For more information, see [Mobile platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span></span>
10. <span data-ttu-id="86235-174">Hvis aktiviteten ikke finnes i listen, velger du **Søk etter**.</span><span class="sxs-lookup"><span data-stu-id="86235-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="86235-175">Søke etter aktivitetsnummeret, eller bytt til å søke etter formål.</span><span class="sxs-lookup"><span data-stu-id="86235-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="86235-176">Velg linjeegenskapen.</span><span class="sxs-lookup"><span data-stu-id="86235-176">Select the line property.</span></span>
12. <span data-ttu-id="86235-177">Valgfritt: Angi eventuelle eksterne og interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="86235-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="86235-178">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="86235-178">Select **Done**.</span></span>

