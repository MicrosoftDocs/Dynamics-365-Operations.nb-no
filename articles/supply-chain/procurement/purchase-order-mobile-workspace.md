---
title: Kjøpsordregodkjenning mobilt arbeidsområde
description: Dette emnet gir informasjon om Kjøpsordregodkjenning mobilt arbeidsområde, som lar deg vise bestillinger og svare på dem gjennom handlinger. Du kan for eksempel godkjenne eller avvise en bestilling.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 19ddd9eb34d5e5248f782aafc9ac9dee1b38dadb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825356"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="8a130-104">Kjøpsordregodkjenning mobilt arbeidsområde</span><span class="sxs-lookup"><span data-stu-id="8a130-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a130-105">Dette emnet gir informasjon om det mobile arbeidsområdet **Godkjenning av bestilling**.</span><span class="sxs-lookup"><span data-stu-id="8a130-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="8a130-106">I dette arbeidsområdet kan du vise bestillinger og svare på dem gjennom handlinger.</span><span class="sxs-lookup"><span data-stu-id="8a130-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="8a130-107">Du kan for eksempel godkjenne eller avvise en bestilling.</span><span class="sxs-lookup"><span data-stu-id="8a130-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="8a130-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="8a130-108">Overview</span></span> 
<span data-ttu-id="8a130-109">Bestillinger som krever godkjenning, går gjennom en godkjenningsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="8a130-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="8a130-110">Arbeidsflyten kan inkludere ulike trinn som krever at en eller flere personer utfører en handling.</span><span class="sxs-lookup"><span data-stu-id="8a130-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="8a130-111">For eksempel kan en person måtte fullføre en oppgave eller godkjenne bestillingen.</span><span class="sxs-lookup"><span data-stu-id="8a130-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="8a130-112">På det mobile arbeidsområdet **Godkjenning av bestilling** kan du lett vise og svare på bestillinger fra en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="8a130-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="8a130-113">På dette arbeidsområdet kan du også utføre de samme handlingene i arbeidsflyten som du kan utføre fra webklienten.</span><span class="sxs-lookup"><span data-stu-id="8a130-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8a130-114">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="8a130-114">Prerequisites</span></span>
<span data-ttu-id="8a130-115">Forutsetningene varierer avhengig av hvilken versjon av Supply Chain Management som er distribuert i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="8a130-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="8a130-116">Forutsetninger hvis du bruker Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8a130-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="8a130-117">Hvis Supply Chain Management har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Godkjenning av bestilling**.</span><span class="sxs-lookup"><span data-stu-id="8a130-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="8a130-118">Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="8a130-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="8a130-119">Forutsetninger hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere</span><span class="sxs-lookup"><span data-stu-id="8a130-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="8a130-120">Hvis Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="8a130-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8a130-121">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="8a130-121">Prerequisite</span></span></th>
<th><span data-ttu-id="8a130-122">Rolle</span><span class="sxs-lookup"><span data-stu-id="8a130-122">Role</span></span></th>
<th><span data-ttu-id="8a130-123">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8a130-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a130-124">Implementer KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="8a130-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="8a130-125">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="8a130-125">System administrator</span></span></td>
<td><span data-ttu-id="8a130-126">KB 4017918 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>Godkjenning av bestilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a130-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="8a130-127">Systemadministrator må følge trinnene nedenfor for å implementere KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="8a130-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="8a130-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="8a130-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="8a130-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="8a130-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="8a130-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</span><span class="sxs-lookup"><span data-stu-id="8a130-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="8a130-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</span><span class="sxs-lookup"><span data-stu-id="8a130-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a130-132">Publiser det mobile arbeidsområdet <strong>Godkjenning av bestilling</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a130-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="8a130-133">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="8a130-133">System administrator</span></span></td>
<td><span data-ttu-id="8a130-134">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="8a130-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="8a130-135">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="8a130-135">Download and install the mobile app</span></span>
<span data-ttu-id="8a130-136">Laste ned og installere Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="8a130-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="8a130-137">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="8a130-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="8a130-138">For iPhone</span><span class="sxs-lookup"><span data-stu-id="8a130-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="8a130-139">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="8a130-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="8a130-140">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="8a130-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="8a130-141">Angi URL-adressen for Microsoft Dynamics365.</span><span class="sxs-lookup"><span data-stu-id="8a130-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="8a130-142">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="8a130-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="8a130-143">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="8a130-143">Enter your credentials.</span></span>
4. <span data-ttu-id="8a130-144">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="8a130-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="8a130-145">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="8a130-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Arbeidsområdet Godkjenning av bestilling i listen over tilgjengelige arbeidsområder](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="8a130-147">Vis bestillinger som er tilordnet til deg</span><span class="sxs-lookup"><span data-stu-id="8a130-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="8a130-148">Velg arbeidsområdet **Godkjenning av bestilling** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="8a130-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="8a130-149">Velg **Ordrer tilordnet til meg** for å vise alle bestillingene som du har blitt bedt om å utføre handlinger for i arbeidsflyten for godkjenning av bestilling.</span><span class="sxs-lookup"><span data-stu-id="8a130-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="8a130-150">Velg en ordre.</span><span class="sxs-lookup"><span data-stu-id="8a130-150">Select an order.</span></span> <span data-ttu-id="8a130-151">På **Ordredetaljer**-siden vises ordrehodeinformasjon og -linjer.</span><span class="sxs-lookup"><span data-stu-id="8a130-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="8a130-152">Du kan også finne retningslinjer fra arbeidsflytoppgaven.</span><span class="sxs-lookup"><span data-stu-id="8a130-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="8a130-153">Velg **Regnskapsdistribusjoner** for å åpne siden **Hoderegnskapsdistribusjoner**.</span><span class="sxs-lookup"><span data-stu-id="8a130-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="8a130-154">Gå tilbake til **Ordredetaljer**-siden, og velg en linje.</span><span class="sxs-lookup"><span data-stu-id="8a130-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="8a130-155">Du kan også utforske de linjespesifikke regnskapsdistribusjonene fra ordrelinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="8a130-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="8a130-156">Fullfør en handling på bestillingen</span><span class="sxs-lookup"><span data-stu-id="8a130-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="8a130-157">Når du har vist bestillingen som er tilordnet til deg og lest instruksjonene for arbeidsflyten, bør du være klar til å utføre handlinger.</span><span class="sxs-lookup"><span data-stu-id="8a130-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="8a130-158">Velg arbeidsområdet **Godkjenning av bestilling** på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="8a130-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="8a130-159">Velg **Ordrer tilordnet til meg** for å vise alle bestillingene som du har blitt bedt om å utføre handlinger for i arbeidsflyten for godkjenning av bestilling.</span><span class="sxs-lookup"><span data-stu-id="8a130-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="8a130-160">Velg en ordre, og vis detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="8a130-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="8a130-161">Velg **Handlinger** for å vise de tilgjengelige handlingene.</span><span class="sxs-lookup"><span data-stu-id="8a130-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="8a130-162">Handlingene som er tilgjengelige, avhenger av oppgaven som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="8a130-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="8a130-163">Oppgavehandling</span><span class="sxs-lookup"><span data-stu-id="8a130-163">Task action</span></span>    | <span data-ttu-id="8a130-164">Godkjenningshandling</span><span class="sxs-lookup"><span data-stu-id="8a130-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="8a130-165">Komplett</span><span class="sxs-lookup"><span data-stu-id="8a130-165">Complete</span></span>       | <span data-ttu-id="8a130-166">Godkjenn</span><span class="sxs-lookup"><span data-stu-id="8a130-166">Approve</span></span>          |
    | <span data-ttu-id="8a130-167">Retur</span><span class="sxs-lookup"><span data-stu-id="8a130-167">Return</span></span>         | <span data-ttu-id="8a130-168">Avvis</span><span class="sxs-lookup"><span data-stu-id="8a130-168">Reject</span></span>           |
    | <span data-ttu-id="8a130-169">Be om endring</span><span class="sxs-lookup"><span data-stu-id="8a130-169">Request change</span></span> | <span data-ttu-id="8a130-170">Be om endring</span><span class="sxs-lookup"><span data-stu-id="8a130-170">Request change</span></span>   |
    | <span data-ttu-id="8a130-171">Deleger</span><span class="sxs-lookup"><span data-stu-id="8a130-171">Delegate</span></span>       | <span data-ttu-id="8a130-172">Deleger</span><span class="sxs-lookup"><span data-stu-id="8a130-172">Delegate</span></span>         |

5. <span data-ttu-id="8a130-173">Velg riktig handling.</span><span class="sxs-lookup"><span data-stu-id="8a130-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="8a130-174">På **Fullfør oppgave**-siden skriver du inn en kommentar.</span><span class="sxs-lookup"><span data-stu-id="8a130-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="8a130-175">Legg merke til at hvis du velger **Deleger**-handlingen, må du velge en bruker delegere oppgaven til.</span><span class="sxs-lookup"><span data-stu-id="8a130-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="8a130-176">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="8a130-176">Select **Done**.</span></span> <span data-ttu-id="8a130-177">Når du har oppdatert arbeidsområdet, fjernes bestillingen fra listen.</span><span class="sxs-lookup"><span data-stu-id="8a130-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]