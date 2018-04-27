---
title: Startside for mobilapp
description: "Dette emnet beskriver mobilappen Microsoft Dynamics 365 for enhetlig drift og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4736a7041c746350fa073bd58929c840f7689bf
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="d03e0-103">Startside for mobilapp</span><span class="sxs-lookup"><span data-stu-id="d03e0-103">Mobile app home page</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d03e0-104">Dette emnet beskriver mobilappen Microsoft Dynamics 365 for enhetlig drift og inneholder koblinger til ressursene som kan hjelpe deg med å implementere den i din organisasjon.</span><span class="sxs-lookup"><span data-stu-id="d03e0-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="d03e0-105">Mobilappen var tidligere kalt *Microsoft Dynamics 365 for Finance and operations*.</span><span class="sxs-lookup"><span data-stu-id="d03e0-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="d03e0-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d03e0-106">Overview</span></span>
--------

<span data-ttu-id="d03e0-107">Mobilappen lar organisasjoner gjøre sine forretningsprosesser tilgjengelige på mobilenheter.</span><span class="sxs-lookup"><span data-stu-id="d03e0-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="d03e0-108">Når IT-administrator har aktivert mobile arbeidsområder for organisasjonen, kan brukere logger på appen og umiddelbart begynne å kjøre forretningsprosesser fra mobilenhetene.</span><span class="sxs-lookup"><span data-stu-id="d03e0-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="d03e0-109">Mobilappen inneholder følgende funksjoner som kan hjelpe med å øke produktiviteten:</span><span class="sxs-lookup"><span data-stu-id="d03e0-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="d03e0-110">Brukere kan vise, redigere og behandle forretningsdata, selv om de har uregelmessige nettverkstilkobling eller mobilenhetene er helt frakoblet.</span><span class="sxs-lookup"><span data-stu-id="d03e0-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="d03e0-111">Når en enhet oppretter en nettverkstilkobling, synkroniseres automatisk frakoblede dataoperasjoner med Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d03e0-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="d03e0-112">IT-administratorer eller utviklere kan bygge og publisere mobile arbeidsområder som er skreddersydd til organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="d03e0-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="d03e0-113">Appen bruker dine eksisterende koderessurser.</span><span class="sxs-lookup"><span data-stu-id="d03e0-113">The app uses your existing code assets.</span></span> <span data-ttu-id="d03e0-114">Derfor trenger du ikke å implementere valideringsprosedyrene, forretningslogikken eller sikkerhetskonfigurasjonen på nytt.</span><span class="sxs-lookup"><span data-stu-id="d03e0-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="d03e0-115">IT-administratorer eller utviklere kan lett utforme mobile arbeidsområder ved hjelp av pek og klikk-arbeidsområdeutformingen som er inkludert i webklienten.</span><span class="sxs-lookup"><span data-stu-id="d03e0-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="d03e0-116">IT-administratorer eller utviklere kan også optimalisere frakoblet-funksjonene for arbeidsområder ved hjelp av utvidelsesrammeverket for forretningslogikk.</span><span class="sxs-lookup"><span data-stu-id="d03e0-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="d03e0-117">Fordi dataene fremdeles behandles når en enhet er frakoblet, forblir mobile scenarioer rike og jevne, selv om enheter ikke har konstant nettverkstilkobling.</span><span class="sxs-lookup"><span data-stu-id="d03e0-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="d03e0-118">Elementer i mobilappen</span><span class="sxs-lookup"><span data-stu-id="d03e0-118">Elements of the mobile app</span></span>
<span data-ttu-id="d03e0-119">Navigasjon i mobilappen består av fire grunnleggende begreper: instrumentbord, arbeidsområder, sider og handlinger.</span><span class="sxs-lookup"><span data-stu-id="d03e0-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="d03e0-120">[![Navigasjonsbegreper i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="d03e0-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="d03e0-121">Når du starter appen, går du til **instrumentbord**.</span><span class="sxs-lookup"><span data-stu-id="d03e0-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="d03e0-122">På instrumentbordet kan du se en liste over **arbeidsområder** som er publisert.</span><span class="sxs-lookup"><span data-stu-id="d03e0-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="d03e0-123">I hver arbeidsområdet kan du se en liste over **sider** som er tilgjengelige for arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="d03e0-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="d03e0-124">Når du er på en side, kan du utføre flere handlinger.</span><span class="sxs-lookup"><span data-stu-id="d03e0-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="d03e0-125">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="d03e0-125">Here are some examples:</span></span>

    - <span data-ttu-id="d03e0-126">Vis detaljerte data.</span><span class="sxs-lookup"><span data-stu-id="d03e0-126">View detailed data.</span></span>
    - <span data-ttu-id="d03e0-127">Naviger til andre sider for relaterte data, for eksempel enhetsdetaljer eller linjer.</span><span class="sxs-lookup"><span data-stu-id="d03e0-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="d03e0-128">Se en liste over **handlinger** som er tilgjengelige for denne siden.</span><span class="sxs-lookup"><span data-stu-id="d03e0-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="d03e0-129">Handlinger lar deg opprette eller redigere eksisterende data.</span><span class="sxs-lookup"><span data-stu-id="d03e0-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="d03e0-130">Implementeringsprosess</span><span class="sxs-lookup"><span data-stu-id="d03e0-130">Implementation process</span></span>
