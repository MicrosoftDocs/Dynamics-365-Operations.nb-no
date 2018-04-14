---
title: "Kjøpsordregodkjenning mobilt arbeidsområde"
description: "Dette emnet gir informasjon om Kjøpsordregodkjenning mobilt arbeidsområde, som lar deg vise bestillinger og svare på dem gjennom handlinger. Du kan for eksempel godkjenne eller avvise en bestilling."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 96d92016a4634291c5d519a2935992b3a50b65dd
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="67347-104">Kjøpsordregodkjenning mobilt arbeidsområde</span><span class="sxs-lookup"><span data-stu-id="67347-104">Purchase order approval mobile workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

<span data-ttu-id="67347-105">Dette emnet gir informasjon om det mobile arbeidsområdet **Godkjenning av bestilling**.</span><span class="sxs-lookup"><span data-stu-id="67347-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="67347-106">I dette arbeidsområdet kan du vise bestillinger og svare på dem gjennom handlinger.</span><span class="sxs-lookup"><span data-stu-id="67347-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="67347-107">Du kan for eksempel godkjenne eller avvise en bestilling.</span><span class="sxs-lookup"><span data-stu-id="67347-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="67347-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="67347-108">Overview</span></span> 
<span data-ttu-id="67347-109">Bestillinger som krever godkjenning, går gjennom en godkjenningsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="67347-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="67347-110">Arbeidsflyten kan inkludere ulike trinn som krever at en eller flere personer utfører en handling.</span><span class="sxs-lookup"><span data-stu-id="67347-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="67347-111">For eksempel kan en person måtte fullføre en oppgave eller godkjenne bestillingen.</span><span class="sxs-lookup"><span data-stu-id="67347-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="67347-112">På det mobile arbeidsområdet **Godkjenning av bestilling** kan du lett vise og svare på bestillinger fra en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="67347-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="67347-113">På dette arbeidsområdet kan du også utføre de samme handlingene i arbeidsflyten som du kan utføre fra Microsoft Dynamics 365 Finance and Operations, webklient.</span><span class="sxs-lookup"><span data-stu-id="67347-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="67347-114">Nødvendig programvare</span><span class="sxs-lookup"><span data-stu-id="67347-114">Prerequisites</span></span>
<span data-ttu-id="67347-115">Forutsetningene varierer avhengig av hvilken versjon av Finance and Operations som er distribuert i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="67347-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="67347-116">Forutsetninger hvis du bruker Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="67347-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span> 
<span data-ttu-id="67347-117">Hvis Microsoft Dynamics 365 for Finance and Operations har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Godkjenning av bestilling**.</span><span class="sxs-lookup"><span data-stu-id="67347-117">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="67347-118">Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="67347-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="67347-119">Forutsetninger hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere</span><span class="sxs-lookup"><span data-stu-id="67347-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="67347-120">Hvis Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="67347-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="67347-121">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="67347-121">Prerequisite</span></span></th>
<th><span data-ttu-id="67347-122">Rolle</span><span class="sxs-lookup"><span data-stu-id="67347-122">Role</span></span></th>
<th><span data-ttu-id="67347-123">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="67347-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67347-124">Implementer KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="67347-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="67347-125">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="67347-125">System administrator</span></span></td>
<td><span data-ttu-id="67347-126">KB 4017918 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>Godkjenning av bestilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="67347-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="67347-127">Systemadministrator må følge trinnene nedenfor for å implementere KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="67347-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="67347-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="67347-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="67347-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="67347-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="67347-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</span><span class="sxs-lookup"><span data-stu-id="67347-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="67347-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</span><span class="sxs-lookup"><span data-stu-id="67347-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67347-132">Publiser det mobile arbeidsområdet <strong>Godkjenning av bestilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="67347-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="67347-133">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="67347-133">System administrator</span></span></td>
<td><span data-ttu-id="67347-134">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="67347-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="67347-135">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="67347-135">Download and install the mobile app</span></span>
<span data-ttu-id="67347-136">Last ned og installer mobilappen Microsoft Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="67347-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="67347-137">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="67347-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="67347-138">For iPhone</span><span class="sxs-lookup"><span data-stu-id="67347-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="67347-139">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="67347-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="67347-140">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="67347-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="67347-141">Skriv inn URL-adressen til Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="67347-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="67347-142">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="67347-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="67347-143">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="67347-143">Enter your credentials.</span></span>
4. <span data-ttu-id="67347-144">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="67347-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="67347-145">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="67347-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Arbeidsområdet Godkjenning av bestilling i listen over tilgjengelige arbeidsområder](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="67347-147">Vis bestillinger som er tilordnet til deg</span><span class="sxs-lookup"><span data-stu-id="67347-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="67347-148">Velg arbeidsområdet **Godkjenning av bestilling** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="67347-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="67347-149">Velg **Ordrer tilordnet til meg** for å vise alle bestillingene som du har blitt bedt om å utføre handlinger for i arbeidsflyten for godkjenning av bestilling.</span><span class="sxs-lookup"><span data-stu-id="67347-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="67347-150">Velg en ordre.</span><span class="sxs-lookup"><span data-stu-id="67347-150">Select an order.</span></span> <span data-ttu-id="67347-151">På **Ordredetaljer**-siden vises ordrehodeinformasjon og -linjer.</span><span class="sxs-lookup"><span data-stu-id="67347-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="67347-152">Du kan også finne retningslinjer fra arbeidsflytoppgaven.</span><span class="sxs-lookup"><span data-stu-id="67347-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="67347-153">Velg **Regnskapsdistribusjoner** for å åpne siden **Hoderegnskapsdistribusjoner**.</span><span class="sxs-lookup"><span data-stu-id="67347-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="67347-154">Gå tilbake til **Ordredetaljer**-siden, og velg en linje.</span><span class="sxs-lookup"><span data-stu-id="67347-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="67347-155">Du kan også utforske de linjespesifikke regnskapsdistribusjonene fra ordrelinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="67347-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="67347-156">Fullfør en handling på bestillingen</span><span class="sxs-lookup"><span data-stu-id="67347-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="67347-157">Når du har vist bestillingen som er tilordnet til deg og lest instruksjonene for arbeidsflyten, bør du være klar til å utføre handlinger.</span><span class="sxs-lookup"><span data-stu-id="67347-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="67347-158">Velg arbeidsområdet **Godkjenning av bestilling** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="67347-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="67347-159">Velg **Ordrer tilordnet til meg** for å vise alle bestillingene som du har blitt bedt om å utføre handlinger for i arbeidsflyten for godkjenning av bestilling.</span><span class="sxs-lookup"><span data-stu-id="67347-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="67347-160">Velg en ordre, og vis detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="67347-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="67347-161">Velg **Handlinger** for å vise de tilgjengelige handlingene.</span><span class="sxs-lookup"><span data-stu-id="67347-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="67347-162">Handlingene som er tilgjengelige, avhenger av oppgaven som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="67347-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="67347-163">Oppgavehandling</span><span class="sxs-lookup"><span data-stu-id="67347-163">Task action</span></span>    | <span data-ttu-id="67347-164">Godkjenningshandling</span><span class="sxs-lookup"><span data-stu-id="67347-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="67347-165">Komplett</span><span class="sxs-lookup"><span data-stu-id="67347-165">Complete</span></span>       | <span data-ttu-id="67347-166">Godkjenn</span><span class="sxs-lookup"><span data-stu-id="67347-166">Approve</span></span>          |
    | <span data-ttu-id="67347-167">Retur</span><span class="sxs-lookup"><span data-stu-id="67347-167">Return</span></span>         | <span data-ttu-id="67347-168">Avvis</span><span class="sxs-lookup"><span data-stu-id="67347-168">Reject</span></span>           |
    | <span data-ttu-id="67347-169">Be om endring</span><span class="sxs-lookup"><span data-stu-id="67347-169">Request change</span></span> | <span data-ttu-id="67347-170">Be om endring</span><span class="sxs-lookup"><span data-stu-id="67347-170">Request change</span></span>   |
    | <span data-ttu-id="67347-171">Deleger</span><span class="sxs-lookup"><span data-stu-id="67347-171">Delegate</span></span>       | <span data-ttu-id="67347-172">Deleger</span><span class="sxs-lookup"><span data-stu-id="67347-172">Delegate</span></span>         |

5. <span data-ttu-id="67347-173">Velg riktig handling.</span><span class="sxs-lookup"><span data-stu-id="67347-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="67347-174">På **Fullfør oppgave**-siden skriver du inn en kommentar.</span><span class="sxs-lookup"><span data-stu-id="67347-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="67347-175">Legg merke til at hvis du velger **Deleger**-handlingen, må du velge en bruker delegere oppgaven til.</span><span class="sxs-lookup"><span data-stu-id="67347-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="67347-176">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="67347-176">Select **Done**.</span></span> <span data-ttu-id="67347-177">Når du har oppdatert arbeidsområdet, fjernes bestillingen fra listen.</span><span class="sxs-lookup"><span data-stu-id="67347-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

