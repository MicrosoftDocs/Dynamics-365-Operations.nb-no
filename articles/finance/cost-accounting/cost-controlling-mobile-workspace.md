---
title: Mobilt arbeidsområde for kostnadskontroll
description: Dette emnet gir informasjon om det mobile arbeidsområdet for kostnadskontroll. I dette arbeidsområdet kan kostsenterledere se kostsenterresultater når som helst og hvor som helst.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 22acdcfbecc1efe78a1b1be87e40b2e7d23506fc
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759454"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="5281f-104">Mobilt arbeidsområde for kostnadskontroll</span><span class="sxs-lookup"><span data-stu-id="5281f-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5281f-105">Dette emnet gir informasjon om det mobile arbeidsområdet **Kostnadskontroll**.</span><span class="sxs-lookup"><span data-stu-id="5281f-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="5281f-106">I dette arbeidsområdet kan kostsenterledere se kostsenterresultater når som helst og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="5281f-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="5281f-107">Dette mobile arbeidsområdet er ment å brukes sammen med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="5281f-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="5281f-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="5281f-108">Overview</span></span>
<span data-ttu-id="5281f-109">Mobilt arbeidsområde for **kostnadskontroll** gir en øyeblikkelig visning av den gjeldende ytelsen til kostsentre ved å sammenligne faktiske kostnader med de budsjetterte kostnadene.</span><span class="sxs-lookup"><span data-stu-id="5281f-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="5281f-110">Du kan drille ned til statusen for individuelle kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="5281f-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="5281f-111">En ansatt mottar for eksempel en invitasjon til en internasjonal konferanse, men organisasjonen må dekke alle reiseutgifter.</span><span class="sxs-lookup"><span data-stu-id="5281f-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="5281f-112">Den ansatte ber lederen om tillatelse til å delta på konferansen.</span><span class="sxs-lookup"><span data-stu-id="5281f-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="5281f-113">Lederen åpner det mobile arbeidsområdet for **kostnadskontroll** på mobilenheten for å se om han/hun har budsjettert for at den ansatte kan delta på konferansen.</span><span class="sxs-lookup"><span data-stu-id="5281f-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="5281f-114">Datasikkerhet</span><span class="sxs-lookup"><span data-stu-id="5281f-114">Data security</span></span>
<span data-ttu-id="5281f-115">Dataene i arbeidsområdet for **kostnadskontroll** er sikret gjennom brukerlegitimasjon.</span><span class="sxs-lookup"><span data-stu-id="5281f-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="5281f-116">Kostsenterledere kan bare se data for sitt eget kostsenter.</span><span class="sxs-lookup"><span data-stu-id="5281f-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="5281f-117">Tilgangsnivåsikkerhet behandles i modulen **Kostnadsregnskap**.</span><span class="sxs-lookup"><span data-stu-id="5281f-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="5281f-118">Regnskapsførere definerer konfigurasjonen av det mobile arbeidsområdet for **kostnadskontroll** i modulen **Kostnadsregnskap**.</span><span class="sxs-lookup"><span data-stu-id="5281f-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="5281f-119">Etter at arbeidsområdet er publisert på mobilappen, er det tilgjengelig i appen.</span><span class="sxs-lookup"><span data-stu-id="5281f-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="5281f-120">Dette sikrer at alle kostsenterledere i organisasjonen ser dataene i det samme formatet.</span><span class="sxs-lookup"><span data-stu-id="5281f-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="5281f-121">Handlinger, visninger og koblinger</span><span class="sxs-lookup"><span data-stu-id="5281f-121">Actions, views, and links</span></span>
<span data-ttu-id="5281f-122">Det mobile arbeidsområdet **Kostnadskontroll** har følgende handlinger, visninger og koblinger:</span><span class="sxs-lookup"><span data-stu-id="5281f-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="5281f-123">**Handlinger:**</span><span class="sxs-lookup"><span data-stu-id="5281f-123">**Actions:**</span></span>

    -   <span data-ttu-id="5281f-124">Bruk **Velg konfigurasjon** for å velge et oppsett.</span><span class="sxs-lookup"><span data-stu-id="5281f-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="5281f-125">Bruk **Velg kostnadsobjekt** for å velge kostsentrene til å filtrere dataene på.</span><span class="sxs-lookup"><span data-stu-id="5281f-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="5281f-126">Kostsentrene som vises i listen, avhenger av tilgangen som gis i modulen **Kostnadsregnskap**.</span><span class="sxs-lookup"><span data-stu-id="5281f-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="5281f-127">**Visninger:** Basert på handlingene som er valgt, og konfigurasjonen i modulen **Kostnadsregnskap**, kan du vise følgende informasjon på kortene:</span><span class="sxs-lookup"><span data-stu-id="5281f-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="5281f-128">Faktisk i forhold til budsjett (gjeldende periode)</span><span class="sxs-lookup"><span data-stu-id="5281f-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="5281f-129">Faktisk i forhold til revidert budsjett (gjeldende periode)</span><span class="sxs-lookup"><span data-stu-id="5281f-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="5281f-130">Faktisk i forhold til budsjett (forrige periode)</span><span class="sxs-lookup"><span data-stu-id="5281f-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="5281f-131">Faktisk i forhold til revidert budsjett (forrige periode)</span><span class="sxs-lookup"><span data-stu-id="5281f-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="5281f-132">Faktisk i forhold til budsjett (hittil i år)</span><span class="sxs-lookup"><span data-stu-id="5281f-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="5281f-133">Faktisk i forhold til revidert budsjett (hittil i år)</span><span class="sxs-lookup"><span data-stu-id="5281f-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="5281f-134">Disse beløpene vises på hvert kort: faktisk, budsjett, avvik og varians %.</span><span class="sxs-lookup"><span data-stu-id="5281f-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="5281f-135">**Koblinger:**</span><span class="sxs-lookup"><span data-stu-id="5281f-135">**Links:**</span></span>

    -   <span data-ttu-id="5281f-136">Detaljer for gjeldende periode</span><span class="sxs-lookup"><span data-stu-id="5281f-136">Details for current period</span></span>
    -   <span data-ttu-id="5281f-137">Detaljer for forrige periode</span><span class="sxs-lookup"><span data-stu-id="5281f-137">Details for previous period</span></span>
    -   <span data-ttu-id="5281f-138">Detaljer for hittil i år</span><span class="sxs-lookup"><span data-stu-id="5281f-138">Details for year to date</span></span>

    <span data-ttu-id="5281f-139">Når du velger en kobling, vises et kort for hvert kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="5281f-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="5281f-140">Følgende beløp vises på hvert kort: faktisk, budsjett, budsjettavvik, budsjettavviks-%, revidert budsjett, revidert budsjettavvik og revidert budsjettavviks-%.</span><span class="sxs-lookup"><span data-stu-id="5281f-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="5281f-141">[![Kort for et kostnadselement ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="5281f-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5281f-142">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="5281f-142">Prerequisites</span></span>
<span data-ttu-id="5281f-143">Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="5281f-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a><span data-ttu-id="5281f-144">Forutsetninger hvis du bruker Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="5281f-144">Prerequisites if you use Microsoft Dynamics 365 Finance</span></span>
<span data-ttu-id="5281f-145">Hvis Finance har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Kostnadskontroll**.</span><span class="sxs-lookup"><span data-stu-id="5281f-145">If Finance has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="5281f-146">Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="5281f-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="5281f-147">Forutsetninger hvis du bruker versjon 1611 med Platform update 3 eller nyere</span><span class="sxs-lookup"><span data-stu-id="5281f-147">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="5281f-148">Hvis versjon 1611 med Platform update 3 eller nyere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="5281f-148">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5281f-149">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="5281f-149">Prerequisite</span></span></th>
<th><span data-ttu-id="5281f-150">Rolle</span><span class="sxs-lookup"><span data-stu-id="5281f-150">Role</span></span></th>
<th><span data-ttu-id="5281f-151">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5281f-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5281f-152">Implementere KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="5281f-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="5281f-153">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="5281f-153">System administrator</span></span></td>

<td><span data-ttu-id="5281f-154">KB 4013633 er en X++-oppdatering eller hurtigreparasjon for metadata som inneholder det mobile arbeidsområdet <strong>Kostnadskontroll</strong>.</span><span class="sxs-lookup"><span data-stu-id="5281f-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="5281f-155">Systemadministrator må følge trinnene nedenfor for å implementere KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="5281f-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="5281f-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="5281f-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="5281f-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="5281f-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="5281f-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</span><span class="sxs-lookup"><span data-stu-id="5281f-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="5281f-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</span><span class="sxs-lookup"><span data-stu-id="5281f-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5281f-160">Publiser det mobile arbeidsområdet <strong>Kostnadskontroll</strong>.</span><span class="sxs-lookup"><span data-stu-id="5281f-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="5281f-161">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="5281f-161">System administrator</span></span></td>
<td><span data-ttu-id="5281f-162">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="5281f-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="5281f-163">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="5281f-163">Download and install the mobile app</span></span>
<span data-ttu-id="5281f-164">Laste ned og installere Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="5281f-164">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="5281f-165">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="5281f-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="5281f-166">For iPhone</span><span class="sxs-lookup"><span data-stu-id="5281f-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="5281f-167">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="5281f-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="5281f-168">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5281f-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="5281f-169">Skriv inn URL-adressen for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5281f-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="5281f-170">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="5281f-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="5281f-171">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="5281f-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="5281f-172">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="5281f-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="5281f-173">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="5281f-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="5281f-174">[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="5281f-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="5281f-175">Vise ytelsen til kostsenteret ved hjelp av det mobile arbeidsområdet for kostnadskontroll</span><span class="sxs-lookup"><span data-stu-id="5281f-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="5281f-176">Velg **Kostnadskontroll**-arbeidsområdet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5281f-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="5281f-177">Velg **Kostnadsobjektobjekt**.</span><span class="sxs-lookup"><span data-stu-id="5281f-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="5281f-178">Velg **Handlinger**.</span><span class="sxs-lookup"><span data-stu-id="5281f-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="5281f-179">Klikk **Velg konfigurasjon** for å velge et kostnadskontrolloppsett.</span><span class="sxs-lookup"><span data-stu-id="5281f-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="5281f-180">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="5281f-180">Select **Done**.</span></span>
6.  <span data-ttu-id="5281f-181">Velg **Handlinger**.</span><span class="sxs-lookup"><span data-stu-id="5281f-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="5281f-182">Klikk **Velg kostnadsobjekt** for å velge kostsentrene du har fått tilgang til.</span><span class="sxs-lookup"><span data-stu-id="5281f-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="5281f-183">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="5281f-183">Select **Done**.</span></span>
9.  <span data-ttu-id="5281f-184">Vis den totale ytelsen til kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="5281f-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="5281f-185">Velg koblingen **Detaljer for gjeldende periode**.</span><span class="sxs-lookup"><span data-stu-id="5281f-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="5281f-186">Vise ytelsen til individuelle kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="5281f-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="5281f-187">Du kan også søke etter bestemte kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="5281f-187">You can also search for specific cost elements.</span></span>