<span data-ttu-id="d03e0-131">Illustrasjonen nedenfor viser prosessen med implementing av både mobile arbeidsområder som leveres av Microsoft, og egendefinerte mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="d03e0-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Implementeringsprosess for mobilapper](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="d03e0-133">Tabellen nedenfor inneholder koblinger til ressurser som kan hjelpe deg med å implementere både mobile arbeidsområder som leveres av Microsoft, og egendefinerte mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="d03e0-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="d03e0-134">Tallene i den første kolonnen samsvarer med de nummererte trinnene i den forrige illustrasjonen.</span><span class="sxs-lookup"><span data-stu-id="d03e0-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03e0-135">Trinn</span><span class="sxs-lookup"><span data-stu-id="d03e0-135">Step</span></span></th>
<th><span data-ttu-id="d03e0-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="d03e0-136">Role</span></span></th>
<th><span data-ttu-id="d03e0-137">Handling</span><span class="sxs-lookup"><span data-stu-id="d03e0-137">Action</span></span></th>
<th><span data-ttu-id="d03e0-138">Ressurser som hjelper deg med å fullføre handlingen</span><span class="sxs-lookup"><span data-stu-id="d03e0-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d03e0-139">1</span><span class="sxs-lookup"><span data-stu-id="d03e0-139">1</span></span></td>
<td><span data-ttu-id="d03e0-140">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="d03e0-140">System administrator</span></span></td>
<td><span data-ttu-id="d03e0-141">Implementere Finance and Operations i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="d03e0-141">Implement Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="d03e0-142">Hvis du ennå ikke har distribuert en versjon av Microsoft Dynamics 365, kan du se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="d03e0-142">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="d03e0-143">Hvis du vil se en oversikt over mobile arbeidsområder som kan brukes, kan du se <a href="mobile-workspaces-released.md">Mobile arbeidsområder som nylig er utgitt</a>.</span><span class="sxs-lookup"><span data-stu-id="d03e0-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03e0-144">2</span><span class="sxs-lookup"><span data-stu-id="d03e0-144">2</span></span></td>
<td><span data-ttu-id="d03e0-145">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="d03e0-145">System administrator</span></span></td>
<td><span data-ttu-id="d03e0-146"><strong>Hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611:</strong> Last ned og installer KB-er som aktiverer de mobile arbeidsområdene som leveres av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d03e0-146"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="d03e0-147">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="d03e0-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="d03e0-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Mobile arbeidsområder for kostnadskontroll</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="d03e0-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobilt arbeidsområde for lagerbeholdning</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="d03e0-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobile arbeidsområder for salgsordrer</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="d03e0-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilt arbeidsområde for leverandørsamarbeid</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="d03e0-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Mobilt arbeidsområde for registrering av prosjekttid</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="d03e0-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Mobilt arbeidsområde for reiseregninger og utlegg</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03e0-154">3</span><span class="sxs-lookup"><span data-stu-id="d03e0-154">3</span></span></td>
<td><span data-ttu-id="d03e0-155">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="d03e0-155">System administrator</span></span></td>
<td><span data-ttu-id="d03e0-156">Publisere de mobile arbeidsområdene som leveres av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d03e0-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="d03e0-157"><a href="publish-mobile-workspace.md">Publisere mobile arbeidsområder</a>
</span><span class="sxs-lookup"><span data-stu-id="d03e0-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03e0-158">4</span><span class="sxs-lookup"><span data-stu-id="d03e0-158">4</span></span></td>
<td><span data-ttu-id="d03e0-159">Utvikler eller uavhengig programvareleverandør (ISV)</span><span class="sxs-lookup"><span data-stu-id="d03e0-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="d03e0-160">Bruk mobilplattformen til å opprette egendefinerte mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="d03e0-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="d03e0-161"><a href="platform/mobile-platform-home-page.md">Mobil plattform</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03e0-162">5</span><span class="sxs-lookup"><span data-stu-id="d03e0-162">5</span></span></td>
<td><span data-ttu-id="d03e0-163">ISV</span><span class="sxs-lookup"><span data-stu-id="d03e0-163">ISV</span></span></td>
<td><span data-ttu-id="d03e0-164">Opprett en distribuerbar pakke som inneholder egendefinerte mobile arbeidsområder, og laste opp pakken til Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d03e0-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="d03e0-165"><a href="../deployment/create-apply-deployable-package.md">Opprette en distribuerbar pakke</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03e0-166">6</span><span class="sxs-lookup"><span data-stu-id="d03e0-166">6</span></span></td>
<td><span data-ttu-id="d03e0-167">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="d03e0-167">System administrator</span></span></td>
<td><span data-ttu-id="d03e0-168">Bruk den distribuerbare pakken som inneholder de egendefinerte arbeidsområdene fra den uavhengige programvareleverandøren.</span><span class="sxs-lookup"><span data-stu-id="d03e0-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="d03e0-169"><a href="../deployment/apply-deployable-package-system.md">Bruke en distribuerbar pakke</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03e0-170">7</span><span class="sxs-lookup"><span data-stu-id="d03e0-170">7</span></span></td>
<td><span data-ttu-id="d03e0-171">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="d03e0-171">System administrator</span></span></td>
<td><span data-ttu-id="d03e0-172">Publisere de egendefinerte mobile arbeidsområdene som leveres av den uavhengige programvareleverandøren.</span><span class="sxs-lookup"><span data-stu-id="d03e0-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="d03e0-173"><a href="publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03e0-174">8</span><span class="sxs-lookup"><span data-stu-id="d03e0-174">8</span></span></td>
<td><span data-ttu-id="d03e0-175">Bruker</span><span class="sxs-lookup"><span data-stu-id="d03e0-175">User</span></span></td>
<td><span data-ttu-id="d03e0-176">Last ned og installer mobilappen.</span><span class="sxs-lookup"><span data-stu-id="d03e0-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="d03e0-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android-telefoner</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="d03e0-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhone</a></span><span class="sxs-lookup"><span data-stu-id="d03e0-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03e0-179">9</span><span class="sxs-lookup"><span data-stu-id="d03e0-179">9</span></span></td>
<td><span data-ttu-id="d03e0-180">Bruker</span><span class="sxs-lookup"><span data-stu-id="d03e0-180">User</span></span></td>
<td><span data-ttu-id="d03e0-181">Logg på og bruk mobilappen.</span><span class="sxs-lookup"><span data-stu-id="d03e0-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="d03e0-182">Appen inneholder de mobile arbeidsområdene som er publisert av systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="d03e0-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="d03e0-183">Hvis du vil se en oversikt over mobile arbeidsområder som Microsoft leverer, kan du se <a href="mobile-workspaces-released.md">Mobile arbeidsområder som nylig er utgitt</a>.</span><span class="sxs-lookup"><span data-stu-id="d03e0-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

