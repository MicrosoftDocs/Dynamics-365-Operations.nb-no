---
title: Mobilt arbeidsområde for fakturagodkjenning
description: Dette emnet gir informasjon om det mobile arbeidsområdet for fakturagodkjenning.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3d90b89900b35bce648841aa9e49737a25309ce2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570082"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="b5bb4-103">Mobilt arbeidsområde for fakturagodkjenning</span><span class="sxs-lookup"><span data-stu-id="b5bb4-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5bb4-104">Dette emnet gir informasjon om det mobile arbeidsområdet **Fakturagodkjenning**.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="b5bb4-105">Dette arbeidsområdet gir en liste over fakturaer som er tilordnet til deg gjennom arbeidsflytprosessen leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="b5bb4-106">Dette mobile arbeidsområdet er ment å brukes sammen med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="b5bb4-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b5bb4-107">Overview</span></span>

<span data-ttu-id="b5bb4-108">Med det mobilie arbeidsområdet **Fakturagodkjenninger**  kan regnskapsassistenter og -sjefer vise fakturaene som er tilordnet til dem, som en del av arbeidsflytprosessen leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="b5bb4-109">Du kan vise fakturainformasjon, og til og med linje- og distribusjonsdetaljer, som hjelper deg å ta informerte beslutninger om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="b5bb4-110">Fra arbeidsområdet kan du utføre handlinger for å flytte fakturaen gjennom arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b5bb4-111">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="b5bb4-111">Prerequisites</span></span>

<span data-ttu-id="b5bb4-112">Før du kan bruke dette mobile arbeidsområdet, må du oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b5bb4-113">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="b5bb4-113">Prerequisite</span></span></th>
<th><span data-ttu-id="b5bb4-114">Rolle</span><span class="sxs-lookup"><span data-stu-id="b5bb4-114">Role</span></span></th>
<th><span data-ttu-id="b5bb4-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b5bb4-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5bb4-116">Microsoft Dynamics 365 Finance må distribueres i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="b5bb4-117">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="b5bb4-117">System administrator</span></span></td>
<td><span data-ttu-id="b5bb4-118">Se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5bb4-119">Det mobile arbeidsområdet <strong>Fakturagodkjenning</strong> må publiseres.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="b5bb4-120">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="b5bb4-120">System administrator</span></span></td>
<td><span data-ttu-id="b5bb4-121">Se <a href="publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="b5bb4-122">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="b5bb4-122">Download and install the mobile app</span></span>

<span data-ttu-id="b5bb4-123">Laste ned og installere Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="b5bb4-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="b5bb4-124">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="b5bb4-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="b5bb4-125">For iPhone</span><span class="sxs-lookup"><span data-stu-id="b5bb4-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="b5bb4-126">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="b5bb4-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="b5bb4-127">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="b5bb4-128">Angi URL-adressen for Microsoft Dynamics365.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="b5bb4-129">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="b5bb4-130">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="b5bb4-131">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="b5bb4-132">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="b5bb4-133">[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="b5bb4-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="b5bb4-134">Godkjenne fakturaer ved hjelp av det mobile arbeidsrområdet Fakturagodkjenning</span><span class="sxs-lookup"><span data-stu-id="b5bb4-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="b5bb4-135">Velg **Fakturagodkjenning**-arbeidsområdet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="b5bb4-136">Velg fakturaen som er tilordnet til deg av arbeidsflytprosessen leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="b5bb4-137">På siden **Fakturaopplysninger** kan du se gjennom fakturahodeinformasjonen, for eksempel leverandør- og datoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="b5bb4-138">Velg en linje på fakturaen for å vise mer detaljert informasjon om den i  **fakturalinjedetaljer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="b5bb4-139">I visningen **Fakturalinjedetaljer** velger du **Distribusjoner** for å vise linjedistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="b5bb4-140">Her kan du vise regnskapet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="b5bb4-141">Informasjonen som vises, inkluderer finansdimensjonene og hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="b5bb4-142">På siden **Fakturadetaljer** velger du **Distribusjoner** for å vise alle distribusjonene.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="b5bb4-143">Her kan du vise regnskapet for hele fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="b5bb4-144">Informasjonen som vises, inkluderer finansdimensjonene og hovedkontoene.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="b5bb4-145">Velg **Vedlegg** for å vise notater eller filer som er knyttet til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="b5bb4-146">På siden **Fakturadetaljer** velger du riktig handling i arbeidsflyten forl å fullføre gjennomgangen.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="b5bb4-147">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="b5bb4-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]